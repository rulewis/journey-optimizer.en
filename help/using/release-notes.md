---
title: Release notes
description: Journey Optimizer Release notes
---

# Release Notes {#release-notes}

This page lists all the new features and improvements for [!DNL Journey Optimizer]. You can also consult the latest [Documentation Updates](documentation-updates.md).

## July 2021 Release {#july-2021-release}

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

* **Journeys**
    * The overall throttling rate of all the read segments that run simultaneously in the same sandbox is limited to 17,000 messages per second. [Read more](building-journeys/read-segment.md#configuring-segment-trigger-activity)
    * The **Cache duration** field has been removed from the data source configuration pane. [Read more](datasource/about-data-sources.md)
    * For external data sources, a capping rule of 15 calls per second is now automatically defined. [Read more](configuration/external-systems.md#capping)
    * For live journeys, the journey properties screen now displays the publication date and the name of the user who published the journey. [Read more](building-journeys/journey-gs.md#change-properties)
    * In the journey list screen, the journey type filter has been added. [Read more](user-interface.md#section_lgm_hpz_pgb)
    * The **[!UICONTROL Throttling rate]** parameter has been added in the Read segment activity. [Read more](building-journeys/read-segment.md#configuring-segment-trigger-activity)

* **Preview and test**
    * Identity and namespace are now visible in the **[!UICONTROL Preview]** screen. [Read more](preview.md#preview-your-messages)
    * The number of test emails for proofs is now restricted to 10.
    * Characters allowed for the **Subject line prefix** in proofs are now limited. [Read more](preview.md#send-proofs)

* **Personalization expression editor**
    * The helper drop-down list has been renamed and reordered.

### Fixes 

* Fixed an issue which was causing duplicate messages being delivered for batch email delivery.
* Events are now generated accordingly when email sending is not performed once the retry period is over.
* Fixed an issue where IP information was missing in PTR Records screen.
* Localization in offer rail within Expression Editor is now implemented.
* Fixed incorrect spacing in information popups.
