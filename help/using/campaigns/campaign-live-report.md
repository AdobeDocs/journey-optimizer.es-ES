---
title: Informe en directo de la campaña
description: Aprenda a utilizar los datos del informe de campaña en directo
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6177a33edeb3b8381c3eb5609762b4d974dc93e3
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 5%

---

# Informe en directo de la campaña {#campaign-live-report}

Se puede acceder al informe de campaña en directo directamente desde la campaña con la variable **[!UICONTROL Live view]** botón.

La campaña **[!UICONTROL Live report]** se muestra con las siguientes pestañas:

* [Campaign](#campaign-live)
* [Correo electrónico](#email-live)
* [Push](#push-live)

La campaña **[!UICONTROL Live report]** se divide en distintas utilidades que detallan el éxito y los errores de la campaña. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](../reports/live-report.md#modify-dashboard).

## Pestaña Campaña {#campaign-global}

### Entrega {#delivery-global}

La variable **[!UICONTROL Campaign Statistics]** La utilidad detalla la información principal relativa a la campaña:

* **[!UICONTROL Entered profiles]**: Número de perfiles que iniciaron el recorrido.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->
## Ficha Correo electrónico {#email-live}

Desde la campaña **[!UICONTROL Live report]**, el **[!UICONTROL Email]** pestaña detalla la información principal relativa a los envíos de correo electrónico realizados en la campaña.

Para obtener un informe detallado sobre un envío de correo electrónico específico, consulte la [Enviar informe activo por correo electrónico](../reports/email-live-report.md) para obtener más información.

La variable **[!UICONTROL Email Sending Statistics]** La utilidad detalla la información principal relativa al mensaje:

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Sending metrics by Email]** tabla y **[!UICONTROL Email Summary]** graph detalla el éxito de la entrega:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Clicks]**: Número de veces que se hizo clic en un contenido en una entrega.

* **[!UICONTROL Unsubscribe]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Spam complaints]**: Número de veces que un mensaje se declaró como correo no deseado o no deseado.

La variable **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** y **[!UICONTROL Hard and bounce - by Email]** los widgets contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Hard bounce]**: El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Soft bounce]**: El número total de errores temporales, como una bandeja de entrada completa.

* **[!UICONTROL Ignored]**: El número total de mensajes temporales, como fuera de la oficina o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

La variable **[!UICONTROL Error Reasons]** y **[!UICONTROL Exclude Reasons]** los gráficos y las tablas permiten ver qué error y exclusiones se produjeron durante el envío.

La variable **[!UICONTROL Email - Top recipient domain]** gráfico y tabla detallan qué dominios son los más utilizados por los destinatarios para abrir el correo electrónico.

## Ficha Insertar {#push-live}

Desde la campaña **[!UICONTROL Live report]**, el **[!UICONTROL Push]** detalla la información principal relativa a los envíos push realizados en la campaña.

Para obtener un informe detallado sobre una entrega push específica, consulte la [Insertar informe activo](../reports/push-live-report.md) para obtener más información.

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** y **[!UICONTROL Sending metrics - by Push]** widgets detalla la información principal relativa a su mensaje:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Actions]**: Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.

* **[!UICONTROL Engagements]**: Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

La variable **[!UICONTROL Error Reasons]** y **[!UICONTROL Exclude Reasons]** los gráficos y las tablas permiten ver qué error y exclusiones se produjeron durante el envío.

La variable **[!UICONTROL Sending statistics - Failed]** permite ver cuántos errores y rechazos se han producido.

La variable **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** y **[!UICONTROL Breakdown by platform]** gráficos y tablas detallan el éxito de la notificación push en función del sistema operativo.

## Recursos adicionales

* [Introducción a las campañas](get-started-with-campaigns.md)
* [Creación de una campaña](create-campaign.md)
* [Creación de campañas activadas por API](api-triggered-campaigns.md)
* [Modificación o detención de una campaña](modify-stop-campaign.md)
* [Informe global de la campaña](campaign-global-report.md)
