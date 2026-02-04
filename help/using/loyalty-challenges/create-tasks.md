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
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---


# Creación de tareas {#create-tasks}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* [Introducción a los retos de fidelización](get-started.md): información general, flujo de trabajo, requisitos previos
* [Acceder y administrar desafíos de fidelidad](access-loyalty-challenges.md): administración de inventario, desafíos y tareas
* [Crear desafíos](create-challenges.md) - Generar y configurar desafíos
* **Crear tareas** ◀︎ **Está aquí** - Definir tareas de desafío

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Para solicitar acceso, póngase en contacto con su representante de Adobe. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

Las tareas definen las acciones o los hitos específicos que los clientes deben completar para obtener recompensas en un desafío de lealtad. Puede configurar tipos de tareas, cantidades y requisitos de productos para crear experiencias de lealtad atractivas y personalizadas.

Cada tarea representa una acción mensurable que contribuye a la finalización del desafío. Las tareas son componentes reutilizables que se pueden crear de forma independiente y, a continuación, añadir a uno o más desafíos, o crear directamente dentro de un desafío.

## Crear una tarea {#create-task}

Puede crear tareas a partir de dos puntos de entrada. El proceso de configuración es el mismo independientemente de dónde comience.

>[!BEGINTABS]

>[!TAB Del inventario de tareas]

Seleccione la ficha **[!UICONTROL Tareas]** y seleccione **[!UICONTROL Crear tarea]**.

![](assets/task-create-inventory.png)

Las tareas creadas a partir del inventario se guardan y están disponibles para su reutilización en varios desafíos.

>[!TAB Desde un desafío]

Abra un desafío existente o cree uno nuevo. Seleccione **[!UICONTROL Agregar tarea]** y haga clic en el botón **[!UICONTROL Nuevo]**.

![](assets/task-create-challenge.png)

Las tareas creadas de esta manera se añaden automáticamente al desafío y también se guardan en el inventario Tareas para reutilizarlas en otros desafíos.

>[!ENDTABS]

## Elegir actividad del cliente {#choose-activity}

Seleccione el tipo de actividad que deben realizar los clientes para completar esta tarea:

* **[!UICONTROL Comprar]**: los clientes deben comprar uno o más elementos para completar esta tarea
* **[!UICONTROL Gasto]**: los clientes deben gastar una cantidad especificada para completar esta tarea

Para seleccionar un tipo de actividad, haga clic en el icono `+` y seleccione la actividad del cliente que mejor se ajuste a los objetivos del resultado. Cada tipo de actividad tiene atributos configurables específicos para definir y dar forma aún más a los requisitos de las tareas.

![](assets/task-create-activitiy.png)

## Definir atributos {#define-attributes}

Configure los atributos de la tarea en función del tipo de actividad seleccionado:

>[!BEGINTABS]

>[!TAB Actividad de compra]

![](assets/task-create-purchase.png)

Configure los siguientes atributos:

* **[!UICONTROL Cantidad]**: escriba el número de artículos que deben comprarse para completar esta tarea
* **[!UICONTROL Elementos y exclusiones aptos]**: defina los elementos o grupos de elementos que se contarán en la finalización de la tarea y los que no se contabilicen. Más información sobre [definición de artículos y exclusiones elegibles](#eligible-items-exclusions)

**Atributos opcionales** (activados mediante el icono de parámetros):

* **[!UICONTROL Importe mínimo del valor de gasto]**: establezca un requisito de importe mínimo de compra
* **[!UICONTROL Número máximo de transacciones]**: Limite cuántas transacciones se pueden usar para completar la tarea

>[!TAB Actividad de gasto]

![](assets/task-create-spend.png)

Configure los siguientes atributos:

* **[!UICONTROL Importe]**: escriba el importe total de gasto necesario para completar la tarea.
* **[!UICONTROL Número máximo de transacciones]**: especifique cuántas transacciones pueden cumplir los requisitos de gasto. Puede desactivar este atributo del icono de parámetros si no desea limitar el número de transacciones.
* **[!UICONTROL Elementos y exclusiones elegibles]**: (Opcional) Defina elementos o grupos de elementos que se contarán para la finalización de la tarea y aquellos que no se contarán. Más información sobre [definición de artículos y exclusiones elegibles](#eligible-items-exclusions)

>[!ENDTABS]

## Definición de artículos y exclusiones aptos {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Para las actividades **Compra** y **Gasto**, puede usar el atributo **[!UICONTROL Elementos y exclusiones elegibles]** para definir qué artículos y grupos son elegibles y cuáles están excluidos. Esto le permite dirigirse a productos, categorías o ubicaciones específicos para alinearlos con los objetivos del desafío.

Los casos de uso incluyen: limitar una tarea de gasto a categorías de productos específicas o excluir del recuento las tarjetas regalo o los artículos promocionales para la finalización de la tarea.

![](assets/tasks-create-eligible.png)

* Para definir artículos elegibles, usa la sección **[!UICONTROL Compras de tareas elegibles limitadas a la siguiente]** sección. Introduce ID de artículo, categorías o ID de destino específicos, separados por comas.

  Ejemplo: `SKU001, SKU002, CategoryA`

  Escriba `*` para que todas las compras sean elegibles (comportamiento predeterminado si se deja vacío).

* Para excluir elementos de la tarea, use la sección **[!UICONTROL Se excluyen los siguientes elementos de esta tarea]**. Introduzca ID de artículo, categorías o ID de destino específicos que no deban contarse para la finalización de la tarea.

  Ejemplo: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`

  >[!NOTE]
  >
  >Las exclusiones tienen prioridad sobre los artículos aptos. Si un artículo coincide con un artículo apto y con una exclusión, se excluye de la tarea.

## Definir propiedades de tarea {#define-task-properties}

En el panel **[!UICONTROL Propiedades]** de la tarea, configure la información básica de la tarea:

* **[!UICONTROL Nombre de tarea]**: escriba un nombre descriptivo para la tarea. Este nombre es visible para usted y para su equipo, pero es posible que no se muestre a los clientes según el diseño de la tarjeta de contenido.
* **[!UICONTROL Descripción de la tarea]**: La descripción se genera automáticamente según el tipo de actividad y los atributos que configure para la tarea. Puede deshabilitar la generación automática e introducir una descripción personalizada si es necesario.

![](assets/tasks-create-properties.png)

Después de configurar todos los atributos y propiedades, seleccione **[!UICONTROL Crear]** para guardar la tarea. La tarea se guarda en el inventario de Tareas y, si se crea desde un desafío, se añade automáticamente a dicho desafío.
