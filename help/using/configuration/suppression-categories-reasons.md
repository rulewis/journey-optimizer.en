---
title: Suppression categories and reasons
description: Learn how to xxxx
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

# Suppression categories and reasons

When a message fails to be delivered to an email address, Journey Optimizer determines why the delivery failed and associates to it a suppression category.

The suppression category determines when the email address is sent to to the suppression list:

* **Soft**: Soft errors send an address to the suppression list once the error counter reaches the limit threshold. Learn more on [retries](using/suppression-lists.md#retries).
* **Hard**: The email address is immediately sent to the suppression list.
* **Spam complaint**: The email address of recipients who issue a spam complaint of some kind against one of your email messages is immediately sent to the suppression list.
* **Manual**: You can also manually add an email address to the suppression list.<!--how?-->
<!--more categories?-->

Learn more on soft bounces and hard bounces in the [Delivery failure types](#delivery-failures) section.

<!--Possible failure reasons and their associated category are as follows:

|Reason|Description|Suppression category|
|------|-----------|----|
|Mail box full| The mail box of the recipient is full and could not receive the message. |Soft|
|DNS failure| xxx |Soft|
|Invalid recipient| xxx |Hard|-->

![](../assets/suppression-list.png)

For each email address that is listed, you can see the **[!UICONTROL Suppression category]** (**[!UICONTROL Soft]**, **[!UICONTROL Hard]**, or **[!UICONTROL Manual]**), the **[!UICONTROL Reason]** for excluding it and the date/time it was added to the suppression list.

The possible reasons for a delivery failure are:<!--from ACS doc-->

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