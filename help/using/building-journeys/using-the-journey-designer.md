---
title: Diseño de un recorrido
description: Aprenda a diseñar su recorrido
feature: Recorridos
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '1407'
ht-degree: 2%

---

# Diseño de un recorrido

![](../assets/do-not-localize/badge.png)

La interfaz de recorrido permite arrastrar y soltar fácilmente actividades de la paleta en el lienzo. También puede hacer doble clic en una actividad para agregarla al lienzo en el siguiente paso disponible. Cada actividad tiene una función y un lugar específicos en el proceso. Las actividades se secuencian. Cuando finaliza una actividad, el flujo continúa y procesa la siguiente actividad, etc.

## Introducción al diseño de recorrido

La **paleta** se encuentra en el lado izquierdo de la pantalla. Todas las actividades disponibles se clasifican en varias categorías: **[!UICONTROL Events]**, **[!UICONTROL Orchestration]** y **[!UICONTROL Actions]**. Puede expandir/contraer las diferentes categorías haciendo clic en su nombre. Para utilizar una actividad en el recorrido, arrástrela desde la paleta y suéltela en el lienzo.

Al iniciar un nuevo recorrido, los elementos que no se pueden soltar en el lienzo como primer paso se ocultan. Esto se refiere a todas las acciones, la actividad de la condición, la espera y la reacción.

![](../assets/journey38.png)

El icono **[!UICONTROL Filter items]** en la esquina superior izquierda permite mostrar los siguientes filtros:

* **Mostrar solo los elementos** disponibles: oculte o muestre elementos no disponibles en la paleta, por ejemplo, los eventos que utilizan un área de nombres diferente a la utilizada en el recorrido. De forma predeterminada, los elementos no disponibles están ocultos. Si elige mostrarlos, aparecerán atenuados.

* **Mostrar solo los elementos** recientes: este filtro le permite mostrar solo los últimos cinco eventos y acciones utilizados, además de los predeterminados. Esto es específico de cada usuario. De forma predeterminada, se muestran todos los elementos.

También puede utilizar el campo **[!UICONTROL Search]** .

El **lienzo** es la zona central del diseñador de recorridos. Es en esta zona donde puede soltar sus actividades y configurarlas. Haga clic en una actividad del lienzo para configurarla. Se abre el panel de configuración de actividad en el lado derecho.

![](../assets/journey39.png)

El **panel de configuración de actividad** aparece al hacer clic en una actividad de la paleta. Rellene los campos obligatorios. Haga clic en el icono **[!UICONTROL Delete]** para eliminar la actividad. Haga clic en **[!UICONTROL Cancel]** para cancelar las modificaciones o en **[!UICONTROL Ok]** para confirmar. Para eliminar actividades, también puede seleccionar una actividad (o varias) y pulsar la tecla de retroceso. Si pulsa la tecla escape, se cerrará el panel de configuración de la actividad.

De forma predeterminada, los campos de solo lectura están ocultos. Para mostrarlos, haga clic en el icono **Show read-only fields** en la parte superior izquierda del panel de configuración de la actividad.

![](../assets/journey59bis.png)

Según el estado del recorrido, puede realizar diferentes acciones en el recorrido mediante los botones disponibles en la esquina superior derecha: **[!UICONTROL Publish]**, **[!UICONTROL Duplicate]**, **[!UICONTROL Delete]**, **[!UICONTROL Journey properties]**, **[!UICONTROL Test]**. Estos botones aparecen cuando no hay actividad seleccionada. Algunos botones aparecerán en contexto. El botón de registro del modo de prueba aparece cuando se activa el modo de prueba.

![](../assets/journey41.png)

## Inicio del recorrido

Al diseñar el recorrido, la primera pregunta que desea hacer es cómo entrarán los perfiles en el recorrido. Hay dos posibilidades:

**Comience con un evento**: cuando un recorrido está configurado para escuchar eventos, las personas entran en el recorrido  **** unitarilyin real. Los mensajes incluidos en el recorrido se envían a la persona que actualmente fluye al recorrido. [Más información sobre los eventos](../event/about-events.md)

**Comience con un segmento** de lectura: puede configurar el recorrido para que escuche los segmentos de Adobe Experience Platform. En este caso, todas las personas que pertenecen al segmento especificado entran en el recorrido. Los mensajes incluidos en el recorrido se envían a las personas pertenecientes al segmento. [Obtenga más información sobre la lectura de segmentos](read-segment.md).

## Defina los pasos siguientes

Después del primer evento o segmento de lectura, puede combinar las diferentes actividades para crear sus escenarios de canales cruzados de varios pasos. Elija, en la paleta, los pasos que necesite.

**Eventos**

Cuando inicie el recorrido con un evento , el recorrido se activará cuando se reciba el evento. La persona seguirá, individualmente, los siguientes pasos definidos en su recorrido.

Puede agregar **varios eventos** en el recorrido, siempre que utilicen el mismo espacio de nombres. Los eventos se configuran de antemano. [Más información sobre los eventos](about-journey-activities.md#event-activities)

También puede agregar un evento **Reaction** después de un mensaje para reaccionar ante los datos de seguimiento relacionados con el mensaje. Esto le permite, por ejemplo, enviar otro mensaje si el individuo ha abierto el mensaje anterior o ha hecho clic en él. Obtenga más información en esta [sección](reaction-events.md).

La actividad de evento **Segment qualification** permite hacer que las personas entren o avancen en un recorrido en función de las entradas y salidas de segmentos de Adobe Experience Platform. Puede hacer que todos los clientes nuevos de plata introduzcan un recorrido y envíen mensajes personalizados. Obtenga más información en esta [sección](segment-qualification-events.md).

**Organización**

En las actividades de organización, encontrará la actividad **Read segment** que le permite configurar el recorrido para que escuche un segmento de Adobe Experience Platform. [Obtenga más información sobre la actividad](read-segment.md) Leer segmento .

Las otras actividades permiten agregar condiciones al recorrido para definir varias rutas, establecer un tiempo de espera antes de ejecutar la siguiente actividad o finalizar el recorrido. Obtenga más información en esta [sección](about-journey-activities.md#orchestration-activities).

**Acciones**

Aquí encontrará la actividad **Message** que le permite incluir un mensaje diseñado en [!DNL Journey Optimizer]. [Descubra más información sobre la actividad Mensaje](journeys-message.md)

También encontrará las acciones personalizadas que ha configurado para enviar mensajes con sistemas de terceros. Obtenga más información en esta [sección](about-journey-activities.md#action-activities).

## Uso de rutas en el lienzo {#paths}

Varias actividades (**[!UICONTROL Condition]**, **[!UICONTROL Action]**) permiten definir una acción de reserva en caso de error o tiempo de espera. En el panel de configuración de actividad, marque la casilla : **[!UICONTROL Add an alternative path in case of a timeout or an error]**. Se agrega otra ruta después de la actividad . La duración del tiempo de espera se define en las propiedades del recorrido (consulte [esta página](../building-journeys/journey-gs.md#change-properties) por un usuario administrador. Por ejemplo, si un correo electrónico tarda demasiado en enviarse o por error, puede decidir enviar un SMS.

![](../assets/journey42.png)

Varias actividades (evento, acción, espera) le permiten agregar varias rutas después de ellas. Para ello, coloque el cursor en la actividad y haga clic en el símbolo &quot;+&quot;. Solo se pueden configurar actividades de evento y espera en paralelo. Si se configuran varios eventos en paralelo, la ruta elegida será la que tenga lugar el primer evento.

Al escuchar un evento, se recomienda no esperar el evento indefinidamente. No es obligatorio, solo es una práctica recomendada. Si desea escuchar uno o varios eventos solo durante un tiempo determinado, colocará uno o varios eventos y una actividad de espera en paralelo. Consulte [esta sección](../building-journeys/general-events.md#events-specific-time).

Para eliminar la ruta, coloque el cursor sobre ella y haga clic en el icono **[!UICONTROL Delete arrow]**.

![](../assets/journey42ter.png)

En el lienzo, cuando se desconectan dos actividades, se muestra una advertencia. Coloque el cursor en el icono de advertencia para mostrar el mensaje de error. Para solucionar el problema, simplemente mueva la actividad desconectada y conéctela a la actividad anterior.

![](../assets/canvas-disconnected.png)

## Copia y pegado de actividades {#copy-paste}

Puede copiar una o varias actividades de un recorrido y pegarlas en el mismo recorrido o en otro diferente. Esto le permite ahorrar tiempo si desea reutilizar numerosas actividades que ya se han configurado en un recorrido anterior.

**Notas importantes**

* Puede copiar y pegar en diferentes pestañas y navegadores. Solo puede copiar/pegar actividades dentro de la misma instancia.
* No se puede copiar/pegar un evento si el recorrido de destino tiene un evento que utiliza un área de nombres diferente.
* Las actividades pegadas pueden hacer referencia a datos que no existen en el recorrido de destino, por ejemplo, si copia o pega en entornos limitados diferentes. Compruebe siempre la existencia de errores y realice los ajustes necesarios.
* Tenga en cuenta que no puede deshacer una acción. Para eliminar las actividades pegadas, deberá seleccionarlas y eliminarlas. Por lo tanto, asegúrese de seleccionar solo las actividades que necesita antes de copiarlas.
* Puede copiar actividades de cualquier recorrido, incluso las que estén en solo lectura.
* Puede seleccionar cualquier actividad, incluso aquellas que no estén vinculadas. Las actividades vinculadas permanecerán vinculadas después de pegarlas.

Estos son los pasos para copiar/pegar actividades:

1. Abra un recorrido.
1. Para seleccionar las actividades que desea copiar, mueva el ratón mientras hace clic. También puede hacer clic en cada actividad mientras pulsa la tecla **Ctrl/Comando**. Utilice **Ctrl/Comando + A** si desea seleccionar todas las actividades.
   ![](../assets/copy-paste1.png)
1. Pulse **Ctrl/Comando + C**.
Si solo desea copiar una actividad, puede hacer clic en ella y utilizar el icono **Copiar** en la parte superior izquierda del panel de configuración de la actividad.
   ![](../assets/copy-paste2.png)
1. En cualquier recorrido, pulse **Ctrl/Comando + V** para pegar las actividades sin vincularlas a un nodo existente. Las actividades pegadas se colocan en el mismo orden. Después de pegarlas, las actividades permanecen seleccionadas para que pueda moverlas fácilmente. También puede colocar el cursor en un marcador de posición vacío y pulsar **Ctrl/Comando + V**. Las actividades pasadas se vincularán al nodo .
   ![](../assets/copy-paste3.png)
