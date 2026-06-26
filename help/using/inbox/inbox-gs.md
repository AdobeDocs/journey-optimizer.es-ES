---
title: Crear una bandeja de entrada
description: Empiece a utilizar la bandeja de entrada en Adobe Journey Optimizer para enviar mensajes persistentes y no intrusivos a los usuarios.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 60190d0b-d8e7-4a78-9924-d948f2769f6c
source-git-commit: c2bb6cf702a14b4eef8f2209082e39cd73338378
workflow-type: ht
source-wordcount: '453'
ht-degree: 100%

---

# Introducción a la bandeja de entrada {#inbox-gs}

>[!BEGINSHADEBOX]

**En esta página:** comprenda cómo el canal de la bandeja de entrada mantiene los mensajes de marketing en un lugar persistente dentro de la aplicación o del sitio web, de modo que los usuarios puedan volver a leerlos y actuar en consecuencia según les convenga.

>[!ENDSHADEBOX]

La bandeja de entrada envía mensajes persistentes y de baja fricción en un solo lugar de la aplicación móvil o del sitio web. Las notificaciones push y en la aplicación pueden desaparecer después de un toque o un deslizamiento de la mano; la bandeja de entrada mantiene los mensajes disponibles para que las personas puedan abrirlos, leerlos y actuar en consecuencia cuando les convenga.

La bandeja de entrada se basa en el canal de tarjetas de contenido y añade:

* **Mensajería persistente**: el contenido permanece en la bandeja de entrada hasta que lo elimine o hasta que caduque, de modo que los usuarios puedan volver a él después de cerrar una notificación o salir de la aplicación.
* **Ubicación centralizada**: un solo buzón en su aplicación o sitio para los mensajes de marketing relevantes.
* **Implementación flexible**: utilice el contenedor de la bandeja de entrada ya preparado o adapte la experiencia en su propia interfaz de usuario.
* **Estado de lectura**: los mensajes se pueden marcar como leídos o no leídos en el dispositivo en el que están abiertos.

## Guía de inicio rápido

Siga estos pasos para configurar y utilizar la bandeja de entrada:

1. [Configurar Adobe Journey Optimizer](inbox-configuration.md)

   Añada una configuración de **Bandeja de entrada** en **Configuraciones de canal** para que Journey Optimizer sepa dónde y cómo se ejecuta la bandeja de entrada (página web, regla o superficie de aplicación móvil).

1. [Crear la bandeja de entrada en Journey Optimizer](inbox-create.md)

   Cree una campaña que utilice la acción **Tarjeta de contenido** y elija **Bandeja de entrada** como ubicación de entrega (programada desde la interfaz de usuario o desencadenada por la API).

1. [Diseño de la bandeja de entrada](inbox-design.md)

   Elija plantillas de bandeja de entrada y diseños de lista o expandidos para que los mensajes coincidan con su marca y experiencia de usuario.

1. [Crear la tarjeta de contenido y vincularla a la bandeja de entrada](../content-card/create-content-card.md)

   Cree el contenido de la tarjeta en el diseñador, finalice las opciones específicas de la bandeja de entrada y, a continuación, active la campaña para que los mensajes lleguen a la bandeja de entrada.

## Recursos adicionales

* [IU de la bandeja de entrada (iOS)](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/iOS): requisitos, superficie de API pública, configuración de la bandeja de entrada y vínculos a tutoriales para implementar la bandeja de entrada de Journey Optimizer en una aplicación de iOS con el SDK de Adobe Experience Platform Mobile (iOS 15 o posterior, Xcode 15 o posterior, Swift 5.1 o posterior).

* [Recuperar y mostrar la bandeja de entrada](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox): cargue los mensajes de la bandeja de entrada de Journey Optimizer y procese la interfaz de usuario de la bandeja de entrada en Android (documentación de Adobe Developer).

* [Personalización de la bandeja de entrada](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox): ajuste el diseño, el estilo y el comportamiento de interacción de la bandeja de entrada para su aplicación de Android (documentación de Adobe Developer).

* [Escucha de eventos de la bandeja de entrada](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events): suscríbase a las devoluciones de llamadas de la bandeja de entrada para acciones de usuarios y actualizaciones del ciclo de vida en Android (documentación de Adobe Developer).
