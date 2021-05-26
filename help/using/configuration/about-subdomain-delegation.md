---
title: Delegate subdomains
description: Learn how to delegate your subdomains
page-status-flag: never-activated
uuid: 
contentOwner:
products:
audience: administrators
content-type: reference
topic-tags: 
discoiquuid:
internal: n
snippet: y
---

# Get started with subdomain delegation

## Isolate your brands to protect your reputation

A subdomain is a division of your domain that can be used to isolate your brands, or various types of traffic (transactional messages, marketing information, etc.).
Let's take the example of the "mybrand.com" domain, that is used to send both transactional and marketing communications. In this situation, you can decide to set up two subdomains:

* "info.mybrand.com" subdomain for your transactional communications (purchases confirmation, password reset, etc.),
* "marketing.mybrand.com" subdomain for your prospecting emailings.

By doing so, you will help preserve the reputation of your domain and other subdomains. For example, if the "marketing.mybrand.com" subdomains ended up being added to the block list by Internet Service Providers due to bad deliverability, this would prevent the whole "mybrand.com" domain and the "info.mybrand.com" subdomain from being added to the block list.

## Keep your resources URLs transparent to customers

When implementing a solution, there are requirements for externally-facing components: these include setting up links and web pages to be tracked, displaying mirror pages, etc.

While these requirements are being managed through components hosted by both Adobe and the customer, they include URLs which can be seen by the recipients of the emails. To avoid having URLs which indicate the underlying technical solution or hosting provider, subdomains can be set up to make this transparent to the recipients of the emails. [Learn more about Domain Delegation](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).

## Subdomain delegation in Journey Optimizer

Journey Optimizer provides several features to help you manage subdomains:

* [Delegate your subdomains](delegate-subdomain.md) directly from the interface,
* [Add Google TXT records](google-txt.md) to your subdomains to ensure the successfull delivery of emails to Gmail addresses,
* [Access the PTR records](ptr-records.md) generated for your subdomains, allowing them to be verified by sending mail servers.
