---
title: Use personalized offers in an email
description: Learn how to add personalized offers to your messages
---
# Configure and add personalized offers in an email {#configure-add-personalized-offers-email}

![](../assets/do-not-localize/badge.png)

In this exercise you’ll improve your newsletter email message with personalized offers based on a decision you previously created.

This is an end-to-end example to show how to configure offers and use them in a email.

## Main steps

1. Before creating offers, define your components:
    
    * Create placements
    * Create decision rules
    * Create tags (optional?)
    * Create rankings(?)

    Learn more in [this section](#define-components)

1. Configure the offers

    * Create offers
    * Inside each offer:
        
        * Create representations, and select a placement and an asset for each representation
        * Add a rule for each offer
        * Define a priority for each offer

        Learn more in [this section]()

1. Create a fallback offer

    Learn more in [this section]()

1. Create a collection to include the offers you just created

    Learn more in [this section]()

1. Configure the decision:

    * Create a decision
    * Select the placements you created
    * For each placement, select the collection
    * Select the fallback

    Learn more in [this section]()

1. Insert the decision in an email

    * Select a placement matching the offers you want to display
    * Select the decision from the items compatible with the selected placement 
    * Preview your offers

    Learn more in [this section]()

## Define the components {#define-components}

To create an offer decision, follow the main steps below:

1. Start by creating **placements** for your offers. You will then use these placements to define where the resulting offer will appear when defining your offer decision. Learn more on placements in [this section](). In this example, create three placements:

    * *Web - Image* placement
    * *Email - Image* placement
    * *Non-digital - Text* placement

1. Create **decision rules**, that will provide the best offer to a profile in the Adobe Experience Platform. Let's configure two simple rules by using the **[!UICONTROL XDM Individual Profile > Person > Gender]** attribute:

    * *Male Customers*
    * *Female Customers*

    Learn more on rules in [this section]().

1. If you want to define rules that will determine which offer should be presented first for a given placement (rather than taking into account the offers' priority scores), you can create a [**ranking formula**](../../using/offers/offer-library/create-ranking-formulas.md#about-ranking-formulas).

    Learn how to create a ranking formula in [this section](../../using/offers/offer-library/create-ranking-formulas.md#create-ranking-formula).

1. You can also create a **tag**. You will then be able to associate it to your offers and use this tag to group your offers together into a collection.

    In this example, create the *Yoga* tag.

    Learn how to create tags in [this section](../../using/offers/offer-library/creating-tags.md).

## Configure offers

1. Create an offer.

1. In this offer, create three representations (combinations of a placement that you created earlier and an asset):

    * One corresponding to the *Web - Image* placement
    * One corresponding to the *Email - Image* placement
    * One corresponding to the *Non-digital - Text* placement

1. Select an appropriate image for the first two placements and enter custom text for the last placement. Learn more on representations in [this section](../../using/offers/offer-library/creating-personalized-offers.md#representations).

1. In the Offer eligiblity section, select By defined decision rule and click the + icon to add the rule Female Customers.

1. Fill out the priority.

1. Click Save and approve.

1. Create three more offers with the same representations but with different assets. Assign them one of the two rules and define a different priority for each one.

## Create a fallback offer

## Create a collection

1. To speed up the decision process, create a collection.

1. Select the four Personalized Offers you created in the previous exercises. You can use the tag you created earlier.

## Configure the decision

1. Create your decision: select the Placements Web - Image, Email - Image and Non-digital - Text by clicking the + icon on the Placement. For each placement, add the collection you just created. Select the fallback offer that you created.

1. Save and activate.

You’ve now successfully configured your Decision. Your Decision is now live, and can be used to deliver optimized and personalized offers to your customers, in real-time.

## Insert the decision in an email

To insert a decision into an email message, follow the steps below:

1. Create your email, then open the [Email Designer](design-emails.md) to configure its content.

1. Add a structure component from the left palette.

1. Add an **[!UICONTROL Offer decision]** content component (see [Use content components](content-components.md)).

    ![](assets/deliver-offer-component.png)

1. Select it and in the right palette, click **[!UICONTROL Select offer decision]** to add an offer activity.

    ![](assets/deliver-offer-tab.png)

1. Select the placement corresponding to the offers that you want to display.

    Placements are containers that are used to showcase your offers. In this example, select **Email - Image** from the **[!UICONTROL Placements]** dropdown menu. This placement has been created in the Offer Library to display image-type offers in emails. Learn more on [creating placements](../../using/offers/offer-library/creating-placements.md).

    ![](assets/deliver-offer-select-placement.png)

    Decisions matching the the "email image" placement are displayed.

    >[!NOTE]
    >
    >Only decisions that are compatible with the selected placement display in the list.
    
1. Select the decision to use in the content component, then click **[!UICONTROL Add]**.

    ![](assets/deliver-offer-placement.png)

1. You can now see all personalized offers and the fallback offer being visualized in the Email Designer.

    ![](assets/deliver-offer-offers-displayed.png)

1. Use the **[!UICONTROL Offers]** section or the content components arrows (right and left arrows) to browse data.

    ![](assets/deliver-offer-preview.png)

1. To display the different offers that are part of the decision with a customer profile, click **[!UICONTROL Preview]**.

    ![](assets/deliver-offer-preview-button.png)

    >[!NOTE]
    >
    >You need to have test profiles available to be able to preview your messages. Learn how to [create test profiles](create-test-profile.md).


1. To choose the namespace to use to identify test profiles, select **[!UICONTROL Email]** from the **[!UICONTROL Identity namespace]** field.

    ![](assets/deliver-offer-identity-namespace.png)

    >[!NOTE]
    >
    >In this example, we will use the **Email** namespace. Learn more about Adobe Experience Platform identity namespaces [in this section](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=en#getting-started).

1. In the list of identity namespaces, select **[!UICONTROL Email]**. Click **[!UICONTROL Select]**.

    ![](assets/deliver-offer-identity-namespace-email.png)

1. In the **[!UICONTROL Identity value]** field, enter the value to identify the test profile. In this example, enter the email address of a test profile.

    For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.

    Add other profiles so that you can test different variants of the message depending on the profile data.

    ![](assets/deliver-offer-test-profiles.png)

1. Click the **[!UICONTROL Preview]** tab to test your message.

1. Select a test profile. You can check the values available in the columns.

    ![](assets/deliver-offer-test-profiles-preview.png)

1. Select other test profiles to preview the email content for each variant of your message.

    In the message content, the offer corresponding to the selected test profile is displayed.

Learn more on the detailed steps to [check the message preview](#preview-your-messages).

After saving your changes and once the message is published, your offers are ready to be displayed to the relevant profiles when sending the message as part of a journey.

Learn how to publish messages in [this section](publish-manage-message.md).

Learn how messages are triggered by one or more journeys in [this section](building-journeys/journey.md).

