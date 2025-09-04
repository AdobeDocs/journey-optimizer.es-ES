---
solution: Journey Optimizer
product: journey optimizer
title: Resolución de problemas de ejecución de recorrido activo
description: Obtenga información sobre cómo solucionar errores en la ejecución de recorridos en directo
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: solución de problemas, solución de problemas, recorrido, comprobación, errores
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 36%

---

# Resolución de problemas de ejecución de recorrido activo {#troubleshooting-execution}

En esta sección, aprenderá a solucionar problemas de eventos de recorrido, comprobar si los perfiles han introducido el recorrido, cómo navegan por él y si se envían mensajes.

También puede solucionar errores antes de probar o publicar un recorrido. Obtenga información sobre cómo [en esta página](troubleshooting.md).

Si usa acciones entrantes, aprenda a solucionarlas [en esta página](troubleshooting-inbound.md).

## Compruebe que los eventos se envían correctamente {#checking-that-events-are-properly-sent}

El punto de partida de un recorrido es siempre un evento. Puede hacer pruebas con herramientas como Postman.

Puede comprobar si la llamada API que envía a través de estas herramientas se envía correctamente o no. Si vuelve a recibir un error, significa que la llamada tiene un problema. Vuelva a comprobar la carga útil, el encabezado (y especialmente el ID de organización) y la dirección URL de destino. Puede preguntar a su administrador cuál es la dirección URL correcta para visitar.

Los eventos no se insertan directamente del origen a los recorridos. De hecho, los recorridos dependen de las API de ingesta de transmisión de Adobe Experience Platform. Como resultado, en caso de problemas relacionados con el evento, puede consultar [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"} para la solución de problemas de las API de ingesta de transmisión.

Si el recorrido no puede habilitar el modo de prueba con el error `ERR_MODEL_RULES_16`, asegúrese de que el evento usado incluya un [área de nombres de identidad](../audience/get-started-identity.md) al usar una acción de canal.

El área de nombres de identidad se utiliza para identificar los perfiles de prueba de forma exclusiva. Por ejemplo, si se usa el correo electrónico para identificar los perfiles de prueba, se debe seleccionar el área de nombres de identidad **Correo electrónico**. Si el identificador único es el número de teléfono, se debe seleccionar el área de nombres de identidad **Teléfono**.

## Comprobar si las personas entran en el recorrido {#checking-if-people-enter-the-journey}

El informe de recorridos mide las entradas de la gente en un recorrido en tiempo real.

Si se consigue enviar el evento pero no se ve ninguna entrada en el recorrido, hay un problema entre el envío del evento y la recepción del evento en el recorrido.

Puede comenzar la resolución de problemas con las preguntas siguientes:

* ¿Seguro que el recorrido en el que espera el evento entrante está en modo de prueba o activo?
* ¿Ha guardado el evento antes de copiar la carga útil de la previsualización de carga útil?
* ¿Su carga útil de evento contiene un ID de evento?
* ¿Ha marcado la dirección URL correcta?
* ¿Ha seguido la estructura de carga útil de las API de ingesta de flujo, utilizando la previsualización de estructura de carga útil del panel de configuración de evento? Consulte [esta página](../event/about-creating.md#preview-the-payload).
* ¿Utilizó los pares clave-valor correctos en el encabezado del evento?

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

## Comprobar cómo navegan las personas por el recorrido {#checking-how-people-navigate-through-the-journey}

La creación de informes de recorrido mide el progreso de las personas dentro de un recorrido. Es fácil identificar dónde y por qué detuvieron a una persona.

A continuación se presentan algunas cosas para comprobar:

* ¿Se debe a una condición que excluye a la persona? Por ejemplo, la condición es &quot;género = hombre&quot; y la persona es mujer. Esta comprobación puede realizarla un usuario empresarial si la condición no es demasiado compleja.
* ¿Se debe a que una llamada a una fuente de datos no responde? Cuando el recorrido está en prueba, esta información se puede ver en los registros del modo de prueba. Cuando el recorrido está activo, un administrador puede probar las llamadas directas a la fuente de datos y comprobar la respuesta recibida. Un administrador también puede realizar el duplicado del recorrido y probarlo.

## Comprobar que los mensajes se envíen correctamente {#checking-that-messages-are-sent-successfully}

Si las personas recorren el recorrido correctamente pero no reciben mensajes que deberían recibir, puede comprobar lo siguiente:

* [!DNL Journey Optimizer] ha tenido en cuenta correctamente la solicitud para enviar el mensaje. Los usuarios empresariales pueden acceder al mensaje que se supone que se debe enviar y comprobar si la hora de la última ejecución corresponde al tiempo de ejecución de su recorrido. También pueden consultar las últimas llamadas o eventos de API recibidas.
* [!DNL Journey Optimizer] ha enviado correctamente el mensaje. Compruebe los informes de recorrido para asegurarse de que no hay errores.

En el caso de un mensaje enviado mediante una acción personalizada, lo único que se puede comprobar durante la prueba de recorrido es el hecho de que la llamada del sistema de la acción personalizada produce un error o no. Si la llamada al sistema externo asociada con la acción personalizada no genera un error pero no conduce al envío de un mensaje, algunas investigaciones deben realizarse en el sistema externo.
