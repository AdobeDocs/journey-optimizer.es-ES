---
title: Fórmulas de clasificación
description: Obtenga información sobre cómo crear fórmulas para clasificar ofertas
feature: Ranking, Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 35d7488b-e7d8-402f-b337-28a0c869bff0
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/WycI0aO1o4KFH1gNieayuhpyNZuoVxL6zhGJBNOht8g
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1731
ht-degree: 5%

---

# Crear fórmulas de clasificación {#create-ranking-formulas}

**Las fórmulas de clasificación** le permiten definir reglas que determinan qué oferta se debe presentar primero, en lugar de tener en cuenta las puntuaciones de prioridad.

Para crear estas reglas, el generador de fórmulas de IA de **[!UICONTROL Adobe Journey Optimizer]** proporciona mayor flexibilidad y control en la clasificación de las ofertas. En lugar de depender únicamente de una prioridad de oferta estática, ahora puede definir fórmulas de clasificación personalizadas que combinen puntuaciones del modelo de IA, prioridades de oferta, atributos de perfil, atributos de oferta y señales contextuales a través de una interfaz guiada.

Este enfoque le permite ajustar dinámicamente la clasificación de la oferta en función de cualquier combinación de tendencia impulsada por IA, valor empresarial y contexto en tiempo real, lo que facilita la alineación de la toma de decisiones con los objetivos de marketing y las necesidades del cliente. El generador de fórmulas de IA admite fórmulas simples o avanzadas en función del control que desee aplicar.

Una vez creada una fórmula de clasificación, puede asignarla a una [estrategia de selección](../selection-strategies.md). Si se pueden presentar varias ofertas al utilizar esta estrategia de selección, el motor de decisión utilizará la fórmula seleccionada para calcular qué oferta se ofrece primero.

➡️ [Descubra esta funcionalidad en vídeo](#video)

## Mecanismos de protección y limitaciones {#ranking-guardrails}

Antes de crear fórmulas de clasificación, tenga en cuenta las siguientes restricciones:

* El generador de fórmulas de IA no admite [modelos de optimización personalizados](personalized-optimization-model.md) que usan métricas continuas.
* Cuando se utiliza un modelo de IA en una fórmula de clasificación, los datos no se reflejan en el informe [Tasa de conversión de tráfico controlado por modelo y en espera](../../reports/campaign-global-report-cja-code.md#conversion-rate).
* La profundidad de anidación en una fórmula de clasificación está limitada a 30 niveles, medidos por el recuento de `)` en la cadena de PQL.
* Una cadena de fórmula de clasificación puede tener hasta 8 KB para caracteres codificados con UTF-8 (8000 caracteres ASCII o 2000-4000 caracteres no ASCII).
* Los periodos retrospectivos no se admiten en fórmulas de clasificación (por ejemplo, eventos de experiencia del último mes). Los intentos de guardar estas fórmulas déclencheur un error.
* La optimización de fórmulas con tecnología de IA [1} se aplica solamente a las fórmulas de clasificación cuya expresión PQL basada en código es mayor que **2 KB** en tamaño codificado UTF-8; no se analizan las fórmulas más pequeñas.](#optimize)

## Crear la fórmula de clasificación y establecer las propiedades {#create-ranking-formula}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Crear fórmulas de clasificación"
>abstract="Las fórmulas le permiten definir reglas que determinarán qué elemento de decisión se debe presentar primero, en lugar de tener en cuenta las puntuaciones de prioridad del elemento. Una vez creada una fórmula de clasificación, puede asignarla a una estrategia de selección."

Para crear una fórmula de clasificación, siga los pasos a continuación.

1. Acceda al menú **[!UICONTROL Configuración de estrategia]** y, a continuación, seleccione la ficha **[!UICONTROL Fórmulas de clasificación]**. Se muestra la lista de fórmulas creadas anteriormente.

   ![](../assets/ranking-formulas-list.png)

1. Haga clic en **[!UICONTROL Crear fórmula]**.

1. Especifique el nombre de la fórmula y añada una descripción si lo desea.

   ![](../assets/create-formula.png){width="80%"}

1. Si lo desea, haga clic en **[!UICONTROL Seleccionar modelo de IA]** para establecer el modelo que se utilizará como referencia para generar la fórmula de clasificación.

   Cada vez que haga referencia a una puntuación de modelo al definir la fórmula a continuación, se utilizará el modelo de IA seleccionado.

1. Defina las condiciones que determinarán la puntuación de clasificación para los elementos de decisión coincidentes. Puede hacer lo siguiente:

   * Rellene la sección **[!UICONTROL Criterios]** con el [generador de fórmulas](#ranking-select-criteria), o
   * Haga clic en **[!UICONTROL Cambiar al editor de código]** para definir o restringir la lógica de clasificación con [PQL en el editor de código](#ranking-code-editor).

## Uso de datos de Adobe Experience Platform {#aep-data}

En la sección **[!UICONTROL Búsqueda de conjuntos de datos]**, puede usar datos de Adobe Experience Platform para ajustar dinámicamente la lógica de clasificación y reflejar las condiciones del mundo real.

Esto resulta especialmente útil para atributos que cambian con frecuencia, como la disponibilidad del producto o los precios en tiempo real. [Aprenda a utilizar los datos de Adobe Experience Platform para la toma de decisiones](../aep-data-exd.md)

![](../assets/ranking-formula-dataset.png)

## Definir criterios con el generador de fórmulas {#ranking-select-criteria}

Defina los **criterios** que determinarán la puntuación de clasificación para los elementos de decisión coincidentes.

Con una interfaz intuitiva, puede ajustar la toma de decisiones ajustando las puntuaciones de IA (tendencia), el valor de oferta (prioridad), las palancas contextuales y las tendencias de perfil externo (individualmente o en combinación) para optimizar cada interacción. <!--Whether you are maximizing revenue, promoting strategic offers, or balancing business goals with real-time context, the formula builder gives you total control in defining ranking strategies.-->

<!--![](../assets/ranking-formula-criteria.png){width="80%"}-->

1. Si es necesario, haga clic en **[!UICONTROL Cambiar al editor de código]** para agregar una expresión que utilice **sintaxis de PQL** junto con el generador de fórmulas. Esta opción complementa los campos de la interfaz de usuario en los pasos siguientes, por lo que puede combinar ambos enfoques en la misma fórmula de clasificación. Para obtener más información sobre cómo usar la sintaxis de PQL, consulte la [documentación específica](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=es). La sintaxis para los atributos del elemento de decisión y los ejemplos de copiar y pegar se proporcionan en la sección [Usar el editor de código](#ranking-code-editor).

   ![](../assets/ranking-formula-code-editor-button.png)

   >[!NOTE]
   >
   >Al cambiar al editor de código, se agrega la entrada basada en expresiones a los criterios y no se eliminan los demás campos de la interfaz de usuario.

1. En la sección **[!UICONTROL Criterio 1]**, especifique los elementos de decisión a los que desea aplicar una puntuación de clasificación haciendo lo siguiente:
   * seleccione un [atributo de elemento de decisión](../items.md#attributes)
   * seleccionar un operador lógico
   * agregar una condición coincidente: puede escribir un valor o seleccionar un atributo de perfil o [datos de contexto](../context-data.md)

   ![](../assets/ranking-formula-criterion-1.png){width="70%"}

1. De forma opcional, puede especificar elementos adicionales para restringir las condiciones de coincidencia para que los criterios sean verdaderos.

   ![](../assets/ranking-formula-addtional-conditions.png){width="80%"}

   Por ejemplo, ha definido el criterio 1, como el atributo personalizado *Weather* *Equals* para la condición *warm*. Además, puede agregar otra condición como, por ejemplo, si se cumple la primera condición y si la temperatura supera los 75 grados en el momento de la solicitud, el criterio 1 es verdadero.<!--Add a screenshot with the example-->

1. Cree una expresión que asigne una puntuación de clasificación a los elementos de decisión que cumplan la condición definida anteriormente. Puede hacer referencia a cualquiera de las siguientes opciones:

   * la puntuación que salió del modelo de IA que seleccionó opcionalmente en la sección **[!UICONTROL Detalles]** [anterior](#create-ranking-formula);
   * prioridad del elemento de decisión, que es un valor asignado manualmente al [crear un elemento de decisión](../items.md#attributes); <!--If a profile qualifies for multiple decision items, a higher priority grants the item precedence over others.-->
   * cualquier atributo que pueda residir en el perfil, como cualquier puntuación de tendencia derivada externamente;
   * un valor estático que se puede asignar en formato libre;
   * cualquier combinación de todos los anteriores.

   ![](../assets/ranking-formula-expression.png){width="70%"}

   >[!NOTE]
   >
   >Haga clic en el icono situado junto al campo para añadir variables predefinidas.

1. Haga clic en **[!UICONTROL Agregar criterio]** para agregar uno o más criterios tantas veces como sea necesario. La lógica es la siguiente:
   * Si el primer criterio es verdadero para un elemento de decisión determinado, tiene prioridad sobre los siguientes.
   * Si no es true, el motor de decisión pasa al segundo criterio, y así sucesivamente.

1. En el último campo, se puede generar una expresión que se asigna a todos los elementos de decisión que no cumplan los criterios anteriores.

   ![](../assets/ranking-formula-criteria-not-met.png){width="70%"}

   +++Ejemplo de fórmula de clasificación

   ![](../assets/ranking-formula-example.png){width="80%"}

   Si la región del elemento de decisión (atributo personalizado) es igual a la etiqueta geográfica del perfil (atributo de perfil), la puntuación de clasificación expresada aquí (que es una combinación de la prioridad del elemento de decisión, la puntuación del modelo de IA y un valor estático) se aplicará a todos los elementos de decisión que cumplan esa condición.

   +++

1. Cuando la fórmula esté lista, haga clic en **[!UICONTROL Crear]**.

Ahora puede acceder a la fórmula de clasificación desde la lista para ver sus detalles y editarla o eliminarla. Está listo para usarse en una [estrategia de selección](../selection-strategies.md) para clasificar los elementos de decisión elegibles.

## Defina los criterios mediante el editor de código {#ranking-code-editor}

Use **[!UICONTROL Cambiar al editor de código]** cuando quiera escribir o editar la lógica de clasificación como expresión **PQL**.

![](../assets/ranking-formula-switch.png)

>[!NOTE]
>
>Esta acción evitará que vuelva a la vista predeterminada del generador para esta fórmula.

Puede aprovechar atributos de perfil, [datos de contexto](../context-data.md) y [atributos de elemento de decisión](../items.md#attributes).

Por ejemplo, desea aumentar la prioridad de todas las ofertas con el atributo &quot;hot&quot; si el tiempo real es caluroso. Para ello, se pasó **contextData.weather=hot** en la llamada de toma de decisiones.

![](../assets/ranking-formula-code-editor.png){width="80%"}

Para aprovechar los atributos relacionados con los elementos de decisión en las fórmulas, asegúrese de seguir la sintaxis correcta en el código de la fórmula de clasificación. Expanda cada sección para obtener más información:

+++Aprovechamiento de atributos estándar de elementos de decisión

![](../assets/formula-attribute.png)

+++

+++Aprovechamiento de atributos personalizados de elementos de decisión

![](../assets/formula-attribute-custom.png)

+++

Puede crear muchas fórmulas de clasificación basadas en código diferentes según sus necesidades. A continuación se muestran algunos ejemplos.

+++Aumente las ofertas con ciertos atributos de oferta según el atributo del perfil

Si el perfil vive en la ciudad correspondiente a la oferta, duplique la prioridad para todas las ofertas de esa ciudad.

**Fórmula de clasificación:**

```
if( offer.characteristics.get("city") = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

+++

+++Ampliar ofertas en las que la fecha de finalización sea en menos de 24 horas a partir de ahora

**Fórmula de clasificación:**

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

+++

+++Aumente las ofertas en función de la tendencia de los clientes a comprar el producto ofrecido

Puede aumentar la puntuación de una oferta en función de una puntuación de tendencia del cliente.

En este ejemplo, el inquilino de instancia es *_salesvelocity* y el esquema de perfil contiene un rango de puntuaciones almacenadas en una matriz:

![](../assets/ranking-example-schema.png)

Teniendo en cuenta esto, para un perfil como:

```
{"_salesvelocity": {"individualScoring": [
                    {"core": {
                            "category":"insurance",
                            "propensityScore": 96.9
                        }},
                    {"core": {
                            "category":"personalLoan",
                            "propensityScore": 45.3
                        }},
                    {"core": {
                            "category":"creditCard",
                            "propensityScore": 78.1
                        }}
                    ]}
}
```

+++

+++Aumente las ofertas en función del código postal y los ingresos anuales de un perfil

En este ejemplo, el sistema siempre intenta mostrar primero una oferta que coincida con el código postal y vuelve a una oferta general si no se encuentra ninguna coincidencia, evitando mostrar ofertas destinadas a otros códigos postales.

```pql
if( offer._luma.offerDetails.zipCode = _luma.zipCode,luma.annualIncome / 1000 + 10000, if( not offer.luma.offerDetails.zipCode,_luma.annualIncome / 1000, -9999) )
```

Lo que hace la fórmula:

* Si la oferta tiene el mismo código postal que el usuario, asígnele una puntuación muy alta para que se seleccione primero.
* Si la oferta no tiene código postal (se trata de una oferta general), asígnele una puntuación normal basada en los ingresos del usuario.
* Si la oferta tiene un código postal diferente al del usuario, asígnele una puntuación muy baja para que no esté seleccionada.

+++

+++Ampliar ofertas según los datos de contexto

[!DNL Journey Optimizer] le permite impulsar ciertas ofertas según los datos de contexto que se pasan en la llamada. Por ejemplo, si se pasa `contextData.weather=hot`, se debe aumentar la prioridad de todas las ofertas con `attribute=hot`.

>[!NOTE]
>
>Para obtener información detallada sobre cómo pasar datos de contexto <!-- using the **Edge Decisioning** and **Decisioning** APIs-->, consulte [esta sección](../context-data.md).

Tenga en cuenta que al usar la API **Decisioning**, los datos de contexto se agregan al elemento de perfil en el cuerpo de la solicitud, como en el ejemplo siguiente:

```
"xdm:profiles": [
{
    "xdm:identityMap": {
        "crmid": [
            {
            "xdm:id": "CRMID1"
            }
        ]
    },
    "xdm:contextData": [
        {
            "@type":"_xdm.context.additionalParameters;version=1",
            "xdm:data":{
                "xdm:weather":"hot"
            }
        }
    ]
    
}],
```

+++

## Optimización de fórmula con tecnología de IA {#optimize}

[!DNL Journey Optimizer] puede analizar automáticamente las fórmulas de clasificación y sugerir simplificaciones que preserven la lógica original. Solo se admiten las fórmulas cuya expresión PQL sea mayor que **2 KB** (con codificación UTF-8); no se analizan las expresiones más pequeñas. Cuando se encuentra una simplificación, aparece un indicador rojo junto al nombre de la fórmula en la lista.

![](../assets/ranking-formula-ai.png)

>[!NOTE]
>
>La optimización de fórmulas con tecnología de IA se basa en las mismas capacidades de IA generativa que **AI Assistant** y usa los mismos controles de acceso. A los usuarios se les debe otorgar el permiso **[!UICONTROL Generar contenido]** en el recurso **[!UICONTROL Asistente de IA]**. Para obtener más información, consulte [Acceder al asistente de IA](../../content-management/gs-generative.md#generative-access).

Para optimizar una fórmula de clasificación:

1. En la lista de fórmulas de clasificación, haga clic en el icono de indicador rojo junto al nombre de la fórmula.

1. Se abre la ventana **[!UICONTROL Optimize]**, que muestra la expresión PQL original junto con la versión sugerida por IA.

   ![](../assets/ranking-formula-ai-details.png)

1. Para comprobar que ambas expresiones producen resultados de clasificación idénticos, haga clic en **[!UICONTROL Descargar análisis de optimización (TSV)]** para descargar un archivo que muestre cómo se evalúan los perfiles simulados en relación con cada versión.

1. Una vez que esté satisfecho, haga clic en **[!UICONTROL Aplicar]** para reemplazar la expresión original por la optimizada.

## Vídeo práctico {#video}

Aprenda a utilizar el Generador de fórmulas de IA en Adobe Journey Optimizer para crear estrategias de clasificación de ofertas personalizadas.

>[!VIDEO](https://video.tv.adobe.com/v/3464446/?learn=on&enablevpops)
