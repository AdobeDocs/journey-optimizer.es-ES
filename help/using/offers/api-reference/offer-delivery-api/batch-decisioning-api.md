---
title: API de decisiones por lotes
description: Aprenda a utilizar la API de decisiones por lotes para seleccionar las mejores ofertas para perfiles segmentados dentro de un ámbito de decisión predefinido.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 4%

---


# Enviar ofertas utilizando la variable [!DNL Batch Decisioning] API {#deliver-offers-batch}

La variable [!DNL Batch Decisioning] La API permite a las organizaciones utilizar la funcionalidad de toma de decisiones para todos los perfiles de un segmento determinado en una llamada. El contenido de la oferta para cada perfil del segmento se coloca en un conjunto de datos de Adobe Experience Platform donde está disponible para flujos de trabajo por lotes personalizados.

Con la variable [!DNL Batch Decisioning] API, puede rellenar un conjunto de datos con las mejores ofertas para todos los perfiles de un segmento de Adobe Experience Platform para los ámbitos de decisión. Por ejemplo, una organización puede querer ejecutarse [!DNL Batch Decisioning] para que puedan enviar ofertas a un proveedor de envíos de mensajes. Estas ofertas se utilizan después como contenido que se envía para la entrega de mensajes por lotes al mismo segmento de usuarios.

Para ello, la organización:

* Ejecute el [!DNL Batch Decisioning] API, que contiene dos solicitudes:

   1. A **Solicitud de POST por lotes** para iniciar una carga de trabajo para procesar por lotes las selecciones de ofertas.

   2. A **Solicitud de GET por lotes** para obtener el estado de carga de trabajo por lotes.

* Exporte el conjunto de datos a la API del proveedor de envíos de mensajes.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en) to learn more about exporting segments.) -->

>[!NOTE]
>
>La toma de decisiones por lotes también se puede realizar mediante la interfaz de Journey Optimizer. Para obtener más información, consulte [esta sección](../../batch-delivery.md), que proporciona información sobre los requisitos previos y limitaciones globales que se deben tener en cuenta al utilizar la toma de decisiones por lotes.

* **Número de trabajos en lote en ejecución por conjunto de datos**: Se pueden ejecutar hasta cinco trabajos por lotes a la vez, por conjunto de datos. Cualquier otra solicitud por lotes con el mismo conjunto de datos de salida se agrega a la cola. Un trabajo en cola se selecciona para procesarse una vez que el trabajo anterior ha terminado de ejecutarse.
* **Restricción de frecuencia**: Se ejecuta un lote de la instantánea de perfil que se produce una vez al día. La variable [!DNL Batch Decisioning] La API limita la frecuencia y siempre carga perfiles de la instantánea más reciente.

## Primeros pasos {#getting-started}

Antes de utilizar esta API, asegúrese de completar los siguientes pasos previos necesarios.

### Preparar la decisión {#prepare-decision}

Para preparar una o más decisiones, asegúrese de que ha creado un conjunto de datos, un segmento y una decisión. Estos requisitos previos se detallan en [esta sección](../../batch-delivery.md).

### Requisitos de API {#api-requirements}

Todo [!DNL Batch Decisioning] las solicitudes requieren los siguientes encabezados además de los mencionados en la [Guía para desarrolladores de API de administración de decisiones](../getting-started.md):

* `Content-Type`: `application/json`
* `x-request-id`: Una cadena única que identifica la solicitud.
* `x-sandbox-name`: El nombre del simulador de pruebas.
* `x-sandbox-id`: El ID del simulador de pruebas.

## Iniciar un proceso por lotes {#start-a-batch-process}

Para iniciar una carga de trabajo para procesar las decisiones por lotes, realice una solicitud de POST al `/workloads/decisions` punto final.

>[!NOTE]
>
>La información detallada sobre el tiempo de procesamiento de los trabajos por lotes está disponible en [esta sección](../../batch-delivery.md).

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
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
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
| `xdm:segmentIds` | El valor es una matriz que contiene el identificador único del segmento. Solo puede contener un valor. | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | El dataSet de salida en el que se pueden escribir los eventos de decisión. | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | Un envoltorio que contiene la variable `placementId` y `activityId` |  |
| `xdm:activityId` | Identificador único de la decisión. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | Identificador de ubicación único. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | Se trata de un campo opcional que muestra el número de elementos, como las opciones solicitadas para el ámbito de decisión. De forma predeterminada, la API devuelve una opción por ámbito, pero puede solicitar explícitamente más opciones especificando este campo. Se puede solicitar un mínimo de 1 y un máximo de 30 opciones por ámbito. | `1` |
| `xdm:includeContent` | Se trata de un campo opcional y es `false` de forma predeterminada. If `true`, el contenido de la oferta se incluye en los eventos de decisión del conjunto de datos. | `false` |

Consulte la [Documentación de gestión de decisiones](../../get-started/starting-offer-decisioning.md) para obtener una descripción general de los conceptos y propiedades principales.

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
| `@id` | UUID generado por la administración de decisiones que identifica una única carga de trabajo. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | El ID de organización. | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | El ID del contenedor. | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Hora a la que se creó la solicitud de carga de trabajo de decisión. | `1648078924834` |
| `ode:status` | Estado de la carga de trabajo. | `ode:status: "QUEUED"` |

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
| `{WORKLOAD_ID}` | UUID generado por la administración de decisiones que identifica una única carga de trabajo. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**Solicitud**

```shell
curl -X GET 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
-H 'x-request-id: 7832a42a-d4e5-413b-98e8-e49bef056436' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}'
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
| `@id` | UUID generado por la administración de decisiones que identifica una única carga de trabajo. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | El ID de organización | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | El ID de contenedor | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Hora a la que se creó la solicitud de carga de trabajo de decisión. | `1648076994405` |
| `ode:status` | El estado de la carga de trabajo comienza con &quot;EN COLA&quot; y cambia a &quot;PROCESAMIENTO&quot;, &quot;INGESTING&quot;, &quot;COMPLETED&quot; o &quot;ERROR&quot;. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Esto muestra más detalles, como sparkJobId y batchID, si el estado es &quot;PROCESAMIENTO&quot; o &quot;INGESTING&quot;. Muestra los detalles del error si el estado es &quot;ERROR&quot;. |  |

## Pasos siguientes {#next-steps}

Al seguir esta guía de API, ha comprobado el estado de la carga de trabajo y ha enviado ofertas utilizando [!DNL [!DNL Batch Decisioning]] API. Para obtener más información, consulte la [información general sobre la gestión de decisiones](../../get-started/starting-offer-decisioning.md).
