---
title: Create a test profile
description: Learn how to create a test profile
feature: Journeys
topic: Content Management
role: User
level: Intermediate
---
# Create test profiles {#create-test-profiles}

Test profiles are required when using the test mode To learn how to use the [test mode](../building-journeys/testing-the-journey.md) in a journey, and to [preview and test your messages](../preview.md).

Available methods to create test profiles are detailed below:

* You can turn an [existing profile](#turning-profile-into-test) into a test profile

* You can create a test profile by uploading a [csv file](#create-test-profiles-csv) or using [API calls](#create-test-profiles-api). In addition to these two methods, Adobe Journey Optimizer comes with a specific [in-product use case](#use-case-1) to facilitate test profile creation.

* You can also upload a json file in a dataset. For more on this, refer to the [Data Ingestion documentation](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html#add-data-to-dataset).

Note that creating a test profile is similar to creating regular profiles in Adobe Experience Platform. For more information, refer to the [Real-time Customer Profile documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html).

## Prerequisites {#test-profile-prerequisites}

In order to be able to create profiles, you first need to create a schema and a dataset in Adobe [!DNL Journey Optimizer].

First, you need to **create a schema**. Follow these steps:

1. In the DATA MANAGEMENT menu section, click **[!UICONTROL Schemas]**.
    ![](../assets/test-profiles-0.png)
1. Click **[!UICONTROL Create schema]**, in the top right, then select a schema type, for example **XDM Individual Profile**.
    ![](../assets/test-profiles-1.png)
1. Select the appropriate field groups. Make sure you add the **Profile test details** field group. 
    ![](../assets/test-profiles-1-ter.png)
    Once done, click **[!UICONTROL Add field groups]**: the list of field groups is displayed on the schema overview screen.
    ![](../assets/test-profiles-2.png)

    >[!NOTE]
    >
    >* Click the name of the schema to change it and update its properties.
    >
    >* Click the **[!UICONTROL Add]** button in the Field groups section to select other fields groups to add in the schema

1. In the list of fields, click on the field that you want to define as the primary identity.
    ![](../assets/test-profiles-3.png)
1. In the **[!UICONTROL Field properties]** right panel, check the **[!UICONTROL Identity]** and **[!UICONTROL Primary Identity]** options and select a namespace. If you want the primary identity to be an email address, choose the **[!UICONTROL Email]** namespace. Click **[!UICONTROL Apply]**.
    ![](../assets/test-profiles-4bis.png)
1. Select the schema and enable the **[!UICONTROL Profile]** option in the **[!UICONTROL Schema properties]** panel.
    ![](../assets/test-profiles-5.png) 
1. Click **Save**.

>[!NOTE]
>
>For more information on schema creation, refer to the [XDM documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#prerequisites).

Then you need to **create the dataset** in which the profiles will be imported. Follow these steps:

1. Browse to **[!UICONTROL Datasets]**, then click **[!UICONTROL Create dataset]**.
    ![](../assets/test-profiles-6.png) 
1. Choose **[!UICONTROL Create dataset from schema]**.
    ![](../assets/test-profiles-7.png) 
1. Select the previously created schema then click **[!UICONTROL Next]**.
    ![](../assets/test-profiles-8.png) 
1. Choose a name then click **[!UICONTROL Finish]**.
    ![](../assets/test-profiles-9.png) 
1. Enable the **[!UICONTROL Profile]** option. 
    ![](../assets/test-profiles-10.png) 

>[!NOTE]
>
> For more information on dataset creation, refer to the [Catalog Service documentation](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#getting-started).

## In-product use case{#use-case-1}

From Adobe Journey Optimizer home page, you can leverage the test profiles in-product use case. This use case facilitates the creation of test profiles used for testing journeys before publishing.

![](../assets/use-cases-home.png)

Click the **[!UICONTROL Begin]** button to start the use case.

The following information is required:

1. **Identity namespace**: The [identity namespace](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html) used to uniquely identify the test profiles. For example, if email is used to identify the test profiles, the identity namespace **Email** should be selected. If the unique identifier is the phone number, then the identity namespace **Phone** should be selected.

2. **CSV file**: A comma separated file containing the list of test profiles to create. The use case expects a predefined format for the CSV file that contains the list of test profiles to create. Each row in the file should include the following fields in the correct order as follows:

    1. **Person Id**: Unique identifier of the test profile. The values of this field should reflect the identity namespace that was selected. (As an example, if **Phone** is selected for the identity namespace, then the values of this field should be phone numbers. Similarly if **Email** is selected, then the values of this field should be emails)
    1. **Email**: Test profile email address. (The **Person Id** field and the **Email** field could potentially contain the same values if **Email** is selected as the identity namespace)
    1. **First Name**: Test profile first name.
    1. **Last Name**: Test profile last name.
    1. **City**: Test profile city of residence
    1. **Country**: Test profile country of residence
    1. **Gender**: Test profile gender. Available values are **male**, **female** and **non_specified**

After selecting the identity namespace and providing the CSV file based on the format above, click on **[!UICONTROL Run]** button at the top right. The use case might take a few minutes to complete. Once the use case completes processing and creating the test profiles, a notification will be sent to notify the user.
 
>[!NOTE]
>
>Test profiles may override existing profiles. Before executing the use case make sure the CSV contains test profiles only and that it is executed against the correct sandbox.

## Turn a profile into a test profile{#turning-profile-into-test}

You can turn an existing profile into a test profile: you can update profiles attributes in the same way as when you create a profile. 

A simple way to do this is by using an **[!UICONTROL Update Profile]** action activity in a journey and change the testProfile boolean field from false to true.

Your journey will be composed of a **[!UICONTROL Read Segment]** and an **[!UICONTROL Update Profile]** activity. You first need to create a segment targeting the profiles you want to turn into test profiles. 

>[!NOTE]
>
> Since you will be updating the **testProfile** field, the chosen profiles must include this field. The related schema must have the **Profile test details** mixin. See [this section](../building-journeys/creating-test-profiles.md#test-profiles-prerequisites).

1. Browse to **Segments**, then **Create segment**, in the top right.
    ![](../assets/test-profiles-22.png) 
1. Define a name for your segment and build the segment: choose the field(s) and value(s) to target the profiles you want.
    ![](../assets/test-profiles-23.png) 
1. Click **Save** and check that the profiles are correctly targeted by the segment.
    ![](../assets/test-profiles-24.png) 

    >[!NOTE]
    >
    > Segment calculation can take some time. Learn more on segments in [this section](../segment/about-segments.md).

1. Now create a new journey and start with a **[!UICONTROL Read Segment]** orchestration activity.
1. Choose the previously created segment and the namespace that your profiles use.
    ![](../assets/test-profiles-25.png)
1. Add an **[!UICONTROL Update Profile]** action activity. 
1. Select the schema, the **testProfiles** field, the dataset and set the value to **True**. To perform this, in the **[!UICONTROL VALUE]** field, click the **Pen** icon on the right, select **[!UICONTROL Advanced mode]** and enter **true**.
    ![](../assets/test-profiles-26.png)
1. Add an **End** activity and click **[!UICONTROL Publish]**.
1. In the **[!UICONTROL Segments]** section, check that the profiles have been correctly updated.
    ![](../assets/test-profiles-28.png)

    >[!NOTE]
    >
    > For more information on the **[!UICONTROL Update Profile]** activity, refer to [this section](../building-journeys/update-profiles.md).

## Create a test profile using a csv file{#create-test-profiles-csv}

In Adobe Experience Platform, you can create profiles by uploading a csv file containing the different profile fields into your dataset. This is the easiest method.

1. Create a simple csv file using a spreadsheet software.
1. Add one column for each needed field. Make sure you add the primary identity field ("personID" in our example above) and the "testProfile" field set to "true". 
    ![](../assets/test-profiles-11.png) 
1. Add one line per profile and fill in the values for each field. 
    ![](../assets/test-profiles-12.png) 
1. Save the spreadsheet as a csv file. Make sure commas are used as separators.
1. Browse to Adobe Experience Platform **Workflows**. 
    ![](../assets/test-profiles-14.png) 
1. Choose **Map CSV to XDM schema**, then click **Launch**.
    ![](../assets/test-profiles-16.png) 
1. Select the dataset you want to import the profiles into. Click **Next**.
    ![](../assets/test-profiles-17.png) 
1. Click **Choose files** and select your csv file. When the file is uploaded, click **Next**.
    ![](../assets/test-profiles-18.png) 
1. Map the source csv fields to the schema fields, then click **Finish**.
    ![](../assets/test-profiles-19.png) 
1. The data import begins. The status will move from **Processing** to **Success**. Click **Preview data set**, in the top right.
    ![](../assets/test-profiles-20.png)
1. Check that the test profiles have been correctly added.
    ![](../assets/test-profiles-21.png)

Your test profiles are added and can now be used when testing a journey. Refer to [this section](../building-journeys/testing-the-journey.md).
>[!NOTE]
>
> For more information on csv imports, refer to the [Data Ingestion documentation](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html#tutorials).

## Create test profiles using API calls{#create-test-profiles-api}

You can also create test profiles via API calls. Learn more in this [page](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html).

You must use a Profile schema that contains the "Profile test details" mixin. The testProfile flag is part of this mixin.

When creating a profile, make sure you pass the value: testProfile = true.

Note that you can also update an existing profile to change its testProfile flag to "true".

Here is an example of an API call to create a test profile:

```
curl -X POST \
'https://dcs.adobedc.net/collection/xxxxxxxxxxxxxx' \
-H 'Cache-Control: no-cache' \
-H 'Content-Type: application/json' \
-H 'Postman-Token: xxxxx' \
-H 'cache-control: no-cache' \
-H 'x-api-key: xxxxx' \
-H 'x-gw-ims-org-id: xxxxx' \
-d '{
"header": {
"msgType": "xdmEntityCreate",
"msgId": "xxxxx",
"msgVersion": "xxxxx",
"xactionid":"xxxxx",
"datasetId": "xxxxx",
"imsOrgId": "xxxxx",
"source": {
"name": "Postman"
},
"schemaRef": {
"id": "https://example.adobe.com/mobile/schemas/xxxxx",
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"xdmEntity": {
"_id": "xxxxx",
"_mobile":{
"ECID": "xxxxx"
},
"testProfile":true
}
}
}'
```
