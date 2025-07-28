---
solution: Journey Optimizer
product: journey optimizer
title: Tipos de error de correo electrónico
description: Acceda a la lista de todos los posibles errores de correo electrónico al realizar entregas con Journey Optimizer.
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: reintentos, rebote, suave, omitido, duro, optimizador, error
hide: true
hidefromtoc: true
source-git-commit: 1e36871c2c975c81d018fabb3cff51d11c98962e
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 11%

---


# Tipos de error de correo electrónico

Los posibles motivos de un error de entrega son múltiples. La siguiente tabla detalla todos los errores que pueden producirse al enviar envíos de correo electrónico con [!DNL Journey Optimizer], junto con su descripción y tipo de error.

Estos errores se pueden encontrar en el [Conjunto de datos de evento de comentarios de mensajes de AJO](../data/datasets-query-examples.md#message-feedback-event-dataset), que contiene los registros de envío de mensajes, incluida la información de todos los envíos de mensajes de [!DNL Journey Optimizer], y los registros de comentarios de los ISP de correo electrónico sobre los rechazos.

| Etiqueta de error | Tipo de error | Valor técnico | Descripción |
| --- | --- | --- | --- |
| **Indeterminado** | Ignorado | 1 | No se puede clasificar el mensaje de rebote SMTP recibido del ISP. |
| **Destinatario no válido** | Rechazo permanente | 10 | La dirección del destinatario no es válida. |
| **Destinatario rechazado** | Rechazo permanente | 15 | El ISP del destinatario ha rechazado el mensaje, y el ISP puede bloquear al remitente si el destinatario no está suprimido. |
| **Rebote suave** | Rechazo temporal | 20 | Se ha producido un error temporal en el mensaje. Puede tener éxito en futuros reintentos. |
| **Error de DNS** | Rechazo temporal | 21 | Se ha producido un error temporal de DNS en la entrega del mensaje. Puede tener éxito en futuros reintentos. |
| **Buzón lleno** | Rechazo temporal | 22 | El mensaje experimentó un error temporal de entrega, ya que el buzón del destinatario estaba lleno. |
| **Demasiado grande** | Ignorado | 23 | Se ha producido un error en la entrega temporal del mensaje porque el tamaño del mensaje ha superado el límite del destinatario. |
| **Tiempo de espera** | Ignorado | 24 | Error en la entrega del mensaje porque la validez del mensaje ha caducado o porque se ha tardado demasiado en enviar al ISP. |
| **Error de administración** | Administración | 25 | Error en la entrega debido a alguna configuración de directiva en la infraestructura de envío de correo electrónico. |
| **Devolución genérica: SIN RCPT** | Ignorado | 30 | No se pudo entregar el mensaje porque no se identificó el destinatario. |
| **Rechazo genérico** | Ignorado | 40 | Se ha producido un error en la entrega temporal del mensaje por motivos no especificados. |
| **Bloque de correo** | Ignorado | 50 | La entrega experimentó un error temporal debido a los altos límites de volumen o velocidad del ISP. |
| **Bloque de correo no deseado** | Ignorado | 51 | La entrega experimentó un error temporal porque el ISP consideraba los dominios o las direcciones IP del remitente una fuente de correo no deseado conocida. |
| **Contenido de spam** | Ignorado | 52 | Se ha producido un error temporal en la entrega porque el ISP ha clasificado el contenido del correo electrónico como correo no deseado. |
| **Retransmisión denegada** | Rechazo temporal | 54 | No se ha podido aceptar el mensaje porque el dominio de destino no está incluido en la lista de permitidos para la retransmisión. |
| **Respuesta automática** | Ignorado | 60 | Estos mensajes son descartados por [!DNL Journey Optimizer] cuando se reciben a menos que el reenvío esté habilitado. |
| **Error transitorio** | Ignorado | 70 | La entrega se volverá a intentar a una velocidad limitada o se puede aplazar en caso de suspensión. |
| **Desafío-respuesta** | Rechazo temporal | 100 | Es posible que el envío falle de forma permanente, ya que [!DNL Journey Optimizer] no admite un mecanismo de autenticación desafío-respuesta. |
