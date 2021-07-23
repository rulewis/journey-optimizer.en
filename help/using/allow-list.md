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

>[!CAUTION]
>
>This feature is not available on production sandboxes.

The **allowed list** enables you to specify individual email addresses or domains that will be the only recipients or domains allowed to receive the emails you are sending from a specific sandbox. This can prevent you from sending emails accidentally to real customer addresses when you are in a testing environment.

>[!NOTE]
>
>This feature is only applicable to the email channel.

## Enable the allowed list

To enable the allowed list on a sandbox, you need to make an Adobe API call.

Using this API, you can disable the feature for any non-production sandbox any time i.e.it is clear that its not a one way street and one can enable/disable any time. Also, one can update the allow list before or after enabling the feature. The logic works when feature is enabled AND the list is not empty.

## Add entities to the allowed list

To add new email addresses or domains to the allowed list for a specific sandbox, you must call the suppression API with the 'allowed'' value for the **listType** attribute. For example:

![](assets/allow-list-api.png)

You can perform the **Add**, **Delete** and **Get** operations.

>[!NOTE]
>
>The allowed list maximum can contain up to 1,000 entries.

The allowed list feature is honored not just when journey is executing, but also when you perform [message proofing](preview.md#send-proofs) and test journey in test mode.

## Allowed list logic

When the allowed list is enabled at the sandbox level using the API call above and:

* If the allowed list is empty, the allowed list logic is not applied. This means that you can send emails to any profiles, provided they are not on the [suppression list](suppression-list.md).

* If the allowed list is **not** empty and the entity is not on the allowed list, the entity is considered as suppressed. The corresponding recipient will not receive the email.

* If the allowed list is **not** empty and the entity is on the allowed list, the email can be sent to the corresponding recipient. However, if the entity is also on the suppression list, the corresponding recipient will not receive the email with the reason being **[!UICONTROL Suppressed]**.

* If the allowed list is **not** empty and the entity is not on the allowed list and also not in suppression list, the corresponding recipient will not receive the email. The entity is considered as not allowed.




