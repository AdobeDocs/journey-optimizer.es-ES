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
source-git-commit: b18f8c468157988be9cca44795b46f6fb4a0208e
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---


# Reintentos {#retries}

Cuando un mensaje de correo electrónico falla debido a un error temporal **Soft bounce**, se realizan varios reintentos. Cada error aumenta un contador de errores. Cuando este contador alcanza el umbral de límite, la dirección se agrega a la lista de supresión.

>[!NOTE]
>
>Obtenga más información sobre los tipos de errores en la sección [Tipos de errores de envío](../suppression-list.md#delivery-failures).

En la configuración predeterminada, el umbral se establece en 5 errores.

* Para el mismo envío, en el quinto error encontrado dentro del [periodo de reintento](#retry-duration), se suprime la dirección.

* Si hay diferentes entregas y dos errores se producen al menos con una diferencia de 24 horas, el contador de errores se incrementa con cada error y la dirección también se suprime en el quinto intento.

Si una entrega se realiza correctamente después de un reintento, el contador de errores de la dirección se reinicia.

Si el valor predeterminado de 5 no se adapta a sus necesidades, puede modificar el umbral de error siguiendo los pasos a continuación.

1. Vaya a **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Suppression list]**.

1. Seleccione el botón **[!UICONTROL Edit suppression rules]**.

   ![](../assets/suppression-list-edit-retries.png)

1. Edite el número permitido de rechazos leves consecutivos según sus necesidades.

   ![](../assets/suppression-list-edit-soft-bounces.png)

   Debe introducir un valor entero entre 1 y 20, lo que significa que el número mínimo de reintentos es 1 y el número máximo es 20.

   >[!CAUTION]
   >
   >Cualquier valor superior a 10 puede causar problemas de reputación de envío, así como restricciones de IP o inclusión en la lista de bloqueados por parte de los ISP. [Más información sobre la capacidad de entrega](../deliverability.md)

<!--![](../assets/retries-edition.png)-->

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

<!--Once a message has been in the retry queue for a maximum of 3.5 days and has failed to deliver, it will time out and its status will be updated to Failed??-->