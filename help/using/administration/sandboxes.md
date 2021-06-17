---
title: Sandboxes management
description: Learn how to manage sandboxes
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
exl-id:
feature: Control Groups
topic: Administration
role: Administrator
level: Intermediate
---
# Sandboxes management {#sandboxes}

## Use sandboxes {#using-sandbox}

[!DNL Journey Optimizer] allows you to partition your instance into separated virtual environments called sandboxes.
Sandboxes are assigned through product profiles in the Admin console. [Learn how to assign sandboxes](permissions.md#create-product-profile).

[!DNL Journey Optimizer] reflects Adobe Experience Platform sandboxes which were created for a given organization.
Adobe Experience Platform sandboxes can be created or reset from your Adobe Experience Platform instance. [Learn more in the Sandbox user guide](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html).

You can find the sandbox switcher control at the top-left of your screen. To switch from one sandbox to another, click the currently active sandbox in the switcher and select another sandbox from the drop-down list.

## Assign sandboxes {#assign-sandboxes}

>[!IMPORTANT]
>
> Sandboxes management can only be carried out by a **[!UICONTROL Product]** or **[!UICONTROL System]** administrator. For more information on this, refer to the [Admin console documentation](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

You can choose to assign different sandboxes to out-of-the-box or custom **[!UICONTROL Product profiles]**.

To assign sandboxes:

1. In the [!DNL Admin Console], from the **[!UICONTROL Products]** tab, select the **[!UICONTROL Adobe Experience Platform Apps]** product.

1. Select a **[!UICONTROL Product profile]**.
    
    ![](../assets/sandbox_1.png)

1. Select the **[!UICONTROL Permissions]** tab.

1. Select the **[!UICONTROL Sandboxes]** capability.

    ![](../assets/sandbox_2.png)

1. Under **[!UICONTROL Available Permissions Items]**, click the plus (+) icon to assign sandboxes to your profile. [Learn more about sandboxes](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html).

    ![](../assets/sandbox_3.png)

1. If needed, under **[!UICONTROL Included Permission Items]**, click the X icon next to remove sandboxes access to your **[!UICONTROL Product profile]**.

    ![](../assets/sandbox_4.png)

1. Click **[!UICONTROL Save]**.

## Access to Content {#content-access}

To configure your content accessibility, you need to assign a content shared folder to each of your sandboxes. You can create and configure your shared folder in the **[!UICONTROL Storage]** tab displayed in the [!DNL Admin Console] for administrators. If you have access to the [!DNL Admin Console] as a system administrator, you can create shared folders and add delegates with different access level to your shared folders.

![](../assets/do-not-localize/content_access.png)

Note that for your content to sync with the correct sandbox, you have to follow the same syntax as the sandbox e.g. if your sandbox is called development your shared folder should have the same name.

[Learn how to manage shared folders](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html).
