---
solution: Journey Optimizer
product: journey optimizer
title: Actualizaciones de la documentación
description: Más información acerca de las últimas actualizaciones de documentación
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: 99c65643dc029514f452b6ad34a957280a59fe9d
workflow-type: tm+mt
source-wordcount: '3464'
ht-degree: 80%

---

# Actualizaciones de la documentación {#latest-updates}

Esta página incluye todos los cambios más recientes en la documentación de [!DNL Journey Optimizer], además de las actualizaciones relacionadas con las características y mejoras de la versión mensual.

## Febrero de 2026 {#february-2026}

* La documentación de **Búsqueda de eventos de experiencia en recorrido** se ha actualizado con la cronología de desuso: a partir del 1 de abril de 2026, las organizaciones que no hayan utilizado atributos de eventos de experiencia en expresiones de recorrido en los últimos 90 días ya no tendrán acceso a esta capacidad. Ahora, las preguntas más frecuentes se centran en el calendario de jubilaciones y en quién se ve afectado. La página de esquema de Experience Event se ha alineado con un vínculo directo a enfoques alternativos. [Más información](../building-journeys/exp-event-lookup.md)

* La documentación de **Decisioning** se ha actualizado para la **búsqueda de conjuntos de datos** con datos de Adobe Experience Platform: la protección de canales admitidos ahora indica que la búsqueda de conjuntos de datos funciona para todos los canales donde Decisioning está disponible (experiencia basada en código, correo electrónico, push, SMS y la actividad de decisión de contenido en recorrido). Se han eliminado las notas de disponibilidad limitada y beta pública de las páginas de reglas de decisión, fórmulas de clasificación y elementos de decisión. [Más información](../experience-decisioning/aep-data-exd.md)

* La página Integración de sistemas externos se ha actualizado con vínculos a fuentes de datos personalizadas y acciones personalizadas, y aclara que el proxy de salida proporciona una IP estática para llamadas salientes de **acciones personalizadas** a sus sistemas externos. [Más información](../configuration/external-systems.md)

* Se ha aclarado la Recorrido de la ejecución en seco: los atributos de evento de paso `inDryRun` y `dryRunID` ahora documentan que devuelven `true`/ID de instancia cuando se encuentran en el modo de ejecución en seco y `null` para recorridos de prueba o activos. Las directrices para excluir los eventos de paso de ejecución en seco en las consultas de creación de informes se han actualizado en consecuencia. [Más información](../building-journeys/journey-dry-run.md)

* **Web push** ya está disponible de forma general. La documentación de las notificaciones push se ha reestructurado y actualizado en consecuencia (introducción, diseño, envío, creación). [Más información](../push/get-started-push.md)

* La página de configuración de Web push ya está disponible en la documentación. [Más información](../push/push-configuration-web.md)

* Se ha actualizado la documentación sobre el uso de fragmentos en Decisioning: se han añadido notas en las secciones Fragmentos y Decisioning, y se ha actualizado la página Fragmentos en políticas de decisión. [Más información](../experience-decisioning/fragments-decision-policies.md)

* Se ha actualizado la documentación del gancho web SMS: se ha eliminado el contenido del gancho web Twilio. [Más información](../sms/sms-webhook.md)

* Se ha actualizado la documentación de la API de migración de Decisioning. [Más información](../experience-decisioning/decisioning-migration-api.md)

* La actividad **Decisión de contenido** ya está disponible de forma general. La página de actividad de Decisión de contenido se ha actualizado con una sección sobre Datos de toma de decisiones disponibles en eventos de paso. [Más información](../building-journeys/content-decision.md)

* Se han añadido vínculos a la documentación de la API de desafío de fidelidad a la sección Retos de fidelidad (introducción, creación de desafíos, creación de tareas, acceso a desafíos de fidelidad). [Más información](../loyalty-challenges/get-started.md)

* Se ha corregido la información de canales admitidos en la documentación del asistente para la creación de campañas. Las páginas de preguntas frecuentes sobre Introducción a canales y campañas organizadas se han actualizado en consecuencia. [Más información](../campaigns/get-started-with-campaigns.md)

* Se ha corregido la documentación de permisos con respecto a los permisos de **Administración de Recorrido** y **Aprobar**. [Más información](../administration/ootb-permissions.md)

* La documentación de integraciones de AEM (Adobe Experience Manager) se ha actualizado con una nomenclatura revisada (fragmentos de contenido dinámico de AEM y AEM). [Más información](../integrations/aem-fragments.md)

* Se ha agregado un nuevo motivo de exclusión a la lista de exclusiones: **UnsubscribeLinkNotValid** (código de error 050081). Esta exclusión se genera cuando la longitud del asunto de mailTo de cancelación de suscripción a una lista es mayor que el límite RFC de 998 caracteres. [Más información](../reports/exclusion-list.md)

* La documentación de la función de ayuda formatDate se ha mejorado con una nota que indica que la función requiere un tipo de campo de fecha y hora (no una cadena) y con varios ejemplos: formato de un campo de fecha y hora, conversión de una cadena a fecha primero, fecha completa con nombre de día, fecha dinámica desde la hora del sistema y formato de día de la semana, incluido el resultado en minúsculas. [Más información](../personalization/functions/dates.md#format-date)

* La documentación de correo electrónico de la versión de texto se ha mejorado con una guía completa de casos de uso, que incluye criterios de decisión sobre cuándo utilizar texto sin formato personalizado en comparación con la sincronización automática, ejemplos prácticos con escenarios reales y una sección de preguntas frecuentes con preguntas comunes. [Más información](../email/text-version-email.md#when-to-use)

* Se ha añadido una limitación a la documentación del asistente de Metadatos de ejecución para aclarar que los metadatos no se capturan para los perfiles excluidos de la acción. [Más información](../personalization/functions/helpers.md#execution-metadata)

* La documentación de ejemplos de implementación basada en código se ha actualizado para incluir el campo de tokens en propositionAction para un seguimiento y una atribución precisos en Decisioning. [Más información](../code-based/code-based-implementation-samples.md#client-side-how)

* Se ha añadido una nota a la documentación de seguimiento de URL y cancelación de suscripción de lista para aclarar que el orden de los parámetros de seguimiento de URL anexados a las URL es aleatorio y no se puede controlar. [Más información](../email/url-tracking.md)

* La documentación de los temas de Designer de correo electrónico se ha actualizado con información sobre las limitaciones de compatibilidad con fuentes web y la importancia de las fuentes de reserva. [Más información](../email/apply-email-themes.md#themes-guardrails)

## Enero de 2026 {#january-2026}

* La documentación del tablero de uso de licencias se ha aclarado con directrices actualizadas sobre **Perfiles atractivos**, incluidos detalles de definición e instrucciones para la solución de problemas. [Más información](../audience/license-usage.md#what-is-engageable-profile)

* Se ha añadido una nota a la documentación de temáticas de Designer de correo electrónico para aclarar las limitaciones de compatibilidad con fuentes web. [Más información](../email/apply-email-themes.md#themes-guardrails)

* Se ha añadido una nueva sección de mecanismo de protección a la validación del tamaño de la carga útil del recorrido del documento, que incluye umbrales de advertencia y error y directrices sobre cómo optimizar los recorridos. [Más información](../start/guardrails.md#journey-payload-size)

* La documentación de las secciones de mecanismo de toma de decisiones se ha actualizado para incluir limitaciones de tamaño de elementos de decisión (1 KB para elementos que incluyen atributos con un máximo de 30 atributos). [Más información](../experience-decisioning/decisioning-guardrails.md)

* Se ha añadido una nota a la documentación de creación de políticas de decisión para informar a los usuarios de que, una vez creada una política de decisión, cualquier cambio puede tardar hasta 15 minutos en propagarse por todas las regiones de datos y hasta 30 minutos para Canadá. [Más información](../experience-decisioning/create-decision-policy.md#review)

* Se ha añadido una nota a la documentación de fragmentos para advertir que cuando la etiqueta del botón y la URL se pueden editar en un fragmento, el conjunto de datos de seguimiento registra el valor de la URL en lugar del valor de la etiqueta. [Más información](../content-management/customizable-fragments.md#visual)

* Ya está disponible una nueva página que describe las ventajas de migrar de Gestión de decisiones a Toma de decisiones, incluida la información sobre las próximas API de herramientas de migración. [Más información](../experience-decisioning/migrate-to-decisioning.md)

* Se ha añadido un mecanismo de protección para aclarar que los conjuntos de datos de búsqueda solo están disponibles para la activación entrante basada en Edge en la región donde reside la zona protegida del conjunto de datos. [Más información](../data/lookup-aep-data.md#guidelines)

* Se ha añadido una nueva sección a la documentación de configuración del canal de campañas orquestadas que explica cómo utilizar atributos contextuales (como ID de campaña, nombre y detalles de acción) en los parámetros de seguimiento de URL con fines de análisis y de creación de informes. [Más información](../orchestrated/channel-config.md#url-tracking)

* La documentación de la optimización de contenido se ha reestructurado para una mejor claridad. La página de optimización principal se ha dividido en cuatro subpáginas centradas: una página de introducción, una página dedicada a la segmentación, una a la experimentación y otra a la combinación de ambos métodos. [Más información](../content-management/gs-message-optimization.md)

* Las notas de disponibilidad limitada se han eliminado de tres recorridos de alertas (recorrido publicado, recorrido finalizado y límite de acción personalizada activado), ya que estas funciones ya están disponibles de forma generalizada. [Más información](../reports/alerts.md)

* La página de destino de Prueba, validación y aprobación se ha mejorado con nuevas secciones que incluyen funciones de prueba, información general, preguntas frecuentes comunes, árbol de decisiones con vínculos de navegación y terminología mejorada con vínculos a documentación. [Más información](../../rp_landing_pages/test-landing-page.md)

* Se ha añadido una nueva sección a la documentación de sintaxis de personalización para aclarar cómo utilizar palabras clave reservadas en expresiones de personalización. Algunas palabras clave de PQL, como `next`, `last` y `this`, deben evitarse con comillas invertidas cuando se utilizan como nombres de campo en el esquema XDM. [Más información](../personalization/personalization-syntax.md#reserved-keywords)

* Las páginas de [Introducción a las campañas](../campaigns/get-started-with-campaigns.md) y [Administrar campañas](../campaigns/manage-campaigns.md) se han reestructurado con una arquitectura de información mejorada, que incluye un flujo de trabajo completo con guías específicas del tipo, comparaciones mejoradas de tipos de campañas y una tabla de estado consolidada.

* La página de destino de Recorridos se ha rediseñado para facilitar la incorporación con un nuevo flujo de trabajo de 6 pasos, comparaciones de tipo de recorrido mejoradas y una navegación mejorada por toda la documentación. [Más información](../building-journeys/journey.md)

* Se ha añadido una sección detallada para ayudar a los usuarios a generar claves privadas OpenSSH codificadas en Base64 para la autenticación SFTP al configurar el enrutamiento de archivos para correo directo a fin de evitar errores de conexión. [Más información](../direct-mail/direct-mail-configuration.md#ssh-key-generation)

* Se ha añadido una nota a la documentación de delegación de subdominios para informar a los usuarios de que deben dejar pasar de 24 a 48 horas para la propagación de DNS antes de intentar la delegación a Adobe. [Más información](../configuration/delegate-subdomain.md#set-up-subdomain)

## Diciembre de 2025 {#december-2025}

* La documentación de públicos de carga personalizados para la toma de decisiones se ha actualizado para incluir un indicador de API necesario para recuperar datos de enriquecimiento. Cuando utilice públicos cargados en CSV en toma de decisiones sobre ofertas, debe incluir `"xdm:enrichedAudience": true` en la carga útil de solicitud de API para recuperar atributos de enriquecimiento en la respuesta de decisión de oferta. [Más información](../offers/custom-upload-decisioning.md#must-read)

* Se ha añadido una nota en la documentación de envío de pruebas para aclarar que las reglas de restricción de frecuencia se aplican a las pruebas. La página ahora incluye una sección &quot;Lectura obligatoria&quot; con consideraciones importantes sobre el comportamiento de restricción de frecuencia, las limitaciones de páginas espejo y las reglas de accesibilidad de recursos. [Más información](../content-management/proofs.md)

* Se ha añadido una nueva tabla de disponibilidad de canales de comunicación a la página Introducción a los canales, que muestra qué canales son compatibles con todos los recorridos y campañas (campañas de acción, campañas activadas por API y campañas orquestadas). [Más información](../channels/gs-channels.md#channels)

* Se ha creado una nueva página de destino de seguimiento completa para ayudar a los usuarios a descubrir y acceder a todas las funcionalidades de seguimiento y monitorización disponibles en Journey Optimizer. [Más información](../start/get-started-tracking.md)

* La página de administración de exclusión de correo electrónico se ha mejorado con información detallada sobre el flujo de cancelación de suscripción, que explica el orden esperado de los eventos para la exclusión de la página de aterrizaje. [Más información](../email/email-opt-out.md#send-message-unsubscribe-link)

* La documentación de la lista de suscripción se ha actualizado para incluir información sobre los criterios de idoneidad del segmento de streaming. [Más información](../landing-pages/subscription-list.md#define-subscription-list)

* Hay disponible una nueva guía de entregabilidad de calentamiento de IP que proporciona directrices completas sobre los fundamentos de reputación, la preparación previa al vuelo, las métricas de monitorización y las prácticas recomendadas para la transición de una reputación cero a una ubicación correcta en la bandeja de entrada. [Más información](../configuration/ip-warmup-deliverability-guide.md)

* Se ha añadido una advertencia a las secciones Página de aterrizaje y Exclusión de correo electrónico para aclarar que al hacer clic en un vínculo para cancelar la suscripción solo se abre la página de aterrizaje, pero los usuarios deben enviar el formulario para completar el proceso de exclusión. [Más información](../landing-pages/lp-use-cases.md#configure-opt-out)

* Ya está disponible una nueva biblioteca de casos de uso de recorrido que reúne una colección de casos de uso prácticos, incluidos patrones tácticos (lógica de supresión, técnicas de personalización, estrategias de salida de recorrido) y escenarios completos de extremo a extremo que abarcan flujos de trabajo técnicos y de marketing. [Más información](../building-journeys/jo-use-cases.md)

* Ya está disponible un nuevo caso de uso que muestra cómo configurar un recorrido para enviar correos electrónicos solo entre semana (lunes a viernes), con colas automáticas para que las entradas de fin de semana se envíen el lunes a una hora especificada. [Más información](../building-journeys/weekday-email-uc.md)

* Ya está disponible una nueva página que explica las capacidades de decisión de Journey Optimizer, incluidas las diferencias entre el marco de toma de decisiones de próxima generación y la solución de gestión de decisiones establecida, y sus ventajas clave para ofrecer ofertas personalizadas en todos los canales. [Más información](../experience-decisioning/gs-decision.md)

* Se ha añadido una nueva sección a la documentación de activación de públicos que explica cómo activar tipos de públicos no compatibles (como públicos de Customer Journey Analytics) en [!DNL Journey Optimizer] ajustándolos en una nueva definición de segmento en Audience Portal. [Más información](../audience/target-audiences.md#activation-non-supported)

* Se ha añadido una nueva sección a la documentación de actividad de espera que explica cómo los perfiles estacionados en una actividad de espera en recorridos de Read Audience actualizan automáticamente sus atributos desde el servicio de perfil unificado (UPS). Esto aclara que los datos de perfil pueden cambiar durante la ejecución del recorrido después de un nodo de espera, lo que puede producir resultados inesperados si espera datos de instantánea coherentes en todo el recorrido. [Más información](../building-journeys/wait-activity.md#profile-refresh)

* Se ha añadido una nota de precaución a la sección Experimentación de rutas en la que se advierte a los usuarios de que no editen los metadatos de un experimento de rutas una vez publicado, ya que esto interrumpirá el cálculo y la creación de informes de los resultados del experimento. [Más información](../building-journeys/optimize.md#experimentation)

* Se ha añadido una nota a la sección Crear un ajuste preestablecido de formulario para especificar los requisitos para que las conexiones de streaming se muestren en la lista desplegable de selección. [Más información](../landing-pages/lp-forms.md#create-form-preset)

* Ahora hay disponible una nueva página en la sección Decisiones sobre cómo configurar la recopilación de datos para el seguimiento de impresiones, clics y eventos personalizados. [Más información](../experience-decisioning/data-collection/schema-requirement.md)

* La documentación de generación de contenido con el Asistente de IA se ha reorganizado para mejorar la claridad y facilidad de uso. Las cinco páginas específicas del canal anterior (correo electrónico, push, SMS, web y página de aterrizaje) se han consolidado en tres páginas de tipo generación: [Generar contenido completo](../content-management/generative-full-content.md), [Generar texto](../content-management/generative-text.md) y [Generar imágenes](../content-management/generative-image.md).

## Noviembre de 2025 {#november-2025}

* Ya está disponible una nueva página de preguntas frecuentes sobre Decisioning que cubre temas como reglas de límite, configuración del modelo de IA, requisitos de tráfico y estrategias de optimización de ofertas. [Más información](../experience-decisioning/decisioning-faq.md)

* La página de Introducción al diseño del correo electrónico se ha actualizado para aclarar cómo acceder al Diseñador de correo electrónico. [Más información](../email/get-started-email-design.md)

* Se ha añadido una sección de solución de problemas a la página de registro DMARC para abordar la latencia de propagación de DNS. [Más información](../configuration/dmarc-record.md#troubleshooting)

* La página Trabajar con GenStudio for Performance Marketing se ha mejorado con nuevas secciones que incluyen funcionalidades clave, casos de uso comunes, requisitos previos y preguntas frecuentes. [Más información](../integrations/genstudio.md)

* Se ha añadido un mecanismo de protección en la segmentación de perfiles seudónimos con canales de entrada a la página Mecanismos de protección y limitaciones: la segmentación de visitantes no autenticados aumenta el recuento total de perfiles atractivos, por lo que Adobe recomienda configurar un período de vida TTL (Time-To-Live) para la eliminación automática de perfiles a fin de administrar los costes asociados. [Más información](../start/guardrails.md#profile-management-inbound)

* Ahora se incluyen dos tutoriales sobre la configuración del SDK web para la toma de decisiones y experiencias basadas en código en la página de muestras Métodos de implementación basados en código. [Más información](../code-based/code-based-decisioning-implementations.md#tutorials)

* Se ha añadido una nota para especificar que los recursos y las imágenes siguen siendo accesibles durante un máximo de 2 años (730 días) desde la primera publicación y que es necesario volver a publicarlos una vez caducados. [Más información](../content-management/proofs.md)

* Ya está disponible una guía completa sobre cómo dar indicaciones de contenido al asistente de IA. Esta guía le enseña a dar indicaciones eficientes para crear contenido de marketing de alta conversión y alineado con la marca. Obtenga más información sobre las prácticas recomendadas para escribir objetivos de marketing, utilizar recursos de marca y optimizar contenido para diferentes canales. [Más información](../content-management/ai-assistant-prompting-guide.md)

* Se ha añadido una nota a la documentación de definición del segmento para aclarar que el uso del atributo `frequencyMap` no se admite en definiciones de segmento y no se puede usar como parte de los criterios de segmentación de público. Para la segmentación basada en la frecuencia, considere utilizar reglas de restricción de frecuencia en reglas empresariales. [Más información](../audience/creating-a-segment-definition.md)
* Se ha añadido un nuevo ejemplo que muestra cómo utilizar respuestas de acción personalizadas en canales nativos a la documentación de respuestas de llamada de API. En el ejemplo se muestra cómo repetir matrices anidadas a partir de respuestas de acciones personalizadas mediante la sintaxis Handlebars en mensajes de correo electrónico, push y SMS. [Más información](../action/action-response.md#response-in-channels)

* Se ha añadido una nueva sección a la documentación de integración de las versiones 7 y 8 de Campaign que explica cómo actualizar las acciones personalizadas existentes cuando cambia el punto final en tiempo real (RT). La sección incluye instrucciones paso a paso para actualizar la URL del punto final, probar la conexión y validar los cambios antes de guardar. [Más información](../action/acc-action.md#update-action)

* Se han añadido nuevas secciones de limitaciones y prácticas recomendadas a la documentación de fragmentos visuales para advertir a los usuarios sobre el anidamiento no admitido de fragmentos con contenido dinámico dentro de otros fragmentos desbloqueados con contenido dinámico. Las directrices incluyen pasos para la resolución de problemas relacionados con el modo de compatibilidad y recomendaciones para un diseño adecuado de la estructura de correo electrónico. [Más información](../email/use-visual-fragments.md#fragment-dynamic-content)

* Se ha añadido una sección de resolución de problemas a la documentación de creación de informes en tiempo real del recorrido para ayudar a los usuarios a solucionar los problemas relacionados con la falta de datos en los informes. La sección abarca la sincronización del nombre del recorrido con conjuntos de datos de creación de informes, temporización de actualización de datos, verificación de permisos de acceso y requisitos de estado de recorrido. [Más información](../building-journeys/report-journey.md#troubleshooting-missing-data)

* Se han añadido tres nuevos elementos de preguntas frecuentes a la documentación de recursos con información sobre la caducidad del recurso y la administración del ciclo de vida. Los temas tratados incluyen la directiva Tiempo de vida (TTL) para los recursos de AEM (730 días), cómo resolver imágenes dañadas debido a la caducidad del recurso e información sobre próximas mejoras en la lógica de caducidad del recurso. [Más información](../integrations/assets.md#faq-assets)

* Se ha añadido una sección completa de resolución de problemas a la documentación de actividad de público de lectura para resolver las discrepancias de recuento de público entre los perfiles estimados y reales que entran en los recorridos. La sección abarca los problemas de temporización y propagación de datos, las técnicas de validación y monitorización de datos, y las prácticas recomendadas, incluido el uso de la opción “Activar después de la evaluación del público por lotes”. [Más información](../building-journeys/read-audience.md#audience-count-mismatch)

* Se ha añadido una nota a la documentación de eventos de calificación de público para aclarar la latencia de segmentación de streaming (hasta 2 horas) y recomendar que se añada una actividad de espera o un tiempo de búfer para recorridos con limitación de tiempo. [Más información](../building-journeys/audience-qualification-events.md#streamed-speed-segment-qualification)

* Se ha añadido una nueva sección a las protecciones de correo electrónico que documentan el límite de tamaño del contenido de los mensajes de 2 MB para la publicación del recorrido, incluidas las prácticas recomendadas para mantener el contenido creado por debajo de 1 MB para permitir la sobrecarga de procesamiento del back-end. [Más información](../start/guardrails.md#message-content-size)

* Documentación mejorada para la opción de lectura incremental en actividades de público de lectura para aclarar las dependencias de temporización de instantáneas y la limitación retrospectiva de 24 horas, incluidas las recomendaciones para evitar la pérdida de perfiles. [Más información](../building-journeys/read-audience.md)

* Se añadió una nota a las protecciones de búsqueda del conjunto de datos para especificar que las búsquedas no se pueden encadenar. [Más información](../data/lookup-aep-data.md#guidelines)

* Los canales de WhatsApp y LINE ya están disponibles para las campañas de Acción. [Más información](../campaigns/campaign-content.md)

* Se ha añadido una nueva sección completa sobre la tasa de procesamiento de recorridos a la documentación de administración de entradas, que incluye las tasas de entrada de perfil, los eventos y las cualificaciones de público dentro de los recorridos, el impacto de las actividades de espera y el impacto de las actividades de acción. [Más información](../building-journeys/entry-management.md#journey-processing-rate)

* Al diseñar mensajes de correo electrónico, el sistema ahora comprueba la configuración de las claves y muestra alertas para detectar advertencias y errores. Se ha añadido información sobre las alertas de correo electrónico y los requisitos de validación a la página Mecanismos de protección. [Más información](../email/create-email.md#check-email-alerts)

* Se ha eliminado de la página Añadir restricciones a una oferta la nota de advertencia que indica que la restricción de frecuencia no se puede habilitar o deshabilitar para ofertas creadas anteriormente. [Más información](../offers/offer-library/add-constraints.md#capping)

* Ya está disponible la documentación sobre cómo trabajar con eventos de paso de recorrido. [Más información](../reports/journey-step-events-overview.md)

* Ya está disponible una nueva guía completa sobre los criterios de entrada y salida de recorrido que abarca las prácticas recomendadas, los ejemplos reales y las directrices prácticas para administrar cuándo los perfiles entran y salen de los recorridos en Adobe Journey Optimizer. [Más información](../building-journeys/entry-exit-criteria-guide.md)

* Ya está disponible una nueva página que explica cómo iterar en los datos contextuales de los mensajes. Esta guía explica cómo utilizar la sintaxis de Handlebars para mostrar listas dinámicas a partir de eventos, respuestas de acciones personalizadas, búsquedas de conjuntos de datos y otras fuentes de contexto en la personalización. [Más información](../personalization/iterate-contextual-data.md)

* La consulta para identificar eventos descartados en recorridos se ha corregido para incluir filtros adecuados para errores de trabajos de exportación de segmentos, descartes del Dispatcher y descartes de equipos de estado. [Más información](../reports/query-examples.md#common-queries)

* Se han añadido frases de introducción a los 37 ejemplos de consultas de la documentación de ejemplos de consultas para proporcionar un mejor contexto y explicar qué hace cada consulta antes de presentar el código SQL. Esto mejora la comprensión del usuario y proporciona una orientación más clara sobre cuándo utilizar cada consulta. [Más información](../reports/query-examples.md)

## Octubre de 2025 {#october-2025}

* Ahora puede convertir imágenes a plantillas de HTML mediante el convertidor de imágenes a HTML. [Más información](../content-management/image-to-html.md)

* Ya está disponible la información sobre el ciclo de lanzamiento de Adobe Journey Optimizer. [Más información](releases.md)

* Ya está disponible la nueva página de Preguntas más frecuentes de recorridos. [Más información](../building-journeys/journey-faq.md)

* Ya está disponible la funcionalidad Monitorizar las acciones personalizadas. [Más información](../action/reporting.md)

* Ya está disponible el modo de alto rendimiento para campañas activadas por API. [Más información](../campaigns/api-triggered-high-throughput.md)

* Ya está disponible una referencia de códigos de error para los recorridos. [Más información](../building-journeys/error-codes-reference.md)

* Ya está disponible la documentación de Journey Optimizer Experimentation Accelerator. [Más información](../content-management/experiment-accelerator-gs.md)

* Se ha añadido una nueva sección a la documentación de la función auxiliar **formatDate**. Esta sección aclara el significado de los símbolos de patrones clave como y, Y, M, d y D. [Más información](../personalization/functions/dates.md#pattern-characters)

* Se ha añadido un ejemplo de PQL a la sección de fórmula de clasificación de Decisioning para mostrar cómo impulsar ofertas basadas en el código postal y los ingresos anuales de un perfil. [Más información](../experience-decisioning/ranking/ranking-formulas.md#ranking-formula-examples)

* Se ha añadido una limitación a la sección del modo de prueba de recorrido para indicar que el modo de prueba no admite el enriquecimiento de atributos de público de carga personalizada. [Más información](../building-journeys/testing-the-journey.md#important_notes)

* Se añadió una nueva sección a las páginas [Limitaciones y mecanismos de protección de gestión de decisiones](../offers/decision-management-guardrails.md#configurations) y [Limitaciones y mecanismos de protección de decisiones](../experience-decisioning/decisioning-guardrails.md#configurations) para especificar el número máximo de configuraciones admitidas (20 000), correspondiente al número total de reglas de límite que existen en la zona protegida.

* Se ha añadido una nota en la sección de actividad Condición del recorrido para documentar que la evaluación de la condición fallará para perfiles que contengan más de dos identidades entre dispositivos. [Más información](../building-journeys/condition-activity.md)

* Se ha añadido una nueva página para describir cómo puede utilizar las políticas de consentimiento para satisfacer las preferencias de los clientes según sus opciones y, al mismo tiempo, respetar su consentimiento. [Más información](../action/preference-center.md)

* Se ha añadido una nota a las páginas Introducción a los perfiles y mecanismos de protección para especificar que, en la ingesta de datos, los correos electrónicos distinguen entre mayúsculas y minúsculas, lo que significa que se pueden crear y utilizar perfiles duplicados al dirigirse al destinatario correspondiente. [Más información](../audience/get-started-profiles.md)

* Se ha introducido el nuevo atributo `render` en el editor de personalización. Establézcalo en `false` en los casos en que desee ocultar el contenido de un fragmento de expresión. [Más información](../personalization/use-expression-fragments.md#use-expression-fragment)

* Se ha añadido una lista de mecanismos de protección a la sección que describe cómo aprovechar los fragmentos adjuntos a los elementos de decisión dentro de las políticas de decisión. [Más información](../experience-decisioning/use-decision-policy.md#fragments)

* Prácticas recomendadas añadidas para búsquedas de conjuntos de datos: mantenga activados los conmutadores para evitar problemas de indexación y conozca cómo las eliminaciones de lotes afectan a los datos de búsqueda. [Más información](../data/lookup-aep-data.md#guidelines)

* Se ha añadido una limitación que indica que solo se admiten públicos del servicio de perfil unificado al utilizar recorridos de público de lectura con identificadores suplementarios. [Más información](../building-journeys/supplemental-identifier.md#guardrails)

* La documentación de Experimentation Accelerator se ha trasladado a una colección independiente. [Más información](https://experienceleague.adobe.com/es/docs/experimentation-accelerator/using/overview)

## Septiembre de 2025 {#september-2025}

* Se ha añadido una nueva sección de canal de entrada a la página Mecanismos de protección y limitaciones para recopilar todas las limitaciones que se aplican a los canales web, en la aplicación, experiencias basadas en código y tarjetas de contenido. Incluye el límite de volumen máximo de 5000 solicitudes de entrada por segundo para todas las solicitudes de entrada y el máximo de 500 acciones de entrada activas. [Más información](../start/guardrails.md#inbound-guardrails)

* Se ha lanzado una página de preguntas más frecuentes para campañas organizadas. [Más información](../orchestrated/orchestrated-campaigns-faq.md)

* Se ha añadido una sección de solución de problemas a la documentación de eventos de paso de Recorrido con definiciones, causas comunes y pasos de solución de problemas para los tipos de eventos de descarte más frecuentes. [Más información](../reports/sharing-field-list.md#discarded-events)

* La documentación sobre cómo utilizar identificadores suplementarios en recorridos ahora incluye una tabla que detalla cómo se comportan los perfiles cuando se aplican criterios de salida en recorridos que utilizan ID suplementarios. [Más información](../building-journeys/supplemental-identifier.md#exit-criteria)

* Se ha añadido una sección de solución de problemas para comprender los descartes de perfil en recorridos pausados. [Más información](../building-journeys/journey-pause.md#discards-troubleshoot)

* Se ha añadido información en la documentación de información general de esquemas para diferenciar los esquemas estándar y relacionales utilizados para campañas orquestadas. [Más información](../data/gs-data.md)

* Se ha añadido información en la documentación de Toma de decisiones y Gestión de decisiones sobre los requisitos para entrenar correctamente los modelos de [optimización automática](../experience-decisioning/ranking/auto-optimization-model.md) y [optimización personalizada](../experience-decisioning/ranking/personalized-optimization-model.md).

* Se ha aclarado que las llamadas a la API de REST de ejecución de mensajes interactivos tienen un tiempo de espera de 60 segundos, con reintentos internos para garantizar el envío. [Más información](../campaigns/trigger-campaigns.md)

* La página de colecciones de elementos de Decisioning se actualizó para aclarar el comportamiento del operador **CONTAINS** al definir reglas. [Más información](../experience-decisioning/collections.md)

* La página Asignar puntuaciones de prioridad se ha actualizado con los pasos específicos para definir una puntuación de prioridad para las acciones del canal de entrada dentro de la actividad **Acción**. [Más información](../conflict-prioritization/priority-scores.md#priority-action)

<!--
## August 2025 {#august-2025}

* A new page listing the best practices for designing accessible email and landing page content with [!DNL Journey Optimizer] was added. [Read more](../email/accessible-content.md)

* The documentation for supplemental identifiers in journeys has been updated with the following clarifications:

    * After adding a supplemental identifier to a schema, a new event (for event-triggered journeys) or a new field group (for Read audience journeys) must be created. Existing entities do not refresh automatically and will not recognize the new identifier.

    * Supplemental identifiers are not validated against Data Usage Labeling & Enforcement (DULE) policies and are not considered during data governance checks in journeys.

        [Read more](../building-journeys/supplemental-identifier.md)

* The Optimization in campaigns page was updated to reflect the fact that optimization is now also available in journeys. [Read more](../content-management/gs-message-optimization.md)

* A link to the tutorial video describing how to leverage message optimization in a campaign was added. [Read more](../content-management/gs-message-optimization.md)

## July 2025 {#july-2025}

* The campaigns interface now features two separate tabs: **Action** and **API Triggered**. The documentation has been updated accordingly, with information for each campaign type organized into dedicated sections to improve clarity and usability. [Read more](../campaigns/get-started-with-campaigns.md)

* The [Get started with subdomain delegation](../configuration/about-subdomain-delegation.md) and [Delegate a subdomain](../configuration/delegate-subdomain.md) pages have been updated to better present the different delegation methods and the steps to set them up.

* A note has been added to the Fragments section, specifying that when tracking is enabled in a journey or a campaign, if links are present in a fragment and if this fragment is used in a message, these links are tracked such as all other links included in the message. [Learn more](../content-management/create-fragments.md#content)

* The guardrails and limitations applying to subdomain delegation in Journey Optimizer have been enriched and consolidated into one dedicated section. [Read more](../configuration/delegate-subdomain.md#guardrails)

* A note has been added to the Create fallback offers and Create decision pages to mention that fallback offers should contain all representations used within a decision. [Read more](../offers/offer-library/creating-fallback-offers.md)

* The guardrails applying to fragments have been enriched. [Read more](../start/guardrails.md#fragments-guardrails).

* A note has been added to specify that links added to messages expire after 25 months and links to mirror pages after 90 days. [Read more](../email/message-tracking.md)

<!--* The possible email error types that could happen upon sending email deliveries with are now listed in a dedicated section. [Read more](../configuration/email-error-types.md)-->

<!--
## June 2025 {#june-2025}

* Added a new section on how to add and use rich text such as line breaks, bold, italics etc., to customizable fragments by using HTML components. [Read more](../content-management/customizable-fragments.md#rich-text)

* The Decisioning part has been updated with a specific section dedicated to building AI models. [Read more](../experience-decisioning/ranking/ai-models.md)

* Added a recommendation about the usage of the `actionExecutionTime` field in the journeyStep events action. [Read more](../reports/sharing-execution-fields.md#actionexecutiontime-field)

* Added a note about the `messageID` which may not be unique for each individual delivery. [Read more](../data/datasets-query-examples.md)

* Added a recommendation about historical events management in data hygiene operations. [Read more](../privacy/data-hygiene.md#data-hygiene-recommendations)

* Added a guardrail about landing pages not being supported for migration between sandboxes. [Read more](../configuration/copy-objects-to-sandbox.md#global)

* Added a caution note about nested JSON objects not supported in custom authentication for custom actions. [Read more](../datasource/external-data-sources.md)

* Added a caution note about conditional content variant naming in the Email designer. [Read more](../personalization/create-conditions.md)

* Updated the "Undelegate a landing page subdomain" section. [Read more](../landing-pages/lp-subdomains.md#undelegate-subdomain)

* Clarified journey reentrance rules when using supplemental identifiers. [Read more](../building-journeys/supplemental-identifier.md#guardrails)

* Added a new note to clarify that you must use the expression editor in Advanced mode when selecting the supplemental identifier attribute during event configuration. [Learn more](../building-journeys/supplemental-identifier.md#add)

* Added clarification on how journey reentrance works with supplemental identifiers. [Learn more](../building-journeys/supplemental-identifier.md#guardrails)

## May 2025 {#may-2025}

* Adobe integrations available with Journey Optimizer are now listed in the "Connect your systems and environments" section. [Read more](../integrations/ajo-integrations.md)

* The content integrations are now grouped in the Content Management section. [Read more](../integrations/content-integrations.md)

* Architecture diagrams for Adobe Experience Platform and Journey Optimizer have been updated. [Read more](../start/get-started.md#architecture)

* Added a video about the personalization editor playground to help you learn how to write and test personalization code using sample data. [Read more](../personalization/personalize.md#video-perso)

* The maximum number of addresses in a seed list has been increased from 50 to 300. [Read more](../configuration/seed-lists.md#create-seed-list)

* A new step detailing how to wrap code when using decision policies in the code-based experience editor has been added to the Create decision policies page. [Read more](../experience-decisioning/create-decision.md#create-decision)

* A note has been added to the Code-based experiences documentation to specify that when you have multiple code-based experience actions running on the same surface, the campaign or journey's priority score determines what is delivered to the end-user if they qualify for more than one action. [Read more](../code-based/code-based-surface.md#surface-definition)

* A new page on troubleshooting inbound actions in journeys provides a step-by-step guide to identify and resolve issues independently before reaching out to support. [Read more](../building-journeys/troubleshooting-inbound.md)

* A new [page](../code-based/code-based-decisioning-implementations.md) has been added to describe how to add the following flags to your client implementation when using decisioning in code-based experiences:

    * Adding the `dryRun` flag to test decisioning in code-based experiences. [Read more](../code-based/code-based-decisioning-implementations.md#code-based-test-decisions)

    * Apply deduplication to decisioning requests in code-based experiences. [Read more](../code-based/code-based-decisioning-implementations.md#code-based-decisioning-deduplication)

## April 2025 {#apr-2025}

* The Configuration chapter is now split into three chapters: [Channel configuration](../configuration/get-started-configuration.md), [Journey configuration](../configuration/about-data-sources-events-actions.md), and [Connect your systems](../configuration/ajo-apis.md).
* Added a caution note about using experience events in journey expressions and conditions. [Read more](../building-journeys/expression/expressionadvanced.md#discovering-the-interface)
* Added a note on the Direct mail configuration page about temporary storage of the output file. [Read more](../direct-mail/direct-mail-configuration.md)
* Added a tip in the journey advanced expression editor section about the condition format guidelines. [Read more](../building-journeys/expression/expressionadvanced.md)
* Added a caution note in the `inAudience` function section about impacts and best practices when renaming an audience. [Read more](../building-journeys/functions/functioninaudience.md)
* Added a recommendation about the native keywords usage when using two-way SMS. [Read more](../sms/sms-opt-out.md)
* Updated the journey test page with a note about the need for including an identity namespace in the event used. [Read more](../building-journeys/testing-the-journey.md)
* Currently, you cannot undelegate subdomains through the [!UICONTROL Journey Optimizer] user interface - you must reach out to your Adobe representative. Steps to undelegate a subdomain are now detailed for [Emails](../configuration/delegate-subdomain.md#undelegate-subdomain), [SMS](../sms/sms-subdomains.md#undelegate-subdomain), [Web experiences](../web/web-delegated-subdomains.md#undelegate-subdomain), and [Landing pages](../landing-pages/lp-subdomains.md#undelegate-subdomain).<!--[Read more](../configuration/delegate-subdomain.md#undelegate-subdomain)-->
<!--
* Added clarification about the optional `maxHttpConnections` parameter in the journeys Capping API, including guidance on how to use it alongside throttling configurations for the same endpoint. [Read more](../configuration/throttling.md)
* In the Decisioning section, added guidance explaining that approved offer items cannot be deleted if they are used in a collection or a decision. Included steps to change their status to "Draft" using the **[!UICONTROL Undo approve]** option. [Read more](../experience-decisioning/items.md#manage)
* Information on sandboxes have been grouped together into a new "Sandboxes management" section. This new section provides information on how to use and assign sandboxes, and how to use package export and import capabilitie to copy objects such as journeys, content templates, or fragments, across multiple sandboxes. [Read more](../administration/sandboxes.md)

## March 2025 {#mar-2025}

* The page about Audience Qualification events has been updated with new recommendations. [Read more](../building-journeys/audience-qualification-events.md)
* Custom action troubleshooting capability is now available to all customers (GA). [Read more](../action/troubleshoot-custom-action.md)
* Data Hygiene is now Data Lifecycle in the product user interface. The documentation has been updated to reflect this change. [Read more](../privacy/data-hygiene.md)
* The missing Landing Page built-in permissions have been added to the documentation. [Read more](../administration/ootb-permissions.md)
* A note has been added about scheduling recurring campaigns. [Read more](../campaigns/create-campaign.md)
* The section about inserting links and enabling tracking in an email message has been updated and reorganized. [Read more](../email/message-tracking.md)
* The section about personalization capabilities into Adobe Journey Optimizer has been reorganized and improved. [Read more](../personalization/personalize.md)
* Decision management API to list personalized offers has been updated with a sample to perform pagination if multiple personalized offers are missing from the response. [Read more](../offers/api-reference/offers-api/personalized-offers/offers-list.md)
* A new page gathering all information regarding the List unsubscribe feature has been created for improved clarity. [Read more](../email/list-unsubscribe.md)
* The Frequency capping section has been updated with information on how the frequency capping counter is updated for the Decisioning and Batch Decisioning APIs, in addition to the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)

## February 2025 {#feb-2025}

* The Read Audience activity guardrails have been updated to specify that only one activity can be used in a journey and that it can target only one audience. [Read more](../building-journeys/read-audience.md)
* Journey guardrails when using Adobe Campaign activities have been updated. [Read more](../start/guardrails.md#ac-g)
* Steps to create your first journeys have been detailed, and links to documentation section have been added. [Read more](../building-journeys/journey-gs.md)
* A new page is now available to detail the journey dashboard and filtering user interface. [Read more](../building-journeys/journey-ui.md)
* Documentation for **[!UICONTROL Send-Time optimization]** and its related FAQ have been updated, improved and moved to a new dedicated page. [Read more](../building-journeys/send-time-optimization.md)
* New guardrails have been added for journey events. [Read more](../start/guardrails.md#events-g)
* The built-in channel actions page has been reorganized. [Read more](../building-journeys/journeys-message.md)
* Guardrails & limitations have been added in the Decisioning and Decision management sections.
    * [Decisioning guardrails & limitations](../experience-decisioning/decisioning-guardrails.md)
    * [Decision management guardrails & limitations](../offers/decision-management-guardrails.md)
* A new section on context data has been added in the Decision management documentation. It provides information on how to leverage context data in the decisioning engine, for example to design a decision rule that requires the current weather to be ≥80 degrees at the time the decision request is made. [Read more](../offers/context-data.md)

## January 2025 {#jan-2025}

* A new section on the **[!UICONTROL Execution address]** option in the email configuration has been added. The primary address is defined at the sandbox level, but the default setting can be overidden for a specific email configuration. [Read more](../email/email-settings.md#execution-address)

* The **Get started with deliverability** page has been updated with the possibility to create IP warmup workflows directly from the user interface. [Read more](../reports/deliverability.md#reputation)

* The **Header parameters** section has been updated to reflect the new labels and changes in the user interface. [Read more](../email/email-settings.md#email-header)

* The **Forward email** section has been updated to specify that all emails sent to the **From email** address are forwarded to the forward email address. If no forward email is specified, these emails are discarded. [Read more](../email/email-settings.md#email-settings)

* The maximum size of contextual attributes passed into an API-triggered campaign request has been updated to 200kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)

* A new section has been added to the **Manage fragments** page to describe how to add new attributes to a live fragment. The whole page has also been improved. [Read more](../content-management/manage-fragments.md#adding-new-attributes)

* A "Guardrails & limitations" section has been added to the conflict management & prioritizations tools documentation. [Read more](../conflict-prioritization/gs-conflict-prioritization.md)

* A new end-to-end use case has been added to present all the steps needed to use Decisioning in content experiments with the [!DNL Journey Optimizer] code-based experience channel. [Read more](../experience-decisioning/experience-decisioning-uc.md)

* The **Configure email settings** page has been divided into several sub-pages for improved readability, including new standalone pages dedicated to [List unsubscribe](../email/list-unsubscribe.md), [Header parameters](../email/header-parameters.md) and [URL tracking](../email/url-tracking.md).

## December 2024 {#nov-2024}

* A note has been added to help troubleshoot a potential error message when making an API call to enable datasets for personalization using Adobe Experience Platform data. [Read more](../personalization/aep-data-perso.md)

## October 2024 {#oct-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] October '24 release have been detailed in the documentation. [Read more](release-notes.md)
* All communication channels available in [!DNL Journey Optimizer] are now grouped in a dedicated section of the documentation. [Read more](../channels/gs-channels.md)
* The **Configure your code-based experience** page has been improved to make the process clearer, including the section explaining what a surface URI is. [Read more](../code-based/code-based-configuration.md)
* The **Create web channel configuration** page has been updated to clarify the steps when creating a pages matching rule, which also apply to Code-based experience configuration. [Read more](../web/web-configuration.md#web-page-matching-rule)
* A note about the upcoming time-to-live (TTL) guardrail for system-generated datasets has been added. [Read more](../data/get-started-datasets.md)
* A new section has been added to describe how to preview your code-based personalized experiences right on your browser or on your mobile devices, using the **Preview on device** option when simulating content in a journey or a campaign. [Read more](../code-based/test-code-based.md#preview-on-device)
* A new page has been added on how to leverage Custom upload audiences for decisioning. [Read more](../offers/custom-upload-decisioning.md)
* A new page has been added to introduce the decision capabilities available in Journey Optimizer. [Read more](../experience-decisioning/gs-decision.md)
* Guardrails and limitations have been added to the Decisioning documentation. [Read more](../experience-decisioning/gs-experience-decisioning.md#guardrails)

## September 2024 {#sept-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] Sept '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a section about journey retry management. [Read more](../building-journeys/read-audience.md#read-audience-retry)
* The FAQ about Capping/throttling rule for custom actions has been updated to mention the default capping rule. [Read more](../configuration/external-systems.md#faq)
* The Control access section has been updated with permissions related to AI Assistant Content Generator. [Read more](../administration/high-low-permissions.md#ai-orchestrated-campaign)
* A video about AI Assistant Content Generator for email generation has been added. [Read more](../content-management/generative-full-content.md#video)

<!--

## August 2024 {#aug-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] August '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Performance guardrails for Decision management have been updated to mention Decisioning APIs delivery throughputs with/without Edge Segmentation. [Read more](../start/guardrails.md#decision-management)
* Journey guardrails have been updated. [Read more](../start/guardrails.md#journeys-guardrails-journeys)


## July 2024 {#july-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] July '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A personalization use case has been added on how to personalize an email with information related health plans and prescriptions. [Read more](../personalization/perso-uc-plan-prescriptions.md)

## June 2024 {#june-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] June '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A note about the usage of merge policies in journeys has been added on [this page](../building-journeys/journey-properties.md#merge-policies).
* The page about how to configure a **Wait** activity in a journey has been reorganized and improved. [Read more](../building-journeys/wait-activity.md)
* A new page has been created to detail journey's properties. [Read more](../building-journeys/journey-properties.md)

## May 2024 {#may-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] May '24 release have been detailed in the documentation. [Read more](release-notes.md)
* The section on seed lists has been updated regarding recurring journeys. [Read more](../configuration/seed-lists.md#use-seed-list)
* The setion on external data sources has been updated. [Read more](../datasource/external-data-sources.md#custom-authentication-access-token)
* The global journey timeout of 30 days has been added to the Guardrail and limitation page. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* The section on the Adobe Campaign v7/v8 integration has been updated with information on provisionning. [Read more](../action/acc-action.md#access)
* The expression editor used to personalize content has been renamed in the documentation to "personalization editor" to clearly differenciate it from the [Journey expression editor](../building-journeys/expression/expressionadvanced.md). [Read more](../personalization/personalization-build-expressions.md)

## April 2024 {#april-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] April '24 release have been detailed in the documentation. [Read more](release-notes.md#apr-2024)
* Configuration steps for In-app messaging have been detailed. [Read more](../in-app/inapp-configuration.md)
* Documentation for [Offer decisioning APIs](../offers/api-reference/offer-delivery-api/decisioning-api.md) and [Batch decisioning APIs](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md) have been updated.
* Information has been added in the Decision management documentation regarding edge and hub regions management when using frequency capping with the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)
* Information has been added on identity creation with custom namespaces when working with API-triggered campaigns. [Read more](../campaigns/api-triggered-campaigns.md)
* Screeshots have been updated to reflect the improved Journey canvas.
* Naming constraints has been updated in the following page: [Configure a unitary event](../event/about-creating.md), [Configure a business event](../event/about-creating-business.md#gs-business-events), [Configure a custom action](../action/about-custom-action-configuration.md#configuration-steps), [External data sources](../datasource/external-data-sources.md)
* A note has been added on Send Time Optimization availability. [Read more](../building-journeys/send-time-optimization.md)
* A new technical use case has been added on how to create a custom action to send data to Experience Platform. [Read more](../building-journeys/custom-action-aep.md)

## March 2024 {#march-2024}
 
* A Frequently Asked Questions section has been added to address common questions regarding the use of audience composition and custom upload audiences in Journey Optimizer. [Read more](../audience/about-audiences.md#faq)
* All new features and improvements coming with [!DNL Journey Optimizer] March '24 release have been detailed in the documentation. [Read more](release-notes.md#mar-2024)
* The page on profile entrance management has been improved. [Read more](../building-journeys/entry-management.md)
* Troubleshooting information has been added to the Alerts page. [Read more](../reports/alerts.md#alert-profile-error-rate)
* Information on the Wait activity has been added to the page on journey reports. [Read more](../reports/sharing-overview.md)
* For Journeys in test mode, following shortcuts have been disabled:
    * T: Shortcut to toggle the test mode on or off.
    * E: Shortcut used to trigger an event in an event-based journey.
    * P: Shortcut to trigger an event in an audience-based journey for which the Single profile at a time option is turned on.
    * L: Shortcut designated to display the test logs.
* The Message frequency rules page has been updated with a new subsection on daily frequency cap, which is available on demand in addition to weekly or monthly capping.
* The Work with consent policies page has been improved and updated with useful links to the Experience Platform documentation. [Read more](../action/consent.md)
* A new section has been added to reflect the fact that you can display HTML email content templates as thumbnails with the Grid view mode (Limited Availability). [Read more](../content-management/content-templates.md#template-thumbnails)
* A new section has been added to the Deliverability page to explain what feedback loops are and how to leverage them. [Read more](../reports/deliverability.md#feedback-loops)
* A note has been added to the Create personalized offers section to specify that the size of an offer including all its representations cannot exceed 300KB. [Read more](../offers/offer-library/creating-personalized-offers.md#create-offer)

## February 2024 {#feb-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] February '24 release have been detailed in the documentation. [Read more](release-notes.md#feb-2024)
* The Journey Optimizer + Workfront integration has been added to the integrations page. [Read more](../integrations/ajo-integrations.md)
* Information has been added on how to personalize offers' representations based on context data. [Read more](../offers/offer-library/add-representations.md#context-data)
* The guardrails page has ben updated with a note on custom actions which support JSON format only when using request or response payloads. [Read more](../start/guardrails.md#custom-actions-g)
* Additional information has been added about the basic authentication type in external datasources. [Read more](../datasource/external-data-sources.md)
* A note has been added to clearly differenciate the [Journey expression editor](../building-journeys/expression/expressionadvanced.md) from the [personalization editor](../personalization/functions/functions.md).
* The list of functions available in the advanced expression editor has been updated. [Read more](../building-journeys/expression/functions.md)
* The page on the Split function has been updated. [Read more](../building-journeys/functions/functioninaudience.md)
* Information has been added regarding the impact of the opt-in or opt-out of push notifications on In-app messages. [Read more](../in-app/create-in-app.md)
* The Message frequency rules page has been updated to reflect the Duration options available in the user interface (weekly or monthly).
* The Edit a PTR record section has been updated to clarify the fact that PTR records cannot be created manually and that you need to edit PTR records to assign them new subdomains. [Read more](../configuration/ptr-records.md#edit-ptr-record)

## January 2024 {#jan-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] January '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A guardrail about the journey size has been added. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* Journey timeout management has been detailed [in the following section](../building-journeys/journey-properties.md#global_timeout).
* Journey Optimizer [documentation home](../../ajo-home.md) page has been redesigned.
* Recommendations about the Update Profiles activity have been added. [Read more](../building-journeys/update-profiles.md) 
* Information has been added regarding the behavior of timeouts on event activities in journeys. When no event is received during the specified timeout period, individuals will continue the journey if no timeout path is defined. [Read more](../building-journeys/general-events.md#events-specific-time)
* In-app channel configuration prerequisites have been updated with a note about the usage of a custom Dataset preference merge policy. [Read more](../in-app/inapp-configuration.md)
* More details have been added about how to manipulate collections in a custom action response. [Read more](../action/action-response.md#exp-syntax).
* A link to the [Schema Dictionary for Adobe Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html) has been added to the home page.
* An outdated reference to the AJO Message resource has been removed from the list of resources available in the Audit Log. When an update is done on a message in a journey, a **Journey** log is created. [Read more](../privacy/audit-logs.md)
* Additional recommendations have been added about the usage of the **Read Audience** activity. [Read more](../building-journeys/read-audience.md#must-read)
* The Get started with Adobe Experience Platform audiences page has been improved with a list of audience generation methods. [Read more](../audience/about-audiences.md)
* Best practices have been added when choosing an endpoint to target using a custom action. [Read more](../action/about-custom-action-configuration.md)
* An note has been added to notify users that events cannot be fired from external systems using an API. [Read more](../building-journeys/testing-the-journey.md#important_notes)
* Information on the **currentActionField** function has been added to the list of [collection management functions](../building-journeys/expression/collection-management-functions.md). An expression sample leveraging the function has been added in the [Use API call reponses in custom actions](../action/action-response.md) page.
* Update custom authentication doc regarding cache duration. [Read more] (../datasource/external-data-sources.md)
* Support of `listObject` has been modified in multiple functions.
* Update the **duration** parameter in the `toString` function. [Read more](../building-journeys/functions/conversion-functions.md#toString)
* For some external data sources use-cases, usage of custom actions is recommended.
* Event field syntax has been updated. The following syntax is deprecated `@(my_event.myfield}` and replaced by `@event{my_event.myfield}`. [Read more](../building-journeys/expression/field-references.md)

+++ 2023

## November 2023 {#nov-2023}

* The guardrail that limits all custom actions has been changed from 150,000 calls over 30 seconds to 300,000 calls over one minute. In addition, the default capping no longer applies to each endpoint. It is now performed per host and per sandbox. For example, on a sandbox, if you have two endpoints with the same host (eg: `https://www.adobe.com/endpoint1` and `https://www.adobe.com/endpoint2`), the capping will apply for all endpoints under the adobe.com host. "endpoint1" and "endpoint2" will share the same capping configuration and having one endpoint reach the limit will have an impact on the other endpoint. [Read more](../action/about-custom-action-configuration.md)
* A new status for email campaigns has been added to the list of campaigns' statuses. [Read more](../campaigns/manage-campaigns.md#modify-an-action-campaign)
* The Get started with Adobe Experience Platform audiences section has been updated to reflect the audience evaluation methods available and how to select them. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* A new subsection has been added to specify which events should be avoided when building your audience if you are using the streaming segmentation evaluation method. [Read more](../audience/about-audiences.md#streaming-segmentation-events-guardrails)

## October 2023 {#oct-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] October '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added GIFs to illustrate some key capabilities, such as: [Content templates](../content-management/content-templates.md), [Fragments](../content-management/fragments.md), [Computed attributes](../audience/computed-attributes.md), [Direct mail](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Decision management optimization models](../offers/ranking/personalized-optimization-model.md), [API-triggered campaigns](../campaigns/api-triggered-campaigns.md), and [Content experiment](../content-management/content-experiment.md).
* The Schema creation process has been updated to reflect latest updates in the user interface, coming with Adobe Experience Platform changes. [Read more](../audience/creating-test-profiles.md) 
* Decision management guardrails have been added to the Guardrails and limitations page. [Read more](../start/guardrails.md#decision-management)
* The Header parameters section has been updated to reflect how out-of-office notifications and challenge responses are handled (they are received on the **[!UICONTROL Error email]**). [Read more](../email/email-settings.md#email-header)
* A new section on how to preview and test your content has been created. [Read more](../content-management/preview-test.md)
* The Implement single-page applications page has been moved to the Adobe Experience Paltform Web SDK documentation. [Read more](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html){target="_blank"}
* The Capping section has been updated to reflect the label changes relating to offer capping in the Decision management interface. [Read more](../offers/offer-library/add-constraints.md#capping)
* The Add dynamic content into emails has been updated with details on how to delete a variant. [Read more](../personalization/dynamic-content.md#emails)
* The example for capping & throttling configurations has been updated. [Read more](../configuration/external-systems.md)
* The limitation regarding scalar arrays has been removed from the external data source section. [Read more](../datasource/external-data-sources.md)
* The multi-channel journey use case has been updated. [Read more](../building-journeys/journeys-uc.md)
* The Journey Optimizer documentation set has been updated to reflect the new Experience Platform schema creation process. 

## September 2023 {#september-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] September '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added with scaling best practices and real-time stitching guidance. [Read more](../start/best-practices.md)
* A Frequently-Asked-Questions section has been added for Send-Time Optimization. [Read more](../building-journeys/journeys-message.md#faq-send-time)
* A note has been added for the audience qualification activity. It may take up to 10 minutes to be active and listen to profiles entering or exiting the audience. [Read more](../building-journeys/audience-qualification-events.md#batch-speed-segment-qualification)
* A list of limitations to be aware of when creating decision rules has been added to the Decision management documentation. [Read more](../offers/offer-library/creating-decision-rules.md)
* Links to access control documentation have been updated. [Read more](../administration/permissions.md)
* In-app channel prerequisites have been updated with Adobe Experience Platform Data Collection details. [Read more](../in-app/inapp-configuration.md)
* Some expressions presented in ranking formula examples have been updated to avoid validation errors. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* A warning has been added to the Define decision scopes section to specify that if AI model is used in an evaluation criteria group, all the evaluation criteria in that group must use the AI ranking method, with the same specific AI model. Moreover, only one evaluation criteria group can use AI model. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## August 2023 {#august-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] August '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The note about **authentication cache management** in journey has been updated to detail that the token is not shared between different journeys. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* The page about journey **entry management** has been updated to clarify behavior. [Read more](../building-journeys/entry-management.md)
* Offer decisioning **export datasets** are now enabled by default. The note about the previous behavior has been removed.  [Read more](../offers/export-catalog/get-started-export.md)
* Various **campaign report metrics** have been renamed, in both Live and Global reports. [Read more](../reports/campaign-live-report.md)
* A new section has been added on content experiment prerequisites for the web channel. [Read more](../web/web-prerequisites.md#experiment-prerequisites)
* A warning has been added on the **Work with content templates** page to indicate that currently tracking is not supported when testing email content templates. To test tracking, you must use the content template in an email and send a proof. [Read more](../content-management/content-templates.md#content-templates)
* Several warnings have been added in the **Create and publish landing pages** section to specify that you cannot access your landing page by simply copy-pasting into a web browser the URL defined when creating the page, even if published. Instead you can test it using the preview function. [Read more](../landing-pages/create-lp.md)
* A new section has been added on how to **manage consent** for the direct mail channel. [Read more](../direct-mail/test-send-direct-mail.md)

## July 2023 {#july-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] July '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The wait activity documentation page has been improved with additional information and best practices related to the global timeout and reentrance usage. [Read more](../building-journeys/wait-activity.md)
* The page on entry management has been improved. [Read more](../building-journeys/entry-management.md)
* Additional information has been added about the throttling rate in the Read audience activity documentation. [Read more](../building-journeys/read-audience.md)
* Additional information has been added about retries. [Read more](../start/guardrails.md#general-actions-g)
* The **Implement personalization consent** section has been updated to describe how to manually enforce personalization consent in campaigns: you can use the segment rule builder to create an audience containing opt-out profiles or add a split activity to a composition workflow. [Read more](../privacy/opt-out.md#opt-out-expression-editor)

## June 2023 {#june-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] June '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the discard rate ratio in the Journeys overview screen. [Read more](../building-journeys/journey-gs.md#journey-access)
* A note has been added with the steps to follow if you modify your schema with new enumeration values after creating an event [Read more](../event/about-creating.md)
* A recommendation has been added to use journeyVersionID instead of journeyVersionName when querying journeys. [Read more](../reports/sharing-common-fields.md#journeyversionid-field)
* Additional examples on the evaluation criteria order have been added to the **Create decisions** section to illustrate cases where multiple criteria and multiple decision scopes are used. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* Decision management documentation has been clarified with a note specifying that the use of Object Level Access Control is not available for dynamic collections. [Read more](../offers/offer-library/creating-collections.md)

## May 2023 {#may-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] May '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added to describe how to set up the subdomain that will be used to publish content coming from the Adobe Experience Manager Assets Essentials in your web experiences. [Read more](../web/web-delegated-subdomains.md)
* A new subsection has been added to explain how to add personalized tracking parameters to URLs in the Email Designer. [Read more](../email/message-tracking.md#url-tracking)
* A new section has been added to describe how to ensure that the choice of your customers who opt out from having their profile data used for personalization is honored. [Read more](../privacy/opt-out.md#opt-out-personalization)
* A note has been added about using special international characters in URLs included in email contents. [Read more](../email/message-tracking.md#insert-links)
* The permission needed to test and publish landing pages has been added. [Read more](../landing-pages/create-lp.md)
* A note has been added about the Adobe Experience Platform endpoints needed to have your custom events accounted for in Decision management frequency capping. [Read more](../offers/data-collection/schema-requirement.md#track-custom-events)

## April 2023 {#apr-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] April '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A note has been added to specify that built-in actions cannot be removed. [Read more](../start/guardrails.md#custom-actions-g)
* Information has been added on serviceEvents as well as a query example to check the details of a serviceEvent. [Read more](../reports/query-examples.md#common-queries) 
* A note has been added to specify that you cannot perform queries on time series. [Read more](../building-journeys/condition-activity.md)
* Adobe Experience Manager Assets Essentials and Adobe Stock have been added to the multi-solution integration page. [Read more](../integrations/ajo-integrations.md)
* The warning on multi-level email subdomains not being allowed has been removed as they are now supported. [Read more](../configuration/delegate-subdomain.md)
* A note has been added to specify that, if changes are made to an offer decision which is being used in a journey's message, you need to unpublish the journey and republish it. [Read more](../building-journeys/publish-journey.md)
* Explanation on how to make sure events are correctly accounted for in the capping counter has been clarified in the Decision management **Capping event** section. [Read more](../offers/offer-library/add-constraints.md#capping-event)
* A new section has been added to the **Change execution addresses** page. It specifies that it is possible to override the execution field set globally in the journey advanced parameters, but the email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. [Read more](../configuration/primary-email-addresses.md#override-execution-address-journey)
* The **URL tracking** section now provides the list and description of all contextual attributes that can be set for URL tracking in an email channel configuration. [Read more](../email/email-settings.md#url-tracking)

## March 2023 {#march-2023}

* The Journey Optimizer schema dictionary is now available. You will find the complete list of fields and attributes for each schema.  [Read more](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html)
* All new features and improvements coming with [!DNL Journey Optimizer] March '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a step to enable Adobe Analytics events in your journeys. [Read more](../event/about-analytics.md)
* A new section has been created in the Decision management guide on how to collect offer decisioning feedback in Adobe Experience Platform, including which offers are displayed and how users interact with them. [Read more](../offers/data-collection/data-collection.md)
* A new subsection has been added to the **Create decision** section to explain the difference between evaluating criteria in a sequential order or at the same time. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* A guardrail has been added for read audience journeys with incremental read. You cannot create a new version, you need to duplicate the journey. [Read more](../start/guardrails.md#journey-versions-g)
* The use case on how to limit throughput put has been updated with information on throttling capabilities. [Read more](../building-journeys/limit-throughput.md)
* A note has been added to specify that scalar arrays are not supported in response payload definition. [Read more](../datasource/external-data-sources.md)
* The section on profile cap conditions has been updated. [Read more](../building-journeys/condition-activity.md#profile_cap)

## February 2023 {#feb-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the canvas toolbar. [Read more](../building-journeys/using-the-journey-designer.md#gs-journey-design)
* Information has been added to state that internal Adobe addresses are not allowed in URLs and APIs. [Read more](../start/guardrails.md)
* A note has been added in the API-triggered campaigns documentation to specify that contextual attributes passed into the request cannot exceed 50kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)
* Information was added on how opt-out information is stored in the **Consent Service Dataset** after recipients are unsubscribed through a landing page. [Read more](../landing-pages/lp-use-cases.md#configure-opt-out)

## January 2023 {#jan-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added on custom authentication endpoints in the capping documentation. [Read more](../configuration/external-systems.md)
* A new custom authentication example has been added in the external datasources section. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* A note has been added about Data Collection Core Service (DCCS) for event-triggered journeys. [Read more](../start/guardrails.md#events-g)
* A note on identity namespace retrieval has been added in the [Read audience](../building-journeys/read-audience.md), [Audience qualification](../building-journeys/audience-qualification-events.md) and [Event creation](../event/about-creating.md) sections.
* Accessibility features in [!DNL Journey Optimizer] are now grouped in a dedicated page. [Read more](../start/accessibility.md)
* The examples have been updated in the Operators section of the advanced expression editor documentation. [Read more](../building-journeys/expression/operators.md)
* A note has been added about the limitation on lookup with array of objects. [Read more](../event/experience-event-schema.md#relationships_limitations)
* Added a new page about data management in [!DNL Journey Optimizer]. [Read more](../data/gs-data.md)
* Added a table listing all codes that can be returned in the response when delivering offers using the Decisioning API. [Read more](../offers/api-reference/offer-delivery-api/decisioning-api.md)

+++

+++ 2022

## December 2022 {#december-2022}

* The Messages guide has been reorganized and split into dedicated guides for each channel:

    * [Email channel](../email/get-started-email.md)
    * [Push notification channel](../../rp_landing_pages/push-landing-page.md)
    * [SMS channel](../sms/get-started-sms.md)

* The Configuration guide has been reorganized for improved readability. [Read more](../configuration/get-started-configuration.md)

## November 2022 {#november-2022}

* Added a new page about Journey Optimizer integrations. [Read more](../integrations/ajo-integrations.md)
* Added a recommendation about the length of mirror pages URLs. [Read more](../email/message-tracking.md)
* A new subsection in the email settings configuration has been added on the reply to email address, including recommendations to ensure proper reply management. [Read more](../email/email-settings.md#send-to-suppressed-email-addresses)
* Added a section on how to modify the content of a message in a live journey. [Read more](../building-journeys/journeys-message.md#update-live-content)

## October 2022 {#october-2022}

* Added a journey use case on how to limit throughput using External Data Sources and Custom Actions. [Read more](../building-journeys/limit-throughput.md)
* The journey use case section has been reorganized into two categories: [Business use cases](../building-journeys/journeys-uc.md) and [Technical use cases](../building-journeys/collections.md).
* The **Entity Dataset** section has been updated with more details. [Read more](../data/datasets-query-examples.md#entity-dataset)
* The opt-out management and consent policies sections have been reorganized. [Read more](../privacy/opt-out.md)
* The section on advanced parameters in journey messages has been clarified and now specifies that email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. 
* Added a note to the **Configure landing page subdomains** section to specify that capital letters are not allowed in landing page subdomains. [Read more](../landing-pages/lp-subdomains.md)

## September 2022 {#september-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] September '22 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a best practice related to the use of wait activities in recurring read audience journeys. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added new step event query examples as well as information on the difference between id, instanceid and profileid. [Read more](../reports/query-examples.md).
* Updated the pages related to the [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly) and [toString](../building-journeys/functions/conversion-functions.md#toString) functions.
* Added details on the time condition parameters. [Read more](../building-journeys/condition-activity.md#time_condition)
* Added information on built-in datasets. [Read more](../data/get-started-datasets.md#access-datasets)
* The Global report and Live report sections have been improved and reorganized. [Read more](../reports/report-gs-cja.md)
* A list of every reporting metric available in Adobe Journey Optimizer has been added.
[Read more](../reports/report-gs-cja.md#email-and-sms-metrics)
* The BCC email section has been moved to the new Support for archiving page. [Read more](../configuration/archiving-support.md)

## August 2022 {#august-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] August '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The Frequency rules section has been updated to reflect the new in-line messaging flow.
* A video showing how to configure subscriptions and create landing pages is now referenced in the Get started with landing pages section. [Read more](../landing-pages/get-started-lp.md#video)
* A limitation has been added for journeys using Read Audience activities. [Read more](../building-journeys/read-audience.md)
* The expression editor operators page has been improved. [Read more](../building-journeys/expression/operators.md)
* A section on how to schedule a campaign has been added. [Read more](../campaigns/create-campaign.md)
* General syntax rules section for expression editor has been updated to take into account the new rule regarding the backslash symbol escaping in literal functions. The existing published messages are not impacted by this change. Only the new or draft messages must be updated. [Read more](../personalization/personalization-syntax.md#general-rules)

## July 2022 {#july-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] July '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Set up channel configurations** section has been clarified and updated with links to the page describing how to configure the SMS channel. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* In the journey properties, the **Profile Time zone** option is now disabled by default. [Read more](../building-journeys/timezone-management.md#timezone-from-profiles)
* In the **Wait** activity, the **Fixed date** option is no longer available. [Read more](../building-journeys/wait-activity.md)
* Added more information on the **Incremental read** option in the **Read audience** activity. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added recommendations on the **Profile cap** condition type. [Read more](../building-journeys/condition-activity.md#profile_cap)
* Added a limitation on business events. [Read more](../start/guardrails.md#events-g)

## June 2022 {#june-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] June '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new section about Privacy requests has been added to the documentation. [Read more](../privacy/requests.md)
* A new section about Audit logs on resources has been added to the documentation. [Read more](../privacy/audit-logs.md)
* A new section about how to add HTML or JSON content coming from Adobe Experience Cloud Asset library to an offer representation has been added to the documentation. [Read more](../offers/offer-library/add-representations.md#html-json)
* Added a new page on journey lifecyle. [Read more](../building-journeys/journey.md)
* Updated the Wait activity page. [Read more](../building-journeys/wait-activity.md)
* Added the list of Adobe Journey Optimizer datasets with query examples. [Read more](../data/datasets-query-examples.md)
* The Allowed list page has been moved to the Configuration section. [Read more](../configuration/allow-list.md)
* The Suppression list page has been updated to clarify some information, including the fact that all ASCII characters comprised between 32 and 126 are allowed in the reason for suppression field. [Read more](../configuration/manage-suppression-list.md)
* The link to guardrails and static limits for Decision management has been added. [Read more](../start/guardrails.md)
* Send-Time Optimization is now available for all customers. The beta mention has been removed. [Read more](../building-journeys/send-time-optimization.md)
* The Batch Decisioning API has been added to the list of available APIs to delivery personalized offers. [Read more](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## May 2022 {#may-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] May '22 release have been detailed in the documentation. [Read more](release-notes.md)
* New query examples related to [audience qualification](../reports/query-examples.md#segment-qualification-queries) and [events](../reports/query-examples.md#event-based-queries) have been added.
* The email design section now mentions new built-in templates available to start content with. Related screenshots have been updated. [Read more](../email/get-started-email-design.md)
* Links to key resources have been updated in Journey Optimizer documentation home page.
* Screenshots for landing page and subscription reporting have been updated. [Read more](../reports/live-report.md)
* A note has been added stating that the Delete method is not supported in custom actions. [Read more](../action/about-custom-action-configuration.md)
* Links to how-to videos have been updated.
* The [Email configuration](../configuration/about-subdomain-delegation.md), [Message presets](../configuration/channel-surfaces.md) and [Configure landing pages](../landing-pages/lp-subdomains.md) sections have been reorganized for improved readability.
* The URL tracking section has been updated and improved with examples. [Read more](../email/email-settings.md#url-tracking)
* A new subsection on setting up a forward email address has been added. Note that you cannot do it through the user interface. [Read more](../email/email-settings.md#email-settings)

## April 2022 {#april-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] April '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **reactions** event documentation page has been updated. [Read more](../building-journeys/reaction-events.md)
* Videos for Decision management capabilities have been updated to reflect Journey Optimizer user interface. [Read more](../offers/get-started/starting-offer-decisioning.md)
* The **Get Started with Datasets** section has been improved to detail how to access and create datasets. [Read more](../data/get-started-datasets.md)
* Links to help guides and product release notes have been added to the **Adobe Journey Optimizer Documentation** home page. [Read more](https://experienceleague.adobe.com/docs/journey-optimizer.html)
* The **Create message presets** section now specifies that you cannot proceed with preset creation while the selected IP pool is under edition (**[!UICONTROL Processing]** status) and has never been associated with the selected subdomain. [Read more](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* The message presets **URL tracking** section has been updated to reflect minor changes in the user interface. [Read more](../configuration/channel-surfaces.md#url-tracking)

## March 2022 {#march-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] March '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page on getting started with AI models has been added to the **Offer decisioning** section, including a thorough description of the [auto-optimization model](../offers/ranking/auto-optimization-model.md), the algorithm it uses and more technical details. [Read more](../offers/ranking/ai-models.md)
* The test profile creation page has been moved to the  **Audience, profiles and identity** section. [Read more](../audience/creating-test-profiles.md)
* Added an example on how to add an expression as a default value in the expression editor. [Read more](../building-journeys/expression/field-references.md#default-value)
* The **Create personalized offers** section has been reorganized for improved readability. [Read more](../offers/offer-library/creating-personalized-offers.md)
* A new section has been added to describe the impacts that changing an offer's start and/or end dates may have on this offer's frequency capping. [Read more](../offers/offer-library/add-constraints.md#capping-change-date)
* The **Change the primary email addresses** section has been updated to reflect the user interface changes. [Read more](../configuration/primary-email-addresses.md)

## February 2022 {#feb-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The [replace](../building-journeys/functions/string-functions.md#replace) and [replaceAll](../building-journeys/functions/string-functions.md#replaceAll) function documentation pages have been updated with additional information and examples regarding the target parameter.
* Best practices have been added to the [Operators](../building-journeys/expression/operators.md#important-notes) page.

## January 2022 {#january-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Offer decisioning AI rankings** section has been updated with a more detailed description of the auto-optimization model. [Read more](../offers/ranking/auto-optimization-model.md)
* A new section on the schema requirements needed to be able to send in event types when using an AI model has been added. [Read more](../offers/data-collection/schema-requirement.md)
* The section related to [!DNL Journey Optimizer] personalization capabilities has been reorganized for better readability. [Read more](../personalization/personalize.md)
* The **Create message presets** section has been divided into several sections for improved clarity. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* The **Opt-out management** section has been clarified and slightly reorganized. [Read more](../privacy/opt-out.md#opt-out-decision-management)
* The **Insert links** section has been updated to reflect the recent user interface changes. [Read more](../email/message-tracking.md#insert-links)

+++

+++ 2021

## November 2021 {#november-2021}

* A full description of the **advanced expression editor** used in journeys is now available. [Read more](../building-journeys/expression/expressionadvanced.md)
* A new section about **CNAME subdomain delegation method** has been added. [Read more](../configuration/delegate-subdomain.md#cname-subdomain-setup)

## October 2021 {#october-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] Oct '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added **Date time function** list. [Read more](../personalization/functions/dates.md)
* New **Get Started sections per user persona**. Take your own path to get to your goals faster! [Read more](../start/quick-start.md)
* New **Edit a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New **Edit a PTR record** section. [Read more](../configuration/ptr-records.md#edit-ptr-record)
* New **Deactivate a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New limitations added to the **Decision Management API developer guide** on offer constraints not supported with the mobile [!DNL Experience Edge] workflows. [Read more](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* New **Create simulations** section. [Read more](../offers/offer-activities/simulation.md)
* Updated **Add decision scopes** section. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Updated **Define content for your representations** section, including a new [subsection](../offers/offer-library/creating-personalized-offers.md#custom-text) on how to define and personalize custom text. [Read more](../offers/offer-library/creating-personalized-offers.md#content)

## September 2021 {#september-2021}

* The following function pages have been updated: [sethours](../building-journeys/functions/date-functions.md#setHours), [getListItem](../building-journeys/functions/list-functions.md#getListItem), [inSegment](../building-journeys/functions/functioninaudience.md)

* The following functions have been added: [filter](../building-journeys/functions/list-functions.md#filter), [intersect](../building-journeys/functions/list-functions.md#intersect), [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly)

* The dateOnly date type has been added in the expression editor documentation. [Read more](../building-journeys/expression/data-types.md)

* Added details on custom action cache duration. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)

* Added information on custom action default ports. [Read more](../action/about-custom-action-configuration.md#url-configuration)

* Added information on multiple business event use cases. [Read more](../event/about-creating-business.md#multiple-business-events)

* Added commonly used examples to query Journey Step Events in Data Lake. [Read more](../reports/query-examples.md)

* Added a new **Limitations** page. [Read more](../start/guardrails.md)

* Improved the **Quick start** page with steps for different personas. [Read more](../start/quick-start.md)

* Now all the Decision management features described in the dedicated section also apply to the Adobe Experience Platform users leveraging the Offer Decisioning application. [Read more](../offers/get-started/starting-offer-decisioning.md)

* Added a subsection to clarify the differences between using audiences versus decision rules when applying a constraint to restrict the selection of offers for a given placement. [Read more](../offers/offer-activities/create-offer-activities.md#decision-list)

* Added specific ranking formula examples to illustrate some real-life use cases. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Added a subsection on how to edit IP pools. [Read more](../configuration/ip-pools.md#edit-ip-pool)

## August 2021 {#august-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] August '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Updated Decision management permissions. [Read more](../administration/ootb-product-profiles.md)
* Updated Email Designer screenshots with latest UI.
* Updated the configuration procedure for custom actions with dynamic URL paths and dynamic headers. [Read more](../action/about-custom-action-configuration.md#url-configuration)
* Added a section about accessibility features and shortcuts. [Read more](../start/user-interface.md#accessibility)
* Added a section about audience evaluation methods. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Added notes to the Suppression list, Allowed list and Email global/live report sections to specify that profiles with Suppressed and Not allowed statuses are excluded from the Email report Sent metrics. [Read more](../reports/report-gs-cja.md)
* Added a new section to describe how to retrieve email addresses or domains that were excluded from a sending because they were not on the allowed list. [Read more](../configuration/allow-list.md#reporting)
* Updated the Enable the allow list section. [Learn more](../configuration/allow-list.md#enable-allow-list)
* Updated the Monitor message presets section with the possible preset creation failure reasons and details on such errors. [Read more](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Updated and renamed the Retry time period section to reflect the fact that you can now adjust the email retry setting in the message presets. [Read more](../configuration/retries.md#retry-duration)
* Updated the Delegate a subdomain section with more detailed information on the validation process performed by Adobe. [Read more](../configuration/delegate-subdomain.md#subdomain-validation)
* Added a section to describe how to manually add email addresses and domains to the suppression list. [Read more](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Updated the [Access the suppression list](../configuration/manage-suppression-list.md#access-suppression-list) section and [Retries](../configuration/retries.md) sections to reflect the new user interface.
* The new flow to add and configure representations when creating an offer has been documented. [Read more](../offers/offer-library/creating-personalized-offers.md#representations)

## July 2021 {#july-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] July '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added direct links to Experience Platform services documentation in [!DNL Journey Optimizer] home page and table of contents
* New landing pages for Experience Platform services available in [!DNL Journey Optimizer] 
* Added links to [!DNL Journey Optimizer] product description in the home page
* Added tutorial videos in multiple pages
* Optimized home page imagery
* Moved, improved and renamed 'Message tracking' section to 'Add links and track messages'. [Read more](../email/message-tracking.md)
* Added a subsection on mirror pages. [Read more](../email/message-tracking.md#mirror-page)
* Renamed 'offer activities' as 'decisions' and 'decisions' as 'decision scopes' in documentation and screens. [Read more](../offers/get-started/starting-offer-decisioning.md)
* New use case: [personalize a message with helper functions](../personalization/personalization-use-case-helper-functions.md)
* Updated the Read audience documentation to reflect materialized segment impacts. [Read more](../building-journeys/read-audience.md)
* Updated the Journey limitations. [Read more](../start/guardrails.md)
* Updated the Configure offers selection in decisions section. [Read more](../offers/offer-activities/configure-offer-selection.md)
* Added a warning to mention that event-based offers are not currently supported. [Read more](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documented the Decision management new **[!UICONTROL Overview]** tab. [Read more](../offers/get-started/user-interface.md#overview)
* Added new sections to describe the actions available from the offer and decision lists: [Offer list](../offers/offer-library/creating-personalized-offers.md#offer-list) and [Decision list](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
-->
