---
title: Retries before sending to the suppression list
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

# Retries before sending to the suppression list

When a message fails due to a soft bounce failure, several retries are performed before sending the email address to the suppression list. Each error increments an error counter. When this counter reaches the limit threshold, the address goes into the suppression list.

In the default configuration, the limit threshold number is set at 3 errors, meaning that the address is sent to the quaratine list at the third encountered error. If a delivery is successful after a retry, the error counter is reinitialized.

You can modify the limit threshold using the **[!UICONTROL Edit]** button.

![](../assets/retries-edition.png)
