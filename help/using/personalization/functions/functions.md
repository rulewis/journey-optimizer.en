---
title: Helper functions library
description: Journey Optimizer Helper functions library
---

# Templating language and helper functions {#functionsL}

![](../../assets/do-not-localize/badge.png)


## About templating language

Use Journey Optimizer templating language to perform operations on data, such as calculations, data formatting or conversions, conditions, and manipulate them in the context of personalization.

Available functions are listed in these pages:

* [Operators](operators.md)
* [Aggregation](aggregation.md)
* [Arrays and list](arrays-list.md)
* [Maths](maths.md)
* [Maps](maps.md)
* [Objects](objects.md)
* [String](string.md)

Templating language is leveraged in helper functions available in the expression editor personalization drop-down list. 

![](../assets/access-helper-functions.png)

They are grouped into three categories: [Functions](#functions-helper), [Helpers](#helper-helper) and [Operators](#operators-helper).

### Functions{#functions-helper}

**Array Functions**

|  |  |  |
| --------- | ----------- | ----------- |
| [Average](aggregation.md#average) | [In](arrays-list.md#in) | [Minimum](aggregation.md#minimum) (min) |
| [Count](aggregation.md#count) | [Includes](arrays-list.md#includes)  | [Not in](arrays-list.md#notin) (notIn) |
| [Distinct](arrays-list.md#distinct) | [Intersects](arrays-list.md#intersects) | [Subset of](arrays-list.md#subset) |
| [First item](arrays-list.md#head) (head) | [Last n in array](arrays-list.md#last-n) (lastN) | Sum |
| [First n in array](arrays-list.md#first-n) (topN)| [Maximum](aggregation.md#maximum) (max) | [Superset of](arrays-list.md#superset) |

* [Average](aggregation.md#average)
* [Count](aggregation.md#count)
* [Distinct](arrays-list.md#distinct)
* [First item](arrays-list.md#head) (head)
* [First n in array](arrays-list.md#first-n) (topN)
* [In](arrays-list.md#in)
* [Includes](arrays-list.md#includes) 
* [Intersects](arrays-list.md#intersects)
* [Last n in array](arrays-list.md#last-n) (lastN)
* [Maximum](aggregation.md#maximum) (max)
* [Minimum](aggregation.md#minimum) (min)
* [Not in](arrays-list.md#notin) (notIn)
* [Subset of](arrays-list.md#subset)
* Sum
* [Superset of](arrays-list.md#superset)

**Map Functions**

* [Get](maps.md#get)
* [Keys](maps.md#keys)
* [Values](maps.md#values)

**Object Functions**

* [Is not null](objects.md#isNotNull)
* [Is null](objects.md#isNull)

**String Functions**

* Camel Case
* Concat
* [Contains](string.md#contains)
* [Does not contain](string.md#doesNotContain)
* [Does not end with](string.md#doesNotEndWith)
* [Does not start with](string.md#doesNotStartWith)
* Encode64
* [Ends with](string.md#endsWith)
* [Equals](string.md#equals)
* EqualsIgnoreCase
* IsEmpty
* Length
* [Like](string.md#like)
* [Lower Case](#lower)
* [Matches](string.md#matches) 
* MD5
* [Not equal to](string.md#notEqualTo)
* [Regular expression group](string.md#regexGroup) (regexGroup)
* Replace
* ReplaceAll
* Split
* [Starts with](string.md#startsWith)
* Title Case
* Trim
* [Upper Case](#upper)

### Helpers{#helper-helper}

* [Each](../personalization-syntax.md#each)
* [if](../personalization-syntax.md#if)
* let
* [unless](../personalization-syntax.md#unless)
* [with](../personalization-syntax.md#with)

### Operators{#operators-helper}

These operators can only be used with numbers.

* [Addition](maths.md#add) (+) - This operator adds two numbers
* [And](operators.md#and) (and) - This operator creates a logical conjunction
* [Division](maths.md#divide) (/) - This operator is used to find the quotient of two numbers
* [Equals to](operators.md#and) (=) - This operation checks if values are equal
* [Greater than](operators.md#greaterthan) (>) - This operator checks if first value is greater than the second value
* [Greater or equals to](operators.md#greaterthanorequal) (>=) - This operator checks if first value is greater than or equal to the second value
* [Multiplication](maths.md#multiply) (*) - This operator multiplies two numbers
* [Negation](operators.md#not) (!) - This operator creates a logical negation
* [Not equals to](operators.md#notequal) (=!) - This operator checks if given expression not equal to give value
* [Or](operators.md#or) (or) - This operator creates a logical disjunction
* [Remainder](maths.md#remainder) (%) - This operator is used to calculate the remaindes after dividing two numbers
* Smaller than (<) - This operator checks if first value is less than the second value
* Smaller or equals to (<=) - This operator checks if first value is less than or equal to the second value
* [Substraction](maths.md#substract) (-) - This operator substracts two numbers

## Functions

### Lower Case{#lower}

The **lowerCase** function converts a string to lower case letters.

Syntax:

```sql
{%=lowerCase(string)%}
```

Example:

This function converts the profile first name to lower case letters.

```sql
{%=lowerCase(profile.person.name.firstName)%}
```

### Upper Case{#upper}

The **upper** function converts a string to lower case letters.

Syntax:

```sql
{%=upperCase(string)%}
```

Example:

This function converts the profile last name to upper case letters.

```sql
{%=upperCase(profile.person.name.lastName)%}
```
