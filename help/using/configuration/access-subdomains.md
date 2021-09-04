---
title: Delegate subdomains
description: Learn how to delegate your subdomains
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
exl-id: cb3248c5-f444-47aa-80b2-c1a9fbebfcc0
---
# Access delegated subdomains

All your delegated subdomains display in the **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** menu. Filters are available to help you refine the list (delegation date, user or status).

![](../assets/subdomain-list.png)

The **[!UICONTROL Status]** column provides information on the subdomain delegation process:

* **[!UICONTROL Draft]**: The subdomain delegation has been saved as a draft. Click the subdomain name to resume the delegation process,
* **[!UICONTROL Processing]**: The subdomain is going through several configuration checks before it can be used,
* **[!UICONTROL Success]**: The subdomain has gone through the checks successfully and can be used to deliver messages,
* **[!UICONTROL Failed]**: One or several checks have failed after the subdomain delegation was submitted.

To access detailed information about a subdomain, open it from the list. You can:
    
* Retrieve the subdomain name (read-only) configured during the delegation process, as well as the generated URLs (resources, mirror pages, tracking URLs),

* Add a Google site verification TXT record to your subdomain to ensure that it is verified (see [Add a Google TXT record to a subdomain](google-txt.md)). 
    
![](../assets/subdomain-delegated.png)
