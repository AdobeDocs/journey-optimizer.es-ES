---
title: Personalización del contenido en Journey Optimizer
description: Introducción a la personalización.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: fab36ea43e92babfacdbaeeaecf6c551c00b3c5b
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 34%

---

# Introducción a la personalización{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] funcionalidades de personalización para adaptar los mensajes a cada destinatario específico aprovechando los datos y la información que tiene sobre ellos. Puede ser su nombre, intereses, dónde viven, qué compraron, etc.

➡️ [Aprenda a personalizar un mensaje en estos vídeos](#video-perso)
➡️ [Descubra casos de uso que aprovechen la personalización](personalization-use-case.md)

## Creación de expresiones de personalización mediante una sintaxis dedicada {#syntax}

[!DNL Journey Optimizer] utiliza una sintaxis de personalización **en línea** sencilla basada en Handlebars, que le permite crear expresiones con contenido entre llaves dobles **{{}}**. Puede añadir varias expresiones en el mismo contenido o campo sin restricciones. Obtenga más información en [Sintaxis de personalización](personalization-syntax.md).

**Ejemplos:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Al procesar el mensaje (correo electrónico y push), Journey Optimizer reemplaza la expresión por los datos contenidos en la base de datos de Experience Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` se convierte en &quot;Hello John Doe&quot;.

## Aproveche los datos de perfil para personalizar sus mensajes {#data}

La personalización se basa en los datos de perfil que administra el esquema **Perfil individual de XDM** definido en Adobe Experience Platform. Obtenga más información en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target=&quot;_blank&quot;}.

>[!CAUTION]
>La variable **Perfil individual XDM** schema es el único esquema que puede utilizar para personalizar el contenido en [!DNL Journey Optimizer].

## Añadir personalización en diferentes contextos {#contexts}

[!DNL Journey Optimizer] le permite personalizar el contenido y la visualización de los mensajes de varias formas diferentes. Obtenga más información sobre los contextos en los que puede realizar personalizaciones en [esta sección](personalization-contexts.md).

## Trabajar con el editor de expresiones {#editor}

[!DNL Journey Optimizer] proporciona un editor de expresiones donde se seleccionan, organizan, personalizan y validan todos los datos para crear una personalización personalizada para el contenido.

Hay varias herramientas disponibles para ayudar a crear su contenido de personalización (funciones de ayuda, biblioteca de expresiones predefinidas, atributos favoritos...).

Más información sobre [!DNL Journey Optimizer] editor de expresiones en [esta sección](personalization-build-expressions.md)

## Vídeotutoriales{#video-perso}

Aprenda a utilizar la información de evento contextual de un recorrido para personalizar un mensaje.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Aprenda a utilizar la información de evento contextual de un recorrido para personalizar un mensaje.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
