---
title: Create IP pools
description: "Learn how to manage ip-pools"
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
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
---
# Create IP pools

## About IP pools {#about-ip-pools}

With Journey Optimizer, you can create IP pools to group together the IP addresses of your subdomains.

Creating IP pools is strongly recommended for email deliverability. By doing so, you can prevent the reputation of a subdomain from impacting your other subdomains.

For example, one best practice is to have one IP pool for your marketing messages, and another one for your transactional messages. This way, if one of your marketing messages performs badly and is declared as spam by a customer, this will not affect the transactional messages sent to this same customer, who will still receive transactional messages (purchase confirmations, password recovery messages, etc.).

## Create an IP pool {#create-ip-pool}

To create an IP pool, follow these steps:

1. Access the **[!UICONTROL Channels]** / **[!UICONTROL IP pools]** menu, then click **[!UICONTROL Create IP Pool]**.

    ![](../assets/ip-pool-create.png)

1. Provide a name and a description (optional) for the IP pool.

    >[!NOTE]
    >
    >The subdomain's name must begin with a letter (A-Z) and include only alpha-numeric characters or special characters ( _, ., - ).

1. Select the IP addresses to include in the pool from the drop-down list, then click **[!UICONTROL Submit]**.

    ![](../assets/ip-pool-config.png) 

    >[!NOTE]
    >
    >All the IP addresses provisioned with your instance are available in the list.
    
The IP pool is now created and displays in the list. You can select it to access its properties and display the associated message preset. For more on how to associate a message preset with an IP pool, refer to [this section](message-presets.md)).

![](../assets/ip-pool-created.png)

## Edit an IP pool {#edit-ip-pool}

To edit an IP pool:

1. From the list, click the IP pool name to open it.

    ![](../assets/ip-pool-list.png)

1. Edit its properties as desired. You can modify the description, and add or remove IP addresses.

    ![](../assets/ip-pool-edit.png)

    >[!CAUTION]
    >
    >Proceed with extra care when considering deleting an IP, as this will put additionnal load on the other IPs and may have severe impacts on your deliverability. In case of any doubt, contact a deliverability expert.

1. Save your changes.

>[!NOTE]
>
>The IP pool name is not editable. If you want to modify it, you need to delete the IP pool and create another one with the name of your choice.

The update is effective immediately or asynchronously, depending on the IP pool being associated to a [message preset](message-presets.md) or not:

* If the IP pool is **not** selected in a message preset, the update is instantaneous (**[!UICONTROL Success]** status).
* If the IP pool **is** selected in a message preset, the update can take up to 7-10 business days (**[!UICONTROL Processing]** status).

<!--If a message preset has been associated with the IP pool, you first need to remove it before editing the IP pool. Once the your modifications have been done, you can associate the message preset again.-->

To check the IP pool update status, click the **[!UICONTROL More actions]** button and select **[!UICONTROL Recent updates]**.

![](../assets/ip-pool-recent-update.png)

>[!NOTE]
>
>Once an IP Pool is updated successfully, you may have to wait:
>* a few minutes before it is consumed by the unitary messages,
>* until the next batch for the IP pool to be effective in batch messages.

You can also use the **[!UICONTROL Delete]** button to delete an IP pool. Note that you cannot delete an IP pool that has been associated to a message preset.

