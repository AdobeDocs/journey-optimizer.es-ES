---
solution: Journey Optimizer
product: journey optimizer
title: campos comunes de los eventos de los recorridos
description: campos comunes de los eventos de los recorridos
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# campos comunes de los eventos de los recorridos {#sharing-common-fields}

Este grupo de campos se compartirá mediante journeyStepEvent y journeyStepProfileEvent.

Estos son los campos XDM comunes que [!DNL Journey Optimizer] envía a Adobe Experience Platform. Se enviarán campos comunes para cada paso que se procese en un recorrido. Se utilizan campos más específicos para acciones y enriquecimientos personalizados.

Algunos de estos campos solo están disponibles en patrones de procesamiento específicos (ejecución de acciones, recuperación de datos, etc.) para limitar el tamaño de los eventos.

## entrada {#entrance-field}

Indica si el usuario ha entrado en el recorrido. Si no está presente, supongamos que el valor es falso.

Tipo: booleano

Valores: true/false

## reentrada {#reentrance-field}

Indica si el usuario ha vuelto a entrar en el recorrido con la misma instancia. Si no está presente, supongamos que el valor es falso.

Tipo: booleano

Valores: true/false

## instanceEnded {#instance-ended-field}

Indica si la instancia ha finalizado (con éxito o no).

Tipo: booleano

## eventID {#eventid-field}

ID de evento en procesamiento, para el procesamiento de pasos. Si el evento es externo, el valor es eventId. Si el evento es interno, el valor es el eventId interno (como scheduledNotificationReceived, executeAction, etc.).

Tipo: string

## nodeID {#nodeid-field}

ID de nodo de cliente (desde el lienzo).

Tipo: string

## stepID {#stepdid-field}

ID único del paso que se está procesando actualmente.

Tipo: string

## stepName {#stepname-field}

Nombre del paso que se está procesando actualmente.

Tipo: string

## stepType {#steptype-field}

Tipo del paso.

Tipo: string

Valores posibles:

* Condición
* Acción
* Planificador
* Temporizador

## stepStatus {#stepstatus-field}

Estado del paso, que representa el estado del paso, cuándo se ha completado su procesamiento (y el evento de paso se ha activado).

Tipo: string

El estado puede ser:

* finalizado: el paso no tiene transición y su procesamiento ha finalizado correctamente.
* error: el procesamiento de pasos ha generado un error.
* transiciones: el paso está esperando a que un evento pase a otro paso.
* límite: el paso ha fallado en un error de restricción, producido durante una acción o enriquecimiento.
* tiempo de espera: el paso ha fallado en un error de tiempo de espera, producido durante una acción o enriquecimiento.
* instanceTimedout: el paso ha detenido su procesamiento, ya que la instancia ha alcanzado su tiempo de espera.

## journeyID {#journeyid-field}

ID del recorrido.

Tipo: string

## journeyVersionID {#journeyversionid-field}

ID de la versión del recorrido. Este id representa la referencia de identidad del recorrido, en el caso de journeyStepEvent.

Tipo: string

## journeyVersionName {#journeyversionname-field}

Nombre de la versión del recorrido.

Tipo: string

## journeyVersion {#journeyversion-field}

Versión del recorrido.

Tipo: string

## instanceID {#instanceid-field}

ID interna de la instancia de recorrido.

Tipo: string

## externalKey {#externalkey-field}

Clave externa extraída del evento para procesarla.

Tipo: string

## parentStepID {#parenstepid-field}

ID de paso del paso principal del paso procesado actual en la instancia.

Tipo: string

## parentStepName {#parentstepname-field}

Nombre del paso principal del paso actual.

Tipo: string

## parentTransitionID {#parenttransitionid-field}

Id de la transición que ha llevado la instancia al paso procesado.

Tipo: string

## parentTransitionName {#parenttransitionname-field}

Nombre de la transición que ha llevado la instancia al paso procesado.

Tipo: string

## inTest {#intest-field}

Se indica si este recorrido está en modo de prueba o no.

Tipo: booleano

## processingTime {#processingtime-field}

Cantidad total de tiempo en milisegundos desde la entrada del paso de la instancia hasta el final del procesamiento.

Tipo: long

## instanceType {#instancetype-field}

Indica el tipo de instancia, si es por lotes o unitarios.

Tipo: string

Valores: lote/unidad

## recurrenceIndex {#recurrenceindex-field}

Índice de la periodicidad si el recorrido es por lotes y recurrente (la primera ejecución tiene un índice de recurrencia = 1).

Tipo: long

## isBatchToUnitary {#isbatchtounitary-field}

Indica si esta instancia unitaria se ha activado desde una instancia por lotes.

Tipo: booleano

## batchExternalKey {#batchexternalkey-field}

Clave externa para el evento por lotes.

Tipo: string

## batchInstanceID {#batchinstanceid-field}

es el ID de instancia por lotes.

Tipo: string

## batchUnitaryBranchID {#batchunitarybranchid-field}

si la instancia se ha activado desde una instancia de lote, ID de rama unitaria.

Tipo: string
