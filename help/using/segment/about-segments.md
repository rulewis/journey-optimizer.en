---
title: About Adobe Experience Platform segments
description: Learn how to configure an Adobe Experience Platform segment
feature: Journeys
topic: Content Management
role: User
level: Intermediate
---
# Get started with segments {#about-segments}

[!DNL Journey Optimizer] allows you to create Adobe Experience Platform segments using Real-Time Customer Profile data directly from the **[!UICONTROL Segments]** menu, and leverage them into your journeys.

Note that segments can also be created from the Segmentation service itself. Learn more in the [Adobe Experience Platform Segmentation Service documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target="_blank"}.

You can leverage segments in journeys in different ways:

* Use a **Read segment** orchestration activity to make all individuals belonging to the specified segment enter the journey. Messages included in your journey are sent to the individuals belonging to the segment. Let's say you have a "silver customer" segment. With this activity, you can make all silver customers enter a journey and send them a series of personalized messages.

    For more on how to use the **[!UICONTROL Read segment]** activity, refer to [this section](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Use the **Segment qualification** event activity to make individuals enter or move forward in a journey based on Adobe Experience Platform segment entrances and exits. For example, you can make all new silver customers enter a journey and send them messages. For more on how to use this activity, refer to [this section](../building-journeys/segment-qualification-events.md).

* Build **complex conditions** in your journeys using the simple or advanced expression editor. Learn more in [this section](../building-journeys/condition-activity.md#using-a-segment).
