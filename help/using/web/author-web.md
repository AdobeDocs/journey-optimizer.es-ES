---
title: Creación de páginas web
description: Obtenga información sobre cómo crear una página web y editar su contenido en Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1623'
ht-degree: 14%

---

# Creación de páginas web {#author-web}

Una vez que [se ha añadido una acción web](create-web.md#create-web-campaign) en la campaña, puede editar el contenido del sitio mediante el diseñador web.

Entrada [!DNL Journey Optimizer], la creación web se basa en **Ayuda visual de Adobe Experience Cloud** extensión del navegador chrome. [Más información](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>Para poder acceder y crear páginas web en [!DNL Journey Optimizer] interfaz de usuario, asegúrese de seguir los requisitos previos enumerados en [esta sección](web-prerequisites.md).

[Aprenda a crear una campaña web en este vídeo](#video)

## Editar contenido de página web {#edit-web-content}

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

1. En su lugar, utilice:

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

## Administración de modificaciones {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Administrar fácilmente todos los cambios"
>abstract="Con este tablero, puede desplazarse por la página web y administrar todos los ajustes y estilos que haya agregado a ella."

Puede administrar fácilmente todos los componentes, ajustes y estilos que agregó a su página web.

1. Seleccione el **[!UICONTROL Modificaciones]** para mostrar el panel correspondiente a la izquierda.

   ![](assets/web-designer-modifications-pane.png)

1. Puede revisar cada uno de los cambios realizados en la página.

1. Seleccione una modificación no deseada y haga clic en el icono Eliminar para eliminarla.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >Proceda con cuidado al eliminar una acción, ya que puede afectar a las acciones posteriores.

1. Utilice el **[!UICONTROL Más acciones]** en la parte superior del **[!UICONTROL Modificaciones]** para eliminar todas las modificaciones a la vez.

   ![](assets/web-designer-delete-modifications.png)

1. Desde el **[!UICONTROL Más acciones]** también puede eliminar únicamente las modificaciones no válidas, es decir, los cambios que fueron anulados por otros cambios. Por ejemplo, si modifica el color de un texto y lo elimina, la modificación del color deja de ser válida porque el texto ya no existe.

1. También puede cancelar y rehacer acciones utilizando el **[!UICONTROL Deshacer/Rehacer]** en la parte superior derecha de la pantalla.

   ![](assets/web-designer-undo-redo.png)

   Haga clic y mantenga presionado el botón para cambiar entre las **[!UICONTROL Deshacer]** y **[!UICONTROL Rehacer]** opciones. A continuación, haga clic en el botón para aplicar la acción deseada.

## Uso del rastreo de clics {#use-click-tracing}

Esta capacidad del diseñador web le permite seleccionar cualquier elemento del sitio web y rastrear los clics en ese elemento.

Una vez que la campaña esté activa, puede comprobar el número de clics de cada elemento en el informe web de la campaña. Esta información puede ser útil para mejorar la experiencia de los usuarios del sitio web. Por ejemplo, si la variable [informes web](../reports/campaign-global-report.md#web-tab) Para mostrar que muchos usuarios hacen clic en un elemento en el que no se puede hacer clic, puede que desee agregar un vínculo a dicho elemento.

1. Seleccione un elemento de la página y elija **[!UICONTROL Elemento de rastreo de clics]** en el menú contextual.

   ![](assets/web-designer-click-track.png)

   >[!NOTE]
   >
   >Se puede seleccionar cualquier elemento, activo o no.

1. La acción rastreada correspondiente se muestra automáticamente en la **[!UICONTROL Seguimiento de clics]** panel de la izquierda.

   ![](assets/web-designer-click-track-pane.png)

1. Añada una etiqueta significativa para administrar todos los elementos rastreados y encontrarlos fácilmente en los informes. El **[!UICONTROL Selector de CSS]** El campo muestra información para localizar el elemento seleccionado.

1. Repita los pasos anteriores para seleccionar tantos otros elementos como necesite para el rastreo de clics. Las acciones correspondientes se enumeran todas en el panel izquierdo.

   ![](assets/web-designer-click-tracking-actions.png)

1. Para eliminar el rastreo de clics en un elemento, seleccione el icono de eliminación correspondiente.

Una vez que la campaña esté activa, puede consultar el informe de campaña **[!UICONTROL Web]** para comparar el número de impresiones, la tasa de clics y el número de clics por elemento. [Más información](../reports/campaign-global-report.md#web-tab)

## Navegar por el diseñador web {#navigate-web-designer}

### Usar rutas {#breadcrumbs}

1. Seleccione cualquier elemento del lienzo.

1. Haga clic en **[!UICONTROL Expandir/contraer rutas de exploración]** en la parte inferior izquierda de la pantalla para mostrar rápidamente información sobre el elemento seleccionado.

   ![](assets/web-designer-breadcrumbs.png)

1. Cuando pasa el ratón por encima de las rutas de exploración, el elemento correspondiente se resalta en el editor.

1. Puede navegar fácilmente a cualquier elemento principal, del mismo nivel o secundario dentro del editor visual.

### Cambiar a modo Examinar {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Usar el modo de exploración"
>abstract="Desde este modo, puede desplazarse a la página exacta desde la superficie seleccionada que desee personalizar."

Puede intercambiar desde el valor predeterminado **[!UICONTROL Diseño]** al modo **[!UICONTROL Examinar]** mediante el botón dedicado.

![](assets/web-designer-browse-mode.png)

Desde el **[!UICONTROL Examinar]** En este modo, puede navegar hasta la página exacta desde la superficie seleccionada que desee personalizar.

Resulta especialmente útil cuando se tratan páginas que están detrás de la autenticación o que no están disponibles desde el principio en una dirección URL determinada. Por ejemplo: podrá autenticarse, navegar a la página de su cuenta o a la página del carro de compras y, a continuación, volver a cambiar a **[!UICONTROL Diseño]** para realizar los cambios en la página deseada.

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

## Prueba de la campaña web {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Previsualizar la experiencia web"
>abstract="Obtenga una simulación del aspecto que tendrá su experiencia web."

Para mostrar una vista previa de la experiencia web modificada, siga los pasos a continuación.

>[!CAUTION]
>
>Debe tener perfiles de prueba disponibles para simular qué ofertas se les enviarán. Obtenga información sobre cómo [creación de perfiles de prueba](../segment/creating-test-profiles.md).

1. En la pantalla de edición de contenido de la campaña web, seleccione **[!UICONTROL Simular contenido]**.

   <!--![](assets/web-designer-simulate.png)-->

   ![](assets/web-campaign-simulate.png)

1. Clic **[!UICONTROL Administración de perfiles de prueba]** para seleccionar uno o varios perfiles de prueba.
1. Se muestra una vista previa de la página web modificada.

   ![](assets/web-designer-preview.png)

1. También puede abrirlo en el explorador predeterminado o copiar la dirección URL de prueba para pegarla en cualquier explorador. Esto le permite compartir el vínculo con su equipo y las partes interesadas, que pueden obtener una vista previa de la nueva experiencia web en cualquier explorador antes de que la campaña se ponga en marcha.

   >[!NOTE]
   >
   >Al copiar la dirección URL de prueba, el contenido mostrado es el personalizado para el perfil de prueba utilizado cuando se generó la simulación de contenido en [!DNL Journey Optimizer].

## Vídeo explicativo{#video}

El siguiente vídeo muestra cómo crear una experiencia web con el diseñador web en [!DNL Journey Optimizer] campañas.

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)
