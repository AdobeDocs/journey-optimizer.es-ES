---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a [!DNL Journey Optimizer] configuración
description: Más información sobre [!DNL Journey Optimizer] configuración
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 34%

---


# Introducción a [!DNL Journey Optimizer] configuración {#start-optimizer-configuration}

Al acceder a [!DNL Journey Optimizer] por primera vez, se le aprovisiona una zona protegida de producción y se le asigna un determinado número de direcciones IP en función de su contrato.

Para poder crear sus recorridos y enviar mensajes, debe seguir los pasos de configuración a continuación.

## Configuración de mensajes y canales

1. Para poder crear y enviar mensajes, debe realizar configuraciones específicas según el canal.

   * Para la variable **Correo electrónico** canal, es necesario delegar subdominios al Adobe y crear grupos de IP para agrupar direcciones IP. [Más información](../email/get-started-email-config.md)

   * Para la variable **Push** canal, debe definir la configuración de las notificaciones push en ambas [!DNL Adobe Experience Platform] y [!DNL Adobe Experience Platform Launch]. [Más información](../push/push-configuration.md)

   * Para la variable **SMS** canal, debe configurar la instancia para enviar SMS, incluida la integración de la configuración del proveedor con [!DNL Journey Optimizer]. [Más información](../sms/sms-configuration.md)

1. Una vez finalizado, debe crear **superficies de canal** para configurar todos los parámetros técnicos necesarios para enviar mensajes. [Más información](channel-surfaces.md)

1. También puede:

   * Administre el número de días durante los cuales se realizan reintentos antes de enviar direcciones de correo electrónico a la lista de supresión. [Más información](manage-suppression-list.md)

   * Active la variable **Opción de correo electrónico de BBC** para mantener una copia de los mensajes enviados a personas. [Más información](archiving-support.md#enable-bcc)

   * Configurar **reglas de frecuencia** para evitar saturar a los destinatarios. [Más información](frequency-rules.md)

   * Determine la dirección de correo electrónico o el número de teléfono que se utilizarán con prioridad para los destinatarios cuando haya varias direcciones o números disponibles en Adobe Experience Platform. [Más información](primary-email-addresses.md)

<!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

>[!NOTE]
>
>Estos pasos debe realizarlos un [Administrador del sistema de Adobe Journey Optimizer](../start/path/administrator.md).

## Configurar recorridos

Para crear recorridos, debe configurar **[!UICONTROL Fuentes de datos]**, **[!UICONTROL Eventos]** y **[!UICONTROL Acciones]**. [Más información](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* La variable **fuente de datos** permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos. [Más información](../datasource/about-data-sources.md)

* Los **Eventos** le permiten activar sus recorridos de forma unitaria para enviar mensajes, en tiempo real, a la persona que entra en el recorrido. En la configuración de eventos, se configuran los eventos esperados en los recorridos. Los datos entrantes de los eventos se normalizan siguiendo el modelo de datos de Experience de Adobe (XDM). Los eventos provienen de las API de ingesta de transmisión para eventos autenticados y no autenticados (como eventos del SDK de Adobe Mobile). [Más información](../event/about-events.md)

* [!DNL Journey Optimizer] incorpora funciones de mensajes que le permiten diseñar y enviar contenido. Si utiliza un sistema de terceros para enviar mensajes, cree un **acción personalizada**. [Más información](../action/action.md)