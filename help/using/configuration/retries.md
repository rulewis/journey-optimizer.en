---
title: Retries
description: Learn how retries are performed before sending an address to the suppression list
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

# Retries {#retries}

When a message fails due to a temporary **Soft bounce** or **Ignored** error, several retries are performed. Each error increments an error counter. When this counter reaches the limit threshold, the address is added to the suppression list.

In the default configuration<!--so can you edit this setting or not?? contradictory information was given-->, the threshold is set at three errors:

* For the same delivery, at the third encountered error, the address is suppressed.

* If there are different deliveries and two errors occur at least 24 hours apart, the error counter is incremented upon each error and the address is also suppressed at the third attempt.

If a delivery is successful after a retry, the error counter of the address is reinitialized.

You can modify the limit threshold using the **[!UICONTROL Edit]** button from the **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]** menu.<!--currently you can edit this in staging // now I see in UI: Suppression rule > Bounce days??? > 4-->

![](../assets/retries-edition.png)

## Retry duration {#retry-duration}

Retries will be performed for **3.5 days** from the time the message was added to the email queue.

The minimum delay between retries and the maximum number of retries to be performed are <!--managed by the Enhanced MTA,--> based on how well an IP is performing, both historically and currently at a given domain.

After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.