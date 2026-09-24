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
source-git-commit: d645b6528fa7a1ae5169f129613f9085672e2ebb
workflow-type: tm+mt
source-wordcount: '3954'
ht-degree: 13%
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

Esta versión incorpora varias características y habilidades nuevas y mejoradas de [Coworker](../start/ai-features.md#cx-coworker) que se enumeran aquí para mayor visibilidad. Cada una de ellas se detalla también en la sección pertinente que figura a continuación.

* [Complemento de contenido de canal CE](#sep-26-content-management): Un nuevo complemento que reúne las habilidades de HTML de copia de campaña, imagen y correo electrónico en Coworker, desde información de campaña hasta copia y HTML listas para la producción.
* [Herramientas MCP de administración de contenido](#sep-26-content-management): descubra y administre plantillas de contenido, fragmentos, páginas de aterrizaje y contenido de mensajes en línea mediante mensajes en lenguaje natural en Coworker.
* [Simulación de Recorrido](#sep-26-journeys): Automatice la validación de recorrido de extremo a extremo e interprete los resultados directamente en Compañero de trabajo.
* [Comparar versiones de un recorrido](#sep-26-journeys): obtenga una diferencia estructurada y de fidelidad total entre dos versiones cualquiera de un recorrido a través de Coworker Chat.
* [Analizar la habilidad de anomalías de Recorrido](#sep-26-journeys): detecta picos, caídas o líneas planas inesperados en los recuentos de entrada, salida o envío de mensajes de un recorrido, con diagnósticos de causa raíz.

+++ Próximamente — **La siguiente información está sujeta a cambios.**

* [Creación de Recorridos desde el carril de Coworker](#sep-26-journeys): genere recorridos con IA directamente desde el carril derecho de Coworker, reemplazando la experiencia anterior del asistente de IA.
* [Habilidad de recomendación de fidelización](#sep-26-loyalty): solicita oportunidades de desafío directamente en la interfaz conversacional de tu compañero y conviértelas en desafíos en vivo sin salir del chat.
* [Aptitud para el análisis de higiene](#sep-26-journeys): analice los recorridos activos y en borrador para detectar configuraciones dañadas, errores silenciosos y recursos en declive o no utilizados, con las correcciones recomendadas.
* [Habilidad con el análisis de rendimiento empresarial](#sep-26-journeys): analice el rendimiento del recorrido y obtenga recomendaciones de optimización concretas desde el chat.

+++

>[!ENDSHADEBOX]

### Administración de contenido {#sep-26-content-management}

La siguiente funcionalidad se incluye en la administración de contenido en esta versión.

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
<th><strong>Herramientas MCP de administración de contenido en CX Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Coworker ahora tiene un nuevo conjunto de <strong>herramientas MCP de administración de contenido</strong>, que le permiten descubrir y administrar recursos de contenido de Journey Optimizer a través de mensajes en lenguaje natural. Pídale que enumere o recupere plantillas de contenido, fragmentos, páginas de aterrizaje y contenido de mensajes en línea de recorrido/campaña. También puede crear contenido, actualizar plantillas y crear, actualizar, clonar y publicar fragmentos, además de actualizar el contenido de acciones del canal en línea directamente en recorrido y campaña.</p>
<p>Para obtener más información, consulte la <a href="../content-management/content-management-coworker-skills.md#content-management">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 3 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Casilla de verificación de consentimiento obligatoria para las páginas de aterrizaje**: ahora puede hacer que una casilla de verificación sea obligatoria en el componente de formulario de la página de aterrizaje, lo que requiere que los visitantes la seleccionen (por ejemplo, dar su consentimiento) antes de que puedan enviar el formulario. [Más información](../landing-pages/lp-content.md#use-form-component)

  Fecha de disponibilidad: 4 de septiembre de 2026

* **Palabras clave reservadas adicionales en la sintaxis de personalización**: la lista de palabras clave reservadas en Profile Query Language (PQL) se ha ampliado para incluir palabras clave generales, unidades de tiempo y operadores booleanos/lógicos. Si el esquema XDM contiene un nombre de campo que coincide con una de estas palabras clave, encapsúlelo en acentos graves para hacer referencia a él en una expresión personalizada. [Más información](../personalization/personalization-syntax.md#reserved-keywords)

  Fecha de disponibilidad: 1 de septiembre de 2026

### Lealtad {#sep-26-loyalty}

<table>
<thead>
<tr>
<th><strong>Actualizaciones de asignación de eventos de fidelización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La creación o edición de una asignación de eventos ahora utiliza un nuevo **generador de asignaciones visuales**: seleccione un esquema, elija campos de un selector de campos en el que se pueda buscar, asigne cada campo a un campo de evento de lealtad con estado de conexión por fila y previsualice la expresión JSONata generada automáticamente, con la opción de cambiar a la edición manual de JSONata en cualquier momento.</p><p>Además, se ha cambiado el nombre de "Definiciones de eventos" en la administración de Fidelidad a "Asignaciones de eventos", con una vista de lista actualizada que muestra el nombre del esquema de evento de Experience legible en lenguaje natural.</p>
<p>Para obtener más información, consulte la <a href="../loyalty-challenges/loyalty-admin.md#event-mappings">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 22 de septiembre de 2026</p>
</td>
</tr>
</tbody>
</table>

* **&quot;Desafíos de fidelidad para siempre&quot;**: los desafíos de fidelidad ahora pueden ejecutarse indefinidamente. Defina **El desafío finalizará** en **Sin fecha de finalización** al configurar la programación y el desafío nunca caducará. [Más información](../loyalty-challenges/create-challenges.md#schedule)

  Fecha de disponibilidad: 1 de septiembre de 2026

* **Lealtad disponible para los clientes de Healthcare Shield y Privacy and Security Shield**: Journey Optimizer Loyalty ya está disponible para los clientes de Healthcare Shield y Privacy and Security Shield. [Más información](../loyalty-challenges/get-started.md)

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

* Dominio de **retos en el editor de personalización de tarjetas de contenido**: el editor de personalización de tarjetas de contenido ahora admite **desafíos** como dominio, lo que le permite acceder a los metadatos de desafíos al crear la personalización de tarjetas de contenido. Esto facilita la creación de contenido personalizado para cada fase de un desafío (inicio, en curso y final) sin código personalizado.

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
<p>La <strong>aptitud de simulación de Recorrido</strong> en Coworker automatiza la validación de recorrido de extremo a extremo y le permite interpretar fácilmente los resultados. Tenga en cuenta que, en la actualidad, esta función solo admite el flujo de simulación rápida y no reemplaza completamente la experiencia de simulación manual de Journey Optimizer.</p>
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
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte <a href="releases.md">Ciclo de lanzamiento de Journey Optimizer</a>.</p>
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
<p>El editor de expresiones avanzadas de recorrido ahora integra la generación de expresiones con tecnología de IA: describa la expresión que desea crear en lenguaje natural y el editor genera código listo para usar que puede aplicar inmediatamente o refinar mediante mensajes de seguimiento.</p>
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

* **La toma de decisiones en la simulación de Recorrido** - Experimentación de rutas, como parte de la actividad **Optimizar**, ahora se admite en la simulación. Decisioning gestiona el enrutamiento, que es aleatorio y no determinista por usuario simulado.

  [Más información](../building-journeys/simulate-journey-gs.md)

  Fecha de disponibilidad: 15 de septiembre de 2026

* **Nueva alerta de anomalía de Recorrido detectada**: ahora una nueva alerta del sistema le avisa cuando el tráfico diario de un recorrido activo se desvía de su propia línea de base histórica o cae a cero inesperadamente en las entradas de Recorrido, salidas de Recorrido y envíos de eventos. Actualmente, esta alerta solo está disponible en zonas protegidas de producción.

  [Más información](../reports/alerts.md)

  Fecha de disponibilidad: 15 de septiembre de 2026

* **Toma de decisiones en la simulación de Recorrido**: ahora puede simular recorridos que dependen de la toma de decisiones, con los siguientes elementos recientemente admitidos:

  * Los nodos de decisión de contenido ahora son compatibles con la simulación.
  * El método de regla Targeting de la actividad Optimize ahora se admite en Simulación.
  * Ahora se admiten acciones con contenido decidido por Adobe Journey Optimizer (por ejemplo, correo electrónico con una directiva de decisión) en Simulación.
  * Las políticas de decisión que utilizan la idoneidad de la oferta y la clasificación por regla, audiencia, prioridad o fórmula son totalmente compatibles. Clasificación por modelo de IA: Personalization también es compatible, aunque las ofertas devueltas pueden variar entre ejecuciones.

  [Más información](../building-journeys/simulate-journey-gs.md)

  Fecha de disponibilidad: 8 de septiembre de 2026

* **Analizar anomalías de Recorrido**: CX Coworker ahora puede detectar picos, caídas o líneas planas inesperados en los recuentos de entrada, salida o envío de mensajes de un recorrido en las líneas de base históricas mediante la habilidad **Analizar anomalías de Recorrido**. Una vez confirmada una anomalía real, la aptitud ejecuta diagnósticos de solo lectura para detectar una causa raíz y una recomendación probables. [Más información](../building-journeys/journeys-coworker-skills.md#journey-analyze)

  Fecha de disponibilidad: 2 de septiembre de 2026

* **Nueva función dateDiff en el editor de expresiones de recorrido**. El editor de expresiones de recorrido ahora incluye la función `dateDiff`, que calcula la diferencia entre dos fechas en número de días. Esta función es útil para lógica basada en tiempo, como la creación de plazos, el cálculo de las duraciones del ciclo vital de los clientes o la creación de temporizadores de cuenta atrás en condiciones de recorrido.  [Más información](../building-journeys/functions/date-functions.md#dateDiff)

  Fecha de disponibilidad: 1 de septiembre de 2026

+++ Próximamente — **La siguiente información está sujeta a cambios.**

<table>
<thead>
<tr>
<th><strong>Tarjetas de recomendación de IA para alertas de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La página de inicio de Journey Optimizer ahora muestra una <strong>tarjeta de recomendaciones de IA</strong> cuando se activa una alerta de recorrido que cubre <strong>errores de acciones personalizadas de Recorrido</strong> y <strong>anomalías de Recorrido detectadas</strong>. Al seleccionar la tarjeta, se abre el recorrido con el carril derecho rellenado previamente con el análisis ya realizado.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actividad de recorrido de desactivación de actividad entrante</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nueva actividad <strong>Inbound Activity Deactivation</strong> en el lienzo de recorrido le permite quitar un perfil de hasta cinco actividades o experiencias entrantes directamente de un recorrido, lo que desvincula la descalificación entrante de la salida del recorrido para una orquestación entre canales más avanzada.</p>
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
<th><strong>Creación de recorridos desde el carril Compañero de trabajo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La creación de Recorridos de <strong>con IA</strong> ya está disponible directamente desde el carril derecho de la barra de tareas del asistente, reemplazando la experiencia anterior del asistente de IA con un punto de entrada integrado con marca modificada para la generación de recorridos.</p>
</td>
</tr>
</tbody>
</table>

* **Aptitud para el análisis de higiene**: CX Coworker ahora puede analizar los recorridos activos y en borrador para detectar configuraciones rotas, errores silenciosos y recursos en declive o no utilizados, como recorridos en borrador antiguos, fuentes de datos huérfanas y errores persistentes de acciones personalizadas, así como correcciones recomendadas superficiales directamente en el chat. <!-- Documentation link: TBD -->

* **Compatibilidad con ID suplementario en la simulación de Recorrido** - **La simulación de Recorrido admite ahora el ID suplementario**, lo que le permite probar escenarios de usuario complejos para recorridos activados por eventos y de audiencia de lectura.

* **Supresión de eventos de paso de ejecución en seco para informes personalizados**: como parte de la optimización de eventos de paso, Journey Optimizer ahora deja de generar ciertos eventos de paso que no se pueden notificar durante las ejecuciones en seco de Recorrido. Esto solo afecta a los informes personalizados creados en estos tipos de eventos de paso de ejecución en seco. Si se ve afectado, vuelva a almacenar en déclencheur la ejecución en seco para regenerar los datos.

* **Tiempo de espera de recuperación de evento automático en Propiedades de Recorrido** - Propiedades de Recorrido ahora incluye una configuración de **Establecer tiempo de espera de recuperación de evento**: de forma predeterminada, los eventos de recorrido afectados se reproducen automáticamente durante un máximo de 72 horas después de una interrupción del servicio sin necesidad de realizar ninguna acción. Puede activar esta configuración para controlar la ventana de reproducción (0-72 horas) para recorridos con distinción de tiempo. El campo **Tiempo de espera o error** existente también ha cambiado de nombre a **Acción personalizada / Tiempo de espera de la fuente de datos** para evitar confusiones entre las dos configuraciones.

+++

### Campañas {#sep-26-campaigns}

+++ Próximamente — **La siguiente información está sujeta a cambios.**

* **Carpetas para campañas de acción**: ahora puede organizar sus campañas de acción en carpetas para mejorar la navegación y la administración en la interfaz.

* **Anular los campos de ejecución predeterminados en las campañas de acción**. Anteriormente disponible en el nivel de recorrido, ahora puede anular los campos de ejecución predeterminados configurados globalmente para las entregas de correo electrónico, SMS y WhatsApp en los parámetros de la campaña de acción.

+++


### Canales {#sep-26-channels}

Las siguientes funcionalidades y mejoras están llegando a los canales en esta versión.

+++ Próximamente — **La siguiente información está sujeta a cambios.**

<table>
<thead>
<tr>
<th><strong>Actividades activas para actualizaciones de Android Live</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora amplía sus capacidades de personalización móvil en tiempo real al ampliar la compatibilidad con <strong>Actividad en directo a Android</strong>. Puede enviar actualizaciones de progreso en tiempo real directamente a los usuarios, como seguimiento de pedidos, estados de vuelos, actualizaciones de eventos en directo y puntuaciones deportivas en tiempo real.</p>
<p>Además de admitir las actividades de iOS Live, Journey Optimizer ahora administra tokens push temporales para las actualizaciones de Android Live en las configuraciones de plataforma. Admite flujos de actualización transaccionales y de difusión mediante campañas activadas por API y API sin encabezado.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Android notificaciones push plantillas mejoras</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las notificaciones push de Android se representaban anteriormente con un diseño único y fijo: las imágenes siempre se recortaban en el centro y el texto largo del cuerpo se truncaba. Esta versión incluye un selector de plantillas en el momento de la creación, lo que permite a los especialistas en marketing controlar el diseño de las notificaciones push de Android.</p>
<p>Las siguientes mejoras están disponibles:</p>
<ul>
<li><b>Selección de diseño</b>: Nuevo selector de diseño de notificaciones push (estándar/expandido) al crear una notificación push de Android.</li>
<li><b>Diseño estándar con "Mostrar toda la imagen"</b>: elija recortado para rellenar frente a escalado para ajustar.</li>
<li><b>Diseño ampliado</b>: texto independiente multilínea sin truncamiento, además de una miniatura de icono grande opcional.</li>
<li><b>Cuerpo contraído (diseño expandido)</b>: establezca un texto independiente más corto para el estado contraído.</li>
</ul>
</td>
</tr>
</tbody>
</table>

* **Flexibilidad de autenticación BYOP de SMS personalizado**: ahora puede configurar **encabezados de autenticación personalizados** al conectar la configuración de OAuth de su proveedor de SMS, incluso dónde se coloca el token en los mensajes salientes y cómo se da formato a la propia solicitud de token.

* **Correo directo - Dividir archivos grandes automáticamente** - Los archivos de correo directo ahora se pueden dividir en varias partes automáticamente cuando superan los 20 GB, o manualmente eligiendo un tamaño de archivo de destino en la configuración de enrutamiento de archivos.

* **Correo directo: límite de audiencia aumentado**: el límite de audiencia del canal de correo directo se ha aumentado de 3 millones a 100 millones de perfiles, lo que permite dirigirse a audiencias mucho más grandes sin llegar a errores de creación de archivos.

+++

### Campañas orquestadas {#sep-26-orchestrated-campaigns}

<table>
<thead>
<tr>
<th><strong>Alerta para campañas orquestadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las campañas orquestadas ahora admiten <strong>alertas automatizadas</strong> a través del mismo marco de alertas utilizado en los recorridos y las campañas. Las alertas se activan cuando falla la ejecución de una campaña, agota el tiempo de espera y cada alerta incluye lo que ha sucedido, cuándo, dónde y un vínculo directo al lienzo para comprobar más detalles en los registros.</p>
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
<th><strong>O unirse a la actividad para campañas orquestadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La <strong>actividad de unión</strong> en las campañas orquestadas ahora admite las condiciones de unión AND y OR. Con la lógica OR, un perfil que completa cualquier rama ascendente, en lugar de todas, continúa a lo largo de una sola ruta descendente compartida. Esto permite modelar patrones "si A, B o C, entonces hágalo" directamente en el lienzo sin duplicar los pasos descendentes a través de ramas independientes.</p>
</td>
</tr>
</tbody>
</table>

* **Canal LINE para campañas orquestadas**: LINE ya está disponible como canal saliente nativo en campañas orquestadas, junto con correo electrónico, SMS y push. Puede crear y enviar mensajes de LINE directamente desde el lienzo de la campaña, incluidos texto, pegatinas, imágenes, vídeos, datos de ubicación y mensajes de Flex, lo que admite casos de uso de participación promocional, transaccional y continua en mercados dominantes de LINE como Japón y APAC. Esta capacidad, que se publicó anteriormente con disponibilidad limitada, ya está disponible de forma general.

* **Supervisión de Campaign Orchestration**: ya está disponible una nueva interfaz de usuario para realizar el seguimiento del estado de ingesta y la actualización de los datos del almacén relacional que usa la segmentación de Campaign orquestada. Le ofrece una visibilidad directa del estado de los datos que alimentan a las audiencias por lotes. Una nueva pestaña de Campaign Orchestration del panel de monitorización de Adobe Experience Platform muestra el estado de los flujos de datos del almacén relacional (registros ingeridos/actualizados/eliminados/fallidos/omitidos), con gráficos desglosados y un desglose por flujo de datos/conjunto de datos, incluido el linaje.

* **Nuevas API de supervisión de campañas orquestadas**: las nuevas **especificaciones de la API** ya están disponibles para las campañas orquestadas, lo que le permite crear, administrar y almacenar en déclencheur mediante programación campañas orquestadas, lo que permite una integración más profunda con sistemas externos y canalizaciones de automatización.

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

### Creación de informes {#sep-26-reporting}

La siguiente funcionalidad se incluye en los informes en esta versión.

+++ Próximamente — **La siguiente información está sujeta a cambios.**

<table>
<thead>
<tr>
<th><strong>Nuevos gráficos de monitorización de entrada en Data Management</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede supervisar el estado de los datos de entrada directamente desde <strong>Administración de datos &gt; Supervisión &gt; Edge</strong>, con seis nuevos gráficos que cubren los eventos de rendimiento, latencia y propuesta:</p>
<ul>
<li><strong>Rendimiento entrante de AJO</strong>: rendimiento entrante general (registros por segundo) a lo largo del tiempo.</li>
<li><strong>Desglose de rendimiento de entrada de AJO</strong>: rendimiento de entrada desglosado por ubicación.</li>
<li><strong>Latencia entrante de AJO</strong>: latencia de solicitud entrante (en milisegundos), desglosada por distribución de valores (P50, P90 y más).</li>
<li><strong>Rendimiento de eventos de propuesta de entrada de AJO</strong>: rendimiento de eventos de propuesta (señales de seguimiento generadas cuando un usuario interactúa con ofertas personalizadas, vistas o déclencheur) a lo largo del tiempo.</li>
<li><strong>Rendimiento de eventos de propuesta de entrada de AJO por canal</strong>: rendimiento de eventos de propuesta desglosado por canal de entrada (CBE, en la aplicación, tarjetas de contenido).</li>
<li><strong>Rendimiento global de eventos de propuesta de entrada de AJO por tipo de evento</strong>: rendimiento de eventos de propuesta desglosado por tipo de evento (descartado, suprimido, mostrado, activado, interactuado, enviado).</li>
</ul>
</td>
</tr>
</tbody>
</table>

+++

### Integraciones {#sep-26-integrations}

Las siguientes funcionalidades están llegando a las integraciones en esta versión.

+++ Próximamente — **La siguiente información está sujeta a cambios.**


* **Sustitución dinámica de tokens para fragmentos de Experience Manager**. Las referencias a fragmentos de contenido de Experience Manager ahora admiten un atributo **tokenSubstitution**. Cuando se establece en `false`, la personalización dentro de los campos del fragmento se resuelve directamente, sin un mapa de token en la referencia. El valor predeterminado es `true`, lo cual mantiene el comportamiento existente.

  Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

* **Compatibilidad con fragmentos de contenido de AEM Managed Services en Decisioning**: los fragmentos de contenido de AEM Managed Services ahora se admiten en Decisioning al administrar elementos de decisión.


+++

### Personalización {#sep-26-personalization}

* **Corregir sintaxis con IA**: cuando se detecta un error de validación de sintaxis de PQL, el Editor de Personalization ahora proporciona una opción &quot;Corregir con IA&quot; para ayudar a resolver el problema directamente desde el editor.

  Fecha de disponibilidad: 22 de septiembre de 2026

### Toma de decisiones {#sep-26-decisioning}

En esta versión se incluyen las siguientes funcionalidades y mejoras para la toma de decisiones.

<table>
<thead>
<tr>
<th><strong>Compatibilidad con decisiones en el canal Web</strong><br/></th>
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

* **Los fragmentos de contenido de AEM en Decisioning estaban disponibles para los clientes de Managed Services**. Anteriormente, los fragmentos de contenido de AEM en Decisioning solo estaban disponibles para los clientes que usaban la integración con **Adobe Experience Manager as a Cloud Service**. Esta funcionalidad ahora también está disponible para los clientes que usan **Adobe Experience Manager Managed Services**. [Más información](../experience-decisioning/items.md#attributes)

  Fecha de disponibilidad: 23 de septiembre de 2026

* **Compatibilidad con perfiles Adobe Experience Platform en la simulación de reglas y fórmulas de clasificación**: al simular una regla o una fórmula de clasificación, ahora puede seleccionar un perfil Adobe Experience Platform para rellenar automáticamente los atributos de una variante de datos de prueba en lugar de introducirlos manualmente. [Más información](../experience-decisioning/ranking/ranking-formulas.md#simulate-ranking-formula)

  Fecha de disponibilidad: 22 de septiembre de 2026

### Públicos {#sep-26-audiences}

El siguiente recordatorio se aplica a las audiencias de esta versión.

* **Próximo cambio en las audiencias de enriquecimiento de Audience Composition**: durante la versión de octubre (finales de octubre), Journey Optimizer detendrá los recorridos y campañas que usen o hagan referencia a una audiencia de Audience Composition cuyo conjunto de datos de origen no tenga un **descriptor de identidad principal**. A partir de ese momento, solo se admitirán en recorridos y campañas las audiencias de Composición de audiencia creadas con un descriptor de identidad principal. Si necesita que estos recorridos o campañas permanezcan activos, póngase en contacto con su representante de Adobe para que nuestro equipo de productos le ayude a migrar. <!-- Documentation link: TBD -->

### Administración {#sep-26-administration}

El siguiente recordatorio se aplica a la administración de en esta versión.

* **Protección de tiempo de vida de conjunto de datos (TTL) — zonas protegidas existentes** - La protección de tiempo de vida (TTL) para conjuntos de datos generados por el sistema de Journey Optimizer (90 días en el almacén de perfiles, 13 meses en el lago de datos) se aplicará en las zonas protegidas de clientes y organizaciones existentes a partir del 1 de octubre de 2026.

### Mejoras de uso {#sep-26-usability}

* **Información general de IA en alertas de validación de fragmentos**: el cuadro de diálogo de alertas de validación de fragmentos ahora incluye una descripción general de IA que resume y explica los problemas de validación (por ejemplo, expresiones mal formadas, campos de perfil que faltan y JSON no válido) para que los usuarios puedan solucionar problemas más rápido.

  Fecha de disponibilidad: 22 de septiembre de 2026

* **Más fácil desasociar y unir ramas en el nuevo lienzo de recorrido**: ahora puede desasociar una rama del resto del recorrido sin eliminarla y volver a unirla más tarde en un punto diferente, ya sea seleccionando una actividad elegible directamente en el lienzo o seleccionándola de una lista de ramas desconectadas o ya utilizadas. [Más información](../building-journeys/using-the-journey-designer.md#join-and-detach-branches)

  Fecha de disponibilidad: 1 de septiembre de 2026

+++ Próximamente — **La siguiente información está sujeta a cambios.**

* **Mejoras de uso en la experiencia de simulación de contenido**: la nueva experiencia de simulación de contenido ahora le permite nombrar y organizar sus variantes para facilitar la comparación, copiar o eliminar detalles de la variante directamente desde cada tarjeta, ver rutas de atributos completas y la configuración de canal por tarjeta bajo demanda, y cargar sus propios perfiles CSV, JSON o JSONL desde un botón de carga más prominente.

+++
