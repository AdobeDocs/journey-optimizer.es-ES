---
solution: Journey Optimizer
product: journey optimizer
title: Campos de captura de datos de eventos de journeySteps
description: Campos de captura de datos de eventos de journeySteps
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
TQID: https://experienceleague.adobe.com/obaiLWD6yq0dZ5ZhE69q-iLHzI99ll7XJnMNlOpJp1A
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 377
ht-degree: 4%

---

# Campos de captura de datos de eventos de journeySteps {#sharing-fetch-fields}

Este grupo de campos lo compartirán journeyStepEvent y journeyStepProfileEvent.

Durante el procesamiento de un paso, es posible que no se recuperen datos en los grupos de campos.

## fetchTotalTime {#fetchtotaltime-field}

Cantidad total de tiempo invertido en la captura de datos en milisegundos durante el procesamiento del paso.

Tipo: long

## fetchTypeInError {#fetchtypeinerror-field}

Define si la recuperación con error se realiza en Adobe Experience Platform o en una fuente de datos personalizada.

Tipo: cadena

Valores:

* aep
* personalizado

## fetchError {#fetcherror-field}

Tipo de error que se produce cuando se procesa la captura de datos.

Tipo: cadena

Valores:

* http
* límite
* timeout
* error

## fetchErrorCode {#fetcherrorcode-field}

Código para error de recuperación. Está presente si el error tiene un código, como uno HTTP. Por ejemplo, si actionExecError es http, el código 404 representa el error HTTP 404.

Tipo: cadena

## fetchOriginError {#fetchoriginerror-field}

Se puede producir un tiempo de espera en dos casos:

* en el primer intento, se ejecuta la acción. En este caso, la ejecución no ha finalizado, por lo que no hay ningún error subyacente
* en un reintento: en este caso, actionExecOrigError/actionExecOrigErrorCode describe el error encontrado en el intento antes del reintento.

Por ejemplo, se están recuperando datos del servicio de perfil unificado y se devuelve un error HTTP 500 en el primer intento. Se vuelve a intentar realizar la recuperación, pero la duración de los dos intentos supera el tiempo de espera. A continuación, la ejecución de la acción se etiqueta como timeout. La parte de acción tendrá este aspecto:

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

Se está consultando el código de error proporcionado por el sistema [!DNL Journey Optimizer]. Por ejemplo, puede ser un 404, 500, etc.

Tipo: cadena

## fetchCount {#fetchcount-field}

La cantidad de veces que se recuperan los datos, independientemente del tipo de origen.

Tipo: long

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

Cantidad total de tiempo que se tarda en recuperar los datos de Adobe Experience Platform en milisegundos. Observación: esta cantidad de tiempo se calcula desde el momento en que el motor envía el evento de enriquecimiento al servicio de enriquecimiento y recibe la respuesta.

Tipo: long

## fetchPlatformCount {#fetchplatformcount-field}

La cantidad de veces que se recuperan los datos de Adobe Experience Platform.

Tipo: long

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

Cantidad de tiempo para recuperar los datos personalizados en milisegundos. Observación: esta cantidad de tiempo se calcula desde el momento en que el motor envía el evento de enriquecimiento al servicio de enriquecimiento y recibe la respuesta

Tipo: long

## fetchCustomCount {#fetchcustomcount-field}

Cantidad de veces que se recuperan los datos personalizados de sistemas externos.

Tipo: long
