---
title: CJM Functions library
description: CJM Functions library
audience: personalize content
content-type: reference
topic: personalization
---
# Maths Functions {#math}

![](../../assets/do-not-localize/badge.png)

Arithmetic functions are used to perform basic calculations on values in [!DNL Profile Query Language] (PQL).

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
