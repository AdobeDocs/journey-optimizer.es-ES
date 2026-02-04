---
solution: Journey Optimizer
product: journey optimizer
title: Acceder a retos de fidelización
description: Obtenga información sobre cómo acceder, buscar y filtrar desafíos de lealtad en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privada" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---


# Acceder a retos de fidelización {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* [Introducción a los retos de fidelización](get-started.md): información general, flujo de trabajo, requisitos previos
* **Desafíos de fidelización de acceso** ◀︎ **Usted está aquí**: inventario y filtrado
* [Crear desafíos](create-challenges.md) - Generar y configurar desafíos
* [Crear tareas](create-tasks.md) - Definir tareas de desafío
* [Administrar desafíos](manage-challenges.md): editar, supervisar y optimizar

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Para solicitar acceso, póngase en contacto con su representante de Adobe. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

## Acceso al inventario Retos de fidelización {#access-inventory}

<!-- SCREENSHOT: Journey Optimizer main menu showing "Loyalty challenges" under "Customer journeys" section -->

Para acceder a Desafíos de fidelidad, vaya a Journey Optimizer y seleccione **[!UICONTROL Desafíos de fidelidad]** en la sección **[!UICONTROL recorridos del cliente]**.

<!-- SCREENSHOT: Loyalty Challenges landing page showing the two tabs: Challenges and Tasks -->

La página Retos de fidelización se muestra con dos pestañas:

* **[!UICONTROL Desafíos]**: Ver y administrar todos los desafíos de lealtad

* **[!UICONTROL Tareas]**: Ver y administrar todas las tareas que se pueden reutilizar en los desafíos

## Inventario de retos {#challenges-tab}

<!-- SCREENSHOT: Challenges tab showing the inventory table with columns: Challenge name, Status, Type, Start date, End date, Created by, Last modified, Tags -->

La pestaña Desafíos muestra todos los desafíos ordenados por fecha de última modificación, y en primer lugar aparecen los desafíos modificados más recientemente. Se muestra la siguiente información:

* **[!UICONTROL Nombre del desafío]**: El nombre que asignó al desafío
* **[!UICONTROL Estado]**: estado actual del desafío (consulte las descripciones de estado más abajo)
* **[!UICONTROL Tipo]**: Tipo de desafío (estándar, de racha o secuencial)
* **[!UICONTROL Fecha de inicio]**: cuando el desafío se active
* **[!UICONTROL Fecha de finalización]**: Cuando caduca el desafío
* **[!UICONTROL Creado por]**: usuario que creó el desafío
* **[!UICONTROL Última modificación]**: fecha y hora de la última modificación
* **[!UICONTROL Etiquetas]**: Cualquier etiqueta aplicada al desafío para la organización

### Estados de desafío {#challenge-statuses}

<!-- VISUAL: Status badges showing different challenge statuses with color coding: Draft (gray), Scheduled (blue), Live (green), Completed (gray), Stopped (red), Archived (gray) -->

Los desafíos se muestran con diferentes estados que indican su estado actual en el ciclo vital:

* **Borrador**: el desafío se está creando o editando
* **Programado**: el desafío se ha publicado y se activará en la fecha de inicio
* **Activo**: el desafío está activo y los clientes pueden participar
* **Completado**: la fecha de finalización del desafío ha pasado o se han cumplido los objetivos
* **Detenido**: el desafío se detuvo manualmente antes de completarse
* **Archivado**: el desafío se archivó con fines organizativos

Para obtener información detallada sobre las transiciones de estado y el ciclo vital de desafío, consulte [Ciclo vital de desafío](manage-challenges.md#challenge-lifecycle).

### Buscar y filtrar desafíos {#search-challenges}

<!-- SCREENSHOT: Search bar and filter panel showing available filters (status, type, dates, tags) with an example of active filters applied -->

Puede localizar rápidamente desafíos mediante la búsqueda y los filtros:

**Buscar:**

* Utilice la barra de búsqueda para buscar desafíos introduciendo palabras clave a partir del nombre o la descripción del desafío. La búsqueda actualiza los resultados en tiempo real a medida que escribe.

**Filtros:**

* Aplique uno o más filtros para reducir los resultados:
   * **Estado**: filtrar por estado de desafío (Borrador, Programado, Activo, Completado, Detenido, Archivado)
   * **Tipo**: filtrar por tipo de desafío (estándar, de flujo, secuencial)
   * **Fechas**: filtrar por fecha de inicio o intervalos de fechas de finalización
   * **Etiquetas**: filtrar por etiquetas aplicadas a los desafíos

Puede combinar varios filtros simultáneamente. Por ejemplo, filtre por desafíos de Live Standard etiquetados con &quot;Verano de 2024&quot; para encontrar rápidamente campañas de temporada activas.

Para borrar filtros, seleccione **[!UICONTROL Borrar todos]** o quite filtros individuales.

### Acciones ante los desafíos {#inventory-actions}

<!-- SCREENSHOT: More actions menu (three dots) expanded showing options: Edit, Duplicate, Stop, Archive, Delete -->

Desde la pestaña Desafíos, puede realizar acciones rápidas en los desafíos:

* **Ver detalles del desafío**: seleccione el nombre del desafío para abrir su página de detalles
* **Editar un desafío**: selecciona el menú **[!UICONTROL Más acciones]** (tres puntos) y elige **[!UICONTROL Editar]**
* **Duplicar un desafío**: selecciona el menú **[!UICONTROL Más acciones]** y elige **[!UICONTROL Duplicar]**
* **Detener un desafío activo**: selecciona el menú **[!UICONTROL Más acciones]** y elige **[!UICONTROL Detener]**
* **Archivar un desafío**: selecciona el menú **[!UICONTROL Más acciones]** y elige **[!UICONTROL Archivar]**
* **Eliminar un desafío de borrador**: seleccione el menú **[!UICONTROL Más acciones]** y elija **[!UICONTROL Eliminar]** (solo disponible para borradores)

Para obtener información detallada sobre cómo administrar los desafíos después de la creación, incluidas las limitaciones de edición, las estrategias de duplicación, la monitorización del rendimiento y la resolución de problemas, consulte [Administrar desafíos](manage-challenges.md).

## Inventario de tareas {#tasks-tab}

<!-- SCREENSHOT: Tasks tab showing the inventory table with columns: Task name, Task type, Description, Created by, Last modified, Used in challenges -->

La pestaña Tareas muestra todas las tareas reutilizables que se pueden utilizar en varios desafíos. Las tareas creadas aquí quedan disponibles para su selección al crear o editar cualquier desafío.

El inventario Tareas muestra la siguiente información:

* **[!UICONTROL Nombre de tarea]**: El nombre que asignó a la tarea
* **[!UICONTROL Tipo de tarea]**: tipo de acción (compra, cantidad de gasto, visita, participación, evento personalizado)
* **[!UICONTROL Descripción]**: breve descripción de lo que requiere la tarea
* **[!UICONTROL Creado por]**: usuario que creó la tarea
* **[!UICONTROL Última modificación]**: fecha y hora de la última modificación
* **[!UICONTROL Utilizado en desafíos]**: Número de desafíos que están utilizando actualmente esta tarea

### Realizar acciones en tareas {#tasks-actions}

Desde la pestaña Tareas, puede realizar acciones en las tareas:

* **Ver detalles de la tarea**: seleccione el nombre de la tarea para ver la configuración completa
* **Editar una tarea**: selecciona el menú **[!UICONTROL Más acciones]** (tres puntos) y elige **[!UICONTROL Editar]**
* **Duplicar una tarea**: selecciona el menú **[!UICONTROL Más acciones]** y elige **[!UICONTROL Duplicar]**
* **Eliminar una tarea**: selecciona el menú **[!UICONTROL Más acciones]** y elige **[!UICONTROL Eliminar]** (solo si no se usa en ningún desafío activo)
* **Ver uso**: Ver qué desafíos están utilizando actualmente la tarea

## Próximos pasos {#next-steps}

Ahora que sabe cómo acceder y navegar por el inventario de Retos de fidelización:

* [Crear desafíos](create-challenges.md): aprenda a crear su primer desafío y a configurar tareas
* [Crear tareas](create-tasks.md) - Aprenda a definir tareas reutilizables para los desafíos
* [Administrar desafíos](manage-challenges.md): Aprenda a editar, monitorizar y optimizar desafíos
