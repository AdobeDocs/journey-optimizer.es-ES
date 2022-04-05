---
title: Seguimiento de mensajes
description: Aprenda a añadir vínculos y rastrear mensajes enviados
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: 1d0e28583c500d5eddf9f88250f279d188c4784a
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 9%

---

# Adición de vínculos y seguimiento de mensajes {#tracking}

Uso [!DNL Journey Optimizer] para añadir vínculos al contenido y realizar un seguimiento de los mensajes enviados para controlar el comportamiento de los destinatarios.

## Habilitar el seguimiento {#enable-tracking}

Puede habilitar el seguimiento a nivel de mensaje de correo electrónico comprobando la variable **[!UICONTROL Open Tracking for email]** y/o **[!UICONTROL Click Tracking for email]** opciones [crear el mensaje](../messages/get-started-content.md).

![](assets/message-tracking.png)

>[!NOTE]
>
>Ambas opciones están habilitadas de forma predeterminada.

Esto le permite hacer un seguimiento del comportamiento de sus destinatarios a través de:

* **[!UICONTROL Open Tracking for email]**: Mensajes que se han abierto.
* **[!UICONTROL Click Tracking for email]**: Haga clic en los vínculos de un correo electrónico.

## Insertar vínculos {#insert-links}

Al diseñar un mensaje, puede agregar vínculos al contenido.

>[!NOTE]
>
>When [el seguimiento está habilitado](#enable-tracking), se rastrearán todos los vínculos incluidos en el contenido del mensaje.

Para insertar vínculos en el contenido del correo electrónico, siga los pasos a continuación:

1. Seleccione un elemento y haga clic en **[!UICONTROL Insert link]** de la barra de herramientas contextual.

   ![](assets/message-tracking-insert-link.png)

1. Elija el tipo de vínculo que desea crear:

   * **[!UICONTROL External link]**: Inserte un vínculo a una URL externa.

   * **[!UICONTROL Landing page]**: Inserte un vínculo a una página de aterrizaje. Obtenga más información en [esta sección](../landing-pages/get-started-lp.md)

   * **[!UICONTROL One click Opt-out]**: Inserte un vínculo para permitir a los usuarios cancelar rápidamente la suscripción a sus comunicaciones sin necesidad de confirmar la exclusión. Obtenga más información en [esta sección](../messages/consent.md#one-click-opt-out).

   * **[!UICONTROL External Opt-in/Subscription]**: Inserte un vínculo para aceptar la recepción de comunicaciones de su marca.

   * **[!UICONTROL External Opt-out/Unsubscription]**: Inserte un vínculo para cancelar la suscripción a la recepción de comunicaciones de su marca. Obtenga más información sobre la administración de exclusiones en [esta sección](../messages/consent.md#opt-out-management).

   * **[!UICONTROL Mirror page]**: Inserte un vínculo para mostrar el contenido del correo electrónico en un explorador web. Obtenga más información en [esta sección](#mirror-page).

   ![](assets/message-tracking-links.png)

1. Puede personalizar los vínculos. Obtenga más información sobre la administración de exclusiones en [esta sección](../personalization/personalization-syntax.md#perso-urls).

1. Guarde los cambios.

1. Una vez creado el vínculo, puede modificarlo desde el **[!UICONTROL Component settings]** a la derecha.

   * Puede editar el vínculo y cambiar su tipo.
   * Puede elegir subrayar el vínculo o no marcando la opción correspondiente.

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>Los mensajes de correo electrónico de tipo de marketing deben incluir un [vínculo de no participación](../messages/consent.md#opt-out-management), que no es necesario para los mensajes transaccionales. La categoría del mensaje (**[!UICONTROL Marketing]** o **[!UICONTROL Transactional]**) se define en la variable [nivel de mensaje preestablecido](../configuration/message-presets.md#email-type) y cuándo [creación del mensaje](../messages/get-started-content.md#create-new-message).

## Vínculo a una página espejo {#mirror-page}

La página espejo es una página HTML accesible en línea mediante un navegador web. Su contenido es idéntico al del correo electrónico.

Para añadir un vínculo a una página espejo en el correo electrónico, [insertar un vínculo](#insert-links) y seleccione **[!UICONTROL Mirror page]** como tipo de vínculo.

![](assets/message-tracking-mirror-page.png)

La página espejo se crea automáticamente.

>[!NOTE]
>
>No se puede editar el vínculo generado automáticamente.

Una vez enviado el correo electrónico, cuando los destinatarios hacen clic en el vínculo de la página espejo, el contenido del correo electrónico se muestra en su navegador web predeterminado.

>[!NOTE]
>
>En el [prueba](preview.md#send-proofs) enviado a los perfiles de prueba, el vínculo a la página espejo no está activo. Solo se activa en los mensajes finales.

El período de retención de una página espejo es de 60 días. Después de ese retraso, la página espejo ya no estará disponible.

## Administrar seguimiento {#manage-tracking}

La variable [Diseñador de correo electrónico](create-email-content.md) le permite administrar las direcciones URL rastreadas, como editar el tipo de seguimiento para cada vínculo.

1. Haga clic en el **[!UICONTROL Links]** del panel izquierdo para mostrar la lista de todas las direcciones URL del contenido de las que se realizará un seguimiento.

   Esta lista permite tener una vista centralizada y localizar cada URL en el contenido del correo electrónico.

1. Para editar un vínculo, haga clic en el icono de lápiz correspondiente.

   ![](assets/message-tracking-edit-links.png)

1. Puede modificar el **[!UICONTROL Tracking Type]** si es necesario:

   ![](assets/message-tracking-edit-a-link.png)

   Para cada URL rastreada, puede establecer el modo de seguimiento en uno de estos valores:

   * **[!UICONTROL Tracked]**: Activa el seguimiento en esta dirección URL.
   * **[!UICONTROL Opt out]**: Considera esta URL como una URL de exclusión o de baja.
   * **[!UICONTROL Mirror page]**: Considera que esta URL es una URL de página espejo.
   * **[!UICONTROL Never]**: Nunca activa el seguimiento de esta dirección URL. <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

El número de mensajes que se han abierto y el número de vínculos en los que se ha hecho clic se enumeran en la variable [Ficha Ejecuciones](../reports/message-monitoring.md).

Los informes de aperturas y clics están disponibles en la [Informe de Email Live](../reports/email-live-report.md) y en el [Informe global de correo electrónico](../reports/email-global-report.md).
