---
title: Functions library
description: Functions library
---
# Aggregation Functions {#aggregation}

![](../../assets/do-not-localize/badge.png)

Aggregation functions are used to group together multiple values within [!DNL Profile Query Language] (PQL) arrays to form a single summary value.

## Count{#count}

The `count` function returns the number of elements within the given array.

**Format**

```sql
count({ARRAY})
```

**Example**

The following operation returns the number of orders in the array.

```
{%=count(orders)%}
```

## Sum{#sum}

The `sum` function returns the sum of all the selected values within the array.

**Format**

```sql
sum({ARRAY})
```

**Example**

The following operation returns the sum of all the orders' prices.

```
{%=sum(orders.order.price)%}
```

## Average{#average}

The `average` function returns the arithmetic mean of all the selected values within the array.

**Format**

```sql
average({ARRAY})
```

**Example**

The following operation returns the average price of all the orders.

```
{%=average(orders.order.price)%}
```

## Minimum{#min}

The `min` function returns the smallest of all the selected values within the array.

**Format**

```sql
min({ARRAY})
```

**Example**

The following operation returns the lowest price of all the orders.

```
{%=min(orders.order.price)%}
```

## Maximum{#max}

The `max` function returns the largest of all the selected values within the array.

**Format**

```sql
max({ARRAY})
```

**Example**

The following operation returns the highest price of all the orders.

```
{%=max(orders.order.price)%}
```
