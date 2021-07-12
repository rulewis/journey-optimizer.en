---
title: Delegate subdomains
description: Learn how to delegate your subdomains
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
---

# Subdomain delegation in [!DNL Journey Optimizer]

Creating a subdomain for email campaigns allows brands to isolate varying types of traffic (marketing vs. corporate for example) into specific IP pools and with specific domains, which will speed the IP warming process and improve deliverability overall. If you share a domain and it gets blocked or added to the deny list, it could impact your corporate mail delivery. However, reputation issues or blocks on a domain specific to your email marketing communications will impact just that flow of email. Using your main domain as the sender or ‘From’ address for multiple mail streams could also break email authentication, causing your messages to be blocked or placed in the spam folder.

A subdomain is a division of your domain that can be used to isolate your brands, or various types of traffic - for example transactional messages and marketing communications.

Let's take the example of the "mybrand.com" domain, that is used to send both transactional and marketing communications. In this situation, you can decide to set up two subdomains:

* "info.mybrand.com" subdomain for your transactional communications (purchases confirmation, password reset, etc.),
* "marketing.mybrand.com" subdomain for your prospecting emailings.

By doing so, you will help preserve the reputation of your domain and other subdomains. For example, if the "marketing.mybrand.com" subdomains ended up being added to the block list by Internet Service Providers due to bad deliverability, this would prevent the whole "mybrand.com" domain and the "info.mybrand.com" subdomain from being added to the block list.

When implementing a solution, there are requirements for externally-facing components: these include setting up links and web pages to be tracked, displaying mirror pages, etc.

While these requirements are being managed through components hosted by both Adobe and the customer, they include URLs which can be seen by the recipients of the emails. To avoid having URLs which indicate the underlying technical solution or hosting provider, subdomains can be set up to make this transparent to the recipients of the emails.

**Learn more**

* Learn how to [delegate your subdomains](delegate-subdomain.md) directly from the interface
* Learn how to [add Google TXT records](google-txt.md) to your subdomains to ensure the successful delivery of emails to Gmail addresses
* Learn how to [access the PTR records](ptr-records.md) generated for your subdomains, allowing them to be verified by sending mail servers
