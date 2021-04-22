---
title: CJM Functions library
description: CJM Functions library
audience: personalize content
content-type: reference
topic: personalization
---
# Operators {#operators}

![](../../assets/do-not-localize/badge.png)

## And

The `and` function is used to create a logical conjunction.

**Format**

```sql
{QUERY} and {QUERY}
```

**Example**

The following PQL query will return all people with home country as Canada and birth year of 1985.

```sql
homeAddress.countryISO = "CA" and person.birthYear = 1985
```

## Or

The `or` function is used to create a logical disjunction.

**Format**

```sql
{QUERY} or {QUERY}
```

**Example**

The following PQL query will return all people with home country as Canada or birth year of 1985.

```sql
homeAddress.countryISO = "CA" or person.birthYear = 1985
```

## Not

The `not` (or `!`) function is used to create a logical negation.

**Format**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following PQL query will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```

## If

The `if` function is used to resolve an expression depending on whether a specified condition is true.

**Format**

```sql
if ({TEST_EXPRESSION}, {TRUE_EXPRESSION}, {FALSE_EXPRESSION})
```

| Argument | Description |
| --------- | ----------- |
| `{TEST_EXPRESSION}` | The boolean expression which is being tested. |
| `{TRUE_EXPRESSION}` | The expression whose value will be used if `{TEST_EXPRESSION}` is true. |
| `{FALSE_EXPRESSION}` | The expression whose value will be used if `{TEST_EXPRESSION}` is false. |

**Example**

The following PQL query will set the value as `1` if the home country is Canada and `2` if the home country is not Canada.

```sql
if (homeAddress.countryISO = "CA", 1, 2)
```

## Equals

The `=` (equals) function checks whether one value or expression is equal to another value or expression.

**Format**

```sql
{EXPRESSION} = {VALUE}
```

**Example**

The following PQL query checks if the home address country is in Canada.

```sql
homeAddress.countryISO = "CA"
```

## Not equal

The `!=` (not equal) function checks whether one value or expression is **not** equal to another value or expression.

**Format**

```sql
{EXPRESSION} != {VALUE}
```

**Example**

The following PQL query checks if the home address country is not in Canada.

```sql
homeAddress.countryISO != "CA"
```

## Greater than

The `>` (greater than) function is used to check if the first value is greater than the second value.

**Format**

```sql
{EXPRESSION} > {EXPRESSION} 
```

**Example**

The following PQL query defines people whose birthdays do not fall in January or February.

```sql
person.birthMonth > 2
```

## Greater than or equal to

The `>=` (greater than or equal to) function is used to check if the first value is greater than or equal to the second value.

**Format**

```sql
{EXPRESSION} >= {EXPRESSION} 
```

**Example**

The following PQL query defines people whose birthdays do not fall in January or February.

```sql
person.birthMonth >= 3
```

## Less than

The `<` (less than) comparison function is used to check if the first value is less than the second value.

**Format**

```sql
{EXPRESSION} < {EXPRESSION} 
```

**Example**

The following PQL query defines people whose birthday is in January.

```sql
person.birthMonth < 2
```

## Less than or equal to

The `<=` (less than or equal to) comparison function is used to check if the first value is less than or equal to the second value.

**Format**

```sql
{EXPRESSION} <= {EXPRESSION} 
```

**Example**

The following PQL query defines people whose birthday is in January or February.

```sql
person.birthMonth <= 2
```

## Add

The `+` (addition) function is used to find the sum of two argument expressions.

**Format**

```sql
{NUMBER} + {NUMBER}
```

**Example**

The following PQL query sums the price of two different products.

```sql
product1.price + product2.price
```

## Multiply

The `*` (multiplication) function is used to find the product of two argument expressions.

**Format**

```sql
{NUMBER} * {NUMBER}
```

**Example**

The following PQL query finds the product of the inventory and the price of a product to find the gross value of the product.

```sql
product.inventory * product.price
```

## Subtract

The `-` (subtraction) function is used to find the difference of two argument expressions.

**Format**

```sql
{NUMBER} - {NUMBER}
```

**Example**

The following PQL query finds the difference in price between two different products.

```sql
product1.price - product2.price
```

## Divide

The `/` (division) function is used to find the quotient of two argument expressions.

**Format**

```sql
{NUMBER} / {NUMBER}
```

**Example**

The following PQL query finds the quotient between the total products sold and total money earned to see the average cost per item.

```sql
totalProduct.price / totalProduct.sold
```

## Remainder

The `%` (modulo/remainder) function is used to find the remainder after dividing the two argument expressions. 

**Format**

```sql
{NUMBER} % {NUMBER}
```

**Example**

The following PQL query checks if the person's age is divisible by five.

```sql
person.age % 5 = 0
```
