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
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
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

    >[!CAUTION]
    >
    >Delegating an invalid subdomain to Adobe is not allowed. Make sure you enter a valid subdomain which is owned by your organization, such as marketing.yourcompany.com.
    >
    >Note that multi-level subdomains such as email.marketing.yourcompany.com are currently not supported.

1. The list of records to be placed in your DNS servers displays. Copy these records, either one by one, or by downloading a CSV file, then navigate to your domain hosting solution to generate the matching DNS records.

1. Make sure that all the DNS records have been generated into your domain hosting solution. If everything is configured properly, check the box "I confirm...", then click **[!UICONTROL Submit]**.

    ![](../assets/subdomain-submit.png)

    >[!NOTE]
    >
    >You can create the records and submit the subdomain configuration later on using the **[!UICONTROL Save as draft]** button. You will then be able to resume the subdomain delegation by opening it from the subdomains list.

1. Once the subdomain delegation has been submitted, the subdomain displays in the list with the **[!UICONTROL Processing]** status. For more on subdomains' statuses, refer to [this section](access-subdomains.md).

    ![](../assets/subdomain-processing.png)

    Before being able to use that subdomain to send messages, you need to wait until Adobe performs the required checks, which can take up to 3 hours. Learn more in [this section](#subdomain-validation).

1. Once the checks are successful, the subdomain gets the **[!UICONTROL Success]** status. It is ready to be used to deliver messages.

    <!-- later on, users will be notified in Pulse -->

    ![](../assets/subdomain-notification.png)

## Subdomain validation {#subdomain-validation}

The checks and actions below will be performed until the subdomain is verified and can be used to send messages.
    
>[!NOTE]
>
>These steps are performed by Adobe and can take up to 3 hours.

1. **Pre-validate**: Adobe checks whether the subdomain has been delegated to Adobe DNS (NS record, SOA record, Zone setup, ownership record). If the pre-validation step fails, an error is returned along with the corresponding reason, otherwise Adobe proceeds to the next step.

1. **Configure DNS for the domain**:

    * **MX record**: Mail eXchange record - Mail server record that processes inbound emails sent to the subdomain.
    * **SPF record**: Sender Policy Framework record - Lists the mail servers' IPs that can send emails from the subdomain.
    * **DKIM record**: DomainKeys Identified Mail standard record - Uses public-private key encryption to authenticate the message to avoid spoofing.
    * **A**: Default IP mapping.

1. **Create tracking and mirror URLs**: if the domain is email.example.com, the tracking/mirror domain will be data.email.example.com. It is secured by installing the SSL certificate.

1. **Provision CDN CloudFront**: if CDN is not setup already, Adobe provisions it for the imsorg.

1. **Create CDN domain**: if the domain is email.example.com, the CDN domain will be cdn.email.example.com.
    
1. **Create and attach CDN SSL certificate**: Adobe creates the CDN certificate for the CDN domain and attaches the certificate to the CDN domain.

1. **Create forward DNS**: if this is the first subdomain that you are delegating, Adobe will create the forward DNS which is required to create PTR records - one for each of your IPs.

1. **Create PTR record**: PTR record, also known as reverse DNS record, is required by the ISPs so that they do not mark the emails as spam. Gmail also recommends having PTR records for each IP. Adobe creates PTR records only when you delegate the first subdomain, one for each IP, all IPs pointing to the first subdomain. For example, if the IP is *192.1.2.1* and the subdomain is *email.example.com*, the PTR record will be: *192.1.2.1  PTR r1.email.example.com*. You can update the PTR record afterwards to point to the new delegated domain.
