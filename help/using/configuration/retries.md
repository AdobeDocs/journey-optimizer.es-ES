---
title: Reintentos
description: Descubra cómo se realizan los reintentos antes de enviar una dirección a la lista de supresión
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
feature: Configuración de la aplicación
topic: Administración
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 2%

---


# Reintentos {#retries}

Cuando un mensaje falla debido a un error temporal **Soft bounce** o **Ignored**, se realizan varios reintentos. Cada error aumenta un contador de errores. Cuando este contador alcanza el umbral de límite, la dirección se agrega a la lista de supresión.

En la configuración predeterminada<!--so can you edit this setting or not?? contradictory information was given-->, el umbral se establece en tres errores:

* Para la misma entrega, en el tercer error encontrado, la dirección se suprime.

* Si hay diferentes entregas y dos errores se producen al menos con una diferencia de 24 horas, el contador de errores se incrementa con cada error y la dirección también se suprime en el tercer intento.

Si una entrega se realiza correctamente después de un reintento, el contador de errores de la dirección se reinicia.

Puede modificar el umbral de límite mediante el botón **[!UICONTROL Edit]** del menú **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]**.<!--currently you can edit this in staging // now I see in UI: Suppression rule > Bounce days??? > 4-->

![](../assets/retries-edition.png)

## Duración del reintento de mensaje {#retry-duration}

Los reintentos se realizarán durante **3,5 días** desde el momento en que se agregó el mensaje a la cola de correo electrónico.

El retardo mínimo entre reintentos y el número máximo de reintentos que se van a realizar es <!--managed by the Enhanced MTA,--> en función del rendimiento histórico y actual de una IP en un dominio determinado.

Después de 3,5 días, cualquier mensaje de la cola de reintentos se eliminará de la cola y se enviará de nuevo como una devolución.<!--???-->