---
solution: Journey Optimizer
product: journey optimizer
title: Administrar la exclusión
description: Obtenga información sobre cómo administrar la exclusión y la privacidad
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# Administrar la exclusión {#consent}

## Acerca de la administración de la exclusión {#about}

Proporcionar a los destinatarios la capacidad de cancelar la suscripción para recibir comunicaciones de una marca es un requisito legal. Obtenga más información sobre la legislación aplicable en la [Documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}.

**¿Por qué es importante?**

* El incumplimiento de estas regulaciones conlleva riesgos legales para su marca.
* Le ayuda a evitar enviar comunicaciones no solicitadas a sus destinatarios, lo que podría hacer que marquen sus mensajes como correo no deseado y dañar su reputación.

## Administración de la exclusión en Journey Optimizer {#opt-out-ajo}

Al enviar mensajes desde recorridos o campañas, siempre debe asegurarse de que los clientes puedan cancelar la suscripción a futuras comunicaciones. Una vez cancelada la suscripción, los perfiles se eliminan automáticamente de la audiencia de futuros mensajes de marketing.

While **[!DNL Journey Optimizer]** proporciona formas de administrar la exclusión en correos electrónicos y mensajes SMS, las notificaciones push no requieren ninguna acción por su parte, ya que los destinatarios pueden cancelar la suscripción a través de sus propios dispositivos. Por ejemplo, al descargar o al usar la aplicación, pueden seleccionar detener las notificaciones. Del mismo modo, pueden cambiar la configuración de notificación a través del sistema operativo móvil.

Aprenda a administrar la exclusión en los mensajes de correo electrónico y SMS de Journey Optimizer en estas secciones:

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="Posible cliente" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;&lt;a href=" ../email/email-opt-out.md"><strong>Administración de exclusión de correo electrónico</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Poco frecuente" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;
&lt;a href=" ../sms/sms-opt-out.md"><strong>Administración de exclusión de SMS</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>En [!DNL Journey Optimizer], el consentimiento lo gestiona Experience Platform [Esquema de consentimiento](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target=&quot;_blank&quot;}. De forma predeterminada, el valor del campo de consentimiento está vacío y se trata como consentimiento para recibir sus comunicaciones. Puede modificar este valor predeterminado al incorporar uno de los posibles valores enumerados [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target=&quot;_blank&quot;}.