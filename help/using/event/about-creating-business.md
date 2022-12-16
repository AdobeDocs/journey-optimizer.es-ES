---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de un evento empresarial
description: Aprenda a crear un evento empresarial
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: 39eb40e1-d7f5-4a8e-9b64-c620940d5ff2
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 8%

---

# Configuración de un evento empresarial {#configure-a-business-event}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_business"
>title="Eventos comerciales"
>abstract="La configuración de evento le permite definir la información que Journey Optimizer recibirá como eventos. Puede utilizar varios eventos (en diferentes pasos de un recorrido) y varios recorridos pueden utilizar el mismo evento. A diferencia de los eventos unitarios, los eventos comerciales no están vinculados a un perfil específico. El tipo de ID de evento siempre se basa en reglas."

A diferencia de los eventos unitarios, los eventos comerciales no están vinculados a un perfil específico. El tipo de ID de evento siempre se basa en reglas. Obtenga más información sobre los eventos empresariales en [esta sección](../event/about-events.md).

Los recorridos basados en segmentos de lectura se pueden activar en una sola toma, por un programador de forma regular o por un evento comercial, cuando se produce el evento.

Los eventos comerciales pueden ser &quot;un producto vuelve a estar en existencias&quot;, &quot;el precio de las acciones de una empresa alcanza cierto valor&quot;, etc.

>[!NOTE]
>
>También puede ver el caso de uso de evento empresarial [tutorial](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-business-event.html). Tenga en cuenta que no es necesario habilitar el esquema para el perfil.

## Notas importantes {#important-notes}

* Solo están disponibles los esquemas de series temporales. Los esquemas de eventos de experiencia, eventos de decisión y eventos de paso de Recorrido no están disponibles.
* El esquema de evento debe contener una identidad principal no basada en personas. Se deben seleccionar los campos siguientes al definir el evento: `_id` y `timestamp`
* Los eventos comerciales solo se pueden eliminar como el primer paso de un recorrido.
* Al soltar un evento empresarial como el primer paso de un recorrido, el tipo de programador del recorrido será &quot;evento empresarial&quot;.
* Solo se puede perder una actividad de segmento de lectura después de un evento comercial. Se añade automáticamente como el siguiente paso.
* Para permitir varias ejecuciones de eventos empresariales, active la opción correspondiente en la **[!UICONTROL Ejecución]** de las propiedades del recorrido.
* Una vez activado un evento empresarial, se producirá un retraso para que el segmento se exporte de 15 minutos a una hora.
* Al probar un evento comercial, debe pasar los parámetros de evento y el identificador del perfil de prueba que va a introducir el recorrido en la prueba. Además, al probar un recorrido basado en eventos empresariales, solo puede almacenar en déclencheur la entrada de perfil único. Consulte [esta sección](../building-journeys/testing-the-journey.md#test-business). En el modo de prueba, no hay ningún modo &quot;Vista de código&quot; disponible.
* ¿Qué les sucede a las personas que están actualmente en el recorrido si llega un nuevo evento de negocios? Se comporta de la misma manera que cuando las personas siguen en un recorrido recurrente cuando ocurre una nueva recurrencia. Su camino ha terminado. Como resultado, los especialistas en marketing deben prestar atención para evitar generar recorridos demasiado largos si esperan eventos comerciales frecuentes.
* Los eventos empresariales no se pueden usar junto con eventos unitarios o actividades de calificación de segmentos.

## Varios eventos comerciales {#multiple-business-events}

Estas son algunas notas importantes que se aplican cuando se reciben varios eventos comerciales seguidos.

**¿Cuál es el comportamiento al recibir un evento comercial mientras el recorrido se está procesando?**

Los eventos comerciales siguen las reglas de reentrada de la misma manera que para los eventos unitarios. Si un recorrido permite la reentrada, se procesará el siguiente evento comercial.

**¿Cuáles son las barreras para evitar la sobrecarga de segmentos materializados?**

En el caso de los eventos empresariales sin conexión, para un recorrido determinado, los datos impulsados por el primer trabajo de evento se reutilizan durante un periodo de tiempo de 1 hora. No hay protección para los recorridos programados. Obtenga más información sobre los segmentos en la [Documentación del servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## Introducción a los eventos empresariales {#gs-business-events}

Estos son los primeros pasos para configurar un evento empresarial:

1. En la sección del menú ADMINISTRACIÓN , seleccione **[!UICONTROL Configuraciones]**. En el  **[!UICONTROL Eventos]** , haga clic en **[!UICONTROL Administrar]**. Se muestra la lista de eventos.

   ![](assets/jo-event1.png)

1. Haga clic en **[!UICONTROL Crear evento]** para crear un nuevo evento. El panel de configuración de evento se abre en el lado derecho de la pantalla.

   ![](assets/jo-event2.png)

1. Introduzca el nombre del evento. También puede agregar una descripción.

   ![](assets/jo-event3-business.png)

   >[!NOTE]
   >
   >No utilice espacios ni caracteres especiales. No utilice más de 30 caracteres.

1. En el **[!UICONTROL Tipo]** , elija **Empresa**.

   ![](assets/jo-event3bis-business.png)

1. El número de recorridos que utilizan este evento se muestra en la variable **[!UICONTROL Se usa en]** campo . Puede hacer clic en el botón **[!UICONTROL Ver recorridos]** para mostrar la lista de recorridos que utilizan este evento.

1. Defina los campos esquema y carga útil: aquí es donde selecciona los recorridos de información de evento (o carga útil) que esperan recibir. Utilizará esta información más adelante en su recorrido. Consulte [esta sección](../event/about-creating-business.md#define-the-payload-fields).

   ![](assets/jo-event5-business.png)

   Solo están disponibles los esquemas de series temporales. `Experience Events`, `Decision Events` y `Journey Step Events` los esquemas no están disponibles. El esquema de evento debe contener una identidad principal no basada en personas. Se deben seleccionar los campos siguientes al definir el evento: `_id` y `timestamp`

   ![](assets/test-profiles-4.png)

1. Haga clic dentro del **[!UICONTROL Condición de ID de evento]** campo . Utilice el editor de expresiones simple para definir la condición que utiliza el sistema para identificar los eventos que déclencheur el recorrido.

   ![](assets/jo-event6-business.png)

   En nuestro ejemplo, escribimos una condición basada en el ID del producto. Esto significa que, cada vez que el sistema recibe un evento que coincide con esta condición, lo pasa a los recorridos.

   >[!NOTE]
   >
   >En el editor de expresiones simple, no todos los operadores están disponibles, dependen del tipo de datos. Por ejemplo, para un tipo de cadena de campo, puede utilizar &quot;contiene&quot; o &quot;igual a&quot;.

1. Haga clic en **[!UICONTROL Guardar]**.

   ![](assets/journey7-business.png)

   El evento está ahora configurado y listo para añadirse a un recorrido. Se requieren pasos de configuración adicionales para recibir eventos. Obtenga más información en [esta página](../event/additional-steps-to-send-events-to-journey.md).

## Definición de los campos de carga útil {#define-the-payload-fields}

La definición de carga útil permite elegir la información que el sistema espera recibir del evento en el recorrido y la clave para identificar qué persona está asociada al evento. La carga útil se basa en la definición del campo XDM del Experience Cloud. Para obtener más información sobre XDM, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target=&quot;_blank&quot;}.

1. Seleccione un esquema XDM de la lista y haga clic en el **[!UICONTROL Campos]** o en el **[!UICONTROL Editar]** icono.

   ![](assets/journey8-business.png)

   Se muestran todos los campos definidos en el esquema . La lista de campos varía de un esquema a otro. Puede buscar un campo específico o utilizar los filtros para mostrar todos los nodos y campos o solo los campos seleccionados. Según la definición del esquema, algunos campos pueden ser obligatorios y estar preseleccionados. No puede desseleccionarlos. Todos los campos obligatorios para que los recorridos reciban el evento correctamente están seleccionados de forma predeterminada.

   ![](assets/journey9-business.png)

   >[!NOTE]
   >
   > Asegúrese de que los campos siguientes estén seleccionados: `_id` y `timestamp`

1. Seleccione los campos que espera recibir del evento. Estos son los campos que el usuario empresarial aprovechará en el recorrido.

1. Cuando haya terminado de seleccionar los campos necesarios, haga clic en **[!UICONTROL Guardar]** o presione **[!UICONTROL Entrar]**.

   El número de campos seleccionados aparece en **[!UICONTROL Campos]**.

   ![](assets/journey12-business.png)

## Vista previa de la carga útil {#preview-the-payload}

Utilice la previsualización de carga útil para validar la definición de carga útil.

1. Haga clic en el **[!UICONTROL Ver carga útil]** para obtener una vista previa de la carga útil esperada por el sistema.

   ![](assets/journey13-business.png)

   Puede observar que se muestran los campos seleccionados.

   ![](assets/journey14-business.png)

1. Compruebe la previsualización para validar la definición de carga útil.

1. A continuación, puede compartir la previsualización de la carga útil con la persona responsable del envío del evento. Esta carga útil puede ayudarles a diseñar la configuración de un evento que se esté insertando en [!DNL Journey Optimizer]. Consulte [esta página](../event/additional-steps-to-send-events-to-journey.md).
