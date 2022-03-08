---
title: Solución de problemas del recorrido
description: Obtenga información sobre cómo solucionar errores en recorridos
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 81%

---

# Resolución de problemas del recorrido{#troubleshooting}

En esta sección, encontrará cómo solucionar problemas de recorridos antes de realizar pruebas o publicar. Todas las comprobaciones que se indican a continuación se pueden realizar cuando el recorrido está en modo de prueba o cuando el recorrido está activo. La recomendación es realizar todas las comprobaciones siguientes en el modo de prueba y luego proceder a la publicación. Consulte [esta página](../building-journeys/testing-the-journey.md).

## Comprobar errores antes de probar{#checking-for-errors-before-testing}

Antes de probar y publicar el recorrido, compruebe que todas las actividades estén correctamente configuradas. No puede realizar pruebas ni publicaciones si el sistema sigue detectando errores.

Los errores aparecen con un símbolo de advertencia en las mismas actividades del lienzo. Coloque el cursor en el signo de exclamación para mostrar el mensaje de error. Si hace clic en la actividad, debería ver la línea por error con una advertencia. Por ejemplo, si un campo obligatorio está vacío, se mostrará un error.

![](assets/journey63.png)

Por ejemplo, cuando se desconectan dos actividades, se muestra una advertencia en el lienzo.

![](assets/canvas-disconnected.png)

Al lado del botón de alternancia **[!UICONTROL Test]** y del botón **[!UICONTROL Publish]**, se puede mostrar un signo de advertencia. Este signo de advertencia muestra los errores detectados por el sistema y evita la activación del modo de prueba o la publicación del recorrido. La mayoría de las veces, los errores detectados por el sistema están vinculados a errores visibles en las actividades, pero a veces están vinculados a otros problemas. En este caso, puede mostrarlos e intentar identificar el problema mediante la descripción del error. Si no puede identificar el problema, puede copiar los detalles y enviarlos al administrador o a la asistencia técnica. Tenga en cuenta que los errores que bloquean la prueba y los errores que bloquean la publicación son similares.

El sistema detecta dos tipos de problemas: errores y advertencias. Los errores bloquean la publicación y la activación de prueba. Las advertencias indican posibles problemas que no bloquean la activación o publicación de pruebas. Verá una descripción de la publicación y un ID de registro de la publicación del tipo ERR_XXX_XXX. Esto ayudará al soporte técnico a identificar el problema.

Se pueden mostrar dos colores diferentes en el signo situado junto al botón de alternancia **[!UICONTROL Test]** y el botón **[!UICONTROL Publish]**. El signo se muestra en rojo en caso de error. Se muestra en color naranja en caso de advertencias.

![](assets/journey75.png)

Los errores y las advertencias que son globales para el recorrido aparecen primero en la lista. Los errores y las advertencias relacionados con actividades específicas se enumeran después, por orden de actividad o por su apariencia en el recorrido de izquierda a derecha. El botón **[!UICONTROL Copy details]** copia información técnica sobre el recorrido que el equipo de asistencia puede utilizar para solucionar problemas.

Cuando se produce un error en una acción o condición, se detiene el recorrido de un individuo. La única manera para continuar es marcar la casilla **[!UICONTROL Add an alternative path in case of a timeout or an error]**. Consulte [esta sección](../building-journeys/using-the-journey-designer.md#paths).

## Compruebe que los eventos se envíen correctamente{#checking-that-events-are-properly-sent}

El punto de partida de un recorrido es siempre un evento. Puede hacer pruebas con herramientas como Postman.

Puede comprobar si la llamada API que envía a través de estas herramientas se envía correctamente o no. Si vuelve a recibir un error, significa que la llamada tiene un problema. Vuelva a comprobar la carga útil, el encabezado (y especialmente el ID de organización) y la dirección URL de destino. Puede preguntar a su administrador cuál es la dirección URL correcta para visitar.

Los eventos no se insertan directamente del origen a los recorridos. De hecho, los recorridos dependen de las API de ingesta de transmisión de Adobe Experience Platform. Como resultado, en caso de problemas relacionados con eventos, puede hacer referencia a [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;} para la solución de problemas de las API de ingesta de transmisión.

## Comprobar si las personas entran en el recorrido{#checking-if-people-enter-the-journey}

Los informes de recorrido miden las entradas de la gente en un recorrido en tiempo real.

Si se consigue enviar el evento pero no se ve ninguna entrada en el recorrido, hay un problema entre el envío del evento y la recepción del evento en el recorrido.

A continuación se indican algunas cosas que el administrador debe comprobar:

* ¿Está seguro de que el recorrido en el que espera el evento entrante está en modo de prueba o activo?
* ¿Ha guardado el evento antes de copiar la carga útil de la previsualización de carga útil?
* ¿Su carga útil de evento contiene un ID de evento?
* ¿Ha marcado la dirección URL correcta?
* ¿Ha seguido la estructura de carga útil de las API de inserción de flujo, utilizando la previsualización de estructura de carga útil del panel de configuración de evento? Consulte [esta página](../event/about-creating.md#preview-the-payload).
* ¿Utilizó los pares clave-valor correctos en el encabezado del evento?

   ```
   X-gw-ims-org-id - your ORGID
   Content-type - application/json
   ```

## Comprobar cómo navegan las personas a través del recorrido{#checking-how-people-navigate-through-the-journey}

Los informes de recorrido miden el progreso de las personas dentro de un recorrido. Es fácil identificar dónde y por qué detuvieron a una persona.

A continuación se presentan algunas cosas para comprobar:

* ¿Se debe a una condición que excluye a la persona? Por ejemplo, la condición es &quot;género = hombre&quot; y la persona es mujer. Esta comprobación puede realizarla un usuario empresarial si la condición no es demasiado compleja.
* ¿Se debe a que una llamada a una fuente de datos no responde? Cuando el recorrido está en prueba, esta información se puede ver en los registros del modo de prueba. Cuando el recorrido está activo, un administrador puede probar las llamadas directas a la fuente de datos y comprobar la respuesta recibida. Un administrador también puede realizar el duplicado del recorrido y probarlo.

## Comprobar que los mensajes se envíen correctamente{#checking-that-messages-are-sent-successfully}

Si los individuos recorren el recorrido correcto, pero no reciben mensajes que deberían recibir, puede comprobar lo siguiente:

* [!DNL Journey Optimizer] ha tenido en cuenta correctamente la solicitud para enviar el mensaje. Los usuarios empresariales pueden acceder al mensaje que se supone que se debe enviar y comprobar si la hora de la última ejecución corresponde al tiempo de ejecución del recorrido. También pueden comprobar las últimas llamadas o eventos de API recibidas.
* [!DNL Journey Optimizer] ha enviado correctamente el mensaje. En los registros de envío del mensaje, puede ver el estado de cada ejecución. Pueden ver si es verde o rojo, y cuál fue el problema. Un usuario empresarial puede acceder a esta pantalla y enviar los registros a un administrador para realizar más investigaciones.

En el caso de un mensaje enviado mediante una acción personalizada, lo único que se puede comprobar durante la prueba de recorrido es el hecho de que la llamada del sistema de la acción personalizada produce un error o no. Si la llamada al sistema externo asociada con la acción personalizada no genera un error pero no conduce al envío de un mensaje, algunas investigaciones deben realizarse en el sistema externo.
