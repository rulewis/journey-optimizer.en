---
title: User Interface
description: Journey Optimizer User Interface
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 681532f8-1149-465e-92c8-2b5366abc3aa
---
# User interface {#cjm-user-interface}

Once connected to [Adobe Experience Cloud](http://experience.adobe.com), browse to [!DNL Journey Optimizer].

Key concepts when browsing the user interface are common with Adobe Experience Platform. Refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-ui/ui-guide.html#adobe-experience-platform-ui-guide){target="_blank"} for more details.

Components and capabilities available in the user interface depend on your [permissions](administration/permissions.md) and on your [licencing package](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. For any question, reach out to your Adobe Customer Success Manager.

>[!NOTE]
>
>This documentation is frequently updated to reflect latest changes in the product user interface. However, some screenshots can slightly differ from your user interface.


## Left navigation

Use the links on the left to browse capabilities.

![](assets/ajo-home.png)

>[!NOTE]
>
>Available capabilities may vary depending on your permissions and licence agreement.

You can find below the full list of services and capabilities available in the left navigation and links to associated documentation.

**Home**

[!DNL Journey Optimizer] home page contains key links and resources to start. The **[!UICONTROL Recents]** list provides shortcuts to the recently created or updated messages, events and journeys. This list shows their creation and modification dates and status.

**[!UICONTROL JOURNEY MANAGEMENT]**

* **[!UICONTROL Journeys]** - Create, configure and orchestrate your customer journeys. [Learn more](building-journeys/journey-gs.md#jo-build)

* **[!UICONTROL Messages]** - Create, design, test and publish email and push messages. [Learn more](create-message.md)
        
**[!UICONTROL DECISION MANAGEMENT]**

* **[!UICONTROL Offers]** - Access your recent sources and datasets from this menu. Use this section to create new offers. [Learn more](offers/offer-library/creating-personalized-offers.md)

* **[!UICONTROL Components]** - Create placements, rules and tags. [Learn more](offers/offer-library/key-steps.md)

**[!UICONTROL CONTENT MANAGEMENT]**

* **[!UICONTROL Assets]** - [!DNL Adobe Experience Manager Assets Essentials] is a centralized repository of assets that you can use to populate your messages. [Learn more](assets-essentials.md)

**[!UICONTROL DATA MANAGEMENT]**

* **[!UICONTROL Schemas]** - Use Adobe Experience Platform to create and manage Experience Data Model (XDM) schemas in an interactive visual canvas called the Schema Editor. [Learn more](get-started-schemas.md)

* **[!UICONTROL Datasets]** - All data that is ingested into Adobe Experience Platform is persisted within the Data Lake as datasets. A dataset is a storage and management construct for a collection of data, typically a table, that contains a schema (columns) and fields (rows). [Learn more](get-started-datasets.md)

* **[!UICONTROL Queries]** - Use Adobe Experience Platform Query Service to write and execute queries, view previously executed queries, and access queries saved by users within your organization. [Learn more](get-started-queries.md)

* **[!UICONTROL Monitoring]** - Use this menu to monitor your data ingestion within Adobe Experience Platform user interface. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/ingestion/quality/monitor-data-ingestion.html){target="_blank"}

**[!UICONTROL CONNECTIONS]**

* **[!UICONTROL Sources]** - Use this menu to ingest data from a variety of sources - such as Adobe applications, cloud-based storages, databases, and more -, and structure, label and enhance incoming data. [Learn more](get-started-sources.md)

**[!UICONTROL CUSTOMER]**

* **[!UICONTROL Segments]** - Create and manage Experience Platform segment definitions and leverage them into your journeys. [Learn more](segment/about-segments.md)

* **[!UICONTROL Profiles]** - Real-time Customer Profile creates a holistic view of each of your individual customers, combining data from multiple channels including online, offline, CRM, and third-party data. [Learn more](get-started-profiles.md)

* **[!UICONTROL Identities]** - Adobe Experience Platform Identity Service manages the cross-device, cross-channel, and near real-time identification of your customers in what is known as an identity graph within Adobe Experience Platform. [Learn more](get-started-identity.md)

**[!UICONTROL ADMINISTRATION]**

* **[!UICONTROL Journey Administration]** - Use this menu to configure [events](event/about-events.md), [data sources](datasource/about-data-sources.md) and [actions](action/action.md) to use in your journeys.

* **[!UICONTROL Sandboxes]** - Adobe Experience Platform provides sandboxes which partition a single instance into separate virtual environments to help develop and evolve digital experience applications. [Learn more](administration/sandboxes.md)

<!--
* **[!UICONTROL Alerts]** - The user interface allows you to view a history of received alerts based on metrics revealed by Adobe Experience Platform Observability Insights. The UI also allows you to view, enable, and disable available alert rules. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html){target="_blank"}
-->

## In-product use cases

Leverage [!DNL Adobe Journey Optimizer] use cases from the Home page, and provide a few quick inputs to create a customer journey.

![](assets/use-cases-home.png)

Available use cases are:

* **Create test profiles**, to create test profiles using our CSV template to test personalized messages and journeys. Learn how to implement this use case [on this page](building-journeys/creating-test-profiles.md#use-case-1).
* **Send a birthday message to customers**, to automatically send an email to wish your customers around their birthday. (coming soon)
* **Send emails to onboard new customers**, to easily send up to two emails to welcome your newly registered customers. (coming soon)
* **Send push messages to imported list of customers**, to quickly send a push notification to a list of customers imported from a CSV file. (coming soon)

Click **[!UICONTROL View details]** to learn more about each use case.

Click the **[!UICONTROL Begin]** button to start the use case.

You can access executed use cases from the **[!UICONTROL View use case library]** button.

## Accessibility{#accessibility}

The accessibility features in [!DNL Adobe Journey Optimizer] are inherited from Adobe Experience Platform:

* Keyboard accessibility
* Color contrast
* Validation of required fields

[Learn more](https://experienceleague.adobe.com/docs/experience-platform/accessibility/features.html){target="_blank"} in Adobe Experience Platform documentation.

You can use these common keyboard shortcuts in [!DNL Journey Optimizer]:

| Action | Shortcut |
| --- | --- |
| Move between user interface elements, sections, and menu groups | Tab |
| Move backward between user interface elements, sections, and menu groups | Shift + Tab |
| Move within sections to set focus to individual elements | Arrow |
| Select or clear an element that is in focus | Enter or Spacebar |
| Cancel a selection, collapse a panel, or close a dialog box | Esc |

[Learn more](https://experienceleague.adobe.com/docs/experience-platform/accessibility/custom.html){target="_blank"} in Adobe Experience Platform documentation.

You can use these shortcuts in specific parts of Journey Optimizer:

<table>
  <thead>
    <tr>
      <th>Interface element</th>
      <th>Action</th>
      <th>Shortcut</th>
    </tr>
  </thead>
  <tr>
    <td>List of journeys, actions, data sources, or events</td>
    <td>Create a journey, an action, a data source, or an event</td>
    <td>C</td>
  </tr>
  <tr>
    <td rowspan="3">Journey canvas in draft status</td>
    <td>Add an activity from the left palette at the first available position, from top to bottom</td>
    <td>Double-click on the activity</td>
  </tr>
  <tr>
    <td>Select all the activities</td>
    <td>Ctrl + A (Windows)<br/>Command + A (Mac)</td>
  </tr>
  <tr>
    <td>Delete the selected activities</td>
    <td>Delete or Backspace, then Enter to confirm the deletion</td>
  </tr>
  <tr>
  <td rowspan="3">
  
  Configuration pane of these elements:

<ul>
  <li>Activity in a journey</li>
  <li>Event</li>
  <li>Data source</li>
  <li>Action</li>
</ul>

  </td>
    <td>Move to the next field to be configured</td>
    <td>Tab</td>
  </tr>
  <tr>
    <td>Save changes and close the configuration pane</td>
    <td>Enter</td>
  </tr>
  <tr>
    <td>Discard changes and close the configuration pane</td>
    <td>Esc</td>
  </tr>
  <tr>
    <td rowspan="4">Journey in test mode</td>
    <td>Enable or disable the test mode</td>
    <td>T</td>
  </tr>
  <tr>
    <td>Trigger an event in an event-based journey</td>
    <td>E</td>
  </tr>
  <tr>
    <td>

  Trigger an event in a segment-based journey for which the **[!UICONTROL Single profile at a time]** option is turned on

  </td>
    <td>P</td>
  </tr>
  <tr>
    <td>Display the test logs</td>
    <td>L</td>
  </tr>
<!-- //Ajouter ce raccourci quand il marchera (actuellement, le raccourci Ctrl/Cmd+F du navigateur a priorité sur celui de AJO).//
  <tr>
    <td>Page with a search bar</td>
    <td>Select the search bar</td>
    <td>Ctrl/Command + F</td>
  </tr>
-->
  <tr>
    <td>Text field</td>
    <td>Select all the text in the selected field</td>
    <td>Ctrl + A (Windows)<br/>Command + A (Mac)</td>
  </tr>
  <tr>
    <td rowspan="2">Pop-up window</td>
    <td>Save changes or confirm the action</td>
    <td>Enter</td>
  </tr>
  <tr>
    <td>Close the window</td>
    <td>Esc</td>
  </tr>
  <tr>
    <td>Simple expression editor</td>
    <td>Select and add a field</td>
    <td>Double-click on a field</td>
  </tr>
  <tr>
    <td>Browsing through XDM fields</td>
    <td>Select all the fields of a node</td>
    <td>Select the parent node</td>
  </tr>
  <tr>
    <td>Payload preview</td>
    <td>Select the payload</td>
    <td>Ctrl + A (Windows)<br/>Command + A (Mac)</td>
  </tr>
</table>

## Find help and support

Access Adobe Journey Optimizer key help pages from the lower section of the home page.

Use the **Help** icon to access help pages, contact support and share feedback. You can search help articles and videos from the search field.

![](assets/ajo-help.png)

## Supported browsers

Adobe [!DNL Journey Optimizer] interface is designed to work optimally in the latest version of Google Chrome. You might have trouble using certain features on older versions or other browsers.

## Language preferences

User interface is currently available in the following languages:

* English
* French
* German

Your default interface language is determined by the preferred language specified in your user profile.

To change your language:

* Click **Preferences** from your avatar, on the top right.
    ![](assets/preferences.png)
* Then click the language displayed under your email address
* Select your preferred language and click **Save**. You can select a second language in case the component you are using is not localized in your forst language.
    ![](assets/select-language.png)

## Search{#unified-search}

Anywhere from Adobe Journey Optimizer interface, use the Unified Adobe Experience Cloud search capability on the center of the top bar to find assets, journeys, datasets, messages, and more across your sandboxes. 

Start entering content to display top results. Help articles about the entered keywords also show up in the results.

![](assets/unified-search.png)

Press **Enter** to access all results and filter by business object.

![](assets/search-and-filter.png)

## Filter lists{#section_lgm_hpz_pgb}

In most of the lists, a search bar allows you to search for a specific item and select filtering criteria.

Filters can be accessed by clicking on the filter icon on the top left of the list. The filter menu allows you to filter the displayed elements according to different criteria. You can choose to display only elements of a certain type or status, the ones you created, or the ones modified in the last 30 days. Options differ depending on the context.

In the list of journeys, you can filter journeys according to their status, type and version from the **[!UICONTROL Status and version filters]**. The type can be: **[!UICONTROL Unitary event]**, **[!UICONTROL Segment qualification]**, **[!UICONTROL Read segment]**, **[!UICONTROL Business event]** or **[!UICONTROL Burst]**. You can choose to display only journeys which use a specific event, field group or action from the **[!UICONTROL Activity filters]** and **[!UICONTROL Data filters]**. The **[!UICONTROL Publication filters]** let you select a publication date or a user. You can choose, for example, to display the latest versions of live journeys that were published yesterday. [Learn more](building-journeys/using-the-journey-designer.md).

>[!NOTE]
>
>Note that columns displayed can be personalized using the configuration button on the top right of the lists. Personalization is saved for each user.

Use the **[!UICONTROL Last update]** and **[!UICONTROL Last update by]** columns to check when happened the last update of your journeys and who saved it.

![](assets/filter-journeys.png)

In the Event, Data source and Action configuration panes, the **[!UICONTROL Used in]** field displays the number of journeys that use that particular event, field group or action. You can click the **[!UICONTROL View journeys]** button to display the list of corresponding journeys.

![](assets/journey3bis.png)

In the different lists, you can perform basic actions on each element. For example, you can duplicate or delete an item.

![](assets/journey4.png)
