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
TQID: https://experienceleague.adobe.com/2YZ6Cjph9Le-HtwKdz4GBgEdhwIMPpVtj9yWKlV3hQ4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: d08afb72-92f6-4856-88e3-11ec34313c2fid: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 2993
ht-degree: 8%

---

# Resolución de problemas de ejecución de recorrido activo {#troubleshooting-execution}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a solucionar problemas de ejecución de un recorrido activo, incluida la comprobación de que se envían eventos, la confirmación de la entrada de perfiles y el progreso en el recorrido, y la comprobación de que se envían mensajes.

>[!ENDSHADEBOX]

En esta sección, aprenderá a solucionar problemas de eventos de recorrido, comprobar si los perfiles han introducido el recorrido, cómo navegan por él y si se envían mensajes.

También puede solucionar errores antes de probar o publicar un recorrido. Obtenga información sobre cómo [en esta página](troubleshooting.md).

Si usa acciones entrantes, aprenda a solucionarlas [en esta página](troubleshooting-inbound.md).

## Compruebe que los eventos se envían correctamente {#checking-that-events-are-properly-sent}

El punto de partida de un recorrido es siempre un evento. Puede hacer pruebas con herramientas como Postman.

Puede comprobar si la llamada API que envía a través de estas herramientas se envía correctamente o no. Si vuelve a recibir un error, significa que la llamada tiene un problema. Vuelva a comprobar la carga útil, el encabezado (y especialmente el ID de organización) y la dirección URL de destino. Puede preguntar a su administrador cuál es la dirección URL correcta para visitar.

Los eventos no se insertan directamente del origen a los recorridos. De hecho, los recorridos dependen de las API de ingesta de transmisión de [!DNL Adobe Experience Platform]. Como resultado, en caso de problemas relacionados con el evento, puede consultar [[!DNL Adobe Experience Platform] documentación](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=es){target="_blank"} para la solución de problemas de las API de ingesta de transmisión.

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

* **Evento descartado - no se cumple la condición de calificación** - Para los eventos basados en reglas, si la **condición de calificación** no se cumple con la carga útil del evento (por ejemplo, falta un campo obligatorio o está vacío, o falla una condición como `isNotEmpty` en un campo), el evento se **recibe pero se descarta** y el recorrido no se activa. Los registros y los seguimientos de Splunk pueden mostrar que el evento se recibió pero se descartó porque no cumplía la condición de calificación, con códigos de descarte como `notSuitableInitialEvent`. Este es el comportamiento esperado: si no se cumple la condición de calificación, el evento se descarta y el recorrido no se activa para ese perfil. Compruebe que la carga útil de evento contiene los campos y valores esperados y que la regla de la configuración de evento coincide con los datos que envía. Si el evento se activa mediante una **acción personalizada** desde otro recorrido, consulte [Gestión de eventos de descarte y tiempos de espera inactivos](../action/troubleshoot-custom-action.md#handling-discard-events-and-idle-timeouts) en la solución de problemas de acciones personalizadas.

>>
**Para recorridos de calificación de audiencia con audiencias de streaming**: Si usa una actividad de calificación de audiencia como punto de entrada de recorrido, tenga en cuenta que no todos los perfiles aptos para la audiencia entrarán necesariamente en la recorrido debido a factores de tiempo, salidas rápidas de la audiencia o si los perfiles ya estaban en la audiencia antes de la publicación. Más información sobre [consideraciones de tiempo para la calificación de audiencias de streaming](audience-qualification-events.md#streaming-entry-caveats).

### Verificar identidad del evento {#verify-event-identity-and-rule-data-types}

Al configurar un recorrido basado en eventos, confirme que el campo de identidad de la carga útil coincide con el área de nombres [seleccionado en el evento](../event/about-creating.md#select-the-namespace). Si el evento incluye campos para la coincidencia de perfiles, compruebe que **mayúsculas y minúsculas** y **tipo de datos** en la condición de evento coincidan exactamente con los datos de entrada. Por ejemplo, si el esquema de eventos define `roStatus` como una cadena, la regla de recorrido también debe evaluarla como una cadena. Los tipos de datos no coincidentes (por ejemplo, cadena frente a entero) hacen que la evaluación de reglas falle y que se eliminen eventos válidos. Del mismo modo, si el evento tiene una **condición de calificación** (por ejemplo, un campo no debe estar vacío), los eventos que no cumplan esa condición se **descartarán** y no almacenarán en déclencheur el recorrido; los registros pueden mostrar códigos de descarte como `notSuitableInitialEvent`.

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
1. Para casos sin resolver, [comuníquese con la atención al cliente](../start/user-interface.md#support-ticket-guidelines) con los registros de recorrido, los identificadores de perfil afectados y los detalles sobre la transición nula

>[!NOTE]
>
>Recuerde que los eventos enviados fuera de la ventana de fecha activa del recorrido se descartan silenciosamente sin ningún mensaje de error. Compruebe siempre primero la configuración del tiempo de recorrido al solucionar problemas de progresión de perfiles de prueba.

## Comprobar cómo navegan las personas por el recorrido {#checking-how-people-navigate-through-the-journey}

La creación de informes de recorrido mide el progreso de las personas dentro de un recorrido. Es fácil identificar dónde y por qué detuvieron a una persona.

A continuación se presentan algunas cosas para comprobar:

* ¿Se debe a una condición que excluye a la persona? Por ejemplo, la condición es &quot;género = hombre&quot; y la persona es mujer. Esta comprobación puede realizarla un usuario empresarial si la condición no es demasiado compleja.
* ¿Se debe a que una llamada a una fuente de datos no responde? Cuando el recorrido está en prueba, esta información se puede ver en los registros del modo de prueba. Cuando el recorrido está activo, un administrador puede probar las llamadas directas a la fuente de datos y comprobar la respuesta recibida. Un administrador también puede realizar el duplicado del recorrido y probarlo.

## Eventos descartados debido a una instancia de recorrido bloqueada {#max-instance-stack-events-reached}

Si ve eventos descartados con el motivo `maxInstanceStackEventsReached`, el tiempo de ejecución de recorrido ha alcanzado su límite interno de pila de eventos por perfil de 10 eventos para una versión de recorrido específica. Se trata de una protección de seguridad que evita que se apilen demasiados eventos pendientes mientras se sigue procesando otro evento para el mismo perfil.

Este es **no** un límite de tiempo o de rendimiento. Se produce cuando la instancia de recorrido del perfil se bloquea en un paso de larga ejecución (por ejemplo, una espera larga, un enriquecimiento o reintentos de acción personalizados) y los eventos del mismo perfil, que también se utilizan en esa recorrido, se acumulan más allá del límite de 10 eventos.

Para identificarlo, consulte los eventos de paso del recorrido donde el motivo de descarte sea igual a `maxInstanceStackEventsReached` (por ejemplo, en `serviceEvents.stateMachine.eventType` o campos similares). Obtenga más información acerca de los tipos de eventos descartados en la [lista de campos de eventos de paso](../reports/sharing-field-list.md#discarded-events).

**Lo que puedes hacer**

* Reduzca las esperas largas o los pasos lentos en rutas que pueden volver a déclencheur con frecuencia.
* Deduplique o devuelva eventos ascendentes cuando sea posible.
* Divida los escenarios de larga duración en varios recorridos para evitar el apilamiento.

## Comprobar que los mensajes se envíen correctamente {#checking-that-messages-are-sent-successfully}

Si las personas recorren el recorrido correctamente pero no reciben mensajes que deberían recibir, puede comprobar lo siguiente:

* [!DNL Journey Optimizer] ha tenido en cuenta correctamente la solicitud para enviar el mensaje. Los usuarios empresariales pueden acceder al mensaje que se supone que se debe enviar y comprobar si la hora de la última ejecución corresponde al tiempo de ejecución de su recorrido. También pueden consultar las últimas llamadas o eventos de API recibidas.
* [!DNL Journey Optimizer] ha enviado correctamente el mensaje. Compruebe los informes de recorrido para asegurarse de que no hay errores.

En el caso de un mensaje enviado mediante una acción personalizada, lo único que se puede comprobar durante la prueba de recorrido es el hecho de que la llamada del sistema de la acción personalizada produce un error o no. Si la llamada al sistema externo asociada con la acción personalizada no genera un error pero no conduce al envío de un mensaje, algunas investigaciones deben realizarse en el sistema externo.

## Explicación de las entradas duplicadas en eventos de paso de Recorrido {#duplicate-step-events}

Utilice esta sección para comprender por qué pueden aparecer filas duplicadas en los eventos de paso de Recorrido.

### ¿Por qué veo varias entradas con la misma instancia de recorrido, perfil, nodo y ID de solicitud?

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

**Nº** El impacto se limita únicamente al registro. [!DNL Adobe Journey Optimizer] tiene mecanismos de deduplicación integrados en la capa de ejecución de mensajes que garantizan:

* Solo un mensaje (correo electrónico, SMS, notificación push, etc.) se envía a cada perfil
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

Si persisten las discrepancias, [póngase en contacto con el Soporte técnico de Adobe](../start/user-interface.md#support-ticket-guidelines) con capturas de pantalla de las pestañas Información general y Examinar para realizar una investigación.

## Parámetros de seguimiento que muestran marcadores de posición vacíos en recorridos cerrados {#tracking-parameters-closed-journeys}

Si las direcciones URL de seguimiento en los correos electrónicos enviados contienen marcadores de posición vacíos como `cid=em-acou-adob{}`, esto puede indicar que no se pudo resolver un campo de contexto como `context.system.source.actionId`. Esto suele ocurrir cuando se cierra un recorrido y no se ha vuelto a publicar después de un cambio de producto relevante: solo los recorridos que se han vuelto a publicar rellenan correctamente estos campos de contexto en las direcciones URL de seguimiento.

Para resolver esto, vuelva a publicar el recorrido ([cree una nueva versión y publíquelo](publish-journey.md#journey-create-new-version)) o quite la referencia al campo de contexto afectado de los [parámetros de seguimiento de URL](../email/url-tracking.md) en la configuración del canal o del contenido del correo electrónico.

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página es una referencia completa de solución de problemas para la ejecución de recorridos en directo en Adobe Journey Optimizer, y abarca la entrega de eventos, errores de entrada de perfil, problemas de transición de modo de prueba, eventos descartados, registros de eventos de pasos duplicados, comprobaciones de entrega de mensajes y discrepancias de métricas de panel.

**Intenciones:**
* Diagnostique por qué los eventos no activan la entrada de recorridos comprobando la estructura de carga útil, los encabezados y las condiciones de calificación
* Compruebe si los perfiles entran y progresan a través de un recorrido en directo o en modo de prueba
* Resolver errores de transición del modo de prueba causados por fechas de inicio futuras o áreas de nombres de identidad mal configuradas
* Comprenda y gestione el motivo de descarte de `maxInstanceStackEventsReached` para las instancias de recorrido bloqueadas
* Identificar y consultar correctamente las entradas duplicadas del registro de eventos de paso de Recorrido provocadas por el escalado automático del servidor
* Investigue los mensajes que faltan comprobando los resultados de los informes de recorrido y las llamadas de acción personalizada
* Corrección de marcadores de posición de URL de seguimiento vacíos en correos electrónicos de recorridos cerrados

**Glosario:**
* **Eventos de paso de Recorrido**: Un conjunto de datos que registra cada paso que un perfil ejecuta dentro de un recorrido y que se utiliza para generar informes y depurar *(específico del producto)*
* **notSuitableInitialEvent**: Se recibió un código de descarte que indica un evento, pero se descartó porque no se cumplió la condición de calificación *(específico del producto)*
* **maxInstanceStackEventsReached**: se ha excedido *(específico del producto)* un código de descarte que indica el límite de 10 eventos de recorrido por perfil
* **isValidTransition**: propiedad de solo interfaz de usuario en los detalles técnicos del recorrido; un valor nulo puede indicar una fecha de inicio futura o una conexión de nodo dañada, pero no afecta al procesamiento back-end *(específico del producto)*
* **Condición de calificación**: regla definida en un evento que debe cumplirse para que el evento almacene en déclencheur un recorrido; los eventos que no cumplan esta condición se descartarán
* **Reequilibrio**: una operación de escalado automático back-end en los microservicios de AJO que puede crear entradas de registro de eventos de pasos de Recorrido duplicadas con valores de `_id` diferentes

**Protecciones:**
* Los eventos enviados fuera de la ventana de fecha y hora activa del recorrido se descartan silenciosamente sin ningún mensaje de error
* El límite de pila de eventos de instancia de recorrido por perfil es de 10 eventos. Si se supera este límite, los eventos se descartarán con `maxInstanceStackEventsReached`
* Las entradas duplicadas de eventos de pasos de Recorrido con valores diferentes de `_id` se esperan en el sistema y no indican la duplicación de mensajes
* Las métricas de Información general del panel solo incluyen recorridos con tráfico en las últimas 24 horas; las métricas pueden tardar hasta 30 minutos en actualizarse
* Los recorridos cerrados que no se hayan vuelto a publicar después de un cambio de producto pueden producir marcadores de posición vacíos en las direcciones URL de seguimiento

**Terminología:**
* Nombre canónico: Eventos de paso de Recorrido — Acrónimo: none — variantes: eventos de paso, registros de ejecución de recorrido
* Nombre canónico: Condición de calificación — Acrónimo: none — variantes: regla de calificación de eventos, condición de evento
* Sinónimos: &quot;reequilibrio&quot; = &quot;escalado automático&quot; (operación back-end que provoca entradas de registro duplicadas)
* No confunda: &quot;duplicar `_id`&quot; ≠ &quot;duplicar entradas de registro del reequilibrio&quot;: los duplicados verdaderos comparten el mismo `_id`; los duplicados del reequilibrio tienen valores diferentes de `_id`

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Por qué mis eventos no desencadenan un recorrido aunque se envíen correctamente?** — Compruebe que el recorrido está activo o en modo de prueba, que la carga útil coincide con la estructura del esquema de eventos, que se cumple la condición de calificación y que se incluyen los encabezados correctos (`X-gw-ims-org-id`, `Content-type`).
* **Q: ¿Por qué los perfiles de prueba entran en el recorrido pero no avanzan más allá del primer paso?** — La causa más común es una fecha de inicio del recorrido establecida en el futuro; los eventos se descartan silenciosamente fuera de la ventana de fecha activa. Compruebe también la coincidencia del indicador del perfil de prueba y el área de nombres de identidad.
* **Q: ¿Qué significa `maxInstanceStackEventsReached`?** — El tiempo de ejecución de la recorrido ha alcanzado el límite interno de pila de 10 eventos para una instancia de perfil específica, normalmente porque un paso de larga duración está bloqueando el procesamiento. Reduzca las esperas largas, deduplique los eventos ascendentes o divida el escenario en varios recorridos.
* **Q: veo filas duplicadas en Eventos de paso de Recorrido. ¿Hay algún problema?** — No. Se esperan entradas duplicadas con diferentes valores de `_id` y el resultado es un escalado automático del backend. Solo se envía un mensaje; compruebe con `ajo_message_feedback_event_dataset`.
* **Q: ¿Por qué las direcciones URL de seguimiento en los correos electrónicos muestran marcadores de posición vacíos como `cid=em-acou-adob{}`?** — El recorrido se cerró y no se volvió a publicar después de un cambio de producto; los campos de contexto no se pueden resolver. Vuelva a publicar el recorrido o elimine la referencia del campo de contexto afectado de los parámetros de seguimiento de URL.
* **Q: ¿Por qué el panel Información general muestra números diferentes a los de la ficha Examinar?** — El tablero solo cuenta los recorridos con tráfico en las últimas 24 horas, las métricas tardan hasta 30 minutos en actualizarse y los permisos de acceso pueden limitar la visibilidad.

+++
