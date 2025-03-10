---
solution: Journey Optimizer
product: journey optimizer
title: Uso de una actividad de canal
description: Obtenga información sobre cómo añadir una actividad de canal
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 48%

---

# Actividades del canal {#channel}

Adobe Journey Optimizer le permite automatizar y ejecutar campañas de marketing en canales entrantes y salientes. Puede combinar actividades de canal en el lienzo de campaña de varios pasos para crear campañas de varios pasos en canales múltiples que puedan almacenar en déclencheur acciones basadas en la conducta y los datos del cliente. Los canales admitidos se enumeran en [esta página](../../channels/gs-channels.md).

Por ejemplo, puede crear una campaña de correo electrónico de bienvenida que incluya una serie de mensajes en diferentes canales, como correo electrónico, SMS, push y correo directo. También puede enviar un correo electrónico de seguimiento a los clientes después de que hayan completado una compra o enviarles un mensaje de cumpleaños personalizado a través de SMS.

Mediante las actividades del canal, puede crear campañas completas y personalizadas que atraigan a los clientes en varios touchpoints e impulsen las conversiones.

## Requisitos previos {#channel-activity-prereq}

Comience a crear su campaña de varios pasos con las actividades relevantes:

* Antes de insertar una actividad de canal, debe definir la audiencia. La audiencia es el destinatario principal del envío: los perfiles que reciben los mensajes.

* Para realizar una entrega recurrente, inicie su campaña de varios pasos con una actividad de **Planificador**. También puede usar una actividad **Scheduler** para envíos únicos de una sola toma a fin de establecer la fecha de contacto para ese envío. Esa fecha de contacto también se puede establecer en la configuración de envío. Consulte [esta sección](scheduler.md).

## Configuración de la actividad de canal {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="Actividad de correo electrónico"
>abstract="La actividad Correo electrónico facilita el envío de correos electrónicos dentro del flujo de trabajo, lo que permite mensajes únicos y recurrentes. Sirve para automatizar el proceso de envío de correos electrónicos a un destinatario calculado dentro del mismo flujo de trabajo. Puede combinar actividades del canal en el lienzo del flujo de trabajo para crear flujos de trabajo entre canales que puedan activar acciones basadas en el comportamiento y los datos del cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="Actividad de SMS"
>abstract="La actividad de SMS facilita el envío de SMS dentro del flujo de trabajo, lo que permite mensajes únicos y recurrentes. Sirve para automatizar el proceso de envío de SMS a un destinatario calculado dentro del mismo flujo de trabajo. Puede combinar actividades del canal en el lienzo del flujo de trabajo para crear flujos de trabajo entre canales que puedan activar acciones basadas en el comportamiento y los datos del cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Actividad de push iOS"
>abstract="La actividad Push de iOS optimiza el proceso de envío de notificaciones Push de iOS como parte del flujo de trabajo. Permite la entrega de mensajes recurrentes y únicos, lo que automatiza el envío de notificaciones Push de iOS a un destino predefinido dentro del mismo flujo de trabajo. Puede combinar actividades del canal en el lienzo del flujo de trabajo para crear flujos de trabajo entre canales que puedan activar acciones basadas en el comportamiento y los datos del cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Actividad de mensajería push de Android"
>abstract="La actividad Push de Android optimiza el proceso de envío de notificaciones Push de Android como parte del flujo de trabajo. Permite enviar mensajes recurrentes y únicos, lo que automatiza el envío de notificaciones Push de Android a un destino predefinido dentro del mismo flujo de trabajo. Puede combinar actividades del canal en el lienzo del flujo de trabajo para crear flujos de trabajo entre canales que puedan activar acciones basadas en el comportamiento y los datos del cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Actividad de correo directo"
>abstract="La actividad de correo directo facilita el envío de correo directo dentro del flujo de trabajo, lo que permite mensajes únicos y recurrentes. Sirve para automatizar el proceso de generación del archivo de extracción requerido por los proveedores de correo directo. Puede combinar actividades del canal en el lienzo del flujo de trabajo para crear flujos de trabajo entre canales que puedan activar acciones basadas en el comportamiento y los datos del cliente."

Para configurar una entrega en el contexto de una campaña de varios pasos, siga los pasos a continuación:

1. Agregue una actividad de canal: **[!UICONTROL Correo electrónico]**, **[!UICONTROL SMS]**, **[!UICONTROL Notificación push (Android)]**, **[!UICONTROL Notificación push (iOS)]** o **[!UICONTROL Correo directo]**.

1. Seleccione **Tipo de entrega**: individual o recurrente.

   * Una **entrega única** es una entrega de una sola toma que se envía una sola vez, por ejemplo un correo electrónico de Black Friday.
   * Se realiza **una entrega recurrente** varias veces según su frecuencia de ejecución definida en una [actividad de planificador](scheduler.md). Cada vez que se ejecuta la campaña de varios pasos, la audiencia se vuelve a calcular y la entrega se envía a la audiencia actualizada, con el contenido actualizado. Puede ser un boletín semanal o un correo electrónico de cumpleaños recurrente, por ejemplo.

1. Seleccione una **Plantilla** de envío. Las plantillas son opciones de envío preconfigurados específicos de un canal. Hay disponible una plantilla integrada para cada canal que se rellena previamente de forma predeterminada.

   ![](../assets/delivery-activity-in-wf.png)

   Puede seleccionar la plantilla en el panel izquierdo de configuración de actividad de canal. Si el público seleccionado anteriormente no es compatible con el canal, no se puede seleccionar una plantilla. Para resolver esto, actualice la actividad **Generar audiencia** para seleccionar una audiencia con la asignación de destino correcta.

1. Haga clic en **Crear envío**. A continuación, puede definir la configuración del mensaje y el contenido del mismo modo que crea un envío independiente. También puede probar y simular el contenido.

1. Vuelva al flujo de trabajo. Si desea continuar con su flujo de trabajo, active la opción **Generar una transición saliente** para agregar una transición después de la actividad del canal.

1. Haga clic en **Iniciar** para iniciar la campaña de varios pasos.

   De forma predeterminada, el inicio de una campaña de varios pasos déclencheur la fase de preparación del mensaje, sin enviarlo inmediatamente.

1. Abra la actividad del canal para confirmar el envío desde el botón **Revisar y enviar**.

1. En el panel de envíos, haga clic en **Enviar**.

## Ejemplos {#cross-channel-workflow-sample}

Este es un ejemplo de campaña en canales múltiples con una segmentación y dos envíos. La campaña de varios pasos está dirigida a todos los clientes que viven en París y que están interesados en las máquinas de café. Se envía un correo electrónico a los clientes habituales y un SMS a los clientes VIP de esta población.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

También puede crear una campaña recurrente de varios pasos para enviar un SMS personalizado todos los primeros días del mes a las 8 p. m. a todos los clientes que viven en París.

![](../assets/workflow-channel-example2.png)

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
