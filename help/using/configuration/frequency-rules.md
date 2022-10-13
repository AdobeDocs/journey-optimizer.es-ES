---
title: Reglas de frecuencia
description: Aprenda a definir las reglas de frecuencia
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: 32c69ef268c78ba834612d16b2ac1c721fb5df56
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 3%

---

# Reglas de frecuencia de mensajes {#frequency-rules}

[!DNL Journey Optimizer] le permite controlar la frecuencia con la que los usuarios recibirán un mensaje o entrar en un recorrido estableciendo reglas de canales cruzados que excluyan automáticamente los perfiles saturados de mensajes y acciones.

Por ejemplo, no desea que la marca envíe más de tres mensajes de marketing al mes a sus clientes.

Para ello, puede utilizar una regla de frecuencia que limite el número de mensajes enviados en función de uno o varios canales durante un periodo de calendario mensual.

>[!NOTE]
>
>Las reglas de frecuencia de mensajes son diferentes de la administración de exclusión, que permite a los usuarios cancelar la suscripción para recibir comunicaciones de una marca. [Más información](../privacy/opt-out.md#opt-out-management)

➡️ [Descubra esta función en vídeo](#video)

## Reglas de acceso {#access-rules}

Las reglas están disponibles en el **[!UICONTROL Administración]** > **[!UICONTROL Reglas]** para abrir el Navegador. Se muestran todas las reglas, ordenadas por fecha de modificación.

Utilice el icono de filtro para filtrar por categoría, estado o canal. También puede buscar en la etiqueta del mensaje.

![](assets/message-rules-filter.png)

### Permisos{#permissions-frequency-rules}

Para acceder, crear, editar o eliminar las reglas de frecuencia de mensajes, debe tener la variable **[!UICONTROL Administrar reglas de frecuencia]** permiso.

Los usuarios con la variable **[!UICONTROL Ver reglas de frecuencia]** pueden ver las reglas, pero no modificarlas ni eliminarlas.

![](assets/message-rules-access.png)

Obtenga más información sobre los permisos en [esta sección](../administration/high-low-permissions.md).

## Crear una regla {#create-new-rule}

Para crear una regla nueva, siga los pasos a continuación.

1. Acceda a la **[!UICONTROL Reglas de frecuencia de mensajes]** a continuación, haga clic en **[!UICONTROL Crear regla]**.

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

1. Seleccione el canal que desee utilizar para esta regla: **[!UICONTROL Correo electrónico]** o **[!UICONTROL Notificaciones push]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Debe seleccionar al menos un canal para poder crear la regla.

1. Seleccione varios canales si desea aplicar límites a todos los canales seleccionados como recuento total.

   Por ejemplo, establezca el límite en 15 y seleccione los canales de correo electrónico y push. Si un perfil ya ha recibido 10 correos electrónicos de marketing y 5 notificaciones push de marketing, este perfil se excluirá de la siguiente entrega de cualquier correo electrónico de marketing o notificación push.

1. Haga clic en **[!UICONTROL Guardar como borrador]** para confirmar la creación de la regla. El mensaje se añade a la lista de reglas, con la variable **[!UICONTROL Borrador]** estado.

   ![](assets/message-rules-created.png)

## Activar una regla {#activate-rule}

Cuando se crea, una regla de frecuencia de mensaje tiene la variable **[!UICONTROL Borrador]** y aún no afecta a ningún mensaje. Para habilitarlo, haga clic en los puntos suspensivos junto a la regla y seleccione **[!UICONTROL Activar]**.

![](assets/message-rules-activate.png)

La activación de una regla afectará a los mensajes a los que se aplique en la siguiente ejecución. Obtenga información sobre cómo [aplicar una regla de frecuencia a un mensaje](#apply-frequency-rule).

>[!NOTE]
>
>Puede tardar hasta 10 minutos en activarse completamente una regla. No es necesario modificar los mensajes ni volver a publicar recorridos para que una regla tenga efecto.

Para desactivar una regla de frecuencia de mensaje, haga clic en los puntos suspensivos junto a la regla y seleccione **[!UICONTROL Desactivar]**.

![](assets/message-rules-deactivate.png)

El estado de la regla cambiará a **[!UICONTROL Inactivo]** y la regla no se aplicará a futuras ejecuciones de mensajes. Los mensajes que se encuentren en ejecución no se verán afectados.

>[!NOTE]
>
>La desactivación de una regla no afecta a los perfiles individuales ni los restablece.

## Aplicación de una regla de frecuencia a un mensaje {#apply-frequency-rule}

Para aplicar una regla de frecuencia a un mensaje, siga los pasos a continuación.

1. [Crear un mensaje](../messages/get-started-content.md#create-new-message) seleccionando uno de los canales definidos para la regla.

1. Seleccione la categoría que definió para la variable [regla creada](#create-new-rule).

   ![](assets/inline-message-category.png)

   >[!NOTE]
   >
   >Actualmente solo el **[!UICONTROL Marketing]** está disponible para reglas de frecuencia de mensajes.

   <!--
   1. You can click the **[!UICONTROL Frequency rule]** link to view the frequency rules that will apply for the selected category and channel(s). A new tab will open to display the matching message frequency rules.-->

1. Todas las reglas de frecuencia que coincidan con la categoría y los canales seleccionados se aplicarán automáticamente a este mensaje.

   >[!NOTE]
   >
   >Mensajes <!--that do not have any selected category or messages -->donde la categoría seleccionada es **[!UICONTROL Transaccional]** no se evaluará según las reglas de frecuencia.

   <!--Clicking the link out button next to the category selector will jump you over to the rules inventory screen to see which rules will be applied to the message.-->

1. Puede ver el número de perfiles excluidos del envío en la [Informe global](../reports/global-report.md)y en la [Informe activo](../reports/live-report.md), donde las reglas de frecuencia se enumerarán como un posible motivo para los usuarios excluidos del envío.

>[!NOTE]
>
>Se pueden aplicar varias reglas al mismo canal, pero una vez alcanzado el límite inferior, el perfil se excluye de los siguientes envíos.

## Ejemplo: combinar varias reglas {#frequency-rule-example}

Puede combinar varias reglas de frecuencia de mensajes, como se describe en el ejemplo siguiente.

1. [Crear una regla](#create-new-rule) llamado *Restricción general de marketing*:

   * Seleccione los canales de correo electrónico y push.
   * Establezca el límite en 12.

   ![](assets/message-rules-ex-overall-cap.png)

1. Para restringir aún más el número de notificaciones push basadas en marketing que envía un usuario, cree una segunda regla llamada *Límite de marketing push*:

   * Seleccione Canal push.
   * Establezca el límite en 4.

   ![](assets/message-rules-ex-push-cap.png)

1. Guardar y [activar](#activate-rule) la regla.

1. Cree un correo electrónico y seleccione la opción **[!UICONTROL Marketing]** para ese mensaje. [Más información](../messages/get-started-content.md#create-new-message)

1. Cree una notificación push y seleccione la opción **[!UICONTROL Marketing]** para ese mensaje. [Más información](../messages/get-started-content.md#create-new-message)

En este escenario, un perfil individual:
* puede recibir hasta 12 mensajes de marketing al mes;
* pero se excluirán de las notificaciones push de marketing una vez que hayan recibido 4 notificaciones push.

>[!NOTE]
>
>Al probar las reglas de frecuencia, se recomienda utilizar una [perfil de prueba](../segment/creating-test-profiles.md), ya que una vez que se alcanza el límite de frecuencia de un perfil, no hay forma de restablecer el contador hasta el mes siguiente. Al desactivar una regla, los perfiles restringidos podrán recibir mensajes, pero no se eliminará ni se eliminará ningún incremento de contador.

## Vídeo explicativo {#video}

Obtenga información sobre cómo crear, activar, probar e informar sobre reglas de frecuencia.

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
