---
solution: Journey Optimizer
product: journey optimizer
title: API de retos de fidelización
description: Aprenda a utilizar las API de REST de Desafíos de fidelización para administrar mediante programación los desafíos y consultar el estado de participación de perfiles en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Developer
level: Intermediate
exl-id: a1b2c3d4-e5f6-7890-abcd-ef1234567890
feature_v2: []
subfeature_v2: []
source-git-commit: 3756e104086c83bbca88b2fe770a40a8e9f39ef3
workflow-type: tm+mt
source-wordcount: 315
ht-degree: 8%

---


# API de retos de fidelización {#loyalty-challenges-api}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a utilizar las API de REST de retos de fidelidad para crear y administrar desafíos mediante programación, así como para consultar y actualizar el estado de participación de desafíos para perfiles individuales.

>[!ENDSHADEBOX]

## Acceso rápido {#quick-access}

Hay dos API de REST disponibles para los retos de fidelidad:

* **[API de metadatos de desafío de fidelidad](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}**: cree, recupere, actualice, publique, archive y duplique desafíos mediante programación.
* **[API de estado de desafío de fidelidad](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges-state){target="_blank"}**: consulte y actualice el estado de participación de desafío para perfiles individuales.

## API de metadatos de desafío de fidelización {#metadata-api}

La API de metadatos de desafío de fidelidad le permite administrar todo el ciclo de vida de los desafíos fuera de la interfaz de usuario de Journey Optimizer. Utilícelo para automatizar operaciones de desafío o integrar la administración de programas de fidelidad en sus propias herramientas y flujos de trabajo. Por ejemplo, puede crear, publicar y archivar desafíos, recuperar todos los desafíos con el filtrado y la ordenación, o duplicar un desafío existente, incluidos sus metadatos de recorrido y campañas.

➡️ [Referencia de API de metadatos de desafío de fidelidad](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

## API de estado de desafío de fidelización {#state-api}

La API de estado de desafío de fidelidad permite interactuar con registros de participación de desafío a nivel de perfil. Utilícelo para consultar el estado de participación actual, el progreso y la finalización de tareas de un perfil; por ejemplo, para recuperar todos los registros de participación de un perfil, comprobar el estado de una tarea específica dentro de un desafío o retirar un perfil de uno o más desafíos.

➡️ [Referencia de API de estado de desafío de fidelidad](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges-state){target="_blank"}

## Autenticación {#authentication}

Todas las llamadas a la API de retos de fidelidad requieren los siguientes encabezados:

| Encabezado | Descripción |
|---|---|
| `Authorization` | Token de portador del token de acceso de IMS |
| `x-gw-ims-org-id` | Su ID de la organización IMS |
| `x-api-key` | Su ID de cliente (clave de API) |
| `x-sandbox-name` | Nombre de la zona protegida a destino |

Siga el [tutorial de autenticación](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"} para recuperar estas credenciales.
