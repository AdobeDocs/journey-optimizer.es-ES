---
solution: Journey Optimizer
product: journey optimizer
title: Acceso y suscripción a alertas del sistema
description: Obtenga información sobre cómo acceder, suscribirse y administrar alertas del sistema en Adobe Journey Optimizer. Monitorice el rendimiento de la recorrido, los errores de acciones personalizadas, los problemas de perfil y la capacidad de envío de correo electrónico con notificaciones de alertas proactivas.
feature: Journeys, Alerts, Monitoring
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 455e462078cffd43f1654278e0478951e78717b2
workflow-type: tm+mt
source-wordcount: '2638'
ht-degree: 1%

---

# Acceso y suscripción a alertas del sistema {#alerts}

## Información general

Las alertas son notificaciones automatizadas que le ayudan a supervisar y solucionar problemas en Adobe Journey Optimizer. Permiten conocer en tiempo real los posibles problemas de los recorridos, las campañas y las configuraciones de canal, lo que permite tomar medidas correctivas antes de que las experiencias de los clientes se vean afectadas.

Adobe Journey Optimizer proporciona dos tipos de alertas:

* **Alertas de validación en lienzo**: al crear recorridos y campañas, use el botón **Alertas** del lienzo para identificar y resolver los errores de configuración antes de publicar. Aprenda a [solucionar problemas de sus recorridos](../building-journeys/troubleshooting.md) y a revisar sus campañas: [Campañas de acción](../campaigns/review-activate-campaign.md) | [Campañas activadas por API](../campaigns/review-activate-api-triggered-campaign.md) | [Campañas organizadas](../orchestrated/start-monitor-campaigns.md).

* **Alertas de monitorización del sistema** (detalladas en esta página): Reciba notificaciones dinámicas cuando se excedan los umbrales operativos o se detecten problemas en las configuraciones de canal y recorridos activos. Las alertas del sistema supervisan métricas como tasas de error, descartes de perfil y problemas de envío de correo electrónico.

**Ventajas principales de las alertas del sistema:**

* Detección proactiva de problemas antes del impacto en el cliente
* Supervisión automatizada del rendimiento y el estado del recorrido
* Advertencia temprana de problemas de envío de correo electrónico
* Menor tiempo para identificar y resolver problemas operativos

Las alertas del sistema están disponibles en el menú **[!UICONTROL Alertas]** en **[!UICONTROL Administración]**. Adobe Experience Platform proporciona varias reglas de alerta predefinidas que puede habilitar, incluidas las alertas específicas de [!DNL Adobe Journey Optimizer] para recorridos y configuraciones de canal.

## Requisitos previos

Antes de trabajar con alertas:

* **Permisos**: Necesita permisos específicos para ver y administrar alertas. Ver [permisos requeridos en Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html#permissions){target="_blank"}.

* **Reconocimiento de zona protegida**: Las suscripciones de alerta son específicas de la zona protegida. Al suscribirse a las alertas, solo se aplican a la zona protegida actual. Cuando se restablece una zona protegida, también se restablecen todas las suscripciones de alerta.

* **Preferencias de notificación**: configure la forma en que recibe las alertas (correo electrónico o en la aplicación) en sus [Preferencias de Adobe Experience Cloud](../start/user-interface.md#in-product-uc).

>[!NOTE]
>
>Las alertas específicas de Journey Optimizer solo se aplican a **recorridos activos**. Las alertas no se activan para los recorridos en el modo de prueba. Para obtener más información acerca del marco de alertas, consulte la [documentación de alertas de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=es){target="_blank"}.

## Alertas disponibles en Journey Optimizer {#available-alerts}

Journey Optimizer proporciona reglas de alerta preconfiguradas que supervisan aspectos específicos de los recorridos y las configuraciones de canal. No es necesario que cree estas alertas: están disponibles de forma predeterminada y se pueden activar mediante suscripción.

**Para tener acceso a la lista de alertas:**

Vaya a **[!UICONTROL Administración]** > **[!UICONTROL Alertas]** en el menú de la izquierda. La pestaña **Examinar** muestra todas las alertas preconfiguradas disponibles para Journey Optimizer.

![](assets/updated-alerts-list.png){width=50%}

### Categorías de alerta

Journey Optimizer proporciona dos categorías de alertas del sistema:

>[!BEGINTABS]

>[!TAB alertas de Recorrido]

Monitorice la ejecución y el rendimiento del recorrido:

* [Déclencheur de lectura de audiencia incorrecto](#alert-read-audiences): advierte cuando una actividad de lectura de audiencia no procesa los perfiles
* [Tasa de error de acción personalizada superada](#alert-custom-action-error-rate) - Detecta tasas de error altas en las llamadas a la API de acción personalizada (reemplaza la alerta de error de acción personalizada de Recorrido anterior)
* [Tasa de descarte de perfil superada](#alert-discard-rate): identifica cuándo se descartan los perfiles a una tasa anormal
* [Tasa de error de perfil superada](#alert-profile-error-rate) - Indica cuándo los perfiles encuentran errores durante la ejecución del recorrido
* [Recorrido publicado](#alert-journey-published): notificación informativa cuando se publica un recorrido
* [Recorrido finalizado](#alert-journey-finished) - Notificación informativa cuando finaliza un recorrido
* [Límite de acción personalizada activado](#alert-custom-action-capping): notifica cuando se alcanzan los límites de llamadas de API

>[!TAB Alertas de configuración de canal]

Detectar problemas con la configuración de envío de correo electrónico:

* [Falta el registro DNS del dominio de AJO](#alert-dns-record-missing) - Identifica registros DNS que faltan o que no están configurados
* [Error de configuración de canal de AJO](#alert-channel-config-failure): detecta problemas de configuración de correo electrónico (registros SPF, DKIM, MX)
  <!--* the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

>[!ENDTABS]

>[!NOTE]
>
>Para obtener alertas de otros servicios de Adobe Experience Platform (ingesta de datos, resolución de identidades, segmentación, etc.), consulte la [documentación de reglas de alerta estándar](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/rules.html){target="_blank"}.

## Suscribirse a alertas {#subscribe-alerts}

Las suscripciones de alerta determinan qué usuarios reciben notificaciones cuando se cumplen condiciones específicas (como umbrales de tasa de error que se superan o problemas de configuración detectados). Solo los usuarios suscritos reciben notificaciones de alerta para las alertas seleccionadas.

### Métodos de suscripción

Puede suscribirse a las alertas de dos formas:

* **[Suscripción global](#global-subscription)**: se aplica a todos los recorridos y campañas de la zona protegida actual. Utilice este método cuando desee monitorizar toda la actividad del recorrido en su organización.
* **[suscripción específica del Recorrido](#unitary-subscription)**: se aplica solo a recorridos individuales. Utilice este método cuando desee supervisar recorridos de prioridad alta específicos sin recibir alertas para todos los recorridos.

### Funcionamiento de las notificaciones de alerta

**Ciclo de vida de la alerta:**

1. **Activación**: La alerta déclencheur cuando se cumple su condición específica (por ejemplo, la tasa de error supera el 20%)
2. **Notificación**: todos los usuarios suscritos reciben notificaciones a través de los canales configurados
3. **Supervisión**: la alerta continúa supervisando la condición a intervalos regulares
4. **Resolución**: cuando se resuelve la condición, los suscriptores reciben una notificación &quot;Resuelta&quot;

**Envío de notificación:**

* **Canales de envío**: las alertas se envían por correo electrónico o a través de notificaciones desde la aplicación en el centro de notificaciones de Journey Optimizer (icono de campana en la esquina superior derecha). Configure sus canales de envío preferidos en [Preferencias de Adobe Experience Cloud](../start/user-interface.md#in-product-uc).

* **Tipos de alerta**: Journey Optimizer proporciona alertas únicas (eventos informativos como &quot;recorrido publicado&quot;) y repetidas (umbrales de supervisión). Las alertas repetidas siguen evaluando y notificando hasta que se resuelva la condición.

* **Resolución automática**: Para evitar que la fatiga de notificaciones fluctúe en los valores, las alertas se resuelven automáticamente después de 1 hora, incluso si la condición persiste. Esto evita notificaciones continuas cuando las métricas giran alrededor de los valores de umbral.

**Método de suscripción alternativo:**

Para integraciones avanzadas, puede suscribirse a través de Eventos de E/S para enviar alertas a sistemas externos. Consulte la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}.


### Suscripción global {#global-subscription}

Las suscripciones globales le permiten recibir alertas de todos los recorridos y campañas de la zona protegida actual.

**Para suscribirse a una alerta:**

1. Vaya a **[!UICONTROL Administración]** > **[!UICONTROL Alertas]** en el menú de la izquierda.

1. En la ficha **[!UICONTROL Examinar]**, busque la alerta que desee supervisar.

1. Haga clic en **[!UICONTROL Suscribirse]** para obtener la alerta deseada.

   ![Suscribiéndose a una alerta](assets/alert-subscribe.png){width=80%}

**Para cancelar la suscripción:**

Haga clic en **[!UICONTROL Cancelar la suscripción]** junto a la alerta.

>[!IMPORTANT]
>
>Las suscripciones de alerta son específicas de la zona protegida. Debe suscribirse a las alertas por separado en cada zona protegida en la que desee recibir notificaciones.

**Método de suscripción alternativo:**

También puede suscribirse a través de [notificaciones de eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}, lo que permite la integración con sistemas externos. Los nombres de suscripción de eventos para las alertas de Journey Optimizer se enumeran en cada [descripción de alerta a continuación](#journey-alerts).

### suscripción específica de recorrido {#unitary-subscription}

Las suscripciones específicas a recorridos le permiten supervisar recorridos individuales de alta prioridad sin recibir alertas de todos los recorridos de su organización.

**Para suscribirse a las alertas de un recorrido específico:**

1. Vaya al inventario de recorrido.

1. Haga clic en el menú **⋯** (más acciones) del recorrido que desee supervisar.

1. Seleccione **[!UICONTROL Suscribirse a alertas]**.

   ![Suscripción a una alerta para un recorrido específico](assets/subscribe-journey-alert.png){width=75%}

1. Seleccione las alertas que desee activar entre las opciones disponibles:
   * [Tasa de descartes de perfil superada](#alert-discard-rate)
   * [Tasa de errores de acción personalizada superada](#alert-custom-action-error-rate)
   * [Tasa de errores de perfil superada](#alert-profile-error-rate)
   * [Recorrido publicado](#alert-journey-published)
   * [Recorrido finalizado](#alert-journey-finished)
   * [Límite de acción personalizado activado](#alert-custom-action-capping)

1. Haz clic en **[!UICONTROL Guardar]** para confirmar tus suscripciones.

**Para cancelar la suscripción:**

Abra el mismo cuadro de diálogo, deseleccione las alertas y haga clic en **[!UICONTROL Guardar]**.

>[!NOTE]
>
>La alerta [Leer Déclencheur de audiencias no se ha realizado correctamente](#alert-read-audiences) solo está disponible a través de una suscripción global, no de una suscripción por recorrido.

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.-->

## alertas de recorrido {#journey-alerts}


A continuación se enumeran todas las notificaciones de recorrido disponibles en la interfaz de usuario de.

>[!CAUTION]
>
>Las alertas específicas de Adobe Journey Optimizer solo se aplican a **recorridos activos**. Las alertas no se activan para los recorridos en el modo de prueba.

### Error al leer Déclencheur de audiencia {#alert-read-audiences}

Esta alerta le advierte si una actividad **Leer audiencia** no ha procesado ningún perfil 10 minutos después de la hora programada de ejecución. Este error puede deberse a problemas técnicos o a que la audiencia está vacía. Si este error se debe a problemas técnicos, tenga en cuenta que aún pueden producirse reintentos, según el tipo de problema (p. ej.: si la creación del trabajo de exportación ha fallado, lo volveremos a intentar cada 10 minutos durante 1 h como máximo).

Las alertas de las actividades **Leer audiencia** solo se aplican a los recorridos recurrentes. Se omiten las actividades de **Leer audiencia** en recorridos activos que tienen una programación para ejecutarse **Una vez** o **Lo antes posible**.

Las alertas de **Leer audiencia** se resuelven cuando un perfil entra en el nodo **Leer audiencia** o después de 1 hora.

El nombre de suscripción de evento de E/S correspondiente a la alerta **Leer Déclencheur de audiencias erróneo** es **Recorrido de retrasos, errores y errores de lectura de audiencia**.

Para solucionar problemas de las alertas de **Leer audiencia**, compruebe su recuento de audiencias en la interfaz de Experience Platform.

### Tasa de descartes de perfil superada {#alert-discard-rate}

Esta alerta le advierte si la proporción de descartes de perfiles respecto a los perfiles introducidos durante los últimos 5 minutos ha superado el umbral. El umbral predeterminado está establecido en 20%, pero puede [definir un umbral personalizado](#custom-threshold).

Haga clic en el nombre de la alerta para comprobar sus detalles y configuración.

![](assets/profile-discard-alert.png)

Existen varias razones por las que se puede descartar un perfil, lo que informará al método de resolución de problemas. A continuación se enumeran algunas razones comunes:

* Perfil descartado en la entrada porque ya está activo en ese recorrido unitario. Para resolver esto, asegúrese de que el perfil tenga tiempo suficiente para salir del recorrido antes de que llegue el siguiente evento para ese perfil.
* La identidad no se define para el perfil o el área de nombres que utiliza el recorrido de audiencia de lectura no se utiliza en ese perfil. Para resolver esto, asegúrese de que el área de nombres de la recorrido coincida con el área de nombres de identidad utilizado por los perfiles.
* Se ha superado la tasa de rendimiento de eventos. Para resolver esto, asegúrese de que los eventos que llegan al sistema no superan estos límites.


### Tasa de errores de acción personalizada superada {#alert-custom-action-error-rate}

Esta alerta le advierte si la proporción de errores de acción personalizada respecto a llamadas HTTP correctas durante los últimos 5 minutos ha superado el umbral. El umbral predeterminado está establecido en 20%, pero puede [definir un umbral personalizado](#custom-threshold).

>[!NOTE]
>
>Esta alerta reemplaza la alerta **Error de acción personalizada de Recorrido** anterior.

Haga clic en el nombre de la alerta para comprobar sus detalles y configuración.

Los errores de acciones personalizadas pueden ocurrir por varios motivos. Para solucionar estos errores, puede:

* Comprueba tu acción personalizada usando [modo de prueba](../building-journeys/testing-the-journey.md) en otro recorrido.
* Consulte su [informe de recorridos](../reports/journey-live-report.md) para ver los motivos de error al realizar la acción.
* Compruebe los stepEvents de recorrido para buscar más información sobre &quot;failureReason&quot;.
* Compruebe que la acción personalizada esté configurada correctamente y valide que la autenticación sigue siendo válida. Realice una comprobación manual con Postman, por ejemplo.
* Compruebe que el punto de conexión sea accesible y que la acción personalizada pueda llegar a él a través del comprobador de conectividad de acción personalizada.
* Compruebe las credenciales de autenticación, la conectividad a Internet, etc.

### Tasa de errores de perfil superada {#alert-profile-error-rate}

Esta alerta le advierte si la proporción de perfiles en error respecto a los perfiles introducidos durante los últimos 5 minutos ha superado el umbral. El umbral predeterminado está establecido en 20%, pero puede [definir un umbral personalizado](#custom-threshold).

Haga clic en el nombre de la alerta para comprobar sus detalles y configuración.

Para solucionar errores de perfil, puede consultar los datos en eventos de paso para comprender dónde y por qué falló el perfil en la recorrido.

### Recorrido publicado {#alert-journey-published}

Esta alerta le avisa cuando un profesional ha publicado un recorrido en el lienzo del recorrido.

Se trata de una alerta informativa que le ayuda a realizar un seguimiento de los eventos del ciclo vital de recorrido en su organización. No hay criterios de resolución, ya que se trata de una notificación única.

### Recorrido finalizado {#alert-journey-finished}

Esta alerta le avisa cuando ha finalizado un recorrido. La definición de &quot;terminado&quot; varía según el tipo de recorrido. [Obtenga más información sobre cuándo se considera que han finalizado los recorridos](../building-journeys/end-journey.md#journey-finished-definition).

Esta es una alerta informativa que le ayuda a realizar un seguimiento de la finalización del recorrido. No hay criterios de resolución, ya que se trata de una notificación única.

### Límite de acción personalizado activado {#alert-custom-action-capping}

Esta alerta le avisa cuando se ha activado el límite de una acción personalizada. El límite se utiliza para limitar el número de llamadas enviadas a un extremo externo para evitar saturar el extremo.

Haga clic en el nombre de la alerta para comprobar sus detalles y configuración.

Cuando se activa el límite, significa que se ha alcanzado el número máximo de llamadas de API en el período de tiempo definido y que se están restringiendo o poniendo en cola más llamadas. Obtenga más información sobre cómo limitar las acciones personalizadas en [esta página](../action/about-custom-action-configuration.md#custom-action-enhancements-best-practices).

Esta alerta se resuelve cuando el límite ya no está activo o cuando ningún perfil alcanza la acción personalizada durante el período de evaluación.

Para solucionar problemas de límite:

* Revise la configuración de límite de la acción personalizada para asegurarse de que los límites sean adecuados para su caso de uso.
* Compruebe si el volumen de llamadas de API es mayor de lo esperado y considere la posibilidad de ajustar el diseño del recorrido o la configuración del límite.
* Supervise el extremo externo para asegurarse de que puede gestionar la carga esperada.

## Alertas de configuración {#configuration-alerts}

A continuación, se enumeran las alertas de monitorización de configuración de canal disponibles en la interfaz de usuario.

### Falta el registro DNS del dominio de AJO {#alert-dns-record-missing}

Esta alerta le notifica cuando faltan o no se han configurado correctamente los registros DNS críticos (NS o CNAME) necesarios para la correcta configuración de la entrega. Sin estos registros, la capacidad de envío del correo electrónico puede verse comprometida.

>[!NOTE]
>
>* Los registros NS son esenciales para la delegación completa de subdominios a Adobe. [Más información](../configuration/about-subdomain-delegation.md#full-subdomain-delegation)
>
>* Los registros CNAME admiten la configuración del subdominio CNAME. [Más información](../configuration/about-subdomain-delegation.md#cname-subdomain-setup)

La alerta **Falta el registro DNS del dominio de AJO** cuando el sistema detecta que los registros NS o CNAME necesarios están ausentes o no coinciden con los estándares de configuración.

1. Haga clic en la alerta para que se le dirija al [subdominio](../configuration/delegate-subdomain.md) afectado en la interfaz [!DNL Journey Optimizer].

   <!--For guidance on editing delegated subdomains, see [this section](../configuration/delegate-subdomain.md).-->

1. Corrija la configuración de DNS estableciendo los registros correctamente y [vuelva a enviar la delegación del subdominio](../configuration/delegate-subdomain.md#submit-subdomain).

   >[!NOTE]
   >
   >Asegúrese de que todos los registros se hayan creado correctamente en la solución de alojamiento de dominios antes de continuar.

1. Si no está seguro de los valores correctos, puede crear un nuevo subdominio en [!DNL Journey Optimizer] con el mismo nombre que el subdominio afectado. [Aprenda a configurar un nuevo subdominio](../configuration/delegate-subdomain.md#set-up-subdomain)

Si los cambios no resuelven el problema, la misma alerta se activará de nuevo al día siguiente.

<!--The I/O event subscription name corresponding to this alert is xx. > Do we need to mention this?-->

### Error de configuración de canal de AJO {#alert-channel-config-failure}

>[!IMPORTANT]
>
>Esta alerta solo se aplica a las configuraciones de canal **email** que usan el tipo de delegación [subdominio personalizado](../configuration/delegate-custom-subdomain.md). <!--Other channel types (such as SMS, push, or in-app) are not covered by this alert.-->

Esta alerta se activa en caso de que la auditoría del sistema detecte problemas de configuración de canales de correo electrónico. Estos problemas pueden incluir configuraciones de canal mal configuradas, configuración de DNS no válida, problema de lista de supresión, incoherencia de IP o cualquier otro error que pueda afectar a la entrega de correo electrónico.

Si recibe una alerta de este tipo, los pasos de resolución se enumeran a continuación:

1. Haga clic en la alerta para que se le dirija a la [configuración del canal de correo electrónico](../email/get-started-email-config.md) afectada en la interfaz [!DNL Journey Optimizer].

   Para obtener instrucciones sobre cómo editar configuraciones de canal, consulte [esta sección](../configuration/channel-surfaces.md#edit-channel-surface).

1. Revise los detalles de configuración y los mensajes de error proporcionados. Las razones comunes de error incluyen:

   * Error de validación de SPF
   * Error de validación de DKIM
   * Error de validación de registro MX
   * Registros DNS no válidos

   >[!NOTE]
   >
   >Los posibles motivos del error de configuración se enumeran en [esta sección](../configuration/channel-surfaces.md).

1. Resuelva el problema:

   * Actualice la configuración del canal según sea necesario.
   * Es posible que tenga que corregir problemas específicos de DNS mencionados en la alerta.

   >[!NOTE]
   >
   >Como un solo dominio se puede asociar con varias configuraciones de canal, la resolución de problemas de DNS para una configuración de canal puede corregir automáticamente los problemas relacionados en varias configuraciones.

Si el cambio no resuelve el problema, la misma alerta se activará de nuevo al día siguiente.

Cuando resuelva problemas de configuración de correo electrónico, tenga en cuenta las prácticas recomendadas que se enumeran a continuación:

* Actuar con rapidez: solucione los errores de configuración en cuanto se detecten para evitar interrupciones en la entrega de correos electrónicos.
* Comprobar todas las configuraciones: si la alerta indica varias configuraciones de correo electrónico afectadas, revise y corrija cada una de ellas.

<!--### AJO domain certificates renewal unsuccessful {#alert-certificates-renewal}

This alert warns you if a domain certificate (CDN, tracking URL) renewal failed for a specific Journey Optimizer subdomain.-->

## Administración de alertas {#manage-alerts}

### Editar una alerta

Puede comprobar los detalles de una alerta haciendo clic en su línea. Los canales de nombre, estado y notificación se muestran en el panel izquierdo.
Para las alertas de Recorrido, usa el botón **[!UICONTROL Más acciones]** para editarlas. A continuación, puede definir un [umbral personalizado](#custom-threshold) para estas alertas.

![](assets/alert-more-actions.png){width=60%}

### Definición de un umbral personalizado {#custom-threshold}

Puede establecer umbrales para [Recorrido alerts](#journey-alerts). El umbral de alertas por encima del valor predeterminado es del 20 %.

Para cambiar el umbral:

1. Vaya a la pantalla **Alertas**
1. Haga clic en el botón **[!UICONTROL Más acciones]** de la alerta para actualizar
1. Introduzca el nuevo umbral y confirme. El nuevo umbral se aplica a **todos** los recorridos


![](assets/alert-threshold.png){width=60%}

>[!CAUTION]
>
>Los niveles de umbral son globales en todos los recorridos y no se pueden modificar individualmente por recorrido.

### Desactivación de una alerta

De forma predeterminada, todas las alertas están habilitadas. Para deshabilitar una alerta, seleccione la opción **[!UICONTROL Deshabilitar alerta]**: todos los suscriptores de esta alerta dejarán de recibir las notificaciones relacionadas.


### Estados de alerta

Los posibles estados de alerta se enumeran a continuación:

* **[!UICONTROL Habilitada]**: la alerta está habilitada y actualmente supervisa la condición de déclencheur.
* **[!UICONTROL Deshabilitada]**: la alerta está deshabilitada y actualmente no supervisa la condición de déclencheur. No recibirá notificaciones para esta alerta.
* **[!UICONTROL Activada]**: actualmente se cumple la condición de déclencheur de la alerta.


### Ver y actualizar suscriptores {#manage-subscribers}

Seleccione **[!UICONTROL Administrar suscriptores de alertas]** para ver la lista de usuarios que se suscribieron a la alerta.

![](assets/alert-subscribers.png){width=80%}

Para agregar a más suscriptores, escribe su correo electrónico separados por una coma y selecciona **[!UICONTROL Actualizar]**.

Para quitar suscriptores, elimina su dirección de correo electrónico de los suscriptores actuales y selecciona **[!UICONTROL Actualizar]**.

## Temas relacionados {#additional-resources-alerts}

**administración de Recorridos y campañas:**

* [Solucionar problemas de recorridos](../building-journeys/troubleshooting.md) - Resolver problemas y errores comunes de recorridos
* [Revisar y activar campañas](../campaigns/review-activate-campaign.md): validación de campañas previas a la publicación

**Marco de alertas:**

* [Información general sobre alertas de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=es): Descripción del marco de alertas
* [Suscribirse a alertas mediante eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html) - Opciones de integración avanzadas
