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
source-git-commit: 5671f510d8be80b53d57b1ff90a101e500773243
workflow-type: tm+mt
source-wordcount: '4368'
ht-degree: 11%

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

### Rendimiento de recorrido {#journey-perfomance}

>[!CONTEXTUALHELP]
>id="ajo_journey_performance"
>title="Rendimiento de recorrido"
>abstract="El widget Rendimiento del Recorrido permite rastrear visualmente la ruta de los perfiles de destino a medida que avanzan por el recorrido."

![](assets/journey_performance.png)

El **[!UICONTROL Rendimiento de recorrido]** Este widget permite rastrear visualmente la trayectoria de los perfiles de destino a medida que navegan por el recorrido.

### Estadísticas de recorrido {#journey-statistics}

>[!CONTEXTUALHELP]
>id="ajo_journey_statistics"
>title="Estadísticas de recorrido"
>abstract="Los indicadores clave de rendimiento (KPI) de las estadísticas de Recorrido sirven como un panel completo, que proporciona un análisis en profundidad de las métricas esenciales relacionadas con su recorrido."

![](assets/journey_statistics.png)

El **[!UICONTROL Estadísticas de recorrido]** Los indicadores clave de rendimiento (KPI) funcionan como un panel que abarca todo, lo que ofrece un análisis de las métricas esenciales asociadas con el recorrido. Esto incluye detalles como el recuento de perfiles introducidos y los casos de recorridos individuales fallidos, lo que ofrece una perspectiva completa de la eficacia y el nivel de participación de su recorrido.

+++ Más información sobre las métricas de Estadísticas de Recorrido

* **[!UICONTROL Perfiles introducidos]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL Perfiles abandonados]**: Número total de personas que salieron del recorrido.

* **[!UICONTROL Recorrido individual fallido]**: Número total de recorridos individuales que no se ejecutaron correctamente.

+++

### Rendimiento de acción {#action-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_performance"
>title="Rendimiento de acción"
>abstract="El widget Rendimiento de la acción ilustra las acciones que tuvieron lugar con mayor éxito cuando se iniciaron las acciones."

![](assets/journey_action_performance.png)

El **[!UICONTROL Rendimiento de acción]** widget representa las acciones más exitosas que se produjeron cuando su **[!UICONTROL acciones]** se activaron.

### Acciones principales {#top-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_top_actions"
>title="Acciones principales"
>abstract="La tabla Acciones principales consolida la información vital sobre sus acciones, ofreciendo observaciones concisas sobre la frecuencia y la eficacia de cada acción."

![](assets/journey_top_actions.png)

El **[!UICONTROL Acciones principales]** La tabla de recopila datos esenciales sobre **[!UICONTROL Acciones]**. Proporciona una perspectiva sucinta de la frecuencia y el rendimiento de cada acción.

+++ Más información sobre las Métricas de acciones principales

* **[!UICONTROL Acciones ejecutadas correctamente]**: Número total de **[!UICONTROL Acciones]** ejecutado correctamente para un recorrido.

* **[!UICONTROL Error en acción]**: Número total de errores que se produjeron para **[!UICONTROL Acciones]**.

+++

### Razones de error de acciones {#action-error}

>[!CONTEXTUALHELP]
>id="ajo_journey_actions_error_reasons"
>title="Razones de error de acciones"
>abstract="La tabla de motivos de error de acciones y el gráfico proporcionan un resumen detallado de los errores encontrados durante la ejecución de sus acciones, y ofrecen una visión general completa de los problemas que pueden haber ocurrido."

![](assets/journey_action_error.png)

El **[!UICONTROL Motivos del error de acción]** La tabla y el gráfico ofrecen una visión general de los errores que se produjeron durante la ejecución de su **[!UICONTROL Acciones]**.

### Eventos por origen {#events-origin}

>[!CONTEXTUALHELP]
>id="ajo_journey_events_origin"
>title="Eventos por origen"
>abstract="La tabla y los gráficos Events by Origin ofrecen una visión de la recepción exitosa de sus eventos. Estas representaciones visuales le permiten identificar con precisión los eventos que se recibieron de forma eficaz, lo que proporciona una valiosa perspectiva del rendimiento y el impacto de cada evento dentro de su recorrido."

![](assets/journey_events_origin.png)

El **[!UICONTROL Eventos por origen]** La tabla y los gráficos proporcionan una perspectiva detallada sobre la recepción exitosa de su **[!UICONTROL eventos]**. A través de estas representaciones visuales, usted puede discernir con precisión cuál de sus **[!UICONTROL eventos]** fueron recibidos con eficacia, ofreciendo valiosas perspectivas sobre el rendimiento y el impacto de los eventos individuales dentro de su recorrido.

### Eventos recibidos por evento {#events-received}

>[!CONTEXTUALHELP]
>id="ajo_journey_events_received"
>title="Eventos recibidos por evento"
>abstract="El gráfico Eventos recibidos por evento permite identificar y analizar los eventos específicos dentro del recorrido que se ejecutaron de forma eficaz, lo que proporciona información valiosa sobre el rendimiento y las tasas de éxito de los eventos individuales."

![](assets/journey_event_received.png)

El **[!UICONTROL Eventos recibidos por evento]** El gráfico permite identificar y analizar cada **[!UICONTROL evento]** dentro de su recorrido se ejecutó de forma eficaz, lo que proporciona una valiosa perspectiva del rendimiento y las tasas de éxito de los eventos individuales.

### Eventos principales {#top-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_top_events"
>title="Eventos principales"
>abstract="La tabla Eventos principales consolida los datos esenciales sobre sus eventos, ofreciendo observaciones concisas sobre la frecuencia y el rendimiento de cada evento individual."

![](assets/journey_top_events.png)

El **[!UICONTROL Eventos principales]** La tabla de recopila datos esenciales sobre **[!UICONTROL Eventos]**. Proporciona una perspectiva sucinta de la frecuencia y el rendimiento de cada **[!UICONTROL Evento]**.

### Políticas de consentimiento {#consent-policies}

>[!CONTEXTUALHELP]
>id="ajo_journey_consent_policies"
>title="Políticas de consentimiento"
>abstract="La tabla y el gráfico de directivas de consentimiento muestran la cantidad de perfiles excluidos de cada directiva dentro de las acciones personalizadas. Esta presentación ofrece una perspectiva clara de la influencia de cada política de consentimiento en las exclusiones de perfil."

![](assets/journey_consent.png)

El **[!UICONTROL Políticas de consentimiento]** La tabla y el gráfico muestran el número de perfiles excluidos de cada directiva dentro de las acciones personalizadas. Esto proporciona una perspectiva clara del impacto de cada política de consentimiento en las exclusiones de perfil.

Para obtener más información sobre las acciones personalizadas, consulte [la documentación detallada](../action/about-custom-action-configuration.md).

Tenga en cuenta que para que estos widgets aparezcan en los informes de Recorrido, deberá restablecer los paneles. Para ello, haga clic en **[!UICONTROL Modificar]** entonces **[!UICONTROL Restablecer]** en la parte superior del informe.

## Pestaña de correo electrónico {#email-global}

De tu recorrido **[!UICONTROL Informe global]**, el **[!UICONTROL Correo electrónico]** Esta pestaña detalla la información principal relativa a los correos electrónicos enviados en el recorrido.

### Correo electrónico: estadísticas de envío {#email-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sending_statistics"
>title="Correo electrónico: estadísticas de envío"
>abstract="La tabla Correo electrónico: Estadísticas de envío resume los datos esenciales sobre sus correos electrónicos, como los segmentados o enviados."

![](assets/journey_email_statistics.png)

El **[!UICONTROL Estadísticas de envío de correo electrónico]** proporciona un resumen completo de los datos esenciales sobre los correos electrónicos en los recorridos. Detalla métricas clave como el tamaño de la audiencia objetivo y la cantidad de correos electrónicos enviados correctamente, lo que ofrece perspectivas valiosas sobre la eficacia y el alcance de los correos electrónicos y recorridos.

+++ Más información sobre las métricas de estadísticas de envío de correo electrónico

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución de recorrido en caso de recorridos recurrentes. Para segmentar solo una o varias recurrencias, selecciónelas en la **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Objetivos]**: Número de perfiles dirigidos para cualquier acción, como enviar correos electrónicos o SMS.

* **[!UICONTROL Enviado]**: Número total de correos electrónicos enviados para el recorrido.

* **[!UICONTROL Entregado]**: Número de correos electrónicos enviados correctamente, en relación con el número total de correos electrónicos enviados.

* **[!UICONTROL Tasa de entrega]**: porcentaje de correos electrónicos enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de correos electrónicos enviados.

* **[!UICONTROL Tasa de devoluciones]**: porcentaje de correos electrónicos que rebotaron en comparación con los enviados.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante el proceso de envío y que impiden su envío a los perfiles.

* **[!UICONTROL Tasa de error]**: porcentaje de errores que se produjeron durante el proceso de envío y que impiden su envío en comparación con los correos electrónicos enviados.

* **[!UICONTROL Reintentos]**: Número de correos electrónicos en cola para reintentos.

* **[!UICONTROL Excluido]**: Número de perfiles que han sido excluidos por Adobe Journey Optimizer.

+++

### Correo electrónico: Estadísticas de seguimiento {#email-tracking}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_tracking_statistics"
>title="Correo electrónico: Estadísticas de seguimiento"
>abstract="La tabla Correo electrónico: Estadísticas de seguimiento proporciona datos sobre la actividad del perfil del Correo electrónico."

![](assets/journey_email_tracking.png)

El **[!UICONTROL Correo electrónico: estadísticas de seguimiento]** La tabla de ofrece una descripción detallada de la actividad de perfil relacionada con los correos electrónicos incluidos en el recorrido. Esto incluye métricas sobre aperturas, clics y otros indicadores de participación relevantes, lo que ofrece una vista completa de cómo los perfiles interactúan con el contenido del correo electrónico.

+++ Más información sobre las Métricas de estadísticas de seguimiento de correo electrónico

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución del correo electrónico recurrente en el recorrido. Para dirigirse solo a uno o varios correos electrónicos recurrentes, selecciónelos en la **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Aperturas]**: Número de veces que los correos electrónicos se abrieron en un recorrido.

* **[!UICONTROL Aperturas únicas]**: porcentaje de correos electrónicos abiertos.

* **[!UICONTROL Tasa de apertura única]**: Número total de correos electrónicos abiertos en comparación con el número de correos electrónicos enviados.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en los correos electrónicos.

* **[!UICONTROL Clics únicos]**: Número de destinatarios que hicieron clic en un contenido de los correos electrónicos.

* **[!UICONTROL Tasa de pulsaciones]**: porcentaje de usuarios que interactuaron con el recorrido.

* **[!UICONTROL Baja de suscripciones]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Quejas de spam]**: Número de veces que los mensajes de correo electrónico se declararon como correo no deseado.

+++

### Correo electrónico: Rendimiento de envío {#email-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sending_performance"
>title="Correo electrónico: Rendimiento de envío"
>abstract="El gráfico de rendimiento Correo electrónico: envío presenta datos completos sobre los correos electrónicos enviados, ofreciendo perspectivas sobre métricas clave como envíos y devoluciones, lo que permite un análisis detallado del proceso de envío de correo electrónico."

![](assets/journey_email_performance.png)

El **[!UICONTROL Correo electrónico: rendimiento de envío]** El gráfico de proporciona una vista completa de los datos relacionados con los correos electrónicos enviados en el recorrido, lo que ofrece perspectivas sobre métricas clave como envíos y devoluciones. Esto permite un análisis detallado del proceso de envío de correo electrónico, lo que proporciona información valiosa sobre la eficacia y el rendimiento de sus recorridos.

+++ Más información sobre el Correo electrónico: envío de métricas de rendimiento

* **[!UICONTROL Entregado]**: Número de correos electrónicos enviados correctamente, en relación con el número total de correos electrónicos enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Reintentos]**: Número de correos electrónicos en cola para reintentos.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante un proceso de envío que impidieron que se enviara a los perfiles.

+++

### Correo electrónico: categorías y motivos de rechazo {#email-bounce-categories}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces"
>title="Correo electrónico: categorías y motivos de rechazo"
>abstract="Los widgets Correo electrónico: categorías y motivos de rechazo agregan los datos correspondientes a los mensajes rechazados, ofreciendo una perspectiva exhaustiva de los motivos y las categorías específicos que contribuyen a los rechazos de correo electrónico"

![](assets/journey_email_bounce_categories.png)

El **[!UICONTROL Motivos del rechazo]** y **[!UICONTROL Categorías de rechazo]** los widgets compilan los datos disponibles relacionados con los mensajes devueltos, proporcionando una perspectiva detallada de los motivos y las categorías específicos detrás de los rechazos de correo electrónico.

Para obtener más información sobre las devoluciones, consulte [Lista de supresión](../reports/suppression-list.md) página.

+++ Más información sobre las métricas Correo electrónico: categorías de rechazo

* **[!UICONTROL Rechazo duro]**: el número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Rechazo suave]**: el número total de errores temporales, como una bandeja de entrada llena.

* **[!UICONTROL Ignorado]**: el número total de mensajes temporales, como Fuera de la oficina, o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

+++

### Correo electrónico: Motivos de error {#email-errors}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_error_reasons"
>title="Correo electrónico: Motivos de error"
>abstract="El correo electrónico: los gráficos y la tabla Motivos de error permiten le permiten identificar los errores específicos que se produjeron durante el envío."

![](assets/journey_email_error.png)

El **[!UICONTROL Motivos del error]** los gráficos y las tablas ofrecen visibilidad de los errores específicos que se produjeron durante el proceso de envío, lo que proporciona información valiosa sobre la naturaleza y la incidencia de los errores.

### Correo electrónico: Motivos excluidos {#email-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_excluded_reasons"
>title="Correo electrónico: Motivos excluidos"
>abstract="Los gráficos y la tabla Motivos excluidos ilustran los distintos factores que llevaron a que los perfiles de usuario, excluidos del público destinatario, no recibieran el mensaje."

![](assets/journey_email_excluded.png)

El **[!UICONTROL Razones de exclusión]** los gráficos y la tabla presentan una vista completa de los diferentes factores que resultaron en la exclusión de perfiles de usuario de la audiencia de destino, lo que da como resultado que el mensaje no se reciba.

Consulte [esta página](exclusion-list.md) para obtener la lista completa de motivos de exclusión.

### Enviados y entregados por dominios {#sent-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sent_delivered_domains"
>title="Enviados y entregados por dominios"
>abstract="La tabla y el gráfico Enviados y entregados por dominios ofrecen un desglose de los correos electrónicos clasificados por dominios, y ofrecen información exhaustiva sobre el rendimiento general de sus comunicaciones por correo electrónico."

![](assets/journey_email_sent_domains.png)

El **[!UICONTROL Enviados y entregados por dominios]** La tabla y el gráfico proporcionan un desglose detallado de los correos electrónicos en el nivel de dominio, lo que ofrece información completa sobre el rendimiento de los correos electrónicos.

+++ Más información sobre las Métricas de Enviado y entregado por dominios

* **[!UICONTROL Enviado]**: Número total de envíos de correos electrónicos.

* **[!UICONTROL Entregado]**: Número de correos electrónicos enviados correctamente, en relación con el número total de correos electrónicos enviados.

+++

### Aperturas y clics por dominios {#open-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_open_clicks_domains"
>title="Aperturas y clics por dominios"
>abstract="El gráfico y la tabla Abrir y clics por dominios ofrecen un desglose detallado a nivel de dominio, y presentan una vista completa de cómo la audiencia interactúa con los correos electrónicos."

![](assets/journey_email_open_domains.png)

El **[!UICONTROL Abrir y hacer clic por dominios]** los gráficos y las tablas muestran un desglose a nivel de dominio de la participación de sus perfiles con su correo electrónico, lo que proporciona una valiosa perspectiva de cómo los distintos dominios interactúan con su contenido.

+++ Más información sobre las métricas Abrir y clics por dominios

* **[!UICONTROL Aperturas]**: Número de veces que se abrió el correo electrónico.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

+++

### Rechazos y errores por dominios {#bounces-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces_errors_domains"
>title="Rechazos y errores por dominios"
>abstract="El gráfico y la tabla Devoluciones y errores por dominios proporcionan un desglose granular a nivel de dominio, y ofrecen perspectivas de errores específicos encontrados durante el proceso de envío de correo electrónico."

![](assets/journey_email_bounce_domains.png)

El **[!UICONTROL Devoluciones y errores por dominios]** El gráfico y la tabla ofrecen un desglose a nivel de dominio de los errores específicos encontrados durante el proceso de envío, lo que proporciona un análisis detallado de los problemas que se han producido.

+++ Más información sobre las Métricas Devoluciones y errores por dominios

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de correos electrónicos enviados.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante el proceso de envío y que impiden su envío a los perfiles.

+++

### Razones de rechazo por dominio {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces_reasons_domains"
>title="Razones de rechazos por dominios"
>abstract="El gráfico y la tabla Razones de rechazo por dominio proporciona un desglose a nivel de dominio, lo que ofrece una perspectiva completa de los errores temporales y permanentes. Este análisis detallado le proporciona información valiosa sobre los motivos específicos detrás de los mensajes rechazados."

![](assets/journey_email_bounce_reasons_domain.png)

El **[!UICONTROL Razones de rechazo por dominio]** los gráficos y las tablas ofrecen un desglose de datos a nivel de dominio sobre los errores temporales y permanentes, lo que proporciona una perspectiva detallada de los motivos que subyacen a los mensajes rechazados.

### Correo electrónico: URL principal {#email-top}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_top_url"
>title="Correo electrónico: URL principal"
>abstract="Correo electrónico: el gráfico y la tabla URL principal ofrecen una visión general de las direcciones URL dentro del correo electrónico que reciben el mayor tráfico de visitantes, lo que le permite identificar los vínculos más populares."

![](assets/journey_email_top.png)

El **[!UICONTROL Correo electrónico: URL principal]** El gráfico y la tabla proporcionan una visión general de las direcciones URL del correo electrónico que atraen el mayor tráfico de visitantes. Esto le permite identificar y priorizar los vínculos más populares, lo que mejora su comprensión de la participación del perfil con contenido específico en los correos electrónicos.

### Correo electrónico: optimización {#email-sto}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_optimization"
>title="Correo electrónico: optimización"
>abstract="Los widgets Optimización del tiempo de envío y Optimizado frente a no optimizado proporcionan información detallada sobre los mensajes, destacando si se han optimizado o no."

![](assets/journey_email_sto.png)

>[!NOTE]
>
>El **[!UICONTROL Optimización del tiempo de envío]** y **[!UICONTROL Optimizado frente a no optimizado]** los widgets solo están disponibles si la opción Send-Time Optimization está activada para la entrega. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

El **[!UICONTROL Optimización del tiempo de envío]** y **[!UICONTROL Optimizado frente a no optimizado]** los widgets detallan el éxito de los correos electrónicos en función del método de envío: optimizado o normal.

+++ Obtenga más información sobre la Optimización del tiempo de envío y las métricas optimizadas frente a las no optimizadas

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.
* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Enviado]**: Número total de correos electrónicos enviados para el recorrido.

* **[!UICONTROL Aperturas]**: Número de veces que se abrieron los correos electrónicos en el recorrido.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en los correos electrónicos.

+++

### Correo electrónico: ofertas {#email-offers}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_offers"
>title="Correo electrónico: ofertas"
>abstract="Los widgets de estadísticas de Ofertas y Ofertas detallados proporcionan una perspectiva completa del rendimiento de sus ofertas, ofreciendo un análisis detallado de su impacto a lo largo del tiempo y presentando estadísticas detalladas para una comprensión más detallada."

>[!NOTE]
>
>Los widgets y las métricas de Ofertas solo están disponibles si se insertó una decisión en un mensaje de correo electrónico. Para obtener más información sobre Gestión de decisiones, consulte esta [página](../offers/get-started/starting-offer-decisioning.md).

El **[!UICONTROL Estadísticas de ofertas]** y **[!UICONTROL Estadísticas detalladas de ofertas]** con el tiempo, los widgets miden el éxito y el impacto de la oferta en la audiencia de destino. Detalla la información principal relativa al mensaje con KPI.

+++ Más información sobre el Correo electrónico: métricas de ofertas

* **[!UICONTROL Oferta enviada]**: Número total de envíos para la oferta.

* **[!UICONTROL Impresión de oferta]**: Número de veces que se abrió la oferta en sus correos electrónicos.

* **[!UICONTROL Clics de oferta]**: Número de veces que se hizo clic en una oferta en sus correos electrónicos.

* **[!UICONTROL Nombre de ubicación]**: Nombre de la ubicación utilizada para mostrar la oferta. Para obtener más información sobre la ubicación, consulte esta sección [página](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Nombre de oferta]**: Nombre de la oferta añadida en los correos electrónicos. Para obtener más información sobre la ubicación, consulte esta sección [página](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Oferta enviada]**: Número total de envíos para la oferta.

* **[!UICONTROL Tasa de impresiones de oferta]**: porcentaje de ofertas abiertas comparado con el número de ofertas enviadas.

* **[!UICONTROL Tasa de pulsaciones de oferta]**: porcentaje de usuarios que interactuaron con la oferta.

+++

## Pestaña de notificación push {#push-global}

De tu recorrido **[!UICONTROL Informe global]**, el **[!UICONTROL Notificación push]** Esta pestaña detalla la información principal relativa a las notificaciones push enviadas en el recorrido.

### Notificación push: estadísticas de envío {#push-sending-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_sending_statistics"
>title="Notificación push: estadísticas de envío"
>abstract="La tabla Estadísticas de envío de notificaciones push resume los datos esenciales sobre las notificaciones push, como los mensajes dirigidos o enviados."

![](assets/journey_push_sending.png)

El **[!UICONTROL Notificación push: estadísticas de envío]** proporciona un resumen conciso de los datos esenciales relacionados con las notificaciones push, incluidas las métricas clave como el número de mensajes dirigidos y el número de mensajes enviados correctamente.

+++ Más información sobre las Notificaciones push: envío de métricas de estadísticas

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución de recorrido en caso de recorridos recurrentes. Para segmentar solo una o varias recurrencias, selecciónelas en la **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Objetivos]**: Número de perfiles dirigidos para cualquier acción, como enviar correos electrónicos o SMS.

* **[!UICONTROL Enviado]**: Número total de notificaciones push enviadas.

* **[!UICONTROL Entregado]**: Número de notificaciones push enviadas correctamente, en relación con el número total de notificaciones push enviadas.

* **[!UICONTROL Tasa de entrega]**: porcentaje de notificaciones push enviadas correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de notificaciones push enviadas.

* **[!UICONTROL Tasa de devoluciones]**: porcentaje de notificaciones push que rebotaron en comparación con las notificaciones push enviadas.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante el proceso de envío y que impiden su envío a los perfiles.

* **[!UICONTROL Tasa de error]**: porcentaje de errores que se produjeron durante el proceso de envío y que impiden su envío en comparación con las notificaciones push enviadas.

* **[!UICONTROL Excluido]**: Número de perfiles que han sido excluidos por Adobe Journey Optimizer.

+++

### Notificación push: estadísticas de seguimiento {#push-tracking-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_tracking_statistics"
>title="Notificación push: estadísticas de seguimiento"
>abstract="Las Estadísticas de seguimiento push proporcionan datos sobre la actividad del perfil de su notificación push."

El **[!UICONTROL Push: estadísticas de seguimiento]** El widget ofrece una instantánea detallada de la actividad del perfil vinculada a las notificaciones push, lo que proporciona una información esencial sobre la participación y la eficacia de las notificaciones push.

+++ Más información sobre las Notificaciones push: métricas de estadísticas de seguimiento

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución de recorrido en caso de recorridos recurrentes. Para segmentar solo una o varias recurrencias, selecciónelas en la **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Aperturas]**: Número de veces que se abrieron las notificaciones push en el recorrido.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación push entregada, por ejemplo, clic en el botón o despido.

+++

### Notificación push: resumen del envío {#push-summary}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_sending_summary"
>title="Notificación push: resumen del envío"
>abstract="El gráfico Resumen del envío de notificaciones push muestra los datos disponibles para las notificaciones push enviadas."

![](assets/journey_push_summary.png)

El **[!UICONTROL Notificación push: resumen de envío]** el gráfico ofrece una representación dinámica que muestra un análisis de la actividad de notificaciones push. Esta representación gráfica proporciona un desglose completo de las notificaciones push enviadas.

+++ Más información sobre las Notificaciones push: envío de métricas de resumen

* **[!UICONTROL Aperturas]**: Número de veces que se abrieron las notificaciones push en el recorrido.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación push entregada, por ejemplo, clic en el botón o despido.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de notificaciones push enviadas.

* **[!UICONTROL Entregado]**: Número de notificaciones push enviadas correctamente, en relación con el número total de notificaciones push enviadas.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante el proceso de envío y que impiden su envío a los perfiles.

+++

### Notificación push: motivos del error {#push-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_error_reasons"
>title="Notificación push: motivos del error"
>abstract="Los gráficos y la tabla Motivos del error permiten identificar los errores específicos que se produjeron durante el proceso de envío"

![](assets/journey_push_error.png)

El **[!UICONTROL Motivos del error]** La tabla y los gráficos le permiten identificar los errores específicos que se produjeron durante el proceso de envío de las notificaciones push, lo que ofrece información detallada sobre cualquier problema que se haya encontrado durante el proceso.

### Notificación push: motivos excluidos {#push-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_excluded_reasons"
>title="Notificación push: motivos excluidos"
>abstract="Los gráficos y la tabla de motivos de exclusión ilustran los distintos factores que impidieron que los perfiles de usuario, excluidos de la audiencia de destino, recibieran el mensaje."

![](assets/journey_push_excluded.png)

El **[!UICONTROL Razones de exclusión]** los gráficos y la tabla muestran los diferentes motivos que impidieron que los perfiles de usuario, excluidos de los perfiles de destino, recibieran las notificaciones push.

Consulte [esta página](exclusion-list.md) para obtener la lista completa de motivos de exclusión.

### Notificación push: desglose por plataforma {#push-breakdown}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_breakdown_platform"
>title="Notificación push: desglose por plataforma"
>abstract="Los gráficos y la tabla Notificación push: desglose por plataforma proporcionan un desglose del éxito de las notificaciones push en función del sistema operativo del perfil."

![](assets/journey_push_breakdown.png)

El **[!UICONTROL Desglose por plataforma]** el gráfico y la tabla proporcionan un análisis detallado del éxito de sus notificaciones push, y ofrecen perspectivas basadas en el sistema operativo de su perfil. Este desglose mejora su comprensión del rendimiento de las notificaciones push en las distintas plataformas.

### Notificación push: optimización {#push-sto}

>[!NOTE]
>
>El **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]** los widgets solo están disponibles si la opción Send-Time Optimization está activada para la entrega. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

El **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]** los widgets detallan la información principal relativa al mensaje, estén optimizados o no.

+++ Más información sobre las Notificaciones push: métricas de optimización

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Aperturas]**: Número de veces que se abrieron las notificaciones push en el recorrido.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación push entregada, por ejemplo, clic en el botón o despido.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

+++

## Pestaña SMS {#sms-global}

### SMS: estadísticas de envío {#sms-sending-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_sending_statistics"
>title="SMS: estadísticas de envío"
>abstract="La tabla SMS: estadísticas de envío resume los datos esenciales sobre sus mensajes SMS, como mensajes dirigidos o enviados."

![](assets/journey_sms_sending.png)

El **[!UICONTROL SMS: estadísticas de envío]** La tabla proporciona un resumen conciso de los datos esenciales relacionados con sus mensajes SMS, que incluye métricas clave como el número de mensajes dirigidos y el recuento de mensajes enviados correctamente.

+++ Más información sobre SMS: métricas de estadísticas de envío

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución de recorrido en caso de recorridos recurrentes. Para segmentar solo una o varias recurrencias, selecciónelas en la **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Objetivos]**: Número de perfiles de usuario que se califican como perfiles de destinatario para sus mensajes SMS.

* **[!UICONTROL Excluido]**: número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron sus mensajes SMS.

* **[!UICONTROL Enviado]**: Número total de mensajes SMS enviados para el recorrido.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes SMS enviados.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante el proceso de envío y que impiden su envío a los perfiles.

+++

### SMS: estadísticas de seguimiento {#sms-tracking-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_tracking_statistics"
>title="SMS: estadísticas de seguimiento"
>abstract="El widget SMS: estadísticas de seguimiento proporciona una visión general completa de la información esencial relacionada con la interacción de los visitantes con la dirección URL."

![](assets/journey_sms_tracking.png)

El **[!UICONTROL SMS: estadísticas de seguimiento]** Este widget proporciona una descripción detallada de la información clave relacionada con la participación de los visitantes con las direcciones URL, lo que ofrece perspectivas sobre la eficacia de los mensajes SMS.

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución del SMS recurrente. Para dirigirse solo a uno o varios SMS recurrentes, selecciónelos en la **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en sus mensajes SMS.

### SMS: rendimiento por fecha {#sms-performance-date}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_perfomance_date"
>title="SMS: rendimiento por fecha"
>abstract="El widget SMS: rendimiento por fecha proporciona información clave sobre sus mensajes a través de una representación gráfica."

![](assets/journey_sms_performance.png)

El **[!UICONTROL SMS: rendimiento por fecha]** El widget ofrece una descripción detallada de la información clave relacionada con los mensajes, presentada a través de un gráfico, que proporciona perspectivas sobre las tendencias de rendimiento en períodos de tiempo específicos.

+++ Más información sobre SMS: rendimiento por métricas de fecha

* **[!UICONTROL Enviado]**: Número total de mensajes SMS enviados para el recorrido

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes SMS enviados.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante el proceso de envío y que impiden su envío a los perfiles.

+++

### SMS: motivos de rechazos {#sms-bounce}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_bounces_reasons"
>title="SMS: motivos de rechazos"
>abstract="Los gráficos y la tabla Motivos de rechazos contienen los datos disponibles relacionados con los mensajes rechazados."

![](assets/journey_sms_bounce_reasons.png)

El **[!UICONTROL Razones de rechazos]** Los gráficos y la tabla proporcionan una visión general completa de los datos relacionados con los mensajes SMS rechazados, lo que ofrece una valiosa perspectiva de las razones específicas detrás de las instancias de rechazos de mensajes SMS.

### SMS: motivos de error {#sms-error}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_error_reasons"
>title="SMS: motivos de error"
>abstract="SMS: los gráficos y la tabla Motivos de error le permiten identificar los errores específicos que se produjeron durante el proceso de envío."

![](assets/journey_sms_error.png)

El **[!UICONTROL Motivos del error]** Los gráficos y las tablas le permiten identificar los errores específicos que se produjeron durante el proceso de envío de sus mensajes SMS, lo que facilita un análisis exhaustivo de cualquier problema encontrado.

### SMS: motivos excluidos {#sms-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_excluded_reasons"
>title="SMS: motivos excluidos"
>abstract="Los gráficos y la tabla Motivos excluidos ilustran los distintos factores que llevaron a que los perfiles de usuario, excluidos del público destinatario, no recibieran el mensaje."

![](assets/journey_sms_excluded.png)

El **[!UICONTROL Razones de exclusión]** Los gráficos y tablas muestran visualmente los diversos factores que llevaron a la exclusión de perfiles de usuario de la audiencia de destino, lo que les impidió recibir sus mensajes SMS.

Consulte [esta página](exclusion-list.md) para obtener la lista completa de motivos de exclusión.

### SMS: clics por vínculos {#sms-clicks}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_clicks"
>title="SMS: clics por vínculos"
>abstract="El widget SMS: clics por vínculos proporciona una información esencial sobre la participación de los visitantes con las direcciones URL de los mensajes."

![](assets/journey_sms_clicks.png)

El **[!UICONTROL SMS: clics por vínculos]** El widget ofrece una información esencial sobre la participación de los visitantes con las direcciones URL incluidas en los mensajes, lo que proporciona información valiosa sobre los vínculos que atraen más interacción.

## Pestaña en la aplicación {#in-app-global}

De tu Recorrido **[!UICONTROL Informe global]**, el **[!UICONTROL En la aplicación]** Esta pestaña detalla la información principal relativa a los mensajes en la aplicación enviados en los recorridos.

### Rendimiento en la aplicación {#inapp-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_performance"
>title="Rendimiento en la aplicación"
>abstract="Los KPI de rendimiento en la aplicación proporcionan información esencial sobre la participación de los visitantes en los mensajes de la aplicación."

![](assets/journey_inapp_performance.png)

El **[!UICONTROL Rendimiento en la aplicación]** Los KPI proporcionan una perspectiva esencial de la participación de sus perfiles con los mensajes en la aplicación, lo que proporciona métricas esenciales para valorar la eficacia y el impacto de los mensajes en la aplicación incluidos en su recorrido.

+++ Más información sobre las Métricas en la aplicación: rendimiento por fecha

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
+++

### Resumen de la aplicación {#inapp-summary}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_summary"
>title="Resumen de la aplicación"
>abstract="El gráfico de resumen de la aplicación ilustra la progresión de las impresiones e interacciones de la aplicación durante el período especificado."

![](assets/journey_inapp_summary.png)

El **[!UICONTROL Resumen en la aplicación]** Este gráfico ilustra la progresión de las impresiones e interacciones en la aplicación durante el periodo especificado, lo que proporciona una visión general del rendimiento de los mensajes en la aplicación.

### Interacciones por tipo {#interactions-type}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_interactions"
>title="Interacciones por tipo"
>abstract="La tabla Interacciones por tipo detalla la interacción de los usuarios con el mensaje de la aplicación mediante el seguimiento de cualquier clic, rechazo o interacción."

![](assets/journey_inapp_interactions.png)

El **[!UICONTROL Interacciones por tipo]** Los gráficos y las tablas proporcionan una descripción detallada de cómo los perfiles interactuaron con el mensaje en la aplicación, el seguimiento de acciones como clics, rechazos o cualquier otra forma de participación.
