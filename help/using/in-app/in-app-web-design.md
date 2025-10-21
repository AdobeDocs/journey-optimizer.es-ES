---
title: Diseño del contenido web en la aplicación
description: Aprenda a diseñar el contenido web en la aplicación
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: en la aplicación, mensaje, creación, inicio
hide: true
hidefromtoc: true
source-git-commit: 722d37dc4bcb9ab7983ea336aa0b12a6a09e01dc
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 7%

---

# Diseño del contenido web en la aplicación {#in-app-web-design}

>[!BEGINSHADEBOX]

**Tabla de contenidos**

* [Configuración del canal web en la aplicación](configure-in-app-web.md)
* [Creación de la campaña de mensajes en la aplicación web](create-in-app-web.md)
* Diseño del contenido web en la aplicación

>[!ENDSHADEBOX]

Para editar el contenido del mensaje en la aplicación, haga clic en el botón **[!UICONTROL Editar contenido]** del menú **[!UICONTROL Acción]** de su campaña.

![](assets/in_app_web_surface_7.png)

La opción **[!UICONTROL Formato avanzado]** activa opciones adicionales para personalizar la experiencia.

Una vez creado el mensaje en la aplicación, y definido y personalizado su contenido, puede revisarlo y activarlo. Las notificaciones se envían según la programación de campaña. Obtenga más información en [esta página](send-in-app.md).

## Diseño del mensaje {#message-layout}

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

El campo **[!UICONTROL Medios]** le permite agregar contenido multimedia al mensaje en la aplicación para crear una experiencia atractiva para el usuario final.

![](assets/in_app_web_design_3.png)

Escriba su URL de medios o haga clic en el icono **[!UICONTROL Seleccionar Assets]** para agregar directamente a su mensaje en la aplicación los recursos almacenados en su biblioteca de Assets. <!--[Learn more about asset management](../content-management/assets-essentials.md).-->

También puede agregar **[!UICONTROL texto alternativo]** para las aplicaciones de lectura de pantalla.

+++Más opciones con formato avanzado

Si el **[!UICONTROL modo de formato avanzado]** está activado, puedes personalizar la **[!UICONTROL altura máxima]** y la **[!UICONTROL anchura máxima]** de tus medios.

+++

### Contenido {#title-body}

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

### Diseño {#layout-options}

![](assets/in_app_web_design_6.png)

El campo **[!UICONTROL Imagen de fondo]** le permite agregar un fondo al mensaje en la aplicación:

* Un contenido de un vínculo URL.

* Un color de fondo.

### Mensaje {#message-tab}

![](assets/in_app_web_design_7.png)

La opción de IU activada de forma predeterminada, permite oscurecer el fondo del mensaje en la aplicación para resaltar el enfoque en el contenido.

+++Más opciones con formato avanzado

Si el **[!UICONTROL modo de formato avanzado]** está activado, puede personalizar aún más el mensaje con las siguientes opciones:

* **[!UICONTROL Personalizar adquisición de IU]**: permite seleccionar un color para mostrarlo en el fondo y su opacidad.

* **[!UICONTROL Personalizar tamaño]**: permite ajustar la anchura y altura de la notificación en la aplicación.

* **[!UICONTROL Personalizar posición]**: permite personalizar la posición de los mensajes en la aplicación en la pantalla de los usuarios. Puede cambiar las alineaciones Vertical y Horizontal.

* **[!UICONTROL Esquina redonda de mensaje]**: permite agregar una esquina redonda a la notificación en la aplicación cambiando el **[!UICONTROL Radio de vértice]**.

+++

**Temas relacionados:**

* [Prueba y envío de un mensaje en la aplicación](send-in-app.md)
* [Informe en la aplicación](../reports/campaign-global-report-cja-inapp.md)
* [Configuración en la aplicación](inapp-configuration.md)