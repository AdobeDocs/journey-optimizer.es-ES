---
title: Acerca de los eventos
description: Más información sobre los eventos
translation-type: tm+mt
source-git-commit: 5c3f1e4d916c7259f25208785788d2566b316934
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 32%

---

# Acerca de los eventos{#concept_gfj_fqt_52b}

![](../assets/do-not-localize/badge.png)

>[!CONTEXTUALHELP]
>id="jo_events"
>title="Acerca de los eventos"
>abstract="Un evento está vinculado a una persona. Se refiere al comportamiento de una persona (por ejemplo, una persona compró un producto, visitó una tienda, salió de un sitio web, etc.) o algo que suceda vinculado a una persona (por ejemplo, una persona alcanzó 10 000 puntos de lealtad). Esto es lo que escucha [!DNL Journey Optimizer] en los recorridos para orquestar las mejores próximas acciones."

La configuración de eventos permite definir la información que [!DNL Journey Optimizer] recibirá como eventos. Puede utilizar varios eventos (en diferentes pasos de un recorrido) y varios recorridos pueden utilizar el mismo evento.

>[!CAUTION]
>
>La configuración de eventos es **obligatoria** y debe realizarla un **usuario técnico**.

Puede configurar dos tipos de eventos:

* **** Eventos unitarios: estos eventos están vinculados a una persona. Se refieren al comportamiento de una persona (por ejemplo, una persona compró un producto, visitó una tienda, salió de un sitio web, etc.) o algo que suceda vinculado a una persona (por ejemplo, una persona alcanzó 10 000 puntos de lealtad). Esto es lo que escucha [!DNL Journey Optimizer] en los recorridos para orquestar las mejores próximas acciones. Los eventos universales pueden estar basados en reglas o generarse en el sistema. Para aprender a crear un evento unitario, consulte esta [página](../event/about-creating.md).

* **** Eventos empresariales: un evento empresarial es un evento que, a diferencia de un evento unitario, no está vinculado a un perfil específico. Por ejemplo, puede ser una alerta de noticias, una actualización de deportes, un cambio o cancelación de vuelo, una actualización de inventario, eventos meteorológicos, etc. Aunque estos eventos no son específicos de un perfil, pueden ser de interés para cualquier número de perfiles: personas suscritas a temas de noticias particulares, pasajeros en un vuelo, compradores interesados en un producto fuera de existencias, etc. Los eventos comerciales siempre se basan en reglas. Cuando se coloca un evento comercial en un recorrido, se agrega automáticamente una actividad **Read segment** justo después. Para aprender a crear un evento empresarial, consulte esta [página](../event/about-creating-business.md).


>[!NOTE]
>
>Si edita un evento utilizado en un recorrido en borrador o activo, solo puede cambiar el nombre, la descripción o agregar campos de carga útil. Limitamos estrictamente la edición de los recorridos en borrador o en directo para evitar que se rompan.

## Tipo de ID de evento{#event-id-type}

Para los eventos empresariales, el tipo de ID de evento siempre se basa en reglas.

Para los eventos unitarios, existen dos tipos de ID de evento:

* **Eventos basados** en reglas: este tipo de evento no genera un eventID. Con el editor de expresiones simple, simplemente define una regla que utilizará el sistema para identificar los eventos relevantes que van a almacenar en déclencheur sus recorridos. Esta regla se puede basar en cualquier campo disponible en la carga útil de evento, por ejemplo la ubicación del perfil o el número de elementos agregados al carro de compras del perfil.

   >[!CAUTION]
   >
   >Se define una regla de límite para los eventos basados en reglas. Limita el número de eventos calificados que un recorrido puede procesar a 5000 por segundos para una organización determinada (ORG). Corresponde a los SLA de Journey Optimizer. Consulte esta [página](https://helpx.adobe.com/legal/product-descriptions/journey-orchestration.html).

* **Eventos** generados por el sistema: estos eventos requieren un eventID. Este campo eventID se genera automáticamente al crear el evento. El sistema que impulsa el evento no debe generar un ID, debe pasar el disponible en la previsualización de carga útil.

## Ciclo de datos {#section_r1f_xqt_pgb}

Los eventos son llamadas API POST. Los eventos se envían a Adobe Experience Platform a través de las API de ingesta de transmisión. El destino URL de los eventos enviados a través de las API de mensajería transaccional se denomina &quot;entrada&quot;. La carga útil de eventos sigue el formato XDM.

La carga útil contiene la información requerida por las API de ingesta de transmisión para funcionar (en el encabezado) y la información requerida por [!DNL Journey Optimizer] para funcionar y la información que se utilizará en los recorridos (en el cuerpo, por ejemplo, la cantidad de un carro abandonado). Existen dos modos para la transmisión de flujo continuo: autenticado y no autenticado. Para obtener más información sobre las API de ingesta de flujos, consulte [este vínculo](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html).

Después de llegar a través de las API de ingesta de transmisión, los eventos fluyen a un servicio interno llamado Canalización y, a continuación, a Adobe Experience Platform. Si el esquema de evento tiene habilitado el indicador de Servicio de Perfil del cliente en tiempo real y un ID de conjunto de datos que también tiene el indicador de Perfil del cliente en tiempo real, se desplaza al servicio de Perfil del cliente en tiempo real.

Para los eventos generados por el sistema, la canalización filtra los eventos que tienen una carga útil que contiene [!DNL Journey Optimizer] eventIDs (consulte el proceso de creación de eventos que se muestra a continuación) proporcionados por [!DNL Journey Optimizer] y contenidos en la carga útil de evento. En el caso de los eventos basados en reglas, el sistema identifica el evento utilizando la condición eventID . Estos eventos son escuchados por [!DNL Journey Optimizer] y se activa el recorrido correspondiente.
