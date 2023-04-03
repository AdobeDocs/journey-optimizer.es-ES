---
solution: Journey Optimizer
product: journey optimizer
title: Informe global de la campaña
description: Aprenda a utilizar los datos del informe Campaign Global
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 8a311d546829d0d80f32dfdddcdf30805688f757
workflow-type: tm+mt
source-wordcount: '1904'
ht-degree: 1%

---

# Informe global de la campaña {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Informe global de la campaña"
>abstract="El informe global de campaña permite medir el impacto de las campañas durante un período de tiempo seleccionado. El informe se divide en distintas utilidades que detallan el éxito y los errores de la campaña. Cada tablero de informes se puede modificar cambiando el tamaño o eliminando las utilidades."

Se puede acceder al informe global de campaña directamente desde la Campaign con la variable **[!UICONTROL Ver informe]** botón.

![](assets/campaign_report_global_5.png)

La campaña **[!UICONTROL Informe global]** se muestra con las siguientes pestañas:

* [Campaign](#campaign-global)
* [Correo electrónico](#email-global)
* [En la aplicación](#inapp-global)
* [Push](#push-global)
* [SMS](#sms-global)

La campaña **[!UICONTROL Informe global]** se divide en distintas utilidades que detallan el éxito y los errores de la campaña. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](../reports/global-report.md#modify-dashboard).

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](global-report.md#list-of-components-global.md)

## Pestaña Campaña {#campaign-global}

### envío {#delivery-global}

![](assets/campaign_report_global_1.png)

La variable **[!UICONTROL Estadísticas de Campaign]** La utilidad detalla la información principal relativa a la campaña:

* **[!UICONTROL Perfiles introducidos]**: Número de perfiles que iniciaron el recorrido.

* **[!UICONTROL Acciones entregadas]**: Número total de veces que se ha entregado una acción en el recorrido.

* **[!UICONTROL Las acciones fallaron en %]**: Número total de veces que una acción ha fallado en el recorrido en comparación con la cantidad total de veces que se ha entregado una acción.

## Ficha Correo electrónico {#email-global}

![](assets/campaign_report_global_2.png)

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL Correo electrónico]** La pestaña detalla la información principal relativa a los envíos de correo electrónico realizados en la campaña.

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe Correo electrónico .

La variable **[!UICONTROL Estadísticas de envío de correo electrónico]** graph detalla el éxito de la entrega:

* **[!UICONTROL Segmentado]**: Número total de mensajes procesados durante el análisis de envío.

* **[!UICONTROL Enviado]**: Número total de envíos para la entrega.

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de entrega]**: Porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Tasa de devoluciones]**: Porcentaje de correos electrónicos devueltos en comparación con los correos electrónicos enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Tasa de error]**: Porcentaje de errores que se produjeron durante una entrega que impiden que se envíe en comparación con los correos electrónicos enviados.

* **[!UICONTROL Reintentos]**: Número de correos electrónicos en cola para reintentos.

* **[!UICONTROL Excluido]**: Número de perfiles que Adobe Journey Optimizer ha excluido.

La variable **[!UICONTROL Correo electrónico: estadísticas de seguimiento]** contiene los datos disponibles para la actividad de destinatario para su envío:

* **[!UICONTROL Aperturas]**: Número de veces que se abrió la entrega en una entrega.

* **[!UICONTROL Aperturas únicas]**: Porcentaje de envíos abiertos.

* **[!UICONTROL Tasa de apertura]**: Número total de correos electrónicos abiertos comparados con el número de correos electrónicos enviados.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

* **[!UICONTROL Clics únicos]**: número de destinatarios que hicieron clic en un contenido en un correo electrónico.

* **[!UICONTROL Tasa de clics únicos]**: Porcentaje de usuarios que interactuaron con la entrega.

* **[!UICONTROL Baja de suscripciones]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Reclamaciones por correo no deseado]**: Número de veces que un mensaje se declaró como correo no deseado o no deseado.

La variable **[!UICONTROL Envío de estadísticas]** El gráfico contiene los datos disponibles para los correos electrónicos enviados, como:

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Reintentos]**: Número de correos electrónicos en cola para reintentos.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Razones de devolución]** y **[!UICONTROL Categorías de rebote]** los widgets contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Rechazo grave]**: El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Rechazo suave]**: El número total de errores temporales, como una bandeja de entrada completa.

* **[!UICONTROL Ignorado]**: El número total de mensajes temporales, como fuera de la oficina o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

Para obtener más información sobre las devoluciones, consulte la sección [Lista de supresión](../reports/suppression-list.md) página.

La variable **[!UICONTROL Motivos del error]** El gráfico y la tabla permiten ver qué error se produjo durante el envío.

La variable **[!UICONTROL Motivos excluidos]** en el gráfico y la tabla se muestran las diferentes razones que impidieron que los perfiles de usuario, excluidos de los perfiles de destino, recibieran el mensaje.

La variable **[!UICONTROL Correo Electrónico: Dirección Url Principal]** gráfico y tabla detallan las direcciones URL de su envío que son las más visitadas.

La variable **[!UICONTROL Correo electrónico: dominio de destinatario principal]** gráfico y tabla detallan qué dominios son los más utilizados por los destinatarios para abrir el correo electrónico.

>[!NOTE]
>
>La variable **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]**  las utilidades solo están disponibles si la opción de optimización del tiempo de envío está activada para la entrega. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

La variable **[!UICONTROL Optimizado frente a no optimizado]** graph detalla la información principal relativa al mensaje, independientemente de si están optimizados o no:

* **[!UICONTROL Enviado]**: Número total de envíos para la entrega.
* **[!UICONTROL Aperturas]**: Número de veces que se abrió la entrega en una entrega.
* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

La variable **[!UICONTROL Optimización del tiempo de envío]** detalla el éxito de la entrega en función del método de envío: optimizado o normal.

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.
* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.
+++

## Pestaña en la aplicación {#inapp-global}

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL En la aplicación]** La pestaña detalla la información principal relativa a los envíos en la aplicación realizados en la campaña.

![](assets/campaign_report_global_6.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe en la aplicación.

La variable **[!UICONTROL Rendimiento en la aplicación]** Los KPI detallan la información principal relativa a la participación de los visitantes en los mensajes en la aplicación, como por ejemplo:

* **[!UICONTROL Impresiones únicas]**: número de usuarios únicos a los que se entregó el mensaje en la aplicación.

* **[!UICONTROL Impresiones]**: número total de mensajes en la aplicación entregados a todos los usuarios.

* **[!UICONTROL Tasa de clics]**: porcentaje de usuarios que interactuaron con los botones incluidos en el mensaje en la aplicación en comparación con los usuarios que vieron el mensaje.

* **[!UICONTROL Tasa de rechazo]**: porcentaje de mensajes en la aplicación que descartaron los destinatarios.

La variable **[!UICONTROL Resumen en la aplicación]** en el gráfico se muestra la evolución de las impresiones en la aplicación durante el periodo correspondiente.

La variable **[!UICONTROL Clics por botón]** la tabla y el gráfico contienen los datos disponibles para el comportamiento del destinatario por botón:

* **[!UICONTROL Clics]**: número total de destinatarios que interactuaron con los botones incluidos en el mensaje en la aplicación.

* **[!UICONTROL Tasa de clics]**: porcentaje de usuarios que interactuaron con los botones incluidos en el mensaje en la aplicación en comparación con los usuarios que vieron el mensaje.
+++

## Pestaña de notificaciones push {#push-global}

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL Notificaciones push]** detalla la información principal relativa a los envíos push realizados en la campaña.

![](assets/campaign_report_global_3.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe push.

La variable **[!UICONTROL Notificaciones push: estadísticas de envío]** la tabla detalla la información principal relativa a las notificaciones push con gráficos y KPI:

* **[!UICONTROL Segmentado]**: Número total de mensajes procesados durante el análisis de envío.

* **[!UICONTROL Enviado]**: Número total de envíos para la entrega.

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de entrega]**: Porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Tasa de devoluciones]**: Porcentaje de notificaciones push que rebotaron en comparación con las notificaciones push enviadas.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Tasa de error]**: Porcentaje de errores que se produjeron durante una entrega que impiden que se envíe comparado con las notificaciones push enviadas.

* **[!UICONTROL Excluido]**: Número de perfiles que Adobe Journey Optimizer ha excluido.

La variable **[!UICONTROL Push - Tracking statistics]** contiene los datos disponibles para la actividad de destinatario para su envío:

* **[!UICONTROL Aperturas]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Tasa de apertura]**: Porcentaje de notificaciones push abiertas.

* **[!UICONTROL Acciones]**: Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.

* **[!UICONTROL Participaciones]**: Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

* **[!UICONTROL Tasa de participación]**: Porcentaje de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

La variable **[!UICONTROL Resumen de notificaciones push]** El gráfico contiene los datos disponibles para las notificaciones push enviadas, como:

* **[!UICONTROL Aperturas]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Acciones]**: Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

>[!NOTE]
>
>La variable **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]**  las utilidades solo están disponibles si la opción de optimización del tiempo de envío está activada para la entrega. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

La variable **[!UICONTROL Optimizado frente a no optimizado]** graph detalla la información principal relativa al mensaje, independientemente de si están optimizados o no:

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.
* **[!UICONTROL Aperturas]**: Número de veces que se abrió la entrega en una entrega.
* **[!UICONTROL Acciones]**: Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.

La variable **[!UICONTROL Optimización del tiempo de envío]** detalla el éxito de la entrega en función del método de envío: optimizado o normal.

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.
* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

La variable **[!UICONTROL Motivos del error]** El gráfico y la tabla permiten ver qué error se produjo durante el envío.

La variable **[!UICONTROL Motivos excluidos]** en el gráfico y la tabla se muestran las diferentes razones que impidieron que los perfiles de usuario, excluidos de los perfiles de destino, recibieran el mensaje.

La variable **[!UICONTROL Seguimiento por plataforma]**, **[!UICONTROL Envío por plataforma]** y **[!UICONTROL Desglose por plataforma]** gráficos y tablas detallan el éxito de la notificación push en función del sistema operativo del destinatario.
+++

## Ficha SMS {#sms-global}

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL SMS]** La pestaña detalla la información principal relativa a los envíos SMS enviados en la campaña.

![](assets/campaign_report_global_4.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe SMS.

La variable **[!UICONTROL SMS: estadísticas de envío]** La tabla detalla el éxito de la entrega:

* **[!UICONTROL Segmentado]**: Número de perfiles de usuario que se califican como perfiles de destinatario para este envío.

* **[!UICONTROL Excluido]**: Número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron el mensaje.

* **[!UICONTROL Enviado]**: Número total de envíos para la entrega.

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Rendimiento de SMS por fecha]** La utilidad detalla la información principal relativa al mensaje con un gráfico:

* **[!UICONTROL Enviado]**: Número total de envíos para la entrega.

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Excluir motivos]**, **[!UICONTROL Razones de devoluciones]** y **[!UICONTROL Motivos del error]** los gráficos y las tablas permiten ver qué error y exclusiones se produjeron durante el envío.

La variable **[!UICONTROL SMS: clics por vínculos]** y **[!UICONTROL SMS - Estadísticas de seguimiento]** las utilidades detallan la información principal relativa a la participación de los visitantes en las direcciones URL.

+++

## Recursos adicionales

* [Introducción a las campañas](../campaigns/get-started-with-campaigns.md)
* [Creación de una campaña](../campaigns/create-campaign.md)
* [Creación de campañas activadas por API](../campaigns/api-triggered-campaigns.md)
* [Modificación o detención de una campaña](../campaigns/modify-stop-campaign.md)
* [Informe en directo de la campaña](campaign-live-report.md)
