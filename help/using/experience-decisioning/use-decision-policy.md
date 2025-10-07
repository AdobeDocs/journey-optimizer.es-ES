---
title: Uso de directivas de decisión en mensajes
description: Aprenda a utilizar las políticas de decisiones en los mensajes.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
mini-toc-levels: 1
source-git-commit: 7896dc3450f499e0889f6e32df5958ae9868d9e6
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 1%

---

# Uso de directivas de decisión en mensajes {#create-decision}

Una vez creada una política de decisión, la política y los atributos vinculados a los elementos de decisión devueltos se pueden utilizar en el contenido para su personalización. Para ello, el código asociado a la política de decisión debe insertarse primero en el contenido. Una vez finalizado, puede aprovechar sus atributos para la personalización.

## Inserción del código de la política de decisión {#insert-code}

1. Abra el editor de personalización y acceda al menú **[!UICONTROL Directiva de decisión]**.

1. Seleccione **[!UICONTROL Insertar directiva]** (experiencia basada en código) o **[!UICONTROL Insertar sintaxis]** (correo electrónico) para agregar el código correspondiente a la directiva de decisión.

   +++Insertar código de política de decisión en correos electrónicos

   ![](assets/decision-policy-add.png)

   En el caso de los correos electrónicos, si no se ha asociado ninguna ubicación al componente de antemano, seleccione una de la lista y haga clic en **[!UICONTROL Asignar]**.

   ![](assets/decision-policy-placement.png)

   +++

   +++Insertar código de política de decisión en una experiencia basada en código

   ![](assets/decision-code-based-add-decision.png)

   +++

   >[!NOTE]
   >
   >Si no aparece el botón de inserción de código, es posible que ya se haya configurado una directiva de decisión para el componente principal.

1. Se agrega el código para la directiva de decisión. Esta secuencia se repetirá el número de veces que desee que se devuelva la política de decisión. Por ejemplo, si eligió devolver 2 elementos al [crear la decisión](#add-decision), la misma secuencia se repetirá dos veces.

## Aprovechamiento de atributos de elementos de decisión {#attributes}

Ahora puede agregar todos los atributos de decisión que desee dentro de ese código. Los atributos disponibles se almacenan en el esquema del catálogo **[!UICONTROL Ofertas]**. Los atributos personalizados se almacenan en la carpeta **`_<imsOrg`>** y los atributos estándar en la carpeta **`_experience`**. [Más información sobre el esquema del catálogo de ofertas](catalogs.md)

![](assets/decision-code-based-decision-attributes.png)

>[!NOTE]
>
>Para el seguimiento de elementos de la directiva de decisión, el atributo `trackingToken` debe agregarse de la siguiente manera para el contenido de la directiva de decisión:
>&#x200B;>`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

Para añadir un atributo, haga clic en el icono &quot;+&quot; junto a él. Puede agregar todos los atributos que desee al código.

![](assets/decision-code-based-add-decision-attributes.png)

Asegúrese de envolver el bucle `#each` dentro de un par de corchetes `[ ]` y agregue una coma justo antes de cerrar `/each`.

![](assets/decision-code-based-wrap-code.png)

También puede añadir cualquier otro atributo disponible en el editor de personalización, como atributos de perfil.

![](assets/decision-code-based-decision-profile-attribute.png)

## Aprovechamiento de fragmentos {#fragments}

Si la política de decisión contiene elementos de decisión, incluidos fragmentos, puede aprovechar estos fragmentos en el código de la política de decisión. [Más información sobre fragmentos](../content-management/fragments.md)

>[!AVAILABILITY]
>
>Actualmente, esta capacidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

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

### Protecciones al usar fragmentos {#fragments-guardrails}

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

## Próximos pasos {#final-steps}

Una vez que el contenido esté listo, revise y publique la campaña o el recorrido:

* [Publicación de un recorrido](../building-journeys/publishing-the-journey.md)
* [Revisar y activar una campaña](../campaigns/review-activate-campaign.md)
* [Publicación y activación de una experiencia basada en código](../code-based/publish-code-based.md)

En el caso de las experiencias basadas en código, tan pronto como el desarrollador realice una llamada de API o SDK para recuperar contenido para la superficie definida en la configuración de canal, los cambios se aplicarán a su página web o aplicación.

>[!NOTE]
>
>Actualmente no puedes simular contenido desde la interfaz de usuario en una campaña o recorrido de [experiencia basada en código](../code-based/create-code-based.md) usando decisiones. Hay una solución disponible en [esta sección](../code-based/code-based-decisioning-implementations.md).

Para ver el rendimiento de sus decisiones, puede crear [paneles personalizados de informes de Customer Journey Analytics](cja-reporting.md).
