---
title: Suppression categories and reasons
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

# Suppression categories and reasons

When a message fails to be delivered to an email address, Journey Optimizer determines why the delivery failed and associates to it a suppression category.

The suppression category determines when the email address is sent to to the suppression list:

* Soft: Soft errors send an address to the suppression list once the error counter reaches the limit threshold (see -ref retries section-).
* Hard: The email address is immediately sent to the suppression list.
* Manual: xxxx. !! how are addresses manually sent to the suppression list?

Possible failure reasons and their associated category are as follows:

|Reason|Description|Suppression category|
|------|-----------|----|
|Mail box full| The mail box of the recipient is full and could not receive the message. |Soft|
|DNS failure| xxx |Soft|
|Invalid recipient| xxx |Hard|

    !! list to enrich 
