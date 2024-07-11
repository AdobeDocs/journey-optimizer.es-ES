---
solution: Journey Optimizer
product: journey optimizer
title: Trabajar con conjuntos de reglas
description: Obtenga información sobre cómo crear y aplicar conjuntos de reglas
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: mensaje, frecuencia, reglas, presión
badge: label="Beta"
hide: true
hidefromtoc: true
exl-id: 07f5f0b4-417e-408e-8d9e-86615c8a3fbf
source-git-commit: f47f4e783dd66d9031c7f7c447c1b20418a583c0
workflow-type: tm+mt
source-wordcount: '1593'
ht-degree: 12%

---

# Trabajar con conjuntos de reglas {#rule-sets}

>[!CONTEXTUALHELP]
>id="ajo_business_rules_rule_sets"
>title="Conjuntos de reglas"
>abstract="Utilice conjuntos de reglas para aplicar límites de frecuencia a diferentes tipos de comunicaciones de marketing. Por ejemplo, puede crear un conjunto de reglas para limitar el número de **comunicaciones promocionales** que se han enviado a sus clientes y crear otro conjunto de reglas para limitar el número de **boletines** que se les ha enviado."

>[!AVAILABILITY]
>
>Actualmente, los conjuntos de reglas solo están disponibles como una versión beta para los usuarios seleccionados. Póngase en contacto con el representante del Adobe para que se le incluya en el Beta.

## ¿Qué son los conjuntos de reglas? {#what}

Además de las reglas empresariales globales que restringen el número de veces que los usuarios reciben mensajes en uno o varios canales, los conjuntos de reglas le permiten **agrupar varias reglas en conjuntos de reglas** y aplíquelas a las campañas que elija. Esto proporciona una granularidad mejorada para controlar la frecuencia con la que los usuarios recibirán un mensaje según el tipo de comunicación.

Por ejemplo, puede crear un conjunto de reglas para limitar el número de **comunicaciones promocionales** enviado a sus clientes y otro conjunto de reglas para limitar el número de **boletines** enviado a ellos. Según el tipo de campaña que esté creando, puede elegir aplicar la comunicación promocional o el conjunto de reglas de los boletines informativos.

## Conjuntos de reglas globales y personalizadas {#global-custom}

Al acceder a los conjuntos de reglas por primera vez desde el **[!UICONTROL Administration]** > **[!UICONTROL Reglas empresariales (Beta)]** menú, un conjunto de reglas predeterminado está creado previamente y activo: **Conjunto de reglas globales predeterminadas**.

Este conjunto de reglas contiene reglas globales que puede aplicar para controlar la frecuencia con la que los usuarios reciben mensajes a través de uno o varios canales, de forma similar a como funcionan las reglas empresariales actuales. Todas las reglas definidas en este conjunto de reglas se aplican a todos los canales seleccionados, independientemente de si las comunicaciones se envían desde un recorrido o desde una campaña. [Aprenda a trabajar con reglas empresariales](frequency-rules.md)

Además de este conjunto de reglas predeterminado global, puede crear lo siguiente **regla personalizada** establece que se puede aplicar a cualquier campaña para restringir el número de mensajes enviados dentro de esa campaña. [Obtenga información sobre cómo crear conjuntos de reglas personalizadas](#create)

![](assets/rule-sets-default.png)

>[!IMPORTANT]
>
>Por ahora, los conjuntos de reglas personalizadas se pueden aplicar a **campañas** solo. Solo las reglas definidas en el conjunto de reglas &quot;Conjunto de reglas predeterminado global&quot; se aplican a las comunicaciones de recorridos y campañas.

## Creación de su primer conjunto de reglas personalizadas {#create-rule-set}

### Creación del conjunto de reglas {#create}

Para crear un conjunto de reglas, siga los pasos a continuación.

>[!NOTE]
>
>Puede crear hasta 3 conjuntos de reglas personalizadas.

1. Acceda a la **[!UICONTROL Conjuntos de reglas]** y haga clic en **[!UICONTROL Crear conjunto de reglas]**.

   ![](assets/rule-sets-create-button.png)

1. Defina el nombre del conjunto de reglas, añada una descripción si lo desea y haga clic en **[!UICONTROL Guardar]**.

   ![](assets/rule-sets-create.png)

   >[!NOTE]
   >
   >El nombre del conjunto de reglas debe ser único.

1. Ahora puede [definir las reglas](#create-new-rule) desea agregar a este conjunto de reglas.

### Añadir reglas al conjunto de reglas {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_category"
>title="Seleccione la categoría de regla de mensaje"
>abstract="Cuando está activada y se aplica a un mensaje, todas las reglas de frecuencia que coincidan con la categoría seleccionada se aplican automáticamente a este mensaje. Actualmente, solo está disponible la categoría Marketing."

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_capping"
>title="Establezca el límite de la regla"
>abstract="Especifique el número máximo de mensajes enviados a un perfil de cliente en el lapso de tiempo elegido. El límite de frecuencia se basará en el período de calendario seleccionado y se restablecerá al principio del lapso de tiempo correspondiente."

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_channel"
>title="Definir los canales a los que se aplica la regla"
>abstract="Seleccione al menos un canal. El límite se aplica a todos los canales como un recuento total."

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_duration"
>title="Seleccione la categoría de regla de mensaje"
>abstract="Cuando está activada y se aplica a un mensaje, todas las reglas de frecuencia que coincidan con la categoría seleccionada se aplican automáticamente a este mensaje. Actualmente, solo está disponible la categoría Marketing."

Para agregar una regla a un conjunto de reglas, siga los pasos a continuación.

1. En el conjunto de reglas que acaba de crear, haga clic en **[!UICONTROL Añadir regla]**.

   ![](assets/rule-sets-create-rule-button.png)

1. Definir un único **Nombre de regla**.

1. El **Categoría** especifica la categoría del mensaje al que se aplica la regla. Por ahora, este campo es de solo lectura como solo la variable **[!UICONTROL Marketing]** La categoría está disponible.

1. Desde el **[!UICONTROL Duración]** , seleccione si desea que el límite se aplique mensualmente, semanalmente o diariamente. El límite de frecuencia se basa en el periodo de calendario seleccionado. Se restablece al principio del lapso de tiempo correspondiente.

   ![](assets/rule-set-capping-duration.png)

   La caducidad del contador para cada período es la siguiente:

   * **[!UICONTROL Mensual]**: el límite de frecuencia es válido hasta el último día del mes a las 23:59:59 UTC. Por ejemplo, la caducidad mensual para enero es del 31 al 01 23:59:59 UTC.

   * **[!UICONTROL Semanalmente]**: El límite de frecuencia es válido hasta el sábado 23:59:59 UTC de esa semana, ya que la semana del calendario comienza el domingo. La caducidad es independiente de la creación de la regla. Por ejemplo, si la regla se crea el jueves, es válida hasta el sábado a las 23:59:59.

   * **[!UICONTROL Diario]**: el límite de frecuencia diario es válido para el día hasta el 23:59:59 UTC y se restablece en 0 al principio del día siguiente.

     >[!CAUTION]
     >
     >Para garantizar la precisión de las reglas diarias de límite de frecuencia, se debe utilizar [segmentación por streaming](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"} es obligatorio. Obtenga más información sobre los métodos de evaluación de audiencias en [esta sección](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

   Tenga en cuenta que el valor del contador de perfiles se actualiza una vez que se envía la comunicación. Tenga esto en cuenta cuando envíe grandes volúmenes de comunicaciones, ya que el rendimiento podría provocar que el destinatario reciba el correo electrónico minutos o incluso horas después del inicio de la comunicación (en el caso de que envíe millones de comunicaciones simultáneamente).

   Esto es importante en el caso de que un destinatario reciba dos comunicaciones muy juntas. Sugerimos separar las comunicaciones por lo menos dos horas cuando sea posible para dar tiempo suficiente al destinatario para recibir la comunicación y al valor del contador para actualizar en consecuencia.

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

### Activar las reglas y el conjunto de reglas {#activate-rule}

Cuando se crea una regla, tiene el **[!UICONTROL Borrador]** estado y aún no afecta a ningún mensaje. Para habilitarlo, haga clic en **[!UICONTROL Más acciones]** junto a la regla y seleccione **[!UICONTROL Activar]**.

![](assets/rule-set-activate-rule.png)

También debe activar el conjunto de reglas para poder acceder a él en campañas/recorridos y aplicarlo a los mensajes.

![](assets/rule-set-activate-set.png)

>[!NOTE]
>
>Una regla o un conjunto de reglas puede tardar hasta 10 minutos en activarse completamente. No es necesario modificar los mensajes ni volver a publicar los recorridos para que una regla surta efecto.

<!--Currently, once a rule set is activated, no more rules can be added to that rule set.-->

Para desactivar una regla o un conjunto de reglas, haga clic en **[!UICONTROL Más acciones]** junto al elemento deseado y seleccione **[!UICONTROL Desactivar]**.

![](assets/rule-set-inactive-rule.png)

Su estado cambiará a **[!UICONTROL Inactivo]** y la regla no se aplicará a futuras ejecuciones de mensajes. Los mensajes que se estén ejecutando actualmente no se verán afectados.

>[!NOTE]
>
>La desactivación de una regla o un conjunto de reglas no afecta ni restablece ningún recuento de perfiles individuales.

## Acceso y administración de conjuntos de reglas {#access-rule-sets}

Todos los conjuntos de reglas creados se muestran en **[!UICONTROL Administration]** > **[!UICONTROL Reglas empresariales (Beta)]** menú. Se ordenan por fecha de la última modificación.

![](assets/rule-sets-list.png)

Haga clic en el nombre de un conjunto de reglas para ver y editar su contenido. Se muestran todas las reglas incluidas en ese conjunto de reglas. El menú contextual de la parte superior derecha le permite:

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

## Aplicación de un conjunto de reglas a un mensaje {#apply-frequency-rule}

Para aplicar una regla de negocio a un mensaje, siga los pasos a continuación.

1. Al crear un [campaña](../campaigns/create-campaign.md), seleccione uno de los canales definidos para el conjunto de reglas y edite el contenido del mensaje.

1. En la pantalla de edición de contenido, haga clic en **[!UICONTROL Agregar regla de negocio]** botón.

1. Seleccione el [conjunto de reglas creado](#create-rule-set).

   ![](assets/rule-set-campaign-add-rule-button.png)

   >[!NOTE]
   >
   >Solo [activado](#activate-rule) los conjuntos de reglas se muestran en la lista.

   <!--Messages where the category selected is **[!UICONTROL Transactional]** will not be evaluated against business rules.-->

1. Antes de activar la campaña, asegúrese de programar su ejecución al menos 10 minutos en el futuro.

   Esto permite disponer de tiempo suficiente para rellenar los valores de contador en el perfil para la regla de negocio seleccionada. Si activa la campaña inmediatamente, los valores del contador del conjunto de reglas no se rellenan en los perfiles de los destinatarios y el mensaje no se contabiliza en sus reglas de límite de frecuencia para los conjuntos de reglas personalizadas.

   ![](assets/rule-set-schedule-campaign.png)

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
