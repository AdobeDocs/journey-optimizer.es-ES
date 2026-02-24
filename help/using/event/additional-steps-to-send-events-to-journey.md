---
solution: Journey Optimizer
product: journey optimizer
title: Pasos adicionales para enviar eventos a un recorrido
description: Conozca los pasos adicionales para enviar eventos a un recorrido
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: pasos, configuración, recorrido, eventos, flujo, API
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: bfcc7b1544a0d58af8ac1ac69e777a3ff894bbdf
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 3%

---

# Pasos adicionales para enviar eventos {#additional-steps-to-send-events}

Para configurar los eventos que se enviarán a **[!UICONTROL API de ingesta de transmisión]** y que se utilizarán en [!DNL Journey Optimizer], debe seguir estos pasos:

1. Obtenga la URL de entrada desde las API de Adobe Experience Platform. Obtenga más información en [Resumen de API de ingesta de transmisión](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=es){target="_blank"}.
1. Copie la carga útil de la previsualización de carga útil en el menú **[!UICONTROL Evento]**. Obtenga más información en [esta página](../event/about-creating.md#define-the-payload-fields).

>[!IMPORTANT]
>
>Para conocer los requisitos y limitaciones de eventos (flujo continuo, servicio de consultas, ingesta por lotes), consulte [protecciones de Recorrido: eventos](../start/guardrails.md#events-g).

A continuación, debe configurar el sistema de datos que inserta eventos en las API de ingesta de transmisión mediante la carga útil copiada:

1. Configure una llamada de la API POST a la URL de las API de ingesta de transmisión (denominada entrada).
1. Utilice la carga que copió de [!DNL Journey Optimizer] en el cuerpo (&quot;sección de datos&quot;) de la llamada de API a las API de ingesta de transmisión. Consulte a continuación un ejemplo
1. Determine dónde obtener todas las variables presentes en la carga útil. Ejemplo: si el evento debe transmitir la dirección, la carga útil pegada mostrará &quot;dirección&quot;: &quot;cadena&quot;. &quot;cadena&quot; debe reemplazarse por la variable que rellena automáticamente el valor correcto, el correo electrónico de la persona a la que enviar un mensaje. Tenga en cuenta que en la vista previa de carga útil, en la sección **[!UICONTROL Header]**, rellenamos automáticamente muchos valores que se espera que faciliten su trabajo.
1. Seleccione &quot;application/json&quot; como tipo de cuerpo.
1. Pase su ID de organización en el encabezado con la clave &quot;x-gw-ims-org-id&quot;. Para el valor, utilice su ID de organización (&quot;XXX@AdobeOrg&quot;).

Este es un ejemplo de evento de API de ingesta de transmisión:

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
            "timestamp": "2023-05-29T00:00:00.000Z",
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

Para facilitar la identificación del lugar donde pegar la parte de &quot;datos&quot;, puede utilizar una herramienta de visualización JSON como [formateador JSON](https://jsonformatter.curiousconcept.com){target="_blank"}.

Para solucionar problemas de las API de ingesta de transmisión, consulte [Documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=es){target="_blank"}.
