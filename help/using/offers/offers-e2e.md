* ---
title: Use personalized offers in an email
description: Learn how to add personalized offers to your messages
---
# Configure and add personalized offers in an email {#configure-add-personalized-offers-email}

![](../assets/do-not-localize/badge.png)

In this exercise you’ll improve your newsletter email message with personalized offers based on a decision you previously created.

This is an end-to-end example to show how to configure offers and use the relevant offers in a email.

## Main steps

The key steps to configure offers, include them in a decision and leverage this decision in an email are listed below:

1. Before creating offers, define your components:
    
    * Create placements
    * Create decision rules
    * Create tags
    * Create rankings (optional)

    [!DNL :bulb:] Learn more in [this section](#define-components)

1. Configure the offers

    * Create offers
    * Inside each offer:
        
        * Create representations, and select a placement and an asset for each representation
        * Add a rule for each offer
        * Define a priority for each offer

        [!DNL :bulb:] Learn more in [this section](#configure-offers)

1. Create a fallback offer

    [!DNL :bulb:] Learn more in [this section](#create-fallback)

1. Create a collection to include the offers you just created

    [!DNL :bulb:] Learn more in [this section](#create-collection)

1. Configure the decision:

    * Create a decision
    * Select the placements you created
    * For each placement, select the collection
    * Select the fallback

    [!DNL :bulb:] Learn more in [this section](#configure-decision)

1. Insert the decision in an email

    * Select a placement matching the offers you want to display
    * Select the decision from the items compatible with the selected placement 
    * Preview your offers

    [!DNL :bulb:] Learn more in [this section](#insert-decision-in-email)

The overall Decision Management process can be described as follows:

![](assets/.png)

## Define the components {#define-components}

Before starting to create offers, you must define several components that you will use in your offers.

You will find them under the **[!UICONTROL Decision Management]** > **[!UICONTROL Components menu]**.

1. Start by creating **placements** for your offers.

    You will use these placements to define where the resulting offer will appear when defining your offer decision.

    In this example, create three placements with the following channel and content types:

    * *Web - Image*
    * *Email - Image*
    * *Non-digital - Text*

    ![](../assets/offers-e2e-placements.png)

    The detailed steps to create placements are described in [this section]().

1. Create **decision rules**.

    Decision rules will provide the best offer to a profile in the Adobe Experience Platform.
    
    Configure two simple rules by using the **[!UICONTROL XDM Individual Profile > Person > Gender]** attribute:

    * *Female Customers*
    * *Male Customers*

    ![](../assets/offers-e2e-rules.png)

    The detailed steps to create rules are described in [this section]().

1. You can also create a **tag**.

    You will then be able to associate it to your offers and use this tag to group your offers together into a collection.

    In this example, create the *Yoga* tag.

    ![](../assets/offers-e2e-tag.png)

    The detailed steps to create tags are described in [this section](../../using/offers/offer-library/creating-tags.md).

1. If you want to define rules that will determine which offer should be presented first for a given placement (rather than taking into account the offers' priority scores), you can create a [**ranking formula**](../../using/offers/offer-library/create-ranking-formulas.md#about-ranking-formulas).

    The detailed steps to create ranking formulas are described in [this section](../../using/offers/offer-library/create-ranking-formulas.md#create-ranking-formula).

    >[!NOTE]
    >
    >In this example, we will only use the priority scores. Learn more on [eligibility rules and constraints](../../using/offers/offer-library/creating-personalized-offers.md#eligibility).


## Configure offers {#configure-offers}

You can now create and configure your offers. In this example, you will create four offers corresponding to the four offers you want to display according to each profile and priority(?).

1. Create an offer. Learn more in [this section](../../using/offers/offer-library/creating-personalized-offers.md#create-offer).

1. In this offer, create three representations (combinations of a placement that you created earlier and an asset):

    * One corresponding to the *Web - Image* placement
    * One corresponding to the *Email - Image* placement
    * One corresponding to the *Non-digital - Text* placement

    Learn more on representations in [this section](../../using/offers/offer-library/creating-personalized-offers.md#representations).

    >[!NOTE]
    >
    >An offer can be displayed at different places in a message to create more opportunities to use the offer in different placement contexts.

1. Select an appropriate image for the first two placements. Enter custom text for the *Non-digital - Text* placement.

    ![](../assets/offers-e2e-representations.png)

1. In the **[!UICONTROL Offer eligiblity]** section, select **[!UICONTROL By defined decision rule]** and drag and drop the rule of your choice.

    ![](../assets/offers-e2e-eligibility.png)

1. Fill out the priority. In this example, add *25*.

1. Review your offer, then click **[!UICONTROL Save and approve]**.

    ![](../assets/offers-e2e-review.png)

1. Create three more offers with the same representations but with different assets. Assign them one of the two rules and define a different priority for each one.

The detailed steps to create and configure offers are described in [this section]().

## Create a fallback offer {#create-fallback}

Create a fallback offer with the same representations as for the offers, with appropriate assets.

![](../assets/offers-e2e-fallback.png)

The detailed steps to create and configure a fallback offer are described in [this section]().

## Create a collection {#create-collection}

1. To speed up the decision process, create a collection.

1. Select the four Personalized Offers you created in the previous exercises. You can use the tag you created earlier.

The detailed steps to create and configure a collection are described in [this section]().

## Configure the decision {#configure-decision}

To create and configure an offer decision, follow the main steps below:

1. Create your decision.

1. Select the Placements Web - Image, Email - Image and Non-digital - Text by clicking the + icon on the Placement.

1. For each placement, add the collection you just created. Select the fallback offer that you created.

1. Save and activate.

You’ve now successfully configured your Decision. Your Decision is now live, and can be used to deliver optimized and personalized offers to your customers, in real-time.

## Insert the decision in an email {#insert-decision-in-email}

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

    ![](assets/deliver-offer-identity-namespace.png)****

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

