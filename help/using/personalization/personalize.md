---
title: Personalización del contenido en Journey Optimizer
description: Introducción a la personalización
feature: Personalización
topic: Personalización
role: Data Engineer
level: Beginner
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 52%

---

# Introducción a la personalización{#add-personalization}

![](../assets/do-not-localize/badge.png)

Descubra las funcionalidades de personalización de Recorrido Optimier para adaptar sus mensajes a cada destinatario específico aprovechando los datos y la información que tiene sobre él. Puede ser su nombre, sus intereses, dónde vive, qué compró, etc.

Journey Optimizer utiliza una sintaxis de personalización **en línea** sencilla basada en Handlebars, que le permite crear expresiones con contenido entre llaves dobles **{{}}**. Puede añadir varias expresiones en el mismo contenido o campo sin restricciones. Obtenga más información en [Sintaxis de personalización](personalization-syntax.md).

La personalización se basa en los datos de perfil que administra el esquema **Perfil individual de XDM** definido en Adobe Experience Platform. Para obtener más información, consulte la [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es).

>[!CAUTION]
>El esquema **XDM Individual Profile** es el único esquema que puede utilizar para personalizar el contenido en Journey Optimizer.

**Ejemplos:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

Al procesar el mensaje (correo electrónico y push), Journey Optimizer reemplaza la expresión por los datos contenidos en la base de datos de Experience Cloud Platform.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
