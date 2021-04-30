---
title: Functions library
description: Functions library
exl-id: 2a147c61-cd2e-4af4-bd02-5b88dece4abb
---
# Object Functions {#objects}

![](../../assets/do-not-localize/badge.png)

## Is null

The `isNull` function determines if an object reference does not exist.

**Format**

```sql
isNull({OBJECT})
```

**Example**

The following PQL query checks if the person's home address does not exist.

```sql
isNull(person.homeAddress)
```

## Is not null

The `isNotNull` function determines if an object reference exists.

**Format**

```sql
isNotNull({OBJECT})
```

**Example**

The following PQL query checks if the person's home address exists.

```sql
isNotNull(person.homeAddress)
```
