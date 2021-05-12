---
title: Functions library
description: Functions library
---
# Maps Functions{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) offers functions to make interaction with maps easier. 

## Get{#get}

The `get` function is used to retrieve the value of a map for a given key.

**Format**

```sql
get({MAP},{STRING})
```

**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
get(identityMap,"example@example.com")
```

## Keys{#keys}

The `keys` function is used to retrieve all the keys for a given map.

**Format**

```sql
keys({MAP})
```

**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
keys(identityMap)
```

## Values{#values}

The `values` function is used to retrieve all the values of a given map.

**Format**

```sql
values({MAP})
```

**Example**

The following operation gets all the values for the map `identityMap`.

```sql
values(identityMap)
```
