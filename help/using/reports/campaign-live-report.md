---
title: Informe en directo de la campaña
description: Aprenda a utilizar los datos del informe de campaña en directo
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: aecbf0f8bcfb8f6747ee072d891029a38f8f2ed1
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 3%

---

# Informe en directo de la campaña {#campaign-live-report}

Se puede acceder al informe de campaña en directo directamente desde la campaña con la variable **[!UICONTROL Vista en directo]** botón.

La campaña **[!UICONTROL Informe activo]** se muestra con las siguientes pestañas:

* [Campaign](#campaign-live)
* [Correo electrónico](#email-live)
* [Push](#push-live)
* [SMS](#sms-live)


La campaña **[!UICONTROL Informe activo]** se divide en distintas utilidades que detallan el éxito y los errores de la campaña. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](../reports/live-report.md#modify-dashboard).

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](live-report.md#list-of-components-live).

## Pestaña Campaña {#campaign-global}

### Entrega {#delivery-global}

La variable **[!UICONTROL Estadísticas de campaña]** La utilidad detalla la información principal relativa a la campaña:

* **[!UICONTROL Perfiles introducidos]**: Número de perfiles que iniciaron el recorrido.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->
## Ficha Correo electrónico {#email-live}

Desde la campaña **[!UICONTROL Informe activo]**, el **[!UICONTROL Correo electrónico]** pestaña detalla la información principal relativa a los envíos de correo electrónico realizados en la campaña.

![](assets/campaign_report_live_1.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe Correo electrónico .

La variable **[!UICONTROL Estadísticas de envío de correo electrónico]** La utilidad detalla la información principal relativa al mensaje:

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Envío de métricas por correo electrónico]** tabla y **[!UICONTROL Resumen de correo electrónico]** graph detalla el éxito de la entrega:

* **[!UICONTROL Enviado]**: Número total de envíos para la entrega.

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Aperturas]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en una entrega.

* **[!UICONTROL Cancelar suscripción]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Reclamaciones por correo no deseado]**: Número de veces que un mensaje se declaró como correo no deseado o no deseado.

La variable **[!UICONTROL Razones de devolución]**, **[!UICONTROL Categorías de rebote]** y **[!UICONTROL Grave y rechazado: por correo electrónico]** los widgets contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Rechazo grave]**: El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Rechazo suave]**: El número total de errores temporales, como una bandeja de entrada completa.

* **[!UICONTROL Ignorado]**: El número total de mensajes temporales, como fuera de la oficina o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

La variable **[!UICONTROL Motivos del error]** y **[!UICONTROL Excluir motivos]** los gráficos y las tablas permiten ver qué error y exclusiones se produjeron durante el envío.

La variable **[!UICONTROL Correo electrónico: dominio de destinatario principal]** gráfico y tabla detallan qué dominios son los más utilizados por los destinatarios para abrir el correo electrónico.
+++

## Pestaña de notificaciones push {#push-live}

Desde la campaña **[!UICONTROL Informe activo]**, el **[!UICONTROL Notificaciones push]** detalla la información principal relativa a los envíos push realizados en la campaña.

![](assets/campaign_report_live_2.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe push.

**[!UICONTROL Rendimiento de envío de notificaciones push]**, **[!UICONTROL Resumen de notificaciones push]** y **[!UICONTROL Envío de métricas: por inserción]** widgets detalla la información principal relativa a su mensaje:

* **[!UICONTROL Enviado]**: Número total de envíos para la entrega.

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Aperturas]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Acciones]**: Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.

* **[!UICONTROL Participaciones]**: Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

La variable **[!UICONTROL Motivos del error]** y **[!UICONTROL Excluir motivos]** los gráficos y las tablas permiten ver qué error y exclusiones se produjeron durante el envío.

La variable **[!UICONTROL Envío de estadísticas: error]** permite ver cuántos errores y rechazos se han producido.

La variable **[!UICONTROL Seguimiento por plataforma]**, **[!UICONTROL Envío por plataforma]** y **[!UICONTROL Desglose por plataforma]** gráficos y tablas detallan el éxito de la notificación push en función del sistema operativo.
+++

## Ficha SMS {#sms-live}

Desde la campaña **[!UICONTROL Informe activo]**, el **[!UICONTROL SMS]** La pestaña detalla la información principal relativa a los envíos SMS enviados en la campaña.

![](assets/campaign_report_live_3.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe SMS.

La variable **[!UICONTROL SMS: estadísticas de envío]** La tabla detalla el éxito de la entrega:

* **[!UICONTROL Segmentado]**: Número de perfiles de usuario que se califican como perfiles de destinatario para este envío.

* **[!UICONTROL Excluido]**: Número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron el mensaje.

* **[!UICONTROL Enviado]**: Número total de envíos para la entrega.

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Rendimiento de SMS por fecha]** La utilidad detalla la información principal relativa al mensaje con un gráfico:

* **[!UICONTROL Enviado]**: Número total de envíos para la entrega.

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Excluir motivos]**, **[!UICONTROL Razones de devoluciones]** y **[!UICONTROL Motivos del error]** los gráficos y las tablas permiten ver qué error y exclusiones se produjeron durante el envío.
+++

## Recursos adicionales

* [Introducción a las campañas](../campaigns/get-started-with-campaigns.md)
* [Creación de una campaña](../campaigns/create-campaign.md)
* [Creación de campañas activadas por API](../campaigns/api-triggered-campaigns.md)
* [Modificación o detención de una campaña](../campaigns/modify-stop-campaign.md)
* [Informe global de la campaña](campaign-global-report.md)
