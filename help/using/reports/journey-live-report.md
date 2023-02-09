---
solution: Journey Optimizer
product: journey optimizer
title: Informe de recorrido en vivo
description: Aprenda a utilizar los datos del informe de recorrido en directo
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e3781f79-7c8d-4512-b44f-835639b1471f
source-git-commit: 0ec122bbf134c41f95755a3b6f08eb7ef68506df
workflow-type: tm+mt
source-wordcount: '1138'
ht-degree: 1%

---

# Informe de recorrido en vivo {#journey-live-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_live_report"
>title="Informe de recorrido en vivo"
>abstract="El informe Recorrido en directo le permite medir y visualizar en tiempo real el impacto y el rendimiento de sus recorridos solo durante las últimas 24 horas. El informe se divide en distintas utilidades que detallan el éxito y los errores del recorrido. Cada tablero de informes se puede modificar cambiando el tamaño o eliminando las utilidades."

Se puede acceder al informe de recorrido en directo directamente desde el recorrido con la variable **[!UICONTROL Ver informe]** botón.

![](assets/report_journey.png)

El recorrido **[!UICONTROL Informe activo]** se muestra con las siguientes pestañas:

* [ Recorrido ](#journey-live)
* [Correo electrónico](#email-live)
* [Push](#push-live)
* [SMS](#sms-live)

El recorrido **[!UICONTROL Informe activo]** se divide en distintas utilidades que detallan el éxito y los errores de su recorrido. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](live-report.md#modify-dashboard).

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](live-report.md#list-of-components-live).

## ficha recorrido {#journey-live}

Desde su recorrido **[!UICONTROL Informe activo]**, el **[!UICONTROL Recorrido]** le proporciona una vista clara de los datos de seguimiento más importantes sobre su recorrido.

![](assets/journey_live_1.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe de Recorrido.

**[!UICONTROL Rendimiento del recorrido]** le permite ver la ruta de sus perfiles de destino paso a paso a través de su recorrido.

La variable **[!UICONTROL Estadísticas de recorrido]** muestra los siguientes KPI:

* **[!UICONTROL Perfiles introducidos]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL Perfiles de salida]**: Número total de personas que salieron del recorrido.

* **[!UICONTROL Recorridos individuales con errores]**: Número total de recorridos individuales que no se ejecutaron correctamente.

La variable **[!UICONTROL Evento ejecutado en las últimas 24 horas]** y **[!UICONTROL Eventos]** las utilidades permiten ver cuál de los eventos se ejecutó correctamente mediante el número de resumen, el gráfico y la tabla.

La variable **[!UICONTROL Acción ejecutada en las últimas 24 horas]** y **[!UICONTROL Acciones ejecutadas y errores]** las utilidades representan la acción más exitosa y los errores que se produjeron cuando se activaron las acciones. Los números del gráfico de acción, la tabla y el resumen contienen los datos disponibles para acciones como:

* **[!UICONTROL Acciones ejecutadas]**: Número total de acciones ejecutadas correctamente para un recorrido.

* **[!UICONTROL Error en las acciones]**: Número total de errores que se produjeron en las acciones.
+++

## Ficha Correo electrónico {#email-live}

Desde su recorrido **[!UICONTROL Informe activo]**, el **[!UICONTROL Correo electrónico]** La pestaña detalla la información principal relativa a los envíos de correo electrónico realizados en el recorrido.

![](assets/journey_live_2.png)

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

>[!NOTE]
>
>Las métricas y las utilidades de Ofertas solo están disponibles si se ha insertado una decisión en un mensaje de correo electrónico. Para obtener más información sobre la gestión de decisiones, consulte esta [página](../offers/get-started/starting-offer-decisioning.md).

La variable **[!UICONTROL Estadística de ofertas]** y **[!UICONTROL Estadísticas de ofertas]** a lo largo del tiempo, los widgets miden el éxito y el impacto de su oferta en la audiencia de destino. Detalla la información principal relativa al mensaje con KPI:

* **[!UICONTROL Oferta enviada]**: Número total de envíos para la oferta.

* **[!UICONTROL Impresión de oferta]**: Número de veces que la oferta se abrió en una entrega.

* **[!UICONTROL Clics en ofertas]**: Número de veces que se hizo clic en una oferta en una entrega.
+++

## Pestaña de notificaciones push {#push-live}

Desde su recorrido **[!UICONTROL Informe activo]**, el **[!UICONTROL Notificaciones push]** detalla la información principal relativa a los envíos push realizados en el recorrido.

![](assets/journey_live_3.png)

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

![](assets/journey_live_4.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe SMS.

La variable **[!UICONTROL SMS: estadísticas de envío]** La tabla detalla el éxito de la entrega:

* **[!UICONTROL Segmentado]**: Número de perfiles de usuario que se califican como perfiles de destinatario para este envío.

* **[!UICONTROL Excluido]**: Número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron el mensaje.

* **[!UICONTROL Enviado]**: Número total de envíos para la entrega.

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente.

* **[!UICONTROL Aperturas]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en una entrega.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Resumen de SMS]** graph detalla el éxito de la entrega:

* **[!UICONTROL Entrega]**: Número de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Excluir motivos]** los gráficos y las tablas permiten ver qué error y exclusiones se produjeron durante el envío.
+++
