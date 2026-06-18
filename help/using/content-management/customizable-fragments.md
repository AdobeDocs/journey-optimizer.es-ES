---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos personalizables
description: Aprenda a personalizar fragmentos haciendo que algunos de sus campos sean editables.
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: cd47ca1d-f707-4425-b865-14f3fbbe5fd1
TQID: https://experienceleague.adobe.com/cwg-nGPftYg6UgVSKXZPdW6DZr4-m5UM5Wqzfx3w028
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c6e980f5-2d4f-494f-beef-186b9ecf1513
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 69ba57a83a35331f05d782588a26f7f45579c180
workflow-type: tm+mt
source-wordcount: 1658
ht-degree: 5%

---

# Fragmentos personalizables {#customizable-fragments}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a hacer editables campos específicos en fragmentos visuales y de expresión para que los usuarios puedan personalizarlos al agregar el fragmento a una campaña o recorrido, sin romper la herencia del fragmento original.

>[!ENDSHADEBOX]

Cuando se utilizan fragmentos en una campaña o acción de recorrido, están bloqueados de forma predeterminada debido a la herencia. Esto significa que los cambios realizados en un fragmento se propagan automáticamente a todas las campañas y recorridos donde se utilice el fragmento.

Con **fragmentos personalizables**, los campos específicos de un fragmento se pueden definir como editables cuando se agrega el fragmento a una acción de campaña o recorrido. Por ejemplo, supongamos que tiene un fragmento con un titular, texto y un botón. Puede designar ciertos campos, como la dirección URL de destino de la imagen o el botón, como editables. Esto permite a los usuarios modificar estos elementos cuando incorporan el fragmento en su campaña o recorrido, lo que proporciona una experiencia adaptada sin afectar al fragmento original.

Los fragmentos personalizables eliminan la necesidad de interrumpir la herencia de fragmentos, que anteriormente impedía que los cambios centralizados en el nivel de fragmento se propagaran a las campañas y recorridos. Este método permite ajustar las partes de contenido en el momento de su uso, lo que ofrece la flexibilidad de anular los valores predeterminados con detalles específicos del contexto.

Al aprovechar los fragmentos personalizables, puede administrar y personalizar el contenido de forma eficaz sin crear bloques de contenido completamente nuevos ni interrumpir la herencia del fragmento original. Esto garantiza que los cambios realizados en el nivel de fragmento se sigan propagando, al tiempo que permite la personalización necesaria en el nivel de campaña o recorrido.

Los fragmentos visuales y de expresión se pueden marcar como personalizables. Para obtener instrucciones detalladas sobre cómo proceder con cada tipo de fragmento, consulte las secciones siguientes.

![](../content-management/assets/do-not-localize/gif-fragments.gif)

## Agregar campos editables a fragmentos visuales {#visual}

Para poder editar partes de un fragmento visual, siga estos pasos:

>[!NOTE]
>
>Los campos editables se pueden agregar a los componentes **image**, **text** y **button**. Para los componentes de **HTML**, se agregan campos editables mediante el editor de personalización, de forma similar a los fragmentos de expresiones. [Aprenda a agregar campos editables en componentes de HTML y fragmentos de expresiones](#expression)

1. Abra la pantalla de edición de contenido del fragmento.

1. Seleccione el componente del fragmento en el que desea configurar los campos editables.

1. El panel de propiedades del componente se abre en el lado derecho. Seleccione la ficha **Campos editables** y, a continuación, active la opción **Habilitar edición**.

1. Todos los campos que se pueden editar para el componente seleccionado se muestran en el panel. Los campos disponibles para editar dependen del tipo de componente seleccionado.

   En el ejemplo siguiente, permitimos la edición de la URL del botón &quot;Haga clic aquí&quot;.

   ![](assets/fragment-param-enable.png)

1. Haga clic en **Información general** para comprobar todos los campos editables y sus valores predeterminados.

   En este ejemplo, el campo URL del botón se muestra con el valor predeterminado definido en el componente. Los usuarios podrán personalizar este valor una vez que hayan agregado el fragmento a su contenido.

   ![](assets/fragment-param-preview.png)

1. Cuando esté listo, guarde los cambios para actualizar el fragmento.

1. Después de agregar el fragmento a un correo electrónico, los usuarios podrán personalizar todos los campos editables configurados en el fragmento. [Aprenda a personalizar campos editables en un fragmento visual](../email/use-visual-fragments.md#customize-fields)

>[!CAUTION]
>
>Cuando la **etiqueta** y la **URL** de un componente de botón se hacen editables en un fragmento, los informes de seguimiento muestran la URL en lugar de la etiqueta de botón. [Más información sobre el seguimiento](../email/message-tracking.md)

## Habilitar la edición de texto enriquecido en un fragmento visual personalizable {#rich-text-visual}

>[!CONTEXTUALHELP]
>id="ajo_editable_fragment_compatibility"
>title="Fragmento heredado"
>abstract="Los campos editables de este fragmento están en modo de solo texto. Esto significa que solo puede introducir texto sin formato al editar este fragmento en correos electrónicos; no se admiten opciones de formato completo como negrita, cursiva, hipervínculos y saltos de línea. Haga clic en <b>Habilitar</b> para permitir texto enriquecido en campos editables al utilizar el fragmento en un mensaje de correo electrónico."

>[!CONTEXTUALHELP]
>id="ajo_editable_field_compatibility"
>title="Fragmento heredado"
>abstract="Este campo editable está en modo de solo lectura. Opciones de formato completo (negrita, cursiva, hipervínculos, saltos de línea, etc.) no están disponibles hasta que el fragmento se actualice al modo de texto enriquecido. Vaya a la configuración del cuerpo del fragmento y haga clic en <b>Habilitar</b> para desbloquear texto enriquecido en campos editables."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/channels/email/design-email/add-content/use-visual-fragments#customize-fields" text="Personalización de campos editables en un fragmento"

>[!CONTEXTUALHELP]
>id="ac_editable_fragment_compatibility"
>title="Fragmento heredado"
>abstract="Los campos editables de este fragmento están en modo de solo texto. Opciones de formato completo (negrita, cursiva, hipervínculos, saltos de línea, etc.) no están disponibles hasta que el fragmento se actualice al modo de texto enriquecido. Para desbloquear este modo, abre el editor de fragmentos y haz clic en <b>Habilitar</b>."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/channels/email/design-email/add-content/use-visual-fragments#customize-fields" text="Personalización de campos editables en un fragmento"

El texto enriquecido <!--— including bold, italic, line breaks, and hyperlinks —--> ahora se admite de forma nativa en fragmentos visuales personalizables.

Cuando se usa un fragmento visual personalizable en un mensaje de correo electrónico, se pueden aprovechar las opciones de formato completo, como negrita, cursiva, saltos de línea, listas con viñetas e hipervínculos, directamente en cualquier campo editable de los componentes **[!UICONTROL Texto]**, **[!UICONTROL Botón]** y **[!UICONTROL Html]** del fragmento. [Aprenda a personalizar campos editables](../email/use-visual-fragments.md#customize-fields)

Sin embargo, si ha creado fragmentos y ha definido campos editables antes de que se introdujera la capacidad de texto enriquecido, los campos editables se establecen en modo de solo texto de forma predeterminada.

* Se muestra una advertencia de compatibilidad en el editor de fragmentos.

  ![](assets/fragment-custom-compatibility.png)

  Para desbloquear el modo de texto enriquecido para estos campos editables al utilizar el fragmento en un mensaje de correo electrónico, haga clic en el botón **Habilitar** y guarde el fragmento.

* Una vez agregado el fragmento a un correo electrónico, también se muestra una advertencia de compatibilidad al seleccionar el fragmento en la Designer de correo electrónico.

  ![](assets/email-fragment-custom-compatibility.png)

  Para actualizar el fragmento al modo de texto enriquecido, usa el botón **Abrir fragmento** para acceder al editor de fragmentos, haz clic en el botón **Habilitar** y guarda el fragmento.

Hasta que se desbloquee el modo de texto enriquecido, los fragmentos visuales personalizables heredados seguirán admitiendo solo texto sin formato. Los usuarios no pueden introducir texto enriquecido en los campos editables de estos fragmentos.

## Agregar campos editables a componentes de HTML y fragmentos de expresiones {#expression}

Para poder editar partes de un componente de HTML o de un fragmento de expresión, debe utilizar una sintaxis específica en el editor de expresiones. Esto implica declarar una **variable** con un valor predeterminado que los usuarios pueden anular después de agregar el fragmento a su contenido.

Por ejemplo, supongamos que desea crear un fragmento para agregarlo a los correos electrónicos y permitir a los usuarios personalizar un color específico utilizado en diferentes ubicaciones, como marcos o colores de fondo de botones. Al crear el fragmento, debe declarar una variable con un **ID único**, por ejemplo, &quot;color&quot;, y llamarla a las ubicaciones deseadas en el contenido del fragmento donde desee aplicar este color. Al añadir el fragmento a su contenido, los usuarios pueden personalizar el color utilizado siempre que se haga referencia a la variable.

Para los componentes de HTML, solo los elementos específicos pueden convertirse en campos editables. Expanda la sección siguiente para obtener más información.

+++Elementos editables en componentes de HTML:

Los elementos siguientes pueden convertirse en campos editables en un componente de HTML:

* Una parte del texto
* Una dirección URL completa para un vínculo o una imagen (no funciona con una parte de una dirección URL)
* Propiedad CSS completa (no funciona con la propiedad parcial)

Por ejemplo, en el siguiente código, cada elemento resaltado en rojo puede convertirse en una propiedad:

![](assets/fragment-html.png){width="70%"}

+++

Para declarar una variable y utilizarla en el fragmento, siga estos pasos:

1. Abra el fragmento de expresión y, a continuación, edite su contenido en el editor de personalización.

   ![](assets/fragment-html-edit.png)

   Para los componentes de HTML, seleccione el componente en el fragmento y haga clic en el botón **Mostrar código fuente**.

1. Declare la variable que desea que los usuarios editen. Vaya al menú **Funciones de ayuda** en el panel de navegación izquierdo y agregue la función de ayuda **inline**. La sintaxis para declarar y llamar a la variable se agrega automáticamente al contenido.

   ![](assets/fragment-add-helper.png)

1. Reemplace `"name"` con un identificador único para identificar el campo editable.

   >[!NOTE]
   >
   >El ID de campo debe ser único y no debe tener espacios. Este ID debe utilizarse en cualquier lugar del contenido donde desee mostrar el valor de la variable.

1. Adapte la sintaxis para adaptarla a sus necesidades añadiendo parámetros detallados en la siguiente tabla:

   | Acción | Parámetro | Ejemplo |
   | ------- | ------- | ------- |
   | Declarar un campo editable con un **valor predeterminado**. Al añadir el fragmento al contenido, se utilizará este valor predeterminado si no lo personaliza. | Agregue el valor predeterminado entre las etiquetas en línea. | `{{#inline "editableFieldID"}}default_value{{/inline}}` |
   | Defina una **etiqueta** para el campo editable. Esta etiqueta se muestra en el Designer de correo electrónico al editar los campos del fragmento. | `name="title"` | `{{#inline "editableFieldID" name="title"}}default_value{{/inline}}` |
   | Declare un campo editable que contenga un **origen de imagen** que deba publicarse. | `assetType="image"` | `{{#inline "editableFieldID" assetType="image"}}default_value{{/inline}}` |
   | Declare un campo editable que contenga una **URL** de la que deba realizarse un seguimiento.<br/>Tenga en cuenta que los bloques predefinidos &quot;URL de página espejo&quot; y &quot;Vínculo de cancelación de suscripción&quot; predeterminados no pueden convertirse en campos editables. | `assetType="url"` | `{{#inline "editableFieldID" assetType="url"}}default_value{{/inline}}` |

1. Utilice la sintaxis `{{{name}}}` en su código en cada lugar donde desee mostrar el valor del campo editable. Reemplazar `name` por el ID único del campo definido anteriormente.

   ![](assets/fragment-call-variable.png)

1. Guarde y publique el fragmento.

Al añadir el fragmento al contenido de su correo electrónico, los usuarios ahora pueden anular los valores predeterminados de las variables con los valores que hayan elegido:

* Para los fragmentos de expresiones, se utiliza una sintaxis específica para anular los valores de las variables. [Aprenda a personalizar campos editables en un fragmento de expresión](../personalization/use-expression-fragments.md#customize-fields)

* Para los componentes de HTML, la variable se muestra en la lista de campos editables del Designer de correo electrónico. [Aprenda a personalizar campos editables en un fragmento visual](../email/use-visual-fragments.md#customize-fields)

### Ejemplo: fragmento de expresión personalizable {#example}

En el ejemplo siguiente, se crea un fragmento de expresión que presenta nuevas colecciones deportivas. De manera predeterminada, el fragmento muestra este contenido: *¿Busca más? ¡No se pierda nuestra última colección de deportes!*

Queremos permitir que los usuarios reemplacen &quot;deportes&quot; en este contenido por el deporte de su elección. Por ejemplo: *¿Busca más? ¡No se pierda nuestra última colección de yoga!*

Para ello:

1. Declare una variable &quot;sport&quot; con el ID &quot;sport&quot;.

   De manera predeterminada, si los usuarios no cambian el valor de la variable después de agregar el fragmento en su contenido, se mostrará el valor definido entre las etiquetas `{{#inline}}` y `{{/inline}}`, por ejemplo, &quot;deportes&quot;.

1. Agregue la sintaxis ``{{{sport}}}`` al contenido del fragmento donde desee mostrar el valor de la variable, es decir, &quot;deportes&quot; de forma predeterminada o el valor elegido por los usuarios.

   ![](assets/fragment-expression-custom.png)

1. Al agregar el fragmento de expresión a su contenido, los usuarios pueden cambiar el valor de la variable con su elección directamente desde el editor de expresiones. [Aprenda a personalizar campos editables en un fragmento de expresión](../personalization/use-expression-fragments.md#customize-fields)

   ![](assets/fragment-expression-use.png)

<!--
## Add rich text to a customizable fragment {#rich-text}

Rich text such as line breaks, bold, italics etc., can be added to a customizable fragment by using HTML components. To do so, follow the steps below.

➡️ [Learn how to add and use rich text in a customizable fragment in this video](#video)

### Create a fragment including rich text {#add-rich-text}

The approach below (using HTML components with inline variables) remains fully supported for advanced HTML-based scenarios??

1. Create a visual [fragment](create-fragments.md) and start adding components.

1. Add an [HTML component](../email/content-components.md#HTML) and open the HTML editor.

1. Navigate to the **[!UICONTROL Helper functions]** menu in the left navigation pane and add the **inline** helper function.

1. Replace `"name"` with the ID you want to use for your editable content, for example "EditableContent".

1. Replace `render_content` with the HTML code corresponding to the default rich content you want. You can add bold, italic, line breaks, bulleted lists, etc.

    ![](assets/fragment-rich-editable-content.png)

1. Within the same HTML component, add another **inline** helper function for your styling elements.

1. Replace `"name"` and `render_content` with the ID and HTML code corresponding to the default styling you want.

    ![](assets/fragment-rich-editable-styling.png)

1. Save your content. The selected editable fields are displayed on the right-hand side.

    ![](assets/fragment-rich-editable-fields.png)

1. Save and [publish](create-fragments.md#publish) the fragment.

### Use rich text in customizable fragments {#use-rich-text}

When adding the fragment to your email, you can now edit the rich text content and styling that you created. As a marketer, follow the steps below.

1. [Create an email](../email/create-email.md) in a campaign or a journey, then add the fragment with rich text that was [created](#add-rich-text).

    You can see the two editable fields that were created on the right-hand side.

    ![](assets/fragment-use-rich-editable-fields.png)

1. Use either simulation method to see how the editable content and styling render: click **[!UICONTROL Simulate content]** to test content variations with sample input data or AI auto-generation, or click **[!UICONTROL Simulate content]**, then select **[!UICONTROL Simulate content (AEP profiles)]** from the dropdown to preview with test profiles. [Learn more on previewing content](preview-test.md)

1. Select the **[!UICONTROL Add personalization]** icon next to one of the editable fields.

1. In the personalization editor that opens, update the styling and/or content as wanted by adding or removing elements of the editable field.

    ![](assets/fragment-rich-editable-fields-update-styling.png)

## How-to video {#video}

This video shows how to make HTML components within a fragment editable, allowing for dynamic updates to both content and styling.

>[!VIDEO](https://video.tv.adobe.com/v/3464363/?learn=on&#x26;enablevpops)
-->