---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del canal de WhatsApp
description: Aprenda a configurar su entorno para enviar mensajes de WhatsApp con Journey Optimizer
feature: Whatsapp, Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: d1f40cd8-f311-4df6-b401-8858095cef3e
source-git-commit: 50a16d70fbf0c64fed64b037a5bcd14c21442c89
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 5%

---

# Introducción a la configuración de WhatsApp {#whatsapp-config}

>[!BEGINSHADEBOX]

**Tabla de contenidos**

* [Introducción a los mensajes de WhatsApp](get-started-whatsapp.md)
* **[Introducción a la configuración de WhatsApp](whatsapp-configuration.md)**
* [Creación de un mensaje de WhatsApp](create-whatsapp.md)
* [Comprobación y envío de los mensajes de WhatsApp](send-whatsapp.md)

>[!ENDSHADEBOX]

Antes de enviar tu mensaje de WhatsApp, debes configurar tu entorno de Adobe Journey Optimizer y asociarlo a tu cuenta de WhatsApp. Para realizar esto:

1. [Cree sus credenciales de la API de WhatsApp](#WhatsApp-credentials)
1. [Crea tu configuración de WhatsApp](#WhatsApp-configuration)
1. [Crea tus webhooks de WhatsApp](#WhatsApp-webhook)


Estos pasos debe realizarlos un administrador del sistema [de Adobe Journey Optimizer](../start/path/administrator.md).

## Crear credenciales de API de WhatsApp {#whatsapp-credentials}

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** `>` **[!UICONTROL Canales]** y seleccione el menú **[!UICONTROL Credenciales de API]**. Haga clic en el botón **[!UICONTROL Crear nuevas credenciales de API]**.

1. Configure las credenciales de la API como se detalla a continuación:

   * **Token de API**: escriba el token de API. Obtenga más información en [Documentación de metadatos](https://developers.facebook.com/docs/facebook-login/guides/access-tokens/)
   * **ID de cuenta empresarial**: escriba el número único relacionado con su portafolio empresarial. Obtenga más información en [Documentación de metadatos](https://www.facebook.com/business/help/1181250022022158?id=180505742745347).

   ![](assets/whatsapp-api.png)

1. Haga clic en **[!UICONTROL Continuar]**.

1. Elija la **cuenta empresarial** a la que desea conectarse con sus credenciales de la API de WhatsApp.

   ![](assets/whatsapp-api-2.png)

1. Seleccione el **nombre del remitente** que se utilizó para enviar sus mensajes de Whatsapp.

1. La configuración de tu número de teléfono se completa automáticamente:

   * **Clasificación de calidad**: refleja los comentarios de los clientes sobre los mensajes enviados en las últimas 24 horas.
      * Verde: alta calidad
      * Amarillo: calidad Medium
      * Rojo: baja calidad

     Más información sobre [Clasificación de calidad](https://www.facebook.com/business/help/766346674749731#)

   * **Rendimiento**: indica la velocidad a la que su número de teléfono puede enviar mensajes.

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar las credenciales de la API.

Después de crear y configurar las credenciales de la API, debe crear una configuración de canal para los mensajes de WhatsApp. [Más información](#whatsapp-configuration)

## Crear configuración de WhatsApp {#whatsapp-configuration}

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** y seleccione **[!UICONTROL Configuración general]** > **[!UICONTROL Configuraciones de canal]**. Haga clic en el botón **[!UICONTROL Crear configuración de canal]**.

   ![](assets/whatsapp-config-1.png)

1. Introduzca un nombre y una descripción (opcional) para la configuración y, a continuación, seleccione el canal de WhatsApp.

   >[!NOTE]
   >
   > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos. También puede utilizar caracteres de guion bajo `_`, punto `.` y guion `-`.

1. Seleccione **[!DNL WhatsApp]** como su canal.

   ![](assets/whatsapp-config-2.png)

1. Seleccione **[!UICONTROL Acciones de marketing]** para asociar directivas de consentimiento a los mensajes que usan esta configuración. Todas las políticas de consentimiento asociadas con la acción de marketing se aprovechan para respetar las preferencias de los clientes. Más información

1. Seleccione la **[!UICONTROL configuración de la API de WhatsApp]** creada anteriormente.

   ![](assets/whatsapp-config-3.png)

1. Escriba el **[!UICONTROL número de remitente]** &#x200B;que desee usar para sus comunicaciones.

1. Una vez configurados todos los parámetros, haga clic en **[!UICONTROL Enviar]** para confirmar. También puede guardar la configuración de canal como borrador y reanudarla más adelante.

1. Una vez creada la configuración del canal, se muestra en la lista con el estado **[!UICONTROL Procesando]**.

   >[!NOTE]
   >
   >Si las comprobaciones no se realizan correctamente, obtenga más información sobre los posibles motivos de error en [esta sección](../configuration/channel-surfaces.md).

1. Una vez que las comprobaciones son correctas, la configuración del canal obtiene el estado **[!UICONTROL Activo]**. Está listo para utilizarse para enviar mensajes.

## Crear webhook {#WhatsApp-webhook}

>[!NOTE]
>
>Sin las palabras clave de inclusión u exclusión especificadas, no se habilitan los mensajes de consentimiento estándar.

Una vez que tus credenciales de la API de WhatsApp y tus [Webhooks Meta](https://developers.facebook.com/docs/whatsapp/webhooks/) se hayan creado correctamente, el siguiente paso es crear un webhook y configurar tu configuración de entrada.

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** `>` **[!UICONTROL Canales]**, seleccione el menú **[!UICONTROL Webhooks de WhatsApp]** en **[!UICONTROL Configuración de WhatsApp]** y haga clic en el botón **[!UICONTROL Crear webhook]**.

1. Escribe un [!UICONTROL Nombre] para tu webhook.

1. En la lista desplegable, seleccione la [configuración](#whatsapp-configuration) que creó anteriormente.

1. Haga clic en ![agregar](assets/do-not-localize/Smock_AddCircle_18_N.svg) para comenzar a configurar una **[!UICONTROL categoría de palabras clave de entrada]** como:

   * **[!UICONTROL Palabras clave de inclusión]**
   * **[!UICONTROL Palabras clave de exclusión]**
   * **[!UICONTROL Palabras clave de ayuda]**

1. Escriba su **[!UICONTROL palabra clave]**.

   Para agregar varias palabras clave, haga clic en ![agregar](assets/do-not-localize/Smock_AddCircle_18_N.svg).

1. Especifique el **[!UICONTROL mensaje de respuesta]** que se enviará cuando se reciba una palabra clave configurada.

<!--
1. Click **[!UICONTROL View payload editor]** to validate and customize your request payloads. 
    
    You can dynamically personalize your payload using profile attributes, and ensure accurate data is sent for processing and response generation with the help of built-in helper functions.
-->

1. Haz clic en **[!UICONTROL Enviar]** cuando hayas terminado la configuración de tu webhook de WhatsApp.

1. En el menú de **[!UICONTROL Webhooks]**, haz clic en el ![icono bin](assets/do-not-localize/Smock_Delete_18_N.svg) para eliminar tu webhook de WhatsApp.

1. Para modificar la configuración existente, busque el webhook deseado y haga clic en la opción **[!UICONTROL Editar]** para realizar los cambios necesarios.

1. Accede y copia tu nueva **[!UICONTROL URL de webhook]** desde tu **[!UICONTROL webhook de WhatsApp]** enviado anteriormente.

Una vez configuradas, puede aprovechar todas las funcionalidades de canal integradas, como la creación de mensajes, la personalización, el seguimiento de vínculos y la creación de informes.

Ya estás listo para enviar mensajes de WhatsApp con Journey Optimizer.
