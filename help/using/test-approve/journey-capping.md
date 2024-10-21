---
title: límite y arbitraje de recorridos
description: Obtenga información sobre cómo crear reglas de límite para los recorridos y cómo arbitrar la entrada de recorridos
role: User
level: Beginner
badge: label="Disponibilidad limitada"
hide: true
hidefromtoc: true
source-git-commit: ea947514012c342fd28155e6610b2eb13547b465
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 2%

---


# límite y arbitraje de recorridos {#journey-capping}

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción a la administración y priorización de conflictos](gs-conflict-prioritization.md)
* [Detección de posibles conflictos en recorridos y campañas](conflicts.md)
* [Asignar puntuaciones de prioridad a recorridos y campañas](priority-scores.md)
* **[límite y arbitraje de Recorridos](journey-capping.md)**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Actualmente, las herramientas de priorización y administración de conflictos están disponibles como disponibilidad limitada solo para usuarios seleccionados.

La restricción de recorrido le ayuda a limitar el número de recorridos en los que se puede inscribir un perfil, lo que evita la sobrecarga de comunicaciones. En Journey Optimizer, puede establecer dos tipos de reglas de límite:

* **Límite de entrada** limita el número de entradas de recorrido durante un período determinado para un perfil.
* **Límite de concurrencia** limita la cantidad de recorridos en los que se puede inscribir un perfil simultáneamente.

Ambos tipos de límite de recorrido aprovechan las puntuaciones de prioridad para arbitrar entradas.

## Creación de una regla de límite de recorrido {#create-rule}

Para crear una regla de límite de recorrido, siga estos pasos:

1. Vaya al menú **[!UICONTROL Reglas de negocio (Beta)]** para acceder al inventario de conjuntos de reglas.

1. Seleccione el conjunto de reglas en el que desea agregar la regla de límite o cree un nuevo conjunto de reglas:

   * Para utilizar un conjunto de reglas existente, selecciónelo en la lista. Las reglas de restricción de recorrido solo se pueden agregar a conjuntos de reglas con el dominio &quot;recorrido&quot;. Puede comprobar esta información en las listas de conjuntos de reglas, en la columna **[!UICONTROL Dominio]**.

     ![](assets/journey-capping-list.png)

   * Para crear la regla de límite dentro de un nuevo conjunto de reglas, haga clic en **[!UICONTROL Crear conjunto de reglas]**, especifique un nombre único para el conjunto de reglas y seleccione &quot;Recorrido&quot; en la lista desplegable **[!UICONTROL Dominio del conjunto de reglas]**; a continuación, haga clic en **[!UICONTROL Guardar]**.

     ![](assets/journey-capping-rule-set.png)

1. En la pantalla del conjunto de reglas, haga clic en el botón **[!UICONTROL Agregar regla]** y, a continuación, configure la regla para adaptarla a sus necesidades:

   ![](assets/journey-capping-concurrency.png)

   * Proporcione un nombre único para la regla.

   * En la lista desplegable **[!UICONTROL Tipo de regla]**, especifique el tipo de límite para la regla.

      * **[!UICONTROL Límite de entrada de Recorrido]**: Limita el número de entradas en el recorrido durante un período determinado para un perfil.
      * **[!UICONTROL Límite de concurrencia de Recorrido]**: Limita la cantidad de recorridos en los que se puede inscribir un perfil simultáneamente.

   * Expanda las secciones siguientes para aprender a configurar cada tipo de límite:

     +++Configuración de una regla de límite de entrada de recorrido

      1. En el campo **[!UICONTROL Límite]**, establezca el número máximo de recorridos que puede ingresar un perfil.
      1. En el campo **[!UICONTROL Duración]**, defina el período de tiempo que debe tenerse en cuenta. Tenga en cuenta que la duración se basa en la zona horaria UTC. Por ejemplo, el Límite diario se restablecerá a medianoche UTC.

     En este ejemplo, queremos restringir la entrada de perfiles en más de &quot;5&quot; recorridos en un mes.

     ![](assets/journey-capping-entry-example.png)

     >[!NOTE]
     >
     >El sistema tendrá en cuenta la prioridad de los próximos recorridos programados que tengan aplicada esta misma regla.
     >
     >En este ejemplo, si el especialista en marketing ya ha introducido 4 recorridos y hay otro recorrido programado para este mes con una prioridad más alta, se impedirá que los clientes entren en el recorrido de prioridad más baja.

+++

     +++Configuración de una regla de límite de concurrencia de recorrido

      1. En el campo **[!UICONTROL Límite]**, establezca el número máximo de recorridos en los que se puede inscribir un perfil simultáneamente.

      1. Utilice el campo **[!UICONTROL Establecimiento de prioridades para mirar hacia delante]** para arbitrar las entradas de recorridos en función de las puntuaciones de prioridad durante un período elegido (por ejemplo, 1 día, 7 días, 30 días). Esto ayuda a priorizar la entrada en recorridos de mayor valor si un perfil es apto para varios recorridos.

     En este ejemplo, queremos restringir la entrada de perfiles en la recorrido si ya están inscritos en otro recorrido que contenga el mismo conjunto de reglas. Si otro recorrido en los próximos 7 días tiene una puntuación de prioridad más alta, el perfil no entrará en este recorrido.

     ![](assets/journey-capping-concurrency-example.png){width="50%" zommable="yes"}

+++

1. Cuando la regla de límite esté lista para aplicarse a los recorridos, actívela haciendo clic en el botón de puntos suspensivos situado junto a su nombre.

   ![](assets/journey-capping-activate-rule.png)

1. Active todo el conjunto de reglas haciendo clic en el botón de puntos suspensivos situado junto al botón Agregar regla en la esquina superior derecha de la pantalla.

   ![](assets/journey-capping-activate-rule-set.png){width="50%" zommable="yes"}

## Aplicación de reglas de límite a los recorridos {#apply-capping}

Para aplicar una regla de límite a un recorrido, acceda al recorrido y abra sus propiedades. En el menú desplegable **[!UICONTROL Reglas de límite]**, seleccione el conjunto de reglas correspondiente.

Una vez activado el recorrido, las reglas de límite definidas en el conjunto de reglas surtirán efecto.

![](assets/journey-capping-apply.png)

>[!IMPORTANT]
>
>Si un recorrido se activa inmediatamente, el sistema puede tardar hasta 15 minutos en empezar a suprimir clientes. Puede programar su recorrido para que comience al menos 15 minutos en el futuro para evitar esta posibilidad.
