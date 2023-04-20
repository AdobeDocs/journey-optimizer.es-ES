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
badge: label="Beta" type="Informative"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 21%

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

En [!DNL Journey Optimizer] la creación web es impulsada por la extensión del explorador Adobe Experience Cloud Visual Helper chrome. [Más información](visual-editing-helper.md)

Para poder acceder y crear páginas web en la variable [!DNL Journey Optimizer] interfaz de usuario, siga los requisitos previos enumerados en [esta sección](create-web.md#prerequesites).

## Editar el contenido de una página web {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Confirmar la dirección URL para editar"
>abstract="Confirme la dirección URL de la página web específica que se utilizará para editar el contenido que se aplicará en la superficie web definida anteriormente. La página web debe implementarse mediante el SDK web de Adobe Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es" text="Más información"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Introduzca la dirección URL para editar"
>abstract="Introduzca la dirección URL de una página web específica que se utilizará para editar el contenido que se aplicará a todas las páginas que coincidan con la regla. La página web debe implementarse mediante el SDK web de Adobe Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es" text="Más información"

<!--Confirm the URL to use for authoring content on the surface. Typically the Authoring URL will be the surface URL itself, but you may include extra parameters if required. The page must include the Adobe Experience Platform Web SDK.-->

Una vez creada una acción web a partir de la campaña, puede editar el contenido mediante el diseñador web. Para ello, siga los pasos que aparecen a continuación.

>[!CAUTION]
>
>Para acceder en [!DNL Journey Optimizer], la página web debe implementarse usando la variable [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"}.

1. En el **[!UICONTROL Acción]** de la campaña, seleccione **[!UICONTROL Editar contenido]** para comenzar a crear la campaña web.

1. Si ha creado una regla de coincidencia de páginas, debe introducir cualquier URL que coincida con esta regla. Los cambios se aplicarán a todas las páginas que coincidan con la regla.

   >[!NOTE]
   >
   >Si ha introducido una sola dirección URL como superficie web, la dirección URL que desea personalizar ya se rellena.

   ![](assets/web-edit-enter-url.png)

1. Se muestra el contenido de la página.

   >[!CAUTION]
   >
   >La página web debe incluir la variable [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"}.

1. Haga clic en **[!UICONTROL Abrir diseñador web]** para editarlo. [Más información](author-web.md)

   ![](assets/web-open-designer.png)

1. Se muestra el diseñador web.

   ![](assets/web-designer.png)

1. Seleccione cualquier elemento del lienzo, como imagen, botón, párrafo, texto, contenedor, encabezado, vínculo, etc. y usar:

   * El menú contextual para editar su contenido, diseño, insertar vínculos o personalización, etc.

      ![](assets/web-designer-contextual-bar.png)

   * Los iconos de la parte superior derecha del panel para editar, duplicar, eliminar u ocultar cada elemento.

      ![](assets/web-designer-right-panel-icons.png)

   * Panel derecho que cambia dinámicamente según el elemento seleccionado. Por ejemplo, puede editar el fondo, la tipografía, el borde, el tamaño, la posición, el espaciado, los efectos o los estilos en línea de un elemento.

      ![](assets/web-designer-right-panel.png)

## Uso de componentes de contenido {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Añadir componentes de contenido a la página web"
>abstract="Puede añadir varios componentes a la página web y editarlos según sea necesario."

1. En el **[!UICONTROL Componentes]** a la izquierda, puede agregar los siguientes componentes a la página web y editarlos según sea necesario:

   * [Divisor](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [Imagen](../email/content-components.md#image)
   * Encabezado : el uso de este componente es similar al uso de la variable **[!UICONTROL Texto]** en el diseñador de correo electrónico. [Más información](../email/content-components.md#text)
   * Párrafo: el uso de este componente es similar al uso de la variable **[!UICONTROL Texto]** en el diseñador de correo electrónico. [Más información](../email/content-components.md#text)
   * Vínculo : Aprenda a definir el estilo del vínculo en [esta sección](../email/styling-links.md)
   * [Decisión de oferta](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. Pase el ratón por encima de la página y haga clic en la **[!UICONTROL Insertar antes]** o **[!UICONTROL Insertar después]** para anexar el componente a un elemento existente en la página.

   ![](assets/web-designer-insert-components.png)

1. Desde el contenedor que se muestra para este componente, edite el contenido del componente según sea necesario.

   ![](assets/web-designer-edit-html.png)

1. Ajuste los estilos que se muestran desde el **[!UICONTROL Contenedor]** panel de la derecha, como fondo, color de texto, borde, tamaño, posición, etc. en función del componente seleccionado.

   ![](assets/web-designer-html-style.png)

## Navegar por el diseñador web

### Usar rutas de exploración

1. Seleccione cualquier elemento del lienzo.

1. Haga clic en el **[!UICONTROL Expandir/Contraer rutas de exploración]** en la parte inferior izquierda de la pantalla para mostrar rápidamente información sobre el elemento seleccionado.

   ![](assets/web-designer-breadcrumbs.png)

1. Cuando pasa el ratón por encima de las rutas de exploración, el elemento correspondiente se resalta en el editor.

1. Con él, puede desplazarse fácilmente a cualquier elemento principal, del mismo nivel o secundario dentro del editor visual.

### Cambiar al modo Examinar {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Usar el modo de exploración"
>abstract="Desde este modo, puede desplazarse a la página exacta desde la superficie seleccionada que desee personalizar."

Puede intercambiar desde el valor predeterminado **[!UICONTROL Diseño]** para **[!UICONTROL Examinar]** usando el botón dedicado.

![](assets/web-designer-browse-mode.png)

En el **[!UICONTROL Examinar]** , puede desplazarse a la página exacta desde la superficie seleccionada que desee personalizar.

Resulta especialmente útil cuando se trata de páginas que están detrás de la autenticación o que no están disponibles desde el principio en una determinada dirección URL. Por ejemplo, podrá autenticarse, navegar a la página de su cuenta o al carro de compras y luego volver a cambiar a **[!UICONTROL Diseño]** para realizar los cambios en la página deseada.

### Cambiar el tamaño del dispositivo

Puede cambiar el tamaño del dispositivo a un tamaño predefinido como **[!UICONTROL Tablet]** o **[!UICONTROL Entorno móvil]** o definir un tamaño personalizado. Introduzca el número deseado de píxeles para definir un tamaño personalizado.

También puede cambiar el enfoque del zoom, de 25% a 400%.

![](assets/web-designer-device.png)

## Administrar modificaciones {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Administrar fácilmente todos los cambios"
>abstract="Con este tablero, puede desplazarse por la página web y administrar todos los ajustes y estilos que haya agregado a ella."

Puede administrar fácilmente todos los componentes, ajustes y estilos agregados a la página web.

1. Seleccione el **[!UICONTROL Modificaciones]** para mostrar el panel correspondiente a la izquierda.

   ![](assets/web-designer-modifications-pane.png)

1. Puede revisar cada uno de los cambios realizados en la página.

1. Seleccione una modificación no deseada y haga clic en el icono de eliminación para eliminarla.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >Tenga cuidado al eliminar una acción, ya que podría afectar a las acciones posteriores.

1. También puede cancelar y rehacer acciones utilizando la variable **[!UICONTROL Deshacer/Rehacer]** en la parte superior derecha de la pantalla.

   ![](assets/web-designer-undo-redo.png)

   Haga clic y mantenga presionado el botón para cambiar entre las **[!UICONTROL Deshacer]** y **[!UICONTROL Rehacer]** opciones. A continuación, haga clic en el propio botón para aplicar la acción deseada.

## Añadir personalización y ofertas

Para añadir personalización, seleccione un contenedor y seleccione el icono de personalización en la barra de menús contextual que se muestra. Añada los cambios mediante el editor de expresiones. [Más información](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Utilice la variable **[!UICONTROL Decisión de oferta]** componente para insertar [ofertas](../offers/get-started/starting-offer-decisioning.md) en las páginas web. El proceso es el mismo que cuando [adición de una oferta a un correo electrónico](../email/add-offers-email.md). Aprovechará la Administración de decisiones para elegir la mejor oferta que se ofrezca a sus clientes.

![](assets/web-designer-offer.png)

## Prueba de la campaña web {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Previsualizar la experiencia web"
>abstract="Obtenga una simulación del aspecto que tendrá su experiencia web."

Para mostrar una vista previa de la experiencia web modificada, siga los pasos a continuación.

>[!CAUTION]
>
>Debe tener perfiles de prueba disponibles para simular las ofertas que se les enviarán. Obtenga información sobre cómo [crear perfiles de prueba](../segment/creating-test-profiles.md).

1. Desde **[!UICONTROL Editar contenido]** o el diseñador web, seleccione **[!UICONTROL Simular contenido]**.

   ![](assets/web-designer-simulate.png)

1. Haga clic en **[!UICONTROL Administrar perfiles de prueba]** para seleccionar uno o varios perfiles de prueba.
1. Se muestra una vista previa de la página web modificada.

   ![](assets/web-designer-preview.png)

1. También puede copiar la dirección URL de prueba para pegarla en cualquier navegador o abrirla en el navegador predeterminado.
