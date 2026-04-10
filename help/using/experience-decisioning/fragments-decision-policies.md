---
title: Aprovechamiento de fragmentos en políticas de decisión
description: Aprenda a aprovechar los fragmentos en las políticas de decisión
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 70f64348-092b-4350-91dc-72c3c07300f9
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: b579e39194f70dd3cb67577b82fa4868de36c5e2
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 1%

---

# Aprovechamiento de fragmentos en políticas de decisión {#fragments}

Si la política de decisión contiene elementos de decisión, incluidos fragmentos, puede aprovechar estos fragmentos en el código de la política de decisión. [Más información sobre fragmentos](../content-management/fragments.md)

>[!AVAILABILITY]
>
>Esta característica está disponible con disponibilidad limitada para los canales de **experiencia basada en código** y **correo electrónico**. Para solicitar acceso, póngase en contacto con su representante de Adobe.

Por ejemplo, supongamos que desea mostrar contenido diferente para varios modelos de dispositivos móviles. Asegúrese de agregar los fragmentos correspondientes a esos dispositivos al elemento de decisión que está utilizando en la directiva de decisión. [Más información](items.md#attributes).

![Sección de fragmentos de un elemento de decisión que muestra referencias de fragmento y claves de ubicación.](assets/item-fragments.png){width=70%}

Una vez finalizado, puede utilizar cualquiera de los siguientes métodos:

>[!BEGINTABS]

>[!TAB Inserte directamente el código]

Simplemente copie y pegue el bloque de código siguiente en el código de la política de decisión. Reemplazar `variable` por el ID de fragmento y `placement` por la clave de referencia de fragmento:

```handlebars
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable}}
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
>Si la clave del fragmento es incorrecta o si el contenido del fragmento no es válido, el procesamiento fallará y provocará un error en la llamada de Edge.

## Protecciones al usar fragmentos {#fragments-guardrails}

**Simular fragmentos de contenido y expresión en correos electrónicos**

Para el canal **Email**, los fragmentos de expresión asociados con un elemento de decisión se muestran correctamente cuando **[!UICONTROL envía la prueba]** o cuando se activa la campaña. Sin embargo, **[!UICONTROL Simular contenido]** no muestra el fragmento de expresión del elemento de decisión.

**Fragmentos visuales y elementos de decisión en correos electrónicos**

No puede asignar un **[!UICONTROL fragmento visual]** a un elemento de decisión, solo se admiten **fragmentos de expresión** en este contexto.

**Elemento de decisión y atributos de contexto**

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

**Validación del contenido de fragmentos de elementos de decisión**

* Debido a la naturaleza dinámica de estos fragmentos, cuando se utilizan en una campaña, la validación de mensajes durante la creación del contenido de la campaña se omite para los fragmentos a los que se hace referencia en los elementos de decisión.

* La validación del contenido del fragmento solo se produce durante la creación y publicación del fragmento.

* Para los fragmentos de expresiones de tipo JSON, el contenido se valida sintácticamente al guardar el fragmento. Los errores de validación se muestran como alertas.

En tiempo de ejecución, se valida el contenido de la campaña (incluido el contenido de fragmento de los elementos de decisión). En caso de error de validación, la campaña no se procesará.
