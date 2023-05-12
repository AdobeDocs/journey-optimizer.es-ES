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
source-git-commit: 33dccf32b60a6afb58931823016821fc1effcbd8
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 13%

---

# Creación de un mensaje SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Creación de un mensaje SMS"
>abstract="Añada el mensaje SMS y comience a personalizarlo con el editor de expresiones."

## Añadir un mensaje SMS {#create-sms-journey-campaign}

Examine las pestañas siguientes para aprender a añadir un mensaje SMS en una campaña o un recorrido.

>[!BEGINTABS]

>[!TAB Añadir un mensaje SMS a un Recorrido]

1. Abra el recorrido y arrastre y suelte una actividad SMS desde la **Acciones** de la paleta.

   ![](assets/sms_create_1.png)

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la superficie del mensaje que desea utilizar.

   ![](assets/sms_create_2.png)

   Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md)

   La variable **[!UICONTROL Superficie]** de forma predeterminada, el campo se rellena previamente y el usuario utiliza la última superficie para ese canal.

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

1. Después de definir el contenido, puede añadir las URL de seguimiento al mensaje. Para ello, acceda al **[!UICONTROL Funciones de ayuda]** y seleccione **[!UICONTROL Ayudantes]**.

   Tenga en cuenta que para utilizar la función de acortamiento de URL, primero debe configurar un subdominio que luego se vinculará a su superficie. [Más información](sms-subdomains.md)

   >[!CAUTION]
   >
   > Para acceder y editar subdominios de SMS, debe tener la variable **[!UICONTROL Administrar subdominios de SMS]** permiso en el simulador de pruebas de producción.

   ![](assets/sms_tracking_1.png)

1. Dentro de **[!UICONTROL Funciones de ayuda]** , haga clic en **[!UICONTROL Función URL]** y, a continuación, seleccione **[!UICONTROL Agregar URL]**.

   ![](assets/sms_tracking_2.png)

1. En el `originalUrl` , pegue la dirección URL que desee abreviar.

1. Haga clic en **[!UICONTROL Guardar]** y compruebe el mensaje en la vista previa. Puede usar **[!UICONTROL Simular contenido]** para previsualizar las direcciones URL abreviadas o el contenido personalizado.

   ![](assets/sms-content-preview.png)

Ahora puede probar y enviar su mensaje SMS a su audiencia. [Más información](send-sms.md)
Una vez enviado, puede medir el impacto del SMS dentro de los informes Campaña o Recorrido . Para obtener más información sobre la creación de informes, consulte [esta sección](../reports/campaign-global-report.md#sms-tab).

>[!NOTE]
>
>De acuerdo con las normas y los reglamentos del sector, todos los mensajes SMS sobre marketing deben contener una forma para que los destinatarios puedan cancelar la suscripción fácilmente. Para ello, los destinatarios de SMS pueden responder con las palabras clave de inclusión y exclusión. [Obtenga información sobre cómo administrar la exclusión](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**Temas relacionados**

* [Previsualice, pruebe y envíe su mensaje SMS](send-sms.md)
* [Configuración del canal de SMS](sms-configuration.md)
* [Informe SMS](../reports/journey-global-report.md#sms-global)
* [Adición de un mensaje en un recorrido](../building-journeys/journeys-message.md)
* [Añadir un mensaje en una campaña](../campaigns/create-campaign.md)
