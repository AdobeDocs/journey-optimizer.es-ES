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
exl-id: 80bd5a61-1368-435c-9a9a-dd84b9e4c208
source-git-commit: 43fe7ca22a7685944b2b11ca3d1872641d1f4694
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 5%

---

# Restricción de frecuencia por canal y tipo de comunicación {#rule-sets}

Los conjuntos de reglas del **canal** aplican reglas de límite a los canales de comunicación. Por ejemplo, no envíe más de 1 correo electrónico o comunicación SMS al día.

El uso de conjuntos de reglas de canal le permite establecer límites de frecuencia por tipo de comunicación para evitar sobrecargar a los clientes con mensajes similares. Por ejemplo, puede crear un conjunto de reglas para limitar el número de **comunicaciones promocionales** enviadas a sus clientes y otro conjunto de reglas para limitar el número de **boletines** enviados a ellos. Según el tipo de campaña que esté creando, puede elegir aplicar la comunicación promocional o el conjunto de reglas de los boletines informativos.

>[!IMPORTANT]
>
>Para asegurarse de que el límite de nivel de canal funciona correctamente, asegúrese de elegir el área de nombres de mayor prioridad al crear una campaña o recorrido. Obtenga más información sobre la prioridad del espacio de nombres en la [Guía del servicio de identidad de Platform](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}

## Crear una regla de límite de recorrido

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_channel"
>title="Definir los canales a los que se aplica la regla"
>abstract="Seleccione al menos un canal. El límite se aplica a todos los canales como un recuento total."

Para crear un conjunto de reglas de canal, siga estos pasos:

>[!NOTE]
>
>Puede crear hasta 10 conjuntos de reglas locales activos para cada dominio de canal y para el dominio de recorrido.

1. Acceda a la lista **[!UICONTROL Conjuntos de reglas]** y haga clic en **[!UICONTROL Crear conjunto de reglas]**.

   ![](assets/rule-sets-create-button.png)

1. Seleccione el conjunto de reglas en el que desea agregar la regla de límite o cree un nuevo conjunto de reglas:

   * Para utilizar un conjunto de reglas existente, selecciónelo en la lista. Las reglas de límite de canal solo se pueden agregar a conjuntos de reglas con el dominio &quot;canal&quot;. Puede comprobar esta información en las listas de conjuntos de reglas, en la columna **[!UICONTROL Dominio]**.

     ![](assets/journey-capping-list.png)

   * Para crear la regla de límite dentro de un nuevo conjunto de reglas, haga clic en **[!UICONTROL Crear conjunto de reglas]**, especifique un nombre único para el conjunto de reglas y seleccione &quot;Canal&quot; en la lista desplegable **[!UICONTROL Dominio del conjunto de reglas]**; a continuación, haga clic en **[!UICONTROL Guardar]**.

     ![](assets/rule-sets-create.png)

1. En la pantalla del conjunto de reglas, haga clic en el botón **[!UICONTROL Agregar regla]** y defina un nombre único para la regla.

1. El campo **Category** especifica la categoría del mensaje a la que se aplica la regla. Por ahora, este campo es de solo lectura ya que solo está disponible la categoría **[!UICONTROL Marketing]**.

   ![](assets/rule-set-channels.png)

1. En el campo **[!UICONTROL Límite]**, establezca el límite de la regla, es decir, el número máximo de mensajes que se pueden enviar a un perfil de usuario individual cada mes, semana o día u hora, según la selección que haya hecho en los campos siguientes.

1. En la lista desplegable **[!UICONTROL Restablecer frecuencia límite]**, seleccione si desea que el límite se aplique cada hora, cada día, cada semana o cada mes. El límite de frecuencia se basa en el periodo de calendario seleccionado. Se restablece al principio del lapso de tiempo correspondiente.

   La caducidad del contador para cada período es la siguiente:

   * **[!UICONTROL Por hora]**: el límite de frecuencia es válido para el número seleccionado de horas (mínimo de 3 horas). El contador se restablece automáticamente al principio de cada intervalo de tiempo. Para un límite de frecuencia de 3 horas, se restablece cada 3 horas, coincidiendo con el final de una hora UTC.

     >[!AVAILABILITY]
     >
     >Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Póngase en contacto con el Servicio de atención al cliente para activarlo.

   * **[!UICONTROL Diario]**: el límite de frecuencia diario es válido para el día hasta el 23:59:59 UTC y se restablece en 0 al comienzo del día siguiente.
   * **[!UICONTROL Semanal]**: el límite de frecuencia es válido hasta el sábado 23:59:59 UTC de esa semana, ya que la semana del calendario comienza el domingo. La fecha de caducidad se aplica independientemente del momento en que se creó la regla. Por ejemplo, si la regla se crea el jueves, es válida hasta el sábado a las 23:59:59.
   * **[!UICONTROL Mensual]**: el límite de frecuencia es válido hasta el último día del mes a las 23:59:59 UTC. Por ejemplo, la caducidad mensual para enero es del 01 al 31 23:59:59 UTC.

   >[!IMPORTANT]
   >
   >* Para garantizar la precisión, asegúrese de elegir el área de nombres de mayor prioridad al crear una campaña o recorrido. Obtenga más información sobre la prioridad del espacio de nombres en la [Guía del servicio de identidad de Platform](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}<br/>
   >
   >* El valor del contador de perfiles se actualiza una vez que se envía la comunicación. Tenga esto en cuenta cuando envíe grandes volúmenes de comunicaciones, ya que el rendimiento podría provocar que el destinatario reciba el correo electrónico minutos o incluso horas después del inicio de la comunicación (en el caso de que envíe millones de comunicaciones simultáneamente). Esto es importante en el caso de que un destinatario reciba dos comunicaciones muy juntas. Sugerimos separar las comunicaciones por lo menos dos horas cuando sea posible para dar tiempo suficiente al destinatario para recibir la comunicación y al valor del contador para actualizar en consecuencia.

1. El campo **[!UICONTROL Cada]** le permite repetir las reglas de restricción de frecuencia durante varias horas, días, semanas o meses, según la duración especificada. Ejemplo: aplique la regla de límite de frecuencia durante 2 semanas.

   Asegúrese de introducir un valor que coincida con el tipo de duración seleccionado: 3-23 para cada hora, 1-30 para cada día, 1-4 para semanales y 1-3 para mensuales.

   El contador se restablece automáticamente a 0 cuando comienza una nueva ventana de tiempo. Para un límite de frecuencia de 2 días, este restablecimiento se produce cada dos días a medianoche UTC.

1. Seleccione el canal que desee usar para esta regla: **[!UICONTROL Correo electrónico]**, **[!UICONTROL SMS]**, **[!UICONTROL Notificación push]** o **[!UICONTROL Correo directo]**.

1. Seleccione varios canales si desea aplicar un límite a todos los canales seleccionados como recuento total.

   Por ejemplo, establezca el límite en 5 y seleccione los canales de correo electrónico y SMS. Si un perfil ya ha recibido 3 correos electrónicos de marketing y 2 SMS de marketing para el periodo seleccionado, este perfil se excluirá de la siguiente entrega de cualquier correo electrónico o SMS de marketing.

1. Haga clic en **[!UICONTROL Guardar]** para confirmar la creación de la regla. Su mensaje se agrega al conjunto de reglas, con el estado **[!UICONTROL Borrador]**.

   ![](assets/rule-set-rule-created.png)

1. Repita los pasos anteriores para agregar tantas reglas como sea necesario al conjunto de reglas.

1. Cuando la regla de límite esté lista para aplicarse a los mensajes, active el conjunto de reglas y la regla en la que se ha agregado. [Aprenda a activar conjuntos de reglas](../conflict-prioritization/rule-sets.md#create)

## Aplicación de conjuntos de reglas a un mensaje {#apply-frequency-rule}

Para aplicar un conjunto de reglas a un mensaje, siga estos pasos:

1. Al crear un mensaje de recorrido o de campaña, seleccione uno de los canales definidos para el conjunto de reglas y edite el contenido del mensaje

1. En la pantalla de edición de contenido, haga clic en el botón **[!UICONTROL Agregar regla de negocio]**.

1. Seleccione el conjunto de reglas que ha creado.

   ![](assets/rule-set-campaign-add-rule-button.png)

   >[!NOTE]
   >
   >En la lista solo se muestran [conjuntos de reglas activados](#activate-rule).

   <!--Messages where the category selected is **[!UICONTROL Transactional]** will not be evaluated against business rules.-->

1. Antes de activar el recorrido o la campaña, asegúrese de programar su ejecución al menos 10 minutos en el futuro.

   Esto permite disponer de tiempo suficiente para rellenar los valores de contador en el perfil para la regla de negocio seleccionada. Si activa la campaña inmediatamente, los valores del contador del conjunto de reglas no se rellenan en los perfiles de los destinatarios y el mensaje no se contabiliza en sus reglas de límite de frecuencia para los conjuntos de reglas personalizadas. Además, es posible que el límite no funcione correctamente para recorridos y campañas activadas inmediatamente y campañas activadas por API.

   ![](assets/rule-set-schedule-campaign.png)

1. Puede ver el número de perfiles excluidos del envío en el [informe de Customer Journey Analytics](../reports/report-gs-cja.md) y en el [informe en vivo](../reports/live-report.md), donde las reglas de frecuencia se enumerarán como un posible motivo para excluir a los usuarios del envío.

>[!NOTE]
>
>Se pueden aplicar varias reglas al mismo canal, pero una vez alcanzado el límite inferior, el perfil se excluye de los siguientes envíos.

Al probar las reglas de frecuencia, se recomienda usar un [perfil de prueba](../audience/creating-test-profiles.md) recién creado, ya que una vez que se alcanza el límite de frecuencia de un perfil, no hay forma de restablecer el contador hasta el siguiente período. Al desactivar una regla, los perfiles con límite pueden recibir mensajes, pero no se elimina ni elimina ningún incremento de contador.

<!--add a new section for default priority namespace.-->

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

## Vídeo práctico {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3444729?quality=12&captions=spa)
