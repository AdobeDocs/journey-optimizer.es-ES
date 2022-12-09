---
solution: Journey Optimizer
product: journey optimizer
title: Campos de ejecución de la acción eventos de los journeyStep
description: Campos de ejecución de la acción eventos de los journeyStep
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Campos de ejecución de la acción eventos de los journeyStep {#sharing-execution-fields}

Este grupo de campos se compartirá mediante journeyStepEvent y journeyStepProfileEvent.

Si el paso tiene que procesarse una acción, esos campos se añaden a la carga útil de evento.

## actionID {#actionid-field}

ID de la acción que se está ejecutando.

Tipo: string

## actionName {#actionname-field}

Nombre de la acción. Si no se ha establecido ningún nombre, se tomará el valor stepName.

Tipo: string

## actionType {#actionType-field}

Tipo de acción.

Tipo: string

## actionParameterized {#actionparameterized-field}

Indica si la acción está parametrizada o no.

Tipo: booleano

## actionExecutionTime {#actionexecutiontime-field}

Cantidad de tiempo (en milisegundos) que se tarda en ejecutar una acción actual.

Tipo: long

## actionExecutionError {#actionexecutionerror-field}

Tipo de error que se produce cuando se llama a la acción.

Tipo: string

Valores:
* http
* restricción
* timeout
* error

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

Código de error de ejecución de acción. Presente si el error tiene un código, como uno HTTP.

Tipo: string

## actionExecutionOriginError {#actionexecutionoriginerror-field}

Se puede producir un tiempo de espera, en dos casos:

* en el primer intento se ejecuta una acción. En este caso, la ejecución no ha finalizado, por lo que no hay ningún error subyacente
* en un reintento: en este caso, actionExecOrigError/actionExecOrigErrorCode describe el error encontrado en el intento antes del reintento.

Por ejemplo, se envía un correo electrónico y se devuelve un error HTTP 500 en el primer intento. Se vuelve a intentar la recuperación, pero la duración de los 2 intentos supera el tiempo de espera. A continuación, la ejecución de la acción se etiqueta como tiempo de espera. La parte de acción tendrá el siguiente aspecto:

```
    ...
    "actionId": "myActionId",
    "actionName": "My mail sending",
    "actionType": "acsRestAction",
    "actionParameterized": true,
    "actionExecError": "timedout",
    "actionExecOrigError": "http",
    "actionExecOrigErrorCode": "500"
```

Tipo: string

## actionExecutionOriginCode {#actionexecutionorigincode-field}

Código de error de actionExecOrigError.

Tipo: string

## actionBusinessType {#actionbusinesstype-field}

Indica el tipo de acción.

Valores:

* creación
* Correo electrónico ACS
* SMS ACS
* ACS Push
* cliente
* Epsilon
* ...

Tipo: string

## deliveryJobID {#deliveryjobid-field}

Esto describe el Id. de trabajo de entrega para el recorrido por lotes.

Tipo: string

## batchDeliveryID {#batchdeliveryid-field}

Esto describe el ID de entrega para el recorrido por lotes.

Tipo: string

## fromSegmentTrigger {#fromsegmenttrigger-field}

Esto describe si el recorrido por lotes se activa desde el segmento de audiencia.

Tipo: booleano

## actionSchedulerCount {#actionschedulercount-field}

Recuento de solicitudes de notificación del planificador enviadas al servicio del planificador durante el procesamiento de pasos.

Tipo: long
