---
solution: Journey Optimizer
product: journey optimizer
title: Personalización del contenido en Journey Optimizer
description: Introducción a la personalización.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: expresión, editor, inicio, personalización
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 35%

---

# Introducción a la personalización{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Personalización de experiencias"
>abstract="Utilice **Adobe Journey Optimizer** para adaptar los mensajes a cada destinatario específico aprovechando los datos y la información que tiene sobre ellos. Pueden ser sus nombres, intereses, dónde viven, qué compraron, etc."

Descubra las funcionalidades de personalización de [!DNL Adobe Journey Optimizer] para adaptar los mensajes a cada destinatario específico aprovechando los datos y la información que tiene sobre ellos. Pueden ser sus nombres, intereses, dónde viven, qué compraron, etc.

➡️ [Aprenda a personalizar un mensaje en estos vídeos](#video-perso)
➡️ [Descubra casos de uso aprovechando la personalización](personalization-use-case.md)

## Crear expresiones de personalización mediante una sintaxis dedicada {#syntax}

[!DNL Journey Optimizer] usa una sintaxis de personalización simple **inline** basada en Handlebars, que le permite crear expresiones con contenido entre llaves dobles **{{}}**. Puede añadir varias expresiones en el mismo contenido o campo sin restricciones. [Más información sobre la sintaxis de personalización](personalization-syntax.md).

**Ejemplos:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Al procesar el mensaje (correo electrónico y push), Journey Optimizer reemplaza la expresión por los datos contenidos en la base de datos del Experience Platform: `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` se convierte en &quot;Hello John Doe&quot;.

## Aprovechamiento de los datos de perfil para personalizar los mensajes {#data}

La personalización se basa en los datos de perfil que administra el esquema **Perfil individual de XDM** definido en Adobe Experience Platform. Obtenga más información en la [documentación del modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

>[!CAUTION]
>El esquema **XDM Individual Profile** es el único esquema que puede usar para personalizar el contenido en [!DNL Journey Optimizer].

Además, también puede aprovechar **atributos calculados** para personalizar el contenido. Los atributos calculados se basan en conjuntos de datos de eventos de experiencia habilitados para perfiles introducidos en Adobe Experience Platform y sirven como puntos de datos agregados almacenados en perfiles de clientes que resumen eventos de comportamiento individuales [Aprenda a trabajar con atributos calculados](../audience/computed-attributes.md)

## Trabajo con el editor de personalización {#editor}

[!DNL Journey Optimizer] proporciona un editor de personalización donde podrá seleccionar, organizar, personalizar y validar todos los datos para crear una personalización personalizada para su contenido. Hay varias herramientas disponibles para ayudarle a crear su contenido de personalización, como funciones de felper, biblioteca de expresiones predefinidas, atributos, marcar como favoritos y más.

* [Aprenda a trabajar con el editor de personalización](personalization-build-expressions.md)
* [Descubra dónde puede realizar la personalización](personalization-contexts.md).

## Vídeotutoriales{#video-perso}

Aprenda a utilizar la información de evento contextual de un recorrido para personalizar un mensaje.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Obtenga información sobre cómo añadir una personalización basada en perfiles a un mensaje y cómo utilizar el abono a un público como condición previa a un bloque de personalización.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

