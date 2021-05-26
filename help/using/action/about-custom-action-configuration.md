---
solution: Journey Orchestration
title: About custom action configuration
description: Learn how to configure a custom action
---
# Configure an action {#configure-an-action}

![](../assets/do-not-localize/badge.png)

If you're using a third-party system to send messages or if you want journeys to send API calls to a third-party system, this is where you configure its connection to journeys. The custom action defined by technical users will then be available in the left palette of your journey, in the **[!UICONTROL Action]** category (see [this page](../building-journeys/about-journey-activities.md#action-activities). Here are a few examples of systems that you can connect to with custom actions: Epsilon, Facebook, Adobe.io, Firebase, etc.
Limitations are listed in [this page](../building-journeys/limitations.md).

Here are the main steps required to configure a custom action:

1. From the **[!UICONTROL Actions]** list, click **[!UICONTROL Add]** to create a new action. The action configuration pane opens on the right side of the screen.

    ![](../assets/custom2.png)

1. Enter a name for your action.

    >[!NOTE]
    >
    >Do not use spaces or special characters. Do not use more than 30 characters.

1. Add a description to your action. This step is optional.
1. The number of journeys that use this action is displayed in the **[!UICONTROL Used in]** field. You can click the **[!UICONTROL View journeys]** button to display the list of  journeys using this action.
1. Define the different **[!UICONTROL URL Configuration]** parameters. See [this page](../action/about-custom-action-configuration.md#url-configuration).
1. Configure the **[!UICONTROL Authentication]** section. This configuration is the same as for data sources.  See [this section](../datasource/external-data-sources.md#section_wjp_nl5_nhb).
1. Define the **[!UICONTROL Message parameters]**. See [this page](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Click **[!UICONTROL Save]**.

    The custom action is now configured and ready to be used in your journeys. See [this page](../building-journeys/about-journey-activities.md#action-activities).

    >[!NOTE]
    >
    >When a custom action is used in a journey, most parameters are read-only. You can only modify the **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** fields and the **[!UICONTROL Authentication]** section.

## URL configuration {#url-configuration}

When configuring a custom action, you need to define the following **[!UICONTROL URL Configuration]** parameters:

![](../assets/journeyurlconfiguration.png)

1. Add the **[!UICONTROL URL]** of the external service.

    >[!NOTE]
    >
    >We strongly recommend using HTTPS for security reasons. We don't allow the use of Adobe addresses that are not public and the use of IP addresses.

1. Select the call **[!UICONTROL Method]**: it can be either **[!UICONTROL POST]** or **[!UICONTROL PUT]**.
1. In the **[!UICONTROL Headers]** section, click **[!UICONTROL Add a header field]** to define a new key/value pair. They correspond to the HTTP headers of the request made to the external service. To delete key/value pairs, place your cursor on the **[!UICONTROL Headers]** field and click on the **[!UICONTROL Delete]** icon.

    **[!UICONTROL Content-Type]** and **[!UICONTROL Charset]** are set by default and cannot be deleted or overridden.

    >[!NOTE]
    >
    >Headers are validated according to the following [parsing rules](https://tools.ietf.org/html/rfc7230#section-3.2.4).

## Define the message parameters {#define-the-message-parameters}

![](../assets/messageparameterssection.png)

In the **[!UICONTROL Message parameters]** section, paste an example of the JSON payload to send to the external service.

![](../assets/customactionpayloadmessage.png)

You will be able to define the parameter type (e.g.: string, integer, etc.).

You will also have a choice between specifying if a parameter is a constant or a variable:

* Constant means that the value of the parameter is defined in the action configuration pane by a technical persona. The value will be always the same across journeys. It will not vary and the marketer won’t see it when using the custom action in the journey. It could be for example an ID the third-party system expects. In that case, the field on the right of the toggle constant/variable is the value passed.
* Variable means the value of the parameter will vary. The marketer using this custom action in a journey will be free to pass the value he wants or to specify where to retrieve the value for this parameter (e.g. from the event, from the Adobe Experience  Platform, etc.). In that case, the field on the right of the toggle constant/variable is the label the marketer will see in the journey to name this parameter.

![](../assets/customactionpayloadmessage2.png)
