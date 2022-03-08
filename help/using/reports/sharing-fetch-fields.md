---
title: Campos de captura de datos de eventos de journeySteps
description: Campos de captura de datos de eventos de journeySteps
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 7%

---

# Campos de captura de datos de eventos de journeySteps {#sharing-fetch-fields}

Este grupo de campos se compartirá mediante journeyStepEvent y journeyStepProfileEvent.

Durante el procesamiento de un paso, es posible que no se recuperen datos en grupos de campos.

## fetchTotalTime {#fetchtotaltime-field}

Cantidad total de tiempo empleado en la recuperación de datos en millones durante el procesamiento del paso.

Tipo: long

## fetchTypeInError {#fetchtypeinerror-field}

Define si la recuperación por error se realiza en Adobe Experience Platform o en una fuente de datos personalizada.

Tipo: cadena

Valores:
* aep
* custom

## fetchError {#fetcherror-field}

Tipo de error que se produce cuando se procesa la captura de datos.

Tipo: cadena

Valores:
* http
* restricción
* timedout
* error

## fetchErrorCode {#fetcherrorcode-field}

Código de error de recuperación. Presente si el error tiene un código, como uno HTTP. Por ejemplo, si actionExecError es http, el código 404 representa el error HTTP 404.

Tipo: cadena

## fetchOriginError {#fetchoriginerror-field}

Se puede producir un tiempo de espera, en dos casos:

* en el primer intento, se ejecuta la acción . En este caso, la ejecución no ha finalizado, por lo que no hay ningún error subyacente
* en un reintento: en este caso, actionExecOrigError/actionExecOrigErrorCode describe el error encontrado en el intento antes del reintento.

Por ejemplo, se están recuperando datos del servicio de perfil unificado y se devuelve un error HTTP 500 en el primer intento. Se vuelve a intentar la recuperación, pero la duración de los 2 intentos supera el tiempo de espera. A continuación, la ejecución de la acción se etiqueta como tiempo de espera. La parte de acción tendrá el siguiente aspecto:

```
    ...
    "fetchTypeInError": "aep",
    "fieldgroupIdInError": "MyProfileFieldgroup",
    "fetchError": "timedout",
    "fetchOrigError": "http",
    "fetchOrigErrorCode": "500"
```

Tipo: cadena

## fetchOriginErrorCode {#fetchoriginerrorcode-field}

El código de error proporcionado por el sistema [!DNL Journey Orchestration] está consultando. Por ejemplo, puede ser 404, 500, etc.

Tipo: cadena

## fetchCount {#fetchcount-field}

Cuántas veces se recuperan los datos, independientemente del tipo de origen.

Tipo: long

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

Cantidad total de tiempo que se tardó en recuperar los datos de Adobe Experience Platform en millones. Comentario: esta cantidad de tiempo se calcula desde el momento en que el motor envía el evento de enriquecimiento al servicio de enriquecimiento y recibe la respuesta.

Tipo: long

## fetchPlatformCount {#fetchplatformcount-field}

Cuántas veces se recuperan los datos de Adobe Experience Platform.

Tipo: long

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

Cantidad de tiempo para recuperar los datos personalizados en milisegundos. Comentario: esta cantidad de tiempo se calcula desde el momento en que el motor envía el evento de enriquecimiento al servicio de enriquecimiento y recibe la respuesta

Tipo: long

## fetchCustomCount {#fetchcustomcount-field}

Cuántas veces se obtienen los datos personalizados de sistemas externos.

Tipo: long
