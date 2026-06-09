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
badge: label="Beta privada" type="Informative"
mini-toc-levels: 1
exl-id: c1e49173-69cc-4729-9f9a-afea2ccff3fa
feature_v2: []
subfeature_v2: []
source-git-commit: 024bf7a15ca8ef80dfd948ad226958ed71f22413
workflow-type: tm+mt
source-wordcount: 1178
ht-degree: 6%

---

# Creación de tareas {#create-tasks}

>[!BEGINSHADEBOX]

**Tabla de contenido**

[Introducción a los retos de fidelización](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Crear y administrar desafíos**

* [Acceder y administrar desafíos y tareas](access-loyalty-challenges.md)
* [Crear desafíos](create-challenges.md)
* **Crear tareas** ◀︎ **Usted está aquí**
* [Monitorización del rendimiento del desafío de fidelidad](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configurar e integrar**

* [Configuración de desafíos de lealtad](loyalty-admin.md)
* [Datos y conjuntos de datos de fidelización](loyalty-data-and-datasets.md)
* [Referencia de API de retos de fidelización](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica se encuentra actualmente en **versión beta privada**. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](../rn/releases.md).

Las tareas definen las acciones o los hitos específicos que los clientes deben completar para obtener recompensas en un desafío de lealtad. Puede configurar tareas de compra y gasto o **[!UICONTROL eventos personalizados]** tareas que hagan un seguimiento de los eventos de experiencia de Adobe Experience Platform que su organización ya capture.

Cada tarea representa una acción mensurable que contribuye a la finalización del desafío. Las tareas son componentes reutilizables que se pueden crear de forma independiente y, a continuación, añadir a uno o más desafíos, o crear directamente dentro de un desafío.

## Crear una tarea {#create-task}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_task_create"
>title="Crear una tarea"
>abstract="Seleccione una actividad de cliente (compra, gasto o evento personalizado) y, a continuación, configure los atributos específicos de la actividad. En el panel Propiedades, establezca el nombre y la descripción de la tarea."

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
* **[!UICONTROL Evento personalizado]**: los clientes deben realizar una actividad representada por un evento de experiencia de Adobe Experience Platform. Por ejemplo, un registro de llegada de hotel, una acción de aplicación móvil o un envío de revisión. El evento subyacente ya debe capturarse en Experience Platform y asignarse mediante una definición de evento en el menú **[!UICONTROL Administrador de fidelidad]**. [Aprenda a configurar definiciones de eventos](loyalty-admin.md#event-definitions)

Para seleccionar una actividad, haga clic en el icono **+** y seleccione la actividad del cliente que mejor se ajuste a los objetivos del resultado. Cada tipo de actividad tiene atributos configurables específicos para definir y dar forma aún más a los requisitos de las tareas.
![](assets/task-create-activity.png)

## Definir los atributos de la tarea {#define-attributes}

Configure los atributos de la tarea en función del tipo de actividad seleccionado. Examine las pestañas siguientes para ver los atributos disponibles para cada tipo de actividad:

>[!BEGINTABS]

>[!TAB Actividad de compra]

Atributos disponibles para actividades **Purchase**:

* **[!UICONTROL Cantidad]**: escriba el número de artículos que deben comprarse para completar esta tarea.
* **[!UICONTROL Elementos y exclusiones elegibles]**: define elementos o grupos de elementos que se cuentan para la finalización de la tarea y aquellos que no se cuentan, o elige **[!UICONTROL Traer tus propios datos]** para determinar la elegibilidad a partir de tus datos externos. [Más información](#eligible-items-exclusions)
* **[!UICONTROL Importe mínimo del valor de gasto]**: establezca un requisito de importe mínimo de compra.
* **[!UICONTROL Número máximo de transacciones]**: Limite cuántas transacciones se pueden usar para completar la tarea.

![](assets/task-create-purchase.png)

>[!TAB Actividad de gasto]

Atributos disponibles para actividades **Spend**:

* **[!UICONTROL Importe]**: escriba el importe total de gasto necesario para completar la tarea.
* **[!UICONTROL Elementos y exclusiones aptos]**: defina los elementos o grupos de elementos que se contarán en la finalización de la tarea y los que no se contabilicen. [Más información sobre artículos y exclusiones elegibles](#eligible-items-exclusions)
* **[!UICONTROL Número máximo de transacciones]**: especifique cuántas transacciones pueden cumplir los requisitos de gasto. Puede activar este atributo desde el icono de parámetros.

![](assets/task-create-spend.png)

>[!TAB Actividad de evento personalizado]

Atributos disponibles para **[!UICONTROL actividades de evento personalizado]**:

* **[!UICONTROL Valores de evento personalizados]**: escriba los valores para el evento personalizado que deben completar los clientes. Utilice una coma para separar cada valor. Estos valores deben coincidir con las definiciones de eventos configuradas en el menú **[!UICONTROL Administrador de fidelización]**. [Aprenda a configurar definiciones de eventos](loyalty-admin.md#event-definitions)

![](assets/task-create-custom.png)

>[!ENDTABS]

## Definir los elementos aptos y las exclusiones {#eligible-items-exclusions}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_task_eligible_items_exclusion"
>title="Elementos aptos y exclusiones"
>abstract="Para las actividades **Purchase** y **Spend**, use el atributo **[!UICONTROL Eligible items &amp; exclusions]** para seleccionar qué artículos y grupos se contabilizan para la finalización de la tarea y cuáles se excluyen. Busque artículos o grupos del inventario de productos configurado por los administradores y, a continuación, inclúyalos o exclúyalos según sea necesario."

<!-- SCREENSHOT: Eligible items & exclusions picker showing the item and group table with Include and Exclude actions -->

Para las actividades **Comprar** y **Gastar**, puede usar la sección **[!UICONTROL Elementos y exclusiones elegibles]** para definir qué artículos y grupos son elegibles y cuáles están excluidos. Esto le permite dirigirse a productos, categorías o ubicaciones específicos para alinearlos con los objetivos del desafío.

Los elementos y grupos disponibles en el selector los definen los usuarios administradores en el menú **[!UICONTROL Administrador de fidelidad]**. Los administradores cargan el inventario de productos utilizado para los artículos aptos y configuran exclusiones de toda la organización que se aplican automáticamente cuando los especialistas en marketing crean tareas. [Aprenda a configurar el inventario de productos](loyalty-admin.md#product-inventory) y [exclusiones](loyalty-admin.md#exclusions)

Las tareas de **[!UICONTROL Custom Event]** no utilizan elementos y exclusiones que cumplan los requisitos; la finalización depende de los **[!UICONTROL valores de Custom Event]** que configure.

Por ejemplo, puede limitar una tarea a categorías de productos específicas o excluir del recuento las tarjetas regalo o los elementos promocionales para la finalización de la tarea.

![](assets/task-create-eligible.png)

### Definir artículos aptos para la tarea

Para definir artículos elegibles, selecciona **[!UICONTROL Agregar]** de la sección **[!UICONTROL Elementos y exclusiones elegibles]**.

En el selector, seleccione los elementos o grupos que se deben contar para la finalización de la tarea y, a continuación, seleccione **[!UICONTROL Incluir]**. Los artículos y grupos incluidos se añaden a la lista de artículos aptos.

![](assets/task-create-eligible-add.png)

Si no se selecciona ningún artículo o grupo apto, las compras no se limitan a un juego de inventario específico, a menos que se configuren exclusiones.

### Excluir elementos de la tarea

Para excluir artículos de la tarea, selecciona **[!UICONTROL Agregar]** de la sección **[!UICONTROL Elementos y exclusiones aptos]**.

Seleccione los elementos o grupos que no deben contarse para la finalización de la tarea y, a continuación, seleccione **[!UICONTROL Excluir]**.

![](assets/task-create-exclusion-add.png)

Los elementos de la lista de exclusiones globales se añaden automáticamente como exclusiones. Las exclusiones tienen prioridad sobre las inclusiones: los elementos enumerados como excluidos no se cuentan, aunque también formen parte de un grupo incluido.

### Incluya sus propios datos sobre elegibilidad y exclusiones {#byod-personalization}

>[!AVAILABILITY]
>
>La opción **[!UICONTROL Traer tus propios datos]** está disponible actualmente para un conjunto restringido de organizaciones y estará disponible de forma más amplia en una versión futura.

Además de seleccionar elementos y grupos en Journey Optimizer, también puedes mejorar la elegibilidad de tus datos externos de Desafíos de fidelidad durante la ejecución mediante la opción **[!UICONTROL Traer tus propios datos]**.

Cuando se selecciona **[!UICONTROL Traer tus propios datos]**, la elegibilidad por participante se resuelve en tiempo de ejecución a partir de los datos sincronizados con tu entorno de retos de fidelidad en lugar de una lista de ID de artículos.

Para usar esta opción, selecciona el icono de personalización en **[!UICONTROL Elementos y exclusiones elegibles]**, y luego elige **[!UICONTROL Traer tus propios datos]**.

![](assets/tasks-create-eligible-bring.png)

>[!IMPORTANT]
>
>Al asignar esta tarea a un desafío, seleccione **[!UICONTROL Estándar]** como tipo de desafío. No seleccione **[!UICONTROL Traer sus propios datos]** al nivel de desafío, ya que esa opción está reservada para desafíos totalmente impulsados por datos donde toda la estructura, incluidas las tareas y las recompensas, se proporciona externamente.

## Definir propiedades de tarea {#define-task-properties}

En el panel **[!UICONTROL Propiedades]** de la tarea, configure la información básica de la tarea:

* **[!UICONTROL Nombre de tarea]**: escriba un nombre descriptivo para la tarea.
* **[!UICONTROL Descripción de tarea]**: la descripción se genera automáticamente en función de la actividad y los atributos configurados. Para introducir una descripción personalizada, desactive la opción de generación automática e introduzca la descripción en el campo de texto.

![](assets/tasks-create-properties.png)

Después de configurar todos los atributos y propiedades, seleccione **[!UICONTROL Crear]** para guardar la tarea. La tarea se guarda en el inventario de Tareas y, si se crea desde un desafío, se añade automáticamente a dicho desafío.
