---
title: User Interface
description: Customer Journey Management User Interface
page-status-flag: never-activated
uuid: 
contentOwner:
products:
audience: customer journey management
content-type: reference
topic-tags: customer-journey-management-user-interface
discoiquuid:
internal: n
snippet: y
---
# User interface {#cjm-user-interface}

![](assets/do-not-localize/badge.png)

>[!NOTE]
>
>To get the best out of [!DNL Customer Journey Management], we recommend using Chrome as your Internet browser. The interface is displayed in the language defined in IMS. If your IMS language is not supported by [!DNL Customer Journey Management], the interface is displayed in English. 
>
>This documentation is frequently updated to reflect recent changes in the product. However, some screenshots can slightly differ from the product's interface.

## Workspace {#cjm-workspace}

Use the links on the left to browse capabilities. The **[!UICONTROL Recents]** list provides shortcuts to the recently created or updated messages, events and journeys. This list displays their creation and modification dates and status.

![](assets/cjm-home.png)

Key concepts when browsing the user interface are detailled in the [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-ui/ui-guide.html?lang=en#adobe-experience-platform-ui-guide).

## Search and filter{#section_lgm_hpz_pgb}

In the most of the lists, a search bar allows you to search for an item.

The **[!UICONTROL Filters]** can be accessed by clicking on the filter icon on the top left of the list. The filter menu allows you to filter the displayed elements according to different criteria. You can choose to display only elements of a certain type or status, the ones you created, or the ones modified in the last 30 days.

In the journey list, in addition to the **[!UICONTROL Creation filters]**, you can also filter the displayed journeys according to their status and version (**[!UICONTROL Status and version filters]**). You can choose to display only journeys which use a particular event, field group or action (**[!UICONTROL Activity filters]** and **[!UICONTROL Data filters]**). The **[!UICONTROL Publication filters]** let you select a publication date or a user. You can choose, for example, to display the latest versions of live journeys that were published yesterday. [Learn more](building-journeys/using-the-journey-designer.md).

>[!NOTE]
>
>Note that columns displayed can be personalized using the configuration button on the top right of the lists. Personalization is saved for each user.

Use the **[!UICONTROL Last update]** and **[!UICONTROL Last update by]** columns to check when happened the last update of your journeys and who saved it.

![](assets/journey74.png)

In the Event, Data source and Action configuration panes, the **[!UICONTROL Used in]** field displays the number of journeys that use that particular event, field group or action. You can click the **[!UICONTROL View journeys]** button to display the list of corresponding journeys.

![](assets/journey3bis.png)

In the different lists, you can perform basic actions on each element. For example, you can duplicate or delete an item.

![](assets/journey4.png)

## Browse through Adobe Experience Platform fields {#friendly-names-display}

When defining [event payload](event/about-creating.md#define-the-payload-fields), [field group payload](datasource/configure-data-sources.md#define-field-groups) and selecting fields in the [expression editor](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html), the display name is displayed in addition to the field name. This information is retrieved from the schema definition in the Experience Data Model.

If descriptors such as "xdm:alternateDisplayInfo" are provided while setting up schemas, the user-friendly names will replace display names. It is especially useful when working with “eVars” and generic fields. You can configure friendly name descriptors via an API call. For more information, see the [Schema Registry developer guide](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html).

![](assets/xdm-from-descriptors.png) 

If a friendly name is available, then the field will be displayed as `<friendly-name>(<name>)`. If no friendly name is available, the display name will appear, for example `<display-name>(<name>)`. If none of them are defined, only the technical name of the field will be displayed `<name>`.

>[!NOTE]
>
>Friendly names are not retrieved when you select fields from a union of schemas.

## Accessibility{#cjm-accessibility}

Here are the different shortcuts available in the [!DNL Customer Journey Management]'s interface.

_In the list of journeys, actions, data sources or events:_

* Press **c** to create a new journey, action, data source or event.

_When configuring an activity in a journey:_

The canvas is automatically saved. You can see, on the top left of the canvas, the saving status.

* Press **escape** to close the configuration pane and discard the changes made. This is the equivalent of the **[!UICONTROL Cancel]** button.
* Press **Enter** or click outside the pane to close the configuration pane. Changes are saved. This is the equivalent of the **[!UICONTROL Ok]** button.
* If you press **Delete** or **backspace**, you can then press **Enter** to confirm the deletion.

_In pop-ups:_

* Press **escape** to close it (equivalent of the **[!UICONTROL Cancel]** button).
* Press **Enter** to save or confirm (equivalent of the **[!UICONTROL Ok]** or **[!UICONTROL Save]** button).

_In the event, data source or action configuration pane:_

* Press **escape** to close the configuration pane without saving.
* Press **Enter** to save modifications and close the configuration pane.
* Press **tab** to jump between the different fields to configure.

_In the simple expression editor_

* Double-click on a field, on the left, to add a query (equivalent to drag & drop).

_When browsing through XDM fields:_

* Checking a "node" will select all the fields of the node.

_In all text areas:_

* Use the **Ctrl/Command + A** key combination to select the text. In the payload preview, it selects the payload.

_In a screen with a search bar:_

* Use the **Ctrl/Command + F** key combination to select the search bar.

_In the canvas of a journey:_

* Use the **Ctrl/Command + A** key combination to select all activities.
* When one or several activities are selected, press **Delete** or **backspace** to delete them. Then you can press **Enter** to confirm in the confirmation pop-up.
* Double-click on an activity from the left palette to add it at the first available position (from top to bottom).

_In a journey:_

* Press **T** to enable/disable the test mode.
* In an event-based journey in test mode, press **E** to trigger an event.
* In a segment-based journey, when the **Single profile at a time** option is selected in test mode, press **P** to trigger an event.
* In test mode, press **L** to display the logs.
