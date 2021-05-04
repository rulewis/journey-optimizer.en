---
title: About data sources
description: Learn how to configure a data source
---
# Set up your data sources {#concept_s1s_dqt_52b}

![](../assets/do-not-localize/badge.png)

>[!CONTEXTUALHELP]
>id="jo_datasources"
>title="About data sources"
>abstract="The data source configuration is always performed by a technical user. The data source configuration allows you to define a connection to a system to retrieve additional information that will be used in your journeys, for: condition definition, parameter and personalization data in actions, custom wait definition, time zone definition."

The data source configuration allows you to define a connection to a system to retrieve additional information that will be used in your journeys, for:

* [condition definition](../building-journeys/condition-activity.md)
* parameter and personalization data in [actions](../action/action.md)
* [custom wait definition](../building-journeys/wait-activity.md#custom)
* [time zone definition](../building-journeys/timezone-management.md)

This configuration is not required if your journeys only leverage local data coming from an event payload. For example, if your journey is composed of an event followed by a message activity that only uses data from the event, there is no need to configure a data source.

There are two types of data sources:

* The pre-configured Adobe Experience Platform data source that defines the connection to the Real-time Customer Profile Service. This is a built-in data source. See [this page](../datasource/adobe-experience-platform-data-source.md).
* The external data sources that allow you to define a connection to external systems. These are the ones you can create. See [this page](../datasource/external-data-sources.md).

For each data source, you define the information to retrieve using field groups. Field groups are sets of fields that can be retrieved from a data source. See [this page](../datasource/configure-data-sources.md#define-field-groups).

For more information on how to configure an Adobe Experience Platform Data Source and an external data source and how to find and use data in a journey, watch this [tutorial video](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/configure-data-sources.html).
