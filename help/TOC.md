---
product: Journey Optimizer
audience: end-user
user-guide-title: Guía de Journey Optimizer
user-guide-description: Utilice Journey Optimizer para crear y ofrecer experiencias conectadas, contextuales y personalizadas a sus clientes
type: Documentation
solution: Journey Optimizer
source-git-commit: c41d7e7543f3254479f63d4e104f471192e63632
workflow-type: tm+mt
source-wordcount: '2339'
ht-degree: 89%

---

# Ayuda de Adobe Journey Optimizer {#using}

+ [Documentación de Journey Optimizer](ajo-home.md)
+ Novedades {#whats-new}
   + [Notas de la versión preliminar](using/rn/e-release-notes.md)
   + [Últimas notas de la versión](using/rn/release-notes.md)
   + Notas de la versión anterior {#previous-rn-new}
      + [2025](using/rn/release-notes-2025.md)
      + [2024](using/rn/release-notes-2024.md)
      + [2023](using/rn/release-notes-2023.md)
      + [2022](using/rn/release-notes-2022.md)
      + [2021](using/rn/release-notes-2021.md)
   + [Actualizaciones de la documentación](using/rn/documentation-updates.md)
   + [Nuevo lienzo de recorrido](using/rn/new-canvas.md)
+ Introducción {#get-started}
   + [Qué es Journey Optimizer](using/start/get-started.md)
   + Guías de inicio rápido{#quick-start}
      + [Información general](using/start/quick-start.md)
      + [Introducción como experto en marketing](using/start/path/marketer.md)
      + [Introducción como ingeniero de datos](using/start/path/data-engineer.md)
      + [Introducción como administrador](using/start/path/administrator.md)
      + [Introducción como desarrollador](using/start/path/developer.md)
   + [Interfaz de usuario](using/start/user-interface.md)
   + [Buscar, filtrar, categorizar](using/start/search-filter-categorize.md)
   + [Accesibilidad](using/start/accessibility.md)
   + [Manuales de tácticas de casos de uso](using/start/playbooks.md)
   + [Trabajo con el asistente de IA](using/start/ai-assistant.md)
   + [Mecanismos de protección](using/start/guardrails.md)
   + [Prácticas recomendadas](using/start/best-practices.md)
+ Recorridos {#orchestrate-journeys}
   + [Introducción a los recorridos](using/building-journeys/journey.md)
   + Creación de un recorrido{#create-journey}
      + [Creación de su primer recorrido](using/building-journeys/journey-gs.md)
      + [Establecimiento de las propiedades del recorrido](using/building-journeys/journey-properties.md)
      + [Configuración y seguimiento de la métrica de recorrido](using/building-journeys/success-metrics.md)
      + [Diseño de un recorrido](using/building-journeys/using-the-journey-designer.md)
      + [Prueba del recorrido](using/building-journeys/testing-the-journey.md)
      + [Simulación del recorrido](using/building-journeys/journey-simulation.md)
      + [Publicación del recorrido](using/building-journeys/publishing-the-journey.md)
      + [Informe en vivo en el recorrido](using/building-journeys/report-journey.md)
   + Administrar los recorridos{#manage-journey}
      + [Examinar y filtrar sus recorridos](using/building-journeys/journey-ui.md)
      + [Administración de la entrada del perfil](using/building-journeys/entry-management.md)
      + [Administración de husos horarios](using/building-journeys/timezone-management.md)
      + [Optimización de hora de envío](using/building-journeys/send-time-optimization.md)
      + [Termine el recorrido](using/building-journeys/end-journey.md)
      + [Copia de un recorrido en otra zona protegida](using/building-journeys/copy-to-sandbox.md)
      + [Resolución de problemas del recorrido](using/building-journeys/troubleshooting.md)
      + [Integración con servicios inteligentes](using/building-journeys/ai-services-overview.md)
   + Actividades {#about-journey-building}
      + [Introducción a actividades de recorrido](using/building-journeys/about-journey-activities.md)
      + [Eventos generales](using/building-journeys/general-events.md)
      + [Reacción](using/building-journeys/reaction-events.md)
      + [Calificación de público](using/building-journeys/audience-qualification-events.md)
      + [Condición](using/building-journeys/condition-activity.md)
      + [Espera](using/building-journeys/wait-activity.md)
      + [Público de lectura](using/building-journeys/read-audience.md)
      + [Acciones de canal integradas](using/building-journeys/journeys-message.md)
      + [Acciones personalizadas](using/building-journeys/using-custom-actions.md)
      + [Acciones de Adobe Campaign Standard](using/building-journeys/using-adobe-campaign-standard.md)
      + [Acciones de Adobe Campaign v7/v8](using/building-journeys/using-adobe-campaign-v7-v8.md)
      + [Salto](using/building-journeys/jump.md)
      + [Actualización de perfil](using/building-journeys/update-profiles.md)
   + Expresiones de compilación {#building-advanced-conditions-journeys}
      + [Trabajo con el editor de expresiones avanzado](using/building-journeys/expression/expressionadvanced.md)
      + Sintaxis {#syntax}
         + [Sintaxis avanzada del editor de expresiones](using/building-journeys/expression/generalities.md)
         + [Instrucción condicional](using/building-journeys/expression/conditional-instruction.md)
         + [Tipos de datos](using/building-journeys/expression/data-types.md)
         + [Referencias del campo](using/building-journeys/expression/field-references.md)
         + [Funciones de administración de colecciones](using/building-journeys/expression/collection-management-functions.md)
         + [Operadores](using/building-journeys/expression/operators.md)
         + [Propiedades del recorrido](using/building-journeys/expression/journey-properties.md)
         + [Ejemplos](using/building-journeys/expression/advanced-editor-use-cases.md)
      + Funciones {#main-functions-journey}
         + [Funciones principales](using/building-journeys/expression/functions.md)
         + Adobe Experience Platform {#adobe-experience-platform}
            + [inAudience](using/building-journeys/functions/functioninaudience.md)
         + Agregación {#aggregation}
            + [avg](using/building-journeys/functions/functionavg.md)
            + [recuento](using/building-journeys/functions/functioncount.md)
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
            + [currentTime&#x200B;InMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
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
            + [ordenar](using/building-journeys/functions/functionsort.md)
         + Matemáticas {#math}
            + [random](using/building-journeys/functions/functionrandom.md)
            + [round](using/building-journeys/functions/functionround.md)
         + Cadena {#string}
            + [concatena](using/building-journeys/functions/functionconcat.md)
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
            + [UUID](using/building-journeys/functions/functionuuid.md)
   + Casos de uso {#journey-use-cases}
      + Casos de uso empresariales {#business-use-cases}
         + [Envío de mensajes multicanal](using/building-journeys/journeys-uc.md)
         + [Envío de un mensaje mediante Campaign v7/v8](using/building-journeys/ajo-ac.md)
         + [Envío de un mensaje a los suscriptores](using/building-journeys/message-to-subscribers-uc.md)
      + Casos de uso técnicos {#technical-use-cases}
         + [Paso de colecciones de forma dinámica mediante acciones personalizadas](using/building-journeys/collections.md)
         + [Aumento de envíos](using/building-journeys/ramp-up-deliveries-uc.md)
         + [Limitación del rendimiento con fuentes de datos externas y acciones personalizadas](using/building-journeys/limit-throughput.md)
         + [Utilice acciones personalizadas para escribir los eventos de recorrido en Experience Platform](using/building-journeys/custom-action-aep.md)
+ Campañas organizadas {#orchestrated-campaigns}
   + [Introducción a las campañas orquestadas](using/ms/gs-ms-campaigns.md)
   + [Pasos de configuración](using/ms/gs-campaign-config.md)
   + [Principios clave](using/ms/gs-campaign-creation.md)
   + Configuración {#ms-config}
      + [Pasos de configuración](using/ms/gs-campaign-config.md)
      + [Esquemas](using/ms/ms-schemas.md)
      + [Trabajo con variables de evento](using/ms/event-variables.md)
   + Creación de la primera campaña orquestada {#create-ms-campaign}
      + [Creación de una campaña organizada](using/ms/create-ms-campaign.md)
      + [Organización de actividades](using/ms/orchestrate-activities.md)
      + [Configuración de campaña](using/ms/ms-campaign-settings.md)
      + [Iniciar y monitorizar campañas](using/ms/start-monitor-campaigns.md)
      + [Administrar personalización](using/ms/ms-personalization.md)
   + Actividades de campaña organizadas {#design-campaigns}
      + [Acerca de las actividades de campaña orquestadas](using/ms/activities/about-activities.md)
      + [And-join](using/ms/activities/and-join.md)
      + [Generar público](using/ms/activities/build-audience.md)
      + [Cambiar dimensión](using/ms/activities/change-dimension.md)
      + [Combinar](using/ms/activities/combine.md)
      + [Deduplicación](using/ms/activities/deduplication.md)
      + [Acciones de canal](using/ms/activities/channels.md)
      + [Enriquecimiento](using/ms/activities/enrichment.md)
      + [Bifurcación](using/ms/activities/fork.md)
      + [Carga de archivo](using/ms/activities/load-file.md)
      + [Reconciliación](using/ms/activities/reconciliation.md)
      + [Guardar público](using/ms/activities/save-audience.md)
      + [Planificador](using/ms/activities/scheduler.md)
      + [División](using/ms/activities/split.md)
      + [Prueba](using/ms/activities/test.md)
      + [Actualización de datos](using/ms/activities/update-data.md)
      + [Espera](using/ms/activities/wait.md)
+ Campañas {#campaigns}
   + [Introducción a las campañas](using/campaigns/get-started-with-campaigns.md)
   + [Creación de una campaña](using/campaigns/create-campaign.md)
   + [Revisión y activación de una campaña](using/campaigns/review-activate-campaign.md)
   + [Administración de campañas](using/campaigns/modify-stop-campaign.md)
   + [Activación de campañas mediante las API](using/campaigns/api-triggered-campaigns.md)
+ Administración de conflictos y priorización {#conflict-prioritization}
   + [Introducción a la administración y priorización de conflictos](using/conflict-prioritization/gs-conflict-prioritization.md)
   + [Identificar posibles conflictos](using/conflict-prioritization/conflicts.md)
   + [Asignar puntuaciones de prioridad](using/conflict-prioritization/priority-scores.md)
   + [Límite y arbitraje de recorrido](using/conflict-prioritization/journey-capping.md)
+ Probar y aprobar {#test}
   + Previsualización y prueba del contenido {#preview-test}
      + [Introducción a la vista previa y prueba](using/content-management/preview-test.md)
      + [Seleccionar perfiles de prueba](using/content-management/test-profiles.md)
      + [Vista previa del contenido](using/content-management/preview.md)
      + [Envío de pruebas de correo electrónico](using/content-management/proofs.md)
      + [Prueba del procesamiento de correo electrónico](using/content-management/rendering.md)
      + [Prueba del contenido con datos de entrada de muestra (Beta)](using/test-approve/simulate-sample-input.md)
      + [Informe de correo electrónico no deseado](using/content-management/spam-report.md)
   + Aprobar recorridos y campañas {#approve}
      + [Introducción a las aprobaciones](using/test-approve/gs-approval.md)
      + [Creación y administración de políticas de aprobación](using/test-approve/approval-policies.md)
      + [Solicitud de aprobación](using/test-approve/request-approval.md)
      + [Aprobación de una solicitud](using/test-approve/review-approve-request.md)
+ Canales de comunicación {#channels}
   + [Introducción a los canales de comunicación](using/channels/gs-channels.md)
   + Canal de correo electrónico {#email}
      + [Empezar con correos electrónicos](using/email/get-started-email.md)
      + [Crear un correo electrónico](using/email/create-email.md)
      + Diseño del contenido del correo electrónico {#design-email}
         + [Introducción al diseño de correo electrónico](using/email/get-started-email-design.md)
         + Empezar a crear contenido {#start-creating-content}
            + [Diseño de contenido desde cero](using/email/content-from-scratch.md)
            + [Importe el contenido](using/email/existing-content.md)
            + [Codifique su propio contenido](using/email/code-content.md)
            + [Uso de plantillas de correo electrónico](using/email/use-email-templates.md)
         + Diseño del contenido {#add-content}
            + [Uso de componentes de contenido](using/email/content-components.md)
            + [Aprovechamiento de fragmentos visuales](using/email/use-visual-fragments.md)
            + [Adición de vínculos y seguimiento de mensajes](using/email/message-tracking.md)
            + [Inserción de ofertas personalizadas](using/email/add-offers-email.md)
            + [Generar la versión de texto](using/email/text-version-email.md)
            + [Añadir metadatos](using/email/email-metadata.md)
         + Editar estilo {#edit-style}
            + [Introducción al diseño de correo electrónico](using/email/get-started-email-style.md)
            + [Editar configuración de fondo](using/email/backgrounds.md)
            + [Ajustar alineación vertical y relleno](using/email/alignment-and-padding.md)
            + [Añadir atributos de estilo en línea](using/email/inline-styling.md)
      + [Administrar la exclusión de correo electrónico](using/email/email-opt-out.md)
      + Configurar canal de correo electrónico {#configure-email}
         + [Empezar a configurar el correo electrónico](using/email/get-started-email-config.md)
         + [Definir la configuración de correo electrónico](using/email/email-settings.md)
         + [Habilitar la cancelación de suscripción a una lista](using/email/list-unsubscribe.md)
         + [Parámetros de encabezado](using/email/header-parameters.md)
         + [Seguimiento de URL](using/email/url-tracking.md)
         + [Personalización de la configuración de correo electrónico](using/email/surface-personalization.md)
   + Canal en la aplicación{#in-app}
      + [Introducción al canal en la aplicación](using/in-app/get-started-in-app.md)
      + [Requisitos previos del canal en la aplicación](using/in-app/inapp-configuration.md)
      + [Creación de un mensaje en la aplicación para móviles](using/in-app/create-in-app.md)
      + [Creación de un mensaje web en la aplicación](using/in-app/create-in-app-web.md)
      + [Diseño del contenido en la aplicación](using/in-app/design-in-app.md)
      + [Comprobación y envío de la notificación en la aplicación](using/in-app/send-in-app.md)
   + Canal de notificaciones push{#push}
      + [Introducción a las notificaciones push](using/push/get-started-push.md)
      + [Crear una notificación push](using/push/create-push.md)
      + [Diseño de la notificación push](using/push/design-push.md)
      + [Comprobación y envío de la notificación push](using/push/send-push.md)
      + Configuración de notificaciones push{#push-config}
         + [Flujo de notificaciones push](using/push/push-gs.md)
         + [Configurar el canal de notificaciones push](using/push/push-configuration.md)
         + [Flujo de trabajo de inicio rápido de incorporación al dispositivo móvil](using/push/mobile-onboarding-wf.md)
   + Canal de SMS/MMS{#sms}
      + [Introducción a la mensajería de texto](using/sms/get-started-sms.md)
      + [Creación de un mensaje de texto (SMS/MMS)](using/sms/create-sms.md)
      + [Comprobación y envío de los mensajes de texto](using/sms/send-sms.md)
      + [Administración de la exclusión de mensajes de texto](using/sms/sms-opt-out.md)
      + [Configuración de subdominios de SMS](using/sms/sms-subdomains.md)
      + Configuración del canal SMS/MMS{#configure-sms}
         + [Introducción a la configuración de SMS](using/sms/sms-configuration.md)
         + [Configuración del proveedor Sinch](using/sms/sms-configuration-sinch.md)
         + [Configuración del proveedor Infobip](using/sms/sms-configuration-infobip.md)
         + [Configuración del proveedor Twilio](using/sms/sms-configuration-twilio.md)
         + [Configure un proveedor personalizado (Beta)](using/sms/sms-configuration-custom.md)
         + [Creación de una configuración de SMS](using/sms/sms-configuration-surface.md)
   + Correo directo {#direct-mail}
      + [Introducción al correo directo](using/direct-mail/get-started-direct-mail.md)
      + [Creación de un correo directo](using/direct-mail/create-direct-mail.md)
      + [Prueba y envío de un mensaje de correo directo](using/direct-mail/test-send-direct-mail.md)
      + [Configuración del correo directo](using/direct-mail/direct-mail-configuration.md)
   + Canal web {#web}
      + [Introducción al canal web](using/web/get-started-web.md)
      + Configuración del canal web {#configure-web-channel}
         + [Requisitos previos de canal web](using/web/web-prerequisites.md)
         + [Configuración de subdominios web](using/web/web-delegated-subdomains.md)
         + [Creación de una configuración de canal web](using/web/web-configuration.md)
      + [Creación de experiencias web](using/web/create-web.md)
      + Creación de páginas web {#author-web-pages}
         + [Trabajar con el diseñador web](using/web/web-visual-editor.md)
         + [Utilizar el editor no visual](using/web/web-non-visual-editor.md)
         + [Administración de modificaciones](using/web/manage-web-modifications.md)
         + [Monitorización de sus experiencias web](using/web/monitor-web-experiences.md)
         + [Creación de aplicaciones de una sola página](using/web/web-spa.md)
   + Experiencia basada en código {#code-based-experience}
      + [Introducción al canal basado en código](using/code-based/get-started-code-based.md)
      + Configuración del canal basado en código {#configure-code-based-channel}
         + [Protecciones y requisitos previos](using/code-based/code-based-prerequisites.md)
         + [Superficies de la experiencia basada en código](using/code-based/code-based-surface.md)
         + [Ejemplos de métodos de implementación](using/code-based/code-based-implementation-samples.md)
         + [Creación de una configuración de experiencia basada en código](using/code-based/code-based-configuration.md)
      + Creación de experiencias basadas en código {#create-code-based-experiences}
         + [Crear y componer experiencias basadas en código](using/code-based/create-code-based.md)
         + [Probar experiencias basadas en código](using/code-based/test-code-based.md)
         + [Administración de experiencias basadas en código](using/code-based/publish-code-based.md)
   + Tarjetas de contenido{#content-card}
      + [Introducción a las tarjetas de contenido](using/content-card/get-started-content-card.md)
      + Configurar el canal de la tarjeta de contenido {#configure}
         + [Requisitos previos de tarjetas de contenido](using/content-card/content-card-configuration-prereq.md)
         + [Configuración del canal de tarjetas de contenido en Journey Optimizer](using/content-card/content-card-configuration.md)
         + [Configuración de la compatibilidad con tarjetas de contenido en el SDK para dispositivos móviles](using/content-card/content-card-lp.md)
         + [Configuración de la compatibilidad con tarjetas de contenido en SDK web](using/content-card/content-card-configuration-sdk.md)
      + [Creación de tarjetas de contenido](using/content-card/create-content-card.md)
      + [Diseño de tarjetas de contenido](using/content-card/design-content-card.md)
   + WhatsApp{#whatsapp}
      + [Introducción a los mensajes de WhatsApp](using/whatsapp/get-started-whatsapp.md)
      + [Configuración del canal de WhatsApp en Journey Optimizer](using/whatsapp/whatsapp-configuration.md)
      + [Creación de un mensaje de WhatsApp](using/whatsapp/create-whatsapp.md)
      + [Comprobación y envío de los mensajes de WhatsApp](using/whatsapp/send-whatsapp.md)
+ Páginas de aterrizaje {#landing-pages}
   + [Introducción a las páginas de aterrizaje](using/landing-pages/get-started-lp.md)
   + [Creación de una página de aterrizaje](using/landing-pages/create-lp.md)
   + Diseño de contenido {#landing-pages-design}
      + [Acerca del diseño de página de aterrizaje](using/landing-pages/design-lp.md)
      + [Creación del contenido de la página de aterrizaje](using/landing-pages/lp-content.md)
      + [Crear plantillas](using/landing-pages/lp-templates.md)
      + [Agregar JavaScript personalizado](using/landing-pages/lp-custom-js.md)
   + [Creación de una lista de suscripción](using/landing-pages/subscription-list.md)
   + [Descubra los casos de uso](using/landing-pages/lp-use-cases.md)
   + Configuración de las páginas de aterrizaje {#lp-configuration}
      + [Configurar subdominios de página de aterrizaje](using/landing-pages/lp-subdomains.md)
      + [Definir ajustes preestablecidos de página de aterrizaje](using/landing-pages/lp-presets.md)
+ Gestión de contenido {#content-management}
   + Asistente de IA para la generación de contenido{#ai-assistant}
      + [Introducción al asistente de IA](using/content-management/gs-generative.md)
      + [Generación de correo electrónico con IA](using/content-management/generative-email.md)
      + [Generación de push con IA](using/content-management/generative-push.md)
      + [Generación de SMS con IA](using/content-management/generative-sms.md)
      + [Generación de web con IA](using/content-management/generative-web.md)
      + [Experimento de contenido con IA](using/content-management/generative-experimentation.md)
      + [Página de aterrizaje con IA](using/content-management/generative-lp.md)
      + [Casos de uso del Asistente de IA](using/content-management/generative-uc.md)
      + [Creación y administración de marcas (Beta)](using/content-management/brands.md)
   + Trabajo con contenido multilingüe{#content-multilingual}
      + [Introducción al contenido multilingüe](using/content-management/multilingual-gs.md)
      + [Creación de una configuración regional](using/content-management/multilingual-locale.md)
      + [Creación de un proveedor de idiomas](using/content-management/multilingual-provider.md)
      + [Creación de contenido multilingüe con traducción manual](using/content-management/multilingual-manual.md)
      + [Creación de contenido multilingüe con traducción automática](using/content-management/multilingual-automated.md)
   + Trabajo con el experimento de contenido {#content-experiment}
      + [Introducción al experimento de contenido](using/content-management/get-started-experiment.md)
      + [Creación de un experimento de contenido](using/content-management/content-experiment.md)
      + Notas técnicas {#technotes}
         + [Comprensión de los cálculos estadísticos](using/content-management/experiment-calculations.md)
         + [Explicación de los cálculos estadísticos en el informe de experimentación](using/content-management/experiment-report-calculations.md)
   + Personalización {#personalization}
      + [Introducción a la personalización](using/personalization/personalize.md)
      + [Adición de personalización](using/personalization/personalization-build-expressions.md)
      + [Sintaxis de personalización](using/personalization/personalization-syntax.md)
      + [Reutilización de fragmentos de expresión](using/personalization/use-expression-fragments.md)
      + [Uso de datos de Adobe Experience Platform para la personalización (Beta)](using/personalization/lookup-aep-data.md)
      + Lista de funciones de ayuda {#functions}
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
      + Casos de uso de Personalization{#personalization-use-cases}
         + [Notificación del estado del pedido](using/personalization/personalization-use-case.md)
         + [Correo electrónico de abandono del carro de compras](using/personalization/personalization-use-case-helper-functions.md)
         + [Correo electrónico de prescripciones del plan de salud](using/personalization/perso-uc-plan-prescriptions.md)
   + Plantillas de contenido {#content-templates}
      + [Introducción a las plantillas de contenido](using/content-management/content-templates.md)
      + [Acceso y administración de plantillas](using/content-management/access-content-templates.md)
      + [Creación de plantillas de contenido](using/content-management/create-content-templates.md)
      + [Bloquear contenido en plantillas de correo electrónico](using/content-management/content-locking.md)
      + [Plantillas de contenido de prueba](using/content-management/test-content-templates.md)
      + [Uso de plantillas de contenido](using/content-management/use-content-templates.md)
   + Fragmentos de contenido reutilizables {#fragments}
      + [Introducción a los fragmentos](using/content-management/fragments.md)
      + [Crear un fragmento](using/content-management/create-fragments.md)
      + [Guardar contenido existente como fragmento](using/content-management/save-fragments.md)
      + [Fragmentos personalizables](using/content-management/customizable-fragments.md)
      + [Administración de fragmentos](using/content-management/manage-fragments.md)
   + Contenido dinámico {#dynamic}
      + [Introducción al contenido dinámico](using/personalization/get-started-dynamic-content.md)
      + [Creación de reglas condicionales](using/personalization/create-conditions.md)
      + [Crear contenido dinámico](using/personalization/dynamic-content.md)
+ Audiencias, perfiles e identidad{#audiences-profiles-identities}
   + Públicos {#audiences}
      + [Introducción a los públicos](using/audience/about-audiences.md)
      + Creación de públicos {#create}
         + [Definiciones de segmentos](using/audience/creating-a-segment-definition.md)
         + [Composición de público](using/audience/get-started-audience-orchestration.md)
         + [Carga personalizada](using/audience/custom-upload.md)
         + [Composición de público federado](using/audience/federated-audience-composition.md)
      + [Activación de público en campañas y recorridos](using/audience/target-audiences.md)
      + [Aprovechar atributos de enriquecimiento](using/audience/enrichment-attributes.md)
   + Perfiles{#profiles}
      + [Introducción a los perfiles](using/audience/get-started-profiles.md)
      + [Creación de perfiles de prueba](using/audience/creating-test-profiles.md)
      + [Trabajo con atributos de varios valores](using/audience/computed-attributes.md)
   + [Identidades](using/audience/get-started-identity.md)
   + [Uso de licencias](using/audience/license-usage.md)
+ Integraciones{#integrations}
   + [Integraciones con otras soluciones](using/integrations/ajo-integrations.md)
   + [Trabajar con Experience Manager Assets](using/integrations/assets.md)
   + [Trabajar con Adobe Stock](using/integrations/stock.md)
   + [Trabajar con Adobe Express](using/integrations/express.md)
   + [Trabajar con plantillas de Experience Manager](using/integrations/aem-templates.md)
   + [Trabajar con fragmentos de contenido de Experience Manager](using/integrations/aem-fragments.md)
   + [Trabajar con Dynamic Media](using/integrations/aem-dynamic.md)
   + [Trabajo con GenStudio](using/integrations/genstudio.md)
+ Seguimiento y monitorización {#reporting}
   + Informe en vivo {#live-report}
      + [Introducción al Informe activo](using/reports/live-report.md)
      + [Lista de métricas](using/reports/live-report-components.md)
      + [Informe activo de recorrido](using/reports/journey-live-report.md)
      + [Informe en vivo de la campaña](using/reports/campaign-live-report.md)
      + [Informe en directo de la página de aterrizaje](using/reports/lp-report-live.md)
      + [Informe en directo de la lista de suscripciones](using/reports/subscription-report-live.md)
   + Informe de todo el tiempo{#channel-report}
      + [Introducción al Informe de todo el tiempo](using/reports/report-gs-cja.md)
      + [Lista de métricas](using/reports/global-report-components-cja.md)
      + [Configurar Customer Journey Analytics manualmente](using/reports/cja-ajo.md)
      + [Administración de informes](using/reports/report-cja-manage.md)
      + [Requisitos previos de creación de informes y experimentación](using/reports/reporting-configuration.md)
      + Informes de campaña{#reporting}
         + [Informe de campaña](using/reports/campaign-global-report-cja.md)
         + [Informe de campaña basado en código](using/reports/campaign-global-report-cja-code.md)
         + [Informe de campaña de tarjeta de contenido](using/reports/campaign-global-report-cja-content.md)
         + [Informe de campaña de correo directo](using/reports/campaign-global-report-cja-direct.md)
         + [Informe de campaña de correo electrónico](using/reports/campaign-global-report-cja-email.md)
         + [Informe de campaña de experimentación](using/reports/campaign-global-report-cja-experimentation.md)
         + [Informe de campaña in-app](using/reports/campaign-global-report-cja-inapp.md)
         + [Informe de campaña de notificaciones push](using/reports/campaign-global-report-cja-push.md)
         + [Informe de campaña de SMS](using/reports/campaign-global-report-cja-sms.md)
         + [Informe de campaña web](using/reports/campaign-global-report-cja-web.md)
      + informes de recorrido{#reporting}
         + [Informe de recorrido](using/reports/journey-global-report-cja.md)
         + [Informe de recorrido basado en código](using/reports/journey-global-report-cja-code.md)
         + [Informe de recorrido de tarjeta de contenido](using/reports/journey-global-report-cja-content.md)
         + [Informe de recorrido de correo directo](using/reports/journey-global-report-cja-direct.md)
         + [Informe de recorrido de correo electrónico](using/reports/journey-global-report-cja-email.md)
         + [Informe de recorrido in-app](using/reports/journey-global-report-cja-inapp.md)
         + [Informe de recorrido push](using/reports/journey-global-report-cja-push.md)
         + [Informe de recorrido de SMS](using/reports/journey-global-report-cja-sms.md)
         + [Informe de recorrido web](using/reports/journey-global-report-cja-web.md)
      + [Informe de información general](using/reports/channel-report-cja.md)
      + [Informe de página de aterrizaje](using/reports/lp-report-global-cja.md)
      + [Informe de la lista de suscripciones](using/reports/subscription-report-global-cja.md)
   + informes de recorrido {#reports}
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
   + Estrategia y definición {#deliverability}
      + [Introducción a la Entregabilidad](using/reports/deliverability.md)
      + [Explicación de la lista de supresión](using/reports/suppression-list.md)
      + [Nuevo requisito de DMARC](using/configuration/dmarc-record-update.md)
   + [Alertas](using/reports/alerts.md)
   + [Motivos de exclusión](using/reports/exclusion-list.md)
+ Capacidades de decisión {#decisioning}
   + [Introducción a las capacidades de decisiones](using/experience-decisioning/gs-decision.md)
   + Toma de decisiones {#experience-decisioning}
      + [Introducción a la toma de decisiones](using/experience-decisioning/gs-experience-decisioning.md)
      + [Limitaciones y protecciones de decisiones](using/experience-decisioning/decisioning-guardrails.md)
      + Referencia de la API{#api-reference}
         + Creación y administración de elementos de oferta {#create-manage}
            + Elementos de decisión{#decision-items}
               + [Creación de elementos de decisión](using/experience-decisioning/api-reference/decisions-items/create.md)
               + [Lista de elementos de decisión](using/experience-decisioning/api-reference/decisions-items/decision-items-list.md)
               + [Eliminar elementos de decisión](using/experience-decisioning/api-reference/decisions-items/delete.md)
               + [Búsqueda de los elementos de decisión](using/experience-decisioning/api-reference/decisions-items/lookup.md)
               + [Actualización de los elementos de decisión](using/experience-decisioning/api-reference/decisions-items/update.md)
            + Colecciones de elementos{#items-collections}
               + [Creación de colecciones de elementos](using/experience-decisioning/api-reference/items-collections/create.md)
               + [Eliminación de colecciones de elementos](using/experience-decisioning/api-reference/items-collections/delete.md)
               + [Lista de colecciones de elementos](using/experience-decisioning/api-reference/items-collections/items-collections-list.md)
               + [Búsqueda de colecciones de elementos](using/experience-decisioning/api-reference/items-collections/lookup.md)
               + [Actualización de colecciones de elementos](using/experience-decisioning/api-reference/items-collections/update.md)
            + Estrategias de selección{#selection-strategies}
               + [Creación de estrategias de selección](using/experience-decisioning/api-reference/selection-strategies/create.md)
               + [Eliminación de estrategias de selección](using/experience-decisioning/api-reference/selection-strategies/delete.md)
               + [Búsqueda de estrategias de selección](using/experience-decisioning/api-reference/selection-strategies/lookup.md)
               + [Lista de estrategias de selección](using/experience-decisioning/api-reference/selection-strategies/selection-strategies-list.md)
               + [Actualización de estrategias de selección](using/experience-decisioning/api-reference/selection-strategies/update.md)
            + Fórmulas de clasificación{#ranking-formulas}
               + [Crear fórmulas de clasificación](using/experience-decisioning/api-reference/ranking-formulas/create.md)
               + [Eliminar fórmulas de clasificación](using/experience-decisioning/api-reference/ranking-formulas/delete.md)
               + [Consultar fórmulas de clasificación](using/experience-decisioning/api-reference/ranking-formulas/lookup.md)
               + [Selección de fórmulas de clasificación](using/experience-decisioning/api-reference/ranking-formulas/ranking-formulas-list.md)
               + [Actualizar fórmulas de clasificación](using/experience-decisioning/api-reference/ranking-formulas/update.md)
            + Reglas de idoneidad{#eligibility-rules}
               + [Crear reglas de idoneidad](using/experience-decisioning/api-reference/eligibility-rules/create.md)
               + [Eliminar reglas de idoneidad](using/experience-decisioning/api-reference/eligibility-rules/delete.md)
               + [Consultar reglas de idoneidad](using/experience-decisioning/api-reference/eligibility-rules/lookup.md)
               + [Lista de reglas de idoneidad](using/experience-decisioning/api-reference/eligibility-rules/eligibility-rules-list.md)
               + [Actualizar reglas de idoneidad](using/experience-decisioning/api-reference/eligibility-rules/update.md)
         + [Entregar ofertas mediante el canal de experiencia basada en código](using/experience-decisioning/api-reference/deliver.md)
      + Administración de elementos de decisión {#decision-items}
         + [Configuración del catálogo de elementos](using/experience-decisioning/catalogs.md)
         + [Creación de elementos de decisión](using/experience-decisioning/items.md)
         + [Administración de colecciones de elementos](using/experience-decisioning/collections.md)
      + Configurar la selección de elementos {#selection}
         + [Crear reglas de decisión](using/experience-decisioning/rules.md)
         + [Creación de métodos de clasificación](using/experience-decisioning/ranking.md)
         + [Uso de datos de contexto](using/experience-decisioning/context-data.md)
      + [Creación de estrategias de selección](using/experience-decisioning/selection-strategies.md)
      + [Creación de políticas de decisión](using/experience-decisioning/create-decision.md)
      + [Informe sobre la toma de decisiones](using/experience-decisioning/cja-reporting.md)
      + [Caso de uso sobre la toma de decisiones](using/experience-decisioning/experience-decisioning-uc.md)
   + Administración de decisiones {#offer-decisioning}
      + Introducción a Administración de decisiones {#get-started-decision}
         + [Acerca de la Gestión de decisiones](using/offers/get-started/starting-offer-decisioning.md)
         + [Limitaciones y protecciones de gestión de decisiones](using/offers/decision-management-guardrails.md)
         + [Interfaz de usuario](using/offers/get-started/user-interface.md)
         + [Pasos clave para crear y administrar ofertas](using/offers/offer-library/key-steps.md)
         + [Aprovechamiento de los públicos de carga personalizados para la toma de decisiones](using/offers/custom-upload-decisioning.md)
         + [Caso práctico: insertar ofertas en un correo electrónico](using/offers/offers-e2e.md)
      + Creación de componentes {#create-components}
         + [Crear ubicaciones](using/offers/offer-library/creating-placements.md)
         + [Crear reglas de decisión](using/offers/offer-library/creating-decision-rules.md)
         + [Crear calificadores de colección](using/offers/offer-library/creating-tags.md)
      + Crear clasificaciones {#rankings}
         + [Introducción a las clasificaciones](using/offers/ranking/get-started-rankings.md)
         + [Fórmulas de clasificación](using/offers/ranking/create-ranking-formulas.md)
         + modelos de IA {#ai-models}
            + [Acerca de los modelos de IA](using/offers/ranking/ai-models.md)
            + Tipos de modelos de IA {#ai-model-types}
            + [Modelo de optimización automática](using/offers/ranking/auto-optimization-model.md)
            + [Modelo de optimización personalizado](using/offers/ranking/personalized-optimization-model.md)
            + [Creación de modelos de IA](using/offers/ranking/create-ranking-strategies.md)
      + Crear y administrar ofertas {#managing-offers-in-the-offer-library}
         + Configuración de ofertas {#configure-offers}
            + [Creación de ofertas personalizadas](using/offers/offer-library/creating-personalized-offers.md)
            + [Añadir representaciones](using/offers/offer-library/add-representations.md)
            + [Añadir restricciones](using/offers/offer-library/add-constraints.md)
         + [Crear ofertas de reserva](using/offers/offer-library/creating-fallback-offers.md)
         + [Crear colecciones](using/offers/offer-library/creating-collections.md)
      + Creación y administración de decisiones {#create-manage-activities}
         + [Crear decisiones](using/offers/offer-activities/create-offer-activities.md)
         + [Configurar selección de ofertas en decisiones](using/offers/offer-activities/configure-offer-selection.md)
         + [Creación de simulaciones](using/offers/offer-activities/simulation.md)
      + [Usar toma de decisiones por lotes](using/offers/batch-delivery.md)
      + Recopilación de datos de evento {#collect-event-data}
         + [Introducción a la recopilación de datos](using/offers/data-collection/data-collection.md)
         + [Crear un conjunto de datos para recopilar eventos](using/offers/data-collection/create-dataset.md)
         + [Configurar la captura de eventos](using/offers/data-collection/schema-requirement.md)
      + Uso de datos de contexto {#context-data}
         + [Introducción a los datos de contexto](using/offers/context-data.md)
         + [Datos de contexto y solicitudes de Edge Decisioning](using/offers/context-data-edge.md)
         + [Solicitud de datos de contexto y toma de decisiones](using/offers/context-data-decisioning.md)
      + Creación de informes de Administración de decisiones {#create-reports}
         + [Trabajar con eventos de gestión de decisiones](using/offers/reports/get-started-events.md)
         + [Campos XDM de eventos de acceso](using/offers/reports/xdm-fields.md)
      + Exportación del catálogo de ofertas {#export-catalog}
         + [Introducción a la exportación del catálogo de ofertas](using/offers/export-catalog/get-started-export.md)
         + [Acceder al catálogo de ofertas exportado](using/offers/export-catalog/access-dataset.md)
         + [Conjunto de datos de ofertas personalizadas](using/offers/export-catalog/export-offers.md)
         + [Conjunto de datos de decisiones](using/offers/export-catalog/export-decisions.md)
         + [Conjunto de datos de ubicaciones](using/offers/export-catalog/export-placements.md)
         + [Conjunto de datos de reserva](using/offers/export-catalog/export-fallback.md)
      + Referencia de API {#api-reference}
         + [Introducción](using/offers/api-reference/getting-started.md)
         + Creación y administración de ofertas mediante API {#offers-api}
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
            + Calificadores de colección {#tags}
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
            + Decisiones {#decisions-api}
               + [Enumerar decisiones](using/offers/api-reference/activities-api/activities/activities-list.md)
               + [Buscar una decisión](using/offers/api-reference/activities-api/activities/lookup.md)
               + [Crear una decisión](using/offers/api-reference/activities-api/activities/create.md)
               + [Actualizar una decisión](using/offers/api-reference/activities-api/activities/update.md)
               + [Eliminar una decisión](using/offers/api-reference/activities-api/activities/delete.md)
            + API heredadas {#legacy-api}
               + [Acerca de las API heredadas](using/offers/api-reference/offers-api/legacy-apis/about-legacy-apis.md)
               + Ubicaciones {#placements}
                  + [Enumerar ubicaciones](using/offers/api-reference/offers-api/legacy-apis/placements/placements-list.md)
                  + [Buscar una ubicación](using/offers/api-reference/offers-api/legacy-apis/placements/lookup.md)
                  + [Crear una ubicación](using/offers/api-reference/offers-api/legacy-apis/placements/create.md)
                  + [Actualizar una ubicación](using/offers/api-reference/offers-api/legacy-apis/placements/update.md)
                  + [Eliminar una ubicación](using/offers/api-reference/offers-api/legacy-apis/placements/delete.md)
               + Reglas de decisión {#decision-rules}
                  + [Enumerar reglas de decisión](using/offers/api-reference/offers-api/legacy-apis/decision-rules/rules-list.md)
                  + [Buscar una regla de decisión](using/offers/api-reference/offers-api/legacy-apis/decision-rules/lookup.md)
                  + [Crear una regla de decisión](using/offers/api-reference/offers-api/legacy-apis/decision-rules/create.md)
                  + [Actualizar una regla de decisión](using/offers/api-reference/offers-api/legacy-apis/decision-rules/update.md)
                  + [Eliminar una regla de decisión](using/offers/api-reference/offers-api/legacy-apis/decision-rules/delete.md)
               + Calificadores de colección {#tags}
                  + [Cualificadores de colección de lista](using/offers/api-reference/offers-api/legacy-apis/tags/tags-list.md)
                  + [Búsqueda de un cualificador de colección](using/offers/api-reference/offers-api/legacy-apis/tags/lookup.md)
                  + [Creación de un cualificador de colección](using/offers/api-reference/offers-api/legacy-apis/tags/create.md)
                  + [Actualización de un cualificador colección](using/offers/api-reference/offers-api/legacy-apis/tags/update.md)
                  + [Eliminación de un cualificador de colección](using/offers/api-reference/offers-api/legacy-apis/tags/delete.md)
               + Ofertas personalizadas {#personalized-offers}
                  + [Enumerar ofertas personalizadas](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/offers-list.md)
                  + [Buscar una oferta personalizada](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/lookup.md)
                  + [Crear una oferta personalizada](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/create.md)
                  + [Actualizar una oferta personalizada](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/update.md)
                  + [Eliminar una oferta personalizada](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/delete.md)
               + Ofertas de reserva {#fallback-offers}
                  + [Enumerar ofertas de reserva](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/fallback-list.md)
                  + [Buscar una oferta de reserva](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/lookup.md)
                  + [Crear una oferta de reserva](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/create.md)
                  + [Actualizar una oferta de reserva](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/update.md)
                  + [Eliminar una oferta de reserva](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/delete.md)
               + Colecciones {#collections}
                  + [Enumerar colecciones](using/offers/api-reference/offers-api/legacy-apis/collections/collections-list.md)
                  + [Buscar una colección](using/offers/api-reference/offers-api/legacy-apis/collections/lookup.md)
                  + [Crear una colección](using/offers/api-reference/offers-api/legacy-apis/collections/create.md)
                  + [Actualizar una colección](using/offers/api-reference/offers-api/legacy-apis/collections/update.md)
                  + [Eliminar una colección](using/offers/api-reference/offers-api/legacy-apis/collections/delete.md)
               + Decisiones {#decisions-api}
                  + [Enumerar decisiones](using/offers/api-reference/offers-api/legacy-apis/activities-api/activities-list.md)
                  + [Buscar una decisión](using/offers/api-reference/offers-api/legacy-apis/activities-api/lookup.md)
                  + [Crear una decisión](using/offers/api-reference/offers-api/legacy-apis/activities-api/create.md)
                  + [Actualizar una decisión](using/offers/api-reference/offers-api/legacy-apis/activities-api/update.md)
                  + [Eliminar una decisión](using/offers/api-reference/offers-api/legacy-apis/activities-api/delete.md)
         + Entrega de ofertas mediante API {#offer-delivery-api}
            + [Introducción a las API de envío de ofertas](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
            + [API de decisiones](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
            + [API de Edge Decisioning](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
            + [API de decisiones por lotes](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ Administración de datos {#data-management}
   + [Introducción a la administración de datos](using/data/gs-data.md)
   + [Usar esquemas](using/data/get-started-schemas.md)
   + Conjuntos de datos Journey Optimizer {#datasets}
      + [Introducción a los conjuntos de datos](using/data/get-started-datasets.md)
      + [Protecciones de tiempo de vida (TTL) de conjuntos de datos](using/data/datasets-ttl.md)
      + [Exportación de conjuntos de datos de Journey Optimizer](using/data/export-datasets.md)
      + [Ejemplos de consultas](using/data/datasets-query-examples.md)
      + [Esquemas integrados > ](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=es)
   + [Consultas](using/data/get-started-queries.md)
+ Configuración de canal {#configuration}
   + [Configuración de los canales](using/configuration/get-started-configuration.md)
   + [Creación de configuraciones de canal](using/configuration/channel-surfaces.md)
   + Configuración de canales guiada {#guided-setup}
      + [Introducción a la configuración de canales guiada](using/configuration/set-mobile-config.md)
      + [Creación de una configuración de canal](using/configuration/create-channel-set-up.md)
   + Delegar subdominios de correo electrónico {#delegate-subdomains}
      + [Introducción a la delegación de subdominios](using/configuration/about-subdomain-delegation.md)
      + [Delegar un subdominio](using/configuration/delegate-subdomain.md)
      + [Configurar el registro DMARC](using/configuration/dmarc-record.md)
      + [Añadir un registro TXT de Google](using/configuration/google-txt.md)
      + [Acceso y edición de registros PTR](using/configuration/ptr-records.md)
      + [Crear grupos de IP](using/configuration/ip-pools.md)
   + Implementación de un plan de calentamiento de IP {#implement-ip-warmup-plan}
      + [Introducción a los planes de calentamiento de IP](using/configuration/ip-warmup-gs.md)
      + [Creación de campañas de calentamiento de IP](using/configuration/ip-warmup-campaign.md)
      + [Creación de un plan de calentamiento de IP](using/configuration/ip-warmup-plan.md)
      + [Ejecución del plan de calentamiento de IP](using/configuration/ip-warmup-execution.md)
      + [Archivos de plan de calentamiento de IP](using/configuration/ip-warmup-plan-files.md)
   + Supervisión de direcciones de correo electrónico {#monitor-reputation}
      + [Lista de supresión](using/configuration/manage-suppression-list.md)
      + [Reintentos](using/configuration/retries.md)
      + [Lista de permitidos](using/configuration/allow-list.md)
   + [Uso de listas semilla](using/configuration/seed-lists.md)
   + [Asistencia para el archivado](using/configuration/archiving-support.md)
   + [Cambio de direcciones de ejecución](using/configuration/primary-email-addresses.md)
   + [Configurar reglas empresariales](using/configuration/frequency-rules.md)
   + [Trabajar con conjuntos de reglas](using/configuration/rule-sets.md)
+ configuración de recorrido {#configure-journeys}
   + [Configuración de fuentes de datos, eventos y acciones](using/configuration/about-data-sources-events-actions.md)
   + Configuración de eventos {#events-journeys}
      + [Trabajo con eventos de recorrido](using/event/about-events.md)
      + [Configuración de un evento unitario](using/event/about-creating.md)
      + [Acerca de los esquemas de ExperienceEvent](using/event/experience-event-schema.md)
      + [Trabajo con datos de Adobe Analytics](using/event/about-analytics.md)
      + [Configuración de un evento empresarial](using/event/about-creating-business.md)
      + [Pasos adicionales para enviar eventos](using/event/additional-steps-to-send-events-to-journey.md)
   + Configuración de fuente de datos{#data-source-journeys}
      + [Introducción a las fuentes de datos](using/datasource/about-data-sources.md)
      + [Configuración de una fuente de datos](using/datasource/configure-data-sources.md)
      + [Fuente de datos de Adobe Experience Platform](using/datasource/adobe-experience-platform-data-source.md)
      + [Fuentes de datos externas](using/datasource/external-data-sources.md)
   + Configuración de acción {#action-journeys}
      + [Introducción a las acciones personalizadas](using/action/action.md)
      + [Configuración de una acción personalizada](using/action/about-custom-action-configuration.md)
      + [Resolución de una acción personalizada](using/action/troubleshoot-custom-action.md)
      + [Uso de respuestas de llamadas API en acciones personalizadas](using/action/action-response.md)
+ Conectar sus sistemas y entornos {#connect-systems}
   + [Trabajo con las API de Journey Optimizer](using/configuration/ajo-apis.md)
   + Integración de los recorridos con sistemas externos {#external-systems}
      + [Recorrido de integración con sistemas externos](using/configuration/external-systems.md)
      + [API de límite](using/configuration/capping.md)
      + [API de limitación](using/configuration/throttling.md)
   + Envío con soluciones de Adobe {#adobe-solutions}
      + [Integración de recorrido con Campaign Standard](using/action/acs-action.md)
      + [Integración de recorrido con las versiones 7 y 8 de Campaign](using/action/acc-action.md)
      + [Integración de recorrido con Marketo Engage](using/action/marketo-engage.md)
   + Administración de zonas protegidas {#sandbox}
      + [Uso y asignación de entornos limitados](using/administration/sandboxes.md)
      + [Exportación de objetos a otra zona protegida](using/configuration/copy-objects-to-sandbox.md)
   + [Configuración del conector de fuentes](using/start/get-started-sources.md)
+ Control de acceso {#access-control}
   + Información general sobre el control de acceso {#privacy}
      + [Introducción a la administración de usuarios](using/administration/permissions-overview.md)
      + [Funciones integradas](using/administration/ootb-product-profiles.md)
      + [Permisos integrados](using/administration/ootb-permissions.md)
      + [Niveles de permisos](using/administration/high-low-permissions.md)
   + [Administración de usuarios y funciones](using/administration/permissions.md)
   + [Control de acceso basado en atributos](using/administration/attribute-based-access.md)
   + [Control de acceso de nivel de objeto](using/administration/object-based-access.md)
+ Privacidad {#privacy}
   + [Introducción a la privacidad](using/privacy/get-started-privacy.md)
   + [Solicitudes de privacidad](using/privacy/requests.md)
   + [Acciones de auditoría en recursos](using/privacy/audit-logs.md)
   + [Realizar operaciones de ciclo de vida de datos](using/privacy/data-hygiene.md)
   + Administración del consentimiento {#consent}
      + [Administración de la exclusión](using/privacy/opt-out.md)
      + [Trabajar con políticas de consentimiento](using/action/consent.md)
   + [Gobernanza de datos](using/action/action-privacy.md)
   + [Configurar y administrar claves administradas por el cliente](using/privacy/cmk.md)
