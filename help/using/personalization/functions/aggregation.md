---
title: Functions library
description: Functions library
exl-id: 3c84411e-1318-406e-a693-8773b74b2fa1
---
# Aggregation Functions {#aggregation}

![](../../assets/do-not-localize/badge.png)

Aggregation functions are used to group together multiple values within [!DNL Profile Query Language] (PQL) arrays to form a single summary value.

## Count

The `count` function returns the number of elements within the given array.

**Format**

```sql
count({ARRAY})
```

**Example**

The following PQL query returns the number of orders in the array.

```sql
count(orders)
```

## Sum

The `sum` function returns the sum of all the selected values within the array.

**Format**

```sql
sum({ARRAY})
```

**Example**

The following PQL query returns the sum of all the orders' prices.

```sql
sum(orders.order.price)
```

## Average

The `average` function returns the arithmetic mean of all the selected values within the array.

**Format**

```sql
average({ARRAY})
```

**Example**

The following PQL query returns the average price of all the orders.

```sql
average(orders.order.price)
```

## Minimum

The `min` function returns the smallest of all the selected values within the array.

**Format**

```sql
min({ARRAY})
```

**Example**

The following PQL query returns the lowest price of all the orders.

```sql
min(orders.order.price)
```

## Maximum

The `max` function returns the largest of all the selected values within the array.

**Format**

```sql
max({ARRAY})
```

**Example**

The following PQL query returns the highest price of all the orders.

```sql
max(orders.order.price)
```
