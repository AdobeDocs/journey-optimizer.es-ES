---
solution: Journey Optimizer
product: journey optimizer
title: Crear un fragmento
description: Aprenda a crear fragmentos para reutilizar contenido en campañas y recorridos de Journey Optimizer
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: da3ffe9c-a244-4246-b4b5-a3a1d0508676
source-git-commit: c42fc1069e11b8e34b7477fc26ed8a6b4ef95ac7
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 14%

---

# Crear un fragmento {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Selección del tipo visual"
>abstract="Cree un fragmento visual independiente para que el contenido se pueda reutilizar en un correo electrónico dentro de un recorrido, una campaña o una plantilla de contenido."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments" text="Añadir fragmentos visuales a los correos electrónicos"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Selección del tipo de expresión"
>abstract="Cree un fragmento de expresión independiente para que el contenido se pueda reutilizar en varios recorridos y campañas. Al utilizar el editor de personalización, puede aprovechar todos los fragmentos de expresiones que se han creado en la zona protegida actual."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html?lang=es" text="Aprovechamiento de fragmentos de expresiones"

Los fragmentos se pueden crear desde cero desde el **[!UICONTROL Fragmentos]** menú izquierdo. Además, también puede guardar una parte del contenido existente como fragmento al diseñar contenido. [Descubra cómo](#save-as-fragment)

Una vez guardado, el fragmento está disponible para utilizarlo en un recorrido, una campaña o una plantilla. Puede utilizar este fragmento al crear contenido dentro de recorridos y campañas. Consulte [Añadir fragmentos visuales](../email/use-visual-fragments.md) y [Aprovechamiento de fragmentos de expresiones](../personalization/use-expression-fragments.md)

Para crear un fragmento, siga los pasos a continuación.

## Definir las propiedades del fragmento {#properties}

1. Acceda a la lista de fragmentos a través de **[!UICONTROL Gestión de contenido]** > **[!UICONTROL Fragmentos]** menú izquierdo.

1. Seleccionar **[!UICONTROL Crear fragmento]** y rellene el nombre y la descripción del fragmento (si es necesario).

   ![](assets/fragment-details.png)

1. Seleccione o cree etiquetas de Adobe Experience Platform en **[!UICONTROL Etiquetas]** para categorizar el fragmento y mejorar la búsqueda. [Aprenda a trabajar con etiquetas unificadas](../start/search-filter-categorize.md#tags)

1. Seleccione el tipo de fragmento: **Fragmento visual** o **Fragmento de expresión**. [Más información sobre los fragmentos visuales y de expresión](../content-management/fragments.md#visual-expression)

   >[!NOTE]
   >
   >Por ahora, los fragmentos visuales están disponibles para **Correo electrónico** solo canal.

1. Si está creando un fragmento de expresión, seleccione el tipo de código que desea utilizar: **[!UICONTROL HTML]**, **[!UICONTROL JSON]** o **[!UICONTROL Texto]**.

   ![](assets/fragment-expression-type.png)

1. Para asignar etiquetas de uso de datos personalizadas o principales al fragmento, haga clic en **[!UICONTROL Administrar acceso]** en la sección superior de la pantalla. [Obtenga más información sobre el Control de acceso de nivel de objeto (OLAC)](../administration/object-based-access.md).

1. Clic **[!UICONTROL Crear]** para diseñar el contenido del fragmento.

## Diseño del contenido del fragmento {#content}

Después de configurar las propiedades del fragmento, se abre Email Designer o el editor de personalización, según el tipo de fragmento que esté creando.

* Para los fragmentos visuales, edite el contenido según sea necesario, del mismo modo que lo haría para cualquier correo electrónico dentro de un recorrido o una campaña. [Más información](../email/get-started-email-design.md)

  ![](assets/fragment-designer.png)

* Para fragmentos de expresiones, aproveche la variable [!DNL Journey Optimizer] editor de personalización con todas sus funcionalidades de personalización y creación para crear el contenido del fragmento. [Más información](../personalization/personalization-build-expressions.md)

  ![](assets/fragment-expression-editor.png)

Cuando el contenido esté listo, haga clic en **Guardar** botón. El fragmento se crea y se añade a la lista de fragmentos con la variable **Borrador** estado. Puede previsualizarlo y publicarlo para que esté disponible en recorridos y campañas.

## Previsualización y publicación del fragmento {#publish}

>[!NOTE]
>
>Para publicar un fragmento, debe tener [Fragmento de Publish](../administration/ootb-product-profiles.md#content-library-manager) permiso de usuario.

Si el fragmento está listo para su publicación, puede previsualizarlo y publicarlo para que esté disponible en sus recorridos y campañas. Para ello, siga estos pasos:

1. Vuelva a la pantalla de creación de fragmentos después de diseñar su contenido o ábralo desde la lista de fragmentos.

1. Una vista previa del fragmento está disponible en la **Etiquetas** , lo que permite comprobar su renderización. Si necesita realizar algún cambio, haga clic en **Editar** en la sección superior de la pantalla para abrir el Designer de correo electrónico o el editor de personalización en función del tipo de fragmento.

   ![](assets/fragment-preview.png)

1. Haga clic en **Publish** en la esquina superior derecha para publicar el fragmento.

   Si el fragmento se está utilizando en un recorrido o campaña en directo, se abre un mensaje para informarle. Haga clic en **Ver más** para acceder a la lista de recorridos o campañas donde se hace referencia. [Aprenda a explorar referencias de un fragmento](../content-management/manage-fragments.md#explore-references)

   Clic **Confirmar** para publicar el fragmento y actualizarlo en los recorridos o campañas en directo que lo estén utilizando.

   ![](assets/fragment-publish.png){width="70%" align="center"}

El fragmento ahora está **Activo** y está disponible al crear contenido dentro de la variable [!DNL Journey Optimizer] Correo electrónico del editor de Designer o personalización:

* [Aprenda a utilizar fragmentos visuales](../email/use-visual-fragments.md)
* [Aprenda a utilizar fragmentos de expresiones](../personalization/use-expression-fragments.md)
