---
title: Recorrido fórmulas de clasificación de mediación
description: Aprenda a crear fórmulas para clasificar los recorridos para la mediación, de modo que se seleccione el mejor recorrido por perfil en función de las reglas y el contexto.
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 2%

---

# Utilizar fórmulas para clasificar recorridos {#journey-ranking-formulas}

>[!AVAILABILITY]
>
>Actualmente, esta función se encuentra en disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

[!DNL Adobe Journey Optimizer] le ayuda a controlar qué recorridos puede introducir un perfil cuando cumplen los requisitos para obtener más de lo que permite el sistema. Para ello, puede usar [conjuntos de reglas](rule-sets.md) para definir límites en la entrada de recorrido o la concurrencia. Cuando un perfil es elegible para recibir más recorridos de los que permite el límite, la prioridad asignada a cada recorrido determina qué recorridos se seleccionan.

En lugar de usar la prioridad, también puede usar **fórmulas de clasificación** para ajustar dinámicamente la clasificación de los recorridos en función de los atributos de recorrido, los atributos de perfil o las puntuaciones del modelo de IA.

Las fórmulas proporcionan más flexibilidad que la prioridad estática. Por ejemplo, puede aumentar un recorrido para los miembros de fidelidad de oro.

<!--
>[!NOTE]
>
>Journey ranking formulas follow the same guardrails as decisioning ranking formulas (nesting depth, rule string size). [Learn more about Decisioning guardrails & limitations](../experience-decisioning/decisioning-guardrails.md#ranking-formulas).-->

## Crear fórmula de clasificación {#create-journey-ranking-formula}

Para crear una fórmula de clasificación para sus recorridos, siga los pasos a continuación.

1. Acceda a la sección **[!UICONTROL Clasificación de orquestaciones]** y, a continuación, seleccione la pestaña **[!UICONTROL Fórmulas de clasificación]**. Se muestra la lista de fórmulas creadas anteriormente.

1. Haga clic en **[!UICONTROL Crear fórmula]**.

1. Especifique el nombre de la fórmula y añada una descripción si lo desea.

   ![Panel de detalles de la fórmula con campos de nombre y descripción](assets/journey-formula-details.png){width="80%"}


   >[!NOTE]
   >
   >El objeto de clasificación es la entidad a la que se aplica la fórmula de clasificación. De manera predeterminada, el objeto de clasificación está establecido en **[!UICONTROL Recorrido]**.

   <!--
    Selecting a formula entity specifies which type of item—such as journeys or other entities—the ranking formula will apply to. This determines the context in which the formula operates, allowing you to define rules that influence how those items are ranked.-->

1. Si lo desea, haga clic en **[!UICONTROL Seleccionar modelo de IA]** para establecer el modelo que se utilizará como referencia para generar la fórmula de clasificación.

<!--
    >[!NOTE]
    >
    >[Personalized optimization models](../experience-decisioning/ranking/personalized-optimization-model.md) using continuous metrics are not supported with the AI formula builder.

    Every time you refer to a model score when defining your formula below, the AI model that you selected will be used. [Learn more on AI models](../experience-decisioning/ranking/ai-models.md)-->

1. En la sección **[!UICONTROL Criterio 1]**, especifique a qué recorridos desea aplicar una puntuación de clasificación haciendo lo siguiente:

   * seleccionar un [atributo de recorrido](../building-journeys/journey-properties.md) (como el nombre del recorrido, las etiquetas, la prioridad u otras propiedades de recorrido);
   * seleccionar un operador lógico;
   * añadir una condición de coincidencia: puede escribir o seleccionar un valor, o elegir un atributo de perfil.

   ![Sección de criterios 1 con atributo de recorrido, operador y condición de coincidencia](assets/journey-formula-criterion-1.png){width="70%"}

1. De forma opcional, puede especificar elementos adicionales para restringir las condiciones de coincidencia para que los criterios sean verdaderos.

   ![Condición adicional para perfeccionar los criterios de coincidencia](assets/journey-formula-additional-condition.png){width="70%"}

   Por ejemplo, ha definido *Criterio 1* como *Recorrido de etiquetas* que contiene *Fidelidad*. Además, puede agregar otra condición como, por ejemplo, si el *estado de fidelidad* es igual a *Oro*, entonces el *criterio 1* es verdadero.

1. Cree una expresión que asigne una puntuación de clasificación a los recorridos que cumplan la condición definida anteriormente. Puede hacer referencia a cualquiera de las siguientes opciones:
   * una variable:
      * la prioridad de recorrido, que es un valor manual asignado al recorrido al [crear un recorrido](../building-journeys/journey-gs.md);
      * la puntuación que salió del modelo de IA que seleccionó anteriormente de forma opcional;
   * un atributo:
      * cualquier atributo que pueda residir en el perfil, como cualquier puntuación de tendencia derivada externamente;
      * un atributo de recorrido;
   * un valor estático que se puede asignar en formato libre;
   * una combinación de todos los anteriores.

   ![Generador de expresiones para asignar una puntuación de clasificación mediante variables, atributos o valores estáticos](assets/journey-formula-expression.png){width="70%"}

1. Haga clic en **[!UICONTROL Agregar criterio]** para agregar uno o más criterios tantas veces como sea necesario. La lógica es la siguiente:
   * Si el primer criterio es verdadero para un elemento de decisión determinado, tiene prioridad sobre los siguientes.
   * Si no es true, el motor de decisión pasa al segundo criterio, y así sucesivamente.

1. Una vez definidos todos los criterios, en el último campo, se puede generar una expresión que se asignará a todos los recorridos que no cumplan los criterios anteriores.

   ![Campo de expresión para recorridos que no cumplen ningún criterio](assets/journey-formula-criteria-not-met.png){width="70%"}

1. Haga clic en **[!UICONTROL Crear]** para completar la fórmula de clasificación.

Ahora puede seleccionar esta fórmula de la lista para ver sus detalles y editarla o eliminarla. A continuación, está disponible al configurar un conjunto de reglas. [Descubra cómo](#assign-formula-to-ruleset)

### Ejemplos de fórmulas de clasificación {#journey-ranking-formula-example}

Consideremos los ejemplos siguientes.

+++Ejemplo 1: Utilice la prioridad de recorrido o la puntuación de IA basada en las etiquetas de recorrido

![Fórmula de clasificación: la etiqueta de marketing usa la prioridad de recorrido](assets/journey-formula-ex-1.png){width="60%"}

Si el recorrido tiene la etiqueta &quot;Marketing&quot;, la puntuación de clasificación es la prioridad de recorrido.

![Fórmula de clasificación: la etiqueta de promoción usa la puntuación del modelo de IA](assets/journey-formula-ex-2.png){width="60%"}

Si el recorrido tiene la etiqueta &quot;Promoción&quot;, la puntuación de clasificación es la puntuación del modelo de IA.

+++

+++Ejemplo 2: Impulsar los recorridos de lealtad por estado de perfil


![Fórmula de clasificación: la etiqueta de fidelización con estado Oro usa la prioridad de recorrido más 5](assets/journey-formula-ex-3.png){width="60%"}

Si el recorrido tiene la etiqueta &quot;Lealtad&quot; y el estado de lealtad del perfil es Oro, la puntuación de clasificación que se utiliza es la prioridad de recorrido más 5.

![Fórmula de clasificación: la etiqueta de fidelización con estado Plata usa la prioridad de recorrido más 2](assets/journey-formula-ex-4.png){width="60%"}

Si el recorrido tiene la etiqueta &quot;Lealtad&quot; y el estado de lealtad del perfil es Plata, la puntuación de clasificación es la prioridad de recorrido más 2.

Si no se cumple ninguna de las condiciones anteriores, la puntuación de clasificación utilizada es la prioridad de recorrido.

+++

### Utilizar el editor de código {#journey-ranking-formula-code-editor}

Para expresar fórmulas de clasificación en **sintaxis de PQL**, cambie al editor de código con el botón específico en la parte superior derecha de la pantalla. Para obtener más información sobre cómo usar la sintaxis de PQL, consulte la [documentación específica](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=es).

>[!CAUTION]
>
>Esta acción evitará que vuelva a la vista predeterminada del generador para esta fórmula.

A continuación, puede aprovechar los atributos de recorrido, los atributos de perfil y los valores estáticos para crear una fórmula de clasificación.

<!--The code editor is similar to the one used in Decisioning ranking formulas. [Learn more](../experience-decisioning/ranking/ranking-formulas.md#ranking-code-editor)-->

## Asignar la fórmula a un conjunto de reglas {#assign-formula-to-ruleset}

Para utilizar una fórmula para clasificar los recorridos, debe asignarla a un conjunto de reglas.

>[!NOTE]
>
>Las fórmulas se asignan en el nivel del conjunto de reglas, no en recorridos individuales.

1. En el menú **[!UICONTROL Reglas de negocio]**, cree un conjunto de reglas que desee usar para el arbitraje de recorrido. [Descubra cómo](rule-sets.md#Create)

1. Asegúrese de seleccionar el dominio **[!UICONTROL Recorrido]**.

   ![Propiedades del conjunto de reglas con dominio de Recorrido seleccionado](assets/journey-formula-rule-set-journey.png){width="60%"}

1. En las propiedades del conjunto de reglas, establezca el **[!UICONTROL método de clasificación]** en **[!UICONTROL Fórmula]** (en lugar de la **[!UICONTROL Prioridad]** predeterminada).

1. Seleccione la fórmula de clasificación que ha creado en la lista desplegable.

   ![Conjunto de reglas con fórmula de clasificación seleccionado de la lista desplegable](assets/journey-rule-set-formula.png){width="60%"}

1. Cree las reglas de límite de recorrido que desee agregar al conjunto de reglas. [Descubra cómo](journey-capping.md#create-rule)

1. Guarde el conjunto de reglas.

Ahora la fórmula se asigna al conjunto de reglas. A continuación, puede aplicar ese conjunto de reglas a los recorridos.

## Aplicación del conjunto de reglas a un recorrido {#assign-rule-set-to-journey}

Para asignar el conjunto de reglas a un recorrido, siga los pasos a continuación.

1. Cree o abra el recorrido al que desee asignar el conjunto de reglas. [Obtenga información sobre cómo crear un recorrido](../building-journeys/journey-gs.md)

1. En las propiedades del recorrido, seleccione el conjunto de reglas en la lista desplegable.  [Más información](journey-capping.md#apply-capping).

   >[!NOTE]
   >
   >Solo se puede aplicar un conjunto de reglas a un recorrido a la vez.

1. Guarde el recorrido.

Todos los recorridos que utilicen este conjunto de reglas se clasificarán con la fórmula seleccionada cuando se aplique el límite.

Para supervisar el rendimiento de los conjuntos de reglas y las fórmulas de clasificación, consulte la sección [Límite de Recorridos y conflictos](../reports/channel-report-cja.md#rule-sets) en el informe Información general.

<!--
## Reporting {#reporting}

Reporting for journey arbitration helps you understand how rule sets and ranking formulas perform:

* **Exclusions** – Whether journeys were excluded from users and which rule set (and reason) prevented entry.
* **Rule set performance** – For each rule set, metrics such as journey enters, journey exclusions, journey engagement, and other optimization metrics.
* **Cross-journey view** – Time-based view of profiles across journeys (e.g. journey enters, failures, exclusions) to see the impact of capping and ranking.

Use these reports to validate that your formulas and caps are behaving as intended and to tune ranking logic over time.-->

