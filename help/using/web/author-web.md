---
title: Creación de páginas web
description: Obtenga información sobre cómo crear una página web y editar su contenido en Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 6%

---

# Creación de páginas web {#author-web}

>[!BEGINSHADEBOX]

Lo que encontrará en esta documentación:

* [Introducción al canal web](get-started-web.md)
* [Creación de experiencias web](create-web.md)
* **[Creación de páginas web](author-web.md)**
* [Extensión Ayuda de edición visual](visual-editing-helper.md)
* [Creación de informes web](web-report.md)

>[!ENDSHADEBOX]

Entrada [!DNL Journey Optimizer] La creación web se basa en la extensión de explorador Chrome Adobe Experience Cloud Visual Helper. [Más información](visual-editing-helper.md)

Para poder acceder y crear páginas web en [!DNL Journey Optimizer] interfaz de usuario, siga los requisitos previos enumerados en [esta sección](create-web.md#prerequesites).

## Editar contenido de página web {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Confirme la dirección URL que desea editar"
>abstract="Confirme la dirección URL de la página web específica que desea utilizar para editar el contenido que se aplicará en la superficie web definida anteriormente. La página web debe implementarse mediante el SDK web de Adobe Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es" text="Más información"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Introduzca la URL que desea editar"
>abstract="Introduzca la dirección URL de una página web específica que se utilizará para editar el contenido que se aplicará a todas las páginas que coincidan con la regla. La página web debe implementarse mediante el SDK web de Adobe Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es" text="Más información"

<!--Confirm the URL to use for authoring content on the surface. Typically the Authoring URL will be the surface URL itself, but you may include extra parameters if required. The page must include the Adobe Experience Platform Web SDK.-->

Una vez creada una acción web desde la campaña, puede editar el contenido con el diseñador web. Para ello, siga los pasos que aparecen a continuación.

>[!CAUTION]
>
>A ser accedido en [!DNL Journey Optimizer], la página web debe implementarse utilizando la variable [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"}.

1. Desde el **[!UICONTROL Acción]** de la campaña, seleccione **[!UICONTROL Editar contenido]** para empezar a crear la campaña web.

1. Si ha creado una regla de coincidencia de páginas, debe introducir cualquier dirección URL que coincida con esta regla. Los cambios se aplicarán a todas las páginas que coincidan con la regla.

   >[!NOTE]
   >
   >Si ha introducido una sola URL como superficie web, la URL que desea personalizar ya se ha rellenado.

   ![](assets/web-edit-enter-url.png)

1. Se muestra el contenido de la página.

   >[!CAUTION]
   >
   >La página web debe incluir [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"}.

1. Clic **[!UICONTROL Abrir diseñador web]** para editarlo. [Más información](author-web.md)

   ![](assets/web-open-designer.png)

1. Se muestra el diseñador web.

   ![](assets/web-designer.png)

1. Seleccione cualquier elemento del lienzo, como imagen, botón, párrafo, texto, contenedor, encabezado, vínculo, etc. y utilice:

   * Menú contextual para editar su contenido, diseño, inserción de vínculos o personalización, etc.

      ![](assets/web-designer-contextual-bar.png)

   * Los iconos de la parte superior del panel derecho para editar, duplicar, eliminar u ocultar cada elemento.

      ![](assets/web-designer-right-panel-icons.png)

   * Panel derecho que cambia dinámicamente según el elemento seleccionado. Por ejemplo, puede editar el fondo, la tipografía, el borde, el tamaño, la posición, el espaciado, los efectos o los estilos en línea de un elemento.

      ![](assets/web-designer-right-panel.png)

## Uso de componentes de contenido {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Añadir componentes de contenido a la página web"
>abstract="Puede agregar varios componentes a la página web y editarlos según sea necesario."

1. Desde el **[!UICONTROL Componentes]** en el panel izquierdo, puede añadir los siguientes componentes a su página web y editarlos según lo necesite:

   * [Divisor](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [Imagen](../email/content-components.md#image)
   * Encabezado: el uso de este componente es similar al uso de la variable **[!UICONTROL Texto]** en el diseñador de correo electrónico. [Más información](../email/content-components.md#text)
   * Párrafo: El uso de este componente es similar al uso del **[!UICONTROL Texto]** en el diseñador de correo electrónico. [Más información](../email/content-components.md#text)
   * Vínculo: aprenda a definir el estilo del vínculo en [esta sección](../email/styling-links.md)
   * [Decisión de oferta](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. Pase el ratón sobre la página y haga clic en **[!UICONTROL Insertar antes]** o **[!UICONTROL Insertar después]** para anexar el componente a un elemento existente de la página.

   ![](assets/web-designer-insert-components.png)

1. Desde el contenedor que se muestra para este componente, edite el contenido del componente según sea necesario.

   ![](assets/web-designer-edit-html.png)

1. Ajuste los estilos que se muestran desde **[!UICONTROL Contenedor]** panel de la derecha, como fondo, color del texto, borde, tamaño, posición, etc. en función del componente seleccionado.

   ![](assets/web-designer-html-style.png)

## Navegar por el diseñador web

### Usar rutas

1. Seleccione cualquier elemento del lienzo.

1. Haga clic en **[!UICONTROL Expandir/contraer rutas de exploración]** en la parte inferior izquierda de la pantalla para mostrar rápidamente información sobre el elemento seleccionado.

   ![](assets/web-designer-breadcrumbs.png)

1. Cuando pasa el ratón por encima de las rutas de exploración, el elemento correspondiente se resalta en el editor.

1. Puede navegar fácilmente a cualquier elemento principal, del mismo nivel o secundario dentro del editor visual.

### Cambiar a modo Examinar {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Uso del modo Examinar"
>abstract="Desde este modo, puede navegar hasta la página exacta desde la superficie seleccionada que desee personalizar."

Puede intercambiar desde el valor predeterminado **[!UICONTROL Diseño]** al modo **[!UICONTROL Examinar]** mediante el botón dedicado.

![](assets/web-designer-browse-mode.png)

Desde el **[!UICONTROL Examinar]** En este modo, puede navegar hasta la página exacta desde la superficie seleccionada que desee personalizar.

Resulta especialmente útil cuando se tratan páginas que están detrás de la autenticación o que no están disponibles desde el principio en una dirección URL determinada. Por ejemplo: podrá autenticarse, navegar a la página de su cuenta o a la página del carro de compras y, a continuación, volver a cambiar a **[!UICONTROL Diseño]** para realizar los cambios en la página deseada.

### Cambiar el tamaño del dispositivo

Puede cambiar el tamaño del dispositivo a un tamaño predefinido como **[!UICONTROL Tableta]** o **[!UICONTROL Horizontal móvil]** o defina un tamaño personalizado. Introduzca el número de píxeles deseado para definir un tamaño personalizado.

También puede cambiar el enfoque del zoom: de 25% a 400%.

![](assets/web-designer-device.png)

## Administración de modificaciones {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Administre fácilmente todos sus cambios"
>abstract="Con este panel, puede desplazarse por todos los ajustes y estilos agregados a la página web y administrarlos."

Puede administrar fácilmente todos los componentes, ajustes y estilos que agregó a su página web.

1. Seleccione el **[!UICONTROL Modificaciones]** para mostrar el panel correspondiente a la izquierda.

   ![](assets/web-designer-modifications-pane.png)

1. Puede revisar cada uno de los cambios realizados en la página.

1. Seleccione una modificación no deseada y haga clic en el icono Eliminar para eliminarla.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >Proceda con cuidado al eliminar una acción, ya que puede afectar a las acciones posteriores.

1. También puede cancelar y rehacer acciones utilizando el **[!UICONTROL Deshacer/Rehacer]** en la parte superior derecha de la pantalla.

   ![](assets/web-designer-undo-redo.png)

   Haga clic y mantenga presionado el botón para cambiar entre las **[!UICONTROL Deshacer]** y **[!UICONTROL Rehacer]** opciones. A continuación, haga clic en el botón para aplicar la acción deseada.

## Añadir personalización y ofertas

Para añadir personalización, seleccione un contenedor y seleccione el icono de personalización de la barra de menús contextual que se muestra. Añada los cambios con el Editor de expresiones. [Más información](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Utilice el **[!UICONTROL Decisión de oferta]** componente a insertar [ofertas](../offers/get-started/starting-offer-decisioning.md) en sus páginas web. El proceso es el mismo que cuando [adición de una oferta a un correo electrónico](../email/add-offers-email.md). Aprovechará Administración de decisiones para elegir la mejor oferta que se ofrezca a sus clientes.

![](assets/web-designer-offer.png)

## Prueba de la campaña web {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Previsualizar la experiencia web"
>abstract="Obtenga una simulación del aspecto que tendrá su experiencia web."

Para mostrar una vista previa de la experiencia web modificada, siga los pasos a continuación.

>[!CAUTION]
>
>Debe tener perfiles de prueba disponibles para simular qué ofertas se les enviarán. Obtenga información sobre cómo [creación de perfiles de prueba](../segment/creating-test-profiles.md).

1. Desde el **[!UICONTROL Editar contenido]** para el diseñador web, seleccione **[!UICONTROL Simular contenido]**.

   ![](assets/web-designer-simulate.png)

1. Clic **[!UICONTROL Administración de perfiles de prueba]** para seleccionar uno o varios perfiles de prueba.
1. Se muestra una vista previa de la página web modificada.

   ![](assets/web-designer-preview.png)

1. También puede copiar la dirección URL de prueba para pegarla en cualquier explorador o abrirla en el explorador predeterminado.
