---
title: Reglas de frecuencia
description: Aprenda a definir las reglas de frecuencia
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Reglas de frecuencia de mensajes {#frequency-rules}

[!DNL Journey Optimizer] le permite controlar la frecuencia con la que los usuarios recibirán un mensaje o entrar en un recorrido estableciendo reglas de canales cruzados que excluyan automáticamente los perfiles saturados de mensajes y acciones.

Por ejemplo, no desea que la marca envíe más de tres mensajes de marketing al mes a sus clientes.

Para ello, puede utilizar una regla de frecuencia que limite el número de mensajes enviados en función de uno o varios canales durante un periodo de calendario mensual.

>[!NOTE]
>
>Las reglas de frecuencia de mensajes son diferentes de la administración de exclusión, que permite a los usuarios cancelar la suscripción para recibir comunicaciones de una marca. [Más información](../messages/consent.md#opt-out-management)

## Reglas de acceso {#access-rules}

Las reglas están disponibles en el **[!UICONTROL Administration]** > **[!UICONTROL Rules]** para abrir el Navegador. Se muestran todas las reglas, ordenadas por fecha de modificación.

![](assets/message-rules-access.png)

<!--To access, create, edit or delete message frequency rules, you must have the message configuration permission. [Learn more](../administration/high-low-permissions.md#administration-permissions)-->

Utilice el icono de filtro para filtrar por categoría, estado o canal. También puede buscar en la etiqueta del mensaje.

![](assets/message-rules-filter.png)

## Crear una regla {#create-new-rule}

Para crear una regla nueva, siga los pasos a continuación.

1. Acceda a la **[!UICONTROL Message frequency rules]** a continuación, haga clic en **[!UICONTROL Create rule]**.

   ![](assets/message-rules-create.png)

1. Defina el nombre de la regla.

   ![](assets/message-rules-details.png)

1. Seleccione la categoría de regla de mensaje.

   >[!NOTE]
   >
   >Actualmente solo el **[!UICONTROL Marketing]** está disponible.

1. Establezca el límite de la regla, es decir, el número máximo de mensajes que se pueden enviar a un perfil de usuario individual cada mes.

   ![](assets/message-rules-capping.png)

   >[!NOTE]
   >
   >El límite de frecuencia se basa en un período de calendario mensual. Se restablece al principio de cada mes.

1. Seleccione el canal que desee utilizar para esta regla: **[!UICONTROL Email]** o **[!UICONTROL Push notification]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Debe seleccionar al menos un canal para poder crear la regla.

1. Seleccione varios canales si desea aplicar límites a todos los canales seleccionados como recuento total.

   Por ejemplo, defina el límite en 15 y seleccione los canales de correo electrónico y push. Si un perfil ya ha recibido 10 correos electrónicos de marketing y 5 notificaciones push de marketing, este perfil se excluirá de la siguiente entrega de cualquier correo electrónico de marketing o notificación push.

1. Haga clic en **[!UICONTROL Save as draft]** para confirmar la creación de la regla. El mensaje se añade en la lista de reglas, con la variable **[!UICONTROL Draft]** estado.

   ![](assets/message-rules-created.png)

## Activar una regla {#activate-rule}

Para activar una regla de frecuencia de mensaje, haga clic en los puntos suspensivos junto a la regla y seleccione **[!UICONTROL Activate]**.

![](assets/message-rules-activate.png)

La activación de una regla afectará a los mensajes a los que se aplique en la siguiente ejecución. Obtenga información sobre cómo [aplicar una regla de frecuencia a un mensaje](#apply-frequency-rule).

>[!NOTE]
>
>No es necesario modificar o volver a publicar mensajes o recorridos para que una regla surta efecto.

Para desactivar una regla de frecuencia de mensaje, haga clic en los puntos suspensivos junto a la regla y seleccione **[!UICONTROL Deactivate]**.

![](assets/message-rules-deactivate.png)

El estado de la regla cambiará a **[!UICONTROL Inactive]** y la regla no se aplicará a futuras ejecuciones de mensajes. Los mensajes que se encuentren en ejecución no se verán afectados.

>[!NOTE]
>
>La desactivación de una regla no afecta a los perfiles individuales ni los restablece.

## Aplicación de una regla de frecuencia a un mensaje {#apply-frequency-rule}

Para aplicar una regla de frecuencia a un mensaje, simplemente debe seleccionar la categoría que definió para esta regla cuando [creación del mensaje](../messages/get-started-content.md#create-new-message).

![](assets/message-rules-properties.png)

Seleccione la **[!UICONTROL Marketing]** , todas las reglas de frecuencia de mensaje coincidentes se aplicarán automáticamente a este mensaje.

<!--Clicking the link out button next to the category selector will jump you over to the rules inventory screen to see which rules will be applied to the message.-->

Puede ver el número de perfiles excluidos del envío en la [Vistas en directo y globales](../reports/message-monitoring.md)y en la [informe de actividades de correo electrónico](../reports/email-live-report.md), donde las reglas de frecuencia se enumerarán como un posible motivo para los usuarios excluidos del envío.

## Ejemplo

Puede combinar varias reglas de frecuencia de mensajes, como se describe en el ejemplo siguiente.

1. Cree una regla llamada *Restricción general de marketing*:

   * Seleccione todos los canales (correo electrónico, push).
   * Establezca el límite en 12.

1. Para restringir aún más el número de notificaciones push basadas en marketing que envía un usuario, cree una segunda regla llamada *Limitar push de marketing*:

   * Seleccione Canal push.
   * Establezca el límite en 4.

En este escenario, un perfil individual puede recibir hasta 12 mensajes de marketing al mes, pero se excluirá de las notificaciones push de marketing después de haber recibido 4 notificaciones push.
