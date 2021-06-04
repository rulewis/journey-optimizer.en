---
title: Create message presets
description: Learn how to configure and monitor message presets
---

# Create message presets

With [!DNL Journey Optimizer], you can set up message presets that define all the technical parameters required for email and push notification message: email type, sender email and name, mobile apps, and more.

>[!CAUTION]
>
> Message presets configuration is restricted to Journey Administrators. [Learn more](../administration/ootb-product-profiles.md#journey-administrator)
>

Once message presets have been configured, you be able to select them when creating messages from the **[!UICONTROL Presets]** list.

## Create a message preset {#create-message-preset}

To create a message preset, follow these steps:

1. Access the **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** menu, then click **[!UICONTROL Create Message preset]**.

    ![](../assets/preset-create.png)

1. Enter a name and a description (optional) for the preset, then select the channel(s) to configure.

    ![](../assets/preset-general.png)


    >[!NOTE]
    >
    > * Names must begin with a letter (A-Z). It can only contain alpha-numeric characters and  `_`, `.`, `-` characters. 

1. Configure **email** settings.

    ![](../assets/preset-email.png)

    * Select the type of message that will be sent with the preset: **Transactional** or **Marketing**

        >[!CAUTION]
        >
        > **Transactional** messages can be sent to profiles who unsubscribed from marketing communications. These messages can only be sent in specific contexts, such as password reset, order status, delivery notification for example.
        >
    
    * Select the subdomain to use to send the emails. [Learn more](about-subdomain-delegation.md)
    * Select the IP pool to associate with the preset. [Learn more](ip-pools.md)
    * Enter the header parameters for the emails sent using the preset. 

        >[!NOTE]
        >
        > * Names must begin with a letter (A-Z). It can only contain alpha-numeric characters and  `_`, `.`, `-` characters. 
        > 
        > * Except for the **Reply to (forward email)**, email addresses domain must use the current selected sub-domain.


1. Configure **push notification** settings.

     ![](../assets/preset-push.png)
   
    * Select at least one platform: iOS and/or Android
    
    * Select the mobile applications to use for each platform. 
        
        For more on how to configure your environment to send push notifications, refer to [this section](../push-configuration.md).

1. Once all the parameters have been configured, click **[!UICONTROL Submit]** to confirm. You can also save the message preset as draft and resume its configuration later on.

    ![](../assets/preset-submit.png)

1. Once the message preset has been created, it displays in the list with the **[!UICONTROL Processing]** status.

    During this step, several checks will be performed to verify that it has been configured properly. The processing time is around 48h-72h, and can take up to 7-10 days.

    These checks include deliverability tests that are performed by Adobe deliverability team:

    * SPF validation
    * DKIM validation
    * MX record validation
    * Check IPs denylisting
    * Helo host check
    * IP pool verification
    * A/PTR record, t/m/res subdomain verification

1. Once the checks are successfull, the message preset gets the **[!UICONTROL Active]** status. It is ready to be used to deliver messages.

    <!-- later on, users will be notified in Pulse -->

    ![](../assets/preset-active.png)

## Monitor message presets

All your message presets display in the **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** menu. Filters are available to help you browse through the list (channel type, user, status).

![](../assets/preset-filters.png)

Message presets can have the following statuses:

* **[!UICONTROL Draft]**: The message preset has been saved as a draft and has not been submitted yet. Open it to resume the configuration.
* **[!UICONTROL Processing]**: The message preset has been submitted and is going through several verifications steps.
* **[!UICONTROL Active]**: The message preset has been verified and can be selected to create messages.
* **[!UICONTROL Failed]**: One or several checks have failed during the message preset verification.
* **[!UICONTROL De-activated]**: The message preset is de-activated. It cannot be used to create new messages.

## Edit message presets

To edit a message preset, you first need to de-activate it to make it unavailable to create new messages (published messages using this preset will not be affected and will continue working). You then need to duplicate the message preset to create a new version that you will use to create new messages:

1. Access the message presets list, then deactivate the message preset that you want to edit.

    ![](../assets/preset-deactivate.png)

1. Duplicate the de-activated message preset. A copy with the **[!UICONTROL Draft]** status is automatically added to the list.

    ![](../assets/preset-duplicated.png)

1. Open the duplicated message preset, modify it according to your needs, then submit your changes. The message preset will go through the same validation cycle as during the [creation step](#create-message-preset).

1. Once validated, it gets the **[!UICONTROL Active]** status and is ready to be used to create new messages.

    >[!NOTE]
    >
    >Deactivated message presets cannot be deleted to avoid any issue in journeys using these presets to send messages.

