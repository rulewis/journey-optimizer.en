---
title: Personalization use case
description: Personalization use case
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
---

# Personalization use case {#personalization-use-case}

In this use case, you will see how to use multiple types of personalization in a single push notification message. Three types of personalization will be used:

* **Profile**: message personalization based on a profile field
* **Offer decision**: personalization based on offer decisionning variables
* **Context**: personalization based on contextual data from the journey

The goal of this example is to push an event to [!DNL Journey Optimizer] every time a customer order is updated. A push notification is then sent to the customer with information on the order and a personalized offer.

For this use case, the following prerequisites are needed:

* create and design a push notification message, without publishing it. Refer to this [section](../create-message.md).
* configure an order event including the order number, status and item name. Refer to this [section](../event/about-events.md).
* create a decision (previously known as ‘offer activity’), refer to this [section](../offers/offer-activities/create-offer-activities.md).

## Step 1 - Add personalization on profile

1. Click the **[!UICONTROL Message]** menu, and select your message.

   ![](assets/perso-uc.png)

1. Click the **Title** field.

   ![](assets/perso-uc2.png)

1. Type in the subject and add profile personalization. Use the search bar to find the profile's first name field. In the subject text, place the cursor where you want to insert the personalization field, and click the **+** icon. Click **Save**.

   ![](assets/perso-uc3.png)

   >[!NOTE]
   >
   >Leave the message in draft. Do not publish it yet.

## Step 2 - Create the journey

1. Click the **[!UICONTROL Journeys]** menu and create a new journey.

   ![](assets/perso-uc4.png)

1. Add your entry event, a **Message** and an **End** activity.

   ![](assets/perso-uc5.png)

1. In the **Message** activity, select the message previously created. Click **Ok**.

   ![](assets/perso-uc6.png)

   A message is displayed to inform you that the entry event data and journey properties have been passed to the message.

   ![](assets/perso-uc7.png)

   >[!NOTE]
   >
   >The message appears with a warning icon. This is because the message is not published yet.

## Step 3 - Add personalization on contextual data

1. From the **Message** activity, click the **Open the message** icon. The message opens in a new tab.

   ![](assets/perso-uc8.png)

1. Click the **Title** field.

   ![](assets/perso-uc9.png)

1. Select the **Context** category. This item is only available if a journey has passed contextual data to the message. Click **Journey Orchestration**. The following contextual information appears:

   * **Events**: this category regroups all fields from the event(s) placed before the **Message** activity in the journey.
   * **Journey Properties**: the technical fields related to the journey for a given profile, for example the journey ID or the specific errors encountered. Refer to the [Journey Orchestration documentation](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/syntax/journey-properties.html#building-advanced-conditions-journeys).

   ![](assets/perso-uc10.png)

1. Expand the **Events** item, and look for the order number field related to your event. You can also use the search box. Click the **+** icon to insert the personalization field in the subject text. Click **Save**.

   ![](assets/perso-uc11.png)

1. Now click the **Body** field.

   ![](assets/perso-uc12.png)

1. Type the message and insert, from the **Context** category, the order item name and the order progress. 

   ![](assets/perso-uc13.png)

1. From the drop-down, select **Offer decision** to insert an offer decisioning variable. Select the placement and click the **+** icon next to the decision (previously known as 'offer activity') to add it to the body.  

   ![](assets/perso-uc14.png)

1. Click validate to make sure that there are no errors, and click **Save**.

   ![](assets/perso-uc15.png)

1. Now, publish the message. 

   ![](assets/perso-uc16.png)

## Step 4 - Test and publish the journey

1. Open the journey again. If the journey is already open, make sure you refresh the page. Now that the message is published, you can see that there is no error in the journey. Click the **Test** button, then click **Trigger an event**.

   ![](assets/perso-uc17.png)

1. Enter the different values to pass in the test. Test mode only works with test profiles. The profile identifier needs to correspong to a test profile. Click **Send**.

   ![](assets/perso-uc18.png)

   The push notification is sent and displayed on the test profile's mobile phone.

    ![](assets/perso-uc19.png)

1. Verify that there is no error and publish the journey. 

