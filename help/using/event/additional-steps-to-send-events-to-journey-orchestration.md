---
title: Pasos adicionales para enviar eventos a un recorrido
description: Conozca los pasos adicionales para enviar eventos a un recorrido
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 3%

---

# Pasos adicionales para enviar eventos {#concept_xrz_n1q_y2b}

![](../assets/do-not-localize/badge.png)

Para configurar los eventos que se enviarán a **[!UICONTROL Streaming Ingestion APIs]** y que se utilizarán en [!DNL Journey Optimizer], debe seguir estos pasos:

1. Obtenga la URL de entrada de las API de Adobe Experience Platform. Obtenga más información en [Resumen de las API de ingesta de transmisión](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html).
1. Copie la carga útil de la previsualización de carga útil en el menú **[!UICONTROL Event]** . Obtenga más información en [esta página](../event/about-creating.md#define-the-payload-fields).

A continuación, debe configurar el sistema de datos que envía eventos a las API de ingesta de transmisión mediante la carga útil que ha copiado:

1. Configure una llamada de API de POST en la URL de las API de ingesta de transmisión (denominada entrada).
1. Utilice la carga útil que ha copiado de [!DNL Journey Optimizer] en el cuerpo (&quot;sección de datos&quot;) de la llamada de API a las API de ingesta de transmisión. Consulte a continuación un ejemplo
1. Determine dónde obtener todas las variables presentes en la carga útil. Ejemplo: si se supone que el evento transmite la dirección, la carga útil pegada mostrará &quot;address&quot; (dirección): &quot;cadena&quot;. &quot;cadena&quot; debe reemplazarse por la variable que rellena automáticamente el valor correcto, el correo electrónico de la persona a la que enviar un mensaje. Tenga en cuenta que en la vista previa de carga útil, en la sección **[!UICONTROL Header]**, rellenamos automáticamente muchos valores que se espera que faciliten su trabajo.
1. Seleccione &quot;application/json&quot; como tipo de cuerpo.
1. Pase su ID de organización de IMS en el encabezado utilizando la clave &quot;x-gw-ims-org-id&quot;. Para el valor, utilice su ID de organización de IMS (&quot;XXX@AdobeOrg&quot;).

Este es un ejemplo de un evento de API de ingesta de transmisión:

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

Para facilitar la identificación del lugar en el que pegar la parte &quot;datos&quot;, puede utilizar una herramienta de visualización JSON como [https://jsonformatter.curiousconcept.com](https://jsonformatter.curiousconcept.com)

Para solucionar los problemas de las API de ingesta de transmisión, consulte esta [página](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html).
