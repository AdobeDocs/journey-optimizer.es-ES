---
solution: Journey Optimizer
product: journey optimizer
title: Principios clave de la creación de campañas de varios pasos
description: Conozca los principios clave de las campañas de varios pasos con Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 326a0a47c859f475d9036c6142b057a5b59b0ae9
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 24%

---

# Principios clave de la campaña orquestada {#ms-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Campaña de varios pasos"
>abstract="En esta pantalla, puede acceder a la lista completa de campañas de varios pasos, comprobar su estado actual, las fechas de última/siguiente ejecución y crear una nueva campaña de varios pasos."

Con Adobe Journey Optimizer, puede crear campañas de varios pasos en un lienzo visual para diseñar procesos multicanal como segmentación, ejecución de campañas o procesamiento de archivos.

## ¿Qué hay dentro de una campaña de varios pasos? {#gs-ms-campaign-inside}

El lienzo de campaña de varios pasos es una representación de lo que se supone que debe suceder. Describe las diversas tareas que se realizan y cómo se relacionan entre sí.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Cada campaña de varios pasos contiene:

* **Actividades**: una actividad es una tarea que se va a realizar. Las distintas actividades disponibles se representan en el diagrama mediante iconos. Cada actividad tiene propiedades específicas y otras propiedades que son comunes a todas las actividades.

  En un diagrama de campaña de varios pasos, una actividad determinada puede producir varias tareas, en particular cuando hay un bucle o una acción recurrente.

* **Transiciones**: las transiciones vinculan una actividad de origen a una actividad de destino y definen su secuencia.

* **Tablas de trabajo**: la tabla de trabajo contiene toda la información que transmite la transición. Cada campaña de varios pasos utiliza varias tablas de trabajo. Los datos transmitidos en estas tablas se pueden utilizar en todo el ciclo de vida de la campaña de varios pasos.

## Pasos clave para crear una campaña de varios pasos {#gs-ms-campaign-steps}

Los pasos clave para crear una campaña de varios pasos son los siguientes:

![](assets/workflow-creation-process.png){zoomable="yes"}

## Acceso a campañas de varios pasos

En el menú **[!UICONTROL Campañas]**, vaya a la pestaña Varios pasos para acceder a la lista completa de campañas de varios pasos.

Cada campaña de varios pasos en la lista muestra información sobre su [estado](#status) actual, la última vez que se ejecutó o modificó, y la siguiente fecha y hora de ejecución programada.

Puede personalizar las columnas mostradas haciendo clic en el icono **[!UICONTROL Configurar la columna para un diseño personalizado]** situado en la esquina superior derecha de la lista. Esto le permite agregar información adicional a la lista, como la última actividad con error para cada campaña de varios pasos o la dimensión de segmentación aplicada.

Además, hay una barra de búsqueda y filtros disponibles para facilitar la búsqueda dentro de la lista. Por ejemplo, puede filtrar las campañas de varios pasos para mostrar solo las que pertenecen a una campaña o las procesadas durante un intervalo de fechas específico.

Para duplicar o eliminar una campaña de varios pasos, haz clic en el botón de puntos suspensivos y selecciona **[!UICONTROL Duplicar]** o **[!UICONTROL Eliminar]**.

>[!NOTE]
>
>Cuando una campaña de varios pasos está en curso, puede duplicarla, pero no puede eliminarla.

## Estados y ciclo vital {#status}

Las campañas pueden tener varios estados:

* **[!UICONTROL Borrador]**: la campaña de varios pasos se ha creado y guardado.
* **[!UICONTROL En curso]**: la campaña de varios pasos se está ejecutando.
* **[!UICONTROL Finalizado]**: la ejecución de la campaña de varios pasos ha finalizado.
* **[!UICONTROL En pausa]**: la campaña de varios pasos se ha pausado.
* **[!UICONTROL Erróneo]**: la campaña de varios pasos encontró un error. Abra la campaña de varios pasos y acceda a los registros y tareas para identificar el error y resolverlo.


## Creación de una consulta

## Directrices de Personalization
