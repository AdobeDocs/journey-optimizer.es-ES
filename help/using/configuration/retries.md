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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 79c3c47eb6978f377bf4dc49f787e9a509aa3f61
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---


# Reintentos {#retries}

Cuando un mensaje de correo electrónico falla debido a un error temporal **Soft bounce** o **Ignored**, se realizan varios reintentos. Cada error aumenta un contador de errores. Cuando este contador alcanza el umbral de límite, la dirección se agrega a la lista de supresión.

>[!NOTE]
>
>Obtenga más información sobre los tipos de errores en la sección [Tipos de errores de envío](../suppression-list.md#delivery-failures).

En la configuración predeterminada, el umbral se establece en tres errores:

* Para la misma entrega, en el tercer error encontrado, la dirección se suprime.

* Si hay diferentes entregas y dos errores se producen al menos con una diferencia de 24 horas, el contador de errores se incrementa con cada error y la dirección también se suprime en el tercer intento.

Si una entrega se realiza correctamente después de un reintento, el contador de errores de la dirección se reinicia.

Puede modificar el umbral de límite mediante el botón **[!UICONTROL Edit]** del menú **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]**.

![](../assets/retries-edition.png)

<!--The minimum delay between retries and the maximum number of retries to be performed are based on how well an IP is performing, both historically and currently, at a given domain.-->

## Período de tiempo de reintento {#retry-duration}

El **periodo de tiempo de reintento** es el periodo en el que se reintentará cualquier mensaje de correo electrónico de la entrega que haya encontrado un error temporal o una devolución del mensaje.

De forma predeterminada, los reintentos se realizan durante **3,5 días** (o **84 horas**) desde el momento en que se agregó el mensaje a la cola de correo electrónico.

Sin embargo, para asegurarse de que los intentos de reintento ya no se realicen cuando ya no se necesiten, puede cambiar esta configuración según sus necesidades al crear o editar un [ajuste preestablecido de mensaje](message-presets.md) que se aplique al canal de correo electrónico.

Por ejemplo, puede establecer el periodo de reintento en 24 horas para un correo electrónico transaccional relacionado con el restablecimiento de contraseña y que contenga un vínculo válido solo para un día. Del mismo modo, para una venta a medianoche, es posible que desee definir un periodo de reintento de 6 horas.

>[!NOTE]
>
>El periodo de reintento no puede exceder las 84 horas. El periodo de reintento mínimo es de 6 horas para los correos electrónicos de marketing y 10 minutos para los correos electrónicos transaccionales.

Aprenda a ajustar los parámetros de reintento de correo electrónico al crear un ajuste preestablecido de mensaje en [esta sección](message-presets.md#create-message-preset).

<!--After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->