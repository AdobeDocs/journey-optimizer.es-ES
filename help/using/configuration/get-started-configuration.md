---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a la configuración de  [!DNL Journey Optimizer] canales
description: Más información sobre la configuración de  [!DNL Journey Optimizer] canales
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: configuración, configurar, mensajes, canal, zona protegida, optimizador
TQID: https://experienceleague.adobe.com/zHp3C6KVKfRsQbi4B710ACFuMQhGuVxjaNIrXkxwhMc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c343082f-e963-4f57-a96b-b64d27f8118e
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
  - id: efb19423-4da4-4fd1-88d8-5ee8c71ae766
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 497
ht-degree: 30%

---

# Introducción a la configuración de canales {#start-optimizer-configuration}

>[!BEGINSHADEBOX]

**En esta página:** Descubra los pasos para configurar sus canales, subdominios, preparación de IP y reglas comerciales para que pueda empezar a enviar mensajes en Adobe Journey Optimizer.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_channels_rate_controls"
>title="Controles de velocidad para canales"
>abstract="Controles de velocidad para canales"

Al acceder a [!DNL Journey Optimizer] por primera vez, se le aprovisiona una zona protegida de producción y se le asigna un determinado número de direcciones IP en función de su contrato.

Para poder enviar mensajes, debe seguir los pasos de configuración que se enumeran a continuación:

1. Como [administrador del sistema de Adobe Journey Optimizer](../start/path/administrator.md), defina las configuraciones específicas del canal. Obtenga información sobre cómo configurar estas configuraciones en las siguientes páginas:

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../email/get-started-email-config.md"><img alt="Correo electrónico" src="../channels/assets/do-not-localize/email.png"></a>
    <div align="center"><a href="../email/get-started-email-config.md"><strong>Correo electrónico</strong></a></div></td>
    <td><a href="../mobile/mobile-configuration.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
    <div align="center"><a href="../mobile/mobile-configuration.md"><strong>SMS</strong></a></div></td>
    <td><a href="../push/push-configuration.md"><img alt="push" src="../channels/assets/do-not-localize/push.png"></a>
    <div align="center"><a href="../push/push-configuration.md"><strong>Notificación push</strong></a></div></td>
    <td><a href="../direct-mail/direct-mail-configuration.md"><img alt="Correo directo" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
    <div align="center"><a href="../direct-mail/direct-mail-configuration.md"><strong>Correo directo</strong></a></div></td>
    </tr></table>

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../in-app/inapp-configuration.md"><img alt="En la aplicación" src="../channels/assets/do-not-localize/inapp.jpg"></a>
    <div align="center"><a href="../in-app/inapp-configuration.md"><strong>En la aplicación</strong></a></div></td>
    <td><a href="../web/web-configuration.md"><img alt="Web" src="../channels/assets/do-not-localize/web.jpg"></a>
    <div align="center"><a href="../web/web-configuration.md"><strong>Web</strong></a></div></td>
    <td><a href="../code-based/code-based-configuration.md"><img alt="Experiencia basada en código" src="../channels/assets/do-not-localize/code.png"></a>
    <div align="center"><a href="../code-based/code-based-configuration.md"><strong>Experiencia basada en código</strong></a></div></td>
    <td><a href="../content-card/content-card-configuration-prereq.md"><img alt="Tarjetas de contenido" src="../channels/assets/do-not-localize/cards.png"></a>
    <div align="center"><a href="../content-card/content-card-configuration-prereq.md"><strong>Tarjetas de contenido</strong></a></div></td>
    </tr></table>

   Para ver canales adicionales, consulta: [Actividades de iOS Live](../mobile-live/mobile-live-configuration.md), [WhatsApp](../whatsapp/whatsapp-configuration.md) y [LINE](../line/line-configuration.md).

   >[!NOTE]
   >
   >En el caso de los canales móviles, la [configuración guiada de canales](set-mobile-config.md) facilita la configuración rápida de los canales de marketing, lo que garantiza que todos los recursos necesarios estén disponibles en Experience Platform, Journey Optimizer y la recopilación de datos. Esto permite a su equipo de marketing iniciar la creación de campañas y recorridos.

1. Una vez finalizado, debe configurar todos los parámetros técnicos necesarios para enviar mensajes creando **configuraciones de canal**. [Más información acerca de las configuraciones de canal](channel-surfaces.md)

1. Según los canales que utilice, los entornos y las necesidades, también debe realizar los siguientes pasos:

   * Configuración y delegación de subdominios para sus canales, como [correos electrónicos](about-subdomain-delegation.md), [SMS](../mobile/mobile-subdomains.md), [páginas de aterrizaje](../landing-pages/lp-subdomains.md) y [experiencias web](../web/web-delegated-subdomains.md).

   * Configure planes de calentamiento de IP para una entrega óptima. [Más información](ip-warmup-gs.md)

   * Defina una lista de permitidos para el envío de correo electrónico. [Más información](allow-list.md)

   * Administre el número de días durante los cuales se realizan reintentos antes de enviar direcciones de correo electrónico a la lista de supresión. [Más información](manage-suppression-list.md)

   * Habilite la opción de correo electrónico **CCO** para conservar una copia de los mensajes enviados a las personas. [Más información](archiving-support.md#enable-bcc)

   * Configure **reglas comerciales** para evitar saturar a los destinatarios. [Más información](../conflict-prioritization/rule-sets.md)

   * Determine la dirección de correo electrónico o el número de teléfono que se utilizará con prioridad para los destinatarios cuando haya varias direcciones o números disponibles en Adobe Experience Platform. [Más información](primary-email-addresses.md)

## Recursos adicionales

* **[Configurar superficies de canal](channel-surfaces.md)**: aprenda a configurar y administrar superficies de canal para correo electrónico, push, SMS y otros canales.
* **[Delegación de subdominios](delegate-subdomain.md)**: aprenda a delegar subdominios a Adobe para la entrega de correo electrónico y la promoción de la marca.
* **[Calentamiento de IP](ip-warmup-gs.md)**: descubra las prácticas recomendadas para el Calentamiento de direcciones IP a fin de mejorar la capacidad de envío de correo electrónico y la reputación del remitente.
* **[Administrar lista de supresión](manage-suppression-list.md)**: aprenda a administrar listas de supresión para gestionar devoluciones y mantener la higiene de las listas.
* **[Configurar aplicaciones móviles](set-mobile-config.md)** - Configurar configuraciones de aplicaciones móviles para notificaciones push y mensajería en la aplicación.
* **[Configurar actividades de iOS Live](../mobile-live/mobile-live-configuration.md)**: configura tu entorno para enviar actividades en directo a la pantalla de bloqueo de iPhone y a Dynamic Island.
* **[Configuración de WhatsApp](../whatsapp/whatsapp-configuration.md)**: configura la mensajería de WhatsApp a través de la API de nube de Meta para campañas y recorridos.
* **[Configuración de LINE](../line/line-configuration.md)**: configure la mensajería LINE para campañas y recorridos.
* **[Tutoriales de configuración](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/configure-channels){target="_blank"}**: explora tutoriales de vídeo paso a paso sobre la configuración del canal y las prácticas recomendadas.
