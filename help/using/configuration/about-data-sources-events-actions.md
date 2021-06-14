---
title: Administración y configuración
description: Conozca las directrices de administración y configuración
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Configuración de la aplicación
topic: Administración
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 19%

---

# Configuración de recorridos

Para enviar mensajes con recorridos, debe configurar **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** y **[!UICONTROL Actions]**.

![](../assets/admin-menu.png)

## Fuentes de datos

La configuración de la fuente de datos permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos. [Más información](../../using/datasource/about-data-sources.md)

## Eventos

Los eventos le permiten almacenar en déclencheur sus recorridos de forma unitaria para enviar mensajes, en tiempo real, al individuo que entra en el recorrido.

En la configuración de eventos, se configuran los eventos esperados en los recorridos. Los datos entrantes de los eventos se normalizan siguiendo el modelo de datos de Adobe Experience (XDM). Los eventos provienen de las API de ingesta de transmisión para eventos autenticados y no autenticados (como eventos del SDK de Adobe Mobile). [Más información](../../using/event/about-events.md)

## Acciones

Las funcionalidades de mensajes de Journey Optimizer están incorporadas: solo necesita diseñar el contenido y publicar el mensaje. Si utiliza un sistema de terceros para enviar mensajes, puede crear una acción personalizada. [Más información](../../using/action/action.md)
