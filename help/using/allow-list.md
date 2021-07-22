---
title: Allow list
description: Learn how to use the allow list.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
---
# Allow list {#allow-list}

As a user, I should be able to define my safe sending list (Allowed list) on a per sandbox basis wherein I should have the flexibility to put individual email addresses or domains so that only those individual recipients OR domains receive the emails. This should work in case of test mails as well as published journeys.

This needs to be a safe environment where there is no risk of sending out messages to profiles inadvertently.

Use case:
In Non Prod - Allow emails only to customer or Adobe or partners domains. This allows work on non prod instances to be free from the risk of sending out emails by mistake to customers. As non-prod is used for development, mistakes are likely.
 
Brands may want to test partial production setup in test sandboxes. 
They will onboard real customer data to test out something, but they wont want to send to these real customer profiles.
They are asking for allow list for these sandboxes, which will only allow sending to domains and addresses in this list. We shouldn’t hardcode the Allowlist so adobe domain or customer domain shouldn’t matter to us. We should only read what is mentioned in allowed list.
Prod sandboxes – we will have to think how to treat allow list here. We don’t need allow list in prod sandbox.
Allow list should be at sandbox level
I think we should over-ride test profile and honor only allow list. 
Partners/consultants don’t want to send mails accidentally to real customer addresses / production addresses. They may try out some workflows related to customers in their setups and wont want to accidentally send to those addresses ever.
So they want an allow list of emails or domains.
Example Adobe consulting domain can only send emails to Adobe domains or partner instances can send to partner domains etc.

Suppression service to support ADD/Delete/Get capabilities for the allowed list.
Add/Delete/Get operations for the allowed list:
user can add new email/domain to the allowed list by calling the suppression API with type=allowed:

![](assets/allow-list-api.png)

Same goes for delete and fetch operations. (Suppression APIs  with type=allowed.)

Allowed list and suppression list logic:
When a user call the suppressed API to verify which emails/domains from the list are suppressed:
If the allowed list is empty. The allowed list logic is not applied. The entity will be verified against the client and global list
If the allowed list is not empty and the entity is not in the allowed list then return the suppression service will return the entity as suppressed. (Client and Global list are ignored)
If the allowed list is not empty and the entity is in the allowed list then the suppression service will verify against the client and global. 



