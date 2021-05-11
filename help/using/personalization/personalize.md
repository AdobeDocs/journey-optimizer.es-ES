---
title: Personalización del contenido en Journey Optimizer
description: Introducción a la personalización
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 5%

---

# Introducción {#add-personalization}

![](../assets/do-not-localize/badge.png)

La personalización, en el contexto de Journey Optimizer, es la acción de dirigir un mensaje a un suscriptor específico aprovechando los datos y la información que tiene sobre él. Puede ser su nombre, sus intereses, dónde vive, y más.

Journey Optimizer utiliza una **sintaxis de personalización en línea** sencilla basada en Handlebars, que le permite crear expresiones con contenido entre llaves dobles **{}}**. Puede añadir varias expresiones en el mismo contenido o campo sin restricciones. Consulte [Sintaxis de personalización](personalization-syntax.md).

La personalización se basa en los datos de perfil que administra el esquema **XDM Individual Profile** definido en Adobe Experience Platform. Para obtener más información, consulte la [documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es).

>[!CAUTION]
>El esquema **XDM Individual Profile** es el único que puede utilizar para personalizar el contenido en Journey Optimizer.

**Ejemplos:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

Durante el **procesamiento de mensajes** (correo electrónico y push), la expresión se reemplaza por los datos contenidos en las bases de datos de la plataforma de Experience Cloud.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
