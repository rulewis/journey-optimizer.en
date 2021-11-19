---
product: adobe campaign
title: inLastHours
description: Learn about the function inLastHours
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
---
# inLastHours {#inLastHours}

Returns true if the given date time is between now and now - delta hours. 

## Category

Date

## Function syntax

`inLastHours(<dateTime>,<delta>)`

## Parameters

| Parameter | Type             |
|-----------|------------------|
| date time | dateTime    |
| delta   | integer     |

## Signatures and returned type

`inLastHours(<dateTime>,<integer>)`

Returns a boolean.

## Examples

`inLastHours(toDateTime('2019-12-12T01:11:00Z'), 4)`

Returns true.

`inLastHours(@{MyEvent.timestamp}, 4)`

Returns true.
