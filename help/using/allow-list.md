---
title: Allow list
description: Learn how to use the allow list.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
---
# Allowed list {#allow-list}

It is now possible to define a specific sending-safe list at the [sandbox](administration/sandboxes.md) level. This allows you to have a safe environment, for testing purpose for example (on a non-production instance, where mistakes can occur), where you have no risk of sending out unwanted messages to your customers.

The **allowed list** enables you to specify individual email addresses or domains that will be the only recipients or domains allowed to receive the emails you are sending from a specific sandbox. This can prevent you from sending emails accidentally to real customer addresses when you are in a testing environment.

## Add entities to the allowed list

To add new email addresses or domains to the allowed list for a specific sandbox, you must call the suppression API with the 'allowed'' value for the **listType** attribute. For example:

![](assets/allow-list-api.png)

You can perform the **Add**, **Delete** and **Get** operations.

>[!NOTE]
>
>The allowed list maximum can contain up to 1,000 entries.

If you want to [send proofs](preview.md#send-proofs), you must also add the email addresses or domains of your [test profiles](building-journeys/creating-test-profiles.md).

## Allowed list logic

When it comes to allowed list, the logic below is applied.

* If the allowed list is empty, the allowed list logic is not applied. This means that you can send emails to any profiles, provided they are not on the [suppression list](suppression-list.md).

* If the allowed list is **not** empty and the entity is not on the allowed list, the entity is considered as suppressed. The corresponding recipient will not receive the email.

* If the allowed list is **not** empty and the entity is on the allowed list, the email can be sent to the corresponding recipient.

* If an entity is on the allowed list **and** on the suppression list, the corresponding recipient will not receive the email.






