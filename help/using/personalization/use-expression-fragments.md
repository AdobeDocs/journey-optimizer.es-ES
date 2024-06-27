---
solution: Journey Optimizer
product: journey optimizer
title: Usar fragmentos de expresión
description: Aprenda a utilizar fragmentos de expresiones en [!DNL Journey Optimizer] editor de personalización.
feature: Personalization, Fragments
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expresión, editor, biblioteca, personalización
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: e6924928e03d494817a2368b33997029ca2eca1c
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Aprovechamiento de fragmentos de expresiones {#use-expression-fragments}

Al usar el **editor de personalización** Además, puede aprovechar todos los fragmentos de expresiones que se han creado o guardado en la zona protegida actual.

Un fragmento es un componente reutilizable al que se puede hacer referencia en [!DNL Journey Optimizer] campañas y recorridos. Esta funcionalidad permite generar previamente varios bloques de contenido personalizados que los usuarios de marketing pueden utilizar para ensamblar contenido rápidamente en un proceso de diseño mejorado. [Obtenga información sobre cómo crear y administrar fragmentos](../content-management/fragments.md).

➡️ [Aprenda a administrar, crear y utilizar fragmentos en este vídeo](../content-management/fragments.md#video-fragments)

## Usar un fragmento de expresión {#use-expression-fragment}

Para añadir fragmentos de expresión al contenido, siga los pasos a continuación.

>[!NOTE]
>
>Puede añadir hasta 30 fragmentos en una entrega determinada. Los fragmentos solo se pueden anidar hasta 1 nivel.

1. Abra el [editor de personalización](personalization-build-expressions.md) y seleccione la **[!UICONTROL Fragmentos]** en el panel izquierdo.

   La lista muestra todos los fragmentos de expresiones que se han creado o guardado como fragmentos en la zona protegida actual. Se ordenan por fecha de creación: los fragmentos de expresión añadidos recientemente se muestran primero en la lista. [Más información](../content-management/fragments.md#create-expression-fragment)

   ![](assets/expression-fragments-pane.png)

   También puede actualizar esta lista.

   >[!NOTE]
   >
   >Si se han modificado o agregado fragmentos mientras edita el contenido, la lista se actualizará con los cambios más recientes.

1. Haga clic en el icono + junto a un fragmento de expresión para insertar el ID de fragmento correspondiente en el editor.

   ![](assets/expression-fragment-add.png)

   >[!CAUTION]
   >
   >Puede añadir cualquiera **Borrador** o **Activo** a su contenido. Sin embargo, no podrá activar su recorrido o campaña si se está utilizando un fragmento con el estado Borrador. En el momento de la publicación del recorrido o de la campaña, los fragmentos de borrador mostrarán un error y deberá aprobarlos para poder publicarlos.

1. Una vez agregado el ID de fragmento, si abre el fragmento de expresión correspondiente y [editarlo](../content-management/fragments.md#edit-fragments) desde la interfaz de, los cambios se sincronizan. Se propagan automáticamente a todos los recorridos o campañas en borrador o activos que contengan ese ID de fragmento.

1. Haga clic en **[!UICONTROL Más acciones]** junto a un fragmento. En el menú contextual que se abre, seleccione **[!UICONTROL Ver fragmento]** para obtener más información sobre ese fragmento. El **[!UICONTROL ID de fragmento]** también se muestra y se puede copiar desde aquí.

   ![](assets/expression-fragment-view.png)

1. Puede abrir el fragmento de expresión en otra ventana para editar su contenido y propiedades, ya sea mediante la variable **[!UICONTROL Abrir fragmento]** en el menú contextual o desde la opción **[!UICONTROL Información del fragmento]** panel. [Obtenga información sobre cómo editar un fragmento](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. A continuación, puede personalizar y validar el contenido de la forma habitual mediante todas las funcionalidades de personalización y creación de la [editor de personalización](personalization-build-expressions.md).

>[!NOTE]
>
>Si crea un fragmento de expresión que contiene varios saltos de línea y lo utiliza en [SMS](../sms/create-sms.md#sms-content) o [push](../push/design-push.md) contenido, se conservan los saltos de línea. Por lo tanto, asegúrese de probar su [SMS](../sms/send-sms.md) o [push](../push/send-push.md) antes de enviarlo.

## Personalizar campos editables {#customize-fields}

Si se han hecho editables ciertas partes de un fragmento de expresión mediante variables, puede anular sus valores predeterminados con una sintaxis específica. [Aprenda a personalizar los fragmentos](../content-management/customizable-fragments.md)

Para personalizar los campos, siga estos pasos:

1. Inserte el fragmento en el código desde el **Fragmentos** menú.

1. Utilice el `<fieldId>="<value>"` código al final de la sintaxis para anular el valor predeterminado de la variable.

   En el ejemplo siguiente, anulamos el valor de una variable cuyo ID es &quot;sports&quot; con el valor &quot;yoga&quot;. Esto mostrará &quot;yoga&quot; en el contenido del fragmento en todas partes donde se haga referencia a la variable &quot;sport&quot;.

   ![](../content-management/assets/fragment-expression-use.png)

Un ejemplo que muestra cómo añadir campos editables a fragmentos de expresión y anular sus valores al crear un correo electrónico está disponible en [esta sección](../content-management/customizable-fragments.md#example).

## Romper herencia {#break-inheritance}

Al agregar un ID de fragmento al editor de personalización, se sincronizan los cambios realizados en el fragmento de expresión original.

Sin embargo, también puede pegar el contenido de un fragmento de expresión en el editor. En el menú contextual, seleccione **[!UICONTROL Pegar fragmento]** para insertar ese contenido.

![](assets/expression-fragment-paste.png)

En ese caso, la herencia del fragmento original se interrumpe. El contenido del fragmento se copia en el editor y los cambios ya no se sincronizan.

Se convierte en un elemento independiente que ya no está vinculado al fragmento original; puede editarlo como cualquier otro elemento del código.

