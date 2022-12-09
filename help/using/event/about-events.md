---
solution: Journey Optimizer
product: journey optimizer
title: Acerca de los eventos
description: Más información sobre los eventos
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# Acerca de los eventos{#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Acerca de los eventos"
>abstract="Un evento está vinculado a una persona. Se refiere al comportamiento de una persona (por ejemplo, una persona compró un producto, visitó una tienda, salió de un sitio web, etc.) o algo que suceda vinculado a una persona (por ejemplo, una persona alcanzó 10 000 puntos de lealtad). Esto es lo que Journey Optimizer escuchará en los recorridos para orquestar las mejores próximas acciones."

La configuración de evento permite definir la información [!DNL Journey Optimizer] recibirá como eventos. Puede utilizar varios eventos (en diferentes pasos de un recorrido) y varios recorridos pueden utilizar el mismo evento.

>[!CAUTION]
>
>La configuración del evento es **mandatory** y debe realizarse mediante una **ingeniero de datos**.

Puede configurar dos tipos de eventos:

* **Unitario** eventos: estos eventos están vinculados a una persona. Se refieren al comportamiento de una persona (por ejemplo, una persona compró un producto, visitó una tienda, salió de un sitio web, etc.) o algo que suceda vinculado a una persona (por ejemplo, una persona alcanzó 10 000 puntos de lealtad). Esto es lo que [!DNL Journey Optimizer] escuchará en los recorridos para orquestar las mejores próximas acciones. Los eventos unitarios pueden generarse mediante reglas o mediante el sistema. Para aprender a crear un evento unitario, consulte esta [página](../event/about-creating.md).

* **Empresa** eventos: un evento empresarial es un evento que, a diferencia de un evento unitario, no está vinculado a un perfil específico. Por ejemplo, puede ser una alerta de noticias, una actualización de deportes, un cambio o cancelación de vuelo, una actualización de inventario, eventos meteorológicos, etc. Aunque estos eventos no son específicos de un perfil, pueden ser de interés para cualquier número de perfiles: personas suscritas a temas de noticias particulares, pasajeros en un vuelo, compradores interesados en un producto fuera de existencias, etc. Los eventos comerciales siempre se basan en reglas. Cuando se coloca un evento empresarial en un recorrido, se agrega automáticamente un **Leer segmento** actividad justo después. Para aprender a crear un evento empresarial, consulte esta [página](../event/about-creating-business.md).


>[!NOTE]
>
>Si edita un evento utilizado en un recorrido en borrador o activo, solo puede cambiar el nombre, la descripción o añadir campos de carga útil. Limitamos estrictamente la edición de los recorridos en borrador o en directo para evitar que se rompan los recorridos.

Los recorridos unitarios (comenzando por un evento o una calificación de segmento) incluyen una protección que evita que los recorridos se activen varias veces por error para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante 5 minutos. Por ejemplo, si un evento activa un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no volverá a comenzar para este perfil.

➡️ [Descubra esta función en vídeo](#video)

## Tipo de ID de evento{#event-id-type}

Para los eventos empresariales, el tipo de ID de evento siempre se basa en reglas.

Para los eventos unitarios, existen dos tipos de ID de evento:

* **Basado en reglas** eventos: este tipo de evento no genera un eventID. Con el editor de expresiones simple, simplemente define una regla que utilizará el sistema para identificar los eventos relevantes que activarán sus recorridos. Esta regla se puede basar en cualquier campo disponible en la carga útil de evento, por ejemplo la ubicación del perfil o el número de elementos agregados al carro de compras del perfil.

   >[!CAUTION]
   >
   >Se define una regla de límite para los eventos basados en reglas. Limita el número de eventos calificados que un recorrido puede procesar a 5000 por segundos para una organización determinada. Corresponde a los SLA de Journey Optimizer. Consulte las licencias de Journey Optimizer y [Descripción del producto de Journey Optimizer](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

* **Generado por el sistema** eventos: estos eventos requieren un eventID. Este campo eventID se genera automáticamente al crear el evento. El sistema que impulsa el evento no debe generar un ID, debe pasar el disponible en la previsualización de carga útil.

Journey Optimizer requiere que los eventos se transmitan o se envíen por lotes a Adobe Experience Platform. Estos datos no necesariamente tienen que ir al Perfil en tiempo real. Si desea utilizar los eventos para la segmentación o la búsqueda en un recorrido independiente, le recomendamos que habilite el conjunto de datos para el perfil.

## Ciclo de datos {#data-cycle}

Los eventos son llamadas de API POST. Los eventos se envían a Adobe Experience Platform a través de las API de ingesta de transmisión. El destino URL de los eventos enviados a través de las API de mensajería transaccional se denomina &quot;entrada&quot;. La carga útil de eventos sigue el formato XDM.

La carga útil contiene la información requerida por las API de ingesta de transmisión para funcionar (en el encabezado) y la información requerida por [!DNL Journey Optimizer] para trabajar y la información que se utilizará en los recorridos (en el cuerpo, por ejemplo, la cantidad de un carro abandonado). Existen dos modos para la transmisión de flujo continuo: autenticado y no autenticado. Para obtener más información sobre las API de ingesta de flujos, consulte [este vínculo](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html).

Después de llegar a través de las API de ingesta de flujos, los eventos fluyen a un servicio interno llamado Canalización y, a continuación, a Adobe Experience Platform. Si el esquema de evento tiene habilitado el indicador del servicio de perfil del cliente en tiempo real y un ID de conjunto de datos que también tiene el indicador Perfil del cliente en tiempo real, se desplaza al servicio de perfil del cliente en tiempo real.

Para los eventos generados por el sistema, la canalización filtra los eventos que tienen una carga útil que contiene [!DNL Journey Optimizer] eventIDs (consulte el proceso de creación de eventos a continuación) proporcionado por [!DNL Journey Optimizer] y contenido en la carga útil de evento. En el caso de los eventos basados en reglas, el sistema identifica el evento utilizando la condición eventID . Estos eventos son escuchados por [!DNL Journey Optimizer] y se activa el recorrido correspondiente.

## Vídeos explicativos {#video}

Obtenga información sobre cómo configurar un evento, especifique el extremo de flujo continuo y la carga útil para un evento.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Comprender los casos de uso aplicables a los eventos empresariales. Aprenda a construir un recorrido utilizando un evento empresarial y qué prácticas recomendadas aplicar.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
