---
title: Personalization syntax
description: 
audience: personalize content
content-type: reference
topic-tags: starting-with-personalization
---
# Personalization syntax {#personalization-syntax}

![](../assets/do-not-localize/badge.png)

## Introduction

The personalization in CJM is based on the templating syntax called Handlebars.
For a complete description of the Handlebars syntax, see [HandlebarsJS](https://handlebarsjs.com/).

It uses a template and an input object to generate HTML or other text formats. Handlebars templates look like regular text with embedded Handlebars expressions.

Simple expression sample:

```
{{profile.person.name}}
```

where:

* **profile** is a namespace.
* **person.name** is a token composed by attributes. The attributes structure is defined in an Adobe Experience Platform XDM Schema. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

## Syntax general rules

Identifiers may be any unicode character except for the following:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

The syntax is case sensitive.

The words **true**, **false**, **null** and **undefined** are only allowed in the first part of a path expression.

In Handlebars, the values returned by the {{expression}} are **HTML-escaped**. If the expression contains &, then the returned HTML-escaped output is generated as &amp;. If you don't want Handlebars to escape a value, use the "triple-stash".

## Profile

This namespace allows you to reference all the attributes defined in the profile schema described in [Adobe Experience Platform Data Model (XDM) documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

The attributes need to be defined in the schema before being referenced in a Customer Journey Management personalization block.

All the references are validated against Profile Schema with a validation mechanism described [here](personalization-validation.md).

**Sample references:**

* ```{{profile.person.name.fullName}}```
* ```{{profile.person.name.firstName}}```
* ```{{profile.person.gender}}```
* ```{{profile.personalEmail.address}}```
* ```{{profile.mobilePhone.number}}```
* ```{{profile.homeAddress.city}}```
* ```{{profile.faxPhone.number}}```

**Determine email address extension**:

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
{%else if contains(profile.personalEmail.address, ".org")%}
<a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
{%else%}
<a href="https://www.adobe.com/users">Checkout our page</a>
{%/if%}
```

## Segments

To learn more about segmentation and segmentation service, refer to this [section](../segment/about-segments.md).

**Render different content based on segment membership**:

```
{%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
  Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
{%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
  Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
{%/if%}
```

**Determine if a profile is already a member**:

```
{%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
    You're a member!
{%else%}
    You should be a member! Sign up now!
{%/if%}
```

## Offers

This namespace allows you to reference existing offers decisions.
To reference an offer you need to declare a path with the different information that define an offer.

This path has the following structure:
0 - 'offers' : identifies the path expression belonging to offer namespace
1 - Type : determines the type of offer representation. Valid values are 'image', 'html' and 'text'
2 - Placement Id
3 - Activity Id
4 - Offer specific attributes. Depending on the offer type supported attributes can be used. For example for images `deliveryUrl`.

For more information on Decisions API, refer to this [page](https://experienceleague.corp.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#deliver-offers-using-the-decisions-api)

For more information on Offers Representation, refer to this [page](https://experienceleague.corp.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#accept-and-content-type-headers).

All the references are validated against Offers Schema with a validation mechanism described [here](personalization-validation.md).

**Sample references:**

* Location where the image is hosted:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl```

* Target URL when you click on the image:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl```

* Text content of the offer coming from the decisionning engine:

```offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```

* HTML content of the offer coming from the decisionning engine:

```offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content``` 


## Helpers

A Handlebars helper is a simple identifier that may be followed by parameters.
Each parameter is a Handlebars expression. These helpers can be accessed from any context in a template.

These block helpers are identified by a # preceeding the helper name and require a matching closing /, of the same name. 
Blocks are expressions that have a block opening ({{# }}) and closing ({{/}}).

### If

The **if** helper is used to define a conditional block.
If the expression evaluation returns true, the block is rendered otherwise it is skipped.

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Following the **if** helper, you can enter an **else** statement to specify a block of code to be executed, if the same condition is false.
The **else if** statement will specify a new condition to test if the first statement returns false.

**Render different store links based on conditional expressions**:

``` 
{%#if profile.homeAddress.countryCode = "FR"%}
  <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
{%else%}
  <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
{%/if%}
```

### Unless

**#unless** helper is used to define a conditional block. By opposition to the **#if** helper, if the expression evaluation returns false, the block is rendered.

**Render some content based on email address extension**:

```
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

### Each

The **each** helper is used to iterate over an array.
The syntax of the helper is ```{{#each ArrayName}}``` YourContent {{/each}} 
We can refer to the individual array items by using the keyword **this** inside the block. The index of the array’s element can be rendered by using {{@index}}. 

Example:

```
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

```
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Render a list of products that this user has in their cart**:

```
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

### With

The **#with** helper is used to change the evaluation token of template-part.

Example:

```
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

The **#with** helper is useful to define a shortcut variable too.

**Use with for aliasing long variable names to shorter ones**:

```
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```


## Limitations 

* The use of **xEvent** variable is not available in personalization expressions. Any reference to xEvent will result in validation failures.
