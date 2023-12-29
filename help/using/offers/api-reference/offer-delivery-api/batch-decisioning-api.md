---
title: API de decisiones por lotes
description: Aprenda a utilizar la API de decisiones por lotes para seleccionar las mejores ofertas para los perfiles de las audiencias dentro de un ámbito de decisión predefinido.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 3%

---


# Entrega de ofertas utilizando [!DNL Batch Decisioning] API {#deliver-offers-batch}

El [!DNL Batch Decisioning] La API permite a las organizaciones utilizar la funcionalidad de toma de decisiones para todos los perfiles de una audiencia determinada en una llamada. El contenido de la oferta para cada perfil de la audiencia se coloca en un conjunto de datos de Adobe Experience Platform, donde está disponible para flujos de trabajo por lotes personalizados.

Con el [!DNL Batch Decisioning] API, puede rellenar un conjunto de datos con las mejores ofertas para todos los perfiles de una audiencia de Adobe Experience Platform para los ámbitos de decisión. Por ejemplo, una organización puede querer ejecutar [!DNL Batch Decisioning] para que puedan enviar ofertas a un proveedor de entrega de mensajes. Estas ofertas se utilizan como contenido que se envía para la entrega de mensajes por lotes a la misma audiencia de usuarios.

Para ello, la organización debería:

* Ejecute el [!DNL Batch Decisioning] API, que contiene dos solicitudes:

   1. A **Solicitud del POST del lote** para iniciar una carga de trabajo para procesar por lotes las selecciones de ofertas.

   2. A **Solicitud de GET por lotes** para obtener el estado de carga de trabajo por lotes.

* Exporte el conjunto de datos a la API del proveedor de entrega de mensajes.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html) to learn more about exporting audiences.) -->

>[!NOTE]
>
>Las decisiones por lotes también se pueden realizar mediante la interfaz de Journey Optimizer. Para obtener más información, consulte [esta sección](../../batch-delivery.md), que proporciona información sobre los requisitos previos globales y las limitaciones que se deben tener en cuenta al utilizar la toma de decisiones por lotes.

* **Número de trabajos por lotes en ejecución por conjunto de datos**: Se pueden ejecutar hasta cinco trabajos por lotes a la vez, por conjunto de datos. Cualquier otra solicitud por lotes con el mismo conjunto de datos de salida se agrega a la cola. Se selecciona un trabajo en cola para procesarlo una vez que el trabajo anterior ha terminado de ejecutarse.
* **Límite de frecuencia**: Un lote se ejecuta fuera de la instantánea de perfil que se produce una vez al día. El [!DNL Batch Decisioning] La API limita la frecuencia y siempre carga perfiles de la instantánea más reciente.

## Introducción {#getting-started}

Antes de utilizar esta API, asegúrese de completar los siguientes pasos previos.

### Preparar la decisión {#prepare-decision}

Para preparar una o más decisiones, asegúrese de haber creado un conjunto de datos, una audiencia y una decisión. Estos requisitos previos se detallan en [esta sección](../../batch-delivery.md).

### Requisitos de API {#api-requirements}

Todo [!DNL Batch Decisioning] Las solicitudes de requieren los siguientes encabezados, además de los mencionados en la [Guía para desarrolladores de API de Administración de decisiones](../getting-started.md):

* `Content-Type`: `application/json`
* `x-request-id`: una cadena única que identifica la solicitud.
* `x-sandbox-name`: Nombre de la zona protegida.
* `x-sandbox-id`: ID de la zona protegida.

## Iniciar un proceso por lotes {#start-a-batch-process}

Para iniciar una carga de trabajo para procesar las decisiones por lotes, realice una solicitud de POST al `/workloads/decisions` punto final.

>[!NOTE]
>
>Encontrará información detallada sobre el tiempo de procesamiento de los trabajos por lotes en [esta sección](../../batch-delivery.md).

**Formato de API**

```https
POST {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | El contenedor en el que se encuentran las decisiones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

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
| `xdm:segmentIds` | El valor es una matriz que contiene el identificador único de la audiencia. Solo puede contener un valor. | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | Conjunto de datos de salida en el que se pueden escribir los eventos de decisión. | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | Un contenedor que contiene el `placementId` y `activityId` |  |
| `xdm:activityId` | El identificador único de la decisión. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | El identificador de ubicación único. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | Es un campo opcional que muestra el número de elementos, como las opciones solicitadas para el ámbito de toma de decisiones. De forma predeterminada, la API devuelve una opción por ámbito, pero puede solicitar explícitamente más opciones especificando este campo. Se pueden solicitar un mínimo de 1 y un máximo de 30 opciones por ámbito. | `1` |
| `xdm:includeContent` | Este es un campo opcional y `false` de forma predeterminada. If `true`, el contenido de la oferta se incluye en los eventos de decisión del conjunto de datos. | `false` |

Consulte la [Documentación de Gestión de decisiones](../../get-started/starting-offer-decisioning.md) para obtener una descripción general de los conceptos y las propiedades principales.

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
| `@id` | El UUID generado por la administración de decisiones que identifica una sola carga de trabajo. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | El ID de la organización. | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | El ID de contenedor. | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Hora a la que se creó la solicitud de carga de trabajo de decisión. | `1648078924834` |
| `ode:status` | El estado de la carga de trabajo. | `ode:status: "QUEUED"` |

## Recuperar información sobre una decisión por lotes {#retrieve-information-on-a-batch-decision}

Para recuperar información sobre una decisión específica, realice una solicitud de GET al `/workloads/decisions` al tiempo que proporciona el valor de ID de carga de trabajo correspondiente para su decisión.

**Formato de API**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | El contenedor en el que se encuentran las decisiones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | El UUID generado por la administración de decisiones que identifica una sola carga de trabajo. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

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
| `@id` | El UUID generado por la administración de decisiones que identifica una sola carga de trabajo. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | El ID de organización | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | El ID de contenedor | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Hora a la que se creó la solicitud de carga de trabajo de decisión. | `1648076994405` |
| `ode:status` | El estado de la carga de trabajo comienza con &quot;EN COLA&quot; y cambia a &quot;PROCESANDO&quot;, &quot;INGIRIENDO&quot;, &quot;COMPLETADO&quot; o &quot;ERROR&quot;. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Esto muestra más detalles, como sparkJobId y batchID si el estado es &quot;PROCESANDO&quot; o &quot;INGIRIENDO&quot;. Muestra los detalles del error si el estado es &quot;ERROR&quot;. |  |

## Pasos siguientes {#next-steps}

Al seguir esta guía de API, ha comprobado el estado de la carga de trabajo y ha enviado ofertas utilizando [!DNL [!DNL Batch Decisioning]] API. Para obtener más información, consulte la [información general sobre Administración de decisiones](../../get-started/starting-offer-decisioning.md).
