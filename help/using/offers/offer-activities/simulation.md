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

## About simulations

To validate your decisioning logic, you can simulate which offers will be delivered to a test profile for a given placement.

Simulation allows you to view the results of offer decisions as a selected profile.

This enables you to test and refine various versions of your offers with no impact on the targeted recipients.

To access this feature, select the **[!UICONTROL Simulation]** tab from the **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** menu.

![](../../assets/offers_simulation-tab.png)

<!-->
➡️ [Discover this feature in video](#video)
-->

## Select profile

Is it recommended to first select profiles or first add decision scopes?

1. From the **[!UICONTROL Simulation]** tab, click **[!UICONTROL Manage profile]**.

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

1. Click the **[!UICONTROL Profile details]** link to display the selected profile date. > Error?

1. **[!UICONTROL Settings]** button?

***

Learn more on [selecting test profiles](preview.md#select-test-profiles)

## Add decision scopes

1. Click **[!UICONTROL Add decision scope]**.

1. Select a placement.

    ![](../../assets/offers_simulation-add-decision-scope.png)

1. The available decisions are displayed. Select the decision of your choice and click **[!UICONTROL Add]**.

    ![](../../assets/offers_simulation-add-decision-scope-2.png)

1. You can click the **[!UICONTROL Open offer decisions]** link to open the list of all the decisions that you created in another tab. Learn more on decisions in [this section](create-offer-activities.md).

1. The decision scope displays in the center of the screen. You can adjust the number of offers you want to request? You can also add as many decisions as you need.

    ![](../../assets/offers_simulation-decision-scope.png)

1. Click **[!UICONTROL View results]** to display the scores for each decision according to the selected profile.

1. Select another profile from the list to display the results of the offer decisions for a different test profile.

***

Nothing displays when I click View results? Can't see any score...
What's the typical example? i.e. how many decisions do you select, and how do you compare scores?
What do you learn from simulation? i.e. if I selected 2 decisions and I compare the scores, which one is better or should I use for my customers?
What does Request offer changes?

***

<!-->
## Tutorial video {#video}

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
-->