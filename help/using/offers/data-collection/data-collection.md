---
title: Recopilación de datos
description: Obtenga más información acerca de la recopilación de datos de comentarios de Administración de decisiones
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 1%

---

# Recopilación de datos de gestión de decisiones {#data-collection}

## Explicación de la recopilación de datos

Puede recopilar comentarios sobre el offer decisioning en Adobe Experience Platform, incluidos los que se muestran las ofertas y cómo interactúan los usuarios con ellas. Estos datos se pueden utilizar para lo siguiente:
* Composición [Informes de administración de decisiones](../reports/get-started-events.md);
* Uso de [restricción de frecuencia](../offer-library/add-constraints.md#capping) reglas;
* Edificio [modelos de IA](../ranking/create-ranking-strategies.md) que puede utilizarse como método de clasificación.

## Tipos de eventos

La forma en que se recopilan los datos varía según el tipo de evento que desee capturar.

### Eventos de decisión

Cada vez que la Administración de decisiones toma una decisión, la información relacionada con ese evento de decisión es **automáticamente** se envía a Adobe Experience Platform para todos los canales. [Más información](../reports/get-started-events.md)

### Eventos de impresión y clics

Las impresiones y clics de gestión de decisiones se definen de la siguiente manera:

* Un **impresión** El evento se produce cuando se muestra una oferta a un usuario.

* A **click** Este evento se produce cuando un usuario hace clic en una oferta o interactúa con ella.

Los comentarios sobre las impresiones y los clics se capturan según el [!DNL Journey Optimizer] canal que se utiliza.

1. Por un lado, algunos canales **automáticamente** rastrear impresiones y clics. Son las siguientes:

   * Correos electrónicos creados por [!DNL Journey Optimizer]
   * Notificaciones push móviles creadas por [!DNL Journey Optimizer]
   * Aplicaciones móviles que utilizan [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} o SDK móvil<!--TBC--> para procesar ofertas <!--need more info + link-->

   >[!NOTE]
   >
   >Si Adobe procesa la oferta visualmente para el usuario final del canal, puede suponer que Adobe enviará automáticamente los comentarios.

1. Por otro lado, algunos canales requieren que los datos de impresiones y clics se envíen a Adobe Experience Platform como un **evento de experiencia**.

   Excepto las aplicaciones móviles que utilizan [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} o SDK móvil<!--TBC-->Sin embargo, todos los canales que utilizan una solicitud de API de decisiones para recibir ofertas necesitan que se envíen comentarios como un evento de experiencia. Esto incluye:

   * Páginas web
   * Quioscos
   * Mensajes enviados a través de aplicaciones de terceros

   >[!NOTE]
   >
   >Si la oferta necesita instrucciones sobre cómo procesarse, puede suponer que debe enviar comentarios como eventos de experiencia.

### Eventos personalizados

Los comentarios sobre los eventos personalizados vinculados a una oferta se pueden enviar a Adobe Experience Platform según sus propias preferencias. Por ejemplo, si una oferta tiene varios botones como *Interesado*, *No me interesa*, etc., es posible que desee enviar esos eventos por separado, pero también se pueden enviar como eventos de experiencia. <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## Envío de datos de comentarios

Para enviar datos de comentarios, debe crear un conjunto de datos para recopilar eventos y, para cada tipo de evento, definir un evento de experiencia que se enviará a Adobe Experience Platform.

* Obtenga información sobre cómo crear un conjunto de datos en el que se recopilarán los eventos de experiencia [esta sección](create-dataset.md).

* Aprenda a definir eventos de experiencia para enviar datos de comentarios en [esta sección](schema-requirement.md).

