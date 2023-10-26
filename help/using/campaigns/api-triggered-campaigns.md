---
solution: Journey Optimizer
product: journey optimizer
title: Activación de campañas mediante las API
description: Obtenga información sobre cómo almacenar en déclencheur las campañas mediante las API de Journey Optimizer
feature: Campaigns, API
topic: Content Management
role: Developer, Admin
level: Experienced
keywords: campañas, activadas por API, REST, optimizador, mensajes
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: d4ecfecdc74c26890658d68d352c36b75f7c9039
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 3%

---

# Activación de campañas mediante las API {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_api_profile_creation"
>title="Tipo de campaña"
>abstract="Para utilizar la funcionalidad de disponibilidad limitada para enviar mensajes sin crear perfiles, siga los pasos detallados en la documentación."

## Acerca de las campañas activadas por API {#about}

Con [!DNL Journey Optimizer], puede crear campañas y luego invocarlas desde un sistema externo basado en el déclencheur del usuario utilizando [API de REST de ejecución de mensaje interactivo](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). Esto le permite cubrir diversas necesidades de marketing y mensajería transaccional, como restablecimientos de contraseña, token OTP, entre otros.

Para ello, primero debe crear una campaña activada por API en Journey Optimizer y luego iniciar su ejecución mediante una llamada de API.

![](../rn/assets/do-not-localize/api-triggered.gif)

Los canales disponibles para las campañas activadas por API son correo electrónico, SMS y mensajes push.

>[!NOTE]
>
>Por ahora, el modo de envío rápido no es compatible con campañas activadas por API de notificaciones push.

## Creación de una campaña activada por API {#create}

### Configuración y activación de la campaña {#create-activate}

Para crear una campaña activada por API, siga los pasos a continuación. Encontrará información detallada sobre cómo crear una campaña en [esta sección](create-campaign.md).

1. Cree una nueva campaña con **[!UICONTROL Activado por API]** escriba.

1. Elija la **[!UICONTROL Marketing]** o **[!UICONTROL Transaccional]** categoría según el tipo de comunicación que desee enviar.

1. Elija uno de los canales admitidos y la superficie de canal asociada que se utilizará para enviar el mensaje y, a continuación, haga clic en **[!UICONTROL Crear]**.

   ![](assets/api-triggered-type.png)

1. Especifique un título y una descripción para la campaña y haga clic en **[!UICONTROL Editar contenido]** para configurar el mensaje que desea enviar.

   >[!NOTE]
   >
   >Puede pasar datos adicionales en la carga útil de la API que puede aprovechar para personalizar su mensaje. [Más información](#contextual)
   >
   >El uso de un gran número o de datos contextuales pesados en el contenido puede afectar al rendimiento.

1. En el **[!UICONTROL Audiencia]** , especifique el área de nombres que se utilizará para identificar a los individuos.

   * Si está creando un **transaccional** del tipo, los perfiles objetivo deben definirse en la llamada de API. El **[!UICONTROL Creación de nuevos perfiles]** permite crear automáticamente perfiles que no existen en la base de datos. [Obtenga más información sobre la creación de perfiles en la ejecución de campañas](#profile-creation)

   * Para **marketing** Campañas de tipo, haga clic en **[!UICONTROL Audiencia]** para elegir el público objetivo.

1. Configure las fechas de inicio y finalización de la campaña.

   Si configura una fecha específica de inicio o finalización de una campaña, esta no se ejecutará fuera de estas fechas y las llamadas a la API fallarán si la campaña se activa mediante API.

1. Clic **[!UICONTROL Revisar para activar]** para comprobar que la campaña está configurada correctamente, actívela.

Ya está listo para ejecutar la campaña desde las API. [Más información](#execute)

### Ejecución de la campaña {#execute}

Una vez activada la campaña, debe recuperar la solicitud cURL de muestra generada y utilizarla en la API para crear la carga útil y almacenar la campaña en déclencheur.

1. Abra la campaña y copie y pegue la solicitud de ejemplo desde el **[!UICONTROL Solicitud cURL]** sección.

   ![](assets/api-triggered-curl.png)

1. Utilice esta solicitud de cURL en las API para crear la carga útil y almacenar en déclencheur la campaña. Para obtener más información, consulte la [Documentación de la API de ejecución de mensaje interactivo](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).


   Los ejemplos de llamadas de API también están disponibles en [esta página](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

   >[!NOTE]
   >
   >Si ha configurado una fecha específica de inicio o finalización al crear la campaña, esta no se ejecuta fuera de estas fechas y las llamadas a la API fallan.

## Uso de atributos contextuales en campañas activadas por API {#contextual}

Con las campañas activadas por API, puede pasar datos adicionales en la carga útil de la API y utilizarlos dentro de la campaña para personalizar el mensaje.

Veamos este ejemplo en el que los clientes desean restablecer su contraseña y usted desea enviarles una URL de restablecimiento de contraseña generada en una herramienta de terceros. Con las campañas activadas por API, puede pasar esta URL generada a la carga útil de la API y aprovecharla en la campaña para agregarla al mensaje.

>[!NOTE]
>
>A diferencia de los eventos habilitados para perfiles, los datos contextuales pasados en la API de REST se utilizan para una comunicación única y no se almacenan en el perfil. Como máximo, el perfil se crea con los detalles del área de nombres, si se ha encontrado que falta.

Para utilizar estos datos en sus campañas, debe pasarlos a la carga útil de la API y añadirlos en su mensaje mediante el Editor de expresiones. Para ello, utilice el `{{context.<contextualAttribute>}}` sintaxis, donde `<contextualAttribute>` debe coincidir con el nombre de la variable en la carga útil de API que contiene los datos que desea pasar.

El `{{context.<contextualAttribute>}}` La sintaxis solo se asigna a un tipo de datos de cadena.

![](assets/api-triggered-context.png)


>[!IMPORTANT]
>
>Los atributos contextuales pasados a la solicitud no pueden superar los 50 KB y siempre se consideran de tipo cadena.
>
>El `context.system` la sintaxis está restringida únicamente al uso interno del Adobe y no debe utilizarse para pasar atributos contextuales.

Tenga en cuenta que, por ahora, no hay ningún atributo contextual disponible para su uso en el menú del carril izquierdo. Los atributos deben escribirse directamente en la expresión personalizada, sin que ninguna comprobación sea realizada por [!DNL Journey Optimizer].

## Creación de perfiles en ejecución de campaña {#profile-creation}

En algunos casos, es posible que deba enviar mensajes transaccionales a perfiles que no existen en el sistema. Por ejemplo, si un usuario desconocido intenta restablecer la contraseña en su sitio web.

Cuando un perfil no existe en la base de datos, Journey Optimizer le permite crearlo automáticamente al ejecutar la campaña para permitir el envío del mensaje a este perfil.

>[!IMPORTANT]
>
>En el caso de los mensajes transaccionales, esta función se proporciona para **creación de perfiles de volumen muy pequeño** en un caso de uso de envío transaccional de gran volumen, con un grueso de perfiles ya existentes en platform.

Para activar la creación de perfiles en la ejecución de la campaña, cambie el **[!UICONTROL Creación de nuevos perfiles]** opción activada en la **[!UICONTROL Audiencia]** sección. Si esta opción está deshabilitada, los perfiles desconocidos se rechazarán para cualquier envío y la llamada de API fallará.

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>Los perfiles desconocidos se crean en **Conjunto de datos del perfil de mensajería interactiva AJO** , en tres áreas de nombres predeterminadas (correo electrónico, teléfono y ECID) respectivamente para cada canal saliente (correo electrónico, SMS y push).
