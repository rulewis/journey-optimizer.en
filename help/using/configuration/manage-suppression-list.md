---
title: Manage the suppression list
description: Learn how to access and manage the Journey Optimizer suppression list 
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
---

# Manage the suppression list {#manage-suppression-list}

With Journey Optimizer, you can monitor all the email addresses that are automatically excluded from sending in a journey, such as:

* Addresses that are invalid (hard bounces), or that consistently soft-bounce, and could adversely affect your email reputation if you continue to include them in your deliveries.
* Recipients who issue a spam complaint of some kind against one of your email messages.

Such email addresses are automatically collected into the Journey Optimizer **suppression list**. [Learn more this section](using/suppression-list.md)

## Access the suppression list {#access-suppression-list}

To access the detailed list of excluded email addresses, open the **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]** menu, then click the **[!UICONTROL View suppression lists]** link.

![](../assets/message-settings.png)

Filters are available to help you browse through the list.
<!--suppression date,  category and reason, but on staging, only creation date filter is available-->

![](../assets/suppression-list.png)

You can also download the list as a CSV file for analysis and reporting purpose.<!--how?-->

## Suppression categories and reasons {#suppression-categories-and-reasons}

When a message fails to be delivered to an email address, Journey Optimizer determines why the delivery failed and associates it with a suppression category.

The suppression categories are as follows:

* **Hard**: The email address is immediately sent to the suppression list.
* **Spam complaint**: The email address of recipients who issue a spam complaint against one of your email messages is immediately sent to the suppression list.
* **Soft**: Soft errors send an address to the suppression list once the error counter reaches the limit threshold. [Learn more on retries](configuration/retries.md)
* **Manual**: You can also manually add an email address to the suppression list.<!--how?-->
<!--More categories?-->

>[!NOTE]
>
>Learn more on soft bounces and hard bounces in the [Delivery failure types](suppression-list.md#delivery-failures) section.

![](../assets/suppression-list.png)

For each email address that is listed, you can also check the **[!UICONTROL Reason]** for excluding it and the date/time it was added to the suppression list.

<!--The possible reasons for a delivery failure are:(from ACS doc)

| Reason | Suppression category | Description |
---------|----------|--------- |
| **[!UICONTROL User unknown]** | Hard | The address does not exist. No further deliveries will be attempted for this profile. |
| **[!UICONTROL Quarantined address]** | Hard | The address was placed in quarantine.
| **[!UICONTROL Unreachable]** | Soft/Hard | An error has occurred in the message delivery chain (such as domain temporarily unreachable). According to the error returned by the provider, the address will be sent to quarantine directly or the delivery will be tried again until Campaign receives an error which justifies the Quarantine status or until the number of errors reaches 5. |
| **[!UICONTROL Address empty]** | Hard | The address is not defined. |
| **[!UICONTROL Mailbox full]** | Soft | The mailbox of this user is full and cannot accept more messages. This address can be removed from the quarantine list to make another attempt. It is removed automatically after 30 days. In order for the address to be automatically removed from the list of quarantined addresses, the **[!UICONTROL Database cleanup]** technical workflow must be started. |
| **[!UICONTROL Refused]** | Soft/Hard | The address has been placed in quarantine due to a security feedback as a spam report. According to the error returned by the provider, the address will be sent to quarantine directly or the delivery will be tried again until Campaign receives an error which justifies the Quarantine status or until the number of errors reaches 5. |
| **[!UICONTROL Duplicate]** | Ignored | The address has already been detected in the segmentation. |
 **[!UICONTROL Not defined]** | Soft | the address is in qualification because errors have not been incremented yet. This type of error occurs when a new error message is sent by the server: it can be an isolated error, but if it occurs again, the error counter increases, which will alert the technical teams. |
| **[!UICONTROL Error ignored]** | Ignored | The address is on allowlist and an email will be sent to it in any case. |
| **[!UICONTROL Address on denylist]** | Hard | The address was added to the denylist at the time of sending. |
| **[!UICONTROL Account disabled]** | Soft/Hard | When the Internet Access Provider (IAP) detects a lengthy period of inactivity, it can close the user's account: deliveries to the user's address will then be impossible. The Soft or Hard type depends upon the type of error received: if the account is temporarily disabled due to six months of inactivity and can still be activated, the status **[!UICONTROL | Erroneous]** will be assigned and the delivery will be tried again. If the error received signals that the account is permanently deactivated then it will directly be sent to suppression list. |
| **[!UICONTROL Not connected]** | Ignored | The profile's mobile phone is switched off or not connected to the network when the message is sent. |
| **[!UICONTROL Invalid domain]** | Soft | The domain of the email address is incorrect or no longer exists. This profile will be targeted again until the error count reaches 5. After this, the record will be set to Quarantine status and no retry will follow. |
| **[!UICONTROL DNS Failure]** | Soft | xxx |
| **[!UICONTROL Invalid Recipient]** | Hard | xxx |

-->