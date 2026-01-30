---
title: Caso de uso sobre la toma de decisiones
description: Aprenda a crear decisiones y utilizarlas en experimentos de contenido con el canal de experiencia basado en código
feature: Decisioning, Use Cases
topic: Integrations
role: User
level: Intermediate, Experienced
exl-id: 09770df2-c514-4217-a71b-e31c248df543
version: Journey Orchestration
source-git-commit: 21de0b9616c414db204a3eafebc6a8184028a1e1
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 4%

---

# Uso de decisiones en una experiencia basada en código con un experimento de contenido {#experience-decisioning-uc}

Este caso de uso presenta todos los pasos necesarios para utilizar Decisioning con el canal basado en código [!DNL Journey Optimizer].

➡️ [Descubra un caso de uso en vídeo](#video)

>[!NOTE]
>
>La capacidad heredada de Administración de decisiones no es compatible con el canal de experiencia basado en código.

En este ejemplo, no está seguro de si una fórmula de clasificación específica tendrá un mejor rendimiento que las prioridades de oferta preasignadas. Para medir cuál ofrece el mejor rendimiento para la audiencia objetivo, cree una campaña con [Experimento de contenido](../content-management/content-experiment.md) en la que defina dos tratamientos de entrega:

* El primer tratamiento usa **priority** como método de clasificación.
* El segundo tratamiento usa **una fórmula** como método de clasificación.

>[!NOTE]
>
>Para obtener detalles de implementación sobre pruebas y deduplicación al utilizar la toma de decisiones en experiencias basadas en código, consulte [esta página](../code-based/code-based-decisioning-implementations.md).

## Creación de estrategias de selección

En primer lugar, debe crear dos estrategias de selección: una con prioridad como método de clasificación y otra con una fórmula como método de clasificación.

>[!NOTE]
>
>También puede crear elementos de decisión únicos sin tener que ejecutar una estrategia de selección. Se aplicará la prioridad establecida para cada elemento.

### Creación de una estrategia con prioridad

Para crear la primera estrategia de selección con la prioridad como método de clasificación, siga los pasos a continuación.

1. Cree un elemento de decisión. [Descubra cómo](items.md)

1. Establezca la **[!UICONTROL Prioridad]** del elemento de decisión en comparación con otros. Si un perfil cumple los requisitos para varios elementos, una prioridad mayor otorga al elemento prioridad sobre otros.

   ![](assets/exd-uc-item-priority.png){width="90%"}

   >[!NOTE]
   >
   >La prioridad es un tipo de datos entero. Todos los atributos que son tipos de datos enteros deben contener valores enteros (sin decimales).

1. Establezca la idoneidad del elemento de decisión:

   * Defina audiencias o reglas para restringir el elemento solo a perfiles específicos. [Más información](items.md#eligibility)

   * Defina las reglas de límite para definir el número máximo de veces que se puede presentar una oferta. [Más información](items.md#capping)

1. Si es necesario, repita los pasos anteriores para crear elementos de decisión adicionales.

1. Cree una **colección** en la que se incluirán los elementos de decisión. [Más información](collections.md)

1. Cree una [estrategia de selección](selection-strategies.md#create-selection-strategy) y seleccione la [colección](collections.md) que contiene las ofertas que deben tenerse en cuenta.

1. [Elija el método de clasificación](#select-ranking-method) que se usará para seleccionar la mejor oferta para cada perfil. En este caso, seleccione **[!UICONTROL Prioridad de ofertas]**: si varias ofertas cumplen los requisitos para esta estrategia, el motor de decisión utiliza el valor establecido como **[!UICONTROL Prioridad]** en las ofertas. [Más información](selection-strategies.md#offer-priority)

   ![](assets/exd-uc-strategy-priority.png){width="90%"}

### Crear otra estrategia con una fórmula

Para crear la segunda estrategia de selección con seleccione una fórmula como método de clasificación, siga los pasos a continuación.

1. Cree un elemento de decisión. [Descubra cómo](items.md)

   <!--Do you need to set the same **[!UICONTROL Priority]** as for the first decision item, or it won't be considered at all?-->

1. Establezca la idoneidad del elemento de decisión:

   * Defina audiencias o reglas para restringir el elemento solo a perfiles específicos. [Más información](items.md#eligibility)

   * Defina las reglas de límite para definir el número máximo de veces que se puede presentar una oferta. [Más información](items.md#capping)

1. Si es necesario, repita los pasos anteriores para crear elementos de decisión adicionales.

1. Cree una **colección** en la que se incluirán los elementos de decisión. [Más información](collections.md)

1. Cree una [estrategia de selección](selection-strategies.md#create-selection-strategy) y seleccione la [colección](collections.md) que contiene las ofertas que deben tenerse en cuenta.

1. [Elige el método de clasificación](#select-ranking-method) que quieras usar para seleccionar la mejor oferta para cada perfil. En este caso, seleccione **[!UICONTROL Fórmula]** para usar una puntuación calculada específica a fin de determinar qué oferta apta para entregar. [Más información](selection-strategies.md#ranking-formula)

   ![](assets/exd-uc-strategy-formula.png){width="90%"}

## Creación de una campaña de experiencia basada en código

Una vez configuradas las dos estrategias de selección, cree una campaña de experiencia basada en código en la que defina un tratamiento diferente para cada estrategia para comparar cuál de ellas tiene el mejor rendimiento.

1. Cree una campaña y seleccione la acción **[!UICONTROL Experiencia basada en código]**. [Más información](../code-based/create-code-based.md)

1. En la página de resumen de la campaña, haga clic en **[!UICONTROL Crear experimento]** para configurar su experimento de contenido. [Descubra cómo](../content-management/content-experiment.md)

   ![](assets/exd-uc-create-experiment.png){width="90%"}

1. En la página de resumen de la campaña, seleccione una configuración basada en código y haga clic en **[!UICONTROL Editar contenido]**.

   ![](assets/exd-uc-edit-cbe-content.png){width="90%"}

1. Desde la ventana de edición de contenido, para comenzar a personalizar **Tratamiento A**, haz clic en **[!UICONTROL Editar código]**.

   ![](assets/exd-uc-experiment-treatment-a.png){width="90%"}

1. En el [editor de código](../code-based/create-code-based.md#edit-code), seleccione **[!UICONTROL directiva de decisión]**, haga clic en **[!UICONTROL Agregar directiva de decisión]** y rellene los detalles de la decisión. [Más información](create-decision.md#add)

   ![](assets/decision-code-based-create.png){width="90%"}

1. En la sección **[!UICONTROL Secuencia de estrategia]**, haga clic en el botón **[!UICONTROL Agregar]** y elija **[!UICONTROL Estrategia de selección]**. [Más información](create-decision.md#select)

   ![](assets/decision-code-based-strategy-sequence.png){width="80%"}

   >[!NOTE]
   >
   >También puede seleccionar **[!UICONTROL elemento de decisión]** para agregar elementos individuales sin tener que ejecutar una estrategia de selección. Se aplicará la prioridad establecida para cada elemento.

1. Seleccione la primera estrategia que ha creado: la que tenga prioridad como método de clasificación.

   ![](assets/exd-uc-experiment-strategy-priority.png){width="90%"}

1. Guarde los cambios y haga clic en **[!UICONTROL Crear]**. La nueva decisión se agrega en **[!UICONTROL Directiva de decisión]**.

1. Haga clic en el botón **[!UICONTROL Insertar directiva]**. Se agrega el código correspondiente a la política de decisión. A continuación, agregue todos los atributos que desee al código, incluidos los atributos de perfil. [Más información](create-decision.md#create-decision)

   ![](assets/exd-uc-experiment-insert-policy.png){width="90%"}

1. Guarde los cambios.

1. Vuelva a la ventana de edición de contenido, seleccione el botón + para agregar **Tratamiento B**, selecciónelo y haga clic en **[!UICONTROL Editar código]**.

   ![](assets/exd-uc-experiment-treatment-b.png){width="90%"}

1. Repita los pasos 5 y 6 anteriores para crear otra política de decisión y seleccione la segunda estrategia de selección que ha creado: la que tiene la fórmula como método de clasificación. <!--Do you need to create exactly the same content to compare only the ranking method?-->

   ![](assets/exd-uc-experiment-strategy-formula.png){width="90%"}

1. Edite la política de decisión según desee (consulte los pasos 8 y 9 anteriores).

1. Guarde los cambios y [publique su campaña de experiencia basada en código](../code-based/publish-code-based.md).

Después de ejecutar el experimento, realiza un seguimiento del rendimiento de los tratamientos de campaña con el [informe de campaña de experimentación](../reports/campaign-global-report-cja-experimentation.md).<!-- and [report on decisioning](cja-reporting.md).--> Entonces puede interpretar los resultados de su experimento. [Descubra cómo](../content-management/get-started-experiment.md#interpret-results)

Si el resultado es concluyente:

* Puede dirigir el tratamiento con la clasificación con mejor rendimiento a todos sus clientes.
* O puede crear una nueva campaña utilizando la estrategia de selección en la que se replica el método de clasificación con mejor rendimiento.

## Vídeo práctico {#video}

Descubra un tutorial completo que muestra cómo utilizar Decisioning en una experiencia basada en código.

>[!VIDEO](https://video.tv.adobe.com/v/3451100/?learn=on&enablevpops)