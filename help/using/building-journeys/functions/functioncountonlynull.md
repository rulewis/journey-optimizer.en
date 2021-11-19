---
product: adobe campaign
title: countOnlyNull
description: Learn about the function countOnlyNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
---
# countOnlyNull {#countOnlyNull}

Counts the number of null values in the list.

## Category

Aggregation

## Function syntax

`countOnlyNull(<listAny>)`

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

## Signature and returned type

`countOnlyNull(<listAny>)`

Returns an integer.

## Example

`countOnlyNull([10,2,10,null])`

Returns 1.
