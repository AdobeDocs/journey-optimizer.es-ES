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
source-git-commit: 5ac3797db8115180094cc97f06ec330839a7a5ff
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 41%

---

# Introducción a la personalización{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Personalización de experiencias"
>abstract="Utilice **Adobe Journey Optimizer** para adaptar los mensajes a cada destinatario específico aprovechando los datos y la información que tiene sobre ellos. Pueden ser sus nombres, intereses, dónde viven, qué compraron, etc."


Discover [!DNL Adobe Journey Optimizer] funcionalidades de personalización para adaptar los mensajes a cada destinatario específico aprovechando los datos y la información que tiene sobre ellos. Pueden ser sus nombres, intereses, dónde viven, qué compraron, etc.

➡️ [Aprenda a personalizar un mensaje en estos vídeos](#video-perso)
➡️ [Descubra casos de uso aprovechando la personalización](personalization-use-case.md)

## Crear expresiones de personalización mediante una sintaxis dedicada {#syntax}

[!DNL Journey Optimizer] utiliza una sintaxis de personalización **en línea** sencilla basada en Handlebars, que le permite crear expresiones con contenido entre llaves dobles **{{}}**. Puede añadir varias expresiones en el mismo contenido o campo sin restricciones. Obtenga más información en [Sintaxis de personalización](personalization-syntax.md).

**Ejemplos:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Al procesar el mensaje (correo electrónico y push), Journey Optimizer reemplaza la expresión con los datos contenidos en la base de datos del Experience Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` se convierte en &quot;Hola John Doe&quot;.

## Aprovechamiento de los datos de perfil para personalizar los mensajes {#data}

La personalización se basa en los datos de perfil que administra el esquema **Perfil individual de XDM** definido en Adobe Experience Platform. Obtenga más información en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

>[!CAUTION]
>El **Perfil individual de XDM** schema es el único esquema que puede utilizar para personalizar el contenido en [!DNL Journey Optimizer].

Además, también puede aprovechar **atributos calculados** para personalizar el contenido. Los atributos calculados se basan en conjuntos de datos de eventos de experiencia habilitados para perfiles introducidos en Adobe Experience Platform y sirven como puntos de datos agregados almacenados en perfiles de clientes que resumen eventos de comportamiento individuales [Aprenda a trabajar con atributos calculados](../audience/computed-attributes.md)

## Añadir personalización en diferentes contextos {#contexts}

[!DNL Journey Optimizer] permite personalizar el contenido y la visualización de los mensajes de varias formas diferentes. Obtenga más información acerca de los contextos en los que puede realizar personalizaciones en [esta sección](personalization-contexts.md).

## Trabajo con el editor de expresiones {#editor}

[!DNL Journey Optimizer] proporciona un editor de expresiones en el que puede seleccionar, organizar, personalizar y validar todos los datos para crear una personalización personalizada para el contenido.

Hay varias herramientas disponibles para crear el contenido de personalización (funciones de ayuda, biblioteca de expresiones predefinidas, atributos, marcar como favorito...)

Más información sobre [!DNL Journey Optimizer] editor de expresiones en [esta sección](personalization-build-expressions.md)

## Vídeotutoriales{#video-perso}

Aprenda a utilizar la información de evento contextual de un recorrido para personalizar un mensaje.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Obtenga información sobre cómo añadir una personalización basada en perfiles a un mensaje y cómo utilizar el abono a un público como condición previa a un bloque de personalización.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

