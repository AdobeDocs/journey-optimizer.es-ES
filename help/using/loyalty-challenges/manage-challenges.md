---
solution: Journey Optimizer
product: journey optimizer
title: Administración de desafíos de lealtad
description: Aprenda a administrar, monitorizar y optimizar los desafíos de lealtad en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privada" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 1%

---


# Gestionar desafíos {#manage-challenges}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* [Introducción a los retos de fidelización](get-started.md): información general, flujo de trabajo, requisitos previos
* [Desafíos de fidelidad de acceso](access-loyalty-challenges.md): inventario y filtrado
* [Crear desafíos](create-challenges.md) - Generar y configurar desafíos
* [Crear tareas](create-tasks.md) - Definir tareas de desafío
* **Administrar desafíos** ◀︎ **Usted está aquí** - Editar, supervisar, optimizar

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Para solicitar acceso, póngase en contacto con su representante de Adobe. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

## Gestionar desafíos {#manage-challenges-section}

### Ciclo de desafío {#challenge-lifecycle}

<!-- VISUAL: Flowchart diagram showing challenge lifecycle with status transitions: Draft → Scheduled → Live → Completed/Stopped/Archived -->

Los desafíos pasan por diferentes estados durante su ciclo de vida:

* **Borrador**: el desafío se está creando o editando y aún no está disponible para los clientes
* **Programado**: el desafío se ha publicado y se activará automáticamente en la fecha de inicio especificada
* **Activo**: el desafío está activo y los clientes pueden participar
* **Completado**: el desafío ha finalizado; la fecha de finalización ha pasado o se han cumplido todos los objetivos
* **Detenido**: el desafío se detuvo manualmente antes de alcanzar su finalización natural
* **Archivado**: el desafío se archivó con fines organizativos y ya no está visible en el inventario principal

### Editar desafíos {#edit-challenges}

Puede editar los desafíos según su estado actual:

* **Desafíos del borrador**: Capacidad de edición completa: se pueden modificar todas las propiedades
* **Desafíos programados/activos**: edición limitada: puede actualizar el contenido, los mensajes y ampliar las fechas, pero no puede cambiar la estructura principal del desafío (definiciones de tipo, audiencia o tarea)

Para editar un desafío:

1. Vaya a la pestaña **[!UICONTROL Retos]** del inventario Retos de fidelización.

1. Busque el desafío que desee editar.

1. Seleccione el nombre del desafío para abrirlo en modo de edición.

1. Realice los cambios según el estado del desafío:
   * **Desafíos del borrador**: modifica cualquier propiedad, tarea, contenido o mensaje
   * **Desafíos programados/activos**: actualice las tarjetas de contenido, los mensajes o extienda las fechas de finalización según sea necesario

1. Guarde los cambios. Para los desafíos programados o activos, los cambios se aplican inmediatamente o según la programación de actualización.

>[!NOTE]
>
>Para los cambios que requieran modificaciones importantes (como cambiar el tipo de desafío, la audiencia o la estructura de la tarea), duplique el desafío y cree una nueva versión en lugar de editar la existente.

### Duplicar desafíos {#duplicate-challenges}

Duplicar desafíos a:

* Volver a ejecutar desafíos correctos para nuevos períodos de tiempo
* Crear variaciones para diferentes audiencias
* Actualizar requisitos o recompensas de tareas
* Reactivar desafíos detenidos o completados

Al duplicar un desafío, se crea una copia exacta con todas las tareas, el contenido y los mensajes intactos, lo que le permite crear rápidamente nuevas versiones sin tener que empezar desde cero.

Para duplicar un desafío:

1. Vaya a la pestaña **[!UICONTROL Retos]** del inventario Retos de fidelización.

1. Busque el desafío que desea duplicar.

1. Seleccione el menú de más acciones (tres puntos) que está junto a ese desafío.

1. Elija **[!UICONTROL Duplicado]**.

1. Se crea una copia del desafío con &quot;[Copy]&quot; anexado a su nombre.

1. Abra el desafío duplicado y modifique las propiedades necesarias:
   * Actualizar el nombre del desafío
   * Ajuste de las fechas de inicio y finalización
   * Cambie la audiencia de destino si es necesario
   * Modifique tareas, recompensas, contenido o mensajes según sea necesario

1. Revise y publique el desafío duplicado.

### Monitorización del rendimiento {#monitor-performance}

<!-- SCREENSHOT: Challenge Performance tab showing key metrics dashboard with participation, completion, reward, and engagement metrics -->

Rastree el rendimiento de los desafíos mediante métricas clave:

* **Métricas de participación**:
   * Inscripción: Número de clientes que se han unido al desafío
   * Participantes activos: Clientes que actualmente participan en el desafío
* **Métricas de finalización**:
   * Tasas de finalización: porcentaje de clientes inscritos que completaron el desafío
   * Average completion time: tiempo promedio empleado para completar todas las tareas
* **Métricas de recompensa**:
   * Total de recompensas distribuidas: Valor agregado de todas las recompensas otorgadas
   * Recompensas por tipo: desglose de las recompensas por categoría de recompensa
* **Métricas de participación**:
   * Impresiones de tarjeta de contenido: Número de veces que se han mostrado las tarjetas de contenido de desafío
   * Entrega de mensajes: recuento de mensajes enviados correctamente a través de todos los canales

Para acceder a los datos de rendimiento:

1. Vaya a la pestaña **[!UICONTROL Retos]** del inventario Retos de fidelización.

1. Seleccione el desafío que desee monitorizar.

1. Abra la pestaña **[!UICONTROL Rendimiento]** para ver las métricas y los análisis en tiempo real.

<!-- SCREENSHOT: Journey report showing challenge performance data with graphs and tables -->

También puede obtener acceso a los datos de rendimiento detallados en los [informes de recorridos generados automáticamente](../reports/journey-global-report-cja.md), que proporcionan información y tendencias históricas adicionales.

## Administrar tareas {#manage-tasks}

Las tareas son componentes reutilizables que se pueden utilizar en varios desafíos. La administración eficaz de tareas garantiza la coherencia en todo el programa de fidelidad y facilita la actualización centralizada de las definiciones de tareas. Las tareas creadas en un desafío pueden reutilizarse en otros, reduciendo la duplicación y manteniendo la estandarización.

### Editar tareas {#edit-tasks}

Puede editar las tareas existentes desde el inventario Tareas. Tenga en cuenta lo siguiente:

* **Tareas no utilizadas en los desafíos activos**: Pueden editarse libremente - todas las propiedades pueden modificarse sin impacto
* **Tareas utilizadas en los desafíos activos**: Tenga cuidado, ya que los cambios afectan a todos los desafíos que utilizan la tarea. Las modificaciones se aplican inmediatamente a todos los desafíos de referencia

Para editar una tarea:

1. Vaya a la pestaña **[!UICONTROL Tareas]** en el inventario Retos de fidelización.

1. Busque la tarea que desee editar.

1. Seleccione el nombre de la tarea para abrirla en modo de edición.

1. Modifique las propiedades de la tarea según sea necesario:
   * Actualizar nombre o descripción de tarea
   * Cambiar el tipo o los atributos de actividad
   * Ajuste de artículos y exclusiones aptos
   * Modificar requisitos de cantidad o cantidad

1. Guarde los cambios.

>[!WARNING]
>
>Al editar una tarea que se utiliza activamente en desafíos en directo, considere la posibilidad de crear un duplicado con una nueva versión en lugar de modificar la original. Esto evita cambios no deseados en los desafíos activos y le permite probar las modificaciones antes de aplicarlas.

### Eliminar tareas {#delete-tasks}

Las tareas solo se pueden eliminar si actualmente no se utilizan en ningún desafío. Antes de eliminar una tarea:

* Comprobar el recuento **[!UICONTROL Utilizado en los desafíos]** en el inventario de tareas
* Asegúrese de que no haya desafíos en borrador, programados o activos que hagan referencia a la tarea

Para eliminar una tarea:

1. Vaya a la pestaña **[!UICONTROL Tareas]** en el inventario Retos de fidelización.

1. Busque la tarea que desee eliminar.

1. Verifique que el recuento **[!UICONTROL Utilizado en los desafíos]** muestre 0. Si el recuento es mayor que 0, primero debe eliminar la tarea de todos los desafíos antes de la eliminación.

1. Seleccione el menú de más acciones (tres puntos) que está junto a la tarea.

1. Elija **[!UICONTROL Eliminar]**.

1. Confirme la eliminación en el cuadro de diálogo.

>[!NOTE]
>
>Si una tarea se utiliza en cualquier desafío (borrador, programado o activo), primero debe eliminarla de todos los desafíos antes de poder eliminarla. Considere la posibilidad de archivar o duplicar tareas en lugar de eliminarlas si es posible que las necesite en el futuro.
