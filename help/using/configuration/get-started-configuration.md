---
title: Introducción a [!DNL Journey Optimizer] configuración
description: Más información sobre [!DNL Journey Optimizer] configuración
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 11%

---


# Introducción a [!DNL Journey Optimizer] configuración {#start-optimizer-configuration}

Al acceder [!DNL Journey Optimizer] por primera vez, se le aprovisiona un simulador para pruebas de producción y se le asigna un determinado número de direcciones IP en función de su contrato.

Para poder crear sus recorridos y enviar mensajes, debe seguir estos pasos de configuración:

1. **Configuración de mensajes y canales**: definir superficies de canal, adaptar y personalizar los mensajes.

   * Cree superficies de canal para configurar todos los parámetros técnicos necesarios para enviar mensajes. [Más información](channel-surfaces.md)

   * Determine qué dirección de correo electrónico utilizar con prioridad para los destinatarios cuando haya varias direcciones disponibles en Adobe Experience Platform. [Más información](primary-email-addresses.md)

   * Administre el número de días durante los cuales se realizan los reintentos antes de enviar direcciones de correo electrónico a la lista de supresión. [Más información](manage-suppression-list.md)

   * Defina la configuración de las notificaciones push en ambas [!DNL Adobe Experience Platform] y [!DNL Adobe Experience Platform Launch]. [Más información](../configuration/push-gs.md)

   <!--* Understand the push notification flow. [Learn more](../configuration/push-gs.md)-->

   * Configure su instancia para que envíe SMS (actualmente solo disponible para un conjunto de organizaciones - Disponibilidad limitada). [Más información](sms-configuration.md)


1. **Delegación de subdominios**: para cualquier nuevo subdominio que se vaya a utilizar en Journey Optimizer, el primer paso será delegarlo. [Más información](about-subdomain-delegation.md)

   ![](assets/subdomain.png)

1. **Crear grupos de IP**: mejore su capacidad de envío de correo electrónico y su reputación agrupando direcciones IP aprovisionadas con su instancia. [Más información](ip-pools.md)

   ![](assets/ip-pool.png)

1. **Configuración de recorridos**: para crear recorridos, debe configurar **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** y **[!UICONTROL Actions]**. [Más información](about-data-sources-events-actions.md)

   ![](assets/admin-menu.png)

   * La variable **fuente de datos** permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos. [Más información](../datasource/about-data-sources.md)

   * **Eventos** le permite realizar el déclencheur de sus recorridos de forma unitaria para enviar mensajes, en tiempo real, a la persona que entra en el recorrido. En la configuración de eventos, se configuran los eventos esperados en los recorridos. Los datos entrantes de los eventos se normalizan siguiendo el modelo de datos de Adobe Experience (XDM). Los eventos provienen de las API de ingesta de transmisión para eventos autenticados y no autenticados (como eventos del SDK de Adobe Mobile). [Más información](../event/about-events.md)

   * [!DNL Journey Optimizer] incorpora funciones de mensajes que le permiten diseñar y enviar contenido. Si utiliza un sistema de terceros para enviar mensajes, cree un **acción personalizada**. [Más información](../action/action.md)