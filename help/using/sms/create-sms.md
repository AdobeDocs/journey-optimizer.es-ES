---
solution: Journey Optimizer
product: journey optimizer
title: Creación de un mensaje SMS
description: Obtenga información sobre cómo crear un mensaje SMS en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 13%

---

# Creación de un mensaje SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Creación de un mensaje SMS"
>abstract="Añada el mensaje SMS y comience a personalizarlo con el editor de expresiones."

## Añadir un mensaje SMS {#create-sms-journey-campaign}

Examine las pestañas siguientes para aprender a añadir un SMS en una campaña o en un recorrido.

>[!BEGINTABS]

>[!TAB Añadir un mensaje SMS a un Recorrido]

1. Abra el recorrido y arrastre y suelte una actividad SMS desde la **Acciones** de la paleta.

   ![](assets/sms_create_1.png)

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la superficie del mensaje que desea utilizar.

   ![](assets/sms_create_2.png)

   Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md)

Ahora puede empezar a diseñar el contenido de su mensaje SMS desde el **[!UICONTROL Editar contenido]** botón. [Definir el contenido del SMS](#sms-content)

>[!TAB Añadir un mensaje SMS a una campaña]

1. Cree una nueva campaña programada o activada por la API, seleccione **[!UICONTROL SMS]** como su acción y elija el **[!UICONTROL Superficie de la aplicación]** para usar. [Más información sobre la configuración de SMS](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. Haga clic en **[!UICONTROL Crear]**.

1. En el **[!UICONTROL Propiedades]** , edite la **[!UICONTROL Título]** y **[!UICONTROL Descripción]**.

   ![](assets/sms_create_4.png)

1. En el **[!UICONTROL Seguimiento de acciones]** , especifique si desea rastrear los clics en los vínculos de su mensaje SMS.

1. Haga clic en el **[!UICONTROL Seleccionar la audiencia]** para definir la audiencia a la que se dirigirá desde la lista de segmentos de Adobe Experience Platform disponibles. [Más información](../segment/about-segments.md).

1. En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado. [Más información](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. Las campañas están diseñadas para ejecutarse en una fecha específica o con una frecuencia recurrente. Obtenga información sobre cómo configurar la variable **[!UICONTROL Programación]** de su campaña en [esta sección](../campaigns/create-campaign.md#schedule).

1. En el **[!UICONTROL Déclencheur de acción]** , seleccione **[!UICONTROL Frecuencia]** de su mensaje SMS:

   * Una vez
   * Diario
   * Semanal
   * Mes

Ahora puede empezar a diseñar el contenido de su mensaje SMS desde el **[!UICONTROL Editar contenido]** botón. [Diseño del contenido de SMS](#sms-content)

>[!ENDTABS]


## Definir el contenido del SMS{#sms-content}

1. En la pantalla de configuración de recorrido o de campaña, haga clic en el botón **[!UICONTROL Editar contenido]** para configurar el contenido del SMS.

1. Haga clic en el **[!UICONTROL Mensaje]** para abrir el editor de expresiones.

   ![](assets/sms-content.png)

1. Utilice el editor de expresiones para definir contenido y añadir contenido dinámico. Puede utilizar cualquier atributo, como el nombre del perfil o la ciudad. Más información sobre [personalización](../personalization/personalize.md) y [contenido dinámico](../personalization/get-started-dynamic-content.md) en el editor de expresiones.

1. Haga clic en **[!UICONTROL Guardar]** y compruebe el mensaje en la vista previa. [Más información](send-sms.md)

   ![](assets/sms-content-preview.png)

>[!NOTE]
>
>De acuerdo con las normas y los reglamentos del sector, todos los mensajes SMS sobre marketing deben contener una forma para que los destinatarios puedan cancelar la suscripción fácilmente. Para ello, los destinatarios de SMS pueden responder con las palabras clave de inclusión y exclusión. [Obtenga información sobre cómo administrar la exclusión](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**Temas relacionados**

* [Configuración del canal de SMS](sms-configuration.md)
* [Informe SMS](../reports/journey-global-report.md#sms-global)
* [Adición de un mensaje en un recorrido](../building-journeys/journeys-message.md)
* [Añadir un mensaje en una campaña](../campaigns/create-campaign.md)
