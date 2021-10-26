---
title: notEqualIgnoreCase
description: Learn about the function notEqualIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
---
# notEqualIgnoreCase {#notEqualIgnoreCase}

Check if the first argument string with the second argument string are different, ignoring case considerations.

## Category

String

## Function syntax

`notEqualIgnoreCase(<parameters>)`

## Parameters

* string

## Signature and returned type

`notEqualIgnoreCase(<string>,<string>)`

Returns a boolean.

## Example

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
