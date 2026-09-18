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
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: 58cf5c8ad76ed988ff797a0d1bcd8328321ee737
workflow-type: tm+mt
source-wordcount: '3407'
ht-degree: 8%
---

# Notas de la versión preliminar {#e-release-notes}

Adobe Journey Optimizer ofrece de forma continua nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

## Notas previas al lanzamiento de septiembre de 2026 {#sep-26-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican una vez que los cambios estén disponibles en producción. Aunque la mayoría de los cambios se implementan en la fecha de lanzamiento de la versión, algunos pueden implementarse más adelante. Consulte la fecha de disponibilidad indicada para cada entrada para obtener más información.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de la versión**: 22 y 23 de septiembre de 2026

>[!BEGINSHADEBOX]

**Novedades de CX Enterprise Coworker este mes**

Esta versión incorpora varias características y habilidades nuevas y mejoradas de [Coworker](../start/ai-features.md#cx-coworker) que se enumeran aquí para mayor visibilidad. Cada una de ellas se detalla también en la sección pertinente que figura a continuación.

* [Complementos de diseño de correo electrónico y copia de mensajes](#sep-26-content-management): dos nuevos complementos que optimizan los flujos de trabajo de mensajería y correo electrónico en Coworker, desde información de campaña hasta copia y HTML preparados para la producción.
* [Habilidad de recomendación de fidelización](#sep-26-loyalty): solicita oportunidades de desafío directamente en la interfaz conversacional de tu compañero y conviértelas en desafíos en vivo sin salir del chat.
* [Simulación de Recorrido](#sep-26-journeys): Automatice la validación de recorrido de extremo a extremo e interprete los resultados directamente en Compañero de trabajo.
* [Creación de Recorridos desde el carril de Coworker](#sep-26-journeys): genere recorridos con IA directamente desde el carril derecho de Coworker, reemplazando la experiencia anterior del asistente de IA.
* [Comparar versiones de un recorrido](#sep-26-journeys): obtenga una diferencia estructurada y de fidelidad total entre dos versiones cualquiera de un recorrido a través de Coworker Chat.
* [Aptitud para el análisis de higiene](#sep-26-journeys): analice los recorridos activos y en borrador para detectar configuraciones dañadas, errores silenciosos y recursos en declive o no utilizados, con las correcciones recomendadas.
* [Habilidad con el análisis de rendimiento empresarial](#sep-26-journeys): analice el rendimiento del recorrido y obtenga recomendaciones de optimización concretas desde el chat.
* [Generación de reglas de decisiones](#sep-26-decisioning): genere reglas de decisiones asistidas por IA directamente en Coworker, que ahora reemplaza el carril derecho para esta experiencia.

>[!ENDSHADEBOX]

### Administración de contenido {#sep-26-content-management}

La siguiente funcionalidad se incluye en la administración de contenido en esta versión.

<table>
<thead>
<tr>
<th><strong>Complementos de diseño de correo electrónico y copia de mensajes en Coworker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Hay dos nuevos complementos disponibles en Coworker para optimizar tus <strong>flujos de trabajo de mensajes y correo electrónico</strong> desde la estrategia hasta la implementación:</p>
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
</td>
</tr>
</tbody>
</table>

* **Habilidad para recomendar fidelidad a compañeros de trabajo**: los especialistas en marketing ahora pueden solicitar **oportunidades de desafío** directamente en la interfaz conversacional de los compañeros de trabajo, obteniendo ideas de desafío fundamentadas en tendencias reales del programa de fidelidad y convirtiéndolas en desafíos en vivo sin salir del chat.

* Dominio de **retos en el editor de personalización de tarjetas de contenido**: el editor de personalización de tarjetas de contenido ahora admite **desafíos** como dominio, lo que le permite acceder a los metadatos de desafíos al crear la personalización de tarjetas de contenido. Esto facilita la creación de contenido personalizado para cada fase de un desafío (inicio, en curso y final) sin código personalizado.

* **Plazos para la finalización del desafío de fidelización por miembro**: los desafíos de fidelización ahora admiten los plazos de finalización por miembro: elija &quot;En un número de días después de la inclusión&quot; en Requisitos de finalización para que el plazo de cada miembro se calcule a partir de su propia fecha de inclusión en lugar de una fecha de finalización fija para todo el programa. Si se establecen tanto una fecha de finalización de desafío como esta ventana de inclusión, el plazo de cada miembro es el que sea primero. <!-- Documentation link: TBD -->

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
</td>
</tr>
</tbody>
</table>

### Públicos {#sep-26-audiences}

El siguiente recordatorio se aplica a las audiencias de esta versión.

* **Próximo cambio en las audiencias de enriquecimiento de Audience Composition**: durante la versión de octubre (finales de octubre), Journey Optimizer detendrá los recorridos y campañas que usen o hagan referencia a una audiencia de Audience Composition cuyo conjunto de datos de origen no tenga un **descriptor de identidad principal**. A partir de ese momento, solo se admitirán en recorridos y campañas las audiencias de Composición de audiencia creadas con un descriptor de identidad principal. Si necesita que estos recorridos o campañas permanezcan activos, póngase en contacto con su representante de Adobe para que nuestro equipo de productos le ayude a migrar. <!-- Documentation link: TBD -->

### Recorridos {#sep-26-journeys}

Las siguientes capacidades y mejoras estarán disponibles en los recorridos en esta versión.

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
<p>La revisión del contenido del canal hoy en día requiere la apertura de cada nodo individualmente, uno a la vez: lento y propenso a errores en recorridos con muchos nodos de canal, especialmente cuando la personalización significa comprobar varios tratamientos o variantes por nodo. <strong>Vista previa del contenido</strong> elimina esa fricción al mostrar una miniatura de contenido para cada nodo de canal directamente en el lienzo, con un modal de pantalla completa para inspeccionar y cambiar entre tratamientos y variantes.</p>
</td>
</tr>
</tbody>
</table>

* **Compatibilidad con ID suplementario en la simulación de Recorrido** - **La simulación de Recorrido admite ahora el ID suplementario**, lo que le permite probar escenarios de usuario complejos para recorridos activados por eventos y de audiencia de lectura.

* **Compatibilidad con saltos para recorridos de calificación de audiencia**: los Recorridos que comienzan con una **calificación de audiencia** ahora pueden usar una actividad **Jump** para entrar en un recorrido de inicio basado en eventos; no se admite el salto a un recorrido basado en calificación de audiencia.

* **Comparar versiones de recorrido con el colaborador**: hoy, para revisar lo que ha cambiado entre dos versiones de un recorrido es necesario compararlo manualmente dentro de Journey Optimizer nodo por nodo. No hay ninguna comparación de diferencias estructurada, lo que hace que las comprobaciones de cambio, revisión, auditoría y prepublicación sean lentas y propensas a errores, especialmente a medida que los recorridos se vuelven más complejos. Esta funcionalidad permite a un cliente o a un agente de IA comparar dos versiones cualquiera de un recorrido a través del chat de compañeros y recuperar una fidelidad completa, **diferencia estructurada**: nodos agregados, eliminados, modificados o movidos con detalles de nivel de campo, conexiones cambiadas, cambios de propiedad de nivel de recorrido y recuentos de acumulación, sin necesidad de abrir Journey Optimizer.

* **Se han reducido los eventos de paso para las actividades de espera y evento** - Ya no se generan eventos de paso para las actividades **wait** y **event** cuando el perfil no se ha procesado realmente en esa actividad. <!-- DRAFT: pending DOCAC sub-task under DOCAC-15691, see CJM-165835 -->
<!-- Documentation link: TBD -->

* **Supresión de eventos de paso de ejecución en seco para informes personalizados**: como parte de la optimización de eventos de paso, Journey Optimizer ahora deja de generar ciertos eventos de paso que no se pueden notificar durante las ejecuciones en seco de Recorrido. Esto solo afecta a los informes personalizados creados en estos tipos de eventos de paso de ejecución en seco. Si se ve afectado, vuelva a almacenar en déclencheur la ejecución en seco para regenerar los datos.

* **Análisis de higiene Habilidad del compañero**: una nueva habilidad de análisis de higiene del compañero analiza los recorridos activos y en borrador para detectar configuraciones dañadas, errores silenciosos y recursos en declive o no utilizados, como recorridos en borrador antiguos, fuentes de datos huérfanas y errores persistentes de acciones personalizadas, así como correcciones recomendadas desde el chat. <!-- Documentation link: TBD -->

* **Habilidad de colaborador de análisis de rendimiento empresarial** - Una nueva habilidad de **análisis de rendimiento empresarial** en colaborador analiza el rendimiento de sus recorridos, explica las áreas de menor rendimiento y recomienda optimizaciones concretas, como esperas de renovación de participación, escalación de canal y optimización del tiempo de envío.  <!-- Documentation link: TBD -->

* **Tiempo de espera de recuperación de evento automático en Propiedades de Recorrido** - Propiedades de Recorrido ahora incluye una configuración de **Establecer tiempo de espera de recuperación de evento**: de forma predeterminada, los eventos de recorrido afectados se reproducen automáticamente durante un máximo de 72 horas después de una interrupción del servicio sin necesidad de realizar ninguna acción. Puede activar esta configuración para controlar la ventana de reproducción (0-72 horas) para recorridos con distinción de tiempo. El campo **Tiempo de espera o error** existente también ha cambiado de nombre a **Acción personalizada / Tiempo de espera de acción IDS** para evitar confusiones entre las dos configuraciones.

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
</td>
</tr>
</tbody>
</table>

* **Canal LINE para campañas orquestadas**: LINE ya está disponible como canal saliente nativo en campañas orquestadas, junto con correo electrónico, SMS y push. Puede crear y enviar mensajes de LINE directamente desde el lienzo de la campaña, incluidos texto, pegatinas, imágenes, vídeos, datos de ubicación y mensajes de Flex, lo que admite casos de uso de participación promocional, transaccional y continua en mercados dominantes de LINE como Japón y APAC. Esta capacidad, que se publicó anteriormente con disponibilidad limitada, ya está disponible de forma general.

* **Nuevas API de supervisión de campañas orquestadas**: las nuevas **especificaciones de la API** ya están disponibles para las campañas orquestadas, lo que le permite crear, administrar y almacenar en déclencheur mediante programación campañas orquestadas, lo que permite una integración más profunda con sistemas externos y canalizaciones de automatización.

* **Mejoras en la experiencia de usuario de unión directa**: al agregar un atributo de una colección relacionada, ahora puede elegir entre tres modos de unión, un nuevo valor predeterminado que le advierte sobre el posible impacto en el rendimiento de los productos cartesianos, además de los modos Agregado y Avanzado existentes, lo que facilita la comprensión de las compensaciones de su consulta antes de crearla.

* **Contenido condicional con datos relacionales en campañas orquestadas**: al crear contenido condicional en el Designer de correo electrónico para campañas orquestadas, ahora puede generar condiciones directamente en **datos relacionales**, como registros relacionados asociados a un perfil, no solo atributos de perfil estándar. Esto reduce una brecha con respecto a la versión original, por lo que los especialistas en marketing pueden crear estas condiciones de forma visual, sin necesidad de ayuda de ingeniería.

* **Supervisión de Campaign Orchestration**: ya está disponible una nueva interfaz de usuario para realizar el seguimiento del estado de ingesta y la actualización de los datos del almacén relacional que usa la segmentación de Campaign orquestada. Le ofrece una visibilidad directa del estado de los datos que alimentan a las audiencias por lotes. Una nueva pestaña de Campaign Orchestration del panel de monitorización de Adobe Experience Platform muestra el estado de los flujos de datos del almacén relacional (registros ingeridos/actualizados/eliminados/fallidos/omitidos), con gráficos desglosados y un desglose por flujo de datos/conjunto de datos, incluido el linaje.


### Campañas {#sep-26-campaigns}

Las siguientes mejoras se implementan en las campañas de esta versión.

* **Carpetas para campañas**: ahora puede organizar sus campañas en **carpetas** para mejorar la navegación y la administración en la interfaz.

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
</td>
</tr>
</tbody>
</table>

* **Generación de reglas de decisiones de Coworker**: la experiencia **generación de reglas de decisiones asistidas por IA**, disponible anteriormente a través del carril derecho, ahora es accesible a través de Coworker, que reemplaza el carril derecho como la forma de generar reglas con IA.

* **Compatibilidad con perfiles Adobe Experience Platform en la simulación de reglas y fórmulas de clasificación**: al simular una regla o una fórmula de clasificación, ahora puede seleccionar un perfil Adobe Experience Platform para rellenar automáticamente los atributos de una variante de datos de prueba en lugar de introducirlos manualmente.

### Correo directo {#sep-26-direct-mail}

Las siguientes funcionalidades y mejoras se incluyen en Direct Mail en esta versión.

* **Dividir archivos grandes automáticamente**: los archivos de correo directo ahora se pueden dividir en varias partes automáticamente cuando superan los 20 GB, o manualmente eligiendo un tamaño de archivo de destino en la configuración de enrutamiento de archivos.

* **Límite de audiencia aumentado**: el límite de audiencia del canal de correo directo se ha aumentado de 3 millones a 100 millones de perfiles, lo que permite dirigirse a audiencias mucho más grandes sin alcanzar los errores de creación de archivos.

### Diseñador de correo electrónico {#sep-26-email-designer}

Las siguientes funcionalidades y mejoras están llegando a Email Designer en esta versión.

<table>
<thead>
<tr>
<th><strong>Compatibilidad con el modo oscuro para variantes de temas de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los temas de correo electrónico ahora admiten el modo oscuro, por lo que cada variante de color puede procesarse con una apariencia adaptada a los destinatarios que ven el correo electrónico en un cliente habilitado para el modo oscuro.</p>
<p>Cuando está habilitada, se genera automáticamente una paleta oscura predeterminada para cada variante y puede personalizarla con una paleta diferente o con sus propios colores personalizados, independientemente del diseño del modo claro, de modo que los cambios realizados en un modo no afectan al otro.</p>
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
</td>
</tr>
</tbody>
</table>

* **Fuentes de reserva para fuentes personalizadas en temas de correo electrónico**: ahora puede definir una fuente de reserva para cualquier fuente personalizada (web) aplicada a través de temáticas de correo electrónico. Si el cliente de correo electrónico de un suscriptor no admite la fuente personalizada, Adobe Journey Optimizer muestra automáticamente la fuente de reserva especificada en lugar de dejar la opción a la fuente predeterminada del cliente de correo electrónico. Esto mantiene la tipografía del correo electrónico más cerca de las directrices de marca y reduce las incoherencias en el procesamiento de fuentes en los clientes de correo electrónico.

### Creación de informes {#sep-26-reporting}

La siguiente funcionalidad se incluye en los informes en esta versión.

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

### Administración {#sep-26-administration}

El siguiente recordatorio se aplica a la administración de en esta versión.

* **Protección de tiempo de vida de conjunto de datos (TTL) — zonas protegidas existentes** - La protección de tiempo de vida (TTL) para conjuntos de datos generados por el sistema de Journey Optimizer (90 días en el almacén de perfiles, 13 meses en el lago de datos) se aplicará en las zonas protegidas de clientes y organizaciones existentes a partir del 1 de octubre de 2026.

### Mejoras de uso {#sep-26-usability}

* **Mejoras de uso en la experiencia de simulación de contenido**: la nueva experiencia de simulación de contenido ahora le permite nombrar y organizar sus variantes para facilitar la comparación, copiar o eliminar detalles de la variante directamente desde cada tarjeta, ver rutas de atributos completas y la configuración de canal por tarjeta bajo demanda, y cargar sus propios perfiles CSV, JSON o JSONL desde un botón de carga más prominente.

* **Calendario unificado para campañas, Recorridos y campañas organizadas**: La vista de calendario para recorridos y campañas ahora se mueve de inventarios separados a un menú unificado, accesible por el carril izquierdo, que muestra ambos en una vista combinada.

