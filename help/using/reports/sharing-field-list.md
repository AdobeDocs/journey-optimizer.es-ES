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
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 18%

---

# Lista de campos de eventos de paso {#sharing-field-list}

Los campos de eventos de paso están organizados por categoría.

* Campos de información de depuración
* Campos del recorrido
* Campos de perfil
* Campos de evento de servicio

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
| description | Cadena | Descripción del recorrido |
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
| status | Cadena | El estado del trabajo de exportación de audiencia: en cola, iniciado, finalizado |
| exportCountTotal | Número entero | El valor máximo posible del trabajo de exportación de audiencia |
| exportCountRealized | Número entero | El número real de audiencias exportadas a través del trabajo |
| exportCountFailed | Número entero | El número de audiencias que fallaron al exportar a través del trabajo |
| exportSegmentID | Cadena | El identificador de la audiencia que se exporta |
| eventType | Cadena | El tipo de evento que indica si es un evento de error del evento de información: Información, Error |
| eventCode | Cadena | El código de error que indica el motivo del eventType correspondiente |

## stepEvents {#stepevents-field}

Esta categoría contiene los campos de eventos de paso originales. Consulte esta [sección](../reports/sharing-legacy-fields.md).
