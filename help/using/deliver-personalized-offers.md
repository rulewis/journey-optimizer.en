---
title: Add personalized offers
description: Learn how to add personalized offers to your messages
---
# Add personalized offers {#deliver-personalized-offers}

![](assets/do-not-localize/badge.png)

## About Decision Management {#about-offer-decisioning}

With [!DNL Journey Optimizer], you can insert in your email messages decisions (previously known as offer activities) that will leverage the Offer Decision Engine in order to pick the best offer to deliver to your customers.

For example, you can add a decision that will display in your email a special discount offer that will vary according to the recipient's loyalty level.

For more on how to create and manage offers, refer to [this section](offers/get-started/starting-offer-decisioning.md).

## Insert a decision in an email {#insert-offers}

>[!CAUTION]
>
>You need to first define an offer decision. Learn how to create decisions in [this section](../../using/offers/offer-activities/create-offer-activities.md).

To insert a decision into an email message, follow the steps below:

1. Create your email, then open the Email Designer to configure its content.

1. Add an **[!UICONTROL Offer decision]** content component.

    ![](assets/deliver-offer-component.png)

    Learn how to use content components in [this section](content-components.md).

1. The **[!UICONTROL Offer decision]** tab displays in the right palette. Click **[!UICONTROL Select Offer decision]**.

    ![](assets/deliver-offer-tab.png)

1. Select the placement corresponding to the offers that you want to display.

    [Placements](../../using/offers/offer-library/creating-placements.md) are containers that are used to showcase your offers. In this example, we will use the "email top image" placement. This placement has been created in the Offer Library to display image-type offers situated to the top of messages.

1. Select the offer activity to use in the content component, then click **[!UICONTROL Add]**.

    >[!NOTE]
    >
    >Only decisions that are compatible with the selected placement display in the list. In this example, only one offer activity matches the "email top image" placement.

    ![](assets/deliver-offer-placement.png)

1. The offer activity is now added to the component. You can preview the different offers that are part of the decision using the **[!UICONTROL Offers]** section or the content components arrows.

    ![](assets/deliver-offer-preview.png)

1. You can also display the different offers that are part of the decision with a customer profile using the **[!UICONTROL Preview]** button.

    Learn more on the detailed steps to [check the message preview](#preview-your-messages).
    
For a full end-to-end example showing how to configure offers, use them in a decision and leverage this decision in an email, check out [this section](../../using/offers/offers-e2e.md#insert-decision-in-email/gi).
