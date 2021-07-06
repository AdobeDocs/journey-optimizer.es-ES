---
title: Uso de los componentes de contenido del diseñador de correo electrónico
description: Aprenda a utilizar componentes de contenido en los correos electrónicos
feature: Información general
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 2%

---

# Uso de los componentes de contenido del Diseñador de correo electrónico {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components"
>title="Acerca de los componentes de contenido"
>abstract="Los componentes de contenido son marcadores de posición de contenido vacíos que se pueden utilizar para crear el diseño de un correo electrónico."


Al crear el contenido del correo electrónico desde cero, **[!UICONTROL Content components]** le permite personalizar aún más el correo electrónico con componentes sin procesar y vacíos que puede utilizar una vez colocados en un correo electrónico.
Puede agregar tantos **[!UICONTROL Content components]** como necesite dentro de un **[!UICONTROL Structure component]** que define el diseño del correo electrónico.

## Botón {#buttons}

Utilice el componente **[!UICONTROL Button]** para insertar varios botones en el correo electrónico y redirigir la audiencia de correo electrónico a otra página.

1. En **[!UICONTROL Content components]**, arrastre y suelte **[!UICONTROL Button]** en un **[!UICONTROL Structure component]**.

   ![](assets/email_designer_13.png)

1. Haga clic en el botón recién agregado para personalizar el texto y tener acceso al **[!UICONTROL Components Settings]** en el panel derecho del diseñador de correo electrónico.

   ![](assets/email_designer_14.png)

1. En el campo **[!UICONTROL Link]** del **[!UICONTROL Components Settings]**, añada la dirección URL a la que desea que se redirija a la audiencia al hacer clic en el botón.

1. Elija cómo se redirigirá la audiencia con la lista desplegable **[!UICONTROL Target]**:

   * **[!UICONTROL None]**: abre el vínculo en el mismo marco en el que se hizo clic (predeterminado).
   * **[!UICONTROL Blank]**: abre el vínculo en una nueva ventana o pestaña.
   * **[!UICONTROL Self]**: abre el vínculo en el mismo marco en el que se hizo clic.
   * **[!UICONTROL Parent]**: abre el vínculo en el marco principal.
   * **[!UICONTROL Top]**: abre el vínculo en todo el cuerpo de la ventana.

   ![](assets/email_designer_15.png)

1. Ahora puede personalizar aún más el botón cambiando **[!UICONTROL Style]**, **[!UICONTROL Margin]** y **[!UICONTROL Border]** por ejemplo.

## Texto {#text}

Utilice el componente **[!UICONTROL Text]** para insertar texto en el correo electrónico. Puede ajustar el color, el estilo y el tamaño del texto en **[!UICONTROL Component Settings]**.

1. En **[!UICONTROL Content Components]**, arrastre y suelte **[!UICONTROL Text]** en un **[!UICONTROL Structure component]**.

   ![](assets/email_designer_11.png)

1. Haga clic en el componente recién agregado para personalizar el texto y tener acceso al **[!UICONTROL Components Settings]** en el panel derecho del diseñador de correo electrónico.

1. Cambie el texto con las siguientes opciones disponibles en la barra de herramientas:

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Change text style]**: aplique negrita, cursiva, subrayado o tachado al texto.
   * **Cambiar alineación**: elija entre alineación izquierda, derecha, centro o justificada para el texto.
   * **[!UICONTROL Create list]**: añada viñetas o listas numéricas al texto.
   * **[!UICONTROL Set heading]**: añada hasta seis niveles de encabezado al texto.
   * **Tamaño** de fuente: seleccione el tamaño de fuente del texto en píxeles.
   * **[!UICONTROL Edit image]**: añada una imagen o un recurso al componente de texto. [Obtenga más información sobre la administración de recursos](assets-essentials.md).
   * **[!UICONTROL Show the source code]**: muestre el código fuente del texto. No se puede modificar.
   * **[!UICONTROL Duplicate]**: añada una copia del componente de texto.
   * **[!UICONTROL Delete]**: elimine el componente de texto seleccionado del correo electrónico.
   * **[!UICONTROL Add personalization]**: añada campos personalizados para personalizar el contenido de los datos de perfiles. [Obtenga más información sobre la personalización de contenido](personalization/personalize.md).

1. Para mejorar la experiencia del usuario, puede añadir campos de personalización para dirigirse al público. Para obtener más información, consulte [esta sección](personalization/personalize.md).

1. Ajuste los **[!UICONTROL Text color]**, **[!UICONTROL Font family]** y **[!UICONTROL Size]** en el **[!UICONTROL Components Settings]**.

   ![](assets/email_designer_12.png)

## Divisor {#divider}

Utilice el componente **[!UICONTROL Divider]** para insertar una línea divisoria y organizar el diseño y el contenido del correo electrónico.
Puede seleccionar el color, el estilo y el tamaño de la línea de salto en **[!UICONTROL Component Settings]**.

![](assets/email_designer_16.png)

## HTML {#HTML}

Utilice **[!UICONTROL HTML]** para copiar y pegar las diferentes partes del HTML existente. Esto le permite crear componentes HTML modulares gratuitos.

Para hacer que un contenido externo sea compatible con el Diseñador de correo electrónico, Adobe recomienda crear un mensaje desde cero y copiar el contenido del correo electrónico existente en los componentes.

1. En **[!UICONTROL Content Components]**, arrastre y suelte **[!UICONTROL HTML]** en un **[!UICONTROL Structure component]**.

   ![](assets/email_designer_22.png)

1. Haga clic en el componente recién agregado y luego **[!UICONTROL Show the source code]** para añadir el HTML.

   ![](assets/email_designer_23.png)

1. Copie y pegue el código HTML que desee añadir al correo electrónico y haga clic en **[!UICONTROL Save]**.

1. Ahora puede personalizar aún más el HTML cambiando **[!UICONTROL Style]**, **[!UICONTROL Margin]** y **[!UICONTROL Border]** por ejemplo o añadiendo un vínculo para redirigir la audiencia a otro contenido.

## Imagen {#image}

Utilice el componente **[!UICONTROL Image]** para insertar un archivo de imagen desde el equipo en el correo electrónico.

1. En **[!UICONTROL Content Components]**, arrastre y suelte **[!UICONTROL Image]** en un **[!UICONTROL Structure component]**.

   ![](assets/email_designer_9.png)

1. Haga clic en **[!UICONTROL Browse]** para elegir un archivo de imagen de sus recursos.

   Para obtener más información sobre [!DNL Assets Essentials], consulte [Documentación de Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;}.

1. Haga clic en el componente recién agregado para comenzar a configurar el **[!UICONTROL Content Components]** y para tener acceso al **[!UICONTROL Components Settings]** en el panel derecho del diseñador de correo electrónico.

1. Configure las propiedades de la imagen:

   * **[!UICONTROL Image Title]** permite definir un título para la imagen.
   * **[!UICONTROL Alt text]** permite definir el rótulo vinculado a la imagen. Esto corresponde al atributo HTML alternativo.

   ![](assets/email_designer_10.png)

1. Ahora puede personalizar aún más la imagen cambiando **[!UICONTROL Style]**, **[!UICONTROL Margin]** y **[!UICONTROL Border]** por ejemplo o agregando un vínculo para redirigir la audiencia a otro contenido.

## Vídeo {#Video}

>[!CONTEXTUALHELP]
>id="ac_edition_video"
>title="Configuración de vídeo"
>abstract="Utilice este componente para insertar un vídeo en el correo electrónico. Tenga en cuenta que los vídeos no funcionan en todos los clientes de correo electrónico. Se recomienda configurar una imagen de reserva."
>additional-url="https://www.emailonacid.com/blog/article/email-development/a_how_to_guide_to_embedding_html5_video_in_email/" text="Información adicional"

Utilice el componente **[!UICONTROL Video]** para insertar un vídeo en el correo electrónico a través de un vínculo URL.

1. En **[!UICONTROL Content Components]**, arrastre y suelte **[!UICONTROL Video]** en un **[!UICONTROL Structure component]**.

   ![](assets/email_designer_17.png)

1. Haga clic en el componente recién agregado para comenzar a configurar el **[!UICONTROL Content Components]** y para tener acceso al **[!UICONTROL Components Settings]** en el panel derecho del diseñador de correo electrónico.

1. En el campo **[!UICONTROL Video link]** del **[!UICONTROL Components Settings]**, añada la URL del vídeo.

   ![](assets/email_designer_18.png)

1. Puede agregar un **[!UICONTROL Poster image]** al vídeo para especificar una imagen que se mostrará hasta que la audiencia haga clic en el botón de reproducción.

1. Ahora puede personalizar aún más la imagen cambiando **[!UICONTROL Style]**, **[!UICONTROL Margin]** y **[!UICONTROL Border]** por ejemplo.

## Social {#social}

Utilice el componente **[!UICONTROL Social]** para insertar vínculos a páginas de medios sociales en el correo electrónico.

1. En **[!UICONTROL Content Components]**, arrastre y suelte **[!UICONTROL Social]** en un **[!UICONTROL Structure component]**.

   ![](assets/email_designer_19.png)

1. Haga clic en el componente recién agregado para comenzar a configurar el **[!UICONTROL Content Components]** y para tener acceso al **[!UICONTROL Components Settings]** en el panel derecho del diseñador de correo electrónico.

1. En el campo **[!UICONTROL Social]** del **[!UICONTROL Components Settings]**, elija qué medios sociales desea agregar o eliminar.

   ![](assets/email_designer_20.png)

1. Elija el tamaño de los iconos en el campo **[!UICONTROL Size of images]**.

1. Haga clic en cada uno de los iconos de medios sociales para configurar el **[!UICONTROL URL]** al que se redirigirá la audiencia.

   ![](assets/email_designer_21.png)

1. También puede cambiar los iconos de cada uno de los medios sociales si es necesario en el campo **[!UICONTROL Image]** .

1. Ahora puede personalizar aún más los iconos de los medios sociales cambiando **[!UICONTROL Style]**, **[!UICONTROL Margin]** y **[!UICONTROL Border]**.

## Decisión de oferta {#offer-decision}

Utilice el componente **[!UICONTROL Offer decision]** para insertar decisiones (anteriormente conocidas como actividades de oferta) en los mensajes. Las decisiones aprovecharán la Administración de decisiones para elegir la mejor oferta que se ofrezca a sus clientes.

Temas relacionados:

* [Introducción a Administración de decisiones](offers/get-started/starting-offer-decisioning.md).
* [Añadir ofertas personalizadas a mensajes](deliver-personalized-offers.md).

