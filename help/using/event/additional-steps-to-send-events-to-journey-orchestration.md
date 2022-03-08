---
title: Additional steps to send events to a journey
description: Learn additional steps to send events to a journey
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 5%

---

# Pasos adicionales para enviar eventos {#additional-steps-to-send-events}

**[!UICONTROL Streaming Ingestion APIs]**[!DNL Journey Optimizer]

1. Get the inlet URL from Adobe Experience Platform APIs. [](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=es)
1. **[!UICONTROL Event]** Obtenga más información en [esta página](../event/about-creating.md#define-the-payload-fields).

You then need to configure the data system that pushes events to Streaming Ingestion APIs using the payload you copied:

1. Set up a POST API call to the Streaming Ingestion APIs URL (called an inlet).
1. [!DNL Journey Optimizer] See below for an example
1. Determine where to get all the variables present in the payload. Example: if the event is supposed to convey the address, the payload pasted will show &quot;address&quot;: &quot;string&quot;. &quot;string&quot; should be replaced by the variable that will automatically populate the right value, the email of the person to send a message to. **[!UICONTROL Header]**
1. Select &quot;application/json&quot; as a body type.
1. Pass your IMS Organization ID in the header using the key &quot;x-gw-ims-org-id&quot;. For the value, use your IMS Organization ID (&quot;XXX@AdobeOrg&quot;).

Here is an example of a Streaming Ingestion APIs event:

```
{
    "header": {
        "msgType": "xdmEntityCreate",
        "msgId": "c25585b9-252e-431d-b562-e73da70c04e7",
        "msgVersion": "1.0",
        "xactionId": "f5995abe-c49d-4848-9577-a7a4fc2996fb",
        "datasetId": "string - required if you want the data to land in a specific dataset - not mandatory",
        "imsOrgId": "XXX@AdobeOrg",
        "schemaRef": {
            "id": "XXX",
            "contentType": "application/vnd.adobe.xed-full+json;version=1"
        },
        "source": {
            "name": "Journeys"
        }
    },
    "body": {
        "xdmMeta": {
            "schemaRef": {
                "id": "XXX",
                "contentType": "application/vnd.adobe.xed-full+json;version=1"
            }
        },
        "xdmEntity": {
            "_instance_name": {
                "person": {
                    "firstName": "string",
                    "lastName": "string",
                    "gender": "string",
                    "birthYear": 10,
                    "emailAddress": "string"
                }
            },
            "identityMap": {
                "Email": [
                {
                    "id": "string"
                    }
                ]
            },
            "_id": "string",
            "timestamp": "2018-05-29T00:00:00.000Z",
            "_experience": {
                "campaign": {
                    "orchestration": {
                    "eventID": "XXX"
                    }
                }
            }
        }
    }
}
```

[](https://jsonformatter.curiousconcept.com)

[](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html)
