---
solution: Journey Optimizer
product: journey optimizer
title: Creación de un mensaje de WhatsApp
description: Aprenda a crear un mensaje de WhatsApp en Journey Optimizer
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: cac6f675-59e0-431d-8c20-f24ef16d7bf2
source-git-commit: 7f507dc0113e85191429c2c48b873112b590e3ce
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 7%

---


# Creación de un mensaje de WhatsApp {#create-whatsapp}

>[!BEGINSHADEBOX]

**Tabla de contenidos**

* [Introducción a los mensajes de WhatsApp](get-started-whatsapp.md)
* [Introducción a la configuración de WhatsApp](whatsapp-configuration.md)
* **[Crear un mensaje de WhatsApp](create-whatsapp.md)**
* [Comprobación y envío de los mensajes de WhatsApp](send-whatsapp.md)

>[!ENDSHADEBOX]

Con Adobe Journey Optimizer, puedes diseñar y enviar mensajes atractivos en WhatsApp. Simplemente agrega una acción de WhatsApp a tu recorrido o campaña y crea el contenido del mensaje como se detalla a continuación. Adobe Journey Optimizer también le permite probar sus mensajes de WhatsApp antes de enviarlos, lo que garantiza un procesamiento perfecto, una personalización precisa y una configuración adecuada de todos los ajustes.

Tenga en cuenta que solo se admiten los elementos de mensajes salientes en Journey Optimizer.

+++ Obtenga más información sobre los elementos de mensaje admitidos y las llamadas a la acción

WhatsApp admite los siguientes tipos de mensajes:

| Función de mensaje | Descripción |
|-|-|
| Encabezados | Texto opcional que aparece encima del cuerpo del mensaje. |
| Texto | Admite contenido dinámico mediante parámetros. |
| Imágenes (JPEG, PNG) | Debe tener un formato RGB o RGBA de 8 bits y un tamaño inferior a 5 MB. |
| Vídeos | Debe ser 3GPP o MP4, de menos de 16 MB y alojado mediante URL. |
| Audio | Solo disponible para mensajes de respuesta. Debe tener el formato AAC, AMR, MP3, MP4 audio u OGG, alojado en una dirección URL y inferior a 16 MB. |
| Documentos | Debe tener menos de 100 MB, estar alojado en una dirección URL y tener uno de los siguientes formatos: .txt, .xls/.xlsx, .doc/.docx, .ppt/.pptx o .pdf. |
| Texto del cuerpo | Admite contenido dinámico mediante parámetros. |
| Texto del pie | Admite contenido dinámico mediante parámetros. |

La siguiente opción de call-to-action está disponible para tus mensajes de WhatsApp:

| Llamadas a la acción | Descripción |
|-|-|
| Visitar sitio web | Solo se permite un botón, con parámetros de variable incluidos. |


+++

## Añadir un mensaje de WhatsApp {#create-whatsapp-journey-campaign}

Examine las pestañas a continuación para aprender a añadir un mensaje de WhatsApp en una campaña o un recorrido.

>[!BEGINTABS]

>[!TAB Agregar un mensaje de WhatsApp a un Recorrido]

1. Abra el recorrido y arrastre y suelte una **actividad WhatsApp** desde la sección **Acciones** de la paleta.

   ![](assets/whatsapp-create-jo.png)

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la configuración de mensaje que desea utilizar.

   Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md)

   El campo **[!UICONTROL configuration]** está rellenado previamente de forma predeterminada con la última configuración que el usuario usó para ese canal.

Ahora puedes empezar a diseñar el contenido de tu mensaje de WhatsApp desde el botón **[!UICONTROL Editar contenido]**, como se detalla a continuación.

>[!TAB Agregar un mensaje de WhatsApp a una campaña]

1. Acceda al menú **[!UICONTROL Campañas]** y haga clic en **[!UICONTROL Crear campaña]**.

1. Seleccione el tipo de campaña **Programada - Marketing**.

1. En la sección **[!UICONTROL Propiedades]**, edite el **[!UICONTROL Título]** y la **[!UICONTROL Descripción]** de su campaña.

1. Haga clic en el botón **[!UICONTROL Seleccionar audiencia]** para definir la audiencia a la que se dirigirá desde la lista de audiencias de Adobe Experience Platform disponibles. [Más información](../audience/about-audiences.md).

1. En el campo **[!UICONTROL Área de nombres de identidad]**, elija el área de nombres que desea usar para identificar a los individuos de la audiencia seleccionada. [Más información](../event/about-creating.md#select-the-namespace).

1. En la sección **[!UICONTROL Acciones]**, elige **[!UICONTROL WhatsApp]** y selecciona o crea una nueva configuración.

   Más información sobre la configuración de WhatsApp en [esta página](whatsapp-configuration.md).

   ![](assets/whatsapp-campaign-1.png)

1. Haga clic en **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido y crear tratamientos para medir su rendimiento e identificar la mejor opción para la audiencia objetivo. [Más información](../content-management/content-experiment.md)

1. En la sección **[!UICONTROL Seguimiento de acciones]**, especifica si deseas rastrear los clics en los vínculos de tu mensaje de WhatsApp.

1. Las campañas están diseñadas para ejecutarse en una fecha específica o en una frecuencia recurrente. Aprenda a configurar la **[!UICONTROL programación]** de su campaña en [esta sección](../campaigns/create-campaign.md#schedule).

1. En el menú **[!UICONTROL déclencheur de acción]**, elige la **[!UICONTROL Frecuencia]** de tu mensaje de WhatsApp:

   * Una vez
   * Diaria
   * Semanal
   * Mes

Ahora puedes empezar a diseñar el contenido de tu mensaje de WhatsApp desde el botón **[!UICONTROL Editar contenido]**, como se detalla a continuación.

>[!ENDTABS]

## Definición del contenido de WhatsApp{#whatsapp-content}

>[!BEGINSHADEBOX]

Antes de diseñar tu mensaje de WhatsApp en Journey Optimizer, primero debes crear y diseñar tu plantilla en Meta. [Más información](https://www.facebook.com/business/help/2055875911147364?id=2129163877102343)

Ten en cuenta que tu plantilla de WhatsApp primero debe ser aprobada por Meta antes de usarla en Journey Optimizer. Este proceso suele durar unas pocas horas, pero puede tardar hasta 24 horas. [Más información](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/#approval-process)

>[!ENDSHADEBOX]

1. En la pantalla de configuración del recorrido o la campaña, haz clic en el botón **[!UICONTROL Editar contenido]** para configurar el contenido del mensaje de WhatsApp.

<!--
1. Select **[!UICONTROL Template message]**.
-->

1. Elija su **categoría de plantilla**:

   * Marketing
   * Utilidad
   * Autenticación

   [Más información sobre las categorías de plantillas](https://developers.facebook.com/docs/whatsapp/updates-to-pricing/new-template-guidelines/#template-category-guidelines)

   ![](assets/whatsapp-design-1.png)

1. En el menú desplegable **Plantilla de WhatsApp**, selecciona la plantilla creada anteriormente y diseñada en Meta.

   [Más información sobre cómo crear tus plantillas de Whatsapp](https://www.facebook.com/business/help/2055875911147364?id=2129163877102343)

   ![](assets/whatsapp-design-2.png)

1. Utilice el editor de personalización para añadir personalización a la plantilla. Puede utilizar cualquier atributo, como el nombre del perfil o la ciudad, por ejemplo.

   Navegue por la siguiente página para obtener más información sobre [personalización](../personalization/personalize.md).

   ![](assets/whatsapp-design-3.png)

1. Usa el botón **[!UICONTROL Simular contenido]** para obtener una vista previa del contenido de tu mensaje de WhatsApp, las URL abreviadas y el contenido personalizado. [Más información](send-whatsapp.md)

Una vez que hayas realizado las pruebas y validado el contenido, puedes [enviar tu mensaje de WhatsApp](send-whatsapp.md) a tu audiencia y monitorizar su rendimiento a través de [informes](../reports/campaign-global-report-cja.md).

<!--
* **[!UICONTROL Template message]**: Predefined message imported from Meta into Journey Optimizer. These are intended for sending notifications, alerts, or updates to your customers.

* **[!UICONTROL Response message]**: Message created in Journey Optimizer and sent in reply to customer queries or interactions.

>[!BEGINTABS]

>[!TAB Template message]

1. From the journey or campaign configuration screen, click the **[!UICONTROL Edit content]** button to configure the WhatsApp message content.

1. Select **[!UICONTROL Template message]**.

1. Choose your Template category. [Learn more](https://developers.facebook.com/docs/WhatsApp/updates-to-pricing/new-template-guidelines/)

1. From the **WhatsApp template** drop-down, select your previously created template designed in Meta.

1. Use the personalization editor to define content, add personalization and dynamic content. You can use any attribute, such as the profile name or city for example. You can also define conditional rules. Browse to the following pages to learn more about [personalization](../personalization/personalize.md) and [dynamic content](../personalization/get-started-dynamic-content.md) in the personalization editor.

1. Use the **[!UICONTROL Simulate content]** button to preview your WhatsApp message content, shortened URLs, and personalized content. [Learn more](send-whatsapp.md)

Once you have performed your tests and validated the content, you can send your WhatsApp message to your audience. These steps are detailed on [this page](send-whatsapp.md)

>[!TAB Response message]

1. From the journey or campaign configuration screen, click the **[!UICONTROL Edit content]** button to configure the WhatsApp message content.

1. Select **[!UICONTROL Response message]**.

1. Enter your text in the **[!UICONTROL Body]** field.

1. Use the personalization editor to define content, add personalization and dynamic content. You can use any attribute, such as the profile name or city for example. You can also define conditional rules. Browse to the following pages to learn more about [personalization](../personalization/personalize.md) and [dynamic content](../personalization/get-started-dynamic-content.md) in the personalization editor.

1. Use the **[!UICONTROL Simulate content]** button to preview your WhatsApp message content, shortened URLs, and personalized content. [Learn more](send-whatsapp.md)

Once you have performed your tests and validated the content, you can send your WhatsApp message to your audience. These steps are detailed on [this page](send-whatsapp.md)

>[!ENDTABS]
-->
