---
title: Built-in product profiles
description: Learn about the built-in product profiles
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
exl-id:
feature: Control Groups
topic: Administration
role: Administrator
level: Intermediate
---
# Built-in product profiles {#ootb-product-profiles}

## Journey Administrator {#journey-administrator}

The **[!UICONTROL Journey Administrator]** product profile allows the administration menus with the possibility to manage and publish Journeys, Messages and Decision management. 

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Journeys| <ul><li> **Manage journeys**: read, create, edit, and delete journeys.</li><li>**Publish journeys**: publish journeys.</li><li>**Manage journeys events, data sources and actions**: read, create, edit, and delete events, sources or actions.</li><li>**View journeys report**: read and edit journeys report.</li></ul>|
|Messages|<ul><li> **Manage messages**: read, create, edit message preview and send test/proof.</li><li>**Manage messages preview and test**: publish messages.</li><li>**Publish messages**: read, create and edit message preview and send test/proof.</li><li>**View messages report**: read and edit messages report.</li></ul>|
|Administration|<ul><li>**Manage subdomains delegation**: read, create, edit, and delete subdomain delegation.</li><li>**Manage IP pools**: read, create, edit, and delete ip pool.</li><li>**View PTR records**: read-only access to PTR records.</li><li> **Manage messages general settings**: read, create, edit, and delete message general settings.</li><li>**Manage messages presets**: read, create, edit, and delete content branding.</li><li>**Manage suppression rules**: access read, create, edit and delete suppression rules.</li><li>**View suppression list**: read and export local suppression list.</li><li>**Manage alerts**: enable/disable alerts for journeys, messages and entitlements.</li></ul>|
|Decision management|<ul><li>**Manage decisions**: read, create, edit, and delete decisions.</li><li>**Manage ranking strategies**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform|<ul><li>**Sandbox**: grant access to sandboxes.</li><li>**Manage segments**: read, create, edit, and delete segments.</li><li>**Manage profiles**: read, create, edit, and delete profiles.</li><li>**Read datasets**: read-only access to datasets.</li><li>**Read schemas**: read-only access to schemas.</li><li>**Read Identity namespace**: read-only access to identity namespace.</li><li>**Manage merge policies**: read, create, edit, and delete merge policies.</li></ul>|

## Journey Approver {#journey-approver}

The **[!UICONTROL Journey Approver]** product profile allows users to approve deliveries and publish them. They can later check the success of their deliveries with the **[!UICONTROL Message]** and **[!UICONTROL Journey]** reports. 

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Journeys| <ul><li>**Manage journeys**: read, create, edit, and delete journeys.</li><li>**Publish journey**: publish journeys.</li><li>**View journeys events, data sources and actions**: read-only access to journey events, journey custom actions and journey data sources sources.</li><li>**View journeys report**: read, edit journey reports.</li></ul>|
|Messages| <ul><li>**Manage messages**: read, create, edit, and delete messages.</li><li>**Publish messages** publish messages.</li><li>**Manage messages preview and test**: read, create and edit message preview and send test/proof.</li><li>**View messages report**: read, create, edit, and delete messages report.</li></ul>|
|Decision management| <ul><li>**Manage decisions**: read, create, edit, and delete decisioning entities.</li><li>**Manage ranking strategies**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li>**Manage segments**: read, create, edit, and delete segments.</li><li>**Manage profiles**: read, create, edit, and delete profiles.</li><li>**Read datasets**: read-only access to datasets.</li><li>**Read schemas**: read-only access to schemas.</li><li>**Manage merge policies**: read, create, edit, and delete merge policies.</li></ul>|
|Administration| <ul><li>**View messages presets**: read-only access to messages presets.</li></ul>|

## Journey Manager {#journey-manager}

The **[!UICONTROL Journey Manager]** product profile allows users to create and edit **[!UICONTROL Journeys]** and every capability linked to **[!UICONTROL Journeys]** but will not be able to publish them.

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Journeys| <ul><li>**Manage journeys**: read, create, edit, and delete journeys.</li><li>**View journeys events**: read-only access to journey events, journey custom actions and journey data sources sources.</li><li>**View journeys report**: read, edit journey report.</li></ul>|
|Messages| <ul><li>**Manage messages**: read, create, edit, and delete messages.</li><li> **Manage messages preview and test**: read, create and edit message preview and send test/proof.</li><li>**View messages report**: read, create, edit, and delete  messages report.</li></ul>|
|Decision management| <ul><li>**Manage decisions**: read, create, edit, and delete decisioning entities.</li><li>**Manage ranking strategies**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li> **Manage segments**: read, create, edit, and delete segments.</li><li>**Manage profiles**: read, create, edit, and delete profiles.</li><li>**Read datasets**: read-only access to datasets.</li><li>**Read schemas**: read-only access to schemas.</li><li>**Manage merge policies**: read, create, edit, and delete merge policies.</li></ul>|
|Administration| <ul><li>**View messages presets**: read-only access to messages presets.</li></ul>|

## Journey viewer {#journey-viewer}

The **[!UICONTROL Journey viewer]** product profile allows read-only access to the **[!UICONTROL Journeys]**, **[!UICONTROL Goals]**, **[!UICONTROL Messages]** and **[!UICONTROL Decision management]** capabilities. 

Users assigned to this product profile will not be able to edit or publish. 

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Journeys| <ul><li>**View journeys**: read-only access to journeys.</li><li>**View journeys event, data sources, actions**: read-only access to journeys events and data sources.</li><li>**View journeys report**: read-only access to journeys reports.</li></ul>|
|Messages| <ul><li>**View messages**: read-only access to messages.</li><li>**View messages report**: read-only access to message reports.</li></ul>|
|Decision management| <ul><li>**View decisions**: read-only access to decisions entities.</li></ul>|

## Message Manager {#message-manager}

The **[!UICONTROL Message Manager]** product profile allows users to create and edit **[!UICONTROL Messages]** and **[!UICONTROL Decision management]** but will not be able to publish them.

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Journeys| <ul><li>**View journeys**: read-only access to journeys.</li><li>**View Journeys events, data sources and actions**: read-only access to journey events, journey custom actions and journey data sources sources.</li></ul>|
|Messages| <ul><li>**Manage messages**: read, create, edit, and delete messages.</li><li>**Manage messages preview and test**: read, create and edit message preview and send test/proof.</li><li> **View messages report**: read, create, edit, and delete  messages reports.</li></ul>|
|Decision management| <ul><li>**Manage decisions**: read, create, edit, and delete decisioning entities.</li></ul>|
|Adobe Experience Platform| <ul><li>**Read profiles**: read-only access to profile for preview and test.</li><li>**Read datasets**: read-only access to datasets.</li><li>**Read schemas**: read-only access to schemas.</li><li>**Manage merge policies**: read, create, edit, and delete merge policies.</li></ul>|
|Administration| <ul><li>**View messages presets**: read-only access to messages presets.</li></ul>|

## Decisioning manager {#decisioning-manager}

The **[!UICONTROL Decisioning manager]** product profile only allows the **[!UICONTROL Decision management]** menu. Users assigned to this product profile will only be able to manage, view and publish decisions. 

This product profile includes the following permissions:

| Capability | Permissions|
|-|-|
|Decision management| <ul><li>**Manage decisions**: read, create, edit, and delete decisioning entities.</li><li>**View decisions**:  read-only access to decisioning entities.</li><li>**Manage ranking strategies**: read, create, edit, and delete custom messages reports and use action features.</li><li>**Publish decisions**: approve or un-approve decisioning activities.</li></ul>|