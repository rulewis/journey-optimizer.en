---
title: Administration and settings
description: Learn administration and settings guidelines
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
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
---

# Get started

When accessing Journey Optimizer for the first time, you are provisioned a production sandbox and allocated a certain number of IPs depending on your contract.

To be able to create your journeys and send messages, you need to go though several configuration steps listed in this page.

## Delegate subdomains

<img src="../assets/do-not-localize/icon-subdomains.svg" width="50px">

For any new subdomain to be used in Journey Optimizer, the first step will be to delegate it. [Learn more](about-subdomain-delegation.md)

## Create IP pools

<img src="../assets/do-not-localize/icon-pools.svg" width="50px">

Improve your email deliverability and reputation by grouping together IP addresses provisioned with your instance. [Learn more](ip-pools.md)

## Configure messages

<img src="../assets/do-not-localize/icon-message.svg" width="50px">

Before starting sending push notifications with [!DNL Journey Optimizer], you need to define settings in both [!DNL Adobe Experience Platform] and [!DNL Adobe Experience Platform Launch]. [Learn more](../push-configuration.md)

Create message presets to configure all the technical parameters required for email and push notification messages. [Learn more](message-presets.md)

Determine which email address to use in priority for your recipients when several addresses are available in the database. [Learn more](primary-email-addresses.md)

## Manage quarantines

<img src="../assets/do-not-localize/icon-quarantines.svg" width="50px">

Monitor the email addresses that have been sent to the suppression list and manage the number of days during which retries are performed before exluding them. [Learn more](get-started-quarantines.md)

## Configure journeys

<img src="../assets/do-not-localize/icon-journey.svg" width="50px">

In order to send messages with journeys, you need to configure **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** and **[!UICONTROL Actions]**. [Learn more](about-data-sources-events-actions.md)
