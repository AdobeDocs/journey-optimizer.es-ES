---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad de anulación de duplicación
description: Aprenda a utilizar la actividad de anulación de duplicación
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 57%

---

# Deduplicación {#deduplication}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_fields"
>title="Campos para identificar los duplicados"
>abstract="En la sección **Campos para identificar duplicados**, haga clic en el botón **Añadir atributo** para especificar los campos para los que los valores idénticos permiten identificar los duplicados, tales como: dirección de correo electrónico, nombre, apellidos, etc. El orden de los campos permite especificar los que se procesarán en primer lugar."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication"
>title="Actividad de deduplicación"
>abstract="La actividad de **deduplicación permite** eliminar duplicados en los resultados de las actividades entrantes. Se utiliza principalmente después de actividades de segmentación y antes de actividades que permiten el uso de datos direccionados."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_complement"
>title="Generación de un complemento"
>abstract="Puede generar una transición saliente adicional con la población restante, que se excluyó como duplicado. Para ello, active la opción **Generar complemento**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_settings"
>title="Configuración de la deduplicación"
>abstract="Para eliminar duplicados en los datos entrantes, defina el método de deduplicación en los campos siguientes. De forma predeterminada, solo se guarda un registro. También debe seleccionar el modo de deduplicación en función de una expresión o un atributo. De forma predeterminada, el registro que se va a excluir de los duplicados se selecciona de forma aleatoria."

La actividad **Deduplication** es una actividad de **segmentación**. Esta actividad le permite eliminar duplicados en los resultados de las actividades entrantes, por ejemplo perfiles duplicados en la lista de destinatarios. La actividad **Deduplication** se utiliza generalmente después de actividades de segmentación y antes de actividades que permiten el uso de datos de destino.

## Configuración de la actividad de anulación de duplicación{#deduplication-configuration}

Siga estos pasos para configurar la actividad **Deduplication**:

![](../assets/workflow-deduplication.png)

1. Agregue una actividad **Deduplication** a su campaña de varios pasos.

1. En la sección **Campos para identificar duplicados**, haga clic en el botón **Añadir atributo** para especificar los campos para los que los valores idénticos permiten identificar los duplicados, tales como: dirección de correo electrónico, nombre, apellidos, etc. El orden de los campos permite especificar los que se procesarán en primer lugar.

1. En la sección **Configuración de anulación de duplicación**, seleccione el número de **duplicados únicos que desea conservar**. El valor predeterminado de este campo es 1. El valor 0 le permite mantener todos los duplicados.

   Por ejemplo, si los registros A y B se consideran duplicados del registro Y, y un registro C se considera un duplicado del registro Z:

   * Si el valor del campo es 1: solo se guardan los registros Y y Z.
   * Si el valor del campo es 0: se guardan todos los registros.
   * Si el valor del campo es 2: se conservan los registros C y Z y se conservan dos registros de A, B e Y, al azar o en función del método de deduplicación seleccionado posteriormente.

1. Seleccione el **método de deduplicación** que se va a utilizar:

   * **Selección aleatoria**: Selecciona aleatoriamente el registro que se va a excluir de los duplicados.
   * **Uso de una expresión**: mantenga los registros en los que el valor de la expresión introducida sea el más pequeño o el más grande.
   * **Valores no vacíos**: Mantenga los registros para los que la expresión no está vacía.
   * **Siguiendo una lista de valores**: defina una prioridad de valor para uno o varios campos. Para definir los valores, haga clic en **Atributo** para seleccionar un campo o crear una expresión y, a continuación, agregue los valores a la tabla adecuada. Para definir un nuevo campo, haga clic en el **botón Agregar** ubicado sobre la lista de valores.

1. Seleccione la opción **Generate complement** si desea utilizar la población restante. El complemento está formado por todos los duplicados. A continuación, se agregará una transición adicional a la actividad.

## Ejemplo{#deduplication-example}

En el siguiente ejemplo, utilice una actividad de anulación de duplicación para excluir duplicados del destinatario antes de realizar una entrega. Los perfiles duplicados identificados se añaden a una audiencia dedicada que se puede reutilizar si es necesario. Elija la dirección de **correo electrónico** para identificar los duplicados. Mantenga 1 entrada y seleccione el método de deduplicación **Random**.

![](../assets/workflow-deduplication-example.png)
