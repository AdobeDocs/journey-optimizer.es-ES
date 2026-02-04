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
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---


# Administrar desafíos y tareas {#manage-challenges}

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

### Estados de desafío {#challenge-lifecycle}

Los desafíos pasan por diferentes estados durante su ciclo de vida:

* **Borrador**: el desafío se está creando o editando y aún no está disponible para los clientes.
* **Publicado**: el desafío está activo y se ha creado el recorrido asociado.

### Editar desafíos {#edit-challenges}

Puede editar los desafíos abriéndolos en el inventario Desafíos. El comportamiento de edición difiere según el estado del desafío:

**Desafíos de borrador**: Tiene capacidad de edición completa. Todas las propiedades, tareas, contenido y mensajes se pueden modificar sin restricciones.

**Desafíos publicados**: Cuando abra un desafío publicado para editarlo, primero deberá revertirlo al estado Borrador.

* Se perderán todas las personalizaciones realizadas directamente en el recorrido generado automáticamente.
* El desafío vuelve al estado Borrador.
* Después de realizar los cambios, debe guardar y publicar el desafío de nuevo.
* Debe volver a publicar el recorrido asociado para que el desafío actualizado esté disponible para los clientes.

>[!IMPORTANT]
>
>La reversión de un desafío publicado a borrador no se puede deshacer. Tenga en cuenta el impacto en el recorrido activo antes de continuar.

### Duplicar desafíos {#duplicate-challenges}

Al duplicar un desafío, se crea una copia exacta con todas las tareas, el contenido y los mensajes intactos, lo que le permite crear rápidamente nuevas versiones sin tener que empezar desde cero.

Para duplicar un desafío:

1. Vaya a la pestaña **[!UICONTROL Desafíos]** y busque el desafío que quiera duplicar.

1. Seleccione el icono ![](assets/do-not-localize/Smock_More_18_N.svg) que está junto a ese desafío y elija **[!UICONTROL Duplicado]**.

1. Se crea una copia del desafío. Abra el desafío duplicado y modifique las propiedades necesarias.

1. Guarde el desafío duplicado y genere el recorrido asociado.

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

Las tareas son componentes reutilizables que se pueden utilizar en varios desafíos. La administración eficaz de tareas garantiza la coherencia en todo el programa de fidelidad y facilita la actualización centralizada de las definiciones de tareas. Las tareas creadas en un desafío pueden reutilizarse en otros, lo que reduce la duplicación y mantiene la estandarización.

### Editar tareas {#edit-tasks}

Puede editar las tareas existentes desde el inventario Tareas. Tenga en cuenta lo siguiente:

* **Tareas no utilizadas en los desafíos activos**: pueden editarse libremente. Todas las propiedades se pueden modificar sin impacto.
* **Tareas utilizadas en los desafíos activos**: Tenga cuidado, ya que los cambios afectan a todos los desafíos que utilizan la tarea. Las modificaciones se aplican inmediatamente a todos los desafíos de referencia.

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

* Compruebe el recuento **[!UICONTROL Utilizado en los desafíos]** en el inventario de tareas.
* Asegúrese de que no haya desafíos en borrador, programados o activos que hagan referencia a la tarea.

Para eliminar una tarea:

1. Vaya a la pestaña **[!UICONTROL Tareas]** en el inventario Retos de fidelización.

1. Busque la tarea que desee eliminar.

1. Verifique que el recuento **[!UICONTROL Utilizado en los desafíos]** muestre 0. Si el recuento es mayor que 0, primero debe eliminar la tarea de todos los desafíos antes de la eliminación.

1. Seleccione el icono ![](assets/do-not-localize/Smock_More_18_N.svg) junto a la tarea.

1. Elija **[!UICONTROL Eliminar]**.

1. Confirme la eliminación en el cuadro de diálogo.

>[!NOTE]
>
>Si una tarea se utiliza en cualquier desafío (borrador, programado o activo), primero debe eliminarla de todos los desafíos antes de poder eliminarla. Considere la posibilidad de archivar o duplicar tareas en lugar de eliminarlas si es posible que las necesite en el futuro.
