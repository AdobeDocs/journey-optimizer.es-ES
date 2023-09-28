---
solution: Journey Optimizer
product: journey optimizer
title: Casos de uso de recorridos
description: Casos de uso de recorridos
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: caso de uso, multicanal, mensajes, recorrido, canal, eventos, push
exl-id: a1bbfcee-2235-4820-a391-d5d35f499cb0
source-git-commit: 2e06ca80a74c6f8a16ff379ee554d57a69ceeffd
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 1%

---

# Caso de uso: Envío de mensajes multicanal{#send-multi-channel-messages}

Esta sección presenta un caso de uso que combina una audiencia de lectura, un evento, eventos de reacción y mensajes de correo electrónico/push.

![](assets/jo-uc1.png)

## Descripción del caso de uso

En este caso de uso, queremos enviar un primer mensaje (correo electrónico y push) a todos los clientes que pertenecen a una audiencia específica.

En función de su reacción al primer mensaje, queremos enviar mensajes específicos.

Después del primer mensaje, esperamos un día a que los clientes abran el mensaje push o de correo electrónico. Si no hay reacción, les enviamos un correo electrónico de seguimiento.

Después, esperamos una compra y enviamos un mensaje push para dar las gracias al cliente.

## Requisitos previos

Para que este caso de uso funcione, debe configurar lo siguiente:

* una audiencia para todos los clientes que viven en Atlanta, San Francisco o Seattle y que nacieron después de 1980.
* un evento de compra

### Creación de la audiencia

En nuestro recorrido, queremos aprovechar una audiencia específica de clientes. Todos los individuos que pertenecen a la audiencia entran en el recorrido y siguen los diferentes pasos. En nuestro ejemplo, necesitamos una audiencia que se dirija a todos los clientes que viven en Atlanta, San Francisco o Seattle y que nacieron después de 1980.

Para obtener más información sobre las audiencias, consulte [página](../audience/about-audiences.md).

1. En la sección del menú CUSTOMER, seleccione **[!UICONTROL Audiencias]**.

1. Haga clic en **[!UICONTROL Crear audiencia]** situado en la parte superior derecha de la lista de audiencias.

1. En el **[!UICONTROL Propiedades de audiencia]** , introduzca un nombre para la audiencia.

1. Arrastre y suelte los campos deseados del panel izquierdo al área de trabajo central y, a continuación, configúrelos según sus necesidades. En este ejemplo, utilizamos la variable **Ciudad** y **Año de nacimiento** campos de atributos.

1. Haga clic en **[!UICONTROL Guardar]**.

   ![](assets/add-attributes.png)

La audiencia se crea y está lista para utilizarse en el recorrido. Uso de un **Leer audiencia** actividad, puede hacer que todas las personas que pertenecen a la audiencia participen en el recorrido.

### Configuración del evento

Debe configurar un evento que se envíe a su recorrido cuando un cliente realice una compra. Cuando el recorrido recibe el evento, envía en déclencheur el mensaje de &quot;gracias&quot;.

Para esto, utilizamos un evento basado en reglas. Para obtener más información, consulte [página](../event/about-events.md).

1. En la sección del menú ADMINISTRACIÓN, seleccione **[!UICONTROL Configuraciones]**, luego haga clic en **[!UICONTROL Eventos]**. Clic **[!UICONTROL Crear evento]** para crear un nuevo evento.

1. Introduzca el nombre del evento.

1. En el **[!UICONTROL Tipo de ID de evento]** , seleccione **[!UICONTROL Basado en reglas]**.

1. Defina el **[!UICONTROL Esquema]** y carga útil **[!UICONTROL Campos]**. Puede utilizar varios campos, por ejemplo, el producto comprado, la fecha de compra y el ID de compra.

1. En el **[!UICONTROL Condición de ID de evento]** , defina la condición utilizada por el sistema para identificar los eventos que almacenan en déclencheur el recorrido. Por ejemplo, puede agregar un `purchaseMessage` y defina la siguiente regla: `purchaseMessage="thank you"`

1. Defina el **[!UICONTROL Área de nombres]** y **[!UICONTROL Identificador de perfil]**.

1. Haga clic en **[!UICONTROL Guardar]**.

   ![](assets/jo-uc2.png)

El evento está ahora configurado y listo para utilizarse en el recorrido. Con la actividad de evento correspondiente, puede almacenar en déclencheur una acción cada vez que un cliente realice una compra.

## Diseño del recorrido

1. Inicie el recorrido con una **Leer audiencia** actividad. Seleccione la audiencia creada anteriormente. Todas las personas que pertenecen a la audiencia entran en el recorrido.

   ![](assets/jo-uc4.png)

1. Suelte un **Correo electrónico** actividad de acción y definir el contenido del &quot;primer mensaje&quot;. Este mensaje se envía a todas las personas del recorrido. Consulte esta sección [sección](../email/create-email.md) para aprender a configurar y diseñar un correo electrónico.

   ![](assets/jo-uc5.png)

1. Coloque el cursor en la actividad de correo electrónico y haga clic en el símbolo &quot;+&quot; para crear una nueva ruta.

1. En la primera ruta, añada un **Reacción** evento y seleccione **Push abierta**. El evento se activa cuando un individuo que pertenece a la audiencia abre la versión push del primer mensaje.

1. En la segunda ruta, añada un **Reacción** evento y seleccione **Correo electrónico abierto**. El evento se activa cuando el usuario abre el correo electrónico.

1. En una de las actividades de reacción, compruebe el **Definir el tiempo de espera del evento** , defina una duración (1 día en nuestro ejemplo) y marque **Establecer una ruta de tiempo de espera**. Esto crea otra ruta para las personas que no abren el primer mensaje push o de correo electrónico.

   >[!NOTE]
   >
   >Al configurar un tiempo de espera en varios eventos (las dos reacciones en este caso), solo es necesario configurar el tiempo de espera en uno de estos eventos.

1. En la ruta de tiempo de espera, suelte un **Correo electrónico** actividad de acción y definir el contenido del mensaje de &quot;seguimiento&quot;. Este mensaje se envía a las personas que no abren el correo electrónico ni insertan el primer mensaje al día siguiente. Consulte esta sección [sección](../email/create-email.md) para aprender a configurar y diseñar un correo electrónico.

1. Conecte las tres rutas al evento de compra creado anteriormente. El evento se activa cuando un individuo realiza una compra.

1. Después del evento, suelte un **Push** actividad de acción y defina el contenido del mensaje &quot;gracias&quot;. Consulte esta sección [sección](../push/create-push.md) para aprender a configurar y diseñar una notificación push.

## Prueba y publicación del recorrido

1. Antes de probar el recorrido, compruebe que es válido y que no hay error.

1. Haga clic en **Prueba** active el modo de prueba en la esquina superior derecha. Consulte esta sección [sección](testing-the-journey.md) para aprender a utilizar el modo de prueba.

1. Cuando el recorrido esté listo, publíquelo con el **Publish** botón, situado en la esquina superior derecha.
