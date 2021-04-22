---
solution: Journey Orchestration
title: About ExperienceEvent Schemas for Journey Orchestration Events 
description: Learn about ExperienceEvent Schemas for Journey Orchestration Events
---
# About ExperienceEvent Schemas for [!DNL Customer Journey Management] Events 

![](../assets/do-not-localize/badge.png)

[!DNL Customer Journey Management] events are XDM Experience Events that are sent to Adobe Experience Platform via Streaming Ingestion.

As such, an important prerequisite for setting up events for [!DNL Customer Journey Management] is that you are familiar with Adobe Experience Platform’s Experience Data Model (or XDM) and how to compose XDM Experience Event schemas, as well as how to stream XDM-formatted data to Adobe Experience Platform.

## Schema requirements for [!DNL Customer Journey Management] Events 

The first step in setting up an event for [!DNL Customer Journey Management] is to ensure that you have an XDM schema defined to represent the event, and a dataset created to record instances of the event on Adobe Experience Platform. Having a dataset for your events is not strictly necessary, but sending the events to a specific dataset will allow you to maintain users’ event history for future reference and analysis, so it is always a good idea. If you do not already have a suitable schema and dataset for your event, both of those tasks can be done in Adobe Experience Platform web interface. 

![](../assets/schema1.png)

Any XDM schema that will be used for [!DNL Customer Journey Management] events should meet the following requirements:  

* The schema must be of the XDM ExperienceEvent class. 

   ![](../assets/schema2.png)

* For system-generated events, the schema must include the Orchestration eventID mixin. [!DNL Customer Journey Management] uses this field to identify events used in journeys.

   ![](../assets/schema3.png)

* Declare an identity field for identifying the subject of the event. If no identity is specified, an identity map can be used. This is not recommended.

   ![](../assets/schema4.png)

* If you would like this data to be available for lookup later in a Journey, mark the schema and dataset for profile. 

   ![](../assets/schema5.png)

   ![](../assets/schema6.png)

* Feel free to include data fields to capture any other context data you want to include with the event, such as information about the user, the device from which the event was generated, location, or any other meaningful circumstances related to the event. 

   ![](../assets/schema7.png)

   ![](../assets/schema8.png)
