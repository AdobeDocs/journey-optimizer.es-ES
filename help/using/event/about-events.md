---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con eventos de recorrido
description: Aprenda a trabajar con eventos en sus recorridos
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: eventos, evento, recorrido, definición, inicio
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: e4ea791dbc4362bff1d822f0b36add829e7a259d
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 43%

---

# Trabajo con eventos de recorrido {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Eventos de recorrido"
>abstract="Un evento está vinculado a una persona. Hace referencia al comportamiento de una persona (por ejemplo, una persona compró un producto, visitó una tienda, salió de un sitio web, etc.) o a algo que sucede vinculado a una persona (por ejemplo, una persona alcanzó 10 000 puntos de lealtad). Journey Optimizer escucha eventos unitarios en recorrido para orquestar las mejores próximas acciones."

Utilice eventos para almacenar en déclencheur los recorridos individualmente y enviar mensajes en tiempo real a cada usuario cuando entre en el recorrido.

En la configuración de eventos, se configuran los eventos esperados en los recorridos. Los datos entrantes de los eventos se normalizan siguiendo el modelo de datos de Experience de Adobe (XDM). Los eventos provienen de las API de ingesta de transmisión para eventos autenticados y no autenticados (como eventos del SDK de Adobe Mobile). Puede utilizar varios eventos (en diferentes pasos de un recorrido) y varios recorridos pueden utilizar el mismo evento.

La configuración del evento es **obligatoria** y la debe realizar un ingeniero de datos.

Puede configurar dos tipos de eventos: **Eventos unitarios** y **Eventos empresariales**.


➡️ [Descubra esta funcionalidad en vídeo](#video)

## Eventos unitarios {#unitary-events}

**Los eventos unitarios** están vinculados a una persona. Se refieren al comportamiento de una persona (por ejemplo, una persona compró un producto, visitó una tienda, salió de un sitio web, etc.) o algo que sucede vinculado a una persona (por ejemplo, una persona alcanzó 10 000 puntos de lealtad). Esto es lo que [!DNL Journey Optimizer] escuchará en los recorridos para orquestar las mejores próximas acciones. Los eventos unitarios pueden basarse en reglas o generarse por el sistema. Para aprender a crear un evento unitario, consulte esta [página](../event/about-creating.md).

Los recorridos unitarios (que se inician con un evento o una calificación de público) incluyen un mecanismo de protección que evita que los recorridos se activen varias veces de forma errónea para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante cinco minutos. Por ejemplo, si un evento activa un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.

## Eventos empresariales {#business-events}

Los eventos de **Empresa** no están vinculados a un perfil específico. Por ejemplo, puede ser una alerta de noticias, una actualización deportiva, un cambio o cancelación de vuelo, una actualización de inventario, eventos meteorológicos, etc. Aunque estos eventos no son específicos de un perfil, pueden ser de interés para cualquier número de perfiles: personas suscritas a temas de noticias particulares, pasajeros en un vuelo, compradores interesados en un producto agotado, etc. Los eventos empresariales siempre están basados en reglas. Cuando suelta un evento empresarial en un recorrido, agrega automáticamente una actividad **Leer audiencia** justo después. Aprenda a crear un evento empresarial [en esta página](../event/about-creating-business.md).


## Tipo de ID de evento {#event-id-type}

Para los eventos **business**, el tipo de ID de evento siempre está basado en reglas.

Para los eventos **unitarios**, existen dos tipos de ID de evento:

* Eventos basados **en reglas**: este tipo de evento no genera ningún eventID. Con el sencillo editor de expresiones simple, solo tendrá que definir una regla que el sistema utilizará para identificar los eventos relevantes que desencadenarán sus recorridos. Esta regla se puede basar en cualquier campo disponible en la carga útil de evento, por ejemplo, la ubicación del perfil o el número de elementos agregados al carro de compras del perfil.

  >[!CAUTION]
  >
  >Se define una regla de límite para los eventos basados en reglas. Limita el número de eventos calificados que un recorrido puede procesar a 5000 por segundo para una organización determinada. Corresponde a los SLA de Journey Optimizer. Consulte sus licencias de Journey Optimizer y [Descripción del producto de Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html).

* Eventos **generados por el sistema**: estos eventos requieren un eventID. Este campo eventID se genera automáticamente al crear el evento. El sistema que impulsa el evento no debe generar un ID, debe pasar el que está disponible en la previsualización de carga útil.

>[!NOTE]
>
>Journey Optimizer requiere que los eventos se transmitan al servicio principal de recopilación de datos (DCCS) para poder activar un recorrido. Los eventos consumidos por lotes o los eventos de conjuntos de datos internos de Journey Optimizer (comentarios de mensajes, seguimiento del correo electrónico, etc.) no se pueden utilizar para activar un recorrido. Para los casos de uso en los que no pueda obtener los eventos transmitidos, genere un público basado en esos eventos y use la actividad **Leer público** en su lugar. Técnicamente, la calificación de audiencias puede utilizarse, pero puede provocar desafíos descendentes en función de las acciones utilizadas. Estos datos no necesariamente tienen que ir al perfil en tiempo real. Si desea utilizar los eventos para la segmentación, le recomendamos que habilite el conjunto de datos para el perfil.

## Ciclo de datos {#data-cycle}

Los eventos son llamadas API POST. Los eventos se envían a Adobe Experience Platform a través de las API de ingesta de transmisión. El destino URL de los eventos enviados a través de las API de mensajería transaccional se denomina &quot;entrada&quot;. La carga útil de eventos sigue el formato XDM.

La carga útil contiene la información requerida por las API de ingesta de transmisión para funcionar (en el encabezado) y la información requerida por [!DNL Journey Optimizer] para funcionar y la información que se utilizará en los recorridos (en el cuerpo, por ejemplo, la cantidad de un carro de compras abandonado). Existen dos modos para la ingesta de flujo continuo: autenticado y no autenticado. Para obtener más información sobre las API de ingesta de flujos, consulte [este vínculo](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=es){target="_blank"}.

Después de llegar a través de las API de ingesta de transmisión, los eventos fluyen a un servicio interno llamado Canalización y, a continuación, a Adobe Experience Platform. Si el esquema de evento tiene habilitado el indicador de Servicio de Perfil del cliente en tiempo real y un ID de conjunto de datos que también tiene el indicador de Perfil del cliente en tiempo real, se desplaza al servicio de Perfil del cliente en tiempo real.

Para los eventos generados por el sistema, la canalización filtra los eventos que tienen una carga útil que contiene [!DNL Journey Optimizer] eventIDs (consulte el proceso de creación de eventos que se muestra a continuación) proporcionados por [!DNL Journey Optimizer] y contenidos en la carga útil de evento. En el caso de los eventos basados en reglas, el sistema identifica el evento con la condición eventID. Estos eventos son escuchados por [!DNL Journey Optimizer] y se activa el recorrido correspondiente.

## Actualización y eliminación de un evento

Para evitar romper los recorridos existentes, al editar un evento utilizado en un recorrido borrador, activo o cerrado, solo puede cambiar el nombre, la descripción o agregar campos de carga útil.

No se puede eliminar ningún evento utilizado en recorridos activos, en borrador o cerrados. Para eliminar un evento utilizado, debe detener los recorridos que lo utilicen o eliminarlo de los recorridos de borrador en los que se utilice. Puede comprobar el campo **[!UICONTROL Utilizado en]**. Muestra el número de recorridos que utilizan ese evento en particular. Puede hacer clic en el botón **[!UICONTROL Ver recorridos]** para mostrar la lista de los recorridos correspondientes.

## Vídeotutoriales {#video}

Aprenda a configurar un evento y a especificar su punto final de reproducción y la carga útil.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Comprenda los casos de uso aplicables a los eventos empresariales. Obtenga información sobre cómo crear un recorrido mediante un evento empresarial y las prácticas recomendadas que se deben aplicar.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
