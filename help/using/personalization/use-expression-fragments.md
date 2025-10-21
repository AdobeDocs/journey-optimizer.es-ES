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
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 0%

---

# Aprovechamiento de fragmentos de expresiones {#use-expression-fragments}

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
>Si crea un fragmento de expresión que contiene varios saltos de línea y lo utiliza en el contenido [SMS](../sms/create-sms.md#sms-content) o [push](../push/design-push.md), se conservarán los saltos de línea. Por lo tanto, asegúrese de probar su mensaje [SMS](../sms/send-sms.md) o [push](../push/send-push.md) antes de enviarlo.

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


## Personalizar campos editables {#customize-fields}

Si se han hecho editables ciertas partes de un fragmento de expresión mediante variables, puede anular sus valores predeterminados con una sintaxis específica. [Aprenda a personalizar los fragmentos](../content-management/customizable-fragments.md)

Para personalizar los campos, siga estos pasos:

1. Inserte el fragmento en su código desde el menú **[!UICONTROL Fragmentos]**.

1. Utilice el código `<fieldId>="<value>"` al final de la sintaxis para anular el valor predeterminado de la variable.

   En el ejemplo siguiente, anulamos el valor de una variable cuyo ID es &quot;sports&quot; con el valor &quot;yoga&quot;. Esto mostrará &quot;yoga&quot; en el contenido del fragmento en todas partes donde se haga referencia a la variable &quot;sport&quot;.

   ![](../content-management/assets/fragment-expression-use.png)

Un ejemplo que muestra cómo agregar campos editables a fragmentos de expresión y anular sus valores al crear un correo electrónico está disponible en [esta sección](../content-management/customizable-fragments.md#example).

## Romper herencia {#break-inheritance}

Al agregar un ID de fragmento al editor de personalización, se sincronizan los cambios realizados en el fragmento de expresión original.

Sin embargo, también puede pegar el contenido de un fragmento de expresión en el editor. En el menú contextual, seleccione **[!UICONTROL Pegar fragmento]** para insertar ese contenido.

![](assets/expression-fragment-paste.png)

En ese caso, la herencia del fragmento original se interrumpe. El contenido del fragmento se copia en el editor y los cambios ya no se sincronizan.

Se convierte en un elemento independiente que ya no está vinculado al fragmento original; puede editarlo como cualquier otro elemento del código.

