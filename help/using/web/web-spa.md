---
title: Creación de aplicaciones de una sola página
description: SPA Obtenga información sobre cómo crear y aplicar modificaciones a distintas vistas de Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
source-git-commit: 59412ecbb8df74c7185b67593131c610d6da4148
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 6%

---

# Creación de aplicaciones de una sola página {#web-author-spas}

## Acerca de las vistas {#about-views}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications_views"
>title="Aplicar cambios a las vistas seleccionadas"
>abstract="Los cambios se aplicarán solamente a las vistas seleccionadas. Las vistas se pueden descubrir utilizando la variable **Examinar** y navegue hasta ellos. ¿No encuentra la vista que busca?"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es" text="Más información"

**Aplicaciones de una sola página** SPA (ahora) se puede crear en el editor visual del diseñador web. Esto le permite seleccionar a qué vistas específicas desea aplicar las modificaciones de la página web.

Una vista puede definirse como un sitio completo o como un grupo de elementos visuales en un sitio, como la página de inicio, la totalidad del sitio de productos o el marco de preferencias de envío en todas las páginas de cierre de compra.

Se necesita una configuración de desarrollador única para definir las vistas en la implementación del SDK web de Adobe Experience Platform. Esto le permite crear y ejecutar campañas web de Adobe Journey Optimizer SPA en el tiempo de ejecución de la.

## Definir vistas en la implementación del SDK web {#define-views}

Las vistas XDM se pueden aprovechar en el Adobe [!DNL Journey Optimizer] SPA para permitir a los especialistas en marketing ejecutar campañas de personalización y experimentación web en el editor visual web de la aplicación de la manera más rápida y eficaz. [Más información](web-spa-implementation.md)

Para poder acceder y crear vistas en la [!DNL Journey Optimizer] interfaz de usuario, asegúrese de seguir los pasos que se indican en [esta sección](web-spa-implementation.md#implement-xdm-views).

## Descubra vistas en el diseñador web {#discover-views}

SPA Una vez completada la configuración en la implementación del SDK web de Adobe Experience Platform, debe navegar por todas las vistas del sitio web a las que desee aplicar las modificaciones. Complete los siguientes pasos.

1. [Creación de una campaña web](create-web.md) y acceder a [diseñador web](edit-web-content.md).

   La vista en la que se encuentra actualmente se muestra en la parte superior izquierda.

   ![](assets/web-designer-view-home.png)

1. Cambiar a **[!UICONTROL Examinar]** modo. [Más información](../web/edit-web-content.md#browse-mode)

   ![](assets/web-designer-view-browse.png)

1. Navegue entre las diferentes páginas del sitio web para descubrirlas todas. El nombre de la vista que aparece en la parte superior cambia al pasar por otra página.

   ![](assets/web-designer-other-view.png)

## Aplicar modificaciones a otras vistas {#apply-modifications-views}

Una vez que haya añadido una modificación mientras se encuentra en una vista específica, puede aplicarla a otras vistas seleccionadas. Complete los siguientes pasos.

>[!CAUTION]
>
>Si no ha descubierto vistas utilizando **[!UICONTROL Examinar]** modo, no podrá seleccionarlos para aplicar las modificaciones. [Más información](#discover-views)

1. Seleccione el **[!UICONTROL Modificaciones]** para mostrar el panel correspondiente a la izquierda.

   ![](assets/web-designer-view-modifications-pane.png)

1. Seleccione cualquier modificación y haga clic en **[!UICONTROL Más acciones]** botón situado junto a él. Seleccionar **[!UICONTROL Aplicar a más vistas]**.

   ![](assets/web-designer-modifications-more-actions.png)

1. Seleccione las vistas a las que desee aplicar los cambios.

   ![](assets/web-designer-modifications-apply-to.png)

1. Haga clic en **[!UICONTROL Aplicar]**.

1. Cambiar a **[!UICONTROL Examinar]** modo para comprobar que las modificaciones se aplican en las páginas deseadas.

   ![](assets/web-designer-modifications-applied-view.png)