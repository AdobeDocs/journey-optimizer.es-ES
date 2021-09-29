---
title: Seguimiento de mensajes
description: Aprenda a añadir vínculos y rastrear mensajes enviados
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: 11a42e404f79f07fb092892d5ebc53f3d1a4351b
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 4%

---

# Adición de vínculos y seguimiento de mensajes {#tracking}

Utilice [!DNL Journey Optimizer] para añadir vínculos al contenido y rastrear los mensajes enviados para controlar el comportamiento de los destinatarios.

## Habilitar el seguimiento {#enable-tracking}

Puede habilitar el seguimiento a nivel de mensaje de correo electrónico comprobando las opciones **[!UICONTROL Open Tracking for email]** o **[!UICONTROL Click Tracking for email]** al [crear su mensaje](create-message.md).

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
>Cuando [el seguimiento está habilitado](#enable-tracking), se realiza un seguimiento de todos los vínculos incluidos en el contenido del mensaje.

Para insertar vínculos en el contenido del correo electrónico, siga los pasos a continuación:

1. Seleccione un elemento y haga clic en **[!UICONTROL Insert link]** en la barra de herramientas contextual.

   ![](assets/message-tracking-insert-link.png)

1. Elija el tipo de vínculo que desea crear:

   * **[!UICONTROL External link]**: Inserte un vínculo a una URL externa.

   * **[!UICONTROL Unsubscription link]**: Inserte un vínculo para cancelar la suscripción a la recepción de comunicaciones de su marca. Obtenga más información sobre la administración de exclusiones en [esta sección](consent.md#opt-out-management).

   * **[!UICONTROL Mirror page]**: Inserte un vínculo para mostrar el contenido del correo electrónico en un explorador web. Obtenga más información en [esta sección](#mirror-page).

   * **[!UICONTROL Opt-out]**: Inserte un vínculo para permitir a los usuarios cancelar rápidamente la suscripción a sus comunicaciones sin necesidad de confirmar la exclusión. Obtenga más información en [esta sección](#one-click-opt-out-link).

   ![](assets/message-tracking-links.png)

1. Puede personalizar los vínculos. Obtenga más información sobre las direcciones URL personalizadas en [esta sección](personalization/personalization-syntax.md#perso-urls).

1. Guarde los cambios.

1. Una vez creado el vínculo, puede modificarlo desde el panel **[!UICONTROL Component settings]** de la derecha.

   * Haga clic en el icono de lápiz para editar el vínculo.
   * Puede elegir subrayar el vínculo o no marcando la opción correspondiente.

   ![](assets/message-tracking-link-settings.png)

## Vínculo a una página espejo {#mirror-page}

La página espejo es una página HTML accesible en línea mediante un navegador web. Su contenido es idéntico al del correo electrónico.

Para añadir un vínculo a una página espejo en el correo electrónico, [inserte un vínculo](#insert-links) y seleccione **[!UICONTROL Mirror page]** como tipo de vínculo.

![](assets/message-tracking-mirror-page.png)

La página espejo se crea automáticamente.

>[!NOTE]
>
>No se puede editar el vínculo generado automáticamente.

Una vez enviado el correo electrónico, cuando los destinatarios hacen clic en el vínculo de la página espejo, el contenido del correo electrónico se muestra en su navegador web predeterminado.

>[!NOTE]
>
>En la [prueba](preview.md#send-proofs) enviada a los perfiles de prueba, el vínculo a la página espejo no está activo. Solo se activa en los mensajes finales.

El período de retención de una página espejo es de 60 días. Después de ese retraso, la página espejo ya no estará disponible.

## Vínculo de no participación de un clic {#one-click-opt-out-link}

Para permitir que los destinatarios cancelen rápidamente la suscripción a la recepción de comunicaciones de su marca, puede insertar un vínculo de exclusión de un solo clic en el contenido del correo electrónico. Esta capacidad evita que los usuarios se redirijan a una página de aterrizaje donde necesitan confirmar su elección, lo que acelera el proceso de cancelación de suscripción.

Para añadir un vínculo de no participación en el correo electrónico, siga los pasos a continuación.

1. [Inserte un ](#insert-links) vínculo y seleccione  **[!UICONTROL Opt-out]** como tipo de vínculo.

   ![](assets/message-tracking-opt-out.png)

1. Seleccione cómo desea aplicar la exclusión: en el nivel de canal, identidad o suscripción.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Channel]**: La exclusión se aplica a mensajes futuros enviados al destinatario del perfil (es decir, la dirección de correo electrónico) para el canal actual. Si hay varios objetivos asociados a un perfil, la exclusión se aplica a todos los destinos (es decir, direcciones de correo electrónico) del perfil de ese canal.
   * **[!UICONTROL Identity]**: La exclusión se aplica a los mensajes futuros enviados al destinatario específico (es decir, la dirección de correo electrónico) que se estén utilizando para el mensaje actual.
   * **[!UICONTROL Subscription]**: La exclusión se aplica a mensajes futuros asociados a una lista de suscripción específica. Esta opción solo se puede seleccionar si el mensaje actual está asociado con una lista de suscripción.

1. Introduzca la dirección URL de la página de aterrizaje a la que se redirigirá al usuario una vez cancelada la suscripción. Esta página solo está aquí para confirmar que la exclusión se ha realizado correctamente.

   ![](assets/message-tracking-opt-out-confirmation.png)

   Puede personalizar los vínculos. Obtenga más información sobre las direcciones URL personalizadas en [esta sección](personalization/personalization-syntax.md).

1. Guarde los cambios.

Una vez enviado el mensaje, si un destinatario hace clic en el vínculo de exclusión, se le excluye inmediatamente.

## Administrar seguimiento {#manage-tracking}

El [Diseñador de correo electrónico](create-email-content.md) le permite administrar las direcciones URL rastreadas, como editar el tipo de seguimiento para cada vínculo.

1. Haga clic en el icono **[!UICONTROL Links]** del panel izquierdo para mostrar la lista de todas las direcciones URL del contenido que se rastreará.

   Esta lista permite tener una vista centralizada y localizar cada URL en el contenido del correo electrónico.

1. Para editar un vínculo, haga clic en el icono de lápiz correspondiente.

   ![](assets/message-tracking-edit-links.png)

1. Puede modificar el **[!UICONTROL Tracking Type]** si es necesario:


   ![](assets/message-tracking-edit-a-link.png)

   Para cada URL rastreada, puede establecer el modo de seguimiento en uno de estos valores:

   * **[!UICONTROL Tracked]**: Activa el seguimiento en esta dirección URL.
   * **[!UICONTROL Opt out]**: Considera esta URL como una URL de exclusión o de baja.
   * **[!UICONTROL Mirror page]**: Considera que esta URL es una URL de página espejo.
   * **[!UICONTROL Never]**: Nunca activa el seguimiento de esta dirección URL.  <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

El número de mensajes que se han abierto y el número de vínculos en los que se ha hecho clic se enumeran en la [ficha Ejecuciones](message-monitoring.md).

Los informes sobre aperturas y clics están disponibles en [Email Live report](reports/email-live-report.md) y en [Email Global report](reports/email-global-report.md).
