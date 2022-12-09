---
solution: Journey Optimizer
product: journey optimizer
title: Uso de los componentes de contenido del diseñador de correo electrónico
description: Aprenda a utilizar componentes de contenido en los correos electrónicos
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1256'
ht-degree: 0%

---

# Uso de los componentes de contenido del Diseñador de correo electrónico {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components_email"
>title="Acerca de los componentes de contenido"
>abstract="Los componentes de contenido son marcadores de posición de contenido vacíos que se pueden utilizar para crear el diseño de un correo electrónico."

>[!CONTEXTUALHELP]
>id="ac_content_components_landing_page"
>title="Acerca de los componentes de contenido"
>abstract="Los componentes de contenido son marcadores de posición de contenido vacíos que se pueden utilizar para crear el diseño de una página de aterrizaje."

>[!CONTEXTUALHELP]
>id="ac_content_components_fragment"
>title="Acerca de los componentes de contenido"
>abstract="Los componentes de contenido son marcadores de posición de contenido vacíos que se pueden utilizar para crear el diseño de un fragmento."

>[!CONTEXTUALHELP]
>id="ac_content_components_template"
>title="Acerca de los componentes de contenido"
>abstract="Los componentes de contenido son marcadores de posición de contenido vacíos que se pueden utilizar para crear el diseño de una plantilla."

Al crear el contenido del correo electrónico, **[!UICONTROL Content components]** le permite personalizar aún más el correo electrónico con componentes sin procesar que puede editar una vez colocados en un correo electrónico.

Puede añadir tantos componentes de contenido como necesite dentro de uno o varios componentes de estructura, que definen el diseño del correo electrónico.

## Añadir componentes de contenido {#add-content-components}

Para añadir componentes de contenido al correo electrónico y ajustarlos a sus necesidades, siga los pasos a continuación.

1. En el Diseñador de correo electrónico, utilice un contenido existente o arrastre y suelte **[!UICONTROL Structure components]** en el contenido vacío para definir el diseño del correo electrónico. [Descubra cómo](content-from-scratch.md)

1. Para acceder a la **[!UICONTROL Content components]** , seleccione el botón correspondiente en el panel izquierdo del Diseñador de correo electrónico.

   ![](assets/email_designer_content_components.png)

1. Arrastre y suelte los componentes de contenido que desee dentro de los componentes de estructura relevantes.

   ![](assets/email_designer_add_content_components.png)

   >[!NOTE]
   >
   >Puede añadir varios componentes en un único componente de estructura y en cada columna de un componente de estructura.

1. Ajuste los atributos de estilo para cada componente mediante el **[!UICONTROL Component settings]** a la derecha. Por ejemplo, puede cambiar el estilo, el relleno o el margen del texto de cada componente. [Obtenga más información sobre la alineación y el relleno](alignment-and-padding.md)

   ![](assets/email_designer_content_components_settings.png)

## Contenedor {#container}

Puede añadir un contenedor simple dentro del cual podrá añadir otro componente de contenido. Esto le permite aplicar un estilo específico al contenedor, que será diferente del componente utilizado dentro.

Por ejemplo, agregue un **[!UICONTROL Container]** y, a continuación, agregue un [Botón](#button) dentro de ese contenedor. Puede utilizar un fondo específico para el contenedor y otro para el botón .

![](assets/email_designer_container_component.png)

## Botón {#button}

Utilice la variable **[!UICONTROL Button]** para insertar uno o varios botones en el correo electrónico y redirigir la audiencia de correo electrónico a otra página.

1. De **[!UICONTROL Content components]**, arrastre y suelte el **[!UICONTROL Button]** en un **[!UICONTROL Structure component]**.

1. Haga clic en el botón recién agregado para personalizar el texto y tener acceso al **[!UICONTROL Components settings]** en el panel derecho del Diseñador de correo electrónico.

   ![](assets/email_designer_button_component.png)

1. En el **[!UICONTROL Link]** , añada la dirección URL a la que desee redirigir al hacer clic en el botón .

1. Elija cómo se redirigirá a su audiencia con la variable **[!UICONTROL Target]** lista desplegable:

   * **[!UICONTROL None]**: abre el vínculo en el mismo marco en el que se hizo clic (predeterminado).
   * **[!UICONTROL Blank]**: abre el vínculo en una nueva ventana o pestaña.
   * **[!UICONTROL Self]**: abre el vínculo en el mismo marco en el que se hizo clic.
   * **[!UICONTROL Parent]**: abre el vínculo en el marco principal.
   * **[!UICONTROL Top]**: abre el vínculo en todo el cuerpo de la ventana.

   ![](assets/email_designer_button_link.png)

1. Puede personalizar aún más el botón cambiando atributos de estilo como **[!UICONTROL Border]**, **[!UICONTROL Size]**, **[!UICONTROL Margin]**, etc. de la variable **[!UICONTROL Component settings]** panel.

## Texto {#text}

Utilice la variable **[!UICONTROL Text]** para insertar texto en el correo electrónico y ajustar el estilo (borde, tamaño, relleno, etc.) usando la variable **[!UICONTROL Component settings]** panel.

![](assets/email_designer_text_component.png)

1. De **[!UICONTROL Content components]**, arrastre y suelte el **[!UICONTROL Text]** en un **[!UICONTROL Structure component]**.

1. Haga clic en el componente recién agregado para personalizar el texto y tener acceso al **[!UICONTROL Components Settings]** en el panel derecho del Diseñador de correo electrónico.

1. Cambie el texto con las siguientes opciones disponibles en la barra de herramientas:

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Change text style]**: aplique negrita, cursiva, subrayado o tachado al texto.
   * **Cambiar alineación**: elija entre alineación izquierda, derecha, centro o justificada para el texto.
   * **[!UICONTROL Create list]**: añada viñetas o listas numéricas al texto.
   * **[!UICONTROL Set heading]**: añada hasta seis niveles de encabezado al texto.
   * **Tamaño de fuente**: seleccione el tamaño de fuente del texto en píxeles.
   * **[!UICONTROL Edit image]**: añada una imagen o un recurso al componente de texto. [Obtenga más información sobre la administración de recursos](assets-essentials.md)
   * **[!UICONTROL Show the source code]**: muestre el código fuente del texto. No se puede modificar.
   * **[!UICONTROL Duplicate]**: añada una copia del componente de texto.
   * **[!UICONTROL Delete]**: elimine el componente de texto seleccionado del correo electrónico.
   * **[!UICONTROL Add personalization]**: añada campos personalizados para personalizar el contenido de los datos de perfiles. [Descubra más información sobre la personalización del contenido](../personalization/personalize.md)
   * **[!UICONTROL Enable conditional content]**: añada contenido condicional para adaptar el contenido del componente a los perfiles de destino. [Descubra más información sobre el contenido dinámico](../personalization/get-started-dynamic-content.md)

1. Ajuste los demás atributos de estilo, como el color del texto, la familia de fuentes, el borde, el relleno, el margen, etc. de la variable **[!UICONTROL Component settings]** panel.

## Divisor {#divider}

Utilice la variable **[!UICONTROL Divider]** para insertar una línea divisoria y organizar el diseño y el contenido del correo electrónico.

Puede ajustar atributos de estilo, como el color de la línea, el estilo y la altura desde la **[!UICONTROL Component settings]** panel.

![](assets/email_designer_divider.png)

## HTML {#HTML}

Utilice la variable **[!UICONTROL HTML]** para copiar y pegar las diferentes partes del HTML existente. Esto le permite crear componentes HTML modulares gratuitos para reutilizar contenido externo.

1. De **[!UICONTROL Content Components]**, arrastre y suelte el **[!UICONTROL HTML]** en un **[!UICONTROL Structure component]**.

1. Haga clic en el componente recién agregado y, a continuación, seleccione **[!UICONTROL Show the source code]** de la barra de herramientas contextual para añadir el HTML.

   ![](assets/email_designer_html_component.png)

1. Copie y pegue el código HTML que desee añadir al correo electrónico y haga clic en **[!UICONTROL Save]**.

   ![](assets/email_designer_html_content.png)

>[!NOTE]
>
>Para hacer que un contenido externo sea compatible con el Diseñador de correo electrónico, Adobe recomienda crear un mensaje desde cero y copiar el contenido del correo electrónico existente en los componentes.

## Imagen {#image}

Utilice la variable **[!UICONTROL Image]** para insertar un archivo de imagen del equipo en el contenido del correo electrónico.

1. De **[!UICONTROL Content components]**, arrastre y suelte el **[!UICONTROL Image]** en un **[!UICONTROL Structure component]**.

1. Haga clic en **[!UICONTROL Browse]** para elegir un archivo de imagen de los recursos.

   Para obtener más información sobre [!DNL Assets Essentials], consulte [Documentación de Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;}.

1. Haga clic en el componente recién agregado y configure las propiedades de la imagen utilizando la variable **[!UICONTROL Components settings]** panel:

   * **[!UICONTROL Image title]** permite definir un título para la imagen.
   * **[!UICONTROL Alt text]** permite definir el rótulo vinculado a la imagen. Esto corresponde al atributo HTML alternativo.

   ![](assets/email_designer_10.png)

1. Ajuste los demás atributos de estilo, como margen, borde, etc. o agregando un vínculo para redirigir a la audiencia a otro contenido de la **[!UICONTROL Component settings]** panel.

## Vídeo {#Video}

>[!CONTEXTUALHELP]
>id="ac_edition_video_email"
>title="Configuración de vídeo"
>abstract="Utilice este componente para insertar un vídeo en el correo electrónico. Tenga en cuenta que los vídeos no funcionan en todos los clientes de correo electrónico. Se recomienda configurar una imagen de reserva."

>[!CONTEXTUALHELP]
>id="ac_edition_video_landing_page"
>title="Configuración de vídeo"
>abstract="Utilice este componente para insertar un vídeo en la página de aterrizaje. Tenga en cuenta que los vídeos no funcionan en todos los clientes de mensajes. Se recomienda configurar una imagen de reserva."

>[!CONTEXTUALHELP]
>id="ac_edition_video_fragment"
>title="Configuración de vídeo"
>abstract="Utilice este componente para insertar un vídeo en el fragmento. Tenga en cuenta que los vídeos no funcionan en todos los clientes de mensajes. Se recomienda configurar una imagen de reserva."

>[!CONTEXTUALHELP]
>id="ac_edition_video_template"
>title="Configuración de vídeo"
>abstract="Utilice este componente para insertar un vídeo en la plantilla. Tenga en cuenta que los vídeos no funcionan en todos los clientes de mensajes. Se recomienda configurar una imagen de reserva."

Utilice la variable **[!UICONTROL Video]** para insertar un vídeo en el contenido del correo electrónico a través de un vínculo URL.

1. De **[!UICONTROL Content Components]**, arrastre y suelte el **[!UICONTROL Video]** componente en un **[!UICONTROL Structure component]**.

   ![](assets/email_designer_17.png)

1. Haga clic en el componente recién agregado.

1. En el **[!UICONTROL Video link]** del campo **[!UICONTROL Components settings]** , agregue la URL del vídeo.

   ![](assets/email_designer_18.png)

1. Puede añadir un **[!UICONTROL Poster image]** al vídeo para especificar una imagen que se mostrará hasta que la audiencia haga clic en el botón de reproducción.

1. Ajuste los demás atributos de estilo, como estilo, margen, borde, etc. de la variable **[!UICONTROL Component settings]** panel.

## Social {#social}

Utilice la variable **[!UICONTROL Social]** para insertar vínculos a páginas de medios sociales en el contenido del correo electrónico.

1. De **[!UICONTROL Content Components]**, arrastre y suelte el **[!UICONTROL Social]** en un **[!UICONTROL Structure component]**.

1. Haga clic en el componente recién agregado.

1. En el **[!UICONTROL Social]** del campo **[!UICONTROL Components settings]** , elija qué medios sociales desea agregar o quitar.

   ![](assets/email_designer_20.png)

1. Elija el tamaño de los iconos a través del campo dedicado.

1. Haga clic en cada uno de los iconos de los medios sociales para configurar la variable **[!UICONTROL URL]** al que se redirigirá la audiencia.

   ![](assets/email_designer_21.png)

1. También puede cambiar los iconos de cada uno de los medios sociales si es necesario en la sección **[!UICONTROL Image]** campo .

1. Ajuste los demás atributos de estilo, como estilo, margen, borde, etc. de la variable **[!UICONTROL Component settings]** panel.

## Decisión de oferta {#offer-decision}

Utilice la variable **[!UICONTROL Offer decision]** para insertar ofertas en los mensajes. La variable [gestión de decisiones](../offers/get-started/starting-offer-decisioning.md) El motor de búsqueda elegirá la mejor oferta para enviarla a sus clientes.

Aprenda a añadir ofertas personalizadas a un correo electrónico en [esta sección](add-offers-email.md).

