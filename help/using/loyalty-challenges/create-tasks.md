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
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 0%

---


# Creación de tareas {#create-tasks}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* [Introducción a los retos de fidelización](get-started.md): información general, flujo de trabajo, requisitos previos
* [Desafíos de fidelidad de acceso](access-loyalty-challenges.md): inventario y filtrado
* [Crear desafíos](create-challenges.md) - Generar y configurar desafíos
* **Crear tareas** ◀︎ **Está aquí** - Definir tareas de desafío
* [Administrar desafíos](manage-challenges.md): editar, supervisar y optimizar

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Para solicitar acceso, póngase en contacto con su representante de Adobe. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

## Información general {#overview}

Las tareas definen las acciones o los hitos específicos que los clientes deben completar para obtener recompensas en un desafío de lealtad. Puede configurar tipos de tareas, cantidades, requisitos de productos y valores de recompensa para crear experiencias de lealtad atractivas y personalizadas.

Cada tarea representa una acción mensurable que contribuye a la finalización del desafío. Las tareas son componentes reutilizables que se pueden crear de forma independiente y, a continuación, añadir a uno o más desafíos, o crear directamente dentro de un desafío.

### Cómo funcionan las tareas en diferentes tipos de desafíos {#task-overview}

<!-- VISUAL: Diagram showing how task completion works differently for Standard, Streak, and Sequential challenges with examples -->

Según el tipo de desafío (estándar, en Streak o secuencial), los clientes completan las tareas de forma diferente:

* **Desafíos estándar**: Los clientes completan cualquier número especificado de tareas en cualquier orden
* **Retos de la racha**: Los clientes completan la misma tarea varias veces consecutivamente
* **Desafíos secuenciales**: Los clientes completan las tareas en un orden definido

## Crear una tarea {#create-task}

<!-- SCREENSHOT: Two screenshots side by side showing the two entry points: Tasks tab with "Create task" button, and challenge editor with "Add task" button -->

Puede crear tareas a partir de dos puntos de entrada. El proceso de configuración es el mismo independientemente de dónde comience.

+++Del inventario Tareas

1. Vaya a **[!UICONTROL Desafíos de fidelidad (Beta)]** en Journey Optimizer.

1. Seleccione la ficha **[!UICONTROL Tareas]**.

1. Seleccione **[!UICONTROL Crear tarea]**.

Las tareas creadas a partir del inventario se guardan y están disponibles para su reutilización en varios desafíos.

+++

+++Desde dentro de un desafío

1. Abra un desafío existente o cree uno nuevo.

1. Vaya a la sección **[!UICONTROL Tareas]**.

1. Seleccione **[!UICONTROL Agregar tarea]** y, a continuación, elija **[!UICONTROL Crear nueva tarea]**.

Las tareas creadas de esta manera se añaden automáticamente al desafío y también se guardan en el inventario Tareas para reutilizarlas en otros desafíos.

+++

### Definir propiedades de tarea {#define-task-properties}

<!-- SCREENSHOT: Task properties form showing Task name and Task description fields -->

Configure la información básica de la tarea:

* **Nombre de tarea**: escriba un nombre descriptivo para la tarea. Este nombre es visible para usted y para su equipo, pero es posible que no se muestre a los clientes según el diseño de la tarjeta de contenido.
* **Descripción de la tarea**: (Opcional) Agregue detalles sobre el propósito o los requisitos de la tarea.

### Elegir actividad del cliente {#choose-activity}

<!-- SCREENSHOT: Activity type selection showing Purchase and Spend options with radio buttons -->

Seleccione el tipo de actividad del cliente que los clientes deben realizar para completar esta tarea:

* **[!UICONTROL Comprar]**: los clientes deben comprar uno o más elementos para completar esta tarea
* **[!UICONTROL Gasto]**: los clientes deben gastar una cantidad especificada para completar esta tarea

Seleccione la actividad del cliente que mejor se ajuste a los objetivos del resultado. Cada tipo de actividad tiene atributos configurables específicos para definir y dar forma aún más a los requisitos de las tareas.

### Definir atributos {#define-attributes}

<!-- SCREENSHOT: Attributes form for Purchase activity showing Quantity field, Eligible items & exclusions field, and parameters icon for optional attributes -->

Configure los atributos de la tarea en función del tipo de actividad seleccionado:

+++Para la actividad de compra

Configure los siguientes atributos:

* **Cantidad**: escriba el número de artículos que deben comprarse para completar esta tarea
* **Elementos y exclusiones aptos**: defina los elementos o grupos de elementos que se contarán en la finalización de la tarea y los que no se contabilicen. Más información sobre [definición de artículos y exclusiones elegibles](#eligible-items-exclusions)

**Atributos opcionales** (configurar mediante el icono de parámetros):

* **Importe mínimo del valor de gasto**: establezca un requisito de importe mínimo de compra
* **Número máximo de transacciones**: Limite cuántas transacciones se pueden usar para completar la tarea

+++

+++Para la actividad de gasto

Configure los siguientes atributos:

* **Importe**: escriba el importe total de gasto necesario para completar la tarea
* **Número máximo de transacciones**: especifique cuántas transacciones pueden cumplir los requisitos de gasto. Puede desactivar este atributo del icono de parámetros si no desea limitar el número de transacciones
* **Elementos y exclusiones elegibles**: (Opcional) Defina elementos o grupos de elementos que se contarán para la finalización de la tarea y aquellos que no se contarán. Más información sobre [definición de artículos y exclusiones elegibles](#eligible-items-exclusions)

+++

Después de configurar todos los atributos, seleccione **[!UICONTROL Crear]** para guardar la tarea. La tarea se guarda en el inventario de Tareas y, si se crea desde un desafío, se añade automáticamente a dicho desafío.

## Definición de artículos y exclusiones aptos {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Tanto para las actividades de compra como de gasto, puede definir artículos y grupos aptos, así como excluir artículos y grupos. Esto le permite dirigirse a productos, categorías o ubicaciones específicos para alinearlos con los objetivos del desafío.

**Casos de uso:**

* Cree una tarea que recompense a los clientes por comprar artículos de café, pero excluya los productos de despacho
* Limitar una tarea de gasto a categorías de productos específicas
* Excluir tarjetas regalo o artículos promocionales del recuento para la finalización de la tarea

### Configurar artículos aptos {#configure-eligible-items}

Para definir artículos elegibles, usa la sección **[!UICONTROL Compras de tareas elegibles limitadas a lo siguiente]**:

* Introduce ID de artículo, categorías o ID de destino específicos, separados por comas
* Ejemplo: `SKU001, SKU002, CategoryA, StoreLocation123`
* **Sugerencia**: Escriba `*` para que todas las compras sean elegibles (comportamiento predeterminado si se deja vacío)

### Configuración de exclusiones {#configure-exclusions}

Para excluir elementos de la tarea, use la sección **[!UICONTROL Se excluyen los siguientes elementos de esta tarea]**:

* Introduzca ID de artículo, categorías o ID de destino específicos que no deban contarse para la finalización de la tarea
* Ejemplo: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`
* Exclusiones comunes: artículos de venta o liquidación, tarjetas regalo, artículos promocionales

>[!NOTE]
>
>Las exclusiones tienen prioridad sobre los artículos aptos. Si un artículo coincide con un artículo apto y con una exclusión, se excluye de la tarea.

## Próximos pasos {#next-steps}

Ahora que sabe cómo crear y configurar tareas:

* [Crear desafíos](create-challenges.md) - Aprenda a crear desafíos completos y a configurar recompensas
* [Administrar desafíos](manage-challenges.md): Aprenda a editar, monitorizar y optimizar desafíos
