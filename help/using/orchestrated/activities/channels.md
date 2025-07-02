---
solution: Journey Optimizer
product: journey optimizer
title: Añadir una actividad de canal en una campaña de varios pasos
description: Obtenga información sobre cómo añadir una actividad de canal en una campaña de varios pasos
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 1a4cd7df44cb54aaf4d18409574f5ceb9537935c
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 16%

---

# Actividades del canal {#channel}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](../configuration-steps.md)<br/><br/>[Pasos clave para la creación de campañas orquestadas](../gs-campaign-creation.md) | [Crear una campaña orquestada](../create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](../orchestrate-activities.md)<br/><br/><br/>[Iniciar y supervisar la campaña](../start-monitor-campaigns.md)<br/><br/>[Informes](../reporting-campaigns.md) | [Trabaje con el Modeler de consultas](../orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](../build-query.md)<br/><br/>[Editar expresiones](../edit-expressions.md) | [Empiece con las actividades](about-activities.md)<br/><br/>Actividades:<br/>[Y únase](and-join.md) - [Generar audiencia](build-audience.md) - [Cambiar dimensión](change-dimension.md) - **[Actividades de canal](channels.md)** - [Combinar](combine.md) - [Anulación de duplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [División](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

[!DNL Adobe Journey Optimizer] le permite automatizar y ejecutar campañas de marketing en todos los canales. Puede combinar actividades de canal en el lienzo de campaña orquestado para crear campañas orquestadas de varios canales que puedan almacenar en déclencheur acciones basadas en el comportamiento y los datos del cliente.

Por ejemplo, puede crear una campaña de correo electrónico de bienvenida que incluya una serie de mensajes en diferentes canales, como correo electrónico, SMS y push. También puede enviar un correo electrónico de seguimiento a los clientes después de que hayan completado una compra o enviarles un mensaje de cumpleaños personalizado a través de SMS.

Mediante las actividades de canal, puede crear campañas completas y personalizadas que atraigan a los clientes en varios puntos de contacto e impulsen las conversiones. Los canales admitidos son Correo electrónico, SMS y Push.

## Requisitos previos {#channel-activity-prereq}

Comience a crear su campaña orquestada con las actividades relevantes:

* Antes de insertar una actividad de canal, debe definir la audiencia. La audiencia es el destinatario principal del envío: los perfiles que reciben los mensajes. [Aprenda a utilizar la actividad Generar audiencia](build-audience.md)

* Para realizar una entrega recurrente, inicie la campaña orquestada con una actividad **[!UICONTROL Scheduler]**. También puede usar una actividad **[!UICONTROL Scheduler]** para envíos únicos de una sola toma a fin de establecer la fecha de contacto para ese envío. Esa fecha de contacto también se puede establecer en la configuración de envío. [Aprenda a programar una campaña organizada](../create-orchestrated-campaign.md#schedule)

## Configuración de una actividad de canal {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="Actividad de Correo electrónico"
>abstract="La actividad Correo electrónico permite enviar correos electrónicos dentro de la campaña orquestada, tanto para mensajes únicos como recurrentes. Sirve para automatizar el proceso de envío de correos electrónicos a un destinatario calculado dentro de la misma campaña orquestada. Puede combinar actividades de canal en el lienzo de la campaña de varios pasos para crear campañas en canales múltiples que puedan activar acciones basadas en el comportamiento y los datos del cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="Actividad de SMS"
>abstract="La actividad SMS permite enviar SMS dentro de la campaña orquestada, para mensajes únicos y recurrentes. Sirve para automatizar el proceso de envío de SMS a un destinatario calculado dentro de la misma campaña orquestada. Puede combinar actividades de canal en el lienzo de la campaña de varios pasos para crear campañas en canales múltiples que puedan activar acciones basadas en el comportamiento y los datos del cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="Actividad push"
>abstract="La actividad Push permite enviar notificaciones push como parte de la campaña orquestada. Permite la entrega de campañas orquestadas únicas y recurrentes, lo que automatiza el envío de notificaciones push a un objetivo predefinido dentro de la misma campaña orquestada. Puede combinar actividades de canal en el lienzo de la campaña para crear campañas en canales múltiples que puedan almacenar en déclencheur acciones basadas en el comportamiento y los datos de los clientes."

<!--
UNUSED IDs in BJ

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Push iOS activity"
>abstract="The Push iOS activity let you send iOS Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring orchestrated campaigns, automating the sending iOS Push notifications to a predefined target within the same workflow. You can combine channel activities into the campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Push Android activity"
>abstract="The Push Android activity ket you send Android Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring messages, automating the sending Android Push notifications to a predefined target within the same orchestrated campaign. You can combine channel activities into the orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

-->

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Actividad de correo directo"
>abstract="La actividad de correo postal facilita el envío de correo postal dentro de la campaña orquestada, tanto para mensajes únicos como recurrentes. Sirve para automatizar el proceso de generación del archivo de extracción requerido por los proveedores de correo directo. Puede combinar actividades de canal en el lienzo de campaña orquestado para crear campañas en canales múltiples que puedan almacenar en déclencheur acciones basadas en la conducta y los datos del cliente."

Para configurar una entrega en el contexto de una campaña orquestada, siga los pasos a continuación.

### Añada una actividad de canal y defina sus propiedades {#add}

1. Añada una actividad de canal al lienzo. Las actividades de canal disponibles son **[!UICONTROL Correo electrónico]**, **[!UICONTROL SMS]** y **[!UICONTROL Push]**.

   ![imagen que muestra el lienzo con actividades disponibles](../assets/channel-add.png)

1. Seleccione la actividad agregada y haga clic en el botón **[!UICONTROL Editar correo electrónico]**, **[!UICONTROL Editar SMS]** o **[!UICONTROL Editar push]** según el canal elegido.

   ![imagen que muestra el lienzo con una actividad de correo electrónico](../assets/channel-edit.png)

1. En la ficha **[!UICONTROL Propiedades]**, escriba una descripción para la campaña.

### Configurar la configuración y los ajustes del canal {#configuration}

1. Seleccione la pestaña **[!UICONTROL Actions]** y elija la configuración de canal que desea utilizar para el mensaje.

   Un [administrador del sistema](../../start/path/administrator.md) define una configuración. Contiene todos los parámetros técnicos para enviar el mensaje, como parámetros de encabezado, subdominio, aplicaciones móviles, etc. [Aprenda a configurar las configuraciones de canal](../../configuration/channel-surfaces.md).

1. Según el canal, hay varias opciones disponibles. Examine las pestañas siguientes para obtener más información:

   >[!BEGINTABS]

   >[!TAB Correo electrónico]

   Use las opciones **[!UICONTROL Rastrear aperturas de correos electrónicos]** y **[!UICONTROL Rastrear clics en vínculos y botones del correo electrónico]** para rastrear cómo reaccionan los destinatarios a su envío.

   Se puede acceder a los resultados de seguimiento desde el informe de campaña una vez que se ha ejecutado la campaña. [Más información sobre los informes de campaña](../reports/campaign-global-report-cja.md)

   >[!TAB SMS]

   Use la opción **[!UICONTROL Rastrear clics en vínculos en SMS]** para rastrear clics en vínculos en su SMS.

   Se puede acceder a los resultados de seguimiento desde el informe de campaña una vez que se ha ejecutado la campaña. [Más información sobre los informes de campaña](../reports/campaign-global-report-cja.md)

   >[!TAB Push]

   El modo de envío rápido es un complemento de **[!DNL Journey Optimizer]** que permite enviar mensajes push muy rápidamente en grandes volúmenes.

   Habilite la opción **[!UICONTROL Modo de envío rápido]** para realizar el envío de mensajes de alta velocidad en el canal push a un tamaño de audiencia inferior a 30 millones. [Más información](../push/create-push.md#rapid-delivery)

   >[!ENDTABS]

1. La sección **[!UICONTROL Experimento de contenido]** le permite definir varios tratamientos de entrega para medir cuál ofrece el mejor rendimiento para la audiencia de destino.

   Para ello, haga clic en el botón **[!UICONTROL Crear experimento]** y siga los pasos detallados en esta sección: [Crear capacidades de experimentación de un experimento de contenido](../../content-management/content-experiment.md).

1. La sección **[!UICONTROL Idiomas]** le permite crear contenido en varios idiomas dentro de la campaña.

   Para ello, haga clic en el botón **[!UICONTROL Agregar idiomas]** y seleccione la **[!UICONTROL configuración de idioma]** que desee. Encontrará información detallada sobre cómo configurar y utilizar las funciones multilingües en esta sección: [Introducción al contenido multilingüe](../../content-management/multilingual-gs.md)

### Definición del contenido {#content}

Seleccione la ficha **[!UICONTROL Contenido]** para definir el contenido del mensaje. El proceso de creación de contenido depende del canal seleccionado.

Conozca los pasos detallados para crear el contenido del mensaje en las siguientes páginas:

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../../email/create-email.md"><img alt="Correo electrónico" src="../../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../../email/create-email.md"><strong>Correo electrónico</strong></a></div></td>
<td><a href="../sms/../create-sms.md"><img alt="SMS" src="../../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../../sms/create-sms.md"><strong>SMS</strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="push" src="../../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../../push/create-push.md"><strong>Notificación push</strong></a></div></td>
</tr></table>

Una vez definido el contenido, utilice el botón **[!UICONTROL Simular contenido]** para previsualizar y probar el contenido con perfiles de prueba o datos de entrada de muestra cargados desde un archivo CSV/JSON, o añadidos manualmente. [Más información](../content-management/preview-test.md).

## Pasos siguientes {#next}

Vuelva a la campaña orquestada con la flecha **[!UICONTROL Atrás]**.

![imagen que muestra el botón de retroceso](../assets/channel-back.png)

Ahora puede completar la orquestación de actividades en el lienzo y publicar la campaña para iniciar el envío de mensajes. [Aprenda a iniciar y supervisar campañas orquestadas](../start-monitor-campaigns.md)

<!--
## Examples {#cross-channel-workflow-sample}

Here is a cross-channel orchestrated campaign example with a segmentation and two deliveries. The orchestrated campaign targets all customers who live in Paris and who are interested in coffee machines. Among this population, an email is sent to the regular customers and an SMS is sent to the VIP clients.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

<!--You can also create a recurring orchestrated campaign to send a personalized SMS every first day of the month at 8 PM to all customers living in Paris.

![](../assets/workflow-channel-example2.png)-->

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
