---
title: Release notes
description: Journey Optimizer Release notes
---

# Release Notes {#release-notes}

This page lists all the new features and improvements for [!DNL Journey Optimizer]. You can also consult the latest [Documentation Updates](documentation-updates.md).


## August 2021 Release {#august-2021-release}

### New capabilities

<table>
<thead>
<tr>
<th><strong>Send-Time Optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer Send-Time Optimization capability, powered by Adobe’s AI services, can predict the best time to send an email or push message to maximize engagement based on historical open and click rates.</p>
<p>This feature is currently in beta version and only available to beta customers. To join the beta program, contact Adobe Customer Care.</p>
<p>For more information, refer to the <a href="building-journeys/journeys-message.md#send-time-optimization">detailed documentation</a>.</p>

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Personalized URLs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Personalized URLs take recipients to specific pages of a website, or to a personalized microsite, depending on the profile attributes. In Adobe Journey Optimizer, you can now add personalization to URLs in your message content. URL personalization can be applied to text and images, and use profile data or contextual data.</p>
<p>For more information, refer to the <a href="documentation-updates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Lookup table management</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experience events often contain identifiers related to a behavior (a hotel ID for a hotel reservation, a list of SKUs for a purchase, an account ID for a bank account creation, etc.). This ID can be linked to various details, stored in different tables. You can now leverage data from a linked schema in your journey business events.</p>
<p>For more information, refer to the <a href="event/experience-event-schema.md#leverage_schema_relationships">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Offer Decision content personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use the Journey Optimizer's Expression Editor to personalize the content of your offers with data from the Experience Cloud Platform database, which allows you to adapt your offers to each specific recipient.</p>
<p>For more information, refer to the <a href="documentation-updates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Customer Alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now subscribe to event-based alerts regarding Adobe Journey Optimizer activities. The user interface allows you to view a history of received alerts based on metrics revealed by Adobe Experience Platform Observability Insights. The UI also allows you to view, enable, and disable available alert rules.</p>
<p>This feature is currently in beta version and only available to beta customers. To join the beta program, contact Adobe Customer Care.
</p>
<p>For more information, refer to the <a href="https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html">Adobe Experience Platform documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Improvements

**Journeys**

* **Dynamic headers** - You can now pass dynamic data in HTTP header parameters. These parameters can be used by the integration systems that receive the journey action HTTP calls, for example timestamp or tracking ID. [Learn more](documentation-updates.md)
* **Collections in actions** - You can now add collections in custom actions and expression editor. Note that only simple arrays are supported for now. [Learn more](documentation-updates.md)

**User interface**

* **Search** - You can now filter search results directly from the search field. [Learn more](documentation-updates.md)
* **Recents** - The display of recents elements from Adobe Journey Optimizer home page is now extended to additional business objects. With this update, shortcuts to your recently accessed include Messages, Journeys, Segments, Schemas, Datasets, Data Sources, Events, Actions, Sources, and Destinations. [Learn more](documentation-updates.md)

**Content Design**

* **Background** - Background images are now supported in live preview. [Learn more](documentation-updates.md)

* **One-click opt-out link** - You can insert a new type of link into your email content: the **Opt-out** link allows users to unsubscribe from receiving your communications in just one click, without being redirected to a landing page to confirm opting out. [Learn more](documentation-updates.md)

**Personalization**

* **Expression Editor** - You can now easily add a fall-back value when defining personalization: when personalization field is empty for a profile, the fall-back value will display. [Learn more](documentation-updates.md)

**Email configuration**

* **Retry** - You can now define the retry period on a per preset basis to ensure that retry attempts are not performed anymore when no longer needed. For example, you may set the retry period to 24 hours for a password reset transactional message containing a link valid for only a day. [Learn more](documentation-updates.md)
* **Suppression list** - Adding email addresses and domains into the suppression list is now available from the user interface, either one by one, either in bulk mode through a CSV file upload. [Learn more](documentation-updates.md)
* **Allowed list** - The allowed list can now be enabled and disabled on a non-production sandbox through an API call. [Learn more](documentation-updates.md)
* **Message preset** - You can now find out the reason why a message preset creation failed through a more explicit warning in the user interface. [Learn more](documentation-updates.md)
* **Navigation** - The suppression list, which was accessible under the **Channels > Email configuration > General** menu, has been moved to the **Channels > Email configuration > Suppression list** menu for easier access.


### Fixes 

* Fixed an accessibility issue in message tab navigation.
* Fixed a localization issue in the email designer labels.
* Fixed an issue when selecting more than one node in a journey and clicking 'Delete' on the property panel.
* Fixed an issue which prevented from adding a new header to an action used in a journey.


## July 2021 Release {#july-2021-release}

### New capabilities

<table>
<thead>
<tr>
<th><strong>Leverage schema relationships</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform allows you to define relationships between schemas in order to use one dataset as a lookup table for another. [!DNL Journey Optimizer] can now leverage data coming from a linked schema.</p>
<p>These fields are available in unitary event configuration, journey conditions, message personalization and custom action personalization.</p>
<p>For more information, refer to the <a href="event/experience-event-schema.md#leverage_schema_relationships">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Allowed list</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define a define a specific sending-safe list at the sandbox level, to have a safe environment for testing purpose. On a non-production instance, where mistakes can occur, the allowed list ensures you have no risk of sending out unwanted messages to your customers. This feature is enabled by leveraging Suppression APIs.</p>
<p>For more information, refer to the <a href="allow-list.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Improvements

**Journeys**

* The overall throttling rate of all the read segments that run simultaneously in the same sandbox is limited to 17,000 messages per second. [Read more](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* The **Cache duration** field has been removed from the data source configuration pane. [Read more](datasource/about-data-sources.md)
* For external data sources, a capping rule of 15 calls per second is now automatically defined. [Read more](configuration/external-systems.md#capping)
* For live journeys, the journey properties screen now displays the publication date and the name of the user who published the journey. [Read more](building-journeys/journey-gs.md#change-properties)
* In the journey list screen, the journey type filter has been added. [Read more](user-interface.md#section_lgm_hpz_pgb)
* The **[!UICONTROL Throttling rate]** parameter has been added in the Read segment activity. [Read more](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Preview and test messages**

* Identity and namespace are now visible in the **[!UICONTROL Preview]** screen. [Read more](preview.md#preview-your-messages)
* The number of test emails for proofs is now restricted to 10.
* Characters allowed for the **Subject line prefix** in proofs are now limited. [Read more](preview.md#send-proofs)

**Personalization expression editor**

* The helper drop-down list has been renamed and reordered.

### Fixes 

* Fixed an issue which was causing duplicate messages being delivered for batch email delivery.
* Events are now generated accordingly when email sending is not performed once the retry period is over.
* Fixed an issue where IP information was missing in PTR Records screen.
* Localization in offer rail within Expression Editor is now implemented.
* Fixed incorrect spacing in information popups.
* Fixed an issue in the Email designer when uploading an HTML file where internal style sheet with `background-image` property was not supported. 

