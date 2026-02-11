---
solution: Journey Optimizer
product: journey optimizer
title: Acceder y administrar desafíos y tareas
description: Obtenga información sobre cómo acceder, administrar y organizar desafíos y tareas de lealtad en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privada" type="Informative"
mini-toc-levels: 1
exl-id: 8907c18e-4623-4743-a76b-333f34e13baf
source-git-commit: c5d7cbde6e0a9b4b835abac19d33b973f9f364e4
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Acceder y administrar desafíos y tareas {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* [Introducción a los retos de fidelización](get-started.md)
* **Acceder y administrar desafíos y tareas** ◀︎ **Usted está aquí**
* [Crear desafíos](create-challenges.md)
* [Creación de tareas](create-tasks.md)
* [Referencia de API de desafíos de fidelidad](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges/){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica se encuentra actualmente en **versión beta privada**. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

## Acceder y administrar desafíos y tareas

Para acceder a Desafíos de fidelización, vaya a Journey Optimizer y seleccione **[!UICONTROL Desafío de fidelización (Beta)]** en la sección **[!UICONTROL Administración de Recorridos]**. La interfaz Retos de fidelización proporciona una ubicación centralizada para ver, administrar y organizar todos los desafíos y tareas.

La interfaz permite acceder a dos inventarios principales:

* **Desafíos**: vea y administre todos los desafíos de fidelidad, supervise su estado y realice acciones rápidas como ver, editar, duplicar o eliminar desafíos
* **Tareas**: Examine tareas reutilizables que pueden utilizarse en varios desafíos y administre definiciones de tareas de forma independiente

## Inventario de retos {#challenges-tab}

La pestaña **[!UICONTROL Desafíos]** muestra todos los desafíos ordenados por fecha de última modificación, y en primer lugar aparecen los desafíos modificados más recientemente.

![](assets/challenges-inventory.png)

Información clave mostrada:

* **[!UICONTROL Estado]**: Estado actual del desafío (Borrador o Publicado)
* **[!UICONTROL Tareas]**: Número de tareas configuradas en el desafío
* **[!UICONTROL Recorrido]**: vínculo al recorrido generado automáticamente asociado con el desafío
* **[!UICONTROL Estado]**: Estado actual del recorrido generado automáticamente que presenta el desafío.
* **[!UICONTROL Fecha de inicio/finalización (UTC)]**: Cuando el desafío se activa y caduca

En la pestaña Desafíos, puede realizar acciones en los desafíos:

* **Ver desafío**: seleccione el nombre del desafío para abrir su página de detalles
* **Duplicar un desafío**: selecciona el icono ![](assets/do-not-localize/Smock_More_18_N.svg) y elige **[!UICONTROL Duplicar]**. Se crea una copia con todas las tareas, el contenido y la mensajería intactos.
* **Eliminar un desafío**: seleccione el icono ![](assets/do-not-localize/Smock_More_18_N.svg) y elija **[!UICONTROL Eliminar]**.

  >[!IMPORTANT]
  >
  >Puede eliminar un desafío incluso cuando esté publicado. Tenga en cuenta el impacto antes de eliminar.

* **Editar un desafío**: seleccione el nombre del desafío para abrir su página de detalles y realizar los cambios deseados.

  Cuando abra un desafío publicado para editarlo, primero debe revertirlo al estado Borrador. Se perderán todas las personalizaciones realizadas directamente en el recorrido generado automáticamente. Después de realizar los cambios, guarde y publique el desafío de nuevo y, a continuación, publique el recorrido asociado. [Aprenda a iniciar un desafío](create-challenges.md#launch)

  >[!IMPORTANT]
  >
  >La reversión de un desafío publicado a borrador no se puede deshacer. Tenga en cuenta el impacto en el recorrido activo antes de continuar.

## Inventario de tareas {#tasks-tab}

La pestaña **[!UICONTROL Tareas]** muestra todas las tareas reutilizables que se pueden usar en varios desafíos. Las tareas creadas aquí quedan disponibles para su selección al crear o editar cualquier desafío.

![](assets/tasks-inventory.png)

Información clave mostrada:

* **[!UICONTROL Descripción]**: breve descripción de lo que requiere la tarea
* **[!UICONTROL Actividad de tarea]**: tipo de actividad (compra, gasto)
* **[!UICONTROL SKU]**: artículos aptos o excluidos
* **[!UICONTROL Utilizado en desafíos]**: Número de desafíos que están utilizando actualmente esta tarea

Desde la pestaña Tareas, puede realizar acciones en las tareas:

* **Ver/editar una tarea**: seleccione el nombre de la tarea para ver la configuración completa y editar la tarea
* **Duplicar una tarea**: seleccione el icono ![](assets/do-not-localize/Smock_More_18_N.svg) y elija **[!UICONTROL Duplicar]**
* **Eliminar una tarea**: seleccione el icono ![](assets/do-not-localize/Smock_More_18_N.svg) y elija **[!UICONTROL Eliminar]**.

  >[!IMPORTANT]
  >
  >Puede eliminar una tarea incluso cuando se utiliza en uno o más desafíos. Tenga en cuenta el impacto en los desafíos que hacen referencia a la tarea antes de eliminarla.
