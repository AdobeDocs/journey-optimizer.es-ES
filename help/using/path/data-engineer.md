---
title: Introducción a Journey Optimizer para ingenieros de datos
description: Como ingeniero de datos, obtenga más información sobre cómo trabajar con Journey Optimizer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: f0c5b42984b76fee005fe0c0e10312d47f9d10e8
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 9%

---

# Introducción al ingeniero de datos {#data-engineer}

![ingeniero de datos](assets/do-not-localize/user-1.png)

Como **Ingeniero de datos de Adobe Journey Optimizer**, prepare y mantenga datos de perfil del cliente para potenciar las experiencias orquestadas por [!DNL Journey Optimizer], modele los datos de cliente y empresa en esquemas y configure los conectores de origen para la ingesta de datos. Puede empezar a trabajar con [!DNL Adobe Journey Optimizer] una vez que la variable [Administrador del sistema](administrator.md) le concedió acceso y preparó su entorno.


Obtenga información sobre cómo **identificar datos y crear esquema y conjunto de datos** para obtener los datos en Adobe Experience Platform en esta página.

>[!NOTE]
>
>Más información sobre **ingesta de datos** en [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=es){target=&quot;_blank&quot;}.

Los pasos para crear un área de nombres de identidad y un conjunto de datos habilitado para perfiles y perfiles de prueba se detallan en las secciones siguientes:

1. **Crear un área de nombres de identidad**. En Adobe [!DNL Journey Optimizer], **Identidades** vincular consumidores entre dispositivos y canales, el resultado es un gráfico de identidad. El gráfico de identidad vinculado se utiliza para personalizar las experiencias en función de las interacciones en todos los puntos de contacto empresariales.  Obtenga más información sobre identidades y áreas de nombres de identidad [en esta página](../get-started-identity.md).

1. **Crear un esquema** y actívelo para perfiles. Un esquema es un conjunto de reglas que representan y validan la estructura y el formato de los datos. En un nivel superior, los esquemas proporcionan una definición abstracta de un objeto real (como una persona) y describen qué datos deben incluirse en cada instancia de ese objeto (como nombre, apellido, cumpleaños, etc.).  Obtenga más información sobre los esquemas [en esta página](../get-started-schemas.md).

1. **Crear conjuntos de datos** y actívelo para perfiles. Un conjunto de datos es una construcción de almacenamiento y administración para una colección de datos, normalmente una tabla, que contiene un esquema (columnas) y campos (filas). Los conjuntos de datos también contienen metadatos que describen varios aspectos de los datos que almacenan. Una vez creado un conjunto de datos, puede asignarlo a un esquema existente y agregarle datos. Más información sobre los conjuntos de datos [en esta página](../get-started-datasets.md).

1. **Configuración de conectores de fuentes**. El Recorrido de Adobe Optimizer permite la ingesta de datos desde fuentes externas, al tiempo que le ofrece la capacidad de estructurar, etiquetar y mejorar los datos entrantes mediante los servicios de Platform. Puede ingerir datos de una variedad de fuentes, como aplicaciones de Adobe, almacenamiento basado en la nube, bases de datos y muchas otras. Más información sobre los conectores de origen [en esta página](../get-started-sources.md).

1. **Creación de perfiles de prueba**. Los perfiles de prueba son obligatorios al usar la variable [modo de prueba](../building-journeys/testing-the-journey.md) en un recorrido y para [obtener una vista previa y probar los mensajes](../preview.md) antes de enviar. Descubra los pasos para crear perfiles de prueba [en esta página](../../using/building-journeys/creating-test-profiles.md).


Además, para poder enviar mensajes en recorridos, debe configurar **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** y **[!UICONTROL Actions]**. Obtenga más información [en esta sección](../../using/configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* La variable **Fuente de datos** permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos. Más información sobre las fuentes de datos [en esta sección](../datasource/about-data-sources.md).

* **Eventos** le permite realizar el déclencheur de sus recorridos de forma unitaria para enviar mensajes, en tiempo real, a la persona que entra en el recorrido. En la configuración de eventos, se configuran los eventos esperados en los recorridos. Los datos entrantes de los eventos se normalizan siguiendo el modelo de datos de Adobe Experience (XDM). Los eventos provienen de las API de ingesta de transmisión para eventos autenticados y no autenticados (como eventos del SDK de Adobe Mobile). Más información sobre los eventos [en esta sección](../event/about-events.md).

* [!DNL Journey Optimizer] incorpora capacidades de mensajes: puede diseñar el contenido y publicar el mensaje. Si utiliza un sistema de terceros para enviar mensajes, como Adobe Campaign, cree un **acción personalizada**. Obtenga más información sobre las acciones en esta [en esta sección](../action/action.md).
