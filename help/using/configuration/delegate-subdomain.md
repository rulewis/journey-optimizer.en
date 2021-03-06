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
role: Administrator
level: Intermediate
---

# Delegate a subdomain

Domain name delegation is a method that allows the owner of a domain name (technically: a DNS zone) to delegate a subdivision of it (technically: a DNS zone under it, which can be called a sub-zone) to another entity. Basically, if a customer is handling the zone “example.com”, he can delegate the sub-zone “marketing.example.com” to Adobe.

By delegating a subdomain for use with [!DNL Journey Optimizer], clients can rely on Adobe to maintain the DNS infrastructure required to meet industry-standard deliverability requirements for their email marketing sending domains, while continuing to maintain and control DNS for their internal email domains.

[!DNL Journey Optimizer] allows you to fully delegate your subdomains to Adobe directly from the product interface. By doing so, Adobe will be able to deliver messages as a managed service by controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking of email campaigns.

>[!NOTE]
>
>By default, [!DNL Journey Optimizer] license contract allows you to delegate up to 10 subdomains. Reach out to your Adobe contact if you want to increase this limitation.
>
>The use of CNAMEs for subdomain delegation is currently not supported by Journey Optimizer.

To delegate a new subdomain, follow the steps below:

1. Access the **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** menu, then click **[!UICONTROL Delegate subdomain]**.

    ![](../assets/subdomain-delegate.png)

1. Specify the name of the subdomain to delegate.

    ![](../assets/subdomain-name.png)

1. The list of records to be placed in your DNS servers displays. Copy these records, either one by one, or by downloading a CSV file, then navigate to your domain hosting solution to generate the matching DNS records.

    Make sure that all the DNS records have been generated into your domain hosting solution. If everything is configured properly, check the box "I confirm...", then click **[!UICONTROL Submit]**.

    ![](../assets/subdomain-submit.png)

    >[!NOTE]
    >
    >You can create the records and submit the subdomain configuration later on using the **[!UICONTROL Save as draft]** button. You will then be able to resume the subdomain delegation by opening it from the subdomains list.

1. Once the subdomain delegation has been submitted, the subdomain displays in the list with the **[!UICONTROL Processing]** status. For more on subdomains' statuses, refer to [this section](access-subdomains.md).

    The checks and actions below will be performed until the subdomain is verified and can be used to send messages.
    
    This step is performed by Adobe and can take up to 3 hours.

    1. Check wether the subdomain has been delegated to Adobe DNS (NS record, SOA record, Zone setup, ownership record),
    1. Configure DNS for the domain,
    1. Create tracking and mirror URLs,
    1. Provision CDN Cloud Front,
    1. Create, validate and attach CDN SSL certificate,
    1. Create Forward DNS,
    1. Create PTR record.

    ![](../assets/subdomain-processing.png)

1. Once the checks are successfull, the subdomain gets the **[!UICONTROL Success]** status. It is ready to be used to deliver messages.

    <!-- later on, users will be notified in Pulse -->

    ![](../assets/subdomain-notification.png)


