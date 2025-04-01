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
badge: label="Beta" type="Informative"
exl-id: d1f40cd8-f311-4df6-b401-8858095cef3e
source-git-commit: a40907925c7f8c783a3baf9673009a54f433b960
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 4%

---

# Introducción a la configuración de WhatsApp {#whatsapp-config}

>[!BEGINSHADEBOX]

**Tabla de contenido**

* [Introducción a los mensajes de WhatsApp](get-started-whatsapp.md)
* **[Introducción a la configuración de WhatsApp](whatsapp-configuration.md)**
* [Crear un mensaje de WhatsApp](create-whatsapp.md)
* [Comprueba y envía tus mensajes de WhatsApp](send-whatsapp.md)

>[!ENDSHADEBOX]

Antes de enviar tu mensaje de WhatsApp, debes configurar tu entorno de Adobe Journey Optimizer y asociarlo a tu cuenta de WhatsApp. Para realizar esto:

1. [Cree sus credenciales de la API de WhatsApp](#WhatsApp-credentials)
1. [Crea tu configuración de WhatsApp](#WhatsApp-configuration)

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

1. Seleccione el **número de teléfono** que utilizó para enviar sus mensajes de Whatsapp.

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

Ya estás listo para enviar mensajes de WhatsApp con Journey Optimizer.
