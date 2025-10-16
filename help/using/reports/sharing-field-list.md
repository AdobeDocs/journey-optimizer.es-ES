---
solution: Journey Optimizer
product: journey optimizer
title: Lista de campos de eventos de paso
description: Lista de campos de eventos de paso
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: f9102c10aa58be0e1a7280aa53fd97b3f792b9e9
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 10%

---

# Lista de campos de eventos de paso {#sharing-field-list}

Los campos de eventos de paso están organizados por categoría.

* Campos de información de depuración
* Campos del recorrido
* Campos de perfil
* Campos de evento de servicio

Para el atributo identityMap, la identidad principal se define de forma predeterminada como &quot;primary = true&quot;.

## debugInfo {#debuginfo-field}

| Nombre del campo | Tipo | Descripción |
|---|---|------------|
| requestId | Cadena | El ID de solicitud utilizado por Journey Optimizer para rastrear el flujo de una solicitud. |

## recorrido {#journey-field}

Este grupo de campos se utiliza en el esquema de recorrido (en relación con journeyStepEvent). Contiene los siguientes campos:

| Nombre del campo | Tipo | Descripción |
|---|---|------------|
| ID | Cadena | Identificador del Recorrido determinado |
| VersionID | Cadena | ID de la versión del recorrido. Este ID representa la identidad de un recorrido |
| name | Cadena | Nombre del recorrido |
| descripción | Cadena | Descripción del recorrido |
| version | Cadena | versión, representada como `major`.`minor` |

## perfil {#profile-field}

Este grupo de campos es específico de journeyStepEvent: este evento está relacionado con el recorrido y no tiene el identityMap, que describe la identidad del perfil, si la hay.

Para journeyStepEvent, también es necesario añadir campos relacionados con la identidad:

| Nombre del campo | Tipo | Descripción |
|---|---|------------|
| ID | Cadena | El identificador de perfil identifica el perfil enviado/utilizado en un recorrido. Por ejemplo: foo@adobe.com. |
| namespace | Cadena | En este campo se describe el área de nombres a la que hace referencia el perfil utilizado en el Recorrido. Por ejemplo: correo electrónico, ECID |

## serviceEvents {#servicevents-field}

Este mixin contiene todos los campos correspondientes a un trabajo de exportación de perfiles.

| Nombre del campo | Tipo | Descripción |
|---|---|------------|
| ID | Cadena | El identificador del trabajo de exportación de audiencia activado |
| estado | Cadena | El estado del trabajo de exportación de audiencia: en cola, iniciado, finalizado |
| exportCountTotal | Entero | El valor máximo posible del trabajo de exportación de audiencia |
| exportCountRealized | Entero | El número real de audiencias exportadas a través del trabajo |
| exportCountFailed | Entero | El número de audiencias que fallaron al exportar a través del trabajo |
| exportSegmentID | Cadena | El identificador de la audiencia que se exporta |
| eventType | Cadena | El tipo de evento que indica si es un evento de error o un evento de información: Información, Error |
| eventCode | Cadena | El código de error que indica el motivo del eventType correspondiente |

Obtenga más información acerca de eventTypes [en esta sección](#discarded-events).

## stepEvents {#stepevents-field}

Esta categoría contiene los campos de eventos de paso originales. Consulte esta [sección](../reports/sharing-legacy-fields.md).


## Solucionar problemas de tipos de eventos descartados en eventos de paso de Recorrido  {#discarded-events}

Al consultar eventos de paso de recorrido para registros con `eventCode = 'discard'`, puede encontrar varios tipos de evento.

A continuación encontrará definiciones, causas comunes y pasos de solución de problemas para el descarte más frecuente `eventTypes`:

* EXTERNAL_KEY_COMPUTATION_ERROR: El sistema no pudo calcular un identificador único (clave externa) para el cliente a partir de los datos de evento.

|---|---|
| **Causas comunes** | Identificadores de cliente faltantes o mal formados (por ejemplo, correo electrónico, ID de cliente) en la carga útil de evento. |
| **Resolución de problemas** | Compruebe la configuración de eventos para ver los identificadores necesarios, asegúrese de que los datos de evento estén completos y tengan el formato correcto. |

* NO_INTERESTED_RECORRIDO_FOR_SEGMENTMEMBERSHIP_EVENT: Se ha recibido un evento de calificación de segmentos, pero no hay recorridos configurados para responder a este segmento.


|---|---|
| **Causas comunes** | Ningún recorrido utiliza el segmento como déclencheur, los recorridos están en estado de borrador/detenido o los ID de segmento no coinciden. |
| **Resolución de problemas** | Asegúrese de que al menos un recorrido esté activo y configurado para el segmento y compruebe los ID de este. |

### RECORRIDO_INSTANCE_ID_NOT_CREATE: Error del sistema al crear una instancia de recorrido para el cliente.

|---|---|
| **Causas comunes** | Eventos duplicados, gran volumen de eventos, restricciones de recursos del sistema. |
| **Resolución de problemas** | Implemente la anulación de duplicación, evite picos de tráfico, optimice el diseño del recorrido y póngase en contacto con el servicio de asistencia si persiste. |

### EVENT_WITH_NO_RECORRIDO: se recibió un evento, pero no hay ningún recorrido activo configurado para responder a él

|---|---|
| **Causas comunes** | El nombre/ID del evento no coincide, el recorrido no se ha publicado, la zona protegida/organización es incorrecta, el modo de prueba/perfil no coincide. |
| **Resolución de problemas** | Compruebe la configuración de eventos y recorridos, compruebe el estado del recorrido y utilice las herramientas de depuración. |

Para descartes que se produzcan en recorridos pausados:

* **PAUSED_RECORRIDO_VERSION**: descartes que se produjeron en el punto de entrada del recorrido
* **RECORRIDO_IN_PAUSED_STATE**: descarta lo que ocurrió cuando los perfiles están en un recorrido

Obtenga más información acerca de estos eventos y cómo solucionarlos en la sección [Pausar un Recorrido](../building-journeys/journey-pause.md#troubleshoot-profile-discards-in-paused-journeys).

## Recursos adicionales

* [Ejemplos de consultas de conjuntos de datos: evento de paso de Recorrido](../data/datasets-query-examples.md#journey-step-event).
* [Ejemplos de consultas: consultas basadas en eventos](query-examples.md#event-based-queries).
* [Diccionario de esquemas integrado](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=es)

