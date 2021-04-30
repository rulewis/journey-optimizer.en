---
title: Monitor message execution
description: Learn monitoring guidelines
exl-id: 1bb8a7ee-de17-4cf3-b72e-f84b5ceee0d1
---
# Message monitoring {#monitor-message-execution}

![](assets/do-not-localize/badge.png)

To make sure your messages are successfully executed, sent and delivered, [!DNL Journey Optimizer] offers capabilities to monitor the messages that are currently published and triggered. You can see how your messages are performing across journeys <!--and APIs--> in real-time from the **[!UICONTROL Executions]** list.

To access this list, from the **[!DNL Journey Optimizer]** home page, select **[!UICONTROL Messages]**, and click the **[!UICONTROL Executions]** tab.

This tab provides two views: **[!UICONTROL Live view]** and **[!UICONTROL Global view]**.

* The **[!UICONTROL Live view]** tab provides a **real-time overview of all the executed messages** triggered by one or more [journeys](building-journeys/journey.md) **over the last 24 hours only**.

  ![](assets/message-execution-tab-live.png)

  This list auto-refreshes every sixty seconds. If no execution occurred in the last 24 hours for a specific message, all columns will display null values (0) for that message.

* The **[!UICONTROL Global view]** tab provides an **overview of all the executed messages** triggered by one or more [journeys](building-journeys/journey.md) **since the message start date**.

  ![](assets/message-execution-tab-global.png)

  This list auto-refreshes every ninety minutes. The data are aggregated over time since each message start date.

If a message is published but not triggered yet by a journey, it it not listed in any of the tabs. Only the following elements are listed:
* Messages that have been triggered, but not yet started (pending).
* Messages that have been triggered and that are currently running (in progress).

For multichannel messages, one row per channel is displayed for each message.

![](assets/message-execution-multichannel.png)

If a message has been used in several journeys, the **[!UICONTROL Source]** column displays **[!UICONTROL Multiple]**.

By default, the messages are displayed starting from the most recent execution date. Click the **[!UICONTROL Filters]** icon to search the messages according to the channel, the start date, and/or the end date.

![](assets/message-execution-tab-filters.png)

The <!--**[!UICONTROL Quick action]**-->second column enables to open the corresponding [message](create-message.md) and to access the [Live Report](reports/live-report.md) if you are in the **[!UICONTROL Live view]**, or the [Global Report](reports/global-report.md) if you are in the **[!UICONTROL Global view]**.

![](assets/message-execution-open-live-report.png)

For each message execution, a number of indicators are displayed:

* **[!UICONTROL Message label]**: Message title that you defined upon [creating the message](create-message.md).
* **[!UICONTROL Execution ID]**: Automatically generated identifier.
* **[!UICONTROL Source]**: Name of the journey leveraging that message.
* **[!UICONTROL Start date]**: Date and time when the message has been executed from the journey.
* **[!UICONTROL Excluded]**: Number of profiles that have been excluded from the initial target due to exclusion rules.
* **[!UICONTROL Sent]**: Number of messages that have been sent.
* **[!UICONTROL Delivered]**: Number of messages successfully delivered in the recipient's mailbox (email) or device (push) without generating a bounce or any other delivery error.
* **[!UICONTROL Bounces]**: Number of messages that cannot be delivered because of a delivery failure. [Learn more about bounces](suppression-lists.md#delivery-failures).
* **[!UICONTROL Opens]**: Number of messages that have been opened.
* **[!UICONTROL Clicks]**: Number of clicks on links in an email.

  >[!NOTE]
  >
  >Clicks do not exist for push notifications: when a user clicks a push notification, it opens the app, which can only be considered as an open.

* **[!UICONTROL Errors]**: Number of messages that cannot be sent because of a technical failure.

Clicking each hyperlink will open the corresponding message summary view. [Learn more on messages](create-message.md).
