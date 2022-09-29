---
title: Activación de campañas mediante las API
description: Aprenda a almacenar en déclencheur las campañas mediante [!DNL Journey Optimizer] API
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 9fbfeef292e4b71396680573007e062b525b24c9
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 1%

---

# Activación de campañas mediante las API {#trigger-campaigns}

## Acerca de las campañas activadas por API {#about}

con [!DNL Journey Optimizer], puede crear campañas y luego invocarlas desde un sistema externo basado en el déclencheur del usuario mediante el [API de REST de ejecución de mensajes interactivos](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). Esto le permite cubrir diversas necesidades operativas y de mensajería transaccional, como los restablecimientos de contraseña, el token OTP, entre otras.

Para ello, primero debe crear una campaña activada por API en Journey Optimizer y, a continuación, iniciar su ejecución mediante una llamada a la API.

Los canales disponibles para las campañas activadas por API son correo electrónico, SMS y mensajes push.

## Creación de una campaña activada por API {#create}

El proceso para crear campañas activadas por API sigue siendo el mismo que las campañas programadas, excepto para la selección de audiencias que se realiza en la carga útil de API. Encontrará información detallada sobre cómo crear una campaña en [esta sección](create-campaign.md).

Para crear una campaña desencadenada por API, siga estos pasos:

1. Cree una nueva campaña con el **[!UICONTROL Activado por API]** tipo .

1. Seleccione el canal y la superficie del canal que desea utilizar para enviar el mensaje y, a continuación, haga clic en **[!UICONTROL Crear]**.

   ![](assets/api-triggered-type.png)

1. Especifique un título y una descripción para la campaña y, a continuación, configure el mensaje que desea enviar.

   ![](assets/api-triggered-properties.png)

   >[!NOTE]
   >
   >Puede pasar datos adicionales a la carga útil de la API que puede aprovechar para personalizar el mensaje. [Más información](#contextual)
   >
   >El uso de un gran número o de datos contextuales pesados en el contenido puede afectar al rendimiento.

1. En el **[!UICONTROL Audiencia]** , especifique el área de nombres que se utilizará para identificar a las personas del segmento.

   La variable **[!UICONTROL Crear nuevos perfiles]** permite crear automáticamente perfiles que no existen en la base de datos. [Obtenga más información sobre la creación de perfiles en la ejecución de campañas](#profile-creation)

1. Configure las fechas de inicio y finalización de la campaña.

   Si configura una fecha de inicio y/o finalización específica para una campaña, no se ejecutará fuera de estas fechas y las llamadas a la API fallarán si la campaña se activa mediante API.

1. En el **[!UICONTROL petición cURL]** , recupere la **[!UICONTROL ID de campaña]** para usar en la carga útil de API.

   ![](assets/api-triggered-curl.png)

1. Haga clic en **[!UICONTROL Revisar para activar]** para comprobar que la campaña está correctamente configurada, actívela.

## Utilizar atributos contextuales en campañas activadas por API {#contextual}

Con las campañas activadas por API, puede pasar datos adicionales en la carga útil de API y utilizarlos dentro de la campaña para personalizar su mensaje.

Veamos este ejemplo, en el que los clientes desean restablecer su contraseña y desea enviarles una URL de restablecimiento de contraseña que se genera en una herramienta de terceros. Con las campañas activadas por API, puede pasar esta URL generada a la carga útil de API y aprovecharla en la campaña para añadirla al mensaje.

>[!NOTE]
>
>A diferencia de los eventos habilitados para perfiles, los datos contextuales pasados en la API de REST se utilizan para comunicaciones únicas y no se almacenan en el perfil. Como máximo, el perfil se crea con los detalles del área de nombres, si se encontró que falta.

Para utilizar estos datos en sus campañas, debe pasarlos a la carga útil de la API y añadirlos en el mensaje mediante el editor de expresiones. Para ello, utilice el `{{context.<contextualAttribute>}}` sintaxis, donde `<contextualAttribute>` debe coincidir con el nombre de la variable en la carga útil de API que contiene los datos que desea pasar.

La variable `{{context.<contextualAttribute>}}` la sintaxis de se asigna únicamente a un tipo de datos de cadena.

![](assets/api-triggered-context.png)

>[!IMPORTANT]
>
>La variable `context.system` la sintaxis está restringida únicamente al uso interno de Adobe y no debe utilizarse para pasar atributos contextuales.
Tenga en cuenta que, por ahora, no hay ningún atributo contextual disponible para usar en el menú del carril izquierdo. Los atributos deben escribirse directamente en la expresión de personalización, sin que la comprobación la realice [!DNL Journey Optimizer].

## Ejecución de la campaña {#execute}

Para ejecutar una campaña activada por API, primero debe recuperar su ID y pasarlo a la carga útil de API. Para ello, abra la campaña y copie el ID y péguelo en el **[!UICONTROL petición cURL]** para obtener más información.

![](assets/api-triggered-id.png)

A continuación, puede utilizar este ID en la carga útil de la API para almacenar en déclencheur la campaña. Consulte la [Documentación de la API de ejecución de mensajes interactivos](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution) para obtener más información.

Tenga en cuenta que si ha configurado una fecha de inicio y/o finalización específica al crear la campaña, no se ejecutará fuera de estas fechas y las llamadas a la API no se ejecutarán correctamente.

## Creación de perfiles en la ejecución de la campaña {#profile-creation}

En algunos casos, es posible que tenga que enviar mensajes transaccionales a perfiles que no existen en el sistema. Por ejemplo, si un usuario desconocido intenta iniciar sesión en el sitio web.

Cuando un perfil no existe en la base de datos, Journey Optimizer le permite crearlo automáticamente al ejecutar la campaña para permitir enviar el mensaje a este perfil.

Para ello, marque la opción **[!UCONTROL Crear nuevos perfiles]** en la **[!UICONTROL Audiencia]** para obtener más información.

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>Los perfiles desconocidos se crean en la variable **Conjunto de datos del perfil de mensajería interactiva AJO** conjunto de datos, en tres área de nombres predeterminada (correo electrónico, teléfono y ECID) respectivamente para cada canal saliente (correo electrónico, SMS y push).
