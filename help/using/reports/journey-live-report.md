---
solution: Journey Optimizer
product: journey optimizer
title: Informe de recorrido en vivo
description: Aprenda a utilizar los datos del informe en directo de recorrido
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e3781f79-7c8d-4512-b44f-835639b1471f
source-git-commit: 98be0e87928ddf0a7a73ca4dd91f5fc99d18d587
workflow-type: tm+mt
source-wordcount: '1285'
ht-degree: 4%

---

# Informe de recorrido en vivo {#journey-live-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_live_report"
>title="Informe de recorrido en vivo"
>abstract="El informe en vivo del recorrido permite medir y visualizar en tiempo real el impacto y el rendimiento de sus recorridos solo durante las últimas 24 horas. El informe se divide en distintos widgets que detallan el éxito y los errores del recorrido. Cada tablero de informes se puede modificar cambiando el tamaño de los widgets o eliminándolos."

Los informes en directo, a los que se puede acceder desde la pestaña Últimas 24 horas, muestran los eventos que han tenido lugar en las últimas 24 horas, con un intervalo de tiempo mínimo de dos minutos desde que se produjo el evento. En comparación, los informes globales se centran en eventos que se produjeron hace al menos dos horas y abarcan eventos durante un período de tiempo seleccionado.

Se puede acceder al informe en directo de recorrido directamente desde el recorrido con el **[!UICONTROL Ver informe]** botón.

![](assets/report_journey.png)

El recorrido **[!UICONTROL Informe en vivo]** se mostrará con las siguientes pestañas:

* [ Recorrido ](#journey-live)
* [Correo electrónico](#email-live)
* [Push](#push-live)
* [SMS](#sms-live)

El recorrido **[!UICONTROL Informe en vivo]** se divide en diferentes widgets que detallan el éxito y los errores de su recorrido. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](live-report.md#modify-dashboard).

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](live-report.md#list-of-components-live).

## pestaña recorrido {#journey-live}

De tu recorrido **[!UICONTROL Informe en vivo]**, el **[!UICONTROL Recorrido]** le ofrece una visión clara de los datos de seguimiento más importantes sobre su recorrido.

![](assets/journey_live_1.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe de Recorrido.

**[!UICONTROL Rendimiento de recorrido]** le permite ver la ruta de los perfiles objetivo paso a paso a través del recorrido.

El **[!UICONTROL Estadísticas de recorrido]** El widget muestra los siguientes KPI:

* **[!UICONTROL Perfiles introducidos]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL Perfiles abandonados]**: Número total de personas que salieron del recorrido.

* **[!UICONTROL Recorridos individuales con errores]**: Número total de recorridos individuales que no se ejecutaron correctamente.

El **[!UICONTROL Evento ejecutado en las últimas 24 horas]** y **[!UICONTROL Eventos]** los widgets permiten ver cuál de sus eventos se ejecutó correctamente a través del número de resumen, el gráfico y la tabla.

El **[!UICONTROL Acción ejecutada en las últimas 24 horas]** y **[!UICONTROL Acciones ejecutadas y errores]** los widgets representan la acción y los errores que se produjeron con mayor éxito cuando se activaron las acciones. El gráfico de acciones, la tabla y los números de resumen contienen los datos disponibles para acciones como las siguientes:

* **[!UICONTROL Acciones ejecutadas]**: Número total de acciones ejecutadas correctamente para un recorrido.

* **[!UICONTROL Error en acciones]**: Número total de errores que se produjeron para las acciones.
+++

## Pestaña Correo electrónico {#email-live}

De tu recorrido **[!UICONTROL Informe en vivo]**, el **[!UICONTROL Correo electrónico]** Esta pestaña detalla la información principal relativa a los envíos de correo electrónico realizados en el recorrido.

![](assets/journey_live_2.png)

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

>[!NOTE]
>
>Los widgets y las métricas de Ofertas solo están disponibles si se insertó una decisión en un mensaje de correo electrónico. Para obtener más información sobre Gestión de decisiones, consulte esta [página](../offers/get-started/starting-offer-decisioning.md).

El **[!UICONTROL Estadísticas de ofertas]** y **[!UICONTROL Estadísticas de ofertas]** con el tiempo, los widgets miden el éxito y el impacto de la oferta en la audiencia de destino. Detalla la información principal relativa al mensaje con KPI:

* **[!UICONTROL Oferta enviada]**: Número total de envíos para la oferta.

* **[!UICONTROL Impresión de oferta]**: Número de veces que se abrió la oferta en una entrega.

* **[!UICONTROL Clics de oferta]**: Número de veces que se hizo clic en una oferta en una entrega.
+++

## Pestaña de notificaciones push {#push-live}

De tu recorrido **[!UICONTROL Informe en vivo]**, el **[!UICONTROL Notificación push]** La pestaña detalla la información principal relativa a las entregas push enviadas en el recorrido.

![](assets/journey_live_3.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe push.

**[!UICONTROL Rendimiento de envío de notificaciones push]**, **[!UICONTROL Resumen de notificaciones push]** y **[!UICONTROL Envío de métricas: por notificación push]** los widgets detallan la información principal relativa al mensaje:

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

![](assets/journey_live_4.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe SMS.

El **[!UICONTROL SMS: estadísticas de envío]** La tabla detalla el éxito de su envío:

* **[!UICONTROL Objetivos]**: número de perfiles de usuario que se califican como perfiles de destinatario para este envío.

* **[!UICONTROL Excluido]**: número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron el mensaje.

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Aperturas]**: Número de veces que se ha abierto un mensaje en una entrega.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en una entrega.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

El **[!UICONTROL Resumen de SMS]** el gráfico detalla el éxito de su envío:

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

El **[!UICONTROL Razones de exclusión]** los gráficos y tablas permiten ver qué error y exclusiones se produjeron durante la entrega.
+++

## Pestaña en la aplicación {#in-app-live}

![](assets/journey_live_5.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe en la aplicación.

El **[!UICONTROL Rendimiento en la aplicación]** Los KPI detallan la información principal relativa a la participación de los visitantes en los mensajes en la aplicación, como:

* **[!UICONTROL Impresiones]**: número total de mensajes en la aplicación entregados a todos los usuarios.

* **[!UICONTROL Interacciones]**: número total de interacciones con el mensaje en la aplicación. Esto incluye cualquier acción realizada por los usuarios, como clics, rechazos o cualquier otra interacción.

El **[!UICONTROL Resumen en la aplicación]** Este gráfico muestra la evolución de las impresiones e interacciones en la aplicación durante el periodo correspondiente.

El **[!UICONTROL Interacciones por tipo]** en los gráficos y la tabla se detalla la interacción de los usuarios con el mensaje en la aplicación mediante el seguimiento de cualquier clic, despido o interacción.

+++
