---
solution: Journey Optimizer
product: journey optimizer
title: Informe global de recorrido
description: Aprenda a utilizar los datos del informe global de recorrido
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: 82b8c9032d6c377cb76acce4d5cc45afb0ddd6ba
workflow-type: tm+mt
source-wordcount: '2408'
ht-degree: 2%

---

# Informe global de recorrido {#journey-global-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_global_report"
>title="Informe global de recorrido"
>abstract="El informe global del recorrido permite medir el impacto de sus recorridos durante un período de tiempo seleccionado. El informe se divide en distintos widgets que detallan el éxito y los errores del recorrido. Cada tablero de informes se puede modificar cambiando el tamaño de los widgets o eliminándolos."

Los informes globales, a los que se puede acceder desde la pestaña Todo el tiempo, muestran los eventos que se produjeron hace al menos dos horas y cubren los eventos de un periodo de tiempo seleccionado. En comparación, los informes en directo se centran en los eventos que han tenido lugar en las últimas 24 horas, con un intervalo de tiempo mínimo de dos minutos desde que se produjo el evento.

Se puede acceder al informe global de recorrido directamente desde su recorrido con el **[!UICONTROL Ver informe]** botón.

![](assets/report_journey.png)

El recorrido **[!UICONTROL Informe global]** se mostrará con las siguientes pestañas:

* [ Recorrido ](#journey-global)
* [Correo electrónico](#email-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [En la aplicación](#in-app-global)

El recorrido **[!UICONTROL Informe global]** se divide en diferentes widgets que detallan el éxito y los errores de su recorrido. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](global-report.md#modify-dashboard).

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](global-report.md#list-of-components-global).

## pestaña recorrido {#journey-global}

De tu recorrido **[!UICONTROL Informe global]**, el **[!UICONTROL Recorrido]** le ofrece una visión clara de los datos de seguimiento más importantes sobre su recorrido.

![](assets/journey_global_1.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe de Recorrido.

El **[!UICONTROL Rendimiento de recorrido]** Este widget permite ver paso a paso la ruta de los perfiles de destino en el recorrido.

El **[!UICONTROL Estadísticas de recorrido]** El widget muestra los siguientes KPI:

* **[!UICONTROL Perfiles introducidos]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL Perfiles abandonados]**: Número total de personas que salieron del recorrido.

* **[!UICONTROL Recorrido individual fallido]**: Número total de recorridos individuales que no se ejecutaron correctamente.

El **[!UICONTROL Eventos recibidos por evento]**, **[!UICONTROL Eventos por origen]** y **[!UICONTROL Eventos principales]** Los widgets permiten ver cuál de sus **[!UICONTROL Eventos]** se ejecutó correctamente mediante gráficos y tablas.

**[!UICONTROL Rendimiento de acción]**, **[!UICONTROL Motivos del error de acción]** y **[!UICONTROL Acciones principales]** los widgets representan la acción y los errores que se produjeron con mayor éxito cuando su **[!UICONTROL Acciones]** se activaron.

El **[!UICONTROL Acciones principales]** contiene los datos disponibles para **[!UICONTROL Acciones]**, como:

* **[!UICONTROL Acciones ejecutadas correctamente]**: Número total de **[!UICONTROL Acciones]** ejecutado correctamente para un recorrido.

* **[!UICONTROL Error en acción]**: Número total de errores que se produjeron para **[!UICONTROL Acciones]**.

El **[!UICONTROL Políticas de consentimiento]** La tabla y el gráfico muestran el número de perfiles excluidos de cada directiva en las acciones personalizadas.
Para obtener más información sobre las acciones personalizadas, consulte [la documentación detallada](../action/about-custom-action-configuration.md).

Tenga en cuenta que para que estos widgets aparezcan en los informes de Recorrido, deberá restablecer los paneles. Para ello, haga clic en **[!UICONTROL Modificar]** entonces **[!UICONTROL Restablecer]** en la parte superior del informe.
+++

## Pestaña de correo electrónico {#email-global}

De tu recorrido **[!UICONTROL Informe global]**, el **[!UICONTROL Correo electrónico]** Esta pestaña detalla la información principal relativa a los envíos de correo electrónico realizados en el recorrido.

![](assets/journey_global_2.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe de correo electrónico.

El **[!UICONTROL Estadísticas de envío de correo electrónico]** el gráfico detalla el éxito de su envío:

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución del correo electrónico recurrente en el recorrido. Para dirigirse solo a uno o varios correos electrónicos recurrentes, selecciónelos en la **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Objetivos]**: Número de perfiles dirigidos para cualquier acción, como enviar correos electrónicos o SMS.

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de entrega]**: porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de devoluciones]**: porcentaje de correos electrónicos que rebotaron en comparación con los enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

* **[!UICONTROL Tasa de error]**: porcentaje de errores que se han producido durante una entrega para evitar que se envíe en comparación con los correos electrónicos enviados.

El **[!UICONTROL Correo electrónico: estadísticas de seguimiento]** contiene los datos disponibles de la actividad del destinatario para la entrega:

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución del correo electrónico recurrente en el recorrido. Para dirigirse solo a uno o varios correos electrónicos recurrentes, selecciónelos en la **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Aperturas]**: Número de veces que se abrió la entrega en una entrega.

* **[!UICONTROL Aperturas únicas]**: porcentaje de envíos abiertos.

* **[!UICONTROL Tasa de apertura única]**: Número total de correos electrónicos abiertos en comparación con el número de correos electrónicos enviados.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

* **[!UICONTROL Clics únicos]**: número de destinatarios que hicieron clic en un contenido de un correo electrónico.

* **[!UICONTROL Tasa de pulsaciones]**: porcentaje de usuarios que interactuaron con el recorrido.

* **[!UICONTROL Cancelar suscripción]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Quejas de spam]**: Número de veces que un mensaje se declaró como correo no deseado.

El **[!UICONTROL Envío de estadísticas]** El gráfico contiene los datos disponibles para los correos electrónicos enviados, como:

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

El **[!UICONTROL Motivos del rechazo]** y **[!UICONTROL Categorías de rechazo]** los widgets contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Rechazo duro]**: el número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Rechazo suave]**: el número total de errores temporales, como una bandeja de entrada llena.

* **[!UICONTROL Ignorado]**: el número total de mensajes temporales, como Fuera de la oficina, o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

Para obtener más información sobre las devoluciones, consulte [Lista de supresión](../reports/suppression-list.md) página.

El **[!UICONTROL Motivos del error]** El gráfico y la tabla permiten ver qué error se produjo durante la entrega.

El **[!UICONTROL Razones de exclusión]** el gráfico y la tabla muestran los diferentes motivos que impidieron que los perfiles de usuario, excluidos de los perfiles de destino, recibieran el mensaje.

El **[!UICONTROL Correo electrónico: URL principal]** Un gráfico y una tabla detallan qué direcciones URL del envío son las más visitadas.

El **[!UICONTROL Correo electrónico: dominio del destinatario principal]** el gráfico y la tabla detallan qué dominios son los más utilizados por los destinatarios para abrir el correo electrónico.

>[!NOTE]
>
>El **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]**  los widgets solo están disponibles si la opción Send-Time Optimization está activada para la entrega. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

El **[!UICONTROL Optimizado frente a no optimizado]** El gráfico detalla la información principal relativa al mensaje, estén optimizados o no:

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.
* **[!UICONTROL Aperturas]**: Número de veces que se abrió la entrega en una entrega.
* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

El **[!UICONTROL Optimización del tiempo de envío]** detalla el éxito de su envío según el método de envío: optimizado o normal.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.
* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

>[!NOTE]
>
>Los widgets y las métricas de Ofertas solo están disponibles si se insertó una decisión en un mensaje de correo electrónico. Para obtener más información sobre Gestión de decisiones, consulte esta [página](../offers/get-started/starting-offer-decisioning.md).

El **[!UICONTROL Estadísticas de ofertas]** y **[!UICONTROL Estadísticas de ofertas]** con el tiempo, los widgets miden el éxito y el impacto de la oferta en la audiencia de destino. Detalla la información principal relativa al mensaje con KPI:

* **[!UICONTROL Oferta enviada]**: Número total de envíos para la oferta.

* **[!UICONTROL Impresión de oferta]**: Número de veces que se abrió la oferta en una entrega.

* **[!UICONTROL Clics de oferta]**: Número de veces que se hizo clic en una oferta en una entrega.

El **[!UICONTROL Estadísticas detalladas de ofertas]** contiene los datos disponibles de la actividad del destinatario con la oferta:

* **[!UICONTROL Nombre de ubicación]**: Nombre de la ubicación utilizada para mostrar la oferta. Para obtener más información sobre la ubicación, consulte esta sección [página](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Nombre de oferta]**: Nombre de la oferta añadida en la entrega. Para obtener más información sobre la ubicación, consulte esta sección [página](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Oferta enviada]**: Número total de envíos para la oferta.

* **[!UICONTROL Tasa de impresiones de oferta]**: porcentaje de ofertas abiertas comparado con el número de ofertas enviadas.

* **[!UICONTROL Tasa de pulsaciones de oferta]**: porcentaje de usuarios que interactuaron con la oferta.
+++

## Pestaña de notificación push {#push-global}

De tu recorrido **[!UICONTROL Informe global]**, el **[!UICONTROL Notificación push]** La pestaña detalla la información principal relativa a las entregas push enviadas en el recorrido.

![](assets/journey_global_3.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe push.

El **[!UICONTROL Notificación push: estadísticas de envío]** Esta tabla detalla la información principal relativa a las notificaciones push con gráficos y KPI:

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución de la notificación push recurrente en el recorrido. Para segmentar solo una o varias notificaciones push recurrentes, selecciónelas en el **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Objetivos]**: Número de perfiles dirigidos para cualquier acción, como enviar correos electrónicos o SMS.

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de entrega]**: porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de devoluciones]**: porcentaje de notificaciones push que rebotaron en comparación con las notificaciones push enviadas.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

* **[!UICONTROL Tasa de error]**: porcentaje de errores que se produjeron durante una entrega y que impiden su envío en comparación con las notificaciones push enviadas.

El **[!UICONTROL Push: estadísticas de seguimiento]** contiene los datos disponibles de la actividad del destinatario para la entrega:

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución de la notificación push recurrente en el recorrido. Para segmentar solo una o varias notificaciones push recurrentes, selecciónelas en el **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Aperturas]**: Número de veces que se ha abierto un mensaje en una entrega.

* **[!UICONTROL Tasa de apertura]**: porcentaje de notificaciones push abiertas.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación push entregada, por ejemplo, clic en el botón o despido.

* **[!UICONTROL Participaciones]**: Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

* **[!UICONTROL Tasa de participación]**: Porcentaje de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

El **[!UICONTROL Resumen de notificaciones push]** El gráfico contiene los datos disponibles para las notificaciones push enviadas, como:

* **[!UICONTROL Aperturas]**: Número de veces que se ha abierto un mensaje en una entrega.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación push entregada, por ejemplo, clic en el botón o despido.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

>[!NOTE]
>
>El **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]**  los widgets solo están disponibles si la opción Send-Time Optimization está activada para la entrega. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

El **[!UICONTROL Optimizado frente a no optimizado]** El gráfico detalla la información principal relativa al mensaje, estén optimizados o no:

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.
* **[!UICONTROL Aperturas]**: Número de veces que se abrió la entrega en una entrega.
* **[!UICONTROL Acciones]**: Número total de acciones en la notificación push entregada, por ejemplo, clic en el botón o despido.

El **[!UICONTROL Optimización del tiempo de envío]** detalla el éxito de su envío según el método de envío: optimizado o normal.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.
* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

El **[!UICONTROL Motivos del error]** El gráfico y la tabla permiten ver qué error se produjo durante la entrega.

El **[!UICONTROL Razones de exclusión]** el gráfico y la tabla muestran los diferentes motivos que impidieron que los perfiles de usuario, excluidos de los perfiles de destino, recibieran el mensaje.

El **[!UICONTROL Seguimiento por plataforma]**, **[!UICONTROL Envío por plataforma]** y **[!UICONTROL Desglose por plataforma]** los gráficos y tablas detallan el éxito de la notificación push según el sistema operativo del destinatario.

El SMS **[!UICONTROL Informe global]** se divide en diferentes widgets que detallan el éxito y los errores de la entrega. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](global-report.md#modify-dashboard).
+++

## Pestaña SMS {#sms-global}

![](assets/journey_global_4.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe SMS.

El **[!UICONTROL SMS: estadísticas de envío]** La tabla detalla el éxito de su envío:

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución del mensaje SMS recurrente en el recorrido. Para dirigirse solo a uno o varios mensajes SMS recurrentes, selecciónelos en la **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Objetivos]**: número de perfiles de usuario que se califican como perfiles de destinatario para este envío.

* **[!UICONTROL Excluido]**: número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron el mensaje.

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

El **[!UICONTROL Resumen de SMS]** El widget detalla la información principal relativa al mensaje con un gráfico:

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

El **[!UICONTROL Razones de exclusión]** los gráficos y tablas permiten ver qué error y exclusiones se produjeron durante la entrega.

El **[!UICONTROL SMS: clics por vínculos]** y **[!UICONTROL SMS: estadísticas de seguimiento]** los widgets detallan la información principal relativa a la participación de los visitantes con las direcciones URL.

+++

## Pestaña en la aplicación {#in-app-global}

De tu Recorrido **[!UICONTROL Informe global]**, el **[!UICONTROL En la aplicación]** Esta pestaña detalla la información principal relativa a los envíos en la aplicación enviados en los recorridos.

![](assets/in-app-journey-report.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe en la aplicación.

El **[!UICONTROL Rendimiento en la aplicación]** Los KPI detallan la información principal relativa a la participación de los visitantes en los mensajes en la aplicación, como:

* **[!UICONTROL Impresiones únicas]**: número de usuarios únicos a los que se ha mostrado el mensaje en la aplicación.

* **[!UICONTROL Impresiones]**: número total de mensajes en la aplicación mostrados a todos los usuarios.

  >[!NOTE]
  >
  >Para garantizar que se cuente una impresión, el usuario debe cumplir dos criterios:
  >* Calificación dentro de la experiencia en la aplicación, que se logra al alcanzar la actividad en la aplicación específica en su recorrido.
  >* Cumplir las condiciones especificadas en las reglas de Déclencheur.
  > 
  >Debido al segundo criterio, puede haber variaciones notables entre el número de perfiles objetivo y el recuento de impresiones únicas.

* **[!UICONTROL Interacción]**: número de interacciones con el mensaje en la aplicación. Esto incluye cualquier acción realizada por los usuarios, como clics, rechazos o cualquier otra interacción.

El **[!UICONTROL Resumen en la aplicación]** Este gráfico muestra la evolución de las impresiones e interacciones en la aplicación durante el periodo correspondiente.

El **[!UICONTROL Interacciones por tipo]** en los gráficos y la tabla se detalla la interacción de los usuarios con el mensaje en la aplicación mediante el seguimiento de cualquier clic, despido o interacción.
+++
