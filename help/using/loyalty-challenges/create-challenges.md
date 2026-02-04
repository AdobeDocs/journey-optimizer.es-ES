---
solution: Journey Optimizer
product: journey optimizer
title: Crear desafíos de fidelidad
description: Aprenda a crear y configurar desafíos de lealtad en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privada" type="Informative"
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '1371'
ht-degree: 0%

---


# Crear desafíos {#create-challenges}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* [Introducción a los retos de fidelización](get-started.md): información general, flujo de trabajo, requisitos previos
* [Acceder y administrar desafíos de fidelidad](access-loyalty-challenges.md): administración de inventario, desafíos y tareas
* **Crear desafíos** ◀︎ **Usted está aquí** - Generar y configurar desafíos
* [Crear tareas](create-tasks.md) - Definir tareas de desafío

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Para solicitar acceso, póngase en contacto con su representante de Adobe. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

## Creación del desafío {#create-the-challenge}

1. Vaya a **[!UICONTROL Desafíos de fidelidad (Beta)]** en Journey Optimizer.

1. Seleccione la ficha **[!UICONTROL Desafíos]** y seleccione **[!UICONTROL Crear desafío]**.

   ![](assets/challenge-create.png)

1. Elija el tipo de desafío:

   * **[!UICONTROL Estándar]**: los clientes completan cualquier número especificado de tareas en cualquier orden\
     *Ejemplo: completar 3 de 5 tareas disponibles*

   * **[!UICONTROL Streak]**: Los clientes completan la misma tarea varias veces de forma consecutiva\
     *Ejemplo: Realizar una compra en 7 días consecutivos*

   * **[!UICONTROL Secuencial]**: Los clientes completan tareas en un orden definido\
     *Ejemplo: compra → revisión → uso compartido (debe completarse en esta secuencia)*

## Configuración de la estructura de desafíos {#structure}

En la ficha **[!UICONTROL Estructura]**, defina la organización del desafío: las propiedades, la programación, las tareas por completar y las recompensas por entregar.

### Defina las propiedades del desafío y utilice metadatos personalizados {#properties}

1. En el panel **[!UICONTROL Propiedades del desafío]**, defina la configuración global del desafío:

   * **[!UICONTROL Nombre]**: escriba un nombre descriptivo para el desafío. Este nombre aparece en el inventario de desafíos.
   * **[!UICONTROL Descripción]**: escriba una descripción que explique el propósito y los objetivos del desafío.

   ![](assets/challenge-create-properties.png)

1. Utilice la sección **[!UICONTROL Metadatos personalizados]** para agregar metadatos personalizados mediante pares clave/valor. Estos metadatos se pueden utilizar para el seguimiento o la integración con sistemas externos.

### Programar el desafío {#schedule}

Configure cuándo se ejecuta el desafío seleccionando el icono ![](assets/do-not-localize/schedule-icon.svg) **[!UICONTROL Abrir programación]**:

![](assets/challenge-create-properties.png)

* **[!UICONTROL Fecha y hora de inicio]**: establezca cuándo el desafío estará disponible para los clientes.
* **[!UICONTROL Fecha y hora de finalización]**: establezca cuándo caduca el desafío y ya no acepta nuevas finalizaciones.
   * **[!UICONTROL Zona horaria]**: El desafío utiliza la zona horaria local del destinatario de forma predeterminada.
* **[!UICONTROL Las tareas deben completarse]**: elija cuándo los clientes pueden completar las tareas:

   * **[!UICONTROL En cualquier momento durante el desafío]**: los clientes pueden completar las tareas en cualquier momento entre las fechas de inicio y finalización del desafío.
   * **[!UICONTROL Durante horas específicas del día]**: Restrinja la finalización de tareas a horas diarias específicas al establecer **[!UICONTROL Hora de inicio]** y **[!UICONTROL Hora de finalización]**.

La programación de desafíos ya está configurada. A continuación, añada las tareas que los clientes necesitan completar.

### Agregar tareas {#add-tasks}

Las tareas definen las acciones específicas que los clientes deben completar para obtener recompensas. Puede configurar tipos de tareas (compras, gastos), cantidades, filtros de productos y otros atributos.

Según el tipo de desafío, los clientes completan las tareas de forma diferente:

* **Desafíos estándar**: complete cualquier número especificado de tareas en cualquier orden\
  *Ejemplo: completar 3 de 5 tareas: realizar una compra, escribir una crítica, recomendar a un amigo, compartir en medios sociales o actualizar perfil*

* **Rastrear desafíos**: complete la misma tarea varias veces de manera consecutiva\
  *Ejemplo: haz una compra por 7 días consecutivos para ganar recompensas de bonificación*

* **Desafíos secuenciales**: complete las tareas en un orden definido\
  *Ejemplo: primero realiza una compra, luego escribe una revisión y luego comparte en los medios sociales; las tareas deben completarse en esta secuencia exacta*

Para añadir tareas al desafío, siga estos pasos:

1. En la sección **[!UICONTROL Tareas]**, seleccione **[!UICONTROL Agregar tarea]**.

   ![](assets/challenge-create-add-task.png)

1. Se abre **[!UICONTROL Inventario de tareas]**. Seleccione una o más tareas de la lista y seleccione **[!UICONTROL Agregar]**. Para crear una tarea nueva, seleccione **[!UICONTROL Nuevo]**. [Aprenda a crear y configurar tareas](create-tasks.md).

1. En la sección **[!UICONTROL Requisito para finalizar la tarea]**, especifique cuándo se considera completado el desafío:

   * **[!UICONTROL El cliente elige 1 tarea para completar]**: Los clientes pueden seleccionar y completar cualquier tarea para obtener recompensas.
   * **[!UICONTROL El cliente completa una cantidad específica de tareas]**: los clientes deben completar una cantidad definida de tareas.

1. De forma predeterminada, los desafíos permiten a los clientes completar tareas en varias transacciones. Para requerir que todas las tareas se completen en una sola transacción, seleccione el icono ![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL Configuración]** y active la siguiente opción.

   ![](assets/challenge-create-single-transaction.png)

Después de agregar tareas al desafío, configure las recompensas que los clientes ganarán por completarlas.

### Configuración de recompensas {#rewards}

Las recompensas son los puntos de lealtad o los beneficios que los clientes reciben por completar los desafíos. Configure cuándo y cómo se entregan las recompensas.

1. En el menú desplegable **[!UICONTROL Entrega de recompensas]**, elija cuándo entregar las recompensas:

   * **[!UICONTROL Entregar recompensas cuando se complete el desafío]**: Premios cuando los clientes completen el desafío completo\
     *Ejemplo: otorga 100 puntos después de completar las 5 tareas*

   * **[!UICONTROL Entregar recompensas en hitos de finalización de tareas a medida que se avanza el desafío]**: Las recompensas se incrementan a medida que los clientes completan tareas individuales (solo están disponibles para desafíos que requieren más de una tarea)\
     *Ejemplo: otorga 10 puntos después de la tarea 1, 20 puntos después de la tarea 2 y 50 puntos después de la tarea 3*

1. Seleccione a su proveedor de recompensas. Esta es su solución de fidelidad que administra los puntos y recompensas del cliente.

1. Configure los importes de recompensa en función del método de entrega seleccionado:

   +++Entregar recompensas cuando se complete el desafío

   Especifique el importe total de recompensa que se proporcionará cuando los clientes completen el desafío completo.

   ![](assets/challenge-create-reward-total.png)

   **Ejemplo**: A los clientes se les otorgan 100 puntos al completar el desafío.

   +++

   +++Entregar recompensas en los hitos de finalización de tarea

   Especifique los importes de recompensa para los hitos de finalización de tarea. Esta opción le permite crear recompensas progresivas que aumentan la motivación del cliente a medida que este avanza en el desafío.

   Para cualquier tarea en la que desee entregar un premio, active la opción de recompensa y especifique cuántos puntos se otorgarán cuando los clientes completen esa tarea específica. Puede optar por recompensar sólo determinadas finalizaciones de tareas; por ejemplo, si tiene 10 tareas, puede recompensar sólo las tareas 1, 5 y 10.

   ![](assets/challenge-create-reward-milestones.png)

   **Ejemplo**: A los clientes se les otorgan 10 puntos al completar la primera tarea y luego 50 puntos adicionales después de completar la segunda tarea, lo que hace un total de 60 puntos cuando se completa el desafío.

   >[!TIP]
   >
   >Considere la posibilidad de aumentar los valores de recompensa por tareas posteriores para mantener la participación del cliente durante todo el desafío.

   +++

Después de configurar la estructura de desafíos con tareas y recompensas, diseñe las tarjetas de contenido para mostrar el desafío a los clientes.

## Configuración de tarjetas de contenido {#configure-content-cards}

Las tarjetas de contenido representan visualmente su desafío en los dispositivos de los clientes, y muestran información de desafío, progreso y recompensas. [Más información sobre las tarjetas de contenido](../content-card/create-content-card.md).

Para configurar las tarjetas de contenido para el desafío:

1. Vaya a la pestaña **[!UICONTROL Contenido]** e introduzca un **[!UICONTROL Nombre]** para la tarjeta de contenido.

1. Seleccione la **[!UICONTROL configuración de canal]**. Las configuraciones de canal contienen todos los parámetros técnicos para enviar mensajes, como parámetros de encabezado, subdominio, aplicaciones móviles, etc. [Más información acerca de las configuraciones de canal](../configuration/channel-surfaces.md).

1. Seleccione **[!UICONTROL Editar contenido]** para diseñar su tarjeta de contenido. [Aprenda a diseñar y personalizar tarjetas de contenido](../content-card/design-content-card.md).

   ![](assets/challenge-create-content.png)

Después de configurar la tarjeta de contenido, configure la mensajería para atraer a los clientes a lo largo del ciclo de vida del desafío.

### Configuración de mensajería {#configure-messaging}

Configure mensajes multicanal para atraer a los clientes en etapas clave del ciclo de vida del desafío. La mensajería es opcional, pero se recomienda para maximizar la participación del cliente.

1. Vaya a la pestaña **[!UICONTROL Mensajería]** y configure los mensajes para cada fase del ciclo vital:

   * **Iniciar** mensaje: Notifique a los clientes cuando comience el desafío
   * Mensaje de **En curso**: Mantén a los clientes comprometidos con los recordatorios y las actualizaciones de progreso
   * **Finalización** mensaje: Celebre el éxito y confirme la asignación del premio

1. Para cada fase, seleccione **[!UICONTROL Agregar mensaje [stage]]** (donde [stage] representa Lanzamiento, En curso o Finalización) para crear un mensaje para esa fase.

1. Elija el canal que desee: **[!UICONTROL En la aplicación]**, **[!UICONTROL Correo electrónico]** o **[!UICONTROL Notificación push]** y seleccione la configuración de canal asociada.

1. Seleccione el icono ![](assets/do-not-localize/Smock_More_18_N.svg) y elija **[!UICONTROL Editar]** para diseñar el contenido del mensaje.

   ![](assets/challenge-create-messaging.png)

Aprenda a crear mensajes para canales específicos:

* [Mensajes en la aplicación](../in-app/get-started-in-app.md)
* [Mensajes de correo electrónico](../email/get-started-email.md)
* [Notificaciones push](../push/get-started-push.md)

Una vez completada la configuración de mensajería, defina qué clientes pueden participar en el desafío.

## Selección de la audiencia del desafío {#audience}

Defina qué clientes pueden participar en su desafío de fidelidad.

1. Vaya a la pestaña **[!UICONTROL Audiencia]** y seleccione el botón **[!UICONTROL Seleccionar audiencia]**.

   ![](assets/challenge-create-audience.png)

1. Seleccione la audiencia de destino en la lista de audiencias de Adobe Experience Platform disponibles. [Aprenda a trabajar con audiencias](../audience/about-audiences.md).

1. Seleccione **[!UICONTROL Agregar audiencia]**.

El desafío está ahora completamente configurado con su estructura, contenido, mensajería y audiencia de destino. El paso final es generar y publicar el recorrido.

## Generación y publicación del recorrido {#review-and-publish}

Genere el recorrido que orquestará la entrega de desafíos y las interacciones con los clientes. Para ello, seleccione **[!UICONTROL Generar Recorrido]**.

![](assets/challenge-create-generate-journey.png)

Journey Optimizer crea automáticamente un [recorrido](../building-journeys/journey-gs.md) en estado de Borrador. El recorrido generado automáticamente aparece en su inventario de recorridos con el formato de nombre &quot;Desafío: [Nombre del desafío]&quot;.

![](assets/challenge-create-journey.png)

Revise la configuración del recorrido si es necesario y publique el recorrido para que el desafío esté disponible para los clientes. [Más información sobre cómo publicar un recorrido](../building-journeys/publish-journey.md).

El recorrido se iniciará automáticamente en la fecha de inicio del desafío especificada y enviará el contenido y los mensajes según la configuración.

>[!NOTE]
>
>El recorrido generado automáticamente se puede personalizar para agregar lógica o mensajes adicionales. Sin embargo, los cambios realizados directamente en el recorrido no se sincronizan con la configuración de desafío. Si edita el desafío más adelante, las personalizaciones del recorrido se perderán cuando se regenere el recorrido.
