---
solution: Journey Optimizer
product: journey optimizer
title: Campos de ejecución de la acción de eventos de journeySteps
description: Campos de ejecución de la acción de eventos de journeySteps
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: b93d2288156713ac7479eef491f6104df1955a18
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 2%

---

# Campos de ejecución de la acción de eventos de journeySteps {#sharing-execution-fields}

Este grupo de campos lo compartirán journeyStepEvent y journeyStepProfileEvent.

Si el paso tiene una acción que procesar, esos campos se añadirán a la carga útil de evento.

## actionID {#actionid-field}

ID de la acción que se está ejecutando.

Tipo: cadena

## actionName {#actionname-field}

Nombre de la acción. Si no se ha definido ningún nombre, se tomará el stepName.

Tipo: cadena

## actionType {#actionType-field}

Tipo de acción.

Tipo: cadena

## actionParameterized {#actionparameterized-field}

Indica si la acción está parametrizada o no.

Tipo: booleano

## actionExecutionTime {#actionexecutiontime-field}

Cantidad de tiempo (en milisegundos) que se tarda en ejecutar una acción actual.

Tipo: long

El campo `actionExecutionTime` representa el tiempo total (en milisegundos) que se tarda en ejecutar la acción, incluido el tiempo que la solicitud ha estado esperando en la cola (si se ha configurado la restricción y se ha alcanzado el límite de velocidad) y el tiempo de ejecución real (incluida la latencia de red al extremo externo).

El campo `Timestamp` indica la hora de finalización de la ejecución de la acción. Para determinar cuándo entró el perfil en el nodo de acción personalizada, reste `actionExecutionTime` de `Timestamp`.

Por ejemplo, si `Timestamp` es &quot;2025-02-04 09:39:03 UTC&quot; y `actionExecutionTime` es 1.813.227 ms (~31 minutos), el perfil ingresó al nodo aproximadamente en &quot;2025-02-04 09:08:32 UTC&quot;.


## actionExecutionError {#actionexecutionerror-field}

Tipo de error que se produce cuando se llama a la acción.

Tipo: cadena

Valores:

* http
* límite
* timeout
* error

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

Código para error de ejecución de acción. Está presente si el error tiene un código, como uno HTTP.

Tipo: cadena

## actionExecutionOriginError {#actionexecutionoriginerror-field}

Se puede producir un tiempo de espera en dos casos:

* en el primer intento se ejecuta una acción. En este caso, la ejecución no ha finalizado, por lo que no hay ningún error subyacente
* en un reintento: en este caso, actionExecOrigError/actionExecOrigErrorCode describe el error encontrado en el intento antes del reintento.

Por ejemplo, se envía un correo electrónico y se devuelve un error HTTP 500 en el primer intento. Se vuelve a intentar realizar la recuperación, pero la duración de los dos intentos supera el tiempo de espera. A continuación, la ejecución de la acción se etiqueta como timeout. La parte de acción tendrá este aspecto:

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

Tipo: cadena

## actionExecutionOriginCode {#actionexecutionorigincode-field}

Código de error de actionExecOrigError.

Tipo: cadena

## actionOriginEndpoint {#actionoriginendpoint}

URI del extremo de acción personalizada utilizado en la acción.

Tipo: cadena

## actionOriginMethod {#actionoriginmethod}

Describe el método utilizado en la solicitud HTTP (GET o POST).

Tipo: cadena

## actionOriginIsMTLS {#actionoriginismtls}

Describe si MTLS está habilitado para el punto de conexión.

Tipo: booleano

## actionIsProxy {#actionisproxy}

Describe si se utiliza un proxy HTTP con un intervalo de direcciones IP definido para la llamada.

Tipo: booleano

## actionExecutionOriginStartTime {#actionexecutionoriginstarttime}

Describe la marca de tiempo a la que se inicia la solicitud HTTP. En caso de reintento, esta es la marca de tiempo a la que se inicia el último intento de reintento. La marca de tiempo utiliza el formato ISO8601 en la zona horaria UTC.

Tenga en cuenta que esta marca de tiempo generalmente se muestra ligeramente después de que el perfil entre en el nodo de acción personalizada, o significativamente después de que entre en el nodo en caso de regulación.

Tipo: marca de tiempo

## actionExecutionOriginTime {#actionexecutionorigintime}

Describe el tiempo de respuesta de la llamada HTTP. En caso de reintento, este es el tiempo que tarda el último intento de reintento. Mide el tiempo desde el momento en que se inicia la solicitud HTTP hasta el momento en que el servidor devuelve la respuesta completa. Tenga en cuenta que esto excluye el tiempo de espera en cola en caso de regulación.

Tipo: long

## actionIsThrottled {#actionisthrottled}

Esto describe si la restricción está habilitada para el extremo.

Tipo: booleano

## actionWaitTime {#actionwaittime}

Esto describe cuándo se alcanza el límite de velocidad configurado para un punto de conexión limitado, las llamadas se ponen en cola y se procesan a la velocidad configurada. Este campo indica la cantidad de tiempo que la llamada ha invertido esperando en la cola antes de ejecutarse. Solo se especifica si actionIsThrottled == true.

Tipo: long

## actionBusinessType {#actionbusinesstype-field}

Indica el tipo de acción.

Valores:

* integrado
   * Correo electrónico ACS
   * ACS SMS
   * Push de ACS
* cliente
   * Épsilon
   * ...

Tipo: cadena

## deliveryJobID {#deliveryjobid-field}

Se describe el ID de trabajo de envío para el Recorrido por lotes.

Tipo: cadena

## batchDeliveryID {#batchdeliveryid-field}

Describe la ID de envío del Recorrido por lotes.

Tipo: cadena

## fromSegmentTrigger {#fromsegmenttrigger-field}

Describe si el Recorrido por lotes se activa desde el segmento de audiencia.

Tipo: booleano

## actionSchedulerCount {#actionschedulercount-field}

Recuento de solicitudes de notificación del planificador enviadas al servicio del planificador durante el procesamiento del paso.

Tipo: long
