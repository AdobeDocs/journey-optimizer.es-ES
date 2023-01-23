---
solution: Journey Optimizer
product: journey optimizer
title: Casos de uso de la página de aterrizaje
description: Descubra los casos de uso más comunes con páginas de aterrizaje en Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
keywords: aterrizaje, página de aterrizaje, caso de uso
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 16%

---

# Casos de uso de la página de aterrizaje {#lp-use-cases}

A continuación se muestran algunos ejemplos de cómo puede utilizar [!DNL Journey Optimizer] páginas de aterrizaje para que sus clientes no reciban ninguna o parte de sus comunicaciones.

## Suscripción a un servicio {#subscription-to-a-service}

Uno de los casos de uso más comunes consiste en invitar a sus clientes a [suscripción a un servicio](subscription-list.md) (como un boletín o un evento) a través de una página de aterrizaje. Los pasos principales se presentan en el gráfico siguiente:

![](assets/lp_subscription-uc.png)

Por ejemplo, supongamos que organiza un evento el mes que viene y desea iniciar una campaña de registro de eventos<!--to keep your customers that are interested updated on that event-->. Para ello, se envía un correo electrónico que incluye un vínculo a una página de aterrizaje que permite a los destinatarios registrarse en este evento. Los usuarios que se registren se agregarán a la lista de suscripción que haya creado con este fin.

### Configuración de una página de aterrizaje {#set-up-lp}

1. Cree la lista de suscripción del registro de eventos, que almacenará los usuarios registrados. Obtenga información sobre cómo crear una lista de suscripción [here](subscription-list.md#define-subscription-list).

   ![](assets/lp_subscription-uc-list.png)

1. [Crear una página de aterrizaje](create-lp.md) para permitir que los destinatarios se registren en el evento.

   ![](assets/lp_create-lp-details.png)

1. Configuración del registro [página de aterrizaje principal](create-lp.md#configure-primary-page).

1. Al diseñar la variable [contenido de la página de aterrizaje](design-lp.md), seleccione la lista de suscripción que ha creado para actualizarla con los perfiles que seleccionan la casilla de verificación de registro.

   ![](assets/lp_subscription-uc-lp-list.png)

1. Cree una página de agradecimiento que se mostrará a sus destinatarios una vez que envíen el formulario de registro. Obtenga información sobre cómo configurar subpáginas de aterrizaje [here](create-lp.md#configure-subpages).

   ![](assets/lp_subscription-uc-thanks.png)

1. [Publicación](create-lp.md#publish) la página de aterrizaje.

1. En un [recorrido](../building-journeys/journey.md), agregue un **Correo electrónico** actividad para dirigir el tráfico a la página de aterrizaje de registro.

   ![](assets/lp_subscription-uc-journey.png)

1. [Diseño del correo electrónico](../email/get-started-email-design.md) para anunciar que el registro está abierto para su evento.

1. [Inserción de un vínculo](../email/message-tracking.md#insert-links) en el contenido del mensaje. Select **[!UICONTROL Página de aterrizaje]** como el **[!UICONTROL Tipo de vínculo]** y seleccione [página de aterrizaje](create-lp.md#configure-primary-page) que ha creado para el registro.

   ![](assets/lp_subscription-uc-link.png)

   >[!NOTE]
   >
   >Para poder enviar el mensaje, asegúrese de que la página de aterrizaje que seleccione no haya caducado aún. Obtenga información sobre cómo actualizar la fecha de caducidad [en esta sección](create-lp.md#configure-primary-page).

   Una vez que reciban el correo electrónico, si los destinatarios hacen clic en el vínculo a la página de aterrizaje, se les dirigirá a la página de agradecimiento y se añadirán a la lista de suscripción.

### Enviar un correo electrónico de confirmación {#send-confirmation-email}

Además, puede enviar un correo electrónico de confirmación a los destinatarios que se hayan registrado en el evento. Para ello, siga los pasos que aparecen a continuación.

1. Crear otro [recorrido](../building-journeys/journey.md). Puede hacerlo directamente desde la página de aterrizaje haciendo clic en el **[!UICONTROL Crear recorrido]** botón. Obtenga más información [aquí](create-lp.md#configure-primary-page)

   ![](assets/lp_subscription-uc-create-journey.png)

1. Despliegue el **[!UICONTROL Eventos]** categoría y suelte a **[!UICONTROL Clasificación del segmento]** actividad en el lienzo. Obtenga más información [aquí](../building-journeys/segment-qualification-events.md)

1. Haga clic en el **[!UICONTROL Segmento]** y seleccione la lista de suscripción que ha creado.

   ![](assets/lp_subscription-uc-confirm-journey.png)

1. Añada un correo electrónico de confirmación de su elección y envíelo a través del recorrido.

   ![](assets/lp_subscription-uc-confirm-email.png)

Todos los usuarios que se hayan registrado para el evento recibirán el correo electrónico de confirmación.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## Exclusión {#opt-out}

Para permitir que sus destinatarios cancelen la suscripción a sus comunicaciones, puede incluir un vínculo a una página de aterrizaje de exclusión en sus correos electrónicos.

Obtenga más información sobre la administración del consentimiento de los destinatarios y por qué esto es importante en [esta sección](../privacy/opt-out.md).

### Administración de exclusiones {#opt-out-management}

Proporcionar a los destinatarios la capacidad de cancelar la suscripción a la recepción de comunicaciones de una marca es un requisito legal. Obtenga más información acerca de la legislación aplicable en la [Documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=es#regulations){target="_blank"}.

Por lo tanto, siempre debe incluir un **enlace para cancelar la suscripción** en cada correo electrónico enviado a los destinatarios:

* Al hacer clic en este vínculo, los destinatarios se dirigen a una página de aterrizaje que incluye un botón para confirmar la exclusión.
* Al hacer clic en el botón de exclusión, los datos de perfil se actualizarán con esta información.

### Configuración de la exclusión {#configure-opt-out}

Para permitir que los destinatarios de un correo electrónico cancelen la suscripción de sus comunicaciones a través de una página de aterrizaje, siga los pasos a continuación.

1. Cree la página de aterrizaje. [Más información](create-lp.md)

1. Defina la página principal. [Más información](create-lp.md#configure-primary-page)

1. [Diseño](design-lp.md) el contenido de la página principal: usar el específico de la página de aterrizaje **[!UICONTROL Formulario]** , defina un **[!UICONTROL Exclusión]** y elija actualizar **[!UICONTROL Canal (correo electrónico)]**: el perfil que marca la casilla de exclusión de la página de aterrizaje se excluirá de todas las comunicaciones.

   ![](assets/lp_opt-out-primary-lp.png)

   <!--You can also build your own landing page and host it on the third-party system of your choice.-->

1. Añadir una confirmación [subpágina](create-lp.md#configure-subpages) que se mostrará a los usuarios que envíen el formulario.

   ![](assets/lp_opt-out-subpage.png)

   >[!NOTE]
   >
   >Asegúrese de hacer referencia a la subpágina en el informe **[!UICONTROL Llamada a acción]** de la sección **[!UICONTROL Formulario]** componente. [Más información](design-lp.md)

1. Una vez configurado y definido el contenido de sus páginas, [publicar](create-lp.md#publish) la página de aterrizaje.

   ![](assets/lp_opt-out-publish.png)

1. [Creación de un mensaje de correo electrónico](../email/get-started-email-design.md) en un recorrido.

1. Seleccione texto en el contenido e [inserte un vínculo](../email/message-tracking.md#insert-links) utilizando la barra de herramientas contextual. También puede utilizar un vínculo en un botón.

   ![](assets/lp_opt-out-insert-link.png)

1. Select **[!UICONTROL Página de aterrizaje]** de la variable **[!UICONTROL Tipo de vínculo]** y seleccione la [página de aterrizaje](create-lp.md#configure-primary-page) que ha creado para la exclusión.

   ![](assets/lp_opt-out-landing-page.png)

   >[!NOTE]
   >
   >Para poder enviar el mensaje, asegúrese de que la página de aterrizaje que seleccione no haya caducado aún. Obtenga información sobre cómo actualizar la fecha de caducidad [en esta sección](create-lp.md#configure-primary-page).

1. Publique y ejecute el recorrido. [Más información](../building-journeys/journey.md).

1. Una vez recibido el mensaje, si un destinatario hace clic en el vínculo unsubscribe del correo electrónico, se muestra la página de aterrizaje.

   ![](assets/lp_opt-out-submit-form.png)

   Si el destinatario marca la casilla y envía el formulario:

   * El destinatario excluido se redirige a la pantalla del mensaje de confirmación.

   * Los datos de perfil se actualizan y no reciben comunicaciones de su marca a menos que se vuelvan a suscribir.

Para comprobar que se ha actualizado la opción del perfil correspondiente, vaya a Experience Platform y acceda al perfil seleccionando un área de nombres de identidad y un valor de identidad correspondiente. Obtenga más información en la [documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=es#getting-started){target="_blank"}.

![](assets/lp_opt-out-profile-choice.png)

En el **[!UICONTROL Atributos]** , puede ver que el valor de **[!UICONTROL choice]** ha cambiado a **[!UICONTROL no]**.

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

1. Click inside the **[!UICONTROL Event ID condition]** field. Using the simple expression editor, define the condition for the **[!UICONTROL Interaction Type]** and **[!UICONTROL Landing Page ID]** fields. This will be used by the system to identify the events that will trigger your journey.

    ![](assets/lp_subscription-uc-event-id-condition.png)

    >[!NOTE]
    >
    >To find the landing page ID, you can insert the landing page as a link into an email and select the source code from the contextual toolbar to display the landing page information.
    >
    >![](assets/lp_subscription-uc-lp-id.png)

1. Save your changes.

1. Create a [journey](../building-journeys/journey.md). You can do it directly from the landing page by clicking the **[!UICONTROL Create journey]** button. Learn more [here](create-lp.md#configure-primary-page)

    ![](assets/lp_subscription-uc-event-create-journey.png)

1. In the journey, unfold the **[!UICONTROL Events]** category and drop the event that you created into the canvas. Learn more [here](../building-journeys/segment-qualification-events.md)

    ![](assets/lp_subscription-uc-journey-event.png)

1. Unfold the **[!UICONTROL Actions]** category and drop an email action into the canvas.

    ![](assets/lp_subscription-uc-journey-email.png)

///How do you use the information from the event to send an email to the users? -->
