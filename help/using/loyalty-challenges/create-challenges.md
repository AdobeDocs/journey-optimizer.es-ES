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
source-git-commit: 831809b4c1dd19fdaeeb646695f606c02ec21265
workflow-type: tm+mt
source-wordcount: '888'
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

<!-- SCHEMA: Visual workflow showing the 5 main steps with icons: Create challenge → Add tasks → Design content cards → Configure messaging → Review and publish -->

La creación y el lanzamiento de un desafío de fidelidad siguen este flujo de trabajo:

1. **Crear un desafío**: defina las propiedades básicas del desafío, como nombre, tipo (Estándar, Streak o Secuencial), audiencia e intervalo de fechas.

1. **Agregar tareas**: defina las acciones específicas que deben completar los clientes, incluidos los tipos de tareas (compras, gastos, visitas, etc.), cantidades, filtros de productos y recompensas.

1. **Diseñar tarjetas de contenido**: cree la representación visual de su desafío con tarjetas de contenido de Journey Optimizer que se muestran en los dispositivos del cliente.

1. **Configurar mensajes** (opcional): configura mensajes multicanal (en la aplicación, correo electrónico, push, SMS) para las fases clave: inicio, en curso y finalización.

1. **Revisar y publicar**: pruebe el desafío con perfiles de prueba y, a continuación, publíquelo para que esté disponible para la audiencia de destino.

## Creación del desafío {#create-challenge}

<!-- SCREENSHOT: Challenge creation screen showing challenge properties form with fields for name, type, audience, dates -->

Para crear un nuevo desafío de fidelidad:

1. Vaya a **[!UICONTROL Desafíos de fidelización]** en Journey Optimizer.

1. Seleccione la ficha **[!UICONTROL Desafíos]**.

1. Seleccione **[!UICONTROL Crear desafío]**.

1. Configure las propiedades del desafío:

   **Nombre del desafío**: escriba un nombre descriptivo para el desafío. Este nombre aparece en el inventario de desafíos y le ayuda a identificar el desafío.

   **Tipo de desafío**: seleccione uno de los siguientes tipos:
   * **[!UICONTROL Estándar]**: los clientes completan cualquier número especificado de tareas en cualquier orden
   * **[!UICONTROL Streak]**: Los clientes completan la misma tarea varias veces de forma consecutiva
   * **[!UICONTROL Secuencial]**: Los clientes completan tareas en un orden definido

   **Audiencia objetivo**: seleccione el segmento de audiencia que define quién puede participar en este desafío. Debe crear audiencias en Experience Platform antes de crear desafíos. Para obtener más información, consulte [Introducción a las audiencias](../audience/about-audiences.md).

   **Fecha de inicio**: establece cuándo el desafío estará disponible para los clientes.

   **Fecha de finalización**: establece cuándo caduca el desafío y ya no acepta nuevas finalizaciones.

<!-- VISUAL: Comparison table or diagram showing the three challenge types (Standard, Streak, Sequential) with examples of each -->

### Agregar tareas {#add-tasks}

Las tareas definen las acciones o los hitos específicos que los clientes deben completar para obtener recompensas. Puede configurar tipos de tareas (compras, gastos, visitas, participaciones, eventos personalizados), cantidades, filtros de productos y recompensas.

Según el tipo de desafío, los clientes completan las tareas de forma diferente:

* **Desafíos estándar**: complete cualquier número especificado de tareas en cualquier orden
* **Rastrear desafíos**: complete la misma tarea varias veces de manera consecutiva
* **Desafíos secuenciales**: complete las tareas en un orden definido

Para agregar tareas al desafío, seleccione **[!UICONTROL Agregar tarea]** en la sección Tareas y configure las propiedades de la tarea.

Para obtener instrucciones detalladas sobre cómo crear y configurar tareas, consulte [Crear tareas](create-tasks.md).

### Configuración de tarjetas de contenido {#configure-content-cards}

<!-- SCREENSHOT: Content cards configuration section in the challenge editor -->

Las tarjetas de contenido proporcionan la representación visual de su desafío en los dispositivos del cliente, mostrando información del desafío, el progreso y las recompensas. Más información sobre [tarjetas de contenido](../content-card/create-content-card.md).

<!-- VISUAL: Example content card designs showing different states: challenge start, in-progress with progress bar, completion with reward -->

Para configurar las tarjetas de contenido para el desafío:

1. En el editor de retos, vaya a la sección **[!UICONTROL Tarjetas de contenido]**.

1. Seleccione **[!UICONTROL Crear tarjeta de contenido]** o elija una plantilla existente.

1. Diseñe su tarjeta de contenido:
   * Agregar imágenes, texto y elementos de personalización de marca
   * Incluir [tokens de personalización](../personalization/personalization-syntax.md) para mostrar información específica del cliente
   * Mostrar indicadores de progreso de desafío
   * Mostrar recompensas e incentivos

1. Configure cuándo se mostrará la tarjeta de contenido:
   * **Inicio del desafío**: mostrar cuando el desafío esté disponible
   * **En curso**: mostrar mientras los clientes participan activamente
   * **Finalización**: mostrar después de que los clientes completen todas las tareas

1. Previsualice la tarjeta de contenido en diferentes dispositivos para garantizar una visualización adecuada.

1. Guarde la configuración de la tarjeta de contenido.

Para obtener más información sobre cómo diseñar y personalizar tarjetas de contenido, consulte [Diseñar tarjetas de contenido](../content-card/design-content-card.md).

### Configuración de mensajería {#configure-messaging}

<!-- SCREENSHOT: Messaging configuration section showing the three lifecycle stages: Launch, In-progress, Completion -->

Configure mensajes multicanal para atraer a los clientes en etapas clave del ciclo de vida del desafío.

<!-- VISUAL: Timeline diagram showing when each message type is sent during the challenge lifecycle -->

Para configurar la mensajería para su desafío:

1. En el editor de desafíos, vaya a la sección **[!UICONTROL Mensajería]**.

1. Configure mensajes para cada fase del ciclo vital:

   **Mensajes de inicio** - Notificar a los clientes cuando comience el desafío:
   * Seleccionar canales: [En la aplicación](../in-app/get-started-in-app.md), [correo electrónico](../email/get-started-email.md), [notificación push](../push/get-started-push.md) o [SMS](../sms/get-started-sms.md)
   * Diseño del mensaje con detalles del desafío y call-to-action
   * Establecer tiempo: Enviar inmediatamente cuando el desafío se active o programe para una hora específica

   **Mensajes en curso** - Mantener el interés de los clientes durante el desafío:
   * Defina las condiciones del déclencheur (por ejemplo, finalización del 50 %, finalización de una tarea específica)
   * Cree mensajes recordatorios para alentar la participación continua
   * Incluir actualizaciones en curso y pasos siguientes

   **Mensajes de finalización** - Celebra el éxito y entrega recompensas:
   * Felicitar a los clientes por completar el desafío
   * Confirmar asignación de recompensa
   * Proporcione instrucciones para reclamar recompensas
   * Sugerir desafíos o acciones siguientes

Para obtener más información sobre la creación de mensajes para canales específicos, consulte:

* [Documentación de mensajes en la aplicación](../in-app/get-started-in-app.md)
* [Documentación de correos electrónicos](../email/get-started-email.md)
* [Documentación de notificaciones push](../push/get-started-push.md)
* [Documentación de mensajes SMS](../sms/get-started-sms.md)

## Revisar y publicar el desafío {#review-and-publish}

<!-- SCREENSHOT: Review screen showing summary of challenge configuration with all components listed -->

Antes de publicar el desafío:

1. **Revisar todos los componentes**: Compruebe las propiedades, tareas, recompensas, tarjetas de contenido y configuraciones de mensajería del desafío.

1. **Probar la experiencia**: use [perfiles de prueba](../test-approve/test-profiles.md) para validar la visualización de la tarjeta de contenido y el comportamiento del déclencheur de tareas.

1. **Publicar**: Seleccione **[!UICONTROL Publicar]** para que el desafío esté disponible para la audiencia de destino.

<!-- SCREENSHOT: Journeys inventory showing the auto-generated journey in Draft status with name format "Challenge: [Challenge Name]" -->

Cuando publica un desafío, Journey Optimizer crea automáticamente un [recorrido](../building-journeys/journey-gs.md) en estado de Borrador. El recorrido generado automáticamente aparece en su inventario de recorridos con el formato de nombre &quot;Desafío: [Nombre del desafío]&quot;.

Para poner el desafío a disposición de los clientes:

1. Vaya al inventario de **[!UICONTROL Recorridos]** en Journey Optimizer.

1. Busque el recorrido generado automáticamente (tendrá el prefijo &quot;Challenge:&quot; en su nombre).

1. [Activar el recorrido](../building-journeys/publishing-the-journey.md).

El recorrido se inicia automáticamente en la fecha de inicio del desafío especificada.

>[!NOTE]
>
>El recorrido generado automáticamente aparece en el inventario de recorridos y se puede personalizar si es necesario. Sin embargo, los cambios realizados directamente en el recorrido no se sincronizan con la configuración de desafío.

## Próximos pasos {#next-steps}

* [Administrar desafíos](manage-challenges.md): Aprenda a editar, monitorizar y optimizar desafíos
* [Comprender los desafíos de fidelidad](get-started.md): revise las características y capacidades

