---
solution: Journey Optimizer
product: journey optimizer
title: Reglas empresariales
description: Obtenga información sobre cómo crear y aplicar reglas empresariales
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: mensaje, frecuencia, reglas, presión
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: c1eef06b0edc4e1bcd1b145f8f822295924b205c
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 10%

---

# Reglas empresariales {#business-rules}

>[!AVAILABILITY]
>
>Actualmente, las reglas empresariales están disponibles como una versión beta para seleccionar solo usuarios.

[!DNL Journey Optimizer] permite controlar la frecuencia con la que los usuarios recibirán un mensaje configurando reglas entre canales que excluirán automáticamente los perfiles saturados de los mensajes y las acciones.

Por ejemplo, para una marca, una regla podría ser: enviar no más de 4 mensajes de marketing al mes a sus clientes. Para ello, puede utilizar una regla de frecuencia que limite el número de mensajes enviados en función de uno o más canales durante un periodo mensual del calendario.

Mediante la creación de diferentes conjuntos de reglas para mejorar la granularidad, [!DNL Journey Optimizer] permite aplicar límites de frecuencia a diferentes tipos de comunicaciones de marketing. Por ejemplo, puede crear un conjunto de reglas para limitar el número de **comunicaciones promocionales** enviado a sus clientes y cree otro conjunto de reglas para limitar el número de **boletines** enviado a ellos.

>[!NOTE]
>
>Las reglas empresariales son diferentes de la administración de la exclusión, que permite a los usuarios cancelar la suscripción y evitar recibir comunicaciones de una marca. [Más información](../privacy/opt-out.md#opt-out-management)

## Conjuntos de reglas de acceso {#access-rule-sets}

Los conjuntos de reglas están disponibles en **[!UICONTROL Administration]** > **[!UICONTROL Reglas empresariales (beta)]** menú. Todas las reglas se enumeran y se ordenan por fecha de creación.

![](assets/rule-sets-list.png)

Haga clic en el nombre de un conjunto de reglas para ver y editar su contenido. Se muestran todas las reglas incluidas en ese conjunto de reglas.

El menú contextual de la parte superior derecha le permite:

* Editar el nombre y la descripción del conjunto de reglas
* Activar el conjunto de reglas: [obtenga más información](#activate-rule)
* Eliminar el conjunto de reglas

![](assets/rule-set-example.png)

Para cada regla del conjunto de reglas, la variable **[!UICONTROL Más acciones]** El botón permite:

* Editar la regla
* Activar la regla [obtenga más información](#activate-rule)
* Eliminar la regla

![](assets/rule-set-example-rules.png)

<!--### Permissions{#permissions-frequency-rules}

To access, create, edit or delete message frequency rules, you must have the **[!UICONTROL Manage frequency rules]** permission. 

Users with the **[!UICONTROL View frequency rules]** permission are able to view rules, but not to modify or delete them.

![](assets/message-rules-access.png)

Learn more about permissions in [this section](../administration/high-low-permissions.md).-->

## Crear un conjunto de reglas {#create-rule-set}

Para crear un conjunto de reglas, siga los pasos a continuación.

1. Acceda a la **[!UICONTROL Conjuntos de reglas]** y haga clic en **[!UICONTROL Crear conjunto de reglas]**.

   ![](assets/rule-sets-create-button.png)

1. Defina el nombre del conjunto de reglas, añada una descripción si lo desea y haga clic en **[!UICONTROL Guardar]**.

   ![](assets/rule-sets-create.png)

   >[!NOTE]
   >
   >El nombre del conjunto de reglas debe ser único.

1. Ahora puede [definir las reglas](#create-new-rule) desea agregar a este conjunto de reglas, y [activar](#activate-rule) it.

   >[!NOTE]
   >
   >Asegúrese de que todas las reglas que desee aplicar a los mensajes también estén activadas en el conjunto de reglas.

## Crear una regla {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_category"
>title="Seleccione la categoría de regla de mensaje"
>abstract="Cuando está activada y se aplica a un mensaje, todas las reglas de frecuencia que coincidan con la categoría seleccionada se aplican automáticamente a este mensaje. Actualmente solo está disponible la categoría Marketing."

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_capping"
>title="Establezca el límite de la regla"
>abstract="Especifique el número máximo de mensajes enviados a un perfil de cliente en el lapso de tiempo elegido. El límite de frecuencia se basará en el período de calendario seleccionado y se restablecerá al principio del lapso de tiempo correspondiente."

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_channel"
>title="Definir los canales a los que se aplica la regla"
>abstract="Seleccione al menos un canal. El límite se aplica a todos los canales como un recuento total."

Para agregar una regla a un conjunto de reglas, siga los pasos a continuación.

1. En el conjunto de reglas que acaba de crear, haga clic en **[!UICONTROL Añadir regla]**.

   ![](assets/rule-sets-create-rule-button.png)

1. Defina el nombre de la regla.

   >[!NOTE]
   >
   >El nombre del conjunto de reglas debe ser único.

1. Seleccione la categoría de regla de mensaje.

   >[!NOTE]
   >
   >Actualmente solo el **[!UICONTROL Marketing]** La categoría está disponible.

1. Desde el **[!UICONTROL Duración]** , seleccione un lapso de tiempo para aplicar el límite. [Más información](#frequency-cap)

1. Establezca el límite de la regla, es decir, el número máximo de mensajes que se pueden enviar a un perfil de usuario individual cada mes, semana o día, según la selección anterior.

1. Seleccione el canal que desee utilizar para esta regla: **[!UICONTROL Correo electrónico]**, **[!UICONTROL SMS]**, **[!UICONTROL Notificación push]** o **[!UICONTROL Correo directo]**.

   ![](assets/rule-set-channels.png)

   >[!NOTE]
   >
   >Debe seleccionar al menos un canal para poder crear la regla.

1. Seleccione varios canales si desea aplicar un límite a todos los canales seleccionados como recuento total.

   Por ejemplo, establezca el límite en 5 y seleccione los canales de correo electrónico y SMS. Si un perfil ya ha recibido 3 correos electrónicos de marketing y 2 SMS de marketing para el periodo seleccionado, este perfil se excluirá de la siguiente entrega de cualquier correo electrónico o SMS de marketing.

1. Clic **[!UICONTROL Guardar]** para confirmar la creación de la regla. El mensaje se añade al conjunto de reglas, con la variable **[!UICONTROL Borrador]** estado.

   ![](assets/rule-set-rule-created.png)

1. Repita los pasos anteriores para agregar tantas reglas como sea necesario al conjunto de reglas.

Ahora debe activar cada regla para poder aplicarla a cualquier mensaje. [Más información](#activate-rule)

>[!NOTE]
>
>Asegúrese de que el conjunto de reglas también esté activado para poder seleccionarlo en los mensajes.

### Límite de frecuencia {#frequency-cap}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_duration"
>title="Seleccione la categoría de regla de mensaje"
>abstract="Cuando está activada y se aplica a un mensaje, todas las reglas de frecuencia que coincidan con la categoría seleccionada se aplican automáticamente a este mensaje. Actualmente solo está disponible la categoría Marketing."

Desde el **[!UICONTROL Duración]** , seleccione si desea que el límite se aplique mensualmente, semanalmente o diariamente.

El límite de frecuencia se basa en el periodo de calendario seleccionado. Se restablece al principio del lapso de tiempo correspondiente.

![](assets/rule-set-capping-duration.png)

La caducidad del contador para cada período es la siguiente:

* **[!UICONTROL Mensual]**: el límite de frecuencia es válido hasta el último día del mes a las 23:59:59 UTC. Por ejemplo, la caducidad mensual para enero es del 31 al 01 23:59:59 UTC.

* **[!UICONTROL Semanalmente]**: El límite de frecuencia es válido hasta el sábado 23:59:59 UTC de esa semana, ya que la semana del calendario comienza el domingo. La caducidad es independiente de la creación de la regla. Por ejemplo, si la regla se crea el jueves, es válida hasta el sábado a las 23:59:59.

* **[!UICONTROL Diario]**: el límite de frecuencia diario es válido para el día hasta el 23:59:59 UTC y se restablece en 0 al principio del día siguiente.

### Límite de frecuencia diario {#daily-frequency-cap}

>[!CAUTION]
>
>Para garantizar la precisión de las reglas diarias de límite de frecuencia, se debe utilizar [segmentación por streaming](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"} es obligatorio. Obtenga más información sobre los métodos de evaluación de audiencias en [esta sección](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

Para cualquier tamaño de segmento hasta el límite de 60 millones de mensajes por hora<!--not clear-->, asegúrese de que las campañas se diferencien al menos dos horas.


<!-- Journey example:

* If customer sets a Daily rule under the Global Ruleset for email <= 2/day:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for noon)
   * Journey 789 (scheduled for 1 pm)

   In this example, the Daily Frequency cap will not guarantee <= 2/day. The rule will only be guaranteed when Journeys are at least 2 hours apart:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for 2 pm)
   * Journey 789 (scheduled for 4 pm)-->

Por ejemplo, si establece una regla diaria en un conjunto de reglas para el canal de correo electrónico de menos o igual a 2 días y crea las siguientes campañas:
* Campaña A (programada para el mediodía)
* Campaña A (programada para las 3 p. m.)
* Campaña B (programada para la 1 p. m.)

Esta configuración no funcionará por dos motivos:
* No se garantiza el límite de frecuencia diario, ya que las campañas no están separadas por dos horas.
* No es recomendable programar la misma campaña varias veces en un mismo día para aprovechar el límite diario.

El ejemplo siguiente debe respetarse con el límite de frecuencia diario:
* Campaña A (programada para el mediodía)
* Campaña B (programada para las 14:00)

<!--* To use the Daily Cap with a Journey, customers can use either an Event Triggered Journey or an Audience Qualified Journey. If customers wish to use the Daily Cap with a Read Audience Journey, they should use a Campaign instead and associate a Local Ruleset with the campaign, following the example given above.-->

## Activar reglas y conjuntos de reglas {#activate-rule}

Cuando se crea una regla, tiene el **[!UICONTROL Borrador]** estado y aún no afecta a ningún mensaje. Para habilitarlo, haga clic en **[!UICONTROL Más acciones]** junto a la regla y seleccione **[!UICONTROL Activar]**.

![](assets/rule-set-activate-rule.png)

También debe activar el conjunto de reglas para poder acceder a él en campañas/recorridos y aplicarlo a los mensajes.

![](assets/rule-set-activate-set.png)

La activación de un conjunto de reglas afectará a cualquier mensaje al que se aplique en su próxima ejecución. Obtenga información sobre cómo [aplicación de un conjunto de reglas a un mensaje](#apply-rule-set).

>[!NOTE]
>
>Una regla o un conjunto de reglas puede tardar hasta 10 minutos en activarse completamente. No es necesario modificar los mensajes ni volver a publicar los recorridos para que una regla surta efecto.

<!--Currently, once a rule set is activated, no more rules can be added to that rule set.-->

## Desactivar reglas y conjuntos de reglas {#deactivate-rule}

Para desactivar una regla o un conjunto de reglas, haga clic en **[!UICONTROL Más acciones]** junto al elemento deseado y seleccione **[!UICONTROL Desactivar]**.

![](assets/rule-set-inactive-rule.png)

Su estado cambiará a **[!UICONTROL Inactivo]** y la regla no se aplicará a futuras ejecuciones de mensajes. Los mensajes que se estén ejecutando actualmente no se verán afectados.

>[!NOTE]
>
>La desactivación de una regla o un conjunto de reglas no afecta ni restablece ningún recuento de perfiles individuales.

## Aplicación de una regla de frecuencia a un mensaje {#apply-frequency-rule}

Para aplicar una regla de frecuencia a un mensaje, siga los pasos a continuación.

1. Al crear un [campaña](../campaigns/create-campaign.md), seleccione uno de los canales definidos para el conjunto de reglas y edite el contenido del mensaje.

1. En la pantalla de edición de contenido, haga clic en **[!UICONTROL Agregar regla de negocio]** botón.

1. Seleccione el [conjunto de reglas creado](#create-rule-set).

   ![](assets/rule-set-campaign-add-rule-button.png)

   >[!NOTE]
   >
   >Solo [activado](#activate-rule) los conjuntos de reglas se muestran en la lista.

   <!--Messages where the category selected is **[!UICONTROL Transactional]** will not be evaluated against business rules.-->

1. Puede ver el número de perfiles excluidos del envío en la [Informe global](../reports/global-report.md), y en el [Informe en vivo](../reports/live-report.md), donde las reglas de frecuencia se enumerarán como un posible motivo para excluir a los usuarios del envío.

>[!NOTE]
>
>Se pueden aplicar varias reglas al mismo canal, pero una vez alcanzado el límite inferior, el perfil se excluye de los siguientes envíos.

<!--
## Example: combine several rules {#frequency-rule-example}

You can combine several message frequency rules, such as described in the example below.

1. [Create a rule](#create-new-rule) called *Overall Marketing Capping*:

   * Select all channels.
   * Set capping to 12 monthly.

   ![](assets/message-rules-ex-overall-cap.png)

1. To further restrict the number of marketing-based push notifications that a user is sent, create a second rule called *Push Marketing Cap*:

   * Select Push channel.
   * Set capping to 4 monthly.

   ![](assets/message-rules-ex-push-cap.png)

1. Save and [activate](#activate-rule) the rule.

1. [Create a message](../building-journeys/journeys-message.md) for every channel you want to communicate through and select the **[!UICONTROL Marketing]** category for each message. [Learn how to apply a frequency rule](#apply-frequency-rule)

   ![](assets/journey-message-category.png)

In this scenario, an individual profile:
* can receive up to 12 marketing messages per month;
* but will be excluded from marketing push notifications after they have received 4 push notifications.-->

Al probar las reglas de frecuencia, se recomienda utilizar un [perfil de prueba](../audience/creating-test-profiles.md), porque una vez que se alcanza el límite de frecuencia de un perfil, no hay forma de restablecer el contador hasta el siguiente período. Al desactivar una regla, los perfiles con límite pueden recibir mensajes, pero no se elimina ni elimina ningún incremento de contador.

