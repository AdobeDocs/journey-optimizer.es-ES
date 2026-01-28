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
source-git-commit: 57017310f5ed34e447c47babe288b28186809f6e
workflow-type: tm+mt
source-wordcount: '4693'
ht-degree: 95%

---

# Actualizaciones de la documentación {#latest-updates}

Esta página incluye todos los cambios más recientes en la documentación de [!DNL Journey Optimizer], además de las actualizaciones relacionadas con las características y mejoras de la versión mensual.

## Enero de 2026 {#january-2026}

* Se ha añadido una nueva sección de protección a la validación del tamaño de la carga útil del recorrido del documento, que incluye umbrales de advertencia y error y directrices sobre cómo optimizar los recorridos. [Más información](../start/guardrails.md#journey-payload-size)

* La documentación de las protecciones de Decisioning se ha actualizado para incluir limitaciones de tamaño de elementos de decisión (1 KB para elementos que incluyen atributos con un máximo de 30 atributos). [Más información](../experience-decisioning/decisioning-guardrails.md)

* Se ha agregado una nota a la documentación de fragmentos para advertir que cuando la etiqueta del botón y la URL se pueden editar en un fragmento, el conjunto de datos de seguimiento registra el valor de la URL en lugar del valor de la etiqueta. [Más información](../content-management/customizable-fragments.md#visual)

* Ya está disponible una nueva página que describe las ventajas de migrar de Administración de decisiones a Toma de decisiones, incluida la información sobre las próximas API de herramientas de migración. [Más información](../experience-decisioning/migrate-to-decisioning.md)

* Se ha añadido una protección para aclarar que los conjuntos de datos de búsqueda solo están disponibles para la activación entrante basada en Edge en la región donde reside la zona protegida del conjunto de datos. [Más información](../data/lookup-aep-data.md#guidelines)

* Se ha añadido una nueva sección a la documentación de configuración del canal de campañas orquestadas que explica cómo utilizar atributos contextuales (como ID de campaña, nombre y detalles de acción) en los parámetros de seguimiento de URL con fines de análisis e informes. [Más información](../orchestrated/channel-config.md#url-tracking)

* La documentación de Optimización de contenido se ha reestructurado para una mejor claridad. La página de optimización principal se ha dividido en cuatro subpáginas centradas: una página de introducción, una página dedicada a la segmentación, una a la experimentación y otra a la combinación de ambos métodos. [Más información](../content-management/gs-message-optimization.md)

* Las notas de disponibilidad limitada se han eliminado de tres recorridos de alertas (Recorrido publicado, Recorrido finalizado y Acción personalizada limitada activada), ya que estas funciones ya están disponibles de forma general. [Más información](../reports/alerts.md)

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

* Ahora puede convertir imágenes a plantillas de HTML mediante el convertidor de imágenes a HTML. [Más información](../email/image-to-html.md)

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

## Agosto de 2025 {#august-2025}

* Se añadió una nueva página que enumera las prácticas recomendadas para diseñar correo electrónico y contenido de página de aterrizaje accesibles con [!DNL Journey Optimizer]. [Más información](../email/accessible-content.md)

* La documentación de los identificadores suplementarios en recorridos se ha actualizado con las siguientes aclaraciones:

   * Después de añadir un identificador suplementario a un esquema, se debe crear un nuevo evento (para recorridos activados por eventos) o un nuevo grupo de campos (para recorridos de públicos de lectura). Las entidades existentes no se actualizan automáticamente y no reconocerán el nuevo identificador.

   * Los identificadores adicionales no se validan con las políticas de etiquetado y aplicación del uso de datos (Data Usage Labeling &amp; Enforcement, DULE) y no se tienen en cuenta durante las comprobaciones de gobernanza de datos en recorridos.

[Más información](../building-journeys/supplemental-identifier.md)

* La página Optimización en campañas se ha actualizado para reflejar el hecho de que la optimización ahora también está disponible en recorridos. [Más información](../content-management/gs-message-optimization.md)

* Se ha añadido un vínculo al tutorial en vídeo que describe cómo aprovechar la optimización de mensajes en una campaña. [Más información](../content-management/gs-message-optimization.md)

## Julio de 2025 {#july-2025}

* La interfaz de campañas ahora cuenta con dos pestañas independientes: **Acción** y **API activada**. La documentación se ha actualizado en consecuencia, con información para cada tipo de campaña organizada en secciones dedicadas para mejorar la claridad y la facilidad de uso. [Más información](../campaigns/get-started-with-campaigns.md)

* Las páginas [Introducción a la delegación de subdominios](../configuration/about-subdomain-delegation.md) y [Delegar un subdominio](../configuration/delegate-subdomain.md) se han actualizado para presentar mejor los diferentes métodos de delegación y los pasos para configurarlos.

* Se ha añadido una nota a la sección Fragmentos que especifica que, cuando el seguimiento está habilitado en un recorrido o una campaña, si los vínculos están presentes en un fragmento y si este fragmento se utiliza en un mensaje, se realiza el seguimiento de estos vínculos, al igual que todos los demás incluidos en el mensaje. [Más información](../content-management/create-fragments.md#content)

* Las protecciones y limitaciones aplicables a la delegación de subdominios en Journey Optimizer se han enriquecido y consolidado en una sección dedicada. [Más información](../configuration/delegate-subdomain.md#guardrails)

* Se ha añadido una nota a las páginas Crear ofertas de reserva y Crear decisión para mencionar que las ofertas de reserva deben contener todas las representaciones utilizadas dentro de una decisión. [Más información](../offers/offer-library/creating-fallback-offers.md)

* Las protecciones que se aplican a los fragmentos se han enriquecido. [Más información](../start/guardrails.md#fragments-guardrails).

* Se ha añadido una nota para especificar que los vínculos añadidos a los mensajes caducan pasados 25 meses y los vínculos a páginas espejo pasados 90 días. [Más información](../email/message-tracking.md)

<!--* The possible email error types that could happen upon sending email deliveries with are now listed in a dedicated section. [Read more](../configuration/email-error-types.md)-->

## Junio de 2025 {#june-2025}

* Se ha añadido una nueva sección sobre cómo añadir y utilizar texto enriquecido como saltos de línea, negrita, cursiva, etc., en fragmentos personalizables mediante componentes HTML. [Más información](../content-management/customizable-fragments.md#rich-text)

* La parte de toma de decisiones se ha actualizado con una sección específica dedicada a la creación de modelos de IA. [Más información](../experience-decisioning/ranking/ai-models.md)

* Se ha añadido una recomendación sobre el uso del campo `actionExecutionTime` en la acción de eventos journeyStep. [Más información](../reports/sharing-execution-fields.md#actionexecutiontime-field)

* Se ha añadido una nota sobre el `messageID`, que puede no ser único para cada envío individual. [Más información](../data/datasets-query-examples.md)

* Se ha añadido una recomendación sobre la administración de eventos históricos en operaciones de higiene de datos. [Más información](../privacy/data-hygiene.md#data-hygiene-recommendations)

* Se ha añadido un mecanismo de protección sobre las páginas de aterrizaje que no son compatibles con la migración entre zonas protegidas. [Más información](../configuration/copy-objects-to-sandbox.md#global)

* Se ha añadido una nota de advertencia sobre los objetos JSON anidados que no son compatibles con la autenticación personalizada para acciones personalizadas. [Más información](../datasource/external-data-sources.md)

* Se ha añadido una nota de advertencia sobre la denominación de variantes de contenido condicional en el Diseñador de correo electrónico. [Más información](../personalization/create-conditions.md)

* Se ha actualizado la sección “Anular la delegación de un subdominio de la página de aterrizaje”. [Más información](../landing-pages/lp-subdomains.md#undelegate-subdomain)

* Se han aclarado las reglas de reentrada de recorrido al usar identificadores suplementarios. [Más información](../building-journeys/supplemental-identifier.md#guardrails)

* Se ha añadido una nueva nota para aclarar que se debe utilizar el editor de expresiones en modo avanzado al seleccionar el atributo de identificador suplementario durante la configuración del evento. [Más información](../building-journeys/supplemental-identifier.md#add)

* Se ha añadido una aclaración sobre cómo funciona la reentrada de recorridos con identificadores suplementarios. [Más información](../building-journeys/supplemental-identifier.md#guardrails)

## Mayo de 2025 {#may-2025}

* Las integraciones de Adobe disponibles con Journey Optimizer ahora se enumeran en la sección “Conectar sus sistemas y entornos”. [Más información](../integrations/ajo-integrations.md)

* Las integraciones de contenido ahora se agrupan en la sección Administración de contenido. [Más información](../integrations/content-integrations.md)

* Se han actualizado los diagramas de arquitectura para Adobe Experience Platform y Journey Optimizer. [Más información](../start/get-started.md#architecture)

* Se ha añadido un vídeo sobre el patio del editor de personalización para ayudarle a aprender a escribir y probar el código de personalización mediante datos de muestra. [Más información](../personalization/personalize.md#video-perso)

* El número máximo de direcciones en una lista semilla ha aumentado a 50 a 300. [Más información](../configuration/seed-lists.md#create-seed-list)

* Se ha añadido a la página Creación de políticas de decisión un nuevo paso que detalla cómo ajustar el código al utilizar directivas de decisión en el editor de la experiencia basada en código. [Más información](../experience-decisioning/create-decision.md#create-decision)

* Se ha añadido una nota a la documentación de experiencias basadas en código para especificar que, cuando se ejecutan varias acciones de experiencias basadas en código en la misma superficie, la puntuación de prioridad de la campaña o el recorrido determina qué se envía al usuario final si cumple los requisitos para más de una acción. [Más información](../code-based/code-based-surface.md#surface-definition)

* La nueva página sobre la resolución de problemas de acciones entrantes en recorridos proporciona una guía paso a paso para identificar y resolver problemas de forma independiente antes de ponerse en contacto con el servicio de asistencia. [Más información](../building-journeys/troubleshooting-inbound.md)

* Se ha añadido una nueva [página](../code-based/code-based-decisioning-implementations.md) para describir cómo añadir los siguientes indicadores a la implementación de su cliente al utilizar la toma de decisiones en experiencias basadas en código:

   * Añadir el indicador `dryRun` para probar la toma de decisiones en experiencias basadas en código. [Más información](../code-based/code-based-decisioning-implementations.md#code-based-test-decisions)

   * Aplicar la deduplicación a las solicitudes de toma de decisiones en experiencias basadas en código. [Más información](../code-based/code-based-decisioning-implementations.md#code-based-decisioning-deduplication)

## Abril de 2025 {#apr-2025}

* El capítulo Configuración ahora se divide en tres: [Configuración del canal](../configuration/get-started-configuration.md), [Configuración de recorrido](../configuration/about-data-sources-events-actions.md) y [Conexión de los sistemas](../configuration/ajo-apis.md).
* Se ha añadido una nota de precaución sobre el uso de eventos de experiencia en expresiones y condiciones de recorrido. [Más información](../building-journeys/expression/expressionadvanced.md#discovering-the-interface)
* Se ha añadido una nota en la página de configuración del correo directo sobre el almacenamiento temporal del archivo de salida. [Más información](../direct-mail/direct-mail-configuration.md)
* Se ha añadido una sugerencia en la sección del editor de expresiones avanzadas de recorrido sobre las directrices del formato de condición. [Más información](../building-journeys/expression/expressionadvanced.md)
* Se ha añadido una nota de precaución en la sección de funciones `inAudience` sobre los impactos y las prácticas recomendadas al cambiar el nombre de un público. [Más información](../building-journeys/functions/functioninaudience.md)
* Se ha añadido una recomendación sobre el uso de palabras claves nativas al usar SMS bidireccionales. [Más información](../sms/sms-opt-out.md)
* Se ha actualizado la página de prueba de recorrido con una nota sobre la necesidad de incluir un espacio de nombres de identidad en el evento utilizado. [Más información](../building-journeys/testing-the-journey.md)
* Actualmente, no puede anular la delegación de subdominios a través de la interfaz de usuario de [!UICONTROL Journey Optimizer]; debe ponerse en contacto con su representante de Adobe. Los pasos para anular la delegación de un subdominio ahora están detallados para [Correos electrónicos](../configuration/delegate-subdomain.md#undelegate-subdomain), [SMS](../sms/sms-subdomains.md#undelegate-subdomain), [Experiencias web](../web/web-delegated-subdomains.md#undelegate-subdomain) y [Páginas de aterrizaje](../landing-pages/lp-subdomains.md#undelegate-subdomain).<!--[Read more](../configuration/delegate-subdomain.md#undelegate-subdomain)-->
* Se ha añadido una aclaración sobre el parámetro opcional `maxHttpConnections` en la API de límite de recorridos, incluyendo instrucciones sobre cómo utilizarlo junto con las configuraciones de restricción para el mismo punto final. [Más información](../configuration/throttling.md)
* En la sección de Toma de decisiones, se han añadido directrices que explican que los elementos de oferta aprobados no se pueden eliminar si se utilizan en una colección o una decisión. Se han incluido pasos para cambiar su estado a “Borrador” usando la opción **[!UICONTROL Deshacer aprobación]**. [Más información](../experience-decisioning/items.md#manage)
* La información sobre las zonas protegidas se han agrupado en la nueva sección “Administración de zonas protegidas”. Esta nueva sección proporciona información sobre cómo utilizar y asignar zonas protegidas y cómo utilizar las posibilidades de exportación e importación de paquetes para copiar objetos como recorridos, plantillas de contenido o fragmentos en varias zonas protegidas. [Más información](../administration/sandboxes.md)

## Marzo de 2025 {#mar-2025}

* La página sobre los eventos de calificación de públicos se ha actualizado con nuevas recomendaciones. [Más información](../building-journeys/audience-qualification-events.md)
* La capacidad de resolución de problemas de acciones personalizadas ya está disponible para todos los clientes (GA). [Más información](../action/troubleshoot-custom-action.md)
* La higiene de datos ahora es el ciclo de vida de datos en la interfaz de usuario del producto. La documentación se ha actualizado para reflejar este cambio. [Más información](../privacy/data-hygiene.md)
* Los permisos integrados de la página de destino que faltan se han añadido a la documentación. [Más información](../administration/ootb-permissions.md)
* Se ha añadido una nota sobre la programación de campañas recurrentes. [Más información](../campaigns/create-campaign.md)
* Se ha actualizado y reorganizado la sección sobre la inserción de vínculos y la habilitación del seguimiento en un mensaje de correo electrónico. [Más información](../email/message-tracking.md)
* Se ha reorganizado y mejorado la sección sobre funcionalidades de personalización en Adobe Journey Optimizer. [Más información](../personalization/personalize.md)
* La API de Gestión de decisiones para enumerar ofertas personalizadas se ha actualizado con una muestra para realizar la paginación si faltan varias ofertas personalizadas en la respuesta. [Más información](../offers/api-reference/offers-api/personalized-offers/offers-list.md)
* Se ha creado una nueva página con toda la información relativa a la función Cancelar la suscripción a una lista para una mayor claridad. [Más información](../email/list-unsubscribe.md)
* La sección Restricción de frecuencia se ha actualizado con información sobre cómo se actualiza el contador de restricción de frecuencia para las API de decisiones y decisiones por lotes, además de la API de decisiones de Edge. [Más información](../offers/offer-library/add-constraints.md#frequency-capping)

## Febrero de 2025 {#feb-2025}

* Se han actualizado los mecanismos de protección de la actividad “Leer público” para especificar que solo se puede utilizar una actividad en un recorrido y dirigirla a un único público. [Más información](../building-journeys/read-audience.md)
* Se han actualizado los mecanismos de protección de recorrido cuando se utilizan actividades de Adobe Campaign. [Más información](../start/guardrails.md#ac-g)
* Se han detallado los pasos para crear sus primeros recorridos y se han añadido vínculos a la sección de documentación. [Más información](../building-journeys/journey-gs.md)
* Ahora hay disponible una nueva página para detallar el panel de control de recorrido y la interfaz de usuario de filtrado. [Más información](../building-journeys/journey-ui.md)
* Se han actualizado, mejorado y movido a una nueva página dedicada la documentación de **[!UICONTROL optimización del tiempo de envío]** y sus preguntas frecuentes relacionadas. [Más información](../building-journeys/send-time-optimization.md)
* Se han añadido nuevos mecanismos de protección a los eventos de recorridos. [Más información](../start/guardrails.md#events-g)
* Se ha reorganizado la página de acciones de canal integradas. [Más información](../building-journeys/journeys-message.md)
* Se han añadido protecciones y limitaciones en las secciones de toma de decisiones y gestión de decisiones.
   * [Limitaciones y protecciones de decisiones](../experience-decisioning/decisioning-guardrails.md)
   * [Limitaciones y mecanismos de protección de gestión de decisiones](../offers/decision-management-guardrails.md)
* Se ha añadido una nueva sección sobre datos de contexto en la documentación de gestión de decisiones. Proporciona información sobre cómo aprovechar los datos de contexto en el motor de decisión, por ejemplo, para diseñar una regla de decisión que requiera que el clima actual sea de ≥80 grados en el momento en que se realice la solicitud de decisión. [Más información](../offers/context-data.md)

## Enero de 2025 {#jan-2025}

* Se ha añadido una nueva sección sobre la opción **[!UICONTROL Dirección de ejecución]** en la configuración de correo electrónico. La dirección principal se define en el nivel de zona protegida, pero la configuración predeterminada se puede sobrescribir para una configuración de correo electrónico específica. [Más información](../email/email-settings.md#execution-address)

* La página **Introducción a la entregabilidad** se ha actualizado con la posibilidad de crear flujos de trabajo de calentamiento de IP directamente desde la interfaz de usuario. [Más información](../reports/deliverability.md#reputation)

* La sección **Parámetros de encabezado** se ha actualizado para reflejar las nuevas etiquetas y los cambios en la interfaz de usuario. [Más información](../email/email-settings.md#email-header)

* La sección **Correo electrónico de reenvío** se ha actualizado para especificar que todos los correos electrónicos enviados a la dirección **Correo electrónico del remitente** se reenvíen a la dirección de correo electrónico de reenvío. Si no se especifica ningún correo electrónico de reenvío, estos correos electrónicos se descartan. [Más información](../email/email-settings.md#email-settings)

* El tamaño máximo de los atributos contextuales pasados a una solicitud de campaña activada por API se ha actualizado a 200 KB. [Más información](../campaigns/api-triggered-campaigns.md#contextual)

* Se ha añadido una nueva sección a la página **Administrar fragmentos** para describir cómo añadir nuevos atributos a un fragmento activo. También se ha mejorado toda la página. [Más información](../content-management/manage-fragments.md#adding-new-attributes)

* Se ha añadido una sección “Mecanismos de protección y limitaciones” a la documentación de las herramientas de administración de conflictos y priorizaciones. [Más información](../conflict-prioritization/gs-conflict-prioritization.md)

* Se ha añadido un nuevo caso de uso de extremo a extremo para presentar todos los pasos necesarios para utilizar la toma de decisiones en experimentos de contenido con el canal de experiencia basado en código de [!DNL Journey Optimizer]. [Más información](../experience-decisioning/experience-decisioning-uc.md)

* La página **Configuración de correo electrónico** se ha dividido en varias subpáginas para mejorar la legibilidad, incluidas las nuevas páginas independientes dedicadas a [Cancelación de suscripción a lista](../email/list-unsubscribe.md), [Parámetros de encabezado](../email/header-parameters.md) y [Seguimiento de URL](../email/url-tracking.md).

## Diciembre de 2024 {#nov-2024}

* Se ha añadido una nota para ayudar a solucionar un posible mensaje de error al realizar una llamada API para habilitar conjuntos de datos para la personalización mediante datos de Adobe Experience Platform. [Más información](../personalization/aep-data-perso.md)

## Octubre de 2024 {#oct-2024}

* Todas las nuevas funciones y mejoras disponibles con la versión de [!DNL Journey Optimizer] de octubre de 2024 se han detallado en la documentación. [Más información](release-notes.md)
* Todos los canales de comunicación disponibles en [!DNL Journey Optimizer] se agrupan ahora en una sección dedicada de la documentación. [Más información](../channels/gs-channels.md)
* Se ha mejorado la página **Configurar la experiencia basada en código** para que el proceso sea más claro, incluida la sección que explica qué es un URI de superficie. [Más información](../code-based/code-based-configuration.md)
* La página **Crear configuración de canal web** se ha actualizado para aclarar los pasos al crear una regla de coincidencia de páginas, que también se aplican a la configuración de experiencias basadas en código. [Más información](../web/web-configuration.md#web-page-matching-rule)
* Se ha añadido una nota sobre el próximo mecanismo de protección del tiempo de vida (TTL) para los conjuntos de datos generados por el sistema. [Más información](../data/get-started-datasets.md)
* Se ha añadido una nueva sección para describir cómo obtener una vista previa de las experiencias personalizadas basadas en código directamente en el explorador o en los dispositivos móviles, mediante la opción **Vista previa en el dispositivo** al simular contenido en un recorrido o una campaña. [Más información](../code-based/test-code-based.md#preview-on-device)
* Se ha añadido una nueva página sobre cómo aprovechar los públicos de carga personalizados para la toma de decisiones. [Más información](../offers/custom-upload-decisioning.md)
* Se ha añadido una nueva página para introducir las funciones de decisión disponibles en Journey Optimizer. [Más información](../experience-decisioning/gs-decision.md)
* Se han añadido mecanismos de protección y limitaciones a la documentación sobre la toma de decisiones. [Más información](../experience-decisioning/gs-experience-decisioning.md#guardrails)

## Septiembre de 2024 {#sept-2024}

* Todas las nuevas funciones y mejoras incluidas en la versión de [!DNL Journey Optimizer] de septiembre de 2024 se han detallado en la documentación. [Más información](release-notes.md)
* Se ha añadido una sección sobre la administración de reintentos de recorrido. [Más información](../building-journeys/read-audience.md#read-audience-retry)
* Se ha actualizado la pregunta frecuente sobre la regla de límite/restricción para las acciones personalizadas con el fin de mencionar la regla de límite predeterminada. [Más información](../configuration/external-systems.md#faq)
* La sección Control de acceso se ha actualizado con permisos relacionados con el generador de contenido del Asistente de IA. [Más información](../administration/high-low-permissions.md#ai-orchestrated-campaign)
* Se ha añadido un vídeo sobre el generador de contenido del Asistente de IA para la generación de correo electrónico. [Más información](../content-management/generative-full-content.md#video)

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
* A link to the [Schema Dictionary for Adobe Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=es) has been added to the home page.
* An outdated reference to the AJO Message resource has been removed from the list of resources available in the Audit Log. When an update is done on a message in a journey, a **Journey** log is created. [Read more](../privacy/audit-logs.md)
* Additional recommendations have been added about the usage of the **Read Audience** activity. [Read more](../building-journeys/read-audience.md#must-read)
* The Get started with Adobe Experience Platform audiences page has been improved with a list of audience generation methods. [Read more](../audience/about-audiences.md)
* Best practices have been added when choosing an endpoint to target using a custom action. [Read more](../action/about-custom-action-configuration.md)
* An note has been added to notify users that events cannot be fired from external systems using an API. [Read more](../building-journeys/testing-the-journey.md#important_notes)
* Information on the **currentActionField** function has been added to the list of [collection management functions](../building-journeys/expression/collection-management-functions.md). An expression sample leveraging the function has been added in the [Use API call reponses in custom actions](../action/action-response.md) page.
* Update custom authentication doc regarding cache duration. [Read more] (../datasource/external-data-sources.md)
* Support of `<listObject>` has been modified in multiple functions.
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
* The Implement single-page applications page has been moved to the Adobe Experience Paltform Web SDK documentation. [Read more](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html?lang=es){target="_blank"}
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

* The Journey Optimizer schema dictionary is now available. You will find the complete list of fields and attributes for each schema.  [Read more](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=es)
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
* Links to help guides and product release notes have been added to the **Adobe Journey Optimizer Documentation** home page. [Read more](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=es)
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
