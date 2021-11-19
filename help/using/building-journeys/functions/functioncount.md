---
product: adobe campaign
title: count
description: Learn about the function count
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
---
# count {#count}

Counts the elements of the list not taking into account the null values.

## Category

Aggregation

## Function syntax

`count(<listAny>)`

## Parameters

| Parameter | Type             |
|-----------|------------------|
| List      | listString       |
| List      | listBoolean      |
| List      | listInteger      |
| List      | listDecimal      |
| List      | listDuration     |
| List      | listDateTime     |
| List      | listDateTimeOnly |
| List      | listDateOnly     |

## Signatures and returned type

`count(<listAny>)`

Returns an integer.

## Example

`count([10,2,10,null])`

Returns 3.
