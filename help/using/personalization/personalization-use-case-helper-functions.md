---
title: Personalization use case&colon; configuration of a cart abandonment email
description: Learn how to personalize a message using helper functions
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
---

# Personalization use case: configuration of a cart abandonment email {#personalization-use-case-helper-functions}

In this example, you will personalize the body of an email message to be sent to customers who have left items in their shopping cart, but have not completed the purchase.

You will use these types of helper functions:

* The `upperCase` string function, to insert the customer's first name in capital letters. [Learn more](functions/string.md#upper).
* The `each` helper, to insert the list of items in the cart. [Learn more](functions/helpers.md#each).
* The `if` helper, to insert a product-specific note if the related product is in the cart. [Learn more](functions/helpers.md#if-function).
<!-- **Context**: personalization based on contextual data from the journey -->

Before you start, you must know how to configure these elements:
* Events. [Learn more](../event/about-events.md).
* Messages. [Learn more](../create-message.md)
* Email body. [Learn more](../create-email-content.md).
* Journeys. [Learn more](../building-journeys/using-the-journey-designer.md).

Follow these steps:
1. [Create an email](#configure-email).
2. [Insert the customer's first name in capital letters](#uppercase-function).
3. [Create the message-triggering event and the journey](#create-context).
4. [Add the cart content to the email](#each-helper).
5. [Insert a product-specific note](#if-helper).
6. [Test and publish the journey](#test-and-publish).

## Step 1: Creating the email{#configure-email}

1. Create or modify an email message, then click **[!UICONTROL Email Designer]**.
   ![](../assets/personalization-uc-helpers-1.png)

2. From the left palette of the Email Designer home page, drag and drop three structure components onto the body of the message.
   
3. Drag and drop an HTML content component onto each new structure component.

   ![](../assets/personalization-uc-helpers-2.png)

## Step 2: Inserting the customer's first name in capital letters {#uppercase-function}

1. On the Email Designer home page, click on the HTML component where you want to add the customer's first name.
2. On the contextual toolbar, click **[!UICONTROL Show the source code]**.
   
   ![](../assets/personalization-uc-helpers-3.png)

3. In the **[!UICONTROL Edit HTML]** window, add the `upperCase` string function:
   1. Select **[!UICONTROL Helper functions]** in the list.
   2. Use the search field to find "uppercase".
   3. From the search results, add the `upperCase` function. To do this, click the Plus (+) sign next to **[!UICONTROL {%= upperCase(string) %}: string]**.

      The Expression editor shows this expression:

      ```handlebars
      {%= upperCase(string) %}
      ``` 
      
      ![](../assets/personalization-uc-helpers-4.png)
   
4. Remove the word "string" from the expression. Leave the cursor at this position.
5. Add the personalization token for the customer's first name:
   1. Select **[!UICONTROL Profile]** in the list.
   2. Navigate to **[!UICONTROL Profile]** > **[!UICONTROL Person]** > **[!UICONTROL Full name]**.
   3. From the search results, add the **[!UICONTROL First name]** token to the expression.
      The Expression editor shows this expression:

      ```handlebars
      {%= upperCase(profile.person.name.firstName) %}
      ``` 
   
      ![](../assets/personalization-uc-helpers-5.png)

      Learn more about the [person name data type](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/person-name.html).

6. Click **[!UICONTROL Validate]**, then **[!UICONTROL Save]**.
   
   ![](../assets/personalization-uc-helpers-6.png)
7. Save the message.

## Step 3: Creating the message-triggering event and the related journey {#create-context}

Because the cart content is contextual information from the journey, you must add the email to a journey before you can personalize it with cart-specific information.

1. Create an event whose schema includes the `productListItems` array. Define all the fields from this array as payload fields.
   

   Learn more about the [product list item data type](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html).

2. Create a journey that starts with this event and add the message to it.
   
   ![](../assets/personalization-uc-helpers-7.png)

3. Click **[!UICONTROL OK]**.

   ![](../assets/personalization-uc-helpers-8.png)

## Step 4: Inserting the list of items from the cart {#each-helper}

1. Reopen the message.
2. On the Email Designer home page, click on the HTML component where you want to list the cart content.
3. On the contextual toolbar, click **[!UICONTROL Show the source code]**.
   
   ![](../assets/personalization-uc-helpers-3.png)

4. In the **[!UICONTROL Edit HTML]** window, add the `each` helper:
   1. Select **[!UICONTROL Helper functions]** in the list.
   2. Use the search field to find "each".
   3. From the search results, add the `each` helper.

      The Expression editor shows this expression:
      ```handlebars
      {{#each someArray as |variable|}} {{/each}}
      ```
   
      ![](../assets/personalization-uc-helpers-9.png)

5. Add the **productListItems** array to the expression:

   1. Remove the word "someArray" from the expression. Leave the cursor at this position.
   2. Select **[!UICONTROL Context]** in the list.
   
      The list shows the **[!UICONTROL Context]** option only after you have added the message to a journey.
   3. Navigate to **[!UICONTROL Journey Orchestration]** > **[!UICONTROL Events]** > ***[!UICONTROL event_name]***, then expand the **[!UICONTROL productListItems]** node.
   
      In this example, *event_name* represents the name of your event.

   4. From the search results, add the **[!UICONTROL Product]** token to the expression.

      The Expression editor shows this expression:

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems.product as |variable|}} {{/each}}
      ```
      In this example, *event_ID* represents the ID of your event.

      ![](../assets/personalization-uc-helpers-10.png)

   5. Modify the expression:
      1. Remove the string ".product". Leave the cursor at this position.
      2. Replace the word "variable" with the word "product".

      This example shows the modified expression:

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems as |product|}}
      ```
6. Paste this code between the opening `{{#each}}` tag and the closing `{/each}}` tag:

   ```html
   <table>
      <tbody>
         <tr>
            <td><b>#name</b></td>
            <td><b>#quantity</b></td>
            <td><b>#currency #priceTotal</b></td>
         </tr>
      </tbody>
   </table>
   ```
7. Add the personalization tokens for the item name, the quantity, and the price:

   1. Remove the word "#name" from the HTML table. Leave the cursor at this position.
   2. From the previous search results, add the **[!UICONTROL Name]** token to the expression.
   
   Repeat these steps twice:
      * Replace "#quantity" with the **[!UICONTROL Quantity]** token.
      * Replace "#priceTotal" with the **[!UICONTROL Total price]** token.
      * Replace "#currency" with the **[!UICONTROL currencyCode]** token.
   
   This example shows the modified expression:

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems as |product|}}
         <table>
            <tbody>
               <tr>
                  <td><b>{{context.journey.events.event_ID.productListItems.name}}</b></td>
                  <td><b>{{context.journey.events.event_ID.productListItems.quantity}}</b></td>
                  <td><b>{{context.journey.events.event_ID.productListItems.currencyCode}}
                         {{context.journey.events.event_ID.productListItems.priceTotal}}</b></td>
               </tr>
            </tbody>
         </table>
      {{/each}}
      ```
8. Click **[!UICONTROL Validate]**, then **[!UICONTROL Save]**.
   ![](../assets/personalization-uc-helpers-11.png)
   
## Step 5: Inserting a product-specific note {#if-helper}

1. On the Email Designer home page, click on the HTML component where you want to insert the note.
2. On the contextual toolbar, click **[!UICONTROL Show the source code]**.
3. In the **[!UICONTROL Edit HTML]** window, add the `if` helper:
   1. Select **[!UICONTROL Helper functions]** in the list.
   2. Use the search field to find "if".
   3. From the search results, add the `if` helper.

      The Expression editor shows this expression:
      ```handlebars
      {%#if condition1%} render_1
         {%else if condition2%} render_2
         {%else%} default_render
      {%/if%}
      ```
      ![](../assets/personalization-uc-helpers-12.png)

4. Remove this `else if` condition from the expression: 

   ```handlebars
   {%else if condition2%} render_2
   ```

5. Add the personalization token to the condition:
   1. Remove the word "condition1" from the expression. Leave the cursor at this position.
   2. Select **[!UICONTROL Context]** in the list.
   3. Navigate to **[!UICONTROL Journey Orchestration]** > **[!UICONTROL Events]** > ***[!UICONTROL event_name]***, then expand the **[!UICONTROL productListItems]** node.
   
      In this example, *event_name* represents the name of your event.

   4. From the search results, add the **[!UICONTROL Name]** token to the expression.

      The Expression editor shows this expression:
      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name%}
         render_1
         {%else%} default_render
      {%/if%}
      ```
      ![](../assets/personalization-uc-helpers-13.png)

1. Modify the expression:
   1. In the Expression editor, specify the product name after the `name` token.
         
      Use this syntax, where &lt;product name&gt; represents the name of your product:

      ```handlebars
      = "<product name>"
      ```

      Example:
      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         render_1
         {%else%} default_render
      {%/if%}
      ```

   1. Add the product-specific note.
         
      Example:
      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         Due to longer than usual lead times on the Juno Jacket, please expect item to ship two weeks after purchase.
         {%else%} default_render
      {%/if%}
      ```
   2. Remove the word "default_render".
1. Click **[!UICONTROL Validate]**, then **[!UICONTROL Save]**.

   ![](../assets/personalization-uc-helpers-14.png)

2. Save and publish the message.

## Step 6: Testing and publishing the journey {#test-and-publish}

1. Open the journey. If the journey is already open, then refresh the page.
2. Click the **Test** button, then click **Trigger an event**.

   You can turn on testing only after you published the message.

   ![](../assets/personalization-uc-helpers-15.png)

1. Enter the different values to pass in the test, then click **Send**.
   
   The test mode only works with test profiles.

///   ![]()

   The email is sent to the email address of the test profile.
   
   The email contains the product-specific note only if the related product is in the cart.

   ![](../assets/personalization-uc-helpers-17.png)

1. Verify that there is no error, then publish the journey.


## Related topics

### Handlebars functions

[Helpers](functions/helpers.md)

[String functions](functions/string.md)

### Use cases

[Message personalization with profile information, context, and offer](personalization-use-case.md)

[Message personalization with decision-based offer](../offers/offers-e2e.md)

## Tutorial video {#helper-functions-video}

[Helper functions for personalization](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html)