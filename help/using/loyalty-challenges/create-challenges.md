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
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 0%

---


# Crear desafíos {#create-challenges}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* [Introducción a los retos de fidelización](get-started.md): información general, flujo de trabajo, requisitos previos
* [Desafíos de fidelidad de acceso](access-loyalty-challenges.md): inventario y filtrado
* **Crear desafíos** ◀︎ **Usted está aquí** - Generar y configurar desafíos
* [Crear tareas](create-tasks.md) - Definir tareas de desafío
* [Administrar desafíos](manage-challenges.md): editar, supervisar y optimizar

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Para solicitar acceso, póngase en contacto con su representante de Adobe. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

## Funcionamiento {#how-it-works}

La creación y el lanzamiento de un desafío de fidelidad siguen este flujo de trabajo:

1. **[Crear el desafío](#create-the-challenge)**: elija el tipo de desafío (estándar, de racha o secuencial) que mejor se ajuste a los objetivos de su programa de fidelidad.

1. **[Configurar la estructura del desafío](#structure)**: defina las propiedades del desafío, el horario, las tareas que los clientes deben completar y las recompensas que obtendrán.

1. **[Configurar tarjetas de contenido](#configure-content-cards)**: diseñe tarjetas de contenido para representar visualmente su desafío en los dispositivos de los clientes y mostrar información de desafío, progreso y recompensas.

1. **[Configurar mensajes](#configure-messaging)** (opcional): configure mensajes multicanal (en la aplicación, correo electrónico, push) para las fases clave: inicio, en curso y finalización.

1. **[Seleccione la audiencia del desafío](#audience)**: defina qué clientes pueden participar en el desafío.

1. **[Generar y activar el recorrido](#review-and-publish)**: genere el recorrido asociado y actívelo para que el desafío esté disponible para la audiencia de destino.

## Creación del desafío {#create-the-challenge}

1. Vaya a **[!UICONTROL Desafíos de fidelidad (Beta)]** en Journey Optimizer.

1. Seleccione la ficha **[!UICONTROL Desafíos]** y seleccione **[!UICONTROL Crear desafío]**.

   ![](assets/challenge-create.png)

1. Elija el tipo de desafío:

   * **[!UICONTROL Estándar]**: los clientes completan cualquier número especificado de tareas en cualquier orden
   * **[!UICONTROL Streak]**: Los clientes completan la misma tarea varias veces de forma consecutiva
   * **[!UICONTROL Secuencial]**: Los clientes completan tareas en un orden definido

## Configuración de la estructura de desafíos {#structure}

La pestaña Estructura es donde define cómo se organiza el desafío: sus propiedades, programación, las tareas que se deben completar y las recompensas que se deben entregar.

### Defina las propiedades del desafío y utilice metadatos personalizados {#properties}

1. En el panel Propiedades del desafío, configure las propiedades del desafío:

   ![](assets/challenge-create-properties.png)

   **Nombre**: escriba un nombre descriptivo para el desafío. Este nombre aparece en el inventario de desafíos y le ayuda a identificar el desafío.

   **Descripción**: Escriba una descripción para el desafío.

1. Utilice la sección **[!UICONTROL Metadatos personalizados]** para agregar metadatos personalizados mediante pares clave/valor. Estos metadatos se pueden utilizar para el seguimiento, la segmentación o la integración con sistemas externos.

### Programar el desafío {#schedule}

Programe el desafío seleccionando el icono ![](assets/do-not-localize/schedule-icon.svg) **[!UICONTROL Abrir programación]**.

* **Fecha y hora de inicio**: establezca cuándo el desafío estará disponible para los clientes (formato: mm/dd/aaaa, —:— AM/PM).

* **Fecha y hora de finalización**: establezca cuándo caduca el desafío y ya no acepta nuevas finalizaciones (formato: mm/dd/aaaa, —:— AM/PM).

* **Zona horaria**: El desafío utiliza la zona horaria local del destinatario de forma predeterminada.

* **Las tareas deben completarse**: elija cuándo los clientes pueden completar las tareas:

   * **[!UICONTROL En cualquier momento durante el desafío]**: los clientes pueden completar las tareas en cualquier momento entre las fechas de inicio y finalización del desafío
   * **[!UICONTROL Durante horas específicas del día]**: Restrinja la finalización de tareas a horas diarias específicas al establecer **[!UICONTROL Hora de inicio]** y **[!UICONTROL Hora de finalización]**

La programación de desafíos ya está configurada. Ahora puede agregar las tareas que los clientes necesitan completar.

### Agregar tareas {#add-tasks}

Las tareas definen las acciones o los hitos específicos que los clientes deben completar para obtener recompensas. Puede configurar tipos de tareas (compras, gastos, visitas, participaciones, eventos personalizados), cantidades, filtros de productos y recompensas.

Según el tipo de desafío, los clientes completan las tareas de forma diferente:

* **Desafíos estándar**: complete cualquier número especificado de tareas en cualquier orden
* **Rastrear desafíos**: complete la misma tarea varias veces de manera consecutiva
* **Desafíos secuenciales**: complete las tareas en un orden definido

Para añadir tareas al desafío, siga estos pasos:

1. En la sección **[!UICONTROL Tareas]**, seleccione **[!UICONTROL Agregar tarea]**.

   ![](assets/challenge-create-add-task.png)

1. Se abre el inventario Tareas. Seleccione una o más tareas de la lista y seleccione **[!UICONTROL Agregar]**. Para crear una tarea nueva, seleccione **[!UICONTROL Nuevo]**.

   Para obtener instrucciones detalladas sobre cómo crear y configurar tareas, consulte [Crear tareas](create-tasks.md).

1. En la sección **[!UICONTROL Requisito para finalizar la tarea]**, especifique cuándo se debe considerar completado el desafío:

   * **[!UICONTROL El cliente elige 1 tarea para completar]**: El cliente puede seleccionar y completar cualquier tarea del desafío para obtener recompensas
   * **[!UICONTROL El cliente completa un número específico de tareas]**: el cliente debe completar un número definido de tareas. Introduzca el número necesario de finalizaciones de tareas.

1. De forma predeterminada, los desafíos permiten a los clientes completar tareas en varias transacciones. Para requerir que todas las tareas se completen en una sola transacción, seleccione el icono ![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL Configuración]** y active la opción **[!UICONTROL Transacción única]**.

   ![](assets/challenge-create-single-transaction.png)

### Configuración de recompensas {#rewards}

Las recompensas son los puntos de lealtad o los beneficios que los clientes reciben por completar los desafíos. Configure cómo y cuándo se entregan las recompensas para motivar la participación del cliente.

1. En el menú desplegable **[!UICONTROL Entrega de recompensas]**, elija cuándo se deben entregar las recompensas:

   * **[!UICONTROL Entregar recompensas cuando se complete el desafío]**: Otorgue todas las recompensas cuando el cliente complete el desafío completo
   * **[!UICONTROL Entregar recompensas en hitos de finalización de tareas a medida que se avanza en el desafío]**: Las recompensas se incrementan a medida que los clientes completan tareas individuales (solo están disponibles cuando el desafío requiere completar más de una tarea)

1. Seleccione su proveedor de recompensas en el menú desplegable. Esta es su solución de fidelidad que administra los puntos y recompensas del cliente.

1. Configure los importes de recompensa en función del método de entrega seleccionado:

   +++Entregar recompensas cuando se complete el desafío

   En el campo **Cantidad de [puntos de fidelidad] al finalizar el desafío**, especifique la cantidad total de recompensa que se otorgará cuando el cliente complete el desafío completo.

   El nombre del campo muestra el nombre de los puntos de lealtad tal como se definen en el proveedor seleccionado. Por ejemplo, si su proveedor utiliza &quot;Puntos de Luma&quot;, el campo muestra &quot;Cantidad de puntos de Luma al finalizar el desafío&quot;.

   ![](assets/challenge-create-reward-total.png)

   **Ejemplo**: en la captura de pantalla anterior, los clientes obtienen 100 puntos al completar el desafío.

   +++

   +++Entregar recompensas en los hitos de finalización de tarea

   Especifique los importes de recompensa para los hitos de finalización de tarea. Esta opción le permite crear recompensas progresivas que aumentan la motivación del cliente a medida que este avanza en el desafío.

   Para cualquier tarea en la que desee entregar un premio, active la opción de recompensa y especifique cuántos puntos se otorgarán cuando los clientes completen esa tarea específica. Puede optar por recompensar sólo determinadas finalizaciones de tareas; por ejemplo, si tiene 10 tareas, puede recompensar sólo las tareas 1, 5 y 10.

   ![](assets/challenge-create-reward-milestones.png)

   **Ejemplo**: en la captura de pantalla anterior, se otorgan a los clientes 10 puntos al completar la primera tarea y luego 50 puntos adicionales después de completar la segunda tarea, para un total de 60 puntos cuando se completa el desafío.

   >[!TIP]
   >
   >Considere la posibilidad de aumentar los valores de recompensa por tareas posteriores para mantener la participación del cliente durante todo el desafío.

   +++

La estructura de desafíos ahora está configurada con tareas y recompensas. Ahora puede diseñar las tarjetas de contenido para mostrar el desafío a los clientes.

## Configuración de tarjetas de contenido {#configure-content-cards}

Las tarjetas de contenido proporcionan la representación visual de su desafío en los dispositivos del cliente, mostrando información del desafío, el progreso y las recompensas. Más información sobre [tarjetas de contenido](../content-card/create-content-card.md).

Para configurar las tarjetas de contenido para el desafío:

1. En el editor de retos, vaya a la pestaña **[!UICONTROL Contenido]**.

1. Escriba un **[!UICONTROL Nombre]** para la tarjeta de contenido.

1. Seleccione la **[!UICONTROL configuración de canal]** asociada. Las configuraciones de canal definen cómo y dónde se entrega el contenido a los clientes. Para obtener más información, consulte [Configuraciones de canal](../configuration/channel-surfaces.md).

1. Seleccione **[!UICONTROL Editar contenido]** para diseñar su tarjeta de contenido.

   ![](assets/challenge-create-content.png)

Para obtener más información sobre cómo diseñar y personalizar tarjetas de contenido, consulte [Diseñar tarjetas de contenido](../content-card/design-content-card.md).

La tarjeta de contenido ya está configurada. Ahora puede configurar la mensajería para atraer a los clientes a lo largo del ciclo de vida del desafío.

### Configuración de mensajería {#configure-messaging}

Configure mensajes multicanal para atraer a los clientes en etapas clave del ciclo de vida del desafío.

1. Vaya a la ficha **[!UICONTROL Mensajería]**.

1. Configure mensajes para cada fase del ciclo vital:

   ![](assets/challenge-create-messaging.png)

   * **Mensajes de lanzamiento**: notifique a los clientes cuando comience el desafío y proporcione los detalles iniciales
   * **Mensajes en curso**: mantenga a los clientes comprometidos durante el desafío con recordatorios, actualizaciones de progreso y ánimo para continuar
   * **Mensajes de finalización**: celebra el éxito, confirma la asignación de la recompensa y sugiere los próximos desafíos o acciones

1. Para cada fase, seleccione **[!UICONTROL Agregar mensaje *stage*]** para crear un mensaje para esa fase.

1. Elija el canal que desee: **[!UICONTROL En la aplicación]**, **[!UICONTROL Correo electrónico]** o **[!UICONTROL Notificación push]** y seleccione la configuración de canal asociada.

1. Seleccione el icono ![](assets/do-not-localize/Smock_More_18_N.svg) y elija **[!UICONTROL Editar]** para diseñar el contenido del mensaje.

   Para obtener más información sobre la creación de mensajes para canales específicos, consulte:

   * [Documentación de mensajes en la aplicación](../in-app/get-started-in-app.md)
   * [Documentación de correos electrónicos](../email/get-started-email.md)
   * [Documentación de notificaciones push](../push/get-started-push.md)

1. Repita estos pasos para cada fase y canal según sea necesario.

La configuración de la mensajería ya está completa. Ahora puede definir qué clientes pueden participar en el desafío.

## Selección de la audiencia del desafío {#audience}

Defina qué clientes pueden participar en su desafío de fidelidad.

1. Vaya a la pestaña **[!UICONTROL Audiencia]** y haga clic en el botón **[!UICONTROL Seleccionar audiencia]**.

   ![](assets/challenge-create-audience.png)

1. Se muestran todas las audiencias de Adobe Experience Platform disponibles. Seleccione la audiencia que desee en la lista.

1. Seleccione **[!UICONTROL Agregar audiencia]** para confirmar su selección.

Se ha completado la configuración del desafío. Ahora puede generar el recorrido que organizará la entrega de desafío.

## Generación y activación del recorrido {#review-and-publish}

Cuando finalice la configuración del desafío, genere el recorrido asociado que organizará la entrega del desafío y las interacciones con los clientes. Para ello, seleccione **[!UICONTROL Generar Recorrido]**.

![](assets/challenge-create-generate-journey.png)

Journey Optimizer crea automáticamente un [recorrido](../building-journeys/journey-gs.md) en estado de Borrador. El recorrido generado automáticamente aparece en su inventario de recorridos con el formato de nombre &quot;Desafío: [Nombre del desafío]&quot;.

Revisa la configuración del recorrido si es necesario, luego [activa el recorrido](../building-journeys/publish-journey.md) para que el desafío esté disponible para los clientes.

El recorrido se iniciará automáticamente en la fecha de inicio del desafío especificada y enviará el contenido y los mensajes según la configuración.

>[!NOTE]
>
>El recorrido generado automáticamente se puede personalizar si es necesario para agregar lógica o mensajes adicionales. Sin embargo, los cambios realizados directamente en el recorrido no se sincronizan con la configuración de desafío. Si edita el desafío más adelante, las personalizaciones del recorrido se perderán cuando se regenere el recorrido.

## Próximos pasos {#next-steps}

* [Administrar desafíos](manage-challenges.md): Aprenda a editar, monitorizar y optimizar desafíos
* [Comprender los desafíos de fidelidad](get-started.md): revise las características y capacidades
