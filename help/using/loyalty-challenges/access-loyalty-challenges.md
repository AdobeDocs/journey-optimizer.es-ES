---
solution: Journey Optimizer
product: journey optimizer
title: Acceder y administrar retos de fidelización
description: Obtenga información sobre cómo acceder, administrar y organizar desafíos y tareas de lealtad en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privada" type="Informative"
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---


# Acceder y administrar retos de fidelización {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* [Introducción a los retos de fidelización](get-started.md): información general, flujo de trabajo, requisitos previos
* **Desafíos de fidelidad de acceso** ◀︎ **Usted está aquí**: administración de inventario, desafíos y tareas
* [Crear desafíos](create-challenges.md) - Generar y configurar desafíos
* [Crear tareas](create-tasks.md) - Definir tareas de desafío

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Para solicitar acceso, póngase en contacto con su representante de Adobe. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

## Acceder a desafíos fieles

Para acceder a Desafíos de fidelización, vaya a Journey Optimizer y seleccione **[!UICONTROL Desafío de fidelización (Beta)]** en la sección **[!UICONTROL Administración de Recorridos]**.

La interfaz Retos de fidelización proporciona una ubicación centralizada para ver, administrar y organizar todos los desafíos y tareas. Puede acceder a dos inventarios principales:

* **Inventario de desafíos**: vea y administre todos los desafíos de lealtad, supervise su estado y realice acciones rápidas
* **Inventario de tareas**: Examine tareas reutilizables que se pueden utilizar en varios desafíos

## Inventario de retos {#challenges-tab}

La pestaña **[!UICONTROL Desafíos]** muestra todos los desafíos ordenados por fecha de última modificación, y en primer lugar aparecen los desafíos modificados más recientemente.

![](assets/challenges-inventory.png)

Información clave mostrada:

* **[!UICONTROL Desafío]**: Nombre del desafío
* **[!UICONTROL Estado]**: Estado actual del desafío (Borrador o Publicado)
* **[!UICONTROL Tareas]**: Número de tareas configuradas en el desafío
* **[!UICONTROL Recorrido]**: vínculo al recorrido generado automáticamente asociado con el desafío
* **[!UICONTROL Estado]**: Estado actual del recorrido asociado (borrador, activo, detenido, etc.)
* **[!UICONTROL Fecha de inicio/finalización (UTC)]**: Cuando el desafío se activa y caduca

En la pestaña Desafíos, puede realizar acciones en los desafíos:

* **Ver desafío**: seleccione el nombre del desafío para abrir su página de detalles
* **Duplicar un desafío**: selecciona el icono ![](assets/do-not-localize/Smock_More_18_N.svg) y elige **[!UICONTROL Duplicar]**. Se crea una copia con todas las tareas, el contenido y la mensajería intactos.
* **Eliminar un desafío**: seleccione el icono ![](assets/do-not-localize/Smock_More_18_N.svg) y elija **[!UICONTROL Eliminar]**
* **Editar un desafío**: seleccione el nombre del desafío para abrir su página de detalles y editarlo.

  Cuando abra un desafío publicado para editarlo, primero debe revertirlo al estado Borrador:

   * Se perderán todas las personalizaciones realizadas directamente en el recorrido generado automáticamente
   * El desafío vuelve al estado Borrador
   * Después de realizar los cambios, debe guardar y publicar el desafío de nuevo
   * Debe volver a publicar el recorrido asociado para que el desafío actualizado esté disponible para los clientes

  >[!IMPORTANT]
  >
  >La reversión de un desafío publicado a borrador no se puede deshacer. Tenga en cuenta el impacto en el recorrido activo antes de continuar.

## Inventario de tareas {#tasks-tab}

La pestaña **[!UICONTROL Tareas]** muestra todas las tareas reutilizables que se pueden usar en varios desafíos. Las tareas creadas aquí quedan disponibles para su selección al crear o editar cualquier desafío.

![](assets/tasks-inventory.png)

Información clave mostrada:

* **[!UICONTROL Nombre de tarea]**: El nombre que asignó a la tarea
* **[!UICONTROL Descripción]**: breve descripción de lo que requiere la tarea
* **[!UICONTROL Actividad de tarea]**: tipo de actividad (compra, gasto)
* **[!UICONTROL SKU]**: artículos aptos o excluidos
* **[!UICONTROL Utilizado en desafíos]**: Número de desafíos que están utilizando actualmente esta tarea

Desde la pestaña Tareas, puede realizar acciones en las tareas:

* **Ver/Editar tarea**: seleccione el nombre de la tarea para ver la configuración completa y editar la tarea
* **Duplicar una tarea**: seleccione el icono ![](assets/do-not-localize/Smock_More_18_N.svg) y elija **[!UICONTROL Duplicar]**
* **Eliminar una tarea**: seleccione el icono ![](assets/do-not-localize/Smock_More_18_N.svg) y elija **[!UICONTROL Eliminar]**
