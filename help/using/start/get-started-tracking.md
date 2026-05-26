---
solution: Journey Optimizer
product: journey optimizer
title: Introducción al seguimiento en Journey Optimizer
description: Obtenga información sobre las funciones de seguimiento y monitorización disponibles en Journey Optimizer
feature: Monitoring
topic: Administration
role: User
level: Beginner
keywords: seguimiento, monitorización, análisis, sistema de informes, capacidad de entrega
exl-id: d5e7adb7-8473-4c29-8ae6-ba979aef97f3
TQID: https://experienceleague.adobe.com/jLHTNJlUPQm39EZvTLLBvYT92eGlCBoHpTKBfJ1Zxlk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe338112-e2ce-4876-8989-fc4d497613f1id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: cfba2953-2ce9-4b00-a00c-71cd338ae63fid: e30b0a1a-b594-47b8-af94-1e3a2be6df11id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c1579802-ddd4-4214-8a91-97b2066abe11id: c4147b6e-073b-4d3c-9ab1-d60f2f4434efid: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ebb3a1face3a72a52ec365c519ac2686c97ad187
workflow-type: tm+mt
source-wordcount: 1964
ht-degree: 3%

---

# Introducción al seguimiento en Journey Optimizer {#get-started-tracking}

El seguimiento le permite medir la eficacia de las campañas, optimizar las experiencias de los clientes y garantizar que los mensajes lleguen a los destinatarios deseados. Journey Optimizer proporciona funciones de seguimiento completas que capturan las interacciones de los clientes, el rendimiento de la entrega y el estado del sistema, lo que le ayuda a tomar decisiones basadas en datos respetando la privacidad y manteniendo el cumplimiento.

La mayoría del seguimiento se configura automáticamente al crear mensajes y recorridos. En los casos avanzados, puede configurar métricas personalizadas, configurar parámetros de URL e integrarlos con plataformas de análisis externas. Acceda a los datos de seguimiento a través de informes integrados o exporte los datos para un análisis más profundo en Customer Journey Analytics.

>[!BEGINSHADEBOX]

Qué se puede rastrear en Journey Optimizer:

📧 **Interacciones por correo electrónico**: aperturas, clics y rendimiento de vínculos

🌐 **Comportamiento web**: vistas de página, clics y patrones de participación

🛤️ **rendimiento de Recorrido**: métricas personalizadas, eventos de paso y rutas de conversión

📊 **Estado de la entrega**: tasas de devolución, quejas de spam y reputación del remitente

⚙️ **Operaciones del sistema**: alertas, errores y rendimiento de acciones personalizadas

>[!ENDSHADEBOX]

Para empezar, explore estos temas esenciales de seguimiento y monitorización:

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="../building-journeys/success-metrics.md">
    <img alt="Métricas" src="../assets/do-not-localize/success-metrics.jpeg">
    </a>
    <div>
    <a href="../building-journeys/success-metrics.md"><strong>Configurar métricas de éxito</strong></a>
    </div>
    <p>
    <em>Rastrear KPI personalizados alineados con sus objetivos empresariales</em>
    <p>
  </td>
  <td>
    <a href="../reports/deliverability.md">
    <img alt="Entregabilidad" src="../assets/do-not-localize/deliverability.jpeg">
    </a>
    <div>
    <a href="../reports/deliverability.md"><strong>Supervisar la entrega</strong></a>
    </div>
    <p>
    <em>Asegúrese de que los mensajes lleguen a las bandejas de entrada de los clientes</em>
    <p>
  </td>
  <td>
    <a href="../reports/gs-reports.md">
    <img alt="Creación de informes" src="../assets/do-not-localize/reporting.jpeg">
    </a>
    <div>
    <a href="../reports/gs-reports.md"><strong>Explorar informes</strong></a>
    </div>
    <p>
    <em>Acceda a informes en vivo e históricos de sus recorridos y campañas</em>
    <p>
  </td>
</tr>
</table>

## Seguimiento de interacciones de clientes entre canales {#tracking-by-channel}

Journey Optimizer proporciona funciones de seguimiento específicas del canal. A continuación, se muestra cómo configurar y utilizar el seguimiento para cada canal.

+++Seguimiento de correo electrónico

El seguimiento de correo electrónico se activa automáticamente al crear un mensaje de correo electrónico. Journey Optimizer realiza un seguimiento de las aperturas, los clics y las bajas de suscripción de forma predeterminada, no se necesita ninguna configuración adicional.

**Configurar opciones de seguimiento:**

* **Habilitar/deshabilitar seguimiento**: controle el seguimiento en el nivel de mensaje al diseñar el correo electrónico. Puede elegir rastrear aperturas, clics o ambos. [Más información](../email/message-tracking.md)

* **Configurar parámetros de seguimiento de URL**: configure parámetros de seguimiento en el nivel de superficie para anexar automáticamente identificadores de campaña (utm_campaign, utm_source, etc.) a todos los vínculos de correo electrónico. Esto permite el seguimiento de la atribución en todo el ecosistema digital. [Más información](../email/url-tracking.md)

* **Rastrear vínculos en fragmentos guardados**: cuando guarda un fragmento a partir de contenido que tiene habilitado el seguimiento, los vínculos de ese fragmento permanecen rastreados cuando se reutiliza en otros recorridos o campañas. [Más información](../content-management/save-fragments.md)

* **Agregar seguimiento de página espejo**: habilita la opción de página espejo para crear una versión web del correo electrónico con seguimiento automático de quién lo ve. [Más información](../email/message-tracking.md#mirror-page)

**Supervisar el rendimiento:** Ver métricas en tiempo real en informes de campañas e recorridos, incluidos aperturas, clics y rendimiento a nivel de vínculo. [Informes de campaña](../reports/campaign-global-report-cja-email.md) | [Informes de Recorrido](../reports/journey-global-report-cja-email.md)

+++

+++Seguimiento web

El seguimiento web requiere una configuración explícita para rastrear las interacciones del usuario con las modificaciones web.

**Configurar el rastreo de clics:**

Al crear una página web, puede seleccionar los elementos específicos (botones, imágenes, vínculos) que desea rastrear. Esto habilita el rastreo de clics para esos elementos sin requerir código adicional. [Más información](../web/monitor-web-experiences.md)

* **Rastrear cualquier elemento en el que se pueda hacer clic**: seleccione botones, imágenes, vínculos o cualquier elemento interactivo en la personalización web.
* **Recopilación automática de datos**: una vez configurada, Journey Optimizer captura automáticamente los eventos de clic y los asocia a perfiles.
* **Supervisar en tiempo real**: efectúe el seguimiento de las interacciones de los usuarios a medida que vayan surgiendo para validar la eficacia de la personalización.

**Ver datos de seguimiento:** Acceda a métricas de visualización, tasas de pulsaciones y rendimiento de nivel de elemento en los informes. [Informes de campaña](../reports/campaign-global-report-cja-web.md) | [Informes de Recorrido](../reports/journey-global-report-cja-web.md)

+++

+++Seguimiento de notificaciones push

El seguimiento push se activa automáticamente y captura impresiones (entregadas), clics (pulsados) y aperturas (aplicación iniciada). Para maximizar el valor de seguimiento, configure los elementos en los que se puede hacer clic en el contenido push.

**Configurar elementos rastreados:**

* **Comportamiento al hacer clic en el cuerpo**: configure lo que sucede cuando los usuarios tocan la notificación: abrir la aplicación, navegar a un vínculo profundo o abrir una URL web. Cada acción se rastrea automáticamente. [Más información](../push/design-push.md#on-click-behavior)

* **Añadir botones de acción**: incluye hasta 3 botones (Android) o varios botones (iOS) con seguimiento independiente para cada acción de botón (abrir aplicación, vínculo profundo, URL web). [Más información](../push/design-push.md#add-buttons-push)

* **Habilitar seguimiento**: compruebe que el seguimiento esté habilitado en la configuración de la actividad del recorrido push o del seguimiento de campaña. [Más información](../push/create-push.md#create)

>[!NOTE]
>
>El seguimiento push requiere una implementación móvil de SDK. Asegúrese de que la aplicación tenga Adobe Experience Platform Mobile SDK correctamente configurado. [Más información](../push/push-configuration.md#integrate-mobile-app)

**Analizar la participación:** Ver las tasas de pulsaciones, el rendimiento de los botones y los detalles de vínculos rastreados en los informes. [Informes de campaña](../reports/campaign-global-report-cja-push.md) | [Informes de Recorrido](../reports/journey-global-report-cja-push.md)

+++

+++Seguimiento de mensajes en la aplicación

Los mensajes en la aplicación rastrean automáticamente las visualizaciones y las interacciones del usuario. Configure los déclencheur y el contenido para maximizar la eficacia del seguimiento.

**Configurar el seguimiento:**

* **Definir reglas de visualización**: configure cuándo y dónde aparecerán los mensajes en la aplicación mediante déclencheur (inicio de la aplicación, carga de pantalla), reglas de frecuencia y condiciones de audiencia. Una configuración adecuada garantiza un seguimiento preciso de los mensajes activados y mostrados.

* **Agregar elementos rastreados**: incluya botones, vínculos y elementos interactivos en el contenido del mensaje. Cada interacción se rastrea automáticamente con etiquetas detalladas.

* **Optimizar el tiempo de visualización**: configure las reglas de día de la semana y de la hora del día para maximizar la probabilidad de que los mensajes activados se muestren a los usuarios.

[Obtenga información sobre cómo configurar mensajes en la aplicación](../in-app/create-in-app.md)

**Lo que se rastrea:** Journey Optimizer captura automáticamente las pantallas, los clics en botones, los rechazos, las métricas activadas frente a las mostradas y el rendimiento de los vínculos. [Informes de campaña](../reports/campaign-global-report-cja-inapp.md) | [Informes de Recorrido](../reports/journey-global-report-cja-inapp.md)

+++

+++Seguimiento de SMS y MMS

El seguimiento de SMS requiere una configuración mínima: Journey Optimizer acorta y rastrea automáticamente los vínculos que incluye en los mensajes.

**Cómo funciona:**

* **Seguimiento automático de vínculos** - Agregue cualquier dirección URL al contenido del SMS mediante la función de ayuda de URL. Journey Optimizer acorta automáticamente el vínculo y rastrea los clics sin necesidad de configuración adicional. Para utilizar el acortamiento de URL, primero debe configurar un subdominio SMS. [Más información](../mobile/mobile-subdomains.md)

* **Seguimiento de mensajes entrantes**: las respuestas de los destinatarios se capturan automáticamente, lo que le permite supervisar las conversaciones bidireccionales y los patrones de respuesta. [Más información](../mobile/mobile-opt-out.md#sms-native-keywords)

**Ver métricas:** Acceder a datos de clics en vínculos, volúmenes de mensajes entrantes y rendimiento de tipos de mensajes en los informes. [Informes de campaña](../reports/campaign-global-report-cja-sms.md) | [Informes de Recorrido](../reports/journey-global-report-cja-sms.md)

+++

+++Seguimiento de experiencias basado en código

Las experiencias basadas en código requieren la configuración de la implementación para enviar datos de seguimiento a Adobe Experience Platform.

**Requisitos previos:**

Antes de que el seguimiento funcione, debe configurar la implementación para enviar eventos de interacción (visualizaciones, clics) a Adobe Experience Platform. Esto requiere lo siguiente:

* Configuración de una secuencia de datos configurada para Adobe Experience Platform. [Más información](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=es)
* Implementar la recopilación de eventos en el código mediante Web SDK o Mobile SDK.
* Envío de eventos de visualización e interacción cuando se muestra o se hace clic en el contenido.

[Obtenga más información sobre los requisitos previos de implementación](../code-based/code-based-prerequisites.md#reporting-prerequisites)

**Qué se rastrea:** Una vez implementado, rastree pantallas, clics, tasas de pulsaciones y rendimiento de nivel de elemento en cualquier punto de contacto digital (sitios web, aplicaciones móviles, dispositivos IoT, etc.). [Informes de campaña](../reports/campaign-global-report-cja-code.md) | [Informes de Recorrido](../reports/journey-global-report-cja-code.md)

+++

+++Seguimiento de tarjeta de contenido

Las tarjetas de contenido rastrean automáticamente las interacciones del usuario. Configure el contenido y las reglas de visualización para controlar el comportamiento de seguimiento.

**Cómo implementar:**

* **Diseñar contenido rastreado** - Agregue botones y vínculos a su tarjeta de contenido. Cada elemento interactivo se rastrea automáticamente con etiquetas y direcciones URL.

* **Configurar persistencia**: las tarjetas de contenido persisten entre sesiones de aplicación, lo que le permite hacer un seguimiento de los patrones de participación a largo plazo. Establezca reglas de caducidad para controlar cuánto tiempo se pueden rastrear las tarjetas.

* **Configurar reglas de visualización**: defina cuándo y dónde aparecerán las tarjetas para garantizar un seguimiento preciso de las pantallas frente a las interacciones.

[Aprenda a configurar tarjetas de contenido](../content-card/create-content-card.md)

**Supervisar la participación:** Realice el seguimiento de visualizaciones, clics, tasas de pulsaciones y patrones de participación en varias sesiones. [Informes de campaña](../reports/campaign-global-report-cja-content.md) | [Informes de Recorrido](../reports/journey-global-report-cja-content.md)

+++

+++Seguimiento de página de aterrizaje

Las páginas de aterrizaje incluyen un seguimiento integrado que no requiere ninguna configuración adicional. Journey Optimizer registra automáticamente las visitas, conversiones y tasas de devolución.

**Se realiza un seguimiento automático de los elementos:**

* **Visitas** - Visitas totales y únicas para medir el alcance
* **Conversiones**: envíos de formularios, confirmaciones de suscripción u otras acciones definidas
* **Tasa de salida hacia otro sitio** - Porcentaje de visitantes que se van sin interactuar
* **Tendencias de rendimiento**: datos de series temporales que muestran cómo evolucionan las métricas

[Obtenga información sobre cómo configurar páginas de aterrizaje](../landing-pages/create-lp.md)

**Supervisar el rendimiento:** Realice un seguimiento de los patrones de visita, las tasas de conversión y las tasas de devolución a lo largo del tiempo para comprender cómo los usuarios interactúan con los formularios e identificar las áreas que se deben mejorar. [Informes de campaña](../reports/lp-report-global-cja.md)

+++

## Seguimiento de la actividad de recorrido y campaña {#journey-campaign-tracking}

Más allá del seguimiento a nivel de canal, configure el seguimiento para medir el rendimiento general y comprender el comportamiento de los clientes en sus iniciativas de marketing.

* **Definir métricas de éxito personalizadas**: configure KPI específicos alineados con sus objetivos empresariales (compras, suscripciones, renovaciones, etc.) más allá de las métricas de participación estándar. [Más información](../building-journeys/success-metrics.md)

* **Habilitar eventos de paso de recorrido**: active el seguimiento detallado de cada acción que realizan los clientes a medida que pasan por los recorridos. Esto proporciona visibilidad granular de los puntos de entrada y salida, la selección de rutas y las ubicaciones de entrega. [Más información](../reports/journey-step-events-overview.md)

* **Configurar programación**: configure la optimización del tiempo de envío para rastrear el rendimiento en diferentes estrategias de tiempo e identificar ventanas de envío óptimas. [Más información](../building-journeys/send-time-optimization.md)

* **Configurar la supervisión de acciones personalizadas**: configure el seguimiento de integraciones con sistemas externos para supervisar llamadas de API, tiempos de respuesta y patrones de error. [Más información](../action/reporting.md)

* **Crear informes personalizados y exportar datos**: cree informes personalizados y exporte datos de seguimiento a sistemas externos para un análisis más profundo. [Más información](../reports/sharing-overview.md)

* **Ver rendimiento unificado:** Acceda a informes completos tanto para campañas como para recorridos con el fin de comparar el rendimiento en correo electrónico, mensajes push, SMS y otros canales, y para comprender qué combinaciones obtienen los mejores resultados. [Informes de campaña](../reports/campaign-global-report-cja.md) | [Informes de Recorrido](../reports/journey-global-report-cja.md)

## Seguimiento de la optimización y el rendimiento de decisiones {#optimization-decisioning-tracking}

Journey Optimizer realiza automáticamente un seguimiento de los experimentos de optimización, las estrategias de segmentación y el rendimiento de las decisiones. Configure los ajustes para garantizar una recopilación de datos adecuada.

### Configuración del seguimiento de optimización {#optimization-tracking}

* **Optimización en tus campañas y recorridos**:

   * Al crear experimentos, defina qué métricas rastrear (conversiones, clics, eventos personalizados). Journey Optimizer recopila automáticamente datos de rendimiento para cada tratamiento. [Más información](../content-management/optimization-experimentation.md)

   * Cree reglas de segmentación para entregar contenido diferente a segmentos de audiencia diferentes. Journey Optimizer realiza automáticamente un seguimiento de las métricas de participación de cada grupo de destino, lo que le permite comparar el rendimiento entre segmentos. [Más información](../content-management/optimization-targeting.md)

* **Optimización de ruta de Recorrido**: Agregue una actividad **Optimizar** a su recorrido y configure varias rutas. Journey Optimizer realiza automáticamente un seguimiento de las rutas que toman los perfiles y mide el rendimiento. [Más información](../building-journeys/optimize.md)

Para analizar los resultados: vea las tasas de conversión, la relevancia estadística y el alza entre tratamientos en los informes de experimentación, o compare las métricas de participación entre segmentos segmentados. [Informe de campaña de experimentación](../reports/campaign-global-report-cja-experimentation.md) | [Informe de recorrido de experimentación](../reports/journey-global-report-cja-experimentation.md) | [Informe de segmentación de Recorridos](../reports/journey-global-report-cja.md#targeting)

### Seguimiento del rendimiento de decisiones {#decisioning-tracking}

Al utilizar Decisioning para personalizar el contenido, Journey Optimizer rastrea automáticamente los eventos de decisión, las impresiones y los clics sin necesidad de configuración adicional.

* **Captura automática de eventos**: Journey Optimizer captura automáticamente los eventos de decisión cada vez que se selecciona un elemento de decisión para un perfil.
* **Seguimiento de impresiones**: en el caso de los mensajes de correo electrónico, las impresiones se rastrean automáticamente. Para las experiencias basadas en código, debe implementar eventos de visualización de propuestas en el código. [Más información](../code-based/code-based-implementation-samples.md#client-side-how)
* **Seguimiento de clics**: Los clics en elementos de decisión se rastrean automáticamente en correos electrónicos; las experiencias basadas en código requieren la implementación de eventos de clic.

>[!NOTE]
>
>Para realizar un seguimiento de las decisiones en **experiencias basadas en código**, asegúrese de que la implementación envíe eventos de interacción de propuestas (visualizaciones y clics) a Adobe Experience Platform mediante Web SDK o Mobile SDK. [Más información](../experience-decisioning/data-collection/schema-requirement.md)

Para supervisar el rendimiento: vea los KPI de toma de decisiones, compare los elementos de decisión, analice las estrategias de selección y supervise el rendimiento del modelo de IA en los informes. [Más información](../experience-decisioning/cja-reporting.md)

## Control del uso de datos de seguimiento {#data-governance}

Las políticas de gobernanza de datos le permiten controlar cómo se pueden utilizar los datos de seguimiento en toda la organización:

* **Datos de seguimiento que distinguen entre etiquetas**: aplique etiquetas de gobernanza a los datos de comportamiento rastreados (por ejemplo, clics en contenido de mantenimiento, interacciones de productos financieros) para marcarlos como confidenciales o regulados.

* **Restringir el uso de datos**: cree directivas que impidan que los datos de seguimiento etiquetados se usen en determinados canales, se exporten a sistemas de terceros o se usen para escenarios de personalización específicos.

* **Aplicación automática**: Journey Optimizer comprueba automáticamente las directivas de gobernanza al generar recorridos y campañas, y bloquea la publicación si los datos rastreados se utilizan en violación de las directivas definidas.

La gobernanza de datos garantiza el cumplimiento de regulaciones como el RGPD y la CCPA, a la vez que le permite rastrear y analizar el comportamiento de los clientes dentro de los límites aprobados. [Más información](../action/action-privacy.md)

## Monitorización de la capacidad de envío y estado del sistema {#monitoring-capabilities}

Más allá de la participación de seguimiento, configure la monitorización para garantizar que los mensajes lleguen a las bandejas de entrada y que los sistemas funcionen de forma óptima.

La monitorización de la capacidad de entrega ayuda a garantizar que los mensajes lleguen a las bandejas de entrada de los destinatarios y mantengan una reputación de remitente saludable mediante el seguimiento de indicadores clave:

* **Revise la lista de supresión** con regularidad para comprender por qué las direcciones están bloqueadas y mantener la higiene de la lista. [Más información](../reports/suppression-list.md)

* **Analice los errores de envío** para diagnosticar errores y tomar medidas correctivas. [Más información](../configuration/email-error-types.md)

* **Siga las prácticas recomendadas** para DMARC, SPF y DKIM para maximizar la ubicación en la bandeja de entrada. [Más información](../reports/deliverability.md)

Configure la monitorización proactiva para recibir notificaciones en tiempo real sobre eventos críticos y problemas del sistema, lo que le permite responder rápidamente antes de que afecten a las experiencias de los clientes:

* **Configuración de alertas**: configure notificaciones en tiempo real para errores de recorrido, errores de acciones personalizadas y problemas críticos para responder rápidamente a los problemas. [Más información](../reports/alerts.md)

* **Habilitar registros de auditoría** - Activar registros de auditoría para rastrear todas las acciones en los recursos para el cumplimiento y la solución de problemas. [Más información](../privacy/audit-logs.md)

* **Supervisar integraciones**: realice un seguimiento del rendimiento de las acciones personalizadas y de la conectividad externa del sistema para identificar los problemas de integración de forma temprana. [Más información](../action/reporting.md)
