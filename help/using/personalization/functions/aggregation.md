---
title: Functions library
description: Functions library
---
# Aggregation Functions {#aggregation}

Aggregation functions are used to group together multiple values to form a single summary value.

## Count{#count}

The `count` function returns the number of elements within the given array.

**Format**

```sql
{%= count(array) %}
```

**Example**

The following operation returns the number of orders in the array.

```sql
{%= count(orders) %}
```

## Sum{#sum}

The `sum` function returns the sum of all the selected values within the array.

**Format**

```sql
{%= sum(array) %}
```

**Example**

The following operation returns the sum of all the orders' prices.

```sql
{%=sum(orders.order.price)%}
```

## Average{#average}

The `average` function returns the arithmetic mean of all the selected values within the array.

**Format**

```sql
{%= average(array) %}
```

**Example**

The following operation returns the average price of all the orders.

```sql
{%=average(orders.order.price)%}
```

## Minimum{#min}

The `min` function returns the smallest of all the selected values within the array.

**Format**

```sql
{%= min(array) %}
```

**Example**

The following operation returns the lowest price of all the orders.

```sql
{%=min(orders.order.price)%}
```

## Maximum{#max}

The `max` function returns the largest of all the selected values within the array.

**Format**

```sql
{%= max(array) %}
```

**Example**

The following operation returns the highest price of all the orders.

```sql
{%=max(orders.order.price)%}
```
