---
solution: Journey Optimizer
product: journey optimizer
title: Guardar contenido como fragmento
description: Aprenda a guardar contenido como fragmentos para reutilizarlo en campañas y recorridos de Journey Optimizer
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 70e88ea0-f2b0-4c13-8693-619741762429
source-git-commit: f47160f40abd9427cb9b9c793ee0ab402bf9f65b
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 2%

---

# Guardar contenido como fragmento {#save-as-fragment}

Al editar contenido en [!DNL Journey Optimizer], puede guardar todo o parte del contenido como fragmento para su reutilización futura.

## Guardar contenido como fragmento visual {#save-as-visual-fragment}

Al diseñar una [plantilla de contenido](content-templates.md) o un [email](../email/get-started-email-design.md) en una campaña o un recorrido, puede guardar una parte del contenido como fragmento visual. Para realizar esto, siga los pasos a continuación.

1. En el [Diseñador de correo electrónico](../email/get-started-email-design.md), haga clic en los puntos suspensivos en la parte superior derecha de la pantalla.

1. Seleccionar **[!UICONTROL Guardar como fragmento]** en el menú desplegable.

   ![](assets/fragment-save-as.png)

1. El **[!UICONTROL Guardar como fragmento]** se muestra. Seleccione los elementos que desee incluir en el fragmento, incluidos los campos de personalización y el contenido dinámico. Tenga en cuenta que los atributos contextuales no son compatibles con los fragmentos.

   >[!CAUTION]
   >
   >Sólo se pueden seleccionar secciones adyacentes entre sí. No puede seleccionar una estructura vacía u otro fragmento.

   ![](assets/fragment-save-as-screen.png)

1. Clic **[!UICONTROL Crear]**. Complete los detalles del fragmento, es decir, el nombre y la descripción (si es necesario).

1. Para asignar etiquetas de uso de datos personalizadas o principales al fragmento, seleccione **[!UICONTROL Administrar acceso]**. [Obtenga más información sobre el Control de acceso de nivel de objeto (OLAC)](../administration/object-based-access.md).

1. Seleccione o cree etiquetas de Adobe Experience Platform en **Etiquetas** para categorizar la plantilla y mejorar la búsqueda. [Más información](../start/search-filter-categorize.md#tags)

1. Clic **[!UICONTROL Crear]** otra vez. El fragmento se guardará en y se agregará a [lista de fragmentos](#access-manage-fragments), accesible desde el [!DNL Journey Optimizer] menú específico.

   Se convierte en un fragmento independiente que se puede [accedido](#access-manage-fragments), [editado](#edit-fragments) y [archivado](#archive-fragments) como cualquier otro elemento de esa lista.

Ahora puede utilizar este fragmento al crear cualquier [email](../email/get-started-email-design.md) o [plantilla de contenido](content-templates.md) dentro [!DNL Journey Optimizer]. [Descubra cómo](../email/use-visual-fragments.md)

>[!NOTE]
>
>Cualquier cambio en ese nuevo fragmento no se propaga al correo electrónico o a la plantilla de los que proviene. Del mismo modo, cuando el contenido original se edita dentro de ese correo electrónico o plantilla, el nuevo fragmento no se modifica.

## Guardar contenido como fragmento de expresión {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="Guardar como fragmento de expresión"
>abstract="El [!DNL Journey Optimizer] el editor de personalización permite guardar contenido como fragmentos de expresión. Estas expresiones están disponibles para crear contenido personalizado."

El [!DNL Journey Optimizer] el editor de personalización permite guardar contenido como fragmentos de expresión. Estas expresiones están disponibles para crear contenido personalizado.

Para guardar contenido como un fragmento de expresión, siga los pasos a continuación.

1. En el [editor de personalización](../personalization/personalization-build-expressions.md) interfaz, cree una expresión y haga clic en **[!UICONTROL Guardar como fragmento]**.

1. En el panel derecho, escriba un nombre y una descripción para la expresión con el fin de ayudar a los usuarios a encontrarla más fácilmente.

   ![](assets/expression-fragment-save-as.png)

1. Clic **[!UICONTROL Guardar fragmento]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. El fragmento de expresión se añade a [lista de fragmentos](#access-manage-fragments). Ahora puede utilizarlo para crear contenido personalizado.

>[!NOTE]
>
>Las expresiones no pueden superar los 200 KB.
