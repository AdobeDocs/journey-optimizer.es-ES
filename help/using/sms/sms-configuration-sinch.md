---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del proveedor de Sinch
description: Aprenda a configurar su entorno para enviar mensajes de texto con Journey Optimizer con Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 3%

---

# Configuración del proveedor de Sinch {#sms-configuration-sinch}

Al utilizar el proveedor de Sinch con Journey Optimizer, puede encontrar dos opciones distintas:

* **Configuración de SMS**: configure sus credenciales de API de Sinch para enviar mensajes SMS sin problemas.

* **Configuración de MMS**: Para la mensajería multimedia (MMS), configure las credenciales de la API de Sinch MMS. Tenga en cuenta que el seguimiento y la respuesta a los mensajes entrantes se gestionan mediante la configuración de SMS. La configuración de MMS solo es para la entrega saliente del mensaje MMS.

## Credenciales de API de Sinch{#create-api}

Para configurar su proveedor de Sinch para que envíe mensajes SMS y MMS con Journey Optimizer, siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administration]** > **[!UICONTROL Canales]** y seleccione la **[!UICONTROL Credenciales de API]** menú. Haga clic en **[!UICONTROL Crear nuevas credenciales de API]** botón.

   ![](assets/sms_6.png)

1. Configure las credenciales de la API de SMS como se detalla a continuación:

   * **[!UICONTROL Nombre]**: elija un nombre para la credencial de la API.

   * **[!UICONTROL ID de servicio]** y **[!UICONTROL Token de API]**: acceda a la página de las API y encontrará sus credenciales en la pestaña SMS. Obtenga más información en [Documentación de Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

   * **[!UICONTROL Palabras clave de inclusión]**: introduzca las palabras clave predeterminadas o personalizadas que almacenarán en déclencheur automáticamente su **[!UICONTROL Mensaje de inclusión]**. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de inclusión]**: introduzca la respuesta personalizada que se envía automáticamente como **[!UICONTROL Mensaje de inclusión]**.

   * **[!UICONTROL Palabras clave de exclusión]**: introduzca las palabras clave predeterminadas o personalizadas que almacenarán en déclencheur automáticamente su **[!UICONTROL Mensaje de exclusión]**. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de exclusión]**: introduzca la respuesta personalizada que se envía automáticamente como **[!UICONTROL Mensaje de exclusión]**.

   * **[!UICONTROL Palabras clave de ayuda]**: introduzca las palabras clave predeterminadas o personalizadas que almacenarán en déclencheur automáticamente su **Mensaje de ayuda**. Para varias palabras clave, utilice valores separados por comas.

   * **[!UICONTROL Mensaje de ayuda]**: introduzca la respuesta personalizada que se envía automáticamente como **Mensaje de ayuda**.

   * **[!UICONTROL Palabras clave de inclusión doble]**: introduzca las palabras clave que almacenan en déclencheur el proceso de inclusión doble. Si no existe ningún perfil de usuario, se crea tras una confirmación correcta. Para varias palabras clave, utilice valores separados por comas. [Obtenga más información sobre la inclusión doble de SMS](https://video.tv.adobe.com/v/3427129/?learn=on).

   * **[!UICONTROL Mensaje de inclusión doble]**: introduzca la respuesta personalizada que se envía automáticamente en respuesta a la confirmación de inclusión doble.

1. Clic **[!UICONTROL Enviar]** cuando haya terminado de configurar las credenciales de la API.

Después de crear y configurar las credenciales de la API, debe crear una superficie de canal para los mensajes SMS. [Más información](sms-configuration-surface.md)

## Credenciales de API de Sinch MMS {#sinch-mms}

>[!IMPORTANT]
>
> Junto con la configuración de MMS, también debe crear credenciales de API de Sinch específicamente para rastrear mensajes entrantes y administrar solicitudes de consentimiento.

Para configurar Sinch MMS para enviar MMS con Journey Optimizer, siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administration]** > **[!UICONTROL Canales]** y seleccione la **[!UICONTROL Credenciales de API]** menú. Haga clic en **[!UICONTROL Crear nuevas credenciales de API]** botón.

   ![](assets/sms_6.png)

1. Configure las credenciales de la API de SMS como se detalla a continuación:

   * **[!UICONTROL Nombre]**: elija un nombre para la credencial de la API.

   * **[!UICONTROL Identificador de proyecto]**, **[!UICONTROL ID de aplicación]** y **[!UICONTROL Token de API]**: en el menú API de conversación, puede encontrar sus credenciales en el menú Aplicación. Obtenga más información en [Documentación de Sinch](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html){target="_blank"}.

   * **[!UICONTROL ID de plan de servicio]** y **[!UICONTROL Token de API de SMS]**: su **[!UICONTROL ID de plan de servicio]** y **[!UICONTROL Token de API de SMS]** se encuentran en la pestaña SMS de la página de API.

1. Clic **[!UICONTROL Enviar]** cuando haya terminado de configurar las credenciales de la API.

Después de crear y configurar las credenciales de la API, debe crear una superficie de canal para los mensajes MMS. [Más información](sms-configuration-surface.md)
