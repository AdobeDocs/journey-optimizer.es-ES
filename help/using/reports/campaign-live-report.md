---
solution: Journey Optimizer
product: journey optimizer
title: Informe en vivo de la campaña
description: Aprenda a utilizar los datos del informe en directo de Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: adcfff1cb8bb2ae98d41e4071f56a137e52ee56a
workflow-type: tm+mt
source-wordcount: '1859'
ht-degree: 4%

---

# Informe en vivo de la campaña {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="Informe en vivo de la campaña"
>abstract="El informe en vivo de la campaña permite medir y visualizar en tiempo real el impacto y el rendimiento de las campañas solo durante las últimas 24 horas. El informe se divide en distintos widgets que detallan el éxito y los errores de la campaña. Cada tablero de informes se puede modificar cambiando el tamaño de los widgets o eliminándolos."

Los informes en directo, a los que se puede acceder desde la pestaña Últimas 24 horas, muestran los eventos que han tenido lugar en las últimas 24 horas, con un intervalo de tiempo mínimo de dos minutos desde que se produjo el evento. En comparación, los informes globales se centran en eventos que se produjeron hace al menos dos horas y abarcan eventos durante un período de tiempo seleccionado.

Se puede acceder directamente al informe de campaña en directo desde la campaña con la variable **[!UICONTROL Vista en vivo]** botón.

La campaña **[!UICONTROL Informe en vivo]** se mostrará con las siguientes pestañas:

* [Campaign](#campaign-live)
* [Correo electrónico](#email-live)
* [En la aplicación](#inapp-live)
* [Push](#push-live)
* [SMS](#sms-live)
* [Web](#web-tab)
* [Correo directo](#direct-mail-tab)

La campaña **[!UICONTROL Informe en vivo]** se divide en diferentes widgets que detallan el éxito y los errores de la campaña. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](../reports/live-report.md#modify-dashboard).

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](live-report.md#list-of-components-live).

## Pestaña Campaña {#campaign-live}

### envío {#delivery-live}

El **[!UICONTROL Estadísticas de campaña]** El widget detalla la información principal relativa a la campaña:

* **[!UICONTROL Perfiles introducidos]**: Número de perfiles que iniciaron el recorrido.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Pestaña Correo electrónico {#email-live}

Desde la campaña **[!UICONTROL Informe en vivo]**, el **[!UICONTROL Correo electrónico]** Esta pestaña detalla la información principal relativa a las entregas de correo electrónico enviadas en la campaña.

![](assets/campaign_report_live_1.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe de correo electrónico.

El **[!UICONTROL Estadísticas de envío de correo electrónico]** El widget detalla la información principal relativa al mensaje:

* **[!UICONTROL Entregado]**: número de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

El **[!UICONTROL Envío de métricas por correo electrónico]** tabla y **[!UICONTROL Resumen de correo electrónico]** el gráfico detalla el éxito de su envío:

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Entregado]**: número de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

* **[!UICONTROL Aperturas]**: Número de veces que se ha abierto un mensaje en una entrega.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en una entrega.

* **[!UICONTROL Cancelar suscripción]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Quejas de spam]**: Número de veces que un mensaje se declaró como correo no deseado.

El **[!UICONTROL Motivos del rechazo]**, **[!UICONTROL Categorías de rechazo]** y **[!UICONTROL Mensaje devuelto no válido y rechazos por correo electrónico]** los widgets contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Rechazo duro]**: el número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Rechazo suave]**: el número total de errores temporales, como una bandeja de entrada llena.

* **[!UICONTROL Ignorado]**: el número total de mensajes temporales, como Fuera de la oficina, o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

El **[!UICONTROL Motivos del error]** y **[!UICONTROL Razones de exclusión]** los gráficos y tablas permiten ver qué error y exclusiones se produjeron durante la entrega.

El **[!UICONTROL Correo electrónico: dominio del destinatario principal]** el gráfico y la tabla detallan qué dominios son los más utilizados por los destinatarios para abrir el correo electrónico.
+++

## Pestaña en la aplicación {#inapp-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_performance"
>title="Rendimiento en la aplicación"
>abstract="Los KPI de rendimiento en la aplicación proporcionan una perspectiva esencial de la participación de los visitantes con los mensajes en la aplicación en las últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="Interacciones por tipo"
>abstract="La tabla Interacciones por tipo detalla la interacción de los usuarios con el mensaje en la aplicación mediante el seguimiento de cualquier clic, despido o interacción de las últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="Resumen en la aplicación"
>abstract="El gráfico de resumen en la aplicación ilustra la progresión de las impresiones e interacciones en la aplicación durante las últimas 24 horas."

Desde la campaña **[!UICONTROL Informe en vivo]**, el **[!UICONTROL En la aplicación]** Esta pestaña detalla la información principal relativa a las entregas en la aplicación enviadas en la campaña.

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe en la aplicación.

El **[!UICONTROL Rendimiento en la aplicación]** Los KPI detallan la información principal relativa a la participación de los visitantes en los mensajes en la aplicación, como:

* **[!UICONTROL Impresiones]**: número total de mensajes en la aplicación entregados a todos los usuarios.

* **[!UICONTROL Interacciones]**: número total de interacciones con el mensaje en la aplicación. Esto incluye cualquier acción realizada por los usuarios, como clics, rechazos o cualquier otra interacción.

El **[!UICONTROL Resumen en la aplicación]** Este gráfico muestra la evolución de las impresiones e interacciones en la aplicación durante el periodo correspondiente.

El **[!UICONTROL Interacciones por tipo]** en los gráficos y la tabla se detalla la interacción de los usuarios con el mensaje en la aplicación mediante el seguimiento de cualquier clic, despido o interacción.

+++

## Pestaña de notificaciones push {#push-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_performance"
>title="Notificación push: rendimiento de envío"
>abstract="El gráfico Rendimiento de envío de notificaciones push resume los datos esenciales sobre las notificaciones push, como los errores o los mensajes enviados de las últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="Notificación push: estadísticas"
>abstract="La tabla Estadísticas push proporciona datos sobre la actividad del destinatario durante la entrega en las últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="Notificación push: resumen de envío"
>abstract="El gráfico Resumen de envío de notificaciones push muestra los datos disponibles para las notificaciones push enviadas desde las últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="Notificación push: razones de exclusión"
>abstract="Los gráficos y la tabla de motivos de exclusión ilustran los distintos factores que llevaron a que los perfiles de usuario, excluidos de la audiencia de destino, no recibieran el mensaje en las últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="Notificación push: razones de error"
>abstract="Los gráficos y la tabla de motivos de error permiten identificar los errores específicos que se produjeron en las últimas 24 horas durante la entrega."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="Notificación push: desglose por plataforma"
>abstract="Los gráficos y la tabla Desglose por plataforma proporcionan un desglose del éxito de las notificaciones push en las últimas 24 horas en función del sistema operativo del destinatario."

Desde la campaña **[!UICONTROL Informe en vivo]**, el **[!UICONTROL Notificación push]** Esta pestaña detalla la información principal relativa a las entregas push enviadas en la campaña.

![](assets/campaign_report_live_2.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe push.

**[!UICONTROL Rendimiento de envío de notificaciones push]**, **[!UICONTROL Resumen de notificaciones push]** y **[!UICONTROL Notificación push: estadísticas]** los widgets detallan la información principal relativa al mensaje:

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Entregado]**: número de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

* **[!UICONTROL Aperturas]**: Número de veces que se ha abierto un mensaje en una entrega.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación push entregada, por ejemplo, clic en el botón o despido.

* **[!UICONTROL Participaciones]**: Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

El **[!UICONTROL Motivos del error]** y **[!UICONTROL Razones de exclusión]** los gráficos y tablas permiten ver qué error y exclusiones se produjeron durante la entrega.

El **[!UICONTROL Envío de estadísticas: error]** El widget permite ver cuántos errores y rechazos se produjeron.

El **[!UICONTROL Seguimiento por plataforma]**, **[!UICONTROL Envío por plataforma]** y **[!UICONTROL Desglose por plataforma]** los gráficos y tablas detallan el éxito de la notificación push en función del sistema operativo.
+++

## Pestaña SMS {#sms-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="SMS: estadísticas"
>abstract="La tabla Estadísticas de envío de SMS resume los datos esenciales sobre sus mensajes SMS, como los mensajes dirigidos o enviados desde las últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="SMS: rendimiento por fecha"
>abstract="El widget Rendimiento por fecha de SMS proporciona información clave de las últimas 24 horas sobre sus mensajes a través de una representación gráfica."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="SMS: razones de error"
>abstract="Los gráficos y la tabla SMS: motivos de error le permiten identificar los errores específicos que se produjeron en las últimas 24 horas durante la entrega."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="SMS: razones de exclusión"
>abstract="Los gráficos y la tabla de motivos de exclusión ilustran los distintos factores que llevaron a que los perfiles de usuario, excluidos de la audiencia de destino, no recibieran el mensaje en las últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="SMS: motivos de rechazos"
>abstract="Los gráficos y la tabla de motivos de rechazos contienen los datos disponibles de las últimas 24 horas relacionados con los mensajes rechazados."

Desde la campaña **[!UICONTROL Informe en vivo]**, el **[!UICONTROL SMS]** Esta pestaña detalla la información principal relativa a los envíos SMS enviados en la campaña.

![](assets/campaign_report_live_3.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe SMS.

El **[!UICONTROL SMS: estadísticas]** La tabla detalla el éxito de su envío:

* **[!UICONTROL Objetivos]**: número de perfiles de usuario que se califican como perfiles de destinatario para este envío.

* **[!UICONTROL Excluido]**: número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron el mensaje.

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

* **[!UICONTROL Clics]**: Número total de visitas de URL.

El **[!UICONTROL Rendimiento de SMS por fecha]** El widget detalla la información principal relativa al mensaje con un gráfico:

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

El **[!UICONTROL Razones de exclusión]**, **[!UICONTROL Razones de rechazos]** y **[!UICONTROL Motivos del error]** los gráficos y tablas permiten ver qué error y exclusiones se produjeron durante la entrega.
+++

## Pestaña web {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_performance"
>title="Rendimiento web"
>abstract="Los KPI de rendimiento web proporcionan información completa sobre la participación de los visitantes con las experiencias web de las últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="Resumen web"
>abstract="El gráfico Resumen web ilustra la progresión de las experiencias web, incluidas las impresiones, las impresiones únicas y las interacciones, desde las últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="Interacciones por elemento"
>abstract="La tabla Interacciones por elemento proporciona información clave sobre la participación de los visitantes con diferentes elementos de las páginas web en las últimas 24 horas."

Desde la campaña **[!UICONTROL Informe en vivo]**, el **[!UICONTROL Web]** La pestaña detalla la información principal relativa a sus páginas web.

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe web.

El **[!UICONTROL Rendimiento web]** Los KPI detallan la información principal relativa a la participación de los visitantes en las experiencias web, como:

* **[!UICONTROL Impresiones]**: número total de experiencias web entregadas a todos los usuarios.

* **[!UICONTROL Interacciones]**: número total de interacciones con la página web. Esto incluye cualquier acción realizada por los usuarios, como clics o cualquier otra interacción.

El **[!UICONTROL Resumen web]** El gráfico muestra la evolución de las experiencias web (impresiones, impresiones únicas e interacciones) durante las últimas 24 horas.

El **[!UICONTROL Interacciones por elemento]** La tabla detalla la información principal relativa a la participación de los visitantes en los distintos elementos de las páginas web.
+++

## Ficha Correo directo {#direct-mail-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_sending_statistics"
>title="Correo directo: estadísticas de envío"
>abstract="La tabla Estadísticas de envío de correo directo resume los datos esenciales de las últimas 24 horas sobre sus mensajes de correo directo, como los mensajes dirigidos o enviados."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="Correo directo: razones de error"
>abstract="Los gráficos y la tabla Correo directo: motivos de error le permiten identificar los errores específicos que se han producido en las últimas 24 horas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="Correo directo: razones de exclusión"
>abstract="Los gráficos y la tabla de motivos de exclusión de correo directo ilustran los distintos factores que llevaron a que los perfiles de usuario, excluidos de la audiencia de destino, no recibieran el mensaje en las últimas 24 horas."

Desde la campaña **[!UICONTROL Informe en vivo]**, el **[!UICONTROL Correo directo]** Esta pestaña detalla la información principal relativa a sus envíos de correo directo.

![](assets/direct-mail-report_2.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe Correo directo.

El **[!UICONTROL Correo directo: estadísticas de envío]** La tabla detalla el éxito de su envío:

* **[!UICONTROL Objetivos]**: número de perfiles de usuario que se califican como perfiles de destinatario para este envío.

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

* **[!UICONTROL Excluido]**: número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron el envío.

El **[!UICONTROL Correo directo: razones de exclusión]** y **[!UICONTROL Correo directo: razones de error]** los gráficos y tablas permiten ver qué error y exclusiones se produjeron durante la entrega.
+++

## Recursos adicionales

* [Introducción a las campañas](../campaigns/get-started-with-campaigns.md)
* [Creación de una campaña](../campaigns/create-campaign.md)
* [Creación de campañas activadas por API](../campaigns/api-triggered-campaigns.md)
* [Modificación o detención de una campaña](../campaigns/modify-stop-campaign.md)
* [Informe global de la campaña](campaign-global-report.md)
