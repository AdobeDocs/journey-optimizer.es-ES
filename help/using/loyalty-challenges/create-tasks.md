---
solution: Journey Optimizer
product: journey optimizer
title: Creación de tareas para desafíos de fidelidad
description: Aprenda a crear y configurar tareas para los desafíos de lealtad en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privada" type="Informative"
mini-toc-levels: 1
source-git-commit: 342df0950622de1c4c246bf624d05843671e199f
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---


# Creación de tareas {#create-tasks}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* [Introducción a los retos de fidelización](get-started.md)
* [Acceder y administrar desafíos y tareas](access-loyalty-challenges.md)
* [Crear desafíos](create-challenges.md)
* **Crear tareas** ◀︎ **Usted está aquí**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica se encuentra actualmente en **versión beta privada**. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

Las tareas definen las acciones o los hitos específicos que los clientes deben completar para obtener recompensas en un desafío de lealtad. Puede configurar tipos de tareas, cantidades y requisitos de productos para crear experiencias de lealtad atractivas y personalizadas.

Cada tarea representa una acción mensurable que contribuye a la finalización del desafío. Las tareas son componentes reutilizables que se pueden crear de forma independiente y, a continuación, añadir a uno o más desafíos, o crear directamente dentro de un desafío.

## Crear una tarea {#create-task}

Puede crear tareas a partir de dos puntos de entrada. El proceso de configuración es el mismo independientemente de dónde comience.

>[!BEGINTABS]

>[!TAB Del inventario de tareas]

Seleccione la ficha **[!UICONTROL Tareas]** y seleccione **[!UICONTROL Crear tarea]**. Las tareas creadas a partir del inventario se guardan y están disponibles para su reutilización en varios desafíos.

![](assets/task-create-inventory.png)

>[!TAB Desde un desafío]

Abra un desafío existente o cree uno nuevo. Seleccione **[!UICONTROL Agregar tarea]** y haga clic en el botón **[!UICONTROL Nuevo]**. Las tareas creadas de esta manera se añaden automáticamente al desafío y también se guardan en el inventario Tareas para reutilizarlas en otros desafíos.

![](assets/task-create-challenge.png)

>[!ENDTABS]

## Elegir actividad del cliente {#choose-activity}

Seleccione el tipo de actividad que deben realizar los clientes para completar esta tarea:

* **[!UICONTROL Comprar]**: los clientes deben comprar uno o más elementos para completar esta tarea
* **[!UICONTROL Gasto]**: los clientes deben gastar una cantidad especificada para completar esta tarea

Para seleccionar una actividad, haga clic en el icono **+** y seleccione la actividad del cliente que mejor se ajuste a los objetivos del resultado. Cada tipo de actividad tiene atributos configurables específicos para definir y dar forma aún más a los requisitos de las tareas.
![](assets/task-create-activity.png)

## Definir los atributos de la tarea {#define-attributes}

Configure los atributos de la tarea en función del tipo de actividad seleccionado. Examine las pestañas siguientes para ver los atributos disponibles para cada tipo de actividad:

>[!BEGINTABS]

>[!TAB Actividad de compra]

Atributos disponibles para actividades **Purchase**:

* **[!UICONTROL Cantidad]**: escriba el número de artículos que deben comprarse para completar esta tarea.
* **[!UICONTROL Elementos y exclusiones aptos]**: defina los elementos o grupos de elementos que se contarán en la finalización de la tarea y los que no se contabilicen. [Más información sobre artículos aptos y exclusiones](#eligible-items-exclusions)
* **[!UICONTROL Importe mínimo del valor de gasto]**: establezca un requisito de importe mínimo de compra.
* **[!UICONTROL Número máximo de transacciones]**: Limite cuántas transacciones se pueden usar para completar la tarea.

![](assets/task-create-purchase.png)

>[!TAB Actividad de gasto]

Atributos disponibles para actividades **Spend**:

* **[!UICONTROL Importe]**: escriba el importe total de gasto necesario para completar la tarea.
* **[!UICONTROL Elementos y exclusiones aptos]**: defina los elementos o grupos de elementos que se contarán en la finalización de la tarea y los que no se contabilicen. [Más información sobre artículos aptos y exclusiones](#eligible-items-exclusions)
* **[!UICONTROL Número máximo de transacciones]**: especifique cuántas transacciones pueden cumplir los requisitos de gasto. Puede activar este atributo desde el icono de parámetros.

![](assets/task-create-spend.png)

>[!ENDTABS]

## Definición de artículos y exclusiones aptos {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Para las actividades **Compra** y **Gasto**, puede usar el atributo **[!UICONTROL Elementos y exclusiones elegibles]** para definir qué artículos y grupos son elegibles y cuáles están excluidos. Esto le permite dirigirse a productos, categorías o ubicaciones específicos para alinearlos con los objetivos del desafío.

Por ejemplo, puede limitar una tarea de gasto a categorías de productos específicas o excluir del recuento las tarjetas regalo o los artículos promocionales para la finalización de la tarea.

![](assets/tasks-create-eligible.png)

* Para definir artículos elegibles, escribe ID de artículo, categorías o ID de destino específicos, separados por comas en **[!UICONTROL Las compras de tareas elegibles están limitadas al siguiente campo]**. Si deja este campo vacío, todas las compras son elegibles de forma predeterminada. También puede ingresar `*` para que todas las compras sean elegibles de manera explícita.

  Ejemplo: `SKU001, SKU002, CategoryA`

* Para excluir elementos de la tarea, escriba id. de elemento, categorías o id. de destino específicos en el campo **[!UICONTROL Se excluyen los siguientes elementos de esta tarea]**.

  Ejemplo: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`

## Definir propiedades de tarea {#define-task-properties}

En el panel **[!UICONTROL Propiedades]** de la tarea, configure la información básica de la tarea:

* **[!UICONTROL Nombre de tarea]**: escriba un nombre descriptivo para la tarea.
* **[!UICONTROL Descripción de tarea]**: la descripción se genera automáticamente en función de la actividad y los atributos configurados. Para introducir una descripción personalizada, desactive la opción de generación automática e introduzca la descripción en el campo de texto.

![](assets/tasks-create-properties.png)

Después de configurar todos los atributos y propiedades, seleccione **[!UICONTROL Crear]** para guardar la tarea. La tarea se guarda en el inventario de Tareas y, si se crea desde un desafío, se añade automáticamente a dicho desafío.
