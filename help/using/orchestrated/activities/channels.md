---
solution: Journey Optimizer
product: journey optimizer
title: Añadir una actividad de canal en una campaña de varios pasos
description: Obtenga información sobre cómo añadir una actividad de canal en una campaña de varios pasos
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 5e52573689ab06084441390299b01e112e699244
workflow-type: tm+mt
source-wordcount: '1213'
ht-degree: 58%

---

# Actividades del canal {#channel}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="Actividad del correo electrónico"
>abstract="La actividad Correo electrónico permite enviar correos electrónicos dentro de la campaña orquestada, tanto para mensajes únicos como recurrentes. Sirve para automatizar el proceso de envío de correos electrónicos a un destinatario calculado dentro de la misma campaña orquestada. Puede combinar actividades de canal en el lienzo de la campaña de varios pasos para crear campañas en canales múltiples que puedan activar acciones basadas en el comportamiento y los datos del cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="Actividad de SMS"
>abstract="La actividad SMS permite enviar SMS dentro de la campaña orquestada, para mensajes únicos y recurrentes. Sirve para automatizar el proceso de envío de SMS a un destinatario calculado dentro de la misma campaña orquestada. Puede combinar actividades de canal en el lienzo de la campaña de varios pasos para crear campañas en canales múltiples para activar acciones basadas en el comportamiento y los datos del cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="Actividad Push"
>abstract="La actividad Push permite enviar notificaciones push como parte de una campaña organizada. Permite la entrega de campañas orquestadas únicas y recurrentes, lo que automatiza el envío de notificaciones push a un objetivo predefinido dentro de la misma campaña orquestada. Puede combinar actividades de canal en el lienzo de la campaña para crear campañas en canales múltiples que puedan activar acciones basadas en el comportamiento y los datos del cliente."

<!--
UNUSED IDs in BJ

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Push iOS activity"
>abstract="The Push iOS activity let you send iOS Push notifications as part of your Orchestrated campaign. It enables the delivery of both one-time and recurring Orchestrated campaigns, automating the sending iOS Push notifications to a predefined target within the same workflow. You can combine channel activities into the campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Push Android activity"
>abstract="The Push Android activity ket you send Android Push notifications as part of your Orchestrated campaign. It enables the delivery of both one-time and recurring messages, automating the sending Android Push notifications to a predefined target within the same Orchestrated campaign. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

-->

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Actividad de correo directo"
>abstract="La actividad de correo postal facilita el envío de correo postal dentro de la campaña orquestada, tanto para mensajes únicos como recurrentes. Sirve para automatizar el proceso de generación del archivo de extracción requerido por los proveedores de correo directo. Puede combinar actividades de canal en el lienzo de campaña orquestada para crear campañas en canales múltiples que puedan almacenar en déclencheur acciones basadas en la conducta y los datos del cliente."


+++ Índice

| Bienvenido a campañas orquestadas | Inicie su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carga de archivos](../file-upload-schema.md)</li><li>[Ingesta de datos](../ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](../access-manage-orchestrated-campaigns.md) | [Pasos clave para crear una campaña orquestada](../gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](../create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](../orchestrate-activities.md)<br/><br/>[Inicie y supervise la campaña](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabajo con el generador de reglas](../orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](../build-query.md)<br/><br/>[Edición de expresiones](../edit-expressions.md)<br/><br/>[Resegmentación](../retarget.md) | [Introducción a las actividades](about-activities.md)<br/><br/>Actividades:<br/>[AND-join](and-join.md) - [Generar público](build-audience.md) - [Cambiar dimensión](change-dimension.md) - <b>[Actividades del canal](channels.md)</b> - [Combinar](combine.md) - [Deduplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [Guardar público](save-audience.md) - [División](split.md) - [Esperar](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] le permite automatizar y ejecutar campañas de marketing en todos los canales: correo electrónico, SMS y notificaciones push. Puede combinar estas actividades de canal en el lienzo de la campaña para crear campañas orquestadas entre canales que puedan almacenar en déclencheur acciones basadas en la conducta y los datos del cliente.

Por ejemplo:
* Envíe una serie de bienvenida por correo electrónico, SMS y push.
* Envíe un correo electrónico de seguimiento después de la compra.
* Envíe felicitaciones de cumpleaños personalizadas por SMS.

Mediante las actividades del canal, puede crear campañas completas y personalizadas que atraigan a los clientes en varios puntos de contacto e impulsen las conversiones.

>[!PREREQUISITES]
>
>Antes de añadir una actividad de canal, defina el público destinatario con la [actividad Generar público](build-audience.md).

## Añadir una actividad de canal y definir sus propiedades {#add}

1. Añada una actividad de canal al lienzo. Las actividades de canal disponibles son **[!UICONTROL correo electrónico]**, **[!UICONTROL SMS]** y **[!UICONTROL push]**.

   ![imagen que muestra el lienzo con las actividades disponibles](../assets/channel-add.png)

1. Seleccione la actividad y haga clic en **[!UICONTROL Editar correo electrónico]**, **[!UICONTROL Editar SMS]** o **[!UICONTROL Editar push]**, según el canal elegido.

   ![imagen que muestra el lienzo con una actividad de correo electrónico](../assets/channel-edit.png)

1. En la pestaña **[!UICONTROL Propiedades]**, escriba una descripción y, a continuación, cambie a la pestaña **[!UICONTROL Acciones]** para configurar la actividad.

## Configuración del canal y los ajustes {#configuration}

Use la pestaña **[!UICONTROL Acciones]** para seleccionar una configuración de canal para el mensaje y configure ajustes adicionales como seguimiento, experimento de contenido o contenido multilingüe.

1. **Seleccionar una configuración de canal**

   La configuración la define el [administrador del sistema](../../start/path/administrator.md). Contiene todos los parámetros técnicos para enviar el mensaje, como parámetros de encabezado, subdominio, aplicaciones móviles, etc. [Aprenda a configurar canales](../../configuration/channel-surfaces.md).

   ![imagen que muestra la sección Acciones](../assets/channel-actions.png)

1. **Aplicar reglas de límite**

   En la lista desplegable **[!UICONTROL Conjunto de reglas]**, seleccione un conjunto de reglas de canal para aplicar reglas de límite a la campaña. El uso de conjuntos de reglas de canal le permite establecer límites de frecuencia por tipo de comunicación para evitar sobrecargar a los clientes con mensajes similares. [Descubra cómo trabajar con conjuntos de reglas](../../conflict-prioritization/rule-sets.md)

1. **Rastrear participación** (Correo electrónico y SMS)

   Utilice la sección **[!UICONTROL Seguimiento de la acción]** para rastrear cómo reaccionan sus destinatarios a sus envíos de correo electrónico o SMS. Puede acceder a los resultados de seguimiento desde el informe de campaña una vez que se haya ejecutado la campaña. [Más información sobre los informes de campaña](../../reports/campaign-global-report-cja.md)

1. **Habilitar modo de envío rápido** (push)

   El modo de envío rápido es un complemento de [!DNL Journey Optimizer] que permite el envío rápido de mensajes push en grandes volúmenes a través de campañas. El envío rápido se utiliza cuando el retraso en el envío de mensajes es crítico para la empresa y cuando desea enviar una alerta push urgente en teléfonos móviles, por ejemplo, una noticia de última hora a los usuarios que han instalado su aplicación de canal de noticias. Para obtener más información sobre el rendimiento al usar el modo de envío rápido, consulte [Descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html).

1. **Crear un experimento de contenido**

   Use la sección **[!UICONTROL Experimento de contenido]** para definir varios tratamientos de envío y poder medir cuál ofrece el mejor rendimiento para su público destinatario. Haga clic en el botón **[!UICONTROL Crear experimento]** y siga los pasos que se detallan en esta sección: [Crear un experimento de contenido](../../content-management/content-experiment.md).

1. **Agregar contenido multilingüe**

   Utilice la sección **[!UICONTROL Idiomas]** para crear contenido en varios idiomas dentro de la campaña. Para ello, haga clic en el botón **[!UICONTROL Añadir idiomas]** y seleccione la **[!UICONTROL Configuración de idioma]** que desee. Encontrará información detallada sobre cómo configurar y utilizar las funciones multilingües en esta sección: [Introducción al contenido multilingüe](../../content-management/multilingual-gs.md)

   ![imagen que muestra la sección Experimento de contenido](../assets/channel-experiment.png)

Una vez configurada la actividad de canal, seleccione la pestaña **[!UICONTROL Contenido]** para definir su contenido.

## Definición del contenido {#content}

Vaya a la pestaña **[!UICONTROL Contenido]** para crear el mensaje. Los pasos del proceso varían en función del canal seleccionado. Conozca los pasos detallados para crear el contenido del mensaje en las siguientes páginas.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="../../email/create-email.md"><img alt="correo electrónico" src="../../channels/assets/do-not-localize/email.png"></a><br/><a href="../../email/create-email.md"><strong>Creación de un correo electrónico</strong></a></td>
<td><a href="../../sms/create-sms.md"><img alt="SMS" src="../../channels/assets/do-not-localize/sms.png"></a><br/><a href="../../sms/create-sms.md"><strong>Creación de un SMS</strong></a></td>
<td><a href="../../push/create-push.md"><img alt="push" src="../../channels/assets/do-not-localize/push.png"></a><a href="../../push/create-push.md"><strong>Creación de una notificación push</strong></a></td>
</tr></table>

## Adición de personalización

Personalization en campañas orquestadas funciona de manera similar a otras campañas o recorridos de **[!UICONTROL Journey Optimizer]**, pero con algunas diferencias clave específicas del lienzo orquestado.

Al acceder al editor de personalización desde una campaña orquestada, dos carpetas principales contienen atributos disponibles para la personalización que se detallan a continuación.

* **[!UICONTROL Atributos de perfil]**

  Esta carpeta incluye todos los datos relacionados con el perfil de [!DNL Adobe Experience Platform]. Son atributos estándar como nombre, dirección de correo electrónico, ubicación o cualquier otro rasgo capturado en el perfil del usuario.

* **[!UICONTROL Atributos de destino]** (específicos de campañas orquestadas)

  Esta carpeta es única para las campañas orquestadas. Contiene atributos calculados directamente dentro del lienzo de la campaña. Contiene dos subcarpetas:

   * **`<Targeting dimension>`** (por ejemplo, &quot;Destinatarios&quot;, &quot;Compras&quot;): Contiene todos los atributos relacionados con la dimensión objetivo de la campaña.

   * **`Enrichment`**: incluye datos agregados mediante actividades **[!UICONTROL Enrichment]** en el lienzo. Esto le permite personalizar mensajes en función de conjuntos de datos externos o lógica adicional incorporada durante la orquestación. [Aprenda a utilizar una actividad de enriquecimiento](../activities/enrichment.md)

Para obtener información detallada sobre cómo usar el editor de personalización, consulte [Introducción a la personalización](../../personalization/personalize.md)

## Comprobación y prueba del contenido

Una vez creado el contenido, use el botón **[!UICONTROL Simular contenido]** para obtener una vista previa y probar el contenido con los perfiles de prueba o los datos de entrada de muestra cargados desde un archivo CSV/JSON, o añadidos manualmente. [Más información](../../content-management/preview-test.md)

![imagen que muestra el botón Simular contenido](../assets/channel-simulate.png)

## Próximos pasos {#next}

Cuando el contenido del mensaje esté listo, vuelva a su campaña orquestada con la flecha **[!UICONTROL Atrás]**. A continuación, puede completar la orquestación de actividades en el lienzo y publicar la campaña para iniciar el envío de mensajes. [Aprenda a iniciar y supervisar campañas orquestadas](../start-monitor-campaigns.md)

![imagen que muestra el botón Atrás](../assets/channel-back.png)

<!--
## Examples {#cross-channel-workflow-sample}

Here is a cross-channel Orchestrated campaign example with a segmentation and two deliveries. The Orchestrated campaign targets all customers who live in Paris and who are interested in coffee machines. Among this population, an email is sent to the regular customers and an SMS is sent to the VIP clients.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

<!--You can also create a recurring Orchestrated campaign to send a personalized SMS every first day of the month at 8 PM to all customers living in Paris.

![](../assets/workflow-channel-example2.png)-->

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
