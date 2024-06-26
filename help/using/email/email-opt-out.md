---
solution: Journey Optimizer
product: journey optimizer
title: Administración de exclusión de correo electrónico
description: Obtenga información sobre cómo administrar la exclusión con correos electrónicos
feature: Email Design, Privacy
topic: Content Management
role: User
level: Intermediate
keywords: exclusión, correo electrónico, vínculo, cancelación de suscripción
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: 38496b93f073c0e9cb208b0c62e6c4cb8a2d8c03
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 26%

---

# Administración de exclusión de correo electrónico {#email-opt-out}

Al enviar mensajes desde recorridos o campañas, siempre debe asegurarse de que los clientes puedan cancelar la suscripción a comunicaciones futuras. Una vez cancelada la suscripción, los perfiles se eliminan automáticamente de la audiencia de futuros mensajes de marketing.  [Más información sobre la administración de la privacidad y la exclusión](../privacy/opt-out.md)

>[!NOTE]
>
>Todos los mensajes de marketing deben incluir un vínculo de no participación. Esto no es necesario para los mensajes transaccionales. La categoría del mensaje - **[!UICONTROL Marketing]** o **[!UICONTROL Transaccional]** - se define en el [superficie de canal](../configuration/channel-surfaces.md#email-type) y al crear el mensaje.

Para insertar un vínculo de baja en el contenido del correo electrónico, puede:

* Añada una URL de cancelación de suscripción de un clic en el encabezado del correo electrónico. Activación de la **[!UICONTROL Encabezado List-Unsubscribe]** en el nivel de superficie de canal agrega un vínculo de no participación en el encabezado del correo electrónico. [Obtenga más información sobre la exclusión en el encabezado del correo electrónico](#unsubscribe-header)

* Habilite la **vínculo de no participación de un clic** para su correo electrónico.  [Obtenga información sobre cómo añadir un vínculo de no participación de un clic](#one-click-opt-out)

* Inserte una **vínculo a una página de aterrizaje**. [Obtenga información sobre cómo añadir una página de aterrizaje de exclusión](#opt-out-external-lp)


## Opción de exclusión en un paso {#opt-out-one-step}

### URL de cancelación de suscripción de un clic en el encabezado del correo electrónico {#unsubscribe-header}

<!--Do not modify - Legal Review Done -->

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Añadir URL de cancelación de suscripción en el encabezado del correo electrónico"
>abstract="Active el encabezado Cancelación de suscripción a una lista para agregar una URL de cancelación de suscripción en el encabezado del correo electrónico. Para establecer la URL &quot;Cancelar la suscripción&quot;, inserte un vínculo de no participación de un solo clic en el contenido del correo electrónico."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=es#one-click-opt-out" text="Opción de exclusión en un clic"

La URL &quot;Cancelar la suscripción&quot; de una lista de un clic es un vínculo o botón &quot;Cancelar la suscripción&quot; que se muestra junto a la información del remitente del correo electrónico y permite a los destinatarios excluirse instantáneamente de sus listas de correo con un solo clic. En Adobe Journey Optimizer, cuando la variable **Habilitar cancelación de suscripción a lista** está activada, el encabezado del correo electrónico incluye un mailto y/o una URL de forma predeterminada que los destinatarios pueden utilizar para cancelar la suscripción a su lista de correo.

El [Habilitar cancelación de suscripción a lista](email-settings.md#list-unsubscribe) La opción debe activarse en el nivel de superficie de canal para que los correos electrónicos que utilicen esta superficie incluyan la URL de cancelación de suscripción de un solo clic en el encabezado del correo electrónico.

>[!NOTE]
>
>Para mostrar la URL &quot;Cancelar la suscripción&quot; con un solo clic en el encabezado del correo electrónico, el cliente de correo electrónico de los destinatarios debe admitir esta función.


Por ejemplo, la URL &quot;Cancelar la suscripción&quot; de un solo clic muestra un vínculo &quot;Cancelar la suscripción&quot; como este en Gmail:

![](assets/unsubscribe-header.png)


Con Adobe Journey Optimizer, puede configurar la superficie del correo electrónico con una dirección URL &quot;Cancelar la suscripción&quot; y &quot;Enviar para&quot; generadas automáticamente con un solo clic en el encabezado del correo electrónico, o incluir una URL de exclusión de un solo clic en el cuerpo del correo electrónico: cuando un destinatario hace clic en el vínculo de no participación de un clic, la solicitud de cancelación de suscripción del destinatario se procesa en consecuencia.

<!--
>[!AVAILABILITY]
>
>One-click Unsubscribe URL Header will be available in Adobe Journey Optimizer starting June 3, 2024.
>
-->

Según el cliente de correo electrónico y la variable [configuración de baja de superficie de correo electrónico](email-settings.md#list-unsubscribe), hacer clic en el vínculo unsubscribe en el encabezado del correo electrónico puede tener los siguientes impactos:

* Si la variable **Mailto (cancelar la suscripción)** Cuando esta función está habilitada, la solicitud de cancelación de suscripción se envía a la dirección de cancelación de suscripción predeterminada en función del subdominio que haya creado.
* Si la variable **URL de cancelación de suscripción de un clic** Esta función la habilita usted (o si ha insertado una URL de baja en el contenido del cuerpo del correo electrónico), el destinatario se excluye directamente, ya sea en el nivel de canal o en el nivel de ID (según cómo se configure el consentimiento), cuando el destinatario hace clic en la URL de cancelación de suscripción de un solo clic, que se basa en el subdominio creado por usted.

En ambos casos, el perfil correspondiente del destinatario se excluye inmediatamente y esta opción se actualiza en Experience Platform. Obtenga más información en la [Documentación del Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=es#getting-started){target="_blank"}.

Si ha activado la **[!UICONTROL Habilitar cancelación de suscripción a lista]** en cuanto al encabezado Cancelar la suscripción a la lista, le recomendamos que habilite ambos métodos: **Mailto (cancelar la suscripción)** y **URL de cancelación de suscripción de un clic**. No todos los clientes de correo electrónico admiten el método HTTP. Con la función de cancelación de suscripción a una lista de Mailto proporcionada como funcionalidad para que usted seleccione una alternativa, su reputación de remitente puede estar mejor protegida y todos sus destinatarios pueden tener acceso para utilizar la funcionalidad de cancelación de suscripción. [Más información](email-settings.md#list-unsubscribe)


### Exclusión en un clic del contenido del correo electrónico {#one-click-opt-out}

Para establecer una URL de cancelación de suscripción personalizada, inserte un vínculo de no participación de un solo clic en el contenido del mensaje de correo electrónico e introduzca la URL que elija, como se describe a continuación:

1. Acceda al contenido de su correo electrónico y [insertar un vínculo](../email/message-tracking.md#insert-links).
1. Seleccionar **[!UICONTROL Exclusión en un clic]** como tipo de vínculo.

   ![](assets/message-tracking-opt-out.png)

1. Introduzca la URL de la página de aterrizaje a la que se redirigirá al usuario una vez cancelada la suscripción. Esta página está aquí para confirmar que la exclusión se ha realizado correctamente.

   >[!NOTE]
   >
   >Si habilitó la variable **[!UICONTROL Cancelación de suscripción a lista]** opción en la [nivel de superficie de canal](email-settings.md#list-unsubscribe) y tienen la opción predeterminada de URL de exclusión en un clic desactivada, se utiliza esta URL cuando los usuarios hacen clic en el vínculo de cancelación de suscripción en el encabezado del correo electrónico. [Más información](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Puede personalizar los vínculos. Obtenga más información sobre las URL personalizadas en [esta sección](../personalization/personalization-syntax.md).

1. Seleccione cómo desea aplicar la exclusión: en el nivel de canal, identidad o suscripción.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Canal]**: la exclusión se aplica a mensajes futuros enviados al destinatario del perfil (es decir, la dirección de correo electrónico) para el canal actual. Si hay varios objetivos asociados a un perfil, la exclusión se aplica a todos los destinatarios (es decir, direcciones de correo electrónico) del perfil de ese canal.
   * **[!UICONTROL Identidad]**: la exclusión se aplica a los mensajes futuros enviados al destinatario específico (es decir, la dirección de correo electrónico) que se esté utilizando para el mensaje actual.
   * **[!UICONTROL Suscripción]**: la exclusión se aplica a mensajes futuros asociados a una lista de suscripción específica. Esta opción solo se puede seleccionar si el mensaje actual está asociado con una lista de suscripción.

1. Guarde los cambios.



## Opción de exclusión en dos pasos {#opt-out-external-lp}

El mecanismo de exclusión estándar se basa en dos pasos: el suscriptor hace clic en el vínculo de exclusión en un mensaje de correo electrónico y, a continuación, se le redirige a una página de aterrizaje de exclusión para confirmar su baja.

Para implementar este modo de baja, debe crear y publicar una página de aterrizaje de exclusión y agregar un vínculo de baja en los mensajes de correo electrónico, con un vínculo a la página de aterrizaje. Estos pasos se describen a continuación.


### Requisitos previos {#prereq-lp}

Para configurar un mecanismo de exclusión de dos pasos, debe crear sus propias páginas de aterrizaje de baja. La primera página de aterrizaje se vinculará desde el mensaje y debe contener un botón de llamada a la acción. Se debe mostrar un mensaje de confirmación cuando el usuario haga clic en el botón.

Obtenga información sobre cómo crear una página de aterrizaje en Adobe Journey Optimizer para administrar bajas en [esta página](../landing-pages/lp-use-cases.md#opt-out).

También puede utilizar una página de aterrizaje externa. En ese caso, configure la API para enviar la información a Adobe Journey Optimizer cuando un destinatario haya cancelado la suscripción.

+++ Obtenga información sobre cómo implementar una llamada de API de exclusión

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

[!DNL Journey Optimizer] utiliza estos parámetros para actualizar la elección del perfil correspondiente a través de [Adobe Developer](https://developer.adobe.com){target="_blank"} Llamada de API.

+++


### Agregar el vínculo &quot;Cancelar la suscripción&quot; {#add-unsubscribe-link}

Primero debe agregar el vínculo &quot;Cancelar la suscripción&quot; a un mensaje. Para realizar esto, siga los pasos a continuación:

1. Cree un mensaje y [insertar un vínculo](../email/message-tracking.md#insert-links) uso de la barra de herramientas contextual.

   ![](assets/opt-out-insert-link.png)

1. Seleccione el **[!UICONTROL Página de aterrizaje]** desde el **[!UICONTROL Tipo]** y seleccione la página de aterrizaje de exclusión en la lista desplegable **[!UICONTROL Página de aterrizaje]** field.

   Si utiliza una página de aterrizaje externa, seleccione **[!UICONTROL Exclusión/baja externa]** desde el **[!UICONTROL Tipo]** lista desplegable.

   ![](assets/opt-out-link-type.png)

   En el campo de **[!UICONTROL Vínculo]**, pegue el vínculo a la página de aterrizaje de terceros.

   ![](assets/opt-out-link-url.png)

1. Haga clic en **[!UICONTROL Guardar]**.


### Enviar el mensaje con el vínculo &quot;Cancelar la suscripción&quot; {#send-message-unsubscribe-link}

Una vez configurado el vínculo &quot;Cancelar la suscripción&quot; a la página de aterrizaje, puede crear y enviar el mensaje.

1. Configure el mensaje con un vínculo de baja y envíelo a sus suscriptores.

1. Una vez recibido el mensaje, si el destinatario hace clic en el vínculo para cancelar la suscripción, se muestra la página de aterrizaje.

   ![](assets/opt-out-lp-example.png)

1. Si el destinatario envía el formulario: aquí, pulsando la tecla **[!UICONTROL Cancelar suscripción]** en la página de aterrizaje: los datos de perfil se actualizan a través de la llamada de API.

1. El destinatario excluido se redirige a la pantalla de mensaje de confirmación para indicar que la exclusión se ha realizado correctamente.

   ![](assets/opt-out-confirmation-example.png)

   Como resultado, este usuario no recibirá comunicaciones de su marca a menos que se vuelva a suscribir.

1. Para comprobar que se ha actualizado la opción del perfil correspondiente, vaya a Experience Platform y acceda al perfil seleccionando un área de nombres de identidad y un valor de identidad correspondiente. Obtenga más información en la [Documentación del Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=es#getting-started){target="_blank"}.

   ![](assets/opt-out-profile-choice.png)

   En la pestaña **[!UICONTROL Atributos]**, puede ver que el valor de **[!UICONTROL elección]** ha cambiado a **[!UICONTROL no]**.

