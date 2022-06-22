---
title: Copiar un recorrido en otro sandox
description: Aprenda a copiar un recorrido en otro sandox
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 4d211b9a0087526fe81d7b989195f21ceab42865
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# Copiar un recorrido en otro simulador de pruebas {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copiar un recorrido en otro simulador de pruebas"
>abstract="Journey Optimizer permite copiar un recorrido completo de un simulador para pruebas a otro. Por ejemplo, puede copiar un recorrido del entorno limitado de ensayo en el entorno limitado de producción. Además del propio Recorrido, Journey Optimizer también copia la mayoría de los objetos de los que depende el recorrido."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Detalles del Simulador para pruebas"
>abstract="Seleccione el simulador para pruebas de destino en el que desea copiar el recorrido. Solo están disponibles los entornos limitados de su organización de IMS."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Detalles del objeto"
>abstract="Este es el recorrido que va a copiar."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Objetos dependientes"
>abstract="Esta es la lista de objetos asociados que se utilizan en el recorrido. Esta lista muestra el nombre, el tipo de objeto y el Journey Optimizer ID interno."

Journey Optimizer permite copiar un recorrido completo de un simulador para pruebas a otro. Por ejemplo, puede copiar un recorrido del entorno de entorno limitado de ensayo en el entorno limitado de producción. Además del propio recorrido, Journey Optimizer también copia la mayoría de los objetos de los que depende el recorrido: mensajes, segmentos, ajustes preestablecidos, esquemas, eventos y acciones. Consulte la [limitaciones](../event/about-events.md)

>[!CAUTION]
>
>No garantizamos que todos los elementos vinculados se copien en el entorno limitado de destino. Le recomendamos encarecidamente que realice una comprobación exhaustiva antes de publicar el recorrido. Esto le permitirá identificar cualquier objeto que pueda faltar.

Los objetos copiados en el entorno limitado de destino son únicos y no existe riesgo de sobrescribir los elementos existentes. Tanto el recorrido como cualquier mensaje dentro del recorrido se transfieren en modo borrador. Esto le permite llevar a cabo una validación exhaustiva antes de la publicación en el simulador para pruebas de destino. El proceso de copia solo copia los metadatos sobre el recorrido y los objetos de ese Recorrido. Como parte de este proceso, no se copian datos de perfiles o conjuntos de datos.

Para copiar un recorrido en otro simulador para pruebas, siga estos pasos:

1. En la sección del menú ADMINISTRACIÓN DE RECORRIDOS , haga clic en **[!UICONTROL Journeys]**. Se muestra la lista de recorridos.

2. Busque el recorrido que desea copiar y haga clic en el botón **Más acciones** (los tres puntos junto al nombre del recorrido) y haga clic en **Copiar en entorno limitado**.

   ![](assets/copy-sandbox1.png)

   La variable **Copiar en entorno limitado** se muestra.

   ![](assets/copy-sandbox2.png)

3. Seleccione el **Espacio aislado de Target** en el campo desplegable . Solo están disponibles los entornos limitados de su organización de IMS.

4. Consulte la **Objetos dependientes** para obtener más información. Esta es la lista de objetos asociados que se utilizan en el recorrido. Esta lista muestra el nombre, el tipo de objeto y el Journey Optimizer ID interno.

5. Haga clic en el **Copiar** , en la esquina superior derecha, para comenzar a copiar el recorrido en el simulador para pruebas de destino.

   ![](assets/copy-sandbox3.png)

   Se inicia el proceso de copia y se muestra el progreso de cada objeto individual. El proceso de copia varía según la complejidad del recorrido y la cantidad de objetos que deben copiarse. Si se encuentra un error, se muestra un mensaje para el objeto relacionado.

   ![](assets/copy-sandbox4.png)

6. Una vez completada la copia, haga clic en **Cerrar**.

7. Acceda al simulador para pruebas de destino y realice una comprobación exhaustiva de todos los objetos copiados.

## Proceso de copia y limitaciones {#limitations}

No garantizamos que todos los elementos vinculados se copien en el entorno limitado de destino. Le recomendamos encarecidamente que realice una comprobación exhaustiva. Identifique cualquier objeto que pueda faltar y créelo manualmente antes de publicar el recorrido.

Se copian los siguientes objetos:

* Segmento

   Un segmento solo se puede copiar una vez de un simulador para pruebas a otro. Las solicitudes posteriores para copiar el segmento darán error. Una vez copiado un segmento, no se puede editar en el entorno limitado de destino.

* Esquema

   Se copian los esquemas utilizados en este recorrido.

* Mensaje

   Los mensajes físicos utilizados en el recorrido (ya sea correo electrónico o mensajes push). Los campos utilizados para la personalización en el mensaje no se comprueban para que estén completos. Los bloques de contenido no se copian.

* Recorrido: detalles del lienzo

   Representación del recorrido en el lienzo, incluidos los objetos del recorrido como condiciones, acciones, eventos, segmentos de lectura, etc. La actividad Jump se excluye de la copia.

* Evento

   Se copian los eventos y los detalles de evento utilizados en el recorrido.

* Acción

   Se copian las acciones y los detalles de acción utilizados en el recorrido.

Los ajustes preestablecidos no se copian. El sistema selecciona automáticamente la coincidencia más cercana posible en el entorno limitado de destino, según el tipo de mensaje y el nombre del ajuste preestablecido. Si no se encuentran ajustes preestablecidos en el entorno limitado de destino, la copia preestablecida fallará. Esto significa que la copia del mensaje también fallará porque un mensaje requiere un ajuste preestablecido para estar disponible para la configuración. En este caso, es necesario crear al menos un ajuste preestablecido para que funcione la copia para el canal correcto del mensaje.

