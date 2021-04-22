---
title: Configure a push notification
description: Learn how to create a push notification in Customer Journey Management
page-status-flag: never-activated
uuid: 
contentOwner:
products:
audience: customer journey management content designer
content-type: reference
topic-tags: starting-with-creating-content
discoiquuid:
internal: n
snippet: y
---
# Configure a push notification {#create-push-notification}

![](assets/do-not-localize/badge.png)

Push notification are configured when creating a message, in the **[!UICONTROL Push Notification]** tab (see [Create a message](create-message.md)).

You can configure push notification contents for iOS or Android operating systems using the dedicated tabs.

![](assets/create-content-push.png)

The steps to configure a push notification are as follows:

1. Select the **[!UICONTROL Silent Notification]** option to silently notify the application without any message or content for the end user. The user is not made aware of the notification’s arrival. It is transferred directly to the application.

    A typical use case for this type of message would be to make the application aware that there is content available on the server to be downloaded.

1. Compose your message. To do this, click the button on the right-hand side of the **[!UICONTROL Title]** and **[!UICONTROL Message]** fields to open the Expression Editor.

    >[!NOTE]
    >
    >Note that the **[!UICONTROL Compose Message]** section is common to both the **[!UICONTROL iOS]** and **[!UICONTROL Android]** tabs. Any change in this section will apply to both operating systems.

1. Select the action to perform when the recipients click the push notification:

    * **[!UICONTROL Open app]**: opens the application configured with the **[!UICONTROL Preset]** that has been selected when creating the content.
    * **[!UICONTROL Deep link]**: redirects the recipients to content located inside the application instead of opening a web browser page.
    * **[!UICONTROL Web URL]**: redirects the recipients to an external URL.

1. Configure the **[!UICONTROL Advanced options]**. Available parameters are:

    |Parameter | Availability | Description |
    |---------|----------|---------|
    |**[!UICONTROL Collapsible]**| iOS / Android | A collapsible message is a message that may be replaced by a new one. For example, an application that updates users with the latest news about a topic. In that case, only the most recent message is relevant. On the other hand, with non-collapsible messages, every message is important to the client app and needs to be delivered. |
    |**[!UICONTROL Custom sound]**| iOS / Android | The sound to be played by the mobile terminal when the notification is received. The sound needs to be bundled in the app.|
    |**[!UICONTROL Badges]**| iOS / Android | A badge is used to display directly on the application icon the number of new unread information. <br/>The badge value will disappear as soon as the user opens or reads the new content from the application. When a notification is received on a device, it can refresh or add a badge value for the related app.<br/>For example, if you are storing the number of unread articles of your customers, you can leverage personalization to send the unique unread articles badge value for each customer. For more personalization, refer to [this section](personalization/personalize.md).|
    |**[!UICONTROL Notification group]** /  | iOS | Associate a notification group to the push notification.<br/>Starting with iOS 12, notification groups allow you to consolidate message threads and notification topics into thread IDs. For example, a brand might send marketing notifications under one group ID, while keeping more operational type notifications under one or more different IDs.<br/>To illustrate this, you can have groupID: 123 "check out the new spring collection of sweaters" and groupID: 456 "your package was delivered" notification groups. In this example, all delivery notifications would be bundled under group ID: 456.|
    |**[!UICONTROL Notification channel]** | Android | Associate a notification channel to the push notification.<br/>Starting in Android 8.0 (API level 26), all notifications must be assigned to a channel in order to display. For more on this, refer to the [Android developer documentation](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels).|
    |**[!UICONTROL Add content-availability flag]**| iOS | Sends the content available flag in the push payload to ensure that the app is woken up as soon as it receives the push notification, meaning that the app will be able to access the payload data.<br/> This works even if the app is running in the background and without needing any user interaction (e.g. tapping on Push notification). However, this does not apply if the app is not running. For more on this, refer to the [Apple developer documentation](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
    |**[!UICONTROL Add mutable-content flag]**| iOS | Sends the mutable-content flag in the push payload and will allow the push notification content to be modified by a notification service application extension provided in iOS SDK. For more on this, refer to [Apple developer documentation](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>You can then leverage your mobile app extensions to further modify the content or presentation of arriving push notifications sent from Customer Journey Management. For example, users can leverage this option to decrypt data, change the body or title text of a notification, add a thread identifier to a notification etc.|
    |**[!UICONTROL Notification visibility]**| Android | Defines the push notification's visibility. <b>private</b> will show the notification on all lockscreens, but conceal sensitive or private information on secure lockscreens. <b>Public</b> will show the notification in its entirety on all lockscreens. <b>Secret</b> will not reveal any part of the notification on a secure lockscreen. For more on this, refer the [Android developer documentation](https://developer.android.com/reference/android/app/Notification).|
    |**[!UICONTROL Notification priority]**| Android | Defines the push notification's importance from Low to Max. This determines how "intrusive" the push notification will be when it is delivered. For more on this, refer to the [Android developer documentation](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance)|
    |**[!UICONTROL Delivery priority]**| Android | Sets up a high or normal priority for your push notifications. For more information on message priority, refer to the [Google developer documentation](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message).|

1. In the **[!UICONTROL Custom data]** section, you can add custom variables to the payload, depending on your mobile application configuration. For more on how to set up push notifications in Adobe Experience Platform and Adobe Launch, refer to [this section](push-configuration.md)
