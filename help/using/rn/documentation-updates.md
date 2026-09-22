---
solution: Journey Optimizer
product: journey optimizer
title: Actualizaciones de la documentación
description: Obtenga información sobre las últimas actualizaciones de la documentación de Adobe Journey Optimizer, incluidas nuevas páginas, reorganizaciones y aclaraciones.
keywords: actualizaciones de la documentación, notas de la versión, optimizador de recorridos, registro de cambios
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: 9c6142de31dfd7e1ce42b0bf0c7fc0be1743312d
workflow-type: tm+mt
source-wordcount: '7217'
ht-degree: 82%
---

# Actualizaciones de la documentación {#latest-updates}

Esta página incluye todos los cambios más recientes en la documentación de [!DNL Journey Optimizer], además de las actualizaciones relacionadas con las características y mejoras de la versión mensual.

## Septiembre de 2026 {#september-2026}

* Las protecciones de `inAudience` ahora incluyen la solución para las zonas protegidas con más de 5000 audiencias, donde las audiencias más antiguas se pueden rechazar durante la creación de recorridos porque la validación solo comprueba las 5000 audiencias actualizadas más recientemente. [Más información](../building-journeys/functions/functioninaudience.md#guardrails)

* Se ha ampliado la orientación para las páginas espejo de correo electrónico: la documentación ahora explica que las direcciones URL de las páginas espejo no se pueden recuperar a través de una API pública o un conjunto de datos, recomienda la exportación de mensajes o el archivado según CCO para conservar el contenido enviado y aclara que los vínculos de las páginas espejo están inactivos en las pruebas y simulaciones. [Más información](../email/message-tracking.md#mirror-page)

* Ahora hay disponible una nueva página **Demostración interactiva** para Desafíos de fidelidad, que se vincula a una demostración autoguiada en la que se puede hacer clic y que cubre el flujo de creación de desafíos del experto en marketing (incluidos sus propios datos y los paneles de perspectivas), la experiencia del cliente final y la administración de desafíos de fidelidad en CX Coworker. [Más información](../loyalty-challenges/loyalty-challenges-demo.md)

* Se ha ampliado y mejorado la página **Personalizar el fondo del correo electrónico**. Ahora documenta la lista desplegable completa de **Colocación de imágenes** para imágenes de fondo y agrega nuevas prácticas recomendadas para colores e imágenes de fondo, incluida la recomendación de probar imágenes de fondo en clientes de correo electrónico reales en lugar de depender únicamente de la vista previa de Designer de correo electrónico. [Más información](../email/backgrounds.md)

* Se ha reorganizado y aclarado el contenido de **Diseño desde cero con la página Designer de correo electrónico**: distingue la estructura de la columna **[!UICONTROL n:n]** de las estructuras preestablecidas fijas, documenta que el recuento de columnas de una estructura se puede aumentar sin perder el contenido existente, explica el comportamiento de apilamiento de columnas en dispositivos móviles y agrega un nuevo paso en el uso de **[!UICONTROL Módulos]** para la creación de correo electrónico de inicio rápido. [Más información](../email/content-from-scratch.md)

* La página **Diseña tu recorrido** ahora incluye una sección de tutorial completa sobre la nueva experiencia de lienzo, que cubre cómo agregar actividades, usar los iconos de la barra de herramientas, seleccionar varias actividades para acciones masivas, copiar y pegar actividades, y unir o desasociar ramas. [Más información](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

* Se han agregado nuevas directrices para comprobar la entrega de acciones personalizadas: la página **Ejemplos de consultas de conjuntos de datos** ahora explica cómo elegir entre los conjuntos de datos Evento de comentarios de mensajes, Seguimiento de correo electrónico y Evento de pasos de Recorrido según el tipo de acción, y documenta cómo resolver el error &quot;Tabla no aprovisionada para el conjunto de datos&quot;. Las páginas **Información general sobre los eventos de paso de Recorrido** y **Solucionar problemas de la ejecución del recorrido en directo** se han actualizado en consecuencia, lo que aclara que una llamada de acción personalizada correcta solo confirma que Journey Optimizer ejecutó la acción, no que el sistema externo entregó un mensaje. [Más información](../data/datasets-query-examples.md#choose-the-correct-dataset)

* Se ha agregado información sobre CX Coworker a la página **Trabajar con IA**, que abarca qué es CX Coworker, cómo se relaciona con el Asistente de IA y referencias a la documentación oficial de Coworker. También se han agregado páginas de aptitudes dedicadas a cada guía de capacidades: [aptitudes de CX Coworker para recorridos](../building-journeys/journeys-coworker-skills.md), [aptitudes de CX Coworker para la lealtad](../loyalty-challenges/loyalty-coworker-skills.md) y [herramientas de administración de contenido de CX Coworker](../content-management/content-management-coworker-skills.md). [Más información](../start/ai-features.md#cx-coworker)

* Se ha documentado una nueva aptitud de **Analizar anomalías de Recorrido** en **Analizar Recorrido** en la página de CX Coworker. Detecta picos, caídas o líneas planas inesperados en los recuentos de entrada, salida o envío de un recorrido con respecto a las líneas de base históricas, y ejecuta diagnósticos de solo lectura para detectar una causa raíz probable. [Más información](../building-journeys/journeys-coworker-skills.md#journey-analyze)

* Las páginas **Protecciones y limitaciones** y **propiedades de Recorrido** se han actualizado para documentar el límite predeterminado de carga útil de recorrido como **2 MB (2.000.000 bytes)**, aclarar que el valor refleja la definición de recorrido serializada en lugar de solo el recuento de actividades y explicar los umbrales de advertencia del 90 % y bloqueo del 100 %. [Más información](../start/guardrails.md#journey-payload-size) y [Más información](../building-journeys/journey-properties.md#journey-payload-size)

* La página **Protecciones y limitaciones** se ha corregido para reflejar el hecho de que los fragmentos visuales de más de 100 KB o los fragmentos de expresiones de más de 200 KB ya no pueden causar problemas de truncamiento en las entregas de correo electrónico: ahora se aplica una única protección de tamaño de fragmento de 700 KB. [Más información](../start/guardrails.md#fragments-guardrails)

* Se ha corregido la página **Crear una actividad en directo**: el campo `executionMetadata` solo está disponible para **campañas transaccionales activadas por API**, no para campañas de marketing activadas por API como se indicó anteriormente. [Más información](../mobile-live/create-mobile-live.md#metadata)

* La documentación de **Conjunto de datos de evento de comentarios de mensajes de AJO** se ha ampliado para aclarar que cubre los comentarios de entrega de mensajes en todos los canales (correo electrónico, SMS/RCS/MMS, correo directo), no solo correo electrónico y push, y ahora incluye una sección de **Clasificar ejecuciones de prueba y no de prueba** que explica cómo interpretar el campo `isTestExecution`, incluidos `NULL` o los valores que faltan. [Más información](../data/datasets-query-examples.md#classify-test-executions)

* Se ha documentado una nueva funcionalidad **Content Management** para CX Coworker, con 15 herramientas MCP de lectura y escritura que le permiten detectar, crear, actualizar, clonar y publicar plantillas de contenido, fragmentos, páginas de aterrizaje y contenido de mensajes en línea de recorrido/campaña utilizando indicaciones en lenguaje natural. [Más información](../content-management/content-management-coworker-skills.md#content-management)

* La documentación de **Agregar contenido a la página de aterrizaje** ahora describe la opción **Hacer obligatorio el campo de formulario** para las casillas de verificación de consentimiento: cuando está habilitada, el formulario no se puede enviar a menos que la casilla de verificación esté seleccionada y se aplique tanto en el lado del cliente como en el del servidor. [Más información](../landing-pages/lp-content.md#use-form-component)

* La página **Introducción a la simulación de Recorrido** se ha actualizado para documentar que los nodos de decisión de contenido y el método de regla de segmentación de la actividad **Optimize** ahora son compatibles con la simulación (anteriormente enumerados como bloqueo), con una nueva tabla de **Toma de decisiones** que detalla cómo se evalúan la elegibilidad de la oferta, las reglas de elegibilidad, las audiencias y los métodos de clasificación durante la ejecución de la simulación. [Más información](../building-journeys/simulate-journey-gs.md#limitations)

* La página **Convertir imágenes en plantillas de contenido de correo electrónico** se ha corregido para eliminar un requisito de permisos impreciso: el permiso **Administrar plantillas de contenido** no es necesario para acceder y crear plantillas con el convertidor de imagen a HTML; solo se necesita el permiso **Generar contenido**. [Más información](../content-management/image-to-html.md#access-image-to-html)

* Se ha corregido la página **Sistemas externos (acciones personalizadas)**: el disyuntor para extremos de acción personalizada lentos ahora se activa cuando más del 20 % de las llamadas en una ventana de 120 segundos superan los **5 segundos** (anteriormente documentados como 10 segundos). [Más información](../configuration/external-systems.md#response-time)

* La página **Configurar la configuración de su canal** ahora incluye una nota que aclara que el esquema utilizado para la dimensión secundaria debe tener una clave principal y que las claves principales compuestas no son compatibles. [Más información](../orchestrated/channel-config.md)

* Se han actualizado las páginas de **Datos y conjuntos de datos de fidelización** y **Introducción a las fuentes** para incluir LAVA como conector de fidelidad y recompensas compatible, junto con Talon.One, Capillary y Kobie. [Más información](../loyalty-challenges/loyalty-data-and-datasets.md)

## Agosto de 2026 {#august-2026}

* La página **Agregar fragmentos visuales a tus correos electrónicos** ahora aclara que un fragmento con contenido dinámico y un estado predeterminado vacío aparece en blanco en el Designer de correo electrónico, simula con un perfil coincidente para obtener una vista previa del contenido. [Más información](../email/use-visual-fragments.md#fragment-dynamic-content)

* La página **Seguir tus mensajes** se ha actualizado para aclarar que los caracteres de URL no admitidos (por ejemplo, apóstrofos) deben tener una codificación porcentual y que, si no se codifican, pueden romperse los vínculos seguidos y los parámetros de seguimiento de URL. [Más información](../email/message-tracking.md#insert-links)

* La página **Enviar mediante oleadas** se ha actualizado para documentar que la última oleada de un recorrido de lectura-audiencia debe programarse en un plazo de **6 días y 18 horas** desde el inicio del recorrido. Si se supera esta ventana, se déclencheur un error de validación y se evita que la recorrido entre en el modo de prueba o se active. [Más información](../delivery/send-using-waves.md#limitations-guardrails)

* Se ha agregado una nueva sección **Suprimir eventos de comentarios** a la página **Recopilación de datos de administración de decisiones**, en la que se documenta cómo usar el indicador `dryRun` para suprimir eventos de decisión durante las pruebas y evitar que se recopilen comentarios para los contadores de informes y límite de frecuencia. [Más información](../offers/data-collection/data-collection.md#suppress-feedback)

* Ya está disponible la nueva página **Elegir un método de validación**. Compara la simulación de Recorrido, el modo de prueba y la ejecución en seco de Recorrido: los datos que utiliza cada uno, independientemente de si envía mensajes reales, errores comunes que se deben evitar y una guía de decisión para elegir el método adecuado en cada fase de la creación de un recorrido. [Más información](../building-journeys/choose-validation-method.md)

* La página **Mecanismos de protección y limitaciones** se ha actualizado para aclarar los mecanismos de protección de la actividad de calificación de público y los eventos: la redacción ahora hace referencia de forma coherente a las **actividades** de calificación de público (en lugar de a los nodos), incluso cuando se utilizan como criterios de salida, y ambos mecanismos de protección ahora abarcan de forma explícita los recorridos **activos, cerrados, pausados, en modo de prueba y de ensayo**. [Más información](../start/guardrails.md#audience-qualif-g)

* Se ha añadido una nota a la sección **Optimización del tamaño de la prueba HTML** para aclarar que los tamaños de prueba reflejan el tamaño de la plantilla HTML (barra de controlador al valor mínimo), no el tamaño final del correo electrónico enviado, que puede ser más grande una vez que las expresiones dinámicas se resuelven en el momento del envío. [Más información](../email/create-email.md#optimize-html-proof)

* Se ha añadido una nueva sección **Limitaciones del explorador web móvil** a la página **Introducción al diseño de correo electrónico**, que documenta por qué los correos electrónicos pueden procesarse de forma diferente en Gmail u Outlook cuando se accede a ellos a través de un explorador móvil, junto con una sugerencia de solución. [Más información](../email/get-started-email-design.md#mobile-web-limitations)

* Se ha añadido una nueva sección de **Consideraciones de procesamiento de Outlook** a la página **Introducción al diseño de correo electrónico**, en la que se enumeran las peculiaridades comunes de Outlook que se deben tener en cuenta durante el diseño: números pares para el relleno y las anchuras, anchos de tabla basados en píxeles, atributos de anchura de imagen HTML, texto ALT, bordes de celdas de tabla y esquinas redondeadas. [Más información](../email/get-started-email-design.md#outlook-tips)

* La página **Mecanismos de protección de tiempo de vida del conjunto de datos (TTL)** se ha actualizado con una tabla **Conjuntos de datos afectados** significativamente ampliada, que ahora cubre todos los conjuntos de datos generados por el sistema de Journey Optimizer (incluidos varios que no se habían enumerado anteriormente, como el servicio de consentimiento de AJO, el perfil de mensajería interactiva, el perfil push y los conjuntos de datos de exportación de mensajes) junto con una nueva columna **Disponibilidad** que indica si cada conjunto de datos se incluye de forma predeterminada o requiere un complemento o licencia específicos. La página **Mecanismos de protección y limitaciones** también se ha actualizado para reflejar la fecha de aplicación confirmada para este mecanismo de protección: el cambio se aplicará en **zonas protegidas de clientes existentes** a partir del **1 de octubre de 2026**. [Más información](../data/datasets-ttl.md#datasets)

* Se ha añadido una nueva sección **Uso del modo de configuración de imagen** a la documentación de contenido generativo. En ella se explican los modos **Equilibrado**, **DAM** y **Creative** disponibles en **[!UICONTROL Configuración de imágenes]**, que controlan si el contenido generado por IA utiliza imágenes de su biblioteca de administración de recursos digitales, las genera con IA o las mezcla. [Más información](../content-management/generative-uc.md#image-mode)

* La descripción de **Destinos** en **Navegación izquierda > Secciones principales** se ha actualizado para tener en cuenta que las organizaciones con [!DNL Real-Time CDP] o [!DNL Adobe Journey Optimizer] también pueden activar audiencias en destinos de personalización aptos, como [!DNL Adobe Target], desde el catálogo de destinos de Experience Platform. [Más información](../start/user-interface.md#main-sections)

* Se han añadido vídeos de procedimientos a la documentación de Retos de fidelización para crear desafíos, configurar proveedores de recompensas y supervisar el rendimiento de los desafíos. [Vea los vídeos del desafío](../loyalty-challenges/create-challenges.md#video), [vea el vídeo del proveedor de recompensas](../loyalty-challenges/reward-definition-guide.md#video) y [vea el vídeo del informe](../loyalty-challenges/loyalty-reporting.md#video).

## Julio de 2026 {#july-2026}

* Se ha añadido una nueva sección **Configuración de envío** a la navegación de la documentación. Agrupa funciones relacionadas con el envío que se aplican a todos los recorridos, las campañas y las campañas orquestadas: **Envío por oleadas**, **Optimización del tiempo de envío** y **Optimización del canal** se han movido allí desde la sección de Recorridos.

* Las páginas de documentación separadas de **Envío por oleadas** para recorridos y campañas de acción se han combinado en una sola página y ahora también abarcan campañas orquestadas. [Más información](../delivery/send-using-waves.md)

* Se ha añadido una sugerencia que apunta al artículo de la comunidad de Experience League sobre **cómo desasociar y volver a unir nodos** en el nuevo lienzo del recorrido a la página **Diseño de su recorrido**. [Más información](../building-journeys/using-the-journey-designer.md)

* La sección de componentes **Cuadrícula** se ha añadido a la página **Componentes de contenido del Diseñador de correo electrónico**. Permite organizar el contenido en una cuadrícula estructurada de filas y columnas, donde cada celda puede contener otros componentes de contenido. [Más información](../email/content-components.md#grid)

* La documentación de la **API de migración de decisiones** se ha actualizado con una aclaración que indica que la zona protegida de destino **puede ser la misma que la de origen**. El proceso de migración gestiona este escenario y garantiza la integridad de los datos independientemente de si los objetos se migran dentro de la misma zona protegida o a una diferente. [Más información](../experience-decisioning/decisioning-migration-api.md#target-sandbox-preparation)

* La documentación de la API de migración de decisiones **Decisioning** se ha mejorado con instrucciones completas para migrar objetos de administración de decisiones a Decisioning. Las nuevas secciones incluyen: referencia de asignación de entidades con 10 convenciones de nomenclatura, cobertura en ámbito frente a fuera de ámbito, comparaciones detalladas de modelos de solicitud/respuesta, tres patrones de implementación (del lado del cliente, del lado del servidor, híbrido) con administración de cookies, requisitos de seguimiento de eventos con 5 ejemplos de JSON de evento, requisitos previos de migración entre zonas protegidas, un proceso de migración de extremo a extremo de 5 pasos y preguntas frecuentes sobre migración. [Más información](../experience-decisioning/decisioning-migration-api.md)

* Ahora hay disponible una nueva página de **Aptitudes de CX Coworker**. Proporciona documentación completa de todas las aptitudes de recorrido disponibles en Journey Optimizer, incluidas la creación de recorridos, la creación de contenido de canal, la administración de retos de lealtad y el análisis de recorridos, con casos de uso, indicaciones de muestra y prácticas recomendadas para cada aptitud. [Más información](../start/ai-features.md#cx-coworker)

* La documentación de la función **A Precisión** se ha actualizado para aclarar que `toPrecision` se comporta como `toFixed()` JavaScript: devuelve una cadena con un número fijo de decimales, incluido el relleno cero cuando es necesario. [Más información](../personalization/functions/math.md#to-precision)

* La página **Finalizar un recorrido** se ha actualizado para aclarar la temporización de la detención automática de los recorridos de público de lectura no recurrentes: un búfer de seguridad de aproximadamente **96 horas (~4 días)** después de la ejecución programada (ventana sin actividad de 24 horas + asignación de horas de inactividad de 72 horas), durante el cual el recorrido puede permanecer en el estado **Activo** antes de pasar a **Detenido** poco después de que transcurra el búfer. La página ahora también aclara que los recorridos basados en oleadas (multioleada) y los recorridos que utilizan la optimización del tiempo de envío se excluyen de esta parada automática y, en su lugar, siguen el tiempo de espera de recorrido estándar de 91 días. [Más información](../building-journeys/end-journey.md#auto-stop-non-recurring)

* La página **Crear campañas de calentamiento de IP** se ha actualizado para aclarar que se pueden aplicar reglas de segmentación a las campañas de calentamiento de IP y para documentar el comportamiento de evaluación: la pertenencia al público se corrige al ejecutar la activación (segmentación por lotes diaria), mientras que los atributos de perfil se leen en el momento de la ejecución a partir de los datos por lotes ingeridos más recientemente. [Más información](../configuration/ip-warmup-campaign.md)

* Se ha añadido una advertencia a la página **Editar registros PTR** para informar a los clientes de que, al incluir un nuevo registro DNS de reenvío a su plataforma, el registro de DNS de reenvío del subdominio anterior no debe quitarse hasta que se complete el movimiento, ya que esto provocará que la edición falle. [Más información](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

* Las páginas **Envío por oleadas** se han actualizado para aclarar el comportamiento de reevaluación de públicos en todas las oleadas: la pertenencia al público se corrige en el momento de la activación (captura de pantalla), pero los atributos de perfil y el consentimiento se evalúan en el momento en que se procesa cada oleada. Esto significa que se respetan las exclusiones que se producen entre oleadas. Puede leer más información en la [sección de preguntas frecuentes](../delivery/send-using-waves.md#faq).

* La página **Gobernanza de datos** se ha actualizado para aclarar que la aplicación de la directiva DULE se aplica solo a **campos de atributos de perfil**. No se admiten los campos basados en eventos (atributos de contexto como los campos de evento de recorrido): las etiquetas aplicadas a esos campos en la interfaz de usuario no restringirán la utilización de datos. [Más información](../action/action-privacy.md)

* La documentación de **Optimización del tiempo de envío** se ha actualizado para reflejar el nuevo límite **[!UICONTROL Enviar dentro de las próximas]** de **2-100 horas** (antes era de 1-168) y para documentar las regiones de AEP Hub admitidas para esta funcionalidad. [Más información](../building-journeys/send-time-optimization.md#use-send-time-optimization)


* Las páginas del **Modelo de optimización personalizada** se han actualizado para reflejar las mejoras del modelo más recientes, que abarcan el funcionamiento del modelo ensamblado, los requisitos de conjuntos de datos, los casos de uso, las suposiciones clave y el comportamiento de inicio en frío. Obtenga más información en las secciones [Decisiones sobre experiencias](../experience-decisioning/ranking/personalized-optimization-model.md) y [Toma de decisiones sobre ofertas](../offers/ranking/personalized-optimization-model.md).

* Se ha añadido una nota a la página **Fórmulas de clasificación de mediación de recorridos** para especificar que las fórmulas de clasificación solo están disponibles para las organizaciones que han adquirido la oferta del complemento **Toma de decisiones**. [Más información](../conflict-prioritization/journey-ranking-formulas.md)

* Ahora hay disponible una nueva página de **Fragmentos dinámicos**. Documenta cómo utilizar la resolución dinámica de fragmentos en [!DNL Journey Optimizer] para seleccionar qué fragmento publicado se inserta en un mensaje durante el tiempo de ejecución, en función de atributos de perfil, búsquedas de conjuntos de datos o datos de contexto pasados en el momento del envío. [Más información](../content-management/dynamic-fragments.md)

## Junio de 2026 {#june-2026}

* La página **Comprobación y envío de un mensaje de correo directo** se ha actualizado para aclarar la temporización y el comportamiento de agrupamiento de las exportaciones de correo directo, incluida la programación fija de 4 horas UTC, por qué se pueden generar varios archivos en un solo día, cuándo se ejecuta **[!UICONTROL Actualizar perfil]** en recorridos y recomendaciones para escenarios de un archivo por día. [Más información](../direct-mail/test-send-direct-mail.md#dm-export-timing)

* Ahora hay disponible una nueva página de **Tipos de recorrido: elija el correcto**. Compara todos los puntos de entrada del recorrido (Leer público, Calificación de público, Evento unitario y Evento empresarial) con guías de decisión y una matriz de compatibilidad de funciones que le ayudará a seleccionar el tipo adecuado para su caso de uso. [Más información](../building-journeys/journey-types-selection.md)

* Ahora hay disponible una nueva página de **Recorridos frente a campañas**. Compara recorridos, campañas de acción y campañas activadas por API en estilos de ejecución, modelos de datos y casos de uso, incluida la activación del canal de entrada para la personalización de Edge con baja latencia, el envío de entrada de varias superficies y la orientación sobre cuándo utilizar campañas orquestadas (composición de público ad hoc, datos federados). [Más información](../start/journeys-vs-campaigns.md)

* La página **Modo de alto rendimiento** se ha actualizado para reflejar la disponibilidad regional ampliada: la función ya está disponible en todas las regiones, excepto en Suiza para organizaciones con licencia con el complemento de mensajería transaccional de alto rendimiento. [Más información](../campaigns/api-triggered-high-throughput.md)

* Se ha añadido una nueva sección **Perfiles interesados y uso de licencias** a la página **Introducción a los perfiles** como única fuente de confianza para este concepto, con referencias de destino incorporadas a las secciones Públicos, Campañas y Toma de decisiones. [Más información](../audience/get-started-profiles.md#engageable-profiles)

* La documentación de la actividad **División** se ha actualizado para documentar el campo **[!UICONTROL Código de segmento]** disponible en la configuración de cada subconjunto, lo que le permite asignar un identificador único a cada segmento del público con fines de seguimiento y creación de informes. [Más información](../orchestrated/activities/split.md)

* La página **Configuración de una dimensión de segmentación** se ha actualizado para documentar los dos tipos de dimensiones de segmentación disponibles en las campañas orquestadas: la **dimensión de segmentación de perfiles** integrada (no se requiere configuración) y las **dimensiones de segmentación personalizadas** basadas en esquemas relacionales. [Más información](../orchestrated/target-dimension.md)

* Se ha aclarado la documentación de **Uso de temáticas en un fragmento** para documentar explícitamente el límite de compatibilidad de cinco temáticas (incluida la restricción de temática predeterminada de Adobe) y explicar que la inserción de fragmentos se bloquea cuando la temática de correo electrónico no es una de las temáticas asociadas a fragmentos. [Más información](../email/apply-email-themes.md#leverage-themes-fragment)

* Las páginas **Introducción a los conjuntos de datos** e **Introducción a los esquemas** se han actualizado con instrucciones sobre la habilitación de conjuntos de datos y esquemas para el Perfil del cliente en tiempo real, incluidas consideraciones clave, la distinción entre la deshabilitación de un conjunto de datos y su esquema subyacente y vínculos a la documentación de prácticas recomendadas y planificación de Adobe Experience Platform. [Más información sobre los conjuntos de datos](../data/get-started-datasets.md) y [más información sobre los esquemas](../data/get-started-schemas.md)

* Ya está disponible un nuevo centro de incorporación de **Introducción a Adobe Journey Optimizer**. Los nuevos usuarios pueden elegir su ruta por función, explorar los aspectos básicos o ir a las áreas diarias si ya están incorporados, sin necesidad de saber dónde buscar primero. [Más información](../../rp_landing_pages/get-started-landing-page.md)

* Una nueva página de **Empiece desde su meta** le permite comenzar desde lo que desea lograr, en lugar de desde un nombre de característica. Asigna las metas empresariales a la funcionalidad [!DNL Journey Optimizer] recomendada en la configuración, los recorridos, las campañas, la personalización, la toma de decisiones y la creación de informes. [Más información](../start/ajo-use-case-guide.md)

* La guía de funciones de **Introducción para desarrolladores** se ha actualizado con introducciones más claras para cada sección y pestañas mejoradas de **Colaboración entre funciones** que hacen referencia a recorridos y vinculan a páginas de implementación clave. [Más información](../start/path/developer.md)

* Se ha añadido una nueva subsección **Asignación de ruta al volver a entrar al recorrido** a la documentación de **Experimentación de rutas**. Aclara que la asignación de ruta es persistente para un perfil en varias entradas en la misma versión de recorrido, pero solo dentro de esa versión de recorrido. Las asignaciones se restablecen cuando se publica una nueva versión del recorrido y cada actividad de experimentación de rutas de un recorrido aplica una asignación aleatoria independiente. [Más información](../building-journeys/path-experimentation.md#path-assignment)
* Las referencias a **Adobe Experience Cloud** se han alineado con la marca **[!DNL Adobe CX Enterprise]** en la documentación de [!DNL Journey Optimizer].

* La documentación de la función de fecha **`nowWithDelta()`** se ha actualizado para aclarar el comportamiento de final de mes: cuando el mes de destino tiene menos días que el día del mes actual, el resultado se normaliza al último día válido de ese mes. [Más información](../building-journeys/functions/date-functions.md#nowWithDelta)

* La página **Introducción a la entregabilidad** se ha actualizado con una nueva subsección **Proveedores sin FBL por destinatario**. Enumera los principales proveedores de buzones de correo que no devuelven quejas de correo no deseado por destinatario (Gmail/Google Workspace, Apple iCloud y Corporate Microsoft 365/Exchange Online) y explica por qué no se espera una entrada de lista de supresión para los destinatarios que utilizan estos servicios. [Más información](../reports/deliverability.md#providers-no-fbl)

* **Decisiones sobre experiencias ya está disponible para el canal de correo directo.** Una nueva página de **Toma de decisiones por lotes en correo directo** describe cómo usar el motor de toma de decisiones para personalizar archivos de extracción de correo directo o para exportar perfiles y sus resultados de toma de decisiones para usarlos en sistemas descendentes. **El correo directo** se ha añadido como un canal admitido en la documentación de toma de decisiones (Introducción, Crear una política de decisión, Usar políticas de decisión en mensajes, Introducción a las políticas de decisiones), incluida la capacidad de devolver varios elementos de decisión por perfil a través del campo **[!UICONTROL Número de elementos]**. [Más información](../experience-decisioning/batch-decisioning-direct-mail.md)

* La documentación de **Fragmentos del recorrido** ya no se marca como Disponibilidad limitada. La página ahora incluye una nota para evitar la ambigüedad entre los fragmentos de recorrido del contenido **[!UICONTROL Fragmentos]** y **Fragmentos de contenido de AEM** (enlazados entre las tres páginas), y documentos compatibles con **Herramientas de zona protegida**, **Registros de auditoría** y **Etiquetado**. Los fragmentos del recorrido también se han añadido a la página **Introducción al recorrido**. [Más información](../building-journeys/journey-fragments.md)

* La documentación de **Fuentes de datos externas** y **Acción personalizada** se ha actualizado para la autenticación personalizada. El campo `tokenInResponse` ahora le permite especificar si `access_token` o `id_token` se utilizan como credencial de autenticación cuando un punto final devuelve ambos. Para la autenticación personalizada basada en certificados, los campos `subType` y `aud` ahora son obligatorios, el punto final del token `method` debe ser `POST` y las referencias a “Azure Entra ID” se han corregido a “Microsoft Entra ID”. [Más información](../datasource/external-data-sources.md#certificate-credential)

* La página **Introducción a la toma de decisiones** se ha actualizado con un gráfico de procesos que resume el flujo de trabajo de extremo a extremo de la toma de decisiones, desde la administración de elementos de decisión y la configuración de estrategias de selección hasta la incrustación de políticas de decisión en un recorrido o campaña. [Más información](../experience-decisioning/gs-experience-decisioning.md#process)

* La documentación de **Encabezados de remitente** ahora aclara que el **[!UICONTROL Nombre de remitente]** y el **[!UICONTROL Correo electrónico del remitente]** deben estar establecidos o ambos vacíos, de lo contrario, no se pueden publicar recorridos y campañas. [Más información](../email/header-parameters.md#sender-header)

## Mayo de 2026 {#may-2026}

* Las limitaciones y prácticas recomendadas al usar contenido dinámico en fragmentos visuales se han combinado en una sola sección **Administración de contenido condicional en fragmentos** para mejorar la legibilidad. [Más información](../email/use-visual-fragments.md#fragment-dynamic-content)

* Se han añadido dos nuevos permisos de alto nivel: **Administrar registro de claves**, que permite a los usuarios ver, crear, rotar y revocar claves del registro de claves, y **Ver registro de claves**, que permite a los usuarios ver la lista del registro de claves y los detalles de las claves. [Más información](../administration/high-low-permissions.md#administration-permissions)

* La documentación de **Uso de políticas de decisión en mensajes** ahora describe cómo ver la estructura completa de una política de decisión desde el resumen de la campaña y copiar un resumen técnico JSON en el portapapeles para la resolución de problemas. [Más información](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

* Se ha reescrito la página heredada [Modelos de optimización automática](../offers/ranking/auto-optimization-model.md) de **Gestión de decisiones** para adaptarla a la documentación actualizada sobre tomas de decisiones, incluyendo información general sobre el aprendizaje mediante refuerzo, requisitos y limitaciones, optimización del equilibrio con el aprendizaje y detalles del muestreo de Thompson. [Más información](../offers/ranking/auto-optimization-model.md)

* La página **Notas de la versión** se ha reestructurado con un diseño basado en temas. Los cambios ahora se agrupan por área de producto en lugar de por tipo de cambio, con una nueva sección **Mejoras de uso** dedicada. Próximamente, las entradas aparecerán como acordeones expandibles dentro de cada tema. [Más información](release-notes.md)

* La página **Mecanismos de protección y limitaciones de las campañas orquestadas** ahora documenta el límite de **actividades de canal** por campaña orquestada. [Más información](../orchestrated/guardrails.md#activities-limitations)

* La documentación de **Copiar objetos de Journey Optimizer entre zonas protegidas** ahora incluye una nota importante para **Campañas orquestadas**: después de la importación, duplique la campaña en la zona protegida de su público destinatario y utilice el duplicado para su ejecución con el fin de garantizar que el sistema de informes capture correctamente los comentarios y datos de seguimiento. [Más información](../configuration/copy-objects-to-sandbox.md#copy-to-sandbox)

* Se ha renovado la página **Terminología clave**: se han añadido seis términos nuevos, se ha introducido una nueva sección **Términos sobre conflicto y priorización** y se ha añadido una nueva guía de desambiguación **Cuando los términos parecen similares** para cuatro pares de términos que suelen confundirse. Los términos específicos de Adobe Experience Platform se han eliminado y reemplazado por una nota que remite al glosario de Adobe Experience Platform. [Más información](../start/terminology.md)

* La documentación de **Enlaces profundos** se ha ampliado con una nueva sección **Creación de enlaces profundos** que detalla las dos opciones disponibles para el correo electrónico (interfaz de usuario del Diseñador de correo electrónico y código del editor de personalización) y la sintaxis de la función URL para SMS. La página **Crear un mensaje SMS** ahora incluye un paso para el enlace profundo en el flujo de creación de contenido. [Más información](../email/deeplinks.md)

* La referencia del asistente de **Url** se ha actualizado con una sección específica en la documentación de Personalización. [Más información](../personalization/functions/helpers.md#url)

* Se ha añadido una limitación a la documentación del asistente de **Metadatos de ejecución**: la función no se admite en los canales entrantes (web, experiencia basada en código, mensaje en la aplicación, tarjetas de contenido). [Más información](../personalization/functions/helpers.md#execution-metadata)

* Se ha añadido la nueva página **Fórmulas de personalización** que proporciona patrones de personalización listos para usar para los casos de uso más comunes de [!DNL Journey Optimizer]. Abarca fórmulas de fecha y hora (formato de fecha actual, cuenta atrás hasta la caducidad, cálculos de días antes, visualización de solo hora y detección de fin de semana vs. día de la semana), fórmulas de cadena (utilizando `replaceAll` con asignación de variables) y fórmulas de reserva condicionales (alternativas para campos vacíos usando `isEmpty`). [Más información](../personalization/personalization-recipes.md)

* La documentación de **Sintaxis de la personalización** se ha actualizado con una introducción ampliada que aclara la diferencia entre las sintaxis de Handlebars (`{{...}}`) y PQL (`{%= ... %}`), incluyendo una tabla de uso, instrucciones sobre cómo escapar las comillas dobles literales y una nueva sección **Reglas de sintaxis de PQL para claves de atributos especiales** que abarca palabras clave reservadas, claves de atributos con guiones e ID de eventos numéricos. También se ha corregido la nota sobre el escape de acentos graves: se puede hacer referencia a los nombres de campo con guiones directamente en bloques `{{...}}`; solo la sintaxis de acento grave falla allí. [Más información](../personalization/personalization-syntax.md)

* La documentación de **Funciones de fecha y hora** se ha enriquecido con nuevos ejemplos reales: un patrón de cuenta atrás para `dateDiff`, un condicional de fin de semana frente al día de la semana para `dayOfWeek` (con una nota sobre el uso de la actividad Condición del recorrido para casos de uso de enrutamiento) y un patrón de visualización de solo hora que combina `extractHours` y `extractMinutes` con una protección de ceros iniciales. [Más información](../personalization/functions/dates.md)

* La documentación de **Funciones de cadena** se ha actualizado con un nuevo ejemplo para `replaceAll` que muestra cómo asignar el resultado a una variable `{% let %}` para su reutilización en varias expresiones en la misma plantilla. [Más información](../personalization/functions/string.md#replace-all)

* La documentación de **Funciones de matriz** se ha actualizado con una nueva sección **Iterar sobre una matriz** que documenta el asistente de bloque `{{#each}}` de Handlebars, incluyendo una nota que aclara que `{{#each}}` solo es compatible con el editor de personalización y no se puede usar dentro de las actividades de condición de recorrido. [Más información](../personalization/functions/arrays-list.md#each-loop)

* La página **Introducción a los conjuntos de datos** se ha actualizado con una nueva entrada **Entrante** en la sección de conjuntos de datos del sistema, que documenta el _conjunto de datos de evento de actividad entrante de AJO_. Se ha añadido una nota para aclarar que un perfil debe tener al menos un mensaje enviado desde [!DNL Journey Optimizer] antes de que los mensajes entrantes se capturen en este conjunto de datos. [Más información](../data/get-started-datasets.md#system-datasets)

* La documentación de **Exportar contenido del mensaje** se ha ampliado con **Preguntas frecuentes sobre la exportación de mensajes** (contenido personalizado, imágenes y medios, vínculos rastreados, PII, retención, casos de uso, etc.) y **ejemplos de JSON exportados de muestra** para SMS y correo electrónico. [Más información](../configuration/message-export.md)

* Una nueva página **Esquema de exportación de mensajes de AJO** documenta todos los campos del conjunto de datos de exportación de mensajes de AJO, con tipos de datos y jerarquía para la carga útil de los correos electrónicos y SMS exportados. [Más información](../configuration/message-export-schema.md)

* Se ha añadido una nueva página **Personalizar direcciones URL en correos electrónicos** que consolida las directrices sobre la personalización de direcciones URL dinámicas, la personalización de direcciones URL completas/base, la personalización de los parámetros de seguimiento de URL y los mecanismos de protección clave. [Más información](../email/url-personalization.md)

* Se ha añadido una nueva sección **Consultas de reglas empresariales** a la página de ejemplos de consultas, que proporciona una consulta de lago de datos para comprobar todos los descartes de perfiles debido a exclusiones de restricción de frecuencia de recorrido en un recorrido específico después de una fecha específica. La consulta incluye el campo `eventCodeReason` para identificar si los perfiles se excluyeron porque se alcanzó un límite (`CAP_REACHED`) o debido a una prioridad inferior (`LOWER_PRIORITY`). [Más información](../reports/query-examples.md#business-rules-queries)

* Se ha actualizado la documentación de **Propiedades del recorrido** para documentar el nuevo indicador **Tamaño de carga útil del recorrido actual** en el panel de propiedades del recorrido. Este campo de solo lectura muestra el tamaño actual de la carga útil de recorrido en comparación con el límite configurado (por ejemplo, 1,5 MB de 2 MB), lo que le ayuda a monitorizar la complejidad del recorrido antes de publicarlo y evitar errores de publicación relacionados con el tamaño. [Más información](../building-journeys/journey-properties.md#journey-payload-size)

## Abril de 2026 {#april-2026}

* La documentación de la actividad **Cambiar dimensión** se ha actualizado para aclarar que mientras la actividad utiliza una unión externa y mantiene todos los registros en el paso de cambio de dimensión, los registros sin un perfil coincidente en la nueva dimensión de segmentación se excluyen silenciosamente en el momento del envío del mensaje. [Más información](../orchestrated/activities/change-dimension.md)

* Se han mejorado los mecanismos de protección de la documentación **Añadir un campo CC a los correos electrónicos**. Ahora especifican que la dirección CC no se comprueba con el consentimiento o la supresión, y que las aperturas y los clics iniciados en los correos electrónicos enviados a la dirección CC se tienen en cuenta en el total de aperturas y clics del análisis de envío. [Más información](../configuration/cc-email-field.md)

* La documentación de **Actividades de canal** se ha actualizado con una nueva sección de **Mensajes de marketing vs. transaccionales** que explica las diferencias de comportamiento entre las dos categorías de canales: requisitos de inclusión, aplicación de reglas empresariales, tipo de configuración de canal y casos de uso recomendados. [Más información](../orchestrated/activities/channels.md#marketing-vs-transactional)

* La documentación de **Actividad de bifurcación** se ha enriquecido con una nueva sección de **Ejemplos** que ilustra cómo usar la actividad de bifurcación para dividir un público en dos ramas de correo electrónico paralelas: una de marketing y otra transaccional, en una sola ejecución de campaña. [Más información](../orchestrated/activities/fork.md#fork-examples)

* La documentación de la **actividad de creación de públicos** se ha enriquecido con un nuevo ejemplo que muestra cómo filtrar perfiles por un atributo de plan de suscripción usando el generador de reglas. [Más información](../orchestrated/activities/build-audience.md#build-audience-examples)

* La página **Introducción a las campañas orquestadas** documenta el patrón de nivel de entrada **Crear público → Bifurcación → Canal A + Canal B** en **¿Qué hay en una campaña orquestada?**, con referencias cruzadas a las páginas de actividad de bifurcación y de mensajes de marketing vs. transaccionales. [Más información](../orchestrated/gs-orchestrated-campaigns.md#gs-ms-campaign-inside)

* La página **Editar contenido de correo electrónico con el editor de HTML avanzado** se ha trasladado de la sección Gestión de contenidos a la sección **Correo electrónico** de la documentación. La página ahora documenta que el editor de HTML avanzado está disponible en el Diseñador de correo electrónico para mensajes de correo electrónico, así como para plantillas de contenido de correo electrónico. [Más información](../email/email-expert-mode.md)

* La documentación de **Iniciar y monitorizar campañas orquestadas** se ha actualizado con una nueva sección que detalla la secuencia de ejecución interna en el tiempo de publicación, junto con una tabla de estado del ciclo de vida de la campaña, una lista de comprobación previa a la publicación y una advertencia de confirmación de envío para campañas no recurrentes. [Más información](../orchestrated/start-monitor-campaigns.md#publication-sequence)

* La documentación de la actividad **Guardar público** se ha actualizado con una nota que aclara que las actividades Guardar público siempre se ejecutan antes que las actividades de mensajes en el momento de la publicación. [Más información](../orchestrated/activities/save-audience.md)

* Se han añadido tres nuevas preguntas y respuestas a las **Preguntas frecuentes sobre campañas orquestadas**: lo que sucede internamente en el momento de la publicación, una lista de comprobación de 7 puntos de motivos por los cuales los mensajes pueden no enviarse después de la publicación y cómo difiere la búsqueda de instantáneas de perfil de la resolución de perfiles en tiempo real. [Más información](../orchestrated/orchestrated-campaigns-faq.md)

* Se ha añadido una nueva sección **[Eventos descartados debido a una instancia de recorrido bloqueada](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached)** a la documentación de solución de problemas del recorrido, en la que se explica el motivo de descarte de `maxInstanceStackEventsReached`, cuándo se produce y cómo mitigarlo. Los mecanismos de protección y las páginas de lista de campos de eventos de los pasos también se han actualizado en consecuencia.

* La documentación de **Aprovechamiento de fragmentos en políticas de decisión** ahora incluye notas de protección para el canal **Correo electrónico**: **[!UICONTROL Simular contenido]** no muestra fragmentos de expresión del elemento de decisión, mientras que **[!UICONTROL Enviar prueba]** y las campañas activadas sí lo hacen. La página también indica que los **[!UICONTROL fragmentos visuales]** no se pueden asignar a un elemento de decisión; solo se admiten **fragmentos de expresiones** en este contexto. [Más información](../experience-decisioning/fragments-decision-policies.md)

## Marzo de 2026 {#march-2026}

* La documentación de **vista previa de experiencias basadas en código con Decisiones sobre experiencias** ahora aclara que **[!UICONTROL Simular contenido]** es solo una vista previa del contenido. Los datos de contexto de las solicitudes activas de Edge no se simulan en la vista previa de la creación. [Más información](../code-based/test-code-based.md#preview-code-based)

* Se ha actualizado la documentación de **Uso de datos de Adobe Experience Platform**: los mecanismos de protección ya no indican que las búsquedas de conjuntos de datos no se pueden encadenar, lo que refleja el comportamiento actual del producto. [Más información](../data/lookup-aep-data.md)

* La documentación de la actividad **Actualizar perfil** se ha actualizado para incluir que ahora se admite la actualización de hasta cinco atributos de perfil en una sola acción. [Más información](../building-journeys/update-profiles.md)

* La actividad **Leer público** y la documentación de **Propiedades del recorrido** se han actualizado para aclarar el ciclo de vida del recorrido de 91 días para recorridos recurrentes siempre activos. La sección de programación ahora confirma explícitamente que los recorridos recurrentes sin fecha de finalización permanecen activos después de 91 días, y las preguntas frecuentes sobre el tiempo de espera global se han ampliado para distinguir el TTL de perfil de 91 días del periodo de creación de informes de 91 días. [Más información](../building-journeys/read-audience.md#schedule)

* La documentación de la actividad **Búsqueda de conjuntos de datos** se ha actualizado para aclarar que la clave de búsqueda debe configurarse en modo avanzado para que la sintaxis de `@datasetLookup{}` funcione en las actividades de condición descendentes. Se ha añadido una sección de solución de problemas con instrucciones para resolver el error “No se ha encontrado la búsqueda de conjuntos de datos”. [Más información](../building-journeys/dataset-lookup.md#troubleshooting)

* La documentación de **Funciones de fecha y hora** se ha actualizado con un nuevo ejemplo que muestra cómo dar formato a una marca de tiempo a partir de un atributo de evento de contexto, incluido el requisito `toDateTime()`, la sintaxis de acento grave para los ID de evento numéricos y una llamada de error común para el error de “entrada no coincidente” de PQL. [Más información](../personalization/functions/dates.md#format-date)

* La documentación de **Limitaciones y mecanismos de protección de campañas orquestadas** e **Introducción a conectores de fuentes** se ha actualizado para aclarar que para la captura de cambios de datos basada en archivos, el campo `_change_request_type` es obligatorio y sus valores deben estar en minúsculas `u` (actualizar) o `d` (eliminar), no en mayúsculas. [Más información](../orchestrated/guardrails.md)

* La documentación de **Añadir vínculos y rastrear mensajes** se ha actualizado con instrucciones sobre cómo se generan los identificadores de seguimiento (urlID): solo se asigna un urlID único cuando la dirección URL y la etiqueta son únicas. Para rastrear la misma dirección URL en varios correos electrónicos (o varias veces en un correo electrónico), los usuarios deben usar una etiqueta única para cada dirección URL similar; de lo contrario, [!DNL Journey Optimizer] no puede determinar en qué vínculo se hizo clic. [Más información](../email/message-tracking.md#track-across-multiple-emails)

* La documentación de **Crear perfiles de prueba** se ha actualizado con una nota importante sobre los requisitos del descriptor de identidad: cuando se elimina y se vuelve a crear un conjunto de datos, el esquema debe conservar el descriptor de identidad correcto en el campo de identidad principal. Sin él, los perfiles ingeridos no se marcarán como `testProfile = true` aunque la ingesta se complete correctamente. Se ha añadido una lista de comprobación de resolución de problemas. [Más información](../audience/creating-test-profiles.md)

* La documentación de la actividad **Leer público** se ha actualizado para aclarar que una actividad de **Evento empresarial** es una excepción a la regla de que Leer público debe ser la primera actividad de un recorrido. También se añadió una nota que hace referencia a la actividad **Optimizar** como alternativa avanzada para controlar la segmentación de público. [Más información](../building-journeys/read-audience.md)

* **Enviar en oleadas** en recorridos ya está disponible de forma general. El indicador de disponibilidad limitada se ha eliminado de la documentación. [Más información](../delivery/send-using-waves.md)

* La documentación de la actividad **Salto** se ha enriquecido con una nueva sección de estrategia de diseño ( **recorridos secundarios de tamaño de mordida**) que explica cómo dividir flujos complejos de extremo a extremo en recorridos secundarios más pequeños y centrados conectados a través de la actividad Salto. [Más información](../building-journeys/jump.md#jump-strategy)

* La documentación de **Etiquetas** se ha actualizado con instrucciones sobre el uso de categorías de etiquetas como alternativa a las convenciones de nomenclatura complejas. En una nueva sección se explica cómo configurar categorías de etiquetas para la administración de recorridos escalable. [Más información](../building-journeys/tags.md)

* La documentación de **Acerca de las fuentes de datos** ahora incluye una nueva sección que ayuda a los profesionales a elegir entre tres estrategias de acceso a datos: acceso a datos externos mediante acciones personalizadas, uso de un conjunto de datos no habilitado para el perfil o uso de un conjunto de datos habilitado para el perfil. Cada opción se describe con compensaciones y casos de uso recomendados. [Más información](../datasource/about-data-sources.md#data-access-strategy)

* La documentación de **Diseño de notificación push** se ha actualizado con una nota que aclara el comportamiento de los vínculos universales en iOS: si la dirección URL de notificación está registrada como vínculo universal, la aplicación asociada se abrirá independientemente de la acción de dirección URL web elegida. Se ha añadido una guía sobre cómo forzar la apertura de un explorador. [Más información](../push/design-push.md)

* Ahora hay disponible una nueva página **Monitorizar sus modelos de IA** en la documentación de Decisioning. Explica cómo realizar un seguimiento del estado, el estado de formación y el rendimiento de los modelos de optimización personalizados directamente en [!DNL Journey Optimizer]. [Más información](../experience-decisioning/ranking/ai-model-observability.md)

* El **editor avanzado de HTML** (modo experto) para plantillas de correo electrónico ya está disponible en disponibilidad limitada. La página de documentación ahora es de acceso público. Esta capacidad le permite ver y editar la fuente sin procesar de HTML de las plantillas de contenido de correo electrónico directamente desde el Diseñador de correo electrónico. [Más información](../email/email-expert-mode.md)

* La documentación de **seguimiento de URL** y **solución de problemas con el recorrido** se ha actualizado para documentar el comportamiento de `context.system.source.actionId` en recorridos cerrados. Los recorridos cerrados o no republicados pueden producir marcadores de posición `{}` vacíos en las direcciones URL de seguimiento. Se ha añadido orientación sobre cómo resolver el problema volviendo a publicar el recorrido o eliminando el parámetro afectado. [Más información](../email/url-tracking.md)

* La documentación de **fuente de datos de Adobe Experience Platform** se ha actualizado con una nota que indica que solo se admiten esquemas basados en perfiles individuales XDM en la configuración de fuente de datos. [Más información](../datasource/adobe-experience-platform-data-source.md)

* La documentación de **mecanismos de protección de periodo de vida (TTL) de conjuntos de datos** se ha mejorado con una nueva entrada de preguntas frecuentes para identificar claramente qué conjuntos de datos están sujetos a TTL. TTL se aplica exclusivamente a conjuntos de datos de series temporales: los conjuntos de datos de tipo de registro, como los conjuntos de datos de entidad, los conjuntos de datos de clasificación y los repositorios de objetos de decisión, no están sujetos a TTL y no se verán afectados por el despliegue de mecanismos de protección. [Más información](../data/datasets-ttl.md)

* La documentación de **propiedades de recorrido** y **Pausar un recorrido** se ha actualizado para documentar los nuevos campos de pausa y reanudación que ahora están disponibles en los detalles técnicos del recorrido. El botón **Copiar detalles técnicos** ahora incluye `lastPausedAt`, `lastPausedBy`, `lastPausedById`, `lastResumedAt`, `lastResumedBy` y `lastResumedById`, además del bloque `pausedJourneySettings` existente. También se ha añadido una nueva sección a la página **Pausar un recorrido** que explica cómo ver las marcas de tiempo de pausa y reanudación directamente desde las propiedades del recorrido. [Más información](../building-journeys/journey-properties.md)

## Febrero de 2026 {#february-2026}

* Ya está disponible una nueva página para la gestión de decisiones. Enumera todos los operadores, ayudas y funciones compatibles al personalizar el contenido de la oferta (representaciones) con el editor de personalización. Utilice esta lista para evitar errores de tiempo de ejecución. Solo se admiten las funciones documentadas al personalizar el contenido en Offer Decisioning. [Más información](../offers/offer-library/personalization-editor-supported-functions.md)

* La documentación de **Crear políticas de decisión** y **Usar políticas de decisión en los mensajes** se ha actualizado para el correo electrónico: una nota explica ahora que cuando la misma oferta se puede seleccionar mediante más de una política de decisión en el cuerpo del correo electrónico, el motor anula la duplicación de ofertas (cada ubicación recibe una oferta diferente). Para mostrar la misma oferta en varias ubicaciones (por ejemplo, en el encabezado y en el pie de página), use **Volver a utilizar el resultado de la decisión**. [Más información](../experience-decisioning/create-decision-policy.md)

* La página Elementos de decisión se ha actualizado con información sobre el canal push y el límite de eventos personalizados. [Más información](../experience-decisioning/items.md#capping)

* La documentación de **Búsqueda de eventos de experiencia en recorrido** se ha actualizado con la cronología de desuso: a partir del 1 de abril de 2026, las organizaciones que no hayan utilizado atributos de eventos de experiencia en expresiones de recorrido en los últimos 90 días ya no tendrán acceso a esta función. Ahora, las preguntas más frecuentes se centran en el calendario de jubilaciones y en quién se ve afectado. La página de esquema de Experience Event se ha alineado con un vínculo directo a enfoques alternativos. [Más información](../building-journeys/exp-event-lookup.md)

* La documentación de **Decisioning** se ha actualizado para la **búsqueda de conjuntos de datos** con datos de Adobe Experience Platform: el mecanismo de protección de canales admitidos ahora indica que la búsqueda de conjuntos de datos funciona para todos los canales donde Decisioning está disponible (experiencia basada en código, correo electrónico, push, SMS y la actividad de decisión de contenido en recorridos). Se han eliminado las notas de disponibilidad limitada y beta pública de las páginas de reglas de decisión, fórmulas de clasificación y elementos de decisión. [Más información](../experience-decisioning/aep-data-exd.md)

* La página Integración de sistemas externos se ha actualizado con vínculos a fuentes de datos personalizadas y acciones personalizadas, y aclara que el proxy de salida proporciona una IP estática para llamadas salientes de **acciones personalizadas** a sus sistemas externos. [Más información](../configuration/external-systems.md)

* Se ha aclarado la documentación de ensayo de recorrido: los atributos de evento de paso `inDryRun` y `dryRunID` ahora documentan que devuelven `true`/ID de instancia cuando se encuentran en el modo de ensayo y `null` para recorridos de prueba o activos. Las directrices para excluir los eventos de paso de ensayo en las consultas de creación de informes se han actualizado en consecuencia. [Más información](../building-journeys/journey-dry-run.md)

* **Web push** ya está disponible de forma general. La documentación de las notificaciones push se ha reestructurado y actualizado en consecuencia (introducción, diseño, envío, creación). [Más información](../push/get-started-push.md)

* La página de configuración de Web push ya está disponible en la documentación. [Más información](../push/push-configuration-web.md)

* Se ha actualizado la documentación sobre el uso de fragmentos en Decisioning: se han añadido notas en las secciones Fragmentos y Decisioning, y se ha actualizado la página Fragmentos en políticas de decisión. [Más información](../experience-decisioning/fragments-decision-policies.md)

* Se ha actualizado la documentación del gancho web SMS: se ha eliminado el contenido del gancho web Twilio. [Más información](../mobile/mobile-webhook.md)

* La documentación de **Convertir imágenes en plantillas de contenido** se ha mejorado con mecanismos de protección y recomendaciones ampliadas, casos de uso comunes y directrices más claras para convertir diseños de imagen en plantillas de contenido editables de HTML. También se menciona el hecho de que ahora puede utilizar una temática como entrada para la conversión. [Más información](../content-management/image-to-html.md)

* Se ha actualizado la documentación de la API de migración de Decisioning. [Más información](../experience-decisioning/decisioning-migration-api.md)

* La actividad **Decisión de contenido** ya está disponible de forma general. La página de actividad de Decisión de contenido se ha actualizado con una sección sobre Datos de toma de decisiones disponibles en eventos de paso. [Más información](../building-journeys/content-decision.md)

* Se han añadido vínculos a la documentación de la API de desafío de fidelidad a la sección Retos de fidelidad (introducción, creación de desafíos, creación de tareas, acceso a desafíos de fidelidad). [Más información](../loyalty-challenges/get-started.md)

* Se ha corregido la información de canales admitidos en la documentación del asistente para la creación de campañas. Las páginas de preguntas frecuentes sobre Introducción a canales y campañas orquestadas se han actualizado en consecuencia. [Más información](../campaigns/get-started-with-campaigns.md)

* Se ha corregido la documentación de permisos con respecto a los permisos de **Administración de recorrido** y **Aprobar**. [Más información](../administration/ootb-permissions.md)

* La documentación de integraciones de AEM (Adobe Experience Manager) se ha actualizado con una nomenclatura revisada (fragmentos de contenido dinámico de AEM y AEM). [Más información](../integrations/aem-fragments.md)

* Se ha añadido un nuevo motivo de exclusión a la lista de exclusiones: **UnsubscribeLinkNotValid** (código de error 050081). Esta exclusión se genera cuando la longitud del asunto de mailTo de cancelación de suscripción a una lista es mayor que el límite RFC de 998 caracteres. [Más información](../reports/exclusion-list.md)

* La documentación de la función de ayuda formatDate se ha mejorado con una nota que indica que la función requiere un tipo de campo de fecha y hora (no una cadena) y con varios ejemplos: formato de un campo de fecha y hora, conversión de una cadena a fecha primero, fecha completa con nombre de día, fecha dinámica desde la hora del sistema y formato de día de la semana, incluido el resultado en minúsculas. [Más información](../personalization/functions/dates.md#format-date)

* La documentación de correo electrónico de la versión de texto se ha mejorado con una guía completa de casos de uso, que incluye criterios de decisión sobre cuándo utilizar texto sin formato personalizado en comparación con la sincronización automática, ejemplos prácticos con escenarios reales y una sección de preguntas frecuentes con preguntas comunes. [Más información](../email/text-version-email.md#when-to-use)

* La documentación de los temas del Diseñador de correo electrónico se ha actualizado con información sobre las limitaciones de compatibilidad con fuentes web y la importancia de las fuentes de reserva. [Más información](../email/apply-email-themes.md#themes-guardrails)

* Se ha añadido una limitación a la documentación del asistente de Metadatos de ejecución para aclarar que los metadatos no se capturan para los perfiles excluidos de la acción. [Más información](../personalization/functions/helpers.md#execution-metadata)

* La documentación de ejemplos de implementación basada en código se ha actualizado para incluir el campo de tokens en propositionAction para un seguimiento y una atribución precisos en Decisioning. [Más información](../code-based/code-based-implementation-samples.md#client-side-how)

* Se ha añadido una nota a la documentación de seguimiento de URL y cancelación de suscripción a la lista para aclarar que el orden de los parámetros de seguimiento de URL anexados a las URL es aleatorio y no se puede controlar. [Más información](../email/url-tracking.md)

## Enero de 2026 {#january-2026}

* La documentación del panel de uso de licencias se ha simplificado con directrices actualizadas sobre **Perfiles atractivos**, incluidos detalles de definición e instrucciones para la solución de problemas. [Más información](../audience/license-usage.md#what-is-engageable-profile)

* Se ha añadido una nota a la documentación de temáticas del Diseñador de correo electrónico para aclarar las limitaciones de compatibilidad con fuentes web. [Más información](../email/apply-email-themes.md#themes-guardrails)

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
