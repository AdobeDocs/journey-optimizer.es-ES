---
solution: Journey Optimizer
product: journey optimizer
title: Resolución de problemas de ejecución de recorrido activo
description: Obtenga información sobre cómo solucionar errores en la ejecución de recorridos en directo
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: solución de problemas, solución de problemas, recorrido, comprobación, errores
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
source-git-commit: dd8fd1099344257a72e9f7f18ef433d35def6689
workflow-type: tm+mt
source-wordcount: '1754'
ht-degree: 14%

---

# Resolución de problemas de ejecución de recorrido activo {#troubleshooting-execution}

En esta sección, aprenderá a solucionar problemas de eventos de recorrido, comprobar si los perfiles han introducido el recorrido, cómo navegan por él y si se envían mensajes.

También puede solucionar errores antes de probar o publicar un recorrido. Obtenga información sobre cómo [en esta página](troubleshooting.md).

Si usa acciones entrantes, aprenda a solucionarlas [en esta página](troubleshooting-inbound.md).

## Compruebe que los eventos se envían correctamente {#checking-that-events-are-properly-sent}

El punto de partida de un recorrido es siempre un evento. Puede hacer pruebas con herramientas como Postman.

Puede comprobar si la llamada API que envía a través de estas herramientas se envía correctamente o no. Si vuelve a recibir un error, significa que la llamada tiene un problema. Vuelva a comprobar la carga útil, el encabezado (y especialmente el ID de organización) y la dirección URL de destino. Puede preguntar a su administrador cuál es la dirección URL correcta para visitar.

Los eventos no se insertan directamente del origen a los recorridos. De hecho, los recorridos dependen de las API de ingesta de transmisión de [!DNL Adobe Experience Platform]. Como resultado, en caso de problemas relacionados con el evento, puede consultar [[!DNL Adobe Experience Platform] documentación](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"} para la solución de problemas de las API de ingesta de transmisión.

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
* ¿Ha seguido la estructura de carga útil de las API de ingesta de streaming, utilizando la previsualización de estructura de carga útil del panel de configuración de evento? Consulte [esta página](../event/about-creating.md#preview-the-payload).
* ¿Utilizó los pares clave-valor correctos en el encabezado del evento?

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

* **Tipos de datos de esquema y condición de evento**: asegúrese de que los tipos de datos utilizados en su condición de evento (regla) coincidan con el esquema de evento. Los tipos no coincidentes (por ejemplo, cadena frente a entero) hacen que la evaluación de reglas falle y que se pierdan eventos. Ver [Verificar identidad del evento](#verify-event-identity-and-rule-data-types).

&#x200B;>>
**Para recorridos de calificación de audiencia con audiencias de streaming**: Si usa una actividad de calificación de audiencia como punto de entrada de recorrido, tenga en cuenta que no todos los perfiles aptos para la audiencia entrarán necesariamente en la recorrido debido a factores de tiempo, salidas rápidas de la audiencia o si los perfiles ya estaban en la audiencia antes de la publicación. Más información sobre [consideraciones de tiempo para la calificación de audiencias de streaming](audience-qualification-events.md#streaming-entry-caveats).

### Verificar identidad del evento {#verify-event-identity-and-rule-data-types}

Al configurar un recorrido basado en eventos, confirme que el campo de identidad de la carga útil coincide con el área de nombres [seleccionado en el evento](../event/about-creating.md#select-the-namespace). Si el evento incluye campos para la coincidencia de perfiles, compruebe que **mayúsculas y minúsculas** y **tipo de datos** en la condición de evento coincidan exactamente con los datos de entrada. Por ejemplo, si el esquema de eventos define `roStatus` como una cadena, la regla de recorrido también debe evaluarla como una cadena. Los tipos de datos no coincidentes (por ejemplo, cadena frente a entero) hacen que la evaluación de reglas falle y que se eliminen eventos válidos.

Para validar la condición de evento en [!DNL Journey Optimizer], utilice la vista previa de carga útil en la configuración de evento y asegúrese de que los tipos y valores de la regla coinciden con la estructura de carga útil. Obtenga información sobre cómo [previsualizar la carga útil](../event/about-creating.md#preview-the-payload) y [configurar eventos basados en reglas](../event/about-creating.md).

## Solución de problemas de transiciones del modo de prueba {#troubleshooting-test-transitions}

Si los perfiles de prueba no progresan a través del recorrido en el modo de prueba o el flujo visual no muestra flechas verdes que indiquen la progresión del paso, el problema puede estar relacionado con la validación de la transición. En esta sección se explica cómo diagnosticar y resolver problemas comunes del modo de prueba.

### Los perfiles de prueba no progresan

Si los perfiles de prueba entran en el recorrido pero no avanzan más allá del paso inicial, compruebe lo siguiente:

* **fecha de inicio del Recorrido** - La causa más común es cuando la fecha de inicio del recorrido se establece en el futuro. Los perfiles de prueba se descartan inmediatamente si la hora actual no coincide con la ventana [fechas/hora de inicio y finalización](journey-properties.md#dates) configurada en el recorrido. Para resolver:
   * Compruebe que la fecha de inicio del recorrido no esté establecida en el futuro
   * Asegúrese de que la hora actual se encuentre dentro de la ventana de fecha activa del recorrido
   * Si es necesario, actualice las propiedades del recorrido para ajustar la fecha de inicio

* **Configuración del perfil de prueba** - Confirme que el perfil está marcado correctamente como perfil de prueba en [!DNL Adobe Experience Platform]. Consulte [cómo crear perfiles de prueba](../audience/creating-test-profiles.md) para obtener más información.

* **Área de nombres de identidad** - Asegúrese de que el área de nombres de identidad utilizada en la configuración del evento coincida con el área de nombres del perfil de prueba.

### Indicadores de transición nulos

Durante la solución de problemas técnicos, puede encontrar una propiedad `isValidTransition` establecida en null en los detalles técnicos del recorrido. Esta propiedad solo de interfaz de usuario no afecta al procesamiento back-end ni al rendimiento del recorrido. Sin embargo, un valor nulo puede indicar:

* **Configuración incorrecta del Recorrido**: la fecha de inicio del recorrido se establece en el futuro, lo que provoca que los eventos de prueba se descarten sin aviso
* **Transición dañada**: en casos excepcionales, es posible que sea necesario volver a conectar los nodos de recorrido

Si encuentra problemas de transición persistentes:

1. Compruebe que la fecha de inicio del recorrido es la actual
1. Desactivar y reactivar el modo de prueba
1. Si el problema persiste, considere la posibilidad de duplicar los nodos de recorrido afectados y reconectarlos
1. Para casos sin resolver, póngase en contacto con el servicio de asistencia técnica con registros de recorrido, los ID de perfil afectados y detalles sobre la transición nula

>[!NOTE]
>
>Recuerde que los eventos enviados fuera de la ventana de fecha activa del recorrido se descartan silenciosamente sin ningún mensaje de error. Compruebe siempre primero la configuración del tiempo de recorrido al solucionar problemas de progresión de perfiles de prueba.

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

## Explicación de las entradas duplicadas en eventos de paso de Recorrido {#duplicate-step-events}

Utilice esta sección para comprender por qué pueden aparecer filas duplicadas en los eventos de paso de Recorrido.

### ¿Por qué veo varias entradas con la misma instancia de recorrido, perfil, nodo e ID de solicitud?

Al consultar los datos de Eventos de paso de Recorrido, puede observar ocasionalmente lo que parecen ser entradas de registro duplicadas para la misma ejecución de recorrido. Estas entradas comparten valores idénticos para:

* `profileID` - La identidad del perfil
* `instanceID`: el identificador de instancia de recorrido
* `nodeID`: el nodo de recorrido específico
* `requestID` - El identificador de la solicitud

Sin embargo, estas entradas tienen **diferentes valores de `_id`**, que es el indicador clave que distingue este escenario de la duplicación de datos real.

### ¿Qué causa este comportamiento?

Esto ocurre debido a las operaciones de escalado automático del servidor (también llamadas &quot;reequilibrio&quot;) en la arquitectura de microservicios de [!DNL Adobe Journey Optimizer]. Durante períodos de alta carga u optimización del sistema:

1. Un evento de paso de recorrido comienza a procesarse y se registra en el conjunto de datos de eventos de paso de Recorrido
2. Una operación de escalado automático redistribuye la carga de trabajo entre instancias de servicio
3. Otra instancia de servicio puede volver a procesar el mismo evento y crear una segunda entrada de registro con un `_id` diferente

Se trata de un comportamiento esperado del sistema y **funciona según lo diseñado**.

### ¿Afecta a la ejecución del recorrido o a la entrega de mensajes?

**No.**: el impacto se limita solamente al registro. [!DNL Adobe Journey Optimizer] tiene mecanismos de deduplicación integrados en la capa de ejecución de mensajes que garantizan:

* Solo se envía un mensaje (correo electrónico, SMS, notificación push, etc.) a cada perfil
* Las acciones se ejecutan solo una vez
* La ejecución del recorrido se realiza correctamente

Puede comprobarlo consultando los `ajo_message_feedback_event_dataset` o comprobando los registros de ejecución de acciones. Verá que solo se envió un mensaje, a pesar de las entradas de evento de paso de recorrido duplicadas.

### ¿Cómo puedo identificar estos casos en mis consultas?

Al analizar los datos de Eventos de paso de Recorrido:

1. **Compruebe el campo `_id`**: Los duplicados verdaderos en el nivel de sistema tendrían el mismo `_id`. Valores diferentes de `_id` indican entradas de registro independientes del escenario de reequilibrio descrito anteriormente.

2. **Verificar entrega de mensajes**: haga referencia cruzada con datos de comentarios de mensajes para confirmar que solo se envió un mensaje:

   ```sql
   SELECT
     timestamp,
     _experience.customerJourneyManagement.messageExecution.messageExecutionID,
     _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
   FROM ajo_message_feedback_event_dataset
   WHERE
     _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journeyVersionID>'
     AND TO_JSON(identityMap) like '%<profileID>%'
   ORDER BY timestamp DESC;
   ```

3. **Agrupar por identificadores únicos**: Al contar las ejecuciones, use `_id` para obtener recuentos precisos:

   ```sql
   SELECT
     COUNT(DISTINCT _id) as unique_executions
   FROM journey_step_events
   WHERE
     _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
     AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID>'
   ```

### ¿Qué debo hacer si observo esto?

Este es un comportamiento normal del sistema y **no se requiere ninguna acción**. El registro duplicado no indica un problema con la configuración del recorrido o la entrega de mensajes.

Si está creando informes o análisis basados en Eventos de pasos de Recorrido:

* Usar `_id` como clave principal para contar eventos únicos
* Referencia cruzada con conjuntos de datos de comentarios de mensajes al analizar el envío de mensajes
* Tenga en cuenta que el análisis de tiempo puede mostrar entradas agrupadas con unos segundos de diferencia

Para obtener más información sobre la consulta de eventos de paso de Recorrido, vea [Ejemplos de consultas](../reports/query-examples.md).

## Solucionar discrepancias de métricas del panel {#dashboard-metrics}

Si las métricas mostradas en el panel **Información general** no coinciden con el número real de recorridos en la pestaña **Examinar**, compruebe lo siguiente:

* Asegúrese de que los recorridos en cuestión hayan tenido tráfico en las últimas 24 horas, ya que los recorridos sin actividad reciente se excluyen del panel.
* Compruebe que dispone de los permisos de acceso adecuados para ver todos los recorridos de su organización.
* Conceda un máximo de 30 minutos para que las métricas se actualicen después de realizar cambios en los recorridos.

Si persisten las discrepancias, póngase en contacto con el Soporte técnico de Adobe con capturas de pantalla de las pestañas Información general y Examinar para investigar.
