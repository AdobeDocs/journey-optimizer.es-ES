---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: c49af406dc410b4f508835207fc7d1e016a8c38b
workflow-type: tm+mt
source-wordcount: '5024'
ht-degree: 67%
---
# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] sigue un modelo de envío continuo, lo que permite a Adobe ofrecer nuevas funciones, mejoras y correcciones de forma continua. Este enfoque permite un despliegue escalable y gradual de las funciones para garantizar el rendimiento y la estabilidad en todos los entornos. Debido a este modelo, las notas de la versión se actualizan entre versiones mensuales. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

>[!NOTE]
>
>Las funcionalidades que se enumeran en estas notas de la versión incluyen una **Fecha de disponibilidad** que indica cuándo se puede acceder a cada cambio en su entorno. Se esperan entradas en los acordeones de **Próximamente** en los próximos días o semanas. La información de estas secciones está sujeta a cambios.

## Notas de la versión de septiembre de 2026 {#sep-26-updates}

>[!BEGINSHADEBOX]

**Novedades de CX Enterprise Coworker este mes**

Esta versión incorpora varias funciones y habilidades nuevas y mejoradas de [Coworker](../start/ai-features.md#cx-coworker) que se enumeran aquí para mayor visibilidad. Cada una de ellas se detalla también en la sección pertinente que figura a continuación.

* [Complemento de contenido de canal CE](#sep-26-content-management): Un nuevo complemento que reúne las habilidades de HTML de copia de campaña, imagen y correo electrónico en Coworker, desde información de campaña hasta copia y HTML listas para la producción.
* [Herramientas MCP de administración de contenido](#sep-26-content-management): descubra y administre plantillas de contenido, fragmentos, páginas de aterrizaje y contenido de mensajes en línea mediante mensajes en lenguaje natural en Coworker.
* [Simulación del recorrido](#sep-26-journeys): automatice la validación del recorrido de extremo a extremo e interprete los resultados directamente en Coworker.
* [Compare versiones de un recorrido](#sep-26-journeys): obtenga una diferencia estructurada y de fidelidad total entre dos versiones cualesquiera de un recorrido a través del chat de Coworke.
* [Analizar la habilidad de anomalías de Recorrido](#sep-26-journeys): detecta picos, caídas o líneas planas inesperados en los recuentos de entrada, salida o envío de mensajes de un recorrido, con diagnósticos de causa raíz.
* [Aptitud del explicador de la toma de decisiones](#sep-26-decisioning): pregunte al compañero por qué se mostró o no una oferta específica en un perfil o en un segmento y obtenga un seguimiento completo de los requisitos, la clasificación y las exclusiones de reglas.
* [Aptitud para reglas y clasificación](#sep-26-decisioning): cree, explique, simule y optimice reglas de elegibilidad para la toma de decisiones y fórmulas de clasificación en lenguaje natural, sin escribir ni validar manualmente la sintaxis de PQL.

+++ Próximamente — **La siguiente información está sujeta a cambios.**

* [Creación de recorridos desde el carril de Coworker](#sep-26-journeys): genere recorridos con IA directamente desde el carril derecho de Coworker, reemplazando la experiencia anterior del Asistente de IA.
* [Habilidad de recomendación de lealtad](#sep-26-loyalty): solicite oportunidades de reto directamente en la interfaz conversacional de Coworker y conviértalas en retos en directo sin salir del chat.
* [Habilidad Análisis de higiene](#sep-26-journeys): analice los recorridos activos y en borrador para detectar configuraciones dañadas, errores silenciosos y recursos deteriorados o en desuso, con las correcciones recomendadas.
* [Habilidad Análisis del rendimiento empresarial](#sep-26-journeys): analice el rendimiento del recorrido y obtenga recomendaciones de optimización concretas, directamente desde el chat.

+++

>[!ENDSHADEBOX]

### Gestión de contenidos {#sep-26-content-management}

En esta versión, se incorporará la siguiente funcionalidad a la gestión de contenidos.

<table>
<thead>
<tr>
<th><strong>Complemento de contenido de canal en Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible un nuevo complemento <strong>Channel Content</strong> en Coworker, que reúne las aptitudes de HTML de copia de campaña, imagen y correo electrónico ensamblado en un solo complemento, desde la estrategia hasta la implementación. Las siguientes habilidades están disponibles en el complemento <b>Contenido del canal</b>:</p>
<ul>
<li><strong>Crear contenido para orquestar</strong>.</li>
<li><strong>Explorar estrategia de contenido</strong></li>
<li><strong>Resumen de contenido</strong></li>
<li><strong>Generar contenido</strong></li>
<li><strong>Comprobar preparación del contenido</strong></li>
<li><strong>Revisión y regeneración de contenido</strong></li>
<li><strong>Generar imagen</strong></li>
<li><strong>Evaluar el diseño del contenido</strong></li>
<li><strong>Guardar contenido del canal</strong></li>
<li><strong>Crear correo electrónico desde Figma</strong></li>
<li><strong>Búsqueda de marca</strong> </li>
</ul>
<p>Para obtener más información, consulte la <a href="../content-management/content-management-coworker-skills.md#content-management#ce-channel-content">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 24 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Herramientas MCP (Protocolo de contexto de modelo) para la gestión de contenidos en CX Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Coworker cuenta ahora con un nuevo conjunto de <strong>herramientas MCP (Protocolo de contexto de modelo) para la administración de contenidos</strong> que le permite descubrir y gestionar recursos de Journey Optimizer mediante indicaciones con lenguaje natural. Pídale que enumere o recupere plantillas de contenido, páginas de destino y el contenido de los mensaje en línea en recorridos y campañas. También permite crear contenido, actualizar plantillas y crear, actualizar, clonar y publicar fragmentos, además de actualizar el contenido de la acción del canal en línea directamente en el recorrido y la campaña.</p>
<p>Para obtener más información, consulte la <a href="../content-management/content-management-coworker-skills.md#content-management">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 3 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Casilla de verificación de consentimiento obligatoria para las páginas de destino**: ahora puede hacer que una casilla de verificación sea obligatoria en el componente de formulario de la página de destino, de modo que los visitantes tengan que seleccionarla (por ejemplo, para dar su consentimiento) para poder enviar el formulario. [Más información](../landing-pages/lp-content.md#use-form-component)

  Fecha de disponibilidad: 4 de septiembre de 2026

* **Palabras clave reservadas en la sintaxis de personalización**: la lista de palabras clave reservadas en Profile Query Language (PQL) se ha ampliado para incluir palabras clave generales, unidades de tiempo y operadores booleanos/lógicos. Si su esquema XDM contiene un nombre de campo que coincide con una de estas palabras clave, colóquelo entre comillas invertidas para hacer referencia a él en una expresión de personalización. [Más información](../personalization/personalization-syntax.md#reserved-keywords)

  Fecha de disponibilidad: 1 de septiembre de 2026

+++ Próximamente — **La siguiente información está sujeta a cambios.**

* **Validación de URL en Simular contenido**: al obtener una vista previa del contenido, Journey Optimizer ahora comprueba automáticamente los vínculos web que contiene y marca las direcciones URL rotas, inseguras o inaccesibles antes de enviarlo. Esta capacidad está disponible en disponibilidad limitada para un conjunto de clientes.

+++

### Lealtad {#sep-26-loyalty}

<table>
<thead>
<tr>
<th><strong>Actualizaciones en la asignación de eventos de lealtad</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora para crear o editar una asignación de evento se utiliza un nuevo **generador visual de asignaciones**: seleccione un esquema, elija campos en un selector de campos con capacidad de búsqueda, asigne cada campo a un campo de evento de lealtad con un estado de conexión por fila y obtenga una vista previa de la expresión JSONata generada automáticamente, con la opción de cambiar a la edición manual de JSONata en cualquier momento.</p><p>Además, el nombre “Definiciones de eventos” en Administración de lealtad pasa a denominarse “Asignaciones de eventos”, con una vista de lista actualizada que muestra el nombre del esquema de evento de Experience en un formato legible para el usuario.</p>
<p>Para obtener más información, consulte la <a href="../loyalty-challenges/loyalty-admin.md#event-mappings">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 22 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Retos de lealtad “para siempre”**: ahora los retos de lealtad se pueden ejecutar indefinidamente. Establezca la **finalización del reto** en **sin fecha de finalización** cuando configure la programación y el reto nunca caducará. [Más información](../loyalty-challenges/create-challenges.md#schedule)

  Fecha de disponibilidad: 1 de septiembre de 2026

* **Loyalty está disponible para los clientes de Healthcare Shield and Privacy and Security Shield**: Journey Optimizer Loyalty ya está disponible para los clientes de Healthcare Shield and Privacy and Security Shield. [Más información](../loyalty-challenges/get-started.md)

  Fecha de disponibilidad: 15 de septiembre de 2026

+++ Próximamente — **La siguiente información está sujeta a cambios.**

<table>
<thead>
<tr>
<th><strong>Recomendaciones de desafío</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El menú Rendimiento de fidelidad ahora incluye las pestañas **Oportunidades** y **Tendencia**, que muestran tendencias y brechas detectadas por IA, como fricción de progresión de nivel o desactivación de tareas de desafío, cada una con un impacto proyectado y una acción de un solo clic "Crear con IA" para generar un desafío que lo aborde.</p><p>Además, los especialistas en marketing pueden solicitar oportunidades de **desafío** directamente en la interfaz conversacional de Coworker, obteniendo ideas de desafío fundamentadas en tendencias reales de programas de lealtad y convirtiéndolas en desafíos en vivo sin salir del chat.</p>
</td>
</tr>
</tbody>
</table>

* **Plazos para la finalización del desafío de fidelización por miembro**: los desafíos de fidelización ahora admiten los plazos de finalización por miembro: elija &quot;En un número de días después de la inclusión&quot; en Requisitos de finalización para que el plazo de cada miembro se calcule a partir de su propia fecha de inclusión en lugar de una fecha de finalización fija para todo el programa. Si se establecen tanto una fecha de finalización de desafío como esta ventana de inclusión, el plazo de cada miembro es el que sea primero. <!-- Documentation link: TBD -->

* **Dominio de los retos en el editor de personalización de las tarjetas de contenido**: el editor de personalización de las tarjetas de contenido ahora admite **Retos** como dominio, lo que le permite acceder a los metadatos de los retos al crear la personalización de las tarjetas de contenido. Esto facilita la creación de contenido personalizado en cada fase de un reto (iniciar, en curso y finalización) sin código personalizado.

+++

### Recorridos {#sep-26-journeys}

<table>
<thead>
<tr>
<th><strong>Comparar versiones de recorrido con Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Hoy en día, para revisar lo que ha cambiado entre dos versiones de un recorrido, es necesario compararlos manualmente dentro de Journey Optimizer nodo por nodo. No hay diferencia estructurada, lo que hace que las comprobaciones de revisión de cambios, auditoría y prepublicación sean lentas y propensas a errores, especialmente a medida que los recorridos se vuelven más complejos. Esta funcionalidad permite a un cliente o a un agente de IA comparar dos versiones cualquiera de un recorrido a través de Coworker Chat y recuperar una comparación de diferencias **estructurada** de plena fidelidad: nodos añadidos/eliminados/modificados/movidos con detalles de nivel de campo, conexiones cambiadas, cambios de propiedad de nivel de recorrido y recuentos de acumulación, sin necesidad de abrir Journey Optimizer. </p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journeys-coworker-skills.md#journey-analyze">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 24 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulación de recorrido en Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La <strong>habilidad Simulación de recorrido</strong> en Coworker automatiza la validación del recorrido de extremo a extremo y le permite interpretar fácilmente los resultados. Tenga en cuenta que, en la actualidad, esta función solo es compatible con el flujo de simulación rápida y no sustituye por completo a la experiencia de simulación manual de Journey Optimizer.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journeys-coworker-skills.md#journey-simulation">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 23 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Exclusión de nivel de recorrido (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede configurar un grupo de exclusión para los recorridos directamente desde las propiedades del recorrido. Una exclusión es un porcentaje configurable del público destinatario que se excluye de la entrada al recorrido y que no recibe ninguna comunicación. Al comparar los perfiles de exclusión con los perfiles activos en los informes de Customer Journey Analytics, puede medir el alza incremental (el verdadero impacto) que ofrece su recorrido.</p>
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte <a href="releases.md">Ciclo de lanzamiento de Journey Optimizer</a>.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-properties.md#performance-management">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 1 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Generación de expresiones con IA en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El editor de expresiones avanzadas de recorrido ahora incorpora una función de generación de expresiones basada en la IA: describa la expresión que desea crear con lenguaje natural y el editor generará código listo para usar que podrá aplicar de inmediato o mejorar mediante indicaciones de seguimiento.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/expression/generate-expression.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 1 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Compatibilidad con actividades de salto en recorridos de calificación de audiencia**. Ahora puede usar actividades de salto en recorridos que comiencen con un nodo de calificación de audiencia para saltar a recorridos basados en eventos. Esta capacidad se está extendiendo progresivamente a las organizaciones. Si no ve esto en su entorno, puede deberse a que aún utiliza audiencias por lotes en las Cualificaciones de audiencia. [Más información](../building-journeys/jump.md)

  Fecha de disponibilidad: 22 de septiembre de 2026.

* **Déclencheur después de la evaluación de audiencia por lotes**: para los recorridos recurrentes dirigidos a audiencias por lotes, puede configurar un período de espera de hasta 6 horas para una nueva evaluación por lotes antes de que se ejecute el recorrido. Si una evaluación está en curso, el recorrido espera a que se complete; si la ejecución anterior utilizó la instantánea más reciente, espera un lote más reciente. Si no hay ninguna audiencia nueva disponible al final de la ventana de espera, se omite esa incidencia. [Más información](../building-journeys/read-audience.md)

  Fecha de disponibilidad: 18 de septiembre de 2026

* **Toma de decisiones en la simulación del recorrido**: la experimentación de rutas, como parte de la actividad **Optimizar** ya es compatible con la simulación. La toma de decisiones gestiona el enrutamiento, y es aleatoria y no determinista para cada usuario simulado.

  [Más información](../building-journeys/simulate-journey-gs.md)

  Fecha de disponibilidad: 15 de septiembre de 2026

* **Nueva alerta de Anomalía de recorrido detectada**: ahora, una nueva alerta del sistema le avisa cuando el tráfico diario de un recorrido en directo se desvía de su propia línea base histórica o cae hasta cero de forma inesperada, tanto en las entradas de recorrido, como en las salidas del mismo y los envíos de eventos. Esta alerta solo está disponible actualmente en las zonas protegidas de producción.

  [Más información](../reports/alerts.md)

  Fecha de disponibilidad: 15 de septiembre de 2026

* **Toma de decisiones en la simulación del recorrido**: ahora puede simular recorridos que se basan en la toma de decisiones, con los siguientes elementos compatibles recientemente:

  * Los nodos de decisión de contenido ya son compatibles con la simulación.
  * El método Regla de segmentación de la actividad Optimizar ya es compatible con la simulación.
  * Las acciones con contenido decidido por Adobe Journey Optimizer (por ejemplo, un correo electrónico que utiliza una política de decisión) ya son compatibles con la simulación.
  * Las políticas de decisión que utilizan la idoneidad de la oferta y se clasifican según la regla, el público, la prioridad o la fórmula son totalmente compatibles. También se admite la clasificación mediante el modelo de IA: personalización, aunque las ofertas devueltas pueden variar entre una ejecución y otra.

  [Más información](../building-journeys/simulate-journey-gs.md)

  Fecha de disponibilidad: 8 de septiembre de 2026

* **Habilidad Analizar anomalías del recorrido**: ahora, CX Coworker puede detectar picos, caídas o líneas planas inesperados en los recuentos de entradas, salidas o envíos de mensajes en comparación con las líneas base históricas, mediante la habilidad **Analizar anomalías del recorrido**. Una vez confirmada una anomalía real, la habilidad ejecuta los diagnósticos de solo lectura para identificar una posible causa raíz y ofrecer una recomendación. [Más información](../building-journeys/journeys-coworker-skills.md#journey-analyze)

  Fecha de disponibilidad: 2 de septiembre de 2026

* **Nueva función dateDiff en el editor de expresiones del recorrido**: el editor de expresiones del recorrido ahora incluye la función `dateDiff`, que calcula la diferencia entre dos fechas en número de días. Esta función es útil para la lógica basada en tiempo, como la creación de fechas límite, el cálculo de las duraciones del ciclo de vida del cliente o la creación de temporizadores de cuenta atrás en las condiciones del recorrido.  [Más información](../building-journeys/functions/date-functions.md#dateDiff)

  Fecha de disponibilidad: 1 de septiembre de 2026

+++ Próximamente — **La siguiente información está sujeta a cambios.**

<table>
<thead>
<tr>
<th><strong>Tarjetas de recomendación de IA para las alertas de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La página de inicio de Journey Optimizer ahora muestra una <strong>tarjeta de recomendación de IA</strong> cuando se activa una alerta de recorrido que incluye las alertas <strong>Error de Acción personalizada de recorrido</strong> y <strong>Anomalía de recorrido detectada</strong>. Al seleccionar la tarjeta, se abrirá el recorrido con el carril derecho rellenado previamente con el análisis ya realizado.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actividad del recorrido Desactivación de actividad entrante</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nueva actividad <strong>Desactivación de actividad entrante</strong> en el lienzo del recorrido le permite quitar un perfil de hasta cinco actividades o experiencias entrantes directamente desde un recorrido, desvinculando la descalificación entrante de la salida del recorrido para una orquestación de canales múltiples más avanzada.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vista previa del contenido en el lienzo del recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La revisión del contenido del canal hoy en día requiere la apertura de cada actividad de forma individual, de una en una, lenta y propensa a errores en recorridos con muchas actividades de canal, especialmente cuando la personalización significa comprobar varios tratamientos o variantes por actividad. <strong>Vista previa del contenido</strong> elimina esa fricción al mostrar una miniatura de contenido para cada actividad de canal directamente en el lienzo, con un modal de pantalla completa para inspeccionar y cambiar entre tratamientos y variantes.</p>
<p>Fecha de disponibilidad del destinatario: 28 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Creación de recorridos desde el carril de Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La <strong>creación de recorridos con IA</strong> ya está disponible directamente desde el carril derecho de Coworker, reemplazando la experiencia anterior del asistente de IA por un punto de entrada rediseñado e integrado para generar recorridos.</p>
</td>
</tr>
</tbody>
</table>

* **Aptitud para el análisis de higiene**: CX Coworker ahora puede analizar los recorridos activos y en borrador para detectar configuraciones rotas, errores silenciosos y recursos en declive o no utilizados, como recorridos en borrador antiguos, fuentes de datos huérfanas y errores persistentes de acciones personalizadas, así como correcciones recomendadas superficiales directamente en el chat. <!-- Documentation link: TBD -->

* **Compatibilidad con el ID adicional en la simulación de recorrido**: el **ID adicional** ya es compatible con la simulación de recorrido, lo que le permite probar escenarios de usuario complejos tanto para recorridos tanto de lectura de público como para aquellos activados por eventos.

* **Supresión de eventos de paso de ensayo para informes personalizados**: como parte de la optimización de eventos de paso, a partir de ahora, Journey Optimizer deja de generar determinados eventos de paso que no se pueden notificar durante los ensayos de Journey. Esto solo afecta a los informes personalizados creados en estos tipos de eventos de paso de ensayo. Si se ve afectado, vuelva a activar el ensayo para volver a generar los datos.

* **Tiempo de espera de recuperación de evento automático en Propiedades del recorrido**: ahora las propiedades del recorrido incluyen una configuración **Establecer tiempo de espera de recuperación de eventos**: de forma predeterminada, los eventos de recorrido afectados se reproducen automáticamente durante un máximo de 72 horas después de una interrupción del servicio sin necesidad de realizar ninguna acción. Puede activar esta configuración para controlar la ventana de reproducción (0-72 horas) para los recorridos urgentes. El campo **Tiempo de espera o error** existente también ha cambiado de nombre a **Acción personalizada / Tiempo de espera de la fuente de datos** para evitar confusiones entre las dos configuraciones.

* **Se han reducido los eventos de paso para las actividades de espera y evento** - Ya no se generan eventos de paso para las actividades **wait** y **event** cuando el perfil no se ha procesado realmente en esa actividad.

+++

### Campañas {#sep-26-campaigns}

+++ Próximamente — **La siguiente información está sujeta a cambios.**

* **Carpetas para campañas de acción**: ahora puede organizar sus campañas de acción en carpetas para mejorar la navegación y la administración en la interfaz.

* **Anular los campos de ejecución predeterminados en las campañas de acción**: aunque anteriormente estaba disponible a nivel de recorrido, ahora puede anular los campos de ejecución predeterminados configurados globalmente para los envíos por correo electrónico, SMS y WhatsApp en los parámetros de la campaña de acción.

+++


### Canales {#sep-26-channels}

En esta versión, se incorporarán las siguientes funcionalidades y mejoras a los canales.

* **Límite aumentado de delegación de subdominios**: según el contrato de licencia, ahora puede solicitar hasta 3000 subdominios (antes limitados a 100) poniéndose en contacto con su representante de Adobe. Esta capacidad está disponible en disponibilidad limitada para un conjunto de clientes. [Más información](../configuration/delegate-subdomain.md#guardrails)

  Fecha de disponibilidad: 25 de septiembre de 2026

+++ Próximamente — **La siguiente información está sujeta a cambios.**

<table>
<thead>
<tr>
<th><strong>Canal de salida personalizado (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los <strong>canales de salida personalizados</strong> permiten a los administradores incorporar cualquier canal de mensajería de salida basado en HTTP, como WeChat, Kakao Talk, Messenger o un proveedor de propiedad, directamente a Journey Optimizer a través de un generador de canales sin código. Una vez configurados, los canales personalizados están disponibles en cualquier campaña, recorrido y campaña orquestada, con el mismo conjunto completo de funcionalidades que los canales nativos: personalización con el editor de expresiones, experimentación de contenido, previsualización y prueba, creación de informes predeterminada y aplicación de consentimiento y gobernanza.</p>
<p>Con esta versión, los canales de salida personalizados también obtienen varias funciones nuevas:</p>
<ul>
<li>Utilice Journey Optimizer Decisioning en la carga útil del canal personalizado a través del editor de personalización, del mismo modo que en las experiencias basadas en código.</li>
<li>Aplique reglas empresariales a los canales personalizados, del mismo modo que ya lo hace en los canales nativos.</li>
<li>Seleccione canales personalizados en la lista de canales para las campañas activadas por API, algo que antes no era posible.</li>
<!--<li>Define a reporting webhook for a custom channel and attach it to a channel configuration, so you can enrich your Journey Optimizer reports with interaction events.</li>-->
</ul>
<p>Esta capacidad, que antes estaba disponible en disponibilidad limitada, ahora está disponible en todos los entornos (disponibilidad general), con las mejoras descritas anteriormente.</p>
<p><img src="assets/do-not-localize/custom-channel.gif"></p>
<p>Para obtener más información, consulte la <a href="../custom-channel/get-started-custom-channel.md">documentación detallada</a>.</p>

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actividades en vivo para actualizaciones en vivo de Android</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora amplía sus funcionalidades de personalización móvil en tiempo real al ampliar la <strong>compatibilidad de la actividad en vivo con Android</strong>. Puede enviar actualizaciones del progreso en tiempo real directamente a los usuarios, como el seguimiento de los pedidos, los estados de los vuelos, las actualizaciones de eventos en vivo y puntuaciones deportivas en tiempo real.</p>
<p>Además de ser compatible con iOS Live Activities, ahora Journey Optimizer administra tokens push temporales para Android Live Updates en las configuraciones de la plataforma. Es compatible con los flujos de actualización tanto de difusión como transaccionales mediante campañas activadas por API y API headless.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mejoras en las plantillas de notificaciones push de Android</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las notificaciones push de Android se representaban anteriormente con un diseño único y fijo: las imágenes siempre se recortaban en el centro y el texto independiente largo se truncaba. Esta versión incluye un selector de plantillas en el momento de la creación, lo que permite a los expertos en marketing controlar el diseño de las notificaciones push de Android.</p>
<p>Se incorporan las siguientes mejoras:</p>
<ul>
<li><b>Selección de diseño</b>: nuevo selector de diseño de notificaciones push (estándar/expandido) al crear una notificación push de Android.</li>
<li><b>Diseño estándar con “Mostrar toda la imagen”</b>: elija entre recortado para rellenar o escalado para el ajuste.</li>
<li><b>Diseño ampliado</b>: texto independiente multilínea sin truncamiento, además de una miniatura de icono grande opcional.</li>
<li><b>Cuerpo contraído (diseño expandido)</b>: establezca un texto independiente más corto para el estado contraído.</li>
</ul>
</td>
</tr>
</tbody>
</table>

* **Flexibilidad de la autenticación personalizada BYOP para SMS**: ahora puede configurar **encabezados de autenticación personalizados** al conectar la configuración de OAuth de su proveedor de SMS, incluyendo dónde se coloca el token en los mensajes de salida y cómo se da formato a la propia solicitud de token.

* **Correo directo - Dividir archivos grandes automáticamente** - Los archivos de correo directo ahora se pueden dividir en varias partes automáticamente cuando superan los 20 GB, o manualmente eligiendo un tamaño de archivo de destino en la configuración de enrutamiento de archivos.

* **Correo directo: límite de audiencia aumentado**: el límite de audiencia del canal de correo directo se ha aumentado de 3 millones a 100 millones de perfiles, lo que permite dirigirse a audiencias mucho más grandes sin llegar a errores de creación de archivos.

+++

### Campañas orquestadas {#sep-26-orchestrated-campaigns}

<table>
<thead>
<tr>
<th><strong>Alertas para las campañas orquestadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las campañas orquestadas admiten ahora <strong>alertas automatizadas</strong> a través del mismo marco de alertas que se utiliza en los recorridos y las campañas. Las alertas se activan cuando falla la ejecución de una campaña, agota el tiempo de espera y cada alerta incluye lo que ha sucedido, cuándo, dónde y un vínculo directo al lienzo para comprobar más detalles en los registros.</p>
<p>Para obtener más información, consulte la <a href="../orchestrated/start-monitor-campaigns.md#alerting">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 22 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Contenido condicional con datos relacionales en campañas orquestadas**: al crear contenido condicional en el Designer de correo electrónico para campañas orquestadas, ahora puede generar condiciones directamente en datos relacionales, como registros relacionados asociados a un perfil, no solo atributos de perfil estándar. [Más información](../orchestrated/activities/channels.md#add-personalization)

  Fecha de disponibilidad: 22 de septiembre de 2026

* **Uniones directas en colecciones en campañas orquestadas**: al agregar un atributo de una colección relacionada, ahora puede elegir entre tres modos de unión (un nuevo valor predeterminado que le advierte sobre el posible impacto en el rendimiento de los productos cartesianos, además de los modos Agregado y Avanzado existentes), lo que facilita la comprensión de las compensaciones de su consulta antes de crearla. [Más información](../orchestrated/build-query.md#links)

  Fecha de disponibilidad: 22 de septiembre de 2026

+++ Próximamente — **La siguiente información está sujeta a cambios.**

<table>
<thead>
<tr>
<th><strong>Actividad de unión OR para las campañas orquestadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La <strong>actividad de unión</strong> en las campañas orquestadas ahora es compatible con las condiciones de unión AND y OR. Con la lógica OR, un perfil que completa cualquier rama ascendente, en lugar de todas ellas, continúa a lo largo de una sola ruta descendente compartida. Esto permite modelar patrones “si A, B o C, entonces haga esto” directamente en el lienzo sin duplicar los pasos descendentes a través de ramas independientes.</p>
</td>
</tr>
</tbody>
</table>

* **Canal LINE para campañas orquestadas**: LINE ya está disponible como canal de salida nativo en campañas orquestadas, junto con el correo electrónico, SMS y la notificación push. Puede crear y enviar mensajes de LINE directamente desde el lienzo de la campaña, incluyendo texto, pegatinas, imágenes, vídeos, datos de ubicación y mensajes Flex, lo que admite casos de uso de promocionales, transaccionales y de participación continua en mercados en los que predomina LINE como Japón y la región de Asia-Pacífico. Esta funcionalidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible de forma general.

* **Monitorización de la orquestación de campañas**: ya está disponible una nueva interfaz de usuario para realizar el seguimiento del estado de ingesta y la actualización de los datos del almacén relacional utilizados en la segmentación de campañas orquestadas. Le ofrece una visibilidad directa del estado de los datos que alimentan a los públicos por lotes. Una nueva pestaña denominada Orquestación de campañas en el panel de control Monitorización de Adobe Experience Platform muestra el estado de los flujos de datos del almacén relacional (registros ingeridos/actualizados/eliminados/fallidos/omitidos), con gráficos desglosados y un desglose por flujo de datos/conjunto de datos que incluye el linaje.

* **Nuevas API de monitorización de campañas orquestadas**: ya están disponibles las nuevas **especificaciones de la API** para las campañas orquestadas, lo que permite crear, administrar y activar campañas orquestadas mediante programación, facilitando así una integración más profunda con sistemas externos y canalizaciones de automatización.

+++

### Canal de correo electrónico {#sep-26-email-channel}

Las siguientes funcionalidades y mejoras están llegando al canal de correo electrónico en esta versión.

+++ Próximamente — **La siguiente información está sujeta a cambios.**

<table>
<thead>
<tr>
<th><strong>Anular ajustes de configuración de canal de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Al crear los recorridos y las campañas, ahora puede anular los parámetros de correo electrónico derivados de la configuración de canal seleccionada directamente a nivel de acción del recorrido o de la campaña.</p>
<p>Esto le permite personalizar los campos de encabezado del correo electrónico (<strong>Nombre del remitente</strong>, <strong>Prefijo desde correo electrónico</strong>, <strong>Responder al nombre</strong> y <strong>Responder a correo electrónico</strong>), la dirección de ejecución y los valores de cancelación de suscripción a una lista, mediante atributos de perfil o datos contextuales para un control más preciso. Esto permite que los detalles del remitente reflejen el asesor, la ubicación o la sucursal relevantes para cada destinatario, en lugar de enrutar todos los envíos a través de una sola dirección corporativa.</p>
</td>
</tr>
</tbody>
</table>

* **Anulación de la lista de supresión en el nivel de acción de correo electrónico**: Journey Optimizer ahora le permite anular el comportamiento de la lista de supresión directamente en el nivel de acción de correo electrónico en recorridos y campañas. Esto proporciona a los equipos más flexibilidad para las comunicaciones operativas o críticas para el cumplimiento que requieren una configuración de envío dedicada, al tiempo que conserva los controles de lista de supresión global existentes para todos los demás envíos. Esta mejora ayuda a las organizaciones a gestionar escenarios de excepción con precisión sin cambiar su modelo de gobernanza de supresión más amplio.

+++

### Diseñador de correo electrónico {#sep-26-email-designer}

En esta versión se incorporarán las siguientes funcionalidades y mejoras al diseñador de correo electrónico.

<table>
<thead>
<tr>
<th><strong>Colaboración en el contenido del correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Designer de correo electrónico ahora incluye <strong>herramientas de colaboración</strong> integradas para realizar comentarios y resolver problemas, de modo que los equipos de marketing puedan revisar, discutir y finalizar el contenido del correo electrónico directamente desde Journey Optimizer, en lugar de compartir borradores con herramientas externas como chat, hilos de correo electrónico u hojas de cálculo. Invite a colaboradores y revisores, añada comentarios generales o específicos de componentes, y responda, resuelva y administre hilos de comentarios, todo sin salir de Designer de correo electrónico.</p>
<p>Para obtener más información, consulte la <a href="../email/email-collaboration.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 25 de septiembre de 2024.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuevo componente Tabla</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Diseñador de correo electrónico ahora incluye un <strong>componente Tabla</strong> integrado, que le permite estructurar el contenido en filas y columnas directamente dentro del correo electrónico. Arrastre y suelte el componente en el lienzo, personalice el número de filas y columnas y aplique estilo a cada celda de forma independiente para crear diseños claros y organizados sin necesidad de recurrir a código HTML personalizado.</p>
<p><img src="assets/do-not-localize/table-component.gif"></p>
<p>Para obtener más información, consulte la <a href="../email/content-components.md#table">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 24 de septiembre de 2024.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Compatibilidad con el modo oscuro para variantes de temas de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las temáticas de correo electrónico ahora son compatibles con el modo oscuro, por lo que cada variante de color se puede representar con un aspecto adaptado a los destinatarios que visualicen el correo electrónico en un cliente habilitado para el modo oscuro.</p>
<p>Cuando está habilitada, se genera automáticamente una paleta oscura predeterminada para cada variante y puede personalizarla aun más con una paleta diferente o con sus propios colores personalizados, independientemente del diseño del modo claro, de modo que los cambios realizados en un modo no afectan al otro.</p>
<p><img src="../email/assets/theme-dark-mode-support.gif"></p>
<p>Para obtener más información, consulte la <a href="../email/apply-email-themes.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 24 de septiembre de 2024.</p>
</td>
</tr>
</tbody>
</table>

+++ Próximamente — **La siguiente información está sujeta a cambios.**

<table>
<thead>
<tr>
<th><strong>Importación de plantillas de Dynamic Media directamente desde archivos de PSD al Diseñador de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El componente Dynamic Media del Diseñador de correo electrónico ahora le permite importar un archivo de Photoshop (PSD) directamente como una plantilla nueva, además de examinar las plantillas de Dynamic Media existentes. Arrastre y suelte un archivo de PSD en el componente y Adobe Journey Optimizer lo convertirá automáticamente en una plantilla de Dynamic Media, sin necesidad de realizar conversiones manuales ni viajes de ida y vuelta a través de Adobe Experience Manager. Una vez importada, edite la plantilla con el editor integrado de Dynamic Media.</p>
</td>
</tr>
</tbody>
</table>

+++

### Incorporación {#sep-26-onboarding}

La siguiente mejora se incorpora en esta versión.

<table>
<thead>
<tr>
<th><strong>Funciones guiadas para incorporar correos electrónicos y recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las funciones guiadas para incorporar correos electrónicos y recorridos ahora incluyen las siguientes mejoras:</p>
<ul>
<li>Al migrar un correo electrónico, [!DNL Journey Optimizer] identifica los bloques de contenido a los que hace referencia ese correo electrónico y los presenta como elementos de acción, de modo que puede migrar los bloques de contenido a lo largo del correo electrónico.</li>
<li>La interfaz se ha mejorado para que la incorporación guiada sea más intuitiva.</li></ul>
<p>Para obtener más información, consulte la <a href="../start/onboarding-hub.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 23 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

+++ Próximamente — **La siguiente información está sujeta a cambios.**

<table>
<thead>
<tr>
<th><strong>Funciones guiadas para incorporar correos electrónicos y recorridos (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La transición a Adobe Journey Optimizer desde otra plataforma de marketing resulta más fácil gracias a las funcionalidades guiadas que le ayudan a trasladar el contenido y los recorridos de correo electrónico existentes a Journey Optimizer. Un <strong>espacio de trabajo dedicado</strong> le permite reutilizar lo que tiene en lugar de reconstruirlo desde cero.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

+++

### Creación de informes {#sep-26-reporting}

En esta versión se incorporará la siguiente funcionalidad a la creación de informes.

<table>
<thead>
<tr>
<th><strong>Nuevos gráficos de monitorización de entrada en la administración de datos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede monitorizar el estado de los datos de entrada directamente desde <strong>Administración de datos &gt; Monitorización &gt; Edge</strong>, con seis nuevos gráficos que cubren los eventos de rendimiento, latencia y propuesta:</p>
<ul>
<li><strong>Rendimiento de entrada de AJO</strong>: rendimiento de entrada general (registros por segundo) a lo largo del tiempo.</li>
<li><strong>Desglose del rendimiento de entrada de AJO</strong>: rendimiento de entrada desglosado por ubicación.</li>
<li><strong>Latencia de entrada de AJO</strong>: latencia de la solicitud de entrada (en milisegundos), desglosada por distribución de valores (P50, P90 y mucho más).</li>
<li><strong>Rendimiento de los eventos de propuesta de entrada de AJO</strong>: rendimiento de los eventos de propuesta (señales de seguimiento generadas cuando un usuario interactúa con, visualiza o activa ofertas personalizadas) a lo largo del tiempo.</li>
<li><strong>Rendimiento de los eventos de propuesta de entrada de AJO por canal</strong>: rendimiento de los eventos de propuesta desglosado por canal de entrada (CBE, en la aplicación, tarjetas de contenido).</li>
<li><strong>Rendimiento global de los eventos de propuesta de entrada de AJO por tipo de evento</strong>: rendimiento de los eventos de propuesta desglosado por tipo de evento (descartado, suprimido, mostrado, activado, interactuado, enviado).</li>
</ul>
<p>Para obtener más información, consulte la <a href="../data/monitoring.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 24 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

### Integraciones {#sep-26-integrations}

Las siguientes funcionalidades están llegando a las integraciones en esta versión.

+++ Próximamente — **La siguiente información está sujeta a cambios.**


* **Sustitución dinámica de tokens para fragmentos de Experience Manager**. Las referencias a fragmentos de contenido de Experience Manager ahora admiten un atributo **tokenSubstitution**. Cuando se establece en `false`, la personalización dentro de los campos del fragmento se resuelve directamente, sin un mapa de token en la referencia. El valor predeterminado es `true`, lo cual mantiene el comportamiento existente.

  Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

* **Compatibilidad con fragmentos de contenido de AEM Managed Services en Decisioning**: los fragmentos de contenido de AEM Managed Services ahora se admiten en Decisioning al administrar elementos de decisión.


+++

### Personalización {#sep-26-personalization}

* **Corregir sintaxis con IA**: al validar una expresión, si se detecta un error de sintaxis de PQL, el editor de Personalization proporciona una opción &quot;Corregir con IA&quot; para ayudar a resolver el problema directamente desde el editor. [Más información](../personalization/personalization-build-expressions.md#validation-mechanisms).

  Fecha de disponibilidad: 22 de septiembre de 2026

### Toma de decisiones {#sep-26-decisioning}

En esta versión se incluyen las siguientes funcionalidades y mejoras para la toma de decisiones.

<table>
<thead>
<tr>
<th><strong>Compatibilidad con la toma de decisiones en el canal web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>La toma de decisiones ya está disponible para el canal web. Puede utilizar las directivas de decisión directamente en el editor visual web para enviar las ofertas más relevantes a cada visitante.</p>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/use-decision-policy.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 22 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Explicador de decisión en Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nueva habilidad de <strong>Explicador de decisiones</strong> en CX Coworker le permite preguntar, en lenguaje natural, por qué se mostró o no una oferta específica a un perfil o segmento, rastreando la elegibilidad, el límite, la clasificación y el grupo de candidatos involucrados en la decisión.</p>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/experience-decisioning-coworker-skills.md#decisioning-explainer">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 16 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Reglas y clasificación en Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nueva habilidad de <strong>Reglas y clasificación</strong> en CX Coworker le permite crear, explicar, simular y optimizar reglas de elegibilidad y fórmulas de clasificación usando lenguaje natural, sin necesidad de escribir o validar manualmente sintaxis de PQL.</p>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/experience-decisioning-coworker-skills.md#rules-ranking">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 16 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Los fragmentos de contenido de AEM en Decisioning estaban disponibles para los clientes de Managed Services**. Anteriormente, los fragmentos de contenido de AEM en Decisioning solo estaban disponibles para los clientes que usaban la integración con **Adobe Experience Manager as a Cloud Service**. Esta funcionalidad ahora también está disponible para los clientes que usan **Adobe Experience Manager Managed Services**. [Más información](../experience-decisioning/items.md#attributes)

  Fecha de disponibilidad: 23 de septiembre de 2026

* **Compatibilidad con los perfiles de Adobe Experience Platform en la simulación de reglas y fórmulas de clasificación**: al simular una regla o una fórmula de clasificación, ahora puede seleccionar un perfil de Adobe Experience Platform para rellenar automáticamente los atributos de una variante de datos de prueba en lugar de introducirlos manualmente. [Más información](../experience-decisioning/ranking/ranking-formulas.md#simulate-ranking-formula)

  Fecha de disponibilidad: 22 de septiembre de 2026

### Públicos {#sep-26-audiences}

El siguiente recordatorio se dirige a los públicos de esta versión.

* **Próximo cambio en los públicos de enriquecimiento de composición de público**: durante la versión de octubre (finales de octubre), Journey Optimizer detendrá los recorridos y las campañas que utilicen o hagan referencia a un público de composición de público cuyo conjunto de datos de origen no tenga un **descriptor de identidad principal**. A partir de ese momento, solo se admitirán los públicos de composición de público creados con un descriptor de identidad principal en los recorridos y las campañas. Si necesita que estos recorridos o campañas permanezcan activos, póngase en contacto con su representante de Adobe para que nuestro equipo de productos le ayude a migrar. <!-- Documentation link: TBD -->

### Administración {#sep-26-administration}

El siguiente recordatorio hace referencia a la administración en esta versión.

* **Mecanismo de protección del tiempo de vida (TTL) de los conjuntos de datos: zonas protegidas existentes**: el mecanismo de protección de tiempo de vida (TTL) para los conjuntos de datos generados por el sistema de Journey Optimizer (noventa días en el almacén de perfiles, trece meses en el lago de datos) se aplicará a las zonas protegidas y organizaciones de clientes existentes a partir del 1 de octubre de 2026.

### Mejoras de uso {#sep-26-usability}

* **Separación y unión más sencillas de las ramas en el nuevo lienzo del recorrido**: ahora puede separar una rama del resto del recorrido sin eliminarla y volverla a unir más tarde en un punto diferente, ya sea seleccionando una actividad idónea directamente en el lienzo o eligiéndola entre una lista de ramas desconectadas o ya utilizadas. [Más información](../building-journeys/using-the-journey-designer.md#join-and-detach-branches)

  Fecha de disponibilidad: 1 de septiembre de 2026

+++ Próximamente — **La siguiente información está sujeta a cambios.**

* **Mejoras de uso en la experiencia de simulación de contenido**: la nueva experiencia de simulación de contenido ahora le permite nombrar y organizar sus variantes para facilitar la comparación, copiar o eliminar detalles de la variante directamente desde cada tarjeta, ver rutas de atributos completas y la configuración de canal por tarjeta bajo demanda, así como cargar sus propios perfiles CSV, JSON o JSONL desde un botón de carga más prominente.

* **Calendario unificado para campañas, recorridos y campañas organizadas**: la vista de calendario para recorridos y campañas ahora pasa de aparecer en inventarios separados a estar en un menú unificado, accesible desde el carril izquierdo, que muestra a los dos elementos en una vista combinada.

+++
