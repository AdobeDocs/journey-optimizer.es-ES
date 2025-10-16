---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a Journey Optimizer para los ingenieros de datos
description: Obtenga más información sobre cómo trabajar con Journey Optimizer como ingeniero de datos
feature: Get Started
role: Data Engineer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 6c73a1ee024ca61b30d71e77268e51b93576ae62
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 100%

---

# Introducción para ingenieros de datos {#data-engineer}

Como **Ingeniero de datos de Adobe Journey Optimizer**, prepare y mantenga datos de perfil del cliente para potenciar las experiencias orquestadas por [!DNL Journey Optimizer], modele los datos de cliente y empresa en esquemas y configure los conectores de origen para la ingesta de datos. Puede comenzar a trabajar con [!DNL Adobe Journey Optimizer] una vez que el [Administrador de sistemas](administrator.md) le conceda acceso y prepare su entorno.


Obtenga información sobre cómo **identificar datos y crear esquemas y conjuntos de datos** para introducir sus datos en Adobe Experience Platform en esta página.

>[!NOTE]
>
>Obtenga más información sobre la **ingesta de datos** en la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=es){target="_blank"}.

Los pasos para crear un espacio de nombres de identidad y un conjunto de datos habilitado para perfiles y perfiles de prueba se detallan en las secciones siguientes:

1. **Cree un espacio de nombres de identidad**. En Adobe [!DNL Journey Optimizer], las **Identidades** vinculan los consumidores con dispositivos y canales, y el resultado es un gráfico de identidad. El gráfico de identidad vinculado se utiliza para personalizar las experiencias en función de las interacciones en todos los puntos de contacto empresariales.  Obtenga más información acerca de identidades y espacios de nombres de identidad [en esta página](../../audience/get-started-identity.md).

1. **Cree un esquema** y actívelo para los perfiles. Un esquema es un conjunto de reglas que representan y validan la estructura y el formato de los datos. En un nivel superior, los esquemas proporcionan una definición abstracta de un objeto del mundo real (como una persona) y describen qué datos deben incluirse en cada instancia de ese objeto (como nombre, apellido, cumpleaños, etc.).  Obtenga más información acerca de los esquemas [en esta página](../../data/get-started-schemas.md).

1. **Cree conjuntos de datos** y actívelos para los perfiles. Un conjunto de datos es una construcción de almacenamiento y administración para una colección de datos, normalmente una tabla, que contiene un esquema (columnas) y campos (filas). Los conjuntos de datos también contienen metadatos que describen varios aspectos de los datos que almacenan. Una vez creado un conjunto de datos, puede asignarlo a un esquema existente y agregarle datos. Más información acerca de los conjuntos de datos [en esta página](../../data/get-started-datasets.md).

1. **Configure conectores de fuentes**. Adobe Journey Optimizer permite la introducción de datos de fuentes externas, al tiempo que le ofrece la capacidad de estructurar, etiquetar y mejorar los datos entrantes mediante los servicios de Platform. Puede ingerir datos de una variedad de fuentes, como aplicaciones de Adobe, almacenamiento basado en la nube, bases de datos y muchas otras. Obtenga más información acerca de los conectores de fuentes [en esta página](../get-started-sources.md).

1. **Creación de perfiles de prueba**. Los perfiles de prueba son obligatorios al usar el [modo de prueba](../../building-journeys/testing-the-journey.md) en un recorrido y para [previsualizar y probar los mensajes](../../content-management/preview-test.md) antes de enviarlos. Los pasos para crear perfiles de prueba se detallan [en esta página](../../audience/creating-test-profiles.md).


Además, para poder enviar mensajes en recorridos, debe configurar **[!UICONTROL Fuentes de datos]**, **[!UICONTROL Eventos]** y **[!UICONTROL Acciones]**. Obtenga más información [en esta sección](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* La configuración de la **fuente de datos** permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos. Obtenga más información acerca de las fuentes de datos [en esta sección](../../datasource/about-data-sources.md).

* Los **Eventos** le permiten activar sus recorridos de forma unitaria para enviar mensajes, en tiempo real, a la persona que entra en el recorrido. En la configuración de eventos, se configuran los eventos esperados en los recorridos. Los datos entrantes de los eventos se normalizan siguiendo el Modelo de datos de experiencia de Adobe (XDM). Los eventos provienen de las API de ingesta de transmisión para eventos autenticados y no autenticados (como eventos del SDK de Adobe Mobile). Obtenga más información acerca de los eventos [en esta sección](../../event/about-events.md).

* [!DNL Journey Optimizer] viene con funcionalidades de mensajes integradas: puede crear los mensajes dentro de un recorrido y diseñar el contenido. Si utiliza un sistema de terceros para enviar mensajes, como Adobe Campaign, cree una **acción personalizada**. Obtenga más información acerca de las acciones [en esta sección](../../action/action.md).
