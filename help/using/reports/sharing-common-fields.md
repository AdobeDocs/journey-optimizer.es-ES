---
solution: Journey Optimizer
product: journey optimizer
title: campos comunes de eventos de recorridos
description: campos comunes de eventos de recorridos
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
TQID: https://experienceleague.adobe.com/MWcV6FkgtiFJd9Y7q8CvTXQsL68cD5JcvqjmoEyiYhI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 634
ht-degree: 0%

---

# campos comunes de eventos de recorridos {#sharing-common-fields}

Este grupo de campos será compartido por los eventos siguientes: **journeyStepEvent** y **journeyStepProfileEvent**.

Estos son los campos XDM comunes que [!DNL Journey Optimizer] envía a Adobe Experience Platform. Se envían campos comunes para cada paso que se procesa en un recorrido. Se utilizan campos más específicos para acciones personalizadas y enriquecimientos.

Algunos de estos campos solo están disponibles en patrones de procesamiento específicos (ejecución de acciones, recuperación de datos, etc.) para limitar el tamaño de los eventos.


>[!NOTE]
>
>Obtenga más información acerca de los atributos de propiedades de recorrido [en esta sección](../building-journeys/expression/journey-properties.md#journey-properties-fields).


## entrada {#entrance-field}

Indica si el usuario ha introducido el recorrido. Si no está presente, suponemos que el valor es falso.

Tipo: booleano

Valores: true/false

## reentrada {#reentrance-field}

Indica si el usuario ha vuelto a entrar en el recorrido con la misma instancia. Si no está presente, suponemos que el valor es falso.

Tipo: booleano

Valores: true/false

## instanceEnded {#instance-ended-field}

Indica si la instancia ha finalizado (correctamente o no).

Tipo: booleano

## eventID {#eventid-field}

ID de evento en procesamiento, para el procesamiento de pasos. Si el evento es externo, el valor es su eventId. Si el evento es interno, el valor es el eventId interno (como scheduledNotificationReceived, executeAction, etc.).

Tipo: cadena

## nodeID {#nodeid-field}

ID del nodo del cliente (desde el lienzo).

Tipo: cadena

## stepID {#stepdid-field}

ID único del paso que se está procesando actualmente.

Tipo: cadena

## stepName {#stepname-field}

Nombre de la etapa que se está procesando actualmente.

Tipo: cadena

## stepType {#steptype-field}

Tipo de paso.

Tipo: cadena

Valores posibles:

* Condición
* Acción
* Planificador
* Temporizador

## stepStatus {#stepstatus-field}

Estado del paso, que representa el estado del paso, cuando se ha realizado su procesamiento (y se ha activado el evento del paso).

Tipo: cadena

El estado puede ser el siguiente:

* ended: el paso no tiene transición y su procesamiento ha finalizado correctamente.
* error: el procesamiento de pasos ha producido un error.
* transiciones: el paso está esperando un evento para pasar a otro paso.
* límite: el paso ha fallado debido a un error de límite, producido durante una acción o enriquecimiento.
* timeout: el paso ha fallado en un error de timeout, producido durante una acción o enriquecimiento.
* instanceTimedout: el paso ha detenido su procesamiento porque la instancia ha alcanzado su tiempo de espera.

## journeyID {#journeyid-field}

ID del recorrido.

Tipo: cadena

## journeyVersionID {#journeyversionid-field}

ID de la versión del recorrido. Este ID representa la referencia de identidad al recorrido, en el caso de journeyStepEvent.

Tipo: cadena

>[!NOTE]
>
>Para solucionar problemas, recomendamos utilizar journeyVersionID en lugar de journeyVersionName al consultar recorridos.

## journeyVersionName {#journeyversionname-field}

Nombre de la versión del recorrido.

Tipo: cadena

>[!NOTE]
>
>Para solucionar problemas, recomendamos utilizar journeyVersionID en lugar de journeyVersionName al consultar recorridos.

## journeyVersion {#journeyversion-field}

Versión de la versión del recorrido.

Tipo: cadena

## instanceID {#instanceid-field}

ID interno de la instancia de recorrido.

Tipo: cadena

## externalKey {#externalkey-field}

Clave externa extraída del evento para procesarlo.

Tipo: cadena

## parentStepID {#parenstepid-field}

ID del paso principal del paso procesado actual en la instancia.

Tipo: cadena

## parentStepName {#parentstepname-field}

Nombre del paso principal del paso actual.

Tipo: cadena

## parentTransitionID {#parenttransitionid-field}

ID de la transición que ha llevado la instancia al paso procesado.

Tipo: cadena

## parentTransitionName {#parenttransitionname-field}

Nombre de la transición que ha llevado la instancia al paso procesado.

Tipo: cadena

## inTest {#intest-field}

Se indica si este recorrido está en modo de prueba o no.

Tipo: booleano

## processingTime {#processingtime-field}

Cantidad total de tiempo en milisegundos desde la entrada del paso de instancia hasta el final del procesamiento.

Tipo: long

## instanceType {#instancetype-field}

Indica el tipo de instancia, si es por lotes o unitario.

Tipo: cadena

Valores: lote/unitario

## recurrenceIndex {#recurrenceindex-field}

Índice de periodicidad si el recorrido es por lotes y recurrente (la primera ejecución tiene recurrenceIndex = 1).

Tipo: long

## isBatchToUnitary {#isbatchtounitary-field}

Indica si esta instancia unitaria se ha activado desde una instancia de lote.

Tipo: booleano

## batchExternalKey {#batchexternalkey-field}

Clave externa del evento por lotes.

Tipo: cadena

## batchInstanceID {#batchinstanceid-field}

este es el ID de instancia de lote.

Tipo: cadena

## batchUnitaryBranchID {#batchunitarybranchid-field}

si la instancia se ha activado desde una instancia de lote, ID de rama unitario.

Tipo: cadena

## exitCriteriaID

ID de exitCriteria

Tipo: cadena

## exitCriteriaName

Nombre de exitCriteria

Tipo: cadena