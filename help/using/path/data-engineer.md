---
title: Journey Optimizer Get Started for Data Engineer
description: As a Data Engineer, learn more how to work with Journey Optimizer
level: Intermediate
---
# Get Started for Data Engineer {#data-engineer}

![data engineer](assets/do-not-localize/user-2-S.jpeg) 

As an **Adobe Journey Optimizer Data Engineer**, prepare and maintain customer profile data used to power the experiences orchestrated by [!DNL Journey Optimizer], model customer and business data in schemas and configure source connectors for ingesting data.

Learn how to **identify data and create schema and dataset** to get your data into Adobe Experience Platform in this page. 

>[!NOTE]
>
>Learn more about **data ingestion** in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html){target="_blank"}

Steps to create an identity namespace and a dataset enabled for profiles, create segments and test profiles are detailed in the sections below:

1.  **Create an identity namespace**. In Adobe [!DNL Journey Optimizer], **Identities** link consumers across devices and channels, the result is an identity graph. The linked identity graph is used to personalize experiences based on interactions across all of your business touchpoints.  Learn more about identities and identity namespaces [in this page](../get-started-identity.md).

1. **Create a schema** and enable it for profiles. A schema is a set of rules that represent and validate the structure and format of data. At a high level, schemas provide an abstract definition of a real-world object (such as a person) and outline what data should be included in each instance of that object (such as first name, last name, birthday, and so on).  Learn more about schemas [in this page](../get-started-schemas.md).

1. **Create datasets**. A dataset is a storage and management construct for a collection of data, typically a table, that contains a schema (columns) and fields (rows). Datasets also contain metadata that describes various aspects of the data they store. Once a dataset is created, you can map it to an existing schema and add data into it. Learn more about datasets [in this page](../get-started-datasets.md).

1. **Configure sources connectors**. Adobe Journey Optimzer allows data to be ingested from external sources while providing you with the ability to structure, label, and enhance incoming data using Platform services. You can ingest data from a variety of sources such as Adobe applications, cloud-based storages, databases, and many others. Learn more about Source connectors [in this page](../get-started-sources.md).

1. **Create test profiles**. Test profiles are required when using the [test mode](../building-journeys/testing-the-journey.md) in a journey, and to [preview and test your messages](../preview.md) before sending. Discover steps to create test profiles [in this page](../../using/building-journeys/creating-test-profiles.md).


In addition, to be able send messages in journeys, you must configure **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** and **[!UICONTROL Actions]**. Learn more [in this section](../../using/configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* The **Data Source** configuration allows you to define a connection to a system to retrieve additional information that will be used in your journeys. Learn more about Data Sources [in this section](../datasource/about-data-sources.md).

* **Events** allow you to trigger your journeys unitarily to send messages, in real-time, to the individual flowing into the journey. In the event configuration, you configure the events expected in the journeys. The incoming events’ data is normalized following the Adobe Experience Data Model (XDM). Events come from Streaming Ingestion APIs for authenticated and unauthenticated events (such as Adobe Mobile SDK events). Learn more about events [in this section](../event/about-events.md).
    
* [!DNL Journey Optimizer] comes with built-in message capabilities: you can design your content and publish your message. If you are using a third-party system to send your messages, for example Adobe Campaign, create a **custom action**. Learn more about actions in this [in this section](../action/action.md).
