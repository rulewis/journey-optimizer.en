---
title: Create a message
description: Learn how to create a message
page-status-flag: never-activated
uuid: 
contentOwner:
products:
audience: send messages
content-type: reference
topic-tags: 
discoiquuid:
internal: n
snippet: y
---
# Create a message {#create-message}

![](assets/do-not-localize/badge.png)

This section describes all the steps needed to create a message.

Messages are available from the **[!UICONTROL Messages]** shortcut on the left. All messages are listed, sorted by publication date (for published messages) or creation date (for draft messages).

>[!NOTE]
>
>Every user can access, create, edit and publish messages. Learn more about user permissions [in this section](permissions.md).

![](assets/messages-list.png)

Use the **[!UICONTROL Show recents]** toggle to add direct links to the messages you accessed in the last 5 days.

![](assets/show-recent-messages.png)

Use the filter icon to display only drafted, published or messages being published. You can also search on message label, as below:

![](assets/filter-messages.png)

To create a new message, follow the steps below:

1. Access the message list, then click **[!UICONTROL Create Message]**.

1. Configure the message properties:

    ![](assets/create-message-properties.png)
    
    * Enter a **[!UICONTROL Title]** (mandatory) and a **[!UICONTROL Description]**. 

    * Select the **[!UICONTROL Preset]** to use for the message.

        Presets include all the parameters that are required for an email or push notification to be sent according to your different brands: from address, reply-to address, mobile application, etc. These fields are read-only. [Learn more about branding](administration.md#cjm-branding).

    * Select the channel(s) you want to use for that message: Email and/or Push notification. You must select at least one channel to be able to create the message.

1. Click **[!UICONTROL Create]**: your message is now created and added in the message list, with the **[!UICONTROL Draft]** status. You can create the content of the message and adapt settings.

    One tab is available for each selected channel. Use these tabs to configure the content for each channel. You can remove a tab by selecting it and clicking the **[!UICONTROL Delete channel]** button on the right. 

    Detailed information on email and push notification configuration is available in these sections:
    * [Configure emails](configure-email.md)
    * [Configure push notifications](configure-push.md)


    ![](assets/create-messages-content.png)

    >[!NOTE]
    >   
    >You can personalize your messages using profiles' data. Personalization is available in any field that can be modified using the Expression Editor. For more on personalization, refer to [this section](personalization/personalize.md).
    
    Note that you can access and modify the message's title, description and preset at any time using the **[!UICONTROL Properties]** button.

    ![](assets/message-properties.png)
    
1. Check the rendering of your push notification and/or email using the preview section on the left-hand side.

    To preview the message personalization using test profiles, use the **[!UICONTROL Preview]** button. For more on this, refer to [this section](preview.md).

    ![](assets/messages-simple-preview.png)

1. Check alerts in the upper section of the editor.  Some of them are simple warnings, while others can prevent you from publishing the message as long as they are not resolved. Learn more in [this section](alerts.md).

1. You can now publish your message by clicking the **[!UICONTROL Publish]** button, or keep it as a draft and publish it later on. For more on how to publish messages, refer to [this section](publish-manage-message.md).
