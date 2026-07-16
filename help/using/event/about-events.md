---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con eventos de recorrido
description: Aprenda a trabajar con eventos en sus recorridos
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: eventos, evento, recorrido, definición, inicio
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
TQID: https://experienceleague.adobe.com/xvLSBd-rwKKNqwQNDa4D8GfFzc-ND1FkC3EdstufkIY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d998adac-2f81-400b-a669-d07bb196e4ebid: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: d08afb72-92f6-4856-88e3-11ec34313c2fid: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 6657a77a27455643fa0fb3d94a4d7e3ab83e6843
workflow-type: tm+mt
source-wordcount: 2407
ht-degree: 15%

---

# Trabajo con eventos de recorrido {#about-events}

>[!BEGINSHADEBOX]

**En esta página:** Comprenda los tres tipos de eventos, sus requisitos de esquema, las restricciones clave y cómo elegir el adecuado para su caso de uso.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Eventos de recorrido"
>abstract="Journey Optimizer admite tres tipos de eventos en los recorridos: eventos unitarios, vinculados al comportamiento de una persona específica (como una compra o un hito de lealtad); eventos empresariales, activados por una ocurrencia global (como una cancelación de un vuelo o una actualización de stock) y eventos de calificación de público, activados cuando un perfil entra o sale de un público. Utilice eventos para activar recorridos y orquestar las acciones adecuadas para sus perfiles."

Utilice eventos para almacenar en déclencheur los recorridos individualmente y enviar mensajes en tiempo real a cada usuario cuando entre en el recorrido. En la configuración de eventos, se configuran los eventos esperados en los recorridos. Puede utilizar varios eventos (en diferentes pasos de un recorrido) y varios recorridos pueden utilizar el mismo evento.

La configuración del evento es **obligatoria** y la debe realizar un ingeniero de datos.

>[!IMPORTANT]
>
>* Antes de configurar eventos, asegúrese de que dispone de: la función **Administrador de Journey Optimizer** o **Ingeniero de datos**, un esquema XDM con **Perfil del cliente en tiempo real** habilitado, un extremo de flujo continuo activo y acceso a la zona protegida correcta.
>
>* Para conocer los requisitos y limitaciones de eventos (flujo continuo, servicio de consultas, ingesta por lotes), consulte [protecciones de Recorrido: eventos](../start/guardrails.md#events-g).

**Quién hace qué:**

| Tarea | Función |
| --- | --- |
| Diseño y creación del esquema XDM | Ingeniero de datos |
| Configuración del extremo de flujo continuo | Ingeniero de datos |
| Configurar eventos unitarios y empresariales (**Administración > Eventos**) | Ingeniero de datos o administrador |
| Uso de eventos en un recorrido | practicante de recorrido |
| Configurar eventos de cualificación de audiencia (seleccionados en el lienzo) | practicante de recorrido |

Puede configurar tres tipos de eventos: **Eventos unitarios**, **Eventos empresariales** y **Eventos de calificación de audiencias**.

➡️ [Descubra esta funcionalidad en vídeo](#video)

➡️ [Descubra esta funcionalidad en vídeo](#video)

## Eventos unitarios {#unitary-events}

**Los eventos unitarios** están vinculados a una persona. Se refieren al comportamiento de una persona (por ejemplo, una persona compró un producto, visitó una tienda, salió de un sitio web, etc.) o algo que suceda vinculado a una persona (por ejemplo, una persona alcanzó 10 000 puntos de lealtad). Esto es lo que escucha [!DNL Journey Optimizer] en los recorridos para orquestar las mejores próximas acciones. Los eventos unitarios pueden basarse en reglas o generarse por el sistema. [Aprenda a crear un evento unitario](../event/about-creating.md).

**Requisito de esquema:** Un esquema XDM ExperienceEvent con una identidad principal basada en persona y **Perfil del cliente en tiempo real** habilitado.

**Ejemplo:** Un cliente agrega elementos al carro de compras y cierra el explorador. Se activa un evento abandonado por el carro de compras, el perfil entra en la recorrido en tiempo real y recibe un correo electrónico de recuperación una hora después.

>[!NOTE]
>
>Los recorridos unitarios incluyen una protección de reentrada: la reentrada del perfil se bloquea de forma predeterminada durante 5 minutos después de los déclencheur del recorrido. Por ejemplo, si un evento déclencheur un recorrido a las 12:01 para un perfil y otro llega a las 12:03, el recorrido no se reiniciará para ese perfil.

## Eventos empresariales {#business-events}

Los eventos de **Empresa** no están vinculados a un perfil específico. Por ejemplo, puede ser una alerta de noticias, una actualización deportiva, un cambio o cancelación de vuelo, una actualización de inventario, eventos meteorológicos, etc. Aunque estos eventos no son específicos de un perfil, pueden ser de interés para cualquier número de perfiles: personas suscritas a temas de noticias particulares, pasajeros en un vuelo, compradores interesados en un producto agotado, etc. Los eventos empresariales siempre están basados en reglas. Cuando suelta un evento empresarial en un recorrido, agrega automáticamente una actividad **Leer audiencia** justo después. [Aprenda a crear un evento empresarial](../event/about-creating-business.md).

**Requisito de esquema:** Un esquema XDM de serie temporal con una identidad principal que no es de persona y los campos `_id` y `timestamp` rellenados. Planifique un retraso de exportación de audiencia de 15 minutos a una hora como máximo.

**Ejemplo:** Una aerolínea cancela un vuelo. Se desencadena un evento empresarial, [!DNL Journey Optimizer] lee la audiencia de los pasajeros afectados y envía a cada uno una notificación de nueva reserva.

## Eventos de calificación de público {#audience-qualification-events}

Se activa un evento **calificación de audiencia** cuando un perfil entra o sale de una audiencia. Por ejemplo, un cliente que cruza un umbral de gasto en fidelidad entra en la audiencia de nivel Gold; esa calificación déclencheur el recorrido de ese perfil en tiempo real (para audiencias de streaming) o en la siguiente evaluación por lotes. A diferencia de los eventos unitarios, la calificación de audiencia permite crear lógicas de activación complejas aprovechando toda la potencia de las definiciones de audiencia, sin requerir cambios de implementación para enviar un nuevo evento. Más información sobre [eventos de calificación de audiencia](../building-journeys/audience-qualification-events.md).

**Requisito de esquema:** No se requiere ningún esquema adicional; el evento se basa en definiciones de audiencia existentes ya creadas en Adobe Experience Platform.

**Ejemplo:** El gasto de lealtad de un cliente cruza el umbral del nivel Gold. Su perfil se clasifica para la audiencia Gold, el recorrido déclencheur automáticamente y envía una recompensa de bienvenida.

>[!NOTE]
>
>Los eventos de cualificación de audiencia no se configuran en **Administración > Eventos**; se seleccionan directamente en el lienzo de recorrido como primer paso de un recorrido.

## Tipos de eventos de un vistazo {#event-comparison}

| | Evento unitario | Evento empresarial | Evento de calificación de audiencia |
| --- | --- | --- | --- |
| **Vinculado a un perfil?** | Sí, se activa por la acción de un individuo específico. | No: se activa por una incidencia externa no vinculada a una persona. | Sí: se activa cuando un perfil entra o sale de una audiencia. |
| **Comportamiento de entrada** | Un perfil entra en el recorrido en tiempo real. | Varios perfiles introducen mediante un paso automático de Lectura de Audiencia. | Se introduce un perfil cuando cambia la pertenencia a la audiencia. |
| **Casos de uso habituales** | Recuperación del abandono del carro de compras, envío de formularios, inicio de sesión en la aplicación, hito de lealtad. | Cancelación de vuelo, alerta de reposición de stock, noticias de última hora, evento meteorológico. | Nuevo compromiso de los clientes caducados, cambios en el nivel de lealtad, flujos de incorporación de VIP. |
| **Cómo inicia el recorrido** | Entrada basada en eventos: no se necesita audiencia. | Evento empresarial + audiencia de lectura automática (añadida por Journey Optimizer). | El perfil entra o sale de una audiencia definida. |
| **Múltiple por recorrido?** | Sí, se pueden escuchar varios eventos unitarios a través de pasos de recorrido. | No: sólo un evento empresarial por recorrido, realizado al principio. | Sí, se puede combinar con otras actividades. |
| **Tipo de ID de evento** | Basado en reglas o generado por el sistema. | Siempre basado en reglas. | Sin ID de evento, según la evaluación de pertenencia a audiencias. |
| **Configurado en la administración?** | Sí | Sí | No: se selecciona directamente en el lienzo de recorrido. |

>[!NOTE]
>
>Un recorrido solo puede contener **un** evento empresarial, que debe ser la primera actividad. Journey Optimizer agrega automáticamente una actividad **Leer audiencia** después de ella para definir qué perfiles reciben el recorrido activado por ese evento.

## Tipo de ID de evento {#event-id-type}

Para los eventos **business**, el tipo de ID de evento siempre está basado en reglas.

Para los eventos **unitarios**, existen dos tipos de ID de evento:

* Eventos basados **en reglas**: este tipo de evento no genera ningún eventID. Con el sencillo editor de expresiones simple, solo tendrá que definir una regla que el sistema utilizará para identificar los eventos relevantes que desencadenarán sus recorridos. Esta regla se puede basar en cualquier campo disponible en la carga útil de evento, por ejemplo, la ubicación del perfil o el número de elementos agregados al carro de compras del perfil.

  >[!CAUTION]
  >
  >Se define una regla de límite para los eventos basados en reglas. Limita el número de eventos calificados que un recorrido puede procesar a 5000 por segundo para una organización determinada. Corresponde a los SLA de Journey Optimizer. Consulte sus licencias de Journey Optimizer y [Descripción del producto de Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

* Eventos **generados por el sistema**: estos eventos requieren un eventID. Este campo eventID se genera automáticamente al crear el evento. El sistema que impulsa el evento no debe generar un ID, debe pasar el que está disponible en la previsualización de carga útil.

>[!NOTE]
>
>Solo los eventos transmitidos pueden almacenar en déclencheur los recorridos. El(la) siguiente **no se puede** usar para almacenar en déclencheur un recorrido:
>
>* Eventos ingeridos en lote
>* Eventos insertados mediante **servicio de consultas**
>* Eventos de conjuntos de datos internos de [!DNL Journey Optimizer] (comentarios de mensajes, seguimiento de correo electrónico y similares)
>
>Si no puede obtener eventos de flujo continuo, genere una audiencia basada en esos eventos y use una actividad **Leer audiencia** en su lugar. Para usar eventos solo para la segmentación, habilita el conjunto de datos para **Perfil del cliente en tiempo real**.

## Cómo elegir {#choose-event-type}

Use los siguientes criterios para seleccionar el tipo de evento adecuado para el recorrido; la pregunta clave es: **¿está activando una acción para una persona específica o está difundiendo a muchos perfiles?** [Más información sobre los tipos de recorrido](../building-journeys/journey.md#journey-types).

Cada tipo de evento se asigna a un patrón de recorrido específico:

| Tipo de evento | patrón de recorrido |
| --- | --- |
| Evento unitario | Recorrido en tiempo real de un solo perfil: déclencheur inmediatamente cuando una persona actúa |
| Evento empresarial | Recorrido de difusión: se dirige a muchos perfiles mediante un paso automático de Lectura de audiencia. |
| Evento de calificación de audiencia | Recorrido activado por segmentos: se activa cuando un perfil entra o sale de una audiencia |

* **Elija un evento unitario** cuando el déclencheur esté vinculado a un individuo específico; por ejemplo, una compra, un envío de formulario o un hito de lealtad. Los eventos unitarios requieren una identidad principal basada en persona en el esquema e inician la recorrido inmediatamente para ese perfil. [Aprenda a configurar un evento unitario](../event/about-creating.md).

* **Elige un evento empresarial** cuando el déclencheur sea global (por ejemplo, reabastecimiento de productos, caída de precios o cancelación de vuelos) y quieras retransmitir a un conjunto de perfiles relacionados con esa señal. Los eventos empresariales deben ser el primer paso en el recorrido y el destino automático de los perfiles mediante una actividad **Leer audiencia**. Requieren un esquema de serie temporal con una identidad principal que no sea personas y los campos `_id` y `timestamp`. Planifique un retraso de exportación de audiencia de 15 minutos a una hora como máximo. [Aprenda a configurar un evento empresarial](../event/about-creating-business.md).

* **Elija un evento de calificación de audiencia** cuando el déclencheur sea un perfil que entra o sale de una audiencia y necesite una lógica de segmentación más compleja de la que puede proporcionar un solo evento; por ejemplo, volver a atraer a los clientes caducados que acaban de cumplir un umbral de gasto o activar un flujo de incorporación cuando un miembro de VIP abandona el nivel de lealtad. [Más información sobre los eventos de calificación de audiencia](../building-journeys/audience-qualification-events.md).

>[!CAUTION]
>
>Los eventos empresariales no se pueden usar en el mismo recorrido que los eventos unitarios o las actividades de calificación de audiencia.

## Restricciones clave {#key-constraints}

Utilice este resumen para planificar la implementación antes de configurar los eventos.

| Restricción | Detalles |
| --- | --- |
| Límite de rendimiento | 5000 eventos por segundo por organización, en todos los entornos limitados (recorridos de audiencia unitarios y de lectura) |
| Bloque de reentrada | Reentrada del perfil bloqueada durante 5 minutos después de un déclencheur de recorrido unitario |
| Eventos empresariales por recorrido | Máximo 1, debe ser el primer paso |
| Combinar empresa y unidad en un recorrido | No compatible |
| Eventos por lotes | No se pueden almacenar en déclencheur los recorridos: use una actividad **Leer audiencia** en su lugar |
| Calificación de audiencias: administración | No configurado en **Administración > Eventos** — seleccionado directamente en el lienzo de recorrido |
| Edición de un evento activo | Solo puede cambiar el nombre, la descripción o agregar campos de carga útil |

## Cómo llegan los eventos a Journey Optimizer {#data-cycle}

Los eventos deben enviarse a [!DNL Journey Optimizer] como llamadas POST a través de [API de ingesta de transmisión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=es){target="_blank"}. La carga útil debe seguir el formato XDM y el esquema de evento debe tener habilitado **Perfil del cliente en tiempo real**.

Se admiten los modos de flujo continuo autenticado y no autenticado. Los eventos ingeridos por lotes y los eventos de conjuntos de datos [!DNL Journey Optimizer] internos (comentarios de mensajes, seguimiento de correo electrónico y similares) no se pueden usar para almacenar en déclencheur los recorridos; use una actividad **Leer audiencia** en su lugar para esos casos de uso.


## Límites de rendimiento de eventos {#event-throughput}

Adobe Journey Optimizer aplica límites de rendimiento independientes por tipo de evento, a nivel de organización, en todas las zonas protegidas:

* **Eventos unitarios**: 5000 eventos por segundo
* **Leer eventos de recorrido basados en audiencias**: 5000 eventos por segundo

Estos límites se aplican a todos los eventos usados en recorridos activos, que incluyen recorridos **Live**, **Dry run**, **Cerrado** y **Pausado**. Cuando se alcanza un límite, los nuevos eventos se ponen en cola y se procesan a 5000 por segundo hasta que se vacía la cola.

Para obtener más información sobre las tasas de procesamiento de recorridos y cómo afectan los distintos tipos de recorridos al rendimiento, [obtenga más información sobre las tasas de procesamiento de recorridos](../building-journeys/entry-management.md#journey-processing-rate).

Para estas cuotas se contabilizan los siguientes tipos de eventos:

* **Eventos unitarios externos**: incluye eventos basados en reglas y generados por el sistema. Si el mismo evento sin procesar cumple los requisitos para varias definiciones de regla, cada regla coincidente cuenta como un evento independiente para la cuota.

* **Eventos de calificación de audiencias**: Si se usa la misma audiencia de flujo continuo en varios recorridos, cada uso se cuenta por separado. Por ejemplo, si se utiliza la misma audiencia en una actividad de calificación de audiencia en dos recorridos, se cuentan dos eventos.

* **Eventos de reacción**: Eventos activados por reacciones de perfil (correo electrónico abierto, correo electrónico en el que se hizo clic, etc.) dentro de un recorrido.

* **Eventos empresariales**: los eventos no están vinculados a un perfil específico, sino a un evento relacionado con el negocio.

* **Eventos de Analytics**: si la [integración con Adobe Analytics en recorridos de déclencheur](about-analytics.md) se ha habilitado, también se incluyen estos eventos.

* **Reanudar eventos**: evento técnico activado cuando un perfil se reanuda desde un recorrido pausado. Más información acerca de [reanudar recorridos en pausa](../building-journeys/journey-pause.md#journey-resume-steps).

* **Eventos de finalización de nodo de espera**: cuando un perfil sale de un nodo de espera, se genera un evento técnico para reanudar la recorrido.

>[!NOTE]
>
>Excepto en los eventos de espera y reanudación, todos los demás tipos de eventos también se contabilizan en la cuota cuando se utilizan en recorridos basados en audiencias de lectura.

## Actualización y eliminación de un evento {#update-event}


Para evitar romper los recorridos existentes, cuando edita un evento utilizado en un recorrido **Borrador**, **Activo** o **Cerrado**, solo puede cambiar el nombre, la descripción o agregar campos de carga útil.

No se puede eliminar ningún evento utilizado en los recorridos **Live**, **Draft** o **Closed**. Para eliminar un evento utilizado, debe detener los recorridos que lo utilicen o eliminarlo de los recorridos de borrador en los que se utilice. Puede comprobar el campo **[!UICONTROL Utilizado en]**. Muestra el número de recorridos que utilizan ese evento en particular. Puede hacer clic en el botón **[!UICONTROL Ver recorridos]** para mostrar la lista de los recorridos correspondientes.

## Preguntas frecuentes {#faq}

**¿Puedo usar el mismo evento en varios recorridos?**
Sí: varios recorridos pueden escuchar el mismo evento simultáneamente.

**¿Puedo combinar un evento empresarial y un evento unitario en el mismo recorrido?**
No: los eventos empresariales no se pueden usar en el mismo recorrido que los eventos unitarios o las actividades de calificación de audiencia.

**¿Necesito configurar algo para los eventos de calificación de audiencia?**
No — los eventos de cualificación de audiencia no están configurados en **Administración > Eventos**. Seleccione la audiencia directamente en el lienzo de recorrido como primer paso.

**¿Puedo usar datos ingeridos por lotes para almacenar en déclencheur un recorrido?**
No, solo los eventos transmitidos pueden almacenar en déclencheur los recorridos. Para los datos por lotes, cree una audiencia y use una actividad **Leer audiencia** en su lugar.

**Mi recorrido no se está activando. ¿Qué debo comprobar?**

* Compruebe que su esquema de evento tenga habilitado **Perfil del cliente en tiempo real**.
* Confirme que los eventos se transmiten por secuencias: los eventos introducidos por lotes no pueden almacenar en déclencheur los recorridos.
* Para los eventos basados en reglas, compruebe que la condición de regla coincida con los campos de carga útil entrantes.
* Compruebe que el recorrido esté en estado **Activo** y que el perfil cumpla las condiciones de entrada.

## Próximos pasos {#next-steps}

* [Configuración de un evento unitario](../event/about-creating.md)
* [Configuración de un evento empresarial](../event/about-creating-business.md)
* [Más información sobre los eventos de calificación de audiencias](../building-journeys/audience-qualification-events.md)
* [Administrar entrada y reentrada de recorrido](../building-journeys/entry-management.md)

>[!TIP]
>
>Si el recorrido no se activa, compruebe que el esquema de eventos tenga habilitado **Perfil del cliente en tiempo real** y que los eventos se transmitan por secuencias; los eventos ingeridos por lotes no pueden almacenar en déclencheur los recorridos.

## Vídeotutoriales {#video}

Aprenda a configurar un evento y a especificar su punto final de reproducción y la carga útil.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Comprenda los casos de uso aplicables a los eventos empresariales. Obtenga información sobre cómo crear un recorrido mediante un evento empresarial y las prácticas recomendadas que se deben aplicar.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
