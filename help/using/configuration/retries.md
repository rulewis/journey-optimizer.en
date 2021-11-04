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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 05564a99-da50-4837-8dfb-bb1d3e0f1097
---
# Retries {#retries}

When an email message fails due to a temporary **Soft bounce** error, several retries are performed. Each error increments an error counter. When this counter reaches the limit threshold, the address is added to the suppression list.

>[!NOTE]
>
>Learn more on the types of errors in the [Delivery failure types](../suppression-list.md#delivery-failures) section.

In the default configuration, the threshold is set to 5 errors.

* For the same delivery, at the fifth encountered error within the [retry time period](#retry-duration), the address is suppressed.

* If there are different deliveries and two errors occur at least 24 hours apart, the error counter is incremented upon each error and the address is also suppressed at the fifth attempt.

If a delivery is successful after a retry, the error counter of the address is reinitialized.

In case the default value of 5 does not suit your needs, you can modify the error threshold following the steps below.

1. Go to **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Suppression list]**.

1. Select the **[!UICONTROL Edit suppression rules]** button.

    ![](../assets/suppression-list-edit-retries.png)

1. Edit the allowed number of consecutive soft bounces according to your needs.

    ![](../assets/suppression-list-edit-soft-bounces.png)

    You must enter an integer value between 1 and 20, meaning that the minimum number of retries is 1 and the maximum number is 20.

    >[!CAUTION]
    >
    >Any value higher than 10 may cause deliverability reputation issues, as well as IP throttling or blocklisting by ISPs. [Learn more on deliverability](../deliverability.md)

<!--![](../assets/retries-edition.png)-->

<!--The minimum delay between retries and the maximum number of retries to be performed are based on how well an IP is performing, both historically and currently, at a given domain.-->

## Retry time period {#retry-duration}

The **retry time period** is the timeframe in which any email message of the delivery that encountered a temporary error or soft bounce will be retried.

By default, retries will be performed for **3.5 days** (or **84 hours**) from the time the message was added to the email queue.

However, to ensure that retry attempts are not performed anymore when no longer needed, you can change this setting according to your needs when creating or editing a [message preset](message-presets.md) applying to the email channel.

For example, you may set the retry period to 24 hours for a transactional email relating to password reset and containing a link valid for only a day. Similarly, for a midnight sale, you may want to define a retry period of 6 hours.

>[!NOTE]
>
>The retry period cannot exceed 84 hours. The minimum retry period is 6 hours for marketing emails and 10 minutes for transactional emails.

Learn how to adjust the email retry parameters when creating a message preset in [this section](message-presets.md#create-message-preset).

<!--After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->

<!--Once a message has been in the retry queue for a maximum of 3.5 days and has failed to deliver, it will time out and its status will be updated to Failed??-->
