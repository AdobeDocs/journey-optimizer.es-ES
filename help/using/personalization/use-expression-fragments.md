---
solution: Journey Optimizer
product: journey optimizer
title: Usar fragmentos de expresión
description: Aprenda a utilizar fragmentos de expresiones en [!DNL Journey Optimizer] Editor de expresiones.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expresión, editor, biblioteca, personalización
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: 623aa2ee317553eaebfb16c350a69672de2866a1
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Aprovechamiento de fragmentos de expresiones {#use-expression-fragments}

Al utilizar el Editor de expresiones, puede aprovechar todos los fragmentos de expresiones que se han creado o guardado en la zona protegida actual.

Obtenga información sobre cómo crear y administrar fragmentos en [esta sección](../content-management/fragments.md).

➡️ [Aprenda a administrar, crear y utilizar fragmentos en este vídeo](../content-management/fragments.md#video-fragments)

## Usar un fragmento de expresión {#use-expression-fragment}

Para añadir fragmentos de expresión al contenido, siga los pasos a continuación.

1. Abra el [Editor de expresiones](personalization-build-expressions.md) y seleccione la **[!UICONTROL Fragmentos]** en el panel izquierdo.

   ![](assets/expression-fragments-pane.png)

   La lista muestra todos los fragmentos de expresiones que se han creado o guardado como fragmentos en la zona protegida actual. [Más información](../content-management/fragments.md#create-expression-fragment)

   >[!NOTE]
   >
   >Los fragmentos se ordenan por fecha de creación: los fragmentos de expresión añadidos recientemente se muestran primero en la lista.

1. También puede actualizar la lista.

   >[!NOTE]
   >
   >Si se han modificado o agregado fragmentos mientras edita el contenido, la lista se actualizará con los cambios más recientes.

1. Haga clic en el icono + junto a un fragmento de expresión para insertar el ID de fragmento correspondiente en el editor.

   ![](assets/expression-fragment-add.png)

   Una vez agregado el ID de fragmento, si abre el fragmento de expresión correspondiente y [editarlo](../content-management/fragments.md#edit-fragments) desde la interfaz de, los cambios se sincronizan. Se propagan automáticamente a todos los **[!UICONTROL Borrador]** recorridos o campañas que contengan ese ID de fragmento.

   >[!NOTE]
   >
   >Los cambios no se propagan al contenido utilizado en **[!UICONTROL Activo]** recorridos o campañas.

1. Haga clic en **[!UICONTROL Más acciones]** junto a un fragmento.

1. En el menú contextual que se abre, seleccione **[!UICONTROL Ver fragmento]** para obtener más información sobre ese fragmento. El **[!UICONTROL ID de fragmento]** también se muestra y se puede copiar desde aquí.

   ![](assets/expression-fragment-view.png)

1. Puede abrir el fragmento de expresión en otra ventana para editar su contenido y propiedades, ya sea mediante la variable **[!UICONTROL Abrir fragmento]** en el menú contextual o desde la opción **[!UICONTROL Información del fragmento]** panel. [Obtenga información sobre cómo editar un fragmento](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. A continuación, puede personalizar y validar el contenido de la forma habitual mediante todas las funcionalidades de personalización y creación de la [Editor de expresiones](personalization-build-expressions.md).

>[!NOTE]
>
>Si crea un fragmento de expresión que contiene varios saltos de línea y lo utiliza en [SMS](../sms/create-sms.md#sms-content) o [push](../push/design-push.md) contenido, se conservan los saltos de línea. Por lo tanto, asegúrese de probar su [SMS](../sms/send-sms.md) o [push](../push/send-push.md) antes de enviarlo.

## Romper herencia {#break-inheritance}

Al agregar un ID de fragmento al Editor de expresiones, se sincronizan los cambios realizados en el fragmento de expresión original.

Sin embargo, también puede pegar el contenido de un fragmento de expresión en el editor. En el menú contextual, seleccione **[!UICONTROL Pegar fragmento]** para insertar ese contenido.

![](assets/expression-fragment-paste.png)

En ese caso, la herencia del fragmento original se interrumpe. El contenido del fragmento se copia en el editor y los cambios ya no se sincronizan.

Se convierte en un elemento independiente que ya no está vinculado al fragmento original; puede editarlo como cualquier otro elemento del código.

