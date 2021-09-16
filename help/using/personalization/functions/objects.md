---
title: Objects functions library
description: Objects functions library
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
---
# Object Functions {#objects}

## Is null{#isNull}

The `isNull` function determines if an object reference does not exist.

**Format**

```sql
{%= isNull(object) %}
```

**Example**

The following operation checks if the person's home address does not exist.

```sql
{%= isNull(person.homeAddress) %}
```

## Is not null{#isNotNull}

The `isNotNull` function determines if an object reference exists.

**Format**

```sql
{%= isNotNull(object) %}
```

**Example**

The following operation checks if the person's home address exists.

```sql
{%= isNotNull(person.homeAddress) %}
```
