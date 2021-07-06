---
title: About events
description: Learn about events
feature: Events
topic: Administration
role: Administrator
level: Intermediate
---
# About events{#concept_gfj_fqt_52b}

>[!CONTEXTUALHELP]
>id="jo_events"
>title="About events"
>abstract="An event is linked to a person. It relates to the behavior of a person (for example, a person bought a product, visited a shop, exited a website, etc.) or something happening linked to a person (for example, a person reached 10 000 loyalty points). This is what [!DNL Journey Optimizer] will listen to in journeys to orchestrate the best next actions."

The event configuration allows you to define the information [!DNL Journey Optimizer] will receive as events. You can use multiple events (in different steps of a journey) and several journeys can use the same event.

>[!CAUTION]
>
>Event configuration is **mandatory** and must be performed by a **technical user**.

You can  configure two types of events:

* **Unitary** events: these event are linked to a person. They relate to the behavior of a person (for example, a person bought a product, visited a shop, exited a website, etc.) or something happening linked to a person (for example, a person reached 10 000 loyalty points). This is what [!DNL Journey Optimizer] will listen to in journeys to orchestrate the best next actions. Unitary events can be rule-based or system generated. To learn how to create a unitary event, refer to this [page](../event/about-creating.md).

* **Business** events: a business event is an event that, in contrast to a unitary event, is not linked to a specific profile. For example, it can be a news alert, a sports update, a flight change or cancellation, an inventory update, weather events, etc. While these events are not specific to a profile, they may be of interest to any number of profiles: individuals subscribed to particular news topics, passengers on a flight, shoppers interested in an out-of-stock product, etc. Business events are always rule-based. When you drop a business event in a journey, it automatically adds a **Read segment** activity right after. To learn how to create a business event, refer to this [page](../event/about-creating-business.md).


>[!NOTE]
>
>If you edit an event used in a draft or live journey, you can only change the name, the description or add payload fields. We strictly limit the edition of draft or live journeys to avoid breaking journeys.

## Event ID type{#event-id-type}

For business events, the event ID type is always rule-based. 

For unitary events, there are two types of event ID:

* **Rule-based** events: this type of event does not generate an eventID. Using the simple expression editor, you simply define a rule which will be used by the system to identify the relevant events that will trigger your journeys. This rule can be based on any field available in the event payload, for example the profile's location or the number of items added to the profile's cart. 

   >[!CAUTION]
   >
   >A capping rule is defined for rule-based events. It limits the number of qualified events that a journey can process to 5000 per seconds for a given Organization (ORG). It corresponds to Journey Optimizer SLAs. See this [page](https://helpx.adobe.com/legal/product-descriptions/journey-orchestration.html).

* **System-generated** events: these events require an eventID. This eventID field is automatically generated when creating the event. The system pushing the event should not generate an ID, it should pass the one available in the payload preview. 

Journey Optimizer requires events to be streamed or batched into Adobe Experience Platform. This data does not necessarily need to go to the Real-Time Profile. If you would like to use the events for segmentation or lookup in a separate journey, we recommend you enable the dataset for profile.

## Data cycle {#section_r1f_xqt_pgb}

Events are POST API calls. Events are sent to Adobe Experience Platform through Streaming Ingestion APIs. The URL destination of events sent through transactional messaging APIs is called an “inlet”. The payload of events follows XDM formatting. 

The payload contains information required by Streaming Ingestion APIs to work (in the header) and the information required by [!DNL Journey Optimizer] to work  and information to be used in journeys (in the body, for example, the amount of an abandoned cart). There are two modes for the streaming ingestion, authenticated and unauthenticated. For details on Streaming Ingestion APIs, refer to [this link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html).

After arriving through Streaming Ingestion APIs, events flow into an internal service called Pipeline and then in Adobe Experience Platform. If the event schema has the Real-time Customer Profile Service flag enabled and a dataset ID that also has the Real-time Customer Profile flag, it flows into the Real-time Customer Profile Service.

For system-generated events, the Pipeline filters events which have a payload containing [!DNL Journey Optimizer] eventIDs (see the event creation process below) provided by [!DNL Journey Optimizer] and contained in event payload. For rule-based events, the system identifies the event using the eventID condition. These events are listened by [!DNL Journey Optimizer] and the corresponding journey is triggered.
