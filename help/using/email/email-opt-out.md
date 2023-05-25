---
solution: Journey Optimizer
product: journey optimizer
title: Administración de exclusión de correo electrónico
description: Obtenga información sobre cómo administrar la exclusión con correos electrónicos
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: exclusión, correo electrónico, vínculo, cancelación de suscripción
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: f5390bbb3bab435b21ace4d1842de0048132bc8c
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 80%

---

# Administración de exclusión de correo electrónico {#email-opt-out}

Para proporcionar a los destinatarios la capacidad de cancelar la suscripción a la recepción de comunicaciones por correo electrónico, siempre debe incluir un **vínculo de cancelación de suscripción** en cada correo electrónico enviado a los destinatarios. [Más información sobre la administración de la privacidad y la exclusión](../privacy/opt-out.md)

Para ello, puede hacer lo siguiente:

* Inserte una **vínculo a una página de aterrizaje externa** en un correo electrónico para permitir a los usuarios cancelar la suscripción y evitar recibir comunicaciones de su marca. [Obtenga información sobre cómo añadir un vínculo de no participación externo](#opt-out-external-lp)

* Añadir un **vínculo de no participación de un clic** en el contenido del correo electrónico. Este vínculo permite a los destinatarios cancelar la suscripción rápidamente a sus comunicaciones, sin que se les redirija a una página de aterrizaje en la que tengan que confirmar la exclusión, lo que acelera el proceso de cancelación de la suscripción. [Obtenga información sobre cómo añadir un vínculo de no participación de un clic](#one-click-opt-out)

Además, si la variable **[!UICONTROL Cancelación de suscripción a lista]** está activada en el nivel de superficie de canal, los correos electrónicos correspondientes enviados con Journey Optimizer incluirán un vínculo de cancelación de suscripción en el encabezado del correo electrónico. [Obtenga más información sobre la exclusión en el encabezado del correo electrónico](#unsubscribe-header)

>[!NOTE]
>
>Los mensajes de correo electrónico de tipo marketing deben incluir un vínculo de no participación, que no es necesario para los mensajes transaccionales. La categoría del mensaje (**[!UICONTROL Marketing]** o **[!UICONTROL Transaccional]**) se define en [superficie de canal](../configuration/channel-surfaces.md#email-type) y al crear el mensaje).

## Exclusión externa {#opt-out-external-lp}

### Agregar el vínculo &quot;Cancelar la suscripción&quot; {#add-unsubscribe-link}

Primero debe agregar el vínculo &quot;Cancelar la suscripción&quot; a un mensaje. Para realizar esto, siga los pasos a continuación:

1. Genere la página de aterrizaje de baja.

1. Alójelo en el sistema de terceros que elija.

1. Cree un mensaje en un recorrido.

1. Seleccione texto en el contenido e [inserte un vínculo](../email/message-tracking.md#insert-links) utilizando la barra de herramientas contextual.

   ![](assets/opt-out-insert-link.png)

1. Seleccione **[!UICONTROL Exclusión/baja externa]** de la lista desplegable **[!UICONTROL Tipo de vínculo]**.

   ![](assets/opt-out-link-type.png)

1. En el campo de **[!UICONTROL Vínculo]**, pegue el vínculo a la página de aterrizaje de terceros.

   ![](assets/opt-out-link-url.png)

1. Haga clic en **[!UICONTROL Guardar]**.

### Implementación de una llamada de API para la exclusión {#opt-out-api}

Para que los destinatarios se excluyan cuando envíen su elección desde la página de aterrizaje, debe implementar un **Llamada de API de suscripción** mediante [Adobe Developer](https://developer.adobe.com){target="_blank"} para actualizar las preferencias de los perfiles correspondientes.

Esta llamada de POST es como sigue:

Punto final: https://platform.adobe.io/journey/imp/consent/preferences

Parámetros de consulta:

* **params**: contiene la carga útil cifrada
* **pid**: ID de perfil cifrado

Estos tres parámetros se incluyen en la dirección URL de la página de aterrizaje de terceros que se envía al destinatario:

![](assets/opt-out-parameters.png)

Requisitos de encabezado:

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* authorization (token de usuario de su cuenta técnica)

Cuerpo de la solicitud:

```
{
   "marketing": [
       {
            "type": "email",           
            "choice": "no",          
            "scope": "channel"       
        }
    ],
 
}
```

[!DNL Journey Optimizer] utilizará estos parámetros para actualizar la elección del perfil correspondiente a través de la variable [Adobe Developer](https://developer.adobe.com){target="_blank"} Llamada de API.

### Enviar el mensaje con el vínculo &quot;Cancelar la suscripción&quot; {#send-message-unsubscribe-link}

Una vez configurado el vínculo &quot;Cancelar la suscripción&quot; a la página de aterrizaje e implementado la llamada de API, el mensaje está listo para enviarse

1. Envíe el mensaje, incluido el vínculo a través de un [recorrido](../building-journeys/journey.md).

1. Una vez recibido el mensaje, si el destinatario hace clic en el vínculo para cancelar la suscripción, se muestra la página de aterrizaje.

   ![](assets/opt-out-lp-example.png)

1. Si el destinatario envía el formulario (aquí, pulsando el botón **Cancelar la suscripción** en la página de aterrizaje), los datos de perfil se actualizan a través de la [llamada de la API](#opt-out-api).

1. El destinatario excluido se redirige a la pantalla de mensaje de confirmación para indicar que la exclusión se ha realizado correctamente.

   ![](assets/opt-out-confirmation-example.png)

   Como resultado, este usuario no recibirá comunicaciones de su marca a menos que se vuelva a suscribir.

1. Para comprobar que se ha actualizado la opción del perfil correspondiente, vaya a Experience Platform y acceda al perfil seleccionando un área de nombres de identidad y un valor de identidad correspondiente. Obtenga más información en la [documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=es#getting-started){target="_blank"}.

   ![](assets/opt-out-profile-choice.png)

   En la pestaña **[!UICONTROL Atributos]**, puede ver que el valor de **[!UICONTROL elección]** ha cambiado a **[!UICONTROL no]**.

## Opción de exclusión en un clic {#one-click-opt-out}

Para añadir un vínculo de no participación en el correo electrónico, siga los pasos a continuación.

1. [Inserte un vínculo](../email/message-tracking.md#insert-links) y seleccione **[!UICONTROL Exclusión con un clic]** como tipo de vínculo.

   ![](assets/message-tracking-opt-out.png)

1. Escriba la dirección URL de la página de aterrizaje a la que se redirigirá al usuario una vez cancelada la suscripción. Esta página solo está aquí para confirmar que la exclusión se ha realizado correctamente.

   >[!NOTE]
   >
   >Si ha activado la opción **Cancelar la suscripción a una lista** en el nivel de superficie de canal, esta URL también se utilizará cuando los usuarios hagan clic en el vínculo &quot;Cancelar la suscripción&quot; en el encabezado del correo electrónico. [Más información](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Puede personalizar los vínculos. Obtenga más información sobre las URL personalizadas en [esta sección](../personalization/personalization-syntax.md).

1. Seleccione cómo desea aplicar la exclusión: en el nivel de canal, identidad o suscripción.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Canal]**: la exclusión se aplica a mensajes futuros enviados al destinatario del perfil (es decir, la dirección de correo electrónico) para el canal actual. Si hay varios objetivos asociados a un perfil, la exclusión se aplica a todos los destinatarios (es decir, direcciones de correo electrónico) del perfil de ese canal.
   * **[!UICONTROL Identidad]**: la exclusión se aplica a los mensajes futuros enviados al destinatario específico (es decir, la dirección de correo electrónico) que se esté utilizando para el mensaje actual.
   * **[!UICONTROL Suscripción]**: la exclusión se aplica a mensajes futuros asociados a una lista de suscripción específica. Esta opción solo se puede seleccionar si el mensaje actual está asociado con una lista de suscripción.

1. Guarde los cambios.

Una vez que el mensaje se envía a través de un [recorrido](../building-journeys/journey.md), si un destinatario hace clic en el vínculo de no participación, su perfil se excluye inmediatamente.

## Vínculo &quot;Cancelar la suscripción&quot;  en el encabezado del correo electrónico {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Agregar vínculo &quot;Cancelar la suscripción&quot; al encabezado del correo electrónico"
>abstract="Active Cancelar la suscripción a una lista para agregar el vínculo &quot;Cancelar la suscripción&quot; al encabezado del correo electrónico. Para establecer la URL &quot;Cancelar la suscripción&quot;, inserte un vínculo de no participación de un solo clic en el contenido del correo electrónico."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=es#one-click-opt-out" text="Opción de exclusión en un clic"

Si la [opción Cancelar la suscripción a una lista](../configuration/channel-surfaces.md#list-unsubscribe) se activa en el nivel de superficie de canal, los correos electrónicos correspondientes enviados con [!DNL Journey Optimizer] incluirán el vínculo &quot;Cancelar la suscripción&quot; en el encabezado del correo electrónico.

Por ejemplo, el vínculo &quot;Cancelar la suscripción&quot; se mostrará en Gmail de la siguiente manera:

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>Para mostrar el vínculo &quot;Cancelar la suscripción&quot; en el encabezado del correo electrónico, el cliente de correo electrónico de los destinatarios debe admitir esta función.

La dirección &quot;Cancelar la suscripción&quot; es la dirección predeterminada **[!UICONTROL Mailto (cancelación de suscripción)]** mostrada en la superficie de canal correspondiente. [Más información](../configuration/channel-surfaces.md#list-unsubscribe).

Para establecer la URL &quot;Cancelar la suscripción&quot; personalizada, inserte un vínculo de no participación de un solo clic en el contenido del mensaje de correo electrónico e introduzca la URL que elija. [Más información](#one-click-opt-out)

Según el cliente de correo electrónico, hacer clic en el vínculo de cancelación de suscripción del encabezado puede tener uno de los siguientes impactos:

* La solicitud de cancelar la suscripción se envía a la dirección de cancelación de suscripción predeterminada.

* El destinatario se dirige a la dirección URL de la página de aterrizaje que especificó al agregar el vínculo de no participación al mensaje.

   >[!NOTE]
   >
   >Si no agrega un vínculo de no participación de un clic al contenido del mensaje, no se mostrará ninguna página de aterrizaje.

* El perfil correspondiente se excluye inmediatamente y esta opción se actualiza en Experience Platform. Obtenga más información en la [documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=es#getting-started){target="_blank"}.
