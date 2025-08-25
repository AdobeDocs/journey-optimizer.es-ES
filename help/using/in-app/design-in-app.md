---
title: Diseño del contenido en la aplicación
description: Aprenda a diseñar el contenido en la aplicación en Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: en la aplicación, mensaje, diseño, formato
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 61a30dcc93823dc5e8b647e683bfa2ebf5bfa01b
workflow-type: tm+mt
source-wordcount: '1222'
ht-degree: 26%

---

# Diseño del contenido en la aplicación {#design-content}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_content"
>title="Definir el contenido en la aplicación"
>abstract="Personalice el contenido y el estilo de los mensajes en la aplicación. También puede añadir medios y botones de acción para que sus mensajes sean más atractivos y eficaces."

Puede editar el contenido en la aplicación para configurar las opciones de experiencia:

* En una **[!UICONTROL campaña]**, desde el menú **[!UICONTROL Acción]**, para configurar el contenido del mensaje, haga clic en el botón **[!UICONTROL Editar contenido]**.

  ![](assets/edit-in-app-content.png)

* En un **[!UICONTROL Recorrido]**, desde el menú avanzado de tu **[!UICONTROL Acción]** en la aplicación, puedes empezar a diseñar tu contenido con el botón **[!UICONTROL Editar contenido]**.

  ![](assets/design_inapp_journey.png)

La opción **[!UICONTROL Formato avanzado]** activa opciones adicionales para personalizar la experiencia.

Una vez creado el mensaje en la aplicación, y definido y personalizado su contenido, puede revisarlo y activarlo. Las notificaciones se envían según la programación de campaña. Obtenga más información en [esta página](send-in-app.md).

## Diseño del mensaje {#message-layout}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_message_layout"
>title="Definir el contenido en la aplicación"
>abstract="El diseño del mensaje le proporciona plantillas comúnmente utilizadas para enmarcar su mensaje. El diseño personalizado proporciona opciones para cargar o componer mensajes HTML personalizados."

En la sección **[!UICONTROL Diseño del mensaje]**, seleccione una de las cuatro opciones de diseño diferentes para elegir según sus necesidades de mensajería.

![](assets/in_app_web_design_1.png)

* **[!UICONTROL Pantalla completa]**: este tipo de diseño cubre toda la pantalla de los dispositivos de audiencia.

  Admite componentes multimedia (imagen, vídeo), de texto y botones.

* **[!UICONTROL Modal]**: este diseño aparece en una ventana grande como si fuera una alerta. La aplicación sigue visible en segundo plano.

  Admite componentes multimedia (imagen, vídeo), de texto y botones.

* **[!UICONTROL Banner]**: este tipo de diseño aparece como un mensaje de alerta de sistema operativo nativo.

  Solo puedes agregar un **[!UICONTROL Encabezado]** y un **[!UICONTROL Cuerpo]** a tu mensaje.

* **[!UICONTROL Personalizado]**: el modo de mensaje personalizado le permite importar y editar directamente uno de sus mensajes preconfigurados de HTML.

   * Seleccione **[!UICONTROL Componer]** para ingresar o pegar su código HTML sin procesar.

     Utilice el panel izquierdo para aprovechar las funcionalidades de personalización de Journey Optimizer. Para obtener más información, consulte [esta sección](../personalization/personalize.md).

   * Seleccione **[!UICONTROL Import]** para importar el archivo HTML o .zip que contiene el contenido de HTML.

## Pestaña Contenido {#content-tab}

Desde la ficha **Contenido**, puede definir y personalizar el contenido de la notificación y el estilo del botón **Cerrar**. También puede añadir contenido multimedia a la notificación en la aplicación y añadir botones de acción desde esta pestaña.

### Botón Cerrar {#close-button}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_close"
>title="Elija el estilo de su botón Cerrar."
>abstract="La sección del botón Cerrar ofrece opciones para seleccionar variaciones del botón Cerrar del mensaje y una opción para cargar una imagen personalizada."

![](assets/in_app_web_design_2.png)

Elige **[!UICONTROL Estilo]** de tu **[!UICONTROL botón Cerrar]**.

Los estilos disponibles son:

* **[!UICONTROL Simple]**
* **[!UICONTROL Círculo]**
* **[!UICONTROL Imagen personalizada]** de una URL multimedia o tu Assets.

+++Más opciones con formato avanzado

Si el **[!UICONTROL modo de formato avanzado]** está activado, puede marcar la opción **[!UICONTROL Color]** para elegir el color y la opacidad del botón.

+++

### Medios {#add-media}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_media"
>title="Añada medios al mensaje en la aplicación para crear una experiencia atractiva para el usuario final."
>abstract="Proporcione un vínculo directo al contenido o utilice el selector de recursos para seleccionar medios en Asset Essentials y añadirlos a su mensaje."

El campo **[!UICONTROL Medios]** le permite agregar contenido multimedia al mensaje en la aplicación para crear una experiencia atractiva para el usuario final.

![](assets/in_app_web_design_3.png)

Escriba su URL de medios o haga clic en el icono **[!UICONTROL Seleccionar Assets]** para agregar directamente a su mensaje en la aplicación los recursos almacenados en su biblioteca de Assets. [Más información acerca de la administración de recursos](../integrations/assets.md).
También puede agregar **[!UICONTROL texto alternativo]** para las aplicaciones de lectura de pantalla.

+++Más opciones con formato avanzado

Si el **[!UICONTROL modo de formato avanzado]** está activado, puedes personalizar la **[!UICONTROL altura máxima]** y la **[!UICONTROL anchura máxima]** de tus medios.

+++

### Contenido {#title-body}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_content"
>title="Para redactar el mensaje, introduzca el contenido en los campos Encabezado y Cuerpo."
>abstract="Aquí se pueden añadir tanto el encabezado como el texto del cuerpo. Para incluir tókenes de personalización, abra el cuadro de diálogo de personalización."

Para redactar el mensaje, escribe el contenido en los campos **[!UICONTROL Encabezado]** y **[!UICONTROL Cuerpo]**.

![](assets/in_app_web_design_4.png)

Utilice el icono **[!UICONTROL Personalization]** para agregar personalización. Obtenga más información acerca de la personalización en el editor de personalización de Adobe Journey Optimizer [en esta sección](../personalization/personalize.md).

+++Más opciones con formato avanzado

Si el **[!UICONTROL modo de formato avanzado]** está activado, puedes elegir entre **[!UICONTROL Encabezado]** y **[!UICONTROL Cuerpo]**:

* la **[!UICONTROL fuente]**
* el **[!UICONTROL tamaño de objeto]**
* el **[!UICONTROL color de fuente]**
* la **[!UICONTROL alineación]**
+++

### Botones {#add-buttons}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_buttons"
>title="Añada botones para que los usuarios interactúen con el mensaje en la aplicación."
>abstract="Esta sección le permite añadir botones de llamada a la acción al mensaje. Puede incluir texto personalizado y destinos para cada botón."

Añada botones para que los usuarios interactúen con el mensaje en la aplicación.

![](assets/in_app_web_design_5.png)

Para personalizar el botón:

1. Edite el campo Button #1 text (primary). También puede usar el icono **[!UICONTROL Personalization]** para definir contenido y datos de personalización.

1. Elija su **[!UICONTROL evento de interacción]** que define la acción del botón después de que los usuarios interactuaran con él.

1. Escriba la URL web o el vínculo profundo en el campo **[!UICONTROL Destino]**.

1. Para agregar varios botones, haga clic en **[!UICONTROL Agregar botón]**.

+++Más opciones con formato avanzado

Si el **[!UICONTROL modo de formato avanzado]** está activado, puede elegir los **[!UICONTROL botones]**:

* la **[!UICONTROL fuente]**
* el **[!UICONTROL tamaño de objeto]**
* el **[!UICONTROL color de fuente]**
* la **[!UICONTROL alineación]**
* el **[!UICONTROL estilo de botón]**
* el **[!UICONTROL radio]**
* el **[!UICONTROL color del botón]**

+++

## Pestaña Configuración {#settings-tab}

En la pestaña **Configuración**, puede definir el diseño del mensaje y previsualizar el mensaje en la aplicación. También puede acceder a las opciones de formato avanzadas.

### Vista previa {#preview-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_preview"
>title="Previsualice el mensaje en la aplicación."
>abstract="Esta es la imagen de vista previa que se mostrará cuando el mensaje se envíe al resumen del mensaje del dispositivo."

>[!NOTE]
>
>La vista previa solo está disponible para mensajes móviles en la aplicación.

![](assets/in_app_content_6.png)

La **[!UICONTROL Vista previa de la aplicación]** le permite agregar un fondo detrás del mensaje en la aplicación:

* Un contenido de un vínculo URL.

* Un recurso de su biblioteca de Assets.

* Un color de fondo.

### Diseño {#layout-options}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_layout"
>title="Defina el diseño del mensaje en la aplicación."
>abstract="Esta sección le permite añadir un fondo al mensaje en la aplicación. Esto requiere que la adquisición de la IU esté habilitada."

![](assets/in_app_web_design_6.png)

El campo **[!UICONTROL Imagen de fondo]** le permite agregar un fondo al mensaje en la aplicación:

* Un contenido de un vínculo URL.

* Un color de fondo.

### Mensaje {#message-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_message_advanced"
>title="Defina la configuración avanzada del mensaje."
>abstract="Esta sección le permite mejorar la personalización del contenido en la aplicación, especialmente cuando tiene activado el Formato avanzado."

![](assets/in_app_web_design_7.png)

La opción de IU activada de forma predeterminada, permite oscurecer el fondo del mensaje en la aplicación para resaltar el enfoque en el contenido.

+++Más opciones con formato avanzado

Si el **[!UICONTROL modo de formato avanzado]** está activado, puede personalizar aún más el mensaje con las siguientes opciones:

* **[!UICONTROL Personalizar gestos]**: permite personalizar la interacción del barrido de usuario. Si se selecciona desechar, se puede añadir un evento de interacción personalizado o un destino de destino.

* **[!UICONTROL Personalizar adquisición de IU]**: permite seleccionar un color para mostrarlo en el fondo y su opacidad.

* **[!UICONTROL Personalizar tamaño]**: permite ajustar la anchura y altura de la notificación en la aplicación.

* **[!UICONTROL Personalizar posición]**: permite personalizar la posición de los mensajes en la aplicación en la pantalla de los usuarios. Puede cambiar las alineaciones Vertical y Horizontal.

* **[!UICONTROL Personalizar animación]**: permite personalizar las animaciones Mostrar y Descartar, por ejemplo, si la notificación en la aplicación aparece a la izquierda o en la parte superior del dispositivo del usuario.

* **[!UICONTROL Esquina redonda de mensaje]**: permite agregar una esquina redonda a la notificación en la aplicación cambiando el **[!UICONTROL Radio de vértice]**.

+++

## Pestaña Datos {#data-tab}

Desde la ficha **Datos**, puede definir una **[!UICONTROL Clave]**&#x200B; y un **[!UICONTROL Valor]** para incluir variables personalizadas en la carga. Estos pares clave/valor le permiten pasar datos adicionales, según la configuración específica.

Para obtener más información, consulte [Documentación para desarrolladores](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/in-app-message/tutorials/messaging-metadata/).

1. En la ficha **[!UICONTROL Datos]**, seleccione **[!UICONTROL Agregar par clave/valor]**.

   ![](assets/in-app-data-menu.png)

1. Rellene los campos **[!UICONTROL Clave]**&#x200B; y **[!UICONTROL Valor]**.

   ![](assets/in-app-data-menu-1.png)

1. Haga clic en ![](assets/do-not-localize/Smock_Delete_18_N.svg) para eliminar cualquier par que se necesite.

**Temas relacionados:**

* [Crear mensaje en la aplicación](create-in-app.md)
* [Informe en la aplicación](../reports/campaign-global-report-cja-inapp.md)
* [Configuración en la aplicación](inapp-configuration.md)

## Vídeo práctico{#video}

El siguiente vídeo muestra cómo crear y probar los mensajes en la aplicación.

>[!VIDEO](https://video.tv.adobe.com/v/3410471?quality=12&learn=on)
