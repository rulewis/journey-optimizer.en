---
title: Functions library
description: Functions library
---
# Arrays and list functions {#arrays}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) offers functions to make interaction with arrays, lists, and strings easier.

## In{#in}

The `in` function is used to determine if an item is a member of an array or list.

**Format**

```sql
in ({VALUE},{ARRAY})
```

**Example**

The following operation defines people with birthdays in March, June, or September.

```sql
in (person.birthMonth, [3, 6, 9])
```

## Not in{#notin}

The `notIn` function is used to determine if an item is not a member of an array or list.

>[!NOTE]
>
>The `notIn` function *also* ensures that neither value is equal to null. Therefore, the results are not an exact negation of the `in` function.

**Format**

```sql
notIn ({VALUE},{ARRAY})
```

**Example**

The following operation defines people with birthdays that are not in March, June, or September.

```
{%=notIn(person.birthMonth ,[3, 6, 9])%}
```

## Intersects{#intersects}

The `intersects` function is used to determine if two arrays or lists have at least one common member.

**Format**

```sql
intersects({ARRAY},{ARRAY})
```

**Example**

The following operation defines people whose favorite colors include at least one of red, blue, or green.

```
{%=intersects(person.favoriteColors,["red", "blue", "green"])%}
```

<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Format**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
--> 
## Subset of{#subset}

The `subsetOf` function is used to determine if a specific array (array A) is a subset of another array (array B). In other words, that all elements in array A are elements of array B.

**Format**

```sql
subsetOf({ARRAY},{ARRAY})
```

**Example**

The following operation defines people who have visited all of their favorite cities.

```
{%=subsetOf(person.favoriteCities,person.visitedCities)%}
```

## Superset of{#superset}

The `supersetOf` function is used to determine if a specific array (array A) is a superset of another array (array B). In other words, that array A contains all elements in array B.

**Format**

```sql
supersetOf({ARRAY},{ARRAY})
```

**Example**

The following operation defines people who have eaten sushi and pizza at least once.

```
{%=supersetOf(person.eatenFoods,["sushi", "pizza"]%}
```

## Includes{#includes}

The `includes` function is used to determine if an array or list contains a given item.

**Format**

```sql
includes({ARRAY},{ITEM})
```

**Example**

The following operation defines people whose favorite color includes red.

```
{%=includes(person.favoriteColors,"red")%}
```

## Distinct{#distinct}

The `distinct` function is used to remove duplicate values from an array or list.

**Format**

```sql
distinct({ARRAY})
```

**Example**

The following operation specifies people who have placed orders in more than one store.

```
{%=distinct(person.orders.storeId).count() > 1%}
```

## First `n` in array {#first-n}

The `topN` function is used to return the first `N` items in an array, when sorted in ascending order based on the given numerical expression.

**Format**

```sql
topN({ARRAY},{VALUE}, {AMOUNT})
```

| Argument | Description |
| --------- | ----------- |
| `{ARRAY}` | The array or list that is to be sorted. |
| `{VALUE}` | The property in which to sort the array or list. |
| `{AMOUNT}` | The number of items to be returned. |

**Example**

The following operation returns the top five orders with the highest price.

```
{%=topN(orders,price, 5)%}
```

## Last `n` in array{#last-n}

The `bottomN` function is used to return the last `N` items in an array, when sorted in ascending order based on the given numerical expression.

**Format**

```sql
bottomN({ARRAY},{VALUE}, {AMOUNT})
```

| Argument | Description |
| --------- | ----------- | 
| `{ARRAY}` | The array or list that is to be sorted. |
| `{VALUE}` | The property in which to sort the array or list. |
| `{AMOUNT}` | The number of items to be returned. |

**Example**

The following operation returns the top five orders with the lowest price.

```
{%=bottomN(orders,price, 5)%
```

## First item{#head}

The `head` function is used to return the first item in the array or list.

**Format**

```sql
head({ARRAY})
```

**Example**

The following operation returns the first of the top five orders with the highest price. More information about the `topN` function can be found in the [first `n` in array](#first-n) section.

```
{%=head(topN(orders,price, 5))%}
```
