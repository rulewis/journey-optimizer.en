---
title: Add a message in a journey
description: Add a message in a journey
feature: Journeys
topic: Content Management
role: User
level: Intermediate
---
# Add a message in a journey

[!DNL Journey Optimizer] message capabilities are built-in, you just need to design your content and publish your message. See [this section](../get-started-content.md). Then you simply add, in your journey, a push or email message designed using Journey Optimizer. 

If you're using a third-party system to send your messages, you can create a custom action. Learn more in this [section](../action/action.md).

## Adding a Message activity

1. As always, start your journey with an event or a **Read Segment** activity.

   ![](../assets/jo-message0.png)

1. From the **Actions** section of the palette, drag and drop a **Message** activity into the canvas.  

   ![](../assets/jo-message1.png)

1. Add a label and description.

   ![](../assets/jo-message2.png)

1. Click inside the **Message** field. The list of available messages designed in Journey Optimizer is displayed. You can filter the list by status. 

   ![](../assets/jo-message3.png)

1. Choose a message and click **Select**. You can also create a new message directly from this screen by clicking **Create new**.

   ![](../assets/jo-message4-ter.png)

   If you want to check your message, you can click the **Open the message** icon in the **Message** field. The message will open in a new tab.

   ![](../assets/jo-message4-bis.png)

1. Add the next steps to your journey.

## Email parameters and push parameters

The **[!UICONTROL Email parameters]** and **[!UICONTROL Push parameters]** sections show read-only fields. You typically perform this configuration when creating the message. See [this section](../get-started-content.md). 

![](../assets/jo-message4.png)

To force a specific value, you can use the **Enable parameter override** icon to the right of the field. This option may be useful for testing purposes. For example, for an email, you can add your email address. After you have published the journey, the email is sent to you.
