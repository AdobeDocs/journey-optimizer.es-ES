---
solution: Journey Optimizer
product: journey optimizer
title: Lista de campos de eventos de paso
description: Lista de campos de eventos de paso
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
TQID: https://experienceleague.adobe.com/7sYxw--oKKa6SnRgoXnwFxme5n-6L4pe9SR-AKZOmHA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 806
ht-degree: 8%

---

# Lista de campos de eventos de paso {#sharing-field-list}

>[!BEGINSHADEBOX]

**En esta página:** Haga referencia a los campos de eventos de paso de recorrido organizados por categoría, incluidos los campos de eventos de depuración, recorrido, perfil y servicio, y solucione los tipos de eventos descartados.

>[!ENDSHADEBOX]

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

Este mixin contiene todos los campos correspondientes a un trabajo de exportación de perfiles. Estos eventos se generan por cada actividad de **Leer audiencia** para hacer un seguimiento del ciclo de vida de las operaciones de exportación de la audiencia (en cola, iniciadas, finalizadas, errores). A diferencia de los eventos de paso normales, serviceEvents no está vinculado a perfiles individuales sino al propio nodo Leer audiencia, lo que significa que es posible que no tengan un identificador de perfil asociado.

| Nombre del campo | Tipo | Descripción |
|---|---|------------|
| ID | Cadena | El identificador del trabajo de exportación de audiencia activado |
| estado | Cadena | El estado del trabajo de exportación de audiencia: en cola, iniciado, finalizado |
| exportCountTotal | Número entero | El valor máximo posible del trabajo de exportación de audiencia |
| exportCountRealized | Número entero | El número real de audiencias exportadas a través del trabajo |
| exportCountFailed | Número entero | El número de audiencias que fallaron al exportar a través del trabajo |
| exportSegmentID | Cadena | El identificador de la audiencia que se exporta |
| eventType | Cadena | El tipo de evento que indica si es un evento de error o un evento de información: Información, Error |
| eventCode | Cadena | El código de error que indica el motivo del eventType correspondiente |

Obtenga más información acerca de eventTypes [en esta sección](#discarded-events).

## stepEvents {#stepevents-field}

Esta categoría contiene los campos de eventos de paso originales. Consulte esta [sección](../reports/sharing-legacy-fields.md).


## Solucionar problemas de tipos de eventos descartados en eventos de paso de Recorrido  {#discarded-events}

Al consultar eventos de paso de recorrido para registros con `eventCode = 'discard'`, puede encontrar varios tipos de evento.

A continuación encontrará definiciones, causas comunes y pasos de solución de problemas para el descarte más frecuente `eventTypes`:

* **EXTERNAL_KEY_COMPUTATION_ERROR**: el sistema no pudo calcular un identificador único (clave externa) para el cliente a partir de los datos de evento.

  **Causas comunes**: Faltan identificadores de cliente o tienen un formato incorrecto (por ejemplo, correo electrónico, ID de cliente) en la carga útil de evento.

  **Solución de problemas**: compruebe la configuración del evento para ver los identificadores necesarios, asegúrese de que los datos del evento estén completos y tengan el formato correcto.

* **NO_INTERESTED_RECORRIDO_FOR_SEGMENTMEMBERSHIP_EVENT**: se recibió un evento de calificación de segmentos, pero no hay recorridos configurados para responder a este segmento.

  **Causas comunes**: Ningún recorrido usa el segmento como déclencheur, los recorridos están en estado de borrador/detenido o los ID de segmento no coinciden.

  **Solución de problemas**: Asegúrese de que haya al menos un recorrido activo y configurado para el segmento y compruebe los ID de segmento.

* **RECORRIDO_INSTANCE_ID_NOT_CREATED**: el sistema no pudo crear una instancia de recorrido para el cliente.

  **Causas comunes**: Eventos duplicados, volumen de evento alto, restricciones de recursos del sistema.

  **Solución de problemas**: Implemente la anulación de duplicación, evite los picos de tráfico, optimice el diseño del recorrido y [póngase en contacto con el servicio de asistencia](../start/user-interface.md#support-ticket-guidelines) si es persistente.

* **maxInstanceStackEventsReached**: El tiempo de ejecución de recorrido alcanzó el límite interno de 10 eventos de pila por perfil para una versión de recorrido determinada.

  **Causas comunes**: La instancia de recorrido del perfil está bloqueada en un paso de larga ejecución (por ejemplo, esperas largas, enriquecimientos lentos o reintentos de acciones personalizadas) y eventos para el mismo perfil, que también se están utilizando en ese recorrido, se acumulan más allá del límite de 10 eventos.

  **Solución de problemas**: reduzca los pasos de larga duración en las rutas que pueden volver a almacenar en déclencheur con frecuencia, devuelva o deduplique eventos ascendentes y divida los escenarios largos en varios recorridos. Se trata de una protección de seguridad y el límite no se puede configurar; los eventos adicionales se descartan hasta que la pila se drene. Para obtener más información, consulte [Eventos descartados debido a una instancia de recorrido bloqueada](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached).

* **EVENT_WITH_NO_RECORRIDO**: se recibió un evento, pero no se configuró ningún recorrido activo para responderlo

  **Causas comunes**: El nombre/ID del evento no coincide, el recorrido no se ha publicado, la zona protegida/organización es incorrecta, el modo de prueba/no coincide el perfil.

  **Solución de problemas**: compruebe la configuración del evento y del recorrido, compruebe el estado del recorrido y use las herramientas de depuración.

* Para descartes que se produzcan en recorridos pausados:

   * **PAUSED_RECORRIDO_VERSION**: descartes que se produjeron en el punto de entrada del recorrido
   * **RECORRIDO_IN_PAUSED_STATE**: descarta lo que ocurrió cuando los perfiles están en un recorrido

  Obtenga más información acerca de estos eventos y cómo solucionarlos en la sección [Pausar un Recorrido](../building-journeys/journey-pause.md#discards-troubleshoot).

## Recursos adicionales

* [Ejemplos de consultas de conjuntos de datos: evento de paso de Recorrido](../data/datasets-query-examples.md#journey-step-event).
* [Ejemplos de consultas: consultas basadas en eventos](query-examples.md#event-based-queries).
* [Ejemplos de consultas: consultas de reglas de negocio](query-examples.md#business-rules-queries).
* [Diccionario de esquemas integrado](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=es)

