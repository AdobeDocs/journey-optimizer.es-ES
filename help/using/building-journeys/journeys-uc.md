---
title: Casos de uso de recorridos
description: Casos de uso de recorridos
feature: Recorridos
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 2%

---

# Caso de uso de recorrido

![](../assets/do-not-localize/badge.png)

Esta sección presenta un caso de uso que combina un segmento de lectura, un evento, eventos de reacción y mensajes push/de correo electrónico.

![](../assets/jo-uc1.png)

## Descripción del caso de uso

En este caso de uso, queremos enviar un primer mensaje (correo electrónico y push) a todos los clientes que pertenecen a un segmento específico.

En función de su reacción al primer mensaje, queremos enviar mensajes específicos.

Después del primer mensaje, esperamos un día para que los clientes abran el mensaje push o el correo electrónico. Si no hay reacción, les enviamos un correo electrónico de seguimiento.

A continuación, esperamos una compra y enviamos un mensaje push para agradecer al cliente.

## Requisitos previos

Para que este caso de uso funcione, debe configurar lo siguiente:

* un segmento para todos los clientes que viven en Atlanta, San Francisco o Seattle y que nacieron después de 1980.
* un evento purchase
* tres mensajes

### Creación del segmento

En nuestro recorrido, queremos aprovechar un segmento específico de clientes. Todas las personas que pertenecen al segmento entran en el recorrido y siguen los diferentes pasos. En nuestro ejemplo, necesitamos un segmento dirigido a todos los clientes que viven en Atlanta, San Francisco o Seattle y que nacieron después de 1980.

Para obtener más información sobre los segmentos, consulte esta [página](../segment/about-segments.md).

1. En el menú **[!UICONTROL Segments]**, haga clic en **[!UICONTROL Create segment]**.

1. En el panel **[!UICONTROL Segment properties]**, introduzca un nombre para el segmento.

1. Arrastre y suelte los campos deseados del panel izquierdo al espacio de trabajo central y, a continuación, configúrelos según sus necesidades. En este ejemplo, se utilizan los campos de atributos **City** y **Birth year**.

1. Haga clic en **[!UICONTROL Save]**.

   ![](../assets/add-attributes.png)

El segmento se ha creado y está listo para utilizarse en el recorrido. Con una actividad **Read segment** , puede hacer que todas las personas que pertenecen al segmento ingresen al recorrido.

### Configuración del evento

Debe configurar un evento que se envíe a su recorrido cuando un cliente realice una compra. Cuando el recorrido recibe el evento, déclencheur el mensaje de agradecimiento.

Para ello, se utiliza un evento basado en reglas. Para obtener más información sobre los eventos, consulte esta [página](../event/about-events.md).

1. En la sección ADMINISTRACIÓN, vaya a **[!UICONTROL Configurations]** y haga clic en **[!UICONTROL Events]**. Haga clic en **[!UICONTROL Add]** para crear un nuevo evento.

1. Introduzca el nombre del evento.

1. En el campo **[!UICONTROL Event ID type]**, seleccione **[!UICONTROL Rule Based]**.

1. Defina el **[!UICONTROL Schema]** y la carga útil **[!UICONTROL Fields]**. Puede utilizar varios campos, por ejemplo, el producto comprado, la fecha de compra y el ID de compra.

1. En el campo **[!UICONTROL Event ID condition]**, defina la condición utilizada por el sistema para identificar los eventos que producen el déclencheur del recorrido. Por ejemplo, puede agregar un campo `purchaseMessage` y definir la siguiente regla: `purchaseMessage="thank you"`

1. Defina los **[!UICONTROL Namespace]** y **[!UICONTROL Key]**.

1. Haga clic en **[!UICONTROL Save]**.

   ![](../assets/jo-uc2.png)

El evento está configurado y listo para utilizarse en el recorrido. Con la actividad de evento correspondiente, puede almacenar en déclencheur una acción cada vez que un cliente realiza una compra.

### Creación de los mensajes

Para este caso de uso, se deben crear tres mensajes:

* un mensaje push y de correo electrónico de primer mensaje
* un mensaje push de agradecimiento
* un mensaje de seguimiento por correo electrónico

![](../assets/jo-uc3.png)

Consulte esta [sección](../segment/about-segments.md) para aprender a diseñar y publicar estos mensajes.

## Diseño del recorrido

1. Inicie el recorrido con una actividad **Read segment**. Seleccione el segmento creado anteriormente. Todas las personas que pertenecen al segmento entran en el recorrido.

   ![](../assets/jo-uc4.png)

1. Suelte una actividad **Message** y seleccione el mensaje push y el mensaje inicial de correo electrónico. Este mensaje se envía a todas las personas del recorrido.

   ![](../assets/jo-uc5.png)

1. Coloque el cursor en la actividad del mensaje y haga clic en el símbolo &quot;+&quot; para crear una nueva ruta.

1. En la primera ruta, añada un evento **Reaction** y seleccione **Push opened**. El evento se activa cuando una persona que pertenece al segmento abre la versión push del primer mensaje.

1. En la segunda ruta, añada un evento **Reaction** y seleccione **Email opened**. El evento se activa cuando el individuo abre el correo electrónico.

1. En una de las actividades de reacción, marque la casilla **Define the event timeout**, defina una duración (1 día en nuestro ejemplo) y marque **Set a timeout path**. Esto crea otra ruta para las personas que no abren el mensaje push o de correo electrónico primero.

   >[!NOTE]
   >
   >Al configurar un tiempo de espera en varios eventos (las dos reacciones en este caso), solo es necesario configurar el tiempo de espera en uno de estos eventos.

1. En la ruta de tiempo de espera, suelte una actividad **Message** y seleccione el mensaje de seguimiento del correo electrónico. Este mensaje se envía a las personas que no abren el correo electrónico ni insertan el primer mensaje al día siguiente.

1. Conecte las tres rutas al evento purchase creado anteriormente. El evento se activa cuando un individuo realiza una compra.

1. Después del evento, suelte una actividad **Message** y seleccione el mensaje de correo electrónico &quot;thank you&quot;.

1. Agregue una actividad **End**.

## Prueba y publicación del recorrido

1. Antes de probar el recorrido, compruebe que sea válido y que no haya ningún error.

1. Haga clic en el botón **Test**, situado en la esquina superior derecha, para activar el modo de prueba. Defina cómo desea que los perfiles de prueba entren en la prueba: un perfil único o hasta 100 a la vez. Consulte esta [sección](testing-the-journey.md) para aprender a utilizar el modo de prueba.

1. Cuando el recorrido esté listo, publíquelo utilizando el botón **Publish**, situado en la esquina superior derecha.
