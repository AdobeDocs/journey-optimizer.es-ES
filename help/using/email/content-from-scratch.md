---
solution: Journey Optimizer
product: journey optimizer
title: Diseño de contenido desde cero en Journey Optimizer
description: Aprenda a diseñar el contenido desde cero
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: contenido, editor, correo electrónico, inicio
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 57%

---

# Diseño de contenido desde cero {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="Adición de componentes de estructura"
>abstract="Los componentes de estructura definen el diseño del correo electrónico. Arrastre y suelte un componente **Estructura** en el lienzo para empezar a diseñar el contenido del correo electrónico."

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="Adición de componentes de estructura"
>abstract="Los componentes de estructura definen el diseño de la página de aterrizaje. Arrastre y suelte un componente **Estructura** en el lienzo para empezar a diseñar el contenido de la página de aterrizaje."

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="Adición de componentes de estructura"
>abstract="Los componentes de estructura definen el diseño del fragmento. Arrastre y suelte un componente **Estructura** en el lienzo para empezar a diseñar el contenido del fragmento."

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="Adición de componentes de estructura"
>abstract="Los componentes de estructura definen el diseño de la plantilla. Arrastre y suelte un componente **Estructura** en el lienzo para empezar a diseñar el contenido de la plantilla."


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="Definición de columnas de correo electrónico"
>abstract="El diseñador de correo electrónico permite definir fácilmente el diseño del correo electrónico mediante la selección de la estructura de columnas."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="Definición de columnas de página de aterrizaje"
>abstract="El diseñador permite definir fácilmente el diseño de la página de aterrizaje mediante la selección de la estructura de columnas."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="Definición de columnas de fragmento"
>abstract="El diseñador permite definir fácilmente el diseño del fragmento mediante la selección de la estructura de columnas."

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="Definición de columnas de plantilla"
>abstract="El diseñador permite definir fácilmente el diseño de la plantilla mediante la selección de la estructura de columnas."


Utilice Adobe Journey Optimizer Designer para definir fácilmente la estructura del contenido. Al agregar y mover elementos estructurales con simples acciones de arrastrar y soltar, puede diseñar la forma del contenido en cuestión de segundos.

Para empezar a crear contenido, siga los pasos a continuación:

1. En la página de inicio de Designer, seleccione **[!UICONTROL Diseñe desde cero]** opción.

   ![](assets/email_designer.png)

1. Para diseñar el contenido, arrastre y suelte **[!UICONTROL Estructuras]** en el lienzo para definir el diseño del correo electrónico.

   >[!NOTE]
   >
   >El apilado de columnas no es compatible con todos los programas de correo electrónico. Cuando no se admite, las columnas no se apilan.

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. Añadir tantos como sea necesario **[!UICONTROL Estructuras]** si es necesario, y edite su configuración en el panel dedicado de la derecha.

   ![](assets/email_designer_structure_components.png)

   Seleccione el componente **[!UICONTROL columna n:n]** para definir el número de columnas que elija (entre 3 y 10). También puede definir la anchura de cada columna moviendo las flechas en la parte inferior de cada columna.

   >[!NOTE]
   >
   >Cada tamaño de columna no puede ser inferior al 10 % de la anchura total del componente de la estructura. No se puede quitar una columna que no esté vacía.

1. Expanda el **[!UICONTROL Contenido]** y añada tantos elementos como necesite a uno o más componentes de estructura. [Más información sobre los componentes de contenido](content-components.md)

1. Cada componente se puede personalizar aún más mediante la variable **[!UICONTROL Configuración]** o **[!UICONTROL Estilo]** pestañas en el menú derecho. Por ejemplo, puede cambiar el estilo, el relleno o el margen del texto de cada componente. [Obtenga más información sobre la alineación y el relleno](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. Desde el **[!UICONTROL Selector de recursos]**, puede seleccionar directamente los recursos almacenados en el **[!UICONTROL Biblioteca de recursos]**. [Más información sobre la administración de recursos](assets-essentials.md)

   Haga doble clic en la carpeta que contiene los recursos. Arrástrelos y suéltelos en un componente de estructura.

   ![](assets/email_designer_asset_picker.png)

1. Inserte campos de personalización para personalizar el contenido desde atributos de perfiles, suscripciones a segmentos, atributos contextuales, etc. [Más información sobre la personalización de contenido](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. Clic **[!UICONTROL Habilitar contenido de condición]** para añadir contenido dinámico y adaptar el contenido a los perfiles de destino según las reglas condicionales. [Introducción al contenido dinámico](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. Haga clic en **[!UICONTROL Vínculos]** del panel izquierdo para mostrar todas las direcciones URL del contenido de las que se realizará un seguimiento. Puede modificar sus **[!UICONTROL Tipo de seguimiento]** o **[!UICONTROL Etiqueta]** y agregue **[!UICONTROL Etiquetas]** si es necesario. [Más información sobre los vínculos y el seguimiento](message-tracking.md)

   ![](assets/email_designer_links.png)

1. Si es necesario, puede personalizar aún más el correo electrónico haciendo clic en **[!UICONTROL Cambiar al editor de código]** en el menú avanzado. Esto le permite editar el código fuente del correo electrónico, por ejemplo, para agregar etiquetas HTML personalizadas o de seguimiento. [Obtenga más información sobre el editor de código](code-content.md)

   >[!CAUTION]
   >
   >No puede volver al diseñador visual para este correo electrónico después de cambiar al editor de código.

1. Una vez que el contenido esté listo, haga clic en **[!UICONTROL Simular contenido]** para comprobar la renderización. Puede elegir la vista de escritorio o la vista móvil. [Obtenga más información sobre la vista previa del correo electrónico](preview.md)

   ![](assets/email_designer_simulate_content.png)

1. Cuando el contenido esté listo, haga clic en **[!UICONTROL Guardar]**.

