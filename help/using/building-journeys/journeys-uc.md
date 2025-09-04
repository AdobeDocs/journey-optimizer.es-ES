---
solution: Journey Optimizer
product: journey optimizer
title: Casos de uso de recorridos
description: Casos de uso de recorridos
feature: Journeys, Use Cases, Email, Push
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: caso de uso, multicanal, mensajes, recorrido, canal, eventos, push
exl-id: a1bbfcee-2235-4820-a391-d5d35f499cb0
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 1%

---

# Envío de mensajes multicanal {#send-multi-channel-messages}

Esta sección presenta un caso de uso que combina una audiencia de lectura, un evento, eventos de reacción y mensajes de correo electrónico/push.

![](assets/jo-uc1.png)

## Descripción del caso de uso

En este caso de uso, el objetivo es enviar un primer mensaje de correo electrónico a todos los clientes que pertenecen a una audiencia específica.

En función de su reacción al primer mensaje, se envían mensajes de seguimiento específicos.

Si el cliente abre el correo electrónico, el sistema espera una compra y envía un mensaje push para darle las gracias al cliente.

Si no hay reacción, se envía un correo electrónico de seguimiento.

## Requisitos previos

Para que este caso de uso funcione, configure lo siguiente:

* Una audiencia para todos los clientes que viven en Atlanta, San Francisco o Seattle y que nacieron después de 1980
* Un evento de compra

### Creación de la audiencia

En este recorrido, se aprovecha una audiencia específica de clientes. Todos los individuos que pertenecen a la audiencia entran en el recorrido y siguen los diferentes pasos. En este ejemplo, la audiencia se dirige a todos los clientes que viven en Atlanta, San Francisco o Seattle y que nacieron después de 1980.

Para obtener más información sobre las audiencias, [consulte esta página](../audience/about-audiences.md).

1. En la sección de menú CLIENTE, seleccione **[!UICONTROL Audiencias]**.
1. Haga clic en el botón **[!UICONTROL Crear audiencia]** ubicado en la parte superior derecha de la lista de audiencias.
1. En el panel **[!UICONTROL Propiedades de audiencia]**, escriba un nombre para la audiencia.
1. Arrastre y suelte los campos deseados del panel izquierdo al espacio de trabajo central y configúrelos según sus necesidades. En este ejemplo, utilice los campos de atributo **City** y **Birth year**.
1. Haga clic en **[!UICONTROL Guardar]**.

   ![](assets/add-attributes.png)

La audiencia se crea y está lista para utilizarse en el recorrido. Con una actividad **Leer audiencia**, todas las personas que pertenezcan a la audiencia podrán entrar al recorrido.

### Configuración del evento

Configure un evento que se envíe al recorrido cuando un cliente realice una compra. Cuando el recorrido recibe el evento, envía en déclencheur el mensaje de &quot;gracias&quot;.

Para ello, usa un [evento basado en reglas](../event/about-events.md).

1. En la sección del menú ADMINISTRACIÓN, seleccione **[!UICONTROL Configuraciones]** y, a continuación, haga clic en **[!UICONTROL Eventos]**. Haga clic en **[!UICONTROL Crear evento]** para crear un nuevo evento.

1. Introduzca el nombre del evento.

1. En el campo **[!UICONTROL Tipo de ID de evento]**, seleccione **[!UICONTROL Basado en reglas]**.

1. Defina el **[!UICONTROL Esquema]** y la carga **[!UICONTROL Campos]**. Utilice varios campos, por ejemplo, el producto comprado, la fecha de compra y el ID de compra.

1. En el campo **[!UICONTROL Condición de ID de evento]**, defina la condición utilizada por el sistema para identificar los eventos que almacenan en déclencheur el recorrido. Por ejemplo, agregue un campo `purchaseMessage` y defina la siguiente regla: `purchaseMessage="thank you"`

1. Defina el **[!UICONTROL espacio de nombres]** y el **[!UICONTROL identificador de perfil]**.

1. Haga clic en **[!UICONTROL Guardar]**.

   ![](assets/jo-uc2.png)

El evento está ahora configurado y listo para utilizarse en el recorrido. Con la actividad de evento correspondiente, se puede activar una acción cada vez que un cliente realiza una compra.

## Diseño del recorrido

1. Inicie el recorrido con una actividad **Leer audiencia**. Seleccione la audiencia creada anteriormente. Todas las personas que pertenecen a la audiencia entran en el recorrido.

   ![](assets/jo-uc4.png)

1. Suelte una actividad de acción **Email** y defina el contenido del &quot;primer mensaje&quot;. Este mensaje se envía a todas las personas del recorrido. Consulte esta [sección](../email/create-email.md) para obtener información sobre cómo configurar y diseñar un mensaje de correo electrónico.

   ![](assets/jo-uc5.png)

1. Agregue un evento **Reaction** y seleccione **Email opened**. El evento se activa cuando un individuo que pertenece a la audiencia abre el correo electrónico.

1. Marque la casilla **Definir el tiempo de espera del evento**, defina una duración (1 día en este ejemplo) y marque **Establecer una ruta de espera**. Esto crea otra ruta para las personas que no abren el primer mensaje push o de correo electrónico.

1. En la ruta de tiempo de espera, suelte una actividad de acción **Correo electrónico** y defina el contenido del mensaje de &quot;seguimiento&quot;. Este mensaje se envía a las personas que no abren el correo electrónico ni insertan el primer mensaje en el día siguiente. [Aprenda a configurar y diseñar un correo electrónico](../email/create-email.md).

1. En la primera ruta, añada el evento de compra creado anteriormente. El evento se activa cuando un individuo realiza una compra.

1. Después del evento, suelta una actividad de acción **Push** y define el contenido del mensaje &quot;gracias&quot;. Consulte esta [sección](../push/create-push.md) para obtener información sobre cómo configurar y diseñar una notificación push.

## Prueba y publicación del recorrido

1. Antes de probar el recorrido, compruebe que es válido y que no hay error.

1. Utilice la opción **Test**, que se encuentra en la esquina superior derecha, para activar el modo de prueba. Consulte esta [sección](testing-the-journey.md) para aprender a utilizar el modo de prueba.

1. Cuando el recorrido esté listo, publíquelo con el botón **Publicar**, ubicado en la esquina superior derecha.
