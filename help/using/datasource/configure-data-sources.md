---
title: Configure a data source
description: Learn how to configure a data source
feature: Data Sources
topic: Administration
role: Administrator
level: Intermediate
---
# Configure a data source {#configure-data-source}

Here are the main data source configuration steps:

>[!NOTE]
>
>The data source configuration is always performed by a **technical user**.

1. In the ADMINISTRATION menu section, select **[!UICONTROL Configurations]**. In the  **[!UICONTROL Data Sources]** section, click **[!UICONTROL Manage]**. The list of data sources is displayed. See [this page](../user-interface.md) for more information on the interface. 

    ![](../assets/journey18.png)

1. Then you can either add field groups to the built-in data source (see [this page](../datasource/adobe-experience-platform-data-source.md)) or create a new external data source (see [this page](../datasource/external-data-sources.md)) and associated field groups (see [this page](../datasource/configure-data-sources.md#define-field-groups)).

    ![](../assets/journey23.png)

1. Click **[!UICONTROL Save]**.

    The data source is now configured and ready to be used in your journeys.

## Define field groups {#define-field-groups}

Field groups are sets of fields that you can retrieve from a data source and use in a journey.

For each data source, you can define several field groups, each of them with a specific cache duration.

For example, you can create a field group with the telephone number, the email, the first name and the address of the profile. You will then be able to use this data in your journey to create conditions. For example, you can decide to send an SMS only if the profile's telephone number is not empty. If it is empty, you can send an email.

Even though a default name is automatically added, we recommend that you give a name to  your field group. Indeed, the field group name will be visible to other users in [!DNL Journey Optimizer]. Giving a relevant name to field groups is a best practice.

When a data source field is used in a journey, the system will retrieve all the fields defined for that field group. Therefore, selecting only the fields that you need for your journeys is a best practice. This will reduce the request latency in your journeys thus increasing performance. Note that you can easily add more fields in field groups later.

**[!UICONTROL Cache duration]** is also important as it will help you optimize performance. Cache duration means that in a journey, if data from a field group is retrieved once, the system will then cache it temporarily. If the same data is required later in the same journey, the system won't make another request to the data source. The configuration of the cache duration should be adapted for each use case. If you need to retrieve real-time data such as hotel reservation status, weather information or the number of loyalty points, you will associate the field group containing these fields with a short cache duration (1 second, for example). For fields that are updated less frequently (name, gender), you will create a second field group with a longer cache duration (5 days, for example).

The number of journeys that use a field group is displayed in the **[!UICONTROL Used in]** field. You can click the **[!UICONTROL View journeys]** button to display the list of journeys using this field group.

>[!NOTE]
>
>Note that if a field group has no field, it won???t be displayed in the expression editor.

 ![](../assets/journey3bis.png)

## Field group lifecycle {#field-group-lifecycle}

You can add or remove fields from a field group that is not used in any draft or live journey.

You can add but you cannot remove a field from a field group used in one or more draft or live journeys. This will avoid breaking journeys.

To delete a field from a field group used in one or more journeys, follow these steps. Let's use an example of a field group named ???Field Group A???.

1. In the list of field groups, place the cursor on ???Field Group A??? and click on the **[!UICONTROL Duplicate]** icon located on the right. Name the duplicated field group "Field Group B???, for example.
1. In "Field Group B???, remove the fields you no longer want.
1. In "Field Group A???, check where this field group is used. This information is displayed in the **[!UICONTROL Used in]** field.
1. Open all the journeys which use "Field Group A???.
1. Create new versions of each of these journeys. Edit all activities using "Field Group A??? and select "Field Group B???.
1. Stop old versions of journeys that use "Field Group A???. You should then have no journey using "Field Group A???.
1. Remove "Field Group A??? as is it not used anymore.
