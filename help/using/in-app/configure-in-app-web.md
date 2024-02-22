---
title: Creación de un mensaje web en la aplicación en Journey Optimizer
description: Obtenga información sobre cómo crear un mensaje web en la aplicación en Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: en la aplicación, mensaje, creación, inicio
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 2%

---


# Configuración del canal web en la aplicación {#configure-in-app-web}

## Requisitos previos {#prerequisites}

* Asegúrese de que está utilizando la versión más reciente para su **SDK web de Adobe Experience Platform** extensión.

* Instale el **SDK web de Adobe Experience Platform** extensión en su **Propiedades de etiqueta** y habilite la **Almacenamiento de personalización** opción.

  Esta configuración es esencial para almacenar historiales de eventos en el cliente, un requisito previo para implementar Reglas de frecuencia en el Generador de reglas. [Más información](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

  ![](assets/configure_web_inapp_1.png)

## Configurar los datos enviados a la regla de plataforma {#configure-sent-data-trigger}

1. Acceda a su **Recopilación de datos de Adobe Experience Platform** y vaya a **Propiedades de etiqueta** configurado con la variable **SDK web de Adobe Experience Platform** extensión.

1. Desde el **Creación** menú, seleccione **Reglas** entonces **Crear nueva regla** o **Añadir regla**.

   ![](assets/configure_web_inapp_2.png)

1. En el **Eventos** , haga clic en **Añadir** y configúrelo como se indica a continuación:

   * **Extensión**: Core

   * **Tipo de evento**: Biblioteca cargada (Principio de página).

   ![](assets/configure_web_inapp_3.png)

1. Clic **Conservar cambios** para guardar la configuración de Evento.

1. En el **Acciones** , haga clic en **Añadir** y configúrelo como se indica a continuación:

   * **Extensión**: SDK web de Adobe Experience Platform

   * **Tipo de acción**: Enviar evento

   ![](assets/configure_web_inapp_4.png)

1. En el **Personalización** de su sección **Acción** escriba, habilite el **Procesar decisiones de personalización visuales** opción.

   ![](assets/configure_web_inapp_5.png)

1. En el **Contexto de decisión** , defina la **Clave** y **Valor** pares que determinan qué experiencia se ofrece.

   ![](assets/configure_web_inapp_6.png)

1. Guarde su **Acción** haciendo clic en **Conservar cambios**.

1. Vaya a **Flujo de publicación** menú. Crear un nuevo **Biblioteca** o seleccione una existente **Biblioteca** y añada el recién creado **Regla** a ella. [Más información](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. De su **Biblioteca**, seleccione **Guardar y generar en desarrollo**.

   ![](assets/configure_web_inapp_7.png)

## Configurar regla manual {#configure-manual-trigger}

1. Acceda a su **Recopilación de datos de Adobe Experience Platform** y vaya a **Propiedades de etiqueta** configurado con la variable **SDK web de Adobe Experience Platform** extensión.

1. Desde el **Creación** menú, seleccione **Reglas** entonces **Crear nueva regla** o **Añadir regla**.

   ![](assets/configure_web_inapp_8.png)

1. En el **Eventos** , haga clic en **Añadir** y configúrelo como se indica a continuación:

   * **Extensión**: Core

   * **Tipo de evento**: haga clic en

   ![](assets/configure_web_inapp_9.png)

1. En el **Haga clic en configuración**, defina la **Selector** que se evaluarán.

   ![](assets/configure_web_inapp_10.png)

1. Clic **Conservar cambios** para guardar **Evento** configuración.

1. En el **Acciones** , haga clic en **Añadir** y configúrelo como se indica a continuación:

   * **Extensión**: SDK web de Adobe Experience Platform

   * **Tipo de acción**: Evaluar conjuntos de reglas

   ![](assets/configure_web_inapp_11.png)

1. En el **Acción Evaluar conjuntos de reglas** de su sección **Acción** escriba, habilite el **Procesar decisiones de personalización visuales** opción.

   ![](assets/configure_web_inapp_13.png)

1. En el **Contexto de decisión** , defina la **Clave** y **Valor** pares que determinan qué experiencia se ofrece.

1. Acceda a la **Flujo de publicación** menú, crear un nuevo **Biblioteca** o seleccione una existente **Biblioteca** y añada el recién creado **Regla**. [Más información](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. De su **Biblioteca**, seleccione **Guardar y generar en desarrollo**.

   ![](assets/configure_web_inapp_14.png)

