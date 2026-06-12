---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: a2257f19ea46aaf4bcf45580a0e6cf0d207be355
workflow-type: tm+mt
source-wordcount: 1876
ht-degree: 5%

---


# Notas de la versión preliminar {#e-release-notes}

Adobe Journey Optimizer ofrece continuamente nuevas funciones, mejoras en las funciones existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

## Notas previas al lanzamiento de junio de 2026 {#june-26-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican una vez que los cambios están activos en la producción. Aunque la mayoría de los cambios se entregan en la fecha de lanzamiento, algunos pueden implementarse más adelante. Consulte la Fecha de disponibilidad indicada para cada entrada para obtener más información.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de la versión**: 16 y 17 de junio de 2026

### Recorridos {#june-26-journeys}

Las siguientes funcionalidades y mejoras están llegando a los recorridos en esta versión.

* **Aumento del límite de recorridos activos y nuevas protecciones**: ahora puede tener hasta **200 recorridos activos**, más que el límite anterior de 100.

* **Fechas de inicio y finalización en el encabezado del recorrido**: cuando las fechas de inicio o finalización se configuran en un recorrido activo, ahora aparecen en el **encabezado del recorrido** junto al distintivo del estado activo. La etiqueta mostrada se adapta en función de si cada fecha es próxima o ya ha pasado.

* **Detener o cerrar un recorrido pausado directamente** - Ahora puede **detener un recorrido o cerrarlo a nuevas entradas** directamente desde el estado **Pausado**. Anteriormente, un recorrido pausado tenía que reanudarse a Activo antes de que se pudiera detener o cerrar.

### Campañas orquestadas {#june-26-oc}

Las siguientes funcionalidades y mejoras están llegando a las campañas orquestadas en esta versión.

<table>
<thead>
<tr>
<th><strong>Direccionamiento basado en archivos en campañas organizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las campañas orquestadas ahora admiten la carga de un <strong>archivo CSV o TXT</strong> directamente en el lienzo de campaña como audiencia de segmentación, sin ingerir primero el archivo en Adobe Experience Platform. Los datos del archivo se consumen en el momento de la ejecución y no persisten como un conjunto de datos de Adobe Experience Platform. Durante la configuración del archivo, puede definir asignaciones de columnas, tipos de datos, control de valores NULL y directivas de error por columna. Las filas que no superan la validación se rechazan y registran antes de que se ejecute la campaña, lo que mantiene la audiencia limpia sin preprocesamiento manual. Esto es especialmente adecuado para envíos específicos o campañas de listas de socios en las que no es práctico crear una canalización de ingesta completa.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
</td>
</tr>
</tbody>
</table>

* **Personalización basada en bucles para datos relacionales en campañas orquestadas**: el editor de personalización ahora admite un **bloque de bucles** que se repite en colecciones relacionales, como pedidos, cuentas o reservas, y procesa un bloque de contenido por registro en un solo correo electrónico o SMS. Las colecciones se configuran mediante el selector de datos utilizando tokens de personalización, sin necesidad de escribir expresiones. Puede obtener una vista previa de cómo se representan los bloques en bucle con los datos de ejemplo antes de que la campaña se ponga en marcha, incluida la administración de colecciones vacías.

* **Personalizar los detalles del remitente del correo electrónico por destinatario y campaña**: las campañas organizadas ahora admiten la personalización de **campos de encabezado de correo electrónico**, incluidos el nombre del remitente, la dirección del remitente y la respuesta a, mediante atributos de perfil o datos relacionales. Esto permite que los detalles del remitente reflejen el asesor, la ubicación o la sucursal relevantes para cada destinatario, en lugar de enrutar todos los envíos a través de una sola dirección corporativa. Los valores del encabezado se pueden establecer en el nivel de canal y anularse por campaña utilizando datos contextuales para un control más preciso.

<!--
* **Target dimension simplification in Orchestrated campaigns** - The active **targeting dimension** is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->

### Toma de decisiones {#june-26-decisioning}

La siguiente funcionalidad llega a Decisioning en esta versión.

<table>
<thead>
<tr>
<th><strong>Aprovechamiento del fragmento de contenido de Adobe Experience Manager en Decisioning</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede asignar <strong>fragmentos de contenido de Adobe Experience Manager</strong> a <strong>elementos de decisión</strong> en la toma de decisiones y aprovecharlos dentro de las directivas de decisión para entregar el fragmento adecuado al cliente correcto en el momento adecuado.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

* **Atributos de oferta dinámicos**: los atributos de oferta de Decisioning ahora se pueden personalizar en el momento de la entrega mediante datos de perfil, contextuales y de audiencia. Esto elimina la necesidad de mantener ofertas duplicadas para variaciones de contenido menores, lo que permite a los especialistas en marketing administrar menos elementos de decisión más flexibles.

* **Límite de frecuencia de nivel de ubicación en Decisioning**: las reglas de límite de frecuencia en Decisioning ahora se pueden vincular a ubicaciones individuales, lo que le proporciona un control más preciso sobre la frecuencia con la que se muestra una oferta en una superficie determinada. Hay dos modos disponibles:

   * Límite específico de la ubicación: define un límite que se aplica solo cuando la oferta se muestra en una ubicación seleccionada.
   * Límite por ubicación: aplique un límite de forma independiente en todas las ubicaciones en las que aparezca la oferta, de modo que cada ubicación mantenga su propio contador de límite.

### Correo electrónico {#june-26-email}

Las siguientes funcionalidades y mejoras están llegando al canal de correo electrónico en esta versión.

<table>
<thead>
<tr>
<th><strong>Comprobaciones de calidad del contenido en el Designer de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora incluye puntuación de calidad de contenido directamente en el Designer de correo electrónico, que analiza el correo electrónico en tres dimensiones antes del lanzamiento: ortografía, gramática y puntuación; legibilidad y tono, incluidos indicadores para frases largas, voz pasiva y jerga; y línea de asunto y efectividad de CTA, puntuados para claridad, urgencia y estructura. Cada comprobación muestra sugerencias procesables, lo que permite a los equipos detectar y resolver problemas sin salir de la interfaz de creación.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activar reducción de tamaño de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora incluye una opción para reducir el tamaño del HTML del correo electrónico eliminando los espacios en blanco, los comentarios y el código redundante innecesarios, sin afectar al procesamiento del correo electrónico. Esto puede mejorar la capacidad de entrega al evitar los umbrales de tamaño que algunos proveedores de correo electrónico utilizan para marcar o rechazar mensajes y puede reducir el tiempo de carga de los destinatarios.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Texto enriquecido en campos editables para fragmentos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede añadir texto enriquecido a fragmentos personalizables que se utilizan en el contenido de los correos electrónicos. Por ejemplo, al utilizar el componente Texto como campo editable en el Designer de correo electrónico, puede dar formato directamente al contenido (por ejemplo, negrita y cursiva) e insertar hipervínculos.</p>
</td>
</tr>
</tbody>
</table>

* **Conversor mejorado de imagen a HTML**: Ya está disponible una nueva versión de la función de conversión de imagen a HTML, que ofrece una precisión mejorada para la generación de HTML. Esta actualización aprovecha los modelos LLM de nivel superior para ofrecer una salida de HTML más precisa y fiable a partir de las entradas de imagen.

+++ Próximamente — **La información siguiente está sujeta a cambios**

<table>
<thead>
<tr>
<th><strong>Módulos de Designer de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Email Designer ahora incluye una biblioteca de módulos de diseño listos para usar, como encabezados, tarjetas de producto, bloques de información y pies de página, que puede arrastrar y soltar directamente en el lienzo del correo electrónico.</p>
<p>Cada módulo viene preconfigurado con propiedades editables (imagen, título, texto, botón, vínculos) y se puede personalizar completamente a través de la interfaz de WYSIWYG, lo que acelera la creación de correos electrónicos sin necesidad de crear estructuras desde cero.</p>
<p>Fecha de disponibilidad: 22 de junio de 2026</p>
</td>
</tr>
</tbody>
</table>

+++

### Mensajería móvil (SMS, MMS, RCS y LINE) {#june-26-mobile}

Las siguientes mejoras se incluyen en la mensajería móvil en esta versión.

* **Clics únicos para informes de SMS**: Se ha introducido un nuevo módulo de **Clics únicos** en los informes de SMS, que trae el mismo nivel de seguimiento granular de rendimiento a los SMS disponibles actualmente para los informes de correo electrónico.

* **Canal LINE - Creación de cambios** - La interfaz de usuario del canal LINE se ha actualizado con funciones avanzadas de creación de mensajes. Esta versión incorpora compatibilidad con **varios formatos de mensaje**, incluidos Texto, Imagen, Mapa de imágenes, Carrusel y Flex (Editor JSON), además de vistas previas de dispositivos en tiempo real. Los usuarios ahora pueden administrar mensajes agrupados de hasta cinco mensajes ordenados (con controles de adición, eliminación y reordenación) y aprovechar el editor de personalización integrado para mensajes validados y dinámicos.

* **SMS - Mostrar métricas de uso** - Para los clientes que compran SMS directamente a través de Adobe Journey Optimizer, se ha introducido un nuevo **panel de uso de SMS**. Ahora puede ver y rastrear las métricas de envío de mensajes de los últimos 90 días, clasificadas por mensajes móviles originados (MO) y móviles terminados (MT). Estos datos también están disponibles para su descarga a través de CSV, lo que proporciona una mayor visibilidad y control sobre la inversión en SMS.

### Contenido e integraciones {#june-26-content}

En esta versión se incluyen las siguientes funcionalidades y mejoras para la administración de contenido y las integraciones.

<table>
<thead>
<tr>
<th><strong>Mejoras en los fragmentos de contenido de Adobe Experience Manager en Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta versión incorpora varias mejoras para que <strong>Fragmentos de contenido de Adobe Experience Manager</strong> sean más utilizables, controlables y estén más listos para la producción dentro de los flujos de trabajo de creación de Journey Optimizer:</p>
<ul>
<li>Journey Optimizer ahora admite la captura de fragmentos de contenido desde varias configuraciones de Adobe Experience Manager, incluidos los niveles de creación, publicación y publicación autenticada.</li>
<li>Una vez seleccionado un fragmento, su contexto se conserva en todo el mensaje, lo que permite a los autores reutilizar los campos de fragmento en bloques de contenido sin volver a seleccionar.</li>
<li>Se ha introducido una nueva página de lista de fragmentos de contenido en Journey Optimizer para mejorar la administración del ciclo vital; los usuarios pueden identificar fragmentos no sincronizados y sincronizar manualmente el déclencheur para mantenerse al día.</li>
<li>La compatibilidad con la configuración regional y las variaciones ahora permite a los especialistas en marketing trabajar con versiones alternativas del mismo fragmento de contenido de forma más deliberada.</li>
<li>Ahora tiene flexibilidad en la forma en que Adobe Journey Optimizer accede al contenido de Adobe Experience Manager. Esta versión incluye la capacidad de <strong>cambiar el repositorio de origen</strong> para los fragmentos de contenido utilizados en sus recorridos y campañas.</li>
<li>Ahora compatible con <b>Managed Services</b>, puede ver, acceder y usar fragmentos de contenido de Adobe Experience Manager directamente en Journey Optimizer para personalización. Simplemente agregue la URL del repositorio de Adobe Experience Manager Managed Services en los ajustes de configuración como una configuración única.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integración del asistente de IA con Adobe Experience Manager Asset Essentials</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El asistente de IA ahora recupera automáticamente <b>imágenes aprobadas por la marca</b> directamente de su Adobe Experience Manager Assets al generar correos electrónicos, páginas web y notificaciones push. Esto elimina la necesidad de buscar manualmente en Assets o confiar en las retrospectivas de IA genéricas, lo que garantiza que cada imagen sea perfectamente precisa y compatible con la marca.</p>
</td>
</tr>
</tbody>
</table>

<!--
### Campaigns {#june-26-campaigns}

The following improvement is coming to campaigns in this release.

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default **execution field** set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.
-->

### Creación de informes {#june-26-reporting}

En esta versión se incluyen las siguientes mejoras en los informes.

* **Clics estimados para informes de correo electrónico y SMS** — Una nueva métrica de **Clics estimados** ya está disponible en los informes de Recorridos, Campañas y Canales para correo electrónico y SMS. Esta métrica excluye el tráfico de interacción identificado y no humano (NHI) para proporcionar una visión más clara de la participación genuina del cliente. La métrica de clics existente permanece disponible y continúa informando de los clics totales.

+++ Próximamente — **La información siguiente está sujeta a cambios**

* **Nuevas métricas estimadas de clics para los informes de correo electrónico y SMS**: para proporcionar una vista más precisa de la participación real de los clientes, ahora hay disponibles nuevas métricas estimadas en los informes Recorridos, Campañas y Canales. Estas métricas ayudan a filtrar las interacciones no humanas (NHI) y los clics de bots a partir de los datos de los informes:

   * Estimated CTR: clics estimados en relación con las entregas totales.
   * Estimated CTOR for email only: Clics estimados en relación con las aperturas estimadas.

  Fecha de disponibilidad: finales de junio de 2026

+++

### Configuración {#june-26-configuration}

Las siguientes mejoras se incluyen en la configuración y administración de esta versión.

* **Conjunto de datos que se mueve de flujo a modo por lotes** - El conjunto de datos de evento de comentarios de mensajes de AJO está pasando de flujo a **modo de ingesta por lotes**. Este cambio garantiza que la ingesta de datos no supere los límites de ingesta de transmisión. Si utiliza este conjunto de datos en informes de Customer Journey Analytics o ejecuta consultas en él, espere un aumento de la latencia de datos de hasta dos horas en adelante.

+++ Próximamente — **La información siguiente está sujeta a cambios**

* **Lista blanca de IP de Firewall de aplicaciones web (WAF)**: Adobe Journey Optimizer ahora admite la lista blanca de IP de Firewall de aplicaciones web (WAF) para páginas de aterrizaje, lo que permite a las organizaciones aplicar que todas las solicitudes entrantes se enruten exclusivamente a través de su infraestructura de WAF configurada. Con esta mejora, los clientes pueden configurar Journey Optimizer para que rechace cualquier solicitud directa que omita el nivel de WAF, lo que garantiza que las políticas de seguridad definidas en herramientas como Imperva se apliquen de forma coherente. Esta capacidad refuerza la postura de seguridad de las empresas con requisitos estrictos de acceso a la red, lo que les permite un control total del flujo de tráfico a sus páginas de aterrizaje alojadas en AJO.

  Fecha de disponibilidad: finales de junio de 2026

+++

### Mejoras de uso {#june-26-usability}

La siguiente mejora de uso se publicará en esta versión.

* **Carpetas para Recorridos y campañas**: ahora puede organizar sus recorridos y campañas en **carpetas** para mejorar la navegación y la administración en la interfaz.
