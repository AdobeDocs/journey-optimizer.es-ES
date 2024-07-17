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

* Compruebe que está utilizando la versión más reciente de su extensión **Adobe Experience Platform Web SDK**.

* Instale la extensión **Adobe Experience Platform Web SDK** en sus **propiedades de etiquetas** y habilite la opción **Personalization Storage**.

  Esta configuración es esencial para almacenar historiales de eventos en el cliente, un requisito previo para implementar Reglas de frecuencia en el Generador de reglas. [Más información](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

  ![](assets/configure_web_inapp_1.png)

## Configurar los datos enviados a la regla de plataforma {#configure-sent-data-trigger}

1. Acceda a su instancia de **recopilación de datos de Adobe Experience Platform** y vaya a **Propiedades de etiquetas** configuradas con la extensión **SDK web de Adobe Experience Platform**.

1. En el menú **Creación**, seleccione **Reglas** y luego **Crear nueva regla** o **Agregar regla**.

   ![](assets/configure_web_inapp_2.png)

1. En la sección **Events**, haga clic en **Add** y configúrelo de la siguiente manera:

   * **Extensión**: Principal

   * **Tipo de evento**: Biblioteca cargada (Principio de página).

   ![](assets/configure_web_inapp_3.png)

1. Haga clic en **Conservar cambios** para guardar la configuración del evento.

1. En la sección **Acciones**, haga clic en **Agregar** y configúrelo de la siguiente manera:

   * **Extensión**: SDK web de Adobe Experience Platform

   * **Tipo de acción**: Enviar evento

   ![](assets/configure_web_inapp_4.png)

1. En la sección **Personalization** de su tipo **Acción**, habilite la opción **Procesar decisiones de personalización visual**.

   ![](assets/configure_web_inapp_5.png)

1. En la sección **Contexto de decisión**, defina los pares **Clave** y **Valor** que determinan qué experiencia se ofrece.

   ![](assets/configure_web_inapp_6.png)

1. Guarde la configuración de **Action** haciendo clic en **Conservar cambios**.

1. Vaya al menú **Flujo de publicación**. Cree una nueva **biblioteca** o seleccione una **biblioteca** existente y agréguele la **regla** recién creada. [Más información](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. En su **biblioteca**, seleccione **Guardar y generar en desarrollo**.

   ![](assets/configure_web_inapp_7.png)

## Configurar regla manual {#configure-manual-trigger}

1. Acceda a su instancia de **recopilación de datos de Adobe Experience Platform** y vaya a **Propiedades de etiquetas** configuradas con la extensión **SDK web de Adobe Experience Platform**.

1. En el menú **Creación**, seleccione **Reglas** y luego **Crear nueva regla** o **Agregar regla**.

   ![](assets/configure_web_inapp_8.png)

1. En la sección **Events**, haga clic en **Add** y configúrelo de la siguiente manera:

   * **Extensión**: Principal

   * **Tipo de evento**: haga clic en

   ![](assets/configure_web_inapp_9.png)

1. En la **configuración de clic**, defina el **Selector** que se evaluará.

   ![](assets/configure_web_inapp_10.png)

1. Haga clic en **Conservar cambios** para guardar la configuración de **Evento**.

1. En la sección **Acciones**, haga clic en **Agregar** y configúrelo de la siguiente manera:

   * **Extensión**: SDK web de Adobe Experience Platform

   * **Tipo de acción**: Evaluar conjuntos de reglas

   ![](assets/configure_web_inapp_11.png)

1. En la sección **Evaluar la acción de conjuntos de reglas** de su tipo **Acción**, habilite la opción **Procesar decisiones de personalización visual**.

   ![](assets/configure_web_inapp_13.png)

1. En la sección **Contexto de decisión**, defina los pares **Clave** y **Valor** que determinan qué experiencia se ofrece.

1. Acceda al menú **Flujo de publicación**, cree una nueva **biblioteca** o seleccione una **biblioteca** existente y agregue la **regla** recién creada. [Más información](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. En su **biblioteca**, seleccione **Guardar y generar en desarrollo**.

   ![](assets/configure_web_inapp_14.png)

