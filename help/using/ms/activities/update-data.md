---
solution: Journey Optimizer
product: journey optimizer
title: Utilice la actividad Update data en sus campañas orquestadas
description: Aprenda a utilizar la actividad de actualización de datos
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 68e7c929-5f07-4d5a-9831-690e071947f8
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 24%

---

# Actualización de datos {#update-data}

La actividad **Actualizar datos** es una actividad **Administración de datos**. Permite realizar una actualización masiva de los campos de la base de datos. Varias opciones permiten personalizar la actualización de datos.

<!--
The **Operation type** field lets you choose the process to be carried out on the data in the database. Select the first option to add data or update (it if it has already been added). You can also only add data, only update data, or delete data. Select the **Update and merge collections** to select a primary record to link duplicates to, and delete those duplicates safely

Specify how to identify the records in the database: if data relate to an existing targeting dimension, select the **Using the targeting dimension** option and select the targeting dimension and fields to update. Otherwise, specify one or more custom links to identify the data in the database, or direct use of reconciliation keys.

Select the fields to update and reconciliation settings. You can use the **Auto-mapping** option to automatically identify the fields to be updated.

The **Advanced options** section let you specify additional settings to manage data and duplicates.

Toggle the **Generate an outbound transition** option to add an outbound transition that will be activated at the end of the execution of the **Update data** activity. The update generally marks the end of a targeting workflow and therefore the option is not activated by default.

Toggle the **Generate an outbound transition for rejects** option to add an outbound transition containing records that have not been correctly processed after the update (for example if there is a duplicate). The update generally marks the end of a targeting workflow and therefore the option is not activated by default.
-->

## Configure la actividad Update data{#update-data-configuration}

Para configurar la actividad **Actualizar datos**, comience agregando la actividad a la campaña orquestada y defina una etiqueta.

![](../assets/workflow-update-data.png)

### Tipo de operación

El campo **Operation type** permite elegir el proceso que se lleva a cabo en la información de la base de datos:

* **Insertar o actualizar**: inserte datos o actualícelos si los registros ya existen en la base de datos.
* **Insertar**: insertar solo datos. Los registros que ya existen no se actualizan. Si se definen los criterios de reconciliación, solo se añaden los registros que no se han cuadrado.
* **Actualizar**: actualice los datos de los registros que ya existen solamente en la base de datos.
* **Delete**: eliminar datos.

El campo **Batch size** permite seleccionar el número de elementos de transición entrantes que se deben actualizar. Por ejemplo, si establece 500, se actualizarán los 500 primeros registros analizados.

### Identificación de registro

Esta sección le permite especificar cómo identificar los registros de la base de datos:

* Si las entradas de datos están relacionadas con una dimensión de segmentación existente, seleccione la opción **Using the targeting dimension** y selecciónela en el campo **Targeting dimension to update**.
* También puede seleccionar **mediante vínculos personalizados** y especificar uno o más vínculos que permitan la identificación de los datos en la base de datos
* Si el tipo de operación seleccionado requiere una actualización, debe usar la opción **Usar reglas de reconciliación**.

### Campos para actualizar

En la sección **Campos para actualizar**, agregue los campos en los que se aplicará la actualización y, si es necesario, agregue las condiciones para que se realice esta actualización. Para ello, utilice el campo **Taken into account if**. Las condiciones se aplican una tras otra en orden de lista. Utilice las flechas de la derecha para cambiar el orden de las actualizaciones. Puede utilizar el mismo campo de destino varias veces.

Puede vincular automáticamente los campos usando el botón **Asignación automática**. La vinculación automática detecta los campos con el mismo nombre.

Durante un tipo de operación **Insert or update**, puede seleccionar individualmente la operación que desea aplicar a cada campo. Para ello, seleccione el valor que desee en el campo **Operation type**.

### Opciones avanzadas

**Opciones avanzadas** le permite especificar opciones adicionales para trabajar con la actualización de datos y para administrar duplicados.

<!--
* **Disable automatic key management**
* **Disable audit**
* **Empty the destination value if the source value is empty**
* **Update all columns with matching names**
* **Ignore records which concern the same target**: only the first in the list of expressions will be considered
-->

Las dos últimas opciones permiten realizar acciones específicas:

* **Generar una transición saliente**: crea una transición saliente que se activará al final de la ejecución. La actualización normalmente indica el final de una campaña orquestada de objetivos y, por lo tanto, la opción no se activa de forma predeterminada.

* **Generar una transición saliente para los rechazos**: crea una transición saliente que contiene registros que no se han procesado correctamente después de la actualización (por ejemplo, si hay un duplicado). Por lo general, la actualización marca el final de una campaña orquestada de objetivos y, por lo tanto, la opción no está activada de forma predeterminada.
