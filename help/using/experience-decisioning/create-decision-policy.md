---
title: Crear políticas de decisiones
description: Obtenga información sobre cómo crear políticas de decisiones
feature: Decisioning
topic: Integrations
role: User
level: Experienced
version: Journey Orchestration
exl-id: e7a89354-28ea-431f-a15d-a8c18946d266
source-git-commit: 743165991c3f4d351cd6ab15e94ece0309c8e82a
workflow-type: tm+mt
source-wordcount: '2108'
ht-degree: 6%

---

# Creación de políticas de decisión {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="Definición del número de elementos que desea devolver"
>abstract="Seleccione el número de elementos de decisión que desea que se devuelvan. Por ejemplo, si selecciona 2, se presentarán las dos mejores ofertas aptas para la configuración actual."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="Selección de una reserva"
>abstract="Un elemento de reserva se muestra al usuario cuando no se cumple ninguna de las estrategias de selección definidas para esa política de decisión."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="¿Qué es una estrategia?"
>abstract="La secuencia de la estrategia de selección determina qué estrategia se evaluará primero. Se requiere al menos una estrategia. Los elementos de decisión de las estrategias combinadas se evaluarán juntos."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Creación de estrategias"

Para presentar la mejor oferta dinámica y experiencia a sus clientes, agregue una política de decisión al contenido de una campaña o recorrido y, a continuación, configure los elementos que desea devolver y la estrategia de selección que desea utilizar. Para ello, siga los pasos a continuación:

1. [Agregar una política de decisión](#add)
1. [Configurar la directiva de decisión](#configure): agregue un nombre y especifique el número de elementos que se devolverán para el canal de correo electrónico.
1. [Configurar una secuencia de estrategia](#strategy): seleccione los elementos que desea devolver con la directiva de decisión.
1. [Seleccionar ofertas de reserva](#fallback) (opcional): seleccione los elementos que desea mostrar si no se cumplen los requisitos para los elementos o las estrategias de selección.
1. [Revisar y guardar](#review) la estrategia de selección
1. [Asignar una ubicación](#placement) (canal de correo electrónico)

>[!AVAILABILITY]
>
>Las directivas de decisión están disponibles para todos los clientes para los canales **Experiencia basada en código**, **Notificación push** y SMS.
>
>La toma de decisiones del canal de correo electrónico está disponible en disponibilidad limitada. Para solicitar acceso, póngase en contacto con su representante de Adobe. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

## Agregar una política de decisión {#add}

Para agregar una directiva de decisión al mensaje, abre un recorrido o una campaña y selecciona una [acción del canal](../building-journeys/journeys-message.md).

Edite el contenido del mensaje y examine las pestañas siguientes para obtener más información sobre cómo añadir la política de decisión en función del canal seleccionado.

>[!BEGINTABS]

>[!TAB Experiencia basada en código]

Para las experiencias basadas en código, puede agregar una nueva directiva de decisión mediante el **editor de código** o el menú **Toma de decisiones** disponible en el panel de propiedades.

+++Añadir una política de decisión desde el editor de código

1. Abra el editor de código con el botón **[!UICONTROL Editar código]**.

1. Vaya al menú **[!UICONTROL Directiva de decisión]** y haga clic en el botón **[!UICONTROL Agregar directiva de decisión]**.

   ![](assets/decision-policy-add-code-editor.png)

+++

+++Agregar una directiva de decisión desde el menú Decisiones

1. Haga clic en el icono ![](assets/do-no-localize/decisioning-icon.png) del panel de propiedades para obtener acceso al menú **[!UICONTROL Decisioning]**.

1. Haga clic en el botón **[!UICONTROL Agregar directiva de decisión]**.

   ![](assets/decision-policy-add-code.png)

+++

>[!TAB Correo electrónico]

1. Alterne la opción **[!UICONTROL Enable Decisioning]**.

   ![](assets/decision-policy-enable.png)

   >[!IMPORTANT]
   >
   >Al habilitar la toma de decisiones, se borra el contenido de correo electrónico existente. Si ya ha diseñado el correo electrónico, asegúrese de guardar el contenido como una plantilla de antemano.

1. Agregue una nueva directiva de decisión mediante el **editor de personalización** o el menú **Toma de decisiones** disponible en el Diseñador de correo electrónico.

   +++Añadir una política de decisión desde el editor de Personalization

   1. Abra el editor de personalización mediante el icono ![](assets/do-no-localize/editor-icon.svg) disponible en el campo de la línea de asunto o en cualquier campo del cuerpo del correo electrónico donde pueda agregar personalización.

   1. Vaya al menú **[!UICONTROL Políticas de decisión]** y haga clic en el botón **[!UICONTROL Agregar política de decisión]**.

      ![](assets/decision-policy-add-email-editor.png)

   +++

   +++Agregar una directiva de decisión desde el menú Decisiones

   1. Abra la Designer de correo electrónico y seleccione cualquier componente de la estructura de correo electrónico.

   1. Haga clic en el icono ![](assets/do-no-localize/decisioning-icon.png) del panel de propiedades para obtener acceso al menú **[!UICONTROL Decisioning]**.

   1. Haga clic en el botón **[!UICONTROL Agregar nueva directiva]**.

      ![](assets/decision-policy-add-email-add.png)

   >[!NOTE]
   >
   >El **[!UICONTROL resultado de reutilización de decisión]** le permite reutilizar una directiva de decisión que ya se ha creado en este correo electrónico.

>[!TAB SMS]

Para SMS, puede agregar una nueva directiva de decisión mediante el **editor de personalización** o el menú **Toma de decisiones** disponible en el panel de propiedades.

+++Añadir una política de decisión desde el editor de personalización

1. Abra el editor de personalización utilizando el icono ![](assets/do-no-localize/editor-icon.svg).
1. Vaya al menú **[!UICONTROL Políticas de decisión]** y haga clic en el botón **[!UICONTROL Agregar política de decisión]**.

   ![](assets/decision-policy-add-sms-editor.png)

+++

+++Agregar una directiva de decisión desde el menú Decisiones

1. Haga clic en el icono ![](assets/do-no-localize/decisioning-icon.png) del panel de propiedades para obtener acceso al menú **[!UICONTROL Decisioning]**.

1. Haga clic en el botón **[!UICONTROL Agregar directiva de decisión]**.

   ![](assets/decision-policy-add-sms.png)

>[!TAB Notificación push]

Para las notificaciones push, puede agregar una nueva directiva de decisión mediante el **editor de personalización** o el menú **Toma de decisiones** disponible en el panel de propiedades.

+++Añadir una política de decisión desde el editor de personalización

1. Abra el editor de personalización utilizando el icono ![](assets/do-no-localize/editor-icon.svg).
1. Vaya al menú **[!UICONTROL Políticas de decisión]** y haga clic en el botón **[!UICONTROL Agregar política de decisión]**.

   ![](assets/decision-policy-add-push.png)

+++

+++Agregar una directiva de decisión desde el menú Decisiones

1. Haga clic en el icono ![](assets/do-no-localize/decisioning-icon.png) del panel de propiedades para obtener acceso al menú **[!UICONTROL Decisioning]**.

1. Haga clic en el botón **[!UICONTROL Agregar directiva de decisión]**.

   ![](assets/decision-policy-add-push-menu.png)

>[!IMPORTANT]
>
>Experience Decisioning con notificaciones push requiere una versión específica de Mobile SDK. Antes de implementar esta característica, compruebe [las notas de la versión](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"} para identificar la versión requerida y asegúrese de haber actualizado según corresponda. También puede ver todas las versiones de SDK disponibles para su plataforma en [esta sección](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}.

>[!ENDTABS]

## Configurar la directiva de decisión {#configure}

Después de agregar una nueva política de decisión al contenido, se abre la pantalla de configuración de la política de decisión. Siga estos pasos para configurar la directiva de decisión:

1. Proporcione un nombre para la política de decisión y seleccione un catálogo (actualmente limitado al catálogo predeterminado de **[!UICONTROL Ofertas]**).

   ![](assets/decision-code-based-details.png)

1. El campo **[!UICONTROL Número de elementos]** le permite definir el número de elementos de decisión que se devolverán con la directiva de decisión. Por ejemplo, si selecciona 2, se presentarán las dos mejores ofertas aptas para la configuración actual.

   >[!NOTE]
   >
   >Esta opción solo está disponible para los canales de experiencia basados en código y correo electrónico. Para el resto de canales, solo se puede devolver 1 elemento de decisión por acción.

   Para devolver varios elementos para el canal de correo electrónico, debe agregar la directiva de decisión dentro de un componente **[!UICONTROL Repetir cuadrícula]**. Expanda la sección siguiente para obtener más detalles:

   +++Devolver varios elementos de decisión en correos electrónicos

   1. Arrastre un componente **[!UICONTROL Repetir cuadrícula]** en el correo electrónico y configúrelo como desee mediante el panel **[!UICONTROL Configuración]**.

      ![](assets/decision-policy-repeat.png)

   1. Haga clic en el icono **[!UICONTROL Decisioning]** en la barra de herramientas del lienzo o abra el panel **[!UICONTROL Decisioning]** y seleccione **[!UICONTROL Agregar directiva de decisión]**.

   1. Especifique el número de elementos que desea devolver en el campo **[!UICONTROL Número de elementos]** y, a continuación, configure la directiva de decisión como se documenta a continuación. El número máximo de elementos que puede seleccionar está limitado por el número de mosaicos definidos en el componente **[!UICONTROL Repetir cuadrícula]**.

   ![](assets/decision-policy-repeat-number.png)

   +++

1. Haga clic en **[!UICONTROL Next]**.

## Configurar una secuencia de estrategia {#strategy}

La sección **[!UICONTROL Secuencia de estrategia]** le permite seleccionar los elementos de decisión y configurar estrategias de selección para presentar con la directiva de decisión.

1. Haga clic en **[!UICONTROL Agregar]** y elija el tipo de objeto que desea incluir en la directiva:

   ![](assets/decision-code-based-strategy-sequence.png)

   * **[!UICONTROL Estrategia de selección]**: las estrategias de decisión aprovechan las colecciones asociadas con las restricciones de elegibilidad y los métodos de clasificación para determinar los elementos que se mostrarán. Puede seleccionar una o varias estrategias de selección existentes, o crear una nueva mediante el botón **[!UICONTROL Crear estrategia de selección]**. [Aprenda a crear estrategias de selección](selection-strategies.md)

   * **[!UICONTROL Elemento de decisión]**: seleccione elementos de decisión únicos sin tener que ejecutar una estrategia de selección. Solo puede seleccionar un elemento de decisión a la vez. Se aplicarán todas las restricciones de aceptación establecidas para el artículo.

   >[!NOTE]
   >
   >Una política de decisión admite hasta 10 estrategias de selección y elementos de decisión combinados. [Más información sobre las limitaciones y protecciones de decisiones](gs-experience-decisioning.md#guardrails)

1. Al agregar varios elementos de decisión o estrategias, se evaluarán en un orden específico. El primer objeto añadido a la secuencia se evaluará primero, y así sucesivamente. Para cambiar la secuencia predeterminada, arrastre y suelte los objetos o los grupos para reordenarlos como desee. Expanda la sección siguiente para obtener más detalles.

   +++Administrar el orden de evaluación en una política de decisión

   Una vez que haya agregado elementos de decisión y estrategias de selección a la directiva, puede organizar su orden para determinar el orden de evaluación y combinar estrategias de selección para evaluarlos juntos.

   El **orden secuencial** en el que se evaluarán los elementos y las estrategias se indica con números a la izquierda de cada objeto o grupo de objetos. Para mover la posición de una estrategia de selección (o un grupo de estrategias) dentro de la secuencia, arrástrela y suéltela en otra posición.

   ![](assets/decision-code-based-strategy-groups.png)

   >[!NOTE]
   >
   >Solo se pueden arrastrar y soltar estrategias de selección dentro de una secuencia. Para cambiar la posición de un elemento de decisión, debe eliminarlo y volver a agregarlo usando el botón **[!UICONTROL Agregar]** después de agregar los demás elementos que desea evaluar antes.

   También puede **combinar** múltiples estrategias de selección en grupos para que se evalúen juntos y no por separado. Para ello, haga clic en el botón **`+`** de una estrategia de selección para combinarlo con otra. También puede arrastrar y soltar una estrategia de selección en otra para agrupar las dos estrategias en un grupo.

   >[!NOTE]
   >
   >Los elementos de decisión no se pueden agrupar con otros elementos o estrategias de selección.

   Varias estrategias y su agrupación determinan la prioridad de las estrategias y la clasificación de las ofertas aptas. La primera estrategia tiene la máxima prioridad y las estrategias combinadas dentro del mismo grupo tienen la misma prioridad.

   Por ejemplo, tiene dos colecciones, una en la estrategia A y otra en la estrategia B. La solicitud es para que se devuelvan dos elementos de decisión. Digamos que hay dos ofertas elegibles de la estrategia A y tres ofertas elegibles de la estrategia B.

   * Si las dos estrategias están **sin combinar** o en orden secuencial (1 y 2), las dos ofertas principales elegibles de la primera estrategia se devolverán en la primera fila. Si no hay dos ofertas aptas para la primera estrategia, el motor de decisión pasará a la siguiente estrategia en secuencia para encontrar tantas ofertas que aún se necesitan y, finalmente, devolverá una reserva si es necesario.

     ![](assets/decision-code-based-consecutive-strategies.png)

   * Si las dos colecciones se **evalúan al mismo tiempo**, ya que hay dos ofertas elegibles de la estrategia A y tres ofertas elegibles de la estrategia B, las cinco ofertas se apilarán todas juntas en función del valor determinado por los métodos de clasificación respectivos. Se solicitan dos ofertas, por lo que se devolverán las dos ofertas aptas principales de estas cinco ofertas.

     ![](assets/decision-code-based-combined-strategies.png)

   **Ejemplo con varias estrategias**

   Veamos un ejemplo en el que tiene varias estrategias divididas en diferentes grupos. Usted definió tres estrategias. La Estrategia 1 y la Estrategia 2 se combinan en el Grupo 1 y la Estrategia 3 es independiente (Grupo 2). Las ofertas elegibles para cada estrategia y su prioridad (utilizadas en la evaluación de la función de clasificación) son las siguientes:

   * Grupo 1:
      * Estrategia 1 - (Oferta 1, Oferta 2, Oferta 3) - Prioridad 1
      * Estrategia 2 - (Oferta 3, Oferta 4, Oferta 5) - Prioridad 1

   * Grupo 2:
      * Estrategia 3 - (Oferta 5, Oferta 6) - Prioridad 0

   Las ofertas de estrategia de mayor prioridad se evalúan primero y se añaden a la lista de ofertas clasificadas.

   * **Iteración 1:**

     Las ofertas de Estrategia 1 y Estrategia 2 se evalúan juntas (Oferta 1, Oferta 2, Oferta 3, Oferta 4, Oferta 5). Digamos que el resultado es:

     Oferta 1 - 10
Oferta 2 - 20
Oferta 3 - 30 de Estrategia 1, 45 de Estrategia 2. Se tendrá en cuenta el más alto de ambos, por lo que se tienen en cuenta 45.
Oferta 4 - 40
Oferta 5 - 50

     Las ofertas clasificadas ahora son las siguientes: Oferta 5, Oferta 3, Oferta 4, Oferta 2, Oferta 1.

   * **Iteración 2:**

     Se evalúan las ofertas de Estrategia 3 (oferta 5, oferta 6). Digamos que el resultado es:

      * Oferta 5: no se evaluará porque ya existe en el resultado anterior.
      * Oferta 6 - 60

     Las ofertas clasificadas ahora son las siguientes: Oferta 5 , Oferta 3, Oferta 4, Oferta 2, Oferta 1, Oferta 6.

   +++

1. Cuando la estrategia de selección esté lista, haga clic en **[!UICONTROL Siguiente]**.

## Añadir ofertas de reserva {#fallback}

Una vez que haya seleccionado elementos de decisión o estrategias de selección, puede añadir ofertas de reserva para mostrar si ninguno de los elementos o estrategias de selección anteriores está cualificado.

Puede seleccionar cualquier elemento de la lista, que muestra todos los elementos de decisión creados en la zona protegida actual. Si no se califica ninguna estrategia de selección, la reserva se mostrará al usuario independientemente de las fechas y restricciones de elegibilidad aplicadas al elemento seleccionado<!--nor frequency capping when available - TO CLARIFY-->.

![](assets/decision-code-based-strategy-fallback.png)

>[!NOTE]
> Las retrospectivas son opcionales. Se puede seleccionar hasta el número de elementos solicitados. Si ninguno es elegible y no se establece ninguna reserva, no se mostrará nada.

## Revisar y guardar la directiva de decisión {#review}

Después de configurar una estrategia de selección y agregar ofertas de reserva, haga clic en **[!UICONTROL Siguiente]** para revisar y guardar la directiva de decisión y, a continuación, haga clic en **[!UICONTROL Crear]** para confirmar la creación de la directiva.

>[!IMPORTANT]
>
>Una vez creada la política de decisión, los cambios realizados en ella pueden tardar hasta 15 minutos en propagarse en todas las regiones de datos y hasta 30 minutos en el caso de Canadá. Esto incluye cambios como agregar un nuevo elemento de decisión a una colección, cambiar una regla de un elemento, cambiar el contenido de un elemento o actualizar una fórmula.

Puede editar o eliminar una directiva de decisión en cualquier momento mediante el botón de puntos suspensivos del editor de personalización o en el menú **[!UICONTROL Decisioning]** del panel de propiedades del componente.

>[!BEGINTABS]

>[!TAB Editar o eliminar una directiva del editor de personalización]

![](assets/decision-policy-edit.png)

>[!TAB Editar o eliminar una directiva del menú Decisioning]

![](assets/decision-policy-edit-properties.png)

>[!ENDTABS]

## Asignar una ubicación (correo electrónico) {#placement}

Para los correos electrónicos, debe definir una ubicación para el componente asociado a la política de decisión. Para ello, haga clic en el botón **[!UICONTROL Decisioning]** del panel de propiedades del componente y seleccione **[!UICONTROL Asignar ubicación]**. [Aprenda a trabajar con ubicaciones](../experience-decisioning/placements.md)

![](assets/decision-policy-rail.png)

## Próximos pasos {#next-steps}

Ahora que sabe cómo crear una directiva de decisión, está listo para usarlo en [!DNL Journey Optimizer] canales para entregar ofertas.

➡️ [Aprenda a utilizar las directivas de decisión en los mensajes](../experience-decisioning/use-decision-policy.md)
