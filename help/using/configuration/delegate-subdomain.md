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
---

# Delegate a subdomain

To delegate a new subdomain, follow the steps below:

1. Access the **[!UICONTROL Message Configuration]** / **[!UICONTROL Subdomain delegation]** menu, then click **[!UICONTROL Delegate subdomain]**.

    ![](../assets/subdomain-delegate.png)

1. Specify the name of the subdomain to delegate.

1. The list of records to be placed in your DNS servers displays. Copy these records, either one by one, or by downloading a CSV file, then navigate to your domain hosting solution to generate the matching DNS records.

    !!Add info on the generated Txt record. Additional check, need additional info.

1. Make sure that all the DNS records have been generated into your domain hosting solution. If everything is configured properly, select the first statement then click **[!UICONTROL Submit]** to confirm.

    ![](../assets/subdomain-submit.png)

    >[!NOTE]
    >
    >You can create the records and submit the subdomain configuration later on using the **[!UICONTROL Save as draft]** button. You will then be able to resume the subdomain delegation by opening it from the subdomains list.

1. Once the subdomain delegation has been subdmitted, the subdomain displays in the list with the **[!UICONTROL Processing]** status.

    ![](../assets/subdomain-processing.png)

    Various configuration checks will be performed until the subdomain is verified and can be used to deliver messages:

    1. xxx
    1. xxx
    1. xxx
    1. xxx

    You can follow the validation progress for a subdomain at any time by opening it from the list.

    ![](../assets/subdomain-processing-steps.png)

1. Once the checks are successfull, the subdomain gets the **[!UICONTROL Success]** (!!or Verified) status. It now ready to be used to deliver messages.

    You can retrieve all the URLs that have been generated (resources, mirror page, tracking URLs) by opening it from the list.

    ![](../assets/subdomain-delegated.png)
