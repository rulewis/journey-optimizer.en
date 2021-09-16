---
title: Journey Optimizer limitations
description: Learn more about Journey Optimizer limitations
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
---
# Limitations {#limitations}

Entitlements, product limitations and performance guardrails are listed in[ Adobe Journey Optimizer product description page](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

You will find below additional limitations when using [!DNL Adobe Journey Optimizer].

## Limitations in messages

* You cannot add attachments to an email with [!DNL Journey Optimizer].
* Email BCC is not supported in [!DNL Journey Optimizer].

## Limitations in journeys

### General actions

* There is no sending throttling. 
* Three retries are systematically performed in case of an error. You cannot adjust the number of retries according to the error message received. 
* The built-in **Reaction** event allows you to react to out-of-the-box actions. Learn more in [this page](building-journeys/reaction-events.md). If you want to react to a message sent via a custom action, you need to configure a dedicated event. 
* You cannot place two actions in parallel, you must add them one after the other.

### Message action

* When you add a multichannel message, two messages will be sent.

### Journey versions {#journey-versions-limitations}

* A journey starting with an event activity in v1 cannot start with something else than an event in further versions. You cannot start a journey with a **Segment Qualification** event. 
* A journey starting with a **Segment Qualification** activity in v1 must always start with a **Segment Qualification** in further versions. 
* The segment and namespace chosen in **Segment Qualification** (first node) can not be changed in new versions.
* The re-entrance rule must be the same in all journey versions.
* A journey starting with a **Read Segment** cannot start with another event in next versions.
 
### Custom actions

* The custom action URL does not support dynamic parameters. 
* Only POST and PUT call methods are supported. 
* The name of the query parameter or header must not start with "." or "$". 
* IP addresses are not allowed. 
* Internal Adobe addresses (.adobe.) are not allowed.
 
### Events

* For system-generated events, streaming data used to initiate a customer journey must be configured within Journey Optimizer first to get a unique orchestration ID. This orchestration ID must be appended to the streaming payload coming into Adobe Experience Platform. This limitation does not apply to rule-based events.
 
## Data sources
#
* External data sources can be leveraged within a customer journey to lookup external data in real-time. These sources must be usable via REST API, support JSON and be able to handle the volume of requests.

### Journeys starting at the same time as a profile creation {#journeys-limitation-profile-creation}
 
There is a delay associated to API based profile creation/update in Adobe Experience Platform. The Service Level Target (SLT) in terms of latency is < 1 min from ingestion to Unified Profile for 95th percentile of requests, at a volume of 20K Requests per second (RPS).

If a journey is triggered simultaneously to a profile creation and immediately checks/retrieves information from Profile Service, it might not work properly.

You can choose from one of these two solutions:

* Add a wait activity after the first event, to give Adobe Experience Platform the time it needs to perform the ingestion to Profile Service.

* Set up a journey that does not immediately leverage the profile. For example, if the journey is designed to confirm an account creation, the experience event could contain information needed to send the first confirmation message (first name, last name, email address, etc). 

### Read segment

* Streamed segments are always up-to-date but batch segments will not be calculated at retrieval time. They are only evaluated every day at the daily batch evaluation time.
