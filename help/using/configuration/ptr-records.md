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

Once a subdomain is delegated in Customer Jourrney Management, a PTR record is automatically created and associated with this subdomain. You can access it from the **[!UICONTROL Channels]** `>` **[!UICONTROL PTR records]** menu.

![](../assets/ptr-records.png)

The list shows the PTR records generated for each delegated subdomain, using the syntax below:

* "r" for record,
* "xx" for the two last figures of the IP address,
* subdomain name.

You can open a PTR record from the list to display the associated subdomain name and IP address.

## Edit a PTR record

You can modify PTR records to edit the subdomain associated to an IP address.

1. From the list, click a PTR record name to open it.

1. Edit the subdomain as desired.

    >[!NOTE]
    >
    >You cannot modify the **[!UICONTROL IP]** and **[!UICONTROL PTR record]** fields.

1. Click **[!UICONTROL Update]** to save your changes.

An **[!UICONTROL Updating]** icon displays next to the name of the PTR record in the list.

To check the PTR record update details, click the **[!UICONTROL More actions]** button and select **[!UICONTROL Recent updates]**.

You can see information such as the update status with the approximate remaining time before completion and the requested changes.
