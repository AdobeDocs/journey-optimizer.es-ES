---
title: Administración de la exclusión
description: Obtenga información sobre cómo administrar la exclusión y la privacidad
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 06a7abc2ada930356cbaf45ce01eed5e3156f2e3
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 98%

---

# Administración de la exclusión {#consent}

Utilice [!DNL Journey Optimizer] para hacer un seguimiento del consentimiento de los destinatarios para fines de comunicación y comprender cómo desean interactuar con su marca administrando sus preferencias y suscripciones.

Las regulaciones como el RGPD establecen que debe cumplir con requisitos específicos antes de poder utilizar la información de sujetos de datos. Además, estos deben poder modificar su consentimiento en cualquier momento.

**¿Por qué es importante?**

* El incumplimiento de estas regulaciones conlleva riesgos legales para su marca.
* Le ayuda a evitar enviar comunicaciones no solicitadas a sus destinatarios, lo que podría hacer que marquen sus mensajes como correo no deseado y dañar su reputación.

Obtenga más información sobre la administración de la privacidad y las regulaciones aplicables en la [Documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=es){target=&quot;_blank&quot;}.

## Administración de exclusiones {#opt-out-management}

Proporcionar a los destinatarios la capacidad de cancelar la suscripción a la recepción de comunicaciones de una marca es un requisito legal. Obtenga más información acerca de la legislación aplicable en la [Documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=es#regulations){target=&quot;_blank&quot;}.

Por lo tanto, siempre debe incluir un **enlace para cancelar la suscripción** en cada correo electrónico enviado a los destinatarios:

* Al hacer clic en este vínculo, los destinatarios se dirigen a una página de aterrizaje que incluye un botón para confirmar la exclusión.
* Al hacer clic en el botón de exclusión, se realiza una llamada de Adobe I/O para actualizar los datos de perfil con esta información. [Obtenga más información relacionada](#consent-service-api).

### Adición de un vínculo de no participación {#add-unsubscribe-link}

Para añadir un vínculo para cancelar la suscripción, siga los pasos a continuación:

1. Cree la página de aterrizaje de baja.

1. Alójelo en el sistema de terceros que elija.

1. [Cree un mensaje](create-message.md) en [!DNL Journey Optimizer].

1. Seleccione texto en el contenido e inserte un vínculo utilizando la barra de herramientas contextual.

   ![](assets/opt-out-insert-link.png)

1. Seleccione **[!UICONTROL Unsubscription link]** en la lista desplegable **[!UICONTROL Link type]**.

   ![](assets/opt-out-link-type.png)

1. En el campo **[!UICONTROL Link]**, copie el vínculo a la página de aterrizaje.

   ![](assets/opt-out-link-url.png)

1. Haga clic en **[!UICONTROL Save]**.

1. Guarde el contenido y [publique el mensaje](publish-manage-message.md).

   >[!NOTE]
   >
   >La dirección URL de la página de aterrizaje de terceros incluirá tres parámetros que se utilizarán para actualizar las preferencias de los perfiles mediante una llamada de Adobe I/O. [Obtenga más información en esta sección](#consent-service-api).

1. Envíe el mensaje con el enlace a su página de aterrizaje a través de un [recorrido](../building-journeys/journey.md).

1. Una vez recibido el mensaje, si el destinatario hace clic en el vínculo para cancelar la suscripción, se muestra la página de aterrizaje.

   ![](assets/opt-out-lp-example.png)

1. Si el destinatario hace clic en el botón de exclusión de la página de aterrizaje (en este caso, el botón **Cancelar la suscripción**), los datos de perfil se actualizan mediante una [llamada de Adobe I/O](#opt-out-api).

   El destinatario excluido se redirige a la pantalla de mensaje de confirmación para indicar que la exclusión se ha realizado correctamente.

   ![](assets/opt-out-confirmation-example.png)

   Como resultado, este usuario no recibirá comunicaciones de su marca a menos que se vuelva a suscribir.

Para comprobar que se ha actualizado la opción del perfil correspondiente, vaya a Experience Platform y acceda al perfil seleccionando un área de nombres de identidad y un valor de identidad correspondiente. Obtenga más información en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=es#getting-started){target=&quot;_blank&quot;}.

![](assets/opt-out-profile-choice.png)

En la pestaña **[!UICONTROL Attributes]**, puede ver que el valor de **[!UICONTROL choice]** ha cambiado a **[!UICONTROL no]**.

### Llamada de API de exclusión {#opt-out-api}

Una vez que el destinatario ha optado por darse de baja haciendo clic en el vínculo para cancelar la suscripción, se llama a una API de Adobe I/O  para actualizar la preferencia del perfil correspondiente.

Esta llamada del POST de Adobe I/O es la siguiente:

Extremo: platform.adobe.io/journey/imp/consent/preferences

Parámetros de consulta:

* **params**: contiene la carga útil cifrada
* **sig**: firma
* **pid**: ID de perfil cifrado

Estos parámetros están disponibles en el vínculo para cancelar la suscripción enviado a su destinatario; es decir, la dirección URL que abrirá la página de aterrizaje de terceros para un destinatario determinado:

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

[!DNL Journey Optimizer] utilizará estos parámetros para actualizar la opción del perfil correspondiente.

## Opción de exclusión en un clic {#one-click-opt-out}

Dado que muchos clientes buscan un proceso más sencillo para cancelar la suscripción, también puede añadir un vínculo de no participación en un solo clic al contenido del correo electrónico. Este vínculo permite a los destinatarios cancelar rápidamente la suscripción a sus comunicaciones, sin que se les redirija a una página de aterrizaje en la que tengan que confirmar la exclusión.

Aprenda a añadir un vínculo de no participación al contenido del mensaje en [esta sección](message-tracking.md#one-click-opt-out-link).

Una vez que el mensaje se envía a través de un [recorrido](../building-journeys/journey.md), si un destinatario hace clic en el vínculo de no participación, su perfil se excluye inmediatamente.

## Vínculo de cancelación de suscripción en el encabezado {#unsubscribe-email}

Si el cliente de correo electrónico de los destinatarios admite la visualización de un vínculo de cancelación de suscripción en el encabezado del correo electrónico, los correos electrónicos enviados con [!DNL Journey Optimizer] incluyen automáticamente este vínculo.

Por ejemplo, el vínculo de cancelación de suscripción se mostrará así en Gmail:

![](assets/unsubscribe-email.png)

Según el cliente de correo electrónico, hacer clic en el vínculo de cancelación de suscripción del encabezado tendrá uno de los siguientes impactos:

* El perfil correspondiente se excluye inmediatamente y esta opción se actualiza en Experience Platform. Obtenga más información en la [Documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

* Tiene el mismo efecto que hacer clic en el vínculo de cancelación de la suscripción del contenido del correo electrónico: se redirige al destinatario a una página de aterrizaje, que incluye un botón para confirmar la exclusión. Obtenga más información sobre la administración de exclusiones en [esta sección](#opt-out-management).

## Administración de exclusiones push {#push-opt-out-management}

Los destinatarios push pueden cancelar la suscripción a través de sus propios dispositivos.

Por ejemplo, al descargar o al usar la aplicación, pueden seleccionar detener las notificaciones. Del mismo modo, pueden cambiar la configuración de notificación a través del sistema operativo móvil.
