---
solution: Journey Optimizer
product: journey optimizer
title: Casos de uso de página de aterrizaje
description: Descubra los casos de uso más comunes con las páginas de aterrizaje en Journey Optimizer
feature: Landing Pages, Subscriptions
topic: Content Management
role: User
level: Intermediate
keywords: aterrizaje, página de aterrizaje, caso de uso
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: daba85693c4733333d6a62ebb5c1f290dbcb1511
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 12%

---

# Casos de uso de página de aterrizaje {#lp-use-cases}

A continuación se muestran algunos ejemplos de cómo puede utilizar [!DNL Journey Optimizer] páginas de aterrizaje para que sus clientes se excluyan de la recepción de algunas o todas sus comunicaciones.

## Suscripción a un servicio {#subscription-to-a-service}

Uno de los casos de uso más comunes consiste en invitar a sus clientes a [suscripción a un servicio](subscription-list.md) (como un boletín informativo o un evento) a través de una página de aterrizaje. Los pasos principales se presentan en el siguiente gráfico:

![](assets/lp_subscription-uc.png)

Por ejemplo, supongamos que organiza un evento el mes que viene y que desea iniciar una campaña de registro de eventos<!--to keep your customers that are interested updated on that event-->. Para ello, va a enviar un correo electrónico con un vínculo a una página de aterrizaje que permitirá a sus destinatarios registrarse en este evento. Los usuarios que se registren se agregarán a la lista de suscripción que haya creado para este fin.

### Configuración de una página de aterrizaje {#set-up-lp}

1. Cree la lista de suscripción del registro de eventos, que almacenará a los usuarios registrados. Obtenga información sobre cómo crear una lista de suscripción [aquí](subscription-list.md#define-subscription-list).

   ![](assets/lp_subscription-uc-list.png)

1. [Creación de una página de aterrizaje](create-lp.md) para permitir que los destinatarios se registren en el evento.

   ![](assets/lp_create-lp-details.png)

1. Configuración del registro [página de aterrizaje principal](create-lp.md#configure-primary-page).

1. Al diseñar el [contenido de página de aterrizaje](design-lp.md), seleccione la lista de suscripción que ha creado para actualizarla con los perfiles que marcan la casilla de verificación de registro.

   ![](assets/lp_subscription-uc-lp-list.png)

1. Cree una página de &quot;agradecimiento&quot; que se muestre a los destinatarios una vez que envíen el formulario de registro. Obtenga información sobre cómo configurar subpáginas de aterrizaje [aquí](create-lp.md#configure-subpages).

   ![](assets/lp_subscription-uc-thanks.png)

1. [Publish](create-lp.md#publish) la página de aterrizaje.

1. En un [recorrido](../building-journeys/journey.md), añada un **Correo electrónico** actividad para dirigir el tráfico a la página de aterrizaje de registro.

   ![](assets/lp_subscription-uc-journey.png)

1. [Diseño del correo electrónico](../email/get-started-email-design.md) para anunciar que el registro está abierto para su evento.

1. [Inserción de un vínculo](../email/message-tracking.md#insert-links) en el contenido del mensaje. Seleccionar **[!UICONTROL Página de aterrizaje]** como el **[!UICONTROL Tipo de vínculo]** y elija la [página de aterrizaje](create-lp.md#configure-primary-page) que creó para el registro.

   ![](assets/lp_subscription-uc-link.png)

   >[!NOTE]
   >
   >Para poder enviar el mensaje, asegúrese de que la página de aterrizaje seleccionada aún no haya caducado. Obtenga información sobre cómo actualizar la fecha de caducidad [en esta sección](create-lp.md#configure-primary-page).

   Una vez que reciban el correo electrónico, si los destinatarios hacen clic en el vínculo a la página de aterrizaje, se les dirigirá a la página &quot;gracias&quot; y se les añadirá a la lista de suscripción.

### Enviar un correo electrónico de confirmación {#send-confirmation-email}

Además, puede enviar un correo electrónico de confirmación a los destinatarios que se registraron en el evento. Para ello, siga los pasos que aparecen a continuación.

1. Crear otro [recorrido](../building-journeys/journey.md). Puede hacerlo directamente desde la página de aterrizaje haciendo clic en **[!UICONTROL Crear recorrido]** botón. [Más información](create-lp.md#configure-primary-page)

   ![](assets/lp_subscription-uc-create-journey.png)

1. Despliegue el **[!UICONTROL Eventos]** categoría y suelte un **[!UICONTROL Calificación de audiencias]** actividad en el lienzo. [Más información](../building-journeys/audience-qualification-events.md)

1. Haga clic en en **[!UICONTROL Audiencia]** y seleccione la lista de suscripción que ha creado.

   ![](assets/lp_subscription-uc-confirm-journey.png)

1. Añada un correo electrónico de confirmación de su elección y envíelo a través del recorrido.

   ![](assets/lp_subscription-uc-confirm-email.png)

Todos los usuarios que se hayan registrado en su evento recibirán el correo electrónico de confirmación.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## Exclusión {#opt-out}

Para permitir que los destinatarios cancelen su suscripción a las comunicaciones, puede incluir en sus correos electrónicos un vínculo a una página de aterrizaje de exclusión.

>[!NOTE]
>
>Obtenga más información sobre la administración del consentimiento de los destinatarios y por qué esto es importante en [esta sección](../privacy/opt-out.md).

### Administración de exclusiones {#opt-out-management}

Proporcionar a los destinatarios la capacidad de cancelar la suscripción a la recepción de comunicaciones de una marca es un requisito legal. Obtenga más información acerca de la legislación aplicable en la [Documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=es#regulations){target="_blank"}.

Por lo tanto, siempre debe incluir un **enlace para cancelar la suscripción** en cada correo electrónico enviado a los destinatarios:

* Al hacer clic en este vínculo, los destinatarios se dirigen a una página de aterrizaje que incluye un botón para confirmar la exclusión.
* Al hacer clic en el botón de exclusión, los datos de perfil se actualizan con esta información.

### Configuración de la exclusión de correo electrónico {#configure-opt-out}

Para permitir que los destinatarios de un correo electrónico cancelen su suscripción a las comunicaciones a través de una página de aterrizaje, siga los pasos a continuación.

1. Cree su página de aterrizaje. [Más información](create-lp.md)

1. Defina la página principal. [Más información](create-lp.md#configure-primary-page)

1. [Diseño](design-lp.md) el contenido de la página principal: utilice la página de aterrizaje específica **[!UICONTROL Form]** componente, definir un **[!UICONTROL Opción de exclusión]** y seleccione para actualizar **[!UICONTROL Canal (correo electrónico)]**: el perfil que marca la casilla de exclusión en la página de aterrizaje se excluirá de todas las comunicaciones.

   ![](assets/lp_opt-out-primary-lp.png)

   <!--You can also build your own landing page and host it on the third-party system of your choice.-->

1. Añadir una confirmación [subpágina](create-lp.md#configure-subpages) que se mostrarán a los usuarios que envíen el formulario.

   ![](assets/lp_opt-out-subpage.png)

   >[!NOTE]
   >
   >Asegúrese de hacer referencia a la subpágina en la página principal de **[!UICONTROL Llamada a la acción]** de la sección **[!UICONTROL Form]** componente. [Más información](design-lp.md)

1. Una vez configurado y definido el contenido de sus páginas, [publicar](create-lp.md#publish) la página de aterrizaje.

1. [Crear un mensaje de correo electrónico](../email/get-started-email-design.md) en un recorrido.

1. Seleccione texto en el contenido y [insertar un vínculo](../email/message-tracking.md#insert-links) uso de la barra de herramientas contextual. También puede utilizar un vínculo en un botón.

1. Seleccionar **[!UICONTROL Página de aterrizaje]** desde el **[!UICONTROL Tipo de vínculo]** y seleccione la opción [página de aterrizaje](create-lp.md#configure-primary-page) que ha creado para la exclusión.

   ![](assets/lp_opt-out-landing-page.png)

   >[!NOTE]
   >
   >Para poder enviar el mensaje, asegúrese de que la página de aterrizaje seleccionada aún no haya caducado. Obtenga información sobre cómo actualizar la fecha de caducidad [en esta sección](create-lp.md#configure-primary-page).

1. Publique y ejecute el recorrido. [Más información](../building-journeys/journey.md).

1. Una vez recibido el mensaje, si un destinatario hace clic en el vínculo para cancelar la suscripción del correo electrónico, se muestra la página de aterrizaje.

   ![](assets/lp_opt-out-submit-form.png)

   Si el destinatario marca la casilla y envía el formulario:

   * El destinatario excluido se redirige a la pantalla de mensaje de confirmación.

   * Los datos del perfil se actualizan y no recibirán comunicaciones de su marca a menos que se vuelva a suscribir.

Para comprobar que se ha actualizado la opción del perfil correspondiente, vaya a Experience Platform y acceda al perfil seleccionando un área de nombres de identidad y un valor de identidad correspondiente. Obtenga más información en la [Documentación del Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=es#getting-started){target="_blank"}.

![](assets/lp_opt-out-profile-choice.png)

En el **[!UICONTROL Atributos]** , puede ver que el valor de **[!UICONTROL elección]** ha cambiado a **[!UICONTROL no]**.

La información de exclusión se almacena en el **Conjunto de datos del servicio de consentimiento**. [Más información sobre los conjuntos de datos](../data/get-started-datasets.md)

>[!NOTE]
>
>Si el método de combinación para el [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"} **[!UICONTROL Perfiles]** la política de combinación es **[!UICONTROL Prioridad de conjuntos de datos]**, asegúrese de habilitar la variable **[!UICONTROL Conjunto de datos del servicio de consentimiento AJO]** y priorizarlo en la política de combinación. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#dataset-precedence-profile){target="_blank"}
>
>Incluso si no se han agregado lotes a este conjunto de datos, seguirá conteniendo la información de inclusión/exclusión.


<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../privacy/opt-out.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../privacy/opt-out.md#unsubscribe-header)

////////


## Leverage landing page submission event {#leverage-lp-event}

You can use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.

To do this, you need to create an event containing the landing page submission information and use it in a journey. Follow the steps below.

1. Go to **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**, and in the **[!UICONTROL Events]** section, select **[!UICONTROL Manage]**.

    ![](assets/lp_subscription-uc-configurations.png)

1. The list of events displays. Select **[!UICONTROL Create Event]**.

    ![](assets/lp_subscription-uc-create-event.png)

1. The event configuration pane opens on the right side of the screen. Configure a rule-based unitary event. [Learn more](../event/about-creating.md)

1. Define the schema: select **[!UICONTROL AJO Email Tracking Experience Event Schema v.1]** (available by default in [!DNL Journey Optimizer]).

    ![](assets/lp_subscription-uc-event-schema.png)

1. In the **[!UICONTROL Fields]** section, select the following elements:

    * **[!UICONTROL _experience]** > **[!UICONTROL customerJourneyManagement]** > **[!UICONTROL messageInteraction]** > **[!UICONTROL Interaction Type]**
    
    * **[!UICONTROL _experience]** > **[!UICONTROL customerJourneyManagement]** > **[!UICONTROL messageInteraction]** > **[!UICONTROL Landing Page Details]** > **[!UICONTROL Landing Page ID]**

    ![](assets/lp_subscription-uc-event-fields.png)

1. Click inside the **[!UICONTROL Event ID condition]** field. Using the simple personalization editor, define the condition for the **[!UICONTROL Interaction Type]** and **[!UICONTROL Landing Page ID]** fields. This will be used by the system to identify the events that will trigger your journey.

    ![](assets/lp_subscription-uc-event-id-condition.png)

    >[!NOTE]
    >
    >To find the landing page ID, you can insert the landing page as a link into an email and select the source code from the contextual toolbar to display the landing page information.
    >
    >![](assets/lp_subscription-uc-lp-id.png)

1. Save your changes.

1. Create a [journey](../building-journeys/journey.md). You can do it directly from the landing page by clicking the **[!UICONTROL Create journey]** button. Learn more [here](create-lp.md#configure-primary-page)

    ![](assets/lp_subscription-uc-event-create-journey.png)

1. In the journey, unfold the **[!UICONTROL Events]** category and drop the event that you created into the canvas. Learn more [here](../building-journeys/audience-qualification-events.md)

    ![](assets/lp_subscription-uc-journey-event.png)

1. Unfold the **[!UICONTROL Actions]** category and drop an email action into the canvas.

    ![](assets/lp_subscription-uc-journey-email.png)

///How do you use the information from the event to send an email to the users? -->
