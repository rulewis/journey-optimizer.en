---
title: Functions library
description: Functions library
---
# Operators {#operators}

![](../../assets/do-not-localize/badge.png)

## And{#and}

The `and` function is used to create a logical conjunction.

**Format**

```sql
{QUERY} and {QUERY}
```

**Example**

The following operation will return all people with home country as Canada and birth year of 1985.

```sql
homeAddress.countryISO = "CA" and person.birthYear = 1985
```

## Or{#or}

The `or` function is used to create a logical disjunction.

**Format**

```sql
{QUERY} or {QUERY}
```

**Example**

The following operation will return all people with home country as Canada or birth year of 1985.

```sql
homeAddress.countryISO = "CA" or person.birthYear = 1985
```

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

## If{#if}

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

The following operation will set the value as `1` if the home country is Canada and `2` if the home country is not Canada.

```sql
if (homeAddress.countryISO = "CA", 1, 2)
```

## Equals{#equals}

The `=` (equals) function checks whether one value or expression is equal to another value or expression.

**Format**

```sql
{EXPRESSION} = {VALUE}
```

**Example**

The following operation checks if the home address country is in Canada.

```sql
homeAddress.countryISO = "CA"
```

## Not equal{#notequal}

The `!=` (not equal) function checks whether one value or expression is **not** equal to another value or expression.

**Format**

```sql
{EXPRESSION} != {VALUE}
```

**Example**

The following operation checks if the home address country is not in Canada.

```sql
homeAddress.countryISO != "CA"
```

## Greater than{#greaterthan}

The `>` (greater than) function is used to check if the first value is greater than the second value.

**Format**

```sql
{EXPRESSION} > {EXPRESSION} 
```

**Example**

The following operation defines people whose birthdays do not fall in January or February.

```sql
person.birthMonth > 2
```

## Greater than or equal to{#greaterthanorequal}

The `>=` (greater than or equal to) function is used to check if the first value is greater than or equal to the second value.

**Format**

```sql
{EXPRESSION} >= {EXPRESSION} 
```

**Example**

The following operation defines people whose birthdays do not fall in January or February.

```sql
person.birthMonth >= 3
```

## Less than{#lessthan}

The `<` (less than) comparison function is used to check if the first value is less than the second value.

**Format**

```sql
{EXPRESSION} < {EXPRESSION} 
```

**Example**

The following operation defines people whose birthday is in January.

```sql
person.birthMonth < 2
```

## Less than or equal to{#lessthanorequal}

The `<=` (less than or equal to) comparison function is used to check if the first value is less than or equal to the second value.

**Format**

```sql
{EXPRESSION} <= {EXPRESSION} 
```

**Example**

The following operation defines people whose birthday is in January or February.

```sql
person.birthMonth <= 2
```

## Add{#add}

The `+` (addition) function is used to find the sum of two argument expressions.

**Format**

```sql
{NUMBER} + {NUMBER}
```

**Example**

The following operation sums the price of two different products.

```sql
product1.price + product2.price
```

## Multiply{#multiply}

The `*` (multiplication) function is used to find the product of two argument expressions.

**Format**

```sql
{NUMBER} * {NUMBER}
```

**Example**

The following operation finds the product of the inventory and the price of a product to find the gross value of the product.

```sql
product.inventory * product.price
```

## Subtract{#substract}

The `-` (subtraction) function is used to find the difference of two argument expressions.

**Format**

```sql
{NUMBER} - {NUMBER}
```

**Example**

The following operation finds the difference in price between two different products.

```sql
product1.price - product2.price
```

## Divide{#divide}

The `/` (division) function is used to find the quotient of two argument expressions.

**Format**

```sql
{NUMBER} / {NUMBER}
```

**Example**

The following operation finds the quotient between the total products sold and total money earned to see the average cost per item.

```sql
totalProduct.price / totalProduct.sold
```

## Remainder{#remainder}

The `%` (modulo/remainder) function is used to find the remainder after dividing the two argument expressions. 

**Format**

```sql
{NUMBER} % {NUMBER}
```

**Example**

The following operation checks if the person's age is divisible by five.

```sql
person.age % 5 = 0
```
