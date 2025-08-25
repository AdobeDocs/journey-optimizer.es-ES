---
title: Recopilación de datos
description: Obtenga más información acerca de la recopilación de datos de comentarios de Administración de decisiones
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer, Developer
level: Experienced
hide: true
hidefromtoc: true
exl-id: 32e3a5b9-0633-48df-95b5-c03536be23a1
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 1%

---

# Recopilación de datos de gestión de decisiones {#data-collection}

## Explicación de la recopilación de datos

Puede recopilar comentarios de Offer Decisioning en Adobe Experience Platform, incluidas las ofertas que se muestran y la forma en que los usuarios interactúan con ellas. Estos datos se pueden utilizar para lo siguiente:

* Escribiendo [informes de toma de decisiones](../cja-reporting.md);
* Usar [límite](../items.md#capping) reglas;
* Generando [modelos de IA](../ranking/ai-models.md) que puedan usarse como método de clasificación.

## Tipos de eventos

La forma en que se recopilan los datos varía según el tipo de evento que desee capturar.

### Eventos de decisión

Cada vez que Decisioning toma una decisión, la información relacionada con ese evento de decisión se **envía automáticamente** a Adobe Experience Platform. <!--TBC + link-->

### Eventos de impresión y clics

Las impresiones y clics de gestión de decisiones se definen de la siguiente manera:

* Un evento **impression** se produce cuando se muestra una oferta a un usuario.

* Un evento **click** se produce cuando un usuario hace clic o interactúa con una oferta.

Los comentarios sobre las impresiones y los clics se capturan según el canal [!DNL Journey Optimizer] que se use.

**Correos electrónicos** creados por [!DNL Journey Optimizer] **rastrean automáticamente** impresiones y clics.

Sin embargo, **la mayoría de los canales** requieren que los datos de impresiones y clics se envíen a Adobe Experience Platform como un **evento de experiencia**. Esto incluye lo siguiente:

* Páginas web que usan [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"} para procesar ofertas

* Aplicaciones móviles que usan [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} para procesar ofertas: [Más información](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* Quioscos
* Mensajes enviados a través de aplicaciones de terceros
  <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>Los canales que utilizan una solicitud de API de decisiones para recibir ofertas necesitan que se envíen comentarios como un evento de experiencia. En otras palabras, si la oferta necesita instrucciones sobre cómo procesarse, puede suponer que debe enviar comentarios como eventos de experiencia.

### Eventos personalizados

Los comentarios sobre los eventos personalizados vinculados a una oferta se pueden enviar a Adobe Experience Platform según sus propias preferencias. Por ejemplo, si una oferta tiene varios botones como *Interesado*, *No interesado*, etc., quizá quiera enviar esos eventos por separado, pero también se pueden enviar como eventos de experiencia.

## Envío de datos de comentarios

Para enviar datos de comentarios, debe crear un conjunto de datos para recopilar eventos y, para cada tipo de evento, definir un evento de experiencia que se enviará a Adobe Experience Platform.

* Aprenda a crear un conjunto de datos donde se recopilarán los eventos de experiencia en [esta sección](create-dataset.md).

* Aprenda a definir eventos de experiencia para enviar datos de comentarios en [esta sección](schema-requirement.md).
