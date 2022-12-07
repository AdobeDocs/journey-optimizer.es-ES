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
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 40%

---


# Introducción a [!DNL Journey Optimizer] configuración {#start-optimizer-configuration}

Al acceder a [!DNL Journey Optimizer] por primera vez, se le aprovisiona una zona protegida de producción y se le asigna un determinado número de direcciones IP en función de su contrato.

Para poder crear sus recorridos y enviar mensajes, debe seguir los pasos de configuración a continuación.

## Configuración de mensajes y canales

Defina las superficies del canal, adapte y personalice los mensajes.

* [Delegar para almacenar en Adobe los subdominios](about-subdomain-delegation.md) desea utilizar para enviar correos electrónicos y [crear grupos de IP](ip-pools.md) para agrupar las direcciones IP aprovisionadas con su instancia.

* Administre el número de días durante los cuales se realizan reintentos antes de enviar direcciones de correo electrónico a la lista de supresión. [Más información](manage-suppression-list.md)

* Defina la configuración de notificaciones push en [!DNL Adobe Experience Platform] y [!DNL Adobe Experience Platform Launch]. [Más información](../push/push-gs.md)

   <!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

* Configure su instancia para que envíe SMS (actualmente solo disponible para un conjunto de organizaciones - Disponibilidad limitada). [Más información](../sms/sms-configuration.md)

* Cree superficies de canal para configurar todos los parámetros técnicos necesarios para enviar mensajes. [Más información](channel-surfaces.md)

* Determine la dirección de correo electrónico o el número de teléfono que se utilizarán con prioridad para los destinatarios cuando haya varias direcciones o números disponibles en Adobe Experience Platform. [Más información](primary-email-addresses.md)

## Configurar recorridos

Para crear recorridos, debe configurar **[!UICONTROL Fuentes de datos]**, **[!UICONTROL Eventos]** y **[!UICONTROL Acciones]**. [Más información](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* La variable **fuente de datos** permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos. [Más información](../datasource/about-data-sources.md)

* Los **Eventos** le permiten activar sus recorridos de forma unitaria para enviar mensajes, en tiempo real, a la persona que entra en el recorrido. En la configuración de eventos, se configuran los eventos esperados en los recorridos. Los datos entrantes de los eventos se normalizan siguiendo el modelo de datos de Experience de Adobe (XDM). Los eventos provienen de las API de ingesta de transmisión para eventos autenticados y no autenticados (como eventos del SDK de Adobe Mobile). [Más información](../event/about-events.md)

* [!DNL Journey Optimizer] incorpora funciones de mensajes que le permiten diseñar y enviar contenido. Si utiliza un sistema de terceros para enviar mensajes, cree un **acción personalizada**. [Más información](../action/action.md)