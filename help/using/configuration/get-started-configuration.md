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

To be able to create your journeys and send messages, you need to go though these configuration steps:

1. **Delegate subdomains**.

    For any new subdomain to be used in Journey Optimizer, the first step will be to delegate it. [Learn more](about-subdomain-delegation.md)

    ![](../assets/subdomain.png)

1. **Create IP pools.**

    Improve your email deliverability and reputation by grouping together IP addresses provisioned with your instance. [Learn more](ip-pools.md)

    ![](../assets/ip-pool.png)

1. **Configure email and push messages**.

    1. Define push notifications settings in both [!DNL Adobe Experience Platform] and [!DNL Adobe Experience Platform Launch]. [Learn more](../push-configuration.md)

    1. Create message presets to configure all the technical parameters required for email and push notification messages. [Learn more](message-presets.md)

    1. Determine which email address to use in priority for your recipients when several addresses are available in Adobe Experience Platform. [Learn more](primary-email-addresses.md)

    1. Manage the number of days during which retries are performed before sending email addresses to the suppression list. [Learn more](manage-suppression-list.md)

1. **Configure journeys**.

    In order to build journeys, you need to configure **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** and **[!UICONTROL Actions]**. [Learn more](about-data-sources-events-actions.md)

    ![](../assets/admin-menu.png)
