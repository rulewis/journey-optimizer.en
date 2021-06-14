---
title: Monitoring message execution
description: Learn monitoring and deliverability guidelines
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
---
# Manage deliverability {#manage-deliverability}

![](assets/do-not-localize/badge.png)

Deliverability is a measure of the success of your deliveries reaching your recipients inboxes.

**Email deliverability** refers to the set of characteristics that determine a message's ability to reach its destination, via a personal e-mail address, within a short time, and with the expected quality in terms of content and format. These characteristics fall into four main categories: data quality, message and content, sending infrastructure, and reputation. Together, they form the foundation of a successful email deliverability program.

The **deliverability rate** is the number of messages that hit the recipients' inboxes compared to the number of messages that were delivered. It depends on numerous factors, particularly:

* Limited spam complaints
* Low hard bounce rates
* Quality of the addresses targeted
* Message content
* Sender reputation

To optimize the deliverability of your [!DNL Journey Optimizer] experiences, we recommend using the best practices listed in this section. Deliverability problems are generally linked to protection against spam implemented by Internet service providers (ISPs) and mail server administrators.

## Reduce complaint rate {#reduce-complaint-rate}

ISPs usually have a prominent means of reporting a received message as spam. This makes it possible to identify unreliable sources. By rapidly honoring opt-out requests and therefore showing that you are a reliable sender, you can reduce complaint rates. [Learn more about opt-out management](consent.md#opt-out-management).

As a general rule, do not try to get in the way of recipients who want to opt-out by requiring them to fill out fields such as their email address or name, for example. The unsubscription landing page should have one validation button only.

Pay extra care when requesting additional confirmation: a user may have two email addresses redirected to the same box (for example: firstname.lastname@club.com and firstname.lastname@internet-club.com). If the profile is able to remember the first address only and wishes to unsubscribe via a message sent to the other one, the form will refuse this because the encrypted identifier and the email address entered will not match.

## Leverage suppression lists {#suppression-lists}

[!DNL Journey Optimizer] manages a suppression list that gathers spam complaints, hard bounces, and soft bounces that occur consistently.

To protect your deliverability, the recipients whose addresses are on the suppression list are excluded by default from all future deliveries, because sending to these contacts could hurt your sending reputation.

[Learn more about the suppression list](suppression-list.md).

## Use monitoring tools {#monitoring-tools}

Use the features offered by [!DNL Journey Optimizer] to monitor your deliverability.

The **[!UICONTROL Executions]** tab of the message list allows you to check how your deliveries are performing through a set of real-time indicators. Amongst other things, this tab displays:
* The number of messages that are successfully executed, sent and delivered.
* The number of messages that have been opened and the number of messages/links that have been clicked.

[Learn more about monitoring message execution](message-monitoring.md).

## Adapt message content {#adapt-message-content}

To a lesser degree, the content of certain messages may be detected as spam.

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

To improve your deliverability rate and make sure that your emails reach your recipients, follow the principles below when designing your message content:

* **Sender name and address**: The address has to explicitly identify the sender. The domain has to be owned by and registered to the sender. The domain registry must not be privatized.
<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **Unsubscribe link and landing page**: The unsubscribe link is essential. It must be visible and valid, and the form must be functional.
<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[Learn more about designing email content](design-emails.md).
