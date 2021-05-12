---
title: Functions library
description: Functions library
---
# Object Functions {#objects}

![](../../assets/do-not-localize/badge.png)

## Is null{#isNull}

The `isNull` function determines if an object reference does not exist.

**Format**

```sql
{%={%= isNull(object)}%}
```

**Example**

The following operation checks if the person's home address does not exist.

```sql
{%={%= isNull(person.homeAddress)}%}
```

## Is not null{#isNotNull}

The `isNotNull` function determines if an object reference exists.

**Format**

```sql
{%={%= isNotNull(object)}%}
```

**Example**

The following operation checks if the person's home address exists.

```sql
{%={%= isNotNull(person.homeAddress)}%}
```
