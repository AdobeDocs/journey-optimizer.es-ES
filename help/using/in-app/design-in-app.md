---
title: Diseño del contenido en la aplicación
description: Aprenda a diseñar el contenido en la aplicación en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: en la aplicación, mensaje, diseño, formato
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 0c32248d13c08a98e9298ddc932aa2e547ab2acd
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 6%

---

# Diseño del contenido en la aplicación {#design-content}

Puede editar el contenido en la aplicación para configurar las opciones de experiencia:

* En un **[!UICONTROL Campaign]**, desde el **[!UICONTROL Acción]** , para configurar el contenido del mensaje, haga clic en **[!UICONTROL Editar contenido]** botón.

   ![](assets/edit-in-app-content.png)

* En un **[!UICONTROL Recorrido]**, en el menú avanzado de la aplicación **[!UICONTROL Acción]**, puede empezar a diseñar el contenido con **[!UICONTROL Editar contenido]** botón.

   ![](assets/design_inapp_journey.png)

El **[!UICONTROL Formato avanzado]** esta opción activa opciones adicionales para personalizar la experiencia.

Una vez creado el mensaje en la aplicación, y definido y personalizado su contenido, puede revisarlo y activarlo. Las notificaciones se envían según la programación de campaña. Obtenga más información en [esta página](send-in-app.md).

## Diseño del mensaje {#message-layout}

Desde el **[!UICONTROL Diseño del mensaje]** , seleccione una de las cuatro opciones de diseño diferentes para elegir según sus necesidades de mensajería.

![](assets/in_app_content_1.png)

* **[!UICONTROL Pantalla completa]**: este tipo de diseño cubre toda la pantalla de los dispositivos de destino.

   Admite componentes multimedia (imagen, vídeo), de texto y botones.

* **[!UICONTROL Modal]**: este diseño aparece en una ventana grande como si fuera una alerta. La aplicación sigue visible en segundo plano.

   Admite componentes multimedia (imagen, vídeo), de texto y botones.

* **[!UICONTROL Titular]**: este tipo de diseño aparece como un mensaje de alerta de sistema operativo nativo.

   Solo puede agregar un **[!UICONTROL Header]** y una **[!UICONTROL Cuerpo]** a su mensaje.

* **[!UICONTROL Personalizado]**: el modo de mensaje personalizado le permite importar y editar directamente uno de los mensajes preconfigurados del HTML.

   * Seleccionar **[!UICONTROL Escribir]** para introducir o pegar el código de HTML sin procesar.

      Utilice el panel izquierdo para aprovechar las funcionalidades de personalización de Journey Optimizer. Para obtener más información, consulte [esta sección](../personalization/personalize.md).

   * Seleccionar **[!UICONTROL Importar]** para importar el archivo HTML o .zip que contiene el contenido del HTML.

## Pestaña Contenido {#content-tab}

Desde el **Contenido** puede definir y personalizar: el contenido de la notificación y el estilo de la **Cerrar** botón. También puede añadir contenido multimedia a la notificación en la aplicación y añadir botones de acción desde esta pestaña.

### Botón Cerrar {#close-button}

![](assets/in_app_content_2.png)

Elija la **[!UICONTROL Estilo]** de su **[!UICONTROL Botón Cerrar]**.

Los estilos disponibles son:

* **[!UICONTROL Sencilla]**
* **[!UICONTROL Círculo]**
* **[!UICONTROL Imagen personalizada]** desde una URL de medios o sus recursos.

+++Más opciones con formato avanzado

Si la variable **[!UICONTROL Modo de formato avanzado]** está activada, puede comprobar las **[!UICONTROL Color]** para elegir el color y la opacidad del botón.

+++

### Medios {#add-media}

El **[!UICONTROL Medios]** Este campo le permite añadir contenido multimedia al mensaje en la aplicación para crear una experiencia atractiva para el usuario final.

![](assets/in_app_content_3.png)

Escriba la URL de medios o haga clic en **[!UICONTROL Seleccionar recursos]** para añadir directamente a su mensaje en la aplicación los recursos almacenados en la biblioteca de recursos. [Más información sobre la administración de recursos](../email/assets-essentials.md).
También puede agregar un **[!UICONTROL Texto alternativo]** para aplicaciones de lectura de pantalla.

+++Más opciones con formato avanzado

Si la variable **[!UICONTROL Modo de formato avanzado]** está activada, puede personalizar la variable **[!UICONTROL Altura máxima]** y **[!UICONTROL Anchura máxima]** de sus medios.

+++

### Encabezado y cuerpo {#title-body}

Para redactar el mensaje, introduzca el contenido en la **[!UICONTROL Header]** y **[!UICONTROL Cuerpo]** campos.

![](assets/in_app_content_4.png)

Utilice el **[!UICONTROL Personalización]** para añadir personalización. Obtenga más información acerca de la personalización en el Editor de expresiones de Adobe Journey Optimizer [en esta sección](../personalization/personalize.md).

+++Más opciones con formato avanzado

Si la variable **[!UICONTROL Modo de formato avanzado]** está activado, puede elegir para su **[!UICONTROL Header]** y **[!UICONTROL Cuerpo]**:

* el **[!UICONTROL Fuente]**
* el **[!UICONTROL Tamaño de punto]**
* el **[!UICONTROL Color de fuente]**
* el **[!UICONTROL Alineación]**
+++

### Botones {#add-buttons}

Agregue botones para que los usuarios interactúen con el mensaje en la aplicación.

![](assets/in_app_content_5.png)

Para personalizar el botón:

1. Edite el campo Button #1 text (primary). También puede utilizar la variable **[!UICONTROL Personalización]** para definir el contenido y los datos de personalización.

1. Elija su **[!UICONTROL Evento Interact]** que define la acción del botón después de que los usuarios interactuaran con él.

1. Introduzca la URL web o el vínculo profundo en la **[!UICONTROL Target]** field.

1. Para añadir varios botones, haga clic en **[!UICONTROL Botón Añadir]**.

+++Más opciones con formato avanzado

Si la variable **[!UICONTROL Modo de formato avanzado]** está activado, puede elegir para su **[!UICONTROL Botones]**:

* el **[!UICONTROL Fuente]**
* el **[!UICONTROL Tamaño de punto]**
* el **[!UICONTROL Color de fuente]**
* el **[!UICONTROL Alineación]**
* el **[!UICONTROL Estilo de botón]**
* el **[!UICONTROL Radio]**
* el **[!UICONTROL Color del botón]**

+++

## Configuración  pestaña {#settings-tab}

Desde el **Configuración** pestaña, puede definir el diseño del mensaje y previsualizar el mensaje en la aplicación. También puede acceder a las opciones de formato avanzadas.

### Vista previa {#preview-tab}

![](assets/in_app_content_6.png)

El **[!UICONTROL Vista previa de aplicación]** le permite añadir un fondo detrás del mensaje en la aplicación:

* Un contenido de un vínculo URL.

* Un recurso de su biblioteca de recursos.

* Un color de fondo.

### Diseño {#layout-options}

![](assets/in_app_content_7.png)

El **[!UICONTROL Imagen de fondo]** Este campo le permite añadir un fondo al mensaje en la aplicación:

* Un contenido de un vínculo URL.

* Un color de fondo.

### Mensaje {#message-tab}

![](assets/in_app_content_8.png)

La opción de IU activada de forma predeterminada, permite oscurecer el fondo del mensaje en la aplicación para resaltar el enfoque en el contenido.

+++Más opciones con formato avanzado

Si la variable **[!UICONTROL Modo de formato avanzado]** está activado, puede personalizar aún más el mensaje con las siguientes opciones:

* **[!UICONTROL Personalizar gestos]**: le permite personalizar qué es la interacción de barrido de usuario. Si se selecciona desechar, se puede añadir un evento de interacción personalizado o un destino de destino.

* **[!UICONTROL Personalizar adquisición de IU]**: permite seleccionar un color para mostrarlo en el fondo y su opacidad.

* **[!UICONTROL Personalizar tamaño]**: le permite ajustar la anchura y altura de la notificación en la aplicación.

* **[!UICONTROL Personalizar posición]**: le permite personalizar la posición de los mensajes en la aplicación en la pantalla de los usuarios. Puede cambiar las alineaciones Vertical y Horizontal.

* **[!UICONTROL Personalizar animación]**: le permite personalizar las animaciones de visualización y descarte, por ejemplo, si la notificación en la aplicación aparece desde la izquierda o desde la parte superior del dispositivo del usuario.

* **[!UICONTROL Esquina de redondeo del mensaje]**: le permite añadir una esquina redonda a la notificación en la aplicación cambiando el **[!UICONTROL Radio de vértice]**.

+++

**Temas relacionados:**

* [Crear un mensaje en la aplicación](create-in-app.md)
* [Informe en la aplicación](../reports/campaign-global-report.md#inapp-report)
* [Configuración en la aplicación](inapp-configuration.md)

## Vídeo explicativo{#video}

El siguiente vídeo muestra cómo crear y probar los mensajes en la aplicación.

>[!VIDEO](https://video.tv.adobe.com/v/3410471?quality=12&learn=on)
