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
source-git-commit: 19b75282b6f6fbc847805a263126534c9035ad5d
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---

# Fragmentos personalizables {#customizable-fragments}

Cuando se utilizan fragmentos en una campaña o acción de recorrido, están bloqueados de forma predeterminada debido a la herencia. Esto significa que los cambios realizados en un fragmento se propagan automáticamente a todas las campañas y recorridos donde se utilice el fragmento. Con los fragmentos personalizables, los campos específicos de un fragmento se pueden definir como editables cuando el fragmento se agrega a una acción de campaña o recorrido. Por ejemplo, supongamos que tiene un fragmento con un titular, texto y un botón. Puede designar ciertos campos, como la dirección URL de destino de la imagen o el botón, como editables. Esto permite a los usuarios modificar estos elementos cuando incorporan el fragmento en su campaña o recorrido, lo que proporciona una experiencia adaptada sin afectar al fragmento original.

Los fragmentos personalizables eliminan la necesidad de interrumpir la herencia de fragmentos, que anteriormente impedía que los cambios centralizados en el nivel de fragmento se propagaran a las campañas y recorridos. Este método permite ajustar las partes de contenido en el momento de su uso, lo que ofrece la flexibilidad de anular los valores predeterminados con detalles específicos del contexto.

Al aprovechar los fragmentos personalizables, puede administrar y personalizar el contenido de forma eficaz sin crear bloques de contenido completamente nuevos ni interrumpir la herencia del fragmento original. Esto garantiza que los cambios realizados en el nivel de fragmento se sigan propagando, al tiempo que permite la personalización necesaria en el nivel de campaña o recorrido.

Los fragmentos visuales y de expresión se pueden marcar como personalizables. Para obtener instrucciones detalladas sobre cómo proceder con cada tipo de fragmento, consulte las secciones siguientes.

![](../content-management/assets/do-not-localize/gif-fragments.gif)

## Agregar campos editables en fragmentos visuales {#visual}

Para poder editar partes de un fragmento visual, siga estos pasos:

>[!NOTE]
>
>Los campos editables se pueden agregar a los componentes **image**, **text** y **button**. Para los componentes **HTML**, se agregan campos editables mediante el editor de personalización, de forma similar a los fragmentos de expresiones. [Aprenda a agregar campos editables en componentes de HTML y fragmentos de expresiones](#expression)

1. Abra la pantalla de edición de contenido del fragmento.

1. Seleccione el componente del fragmento en el que desea configurar los campos editables.

1. El panel de propiedades del componente se abre en el lado derecho. Seleccione la pestaña **Campos editables** y luego cambie la opción **Habilitar edición**.

1. Todos los campos que se pueden editar para el componente seleccionado se muestran en el panel. Los campos disponibles para editar dependen del tipo de componente seleccionado.

   En el ejemplo siguiente, permitimos la edición de la URL del botón &quot;Haga clic aquí&quot;.

   ![](assets/fragment-param-enable.png)

1. Haga clic en **Información general** para comprobar todos los campos editables y sus valores predeterminados.

   En este ejemplo, el campo URL del botón se muestra con el valor predeterminado definido en el componente. Los usuarios podrán personalizar este valor una vez que hayan agregado el fragmento a su contenido.

   ![](assets/fragment-param-preview.png)

1. Cuando esté listo, guarde los cambios para actualizar el fragmento.

1. Después de agregar el fragmento a un correo electrónico, los usuarios podrán personalizar todos los campos editables configurados en el fragmento. [Aprenda a personalizar campos editables en un fragmento visual](../email/use-visual-fragments.md#customize-fields)

## Adición de campos editables en componentes de HTML y fragmentos de expresiones {#expression}

Para poder editar partes de un componente HTML o un fragmento de expresión, debe utilizar una sintaxis específica en el editor de expresiones. Esto implica declarar una **variable** con un valor predeterminado que los usuarios pueden anular después de agregar el fragmento a su contenido.

Por ejemplo, supongamos que desea crear un fragmento para agregarlo a los correos electrónicos y permitir a los usuarios personalizar un color específico utilizado en diferentes ubicaciones, como marcos o colores de fondo de botones. Al crear el fragmento, debe declarar una variable con un **ID único**, por ejemplo, &quot;color&quot;, y llamarla a las ubicaciones deseadas en el contenido del fragmento donde desee aplicar este color. Al añadir el fragmento a su contenido, los usuarios pueden personalizar el color utilizado siempre que se haga referencia a la variable.

Para los componentes de HTML, solo los elementos específicos pueden convertirse en campos editables. Expanda la sección siguiente para obtener más información.

+++Elementos editables en componentes de HTML:

Los elementos siguientes pueden convertirse en campos editables en un componente de HTML:

* Una parte del texto
* Una dirección URL completa para un vínculo o una imagen (no funciona con una parte de la dirección URL)
* Propiedad CSS completa (no funciona con la propiedad parcial)

Por ejemplo, en el siguiente código, cada elemento resaltado en rojo puede convertirse en una propiedad:

![](assets/fragment-html.png){width="70%"}

+++

Para declarar una variable y utilizarla en el fragmento, siga estos pasos:

1. Abra el fragmento de expresión y edite su contenido en el editor de personalización. Para los componentes de HTML, seleccione el componente en el fragmento y haga clic en el botón **Mostrar código fuente**.

   ![](assets/fragment-html-edit.png)

1. Declare la variable que desea que los usuarios editen. Vaya al menú **Funciones de ayuda** en el panel de navegación izquierdo y agregue la función de ayuda **inline**. La sintaxis para declarar y llamar a la variable se agrega automáticamente al contenido.

   ![](assets/fragment-add-helper.png)

1. Reemplace `"name"` con un identificador único para identificar el campo editable.

   >[!NOTE]
   >
   >El ID de campo debe ser único y no debe tener espacios. Este ID debe utilizarse en cualquier lugar del contenido donde desee mostrar el valor de la variable.

1. Adapte la sintaxis para adaptarla a sus necesidades añadiendo parámetros detallados en la siguiente tabla:

   | Acción | Parámetro | Ejemplo |
   | ------- | ------- | ------- |
   | Declarar un campo editable con un **valor predeterminado**. Al añadir el fragmento al contenido, se utiliza este valor predeterminado si no lo personaliza. | Agregue el valor predeterminado entre las etiquetas en línea. | `{{#inline "editableFieldID"}}default_value{{/inline}}` |
   | Defina una **etiqueta** para el campo editable. Esta etiqueta se muestra en el Designer de correo electrónico al editar los campos del fragmento. | `name="title"` | `{{#inline "editableFieldID" name="title"}}default_value{{/inline}}` |
   | Declare un campo editable que contenga un **origen de imagen** que deba publicarse. | `assetType="image"` | `{{#inline "editableFieldID" assetType="image"}}default_value{{/inline}}` |
   | Declare un campo editable que contenga una **URL** de la que deba realizarse un seguimiento.<br/>Tenga en cuenta que los bloques predefinidos &quot;URL de página espejo&quot; y &quot;Vínculo de cancelación de suscripción&quot; predeterminados no pueden convertirse en campos editables. | `assetType="url"` | `{{#inline "editableFieldID" assetType="url"}}default_value{{/inline}}` |

1. Utilice la sintaxis `{{{name}}}` en su código en cada lugar donde desee mostrar el valor del campo editable. Reemplazar `name` por el ID único del campo definido anteriormente.

   ![](assets/fragment-call-variable.png)

1. Guarde el fragmento.

Al añadir el fragmento al contenido de su correo electrónico, los usuarios ahora pueden anular los valores predeterminados de las variables con los valores que hayan elegido:

* Para los fragmentos de expresiones, se utiliza una sintaxis específica para anular los valores de las variables. [Aprenda a personalizar campos editables en un fragmento de expresión](../personalization/use-expression-fragments.md#customize-fields)

* Para los componentes del HTML, la variable se muestra en la lista de campos editables de la Designer de correo electrónico. [Aprenda a personalizar campos editables en un fragmento visual](../email/use-visual-fragments.md#customize-fields)

## Ejemplo de fragmento de expresión editable {#example}

En el ejemplo siguiente, se crea un fragmento de expresión que presenta nuevas colecciones deportivas. De manera predeterminada, el fragmento muestra este contenido: *¿Busca más? ¡No se pierda nuestra última colección de deportes!*

Queremos permitir que los usuarios reemplacen &quot;deportes&quot; en este contenido por el deporte de su elección. Por ejemplo: *¿Busca más? ¡No se pierda nuestra última colección de yoga!*

Para ello:

1. Declare una variable &quot;sport&quot; con el ID &quot;sport&quot;.

   De manera predeterminada, si los usuarios no cambian el valor de la variable después de agregar el fragmento en su contenido, se mostrará el valor definido entre las etiquetas `{{#inline}}` y `{{/inline}}`, por ejemplo, &quot;deportes&quot;.

1. Agregue la sintaxis ``{{{sport}}}`` al contenido del fragmento donde desee mostrar el valor de la variable, es decir, &quot;deportes&quot; de forma predeterminada o el valor elegido por los usuarios.

   ![](assets/fragment-expression-custom.png)

1. Al agregar el fragmento de expresión a su contenido, los usuarios pueden cambiar el valor de la variable con su elección directamente desde el editor de expresiones. [Aprenda a personalizar campos editables en un fragmento de expresión](../personalization/use-expression-fragments.md#customize-fields)

   ![](assets/fragment-expression-use.png)
