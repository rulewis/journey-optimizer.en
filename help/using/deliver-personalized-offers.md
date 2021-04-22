---
title: Add personalized offers
description: Learn how to deliver personalized offers to your customers using the Offer Decisioning service.
page-status-flag: never-activated
uuid: 
contentOwner:
products:
content-type: reference
topic-tags: 
discoiquuid:
internal: n
snippet: y
---
# Add personalized offers {#deliver-personalized-offers}

![](assets/do-not-localize/badge.png)

## About Offer Decisioning {#about-offer-decisioning}

With Customer Journey Management, you can insert in your email messages offer activities that will leverage the Offer Decision Engine in order to pick the best offer to deliver to your customers.

For example, you can add an offer activity that will display in your email a special discount offer that will vary according to the recipient's loyalty level.

Offers activities are made up of several components: personalized offers, fallback offers, tags, decision rules, and placements. They are all created in Adobe Experience Platform Offer Library. For more on how to work with the Offer Library, refer to the [Offer Decisioning documentation](https://experienceleague.adobe.com/docs/offer-decisioning/using/offer-decisioning-home.html).

## Insert an offer activity in an email {#insert-offers}

To insert an offer activity into an email message, follow the steps below:

1. Create your email, then open the Email Designer to configure its content.

1. Add an **[!UICONTROL Offer decision]** content component (see [Use content components](content-components.md)).

    ![](assets/deliver-offer-component.png)

1. An **[!UICONTROL Offer decision]** tab is added to the component. Click **[!UICONTROL Add personalization - Offer decision]** to add an offer activity.

    ![](assets/deliver-offer-tab.png)

1. Select the placement corresponding to the offers that you want to display.

    Placements are containers that are used to showcase your offers. In this example, we will use the "email top image" placement. This placement has been created in the Offer Library to display image-type offers situated to the top of messages.

1. Select the offer activity to use in the content component, then click **[!UICONTROL Add]**.

    >[!NOTE]
    >
    >Note that only Offer activities that are compatible with the selected placement display in the list. In this example, only one offer activity matches the "email top image" placement.

    ![](assets/deliver-offer-placement.png)

1. The offer activity is now added to the component. You can preview the different offers that are part of the offer activity using the **[!UICONTROL Offers]** section or the content components arrows.

    ![](assets/deliver-offer-preview.png)
