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
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 2152
ht-degree: 27%

---

# Trabajo con eventos de recorrido {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Eventos de recorrido"
>abstract="Journey Optimizer admite tres tipos de eventos en los recorridos: eventos unitarios, vinculados al comportamiento de una persona específica (como una compra o un hito de lealtad); eventos empresariales, activados por una ocurrencia global (como una cancelación de un vuelo o una actualización de stock) y eventos de calificación de público, activados cuando un perfil entra o sale de un público. Utilice eventos para activar recorridos y orquestar las acciones adecuadas para sus perfiles."

Utilice eventos para almacenar en déclencheur los recorridos individualmente y enviar mensajes en tiempo real a cada usuario cuando entre en el recorrido.

>[!IMPORTANT]
>
>Para conocer los requisitos y limitaciones de eventos (flujo continuo, servicio de consultas, ingesta por lotes), consulte [protecciones de Recorrido: eventos](../start/guardrails.md#events-g).

En la configuración de eventos, se configuran los eventos esperados en los recorridos. Los datos entrantes de los eventos se normalizan siguiendo el modelo de datos de Experience de Adobe (XDM). Los eventos provienen de las API de ingesta de streaming para eventos autenticados y no autenticados (como eventos del SDK de Adobe Mobile). Puede utilizar varios eventos (en diferentes pasos de un recorrido) y varios recorridos pueden utilizar el mismo evento.

La configuración del evento es **obligatoria** y la debe realizar un ingeniero de datos.

Puede configurar tres tipos de eventos: **Eventos unitarios**, **Eventos empresariales** y **Eventos de calificación de audiencias**.

➡️ [Descubra esta funcionalidad en vídeo](#video)

## Eventos unitarios {#unitary-events}

**Los eventos unitarios** están vinculados a una persona. Se refieren al comportamiento de una persona (por ejemplo, una persona compró un producto, visitó una tienda, salió de un sitio web, etc.) o algo que suceda vinculado a una persona (por ejemplo, una persona alcanzó 10 000 puntos de lealtad). Esto es lo que escucha [!DNL Journey Optimizer] en los recorridos para orquestar las mejores próximas acciones. Los eventos unitarios pueden basarse en reglas o generarse por el sistema. Para aprender a crear un evento unitario, consulte esta [página](../event/about-creating.md).

Los recorridos unitarios (que se inician con un evento o una calificación de público) incluyen un mecanismo de protección que evita que los recorridos se activen varias veces de forma errónea para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante cinco minutos. Por ejemplo, si un evento activa un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.

## Eventos empresariales {#business-events}

Los eventos de **Empresa** no están vinculados a un perfil específico. Por ejemplo, puede ser una alerta de noticias, una actualización deportiva, un cambio o cancelación de vuelo, una actualización de inventario, eventos meteorológicos, etc. Aunque estos eventos no son específicos de un perfil, pueden ser de interés para cualquier número de perfiles: personas suscritas a temas de noticias particulares, pasajeros en un vuelo, compradores interesados en un producto agotado, etc. Los eventos empresariales siempre están basados en reglas. Cuando suelta un evento empresarial en un recorrido, agrega automáticamente una actividad **Leer audiencia** justo después. Aprenda a crear un evento empresarial [en esta página](../event/about-creating-business.md).

## Eventos de calificación de público {#audience-qualification-events}

Se activa un evento **calificación de audiencia** cuando un perfil entra o sale de una audiencia. Por ejemplo, un cliente que cruza un umbral de gasto en fidelidad entra en la audiencia de nivel Gold; esa calificación déclencheur el recorrido de ese perfil en tiempo real (para audiencias de streaming) o en la siguiente evaluación por lotes. A diferencia de los eventos unitarios, la calificación de audiencia permite crear lógicas de activación complejas aprovechando toda la potencia de las definiciones de audiencia, sin requerir cambios de implementación para enviar un nuevo evento. Más información sobre [eventos de calificación de audiencia](../building-journeys/audience-qualification-events.md).

>[!NOTE]
>
>Los eventos de cualificación de audiencia no se configuran en **Administración > Eventos**; se seleccionan directamente en el lienzo de recorrido como primer paso de un recorrido.

## Eventos unitarios o empresariales de un vistazo {#event-comparison}

| | Evento unitario | Evento empresarial |
|---|---|---|
| **Vinculado a un perfil?** | Sí, se activa por la acción de un individuo específico. | No: se activa por una incidencia externa no vinculada a una persona. |
| **Comportamiento de entrada** | Un perfil entra en el recorrido en tiempo real. | Varios perfiles introducen mediante un paso automático de Lectura de Audiencia. |
| **Casos de uso habituales** | Confirmación de compra, envío de formulario, inicio de sesión en la aplicación, hito de lealtad. | Cancelación de vuelo, alerta de reposición de stock, noticias de última hora, evento meteorológico. |
| **Cómo inicia el recorrido** | Entrada basada en eventos: no se necesita audiencia. | Evento empresarial + audiencia de lectura automática (añadida por Journey Optimizer). |
| **Múltiple por recorrido?** | Sí, se pueden escuchar varios eventos unitarios a través de pasos de recorrido. | No: sólo un evento empresarial por recorrido, realizado al principio. |
| **Tipo de ID de evento** | Basado en reglas o generado por el sistema. | Siempre basado en reglas. |

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
>Journey Optimizer requiere que los eventos se transmitan al servicio principal de recopilación de datos (DCCS) para poder activar un recorrido. Los eventos importados por lotes, los eventos insertados a través de **Query Service** o los eventos procedentes de conjuntos de datos internos de Journey Optimizer (comentarios sobre mensajes, seguimiento de correos electrónicos, etc.) no se puede usar para activar un recorrido. Para los casos de uso en los que no pueda obtener los eventos transmitidos, genere un público basado en esos eventos y use la actividad **Leer público** en su lugar. Técnicamente, la calificación de audiencias puede utilizarse, pero puede provocar desafíos descendentes en función de las acciones utilizadas. Estos datos no necesariamente tienen que ir al perfil en tiempo real. Si desea utilizar los eventos para la segmentación, le recomendamos que habilite el conjunto de datos para el perfil.

## Cómo elegir {#choose-event-type}

Use los siguientes criterios para seleccionar el tipo de evento adecuado para el recorrido; la pregunta clave es: **¿está activando una acción para una persona específica o está difundiendo a muchos perfiles?** [Más información sobre los tipos de recorrido](../building-journeys/journey.md#journey-types).

* **Elija un evento unitario** cuando el déclencheur esté vinculado a un individuo específico; por ejemplo, una compra, un envío de formulario o un hito de lealtad. Los eventos unitarios requieren una identidad principal basada en persona en el esquema e inician la recorrido inmediatamente para ese perfil. [Aprenda a configurar un evento unitario](../event/about-creating.md).

* **Elige un evento empresarial** cuando el déclencheur sea global (por ejemplo, reabastecimiento de productos, caída de precios o cancelación de vuelos) y quieras retransmitir a un conjunto de perfiles relacionados con esa señal. Los eventos empresariales deben ser el primer paso en el recorrido y el destino automático de los perfiles mediante una actividad **Leer audiencia**. Requieren un esquema de serie temporal con una identidad principal que no sea personas y los campos `_id` y `timestamp`. Planifique un retraso de exportación de audiencia de 15 minutos a una hora como máximo. [Aprenda a configurar un evento empresarial](../event/about-creating-business.md).

* **Elija un evento de calificación de audiencia** cuando el déclencheur sea un perfil que entra o sale de una audiencia y necesite una lógica de segmentación más compleja de la que puede proporcionar un solo evento; por ejemplo, volver a atraer a los clientes caducados que acaban de cumplir un umbral de gasto o activar un flujo de incorporación cuando un miembro de VIP abandona el nivel de lealtad. [Más información sobre los eventos de calificación de audiencia](../building-journeys/audience-qualification-events.md).

>[!CAUTION]
>
>Los eventos empresariales no se pueden usar en el mismo recorrido que los eventos unitarios o las actividades de calificación de audiencia.

## Ciclo de datos {#data-cycle}

Los eventos son llamadas API POST. Los eventos se envían a Adobe Experience Platform a través de las API de ingesta de transmisión. El destino URL de los eventos enviados a través de las API de mensajería transaccional se denomina &quot;entrada&quot;. La carga útil de eventos sigue el formato XDM.

La carga útil contiene la información requerida por las API de ingesta de transmisión para funcionar (en el encabezado) y la información requerida por [!DNL Journey Optimizer] para funcionar y la información que se utilizará en los recorridos (en el cuerpo, por ejemplo, la cantidad de un carro de compras abandonado). Existen dos modos para la ingesta de streaming: autenticado y no autenticado. Para obtener más información sobre las API de ingesta de streaming, consulte [este vínculo](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=es){target="_blank"}.

Después de llegar a través de las API de ingesta de transmisión, los eventos fluyen a un servicio interno llamado Canalización y, a continuación, a Adobe Experience Platform. Si el esquema de evento tiene habilitado el indicador de Servicio de Perfil del cliente en tiempo real y un ID de conjunto de datos que también tiene el indicador de Perfil del cliente en tiempo real, se desplaza al servicio de Perfil del cliente en tiempo real.

Para los eventos generados por el sistema, la canalización filtra los eventos que tienen una carga útil que contiene [!DNL Journey Optimizer] eventIDs (consulte el proceso de creación de eventos que se muestra a continuación) proporcionados por [!DNL Journey Optimizer] y contenidos en la carga útil de evento. En el caso de los eventos basados en reglas, el sistema identifica el evento con la condición eventID. Estos eventos son escuchados por [!DNL Journey Optimizer] y se activa el recorrido correspondiente.


## Acerca del rendimiento de eventos de Recorrido {#event-thoughput}

Adobe Journey Optimizer admite un volumen máximo de 5000 eventos de recorrido por segundo a nivel de organización, en todas las zonas protegidas. Esta cuota se aplica a todos los eventos que se usan en recorridos activos, entre los que se incluyen los recorridos **Live**, **Dry run**, **Closed** y **Paused**. Cuando se alcanza esta cuota, los nuevos eventos se ponen en cola con una velocidad de procesamiento de 5000 por segundo. El tiempo máximo que un evento puede pasar en la cola es de **24 horas**.

Para obtener más información sobre las tasas de procesamiento de recorridos y cómo afectan los distintos tipos de recorridos al rendimiento, consulte [esta sección](../building-journeys/entry-management.md#journey-processing-rate).

Los siguientes tipos de eventos se contabilizan dentro de la cuota de 5,000 TPS:

* **Eventos unitarios externos**: incluye eventos basados en reglas y generados por el sistema. Si el mismo evento sin procesar cumple los requisitos para varias definiciones de regla, cada regla completa se cuenta como un evento independiente. Más detalles a continuación.

* **Eventos de calificación de audiencias**: Si se usa la misma audiencia de flujo continuo en varios recorridos, cada uso se cuenta por separado. Por ejemplo, si se utiliza la misma audiencia en una actividad de calificación de audiencia en dos recorridos, se cuentan dos eventos.

* **Eventos de reacción**: Eventos activados por reacciones de perfil (correo electrónico abierto, correo electrónico en el que se hizo clic, etc.) dentro de un recorrido.

* **Eventos empresariales**: los eventos no están vinculados a un perfil específico, sino a un evento relacionado con el negocio.

* **Eventos de Analytics**: si la [integración con Adobe Analytics en recorridos de déclencheur](about-analytics.md) se ha habilitado, también se incluyen estos eventos.

* **Reanudar eventos**: evento técnico activado cuando un perfil se reanuda desde un recorrido pausado. Más información acerca de [reanudar recorridos en pausa](../building-journeys/journey-pause.md#journey-resume-steps).

* **Eventos de finalización de nodo de espera**: cuando un perfil sale de un nodo de espera, se genera un evento técnico para reanudar la recorrido.

>[!NOTE]
>
>Excepto en los eventos de espera y reanudación, todos los demás tipos de eventos también se contabilizan en la cuota cuando se utilizan en recorridos basados en audiencias de lectura.

### Acerca de los eventos sin procesar que cumplen los requisitos para varias definiciones de regla

El mismo evento sin procesar puede cumplir los requisitos para varias definiciones de regla en los recorridos. Cuando se configura un evento en la sección **Administration** para el mismo esquema de evento, se pueden definir varias reglas de evento. Supongamos, por ejemplo, que tenemos un evento de compra con campos city y purchaseValue. Consideremos los siguientes escenarios:

1. Se crea un evento **E1** denominado `newYorkPurchases` con una definición de regla que indica `city=='New York'`. Este evento puede utilizarse en 10 recorridos, pero se contará solo como 1 evento cuando llegue.

1. Ahora supongamos que también se crea un evento **E2** denominado `highValuePurchases` con `purchaseValue > 1000` como definición de regla, en el mismo esquema de evento que **E1**. En este caso, el mismo evento entrante se evaluará con dos reglas: `newYorkPurchases` y `highValuePurchases`. Ahora puede ocurrir que una compra en Nueva York también sea una compra de alto valor.

   En este caso, Journey Optimizer creará dos eventos, **E1** y **E2**, a partir del mismo evento entrante, lo que hará que este solo evento entrante se cuente como dos eventos.

   Tenga en cuenta que estos eventos comienzan a contarse cuando se utilizan en un recorrido activo, incluido el recorrido **Activo**, **Ejecución en seco**, **Cerrado** y **En pausa**.

## Actualización y eliminación de un evento {#update-event}


Para evitar romper los recorridos existentes, cuando edita un evento utilizado en un recorrido **Borrador**, **Activo** o **Cerrado**, solo puede cambiar el nombre, la descripción o agregar campos de carga útil.

No se puede eliminar ningún evento utilizado en los recorridos **Live**, **Draft** o **Closed**. Para eliminar un evento utilizado, debe detener los recorridos que lo utilicen o eliminarlo de los recorridos de borrador en los que se utilice. Puede comprobar el campo **[!UICONTROL Utilizado en]**. Muestra el número de recorridos que utilizan ese evento en particular. Puede hacer clic en el botón **[!UICONTROL Ver recorridos]** para mostrar la lista de los recorridos correspondientes.

## Vídeotutoriales {#video}

Aprenda a configurar un evento y a especificar su punto final de reproducción y la carga útil.

>[!VIDEO](https://video.tv.adobe.com/v/3431518?captions=spa&quality=12)

Comprenda los casos de uso aplicables a los eventos empresariales. Obtenga información sobre cómo crear un recorrido mediante un evento empresarial y las prácticas recomendadas que se deben aplicar.

>[!VIDEO](https://video.tv.adobe.com/v/3416328?captions=spa&quality=12)
