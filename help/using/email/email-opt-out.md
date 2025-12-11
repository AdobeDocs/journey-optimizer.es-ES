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
source-git-commit: b1d262723b68083d1a32d259f3974a287f898579
workflow-type: tm+mt
source-wordcount: '1031'
ht-degree: 26%

---

# Administración de exclusión de correo electrónico {#email-opt-out}

Al enviar mensajes desde recorridos o campañas, siempre debe asegurarse de que los clientes puedan cancelar la suscripción a comunicaciones futuras. Una vez cancelada la suscripción, los perfiles se eliminan automáticamente de la audiencia de futuros mensajes de marketing.  [Más información acerca de la administración de la privacidad y la exclusión](../privacy/opt-out.md)

>[!NOTE]
>
>Todos los mensajes de marketing deben incluir un vínculo de no participación. Esto no es necesario para los mensajes transaccionales. La categoría del mensaje **[!UICONTROL Marketing]** o **[!UICONTROL Transaccional]**- se define en el nivel de [configuración de canal](email-settings.md#email-type) y durante la creación del mensaje.

Para insertar un vínculo de baja en el contenido del correo electrónico, puede:

* Añada una URL de cancelación de suscripción de un clic en el encabezado del correo electrónico. La opción **[!UICONTROL Habilitar cancelación de suscripción a una lista]** en el nivel de configuración de canal agrega un vínculo de no participación al encabezado del correo electrónico. [Obtenga más información acerca de la exclusión en el encabezado del correo electrónico](#unsubscribe-header)

* Habilite el **vínculo de no participación de un clic** para su correo electrónico.  [Aprenda a agregar un vínculo de no participación de un clic](#one-click-opt-out)

* Insertar un **vínculo a una página de aterrizaje**. [Aprenda a agregar una página de aterrizaje de exclusión](#opt-out-external-lp)

Cuando un destinatario hace clic en el vínculo de no participación, su solicitud de cancelación de suscripción se procesa en consecuencia.

Para comprobar que se ha actualizado la opción del perfil correspondiente, vaya a Experience Platform y [busque ese perfil](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide?lang=en#browse-tab){target="_blank"}. En la ficha [Atributos](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide#attributes){target="_blank"}, puede ver que el valor de **[!UICONTROL choice]** ha cambiado a **[!UICONTROL no]**. Obtenga más información sobre el procesamiento del consentimiento en la [documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/consent/adobe/overview.html?lang=es){target="_blank"}.

![](assets/opt-out-profile-choice.png)

>[!NOTE]
>
>En ocasiones, los eventos de cancelación de suscripción pueden tardar más en reflejarse en el nivel de perfil debido al procesamiento de datos descendente. Espere un poco para que se actualice el sistema.

## Opción de exclusión en un solo paso {#opt-out-one-step}

Con [!DNL Adobe Journey Optimizer], puede configurar sus [opciones de configuración del correo electrónico](email-settings.md#list-unsubscribe) con una dirección de correo electrónico de cancelación de suscripción y cancelación de suscripción generada automáticamente con un solo clic en el encabezado del correo electrónico, o incluir una dirección URL de exclusión con un solo clic en el cuerpo del correo electrónico.

### URL de cancelación de suscripción de un solo clic en el encabezado del correo electrónico {#unsubscribe-header}

La URL &quot;Cancelar la suscripción&quot; de una lista con un solo clic es un vínculo o botón &quot;Cancelar la suscripción&quot; que se muestra junto a la información del remitente del correo electrónico y permite a los destinatarios excluirse instantáneamente de sus listas de correo con un solo clic. Aprenda a administrar la opción **[!UICONTROL Cancelar la suscripción a la lista]** en [esta sección](list-unsubscribe.md).

### Exclusión con un clic del contenido del correo electrónico {#one-click-opt-out}

Para establecer una URL de cancelación de suscripción personalizada, inserte un vínculo de no participación de un solo clic en el contenido del mensaje de correo electrónico e introduzca la URL que elija, como se describe a continuación:

1. Acceda al contenido de su correo electrónico e [inserte un vínculo](../email/message-tracking.md#insert-links).
1. Seleccione **[!UICONTROL Exclusión con un clic]** como tipo de vínculo.

   ![](assets/message-tracking-opt-out.png)

1. Introduzca la URL de la página de aterrizaje a la que se redirigirá al usuario una vez cancelada la suscripción. Esta página está aquí para confirmar que la exclusión se ha realizado correctamente.

   >[!NOTE]
   >
   >Si habilitó la opción **[!UICONTROL Cancelar la suscripción a una lista]** en el nivel de configuración de [canal](email-settings.md#list-unsubscribe) y tiene la opción predeterminada **[!UICONTROL Cancelar la suscripción mediante un solo clic]** desactivada, esta dirección URL de la página de aterrizaje también se usa cuando los usuarios hacen clic en el vínculo de cancelación de suscripción en el encabezado del correo electrónico. [Más información](list-unsubscribe.md)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Puede personalizar los vínculos. Obtenga más información acerca de las direcciones URL personalizadas en [esta sección](../personalization/personalization-syntax.md).

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

Para configurar un mecanismo de exclusión de dos pasos, debe crear sus propias páginas de aterrizaje de baja. La primera página de aterrizaje se vinculará desde el mensaje y debe contener un botón call-to-action. Se debe mostrar un mensaje de confirmación cuando el usuario haga clic en el botón.

Aprenda a crear una página de aterrizaje en Adobe Journey Optimizer para administrar las bajas de suscripción en [esta página](../landing-pages/lp-use-cases.md#opt-out).

También puede utilizar una página de aterrizaje externa. En ese caso, configure la API para enviar la información a Adobe Journey Optimizer cuando un destinatario haya cancelado la suscripción.

+++ Obtenga información sobre cómo implementar una llamada de API de exclusión

Para que los destinatarios se excluyan cuando envíen su elección desde la página de aterrizaje, debe implementar una **Llamada de API de suscripción** a través de [Adobe Developer](https://developer.adobe.com){target="_blank"} para actualizar las preferencias de los perfiles correspondientes.

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

   En el campo de **[!UICONTROL Vínculo]**, pegue el vínculo a la página de destino de terceros.

   ![](assets/opt-out-link-url.png)

1. Haga clic en **[!UICONTROL Guardar]**.


### Enviar el mensaje con el vínculo &quot;Cancelar la suscripción&quot; {#send-message-unsubscribe-link}

Una vez configurado el vínculo &quot;Cancelar la suscripción&quot; a la página de aterrizaje, puede crear y enviar el mensaje.

1. Configure el mensaje con un vínculo de baja y envíelo a sus suscriptores.

1. Una vez recibido el mensaje, si el destinatario hace clic en el vínculo para cancelar la suscripción, se muestra la página de destino.

   ![](assets/opt-out-lp-example.png)

   >[!WARNING]
   >
   >Al hacer clic en el vínculo unsubscribe del correo electrónico, solo se abre la página de aterrizaje. El destinatario debe **enviar el formulario haciendo clic en el botón de exclusión de la página de aterrizaje** para completar la cancelación de la suscripción y actualizar el consentimiento de su perfil.

1. Si el destinatario envía el formulario (aquí, pulsando el botón **[!UICONTROL Cancelar la suscripción]** de la página de aterrizaje), los datos de perfil se actualizan mediante la llamada de API.

1. El destinatario excluido se redirige a la pantalla de mensaje de confirmación para indicar que la exclusión se ha realizado correctamente.

   ![](assets/opt-out-confirmation-example.png)

   Como resultado, este usuario no recibirá comunicaciones de su marca a menos que se vuelva a suscribir.

