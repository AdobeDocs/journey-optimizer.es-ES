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
source-git-commit: 6da1d9a3edb8a30b8f13fd0cb6a138f22459ad00
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 54%

---


# Introducción a la configuración de canales {#start-optimizer-configuration}

Al acceder a [!DNL Journey Optimizer] por primera vez, se le aprovisiona una zona protegida de producción y se le asigna un determinado número de direcciones IP en función de su contrato.


Para poder enviar mensajes, debe seguir los pasos de configuración que se enumeran a continuación:

1. Como [administrador del sistema de Adobe Journey Optimizer](../start/path/administrator.md), defina las configuraciones de canal. Obtenga información sobre cómo configurar estas configuraciones en las siguientes páginas:

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/get-started-email-config.md"><img alt="Correo electrónico" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/get-started-email-config.md"><strong>Correo electrónico</strong></a></div></td>
<td><a href="../sms/sms-configuration.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/sms-configuration.md"><strong>SMS</strong></a></div></td>
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

>[!NOTE]
>
>En el caso de los canales móviles, la [configuración guiada de canales](set-mobile-config.md) facilita la configuración rápida de los canales de marketing, lo que garantiza que todos los recursos necesarios estén disponibles en Experience Platform, Journey Optimizer y la recopilación de datos. Esto permite a su equipo de marketing iniciar la creación de campañas y recorridos.

1. Una vez finalizado, debe crear **configuraciones de canal** para configurar todos los parámetros técnicos necesarios para enviar mensajes. [Más información acerca de las configuraciones de canal](channel-surfaces.md)

1. También puede:

   * Administre el número de días durante los cuales se realizan reintentos antes de enviar direcciones de correo electrónico a la lista de supresión. [Más información](manage-suppression-list.md)

   * Active la **Opción de correo electrónico de BBC** para mantener una copia de los mensajes enviados a personas. [Más información](archiving-support.md#enable-bcc)

   * Configure **reglas comerciales** para evitar saturar a los destinatarios. [Más información](../conflict-prioritization/rule-sets.md)

   * Determine la dirección de correo electrónico o el número de teléfono que se utilizará con prioridad para los destinatarios cuando haya varias direcciones o números disponibles en Adobe Experience Platform. [Más información](primary-email-addresses.md)
