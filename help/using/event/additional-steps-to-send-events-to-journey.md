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
TQID: https://experienceleague.adobe.com/SiUXmerz2D-TYmIEXvaYk4usjRq67Y0v7V7sGVN-4vo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 867eeef1f90c152c463397222f5ed95f3b9c264b
workflow-type: tm+mt
source-wordcount: 347
ht-degree: 5%

---

# Pasos adicionales para enviar eventos {#additional-steps-to-send-events}

>[!BEGINSHADEBOX]

**En esta página:** Configure su sistema de datos para insertar eventos en las API de ingesta de transmisión y que los eventos que configuró lleguen a Journey Optimizer y almacenen en déclencheur sus recorridos.

>[!ENDSHADEBOX]

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

Para solucionar problemas de las API de ingesta de transmisión, consulte [Documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"}.
