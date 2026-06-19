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
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 5ff88c5deec3f9fa326fe6fd2d71133ba4135fc4
workflow-type: tm+mt
source-wordcount: 1744
ht-degree: 0%

---

# Aprovechamiento de fragmentos en políticas de decisión {#fragments}

>[!BEGINSHADEBOX]

**En esta página:** Aproveche los fragmentos de contenido de Journey Optimizer y los fragmentos de contenido de AEM dentro de las directivas de decisión para que pueda personalizar y optimizar las ofertas de toma de decisiones de contenido entre canales.

>[!ENDSHADEBOX]

Los elementos de decisión admiten dos tipos de contenido de fragmento que se pueden aprovechar al crear mensajes dentro de una política de decisión:

* **Fragmentos de contenido de Journey Optimizer**: fragmentos de expresiones reutilizables creados en Journey Optimizer y agregados a la sección **[!UICONTROL Fragmentos]** del elemento de decisión. [Más información sobre los fragmentos de contenido de AJO](../content-management/fragments.md)
* **Fragmentos de contenido de AEM**: contenido creado en Adobe Experience Manager, asignado a los atributos del elemento de decisión y seleccionado en el editor de personalización por nombre de clave. [Aprenda a vincular un fragmento de contenido de AEM a un elemento de decisión](items.md#aem-fragments)

## Fragmentos de contenido de Journey Optimizer {#ajo-fragments}

Si la política de decisión contiene elementos de decisión, incluidos fragmentos de contenido de AJO, puede aprovechar estos fragmentos al crear un mensaje dentro de la política de decisión en todos los canales donde Decisioning está disponible (experiencia basada en código, correo electrónico, push, SMS y recorridos).

Por ejemplo, supongamos que desea mostrar contenido diferente para varios modelos de dispositivos móviles. Agregue los fragmentos especificados, cada uno perteneciente a un modelo de teléfono diferente, al elemento de decisión que esté utilizando en la directiva de decisión. [Aprenda a agregar fragmentos a un elemento de decisión](items.md#attributes).

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
>Para evitar errores cuando un fragmento no está disponible temporalmente, se utiliza el indicador `required=false` para que se omita el fragmento en su lugar. [Más información sobre fragmentos que no están disponibles temporalmente](#temporary-unavailable-fragments)

### Uso y protecciones {#fragments-guardrails}

Las siguientes protecciones se aplican específicamente a **fragmentos de contenido de AJO** utilizados en elementos de decisión.

+++Simulación de fragmentos de contenido y expresión en correos electrónicos

Para el canal **Email**, los fragmentos de expresión asociados con un elemento de decisión se muestran correctamente cuando **[!UICONTROL envía la prueba]** o cuando se activa la campaña. Sin embargo, **[!UICONTROL Simular contenido]** no muestra el fragmento de expresión del elemento de decisión.

+++

+++Fragmentos visuales y elementos de decisión en correos electrónicos

No puede asignar un **[!UICONTROL fragmento visual]** a un elemento de decisión, solo se admiten **fragmentos de expresión** en este contexto.

+++

+++Elemento de decisión y atributos de contexto

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

+++

+++Validación de contenido de fragmento de elemento de decisión

* Debido a la naturaleza dinámica de estos fragmentos, cuando se utilizan en una campaña, la validación de mensajes durante la creación del contenido de la campaña se omite para los fragmentos a los que se hace referencia en los elementos de decisión.

* La validación del contenido del fragmento solo se produce durante la creación y publicación del fragmento.

* Para los fragmentos de expresiones de tipo JSON, el contenido se valida sintácticamente al guardar el fragmento. Los errores de validación se muestran como alertas.

En tiempo de ejecución, se valida el contenido de la campaña (incluido el contenido de fragmento de los elementos de decisión). En caso de error de validación, la campaña no se procesará.

+++

+++Los fragmentos temporalmente no disponibles se omiten {#temporary-unavailable-fragments}

Cuando los recorridos o campañas hacen referencia a fragmentos adjuntos a elementos de decisión, puede haber breves retrasos de sincronización antes de que los fragmentos actualizados estén disponibles en Edge.

Para evitar errores cuando un fragmento no está disponible temporalmente, los fragmentos ahora tienen el indicador `required` establecido en `false` de forma predeterminada para que se omitan en lugar de provocar el error del recorrido o la campaña.

Esto significa que si el fragmento no está disponible temporalmente en Edge, simplemente se ignora. Si el fragmento está disponible, se procesa normalmente.

**Ejemplo**

Si la directiva de decisión cumple los requisitos para dos ofertas y cada una tiene un fragmento (por ejemplo, &quot;20 % de descuento&quot; y &quot;30 % de descuento&quot;) y el segundo fragmento no está disponible temporalmente, con `required=false` el sistema procesa la oferta disponible (20 % de descuento) y omite el otro fragmento (30 % de descuento) en lugar de realizar un error en el recorrido o la campaña. Esto mejora la fiabilidad cuando el contenido aún se está sincronizando.

+++

>[!NOTE]
>
>Puede seguir marcando un fragmento como obligatorio si establece el indicador `required` en `true`. Sin embargo, si un fragmento falta temporalmente, puede provocar un error en el procesamiento del recorrido o de la campaña.

## Fragmentos de contenido de AEM {#aem-fragments-decisioning}

>[!AVAILABILITY]
>
>Esta función está disponible para canales salientes con compatibilidad con Decisioning.

Antes de aprovechar los fragmentos de contenido de AEM en una política de decisión, asegúrese de lo siguiente:

* Se creó el fragmento de contenido en Adobe Experience Manager y se etiquetó con `ajo-enabled:{OrgId}/{SandboxName}` para que Journey Optimizer pueda detectarlo. [Aprenda a crear y asignar una etiqueta](../integrations/aem-fragments.md#create-tag)
* Asocie el fragmento a la sección **[!UICONTROL Fragmentos de AEM]** del elemento de oferta asignándole un nombre de referencia único. [Aprenda a vincular un fragmento de contenido de AEM a un elemento de decisión](items.md#attributes)

En el editor de personalización, están disponibles todos los fragmentos de contenido de AEM asociados con los elementos de decisión seleccionados por la directiva. Aparece una carpeta por nombre de clave de fragmento.

➡️ [Descubra cómo usar fragmentos de contenido de AEM con Journey Optimizer Decisioning en vídeo](#video)

En este ejemplo, la política de decisión incluye dos elementos de decisión que tienen fragmentos de AEM vinculados a ellos a través de su nombre de referencia.

![Editor de Personalization que muestra fragmentos de contenido de AEM disponibles por nombre de clave de fragmento en una directiva de decisión.](assets/aem-fragment-select.png)

1. Haga clic en el botón + para añadir el fragmento deseado a la expresión.

   Dado que un solo nombre de referencia puede tener varios fragmentos vinculados a él en diferentes elementos de oferta, Decisioning determina el mejor para entregar a cada cliente en función de los criterios de clasificación de la política de decisión.

1. Una vez seleccionado el fragmento, puede aprovechar sus atributos, como direcciones URL de imagen, campos de texto u otro contenido, y utilizar Decisioning para mostrar el contenido correcto al cliente correcto en el momento adecuado.

   ![Atributos de fragmento de contenido de AEM seleccionados disponibles para su personalización en la expresión de directiva de decisión.](assets/aem-fragment-attribute.png)

1. Antes de activar la campaña o el recorrido, utilice cualquiera de los métodos de simulación para previsualizar cómo se renderizarán los valores de los campos de fragmento de contenido de AEM. [Más información sobre la simulación de contenido](../content-management/preview-test.md)

### Usar fragmentos de contenido de AEM en varios canales {#aem-fragments-channels}

La forma de insertar atributos de fragmento de contenido de AEM desde una directiva de decisión depende del canal en el que esté trabajando.

>[!BEGINTABS]

>[!TAB Correo electrónico]

Para insertar atributos de fragmento de contenido de AEM en el correo electrónico mediante una directiva de decisión:

1. Abra el borrador del correo electrónico en el Designer de correo electrónico y haga clic en el icono **[!UICONTROL Toma de decisiones]**, en el carril derecho, para abrir el panel de la política de decisión.
1. Seleccione la estrategia de selección que ha ensamblado y especifique una **ubicación** para definir el área del correo electrónico donde se rellenará la oferta.
1. Haga clic en el icono **+** y seleccione el campo específico del fragmento de contenido de AEM que se debe representar en esa área como, por ejemplo, el campo URL de imagen a pantalla completa.

   ![Panel de directivas de decisión de Designer de correo electrónico con un campo de fragmento de contenido de AEM seleccionado para una ubicación.](assets/aem-fragment-email.png)

1. Antes de publicar, haga clic en **[!UICONTROL Simular contenido]** para obtener una vista previa del resultado y comprobar que la oferta de mayor prioridad y su fragmento de contenido se representan como se espera para un perfil de prueba.

>[!TAB Experiencia basada en código (JSON)]

Cuando cree una experiencia basada en código JSON, utilice la siguiente estructura para procesar atributos de fragmento de contenido de AEM a partir de una política de decisión.

```handlebars
[
{{#each decisionPolicy.YOUR_POLICY_ID.items as |item|}}
{% let frag = get(item._experience.decisioning.offeritem.aemContentReferencesMap, "YOUR_REFERENCE_KEY").id %}
{{fragment id = frag result='YOUR_REFERENCE_KEY' required=false}}
{
  "fieldName": "{{{YOUR_REFERENCE_KEY.fieldName}}}"
},
{{/each}}
]
```

>[!NOTE]
>
>Los fragmentos de contenido de AEM utilizan `aemContentReferencesMap` para buscar fragmentos por clave de referencia. Es diferente de `contentReferencesMap`, que se usa para fragmentos de contenido de Journey Optimizer.

Tenga en cuenta lo siguiente al crear la carga útil JSON:

* Coloque los corchetes de matriz JSON `[` y `]` **fuera** del bucle `#each`.
* Utilice **llaves triples** `{{{ }}}` para los valores de campo dentro de cadenas JSON a fin de evitar que HTML escape caracteres especiales y garantizar una salida JSON válida.
* El parámetro `result='YOUR_REFERENCE_KEY'` captura el contenido del fragmento resuelto con ese nombre para que pueda hacer referencia a sus campos con `YOUR_REFERENCE_KEY.fieldName`.

![Editor de experiencias basado en código que muestra atributos de fragmentos de contenido de AEM procesados a partir de una directiva de decisión en JSON.](assets/aem-fragments-cbe.png)

>[!TAB Experiencia basada en código (HTML)]

Para las experiencias basadas en código basadas en HTML, utilice llaves dobles estándar para la renderización de campos:

```handlebars
{{#each decisionPolicy.YOUR_POLICY_ID.items as |item|}}
{% let frag = get(item._experience.decisioning.offeritem.aemContentReferencesMap, "YOUR_REFERENCE_KEY").id %}
{{fragment id = frag result='YOUR_REFERENCE_KEY' required=false}}
<div>{{YOUR_REFERENCE_KEY.fieldName}}</div>
{{/each}}
```

>[!ENDTABS]

### Uso de recursos de fragmentos de contenido de AEM {#aem-cf-assets}

Los fragmentos de contenido de AEM pueden incluir campos de imagen que hacen referencia a recursos almacenados en AEM. Dado que Journey Optimizer solo recibe la **ruta relativa** de esos recursos, es posible que las imágenes no se carguen a menos que se anteponga la dirección URL de publicación completa.

>[!NOTE]
>
>Todavía no se admite la resolución nativa de referencias de recursos de AEM dentro de fragmentos de contenido. Los enfoques siguientes son soluciones alternativas disponibles hasta que se añada dicha compatibilidad.

>[!BEGINTABS]

>[!TAB Anteponer el dominio de publicación de AEM]

1. Desde la dirección URL de la instancia de AEM, identifique el dominio de autor; por ejemplo, `author-p12345-e67890.adobeaemcloud.com`.

   ![URL de instancia de AEM que muestra el dominio de autor utilizado para derivar el dominio de publicación.](assets/aem-fragment-author-domain.png)

1. Reemplazar `author` por `publish` para obtener el dominio de publicación: `publish-p12345-e67890.adobeaemcloud.com`.

1. En el editor de personalización de Journey Optimizer, anteponga ese dominio de publicación al campo de referencia de recursos del fragmento de contenido.

   ![Editor de Personalization con el dominio de publicación de AEM antepuesto a un campo de referencia de recurso de fragmento de contenido.](assets/aem-fragment-publish-domain.png)

La imagen ahora se resolverá en la dirección URL de publicación completa a la hora de la entrega.

>[!TAB Almacenar la dirección URL de publicación en un campo de texto]

1. Abra el fragmento de contenido en AEM.
1. Vaya a la vista previa de JSON y marque la sección **Referencias** para localizar la URL del recurso publicado.

   ![Sección de referencias de la vista previa JSON del fragmento de contenido de AEM que muestra la URL del recurso publicado.](assets/aem-fragment-published-url.png)

1. Copie la URL de publicación y péguela en un campo de texto dedicado dentro del fragmento de contenido.

   ![Campo de texto de fragmento de contenido de AEM que contiene la URL de publicación copiada para el recurso al que se hace referencia.](assets/aem-fragment-copy-url.png)

1. En Journey Optimizer, haga referencia a ese campo de texto directamente como origen de imagen en la expresión de personalización.

   ![Expresión de personalización de Journey Optimizer que hace referencia al campo de texto Fragmento de contenido como origen de imagen.](assets/aem-fragment-use-url.png)

Este método evita la construcción manual de direcciones URL y mantiene la dirección URL de publicación dentro del propio fragmento de contenido.

>[!ENDTABS]

## Vídeo práctico {#video}

Aprenda a utilizar los fragmentos de contenido de Adobe Experience Manager con Journey Optimizer Decisioning para personalizar y optimizar el contenido.

>[!VIDEO](https://video.tv.adobe.com/v/3492218/?captions=spa&learn=on&enablevpops)
