---
title: Content branding
description: Learn how xxxx
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

# Create message presets

With [!DNL Journey Optimizer], you can set up message presets that define all the technical parameters required for email and push notification message: email type, sender email and name, mobile apps, and more.

You can set up as many message presets as needed depending on your different brands and usage of the product.

Once message presets have been configured, you be able to select them when creating messages from the **[!UICONTROL Presets]** list.

## Create a message preset {#create-message-preset}

To create a message preset, follow these steps:

1. Access the **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** menu, then click **[!UICONTROL Create Message preset]**.

    ![](../assets/preset-create.png)

1. Enter a name and a description (optional) for the preset, then specify the channel(s) that you want to configure.

    ![](../assets/preset-general.png)

1. Configure the message settings.

    For the **email** channel, define the following settings:

    ![](../assets/preset-email.png)

    * The type of message that will be sent with the preset: **Transactional** or **Marketing**

        >[!CAUTION]
        >
        > Transactional messages can be sent to profiles who unsubscribed from communications, or to addresses added to the suppression list after hard bounces for example. These messages can only be sent in specific contexts, such as password reset.
        >
    
    * The [subdomain](about-subdomain-delegation.md) to use to send the emails
    * The [IP pool](ip-pools.md) to associate with the preset
    * The header parameters to use for the emails sent using the preset

    For the **push notification** channel, define the following settings:

     ![](../assets/preset-push.png)
   
    * Select at least one platform: IOS and/or Android
    
    * Select the mobile applications to use for each platform 
        
        For more on how to configure your environment to send push notifications, refer to [this section](../push-configuration.md).

1. Once all the parameters have been configured, click **[!UICONTROL Submit]** to confirm. You can also save the message preset as draft and resume its configuration later on.

    ![](../assets/preset-submit.png)

1. Once the message preset has been created, it displays in the list with the **[!UICONTROL Processing]** status.

    During this step, several checks will be performed to verify that it has been configured properly. The processing time is around 48h-72h, and can take up to 7-10 days.

    These checks include deliverability tests that are performed by Adobe deliverability team:

    * SPF validation,
    * DKIM validation,
    * MX record validation,
    * Check IPs blacklisting,
    * Helo host check,
    * IP pool verification,
    * A/PTR record, t/m/res subdomain verification.

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
    >De-activated message presets cannot be deleted to avoid any issue in journeys using these presets to send messages.

<!-- To add when questions are answered + add link to this section in Create message presets section.

## Header parameters

The fields below allow you to enter information necessary to elaborate email message headers. This information can be personalized??

>[!NOTE]
>
>All fields are required.


To define the name and address of the sender which will appear in the header of messages sent, edit the settings below:

**[!UICONTROL Sender email]**: Address of the sender

**[!UICONTROL Sender name]**: Name of the sender. you can change the sender name

**[!UICONTROL Reply to (email)]**: The email address to use when the recipient clicks the Reply button in their e-mail client software,

**[!UICONTROL Reply to (name)]**: The name, which is customizable, that will be used when the recipient clicks the Reply button in their e-mail client software,

**[!UICONTROL Reply to (forward email)]**:
Cf. https://jira.corp.adobe.com/browse/CJM-9824

**[!UICONTROL Error email]**: Email address of messages with errors. This is the technical address used to handle bounce mail, including emails received by the AJO server due to non-existent target addresses.
This fields is automatically populated with the value you add in the Reply to (forward email) field.

>[!NOTE]
>
>The sender’s address will be used for replies by default.
>The header parameters must not be empty. By default, they contain the values input >when configuring the deployment wizard??
>The sender’s address is mandatory to allow an email to be sent (RFC standard).
Journey Optimizer checks the syntax of email addresses entered.

>[!CAUTION]
>
>In the context of the checks implemented by Internet Access Providers (ISPs) to combat unsolicited email (spam), Adobe recommends creating email accounts that correspond to the addresses specified for deliveries and replies. Check with your messaging system administrator.-->

