---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del proveedor Sinch
description: Aprenda a configurar su entorno para enviar mensajes de texto con Journey Optimizer con Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 794ac45177e467be4bd5b8f7288e07c85e4d806a
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 3%

---

# Configuración del proveedor Sinch {#sms-configuration-sinch}

Al utilizar el proveedor de Sinch con Journey Optimizer, puede encontrar dos opciones distintas:

* **Configuración de SMS**: configura tus credenciales de la API de Sinch para enviar mensajes SMS sin problemas.

* **Configuración de MMS**: para la mensajería multimedia (MMS), configure sus credenciales de API de MMS de Sinch. Tenga en cuenta que el seguimiento y la respuesta a los mensajes entrantes se gestionan mediante la configuración de SMS. La configuración de MMS solo es para la entrega saliente del mensaje MMS.

## Credenciales de API de Sinch{#create-api}

Para configurar su proveedor de Sinch para que envíe mensajes SMS y MMS con Journey Optimizer, siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** y seleccione el menú **[!UICONTROL Credenciales de API]**. Haga clic en el botón **[!UICONTROL Crear nuevas credenciales de API]**.

1. Configure las credenciales de la API de SMS como se detalla a continuación:

   * **[!UICONTROL Proveedor de SMS]**: Sinch.

   * **[!UICONTROL Nombre]**: elige un nombre para tu credencial de API.

   * **[!UICONTROL ID de servicio]** y **[!UICONTROL token de API]**: para acceder a la página de API, puede encontrar sus credenciales en la pestaña SMS. Obtenga más información en [Documentación de Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

   * **[!UICONTROL Palabras clave de inclusión]**: escriba las palabras clave predeterminadas o personalizadas que almacenarán en déclencheur automáticamente su **[!UICONTROL mensaje de inclusión]**. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de inclusión]**: escriba la respuesta personalizada que se enviará automáticamente como **[!UICONTROL Mensaje de inclusión]**.

   * **[!UICONTROL Palabras clave de exclusión]**: escriba las palabras clave predeterminadas o personalizadas que almacenarán en déclencheur automáticamente su **[!UICONTROL mensaje de exclusión]**. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de exclusión]**: escriba la respuesta personalizada que se enviará automáticamente como **[!UICONTROL Mensaje de exclusión]**.

   * **[!UICONTROL Palabras clave de ayuda]**: escribe las palabras clave predeterminadas o personalizadas que almacenarán automáticamente en déclencheur tu **mensaje de ayuda**. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de ayuda]**: escriba la respuesta personalizada que se enviará automáticamente como **Mensaje de ayuda**.

   * **[!UICONTROL Palabras clave de inclusión doble]**: escriba las palabras clave que almacenan en déclencheur el proceso de inclusión doble. Si no existe ningún perfil de usuario, se crea tras una confirmación correcta. Para varias palabras clave, utilice valores separados por comas. [Más información sobre la inclusión doble de SMS](https://video.tv.adobe.com/v/3427129/?learn=on).

   * **[!UICONTROL Mensaje de inclusión doble]**: escriba la respuesta personalizada que se enviará automáticamente en respuesta a la confirmación de inclusión doble.

   * **[!UICONTROL Número de entrada]**: agrega tu número de entrada único. Esto le permite utilizar las mismas credenciales de API en diferentes zonas protegidas, cada una con su propio número de entrada.

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar las credenciales de la API.

Después de crear y configurar las credenciales de la API, debe crear una superficie de canal para los mensajes SMS. [Más información](sms-configuration-surface.md)

## Credenciales de API de Sinch MMS {#sinch-mms}

>[!IMPORTANT]
>
> Junto con la configuración de MMS, también debe crear credenciales de API de Sinch específicamente para rastrear mensajes entrantes y administrar solicitudes de consentimiento.

Para configurar Sinch MMS para enviar MMS con Journey Optimizer, siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** y seleccione el menú **[!UICONTROL Credenciales de API]**. Haga clic en el botón **[!UICONTROL Crear nuevas credenciales de API]**.

1. Configure las credenciales de la API de MMS como se detalla a continuación:

   * **[!UICONTROL Proveedor de SMS]**: Sinch MMS.

   * **[!UICONTROL Nombre]**: elige un nombre para tu credencial de API.

   * **[!UICONTROL ID de proyecto]**, **[!UICONTROL ID de aplicación]** y **[!UICONTROL token de API]**: siga los pasos a continuación para recopilar sus credenciales de API de MMS.

      * Para **[!UICONTROL ID de proyecto]** e **[!UICONTROL ID de aplicación]**: acceda a la página [Información general de la API de conversación](https://dashboard.sinch.com/convapi/overview) de su proyecto de Sinch en su panel de Sinch.
      * Para **[!UICONTROL token de API]**: obtenga las [claves de acceso](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) para su proyecto Sinch y genere un **Token de API Base64** de su proyecto Sinch **Claves de acceso**.

   * **[!UICONTROL ID de plan de servicio]** y **[!UICONTROL token de API de SMS]**: su **[!UICONTROL ID de plan de servicio]** y **[!UICONTROL token de API de SMS]** se encuentran en la pestaña SMS de la página de API.

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar las credenciales de la API.

Después de crear y configurar las credenciales de la API, debe crear una superficie de canal para los mensajes MMS. [Más información](sms-configuration-surface.md)
