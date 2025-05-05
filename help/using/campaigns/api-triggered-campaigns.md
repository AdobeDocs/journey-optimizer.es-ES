---
solution: Journey Optimizer
product: journey optimizer
title: Activación de campañas mediante las API
description: Obtenga información sobre cómo almacenar en déclencheur las campañas mediante las API de Journey Optimizer
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campañas, activadas por API, REST, optimizador, mensajes
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 2%

---

# Activación de campañas mediante las API {#trigger-campaigns}

## Acerca de las campañas activadas por API {#about}

Con [!DNL Journey Optimizer], puede crear campañas y luego ejecutarlas desde un sistema externo basado en el déclencheur del usuario mediante la [API de REST de ejecución de mensajes interactiva](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). Esto le permite cubrir diversas necesidades de marketing y mensajería transaccional, como restablecimientos de contraseña, token OTP, entre otros.

Para ello, primero debe crear una campaña activada por API en Journey Optimizer y luego iniciar su ejecución mediante una llamada de API.

![](../rn/assets/do-not-localize/api-triggered.gif)

Los canales disponibles para las campañas activadas por API son correo electrónico, SMS y mensajes push.

>[!NOTE]
>
>Por ahora, el modo de envío rápido no es compatible con campañas activadas por API de notificaciones push.

➡️ [Descubra esta función en vídeo](#video)

## Creación de una campaña activada por API {#create}

### Configuración y activación de la campaña {#create-activate}

Para crear una campaña activada por API, siga los pasos a continuación. Encontrará información detallada sobre cómo crear una campaña en [esta sección](create-campaign.md).

1. Cree una nueva campaña con el tipo **[!UICONTROL activado por API]**.

1. Elija la categoría **[!UICONTROL Marketing]** o **[!UICONTROL Transaccional]** según el tipo de comunicación que desee enviar.

1. Elija uno de los canales admitidos y la configuración de canal asociada que se utilizará para enviar el mensaje y, a continuación, haga clic en **[!UICONTROL Crear]**.

   ![](assets/api-triggered-type.png)

1. Especifique un título y una descripción para la campaña y luego haga clic en **[!UICONTROL Editar contenido]** para configurar el mensaje que desea enviar.

   >[!NOTE]
   >
   >Puede pasar datos adicionales en la carga útil de la API que puede aprovechar para personalizar su mensaje. [Más información](#contextual)
   >
   >El uso de un gran número o de datos contextuales pesados en el contenido puede afectar al rendimiento.

1. En la sección **[!UICONTROL Audience]**, especifique el área de nombres que se utilizará para identificar a los individuos.

   * Si está creando una campaña del tipo **transaccional**, los perfiles de destino deben definirse en la llamada de API. La opción **[!UICONTROL Crear nuevos perfiles]** le permite crear automáticamente perfiles que no existen en la base de datos. [Obtenga más información acerca de la creación de perfiles en la ejecución de la campaña](#profile-creation)

     >[!NOTE]
     >
     >Una sola llamada de API admite hasta 20 destinatarios únicos. Cada destinatario debe tener un ID de usuario único, no se permiten ID de usuario duplicados. Obtenga más información en la [documentación interactiva de la API de ejecución de mensajes](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution/operation/postIMUnitaryMessageExecution){target="_blank"}

   * Para las campañas del tipo **marketing**, haga clic en el botón **[!UICONTROL Audiencia]** para elegir la audiencia a la que se dirigirá.

1. Configure las fechas de inicio y finalización de la campaña.

   Si configura una fecha específica de inicio o finalización de una campaña, esta no se ejecutará fuera de estas fechas y las llamadas a la API fallarán si la campaña se activa mediante API.

1. Haga clic en **[!UICONTROL Revisar para activar]** y comprobar que la campaña esté configurada correctamente y, a continuación, actívela.

Ya está listo para ejecutar la campaña desde las API. [Más información](#execute)

### Ejecución de la campaña {#execute}

Una vez activada la campaña, debe recuperar la solicitud cURL de muestra generada y utilizarla en la API para crear la carga útil y almacenar la campaña en déclencheur.

1. Abra la campaña y copie y pegue la solicitud de carga útil de la sección **[!UICONTROL cURL request]**. Esta carga útil incluye todas las variables de personalización (perfil y contexto) utilizadas en el mensaje. Está disponible una vez que la campaña está activa.

   ![](assets/api-triggered-curl.png)

1. Utilice esta solicitud de cURL en las API para crear la carga útil y almacenar en déclencheur la campaña. Para obtener más información, consulte la [documentación interactiva de la API de ejecución de mensajes](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).


   También hay ejemplos de llamadas API disponibles en [esta página](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

   >[!NOTE]
   >
   >Si ha configurado una fecha específica de inicio o finalización al crear la campaña, esta no se ejecuta fuera de estas fechas y las llamadas a la API fallan.

## Uso de atributos contextuales en campañas activadas por API {#contextual}

Con las campañas activadas por API, puede pasar datos adicionales en la carga útil de la API y utilizarlos dentro de la campaña para personalizar el mensaje.

Veamos este ejemplo en el que los clientes desean restablecer su contraseña y usted desea enviarles una URL de restablecimiento de contraseña generada en una herramienta de terceros. Con las campañas activadas por API, puede pasar esta URL generada a la carga útil de la API y aprovecharla en la campaña para agregarla al mensaje.

>[!NOTE]
>
>A diferencia de los eventos habilitados para perfiles, los datos contextuales pasados en la API de REST se utilizan para una comunicación única y no se almacenan en el perfil. Como máximo, el perfil se crea con los detalles del área de nombres, si se ha encontrado que falta.

Para utilizar estos datos en sus campañas, debe pasarlos a la carga útil de la API y añadirlos en su mensaje mediante el editor de personalización. Para ello, utilice la sintaxis `{{context.<contextualAttribute>}}`, donde `<contextualAttribute>` debe coincidir con el nombre de la variable en la carga útil de la API que contiene los datos que desea pasar.

La sintaxis `{{context.<contextualAttribute>}}` solo está asignada a un tipo de datos de cadena.

![](assets/api-triggered-context.png)


>[!IMPORTANT]
>
>Los atributos contextuales pasados a la solicitud no pueden superar los 200 KB y siempre se consideran de tipo cadena.
>
>La sintaxis `context.system` está restringida únicamente al uso interno de Adobe y no debe usarse para pasar atributos contextuales.

Tenga en cuenta que, por ahora, no hay ningún atributo contextual disponible para su uso en el menú del carril izquierdo. Los atributos deben escribirse directamente en la expresión personalizada, sin que [!DNL Journey Optimizer] realice ninguna comprobación.

## Creación de perfiles en ejecución de campaña {#profile-creation}

En algunos casos, es posible que deba enviar mensajes transaccionales a perfiles que no existen en el sistema. Por ejemplo, si un usuario desconocido intenta restablecer la contraseña en su sitio web.

Cuando un perfil no existe en la base de datos, Journey Optimizer le permite crearlo automáticamente al ejecutar la campaña para permitir el envío del mensaje a este perfil.

>[!IMPORTANT]
>
>En el caso de los mensajes transaccionales, esta característica se proporciona para la creación de perfiles de **volumen muy pequeño** en un caso de uso de envío transaccional de gran volumen, con una gran cantidad de perfiles ya existentes en la plataforma.

Para activar la creación de perfiles en la ejecución de la campaña, active la opción **[!UICONTROL Crear nuevos perfiles]** en la sección **[!UICONTROL Audiencia]**. Si esta opción está deshabilitada, los perfiles desconocidos se rechazarán para cualquier envío y la llamada de API fallará.

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>Se crean perfiles desconocidos en el conjunto de datos **AJO Interactive Messaging Profile Dataset**, en tres áreas de nombres predeterminadas (correo electrónico, teléfono y ECID) respectivamente para cada canal saliente (correo electrónico, SMS y push). Sin embargo, si utiliza un área de nombres personalizada, la identidad se crea con el mismo área de nombres personalizada.

## Vídeo práctico {#video}

Obtenga información sobre cómo crear una campaña y almacenarla en déclencheur desde un sistema externo basado en las interacciones del usuario, mediante la API de REST de ejecución de mensaje interactivo.

>[!VIDEO](https://video.tv.adobe.com/v/3452728?quality=12&captions=spa)
