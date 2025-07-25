---
solution: Journey Optimizer
product: journey optimizer
title: Cree su dimensión de segmentación
description: Obtenga información sobre cómo asignar un esquema relacional al perfil del cliente
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 0abe441a413b748b46379871f3b70842715921a3
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 11%

---


# Configuración de una dimensión de segmentación {#configuration}

+++ Índice

| Bienvenido a las campañas organizadas | Inicio de su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md)<br/><br/>[Configurar una dimensión de Target](target-dimension.md) | <b>[Creación y programación de las campañas](create-orchestrated-campaign.md)</b><br/><br/>[Organización de actividades](orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabajo con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](build-query.md)<br/><br/>[Edición de expresiones](edit-expressions.md)<br/><br/>[Resegmentación](retarget.md) | [Introducción a las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[AND-join](activities/and-join.md) - [Generar público](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades del canal](activities/channels.md) - [Combinar](activities/combine.md) - [Deduplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar público](activities/save-audience.md) - [División](activities/split.md) - [Esperar](activities/wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

En muchos casos, un solo perfil de cliente se puede vincular a varias entidades relacionadas, como suscripciones, contratos de servicio o dispositivos, cada uno con su propio identificador único y necesidades de comunicación.

Con **Campañas orquestadas**, ahora puede diseñar y enviar comunicaciones de destino en el nivel de entidad mediante las **funciones de esquema relacional de Adobe Experience Platform**. Esto le permite segmentar, personalizar e informar por entidad en lugar de por destinatario.

## Cree su dimensión de segmentación {#targeting-dimension}

Un único perfil de cliente se puede asociar con varias entidades relacionadas, como contratos, dispositivos o suscripciones, cada una con su propio identificador único. Esta configuración le permite establecer como objetivo, segmentar e informar sobre cada entidad individualmente.

Comience por configurar la orquestación de campañas asignando un esquema relacional al perfil del cliente.

1. Desde **[!UICONTROL Administration]**, acceda al menú **[!UICONTROL Configurations]** y seleccione **[!UICONTROL Campaign Target Dimension]**.

   ![](assets/target-dimension-1.png)

1. Haga clic en **[!UICONTROL Crear]** para empezar a crear su **[!UICONTROL dimensión de segmentación]**.

1. Elija su [esquema](gs-schemas.md) configurado previamente &#x200B;de la lista desplegable.

1. Seleccione el **[!UICONTROL valor de identidad]** que representa la entidad a la que desea destinar.

   En este ejemplo, el perfil del cliente está vinculado a varias suscripciones, cada una representada por un único `crmID` en el esquema `Recipient`. Al configurar **[!UICONTROL Target Dimension]** para que use el esquema `Recipient` y su identidad `crmID`, puede enviar mensajes en el nivel de suscripción, en lugar de al perfil de cliente principal, asegurándose de que cada contrato o línea reciba su propio mensaje personalizado.

   [Más información en la documentación de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/schema/composition#identity).

   ![](assets/target-dimension-2.png)

1. Haga clic en **[!UICONTROL Guardar]** para completar la configuración.

Después de configurar **[!UICONTROL Target Dimension]**, proceda a crear y configurar su **[!UICONTROL configuración de canal]** y defina los **[!UICONTROL detalles de ejecución]** correspondientes.

## Configure su configuración de canal {#channel-configuration}

Después de configurar tu **[!UICONTROL Dimension de Target]**, debes configurar tu correo electrónico o SMS **[!UICONTROL Configuración del canal]** y definir los **[!UICONTROL Detalles de ejecución]** adecuados. Esto garantiza que los mensajes se envíen con la identidad y la lógica de segmentación correctas.

1. Comience creando y configurando su **[!UICONTROL configuración de canal]**.

   También puede actualizar una **[!UICONTROL configuración de canal]** existente.

   ➡️ [Siga los pasos detallados en esta página](../email/surface-personalization.md)

1. Desde la sección **[!UICONTROL Detalles de ejecución]** de tu **[!UICONTROL configuración de canal]**, accede a la pestaña **[!UICONTROL Campañas orquestadas]**.

   ![](assets/target-dimension-3.png)

1. Haga clic en **[!UICONTROL Habilitado]** para que sea compatible con campañas orquestadas.

1. Elija el método de entrega:

   * **[!UICONTROL Target Dimension]**: enviar a la entidad principal; por ejemplo, destinatario.

   * **[!UICONTROL Target + Dimension secundario]**: envíe utilizando entidades primarias y secundarias; por ejemplo, destinatario + contrato.

1. Seleccione en la lista desplegable su [Dimension de Target creado anteriormente](#targeting-dimension).

   ![](assets/target-dimension-4.png)

1. En la sección **[!UICONTROL Dirección de ejecución]**, elija qué **[!UICONTROL Source]** se debe usar para obtener la dirección de entrega, como la dirección de correo electrónico o el número de teléfono:

   * **[!UICONTROL Perfil]**: seleccione esta opción si la dirección de envío, por ejemplo: correo electrónico, se almacena directamente en el perfil principal del cliente.

     Resulta útil al enviar mensajes al cliente principal, no a una entidad asociada específica.

   * **[!UICONTROL Target Dimension]**: elija esta opción si la dirección de envío está almacenada en la entidad relacionada, por ejemplo, un destinatario o una suscripción.

     Resulta útil cuando cada destinatario tiene su propia dirección de envío, como un correo electrónico o un número de teléfono diferentes.

1. En el campo **[!UICONTROL Dirección de entrega]**, haga clic en ![icono de edición](assets/do-not-localize/edit.svg) para elegir el campo específico que se usará para la entrega de mensajes.

   ![](assets/target-dimension-4.png)

1. Una vez configurada, haga clic en **[!UICONTROL Enviar]**.

El canal está listo para usarse con **Campañas orquestadas**, y los mensajes se enviarán de acuerdo con la dimensión de destino seleccionada.
