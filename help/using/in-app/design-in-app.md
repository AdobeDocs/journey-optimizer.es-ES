---
title: Diseño del contenido en la aplicación
description: Aprenda a diseñar su contenido en la aplicación en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---

# Diseño del contenido en la aplicación {#design-content}

Puede editar el contenido en la aplicación para configurar las opciones de experiencia, incluido el diseño y la visualización del mensaje, el texto y las opciones de botones.

Para configurar el contenido del mensaje, haga clic en el botón **[!UICONTROL Edit content]** y utilice las opciones de la sección derecha de la pantalla para diseñar el contenido del mensaje en la aplicación.

![](assets/edit-in-app-content.png)

La variable **[!UICONTROL Advanced formatting]** activa opciones adicionales para personalizar la experiencia.

Una vez creado el mensaje en la aplicación y definido y personalizado su contenido, puede revisarlo y activarlo. Las notificaciones se envían según la programación de la campaña. Obtenga más información en [esta página](create-in-app.md#in-app-send).

## Diseño del mensaje {#message-layout}

En el **[!UICONTROL Message Layout]** , seleccione una de las cuatro opciones de diseño diferentes para elegir según sus necesidades de mensajería.

![](assets/in_app_content_1.png)

* **[!UICONTROL Fullscreen]**: Este tipo de diseño cubre toda la pantalla de los dispositivos de destino.

   Admite componentes multimedia (imagen, vídeo), de texto y botones.

* **[!UICONTROL Modal]**: Este diseño aparece en una ventana grande como si fuera una alerta. La aplicación sigue visible en segundo plano.

   Admite componentes multimedia (imagen, vídeo), de texto y botones.

* **[!UICONTROL Banner]**: Este tipo de diseño aparece como un mensaje de alerta de sistema operativo nativo.

   Solo se puede añadir un **[!UICONTROL Header]** y **[!UICONTROL Body]** a su mensaje.

* **[!UICONTROL Custom]**: El modo de mensaje personalizado le permite importar y editar directamente uno de los mensajes HTML preconfigurados.

   * Select **[!UICONTROL Compose]** para introducir o pegar el código HTML sin procesar.

      Utilice el panel izquierdo para aprovechar las funciones de personalización de Journey Optimizer. Para obtener más información, consulte [esta sección](../personalization/personalize.md).

   * Select **[!UICONTROL Import]** para importar el archivo HTML o .zip que contiene el contenido HTML.

## Pestaña Contenido {#content-tab}

En el **Contenido** , puede definir y personalizar: el contenido de la notificación y el estilo del **Cerrar** botón. También puede añadir un contenido a la notificación en la aplicación y añadir botones de acción desde esta pestaña.

### Botón Cerrar {#close-button}

![](assets/in_app_content_2.png)

Elija la **[!UICONTROL Style]** de su **[!UICONTROL Close button]**.

Los estilos disponibles son:

* **[!UICONTROL Simple]**
* **[!UICONTROL Circle]**
* **[!UICONTROL Custom image]** desde una URL de medios o sus recursos.

+++Más opciones con formato avanzado

Si la variable **[!UICONTROL Advanced formatting mode]** está activada, puede comprobar la **[!UICONTROL Color]** para elegir el color y la opacidad del botón.

+++

### Medios {#add-media}

La variable **[!UICONTROL Media]** le permite añadir contenido multimedia al mensaje en la aplicación para crear una experiencia atractiva para el usuario final.

![](assets/in_app_content_3.png)

Escriba la URL del medio o haga clic en el botón **[!UICONTROL Select Assets]** para añadir directamente los recursos almacenados en la biblioteca de Assets al mensaje en la aplicación. [Obtenga más información sobre la administración de recursos](../email/assets-essentials.md).
También puede agregar una **[!UICONTROL Alternative text]** para aplicaciones de lectura de pantalla.

+++Más opciones con formato avanzado

Si la variable **[!UICONTROL Advanced formatting mode]** está activada, puede personalizar el **[!UICONTROL Max height]** y **[!UICONTROL Max width]** del medio.

+++

### Encabezado y cuerpo {#title-body}

Para componer el mensaje, introduzca el contenido en la **[!UICONTROL Header]** y **[!UICONTROL Body]** campos.

![](assets/in_app_content_4.png)

Utilice la variable **[!UICONTROL Personalization]** para añadir personalización. Obtenga más información sobre la personalización en el Editor de expresiones de Adobe Journey Optimizer [en esta sección](../personalization/personalize.md).

+++Más opciones con formato avanzado

Si la variable **[!UICONTROL Advanced formatting mode]** está activada, puede elegir para **[!UICONTROL Header]** y **[!UICONTROL Body]**:

* el **[!UICONTROL Font]**
* el **[!UICONTROL Pt size]**
* el **[!UICONTROL Font Color]**
* el **[!UICONTROL Alignment]**
+++

### Botones {#add-buttons}

Agregue botones para que los usuarios interactúen con su mensaje en la aplicación.

![](assets/in_app_content_5.png)

Para personalizar el botón:

1. Edite el campo de texto Botón #1 (principal) . También puede usar la variable **[!UICONTROL Personalization]** para definir el contenido y los datos de personalización.

1. Elija su **[!UICONTROL Interact event]** que define la acción del botón después de que los usuarios interactuaran con él.

1. Introduzca la URL web o el vínculo profundo en la **[!UICONTROL Target]** campo .

1. Para agregar varios botones, haga clic en **[!UICONTROL Add button]**.

+++Más opciones con formato avanzado

Si la variable **[!UICONTROL Advanced formatting mode]** está activada, puede elegir para **[!UICONTROL Buttons]**:

* el **[!UICONTROL Font]**
* el **[!UICONTROL Pt size]**
* el **[!UICONTROL Font Color]**
* el **[!UICONTROL Alignment]**
* el **[!UICONTROL Button style]**
* el **[!UICONTROL Radius]**
* el **[!UICONTROL Button color]**

+++

## Ficha Configuración {#settings-tab}

En el **Configuración** , puede definir el diseño del mensaje y previsualizar el mensaje en la aplicación. También puede acceder a las opciones avanzadas de formato.

### Vista previa {#preview-tab}

![](assets/in_app_content_6.png)

La variable **[!UICONTROL App Preview]** le permite añadir un fondo detrás del mensaje en la aplicación:

* Medios de un vínculo de URL.

* Un recurso de la biblioteca de recursos.

* Color de fondo.

### Diseño {#layout-options}

![](assets/in_app_content_7.png)

La variable **[!UICONTROL Background image]** permite añadir un fondo al mensaje en la aplicación:

* Medios de un vínculo de URL.

* Color de fondo.

### Mensaje {#message-tab}

![](assets/in_app_content_8.png)

La opción de adquisición de interfaz de usuario, activada de forma predeterminada, le permite oscurecer el fondo del mensaje en la aplicación para resaltar el enfoque en el contenido.

+++Más opciones con formato avanzado

Si la variable **[!UICONTROL Advanced formatting mode]** está activada, puede personalizar aún más el mensaje con las siguientes opciones:

* **[!UICONTROL Customize gestures]**: le permite personalizar lo que es la interacción de barrido del usuario. Si se selecciona rechazar , puede agregar un evento de interacción personalizado o un destino de destino.

* **[!UICONTROL Customize UI takeover]**: permite seleccionar un color para mostrar en el fondo y su opacidad.

* **[!UICONTROL Customize size]**: le permite ajustar la anchura y la altura de la notificación en la aplicación.

* **[!UICONTROL Customize position]**: le permite personalizar la posición de los mensajes en la aplicación en la pantalla de los usuarios. Puede cambiar las alineaciones verticales y horizontales.

* **[!UICONTROL Customize animation]**: le permite personalizar las animaciones de visualización y de rechazo, por ejemplo, si la notificación en la aplicación aparece a la izquierda o en la parte superior del dispositivo del usuario.

* **[!UICONTROL Message round corner]**: le permite añadir una esquina redonda a la notificación en la aplicación cambiando el **[!UICONTROL Corner radius]**.

+++

**Temas relacionados:**

* [Crear mensaje en la aplicación](create-in-app.md)
* [Informe en la aplicación](inapp-report.md)
* [Configuración en la aplicación](inapp-configuration.md)
