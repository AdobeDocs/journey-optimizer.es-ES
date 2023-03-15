---
title: Recopilación de datos
description: Obtenga más información sobre la recopilación de datos de comentarios de Administración de decisiones
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: c9e970bc231fc3d19f0243b71256ea0f5a981af7
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 3%

---

# Recopilación de datos de gestión de decisiones {#data-collection}

## Explicación de la recopilación de datos

Puede recopilar comentarios sobre el offer decisioning en Adobe Experience Platform, incluidas las ofertas que se muestran y la forma en que los usuarios interactúan con ellas. Estos datos se pueden utilizar para:
* Composición [Informes de gestión de decisiones](../reports/get-started-events.md);
* Uso [restricción de frecuencia](../offer-library/add-constraints.md#capping) reglas;
* Creación [Modelos de IA](../ranking/create-ranking-strategies.md) que puede utilizarse como método de clasificación.

## Tipos de eventos

La forma en que se recopilan los datos varía según el tipo de evento que se desea capturar.

### Eventos de decisión

Cada vez que la administración de decisiones toma una decisión, la información relacionada con ese evento de decisión es **automatically** enviado a Adobe Experience Platform para todos los canales. [Más información](../reports/get-started-events.md)

### Impresión y eventos de clic

Las impresiones y los clics de la administración de decisiones se definen de la siguiente manera:

* Un **impresión** es cuando se muestra una oferta a un usuario.

* A **click** es cuando un usuario hace clic o interactúa con una oferta.

Los comentarios sobre impresiones y clics se capturan en función de la variable [!DNL Journey Optimizer] canal que se utiliza.

**Correos electrónicos** creado por [!DNL Journey Optimizer] **automatically** rastrear impresiones y clics.

Sin embargo, **mayoría de los canales** requieren que los datos de impresiones y clics se envíen a Adobe Experience Platform como **evento de experiencia**. Esto incluye:

* Las páginas web que utilizan la variable [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es){target="_blank"} para procesar ofertas

* Aplicaciones móviles que usan la variable [SDK de Adobe Experience Platform Mobile](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} to render offers - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* Kioscos
* Mensajes enviados a través de aplicaciones de terceros
   <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>Los canales que utilizan una solicitud de API de decisión para recibir ofertas necesitan que se envíen comentarios como un evento de experiencia. En otras palabras, si la oferta necesita instrucciones sobre cómo procesarla, puede suponer que debe enviar comentarios como eventos de experiencia.

### Eventos personalizados

Los comentarios sobre eventos personalizados vinculados a una oferta se pueden enviar a Adobe Experience Platform según sus propias preferencias. Por ejemplo, si una oferta tiene varios botones, como *Interesado*, *No interesado*, etc., puede que desee enviar esos eventos por separado, pero también se pueden enviar como eventos de experiencia. <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## Envío de datos de comentarios

Para enviar datos de comentarios, debe crear un conjunto de datos para recopilar eventos y, para cada tipo de evento, definir un evento de experiencia que se enviará a Adobe Experience Platform.

* Obtenga información sobre cómo crear un conjunto de datos en el que se recopilen los eventos de experiencia [esta sección](create-dataset.md).

* Aprenda a definir eventos de experiencia para enviar datos de comentarios en [esta sección](schema-requirement.md).

