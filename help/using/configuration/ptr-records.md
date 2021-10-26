---
title: PTR records
description: "Learn how to manage ptr-records"
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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
---
# PTR records

## About PTR records

A pointer record (PTR) is a type of Domain Name System (DNS) record that provides the domain name linked to an IP address.

With PTR records, receiving mail servers can check the authenticity of sending mail servers by identifying whether their IP addresses correspond to the names with which the servers connect.

## Access your subdomains' PTR records

Once a subdomain is delegated in Customer Journey Management, a PTR record is automatically created and associated with this subdomain. You can access it from the **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL PTR records]** menu.

![](../assets/ptr-records.png)

The list shows the PTR records generated for each delegated subdomain, using the syntax below:

* "r" for record,
* "xx" for the two last figures of the IP address,
* subdomain name.

You can open a PTR record from the list to display the associated subdomain name and IP address.

## Edit a PTR record

You can modify PTR records to edit the subdomain associated to an IP address.

1. From the list, click a PTR record name to open it.

    ![](../assets/ptr-record-select.png)

1. Edit the subdomain as desired.

    ![](../assets/ptr-record-subdomain.png)

    >[!NOTE]
    >
    >You cannot modify the **[!UICONTROL IP]** and **[!UICONTROL PTR record]** fields.

1. Click **[!UICONTROL Update]** to save your changes.

An **[!UICONTROL Updating]** icon displays next to the name of the PTR record in the list.

![](../assets/ptr-record-updating.png)

To check the PTR record update details, click the **[!UICONTROL Updating]** or **[!UICONTROL Recent updates]** icon.

![](../assets/ptr-record-recent-update.png)

You can see information such as the update status and the requested changes.

![](../assets/ptr-record-updates.png)

### Update statuses

A PTR record update can have the following statuses:

* **[!UICONTROL Processing]**: The PTR record update has been submitted and is going through a verification process.
* **[!UICONTROL Success]**: The updated PTR record has been verified and the new subdomain is now associated with the IP address.
* **[!UICONTROL Failed]**: One or several checks have failed during the PTR record update verification.

**Processing**

Several deliverability checks will be performed to verify that the new subdomain to associate with the IP address is valid. <!--The processing time is around **48h-72h**, and can take up to **7-10 days**. Learn more on the checks performed during the validation cycle in [this section](#create-message-preset).-->

>[!NOTE]
>
>You cannot modify a PTR record while update is in progress. You can still click its name, but the **[!UICONTROL Subdomain]** field is greyed out. The changes will not be reflected until the update is successful.

During the validation process, the old subdomain is still associated with the IP address.

**Success**

Once the validation process is successful, the new subdomain is automatically associated with the IP address.

**Failed**

If the validation process fails, the older PTR record is displayed. The valid subdomain that was previously associated with the IP address remains unchanged.

When the update fails, the PTR record becomes editable again. You can then click its name and update the subdomain again. <!--Learn more on the possible failure reasons in [this section](#monitor-message-presets).-->

The possible update error types are as follows:
* Failure to create a new forward DNS for PTR record
* Failure to update the record
* Failure to re-onboard the affinities
