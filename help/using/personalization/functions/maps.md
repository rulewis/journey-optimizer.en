---
title: CJM Functions library
description: CJM Functions library
audience: personalize content
content-type: reference
topic: personalization
---
# Maps Functions {#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) offers functions to make interaction with maps easier. 

## Get

The `get` function is used to retrieve the value of a map for a given key.

**Format**

```sql
get({MAP},{STRING})
```

**Example**

The following PQL query gets the value of the identity map for the key `example@example.com`.

```sql
get(identityMap,"example@example.com")
```

## Keys

The `keys` function is used to retrieve all the keys for a given map.

**Format**

```sql
keys({MAP})
```

**Example**

The following PQL query gets all the keys for the map `identityMap`.

```sql
keys(identityMap)
```

## Values

The `values` function is used to retrieve all the values of a given map.

**Format**

```sql
values({MAP})
```

**Example**

The following PQL query gets all the values for the map `identityMap`.

```sql
values(identityMap)
```
