---
solution: Journey Optimizer
product: journey optimizer
title: Usar fragmentos de expresión
description: Aprenda a utilizar fragmentos de expresiones en el  [!DNL Journey Optimizer] editor de personalización.
feature: Personalization, Fragments
topic: Personalization
role: Developer
level: Intermediate
keywords: expresión, editor, biblioteca, personalización
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
TQID: https://experienceleague.adobe.com/0N5waBGElHBnlsk1pHhKT8roaly-A6srIjb3UPIDNqY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 2174
ht-degree: 0%

---

# Aprovechamiento de fragmentos de expresiones {#use-expression-fragments}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a insertar y reutilizar fragmentos de expresiones en el editor de personalización, a trabajar con variables implícitas, a utilizar fragmentos dentro de bucles, a personalizar campos editables y a interrumpir la herencia en Adobe Journey Optimizer.

>[!ENDSHADEBOX]

Al usar el **editor de personalización**, puede aprovechar todos los fragmentos de expresiones que se han creado o guardado en la zona protegida actual.

Un fragmento es un componente reutilizable al que se puede hacer referencia en [!DNL Journey Optimizer] campañas y recorridos. Esta funcionalidad permite generar previamente varios bloques de contenido personalizados que los usuarios de marketing pueden utilizar para ensamblar contenido rápidamente en un proceso de diseño mejorado. [Más información sobre fragmentos](../content-management/fragments.md)

➡️ [Aprenda a administrar, crear y usar fragmentos en este vídeo](../content-management/fragments.md#video-fragments)

## Usar un fragmento de expresión {#use-expression-fragment}

Para añadir fragmentos de expresión al contenido, siga los pasos a continuación.

>[!NOTE]
>
>Puede añadir hasta 30 fragmentos en una entrega determinada. Los fragmentos solo se pueden anidar hasta 1 nivel.

1. Abra [editor de personalización](personalization-build-expressions.md) y seleccione el botón **[!UICONTROL Fragmentos]** en el panel izquierdo.

   La lista muestra todos los fragmentos de expresiones que se han creado o guardado como fragmentos en la zona protegida actual. [Aprenda a crear fragmentos](../content-management/create-fragments.md)
Se ordenan por fecha de creación: los fragmentos de expresión añadidos recientemente se muestran primero en la lista.

   ![](assets/expression-fragments-pane.png)

   También puede actualizar esta lista.

   >[!NOTE]
   >
   >Si se han modificado o agregado fragmentos mientras edita el contenido, la lista se actualizará con los cambios más recientes.

1. Haga clic en el icono + junto a un fragmento de expresión para insertar el ID de fragmento correspondiente en el editor.

   ![](assets/expression-fragment-add.png)

   >[!CAUTION]
   >
   >Puede agregar cualquier fragmento de **Borrador** o **Activo** al contenido. Sin embargo, no podrás activar tu recorrido o campaña si se está usando un fragmento con el estado **Borrador**. En el momento de la publicación del recorrido o de la campaña, los fragmentos de borrador mostrarán un error y deberá aprobarlos para poder publicarlos.

1. Una vez agregado el ID del fragmento, si abre el fragmento de expresión correspondiente y lo [edita](../content-management/manage-fragments.md#edit-fragments) desde la interfaz, los cambios se sincronizarán. Se propagan automáticamente a todos los recorridos o campañas en borrador o activos que contengan ese ID de fragmento.

1. Haga clic en el botón **[!UICONTROL Más acciones]** que está junto a un fragmento. En el menú contextual que se abre, seleccione **[!UICONTROL Ver fragmento]** para obtener más información sobre ese fragmento. El **[!UICONTROL ID de fragmento]** también se muestra y se puede copiar desde aquí.

   ![](assets/expression-fragment-view.png)

1. Puede abrir el fragmento de expresión en otra ventana para editar su contenido y propiedades, ya sea mediante la opción **[!UICONTROL Abrir fragmento]** del menú contextual o desde el panel **[!UICONTROL Información de fragmento]**. [Obtenga información sobre cómo editar un fragmento](../content-management/manage-fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. A continuación, puede personalizar y validar el contenido como de costumbre utilizando todas las capacidades de personalización y creación de [editor de personalización](personalization-build-expressions.md).

1. En algunos casos, solo es necesario calcular las variables, por lo que es posible que desee ocultar el contenido del fragmento de expresión. Para ello, use el atributo `render` y configúrelo en `false`. Por ejemplo:

   ```
   Hi {{profile.person.name.firstName|fragment id='ajo:fragmentId/variantId' mode ='inline' render=false}}
   ```

>[!NOTE]
>
>Si crea un fragmento de expresión que contiene varios saltos de línea y lo utiliza en el contenido [SMS](../mobile/create-mobile-message.md#sms-content) o [push](../push/design-push.md), se conservarán los saltos de línea. Por lo tanto, asegúrese de probar su mensaje [SMS](../mobile/send-mobile-message.md) o [push](../push/send-push.md) antes de enviarlo.

## Uso de variables implícitas {#implicit-variables}

Las variables implícitas mejoran la funcionalidad de fragmento existente para mejorar la eficacia en la reutilización de contenido y en los casos de uso de scripts. Los fragmentos pueden utilizar variables de entrada y crear variables de salida que se pueden utilizar en el contenido de la campaña y del recorrido.

Esta capacidad se puede utilizar, por ejemplo, para inicializar los parámetros de seguimiento de los correos electrónicos, en función de la campaña o el recorrido actual, y utilizar estos parámetros en los vínculos personalizados añadidos al contenido del correo electrónico.

Los siguientes casos de uso son posibles:

1. **Usar variables de entrada en un fragmento.**

   Cuando se utiliza un fragmento en el contenido de una acción de campaña o recorrido, tiene la capacidad de aprovechar las variables que se declararon fuera del fragmento. A continuación se muestra un ejemplo:

   ![](../personalization/assets/variable-in-a-fragment.png)

   Podemos ver arriba que la variable `utm_content` está declarada en el contenido de la campaña. Cuando se usa el fragmento **Bloque principal**, mostrará un vínculo al que se agregará el valor del parámetro `utm_content`. El resultado final es: `https://luma.enablementadobe.com?utm_campaign= Product_launch&utm_content= start_shopping`.

1. **Usar variables de salida de un fragmento.**

   Las variables calculadas o definidas dentro de un fragmento están disponibles para su uso en el contenido. En el ejemplo siguiente, un fragmento **F1** declara un conjunto de variables:

   ![](../personalization/assets/personalize-with-variables.png)

   En el contenido de un correo electrónico, puede tener la siguiente personalización:

   ![](../personalization/assets/use-fragment-variable.png)

   El fragmento F1 inicializa las siguientes variables: `utm_campaign` y `utm_content`. A continuación, se adjuntan estos parámetros al vínculo del contenido del mensaje. El resultado final es: `https://luma.enablementadobe.com?utm_campaign= Product_launch&utm_content= start_shopping`.

>[!NOTE]
>
>En tiempo de ejecución, el sistema expande lo que hay dentro de los fragmentos y, a continuación, interpreta el código de personalización de arriba a abajo. Teniendo esto en cuenta, se pueden lograr casos de uso más complejos. Por ejemplo, puede hacer que un fragmento F1 pase variables a otro fragmento F2 situado debajo. También puede hacer que un fragmento visual F1 pase variables a un fragmento de expresión anidado F2.

## Usar fragmentos de expresión dentro de bucles {#fragments-in-loops}

Cuando se utilizan fragmentos de expresión en bucles `{{#each}}`, es importante comprender cómo funciona el ámbito de variables. Los fragmentos de expresiones pueden acceder a las variables globales definidas en el contenido del mensaje, pero no pueden recibir variables específicas del bucle como parámetros.

### Patrón admitido: usar variables globales {#global-variables-in-loops}

Los fragmentos de expresiones pueden hacer referencia a variables globales que se definen fuera del fragmento, incluso cuando se llama al fragmento desde un bucle. Este es el enfoque recomendado cuando necesita utilizar fragmentos en contextos iterativos.

**Ejemplo: Usar un fragmento con variables globales dentro de un bucle**

En el contenido del mensaje, defina una variable global y utilice un fragmento que haga referencia a ella:

```handlebars
{% let globalDiscount = 15 %}

{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    <p>Price: ${{product.price}}</p>
    {{fragment id='ajo:fragment123/variant456' mode='inline'}}
  </div>
{{/each}}
```

En el fragmento de expresión (fragmento123), puede hacer referencia a la variable `globalDiscount`:

```handlebars
<p class="discount-info">Save {{globalDiscount}}% on all items!</p>
```

Este patrón funciona porque la variable global es accesible a través del mensaje, incluso dentro de fragmentos, independientemente del contexto de bucle.

### No compatible: Pasar variables de bucle como parámetros de fragmento {#loop-variables-limitations}

No puede pasar el elemento de iteración actual (por ejemplo, `product` en el ejemplo anterior) como parámetro a un fragmento de expresión. El fragmento no puede tener acceso directo a variables con ámbito de bucle desde el bloque `{{#each}}` que lo rodea.

**Ejemplo: Lo que NO funciona**

```handlebars
{{#each context.journey.actions.GetProducts.items as |product|}}
  <!-- This will NOT work as expected -->
  {{fragment id='ajo:fragment123/variant456' mode='inline' currentProduct=product}}
{{/each}}
```

El fragmento no puede recibir `product` como parámetro y utilizarlo internamente porque no se admite el paso de parámetros para variables específicas del bucle en la implementación actual.

### Soluciones recomendadas {#fragments-in-loops-workarounds}

Cuando necesite utilizar fragmentos de expresión con datos de un bucle, tenga en cuenta los siguientes enfoques:

1. **Incluir lógica directamente en el mensaje**: en lugar de usar un fragmento para lógica específica del bucle, agregue el código de personalización directamente dentro del bloque `{{#each}}`.

   ```handlebars
   {{#each context.journey.actions.GetProducts.items as |product|}}
     <div class="product">
       <h3>{{product.name}}</h3>
       <p>Price: ${{product.price}}</p>
       {{#if product.price > 100}}
         <span class="premium-badge">Premium Product</span>
       {{/if}}
     </div>
   {{/each}}
   ```

2. **Usar fragmentos fuera de los bucles**: Si el contenido del fragmento no depende del bucle, llame al fragmento antes o después del bloque de iteración.

   ```handlebars
   {{fragment id='ajo:fragment123/variant456' mode='inline'}}
   
   {{#each context.journey.actions.GetProducts.items as |product|}}
     <div class="product">
       <h3>{{product.name}}</h3>
       <p>Price: ${{product.price}}</p>
     </div>
   {{/each}}
   ```

3. **Establecer varias variables globales**: Si necesita pasar valores diferentes a un fragmento a través de iteraciones, establezca variables globales antes de cada llamada de fragmento (aunque esto limita la flexibilidad).

>[!NOTE]
>
>Para iterar en datos contextuales y trabajar con bucles, consulte la guía completa sobre [iterar en datos contextuales](iterate-contextual-data.md), que incluye prácticas recomendadas, sugerencias para la solución de problemas y patrones avanzados.

## Personalizar campos editables {#customize-fields}

Si se han hecho editables ciertas partes de un fragmento de expresión mediante variables, puede anular sus valores predeterminados con una sintaxis específica. [Aprenda a personalizar los fragmentos](../content-management/customizable-fragments.md)

Para personalizar los campos, siga estos pasos:

1. Inserte el fragmento en su código desde el menú **[!UICONTROL Fragmentos]**.

1. Utilice el código `<fieldId>="<value>"` al final de la sintaxis para anular el valor predeterminado de la variable.

   En el ejemplo siguiente, anulamos el valor de una variable cuyo ID es &quot;sports&quot; con el valor &quot;yoga&quot;. Esto mostrará &quot;yoga&quot; en el contenido del fragmento en todas partes donde se haga referencia a la variable &quot;sport&quot;.

   ![](../content-management/assets/fragment-expression-use.png)

Un ejemplo que muestra cómo agregar campos editables a fragmentos de expresión y anular sus valores al crear un correo electrónico está disponible en [esta sección](../content-management/customizable-fragments.md#example).

## Usar la resolución dinámica de fragmentos {#dynamic-resolution}

En lugar de incrustar estáticamente un ID de fragmento en tiempo de diseño, puede resolver el ID de fragmento de forma dinámica en tiempo de ejecución por destinatario. Esto permite que perfiles diferentes reciban bloques de contenido completamente diferentes dentro de la misma campaña o recorrido, según atributos de perfil, búsquedas de conjuntos de datos o datos de contexto.

[Aprenda a utilizar fragmentos dinámicos](../content-management/dynamic-fragments.md)

## Romper herencia {#break-inheritance}

Al agregar un ID de fragmento al editor de personalización, se sincronizan los cambios realizados en el fragmento de expresión original.

Sin embargo, también puede pegar el contenido de un fragmento de expresión en el editor. En el menú contextual, seleccione **[!UICONTROL Pegar fragmento]** para insertar ese contenido.

![](assets/expression-fragment-paste.png)

En ese caso, la herencia del fragmento original se interrumpe. El contenido del fragmento se copia en el editor y los cambios ya no se sincronizan.

Se convierte en un elemento independiente que ya no está vinculado al fragmento original; puede editarlo como cualquier otro elemento del código.

## Referencia rápida {#quick-reference}

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

>[!BEGINTABS]

>[!TAB Información general]

**TL;DR**

En esta página se explica cómo insertar, personalizar y administrar fragmentos de expresiones en el editor de personalización, incluidas las variables implícitas, el uso de fragmentos dentro de bucles, campos editables, la resolución dinámica y la interrupción de la herencia.

**Intenciones**

* Inserte un fragmento de expresión desde el menú Fragmentos y comprenda la propagación automática de cambios
* Usar variables implícitas: variables de entrada (declaradas fuera del fragmento y utilizadas dentro) y variables de salida (declaradas dentro del fragmento y utilizadas dentro del contenido del mensaje)
* Usar fragmentos de expresión dentro de bucles: aprovechar las variables globales para el acceso a fragmentos; comprender la limitación de pasar variables con ámbito de bucle como parámetros
* Anular campos editables en un fragmento personalizable mediante la sintaxis `<fieldId>="<value>"`
* Resolver ID de fragmento de forma dinámica durante la ejecución en función de atributos de perfil, búsquedas de conjuntos de datos o datos de contexto
* Para romper la herencia, pegue el contenido del fragmento directamente en el editor

>[!TAB Glosario]

* **Fragmento de expresión**: Componente de expresión de personalización reutilizable al que hace referencia el identificador en todas las campañas y recorridos; los cambios en el fragmento se propagan automáticamente a todo el contenido que hace referencia a él. *(específico del producto)*
* **Variables implícitas**: Variables que amplían la funcionalidad del fragmento: variables de entrada (declaradas en el contenido de campaña/recorrido, consumidas dentro del fragmento) y variables de salida (declaradas dentro del fragmento, disponibles en el contenido del mensaje circundante). *(específico del producto)*
* **Variable de entrada**: Una variable declarada fuera del fragmento (en contenido de campaña o recorrido) al que el fragmento puede hacer referencia y usar internamente.
* **Variable de salida**: Una variable declarada o calculada dentro de un fragmento que está disponible para su uso en el contenido del mensaje adyacente después de llamar al fragmento.
* **Campos editables**: Las variables de fragmento expuestas permiten al usuario que realiza la inserción anular los valores predeterminados mediante la sintaxis `<fieldId>="<value>"`, sin editar el origen del fragmento. *(específico del producto)*
* **Resolución dinámica de fragmentos**: La capacidad para resolver un ID de fragmento durante la ejecución (según atributos de perfil, búsquedas de conjuntos de datos o datos de contexto) en lugar de incrustar un ID de fragmento estático en tiempo de diseño. *(específico del producto)*
* **Romper herencia**: al usar &quot;Pegar fragmento&quot; desde el menú contextual, se copia el contenido del fragmento en el editor como un elemento independiente que ya no se sincroniza con el fragmento original. *(específico del producto)*

>[!TAB Terminología]

* **Nombre canónico:** fragmento de expresión — variantes: fragmento, fragmento de expresión
* **Sinónimos:** &quot;ID de fragmento&quot; = el identificador utilizado para hacer referencia al fragmento en las expresiones
* **No confunda:** al insertar un fragmento por identificador (al que se hace referencia; los cambios se propagan automáticamente a todo el contenido) ≠ de romper la herencia / pegar fragmento (contenido copiado en el editor; elemento independiente, ya no vinculado al original)
* **No confunda:** variables de entrada (declaradas fuera del fragmento, consumidas dentro) ≠ variables de salida (declaradas dentro del fragmento, consumidas fuera en el contenido del mensaje adyacente)
* **No confunda:** Fragmento de borrador (se puede agregar al contenido, pero bloquea la publicación de recorrido/campaña hasta que se apruebe) ≠ Fragmento activo (totalmente publicado; seguro para recorridos y campañas activos)

>[!TAB Protecciones y limitaciones]

* Se pueden agregar un máximo de 30 fragmentos en una entrega determinada.
* Los fragmentos solo se pueden anidar hasta 1 nivel.
* Un recorrido o campaña no se puede activar ni publicar si contiene un fragmento con el estado Borrador; los fragmentos de borrador deben aprobarse antes de la publicación.
* Los fragmentos de expresiones no pueden recibir variables de ámbito de bucle (el elemento de iteración actual `{{#each}}`) como parámetros; se trata de una limitación conocida. Utilice variables globales o lógica en línea como solución alternativa.
* Si se utiliza un fragmento que contiene varios saltos de línea en el contenido push o SMS, se conservan los saltos de línea; pruebe el contenido antes de enviarlo.

>[!TAB Preguntas más frecuentes]

**Q: ¿Cuántos fragmentos se pueden agregar en una sola entrega?**

Hasta 30 fragmentos.

**Q: ¿Es posible anidar fragmentos dentro de otros fragmentos?**

Sí, pero solo hasta 1 nivel de anidación.

**Q: ¿Qué sucede si utilizo un fragmento de borrador en un recorrido o una campaña?**

Puede agregar un fragmento de borrador al contenido, pero no puede activar ni publicar el recorrido o la campaña hasta que el fragmento se apruebe y su estado cambie a Activo.

**Q: ¿Puede un fragmento de expresión recibir el elemento de bucle actual (por ejemplo, `product` en `{{#each}}`) como parámetro?**

No. Los fragmentos de expresión no pueden recibir variables de ámbito de bucle como parámetros. Utilice variables globales declaradas fuera del bucle (a las que puede acceder el fragmento) o incluya la lógica de personalización directamente dentro del bucle en lugar de utilizar un fragmento.

**Q: ¿Qué es romper la herencia y cuándo debo usarla?**

Romper la herencia significa utilizar &quot;Pegar fragmento&quot; del menú contextual para copiar el contenido del fragmento directamente en el editor. El contenido pegado se convierte en un elemento independiente que ya no se sincroniza con el fragmento original. Utilícelo cuando necesite personalizar el contenido más allá de lo que permitan los campos editables, sabiendo que los cambios futuros en el fragmento original no se propagarán a esta copia.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 64745ff0 -->

