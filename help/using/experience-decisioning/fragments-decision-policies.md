---
title: Aprovechamiento de fragmentos en políticas de decisión
description: Aprenda a aprovechar los fragmentos en las políticas de decisión
feature: Decisioning
topic: Integrations
role: User
level: Experienced
source-git-commit: 083545ff7b2dc5ce45ef3766321fdf12e1b96c5c
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 1%

---


# Aprovechamiento de fragmentos en políticas de decisión {#fragments}

Si la política de decisión contiene elementos de decisión, incluidos fragmentos, puede aprovechar estos fragmentos en el código de la política de decisión. [Más información sobre fragmentos](../content-management/fragments.md)

>[!AVAILABILITY]
>
>Actualmente, esta funcionalidad solo está disponible para el canal de **experiencia basada en código** y para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

Por ejemplo, supongamos que desea mostrar contenido diferente para varios modelos de dispositivos móviles. Asegúrese de agregar los fragmentos correspondientes a esos dispositivos al elemento de decisión que está utilizando en la directiva de decisión. [Más información](items.md#attributes).

![](assets/item-fragments.png){width=70%}

Una vez finalizado, puede utilizar cualquiera de los siguientes métodos:

>[!BEGINTABS]

>[!TAB Inserte directamente el código]

Simplemente copie y pegue el bloque de código siguiente en el código de la política de decisión. Reemplazar `variable` por el ID de fragmento y `placement` por la clave de referencia de fragmento:

```
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable}}
```

>[!TAB Siga los pasos detallados]

1. Vaya a las **[!UICONTROL funciones de ayuda]** y agregue la función **Permitir** `{% let variable = expression %} {{variable}}` al panel de código, donde puede declarar la variable para el fragmento.

   ![](assets/decision-let-function.png)

1. Use la función **Map** > **Get** `{%= get(map, string) %}` para generar su expresión. El mapa es el fragmento al que se hace referencia en el elemento de decisión y la cadena puede ser el modelo de dispositivo que especificó en el elemento de decisión como **[!UICONTROL clave de referencia de fragmento]**.

   ![](assets/decision-map-function.png)

1. También puede utilizar un atributo contextual que contenga este ID de modelo de dispositivo.

   ![](assets/decision-contextual-attribute.png)

1. Agregue la variable que eligió para el fragmento como ID de este.

   ![](assets/decision-fragment-id.png)

>[!ENDTABS]

El ID de fragmento y la clave de referencia se seleccionarán de la sección **[!UICONTROL Fragmentos]** del elemento de decisión.

>[!WARNING]
>
>Si la clave del fragmento es incorrecta o si el contenido del fragmento no es válido, el procesamiento fallará y provocará un error en la llamada de Edge.

## Protecciones al usar fragmentos {#fragments-guardrails}

**Elemento de decisión y atributos de contexto**

Los atributos de elemento de decisión y los atributos contextuales no son compatibles de forma predeterminada en los fragmentos de [!DNL Journey Optimizer]. Sin embargo, puede utilizar variables globales en su lugar, como se describe a continuación.

Supongamos que desea utilizar la variable *sport* en el fragmento.

1. Cite esta variable en el fragmento, por ejemplo:

   ```
   Elevate your practice with new {{sport}} gear!
   ```

1. Defina la variable con la función **Let** dentro del bloque de directivas de decisión. En el ejemplo siguiente, *sport* se define con el atributo de elemento de decisión:

   ```
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

**Validación del contenido de fragmentos de elementos de decisión**

* Debido a la naturaleza dinámica de estos fragmentos, cuando se utilizan en una campaña, la validación del mensaje durante la creación del contenido de la campaña se omite para los fragmentos a los que se hace referencia en los elementos de decisión.

* La validación del contenido del fragmento solo se produce durante la creación y publicación del fragmento.

* En el caso de los fragmentos JSON, no se garantiza la validez del objeto JSON. Asegúrese de que el contenido del fragmento de expresión sea un JSON válido para que pueda utilizarse en elementos de decisión.

En tiempo de ejecución, se valida el contenido de la campaña (incluido el contenido de fragmento de los elementos de decisión). En caso de error de validación, la campaña no se procesará.
