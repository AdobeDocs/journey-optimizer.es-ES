---
title: Edición de contenido web
description: Obtenga información sobre cómo crear una página web y editar su contenido en Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 59412ecbb8df74c7185b67593131c610d6da4148
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 17%

---

# Edición de contenido web {#edit-web-content}

Una vez que [se ha añadido una acción web](create-web.md#create-web-campaign) en la campaña, puede editar el contenido del sitio mediante el diseñador web.

[Aprenda a crear una campaña web en este vídeo](#video)

Entrada [!DNL Journey Optimizer], la creación web se basa en **Ayuda visual de Adobe Experience Cloud** extensión del navegador chrome. [Más información](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>Para poder acceder y crear páginas web en [!DNL Journey Optimizer] interfaz de usuario, asegúrese de seguir los requisitos previos enumerados en [esta sección](web-prerequisites.md).

Acceda a las siguientes secciones para obtener más información sobre cada tema:

* [Administración de modificaciones](manage-web-modifications.md)

* [Monitorización de sus campañas web](monitor-web-campaigns.md)

## Trabajar con el diseñador web {#work-with-web-designer}

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

Para empezar a crear la campaña web, siga los pasos a continuación.

1. Desde el **[!UICONTROL Acción]** de la pestaña [campaña](create-web.md#create-web-campaign), seleccione **[!UICONTROL Editar contenido]**.<!--change screen with rule-->

   ![](assets/web-campaign-edit-content.png)

1. Si ha creado una regla de coincidencia de páginas, debe introducir cualquier dirección URL que coincida con esta regla: los cambios se aplicarán a todas las páginas que coincidan con la regla. Se muestra el contenido de la página.

   >[!NOTE]
   >
   >Si ha introducido una sola URL como superficie web, la URL que desea personalizar ya se ha rellenado.

   ![](assets/web-edit-enter-url.png)

   >[!CAUTION]
   >
   >La página web debe incluir [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"}. [Más información](web-prerequisites.md#implementation-prerequisites)

1. Clic **[!UICONTROL Editar página web]** para empezar a crearlo. Se muestra el diseñador web.

   ![](assets/web-designer.png)

   >[!NOTE]
   >
   >Si intenta cargar un sitio web que no se puede cargar, aparece un mensaje sugiriendo que instale el [Extensión de explorador Ayuda de edición visual](#install-visual-editing-helper). Consulte algunas sugerencias para solucionar problemas en [esta sección](web-prerequisites.md#troubleshooting).

1. Seleccione cualquier elemento del lienzo, como imagen, botón, párrafo, texto, contenedor, encabezado, vínculo, etc. [Más información](#content-components)

1. Utilice:

   * Menú contextual para editar su contenido, diseño, inserción de vínculos o personalización, etc.

     ![](assets/web-designer-contextual-bar.png)

   * Los iconos de la parte superior del panel derecho para editar, duplicar, eliminar u ocultar cada elemento.

     ![](assets/web-designer-right-panel-icons.png)

   * Panel derecho que cambia dinámicamente según el elemento seleccionado. Por ejemplo, puede editar el fondo, la tipografía, el borde, el tamaño, la posición, el espaciado, los efectos o los estilos en línea de un elemento.

     ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>El diseñador de contenido web es similar al diseñador de correo electrónico. Más información sobre [diseño de contenido con [!DNL Journey Optimizer]](../email/get-started-email-design.md).

## Uso de componentes {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Añadir componentes a la página web"
>abstract="Puede añadir varios componentes a la página web y editarlos según sea necesario."

1. Desde el **[!UICONTROL Componentes]** panel de la izquierda, seleccione un elemento. Puede añadir los siguientes componentes a la página web y editarlos según sea necesario:

   * [Divisor](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [Imagen](../email/content-components.md#image)
   * Encabezado: el uso de este componente es similar al uso de la variable **[!UICONTROL Texto]** en el diseñador de correo electrónico. [Más información](../email/content-components.md#text)
   * Párrafo: El uso de este componente es similar al uso del **[!UICONTROL Texto]** en el diseñador de correo electrónico. [Más información](../email/content-components.md#text)
   * Vínculo
   * [Decisión de oferta](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. Pase el ratón sobre la página y haga clic en **[!UICONTROL Insertar antes]** o **[!UICONTROL Insertar después]** para anexar el componente a un elemento existente de la página.

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >Para anular la selección de un componente, haga clic en **[!UICONTROL ESC]** en el titular azul contextual que se muestra en la parte superior del lienzo.

1. Edite el componente según sea necesario directamente en el contenido de la página.

   ![](assets/web-designer-edit-header.png)

1. Ajuste los estilos que se muestran en el panel contextual de la derecha, como fondo, color del texto, borde, tamaño, posición, etc. - según el componente seleccionado.

   ![](assets/web-designer-header-style.png)

## Añadir personalización y ofertas

Para añadir personalización, seleccione un contenedor y seleccione el icono de personalización de la barra de menús contextual que se muestra. Añada los cambios con el Editor de expresiones. [Más información](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Utilice el **[!UICONTROL Decisión de oferta]** componente a insertar [ofertas](../offers/get-started/starting-offer-decisioning.md) en sus páginas web. El proceso es el mismo que cuando [adición de una oferta a un correo electrónico](../email/add-offers-email.md). Aprovechará Administración de decisiones para elegir la mejor oferta que se ofrezca a sus clientes.

![](assets/web-designer-offer.png)

## Navegar por el diseñador web {#navigate-web-designer}

En esta sección se detallan las distintas formas de desplazarse por el diseñador web. Para ver y administrar las modificaciones agregadas a la experiencia web, consulte [esta sección](manage-web-modifications.md).

### Usar rutas {#breadcrumbs}

1. Seleccione cualquier elemento del lienzo.

1. Haga clic en **[!UICONTROL Expandir/contraer rutas de exploración]** en la parte inferior izquierda de la pantalla para mostrar rápidamente información sobre el elemento seleccionado.

   ![](assets/web-designer-breadcrumbs.png)

1. Cuando pasa el ratón por encima de las rutas de exploración, el elemento correspondiente se resalta en el editor.

1. Puede navegar fácilmente a cualquier elemento principal, del mismo nivel o secundario dentro del editor visual.

### Cambiar al modo Examinar {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Usar el modo Examinar"
>abstract="Desde este modo, puede desplazarse a la página exacta desde la superficie seleccionada que desee personalizar."

Puede intercambiar desde el valor predeterminado **[!UICONTROL Diseño]** al modo **[!UICONTROL Examinar]** mediante el botón dedicado.

![](assets/web-designer-browse-mode.png)

Desde el **[!UICONTROL Examinar]** En este modo, puede navegar hasta la página exacta desde la superficie seleccionada que desee personalizar.

Resulta especialmente útil cuando se tratan páginas que están detrás de la autenticación o que no están disponibles desde el principio en una dirección URL determinada. Por ejemplo: podrá autenticarse, navegar a la página de su cuenta o a la página del carro de compras y, a continuación, volver a cambiar a **[!UICONTROL Diseño]** para realizar los cambios en la página deseada.

Uso de **[!UICONTROL Examinar]** Este modo también permite navegar por todas las vistas del sitio web al crear aplicaciones de una sola página. [Más información](web-spa.md)

### Cambiar el tamaño del dispositivo {#change-device-size}

Puede cambiar el tamaño del dispositivo de visualización del diseñador web a un tamaño predefinido como **[!UICONTROL Tableta]** o **[!UICONTROL Horizontal móvil]** o defina un tamaño personalizado introduciendo el número deseado de píxeles.

También puede cambiar el enfoque del zoom: de 25% a 400%.

![](assets/web-designer-device.png)

La capacidad de cambiar el tamaño del dispositivo está diseñada para sitios adaptables que se renderizan bien en varios dispositivos, ventanas y tamaños de pantalla. Los sitios adaptables se ajustan y adaptan automáticamente a cualquier tamaño de pantalla, incluidos escritorios, portátiles, tabletas o teléfonos móviles.

>[!CAUTION]
>
>Puede editar una experiencia web con un tamaño de dispositivo específico. Sin embargo, siempre que los selectores sean los mismos, estos cambios se aplican a todos los tamaños y dispositivos, no solo al tamaño del dispositivo en el que está trabajando. Del mismo modo, si edita una experiencia en la vista de escritorio normal, los cambios se aplican a todos los tamaños de pantalla, no solo a la vista de escritorio.
>
>Actualmente, [!DNL Journey Optimizer] no admite cambios de página específicos del tamaño del dispositivo. Esto significa que, por ejemplo, si tiene un sitio web móvil independiente con otra estructura de sitio, debe realizar los cambios específicos del sitio móvil en una campaña diferente.

## Vídeo explicativo{#video}

El siguiente vídeo muestra cómo crear una experiencia web con el diseñador web en [!DNL Journey Optimizer] campañas.

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)