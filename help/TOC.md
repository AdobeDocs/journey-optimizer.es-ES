---
product: Journey Optimizer
audience: end-user
user-guide-title: Guía de Journey Optimizer
user-guide-description: Utilice Journey Optimizer para crear y ofrecer experiencias conectadas, contextuales y personalizadas a sus clientes
type: Documentation
solution: Journey Optimizer
source-git-commit: 5e1485b33608d55d878d311c2448669f898486b3
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 100%

---

# Ayuda de Adobe Journey Optimizer {#using}

+ [Documentación de Journey Optimizer](ajo-home.md)
+ Novedades {#whats-new}
   + [Últimas notas de la versión](using/rn/release-notes.md)
   + Notas de la versión anterior {#previous-rn-new}
      + [Notas de la versión de 2022](using/rn/release-notes-2022.md)
      + [Notas de la versión de 2021](using/rn/release-notes-2021.md)
   + [Actualizaciones de documentación](using/rn/documentation-updates.md)
+ Introducción{#get-started}
   + [Qué es Journey Optimizer](using/start/get-started.md)
   + Guías de inicio rápido{#quick-start}
      + [Información general](using/start/quick-start.md)
      + [Introducción como experto en marketing](using/start/path/marketer.md)
      + [Introducción como ingeniero de datos](using/start/path/data-engineer.md)
      + [Introducción como administrador](using/start/path/administrator.md)
      + [Introducción como desarrollador](using/start/path/developer.md)
   + [Interfaz de usuario](using/start/user-interface.md)
   + [Accesibilidad](using/start/accessibility.md)
   + [Integraciones](using/start/ajo-integrations.md)
   + [Mecanismos de protección](using/start/guardrails.md)
+ Recorridos {#orchestrate-journeys}
   + [Introducción a los recorridos](using/building-journeys/journey.md)
   + Creación de un recorrido{#create-journey}
      + [Creación de su primer recorrido](using/building-journeys/journey-gs.md)
      + [Diseño de un recorrido](using/building-journeys/using-the-journey-designer.md)
      + [Prueba del recorrido](using/building-journeys/testing-the-journey.md)
      + [Publicación del recorrido](using/building-journeys/publishing-the-journey.md)
   + Administrar los recorridos{#manage-journey}
      + [Termine el recorrido](using/building-journeys/end-journey.md)
      + [Administración de husos horarios](using/building-journeys/timezone-management.md)
      + [Administración de la entrada del perfil](using/building-journeys/entry-management.md)
      + [Copia de un recorrido en otra zona protegida](using/building-journeys/copy-to-sandbox.md)
      + [Resolución de problemas del recorrido](using/building-journeys/troubleshooting.md)
      + [Integración con servicios inteligentes](using/building-journeys/ai-services-overview.md)
      + [Administración de etiquetas en recorrido](using/building-journeys/tags.md)
   + Actividades {#about-journey-building}
      + [Introducción a actividades de recorrido](using/building-journeys/about-journey-activities.md)
      + [Eventos generales](using/building-journeys/general-events.md)
      + [Reacción](using/building-journeys/reaction-events.md)
      + [Clasificación del segmento](using/building-journeys/segment-qualification-events.md)
      + [Condición](using/building-journeys/condition-activity.md)
      + [Espera](using/building-journeys/wait-activity.md)
      + [Lectura de segmento](using/building-journeys/read-segment.md)
      + [Correo electrónico, SMS, push](using/building-journeys/journeys-message.md)
      + [Acciones personalizadas](using/building-journeys/using-custom-actions.md)
      + [Acciones de Adobe Campaign Standard](using/building-journeys/using-adobe-campaign-standard.md)
      + [Acciones de Adobe Campaign v7/v8](using/building-journeys/using-adobe-campaign-classic.md)
      + [Salto](using/building-journeys/jump.md)
      + [Actualización de perfil](using/building-journeys/update-profiles.md)
   + Expresiones de compilación {#building-advanced-conditions-journeys}
      + [Información general](using/building-journeys/expression/expressionadvanced.md)
      + Sintaxis {#syntax}
         + [Generalidades](using/building-journeys/expression/generalities.md)
         + [Instrucción condicional](using/building-journeys/expression/conditional-instruction.md)
         + [Tipos de datos](using/building-journeys/expression/data-types.md)
         + [Referencias de campo](using/building-journeys/expression/field-references.md)
         + [Funciones de administración de colecciones](using/building-journeys/expression/collection-management-functions.md)
         + [Operadores](using/building-journeys/expression/operators.md)
         + [Propiedades del recorrido](using/building-journeys/expression/journey-properties.md)
         + [Ejemplos](using/building-journeys/expression/advanced-editor-use-cases.md)
      + Funciones {#main-functions-journey}
         + [Funciones principales](using/building-journeys/expression/functions.md)
         + Adobe Experience Platform {#adobe-experience-platform}
            + [inSegment](using/building-journeys/functions/functioninsegment.md)
         + Agregación {#aggregation}
            + [avg](using/building-journeys/functions/functionavg.md)
            + [count](using/building-journeys/functions/functioncount.md)
            + [countOnlyNull](using/building-journeys/functions/functioncountonlynull.md)
            + [countWithNull](using/building-journeys/functions/functioncountwithnull.md)
            + [distinctCount](using/building-journeys/functions/functiondistinctcount.md)
            + [distinctCountWithNull](using/building-journeys/functions/functiondistinctcountwithnull.md)
            + [max](using/building-journeys/functions/functionmax.md)
            + [min](using/building-journeys/functions/functionmin.md)
            + [sum](using/building-journeys/functions/functionsum.md)
         + Conversión {#conversion}
            + [toBool](using/building-journeys/functions/functiontobool.md)
            + [toDateOnly](using/building-journeys/functions/functiontodateonly.md)
            + [toDateTime](using/building-journeys/functions/functiontodatetime.md)
            + [toDateTimeOnly](using/building-journeys/functions/functiontodatetimeonly.md)
            + [toDecimal](using/building-journeys/functions/functiontodecimal.md)
            + [toDuration](using/building-journeys/functions/functiontoduration.md)
            + [toInteger](using/building-journeys/functions/functiontointeger.md)
            + [toString](using/building-journeys/functions/functiontostring.md)
         + Fecha {#date}
            + [currentTimeInMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
            + [inLastDays](using/building-journeys/functions/functioninlastdays.md)
            + [inLastHours](using/building-journeys/functions/functioninlasthours.md)
            + [inLastMonths](using/building-journeys/functions/functioninlastmonths.md)
            + [inLastYears](using/building-journeys/functions/functioninlastyears.md)
            + [inNextDays](using/building-journeys/functions/functioninnextdays.md)
            + [inNextHours](using/building-journeys/functions/functioninnexthours.md)
            + [inNextMonths](using/building-journeys/functions/functioninnextmonths.md)
            + [inNextYears](using/building-journeys/functions/functioninnextyears.md)
            + [now](using/building-journeys/functions/functionnow.md)
            + [nowWithDelta](using/building-journeys/functions/functionnowwithdelta.md)
            + [setHours](using/building-journeys/functions/functionsethours.md)
            + [setDays](using/building-journeys/functions/functionsetdays.md)
            + [updateTimeZone](using/building-journeys/functions/functionupdatetimezone.md)
         + Lista {#list}
            + [distinct](using/building-journeys/functions/functiondistinct.md)
            + [distinctWithNull](using/building-journeys/functions/functiondistinctwithnull.md)
            + [filter](using/building-journeys/functions/functionfilter.md)
            + [getListItem](using/building-journeys/functions/functiongetlistitem.md)
            + [en](using/building-journeys/functions/functionin.md)
            + [intersect](using/building-journeys/functions/functionintersect.md)
            + [límite](using/building-journeys/functions/functionlimit.md)
            + [listSize](using/building-journeys/functions/functionlistsize.md)
            + [serializeList](using/building-journeys/functions/functionserializelist.md)
            + [sort](using/building-journeys/functions/functionsort.md)
         + Math {#math}
            + [random](using/building-journeys/functions/functionrandom.md)
            + [round](using/building-journeys/functions/functionround.md)
         + Cadena {#string}
            + [concat](using/building-journeys/functions/functionconcat.md)
            + [contain](using/building-journeys/functions/functioncontain.md)
            + [containIgnoreCase](using/building-journeys/functions/functioncontainwithignorecase.md)
            + [endWith](using/building-journeys/functions/functionendwith.md)
            + [endWithIgnorecase](using/building-journeys/functions/functionendwithignorecase.md)
            + [equalIgnoreCase](using/building-journeys/functions/functionequalignorecase.md)
            + [indexOf](using/building-journeys/functions/functionindexof.md)
            + [isEmpty](using/building-journeys/functions/functionisempty.md)
            + [isNotEmpty](using/building-journeys/functions/functionisnotempty.md)
            + [lastIndexOf](using/building-journeys/functions/functionlastindexof.md)
            + [length](using/building-journeys/functions/functionlength.md)
            + [lower](using/building-journeys/functions/functionlower.md)
            + [matchRegExp](using/building-journeys/functions/functionmatchregexp.md)
            + [notequalIgnoreCase](using/building-journeys/functions/functionnotequalignorecase.md)
            + [replace](using/building-journeys/functions/functionreplace.md)
            + [replaceAll](using/building-journeys/functions/functionreplaceall.md)
            + [split](using/building-journeys/functions/functionsplit.md)
            + [startWith](using/building-journeys/functions/functionstartwith.md)
            + [startWithIgnoreCase](using/building-journeys/functions/functionstartwithignorecase.md)
            + [substr](using/building-journeys/functions/functionsubstr.md)
            + [trim](using/building-journeys/functions/functiontrim.md)
            + [upper](using/building-journeys/functions/functionupper.md)
            + [uuid](using/building-journeys/functions/functionuuid.md)
   + Casos de uso {#journey-use-cases}
      + Casos de uso empresariales {#business-use-cases}
         + [Envío de mensajes multicanal](using/building-journeys/journeys-uc.md)
         + [Envío de un mensaje mediante Campaign v7/v8](using/building-journeys/ajo-ac.md)
         + [Envío de un mensaje a los suscriptores](using/building-journeys/message-to-subscribers-uc.md)
      + Casos de uso técnicos {#technical-use-cases}
         + [Paso de colecciones de forma dinámica mediante acciones personalizadas](using/building-journeys/collections.md)
         + [Aumento de envíos](using/building-journeys/ramp-up-deliveries-uc.md)
         + [Limitación del rendimiento con fuentes de datos externas y acciones personalizadas](using/building-journeys/limit-throughput.md)
+ Campañas{#campaigns}
   + [Introducción a las campañas](using/campaigns/get-started-with-campaigns.md)
   + [Creación de una campaña](using/campaigns/create-campaign.md)
   + [Revisión y activación de una campaña](using/campaigns/review-activate-campaign.md)
   + [Administración de campañas](using/campaigns/modify-stop-campaign.md)
   + Experimento de contenido {#content-experiment}
      + [Introducción al experimento de contenido](using/campaigns/get-started-experiment.md)
      + [Creación de un experimento de contenido](using/campaigns/content-experiment.md)
      + [Comprensión de los cálculos estadísticos](using/campaigns/experiment-calculations.md)
      + [Configurar informes de experimentación](using/campaigns/reporting-configuration.md)
      + [Cálculos estadísticos en el informe de experimentación](using/campaigns/experiment-report-calculations.md)
   + [Activación de campañas mediante las API](using/campaigns/api-triggered-campaigns.md)
+ Canal de correo electrónico {#email}
   + [Empezar con correos electrónicos](using/email/get-started-email.md)
   + [Crear un correo electrónico](using/email/create-email.md)
   + Diseño del contenido del correo electrónico {#design-email}
      + [Introducción al diseño de correo electrónico](using/email/get-started-email-design.md)
      + Empezar a crear contenido {#start-creating-content}
         + [Empezar desde cero](using/email/content-from-scratch.md)
         + [Importar el contenido del correo electrónico](using/email/existing-content.md)
         + [Codifique su propio contenido](using/email/code-content.md)
         + [Uso de plantillas](using/email/email-templates.md)
      + Diseño del contenido {#add-content}
         + [Uso de componentes de contenido](using/email/content-components.md)
         + [Adición de vínculos y seguimiento de mensajes](using/email/message-tracking.md)
         + Administración de recursos {#manage-asset}
            + [Trabajar con Assets Essentials](using/email/assets-essentials.md)
            + [Trabajar con Adobe Stock](using/email/stock.md)
         + [Inserción de ofertas personalizadas](using/email/add-offers-email.md)
         + [Generar la versión de texto](using/email/text-version-email.md)
         + [Añadir un encabezado previo](using/email/preheader.md)
      + Editar estilo {#edit-style}
         + [Introducción al diseño de correo electrónico](using/email/get-started-email-style.md)
         + [Editar configuración de fondo](using/email/backgrounds.md)
         + [Ajustar alineación vertical y relleno](using/email/alignment-and-padding.md)
         + [Definición de un estilo para los vínculos](using/email/styling-links.md)
         + [Añadir atributos de estilo en línea](using/email/inline-styling.md)
   + [Previsualizar y probar el correo electrónico](using/email/preview.md)
   + [Creación de plantillas de contenido](using/email/content-templates.md)
   + [Uso de plantillas de Experience Manager](using/email/aem-templates.md)
   + [Administrar la exclusión de correo electrónico](using/email/email-opt-out.md)
   + Configurar canal de correo electrónico {#configure-email}
      + [Empezar a configurar el correo electrónico](using/email/get-started-email-config.md)
      + [Configuración de correo electrónico](using/email/email-settings.md)
+ Canal en la aplicación{#in-app}
   + [Introducción al canal en la aplicación](using/in-app/get-started-in-app.md)
   + [Creación de un mensaje en la aplicación ](using/in-app/create-in-app.md)
   + [Diseño del contenido en la aplicación](using/in-app/design-in-app.md)
   + [Prueba y envío de notificación en la aplicación](using/in-app/send-in-app.md)
   + [Configuración del canal en la aplicación](using/in-app/inapp-configuration.md)
+ Canal de notificaciones push{#push}
   + [Introducción a las notificaciones push](using/push/get-started-push.md)
   + [Crear una notificación push](using/push/create-push.md)
   + [Diseño de la notificación push](using/push/design-push.md)
   + [Enviar la notificación push](using/push/send-push.md)
   + Configuración de notificaciones push{#push-config}
      + [Notificaciones push con Adobe Journey Optimizer](using/push/push-gs.md)
      + [Configurar el canal de notificaciones push](using/push/push-configuration.md)
+ Canal de SMS{#sms}
   + [Introducción a los SMS](using/sms/get-started-sms.md)
   + [Creación de un mensaje SMS](using/sms/create-sms.md)
   + [Previsualizar y probar SMS](using/sms/send-sms.md)
   + [Administrar la exclusión de SMS](using/sms/sms-opt-out.md)
   + [Configuración del canal de SMS](using/sms/sms-configuration.md)
   + [Configuración de subdominios SMS](using/sms/sms-subdomains.md)
+ Correo directo {#direct-mail}
   + [Creación de un correo directo](using/direct-mail/create-direct-mail.md)
   + [Configuración del correo directo](using/direct-mail/direct-mail-configuration.md)
+ Canal web{#web}
   + [Introducción al canal web](using/web/get-started-web.md)
   + [Creación de experiencias web](using/web/create-web.md)
   + [Creación de páginas web](using/web/author-web.md)
   + [Extensión Ayuda de edición visual](using/web/visual-editing-helper.md)
   + [Creación de informes web](using/web/web-report.md)
+ Páginas de aterrizaje {#landing-pages}
   + [Introducción a las páginas de aterrizaje](using/landing-pages/get-started-lp.md)
   + [Creación de una página de aterrizaje](using/landing-pages/create-lp.md)
   + Diseño de contenido de {#landing-pages-design}
      + [Acerca del diseño de página de aterrizaje](using/landing-pages/design-lp.md)
      + [Creación del contenido de la página de aterrizaje](using/landing-pages/lp-content.md)
      + [Crear plantillas](using/landing-pages/lp-templates.md)
      + [Agregar JavaScript personalizado](using/landing-pages/lp-custom-js.md)
   + [Creación de una lista de suscripción](using/landing-pages/subscription-list.md)
   + [Descubra los casos de uso](using/landing-pages/lp-use-cases.md)
   + Configuración de las páginas de aterrizaje {#lp-configuration}
      + [Configurar subdominios de página de aterrizaje](using/landing-pages/lp-subdomains.md)
      + [Definir ajustes preestablecidos de página de aterrizaje](using/landing-pages/lp-presets.md)
+ Personalización y contenido dinámico {#personalized-dynamic-content}
   + Personalización {#personalization}
      + [Introducción a la personalización](using/personalization/personalize.md)
      + [Contextos de personalización](using/personalization/personalization-contexts.md)
      + Expresiones de compilación {#build-expressions}
         + [Sintaxis de personalización](using/personalization/personalization-syntax.md)
         + Trabajo con el Editor de expresiones {#expression-editor}
            + [Acerca del Editor de expresiones](using/personalization/personalization-build-expressions.md)
            + [Adición de atributos a favoritos](using/personalization/personalization-favorites.md)
            + [Uso de expresiones guardadas](using/personalization/personalization-library.md)
            + [Validación de personalización](using/personalization/personalization-validation.md)
         + Funciones de ayuda{#functions}
            + [Introducción a las funciones de ayuda](using/personalization/functions/functions.md)
            + [Funciones de agregación](using/personalization/functions/aggregation.md)
            + [Funciones aritméticas](using/personalization/functions/arithmetic-functions.md)
            + [Funciones de matrices y listas](using/personalization/functions/arrays-list.md)
            + [Funciones de fecha](using/personalization/functions/dates.md)
            + [Funciones booleanas y de comparación](using/personalization/functions/operators.md)
            + [Ayudantes](using/personalization/functions/helpers.md)
            + [Funciones de asignación](using/personalization/functions/maps.md)
            + [Funciones matemáticas](using/personalization/functions/math.md)
            + [Funciones de objeto](using/personalization/functions/objects.md)
            + [Funciones de cadena](using/personalization/functions/string.md)
      + Casos de uso{#personalization-use-cases}
         + [Notificación del estado del pedido](using/personalization/personalization-use-case.md)
         + [Correo electrónico de abandono del carro de compras](using/personalization/personalization-use-case-helper-functions.md)
   + Contenido dinámico {#dynamic}
      + [Introducción al contenido dinámico](using/personalization/get-started-dynamic-content.md)
      + [Creación de reglas condicionales](using/personalization/create-conditions.md)
      + [Crear contenido dinámico](using/personalization/dynamic-content.md)
+ Segmentos, perfiles e identidad{#segment}
   + Segmentos {#segments}
      + [Introducción a los segmentos](using/segment/about-segments.md)
      + [Generación de segmentos](using/segment/creating-a-segment.md)
   + Perfiles{#profiles}
      + [Introducción a los perfiles](using/segment/get-started-profiles.md)
      + [Creación de perfiles de prueba](using/segment/creating-test-profiles.md)
   + [Identidades](using/segment/get-started-identity.md)
   + Componer audiencias {#audience-orchestration}
      + [Introducción a Composición de audiencias](using/segment/get-started-audience-orchestration.md)
      + [Creación de flujos de trabajo de composición](using/segment/create-compositions.md)
      + [Trabajo con el lienzo de composición](using/segment/composition-canvas.md)
      + [Acceso y administración de audiencias](using/segment/access-audiences.md)
   + [Uso de licencias](using/segment/license-usage.md)
+ Seguimiento y monitorización {#reporting}
   + Informe en vivo {#live-report}
      + [Introducción al Informe en vivo](using/reports/live-report.md)
      + [Informe activo de recorrido](using/reports/journey-live-report.md)
      + [Informe en directo de la campaña](using/reports/campaign-live-report.md)
      + [Informe en directo de la página de aterrizaje](using/reports/lp-report-live.md)
      + [Informe en directo de la lista de suscripciones](using/reports/subscription-report-live.md)
   + Informe global {#global-report}
      + [Introducción al Informe global](using/reports/global-report.md)
      + [Informe global de recorrido](using/reports/journey-global-report.md)
      + [Informe global de la campaña](using/reports/campaign-global-report.md)
      + [Informe global de la página de aterrizaje](using/reports/lp-report-global.md)
      + [Informe global de la lista de suscripciones](using/reports/subscription-report-global.md)
   + Informes de recorrido {#reports}
      + [Creación de informes de recorrido](using/reports/sharing-overview.md)
      + [Lista de campos de eventos de paso](using/reports/sharing-field-list.md)
      + Campos de eventos de paso heredados {#legacy-step-event-fields}
         + [Acerca de los campos heredados](using/reports/sharing-legacy-fields.md)
         + [Campos del recorrido](using/reports/sharing-journey-fields.md)
         + [Campos comunes](using/reports/sharing-common-fields.md)
         + [Campos de ejecución de la acción](using/reports/sharing-execution-fields.md)
         + [Campos de captura de datos](using/reports/sharing-fetch-fields.md)
         + [Campos de identidad](using/reports/sharing-identity-fields.md)
      + [Ejemplos de consultas](using/reports/query-examples.md)
   + Capacidad de entrega {#deliverability}
      + [Introducción a la capacidad de entrega](using/reports/deliverability.md)
      + [Explicación de la lista de supresión](using/reports/suppression-list.md)
   + [Alertas](using/reports/alerts.md)
   + [Uso de Customer Journey Analytics](using/reports/cja-ajo.md)
+ Gestión de decisiones {#offer-decisioning}
   + Introducción a la Gestión de decisiones {#get-started-decision}
      + [Acerca de la Gestión de decisiones](using/offers/get-started/starting-offer-decisioning.md)
      + [Interfaz de usuario](using/offers/get-started/user-interface.md)
      + [Pasos clave para crear y administrar ofertas](using/offers/offer-library/key-steps.md)
      + [Caso práctico: insertar ofertas en un correo electrónico](using/offers/offers-e2e.md)
   + Crear componentes {#create-components}
      + [Crear ubicaciones](using/offers/offer-library/creating-placements.md)
      + [Crear reglas de decisión](using/offers/offer-library/creating-decision-rules.md)
      + [Crear calificadores de colección](using/offers/offer-library/creating-tags.md)
   + Crear clasificaciones de {#rankings}
      + [Introducción a las clasificaciones](using/offers/ranking/get-started-rankings.md)
      + [Fórmulas de clasificación](using/offers/ranking/create-ranking-formulas.md)
      + Modelos de IA {#ai-models}
         + [Acerca de los modelos de IA](using/offers/ranking/ai-models.md)
         + Tipos de modelos de IA {#ai-model-types}
            + [Modelo de optimización automática](using/offers/ranking/auto-optimization-model.md)
            + [Modelo de optimización personalizado](using/offers/ranking/personalized-optimization-model.md)
         + [Creación de modelos de IA](using/offers/ranking/create-ranking-strategies.md)
   + Crear y administrar ofertas {#managing-offers-in-the-offer-library}
      + Configurar ofertas {#configure-offers}
         + [Creación de ofertas personalizadas](using/offers/offer-library/creating-personalized-offers.md)
         + [Añadir representaciones](using/offers/offer-library/add-representations.md)
         + [Añadir restricciones](using/offers/offer-library/add-constraints.md)
      + [Crear ofertas de reserva](using/offers/offer-library/creating-fallback-offers.md)
      + [Crear colecciones](using/offers/offer-library/creating-collections.md)
   + Crear y administrar decisiones {#create-manage-activities}
      + [Crear decisiones](using/offers/offer-activities/create-offer-activities.md)
      + [Configurar selección de ofertas en decisiones](using/offers/offer-activities/configure-offer-selection.md)
      + [Creación de simulaciones](using/offers/offer-activities/simulation.md)
   + [Usar toma de decisiones por lotes](using/offers/batch-delivery.md)
   + Recopilación de datos de evento {#collect-event-data}
      + [Introducción a la recopilación de datos](using/offers/data-collection/data-collection.md)
      + [Crear un conjunto de datos para recopilar eventos](using/offers/data-collection/create-dataset.md)
      + [Configurar la captura de eventos](using/offers/data-collection/schema-requirement.md)
   + Creación de informes de Gestión de decisiones {#create-reports}
      + [Introducción a los eventos de Gestión de decisiones](using/offers/reports/get-started-events.md)
      + [Información clave sobre eventos de gestión de decisiones](using/offers/reports/key-information.md)
      + [Campos XDM de eventos de acceso](using/offers/reports/xdm-fields.md)
   + Exportación del catálogo de ofertas {#export-catalog}
      + [Introducción a la exportación del catálogo de ofertas ](using/offers/export-catalog/get-started-export.md)
      + [Acceder al catálogo de ofertas exportado](using/offers/export-catalog/access-dataset.md)
      + [Conjunto de datos de ofertas personalizadas](using/offers/export-catalog/export-offers.md)
      + [Conjunto de datos de decisiones](using/offers/export-catalog/export-decisions.md)
      + [Conjunto de datos de ubicaciones](using/offers/export-catalog/export-placements.md)
      + [Conjunto de datos de reserva](using/offers/export-catalog/export-fallback.md)
   + Referencia de API {#api-reference}
      + [Introducción](using/offers/api-reference/getting-started.md)
      + Crear y administrar ofertas mediante API {#offers-api}
         + Ubicaciones {#placements}
            + [Enumerar ubicaciones](using/offers/api-reference/offers-api/placements/placements-list.md)
            + [Buscar una ubicación](using/offers/api-reference/offers-api/placements/lookup.md)
            + [Crear una ubicación](using/offers/api-reference/offers-api/placements/create.md)
            + [Actualizar una ubicación](using/offers/api-reference/offers-api/placements/update.md)
            + [Eliminar una ubicación](using/offers/api-reference/offers-api/placements/delete.md)
         + Reglas de decisión {#decision-rules}
            + [Enumerar reglas de decisión](using/offers/api-reference/offers-api/decision-rules/rules-list.md)
            + [Buscar una regla de decisión](using/offers/api-reference/offers-api/decision-rules/lookup.md)
            + [Crear una regla de decisión](using/offers/api-reference/offers-api/decision-rules/create.md)
            + [Actualizar una regla de decisión](using/offers/api-reference/offers-api/decision-rules/update.md)
            + [Eliminar una regla de decisión](using/offers/api-reference/offers-api/decision-rules/delete.md)
         + Cualificadores de colección {#tags}
            + [Cualificadores de colección de lista](using/offers/api-reference/offers-api/tags/tags-list.md)
            + [Búsqueda de un cualificador de colección](using/offers/api-reference/offers-api/tags/lookup.md)
            + [Creación de un cualificador de colección](using/offers/api-reference/offers-api/tags/create.md)
            + [Actualización de un cualificador colección](using/offers/api-reference/offers-api/tags/update.md)
            + [Eliminación de un cualificador de colección](using/offers/api-reference/offers-api/tags/delete.md)
         + Ofertas personalizadas {#personalized-offers}
            + [Enumerar ofertas personalizadas](using/offers/api-reference/offers-api/personalized-offers/offers-list.md)
            + [Buscar una oferta personalizada](using/offers/api-reference/offers-api/personalized-offers/lookup.md)
            + [Crear una oferta personalizada](using/offers/api-reference/offers-api/personalized-offers/create.md)
            + [Actualizar una oferta personalizada](using/offers/api-reference/offers-api/personalized-offers/update.md)
            + [Eliminar una oferta personalizada](using/offers/api-reference/offers-api/personalized-offers/delete.md)
         + Colecciones {#collections}
            + [Enumerar colecciones](using/offers/api-reference/offers-api/collections/collections-list.md)
            + [Buscar una colección](using/offers/api-reference/offers-api/collections/lookup.md)
            + [Crear una colección](using/offers/api-reference/offers-api/collections/create.md)
            + [Actualizar una colección](using/offers/api-reference/offers-api/collections/update.md)
            + [Eliminar una colección](using/offers/api-reference/offers-api/collections/delete.md)
         + Ofertas de reserva {#fallback-offers}
            + [Enumerar ofertas de reserva](using/offers/api-reference/offers-api/fallback-offers/fallback-list.md)
            + [Buscar una oferta de reserva](using/offers/api-reference/offers-api/fallback-offers/lookup.md)
            + [Crear una oferta de reserva](using/offers/api-reference/offers-api/fallback-offers/create.md)
            + [Actualizar una oferta de reserva](using/offers/api-reference/offers-api/fallback-offers/update.md)
            + [Eliminar una oferta de reserva](using/offers/api-reference/offers-api/fallback-offers/delete.md)
      + Crear y administrar decisiones mediante API {#activities-api}
         + [Enumerar decisiones](using/offers/api-reference/activities-api/activities/activities-list.md)
         + [Buscar una decisión](using/offers/api-reference/activities-api/activities/lookup.md)
         + [Crear una decisión](using/offers/api-reference/activities-api/activities/create.md)
         + [Actualizar una decisión](using/offers/api-reference/activities-api/activities/update.md)
         + [Eliminar una decisión](using/offers/api-reference/activities-api/activities/delete.md)
      + Entrega de ofertas mediante API {#offer-delivery-api}
         + [Introducción a las API de envío de ofertas](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
         + [API de decisiones](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
         + [API de Edge Decisioning](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
         + [API de decisiones por lotes](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ Administración de datos {#data-management}
   + [Introducción a la administración de datos](using/data/gs-data.md)
   + [Usar esquemas](using/data/get-started-schemas.md)
   + Conjuntos de datos de Journey Optimizer {#datasets}
      + [Introducción a los conjuntos de datos](using/data/get-started-datasets.md)
      + [Exportación de conjuntos de datos de Journey Optimizer](using/data/export-datasets.md)
      + [Ejemplos de consultas](using/data/datasets-query-examples.md)
      + [Esquemas integrados > ](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=es)
   + [Consultas](using/data/get-started-queries.md)
+ Configuración{#configuration}
   + [Introducción a la configuración de Journey Optimizer](using/configuration/get-started-configuration.md)
   + Delegación de subdominios de correo electrónico {#delegate-subdomains}
      + [Introducción a la delegación de subdominios](using/configuration/about-subdomain-delegation.md)
      + [Delegar un subdominio](using/configuration/delegate-subdomain.md)
      + [Añadir un registro TXT de Google](using/configuration/google-txt.md)
      + [Acceso y edición de registros PTR](using/configuration/ptr-records.md)
      + [Crear grupos de IP](using/configuration/ip-pools.md)
   + [Configuración de superficies de canal](using/configuration/channel-surfaces.md)
   + Supervisar las direcciones de correo electrónico {#monitor-reputation}
      + [Lista de supresión](using/configuration/manage-suppression-list.md)
      + [Reintentos](using/configuration/retries.md)
      + [Lista de permitidos](using/configuration/allow-list.md)
   + [Asistencia para el archivado](using/configuration/archiving-support.md)
   + [Configuración de las reglas de frecuencia](using/configuration/frequency-rules.md)
   + [Administrar direcciones de ejecución](using/configuration/primary-email-addresses.md)
   + Configurar recorridos {#configure-journeys}
      + [Acerca de las fuentes de datos, los eventos y las acciones](using/configuration/about-data-sources-events-actions.md)
      + Integración con sistemas externos {#external-systems}
         + [Integración de recorridos con sistemas externos](using/configuration/external-systems.md)
         + [API de límite](using/configuration/capping.md)
         + [API de limitación](using/configuration/throttling.md)
      + Configuración de eventos {#events-journeys}
         + [Principio general](using/event/about-events.md)
         + Configuración de un evento unitario {#unitary-events}
            + [Introducción a los eventos unitarios](using/event/about-creating.md)
            + [Acerca de los esquemas de ExperienceEvent](using/event/experience-event-schema.md)
            + [Trabajar con Adobe Analytics](using/event/about-analytics.md)
         + [Configuración de un evento empresarial](using/event/about-creating-business.md)
         + [Pasos adicionales para enviar eventos](using/event/additional-steps-to-send-events-to-journey.md)
      + Configuración de la fuente de datos{#data-source-journeys}
         + [Acerca de las fuentes de datos](using/datasource/about-data-sources.md)
         + [Configuración de una fuente de datos](using/datasource/configure-data-sources.md)
         + [Fuente de datos de Adobe Experience Platform](using/datasource/adobe-experience-platform-data-source.md)
         + [Fuentes de datos externas](using/datasource/external-data-sources.md)
      + Configuración de la acción {#action-journeys}
         + [Acerca de las acciones](using/action/action.md)
         + [Configuración de una acción](using/action/about-custom-action-configuration.md)
         + [Integrar con Adobe Campaign Standard](using/action/acs-action.md)
         + [Integración con las versiones 7 y 8 de Adobe Campaign](using/action/acc-action.md)
   + [Fuentes](using/start/get-started-sources.md)
+ Control de acceso {#access-control}
   + [Información general sobre el control de acceso](using/administration/permissions-overview.md)
   + [Perfiles de producto integrados](using/administration/ootb-product-profiles.md)
   + [Administrar usuarios y perfiles de producto](using/administration/permissions.md)
   + [Niveles de permisos](using/administration/high-low-permissions.md)
   + [Administración de zonas protegidas](using/administration/sandboxes.md)
   + [Control de acceso basado en atributos](using/administration/attribute-based-access.md)
   + [Control de acceso de nivel de objeto](using/administration/object-based-access.md)
+ Privacidad {#privacy}
   + [Introducción a la privacidad](using/privacy/get-started-privacy.md)
   + [Solicitudes de privacidad](using/privacy/requests.md)
   + [Acciones de auditoría en recursos](using/privacy/audit-logs.md)
   + [Realizar operaciones de limpieza de datos](using/privacy/data-hygiene.md)
   + Administración del consentimiento {#consent}
      + [Administración de la exclusión](using/privacy/opt-out.md)
      + [Trabajar con políticas de consentimiento](using/action/consent.md)
   + [Control de datos](using/action/action-privacy.md)
