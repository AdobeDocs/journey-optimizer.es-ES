---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: API de decisiones por lotes
description: Aprenda a utilizar la API de decisiones por lotes para seleccionar las mejores ofertas para los perfiles de las audiencias dentro de un ámbito de decisión predefinido.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 4%

---


# Enviar ofertas utilizando la API [!DNL Batch Decisioning] {#deliver-offers-batch}

La API [!DNL Batch Decisioning] permite a las organizaciones utilizar la funcionalidad de toma de decisiones para todos los perfiles de una audiencia determinada en una llamada. El contenido de la oferta para cada perfil de la audiencia se coloca en un conjunto de datos de Adobe Experience Platform, donde está disponible para flujos de trabajo por lotes personalizados.

Con la API [!DNL Batch Decisioning], puede rellenar un conjunto de datos con las mejores ofertas para todos los perfiles de una audiencia de Adobe Experience Platform para los ámbitos de decisión. Por ejemplo, es posible que una organización desee ejecutar [!DNL Batch Decisioning] para que pueda enviar ofertas a un proveedor de entrega de mensajes. Estas ofertas se utilizan como contenido que se envía para la entrega de mensajes por lotes a la misma audiencia de usuarios.

Para ello, la organización debería:

* Ejecute la API [!DNL Batch Decisioning], que contiene dos solicitudes:

   1. Una **solicitud POST por lotes** para iniciar una carga de trabajo para procesar por lotes las selecciones de ofertas.

   2. Una **solicitud GET por lotes** para obtener el estado de la carga de trabajo por lotes.

* Exporte el conjunto de datos a la API del proveedor de entrega de mensajes.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=es) to learn more about exporting audiences.) -->

>[!NOTE]
>
>Las decisiones por lotes también se pueden realizar mediante la interfaz de Journey Optimizer. Para obtener más información, consulte [esta sección](../../batch-delivery.md), que proporciona información sobre los requisitos previos globales y las limitaciones que se deben tener en cuenta al utilizar la toma de decisiones por lotes.

* **Número de trabajos por lotes en ejecución por conjunto de datos**: Se pueden ejecutar hasta cinco trabajos por lotes a la vez, por conjunto de datos. Cualquier otra solicitud por lotes con el mismo conjunto de datos de salida se agrega a la cola. Se selecciona un trabajo en cola para procesarlo una vez que el trabajo anterior ha terminado de ejecutarse.
* **Límite de frecuencia**: Un lote se ejecuta fuera de la instantánea de perfil que se produce una vez al día. La API [!DNL Batch Decisioning] limita la frecuencia y siempre carga perfiles de la instantánea más reciente.

## Introducción {#getting-started}

Antes de utilizar esta API, asegúrese de completar los siguientes pasos previos.

### Preparar la decisión {#prepare-decision}

Para preparar una o más decisiones, asegúrese de haber creado un conjunto de datos, una audiencia y una decisión. Estos requisitos previos se detallan en [esta sección](../../batch-delivery.md).

### Requisitos de API {#api-requirements}

Todas las [!DNL Batch Decisioning] solicitudes requieren los siguientes encabezados además de los mencionados en la [Guía para desarrolladores de API de administración de decisiones](../getting-started.md):

* `Content-Type`: `application/json`
* `x-request-id`: cadena única que identifica la solicitud.
* `x-sandbox-name`: nombre de la zona protegida.

## Iniciar un proceso por lotes {#start-a-batch-process}

Para iniciar una carga de trabajo para procesar decisiones por lotes, realice una petición POST al extremo `/workloads/decisions`.

>[!NOTE]
>
>Encontrará información detallada sobre el tiempo de procesamiento de los trabajos por lotes en [esta sección](../../batch-delivery.md).

**Formato de API**

```https
POST {ENDPOINT_PATH}/workloads/decisions
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/dwm` |

**Solicitud**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dwm/workloads/decisions' \
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
| `xdm:activityId` | El identificador único de la decisión. |  |
| `xdm:dataSetId` | Conjunto de datos de salida en el que se pueden escribir los eventos de decisión. | `6196b4a1a63bd118dafe093c` |
| `xdm:includeContent` | Este es un campo opcional y es `false` de manera predeterminada. Si `true`, el contenido de la oferta se incluye en los eventos de decisión del conjunto de datos. | `false` |
| `xdm:itemCount` | Es un campo opcional que muestra el número de elementos, como las opciones solicitadas para el ámbito de toma de decisiones. De forma predeterminada, la API devuelve una opción por ámbito, pero puede solicitar explícitamente más opciones especificando este campo. Se pueden solicitar un mínimo de 1 y un máximo de 30 opciones por ámbito. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | El identificador de ubicación único. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:propositionRequests` | Un contenedor que contiene `placementId` y `activityId` |  |
| `xdm:segmentIds` | El valor es una matriz que contiene el identificador único de la audiencia. Solo puede contener un valor. | `609028e4-e66c-4776-b0d9-c782887e2273` |

Consulte la [documentación de Administración de decisiones](../../get-started/starting-offer-decisioning.md) para obtener una descripción general de los conceptos y propiedades principales.

**Respuesta**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| Propiedad | Descripción | Ejemplo |
| -------- | ----------- | ------- |
| `@id` | El UUID generado por la administración de decisiones que identifica una sola carga de trabajo. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | El ID de la organización. | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | Hora a la que se creó la solicitud de carga de trabajo de decisión. | `1648078924834` |
| `ode:status` | El estado de la carga de trabajo. | `ode:status: "QUEUED"` |

## Recuperar información sobre una decisión por lotes {#retrieve-information-on-a-batch-decision}

Para recuperar información sobre una decisión específica, realice una petición GET al extremo `/workloads/decisions` y proporcione el valor de ID de carga de trabajo correspondiente para su decisión.

**Formato de API**

```https
GET {ENDPOINT_PATH}/workloads/decisions/{WORKLOAD_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/dwm` |
| `{WORKLOAD_ID}` | El UUID generado por la administración de decisiones que identifica una sola carga de trabajo. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**Solicitud**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dwm/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
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
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| Propiedad | Descripción | Ejemplo |
| -------- | ----------- | ------- |
| `@id` | El UUID generado por la administración de decisiones que identifica una sola carga de trabajo. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | El ID de organización | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | Hora a la que se creó la solicitud de carga de trabajo de decisión. | `1648076994405` |
| `ode:status` | El estado de la carga de trabajo comienza con &quot;EN COLA&quot; y cambia a &quot;PROCESANDO&quot;, &quot;INGIRIENDO&quot;, &quot;COMPLETADO&quot; o &quot;ERROR&quot;. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Esto muestra más detalles, como sparkJobId y batchID si el estado es &quot;PROCESANDO&quot; o &quot;INGIRIENDO&quot;. Muestra los detalles del error si el estado es &quot;ERROR&quot;. |  |

## Próximos pasos {#next-steps}

Siguiendo esta guía de API, ha comprobado el estado de la carga de trabajo y ha enviado ofertas utilizando la API de [!DNL [!DNL Batch Decisioning]]. Para obtener más información, consulte la [descripción general de Administración de decisiones](../../get-started/starting-offer-decisioning.md).
