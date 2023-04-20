---
solution: Journey Optimizer
product: journey optimizer
title: Copiar un recorrido en otro sandox
description: Aprenda a copiar un recorrido en otro sandox
feature: Journeys
topic: Content Management
role: User, Developer
level: Intermediate
keywords: entorno limitado, recorrido, copiar, entorno
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 20%

---

# Copia de un recorrido en otra zona protegida {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copia de un recorrido en otra zona protegida"
>abstract="Journey Optimizer permite copiar un recorrido completo de una zona protegida a otra. Por ejemplo, puede copiar un recorrido del entorno de zona protegida de fase en la zona protegida de producción. Además del propio recorrido, Journey Optimizer también copia la mayoría de los objetos de los que depende el recorrido."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Detalles de la zona protegida"
>abstract="Seleccione la zona protegida de destino en la que desea copiar el recorrido. Solo están disponibles las zonas protegidas de su organización IMS."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Detalles del objeto"
>abstract="Este es el recorrido que va a copiar."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Objetos dependientes"
>abstract="Esta es la lista de objetos asociados que se utilizan en el recorrido. Esta lista muestra el nombre, el tipo de objeto y el ID interno de Journey Optimizer."

Journey Optimizer permite copiar un recorrido completo de una zona protegida a otra. Por ejemplo, puede copiar un recorrido del entorno de entorno limitado de ensayo en el entorno limitado de producción. Además del propio recorrido, Journey Optimizer también copia la mayoría de los objetos de los que depende el recorrido: segmentos, superficies (es decir, ajustes preestablecidos), esquemas, eventos y acciones. Para obtener más información sobre los objetos copiados, consulte esta [sección](#limitations).

>[!CAUTION]
>
>No garantizamos que todos los elementos vinculados se copien en el entorno limitado de destino. Le recomendamos encarecidamente que realice una comprobación exhaustiva antes de publicar el recorrido. Esto le permitirá identificar cualquier objeto que pueda faltar.

Los objetos copiados en el entorno limitado de destino son únicos y no existe riesgo de sobrescribir los elementos existentes. Tanto el recorrido como cualquier mensaje dentro del recorrido se transfieren en modo borrador. Esto le permite llevar a cabo una validación exhaustiva antes de la publicación en el simulador para pruebas de destino. El proceso de copia solo copia los metadatos sobre el recorrido y los objetos de ese Recorrido. Como parte de este proceso, no se copian datos de perfiles o conjuntos de datos.

Para copiar un recorrido en otro simulador para pruebas, siga estos pasos:

1. En la sección del menú ADMINISTRACIÓN DE RECORRIDOS , haga clic en **[!UICONTROL Recorridos]**. Se muestra la lista de recorridos.

2. Busque el recorrido que desea copiar y haga clic en el botón **Más acciones** (los tres puntos junto al nombre del recorrido) y haga clic en **Copiar en entorno limitado**.

   ![](assets/copy-sandbox1.png)

   La variable **Copiar en entorno limitado** se muestra.

   ![](assets/copy-sandbox2.png)

3. Seleccione el **Espacio aislado de Target** en el campo desplegable . Solo están disponibles las zonas protegidas de su organización IMS.

4. Consulte la **Objetos dependientes** para obtener más información. Esta es la lista de objetos asociados que se utilizan en el recorrido. Esta lista muestra el nombre, el tipo de objeto y el ID interno de Journey Optimizer.

5. Haga clic en el **Copiar** , en la esquina superior derecha, para comenzar a copiar el recorrido en el simulador para pruebas de destino.

   ![](assets/copy-sandbox3.png)

   Se inicia el proceso de copia y se muestra el progreso de cada objeto individual. El proceso de copia varía según la complejidad del recorrido y la cantidad de objetos que deben copiarse. Si se encuentra un error, se muestra un mensaje para el objeto relacionado.

   ![](assets/copy-sandbox4.png)

6. Una vez completada la copia, haga clic en **Cerrar**.

7. Acceda al simulador para pruebas de destino y realice una comprobación exhaustiva de todos los objetos copiados.

## Proceso de copia y limitaciones {#limitations}

Es posible que no todos los elementos vinculados se copien en el entorno limitado de destino. Adobe recomienda encarecidamente que realice una comprobación exhaustiva. Identifique cualquier objeto que pueda faltar y créelo manualmente antes de publicar el recorrido.

Se copian los siguientes objetos:

* Segmento

   Un segmento solo se puede copiar una vez de un simulador para pruebas a otro. Una vez copiado un segmento, no se puede editar en el entorno limitado de destino.

* Esquema

   Se copian los esquemas utilizados en este recorrido.

* Mensaje

   Las actividades de acción del canal utilizadas en el recorrido. Los campos utilizados para la personalización en el mensaje no se comprueban para que estén completos. Los bloques de contenido no se copian.

* Recorrido: detalles del lienzo

   Representación del recorrido en el lienzo, incluidos los objetos del recorrido como condiciones, acciones, eventos, segmentos de lectura, etc. La actividad Jump se excluye de la copia.

* Evento

   Se copian los eventos y los detalles de evento utilizados en el recorrido.

* Acción

   Se copian las acciones y los detalles de acción utilizados en el recorrido.

Las superficies (es decir, los ajustes preestablecidos) no se copian. El sistema selecciona automáticamente la coincidencia más cercana posible en el entorno limitado de destino, según el tipo de mensaje y el nombre de superficie. Si no hay superficies encontradas en el simulador de pruebas de destino, la copia superficial fallará. Esto significa que la copia del mensaje también fallará porque un mensaje requiere que una superficie esté disponible para la configuración. En este caso, se debe crear al menos una superficie para que funcione la copia para el canal correcto del mensaje.

En el caso de esquemas, políticas de combinación y segmentos, la segunda vez que estos objetos intenten copiarse, solo se hará referencia a ellos. Se tratarán como objetos que ya existen y se copiarán de nuevo. Esto significa que estos objetos solo se pueden copiar una vez.

Transcurridos cinco minutos, Adobe Journey Optimizer puede hacer referencia a esquemas, políticas de combinación y segmentos sin que aparezca un error en el lienzo. Espere cinco minutos y estas referencias estarán disponibles.
