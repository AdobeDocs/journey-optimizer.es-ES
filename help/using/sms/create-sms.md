---
solution: Journey Optimizer
product: journey optimizer
title: Creación de un mensaje SMS/MMS
description: Obtenga información sobre cómo crear un mensaje SMS/MMS en Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 227cdb77b0db40c59fa089789c444c2364fd062e
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 4%

---

# Creación de un mensaje de texto (SMS/MMS){#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Creación de un mensaje de texto"
>abstract="Para crear un mensaje de texto (SMS/MMS), añada una acción SMS en un recorrido o una campaña y comience a personalizarla con el editor de expresiones."

Puede diseñar y enviar mensajes de texto (SMS) y multimedia (MMS) con Adobe Journey Optimizer. Primero debe agregar una acción SMS en un recorrido o una campaña y luego definir el contenido del mensaje de texto, como se detalla a continuación. Adobe Journey Optimizer también ofrece funciones para probar los mensajes de texto antes de enviarlos, de modo que pueda comprobar el procesamiento, los atributos de personalización y todos los demás ajustes.

>[!NOTE]
>
>De acuerdo con las normas y regulaciones del sector, todos los mensajes de marketing SMS/MMS deben contener una forma para que los destinatarios puedan cancelar la suscripción fácilmente. Para ello, los destinatarios de SMS pueden responder con las palabras clave de inclusión y exclusión. [Obtenga información sobre cómo administrar la exclusión](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)


## Añadir un mensaje de texto {#create-sms-journey-campaign}

Examine las pestañas siguientes para aprender a añadir un mensaje de texto (SMS/MMS) en una campaña o un recorrido.

>[!BEGINTABS]

>[!TAB Añadir un mensaje de texto a un Recorrido]

1. Abra el recorrido y arrastre y suelte una actividad SMS desde el **Acciones** de la paleta.

   ![](assets/sms_create_1.png)

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la superficie de mensaje que desea utilizar.

   ![](assets/sms_create_2.png)

   Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md)

   El **[!UICONTROL Superficie]** de forma predeterminada, el campo está rellenado previamente con la última superficie que el usuario utilizó para ese canal.

Ahora puede empezar a diseñar el contenido de su mensaje SMS desde el **[!UICONTROL Editar contenido]** , como se detalla a continuación.

>[!TAB Adición de un mensaje de texto a una campaña]

1. Cree una nueva campaña programada o activada por API, seleccione **[!UICONTROL SMS]** como su acción y elija la **[!UICONTROL Superficie de aplicación]** para usar. Obtenga más información acerca de la configuración de SMS en [esta página](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. Haga clic en **[!UICONTROL Crear]**.

1. Desde el **[!UICONTROL Propiedades]** , edite el de la campaña **[!UICONTROL Título]** y **[!UICONTROL Descripción]**.

   ![](assets/sms_create_4.png)

1. Haga clic en **[!UICONTROL Seleccionar audiencia]** para definir la audiencia de destino a partir de la lista de audiencias de Adobe Experience Platform disponibles. [Más información](../audience/about-audiences.md).

1. En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a los individuos de la audiencia seleccionada. [Más información](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. Clic **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido y crear tratamientos para medir su rendimiento e identificar la mejor opción para la audiencia de destino. [Más información](../campaigns/content-experiment.md)

1. En el **[!UICONTROL Seguimiento de acciones]** , especifique si desea rastrear los clics en los vínculos del mensaje SMS.

1. Las campañas están diseñadas para ejecutarse en una fecha específica o en una frecuencia recurrente. Obtenga información sobre cómo configurar el **[!UICONTROL Programación]** de la campaña en [esta sección](../campaigns/create-campaign.md#schedule).

1. Desde el **[!UICONTROL Déclencheur de acción]** , seleccione la opción **[!UICONTROL Frecuencia]** del mensaje SMS:

   * Una
   * Diario
   * Semanal
   * Mes

Ahora puede empezar a diseñar el contenido del mensaje de texto desde el **[!UICONTROL Editar contenido]** , como se detalla a continuación.

>[!ENDTABS]

## Definición del contenido de los SMS{#sms-content}

>[!CONTEXTUALHELP]
>id="ajo_message_sms_content"
>title="Definición del contenido de los SMS"
>abstract="Personalice y personalice sus mensajes de texto (SMS/MMS) mediante el Editor de expresiones para definir el contenido e incorporar elementos dinámicos."

Para configurar el contenido del SMS, siga los pasos a continuación. La configuración de MMS se detalla en [esta sección](#mms-content).

1. En la pantalla de configuración del recorrido o la campaña, haga clic en **[!UICONTROL Editar contenido]** para configurar el contenido del mensaje de texto.

1. Haga clic en **[!UICONTROL Mensaje]** para abrir el Editor de expresiones.

   ![](assets/sms-content.png)

1. Utilice el Editor de expresiones para definir contenido, añadir personalización y contenido dinámico. Puede utilizar cualquier atributo, como el nombre del perfil o la ciudad, por ejemplo. También puede definir reglas condicionales. Vaya a las páginas siguientes para obtener más información sobre [personalización](../personalization/personalize.md) y [contenido dinámico](../personalization/get-started-dynamic-content.md) en el Editor de expresiones.

1. Después de definir el contenido, puede agregar direcciones URL rastreadas al mensaje. Para ello, acceda al **[!UICONTROL Funciones de ayuda]** y seleccione **[!UICONTROL Ayudantes]**.

   Tenga en cuenta que para utilizar la función de acortamiento de URL, primero debe configurar un subdominio que luego se vinculará a la superficie. [Más información](sms-subdomains.md)

   >[!CAUTION]
   >
   > Para acceder y editar subdominios SMS, debe tener los siguientes **[!UICONTROL Administrar subdominios de SMS]** en la zona protegida de producción. Puede obtener más información sobre permisos en [esta sección](../administration/high-low-permissions.md).

   ![](assets/sms_tracking_1.png)

1. Dentro de **[!UICONTROL Funciones de ayuda]** , haga clic en **[!UICONTROL Función URL]** y luego seleccione **[!UICONTROL Añadir URL]**.

   ![](assets/sms_tracking_2.png)

1. En el `originalUrl` , pegue la dirección URL que desee acortar y haga clic en **[!UICONTROL Guardar]**.

1. Clic **[!UICONTROL Guardar]** y compruebe el mensaje en la vista previa. Ahora puede probar y comprobar el contenido del mensaje como se detalla en [esta sección](#sms-mms-test).


## Definición del contenido de MMS{#mms-content}

Puede mejorar su comunicación enviando mensajes del Servicio de mensajes multimedia (MMS), lo que permite compartir contenidos como vídeos, imágenes, clips de audio y GIF, etc. Además, el MMS admite hasta 1600 caracteres de texto en el mensaje.


>[!NOTE]
>
>* Esta función está disponible actualmente con **Sinch** solo.
>
>* El canal MMS incluye algunas limitaciones enumeradas en [esta página](../start/guardrails.md#sms-guardrails).
>

Para crear contenido MMS, siga estos pasos:

1. Cree un SMS como se describe en [esta sección](#create-sms-journey-campaign).

1. Edite su contenido SMS como se detalla en [esta sección](#sms-content).

1. Habilite la opción MMS para añadir contenido multimedia al contenido de SMS.

   ![](assets/sms_create_6.png)

1. Añadir un **[!UICONTROL Título]** a sus medios.

1. Introduzca la URL del contenido en la **[!UICONTROL Medios]** field.

   ![](assets/sms_create_7.png)

1. Clic **[!UICONTROL Guardar]** y compruebe el mensaje en la vista previa. Ahora puede probar y comprobar el contenido del mensaje como se detalla a continuación.

## Prueba y envío de mensajes {#sms-mms-test}

Utilice el **[!UICONTROL Simular contenido]** para obtener una vista previa del contenido del mensaje de texto, las direcciones URL abreviadas y el contenido personalizado.

![](assets/sms-content-preview.png)

Una vez que haya realizado las pruebas y validado el contenido, puede enviar el mensaje de texto a la audiencia. Estos pasos se detallan en [esta página](send-sms.md)

Una vez enviado, puede medir el impacto de su SMS dentro de los informes de Campaña o Recorrido. Para obtener más información sobre la creación de informes, consulte [esta sección](../reports/campaign-global-report.md#sms-tab).

**Temas relacionados**

* [Previsualización, prueba y envío del mensaje de texto](send-sms.md)
* [Configuración del canal de SMS](sms-configuration.md)
* [Informes de SMS/MMS](../reports/journey-global-report.md#sms-global)
* [Añadir un mensaje en un recorrido](../building-journeys/journeys-message.md)
* [Añadir un mensaje en una campaña](../campaigns/create-campaign.md)
