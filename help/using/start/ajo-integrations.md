---
solution: Journey Optimizer
product: journey optimizer
title: Integración con otras soluciones
description: Obtenga más información sobre cómo integrar Journey Optimizer con otras soluciones
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 9331c5de057a8de0b52bc4db34c17bc3ab79f193
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 5%

---

# Integración con otras soluciones {#integration}

Con Adobe Journey Optimizer, puede administrar, conservar y exportar fácilmente estos datos a plataformas o sistemas que forman parte de su pila de tecnología. Estas integraciones le ayudan a abordar sus casos de uso específicos y a ampliar el ámbito funcional de Adobe Journey Optimizer.

>[!NOTE]
>
> Adobe Journey Optimizer, creado en Adobe Experience Platform, está conectado de forma nativa a [Adobe Perfil del cliente en tiempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target=&quot;_blank&quot;}. Esta fuente de datos integrada está preconfigurada y está diseñada para recuperar y utilizar datos del perfil del cliente en tiempo real (por ejemplo, comprobar si la persona que ha introducido un recorrido es cliente o no). Permite utilizar datos de perfil y datos de eventos de experiencia.


## Informes{#integration-reporting}

### Adobe Customer Journey Analytics{#integration-cja}

Puede exportar los datos generados por Journey Optimizer para realizar análisis avanzados en Customer Journey Analytics.

La integración de Journey Optimizer con Customer Journey Analytics proporciona una vista holística de todos sus recorridos con distribución automatizada de informes y visualizaciones personalizadas de los datos.

Después de crear el recorrido en Journey Optimizer, puede importar los datos de clientes al Customer Journey Analytics para iniciar informes y comprender el impacto de cada interacción que un cliente tenga con sus recorridos.

Más información sobre [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

### Adobe Analytics{#integration-aa}

Puede aprovechar todos los datos de evento de comportamiento de Adobe Analytics que ya está capturando y transmitiendo a Adobe Experience Platform para almacenar en déclencheur los recorridos y automatizar las experiencias para sus clientes.

Más información sobre [Journey Optimizer + Analytics](../event/about-analytics.md).

## Aprendizaje automático{#integration-intelligent-service}

La integración con Adobe Intelligent Services le permite aprovechar la potencia de la inteligencia artificial y el aprendizaje automático en casos de uso de experiencias del cliente. Esto permite que los analistas de marketing configuren predicciones específicas de las necesidades de una empresa mediante configuraciones de nivel empresarial sin necesidad de experiencia en ciencia de datos.

## Entrega de mensajes {#integration-messages}

Puede utilizar un sistema de terceros para enviar mensajes.

### Adobe Campaign{#integration-ac}

Una integración está disponible si tiene Adobe Campaign v7 o v8. Utilice esta integración para enviar correos electrónicos, notificaciones push y SMS mediante las funciones de mensajería transaccional de Adobe Campaign.

Más información sobre [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md).

También puede configurar una integración con Adobe Campaign Standard para enviar mensajes en sus recorridos.

Más información sobre [Journey Optimizer + Campaign Standard](../building-journeys/ajo-ac.md).

### Canales personalizados{#integration-custom}

Si utiliza un sistema de terceros para enviar mensajes o si desea que los recorridos envíen llamadas de API a un sistema de terceros, utilice acciones personalizadas para configurar su conexión con el recorrido. Por ejemplo, puede conectarse a los siguientes sistemas con acciones personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com/){target=&quot;_blank&quot;}, Firebase, etc.

Las acciones personalizadas son acciones adicionales definidas por usuarios técnicos y que se ponen a disposición de los especialistas en marketing. Una vez configurados, aparecen en la paleta izquierda del recorrido, en la **[!UICONTROL Acción]** categoría. Obtenga más información en [esta página](../building-journeys/about-journey-activities.md#action-activities).

Más información sobre [acciones personalizadas](../action/about-custom-action-configuration.md).

## Sistemas externos{#integration-external-systems}

Journey Optimizer le permite configurar conexiones a sistemas externos mediante fuentes de datos personalizadas y acciones personalizadas. Esto le permite, por ejemplo, enriquecer sus recorridos con datos procedentes de un sistema de reservas externo.

Aprenda a utilizar fuentes de datos externas para definir una conexión con un sistema de terceros en [esta sección](../datasource/external-data-sources.md).
