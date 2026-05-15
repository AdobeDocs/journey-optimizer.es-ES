---
title: Aprovechamiento de fragmentos en políticas de decisión
description: Aprenda a aprovechar los fragmentos en las políticas de decisión
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 70f64348-092b-4350-91dc-72c3c07300f9
TQID: https://experienceleague.adobe.com/5Vpngi03UnC9YPlB5tdTRcd0NoT7iglH2pRDkmeZKOg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 2225d3c796e777f459bebc35a5c33ce1a0635f42
workflow-type: tm+mt
source-wordcount: 752
ht-degree: 1%

---

# Aprovechamiento de fragmentos en políticas de decisión {#fragments}

Si la política de decisión contiene elementos de decisión, incluidos fragmentos, puede aprovechar estos fragmentos al crear un mensaje, dentro de la política de decisión. [Más información sobre fragmentos](../content-management/fragments.md)

>[!AVAILABILITY]
>
>Esta característica está disponible para los canales de **experiencia basada en código** y **correo electrónico**.

Por ejemplo, supongamos que desea mostrar contenido diferente para varios modelos de dispositivos móviles. Agregue los fragmentos especificados, cada uno perteneciente a un modelo de teléfono diferente, al elemento de decisión que esté utilizando en la directiva de decisión. [Más información](items.md#attributes).

![Sección de fragmentos de un elemento de decisión que muestra referencias de fragmento y claves de ubicación.](assets/item-fragments.png){width=70%}

Una vez finalizado, puede utilizar cualquiera de los siguientes métodos:

>[!BEGINTABS]

>[!TAB Inserte directamente el código]

Simplemente copie y pegue el bloque de código siguiente en el código de la política de decisión. Reemplazar `variable` por el ID de fragmento y `placement` por la clave de referencia de fragmento:

```handlebars
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable required=false}}
```

>[!TAB Siga los pasos detallados]

1. Vaya a las **[!UICONTROL funciones de ayuda]** y agregue la función **Permitir** `{% let variable = expression %} {{variable}}` al panel de código, donde puede declarar la variable para el fragmento.

   ![Editor de código de directiva de decisión que muestra la función Permitir ayuda agregada al panel de código.](assets/decision-let-function.png)

1. Use la función **Map** > **Get** `{%= get(map, string) %}` para generar su expresión. El mapa es el fragmento al que se hace referencia en el elemento de decisión. La cadena puede ser el modelo de dispositivo que especificó en el elemento de decisión como **[!UICONTROL clave de referencia de fragmento]**.

   Se han usado las funciones ![Map y Get para hacer referencia al mapa de fragmento y a la clave de referencia de fragmento.](assets/decision-map-function.png)

1. También puede utilizar un atributo contextual que contenga este ID de modelo de dispositivo.

   ![Atributo contextual seleccionado para el identificador del modelo del dispositivo.](assets/decision-contextual-attribute.png)

1. Agregue la variable que eligió para el fragmento como ID de este.

   ![Variable de ID de fragmento establecida a partir del elemento de decisión en el código de directiva de decisión.](assets/decision-fragment-id.png)

>[!ENDTABS]

El ID de fragmento y la clave de referencia se seleccionarán de la sección **[!UICONTROL Fragmentos]** del elemento de decisión.

>[!WARNING]
>
>Si la clave del fragmento es incorrecta o si el contenido del fragmento no es válido, el procesamiento puede fallar y provocar un error en la llamada de Edge.
>
>Para evitar errores cuando un fragmento no está disponible temporalmente, se utiliza el indicador `required=false` para que se omita el fragmento en su lugar. [Más información](#temporary-unavailable-fragments)

## Uso y protecciones {#fragments-guardrails}

### Simulación de fragmentos de contenido y expresión en correos electrónicos {#simulate-content-expression-fragments}

Para el canal **Email**, los fragmentos de expresión asociados con un elemento de decisión se muestran correctamente cuando **[!UICONTROL envía la prueba]** o cuando se activa la campaña. Sin embargo, **[!UICONTROL Simular contenido]** no muestra el fragmento de expresión del elemento de decisión.

### Fragmentos visuales y elementos de decisión en correos electrónicos {#visual-fragments-decision-items}

No puede asignar un **[!UICONTROL fragmento visual]** a un elemento de decisión, solo se admiten **fragmentos de expresión** en este contexto.

### Elemento de decisión y atributos de contexto {#decision-item-context-attributes}

Los atributos de elemento de decisión y los atributos contextuales no son compatibles de forma predeterminada en [!DNL Journey Optimizer] fragmentos. Sin embargo, puede utilizar variables globales en su lugar, como se describe a continuación.

Supongamos que desea utilizar la variable *sport* en el fragmento.

1. Cite esta variable en el fragmento, por ejemplo:

   ```text
   Elevate your practice with new {{sport}} gear!
   ```

1. Defina la variable con la función **Let** dentro del bloque de directivas de decisión. En el ejemplo siguiente, *sport* se define con el atributo de elemento de decisión:

   ```handlebars
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

### Validación de contenido de fragmento de elemento de decisión {#fragment-content-validation}

* Debido a la naturaleza dinámica de estos fragmentos, cuando se utilizan en una campaña, la validación de mensajes durante la creación del contenido de la campaña se omite para los fragmentos a los que se hace referencia en los elementos de decisión.

* La validación del contenido del fragmento solo se produce durante la creación y publicación del fragmento.

* Para los fragmentos de expresiones de tipo JSON, el contenido se valida sintácticamente al guardar el fragmento. Los errores de validación se muestran como alertas.

En tiempo de ejecución, se valida el contenido de la campaña (incluido el contenido de fragmento de los elementos de decisión). En caso de error de validación, la campaña no se procesará.

### Se omiten los fragmentos temporalmente no disponibles {#temporary-unavailable-fragments}

Cuando los recorridos o campañas hacen referencia a fragmentos adjuntos a elementos de decisión, puede haber breves retrasos de sincronización antes de que los fragmentos actualizados estén disponibles en Edge.

Para evitar errores cuando un fragmento no está disponible temporalmente, los fragmentos ahora tienen el indicador `required` establecido en `false` de forma predeterminada para que se omitan en lugar de provocar el error del recorrido o la campaña.

Esto significa que si el fragmento no está disponible temporalmente en Edge, simplemente se ignora. Si el fragmento está disponible, se procesa normalmente.

**Ejemplo**

Si la directiva de decisión cumple los requisitos para dos ofertas y cada una tiene un fragmento (por ejemplo, &quot;20 % de descuento&quot; y &quot;30 % de descuento&quot;) y el segundo fragmento no está disponible temporalmente, con `required=false` el sistema procesa la oferta disponible (20 % de descuento) y omite el otro fragmento (30 % de descuento) en lugar de realizar un error en el recorrido o la campaña. Esto mejora la fiabilidad cuando el contenido aún se está sincronizando.

>[!NOTE]
>
>Puede seguir marcando un fragmento como obligatorio si establece el indicador `required` en `true`. Sin embargo, si un fragmento falta temporalmente, puede provocar un error en el procesamiento del recorrido o de la campaña.
