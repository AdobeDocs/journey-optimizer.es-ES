---
solution: Journey Optimizer
product: journey optimizer
title: Uso de datos de Adobe Experience Platform para las decisiones
description: Aprenda a utilizar los datos de Adobe Experience Platform para la toma de decisiones.
badge: label="Disponibilidad limitada" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expresión, editor
exl-id: 46d868b3-01d2-49fa-852b-8c2e2f54292f
source-git-commit: 42f231a9b0b34a63d1601dcae653462f6321caed
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 24%

---

# Uso de datos de Adobe Experience Platform para decisiones {#aep-data}

>[!CONTEXTUALHELP]
>id="ajo_exd_rules_dataset_lookup"
>title="Búsqueda de conjuntos de datos"
>abstract="El uso de datos de Adobe Experience Platform en las reglas de decisión permite definir criterios de idoneidad basados en atributos dinámicos, externos, lo que garantiza que los elementos de decisión solo se muestren cuando corresponda. Cree una asignación para definir cómo se une el conjunto de datos de Adobe Experience Platform con los datos de [!DNL Journey Optimizer]. Seleccione el conjunto de datos con los atributos que necesita y elija una clave de unión que exista tanto en los atributos del elemento de decisión como en el conjunto de datos."

>[!CONTEXTUALHELP]
>id="ajo_exd_formula_dataset_lookup"
>title="Búsqueda de conjuntos de datos"
>abstract="Las fórmulas de clasificación definen la prioridad de los elementos de decisión. Mediante atributos del conjunto de datos de [!DNL Adobe Experience Platform], puede ajustar dinámicamente la lógica de clasificación para reflejar las condiciones reales. Cree una asignación para definir cómo se une el conjunto de datos de Adobe Experience Platform con los datos de [!DNL Journey Optimizer]. Seleccione el conjunto de datos con los atributos que necesita y elija una clave de unión que exista tanto en los atributos del elemento de decisión como en el conjunto de datos"

>[!AVAILABILITY]
>
>Actualmente, esta función está disponible para todos los clientes como una versión de disponibilidad limitada.

[!DNL Journey Optimizer] le permite aprovechar los datos de [!DNL Adobe Experience Platform] para la toma de decisiones. Esto le permite ampliar la definición de los atributos de decisión a datos adicionales en conjuntos de datos para actualizaciones masivas que cambian periódicamente sin tener que actualizar manualmente los atributos de uno en uno. Por ejemplo, disponibilidad, tiempos de espera, etc.

Antes de empezar, los conjuntos de datos necesarios para la personalización de la búsqueda deben habilitarse primero para la búsqueda. Encontrará información detallada en esta sección: [Usar datos de Adobe Experience Platform](../data/lookup-aep-data.md).

## Mecanismos de protección y limitaciones {#guidelines}

Antes de empezar, tome nota de las siguientes restricciones y directrices:

* Una política de decisión puede hacer referencia a hasta 3 conjuntos de datos en total, en todas sus reglas de decisión y fórmulas de clasificación combinadas. Por ejemplo, si las reglas utilizan 2 conjuntos de datos, las fórmulas solo pueden utilizar 1 conjunto de datos adicional.
* Una regla de decisión puede utilizar 3 conjuntos de datos.
* Una fórmula de clasificación puede utilizar 3 conjuntos de datos.
* Cuando se evalúa una directiva de decisión, el sistema realiza hasta 1000 consultas de conjuntos de datos (búsquedas) en total. Cada asignación de conjunto de datos utilizada por un elemento de decisión se cuenta como una consulta. Ejemplo: Si un elemento de decisión utiliza 2 conjuntos de datos, la evaluación de esa oferta cuenta como 2 consultas hacia el límite de 1000 consultas.

## Aprovechamiento de datos de Adobe Experience Platform {#leverage-aep-data}

Una vez que un conjunto de datos está habilitado para la búsqueda, puede utilizar sus atributos para enriquecer la lógica de decisión con datos externos. Esto resulta especialmente útil para atributos que cambian con frecuencia, como la disponibilidad del producto o los precios en tiempo real.

Los atributos de los conjuntos de datos de Adobe Experience Platform se pueden utilizar en dos partes de la lógica de decisión:

* **Reglas de decisión**: defina si un elemento de decisión es elegible para mostrarse.
* **Fórmulas de clasificación**: dé prioridad a los elementos de decisión según los datos externos.

En las siguientes secciones se explica cómo utilizar los datos de Adobe Experience Platform en ambos contextos.

### Reglas de decisión {#rules}

El uso de datos de Adobe Experience Platform en reglas de decisión permite definir criterios de idoneidad basados en atributos externos dinámicos, lo que garantiza que los elementos de decisión solo se muestren cuando corresponda.

Por ejemplo, supongamos que un retailer en línea desea promocionar las recomendaciones de productos en función del inventario de la tienda local. Un producto solo debe ser apto para la recomendación si está disponible en la ubicación más cercana. Se carga en Adobe Experience Platform un conjunto de datos que contiene actualizaciones diarias del inventario. La lógica de regla comprueba si el `inventory_count` de un producto determinado es mayor que 0 en la tienda preferida del cliente. Si es así, el elemento de decisión es elegible.

Para utilizar datos de Adobe Experience Platform en reglas de decisión, siga estos pasos:

1. Vaya al menú **[!UICONTROL Configuración de estrategia]** / **[!UICONTROL Reglas de decisión]** y seleccione **[!UICONTROL Crear regla con el conjunto de datos]**.

   ![](assets/exd-lookup-rule.png)

1. Haga clic en **[!UICONTROL Crear asignación]** para definir cómo se une el conjunto de datos de Adobe Experience Platform con los datos de [!DNL Journey Optimizer].

   * Seleccione el conjunto de datos con los atributos que necesite.
   * Elija una clave de unión (por ejemplo, ID de producto o ID de tienda) que exista tanto en los atributos del elemento de decisión como en el conjunto de datos.

   ![](assets/exd-lookup-mapping.png)

   >[!NOTE]
   >
   >Puede crear hasta 3 asignaciones por regla.

1. Haga clic en **[!UICONTROL Continuar]**. Ahora puede acceder a los atributos del conjunto de datos en el menú **[!UICONTROL Búsqueda de conjuntos de datos]** y utilizarlos en las condiciones de regla. [Aprenda a crear una regla de decisión](../experience-decisioning/rules.md#create)

   ![](assets/exd-lookup-menu.png)

### Fórmulas de clasificación {#ranking-formulas}

Las fórmulas de clasificación definen la prioridad de los elementos de decisión. Mediante [!DNL Adobe Experience Platform] atributos del conjunto de datos, puede ajustar dinámicamente la lógica de clasificación para reflejar las condiciones reales.

Por ejemplo, supongamos que una aerolínea utiliza una fórmula de clasificación para priorizar las ofertas de actualización. Si un cliente tiene un nivel de lealtad alto y la disponibilidad de puestos actual es baja (según un conjunto de datos actualizado cada hora), se le da una prioridad más alta. El conjunto de datos incluye campos como `flight_number`, `available_seats` y `loyalty_score`.

Para utilizar datos de Adobe Experience Platform en fórmulas de clasificación, siga estos pasos:

1. Cree o edite una fórmula de clasificación. En la sección **[!UICONTROL Búsqueda de conjuntos de datos]**, haga clic en **[!UICONTROL Crear asignación]**.

1. Defina la asignación del conjunto de datos:

   * Seleccione el conjunto de datos adecuado (por ejemplo, disponibilidad de puestos por vuelo).
   * Elija una clave de unión (por ejemplo, número de vuelo o ID de cliente) que exista tanto en los atributos del elemento de decisión como en el conjunto de datos.

   ![](assets/exd-lookup-formula-mapping.png)

   >[!NOTE]
   >
   >Puede crear hasta 3 asignaciones por fórmula de clasificación.

1. Utilice los campos del conjunto de datos para crear la fórmula de clasificación como de costumbre. [Aprenda a crear una fórmula de clasificación](ranking/ranking-formulas.md#create-ranking-formula)

   ![](assets/exd-lookup-formula-criteria.png)
