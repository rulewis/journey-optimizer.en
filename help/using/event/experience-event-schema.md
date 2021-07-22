---
title: About ExperienceEvent Schemas for journey events
description: Learn about ExperienceEvent Schemas for journey events
feature: Schemas
topic: Administration
role: Admin
level: Intermediate
---
# About ExperienceEvent Schemas for [!DNL Journey Optimizer] Events 

[!DNL Journey Optimizer] events are XDM Experience Events that are sent to Adobe Experience Platform via Streaming Ingestion.

As such, an important prerequisite for setting up events for [!DNL Journey Optimizer] is that you are familiar with Adobe Experience Platform’s Experience Data Model (or XDM) and how to compose XDM Experience Event schemas, as well as how to stream XDM-formatted data to Adobe Experience Platform.

## Schema requirements for [!DNL Journey Optimizer] Events 

The first step in setting up an event for [!DNL Journey Optimizer] is to ensure that you have an XDM schema defined to represent the event, and a dataset created to record instances of the event on Adobe Experience Platform. Having a dataset for your events is not strictly necessary, but sending the events to a specific dataset will allow you to maintain users’ event history for future reference and analysis, so it is always a good idea. If you do not already have a suitable schema and dataset for your event, both of those tasks can be done in Adobe Experience Platform web interface. 

![](../assets/schema1.png)

Any XDM schema that will be used for [!DNL Journey Optimizer] events should meet the following requirements:  

* The schema must be of the XDM ExperienceEvent class. 

   ![](../assets/schema2.png)

* For system-generated events, the schema must include the Orchestration eventID field group. [!DNL Journey Optimizer] uses this field to identify events used in journeys.

   ![](../assets/schema3.png)

* Declare an identity field for identifying the subject of the event. If no identity is specified, an identity map can be used. This is not recommended.

   ![](../assets/schema4.png)

* If you would like this data to be available for lookup later in a Journey, mark the schema and dataset for profile. 

   ![](../assets/schema5.png)

   ![](../assets/schema6.png)

* Feel free to include data fields to capture any other context data you want to include with the event, such as information about the user, the device from which the event was generated, location, or any other meaningful circumstances related to the event. 

   ![](../assets/schema7.png)

   ![](../assets/schema8.png)

## Leverage schema relationships

Adobe Experience Platorm allows you to define relationships between schemas in order to use one dataset as a lookup table for another. 

Let's say your brand data model has a schema capturing purchases. You also have a schema for the product catalog. You can capture the product ID in the purchase schema and use a relationship to look up more complete product details from the product catalog. This allows you to create a segment for all customers who bought a laptop, for example, without having to explicitely list out all laptop IDs or capture every singe product details in transactionnal systems.

To define a relationship, needs to be a dedicated field in the source schema, in this case the product SKU field in both the in-store purchases and web events schemas. This field needs to reference another field in the detination schema. whish is oing to be the product SKU field in the product catalago schema; Also the source and destination tables must be enabled for real time customer profile and the destination scehma must have that common field defined as its primary identity. 

product catalalog schema enabled for profile with the product SKU as the primay identity. 

In my store purchase shema I select the product SKU field and in the field properties check the relationship checkbox. I enter the product catalog schema as the reference schema and select the identity name space for the product. Ibn this case it's a custom non peple id defined called luma product sku. we can see the relation ship in the schema editor. I can do the same in the web event checma. You could do the same for the store ID and the promotion ID. 
