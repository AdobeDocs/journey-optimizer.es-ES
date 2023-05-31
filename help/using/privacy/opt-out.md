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
source-git-commit: 8b459f71852d031dc650b77725bdc693325cdb1d
workflow-type: ht
source-wordcount: '478'
ht-degree: 100%

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



1. Crear un [Segmento de Adobe Experience Platform](../segment/about-segments.md) mediante un atributo de perfil como: *&quot;Consentimientos para la personalización = Verdadero&quot;* para dirigirse a los usuarios que hayan aceptado la personalización.

1. Al crear una [decisión](../offers/offer-activities/create-offer-activities.md), agregue un ámbito de decisión y defina una restricción de elegibilidad basada en este segmento para cada recopilación de criterios de evaluación que contenga ofertas personalizadas.

1. Crear una [oferta de reserva](../offers/offer-library/creating-fallback-offers.md) que no incluye contenido personalizado.

1. [Asignar](../offers/offer-activities/create-offer-activities.md#add-fallback) la oferta de reserva no personalizada a la decisión.

1. [Revisar y guardar](../offers/offer-activities/create-offer-activities.md#review) la decisión.

Si un usuario:

* ha aceptado la personalización, el ámbito de decisión determinará la mejor oferta para ese perfil.

* no ha aceptado la personalización, el perfil correspondiente no será apto para ninguna de las ofertas que se encuentren en los criterios de evaluación y, por lo tanto, recibirán la oferta de reserva no personalizada.

>[!NOTE]
>
>El consentimiento que los datos de perfil se utilicen en [modelado de datos](../offers/ranking/ai-models.md) aún no es compatible con [!DNL Journey Optimizer].

