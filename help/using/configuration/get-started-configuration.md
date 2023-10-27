---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a la configuración de  [!DNL Journey Optimizer]
description: Obtenga más información sobre la configuración de  [!DNL Journey Optimizer]
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: configuración, configurar, mensajes, canal, zona protegida, optimizador
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: ht
source-wordcount: '387'
ht-degree: 100%

---


# Introducción a la configuración de [!DNL Journey Optimizer] {#start-optimizer-configuration}

Al acceder a [!DNL Journey Optimizer] por primera vez, se le aprovisiona una zona protegida de producción y se le asigna un determinado número de direcciones IP en función de su contrato.

Para poder crear sus recorridos y enviar mensajes, debe seguir los pasos de configuración siguientes.

## Configuración de mensajes y canales

1. Para poder crear y enviar mensajes, debe realizar configuraciones específicas según el canal.

   * Para el canal **Correo electrónico**, es necesario delegar subdominios al Adobe y crear grupos de IP para agrupar direcciones IP. [Más información](../email/get-started-email-config.md)

   * Para el canal **Push**, debe definir la configuración de las notificaciones push en ambas [!DNL Adobe Experience Platform] y [!DNL Adobe Experience Platform Launch]. [Más información](../push/push-configuration.md)

   * Para el canal **SMS**, debe configurar la instancia para enviar SMS, incluida la integración de la configuración del proveedor con [!DNL Journey Optimizer]. [Más información](../sms/sms-configuration.md)

1. Cuando haya finalizado, deberá crear **superficies de canal** para configurar todos los parámetros técnicos necesarios para enviar mensajes. [Más información](channel-surfaces.md)

1. También puede:

   * Administre el número de días durante los cuales se realizan reintentos antes de enviar direcciones de correo electrónico a la lista de supresión. [Más información](manage-suppression-list.md)

   * Active la **Opción de correo electrónico de BBC** para mantener una copia de los mensajes enviados a personas. [Más información](archiving-support.md#enable-bcc)

   * Configure **reglas de frecuencia** para evitar saturar a los destinatarios. [Más información](frequency-rules.md)

   * Determine la dirección de correo electrónico o el número de teléfono que se utilizará con prioridad para los destinatarios cuando haya varias direcciones o números disponibles en Adobe Experience Platform. [Más información](primary-email-addresses.md)

<!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

>[!NOTE]
>
>Estos pasos debe realizarlos un [administrador del sistema de Adobe Journey Optimizer](../start/path/administrator.md).

## Configurar recorridos

Para enviar mensajes con recorridos, debe configurar **[!UICONTROL Fuentes de datos]**, **[!UICONTROL Eventos]** y **[!UICONTROL Acciones.]** [Más información](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* La configuración de la **fuente de datos** permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos. [Más información](../datasource/about-data-sources.md)

* Los **Eventos** le permiten activar sus recorridos de forma unitaria para enviar mensajes, en tiempo real, a la persona que entra en el recorrido. En la configuración de eventos, se configuran los eventos esperados en los recorridos. Los datos entrantes de los eventos se normalizan siguiendo el modelo de datos de Experience de Adobe (XDM). Los eventos provienen de las API de ingesta de transmisión para eventos autenticados y no autenticados (como eventos del SDK de Adobe Mobile). [Más información](../event/about-events.md)

* [!DNL Journey Optimizer] incorpora funcionalidades de mensajes que le permiten diseñar y enviar contenido. Si utiliza un sistema de terceros para enviar mensajes, como Adobe Campaign, cree una **acción personalizada**. [Más información](../action/action.md)