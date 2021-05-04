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

With Journey Optimizer, you can set up message presets that define all the technical parameters required for email and push notification messages (email type, sender email and name, mobile apps, etc.).

You can set up as many message presets as desired according, depending on the different brands you need to communicate for.

Once message presets have been configured, you be able to select them when creating messages from the **[!UICONTROL Presets]** list.

## Create a message preset {#create-message-preset}

To create a message preset, follow these steps:

1. Access the **[!UICONTROL Message Configuration]** / **[!UICONTROL Message presets]** menu, then click **[!UICONTROL Create message preset]**.

    ![](../assets/preset-create.png)

1. Provide a name and a description (optional) for the preset, then specify the channel(s) that you want to configure.

    ![](../assets/preset-general.png)

1. Configure the email and push notification settings:

    For the email channel, specify:

    * The type of communications that will be sent with the preset (transactional or marketing messages),
    * The [subdomain](about-subdomain-delegation.md) to use to send the emails,
    * The [IP pool](ip-pools.md) to link to the preset,
    * The header parameters to use for your emails sent using the preset.

    ![](../assets/preset-email.png)

    For the push notification channel, specify the IOS and/or Android mobile applications to use for your messages.

    ![](../assets/preset-push.png)

1. Once all the parameters have been configured, click **[!UICONTROL Submit]** to confirm. You can also save the message preset as draft and resume its configuration later on.

    ![](../assets/preset-submit.png)

1. Once the message preset has been created, it displays in the list with the **[!UICONTROL Processing]** status.

    During this step, several checks will be performed to verify that it has been configured properly. The processing time is around 48h-72h, and can take up to 7-10 days.

    You can track the verification process by opening the message preset from the list.

    -SCREENSHOT SHOWING THE TWO CHECKS-

    !!no processing preset on stage + unable to submit a preset 

    * **xxxx**: 
    * **Audit step**: deliverability tests are performed by Adobe deliverability team. This step can take up to 10 days if some steps fail during the audit. The checks include:

        * SPF validation,,
        * DKIM validation
        * MX record validation,
        * Check IPs blacklisting,
        * Helo host check,
        * IP pool verification,
        * A/PTR record, t/m/res subdomain verification.

1. Once the checks are successfull, the message preset gets the **[!UICONTROL Active]** status. It now ready to be used to deliver messages.

## Manage and edit message presets

All your message presets display in the **[!UICONTROL Message Configuration]** / **[!UICONTROL Message presets]** menu. Filters are available to help you browse through the list (channel type, user, status).

![](../assets/preset-filters.png)

Message presets can have the following statuses:

* **[!UICONTROL Draft]**: The message preset has been saved as a draft and has not been submitted yet. Open it to resume the configuration.
* **[!UICONTROL Processing]**: The message preset has been submitted and is going through several verifications steps.
* **[!UICONTROL Active]**: The message preset has been verified and can be selected to create messages.
* **[!UICONTROL Failed]**: One or several checks have failed during the message preset verification.
* **[!UICONTROL De-activated]**: The message preset is de-activated. It cannot be used to create messages.

To edit a message preset, you first need to de-activate it to make it unavailable to create new messages (published messages using this preset will not be affected and will continue working).

You then need to duplicate the message preset to create a new version to use to create new messages:

1. Access the message presets list, then deactivate the message preset that you want to edit.

    ![](../assets/preset-deactivate.png)

1. Duplicate the de-activated message preset. A copy with the **[!UICONTROL Draft]** status is automatically added to the list.

    ![](../assets/preset-duplicated.png)

1. Open the duplicated message preset, modify it according to your needs, then submit your changes. The message preset will go through the same validation cycle as during the [creation step](#create-message-preset).

1. Once validated, it gets the **[!UICONTROL Active]** status and is ready to be used to create new messages.

    ![](../assets/preset-active.png)

<!--que fait-on ensuite avec l'ancienne version deactivated: reste là pour être utilisée par les anciens messages?). quand un deactivate preset est-il enlevé de la liste?-->
