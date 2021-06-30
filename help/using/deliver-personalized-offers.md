---
title: Add personalized offers
description: Learn how to add personalized offers to your messages
feature: Journeys
topic: Content Management
role: User
level: Intermediate
---
# Add personalized offers {#deliver-personalized-offers}

In [!DNL Journey Optimizer] email messages, you can insert decisions (previously known as 'offer activities') that will leverage the Offer Decision Engine in order to pick the best offer to deliver to your customers.

For example, you can add a decision that will display in your email a special discount offer that will vary according to the recipient's loyalty level.

For more on how to create and manage offers, refer to [this section](offers/get-started/starting-offer-decisioning.md).

For a **full end-to-end example** showing how to configure offers, use them in a decision and leverage this decision in an email, check out [this section](offers/offers-e2e.md#insert-decision-in-email).

![](assets/do-not-localize/how-to-video.png) [Learn how to add offers as personalization in this video](#video-offers)

## Insert a decision in an email {#insert-offers}

>[!CAUTION]
>
>Before starting, you must [define an offer decision](offers/offer-activities/create-offer-activities.md).

To insert a decision into an email message, follow the steps below:

1. Create your email, then open the Email Designer to configure its content.

1. Add an **[!UICONTROL Offer decision]** content component.

    ![](assets/deliver-offer-component.png)

    Learn how to use content components in [this section](content-components.md).

1. The **[!UICONTROL Offer decision]** tab displays in the right palette. Click **[!UICONTROL Select Offer decision]**.

    ![](assets/deliver-offer-tab.png)

1. In the window that displays, select the placement corresponding to the offers that you want to display.

    [Placements](offers/offer-library/creating-placements.md) are containers that are used to showcase your offers. In this example, we will use the "email top image" placement. This placement has been created in the Offer Library to display image-type offers situated to the top of messages.

1. Select the offer activity to use in the content component, then click **[!UICONTROL Add]**.

    >[!NOTE]
    >
    >Only decisions that are compatible with the selected placement display in the list. In this example, only one offer activity matches the "email top image" placement.

    ![](assets/deliver-offer-placement.png)

The offer activity is now added to the component.
    

## Preview offers in an email {#preview-offers-in-email}

You can preview the different offers that are part of the decision added to the email using the **[!UICONTROL Offers]** section or the content components arrows.

![](assets/deliver-offer-preview.png)

To display the different offers that are part of the decision with a customer profile, follow the steps below.

1. Click **[!UICONTROL Preview]**.

    ![](assets/deliver-offer-preview-button.png)

    >[!NOTE]
    >
    >You need to have test profiles available to be able to preview your messages. Learn how to [create test profiles](building-journeys/creating-test-profiles.md).

1. To choose the namespace to use to identify test profiles, select **[!UICONTROL Email]** from the **[!UICONTROL Identity namespace]** field.

    >[!NOTE]
    >
    >In this example, we will use the **Email** namespace. Learn more about Adobe Experience Platform identity namespaces [in this section](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=en#getting-started).

1. In the list of identity namespaces, select **[!UICONTROL Email]** and click **[!UICONTROL Select]**.

1. In the **[!UICONTROL Identity value]** field, enter the value to identify the test profile. In this example, enter the email address of a test profile.

    <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

1. Add other profiles so that you can test different variants of the message depending on the profile data.

    ![](assets/deliver-offer-test-profiles.png)

1. Click the **[!UICONTROL Preview]** tab to test your message.

1. Select a test profile. The offer corresponding to the selected profile (a woman) is displayed.

    ![](assets/deliver-offer-test-profile-female-preview.png)

1. Select other test profiles to preview the email content for each variant of your message. In the message content, the offer corresponding to the selected test profile (now a man) is now displayed.

    ![](assets/deliver-offer-test-profile-male-preview.png)

Learn more on the detailed steps to check the message preview in [this section](#preview-your-messages).

## How-to video{#video-offers}

Learn how to add an offer decisioning component to messages in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)
