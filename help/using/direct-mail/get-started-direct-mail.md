---
solution: Journey Optimizer
product: journey optimizer
title: Introducción al correo directo
description: Obtenga información sobre cómo crear y enviar un mensaje de correo directo en Journey Optimizer
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: correo directo, mensaje, campaña
exl-id: bb52f400-6289-4a7f-a34f-98eb5d27c76a
TQID: https://experienceleague.adobe.com/Gmtr-7HW70-cg7va8iHfR5xKdYts-ZdDCm6CeQHJ0tg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: cb1f1586-9fb4-4de2-8332-02cebb88d42d
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: e7702a4706509a8181ee39cccc510656c5230a16
workflow-type: tm+mt
source-wordcount: 487
ht-degree: 74%

---

# Introducción al correo directo {#create-direct}

>[!BEGINSHADEBOX]

**En esta página:** Comprenda cómo funciona el canal de correo postal para que pueda generar los archivos de extracción que los proveedores de terceros utilizan para enviar correo físico a sus clientes.

>[!ENDSHADEBOX]

El correo directo es un canal sin conexión que le permite personalizar y generar los archivos de extracción necesarios para que los proveedores de correo postal de terceros envíen correo a sus clientes.

Al crear un recorrido o una campaña de correo directo, Journey Optimizer genera automáticamente un archivo que contiene todos los perfiles de destino y los datos seleccionados, como las direcciones postales y los atributos de perfil. Este archivo se envía al servidor de su elección para que el proveedor de correo directo de terceros elegido pueda acceder a él, quien se encargará del proceso de envío.

Deberá trabajar con el proveedor de correo directo de terceros que haya elegido para obtener el consentimiento necesario de sus clientes, si corresponde, para que estos puedan recibir correo de usted.

El uso de los servicios de correo está sujeto a términos y condiciones adicionales del proveedor de correo directo de terceros correspondiente.  Adobe no controla ni es responsable del uso que se haga de los productos de terceros. Para cualquier problema o solicitud de asistencia relacionada con el envío de correo de su campaña de correo directo, póngase en contacto con el proveedor de correo directo de terceros que haya elegido.

## Antes de comenzar {#before-you-start}

Antes de crear mensajes de correo postal, configure [enrutamiento de archivos y una configuración de canal de correo postal](direct-mail-configuration.md). También necesita audiencias y datos de perfil (como direcciones postales) en Adobe Experience Platform.

Los pasos principales para enviar mensajes de correo directo son los siguientes:

![Flujo de trabajo de creación de correo directo desde la configuración hasta la entrega](assets/dm-creation-process.png)

>[!AVAILABILITY]
>
>Los mensajes de correo directo solo se pueden crear en el contexto de recorridos y campañas. No están disponibles para su uso en campañas activadas por API.

![Descripción general animada del canal de correo postal en Journey Optimizer](../rn/assets/do-not-localize/gif-dm.gif)

## Recursos adicionales {#additional-resources}

* **[Cree correo postal](create-direct-mail.md)**: aprenda a crear envíos de correo postal y a configurar archivos de extracción para canales sin conexión.
* **[Configure el canal de correo postal](direct-mail-configuration.md)**: configure las superficies de correo postal y las configuraciones de enrutamiento de archivos.
* **[Toma de decisiones por lotes en el correo postal](../experience-decisioning/batch-decisioning-direct-mail.md)**: use la toma de decisiones para personalizar los archivos de extracción para el correo postal o para exportar los datos de toma de decisiones para los sistemas descendentes.
* **[Pruebe y envíe correo postal](test-send-direct-mail.md)**: aprenda a probar, validar y publicar sus envíos de correo postal.
* **[Tutoriales de correo postal](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/channels/direct-mail-channel/direct-mail){target="_blank"}**: explore tutoriales de vídeo paso a paso sobre las características del correo directo y las prácticas recomendadas.

## Vídeo tutorial {#how-to-video}

Aprenda cómo aprovechar el canal de correo directo en Adobe Journey Optimizer para automatizar y programar envíos de correo directo en sus recorridos.

+++ Vea el vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3479165?captions=spa&quality=12)

+++

Para ver un tutorial escrito de los mismos pasos, vea los [tutoriales del canal de correo postal](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/channels/direct-mail-channel/direct-mail){target="_blank"}.

Si tiene preguntas comunes acerca del correo postal, consulte la sección [Recursos adicionales](#additional-resources) más arriba.
