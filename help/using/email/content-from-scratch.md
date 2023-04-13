---
solution: Journey Optimizer
product: journey optimizer
title: Diseño de contenido desde cero en Journey Optimizer
description: Aprenda a diseñar su contenido desde cero
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: contenido, editor, correo electrónico, iniciar
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 4ce8573aa76ceae807d404e736b2d780f687aa56
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Diseño de contenido desde cero {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="Añadir componentes de estructura"
>abstract="Los componentes de estructura definen el diseño del correo electrónico. Arrastre y suelte una **Estructura** en el lienzo para empezar a diseñar el contenido del correo electrónico."

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="Añadir componentes de estructura"
>abstract="Los componentes de estructura definen el diseño de la página de aterrizaje. Arrastre y suelte una **Estructura** en el lienzo para empezar a diseñar el contenido de la página de aterrizaje."

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="Añadir componentes de estructura"
>abstract="Los componentes de estructura definen el diseño del fragmento. Arrastre y suelte una **Estructura** en el lienzo para empezar a diseñar el contenido del fragmento."

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="Añadir componentes de estructura"
>abstract="Los componentes de estructura definen el diseño de la plantilla. Arrastre y suelte una **Estructura** en el lienzo para empezar a diseñar el contenido de la plantilla."


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="Definir columnas de correo electrónico"
>abstract="El Diseñador de correo electrónico le permite definir fácilmente el diseño del correo electrónico seleccionando la estructura de columna."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="Definir columnas de página de aterrizaje"
>abstract="Designer permite definir fácilmente el diseño de la página de aterrizaje mediante la selección de la estructura de columnas."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="Definir columnas de fragmento"
>abstract="Designer permite definir fácilmente el diseño del fragmento seleccionando la estructura de columna."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="Definir columnas de plantilla"
>abstract="Designer permite definir fácilmente el diseño de la plantilla mediante la selección de la estructura de columna."


Utilice Adobe Journey Optimizer Designer para definir fácilmente la estructura del contenido. Al agregar y mover elementos estructurales con simples acciones de arrastrar y soltar, puede diseñar la forma de su contenido en cuestión de segundos.

Para comenzar a crear el contenido, siga los pasos a continuación:

1. En la página de inicio de Designer, seleccione la **[!UICONTROL Diseño desde cero]** .

   ![](assets/email_designer.png)

1. Empiece a diseñar el contenido arrastrando y soltando **[!UICONTROL Estructuras]** en el lienzo para definir el diseño del correo electrónico.

   >[!NOTE]
   >
   >El apilamiento de columnas no es compatible con todos los programas de correo electrónico. Cuando no se admita, las columnas no se apilarán.

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. Agregar tantos **[!UICONTROL Estructuras]** según sea necesario y edite su configuración en el panel dedicado de la derecha.

   ![](assets/email_designer_structure_components.png)

   Seleccione el **[!UICONTROL columna n:n]** para definir el número de columnas que elija (entre 3 y 10). También puede definir el ancho de cada columna moviendo las flechas en la parte inferior de cada columna.

   >[!NOTE]
   >
   >Cada tamaño de columna no puede ser inferior al 10 % de la anchura total del componente de estructura. No se puede quitar una columna que no esté vacía.

1. Expanda el **[!UICONTROL Contenido]** y añada tantos elementos como necesite en uno o varios componentes de estructura. [Descubra más información sobre los componentes de contenido](content-components.md)

1. Cada componente se puede personalizar aún más mediante el **[!UICONTROL Configuración]** o **[!UICONTROL Estilo]** en el menú de la derecha. Por ejemplo, puede cambiar el estilo, el relleno o el margen del texto de cada componente. [Obtenga más información sobre la alineación y el relleno](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. En el **[!UICONTROL Selector de recursos]**, puede seleccionar directamente los recursos almacenados en la variable **[!UICONTROL Biblioteca de activos]**. [Obtenga más información sobre la administración de recursos](assets-essentials.md)

   Haga doble clic en la carpeta que contiene los recursos. Arrástrelos y suéltelos en un componente de estructura.

   ![](assets/email_designer_asset_picker.png)

1. Inserte campos de personalización para personalizar el contenido a partir de atributos de perfiles, suscripciones a segmentos, atributos contextuales, etc. [Descubra más información sobre la personalización del contenido](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. Haga clic en **[!UICONTROL Habilitar contenido de condición]** para añadir contenido dinámico y adaptar el contenido a los perfiles de destino según las reglas condicionales. [Introducción al contenido dinámico](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. Haga clic en el **[!UICONTROL Vínculos]** del panel izquierdo para mostrar todas las direcciones URL del contenido que se rastreará. Puede modificar sus **[!UICONTROL Tipo de seguimiento]** o **[!UICONTROL Etiqueta]** y agregue **[!UICONTROL Etiquetas]** si es necesario. [Obtenga más información sobre los vínculos y el seguimiento](message-tracking.md)

   ![](assets/email_designer_links.png)

1. Si es necesario, puede personalizar aún más el contenido haciendo clic en **[!UICONTROL Cambiar al editor de código]** desde la parte superior **Más** botón. [Obtenga más información sobre el editor de código](code-content.md)

   ![](assets/email_designer_switch-to-code.png)

   >[!CAUTION]
   >
   >No puede volver al diseñador visual para este contenido después de cambiar al editor de código.

1. Una vez que el contenido esté listo, haga clic en el botón **[!UICONTROL Simular contenido]** para comprobar la renderización. Puede elegir la vista de escritorio o la vista móvil. [Obtenga más información sobre la vista previa del correo electrónico](preview.md)

   ![](assets/email_designer_simulate_content.png)

1. Cuando el contenido esté listo, haga clic en **[!UICONTROL Guardar]**.

