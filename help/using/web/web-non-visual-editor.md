---
title: Edición de contenido mediante el editor no visual
description: Aprenda a crear una página web y editar su contenido con el editor no visual de Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Experienced
exl-id: 00d2fc73-3ac8-421c-982a-0f3ec7e3dacd
source-git-commit: f5df65a0225754ab66fb2ffa33c5130f7137b644
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Uso del editor no visual web {#web-non-visual-editor}

Además del [!DNL Journey Optimizer] diseñador web [visual](web-visual-editor.md), también puede agregar modificaciones a sus páginas web usando un **editor no visual**.

Esto puede resultar útil si no puede instalar o no se le permite instalar extensiones de explorador como [Adobe Experience Cloud Visual Helper](web-prerequisites.md#visual-authoring-prerequisites), que es necesario para cargar las páginas en el diseñador web.

En algunos casos, también es posible que le resulte más fácil utilizar un editor no visual para aplicar modificaciones en un selector CSS concreto, sin el riesgo de modificar otros elementos en una página web o de cambiar la estructura de la página.

Para crear sus experiencias web con el editor no visual, siga los pasos a continuación.

1. En la pantalla **[!UICONTROL Editar contenido]** del recorrido o la campaña, anule la selección de la opción **[!UICONTROL Editor visual]**.

1. Haga clic en **[!UICONTROL Agregar una modificación]** para empezar a editar el contenido web.

   ![](assets/web-campaign-add-modification-button.png)

1. Se muestra el editor no visual. Puede añadir la primera modificación mediante el panel izquierdo.

   ![](assets/web-non-visual-editor.png)

1. En la lista desplegable, seleccione el tipo de modificación.

   Hay dos tipos disponibles. Vienen con diferentes opciones. Consulte los vínculos siguientes para obtener más información:

   * **[!UICONTROL Selector de CSS]** - [Más información](manage-web-modifications.md#css-selector)
   * **[!UICONTROL Página`<head>`]** - [Más información](manage-web-modifications.md#page-head)

1. Haga clic en el botón **[!UICONTROL Agregar personalización]**. Se abre el editor de personalización.

   Puede aprovechar el editor de personalización [!DNL Journey Optimizer] con todas sus capacidades de personalización y creación. [Más información](../personalization/personalization-build-expressions.md)

1. Escribe tu contenido y **[!UICONTROL guarda]** tus cambios.

   ![](assets/web-non-visual-editor-ex-save.png)

1. La primera modificación se muestra en la parte superior del panel **[!UICONTROL Modificaciones]**.

   Haga clic en el botón **[!UICONTROL Más acciones]** que está junto a la modificación y seleccione **[!UICONTROL Información]** para mostrar sus detalles. También puede **[!UICONTROL eliminar la modificación]** si es necesario.

   ![](assets/web-non-visual-editor-ex-more.png){width="50%" align="left"}

   >[!NOTE]
   >
   >El panel **[!UICONTROL Modificaciones]** es el mismo que al usar el [diseñador web](web-visual-editor.md). Todas las acciones que puede realizar con él se detallan en [esta sección](manage-web-modifications.md#use-modifications-pane).

1. Haga clic en el botón **[!UICONTROL Agregar]** en la parte superior del panel **[!UICONTROL Modificaciones]** para agregar otra modificación y repita los pasos anteriores.


1. Además, puede seleccionar cualquier elemento del sitio web y rastrear los clics en ese elemento. Para habilitar el rastreo de clics y definir las acciones que desea rastrear, haga clic en el segundo icono del carril izquierdo, como se muestra a continuación:

   ![](assets/web-campaign-click.png){width="50%" align="left"}

   Use el botón **Agregar componente** para seleccionar una nueva acción que rastrear. Obtenga más información acerca del uso del rastreo de clics en [esta sección](monitor-web-experiences.md#use-click-tracking).


1. Haga clic en la flecha de la parte superior izquierda de la pantalla para volver a la pantalla de edición de recorrido o campaña. Puede ver la cantidad actual de cambios y agregar más.

   ![](assets/web-campaign-modifications.png)

   También puede cambiar al diseñador web si lo desea. Se conservarán todas las modificaciones.
