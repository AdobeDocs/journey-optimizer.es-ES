---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b53c28405e453be3767f05e2c7a7a1b2e69d0416
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 29%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] sigue un modelo de envío continuo, lo que permite a Adobe ofrecer nuevas funciones, mejoras y correcciones de forma continua. Este enfoque permite un despliegue escalable y gradual de las funciones para garantizar el rendimiento y la estabilidad en todos los entornos.

Debido a este modelo, las notas de la versión se actualizan entre versiones mensuales. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Notas de la versión de febrero de 2026 {#feb-26-01-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican en las notas de la versión en la fecha de lanzamiento.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de lanzamiento**: 17-18 de febrero de 2026

### Nuevas funciones {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>Envío de ondas de mensajes salientes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Puede programar mensajes salientes de <strong>campañas</strong> o <strong>recorridos</strong> para que se entreguen en <strong>lotes</strong> controlados a lo largo del tiempo.</p>
<p>El envío de ondas ofrece las siguientes ventajas:</p>
<ul>
<li>Mejor <strong>capacidad de entrega</strong>: la propagación envía con el tiempo para ayudar a mantener una sólida <strong>reputación de remitente</strong> y reducir el riesgo de ser marcado como correo no deseado.</li>
<li><strong>Control de carga</strong>: evita sistemas descendentes abrumadores (por ejemplo, centros de llamadas o páginas de aterrizaje) al limitar la cantidad de mensajes que se emiten a la vez.</li>
<li>Casos de uso de gran volumen y sensibles al tiempo: adecuados para audiencias grandes o cuando necesite controlar el tiempo (por ejemplo, capacidad del centro de llamadas, ampliación u ofertas con límite de tiempo).</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>arbitraje de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede usar <strong>fórmulas</strong> y <strong>modelos de IA</strong> para aumentar automáticamente <strong>las puntuaciones de recorrido</strong> según los atributos del perfil del cliente y los factores contextuales, asegurándose de que los clientes ingresen los recorridos más relevantes.</p>
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (<strong>Disponibilidad limitada</strong>). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: Creación de contenido de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con tecnología de <strong>Adobe Experience Platform Agent Orchestrator</strong>, <strong>Journey Agent</strong> está disponible en Journey Optimizer y le permite analizar recorridos a través de una <strong>interfaz de lenguaje natural</strong>. Ahora también puede generar y administrar contenido específico del canal directamente en Journey Agent, creando contenido para canales como correo electrónico y push, aplicando y previsualizando plantillas, refinando el tono y el estilo mediante mensajes y abriendo contenido en <strong>Content Designer</strong> para la edición en contexto.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actividades de Mobile Live</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Actividades en vivo</strong> proporciona <strong>actualizaciones en tiempo real</strong> y experiencias interactivas dentro de las aplicaciones móviles, lo que permite a los usuarios mantenerse informados sobre eventos o tareas en curso directamente en la pantalla de su dispositivo. Esta función mejora la participación al ofrecer información en directo, como el seguimiento del progreso, las actualizaciones de eventos o el contenido interactivo, sin que sea necesario que los usuarios abran la aplicación.</p>
<p>Esta funcionalidad, que ya se publicó en la versión beta, ya está disponible para todos los entornos (<strong>Disponibilidad general</strong>).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actividad de acción en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer admite una nueva actividad <strong>Action</strong> genérica que permite configurar acciones únicas y <strong>grupos de acciones entrantes de varias acciones</strong>, lo que permite una configuración de acciones optimizada dentro del <strong>lienzo de recorrido</strong>. En particular, esta nueva función permite lo siguiente:</p>
<ul>
<li>Una configuración de acción nativa simplificada dentro del lienzo de recorrido.</li>
<li>La capacidad para crear grupos de acciones entrantes de varias acciones.</li>
<li>La capacidad de agregar <strong>optimización</strong> a cualquier acción de canal integrada.</li>
<li>Posibilidad de agregar las opciones <strong>experimentación</strong> y <strong>multilingüe</strong> a cualquier acción.</li>
</ul>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de notificaciones push web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ahora admite <strong>notificaciones push web</strong>, lo que expande el canal push más allá del dispositivo móvil. Puede enviar notificaciones perfectamente a exploradores móviles y de escritorio, lo que permite llegar a los clientes directamente en sus dispositivos sin necesidad de una aplicación. Esta mejora le permite atraer a usuarios con mensajes personalizados y oportunos en tiempo real, aprovechando los mismos <strong>flujos de trabajo de creación</strong> y las <strong>funcionalidades de segmentación</strong> ya disponibles para notificaciones push móviles.</p>
<p>Esta funcionalidad, que ya se publicó en la versión beta, ya está disponible para todos los entornos (<strong>Disponibilidad general</strong>).</p>
<p>Fecha de disponibilidad: sábado, 13 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actividad de decisión de contenido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una nueva actividad <strong>Content decision activity</strong> en el <strong>lienzo de recorrido</strong> para integrar <strong>ofertas personalizadas</strong> directamente en las recorridos de cliente. Esta actividad le permite entregar contenido basado en decisiones y hacer referencia a esas ofertas en todo el recorrido: en condiciones para crear ramas basadas en la idoneidad, en acciones personalizadas para pasar datos de ofertas a sistemas externos y en otras actividades para crear experiencias de cliente totalmente personalizadas.</p>
<p>Publicada anteriormente en Disponibilidad limitada, esta funcionalidad ya está disponible para todos los entornos (<strong>Disponibilidad general</strong>).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/content-decision.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: jueves, 11 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API de herramientas de migración de autoservicio</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las <strong>API de herramientas de migración</strong> ya están disponibles para migrar mediante programación las entidades de <strong>Administración de decisiones</strong> a <strong>Toma de decisiones</strong>, que incluyen:</p>
<ul>
<li>Ámbitos de migración flexibles (<strong>espacio aislado</strong>, <strong>oferta</strong> o nivel de <strong>decisión</strong>)</li>
<li>Validación y análisis de dependencia <strong>automatizados</strong></li>
<li><strong>Soporte de reversión</strong> para migraciones completadas</li>
<li>Informes de migración detallados con asignaciones de objetos</li>
</ul>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/decisioning-migration-api.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 3 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitorización de acciones personalizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Obtenga información más detallada de insight sobre el estado y el rendimiento de sus <strong>extremos de acción personalizados</strong> con un nuevo <strong>tablero de supervisión</strong> y <strong>datos de evento de paso de recorrido</strong> enriquecidos. Rastree las llamadas, los errores, el rendimiento, los tiempos de respuesta y los tiempos de espera de cola correctos para comprender rápidamente cuándo, dónde y por qué se producen anomalías.</p>
<p>Publicada anteriormente en Disponibilidad limitada, esta funcionalidad ya está disponible para todos los entornos (<strong>Disponibilidad general</strong>).</p>
<p>Para obtener más información, consulte la <a href="../action/reporting.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 3 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Compatibilidad con decisiones en el canal SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede personalizar y optimizar el contenido de sus <strong>mensajes SMS</strong> con <strong>Decisioning</strong>. Use <strong>Puntuaciones de prioridad</strong>, <strong>Fórmulas</strong> o <strong>Modelos de IA</strong> para mostrar el mejor contenido a sus clientes.</p>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/create-decision.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 2 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#feb-26-01-improv}

A continuación, se describen las mejoras incluidas en esta versión.

#### Configuración

* **Uso de eventos de experiencia en expresiones de recorrido**: a partir del 1 de abril de 2026, el uso de atributos de eventos de experiencia en expresiones de recorrido dejará de ser compatible con las organizaciones que no hayan utilizado esta capacidad en los últimos 90 días. Esta capacidad ya no está disponible para las nuevas organizaciones de clientes desde el 8 de julio de 2025. Para ver alternativas, consulte [Búsqueda de eventos de experiencia en recorrido](../building-journeys/exp-event-lookup.md).


* **Cambio del método de delegación de subdominios** - Ahora puede cambiar de un método de <strong>delegación de subdominios</strong> a otro. Esto le permite migrar dominios utilizando el modo <strong>CNAME delegation</strong> al método <strong>custom delegation</strong> para adherirse a las políticas de seguridad de su compañía.

  **Nota**: Esta funcionalidad solo está disponible para un conjunto de organizaciones (<strong>Disponibilidad limitada</strong>). Para obtener acceso, póngase en contacto con su representante de Adobe.


#### Diseñador de correo electrónico

* **Use un tema de marca para convertir una imagen en una plantilla de correo electrónico**: al convertir una imagen en una plantilla de correo electrónico en Journey Optimizer, ahora puede usar un <strong>tema</strong> como entrada para que el HTML generado siga sus <strong>parámetros de marca</strong>. El estilo, como el color de fondo, el color del botón, las fuentes, el interlineado, los márgenes y el relleno, se aplica automáticamente, lo que reduce el trabajo de diseño manual y proporciona una plantilla lista para usar con ediciones mínimas.


* **Actualice las marcas con una nueva ficha de color** - las <strong>Directrices de marca</strong> le ayudarán a garantizar que su marca se presente de manera consistente en todos los puntos de contacto. La nueva <strong>sección Colores</strong> define los estándares para el sistema de colores de su marca y describe cómo se seleccionan, organizan y aplican los colores en todas las experiencias. Garantiza el uso consistente de los colores primarios, secundarios, acentuados y neutros para apoyar una identidad de marca coherente, accesible y reconocible.


#### IA

* **Integración de modelos Firefly personalizados y modelos de generación de imágenes de terceros**: habilita la integración perfecta de <strong>modelos Firefly estándar y personalizados</strong>, junto con <strong>modelos de imágenes de terceros</strong> aprobados (por ejemplo, NanoBanana), para proporcionar mayor flexibilidad, control y alineación de marca al generar imágenes. Esto le permite seleccionar el mejor modelo para cada caso de uso: Firefly estándar para necesidades generales, Firefly personalizado para la generación sin marca o modelos de terceros aprobados para escenarios especializados o experimentales.


#### Decisiones sobre experiencias

* **Compatibilidad de entrada de Edge con el uso de datos de Adobe Experience Platform en Decisioning**: la compatibilidad de decisioning con <strong>Experience Platform data lookup</strong> ahora incluye <strong>casos de uso de canales de entrada Edge</strong>. La funcionalidad permanece en Disponibilidad limitada; aún no se anuncia la disponibilidad general de la función de búsqueda de datos subyacente (dependencia de AEP/producto).

  **Nota**: Esta funcionalidad solo está disponible para un conjunto de organizaciones (<strong>Disponibilidad limitada</strong>). Para obtener acceso, póngase en contacto con su representante de Adobe.


* **Vista previa de Experience Decisioning en el canal de experiencia basado en código**: ahora puede obtener una vista previa de <strong>elementos de decisión</strong> al configurar <strong>Experience Decisioning</strong> con el canal <strong>Experiencia basada en código</strong>. La vista previa está disponible directamente en la interfaz de creación antes de lanzarse.


* **Observabilidad del modelo de IA de clasificación de ofertas**: Journey Optimizer ahora le permite supervisar el <strong>estado de la formación</strong>, el <strong>estado de la formación</strong> y el <strong>rendimiento</strong> de sus <strong>modelos de IA</strong> en la toma de decisiones, para que pueda comprobar el éxito de la formación, solucionar errores y comprender el impacto en sus resultados. Esta capacidad solo está disponible para modelos de optimización personalizados (no para la optimización automática).


* **Adjuntar fragmentos a elementos de decisión**: Journey Optimizer ahora permite adjuntar <strong>fragmentos</strong> a <strong>elementos de decisión</strong> que se pueden aprovechar en campañas de experiencia basadas en código mediante <strong>políticas de decisión</strong>.

  **Nota**: Publicada anteriormente en Disponibilidad limitada, esta capacidad ya está disponible para todos los entornos (Disponibilidad general).

  Fecha de disponibilidad: 12 de febrero de 2026.


#### Recorridos

* **Varias acciones entrantes en recorrido**: para simplificar la orquestación de recorrido, ahora puede definir varias <strong>acciones entrantes</strong> en un solo recorrido. Esta funcionalidad, que antes estaba disponible en las campañas, le permite enviar varias <strong>experiencias basadas en código</strong>, <strong>mensajes en la aplicación</strong>, <strong>tarjetas de contenido</strong> o <strong>acciones web</strong> a diferentes ubicaciones al mismo tiempo, cada una de las cuales contiene contenido específico.

  **Nota**: Publicada anteriormente en Disponibilidad limitada, esta capacidad ya está disponible para todos los entornos (Disponibilidad general).


* **Webhooks de SMS**: los <strong>Webhooks</strong> son ahora compatibles con todos los proveedores de SMS. Puede configurar cada webhook en función de su propósito: <strong>Webhooks entrantes</strong> para capturar mensajes entrantes y <strong>Webhooks de comentarios</strong> para recibir confirmaciones de entrega, actualizaciones de estado y otros eventos relacionados con mensajes. [Más información](../sms/sms-webhook.md)

  Fecha de disponibilidad: 2 de febrero de 2026.