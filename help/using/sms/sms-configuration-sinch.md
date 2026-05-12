---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del proveedor de Sinch
description: Aprenda a configurar su entorno para enviar mensajes de texto con Journey Optimizer con Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
TQID: https://experienceleague.adobe.com/24n9GhVTfQ9y4hlvY6g67dyL0FHqNOJW0aP-WIpzRqs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 9e5edbefb19b7cf30da3a7164300e966a42e8711
workflow-type: tm+mt
source-wordcount: 946
ht-degree: 1%

---

# Configuración del proveedor de Sinch {#sms-configuration-sinch}

Al utilizar el proveedor de Sinch con Journey Optimizer, puede encontrar tres opciones distintas:

* **Configuración de SMS**: configura tus credenciales de la API de Sinch para enviar mensajes SMS sin problemas.

* **Configuración de MMS**: para la mensajería multimedia (MMS), configure sus credenciales de API de MMS de Sinch. Tenga en cuenta que el seguimiento y la respuesta a los mensajes entrantes se gestionan mediante la configuración de SMS. La configuración de MMS solo es para la entrega saliente del mensaje MMS.

* **Configuración de RCS**: configure sus credenciales de API de Sinch para enviar mensajes RCS sin problemas.

Para configurar su proveedor de Sinch, siga los pasos a continuación:

1. [Crear credencial de API](#create-api)
1. [Crear webhook](sms-webhook.md)
1. [Crear configuración de canal](sms-configuration-surface.md)
1. [Creación de un Recorrido o una campaña con una acción de canal SMS](create-sms.md)

## Configuración de credenciales de API para SMS{#create-api}

Para configurar su proveedor de Sinch para que envíe mensajes SMS y MMS con Journey Optimizer, siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** `>` **[!UICONTROL Configuración de SMS]** y seleccione el menú **[!UICONTROL Credenciales de API]**. Haga clic en el botón **[!UICONTROL Crear nuevas credenciales de API]**.

1. Configure las credenciales de la API de SMS como se detalla a continuación:

   +++ Lista de credenciales de SMS para la configuración

   | Campos de configuración | Descripción |
   |---|---|
   | Proveedor de SMS | Sinch |
   | Nombre | Elija un nombre para su credencial de API. |
   | ID de servicio y token de API | Acceda a la página de API y encontrará sus credenciales en la pestaña SMS. Obtenga más información en [Documentación de Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}. |
   | Número entrante | Añada su número de entrada único o código corto. Esto le permite utilizar las mismas credenciales de API en diferentes entornos limitados, cada uno con su propio número de entrada o código corto. |
   | Anular URL | Introduzca la URL personalizada para reemplazar los puntos finales predeterminados para los informes de entrega de SMS, los datos de comentarios, los mensajes entrantes o las notificaciones de eventos. Sinch enviará todas las actualizaciones relevantes a esta URL en lugar de a las predefinidas. |

   +++

<!--
1. Choose how user consent should be tracked for messaging:

    * **[!UICONTROL Sender short code]**: Inbound keyword consent is keyed to your **sender short code** only. Use when one inbound number is enough to represent consent.

    * **[!UICONTROL Sender short code + profile number]**: Consent is keyed to the **sender short code** and the profile **mobile number**. Use when profiles can have several numbers, or when opt-in/out must apply per sender and recipient pair.
-->

1. Seleccione **[!UICONTROL Usar conjunto de datos personalizado para entrante]** para enrutar el SMS entrante de esta credencial a un conjunto de datos creado previamente que elija en el menú desplegable. [Más información acerca del uso de un conjunto de datos personalizado para palabras clave entrantes](custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >El esquema del conjunto de datos debe ser **[!UICONTROL XDM ExperienceEvent]** e incluir al menos estos grupos de campos:
   >* Adobe CJM ExperienceEvent: Detalles de interacción del mensaje
   >* Adobe CJM ExperienceEvent: Detalles de ejecución de mensajes
   >* Adobe CJM ExperienceEvent: Detalles del perfil de mensaje
   >
   >El esquema y el conjunto de datos deben estar habilitados para el perfil.


1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar las credenciales de la API.

1. En el menú **[!UICONTROL Credenciales de API]**, haga clic en el icono bin para eliminar sus credenciales de API.

1. Para modificar las credenciales existentes, busque las credenciales de API que desee y haga clic en la opción **[!UICONTROL Editar]** para realizar los cambios necesarios.

1. Haga clic en **[!UICONTROL Verificar conexión de SMS]**, a partir de las credenciales de la API existente, para probar y comprobar las credenciales de la API de SMS enviando un mensaje de ejemplo a un dispositivo designado.

1. Rellene los campos **Número** y **Mensaje** y haga clic en **[!UICONTROL Verificar conexión]**.

   >[!IMPORTANT]
   >
   >El mensaje debe estar estructurado para alinearse con el formato de carga útil del proveedor.

   ![](assets/verify-connection.png)

Después de crear y configurar tu credencial de API, ahora necesitas crear [tu webhook](sms-webhook.md) y una configuración de canal para tus mensajes RCS. [Más información](sms-configuration-surface.md)

## Configurar credenciales de API para MMS{#sinch-mms}

>[!IMPORTANT]
>
> Junto con la configuración de MMS, también debe crear credenciales de API de Sinch específicamente para rastrear mensajes entrantes y administrar solicitudes de consentimiento.

Para configurar Sinch MMS para enviar MMS con Journey Optimizer, siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** `>` **[!UICONTROL Configuración de SMS]** y seleccione el menú **[!UICONTROL Credenciales de API]**. Haga clic en el botón **[!UICONTROL Crear nuevas credenciales de API]**.

1. Configure las credenciales de la API de MMS como se detalla a continuación:

   * **[!UICONTROL Proveedor de SMS]**: Sinch MMS.

   * **[!UICONTROL Nombre]**: elige un nombre para tu credencial de API.

   * **[!UICONTROL ID de proyecto]**, **[!UICONTROL ID de aplicación]** y **[!UICONTROL token de API]**: siga los pasos a continuación para recopilar sus credenciales de API de MMS.

      * Para **[!UICONTROL ID de proyecto]** e **[!UICONTROL ID de aplicación]**: acceda a la página [Información general de la API de conversación](https://dashboard.sinch.com/convapi/overview) de su proyecto de Sinch en su panel de Sinch.
      * Para **[!UICONTROL token de API]**: obtenga las [claves de acceso](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) para su proyecto Sinch y genere un **Token de API Base64** de su proyecto Sinch **Claves de acceso**.

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar las credenciales de la API.

1. En el menú **[!UICONTROL Credenciales de API]**, haga clic en el icono bin para eliminar sus credenciales de API.

1. Para modificar las credenciales existentes, busque las credenciales de API que desee y haga clic en la opción **[!UICONTROL Editar]** para realizar los cambios necesarios.

Después de crear y configurar tu credencial de API, ahora necesitas crear [tu webhook](sms-webhook.md) y una configuración de canal para tus mensajes RCS. [Más información](sms-configuration-surface.md)

## Configurar las credenciales de API para RCS

<!--![](assets/do-not-localize/rcs-sms.png)-->

La mensajería RCS (servicios de comunicación enriquecidos) es compatible con Journey Optimizer a través de Sinch, lo que permite enviar mensajes básicos utilizando perfiles comerciales verificados con elementos de marca como logotipos y nombres de remitente.

Tenga en cuenta que los mensajes vuelven automáticamente a SMS cuando el dispositivo del perfil no admite RCS o no se puede acceder a él temporalmente mediante RCS.

<!--
### Basic RCS Messages

>[!AVAILABILITY]
>
> Basic RCS messages is only available upon Adobe RCS add-on offering.

1. **Set up your branded RCS agent**

    Create a branded RCS agent in the Sinch Dashboard. [Learn more on branded RCS agent](https://community.sinch.com/t5/RCS/Getting-Started-with-RCS-using-Conversation-API/ta-p/17844)

1. **Set up your [Custom API credentials](sms-configuration-custom.md)**
    
    Once your RCS agent is approved, you need to set up your Sinch API credentials, which include your access key, secret, and service plan ID. These credentials will be used by Journey Optimizer to authenticate and send messages through Sinch's platform.

1. **Create a [channel configuration](sms-configuration-surface.md) for your RCS messages**

    Configure a channel surface in Journey Optimizer by linking your Sinch credentials and defining the messaging parameters. This setup enables you to compose and send RCS messages from Journey Optimizer.

1. **Create and personalize your [SMS message](../sms/create-sms.md)**

    Your messages automatically falls back to SMS when the profile's device does not support RCS or is temporarily unreachable via RCS.
-->

### Mensajes multimedia RCS

>[!AVAILABILITY]
>
> Los mensajes RCS avanzados solo están disponibles con una cuenta directa administrada por Sinch.

1. **Configure su agente RCS de marca**

   Cree un agente de RCS de marca en el panel de Sinch. [Más información sobre el agente de RCS de marca](https://community.sinch.com/t5/RCS/Getting-Started-with-RCS-using-Conversation-API/ta-p/17844)

1. **Configure sus [credenciales de API personalizadas](sms-configuration-custom.md)**

   Una vez aprobado el agente de RCS, debe configurar las credenciales de API personalizadas, que incluyen su AppId, nombre, dirección URL y tipo de autenticación.

1. **Configure su RCS con la carga útil del proveedor.**

   En sus [credenciales de API personalizadas](sms-configuration-custom.md), agregue la carga útil del proveedor para validar y personalizar los mensajes RCS.

1. **Cree una [configuración de canal](sms-configuration-surface.md) para sus mensajes RCS**

   Configure una superficie de canal en Journey Optimizer vinculando las credenciales de Sinch y definiendo los parámetros de mensajería. Esta configuración le permite componer y enviar mensajes RCS desde Journey Optimizer.

1. **Crea y personaliza tu [mensaje SMS](../sms/create-sms.md)**

   Pegue su carga útil directamente en el contenido del SMS para incrustar y enviar los mensajes de los servicios de comunicación enriquecidos (RCS).

   ➡️ [Explore cómo Sinch admite RCS en la documentación de Sinch](https://sinch.com/blog/rcs-api-guide/)


