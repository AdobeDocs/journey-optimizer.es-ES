---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de un evento empresarial
description: Obtenga información sobre cómo crear un evento empresarial
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: evento, recorrido, empresa, configuración
exl-id: 39eb40e1-d7f5-4a8e-9b64-c620940d5ff2
TQID: https://experienceleague.adobe.com/7-S4UBWGIpqk798A7EreKtcuX-HxUgq34DG3Wek-qmM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 867eeef1f90c152c463397222f5ed95f3b9c264b
workflow-type: tm+mt
source-wordcount: 1191
ht-degree: 14%

---

# Configuración de un evento empresarial {#configure-a-business-event}

>[!BEGINSHADEBOX]

**En esta página:** configure un evento empresarial para que pueda almacenar en déclencheur un recorrido para un conjunto de perfiles cada vez que se produzca una incidencia global, como un producto que vuelva a estar disponible.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_event_business"
>title="Eventos empresariales"
>abstract="La configuración de evento permite definir la información que Journey Optimizer recibirá como eventos. Puede utilizar varios eventos (en diferentes pasos de un recorrido) y varios recorridos pueden utilizar el mismo evento. A diferencia de los eventos unitarios, los eventos empresariales no están vinculados a un perfil específico. El tipo de ID de evento siempre se basa en reglas."

A diferencia de los eventos unitarios, los eventos empresariales no están vinculados a un perfil específico. El tipo de ID de evento siempre se basa en reglas. Obtenga más información sobre los eventos empresariales en [esta sección](../event/about-events.md).

Los recorridos basados en audiencias de lectura se pueden activar de una sola vez, mediante un planificador de forma regular o mediante un evento empresarial, cuando se produce el evento.

Los eventos empresariales pueden ser &quot;un producto vuelve a estar en stock&quot;, &quot;el precio de las acciones de una empresa alcanza un determinado valor&quot;, etc.

>[!NOTE]
>
>También puede ver el caso de uso de evento empresarial [tutorial](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/journeys/use-case-business-event){target="_blank"}. Tenga en cuenta que no es necesario habilitar el esquema para el perfil.

## Notas importantes {#important-notes}

* Solo están disponibles los esquemas de series temporales. Los esquemas Eventos de experiencia, Eventos de decisión y Eventos de paso de Recorrido no están disponibles.
* El esquema de evento debe contener una identidad principal no basada en personas. Se deben seleccionar los campos siguientes al definir el evento: `_id` y `timestamp`
* Los eventos empresariales solo se pueden eliminar como primer paso de un recorrido.
* Al eliminar un evento empresarial como primer paso de un recorrido, el tipo de programador del recorrido será &quot;evento empresarial&quot;.
* Solo se puede eliminar una actividad de audiencia de lectura después de un evento empresarial. Se añade automáticamente como el siguiente paso.
* Para permitir varias ejecuciones de eventos empresariales, active la opción correspondiente en la sección **[!UICONTROL Execution]** de las propiedades del recorrido.
* Después de activarse un evento empresarial, se producirá un retraso para exportar la audiencia de 15 minutos a hasta una hora.
* Al probar un evento empresarial, debe pasar los parámetros de evento y el identificador del perfil de prueba que va a introducir el recorrido en la prueba. Además, al probar un recorrido basado en eventos empresariales, solo puede almacenar en déclencheur una entrada de perfil única. Consulte [esta sección](../building-journeys/testing-the-journey.md#test-business). En el modo de prueba, no hay disponible el modo &quot;Vista de código&quot;.
* ¿Qué les sucede a las personas que están actualmente en el recorrido si llega un nuevo evento empresarial? Se comporta de la misma manera que cuando los individuos siguen en un recorrido recurrente cuando ocurre una nueva recurrencia. Su camino ha terminado. Como resultado, los especialistas en marketing deben prestar atención para evitar crear recorridos demasiado largos si esperan eventos comerciales frecuentes.
* Los eventos empresariales no se pueden usar junto con eventos unitarios o actividades de calificación de público.

## Varios eventos empresariales {#multiple-business-events}

Estas son algunas notas importantes que se aplican cuando se reciben varios eventos empresariales seguidos.

**¿Cuál es el comportamiento al recibir un evento empresarial mientras se procesa el recorrido?**

Los eventos empresariales siguen las reglas de reentrada del mismo modo que para los eventos unitarios. Si un recorrido permite la reentrada, se procesará el siguiente evento empresarial.

**¿Cuáles son las protecciones para evitar la sobrecarga de audiencias materializadas?**

En el caso de eventos empresariales puntuales, para un recorrido determinado, los datos insertados por el primer trabajo de evento se reutilizan durante un periodo de tiempo de 1 hora. Para los recorridos programados, no hay ninguna protección. Obtenga más información acerca de las audiencias en la [documentación del servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=es){target="_blank"}.

## Introducción a los eventos empresariales {#gs-business-events}

Estos son los primeros pasos para configurar un evento empresarial:

1. En la sección del menú ADMINISTRACIÓN, seleccione **[!UICONTROL Configuraciones]**. En la sección **[!UICONTROL Eventos]**, haga clic en **[!UICONTROL Administrar]**. Se muestra la lista de eventos.

   ![](assets/jo-event1.png)

1. Haga clic en **[!UICONTROL Crear evento]** para crear un nuevo evento. El panel de configuración de evento se abre en el lado derecho de la pantalla.

   ![](assets/jo-event2.png)

1. Introduzca el nombre del evento. También puede añadir una descripción.

   ![](assets/jo-event3-business.png)

   >[!NOTE]
   >
   >Solo se permiten caracteres alfanuméricos y guiones bajos. La longitud máxima es de 30 caracteres.

1. En el campo **[!UICONTROL Tipo]**, elija **Empresa**.

   ![](assets/jo-event3bis-business.png)

1. El número de recorridos que usa este evento se muestra en el campo **[!UICONTROL Utilizado en]**. Puede hacer clic en el icono **[!UICONTROL Ver recorridos]** para mostrar la lista de recorridos con este evento.

1. Defina los campos esquema y carga útil: aquí es donde selecciona la información de evento (o carga útil) que recorrido espera recibir. Esta información se utilizará más adelante en el recorrido. Consulte [esta sección](../event/about-creating-business.md#define-the-payload-fields).

   ![](assets/jo-event5-business.png)

   Solo están disponibles los esquemas de series temporales. Los esquemas `Experience Events`, `Decision Events` y `Journey Step Events` no están disponibles. El esquema de evento debe contener una identidad principal no basada en personas. Se deben seleccionar los campos siguientes al definir el evento: `_id` y `timestamp`

   ![](assets/test-profiles-4.png)

1. Haga clic dentro del campo **[!UICONTROL ID de evento]**. Utilice el editor de expresiones simple para definir la condición que utiliza el sistema para identificar los eventos que almacenan en déclencheur el recorrido.

   En nuestro ejemplo, escribimos una condición basada en el ID del producto. Esto significa que, siempre que el sistema reciba un evento que coincida con esta condición, lo pasará a los recorridos.

   >[!NOTE]
   >
   >En el editor de expresiones simple, no todos los operadores están disponibles, sino que dependen del tipo de datos. Por ejemplo, para un tipo de cadena de campo, puede utilizar &quot;contiene&quot; o &quot;es igual a&quot;.

1. Haga clic en **[!UICONTROL Guardar]**.

   ![](assets/journey7-business.png)

   El evento está ahora configurado y listo para añadirse a un recorrido. Se requieren pasos de configuración adicionales para recibir eventos. Obtenga más información en [esta página](../event/additional-steps-to-send-events-to-journey.md).

## Definición de los campos de carga útil {#define-the-payload-fields}

La definición de carga útil permite elegir la información que el sistema espera recibir del evento en su recorrido y la clave para identificar a qué persona está asociada al evento. La carga útil se basa en la definición del campo XDM de Experience Cloud. Para obtener más información sobre XDM, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

1. Seleccione un esquema XDM de la lista y haga clic en el campo **[!UICONTROL Campos]** o en el icono **[!UICONTROL Editar]**.

   ![](assets/journey8-business.png)

   Se muestran todos los campos definidos en el esquema. La lista de campos varía según el esquema. Puede buscar un campo específico o utilizar los filtros para mostrar todos los nodos y campos o solo los campos seleccionados. Según la definición del esquema, algunos campos pueden ser obligatorios y preseleccionados. No puede anular su selección. Todos los campos obligatorios para que los recorridos reciban el evento correctamente están seleccionados de forma predeterminada.

   ![](assets/journey9-business.png)

   >[!NOTE]
   >
   > Asegúrese de que los campos siguientes estén seleccionados: `_id` y `timestamp`

1. Seleccione los campos que espera recibir del evento. Estos son los campos que el usuario empresarial aprovechará en el recorrido.

1. Cuando termine de seleccionar los campos necesarios, haga clic en **[!UICONTROL Guardar]** o presione **[!UICONTROL Entrar]**.

   El número de campos seleccionados aparece en **[!UICONTROL Campos]**.

   ![](assets/journey12-business.png)

## Previsualización de la carga útil {#preview-the-payload}

Utilice la previsualización de carga útil para validar la definición de carga útil.

1. Haga clic en el icono **[!UICONTROL Ver carga útil]** para previsualizar la carga útil esperada por el sistema.

   ![](assets/journey13-business.png)

   Puede observar que se muestran los campos seleccionados.

   ![](assets/journey14-business.png)

1. Compruebe la previsualización para validar la definición de carga útil.

1. A continuación, puede compartir la previsualización de carga útil con la persona responsable del envío del evento. Esta carga útil puede ayudarles a diseñar la configuración de un evento que inserte [!DNL Journey Optimizer]. Consulte [esta página](../event/additional-steps-to-send-events-to-journey.md).
