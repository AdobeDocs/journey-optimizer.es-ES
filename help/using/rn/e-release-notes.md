---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
hide: true
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
source-git-commit: 498ffd4d4d68dfc678ae4e2e8ad9ae39834a6b23
workflow-type: tm+mt
source-wordcount: 2594
ht-degree: 13%

---


# Notas de la versión preliminar {#e-release-notes}

Adobe Journey Optimizer ofrece de forma continua nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

## Notas previas al lanzamiento de septiembre de 2026 {#sep-26-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican una vez que los cambios estén disponibles en producción. Aunque la mayoría de los cambios se implementan en la fecha de lanzamiento de la versión, algunos pueden implementarse más adelante. Consulte la fecha de disponibilidad indicada para cada entrada para obtener más información.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de la versión**: 22 y 23 de septiembre de 2026

### Administración de contenido {#sep-26-content-management}

La siguiente funcionalidad se incluye en la administración de contenido en esta versión.

<table>
<thead>
<tr>
<th><strong>Complementos de diseño de correo electrónico y copia de mensajes en CX Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Hay dos nuevos complementos disponibles en CX Coworker para optimizar tus flujos de trabajo de <strong>mensajería y correo electrónico</strong> desde la estrategia hasta la implementación:</p>
<p><strong>Complemento de copia de mensaje</strong>:</p>
<ul>
<li>Captura informes de campaña y define mapas de mensajería, arcos narrativos y funciones de canal.</li>
<li>Crea una matriz de contenido multidimensional adaptada a canales, puntos de contacto, configuraciones regionales, audiencias y variantes.</li>
<li>Produce una copia nueva y aprovecha Adobe Firefly para generar, recortar y adaptar los elementos visuales de la campaña.</li>
<li>Permite la evaluación de contenido in situ y vuelve a sincronizar directamente los recursos aprobados con Journey Optimizer, Adobe Campaign V8 y Marketo.</li>
</ul>
<p><strong>Complemento de diseño de correo electrónico</strong>:</p>
<ul>
<li>Convierte los objetivos de marketing, las capturas de pantalla de referencia o los vínculos de diseño de Figma en planes de diseño personalizados y HTML de correo electrónico listo para la producción.</li>
<li>Gestiona recursos de marca reutilizables, tokens de diseño y plantillas de correo electrónico estructurales.</li>
<li>Las auditorías reunieron el código de correo electrónico para el cumplimiento normativo corporativo, la calidad del diseño visual y los estándares de accesibilidad WCAG 2.1 AA.</li>
<li>Exporta HTML aprobado directamente a Adobe Journey Optimizer y Adobe Campaign.</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15642" target="_blank">DOCAC-15642</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Lealtad {#sep-26-loyalty}

Las siguientes capacidades y mejoras llegan a Loyalty en esta versión.

<table>
<thead>
<tr>
<th><strong>Oportunidades de desafío</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El menú Rendimiento de fidelización ahora incluye una <strong>pestaña Oportunidades</strong>, que muestra tendencias y brechas detectadas por IA, como fricción de progresión de nivel o abandono de tarea de desafío, cada una con un impacto proyectado y una acción de un solo clic "Crear con IA" para generar un desafío que lo resuelva.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15563" target="_blank">DOCAC-15563</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15661" target="_blank">DOCAC-15661</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **aptitud para recomendar fidelidad de CX Coworker**: los especialistas en marketing ahora pueden solicitar **oportunidades de desafío** directamente en la interfaz conversacional de CX Coworker, obteniendo ideas de desafío fundamentadas en tendencias reales del programa de fidelidad y convirtiéndolas en desafíos en vivo sin abandonar el chat. <a href="https://jira.corp.adobe.com/browse/DOCAC-15565" target="_blank">DOCAC-15565</a> <!-- Documentation link: TBD -->

### Incorporación {#sep-26-onboarding}

La siguiente funcionalidad se incorpora en esta versión.

<table>
<thead>
<tr>
<th><strong>Funciones guiadas para incorporar correos electrónicos y recorridos (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La transición a Adobe Journey Optimizer desde otra plataforma de marketing es más sencilla gracias a las funcionalidades guiadas que le ayudan a trasladar el contenido y los recorridos de correo electrónico existentes a Journey Optimizer. Un <strong>espacio de trabajo dedicado</strong> le permite reutilizar lo que tiene en lugar de reconstruirlo desde cero.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15330" target="_blank">DOCAC-15330</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Recorridos {#sep-26-journeys}

Las siguientes capacidades y mejoras estarán disponibles en los recorridos en esta versión.

<table>
<thead>
<tr>
<th><strong>Simulación de recorrido en CX Coworker (MCP y chat)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La <strong>aptitud de simulación de Recorrido</strong> de CX Coworker automatiza la validación de recorrido de extremo a extremo y le permite interpretar fácilmente los resultados. Tenga en cuenta que, en la actualidad, esta función solo admite el flujo de simulación rápida y no reemplaza completamente la experiencia de simulación manual de Journey Optimizer.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15374" target="_blank">DOCAC-15374</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **La experimentación de rutas de decisiones en la simulación de Recorridos** - **Experimentación de rutas**, parte de la actividad de optimización en Decisioning, ahora se admite en la simulación de Recorridos. <a href="https://jira.corp.adobe.com/browse/DOCAC-15641" target="_blank">DOCAC-15641</a> <!-- Documentation link: TBD -->

* **Compatibilidad con ID suplementario en la simulación de Recorrido** - **La simulación de Recorrido admite ahora el ID suplementario**, lo que le permite probar escenarios de usuario complejos para recorridos activados por eventos y de audiencia de lectura. <a href="https://jira.corp.adobe.com/browse/DOCAC-15448" target="_blank">DOCAC-15448</a> <!-- Documentation link: TBD -->

<table>
<thead>
<tr>
<th><strong>Creación de recorridos desde el carril de CX Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La creación de Recorridos de <strong>con IA</strong> ya está disponible directamente desde el carril derecho de CX Coworker, reemplazando la experiencia anterior del asistente de IA con un punto de entrada integrado con marca modificada para la generación de recorridos.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14898" target="_blank">DOCAC-14898</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Lógica de espera de evaluación de audiencia por lotes refinada** - En la **actividad Leer audiencia**, la opción &quot;Déclencheur tras evaluación de audiencia por lotes&quot; en recorrido ahora espera a que se complete cualquier segmentación por lotes que ya esté en curso, lo que garantiza que el recorrido utilice los datos de esa ejecución en lugar de volver a una instantánea anterior. Si no hay ninguna segmentación por lotes en curso, la recorrido se activa inmediatamente con los datos de audiencia más recientes disponibles. <a href="https://jira.corp.adobe.com/browse/DOCAC-15465" target="_blank">DOCAC-15465</a> <!-- Documentation link: TBD -->

* **Comparar versiones de recorrido con CX Coworker**: hoy, para revisar lo que ha cambiado entre dos versiones de un recorrido es necesario compararlo manualmente dentro de Journey Optimizer nodo por nodo. No hay una comparación de diferencias estructurada, lo que hace que las comprobaciones de cambio, revisión, auditoría y prepublicación sean lentas y propensas a errores, especialmente a medida que los recorridos se vuelven más complejos. Esta funcionalidad permite a un cliente o a un agente de IA comparar dos versiones cualquiera de un recorrido a través de CX Coworker Chat y recuperar una fidelidad completa, **comparación de diferencias estructurada** - nodos agregados/eliminados/modificados/movidos con detalles de nivel de campo, conexiones cambiadas, cambios de propiedad de nivel de recorrido y recuentos de acumulación - sin necesidad de abrir Journey Optimizer. <a href="https://jira.corp.adobe.com/browse/DOCAC-15297" target="_blank">DOCAC-15297</a> <!-- Documentation link: TBD -->

* **Vista previa del contenido en el lienzo del recorrido**. Para revisar el contenido del canal hoy mismo es necesario abrir cada nodo individualmente, uno por vez. Es lento y propenso a errores en recorridos con muchos nodos de canal, especialmente cuando la personalización significa comprobar varios tratamientos o variantes por nodo. **Vista previa del contenido** elimina esa fricción al mostrar una miniatura de contenido para cada nodo de canal directamente en el lienzo, con un modal de pantalla completa para inspeccionar y cambiar entre tratamientos y variantes. <a href="https://jira.corp.adobe.com/browse/DOCAC-15456" target="_blank">DOCAC-15456</a> <!-- Documentation link: TBD -->

### Canales {#sep-26-channels}

Las siguientes funcionalidades y mejoras están llegando a los canales en esta versión.

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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15510" target="_blank">DOCAC-15510</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal saliente personalizado (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Canales salientes personalizados</strong> permiten a los administradores llevar cualquier canal de mensajería saliente basado en HTTP, como WeChat, Kakao Talk, Messenger o un proveedor propietario, directamente a Journey Optimizer a través de un Generador de canales sin código. Una vez configurados, los canales personalizados están disponibles en cualquier campaña, recorrido y campaña orquestada, con el mismo conjunto completo de funcionalidades que los canales nativos: personalización con el editor de expresiones, experimentación de contenido, previsualización y prueba, creación de informes predeterminada y aplicación de consentimiento y gobernanza.</p>
<p>Con esta versión, los canales salientes personalizados también obtienen varias funciones nuevas:</p>
<ul>
<li>Utilice Journey Optimizer Decisioning en la carga útil del canal personalizado a través del Editor de Personalization, del mismo modo que en las experiencias basadas en código.</li>
<li>Aplique reglas empresariales a los canales personalizados, del mismo modo que ya lo hace en los canales nativos.</li>
<li>Seleccione canales personalizados en la lista de canales para campañas activadas por API, lo que anteriormente no era posible.</li>
<li>Defina un webhook de informes para un canal personalizado y adjúntelo a una configuración de canal para que pueda enriquecer los informes de Journey Optimizer con eventos de interacción.</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14037" target="_blank">DOCAC-14037</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Anular configuración de canal de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Al crear los recorridos y las campañas, ahora puede anular los parámetros de correo electrónico derivados de la configuración de canal seleccionada directamente en el nivel de acción de recorrido o campaña.</p>
<p>Esto le permite personalizar los campos de encabezado del correo electrónico (<strong>De nombre</strong>, <strong>De prefijo de correo electrónico</strong>, <strong>Responder al nombre</strong> y <strong>Responder al correo electrónico</strong>), la dirección de ejecución y los valores de cancelación de suscripción a una lista, mediante atributos de perfil o datos contextuales para un control más preciso. En particular, esto permite que los detalles del remitente reflejen el asesor, la ubicación o la sucursal relevantes para cada destinatario, en lugar de enrutar todos los envíos a través de una sola dirección corporativa.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14718" target="_blank">DOCAC-14718</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Flexibilidad de autenticación BYOP de SMS personalizado**: ahora puede configurar **encabezados de autenticación personalizados** al conectar la configuración de OAuth de su proveedor de SMS, incluso dónde se coloca el token en los mensajes salientes y cómo se da formato a la propia solicitud de token. <a href="https://jira.corp.adobe.com/browse/DOCAC-15638" target="_blank">DOCAC-15638</a> <!-- Documentation link: TBD -->

### Campañas orquestadas {#sep-26-oc}

Las siguientes funcionalidades y mejoras estarán disponibles en las campañas orquestadas en esta versión.

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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15020" target="_blank">DOCAC-15020</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alerta para campañas orquestadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las campañas orquestadas ahora admiten <strong>alertas automatizadas</strong> a través del mismo marco de alertas utilizado en los recorridos y las campañas. Las alertas se activan cuando falla la ejecución de una campaña, agota el tiempo de espera o requiere confirmación, y cada alerta incluye lo que ha sucedido, cuándo, dónde y un vínculo directo a la vista de monitorización, clasificados por gravedad para que los equipos puedan priorizar sin comprobaciones manuales de la IU.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14886" target="_blank">DOCAC-14886</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Canal LINE para campañas orquestadas**: LINE ya está disponible como canal saliente nativo en campañas orquestadas, junto con correo electrónico, SMS y push. Puede crear y enviar mensajes de LINE directamente desde el lienzo de la campaña, incluidos texto, pegatinas, imágenes, vídeos, datos de ubicación y mensajes de Flex, lo que admite casos de uso de participación promocional, transaccional y continua en mercados dominantes de LINE como Japón y APAC. Esta capacidad, que se publicó anteriormente con disponibilidad limitada, ya está disponible de forma general. <a href="https://jira.corp.adobe.com/browse/DOCAC-15102" target="_blank">DOCAC-15102</a> <!-- Documentation link: TBD -->

* **Nuevas API de supervisión de campañas orquestadas**: las nuevas **especificaciones de la API** ya están disponibles para las campañas orquestadas, lo que le permite crear, administrar y almacenar en déclencheur mediante programación campañas orquestadas, lo que permite una integración más profunda con sistemas externos y canalizaciones de automatización. <a href="https://jira.corp.adobe.com/browse/DOCAC-14308" target="_blank">DOCAC-14308</a> <!-- Documentation link: TBD -->

* **Mejoras en la experiencia de usuario de unión directa**: al agregar un atributo de una colección relacionada, ahora puede elegir entre tres modos de unión, un nuevo valor predeterminado que le advierte sobre el posible impacto en el rendimiento de los productos cartesianos, además de los modos Agregado y Avanzado existentes, lo que facilita la comprensión de las compensaciones de su consulta antes de crearla. <a href="https://jira.corp.adobe.com/browse/DOCAC-15675" target="_blank">DOCAC-15675</a> <!-- Documentation link: TBD -->

* **Contenido condicional con datos relacionales en campañas orquestadas**: al crear contenido condicional en el Designer de correo electrónico para campañas orquestadas, ahora puede generar condiciones directamente en **datos relacionales**, como registros relacionados asociados a un perfil, no solo atributos de perfil estándar. Esto reduce una brecha con respecto a la versión original, por lo que los especialistas en marketing pueden crear estas condiciones de forma visual, sin necesidad de ayuda de ingeniería. <a href="https://jira.corp.adobe.com/browse/DOCAC-15679" target="_blank">DOCAC-15679</a> <!-- Documentation link: TBD -->

### Campañas {#sep-26-campaigns}

Las siguientes funcionalidades y mejoras están llegando a las campañas de esta versión.

<table>
<thead>
<tr>
<th><strong>Simulación de experiencia entrante en campañas de acción (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede simular acciones de canal de entrada en campañas de acción antes de lanzarlas. Utilice el modo de simulación para probar la configuración con usuarios simulados y previsualizar la experiencia procesada, incluida una URL y un código QR generados, para poder validar las reglas, la toma de decisiones y el renderizado de contenido de extremo a extremo.</p>
<p>Actualmente, esta funcionalidad está en versión Private Beta y está disponible para un conjunto limitado de organizaciones. Póngase en contacto con su representante de Adobe para obtener más información.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15166" target="_blank">DOCAC-15166</a></p>
</td>
</tr>
</tbody>
</table>

* **Carpetas para campañas**: ahora puede organizar sus campañas en **carpetas** para mejorar la navegación y la administración en la interfaz. <a href="https://jira.corp.adobe.com/browse/DOCAC-15098" target="_blank">DOCAC-15098</a> <!-- Documentation link: TBD -->

### Toma de decisiones {#sep-26-decisioning}

Las siguientes funcionalidades y mejoras estarán disponibles en la toma de decisiones en esta versión.

<table>
<thead>
<tr>
<th><strong>Compatibilidad con decisiones en el canal Web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La toma de decisiones ya está disponible para el canal web. Puede utilizar las directivas de decisión directamente en el editor visual web para enviar las ofertas más relevantes a cada visitante.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11548" target="_blank">DOCAC-11548</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Generación de reglas de decisiones desde CX Coworker**: la experiencia **generación de reglas de decisiones asistidas por IA**, disponible anteriormente a través del carril derecho, ahora es accesible a través de CX Coworker, que reemplaza el carril derecho como la forma de generar reglas con IA. <a href="https://jira.corp.adobe.com/browse/DOCAC-15290" target="_blank">DOCAC-15290</a> <!-- Documentation link: TBD -->

### Correo directo {#sep-26-direct-mail}

Las siguientes funcionalidades y mejoras se incluyen en Direct Mail en esta versión.

* **Dividir archivos grandes automáticamente**: los archivos de correo directo ahora se pueden dividir en varias partes automáticamente cuando superan los 20 GB, o manualmente eligiendo un tamaño de archivo de destino en la configuración de enrutamiento de archivos. Un archivo de manifiesto JSON opcional describe todas las partes generadas. <a href="https://jira.corp.adobe.com/browse/DOCAC-15677" target="_blank">DOCAC-15677</a> <!-- Documentation link: TBD -->

* **Límite de audiencia aumentado**: el límite de audiencia del canal de correo directo se ha aumentado de 3 millones a 100 millones de perfiles, lo que permite dirigirse a audiencias mucho más grandes sin alcanzar los errores de creación de archivos. <a href="https://jira.corp.adobe.com/browse/DOCAC-15676" target="_blank">DOCAC-15676</a> <!-- Documentation link: TBD -->

### Diseñador de correo electrónico {#sep-26-email-designer}

Las siguientes funcionalidades y mejoras están llegando a Email Designer en esta versión.

<table>
<thead>
<tr>
<th><strong>Estilo de modo oscuro independiente para variantes de temas de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los temas de correo electrónico ahora admiten un estilo independiente para el modo oscuro. En el generador de temáticas, puede activar el modo oscuro para una variante determinada para generar una hoja de estilos en modo oscuro dedicada que edite por separado de los estilos en modo claro: los cambios realizados en un modo ya no sobrescriben al otro. En el editor de correo electrónico y plantillas, una nueva opción de previsualización junto a las opciones de escritorio y vista móvil permite previsualizar el contenido en modo oscuro.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15663" target="_blank">DOCAC-15663</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Importar plantillas de Dynamic Media directamente desde archivos de PSD en el Designer de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El componente Dynamic Media de Designer de correo electrónico ahora le permite importar un archivo de Photoshop (PSD) directamente como una plantilla nueva, además de examinar las plantillas de Dynamic Media existentes. Arrastre y suelte un archivo de PSD en el componente y Adobe Journey Optimizer lo convertirá automáticamente en una plantilla de Dynamic Media almacenada en Dynamic Media, sin necesidad de realizar conversiones manuales ni viajes de ida y vuelta a través de Adobe Experience Manager. Una vez importada, puede editarla con el editor integrado de Dynamic Media, la misma experiencia que se utiliza para el contenido de Adobe Express en el Designer de correo electrónico.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15664" target="_blank">DOCAC-15664</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuevo componente de tabla en Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Designer de correo electrónico ahora incluye un <strong>componente Tabla</strong> integrado, que le permite estructurar el contenido en filas y columnas directamente dentro del correo electrónico. Arrastre y suelte el componente en el lienzo, personalice el número de filas y columnas y aplique estilo a cada celda de forma independiente para crear diseños claros y organizados sin depender del HTML personalizado.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15093" target="_blank">DOCAC-15093</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Fuentes de reserva para fuentes personalizadas en temas de correo electrónico**: ahora puede definir una fuente de reserva para cualquier fuente personalizada (web) aplicada a través de temáticas de correo electrónico. Si el cliente de correo electrónico de un suscriptor no admite la fuente personalizada, Adobe Journey Optimizer muestra automáticamente la fuente de reserva especificada en lugar de dejar la opción a la fuente predeterminada del cliente de correo electrónico. Esto mantiene la tipografía del correo electrónico más cerca de las directrices de marca y reduce las incoherencias en el procesamiento de fuentes en los clientes de correo electrónico. <a href="https://jira.corp.adobe.com/browse/DOCAC-15662" target="_blank">DOCAC-15662</a> <!-- Documentation link: TBD -->

### Mejoras de uso {#sep-26-usability}

* **Mejoras de uso en la experiencia de simulación de contenido**: la nueva experiencia de simulación de contenido ahora le permite nombrar y organizar sus variantes para facilitar la comparación, copiar o eliminar detalles de la variante directamente desde cada tarjeta, ver rutas de atributos completas y la configuración de canal por tarjeta bajo demanda, y cargar sus propios perfiles CSV, JSON o JSONL desde un botón de carga más prominente. <a href="https://jira.corp.adobe.com/browse/DOCAC-15570" target="_blank">DOCAC-15570</a>


