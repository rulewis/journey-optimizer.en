---
title: Functions library
description: Functions library
---
# Operators {#operators}

![](../../assets/do-not-localize/badge.png)

**Logical operators**

## And{#and}

The `and` function is used to create a logical conjunction.

**Format**

```sql
{%=query1 and query2%}
```

**Example**

The following operation will return all people with home country as France and birth year of 1985.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985%}
```

## Or{#or}

The `or` function is used to create a logical disjunction.

**Format**

```sql
{%=query1 or query2%}
```

**Example**

The following operation will return all people with home country as France or birth year of 1985.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985%}
```
<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Format**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

## If{#if}

The `if` function is used to resolve an expression depending on whether a specified condition is true.

**Format**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**Example**

The following operation will add a link to the 'www.adobe.com/academia' website for profiles with '.edu' email adresses only, to the 'www.adobe.com/org' website for profiles with '.org' email addresses, and the default URL 'www.adobe.com/users' for all other profiles.

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
{%else if contains(profile.personalEmail.address, ".org")%}
<a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
{%else%}
<a href="https://www.adobe.com/users">Checkout our page</a>
{%/if%}
```

You will find other samples in [this section](personalization-syntax.md#perso-segments).

## Equals{#equals}

The `=` (equals) function checks whether one value or expression is equal to another value or expression.

**Format**

```sql
{%=expression = value%}
```

**Example**

The following operation checks if the home address country is France.

```sql
{%=profile.homeAddress.country = "France"%}
```

## Not equal{#notequal}

The `!=` (not equal) function checks whether one value or expression is **not** equal to another value or expression.

**Format**

```sql
{%=expression != value%}
```

**Example**

The following operation checks if the home address country is not France.

```sql
{%=profile.homeAddress.country != "France"%}
```

## Greater than{#greaterthan}

The `>` (greater than) function is used to check if the first value is greater than the second value.

**Format**

```sql
{%= expression1 > expression2}%}
```

**Example**

The following operation defines people born strictly after 1970.

```sql
{%= profile.person.birthYear > 1970%}
```

## Greater than or equal to{#greaterthanorequal}

The `>=` (greater than or equal to) function is used to check if the first value is greater than or equal to the second value.

**Format**

```sql
{%= expression1 >= expression2}%}
```

**Example**

The following operation defines people born in or after 1970.

```sql
{%= profile.person.birthYear >= 1970%}
```

## Less than{#lessthan}

The `<` (less than) comparison function is used to check if the first value is less than the second value.

**Format**

```sql
{%= expression1 < expression2}%}
```

**Example**

The following operation defines people born before 2000.

```sql
{%= profile.person.birthYear < 2000%}
```

## Less than or equal to{#lessthanorequal}

The `<=` (less than or equal to) comparison function is used to check if the first value is less than or equal to the second value.

**Format**

```sql
{%= expression1 <= expression2}%}
```

**Example**

The following operation defines people born in 2000 or before.

```sql
{%= profile.person.birthYear <= 2000%}
```

**Operations with numbers**

## Add{#add}

The `+` (addition) function is used to find the sum of two argument expressions.

**Format**

```sql
{%={%= double + double}%}
```

**Example**

The following operation sums the price of two different products.

```sql
{%={%= product1.price + product2.price}%}
```

## Multiply{#multiply}

The `*` (multiplication) function is used to find the product of two argument expressions.

**Format**

```sql
{%={%= double * double}%}
```

**Example**

The following operation finds the product of the inventory and the price of a product to find the gross value of the product.

```sql
{%={%= product.inventory * product.price}%}
```

## Subtract{#substract}

The `-` (subtraction) function is used to find the difference of two argument expressions.

**Format**

```sql
{%={%= double - double}%}
```

**Example**

The following operation finds the difference in price between two different products.

```sql
{%={%= product1.price - product2.price}%}
```

## Divide{#divide}

The `/` (division) function is used to find the quotient of two argument expressions.

**Format**

```sql
{%={%= double / double}%}
```

**Example**

The following operation finds the quotient between the total products sold and total money earned to see the average cost per item.

```sql
{%={%= totalProduct.price / totalProduct.sold}%}
```

## Remainder{#remainder}

The `%` (modulo/remainder) function is used to find the remainder after dividing the two argument expressions. 

**Format**

```sql
{%={%= double % double}%}
```

**Example**

The following operation checks if the person's age is divisible by five.

```sql
{%={%= person.age % 5 = 0}%}
```
