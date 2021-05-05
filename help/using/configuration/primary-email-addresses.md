---
title: General message settings
description: Learn how to xxxx
page-status-flag: never-activated
uuid: 
contentOwner:
products:
audience: administrators
content-type: reference
topic-tags: 
discoiquuid:
internal: n
snippet: y
---

# Determine profiles' primary addresses

When you target a profile, several email addresses may be available in the database (personal, professional email address, etc.).

With Journey Optimizer, you can determine which email address to use from the profile service and prioritize when several addresses are available. To do this, follow these steps:

1. Access the Settings / General settings menu.
1. The Execution addresses field shows which field is currently used by default to determine the profiles' email addresses. Click the Edit button to change it.

![](../assets/primary-address.png)

1. Click the modify button to select the new field to use as primary email address.

![](../assets/primary-address-edit.png)

1. The list of all email address-type XDM fields displays. Select the field to use, then click Add.

    -SCREENSHOT-

!!no xdm fields available on stage

1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile.
