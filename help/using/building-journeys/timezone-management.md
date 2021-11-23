---
title: Time zone management
description: Learn about time zone management
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
---
# Time zone management {#timezone_management}

You can define a time zone in the [properties](../building-journeys/journey-gs.md#change-properties) of your journey.

To access Properties,click on the pencil icon in the top-right of the screen.

This time zone will be used for every activity of the journey containing a time element such as:

* [Time condition](../building-journeys/condition-activity.md#time_condition)
* [Date condition](../building-journeys/condition-activity.md#date_condition)
* [Custom wait](../building-journeys/wait-activity.md#custom)
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)

You can select a time zone or choose to use the time zone defined in the user profile.

>[!NOTE]
>
>The profile time zone works with the **timeZone** field existing in the **Preference Details** field group.

## Defining a fixed time zone {#fixed-timezone}

The time zone can also be fixed. Clear the pre-defined time zone and pick one from the drop-down list. If you use a fixed time zone, it will be the same for all individuals entering the journey.

To do so, in the **[!UICONTROL Journey Properties]** pane, select a time zone. 

![](../assets/journey72.png)

## Using profiles to define the journey time zone {#timezone-from-profiles}

If the entry event of the journey has a namespace, meaning that the journey can reach the Real-time Customer Profile service of Adobe Experience Platform, the time zone is pre-defined with the one specified in the profile of the individual flowing in the journey.

If a time zone is defined in Adobe Experience Platform profile, it can be retrieved in the journey.

If the individual's profile does not contain a time zone, the timezone used will be the one set in the Journey properties.

To do so, in **[!UICONTROL Properties]**, check **[!UICONTROL Use Profile timezone in waits and conditions]**.

![](../assets/journey73.png)

## Using time zones in expressions {#timezone-in-expressions}

The start and end dates of a journey cannot be linked to a specific time zone. They are automatically associated to the instance's time zone.
