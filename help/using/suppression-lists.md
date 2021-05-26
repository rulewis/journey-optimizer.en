---
title: Monitoring message execution
description: Learn monitoring and deliverability guidelines
---
# Manage suppression lists {#manage-suppression-lists}

![](assets/do-not-localize/badge.png)

A suppression list consists of email addresses that you want to exclude from your deliveries because sending to these contacts could hurt your sending reputation and delivery rates.

The Journey Optimizer **suppression list** is managed at your own environment level. It gathers spam complaints, hard bounces, and soft bounces that occur consistently.

## Why suppression lists? {#why-suppression-lists}

To control the email messages that are received by their inbox owners and ensure they only receive those they want, Internet service providers (ISPs) and commercial spam filters have their proprietary algorithms to track the overall reputation of email senders based on the IP addresses and sending domain(s) they use.

If you do not take their feedback (such as spam complaints, bounces, etc.) into account, they will rate your reputation down. The suppression list helps you with honoring the ISPs' feedback.

The recipients whose email addresses are suppressed are automatically excluded from message delivery. This will speed up deliveries, as the error rate has a significant effect on delivery speed.

### Spam complaints {#spam-complaints}

The suppression list collects email addresses that mark your message as spam. Sending to recipients after they submit a spam complaint may have a huge impact on your sending reputation, because it informs ISPs that you may send unwanted emails and may not listen to your recipients.

This could lead to your IP address or sending domain being blocked, which can be avoided with these addresses being on the suppression list.

### Bounces {#bounces}

In addition to this, the suppression list contains email addresses that hard bounce, or that soft bounce too many times. If you continue sending to these addresses, it may affect your delivery rates, because it tells ISPs that you may not be following email address list maintenance best practices, and therefore may not be a trustworthy sender.

## Suppression list management {#suppression-list-management}

The Journey Optimizer suppression list gathers email addresses and domains that are suppressed across all mailings **in a single client environment**, meaning specific to an IMS organization ID associated with a sandbox ID.

The suppression list allows you to automatically collect:
* Email addresses that are invalid, or that consistently soft-bounce and could adversely affect your email reputation if you continue to include them in your deliveries.
* Recipients who issue a spam complaint of some kind against one of your email messages.

For example, if someone writes to a customer service requesting to never receive mail again from you, the email address of that person will be suppressed across your instance and you won't be able to deliver to that address anymore.

<!--For each address, the basic reason for suppression (soft bounces, a hard bounce or a spam complaint) will be shown in the Suppression list.-->

### Delivery failures {#delivery-failures}

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

There are three types of errors when a delivery fails:

* **Hard bounce**. A hard bounce indicates an invalid email address (i.e. an email address that does not exist). This involves a bounce message from the receiving email server that explicitly states that the address is invalid, such as 'unknown user'.
* **Soft bounce**. This is a temporary email bounce that occurred for a valid email address.
* **Ignored**. This is an email bounce that occurred for a valid email address but is known to be temporary, such as a failed connection attempt, a temporary Spam-related issue (email reputation), or a temporary technical issue.

The hard bounces and soft bounces can be a reason for an email address to be automatically added to the suppression list.

### What's on the suppression list? {#what-s-on-suppression-list}

Email addresses are added to the suppression list as follows:

* All **hard bounces** and **spam complaints** automatically send the corresponding email addresses to the suppression list after a single occurrence.

* **Soft bounces** do not immediately send an email address to the suppression list, but they increment an error counter. Wen the error counter reaches the threshold, the address is then added to the suppression list.

    The threshold is set at three errors:
    * For the same delivery, at the third attempt, the address is suppressed.
    * If there are different deliveries and two errors occur at least 24 hours apart, the error counter is incremented upon each error and the address is also suppressed at the third attempt.

    When a delivery is successful after a retry, the error counter of the address is reinitialized.

### Retries {#retries}

If a message fails due to a temporary bounce of the **Ignored** type, retries will be performed for **3.5 days** from the time the message was added to the email queue.

The minimum delay between retries and the maximum number of retries to be performed are <!--managed by the Enhanced MTA,--> based on how well an IP is performing, both historically and currently at a given domain.

After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.
