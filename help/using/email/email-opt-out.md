---
solution: Journey Optimizer
product: journey optimizer
title: Administración de exclusión de correo electrónico
description: Obtenga información sobre cómo administrar la exclusión con correos electrónicos
feature: Email Design, Consent Management
topic: Content Management
role: User
level: Intermediate
keywords: exclusión, correo electrónico, vínculo, cancelación de suscripción
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: f916d91ffd2c41261612f2127f35c41275c9d013
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 26%

---

# Administración de exclusión de correo electrónico {#email-opt-out}

Al enviar mensajes desde recorridos o campañas, siempre debe asegurarse de que los clientes puedan cancelar la suscripción a comunicaciones futuras. Una vez cancelada la suscripción, los perfiles se eliminan automáticamente de la audiencia de futuros mensajes de marketing.  [Más información sobre la administración de la privacidad y la exclusión](../privacy/opt-out.md)

>[!NOTE]
>
>Todos los mensajes de marketing deben incluir un vínculo de no participación. Esto no es necesario para los mensajes transaccionales. La categoría del mensaje **[!UICONTROL Marketing]** o **[!UICONTROL Transaccional]**- se define en el nivel de [configuración de canal](../configuration/channel-surfaces.md#email-type) y durante la creación del mensaje.

Para insertar un vínculo de baja en el contenido del correo electrónico, puede:

* Añada una URL de cancelación de suscripción de un clic en el encabezado del correo electrónico. La opción **[!UICONTROL Habilitar cancelación de suscripción a una lista]** en el nivel de configuración de canal agrega un vínculo de no participación al encabezado del correo electrónico. [Obtenga más información sobre la exclusión en el encabezado del correo electrónico](#unsubscribe-header)

* Habilite el **vínculo de no participación de un clic** para su correo electrónico.  [Aprenda a agregar un vínculo de no participación de un clic](#one-click-opt-out)

* Insertar un **vínculo a una página de aterrizaje**. [Aprenda a agregar una página de aterrizaje de exclusión](#opt-out-external-lp)


## Opción de exclusión en un solo paso {#opt-out-one-step}

Con [!DNL Adobe Journey Optimizer], puede configurar sus [opciones de configuración del correo electrónico](email-settings.md#list-unsubscribe) con una dirección de correo electrónico de cancelación de suscripción y cancelación de suscripción generada automáticamente con un solo clic en el encabezado del correo electrónico, o incluir una dirección URL de exclusión con un solo clic en el cuerpo del correo electrónico.

Cuando un destinatario hace clic en el vínculo de no participación de un solo clic, la solicitud de cancelación de suscripción de ese destinatario se procesa en consecuencia.

### URL de cancelación de suscripción de un solo clic en el encabezado del correo electrónico {#unsubscribe-header}

<!--Do not modify - Legal Review Done -->

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Añadir una URL de cancelación de suscripción a los correos electrónicos"
>abstract="Habilite Cancelación de suscripción a lista para añadir un vínculo de cancelación de suscripción al encabezado del correo electrónico. También puede establecer una URL de cancelación de suscripción en un mensaje, insertando un vínculo de no participación con un solo clic en el contenido del correo electrónico."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/channels/email/email-opt-out#one-click-opt-out" text="Exclusión con un clic del contenido del correo electrónico"
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/channels/email/email-opt-out#one-click-opt-out" text="Habilitar cancelación de suscripción a lista en la configuración de correo electrónico"

La URL &quot;Cancelar la suscripción&quot; de una lista con un solo clic es un vínculo o botón &quot;Cancelar la suscripción&quot; que se muestra junto a la información del remitente del correo electrónico y permite a los destinatarios excluirse instantáneamente de sus listas de correo con un solo clic.

En [!DNL Adobe Journey Optimizer], cuando la opción **Habilitar cancelación de suscripción a una lista** está activada, el encabezado del correo electrónico incluye un mailto y/o una URL de forma predeterminada que los destinatarios pueden usar para cancelar la suscripción a su lista de correo.

La opción [Habilitar cancelación de suscripción a una lista](email-settings.md#list-unsubscribe) debe activarse en el nivel de configuración de canal para que los correos electrónicos que usen esta configuración incluyan la URL de cancelación de suscripción de un solo clic en el encabezado del correo electrónico.

>[!NOTE]
>
>Para mostrar la URL &quot;Cancelar la suscripción&quot; con un solo clic en el encabezado del correo electrónico, el cliente de correo electrónico de los destinatarios debe admitir esta función.


Por ejemplo, la URL &quot;Cancelar la suscripción&quot; con un solo clic muestra el siguiente vínculo en Gmail:

![](assets/unsubscribe-header.png)


<!--With Adobe Journey Optimizer, you can configure your email configuration settings with an auto-generated one-click unsubscribe URL and mailto address in the email header, or include a one-click opt-out URL in your email body: when a recipient clicks the one-click opt-out link, recipient's unsubscribe request is processed accordingly.-->

<!--
>[!AVAILABILITY]
>
>One-click Unsubscribe URL Header will be available in Adobe Journey Optimizer starting June 3, 2024.
>
-->

Según el cliente de correo electrónico y la [configuración de correo electrónico para la cancelación de la suscripción](email-settings.md#list-unsubscribe), hacer clic en el vínculo de cancelación de suscripción en el encabezado del correo electrónico puede tener los siguientes impactos:

* Cuando la característica **Mailto (cancelar la suscripción)** está habilitada, la solicitud de cancelación de suscripción se envía a la dirección de cancelación de suscripción predeterminada según el subdominio que haya configurado.
* Cuando la función **Cancelar la suscripción con un solo clic** está habilitada (o si insertó una URL de cancelación de suscripción en el contenido del cuerpo del correo electrónico), el destinatario se excluye directamente, ya sea en el nivel de canal o en el nivel de ID (según cómo se configure el consentimiento), cuando el destinatario hace clic en la URL de cancelación de suscripción con un solo clic (según el subdominio que haya configurado).

![](../email/assets/surface-list-unsubscribe-mailto.png){width="80%"}

En ambos casos, el perfil correspondiente del destinatario se excluye inmediatamente y esta opción se actualiza en Experience Platform. Obtenga más información en la [documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=es#getting-started){target="_blank"}.

Si ha activado la opción **[!UICONTROL Habilitar cancelación de suscripción a una lista]** en la [configuración de correo electrónico](email-settings.md#list-unsubscribe), le recomendamos que habilite ambos métodos: **Mailto (cancelación de suscripción)** y **URL de cancelación de suscripción con un solo clic**. No todos los clientes de correo electrónico admiten el método HTTP. Con la función de cancelación de suscripción a una lista Mailto que se proporciona para que seleccione una alternativa, su reputación de remitente puede estar mejor protegida y todos sus destinatarios pueden tener acceso para utilizar la funcionalidad de cancelación de suscripción. [Más información](email-settings.md#list-unsubscribe)


### Exclusión con un clic del contenido del correo electrónico {#one-click-opt-out}

Para establecer una URL de cancelación de suscripción personalizada, inserte un vínculo de no participación de un solo clic en el contenido del mensaje de correo electrónico e introduzca la URL que elija, como se describe a continuación:

1. Acceda al contenido de su correo electrónico e [inserte un vínculo](../email/message-tracking.md#insert-links).
1. Seleccione **[!UICONTROL Exclusión con un clic]** como tipo de vínculo.

   ![](assets/message-tracking-opt-out.png)

1. Introduzca la URL de la página de aterrizaje a la que se redirigirá al usuario una vez cancelada la suscripción. Esta página está aquí para confirmar que la exclusión se ha realizado correctamente.

   >[!NOTE]
   >
   >Si habilitó la opción **[!UICONTROL Cancelar la suscripción a una lista]** en el nivel de configuración de [canal](email-settings.md#list-unsubscribe) y tiene la opción predeterminada **[!UICONTROL Cancelar la suscripción mediante un solo clic]** desactivada, esta dirección URL de la página de aterrizaje también se usa cuando los usuarios hacen clic en el vínculo de cancelación de suscripción en el encabezado del correo electrónico. [Más información](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Puede personalizar los vínculos. Obtenga más información sobre las URL personalizadas en [esta sección](../personalization/personalization-syntax.md).

1. Seleccione cómo desea aplicar la exclusión: en el nivel de canal o de identidad.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Canal]**: la exclusión se aplica a mensajes futuros enviados al destinatario del perfil (es decir, la dirección de correo electrónico) para el canal actual. Si hay varios objetivos asociados a un perfil, la exclusión se aplica a todos los destinatarios (es decir, direcciones de correo electrónico) del perfil de ese canal.
   * **[!UICONTROL Identidad]**: la exclusión se aplica a los mensajes futuros enviados al destinatario específico (es decir, la dirección de correo electrónico) que se esté utilizando para el mensaje actual.
     <!--* **[!UICONTROL Subscription]**: The opt-out applies to future messages associated with a specific subscription list. This option can only be selected if the current message is associated with a subscription list.-->

1. Guarde los cambios.


## Opción de exclusión en dos pasos {#opt-out-external-lp}

El mecanismo de exclusión estándar se basa en dos pasos: el suscriptor hace clic en el vínculo de exclusión en un mensaje de correo electrónico y, a continuación, se le redirige a una página de aterrizaje de exclusión para confirmar su baja.

Para implementar este modo de baja, debe crear y publicar una página de aterrizaje de exclusión y agregar un vínculo de baja en los mensajes de correo electrónico, con un vínculo a la página de aterrizaje. Estos pasos se describen a continuación.


### Requisitos previos {#prereq-lp}

Para configurar un mecanismo de exclusión de dos pasos, debe crear sus propias páginas de aterrizaje de baja. La primera página de aterrizaje se vinculará desde el mensaje y debe contener un botón de llamada a la acción. Se debe mostrar un mensaje de confirmación cuando el usuario haga clic en el botón.

Aprenda a crear una página de aterrizaje en Adobe Journey Optimizer para administrar las bajas de suscripción en [esta página](../landing-pages/lp-use-cases.md#opt-out).

También puede utilizar una página de aterrizaje externa. En ese caso, configure la API para enviar la información a Adobe Journey Optimizer cuando un destinatario haya cancelado la suscripción.

+++ Obtenga información sobre cómo implementar una llamada de API de exclusión

Para que los destinatarios se excluyan cuando envíen su elección desde la página de aterrizaje, debe implementar una **llamada de API de suscripción** a través de [Adobe Developer](https://developer.adobe.com){target="_blank"} para actualizar las preferencias de los perfiles correspondientes.

Esta llamada de POST es como sigue:

Punto final: https://platform.adobe.io/journey/imp/consent/preferences

Parámetros de consulta:

* **params**: contiene la carga útil cifrada
* **pid**: ID de perfil cifrado

Estos dos parámetros se incluyen en la dirección URL de la página de aterrizaje de terceros que se envía al destinatario:

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

[!DNL Journey Optimizer] utiliza estos parámetros para actualizar la elección del perfil correspondiente a través de la llamada de API [Adobe Developer](https://developer.adobe.com){target="_blank"}.

+++


### Agregar el vínculo &quot;Cancelar la suscripción&quot; {#add-unsubscribe-link}

Primero debe agregar el vínculo &quot;Cancelar la suscripción&quot; a un mensaje. Para realizar esto, siga los pasos a continuación:

1. Cree un mensaje e [inserte un vínculo](../email/message-tracking.md#insert-links) utilizando la barra de herramientas contextual.

   ![](assets/opt-out-insert-link.png)

1. Seleccione la **[!UICONTROL página de aterrizaje]** de la lista desplegable **[!UICONTROL Tipo]** y seleccione la página de aterrizaje de exclusión en el campo **[!UICONTROL Página de aterrizaje]**.

   Si está usando una página de aterrizaje externa, seleccione **[!UICONTROL Exclusión/baja externa]** de la lista desplegable **[!UICONTROL Tipo]**.

   ![](assets/opt-out-link-type.png)

   En el campo de **[!UICONTROL Vínculo]**, pegue el vínculo a la página de aterrizaje de terceros.

   ![](assets/opt-out-link-url.png)

1. Haga clic en **[!UICONTROL Guardar]**.


### Enviar el mensaje con el vínculo &quot;Cancelar la suscripción&quot; {#send-message-unsubscribe-link}

Una vez configurado el vínculo &quot;Cancelar la suscripción&quot; a la página de aterrizaje, puede crear y enviar el mensaje.

1. Configure el mensaje con un vínculo de baja y envíelo a sus suscriptores.

1. Una vez recibido el mensaje, si el destinatario hace clic en el vínculo para cancelar la suscripción, se muestra la página de aterrizaje.

   ![](assets/opt-out-lp-example.png)

1. Si el destinatario envía el formulario (aquí, pulsando el botón **[!UICONTROL Cancelar la suscripción]** de la página de aterrizaje), los datos de perfil se actualizan mediante la llamada de API.

1. El destinatario excluido se redirige a la pantalla de mensaje de confirmación para indicar que la exclusión se ha realizado correctamente.

   ![](assets/opt-out-confirmation-example.png)

   Como resultado, este usuario no recibirá comunicaciones de su marca a menos que se vuelva a suscribir.

1. Para comprobar que se ha actualizado la opción del perfil correspondiente, vaya a Experience Platform y acceda al perfil seleccionando un área de nombres de identidad y un valor de identidad correspondiente. Obtenga más información en la [documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=es#getting-started){target="_blank"}.

   ![](assets/opt-out-profile-choice.png)

   En la pestaña **[!UICONTROL Atributos]**, puede ver que el valor de **[!UICONTROL elección]** ha cambiado a **[!UICONTROL no]**.

