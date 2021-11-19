---
product: adobe campaign
title: matchRegExp
description: Learn about the function matchRegExp
feature: Journeys
role: Data Engineer
level: Experienced
---
# matchRegExp {#matchRegExp}

Returns true if the string in the first parameter matches the regular expression in the second parameter. For more information, see [this page](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Category

String

## Function syntax

`matchRegExp(<parameters>)`

## Parameters

|Parameter|Type|
|--- |--- |
|string|string|
|regexp|string|

## Signature and returned type

`matchRegExp(<string>,<string>)`

Returns a boolean.

## Example

`matchRegExp("username@adobe.com", "*adobe")`

Returns true.
