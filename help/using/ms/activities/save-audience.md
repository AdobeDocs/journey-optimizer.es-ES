---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Guardar audiencia
description: Aprenda a utilizar la actividad Bifurcación en una campaña de varios pasos
hide: true
hidefromtoc: true
exl-id: 84e34d21-dca1-4203-8539-f2b20e461936
source-git-commit: 323472ef9d6203cbbadc44ceb17ddcc7f6207323
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 15%

---

# Guardar público {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Guardar un público"
>abstract="Utilice esta actividad para actualizar un público existente o crear uno nuevo a partir de la población calculada en sentido ascendente en la campaña de varios pasos. Los públicos creados se añaden a la lista de públicos y están disponibles en el menú **Públicos**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_saveaudience_outbound"
>title="Generar transición de salida"
>abstract="Utilice esta opción si desea añadir una transición después de la actividad **Guardado de público**."

La actividad **Guardar audiencia** es una actividad de **segmentación**. Esta actividad le permite actualizar una audiencia existente o crear una nueva a partir de la población calculada en sentido ascendente en una campaña de varios pasos. Las audiencias creadas se agregan a la lista de audiencias de aplicación y están disponibles a través del menú **Audiencias**.

Esta actividad se utiliza esencialmente para mantener los grupos de población calculados en la misma campaña de varios pasos, convirtiéndolos en audiencias reutilizables. Conéctelo a otras actividades de segmentación, como una **audiencia de compilación** o una actividad **Combinar**.

## Configuración de la actividad Guardar audiencia{#save-audience-configuration}

Siga estos pasos para configurar la actividad **Guardar audiencia**:

![](../assets/workflow-save-audience.png)

1. Agregue una actividad **Guardar audiencia** a su campaña de varios pasos.

1. En la lista desplegable **Modo**, seleccione la acción que desee llevar a cabo:

   * **Crear o actualizar una audiencia existente**: defina una **etiqueta de audiencia**. Si la audiencia ya existe, se actualiza; de lo contrario, se crea una nueva.

   * **Actualizar una audiencia existente**: elija la **audiencia** que desee actualizar entre la lista de audiencias existentes.

1. Seleccione el **modo de actualización** que se aplicará a las audiencias existentes:

   * **Reemplazar contenido de audiencia por nuevos datos**: se reemplaza todo el contenido de audiencia. Se pierden los datos antiguos. Solo se conservan los datos de la transición entrante de la actividad Guardar audiencia. Esta opción borra el tipo de audiencia y la dimensión de segmentación de la audiencia actualizada.

   * **Audiencia completa con nuevos datos**: el contenido de audiencia anterior se conserva y los datos de la transición de entrada de la actividad Guardar audiencia se agregan a ella.

1. Marque la opción **Generar una transición saliente** si desea agregar una transición después de la actividad **Guardar audiencia**.

El contenido de la audiencia guardada está disponible en la vista de detalles de la audiencia, a la que se puede acceder desde el menú **Audiencias**. Las columnas disponibles en esta vista corresponden a las columnas de la transición de entrada de la actividad **Guardar audiencia** de la campaña de varios pasos.


## Ejemplo{#save-audience-example}

El siguiente ejemplo ilustra una actualización de audiencia simple desde la segmentación. Se agrega un planificador para ejecutar la campaña de varios pasos una vez al mes. Una consulta recupera todos los perfiles suscritos a las diferentes aplicaciones disponibles. La actividad **Guardar audiencia** actualiza la audiencia eliminando perfiles que han cancelado la suscripción al servicio desde la última ejecución de campaña de varios pasos y agregando los perfiles recién suscritos.
