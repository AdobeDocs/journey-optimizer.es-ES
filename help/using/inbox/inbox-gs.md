---
title: Crear una bandeja de entrada
description: Empiece a utilizar la bandeja de entrada en Adobe Journey Optimizer para enviar mensajes persistentes y no intrusivos a los usuarios.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
source-git-commit: 337b8ed47892ef06a84884468919e32a333653f3
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Introducción a la bandeja de entrada {#inbox-gs}

La bandeja de entrada envía mensajes persistentes y de baja fricción en un solo lugar de la aplicación móvil o del sitio web. Las notificaciones push y en la aplicación pueden desaparecer después de un toque o un barrido; la bandeja de entrada mantiene los mensajes disponibles para que las personas puedan abrirlos, leerlos y actuar en consecuencia cuando les convenga.

La bandeja de entrada se basa en el canal de tarjetas de contenido y añade:

* **Mensajería persistente**: El contenido permanece en la bandeja de entrada hasta que lo elimine o hasta que caduque, de modo que los usuarios puedan volver a ella después de cerrar una notificación o salir de la aplicación.
* **Ubicación centralizada**: Un solo buzón en su aplicación o sitio para mensajes de marketing relevantes.
* **Implementación flexible**: use el contenedor de bandeja de entrada listo para usar o adapte la experiencia en su propia interfaz de usuario.
* **Sincronización entre dispositivos**: el estado de lectura y la participación permanecen alineados entre los dispositivos del usuario.

## Guía de inicio rápido

Siga estos pasos para configurar y utilizar la bandeja de entrada:

1. [Configuración de Adobe Journey Optimizer](inbox-configuration.md)

   Agregue una configuración de canal **Bandeja de entrada** en **Configuraciones de canal** para que Journey Optimizer sepa dónde y cómo se ejecuta la bandeja de entrada (página web, regla o superficie de aplicación móvil).

1. [Cree su bandeja de entrada en Journey Optimizer](inbox-create.md)

   Cree una campaña que use la acción **Tarjeta de contenido** y elija **Bandeja de entrada** como ubicación de entrega (programada desde la interfaz de usuario o desencadenada por la API).

1. [Diseño de la bandeja de entrada](inbox-design.md)

   Elija plantillas de bandeja de entrada y diseños de lista o expandidos para que los mensajes coincidan con su marca y experiencia de usuario.

1. [Cree la tarjeta de contenido y vincúlela a la bandeja de entrada](../content-card/create-content-card.md)

   Cree el contenido de la tarjeta en el diseñador, finalice las opciones específicas de la bandeja de entrada y, a continuación, active la campaña para que los mensajes lleguen a la bandeja de entrada.

## Recursos adicionales

* [Recuperar y mostrar bandeja de entrada](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox/): cargue mensajes de la bandeja de entrada Journey Optimizer y procese la interfaz de usuario de la bandeja de entrada en Android (documentación de Adobe Developer).
* [Personalización de la bandeja de entrada](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox/): ajuste el diseño, el estilo y el comportamiento de interacción de la bandeja de entrada para su aplicación de Android (documentación de Adobe Developer).
* [Escucha de eventos en la bandeja de entrada](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events/): suscríbete a las devoluciones de llamadas de la bandeja de entrada para acciones de usuarios y actualizaciones del ciclo vital en Android (documentación de Adobe Developer).
