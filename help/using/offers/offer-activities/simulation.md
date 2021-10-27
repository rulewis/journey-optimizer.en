---
title: Create simulations
description: Learn how to create simulations
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
---

# Create simulations

## About simulation

To validate your decisioning logic, you can simulate which offers will be delivered to a test profile for a given placement.

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

This enables you to test and refine various versions of your offers with no impact on the targeted recipients.

To access this feature, select the **[!UICONTROL Simulation]** tab from the **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** menu.

![](../../assets/offers_simulation-tab.png)

<!-->
➡️ [Discover this feature in video](#video)
-->

## Add decision scopes

First you need to select the offer decisions that you want to test.

1. Select **[!UICONTROL Add decision scope]**.

    ![](../../assets/offers_simulation-add-decision.png)

1. Select a placement from the list.

    ![](../../assets/offers_simulation-add-decision-scope.png)

1. The available decisions are displayed.

    * You can use the search field to refine the selection.
    * You can click the **[!UICONTROL Open offer decisions]** link to open the list of all the decisions that you created. Learn more on [decisions](create-offer-activities.md).
    
    Select the decision of your choice and click **[!UICONTROL Add]**.

    ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. The decision scope you just defined displays in the main workspace.

    You can adjust the number of offers that you want to request. For example, if you select 2, the best 2 offers will display for this decision scope.

    ![](../../assets/offers_simulation-request-offer.png)

    >[!NOTE]
    >
    >You can request up to 30 offers.

1. Repeat the steps above to add as many decisions as you need.

    ![](../../assets/offers_simulation-add-more-decisions.png)

    >[!NOTE]
    >
    >Even if you define several decision scopes, only one decisioning request is run.

## Select test profiles

Now you need to select test profiles to view the results of your offer decisions on them.

1. Click **[!UICONTROL Manage profile]**.

    ![](../../assets/offers_simulation-manage-profile.png)

1. Select the identity namespace you want to use to identify test profiles. In this example, we will use the **Email** namespace.

    >[!NOTE]
    >
    >An identity namespace defines the context of an identifier such as an email address or CRM ID. Learn more about Adobe Experience Platform identity namespaces [in this section](get-started-identity.md){target="_blank"}.

1. Enter the identity value and click **[!UICONTROL View]** to list the available profiles.

    ![](../../assets/offers_simulation-add-profile.png)

1. Add other profiles if you want to test different profile data, and save your selection.

    ![](../../assets/offers_simulation-save-profiles.png)

1. Once added, all profiles are listed in the drop-down list under **[!UICONTROL Test profile]**. You can switch between the saved test profiles to display the results for each selected profile.

    ![](../../assets/offers_simulation-saved-profiles.png)

1. You can click the **[!UICONTROL Profile details]** link to display the selected profile data.

<!--Learn more on [selecting test profiles](preview.md#select-test-profiles)-->

## View simulation results

Once you added a decision scope and selected a test profile, you can view the results.

1. Click **[!UICONTROL View results]**.

    ![](../../assets/offers_simulation-view-results.png)

1. The best available offer(s) are displayed according to the selected profile for each decision.

    Select an offer to display its details.

    ![](../../assets/offers_simulation-offer-details.png)

1. Select another profile from the list to display the results of the offer decisions for a different test profile.

1. You can add, remove or update the decision scopes as many times as needed.

>[!NOTE]
>
>Each time you change profiles or update decision scopes, you need to refresh the results using the **[!UICONTROL View results]** button.

<!--Questions

* Is it recommended to first select profiles or first add decision scopes?
* What does Request offer changes?
* Nothing displays when I click View results? Can't see any score...
* What's the typical example? i.e. how many decisions do you select, and how do you compare scores?
* What do you learn from simulation? i.e. if I selected 2 decisions and I compare the scores, which one is better or should I use for my customers?
* Is there a way to create relevant test profiles?
* Error on Profile details link.
* Is there a tutorial planned to be released?
* Why still a big red frame when no profile is found?

## Tutorial video {#video}

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
-->