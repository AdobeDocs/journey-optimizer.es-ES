---
solution: Journey Optimizer
product: journey optimizer
title: Reglas empresariales
description: Obtenga información sobre cómo definir reglas de frecuencia
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: mensaje, frecuencia, reglas, presión
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: f47f4e783dd66d9031c7f7c447c1b20418a583c0
workflow-type: tm+mt
source-wordcount: '1262'
ht-degree: 6%

---

# Reglas empresariales {#frequency-rules}

>[!CONTEXTUALHELP]
>id="ajo_business_rules_message_frequency_rules"
>title="Reglas comerciales"
>abstract="Las reglas de frecuencia de mensajes son un tipo de regla empresarial que restringe el número de veces que los usuarios reciben mensajes o entran en recorridos a través de uno o varios canales. Estas reglas entre canales excluyen automáticamente los perfiles saturados de mensajes y acciones."

[!DNL Journey Optimizer] permite controlar la frecuencia con la que los usuarios recibirán un mensaje o entrarán en un recorrido a través de uno o varios canales. Reglas de frecuencia de mensajes que excluyen automáticamente los perfiles saturados de mensajes y acciones.

Por ejemplo, para una marca una regla podría ser no enviar más de 4 mensajes de marketing al mes a sus clientes. Para ello, puede utilizar una regla de negocio que limite el número de mensajes enviados en función de uno o más canales durante un periodo mensual del calendario.

![](assets/do-not-localize/sms-dm-rules.gif)

>[!NOTE]
>
>Las reglas empresariales son diferentes de la administración de la exclusión, que permite a los usuarios cancelar la suscripción y evitar recibir comunicaciones de una marca. [Más información](../privacy/opt-out.md#opt-out-management)

➡️ [Descubra esta función en vídeo](#video)

## Acceso a reglas empresariales {#access-rules}

Las reglas de negocio están disponibles en **[!UICONTROL Administration]** > **[!UICONTROL Reglas empresariales]** menú. Todas las reglas se enumeran y se ordenan por fecha de modificación. Utilice el icono de filtro para filtrar por categoría, estado o canal. También puede buscar en la etiqueta del mensaje.

![](assets/message-rules-filter.png)

### Permisos{#permissions-frequency-rules}

Para acceder, crear, editar o eliminar reglas de negocio, debe tener **[!UICONTROL Administrar reglas de frecuencia]** permiso.

Usuarios con **[!UICONTROL Ver reglas de frecuencia]** Los permisos de pueden ver las reglas, pero no modificarlas ni eliminarlas.

![](assets/message-rules-access.png)

Más información sobre los permisos en [esta sección](../administration/high-low-permissions.md).

## Crear una regla de negocio {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rules_category"
>title="Seleccione la categoría de regla de mensaje"
>abstract="Cuando se activa y se aplica a un mensaje, todas las reglas de negocio que coincidan con la categoría seleccionada se aplicarán automáticamente a este mensaje. Actualmente solo está disponible la categoría Marketing."

>[!CONTEXTUALHELP]
>id="ajo_rules_capping"
>title="Establezca el límite de la regla de negocio"
>abstract="Especifique el número máximo de mensajes enviados a un perfil de cliente en el lapso de tiempo elegido. El límite de frecuencia se basará en el período de calendario seleccionado y se restablecerá al comienzo del lapso de tiempo correspondiente."

>[!CONTEXTUALHELP]
>id="ajo_rules_channel"
>title="Defina los canales a los que se aplica la regla de negocio"
>abstract="Seleccione al menos un canal. El límite se aplica a todos los canales como recuento total."

Para crear una nueva regla de negocio, siga los pasos a continuación.

1. Acceda a la **[!UICONTROL Reglas empresariales]** y haga clic en **[!UICONTROL Crear regla]**.

   ![](assets/message-rules-create.png)

1. Defina el nombre de la regla y seleccione la categoría de regla de mensaje.

   >[!NOTE]
   >
   >Solo el **[!UICONTROL Marketing]** La categoría está disponible.

   ![](assets/message-rules-details.png)

1. Desde el **[!UICONTROL Duración]** , seleccione un lapso de tiempo para aplicar el límite. [Más información](#frequency-cap)

1. Establezca el límite de la regla, es decir, el número máximo de mensajes que se pueden enviar a un perfil de usuario individual cada mes o semana <!--or day--> - según su selección anterior.

   <!--![](assets/message-rules-capping.png)-->

1. Seleccione el canal que desee utilizar para esta regla: **[!UICONTROL Correo electrónico]**, **[!UICONTROL Notificación push]**, **[!UICONTROL SMS]** o **[!UICONTROL Correo directo]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Debe seleccionar al menos un canal para poder crear la regla.

1. Seleccione varios canales si desea aplicar un límite a todos los canales seleccionados como recuento total.

   Por ejemplo, establezca el límite en 15 y seleccione los canales push y de correo electrónico. Si un perfil ya ha recibido 10 correos electrónicos de marketing y 5 notificaciones push de marketing para el periodo seleccionado, este perfil se excluye de la siguiente entrega de cualquier correo electrónico de marketing o notificación push.

1. Clic **[!UICONTROL Guardar como borrador]** para confirmar la creación de la regla. El mensaje se añade a la lista de reglas, con el **[!UICONTROL Borrador]** estado.

   ![](assets/message-rules-created.png)

### Límite de frecuencia {#frequency-cap}

Desde el **[!UICONTROL Duración]** , seleccione si desea que el límite se aplique de forma mensual o semanal.

>[!NOTE]
>
>El límite diario de frecuencia también está disponible bajo demanda. [Más información](#daily-frequency-cap)

El límite de frecuencia se basa en el periodo de calendario seleccionado. Se restablece al principio del lapso de tiempo correspondiente.

![](assets/message-rules-capping-duration.png)

La caducidad del contador para cada período es la siguiente:

* **[!UICONTROL Mensual]**: el límite de frecuencia es válido hasta el último día del mes a las 23:59:59 UTC. Por ejemplo, la caducidad mensual para enero es del 31 al 01 23:59:59 UTC.

* **[!UICONTROL Semanalmente]**: El límite de frecuencia es válido hasta el sábado 23:59:59 UTC de esa semana, ya que la semana del calendario comienza el domingo. La caducidad es independiente de la creación de la regla. Por ejemplo, si la regla se crea el jueves, es válida hasta el sábado a las 23:59:59.

### Límite de frecuencia diario {#daily-frequency-cap}

Además del límite de frecuencia mensual y semanal, también está disponible bajo demanda. Para obtener más información, póngase en contacto con el representante del Adobe.

El límite diario de frecuencia es válido durante el día hasta el 23 de abril:59:59 UTC y se restablece en 0 al principio del día siguiente.

>[!NOTE]
>
>Para garantizar la precisión de las reglas diarias de límite de frecuencia, se debe utilizar [segmentación por streaming](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"} se recomienda. Obtenga más información sobre los métodos de evaluación de audiencias en [esta sección](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

## Activar una regla de negocio {#activate-rule}

Cuando se crea una regla de negocio, **[!UICONTROL Borrador]** estado y aún no afecta a ningún mensaje. Para habilitarlo, haga clic en los puntos suspensivos junto a la regla y seleccione **[!UICONTROL Activar]**.

![](assets/message-rules-activate.png)

La activación de una regla afectará a cualquier mensaje al que se aplique en su próxima ejecución. Obtenga información sobre cómo [aplicación de una regla de negocio a un mensaje](#apply-frequency-rule).

>[!NOTE]
>
>Una regla puede tardar hasta 10 minutos en activarse completamente. No es necesario modificar los mensajes ni volver a publicar los recorridos para que una regla surta efecto.

Para desactivar una regla de negocio, haga clic en los puntos suspensivos junto a la regla y seleccione **[!UICONTROL Desactivar]**.

![](assets/message-rules-deactivate.png)

El estado de la regla cambiará a **[!UICONTROL Inactivo]** y la regla no se aplicará a futuras ejecuciones de mensajes. Los mensajes que se estén ejecutando actualmente no se verán afectados.

>[!NOTE]
>
>La desactivación de una regla no afecta ni restablece ningún recuento en perfiles individuales.

## Aplicación de una regla de negocio a un mensaje {#apply-frequency-rule}

Para aplicar una regla de negocio a un mensaje, siga los pasos a continuación.

1. Al crear un [recorrido](../building-journeys/journey-gs.md), añada un mensaje seleccionando uno de los canales definidos para la regla.

1. Seleccione la categoría que definió para el [regla que ha creado](#create-new-rule).

   ![](assets/journey-message-category.png)

   >[!NOTE]
   >
   >Actualmente solo el **[!UICONTROL Marketing]** La categoría está disponible para reglas de negocio.

1. Puede hacer clic en **[!UICONTROL Regla de frecuencia]** para ver la pantalla de reglas de frecuencia en una nueva pestaña. [Más información](#access-rules)

   Todas las reglas que coincidan con la categoría y los canales seleccionados se aplicarán automáticamente a este mensaje.

   >[!NOTE]
   >
   >Mensajes en los que se selecciona la categoría **[!UICONTROL Transaccional]** no se evaluarán con reglas de frecuencia.

1. Puede ver el número de perfiles excluidos del envío en la [Informe global](../reports/global-report.md), y en el [Informe en vivo](../reports/live-report.md), donde las reglas empresariales se enumerarán como un posible motivo para que los usuarios se excluyan de la entrega.

>[!NOTE]
>
>Se pueden aplicar varias reglas al mismo canal, pero una vez alcanzado el límite inferior, el perfil se excluye de los siguientes envíos.

## Ejemplo: combinar varias reglas {#frequency-rule-example}

Puede combinar varias reglas de negocio, como se describe en el ejemplo siguiente.

1. [Crear una regla de negocio](#create-new-rule) llamado *Límite general de marketing*:

   * Seleccione todos los canales.
   * Establezca un límite de 12 al mes.

   ![](assets/message-rules-ex-overall-cap.png)

1. Para restringir aún más el número de notificaciones push basadas en marketing que se envían a un usuario, cree una segunda regla llamada *Límite de marketing push*:

   * Seleccione Canal push.
   * Establezca un límite de 4 al mes.

   ![](assets/message-rules-ex-push-cap.png)

1. Guardar y [activar](#activate-rule) la regla.

1. [Creación de un mensaje](../building-journeys/journeys-message.md) para cada canal con el que desee comunicarse y seleccione **[!UICONTROL Marketing]** categoría para cada mensaje. [Obtenga información sobre cómo aplicar una regla de negocio](#apply-frequency-rule)

   ![](assets/journey-message-category.png)


<!--
Learn how to create a message for the different channels in the following sections:
* [Create an email](../email/create-email.md)
* [Create a push notification](../push/create-push.md)
* [Create an SMS](../sms/create-sms.md)
* [Create a direct mail](../direct-mail/create-direct-mail.md)

Create an email and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../email/create-email.md)

Create a push notification and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../push/create-push.md)

Create an SMS and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../sms/create-sms.md)

Create a direct mail and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../direct-mail/create-direct-mail.md)
-->

En esta situación, un perfil individual:
* puede recibir hasta 12 mensajes de marketing al mes;
* pero se excluirán de las notificaciones push de marketing una vez que hayan recibido 4 notificaciones push.

>[!NOTE]
>
>Al probar las reglas empresariales, se recomienda utilizar un recién creado [perfil de prueba](../audience/creating-test-profiles.md), porque una vez que se alcanza el límite de frecuencia de un perfil, no hay forma de restablecer el contador hasta el mes siguiente. Al desactivar una regla, los perfiles con límite pueden recibir mensajes, pero no se elimina ni elimina ningún incremento de contador.

## Vídeo explicativo {#video}

Obtenga información sobre cómo crear, activar, probar e informar sobre reglas empresariales.

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
