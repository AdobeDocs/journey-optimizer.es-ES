---
solution: Journey Optimizer
product: journey optimizer
title: Añadir una actividad de canal en una campaña de varios pasos
description: Obtenga información sobre cómo añadir una actividad de canal en una campaña de varios pasos
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 15%

---

# Actividades del canal {#channel}

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

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md) | [Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Organice las actividades](orchestrate-activities.md)<br/><br/><b>[Inicie y supervise la campaña](start-monitor-campaigns.md)</b><br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md)<br/><br/>[Redireccionamiento](retarget.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar](save-audience.md) - [División](activities/split.md) [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

[!DNL Adobe Journey Optimizer] le permite automatizar y ejecutar campañas de marketing en todos los canales: correo electrónico, SMS y notificaciones push. Puede combinar estas actividades de canal en el lienzo de la campaña para crear campañas orquestadas en canales múltiples que puedan almacenar en déclencheur acciones basadas en la conducta y los datos del cliente.

Por ejemplo:
* Envíe una serie de bienvenida por correo electrónico, SMS y push.
* Envíe un correo electrónico de seguimiento después de la compra.
* Envíe saludos de cumpleaños personalizados por SMS.

Mediante las actividades del canal, puede crear campañas completas y personalizadas que atraigan a los clientes en varios touchpoints e impulsen las conversiones.

>[!PREREQUISITES]
>
>Antes de agregar una actividad de canal, defina la audiencia de destinatario con una [actividad de audiencia de compilación](build-audience.md).

## Añada una actividad de canal y defina sus propiedades {#add}

1. Añada una actividad de canal al lienzo. Las actividades de canal disponibles son **[!UICONTROL Correo electrónico]**, **[!UICONTROL SMS]** y **[!UICONTROL Push]**.

   ![imagen que muestra el lienzo con actividades disponibles](../assets/channel-add.png)

1. Seleccione la actividad y haga clic en **[!UICONTROL Editar correo electrónico]**, **[!UICONTROL Editar SMS]** o **[!UICONTROL Editar push]** según el canal elegido.

   ![imagen que muestra el lienzo con una actividad de correo electrónico](../assets/channel-edit.png)

1. En la ficha **[!UICONTROL Propiedades]**, escriba una descripción y, a continuación, cambie a la ficha **[!UICONTROL Acciones]** para configurar la actividad.

## Configurar la configuración y los ajustes del canal {#configuration}

Use la ficha **[!UICONTROL Acciones]** para seleccionar una configuración de canal para el mensaje y establecer opciones adicionales como seguimiento, experimento de contenido o contenido multilingüe.

1. Seleccione una configuración de canal.

   Un [administrador del sistema](../../start/path/administrator.md) define una configuración. Contiene todos los parámetros técnicos para enviar el mensaje, como parámetros de encabezado, subdominio, aplicaciones móviles, etc. [Aprenda a configurar las configuraciones de canal](../../configuration/channel-surfaces.md).

   ![imagen que muestra la sección Acciones](../assets/channel-actions.png)

1. Rastree la participación (para correo electrónico y SMS).

   Utilice la sección **[!UICONTROL Seguimiento de acciones]** para rastrear cómo reaccionan sus destinatarios a sus envíos de correo electrónico o SMS. Se puede acceder a los resultados de seguimiento desde el informe de campaña una vez que se ha ejecutado la campaña. [Más información sobre los informes de campaña](../../reports/campaign-global-report-cja.md)

1. Active el modo de envío rápido (para push).

   El modo de envío rápido es un complemento de [!DNL Journey Optimizer] que permite el envío muy rápido de mensajes push en grandes volúmenes a través de campañas. La entrega rápida se utiliza cuando el retraso en la entrega de mensajes es crítico para la empresa, cuando desea enviar una alerta push urgente en teléfonos móviles, por ejemplo, una noticia de última hora a los usuarios que han instalado su aplicación de canal de noticias. Para obtener más información sobre el rendimiento al usar el modo de envío rápido, consulte [Descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html).

1. Cree un experimento de contenido.

   Utilice la sección **[!UICONTROL Experimento de contenido]** para definir varios tratamientos de envío y medir cuál ofrece el mejor rendimiento para la audiencia de destino. Haga clic en el botón **[!UICONTROL Crear experimento]** y siga los pasos detallados en esta sección: [Crear un experimento de contenido](../../content-management/content-experiment.md).

1. Añada contenido multilingüe.

   Utilice la sección **[!UICONTROL Idiomas]** para crear contenido en varios idiomas dentro de la campaña. Para ello, haga clic en el botón **[!UICONTROL Agregar idiomas]** y seleccione la **[!UICONTROL configuración de idioma]** que desee. Encontrará información detallada sobre cómo configurar y utilizar las funciones multilingües en esta sección: [Introducción al contenido multilingüe](../../content-management/multilingual-gs.md)

   ![imagen que muestra la sección Experimento de contenido](../assets/channel-experiment.png)

Una vez configurada la actividad del canal, selecciona la pestaña **[!UICONTROL Contenido]** para definir su contenido.

## Definición del contenido {#content}

Cambie a la ficha **[!UICONTROL Contenido]** para crear el mensaje. El proceso de pasos varía en función del canal seleccionado. Conozca los pasos detallados para crear el contenido del mensaje en las siguientes páginas.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="../../email/create-email.md"><img alt="Correo electrónico" src="../../channels/assets/do-not-localize/email.png"></a><br/><a href="../../email/create-email.md"><strong>Crear un correo electrónico</strong></a></td>
<td><a href="../../sms/create-sms.md"><img alt="SMS" src="../../channels/assets/do-not-localize/sms.png"></a><br/><a href="../../sms/create-sms.md"><strong>Creación de un SMS</strong></a></td>
<td><a href="../../push/create-push.md"><img alt="push" src="../../channels/assets/do-not-localize/push.png"></a><a href="../../push/create-push.md"><strong>Crear una notificación push</strong></a></td>
</tr></table>

Una vez creado el contenido, use el botón **[!UICONTROL Simular contenido]** para obtener una vista previa y probar el contenido con perfiles de prueba o datos de entrada de muestra cargados desde un archivo CSV/JSON, o agregados manualmente. [Más información](../../content-management/preview-test.md)

![imagen que muestra el botón Simular contenido](../assets/channel-simulate.png)

## Pasos siguientes {#next}

Cuando el contenido del mensaje esté listo, vuelva a la campaña orquestada con la flecha **[!UICONTROL Atrás]**. A continuación, puede completar la orquestación de actividades en el lienzo y publicar la campaña para iniciar el envío de mensajes. [Aprenda a iniciar y supervisar campañas orquestadas](../start-monitor-campaigns.md)

![imagen que muestra el botón de retroceso](../assets/channel-back.png)

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
