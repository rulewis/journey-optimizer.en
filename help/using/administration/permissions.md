---
title: Manage users and product profiles
description: Learn how to manage permissions
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
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
---
# Manage users and product profiles {#manage-permissions}

![](../assets/do-not-localize/badge.png)

>[!IMPORTANT]
>
> Each of the procedures detailed below can only be carried out by a **[!UICONTROL Product]** or **[!UICONTROL System]** administrator. For more information on this, refer to the [Admin console documentation](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Product profiles]** are sets of users that share the same permissions and sandboxes within your organization.

The [!DNL Journey Optimizer] product allows you to select between different out-of-the-box **[!UICONTROL Product profiles]** with different levels of permissions to assign to your users. For more information on the available **[!UICONTROL Product profiles]**, refer to this [page](ootb-product-profiles.md).

Each user belonging to a **[!UICONTROL Product profiles]** is entitled with the Adobe apps and services contained in the product.

You can also create your own **[!UICONTROL Product profiles]** if you want to fine-tune your users' access to certain functionalities or objects in the interface.
 
## Assigning a product profile {#assigning-product-profile}

You can choose to assign an out-of-the-box or custom **[!UICONTROL Product profile]** to your users.

The list of every out-of-the-box product profiles with assigned permissions can be found in the [Built-in product profiles](ootb-product-profiles.md) section.

To assign a **[!UICONTROL Product profile]**:

1. In the [!DNL Admin Console], from the **[!UICONTROL Products]** tab, select the **[!UICONTROL Experience Cloud - Platform powered applications]** product.

1. Select a **[!UICONTROL Product profile]**.

1. From the **[!UICONTROL Users]** tab, click **[!UICONTROL Add user]**.

1. Type in your user's name or email address and select the user.

   If the user was not previously created in the [!DNL Admin Console], refer to the [Add users documentation](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

1. Carry out the same steps as above to add other users to your **[!UICONTROL Product profile]**. Then, click **[!UICONTROL Save]**.

Your user should then receive an email redirecting to your instance.

For more information on users management, refer to the [Admin Console documentation](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

When accessing the instance, your user will see a specific view depending on the assigned permissions in the **[!UICONTROL Product profile]**. If the user does not have the right access to a feature, the following screen will appear.

## Editing an existing product profile {#edit-product-profile}

For out-of-the-box or custom **[!UICONTROL Product profiles]**, you can decide at any time to add or delete permissions.

In this example, we want to add **[!UICONTROL Permissions]** related to the **[!UICONTROL Message]** capability for users assigned to the Journey viewer **[!UICONTROL Product profile]**. The users will then be able to publish messages.

Note that if you modify an out-of-the-box or custom **[!UICONTROL Product profile]**, it will impact every user assigned to this **[!UICONTROL Product profile]**.

1. In the [!DNL Admin Console], from the **[!UICONTROL Products]** tab, select the **[!UICONTROL Experience Cloud - Platform powered applications]** product.

1. Select your previously configured Journey Read-only **[!UICONTROL Product profile]**.

1. Select the **[!UICONTROL Permissions]** tab.

    The **[!UICONTROL Permissions]** tab displays the list of capabilities that apply to the ***[!UICONTROL Experience Cloud - Platform powered applications]** product.

1. Select the **[!UICONTROL Messages]** capability.

1. From the **[!UICONTROL Available Permission Items]** list, select the permissions to assign to your **[!UICONTROL Product profile]** by clicking the plus (+) icon. 

    Here, we add the **[!UICONTROL Publish messages]** permission.

1. If needed, under **[!UICONTROL Included Permission Items]**, click the X icon next to remove permissions to your product profile.

1. When finished, click **[!UICONTROL Save]**.

If needed, you can also create new product profile with specific permissions. For more on this, refer to [Creating a product profile](#create-product-profile).

## Creating a product profile {#create-product-profile}

[!DNL Journey Optimizer] allows you to create your own **[!UICONTROL Product profiles]** and assign a set of permissions and sandboxes to your users. With **[!UICONTROL Product profiles]**, you can authorize or deny access to certain functionalities or objects in the interface.

For more information on how to create and manage sandboxes, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html).

In this example, we will create a product profile named **Journeys read-only** where we will grant read-only rights to the Journey feature. Users will only be able to access and view journeys and will not be able to access other features such as **[!UICONTROL Decision management]** or **[!UICONTROL Messages]** in [!DNL Journey Optimizer].

To create our **Journeys read-only** **[!UICONTROL product profiles]**:

1. Access the [!DNL Admin Console].

1. From the **[!UICONTROL Products]** tab, select the **[!UICONTROL Experience Cloud - Platform powered applications]** product.

1. Click **[!UICONTROL New Profile]**.

1. Add a **[!UICONTROL Profile Name]** and **[!UICONTROL Description]** for your new **[!UICONTROL product profiles]**. 
    
    If you want your profile's **[!UICONTROL Display name]** to be different, uncheck **[!UICONTROL Same as Profile Name]** and type in your **[!UICONTROL Display name]**.

1. In the **[!UICONTROL User Notifications]** category, choose whether users will be notified by email when they are added or removed from this product profile.

1. When finished, click **[!UICONTROL Done]**.

1. To add permissions for users to access different features, select between the different capabilities such as **[!UICONTROL Messages]**, **[!UICONTROL Segments]** or **[!UICONTROL Decision management]** available in [!DNL Journey Optimizer] listed in the left-hand menu. 
    
    Here we select the **[!UICONTROL Journeys]** capability.

1. From the **[!UICONTROL Available Permission Items]** list, select the permissions to assign to your **[!UICONTROL Product profile]** by clicking the plus (+) icon.

1. Select the **[!UICONTROL Sandbox access]** capability to choose which sandbox(es) to assign to your **[!UICONTROL Product profile]**. 

1. Under **[!UICONTROL Available Permissions Items]**, click the plus (+) icon to assign sandboxes to your profile. [Learn more about sandboxes](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html).

1. When finished, click **[!UICONTROL Save]**.

Your **[!UICONTROL Product profile]** is now created and configured. You now need to assign it to users.

For more information on product profile creation and management, refer to the [Admin Console documentation](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
