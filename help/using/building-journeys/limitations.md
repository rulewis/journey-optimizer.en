---
title: Journey limitations
description: Learn more about Journey limitations
---
# Limitations {#journey-limitations}

![](../assets/do-not-localize/badge.png)

Here are limitations related to the use of journeys.

## Journey list limitations

* In the journeys list, filters, searches and column selection are reset at page refresh.

## General actions limitations

* There is no sending throttling. 
* Two retries are systematically performed in case of an error. You cannot adjust the number of retries according to the error message received. 
* The built-in **Reaction** event allows you to react to out-of-the-box actions (see this [page](../building-journeys/reaction-events.md)). If you want to react to a message sent via a custom action, you need to configure a dedicated event. 
* There is no Adobe Campaign Classic productized integration.
* You cannot place two actions in parallel, you must add them one after the other.

## Message action limitations

* The **Message** activity does not allow you to use contextual data coming from the journey. The personalization of messages is performed directly when designing the message in Journey Optimizer.

* When you add a multichannel message, two messages will be sent.

## Journey versions limitations {#journey-versions-limitations}

* a journey starting with an event activity in v1 cannot start with something else than an event in further versions. You cannot start a journey with a **Segment Qualification** event. 
* a journey starting with a **Segment Qualification** activity in v1 must always start with a **Segment Qualification** in further versions. 
* The segment and namespace chosen in **Segment qualification** (first node) can not be changed in new versions.
* The re-entrance rule must be the same in all journey versions.
* A journey starting with a **Read segment** cannot start with another event in next versions.
 
## Custom actions limitations

* The custom action URL does not support dynamic parameters. 
* Only POST and PUT call methods are supported. 
* The name of the query parameter or header must not start with "." or "$". 
* IP addresses are not allowed. 
* Internal Adobe addresses (.adobe.) are not allowed.
 
## Events limitations

* For system-generated events, streaming data used to initiate a customer journey must be configured within Journey Optimizer first to get a unique orchestration ID. This orchestration ID must be appended to the streaming payload coming into Adobe Experience Platform. This limitation does not apply to rule-based events.
 
## Data sources limitations

* External data sources can be leveraged within a customer journey to lookup external data in real-time. These sources must be usable via REST API, support JSON and be able to handle the volume of requests.

## Journeys starting at the same time as a profile creation {#journeys-limitation-profile-creation}
 
There is a delay associated to API based profile creation/update in Adobe Experience Platform. The Service Level Target (SLT) in terms of latency is < 1 min from ingestion to Unified Profile for 95th percentile of requests, at a volume of 20K Requests per second (RPS).

If a Journey is triggered simultaneously to a profile creation and immediately checks/retrieves information from Profile Service, it might not work properly.

You can choose from one of these two solutions:

* Add a wait activity after the first event, to give Adobe Experience Platform the time it needs to perform the ingestion to Profile Service.

* Set up a journey that does not immediately leverage the profile. For example, if the journey is designed to confirm an account creation, the experience event could contain information needed to send the first confirmation message (first name, last name, email address, etc). 

## Read segment limitations

* It is not possible to trigger a segment-based journey in a shorter timeframe than 1 hour.
* Streamed segments are always up-to-date but batch segments will not be calculated at retrieval time. They are only evaluated every day at the daily batch evaluation time.
