---
title: Allow list
description: Learn how to use the allow list.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
---
# Allowed list {#allow-list}

It is now possible to define a specific sending-safe list at the [sandbox](administration/sandboxes.md) level.

This allows you to have a safe environment, for testing purpose for example (on a non-production instance, where mistakes can occur), where you have no risk of sending out unwanted messages to your customers.

The **Allowed list** enables you to specify individual email addresses or domains that will be the only recipients or domains allowed to receive the emails you are sending from a specific sandbox.

This can prevent you from sending mails accidentally to real customer addresses when you are in a testing environment.

To add new email addresses or domains to the Allowed list, you must call the suppression API with the ALLOWED value for the listType attribute. For example:

![](assets/allow-list-api.png)

You can perform the Add, Delete and Get operations.


Allowed list and suppression list logic:
When a user call the suppressed API to verify which emails/domains from the list are suppressed:
If the allowed list is empty. The allowed list logic is not applied. The entity will be verified against the client and global list
If the allowed list is not empty and the entity is not in the allowed list then return the suppression service will return the entity as suppressed. (Client and Global list are ignored)
If the allowed list is not empty and the entity is in the allowed list then the suppression service will verify against the client and global. 



