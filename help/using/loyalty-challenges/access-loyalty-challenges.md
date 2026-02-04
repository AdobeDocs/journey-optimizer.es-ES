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
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---


# Acceder a retos de fidelización {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* [Introducción a los retos de fidelización](get-started.md): información general, flujo de trabajo, requisitos previos
* **Desafíos de fidelización de acceso** ◀︎ **Usted está aquí**: inventario y filtrado
* [Crear desafíos](create-challenges.md) - Generar y configurar desafíos
* [Administrar desafíos](manage-challenges.md): editar, supervisar y optimizar

>[!ENDSHADEBOX]

## Acceso al inventario Retos de fidelización {#access-inventory}

Para acceder a Desafíos de fidelización:

1. En Adobe Journey Optimizer, seleccione **[!UICONTROL Desafíos de fidelidad]** en el menú de navegación de la izquierda, en la sección **[!UICONTROL recorridos del cliente]**.

2. La página Retos de fidelización se muestra con dos pestañas:
   * **[!UICONTROL Desafíos]**: Ver y administrar todos los desafíos de lealtad
   * **[!UICONTROL Tareas]**: Ver y administrar todas las tareas que se pueden reutilizar en los desafíos

De manera predeterminada, la ficha **[!UICONTROL Desafíos]** está seleccionada y muestra todos los desafíos existentes en su organización.

## Pestaña Retos {#challenges-tab}

La pestaña Desafíos muestra todos los desafíos ordenados por fecha de última modificación, y en primer lugar aparecen los desafíos modificados más recientemente.

### Comprender el inventario de desafíos {#inventory-overview}

El inventario Retos muestra todos los desafíos con la siguiente información:

* **[!UICONTROL Nombre del desafío]**: El nombre que asignó al desafío
* **[!UICONTROL Estado]**: estado actual del desafío (consulte las descripciones de estado más abajo)
* **[!UICONTROL Tipo]**: Tipo de desafío (estándar, de racha o secuencial)
* **[!UICONTROL Fecha de inicio]**: cuando el desafío se active
* **[!UICONTROL Fecha de finalización]**: Cuando caduca el desafío
* **[!UICONTROL Creado por]**: usuario que creó el desafío
* **[!UICONTROL Última modificación]**: fecha y hora de la última modificación
* **[!UICONTROL Etiquetas]**: Cualquier etiqueta aplicada al desafío para la organización

### Estados de desafío {#challenge-statuses}

Los desafíos pueden tener los siguientes estados:

* **[!UICONTROL Borrador]**: el desafío se está creando o editando, pero aún no se ha publicado
* **[!UICONTROL Programado]**: el desafío se ha publicado y está programado para iniciarse en una fecha futura
* **[!UICONTROL Activo]**: el desafío está activo y disponible para la audiencia de destino
* **[!UICONTROL Completado]**: el desafío ha pasado su fecha de finalización o se han cumplido todos los objetivos
* **[!UICONTROL Detenido]**: el desafío se detuvo manualmente antes de completarse
* **[!UICONTROL Archivado]**: el desafío se archivó con fines organizativos

### Buscar y filtrar desafíos {#search-challenges}

Utilice la funcionalidad de búsqueda para encontrar rápidamente desafíos específicos por nombre o descripción.

También puede aplicar filtros para reducir la lista de desafíos en función de criterios específicos. Puede combinar varios filtros para restringir la búsqueda.

Puede filtrar los desafíos por su estado actual, por tipo de desafío, según las fechas de inicio o finalización o por etiquetas que haya aplicado a la organización.

### Acciones ante los desafíos {#inventory-actions}

Desde la pestaña Desafíos, puede realizar acciones rápidas en los desafíos:

* **Ver detalles del desafío**: seleccione un nombre de desafío para abrir su página de detalles
* **Editar un desafío**: selecciona el menú de más acciones (tres puntos) y elige **[!UICONTROL Editar]**
* **Duplicar un desafío**: selecciona el menú de más acciones y elige **[!UICONTROL Duplicar]**
* **Detener un desafío activo**: selecciona el menú de más acciones y elige **[!UICONTROL Detener]**
* **Archivar un desafío**: selecciona el menú de más acciones y elige **[!UICONTROL Archivar]**
* **Eliminar un desafío de borrador**: selecciona el menú de más acciones y elige **[!UICONTROL Eliminar]** (solo disponible para borradores)

### Crear un nuevo desafío {#create-from-inventory}

Para crear un nuevo desafío desde la pestaña Desafíos:

1. Seleccione **[!UICONTROL Crear desafío]** en la esquina superior derecha.

2. Comienza el flujo de trabajo de creación de desafíos.

Para obtener instrucciones detalladas, consulte [Crear desafíos](create-challenges.md).

## Pestaña Tareas {#tasks-tab}

La pestaña Tareas muestra todas las tareas reutilizables que se pueden utilizar en varios desafíos. Las tareas creadas aquí quedan disponibles para su selección al crear o editar cualquier desafío.

### Explicación del inventario de tareas {#tasks-inventory-overview}

El inventario Tareas muestra todas las tareas con la siguiente información:

* **[!UICONTROL Nombre de tarea]**: El nombre que asignó a la tarea
* **[!UICONTROL Tipo de tarea]**: tipo de acción (compra, cantidad de gasto, visita, participación, evento personalizado)
* **[!UICONTROL Descripción]**: breve descripción de lo que requiere la tarea
* **[!UICONTROL Creado por]**: usuario que creó la tarea
* **[!UICONTROL Última modificación]**: fecha y hora de la última modificación
* **[!UICONTROL Utilizado en desafíos]**: Número de desafíos que están utilizando actualmente esta tarea

### Cree tareas desde la pestaña Tareas {#create-tasks-from-tab}

Puede crear tareas de dos formas:

1. **Desde la ficha Tareas** (recomendado para tareas reutilizables):
   * Vaya a la ficha **[!UICONTROL Tareas]**
   * Seleccionar **[!UICONTROL Crear tarea]**
   * Configure las propiedades de la tarea (nombre, tipo, cantidad, filtros de producto, recompensas)
   * Guarde la tarea para que esté disponible para usarla en cualquier desafío

2. **Al crear un desafío** (para tareas específicas del desafío):
   * Durante la creación del desafío, seleccione **[!UICONTROL Agregar tarea]** en la sección Tareas
   * Elija **[!UICONTROL Crear nueva tarea]** o seleccione una de las tareas existentes
   * Las tareas creadas de esta forma también se guardan en el inventario Tareas y se pueden reutilizar

>[!TIP]
>
>Se recomienda crear tareas desde la pestaña Tareas cuando planee utilizar la misma tarea en varios desafíos. Esto garantiza la coherencia y facilita la actualización centralizada de las definiciones de tareas.

### Realizar acciones en tareas {#tasks-actions}

Desde la pestaña Tareas, puede realizar acciones en las tareas:

* **Ver detalles de la tarea**: seleccione un nombre de tarea para ver la configuración completa
* **Editar una tarea**: selecciona el menú de más acciones (tres puntos) y elige **[!UICONTROL Editar]**
* **Duplicar una tarea**: selecciona el menú de más acciones y elige **[!UICONTROL Duplicar]**
* **Eliminar una tarea**: selecciona el menú de más acciones y elige **[!UICONTROL Eliminar]** (solo si no se usa en ningún desafío activo)
* **Ver uso**: Ver qué desafíos están utilizando actualmente la tarea

## Próximos pasos {#next-steps}

Ahora que sabe cómo acceder y navegar por el inventario de Retos de fidelización:

* [Crear desafíos](create-challenges.md) - Aprenda a crear su primer desafío
* [Administrar desafíos](manage-challenges.md): aprenda a editar y supervisar desafíos
