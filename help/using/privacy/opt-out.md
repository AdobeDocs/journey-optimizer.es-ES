---
solution: Journey Optimizer
product: journey optimizer
title: Administración de la exclusión
description: Obtenga información sobre cómo administrar la exclusión y la privacidad
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 42%

---

# Administración de la exclusión {#consent}

Proporcionar a los destinatarios la capacidad de cancelar la suscripción a la recepción de comunicaciones de una marca es un requisito legal, así como garantizar que se cumpla esta opción. Obtenga más información acerca de la legislación aplicable en la [Documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=es#regulations){target="_blank"}.

**¿Por qué es importante?**

* El incumplimiento de estas regulaciones conlleva riesgos legales para su marca.
* Le ayuda a evitar enviar comunicaciones no solicitadas a sus destinatarios, lo que podría hacer que marquen sus mensajes como correo no deseado y dañar su reputación.

## Administración de bajas en recorridos y campañas {#opt-out-ajo}

Al enviar mensajes desde recorridos o campañas, siempre debe asegurarse de que los clientes puedan cancelar la suscripción a comunicaciones futuras. Una vez cancelada la suscripción, los perfiles se eliminan automáticamente de la audiencia de futuros mensajes de marketing.

Mientras **[!DNL Journey Optimizer]** proporciona formas de administrar la exclusión en correos electrónicos y mensajes SMS, las notificaciones push no requieren ninguna acción por su parte, ya que los destinatarios pueden cancelar la suscripción a través de sus propios dispositivos. Por ejemplo, al descargar o al usar la aplicación, pueden seleccionar detener las notificaciones. Del mismo modo, pueden cambiar la configuración de notificación a través del sistema operativo móvil.

Aprenda a administrar la exclusión en los mensajes de correo electrónico y SMS de Journey Optimizer en estas secciones:

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="Posible cliente" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%">
</a>
<div><a href="../email/email-opt-out.md"><strong>Administración de exclusión de correo electrónico</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Poco frecuente" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%">
</a>
<div>
<a href="../sms/sms-opt-out.md"><strong>Administración de exclusión de SMS</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>En [!DNL Journey Optimizer], Experience Platform gestiona el consentimiento [Esquema de consentimiento](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=es){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=es#choice-values){target="_blank"}.

## Implementación del consentimiento de personalización {#opt-out-personalization}

Los clientes también pueden optar por no recibir contenido personalizado. Una vez que un perfil se ha excluido de la personalización, debe asegurarse de que sus datos no se utilicen para ella y debe reemplazar cualquier contenido personalizado con una variante de reserva.

### En gestión de decisiones

Al aprovechar las ofertas, las preferencias de personalización no se implementan automáticamente en [ámbitos de decisión](../offers/offer-activities/create-offer-activities.md#add-decision-scopes) utilizado desde una solicitud de API de [Decisioning](../offers/api-reference/offer-delivery-api/decisioning-api.md) o una solicitud de API de [Edge Decisioning](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md). En este caso, debe aplicar manualmente el consentimiento de personalización. Para ello, siga los pasos que aparecen a continuación.

>[!NOTE]
>
>Los ámbitos de decisión utilizados en los canales creados de [!DNL Journey Optimizer] cumplen este requisito desde el recorrido o la campaña a los que pertenecen.

1. Crear un [Audiencia de Adobe Experience Platform](../audience/access-audiences.md) uso del [Servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target="_blank"} y utilice un atributo de perfil como **[!UICONTROL Personalizar contenido = Sí (inclusión)]** para dirigirse a los usuarios que hayan aceptado la personalización.

   ![](assets/perso-consent-od-audience.png)

1. Al crear un [decisión](../offers/offer-activities/create-offer-activities.md), agregue un ámbito de decisión y defina una restricción de elegibilidad basada en esta audiencia para cada colección de criterios de evaluación que contenga ofertas personalizadas.

   ![](assets/perso-consent-od-audience-decision.png)

1. Crear una [oferta de reserva](../offers/offer-library/creating-fallback-offers.md) que no incluye contenido personalizado.

1. [Asignar](../offers/offer-activities/create-offer-activities.md#add-fallback) la oferta de reserva no personalizada a la decisión.

   ![](assets/perso-consent-od-audience-fallback.png)

1. [Revisar y guardar](../offers/offer-activities/create-offer-activities.md#review) la decisión.

Si un usuario:

* ha aceptado la personalización, el ámbito de decisión determinará la mejor oferta para ese perfil.

* no ha aceptado la personalización, el perfil correspondiente no será apto para ninguna de las ofertas que se encuentren en los criterios de evaluación y, por lo tanto, recibirán la oferta de reserva no personalizada.

>[!NOTE]
>
>El consentimiento que los datos de perfil se utilicen en [modelado de datos](../offers/ranking/ai-models.md) aún no es compatible con [!DNL Journey Optimizer].

## En el Editor de expresiones

<!--Expressions Editor while personalizing images, text, subject line  ( Segment in Campaigns) - UI and Headless -->

El [Editor de expresiones](../personalization/personalization-build-expressions.md) no realiza ninguna comprobación ni aplicación del consentimiento, ya que no participa en la entrega de mensajes.

Sin embargo, el uso de etiquetas de control de acceso basadas en los derechos permite restringir qué campos se pueden utilizar para la personalización. El [vista previa del mensaje](../email/preview.md#preview-email) y [servicio de procesamiento de correo electrónico](../email/preview.md#email-rendering) enmascarará los campos identificados con información confidencial.

>[!NOTE]
>
>Obtenga más información sobre el Control de acceso de nivel de objeto (OLAC) en [esta sección](../administration/object-based-access.md).


Entrada [!DNL Journey Optimizer] Para las campañas de, la política de consentimiento se aplica de la siguiente manera:

* Puede incluir definiciones de políticas de consentimiento como parte de la creación de audiencias para asegurarse de que la audiencia seleccionada para la campaña ya haya **perfiles filtrados que no coinciden con los criterios de consentimiento**.

* [!DNL Journey Optimizer] realizará una comprobación de consentimiento general en el nivel de canal para lo siguiente **asegúrese de que los perfiles se hayan suscrito** para recibir comunicaciones de marketing en el canal correspondiente.

  >[!NOTE]
  >
  >El [!DNL Journey Optimizer] el propio objeto campaign no realiza ninguna comprobación de aplicación de directivas de consentimiento adicional en este momento.

Para aplicar manualmente el consentimiento de personalización en las campañas, siga una de las opciones a continuación.

### Uso del generador de reglas de segmentos

Puede usar el Generador de reglas de segmentos para crear una audiencia que contenga perfiles de exclusión.

1. Crear un [Audiencia de Adobe Experience Platform](../audience/access-audiences.md) uso del [Servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target="_blank"}.

   ![](assets/perso-consent-audience-build-rule.png)

1. Seleccione un atributo de perfil como **[!UICONTROL Personalizar contenido = No (exclusión)]** para excluir a los usuarios que no hayan aceptado la personalización.

   ![](assets/perso-consent-audience-no.png)

1. Haga clic en **[!UICONTROL Guardar]**.

Ahora puede utilizar esta audiencia para filtrar los perfiles que no han dado su consentimiento para la personalización de sus campañas.

### Uso de una actividad de división en un flujo de trabajo de composición

También puede añadir una comprobación de consentimiento de personalización a una audiencia añadiendo una actividad dividida a un flujo de trabajo de composición.

1. Cree una audiencia con el **[!UICONTROL Componer audiencia]** opción. [Más información sobre la creación de un flujo de trabajo de composición](../audience/create-compositions.md)

   ![](assets/perso-consent-audience-compose.png)

1. Añada la audiencia inicial con el botón específico a la derecha.

1. Haga clic en el icono + y seleccione **[!UICONTROL Split]** para crear una audiencia dividida. [Más información sobre la actividad Dividir](../audience/composition-canvas.md#split)

   ![](assets/perso-consent-audience-split.png)

1. Seleccionar **[!UICONTROL División de atributos]** como el tipo de división en el panel derecho.

   ![](assets/perso-consent-audience-attribute-split.png)

1. Haga clic en el icono de lápiz situado junto al **[!UICONTROL Atributo]** para que aparezca el campo **[!UICONTROL Seleccionar un atributo de perfil]** ventana.

1. Busque el atributo de consentimiento de personalización (`profile.consents.personalize.content.val`) y selecciónelo.

   ![](assets/perso-consent-audience-consent-attribute.png)

1. **[!UICONTROL Ruta 1]** será la audiencia no personalizada. Elija una etiqueta relevante.

1. Elija el valor apropiado de esta lista [lista](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=es#choice-values){target="_blank"}.

   En este caso utilizaremos `n` para indicar que los usuarios no consienten el uso de sus datos para la personalización.

   ![](assets/perso-consent-audience-path-1-n.png)

1. Puede crear una ruta independiente para otros valores de opción. También puede optar por eliminar las rutas restantes y activar **[!UICONTROL Otros perfiles]** para incluir todos los demás perfiles que no tenían un valor de opción de `n`.

1. Una vez finalizado, haga clic en **[!UICONTROL Guardar audiencia]** para cada ruta y guardar el resultado del flujo de trabajo en una nueva audiencia. Se guardará una audiencia en Adobe Experience Platform para cada ruta.

1. Una vez finalizado, publique el flujo de trabajo de composición.

Ahora puede utilizar esta audiencia para filtrar los perfiles que no han dado su consentimiento para la personalización de sus campañas.

>[!NOTE]
>
>Si crea una audiencia que no ha dado su consentimiento para la personalización y, a continuación, selecciona esta audiencia en una campaña, las herramientas de personalización permanecerán disponibles. Depende de los usuarios de marketing comprender que, si trabajan con una audiencia que no debería recibir personalización, no deben utilizar herramientas de personalización.
