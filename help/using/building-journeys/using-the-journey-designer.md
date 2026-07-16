---
solution: Journey Optimizer
product: journey optimizer
title: Diseño de un recorrido
description: Aprenda a diseñar su recorrido
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: diseño, lienzo, recorrido, interfaz, arrastrar, soltar
exl-id: 1998f6fc-60fd-4038-8669-39cd55bc02d1
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Mn8oR-jsUTbkXoohAgCulA-SBY8xRVy75z6H7j9ETvE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
  - id: c3f67a94-f1ff-4f5e-bf6f-bc22405930a3
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: e57d1da4-32c2-4cc6-945c-9feb219156ff
  - id: ebd64fe4-362a-4a1c-9476-b2573ed12a95
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2b5248d7f364eb3c9505d2e844f4b8ab9dce1dac
workflow-type: tm+mt
source-wordcount: 2469
ht-degree: 2%

---

# Diseño de un recorrido {#design-your-journey}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a utilizar el lienzo y la paleta del diseñador de recorridos para arrastrar y soltar eventos, orquestación y actividades de acción en un flujo secuenciado que genere su recorrido.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] incluye un lienzo de orquestación omnicanal que permite a los especialistas en marketing armonizar el alcance de marketing con la participación individual del cliente. La interfaz de usuario de le permite arrastrar y soltar fácilmente actividades de la paleta en el lienzo para crear su recorrido. Tenga en cuenta que también puede hacer doble clic en una actividad para agregarla al lienzo en el siguiente paso disponible.

Los eventos, la orquestación y las actividades de acción tienen un papel y un lugar específicos en el proceso. Las actividades se secuencian: cuando finaliza una actividad, el flujo continúa, procesa la siguiente actividad, etc.

## Introducción al diseño de recorridos {#gs-journey-design}

La **paleta** se encuentra en el lado izquierdo de la pantalla. Todas las actividades disponibles se han clasificado en varias categorías: [Eventos](#jo-event), [Orquestación](#jo-orch) y [Acciones](#jo-actions). Puede expandir o contraer las diferentes categorías haciendo clic en su nombre. Para utilizar una actividad en el recorrido, arrástrela y suéltela desde la paleta al lienzo.

Al iniciar un nuevo recorrido, se ocultan los elementos que no se pueden soltar en el lienzo como primer paso. Esto se refiere a todas las acciones, la actividad de la condición, la espera y la reacción.

![Interfaz del diseñador de recorrido con panel de paleta, lienzo y propiedades](assets/journey38.png)

El icono **[!UICONTROL Filtrar elementos]** de la esquina superior izquierda le permite mostrar los siguientes filtros:

* **Mostrar solo los elementos disponibles**: oculta o muestra los elementos no disponibles en la paleta, por ejemplo los eventos que utilizan un área de nombres diferente a la utilizada en el recorrido. De forma predeterminada, los elementos no disponibles están ocultos. Si decide mostrarlos, aparecerán atenuados. No obstante, no es posible mostrarlos.

* **Mostrar solo los elementos recientes**: este filtro le permite mostrar solo los últimos cinco eventos y acciones utilizados, además de los predeterminados. Esto es específico de cada usuario. De forma predeterminada, se muestran todos los elementos.

También puede usar el campo **[!UICONTROL Buscar]**. Solo se filtran los eventos y las acciones.

**canvas** es la zona central del diseñador de recorridos. Es en esta zona donde puede soltar sus actividades y configurarlas. Haga clic en una actividad del lienzo para configurarla. Se abrirá el panel de configuración de actividad en el lado derecho.

![Lienzo de Recorrido con el panel de configuración de actividad abierto a la derecha](assets/journey39.png)

La **barra de herramientas**, ubicada en la esquina superior derecha del lienzo, le permite mostrar/ocultar la cuadrícula, acercar/alejar y descargar una captura de pantalla del lienzo. Consulte esta [sección](../building-journeys/journey-properties.md#timeout_and_error).

<!--and show/hide timeout and error paths-->

![barra de herramientas de Recorrido con controles de zoom, cuadrícula y captura de pantalla](assets/toolbar.png){width="70%"}

El **panel de configuración de actividad** aparece al hacer clic en una actividad de la paleta. Rellene los campos obligatorios. Haga clic en el icono **[!UICONTROL Eliminar]** para eliminar la actividad. Haga clic en **[!UICONTROL Cancelar]** para cancelar las modificaciones o en **[!UICONTROL Aceptar]** para confirmar. Para eliminar actividades, también puede seleccionar una actividad (o varias) y pulsar la tecla de retroceso. Si pulsa la tecla Esc, se cerrará el panel de configuración de actividad.

De forma predeterminada, los campos de solo lectura están ocultos. Para mostrar campos de solo lectura, haga clic en el icono **Mostrar campos de solo lectura** en la parte superior izquierda del panel de configuración de la actividad. Esta configuración se aplica a todas las actividades de todos los recorridos.

![Panel de configuración de actividad con la opción Mostrar campos de solo lectura](assets/journey59bis.png)

Según el estado del recorrido, puede realizar diferentes acciones en el recorrido mediante los botones disponibles en la esquina superior derecha: **[!UICONTROL Publicar]**, **[!UICONTROL Duplicar]**, **[!UICONTROL Eliminar]**, **[!UICONTROL Modo de prueba]**, **[!UICONTROL Administrar el acceso]**, **[!UICONTROL Alertas]**. Estos botones aparecen cuando no se ha seleccionado ninguna actividad. Algunos botones aparecerán en contexto. El botón de registro del modo de prueba aparece cuando se activa el modo de prueba.

![Botones de acción de Recorrido: Publicar, Duplicar, Eliminar, Modo de prueba, Administrar acceso, Alertas](assets/journey41.png)

## nueva experiencia de interfaz de recorrido {#canvas-capabilities}

Hay disponible una **nueva interfaz de usuario** para el lienzo de recorrido, diseñada para adaptarse a los casos de uso más complejos:

* **Rendimiento**: administra recorridos grandes con muchos pasos y ramas de forma eficaz.
* **Diseño automático**: organiza automáticamente las actividades para mejorar la legibilidad.
* **Creación guiada**: proporciona una experiencia de creación estructurada que le ayudará a crear recorridos con facilidad y eficacia.

![](assets/journey-new-canvas.png)

Para cambiar a la nueva experiencia, haz clic en el botón **[!UICONTROL Nueva experiencia]** en el lienzo del recorrido. Una vez cambiado, este ajuste se guarda en el nivel de recorrido, por lo que el recorrido se abrirá en la nueva experiencia de forma predeterminada en las visitas posteriores. Para volver, haz clic en el botón **[!UICONTROL Experiencia antigua]**.

![](assets/journey-new-experience-switch.png)


## Inicie el recorrido {#start-your-journey}

Al diseñar el recorrido, la primera pregunta que debe hacerse es cómo entran los perfiles en el recorrido.

Hay dos posibilidades:

1. **Empieza con un evento**: cuando un recorrido está configurado para recibir eventos, los usuarios entran al recorrido **unitariamente** en tiempo real. Los mensajes incluidos en su recorrido se envían a la persona que está entrando en el recorrido en ese momento. [Más información sobre los eventos](../event/about-events.md)

1. **Empiece con una audiencia de lectura**: puede configurar su recorrido para que escuche [!DNL Adobe Experience Platform] audiencias. En este caso, todas las personas que pertenecen a la audiencia especificada entran en el recorrido. Los mensajes incluidos en su recorrido se envían a las personas que pertenecen a la audiencia. Más información sobre [leer audiencia](read-audience.md). Para obtener más información sobre cómo generar y segmentar audiencias en Journey Optimizer, consulte [esta sección](../audience/about-audiences.md).

## Defina los pasos siguientes{#define-next-steps}

Después del primer evento o de la lectura de audiencias, puede combinar las distintas actividades para crear sus escenarios de canales cruzados de varios pasos. Elija, en la paleta, los pasos que necesite.

### Eventos{#jo-event}

Los eventos son el déclencheur de un recorrido personalizado, como una compra en línea. Una vez que alguien entra en un recorrido, se mueve como un individuo, y no dos individuos se mueven a la misma velocidad o a lo largo del mismo camino.

Cuando se inicia el recorrido con un evento, el recorrido se activa cuando se recibe el evento. Cada persona del recorrido sigue, individualmente, los siguientes pasos definidos en el recorrido.

Puede agregar **varios eventos** en el recorrido, siempre que utilicen el mismo espacio de nombres. Los eventos se configuran de antemano. [Más información sobre los eventos de recorrido](about-journey-activities.md#event-activities)

También puede agregar un evento **Reaction** después de un mensaje para reaccionar a los datos de seguimiento relacionados con el mensaje. Esto le permite, por ejemplo, enviar otro mensaje si el individuo abrió el mensaje anterior o hizo clic dentro de él. [Más información sobre los eventos de reacción](reaction-events.md).

Utilice la actividad de evento **Calificación de audiencias** para hacer que los individuos entren o avancen en un recorrido según las [!DNL Adobe Experience Platform] entradas y salidas de la audiencia. Puede hacer que todos los clientes nuevos de plata entren en un recorrido y envíen mensajes personalizados. Obtenga más información en esta [sección](audience-qualification-events.md).

### Orquestación{#jo-orch}

Las actividades de orquestación son condiciones diferentes que ayudan a determinar el siguiente paso del recorrido.

En las actividades de orquestación, use la actividad **Leer audiencia** para configurar el recorrido y escuchar una audiencia [!DNL Adobe Experience Platform]. [Más información sobre la actividad Leer audiencia](read-audience.md).

Use **Fragmentos de Recorrido** para insertar conjuntos reutilizables de nodos de recorrido pregenerados directamente en el lienzo. Los fragmentos ayudan a los equipos a mantener la coherencia y avanzar más rápido al evitar reconstruir la misma lógica, como las comprobaciones de elegibilidad, el enrutamiento de canales o las secuencias de bienvenida, desde cero. [Más información sobre los fragmentos de Recorrido](journey-fragments.md).

Las demás actividades le permiten agregar condiciones al recorrido para definir varias rutas, establecer un tiempo de espera antes de ejecutar la siguiente actividad o finalizar el recorrido. [Más información sobre las actividades de orquestación](about-journey-activities.md#orchestration-activities).

### Acciones{#jo-actions}

Las acciones son lo que desea que ocurra como resultado de algún tipo de déclencheur, como enviar un mensaje. Es el recorrido que el cliente experimenta. Podría ser un correo electrónico, un mensaje SMS o push, o una acción de terceros, como un mensaje de Slack.

Las actividades de acción de canal le permiten incluir un mensaje diseñado en [!DNL Journey Optimizer]. [Más información acerca de las actividades de acción del canal](journey-action.md)

Desde las actividades de acción, utilice acciones personalizadas para enviar mensajes con sistemas de terceros. [Más información sobre las acciones personalizadas](about-journey-activities.md#action-activities).

## Añadir rutas alternativas {#paths}

Puede definir una acción de reserva en caso de error o tiempo de espera para las siguientes actividades de recorrido: **[!UICONTROL Condición]** y **[!UICONTROL Acción]**.

Para agregar una acción de reserva para una actividad, seleccione el cuadro **[!UICONTROL Agregar una ruta de acceso alternativa en caso de tiempo de espera o error]** en las propiedades de la actividad: se agrega otra ruta de acceso después de la actividad. Los usuarios administradores definen la duración del tiempo de espera en [propiedades de recorrido](../building-journeys/journey-properties.md). Por ejemplo, si un correo electrónico tarda demasiado en enviarse o presenta un error, puede decidir enviar una notificación push.

![Agregar una ruta alternativa en caso de tiempo de espera u opción de error](assets/journey42.png)

Varias actividades (evento, acción, espera) permiten agregar varias rutas después de ellas. Para ello, coloque el cursor en la actividad y haga clic en el símbolo &quot;+&quot;. Solo se pueden configurar actividades de evento y espera en paralelo. Si se configuran varios eventos en paralelo, la ruta elegida será la del primer evento que se produzca.

Al escuchar un evento, le recomendamos que no espere al evento indefinidamente. No es obligatorio, solo es una práctica recomendada. Si desea escuchar uno o varios eventos solo durante un tiempo determinado, colocará uno o varios eventos y una actividad de espera en paralelo. Consulte [esta sección](../building-journeys/general-events.md#events-specific-time).

Para eliminar la ruta, coloque el cursor sobre ella y haga clic en el icono **[!UICONTROL Eliminar ruta]**.

![Eliminar icono de ruta de acceso para quitar una ruta de acceso alternativa](assets/journey42ter.png)

En el lienzo, cuando se desconectan dos actividades, se muestra una advertencia. Coloque el cursor en el icono de advertencia para mostrar el mensaje de error. Para solucionar el problema, simplemente mueva la actividad desconectada y conéctela a la actividad anterior.

![Icono de advertencia que muestra actividades desconectadas en el lienzo](assets/canvas-disconnected.png)

## Copiar y pegar actividades {#copy-paste}

Puede copiar una o varias actividades de un recorrido y pegarlas en el mismo recorrido o en uno diferente. Esto le permite ahorrar tiempo si desea reutilizar numerosas actividades que ya se han configurado en un recorrido anterior.

**Notas importantes**

* Puede copiar/pegar en diferentes pestañas y navegadores. Solo puede copiar/pegar actividades dentro de la misma instancia.
* No puede copiar/pegar un evento si el recorrido de destino tiene un evento que utiliza un área de nombres diferente.
* Las actividades pegadas pueden hacer referencia a datos que no existen en el recorrido de destino, por ejemplo, si copia o pega en diferentes zonas protegidas. Compruebe siempre la existencia de errores y realice los ajustes necesarios.
* Tenga en cuenta que no puede deshacer una acción. Para eliminar las actividades pegadas, deberá seleccionarlas y eliminarlas. Por lo tanto, asegúrese de seleccionar solo las actividades que necesita antes de copiarlas.
* Puede copiar actividades de cualquier recorrido, incluso las que estén en solo lectura.
* Puede seleccionar cualquier actividad, incluso las que no estén vinculadas. Las actividades vinculadas permanecerán vinculadas después de pegarse.

Estos son los pasos para copiar/pegar actividades:

1. Abra un recorrido.
1. Seleccione las actividades que desee copiar moviendo el ratón mientras hace clic en. También puede hacer clic en cada actividad mientras presiona la tecla **Ctrl/Comando**. Use **Ctrl/Comando + A** si desea seleccionar todas las actividades.
   ![Seleccionar varias actividades en el recorrido para copiarlas](assets/copy-paste1.png)
1. Presione **Ctrl/Comando + C**.
Si solo desea copiar una actividad, puede hacer clic en ella y usar el icono **Copiar** en la parte superior izquierda del panel de configuración de la actividad.
   ![Icono de copiar en el panel de configuración de la actividad](assets/copy-paste2.png)
1. En cualquier recorrido, presione **Ctrl/Comando + V** para pegar las actividades sin vincularlas a un nodo existente. Las actividades pegadas se colocan en el mismo orden. Después de pegarlas, las actividades permanecen seleccionadas para que pueda moverlas fácilmente. También puede colocar el cursor en un marcador de posición vacío y presionar **Ctrl/Comando + V**. Las actividades pegadas se vincularán al nodo.
   ![Actividades pegadas en lienzo de recorrido listas para conectarse](assets/copy-paste3.png)

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página presenta el lienzo del diseñador de recorridos de Journey Optimizer, donde se explica cómo crear recorridos de varios pasos arrastrando y soltando eventos, orquestación y actividades de acción desde la paleta.

**Intenciones:**

* Navegue por la interfaz del diseñador de recorridos (paleta, lienzo, barra de herramientas, panel de configuración de actividad)
* Agregar eventos, actividades de orquestación y actividades de acción a un lienzo de recorrido
* Configurar una ruta alternativa de reserva para las actividades Condición y Acción en tiempo de espera o error
* Copiar y pegar actividades dentro del mismo recorrido o en distintos recorridos de la misma instancia
* Iniciar un recorrido con un déclencheur de eventos o un punto de entrada de audiencia de lectura

**Glosario:**

* **Paleta**: el panel izquierdo del diseñador de recorrido que enumera todos los eventos, orquestaciones y actividades de acción disponibles para arrastrar y soltar en el lienzo *(específico del producto)*
* **Lienzo**: área de diseño central del diseñador de recorrido donde se colocan, conectan y configuran las actividades *(específico del producto)*
* **Panel de configuración de actividad**: El panel derecho que se abre cuando se selecciona una actividad en el lienzo y se usa para rellenar la configuración de actividad *(específica del producto)*
* **Fragmentos de Recorrido**: conjuntos reutilizables de nodos de recorrido pregenerados que se pueden insertar directamente en el lienzo para evitar la reconstrucción de la lógica común *(específica del producto)*
* **Evento de reacción**: una actividad de evento colocada después de un mensaje para bifurcar el recorrido en función de las interacciones de seguimiento del destinatario (abrir, hacer clic) *(específico del producto)*

**Protecciones:**

* Las acciones, condiciones, actividades de espera y eventos de reacción no pueden colocarse como el primer paso en un nuevo recorrido.
* Copiar/pegar solo se admite en la misma instancia; no se admite copiar/pegar en varias instancias.
* No puede copiar/pegar un evento en un recorrido de destino que utilice un área de nombres diferente.
* Las actividades pegadas desde una zona protegida diferente pueden hacer referencia a datos que no existen en el recorrido de destino.
* Solo se pueden configurar actividades de evento y de espera en paralelo; otros tipos de actividades no se pueden ejecutar en paralelo.
* Las rutas alternativas (tiempo de espera/error de reserva) solo están disponibles para las actividades Condición y Acción.

**Terminología:**

* Nombre canónico: Recorrido Designer — Acrónimo: none — variantes: lienzo recorrido, lienzo orquestación
* Sinónimos: &quot;paleta&quot; = &quot;panel de actividad&quot;; &quot;lienzo&quot; = &quot;área de diseño&quot;
* No confunda: &quot;events&quot; (entrada o ramificación del recorrido de déclencheur) ≠ &quot;actions&quot; (qué sucede con el cliente, por ejemplo, enviar un mensaje)

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Cómo ingresan los perfiles a un recorrido?** — Los perfiles se introducen de forma unitaria en tiempo real cuando se recibe un evento configurado o en lote cuando una actividad Leer audiencia déclencheur el recorrido.
* **Q: ¿Puedo agregar varios eventos a un recorrido?** — Sí, se pueden añadir varios eventos siempre que todos utilicen la misma área de nombres.
* **Q: ¿Cómo defino una reserva cuando falla una acción?** — En las propiedades de la actividad, habilite la opción &quot;Añadir una ruta alternativa en caso de tiempo de espera o error&quot; para agregar una ruta de reserva después de la actividad.
* **Q: ¿Puedo copiar actividades desde un recorrido de solo lectura?** — Sí, puede copiar actividades desde cualquier recorrido independientemente de su estado, pero solo puede pegar dentro de la misma instancia.
* **Q: ¿Qué es un fragmento de Recorrido?** — Un conjunto reutilizable de nodos de recorrido creados previamente (por ejemplo, comprobaciones de idoneidad o secuencias de bienvenida) que se pueden insertar directamente en el lienzo para evitar la reconstrucción de la lógica común desde cero.

+++
