---
title: Technical settings
description: Learn administration and settings guidelines
---
# Technical settings

![](../assets/do-not-localize/badge.png)

## Set up branding parameters{#cjm-branding}

Every company has brand visual and technical guidelines. You can define a set of specification to present a consistent brand to your customers, from logos to technical aspects, such as email sender, the domain of the mirror pages' URL, or message tracking settings.
Brands cannot be created or modified by end-users: this configuration is managed by Adobe.

To set up branding parameters for your [!DNL Journey Optimizer] instance, you need to contact Adobe and share the following details:

* Company Name

* Sender (From) email address

* Sender (From) Name

* Reply-to address
 
Once branding parameters have been configured, you will be able to select them when creating messages. 

Once branding parameters have been configured, you will be able to select them when creating messages from the **[!UICONTROL Presets]** list. [Learn more about content creation](../create-message.md).

## Configure the push notification channel

Learn how to configure push channel in this [section](../create-push.md).

## Sub-domain delegation

For any new subdomain to be used in [!DNL Journey Optimizer], the first step will be to delegate it. You need to reach out to your Adobe technical contact.

When implementing a solution, there are requirements for externally-facing components: these include setting up links and web pages to be tracked, displaying mirror pages, etc.

While these requirements are being managed through components hosted by both Adobe and the customer, they include URLs which can be seen by the recipients of the emails.  To avoid having URLs which indicate the underlying technical solution or hosting provider, subdomains can be set up to make this transparent to the recipients of the emails.

Following these delegations, the infrastructure put in place by Adobe ensures the following services are carried out for each delegated or CNAME-aliased sending domain:

* Creation of postmaster@ and abuse@ inboxes

* Setup of Feedback loops for the delegated domain

* Basic DMARC record configuration

Parameters established by Adobe are only valid from the time that the delegation was completed and then verified by Adobe, and remains functional.

[Learn more about Domain Delegation](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).


## Create Data Sources, Events and Actions

Use the **[!UICONTROL Admin]** section to manage **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** and **[!UICONTROL Actions]**.

![]()../assets/do-not-localize/admin-menu.png)

### Data Sources

The Data Source configuration allows you to define a connection to a system to retrieve additional information that will be used in your journeys.

Learn more about Data Sources in this [section](../datasource/about-data-sources.md)

### Events 

Events allow you to trigger your journeys unitarily to send messages, in real-time, to the individual flowing into the journey.

In the event configuration, you configure the events expected in the journeys. The incoming events’ data is normalized following the Adobe Experience Data Model (XDM). Events come from Streaming Ingestion APIs for authenticated and unauthenticated events (such as Adobe Mobile SDK events).

Learn more about events in this [section](../event/about-events.md)
 
### Actions 

[!DNL Journey Optimizer] message capabilities are built-in: you only need to design your content and publish your message. If you are using a third-party system to send your messages, you can create a custom action.

Learn more about actions in this [section](../action/action.md)
