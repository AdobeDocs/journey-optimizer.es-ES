---
title: API de decisiones por lotes
description: Aprenda a utilizar la API de decisiones por lotes para seleccionar las mejores ofertas para perfiles segmentados dentro de un ámbito de decisión predefinido.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: 817a77c5717804ccae36db3dd8920008ab127684
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 3%

---

# Enviar ofertas utilizando la variable [!DNL Batch Decisioning] API

La variable [!DNL Batch Decisioning] La API de permite a las organizaciones utilizar la funcionalidad de offer decisioning para todos los perfiles de un segmento determinado en una llamada de . El contenido de la oferta para cada perfil del segmento se coloca en un conjunto de datos de Adobe Experience Platform donde está disponible para flujos de trabajo por lotes personalizados.

Con la variable [!DNL Batch Decisioning] API, puede rellenar un conjunto de datos con las mejores ofertas para todos los perfiles de un segmento de Adobe Experience Platform para un ámbito de decisión. Por ejemplo, es posible que una organización desee ejecutar la toma de decisiones por lotes para que pueda enviar ofertas a un proveedor de envíos de mensajes. Estas ofertas se utilizan después como contenido que se envía para la entrega de mensajes por lotes al mismo segmento de usuarios.

Para ello, la organización:

* Ejecute el [!DNL Batch Decisioning] API, que contiene dos solicitudes:

   1. A **Solicitud de GET por lotes** para obtener el estado de carga de trabajo por lotes.

   2. A **Solicitud de POST por lotes** para iniciar una carga de trabajo para procesar por lotes las selecciones de ofertas.

* Exporte el conjunto de datos a la API del proveedor de envíos de mensajes.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en) to learn more about exporting segments.) -->

## Primeros pasos {#getting-started}

Antes de utilizar esta API, asegúrese de completar los siguientes pasos previos necesarios.

### Preparar la decisión

Siga los pasos a continuación para preparar sus decisiones:

* Para exportar un resultado de decisión, cree un conjunto de datos con el esquema &quot;Eventos de decisión de ODE&quot;.

* Cree un segmento de Platform que debe evaluarse y luego actualizarse. Consulte la [documentación de segmentación](http://www.adobe.com/go/segmentation-overview-en) para obtener más información sobre cómo actualizar la evaluación de pertenencia a segmentos.

* Cree una decisión (que tenga un ámbito de decisión que consista en un ID de decisión y un ID de colocación) en Adobe Journey Optimizer. Consulte la [sección sobre la definición de ámbitos de decisión](../../offer-activities/create-offer-activities.md) de la guía sobre la creación de decisiones para obtener más información.

### Requisitos de API

Todas las solicitudes de decisiones por lotes requieren los siguientes encabezados adicionales:

* `Content-Type`: `application/json`
* `x-request-id`: Una cadena única que identifica la solicitud.
* `x-sandbox-name`: El nombre del simulador de pruebas.
* `x-sandbox-id`: El ID del simulador de pruebas.

## Recuperar información sobre una decisión por lotes {#retrieve-information-on-a-batch-decision}

Para recuperar información sobre una decisión específica, realice una solicitud de GET a la `/workloads/decisions` al proporcionar el valor de ID de carga de trabajo correspondiente para su decisión.

**Formato de API**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las decisiones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | UUID generado por el Offer decisioning que identifica una sola carga de trabajo. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**Solicitud**

```shell
curl -X GET 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
-H 'x-request-id: 7832a42a-d4e5-413b-98e8-e49bef056436' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: {ACCESS_TOKEN}'
```

**Respuesta**

```json
{
    "@id": "f395ab1f-dfaf-48d4-84c9-199ad6354591",
    "xdm:imsOrgId": "{IMS_ORG}",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| Propiedad | Descripción | Ejemplo |
| -------- | ----------- | ------- |
| `@id` | UUID generado por el Offer decisioning que identifica una sola carga de trabajo. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | ID de organización de IMS | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | El ID de contenedor | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Hora a la que se creó la solicitud de carga de trabajo de decisión. | `1648076994405` |
| `ode:status` | El estado de la carga de trabajo comienza con &quot;EN COLA&quot; y cambia a &quot;PROCESAMIENTO&quot;, &quot;INGESTING&quot;, &quot;COMPLETED&quot; o &quot;ERROR&quot;. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Esto muestra más detalles, como sparkJobId y batchID, si el estado es &quot;PROCESAMIENTO&quot; o &quot;INGESTING&quot;. Muestra los detalles del error si el estado es &quot;ERROR&quot;. |  |

## Iniciar un proceso por lotes {#start-a-batch-process}

Para iniciar una carga de trabajo para procesar las decisiones por lotes, realice una solicitud de POST al `/workloads/decisions` punto final.

**Formato de API**

```https
POST {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las decisiones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitud**

```shell
curl -X POST 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions' \
-H 'x-request-id: f671a589-eb7b-432f-b6b9-23d5b796b4dc' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: {ACCESS_TOKEN}' \
-d '{
  "xdm:segmentIds": [
    "609028e4-e66c-4776-b0d9-c782887e2273"
  ],
  "xdm:dataSetId": "6196b4a1a63bd118dafe093c",
  "xdm:propositionRequests": [
        {
            "xdm:activityId": "xcore:offer-activity:1410cdcda196707b",
            "xdm:placementId": "xcore:offer-placement:1410c4117306488a",
            "xdm:itemCount": 1
        }
  ],
  "xdm:includeContent": false
}'
```

| Propiedad | Descripción | Ejemplo |
| -------- | ----------- | ------- |
| `xdm:segmentIds` | Identificador único del segmento. Solo puede contener un valor. | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | El dataSet de salida en el que se pueden escribir los eventos de decisión. | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | Un envoltorio que contiene placementId y activityId |  |
| `xdm:activityId` | Identificador único de la decisión. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | Identificador de ubicación único. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | Se trata de un campo opcional que muestra el número de elementos, como las opciones solicitadas para el ámbito de decisión. De forma predeterminada, la API devuelve una opción por ámbito, pero puede solicitar explícitamente más opciones especificando este campo. Se puede solicitar un mínimo de 1 y un máximo de 30 opciones por ámbito. | `1` |
| `xdm:includeContent` | Se trata de un campo opcional y es `false` de forma predeterminada. If `true`, el contenido de la oferta se incluye en los eventos de decisión del conjunto de datos. | `false` |

Consulte la [Documentación de gestión de decisiones](../../get-started/starting-offer-decisioning.md) para obtener una descripción general de los conceptos principales.

**Respuesta**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| Propiedad | Descripción | Ejemplo |
| -------- | ----------- | ------- |
| `@id` | UUID generado por el Offer decisioning que identifica una sola carga de trabajo. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | El ID de su organización de IMS. | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | Su ID de contenedor. | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Hora a la que se creó la solicitud de carga de trabajo de decisión. | `1648078924834` |
| `ode:status` | Estado de la carga de trabajo. | `ode:status: "QUEUED"` |

## Niveles de servicio {#service-levels}

La hora de extremo a extremo para cada decisión de lote es la duración desde el momento en que se crea la carga de trabajo hasta el resultado de decisión disponible en el conjunto de datos de salida. El tamaño del segmento en la carga útil de la solicitud del POST es el factor principal que afecta al tiempo de decisión del lote de extremo a extremo. A continuación se presentan algunas observaciones sobre diferentes tamaños de segmentos:

* tamaño del segmento &lt;= 10K: 6 minutos
* tamaño del segmento &lt;= 1M: 10 minutos
* tamaño del segmento &lt;= 15M: 75 minutos

## Limitaciones {#limitations}

Las siguientes limitaciones existen con [!DNL Batch Decisioning] API:

* **Trabajo de lote único**: Actualmente, solo se puede ejecutar un único trabajo por lotes por conjunto de datos a la vez. Cualquier otra solicitud respondería con HTTP 429 (demasiadas solicitudes).
* **Restricción de frecuencia**: Se ejecuta un lote de la instantánea de perfil que se produce una vez al día. La variable [!DNL Batch Decisioning] La API limita la frecuencia y siempre carga perfiles de la instantánea más reciente.

## Pasos siguientes {#next-steps}

Al seguir esta guía de API, ha comprobado el estado de la carga de trabajo y las ofertas entregadas mediante la variable [!DNL Batch Decisioning] API. Para obtener más información, consulte la [información general sobre la gestión de decisiones](../../get-started/starting-offer-decisioning.md).
