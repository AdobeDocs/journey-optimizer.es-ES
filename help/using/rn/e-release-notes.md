---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 9605b5bec688c5afcbcc7b391218cdef6cb3b196
workflow-type: tm+mt
source-wordcount: '2342'
ht-degree: 21%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).


## Notas previas al lanzamiento de enero de 2026 {#jan-26-01-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican en las notas de la versión en la fecha de lanzamiento.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de lanzamiento**: miércoles, 27 de enero de 2026

### Nuevas funciones {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Actividad de acción en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer admite una nueva actividad <strong>Action</strong> genérica que permite configurar acciones únicas y <strong>grupos de acciones entrantes de varias acciones</strong>, lo que permite una configuración de acciones optimizada dentro del lienzo de recorrido. En particular, esta nueva función permite lo siguiente:</p>
<ul>
<li>Una configuración de acción nativa simplificada dentro del lienzo de recorrido.</li>
<li>La capacidad para crear grupos de acciones entrantes de varias acciones.</li>
<li>Capacidad de añadir optimización a cualquier acción de canal integrada.</li>
<li>Capacidad de añadir opciones de experimentación y multilingües a cualquier acción.</li>
</ul>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13290">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">Vínculo a la tarea JIRA del PRODUCTO</a></p>
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
<p>Obtenga información más detallada de insight sobre el estado y el rendimiento de sus puntos finales de acciones personalizadas con un nuevo <strong>tablero de monitorización</strong> y datos de eventos de pasos de recorrido enriquecidos. Rastree las llamadas, los errores, el rendimiento, los tiempos de respuesta y los tiempos de espera de cola correctos para comprender rápidamente cuándo, dónde y por qué se producen anomalías.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13981">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-126869">Vínculo a la tarea JIRA del PRODUCTO</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Horas tranquilas/Exclusiones basadas en el tiempo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las horas tranquilas le permiten definir <strong>exclusiones basadas en el tiempo</strong> para los canales de correo electrónico, SMS, Push y WhatsApp. Garantizan que no se envíen mensajes durante períodos de tiempo específicos, lo que le ayuda a respetar las preferencias de los clientes y los requisitos de cumplimiento. Puede aplicar horas tranquilas a través de <strong>conjuntos de reglas</strong>, que se pueden asignar a acciones individuales en campañas o recorridos para un control preciso.</p>
<p>Esta función, lanzada anteriormente en disponibilidad limitada, ya está disponible para todos los entornos. Con esta versión de Disponibilidad general, la función ahora incluye la capacidad para que el cliente ponga en cola una acción de campaña hasta que se completen las horas tranquilas y la capacidad de previsualizar la regla de horas silenciosas activada.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13986">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-63912">Vínculo a la tarea JIRA del PRODUCTO</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de correo postal en recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente limitado a Campañas, el <strong>canal de correo postal</strong> ya está disponible en el <strong>lienzo de recorrido</strong>, lo que le permite incorporar el correo postal en sus recorridos. Ahora, el correo postal se puede utilizar en escenarios de recorrido por lotes y 1:1, con compatibilidad con la configuración de extracción de archivos y los ajustes de frecuencia basados en el tiempo.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13543">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-38399">Vínculo a la tarea JIRA del PRODUCTO</a></p>
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
<p>Adobe Journey Optimizer ahora admite <strong>notificaciones push web</strong>, lo que expande el canal push más allá del móvil. Puede enviar notificaciones sin problemas a exploradores móviles y de escritorio, lo que permite llegar a los clientes directamente en sus dispositivos sin necesidad de una aplicación. Esta mejora le permite atraer a los usuarios con mensajes personalizados y oportunos en tiempo real, aprovechando los mismos flujos de trabajo de creación y las mismas capacidades de direccionamiento ya disponibles para las notificaciones push móviles.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13581">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-37866">Vínculo a la tarea JIRA del PRODUCTO</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Compatibilidad con decisiones en los canales push y SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede agregar <strong>políticas de decisión</strong> a los recorridos y campañas push y SMS. Las políticas de decisión son contenedores para sus ofertas que aprovechan el motor de Decisioning para devolver dinámicamente el mejor contenido para entregar a cada miembro del público.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13426">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/DOCAC-13425">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55817">Vínculo a la tarea JIRA del PRODUCTO</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55818">Vínculo a la tarea JIRA del PRODUCTO</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de correo directo en campañas organizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El canal de correo postal ya está disponible en campañas orquestadas. La <strong>actividad de correo directo</strong> facilita el envío de correo directo dentro de su campaña orquestada, tanto para mensajes recurrentes como únicos. Sirve para automatizar el proceso de generación del <strong>archivo de extracción</strong> requerido por los proveedores de correo postal. Puede combinar actividades de canal en el lienzo de la campaña orquestada para crear campañas en canales múltiples que puedan activar acciones basadas en el comportamiento y los datos del cliente.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13379">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-82584">Vínculo a la tarea JIRA del PRODUCTO</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuevos conectores de origen para aplicaciones de lealtad</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Hay nuevos <strong>conectores de origen</strong> disponibles en Adobe Experience Platform para las aplicaciones de fidelidad Talon.One, Capillary y Kobie. Estos conectores le permiten transmitir sin problemas datos de lealtad a Adobe Experience Platform y aprovechar estos datos en Journey Optimizer.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13372">Vincular a tarea DOCAC JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Exportación de mensajes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora es posible <strong>exportar envíos enviados</strong> a un conjunto de datos específico para fines de archivado y cumplimiento normativo. Esta capacidad está disponible no solo para correo electrónico, sino también para otros canales, como SMS. La retención de datos para el conjunto de datos de exportación de mensajes ahora es de <strong>7 días</strong>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12915">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105313">Vínculo a la tarea JIRA del PRODUCTO</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nueva API para recuperar campañas de acción</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ya está disponible la nueva <strong>API de Journey Optimizer</strong>, que le permite recuperar e inspeccionar mediante programación datos relacionados con la campaña, como detalles, versiones y configuraciones.</p>
<p>Para obtener más información, consulte la <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">documentación detallada</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13506">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-96195">Vínculo a la tarea JIRA del PRODUCTO</a></p>
<p>Fecha de disponibilidad: martes, 24 de noviembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuevas alertas de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay tres nuevas <strong>alertas de recorrido</strong> disponibles para ayudarle a supervisar y realizar un seguimiento de los eventos de ciclo de vida de recorrido y del rendimiento de las acciones personalizadas:</p>
<ul>
<li><strong>Recorrido publicado</strong>: reciba notificaciones cuando un profesional publique un recorrido en el lienzo de recorrido.</li>
<li><strong>Recorrido finalizado</strong>: obtenga alertas cuando haya finalizado un recorrido, con definiciones específicas basadas en el tipo de recorrido (Leer público o Activado por evento).</li>
<li><strong>Límite de acción personalizada activado</strong>: reciba una notificación cuando se active el límite en un punto final de acción personalizada.</li>
</ul>
<p>Estas alertas se pueden suscribir al nivel de organización o para recorridos específicos.</p>
<p>Para obtener más información, consulte la <a href="../reports/alerts.md#journey-alerts">documentación detallada</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13465">Vincular a tarea DOCAC JIRA</a></p>
<p>Fecha de disponibilidad: jueves, 05 de noviembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temas del Diseñador de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aplicar rápidamente <strong>temas preaprobados</strong> para garantizar la coherencia de la marca en todos los correos electrónicos, acelerar el proceso de creación de campañas y producir correos electrónicos de alta calidad de forma independiente, al tiempo que reduce la dependencia en los equipos de diseño.</p>
<p>Esta funcionalidad, que se publicó anteriormente en la versión Beta, ya está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Para obtener más información, consulte la <a href="../email/apply-email-themes.md">documentación detallada</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12941">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/NEO-88838">Vínculo a la tarea JIRA del PRODUCTO</a></p>
<p>Fecha de disponibilidad: jueves, 05 de noviembre de 2025</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#jan-26-01-improv}

A continuación, se describen las mejoras incluidas en esta versión.

#### IA

* **Comprobaciones de calidad del contenido del Asistente de IA**: además de la alineación de marca, ahora puede evaluar la <strong>calidad del contenido</strong> en general para descubrir posibles problemas con legibilidad, coherencia y eficacia, independientemente de las directrices de marca. Estas comprobaciones automatizadas ayudan a identificar mensajes poco claros, tonos incoherentes o lagunas estructurales.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13917">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-103238">Vínculo a la tarea JIRA del PRODUCTO</a>
* **Actualice las marcas con una nueva ficha de colores**: las directrices de marca garantizan que la marca se presente de manera coherente en todos los puntos de contacto. La nueva <strong>sección Colores</strong> define los estándares para el sistema de colores de su marca y describe cómo se seleccionan, organizan y aplican los colores en todas las experiencias. Garantiza el uso coherente de los colores primarios, secundarios, acentuados y neutros para apoyar una identidad de marca cohesiva, accesible y reconocible.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13811">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-121183">Vínculo a la tarea JIRA del PRODUCTO</a>

#### Campañas

* **Programar campaña usando la zona horaria del perfil**. La programación de campañas ahora puede usar la <strong>zona horaria</strong> de cada perfil para enviar mensajes a la hora local prevista.

  **Nota**: esta mejora solo está disponible para un conjunto de organizaciones (disponibilidad limitada).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-11534">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-43782">Vínculo a la tarea JIRA del PRODUCTO</a>

#### Canales

* **Webhooks de SMS: fase II**: descripción que se debe proporcionar.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13978">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-93914">Vínculo a la tarea JIRA del PRODUCTO</a>

* **Oferta de reventa de WhatsApp** - Descripción que se proporcionará.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13669">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-86420">Vínculo a la tarea JIRA del PRODUCTO</a>

#### Diseñador de correos electrónicos

* **Correcciones in situ en el Diseñador de correo electrónico** - <strong>Las sugerencias de contenido automáticas con tecnología de IA</strong> ya están disponibles en el Designer de correo electrónico cuando se detectan infracciones durante la validación del contenido. Si el contenido se marca como desalineado con las directrices de la marca o falla en los criterios de calidad, el sistema genera de forma proactiva alternativas corregidas que se pueden revisar y aplicar en línea, mejorando el cumplimiento y acelerando la producción.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13979">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95365">Vínculo a la tarea JIRA del PRODUCTO</a>

#### Experience Decisioning

* **arbitraje de Recorridos**: ahora puede usar <strong>fórmulas y modelos de IA</strong> para aumentar automáticamente las puntuaciones de prioridad de recorridos en función de los atributos de perfil del cliente y los factores contextuales, lo que garantiza que los clientes ingresen los recorridos más relevantes.

  **Nota**: esta mejora solo está disponible para un conjunto de organizaciones (disponibilidad limitada).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13976">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-78932">Vínculo a la tarea JIRA del PRODUCTO</a>

* **documentación de herramientas de zona protegida exd - actualizar** - Descripción que se proporcionará.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13596">Vincular a tarea DOCAC JIRA</a>

* **API de herramientas de migración de autoservicio**: hay un nuevo conjunto de <strong>API de herramientas de migración</strong> disponibles para migrar entidades de Administración de ofertas a Experience Decisioning. Las herramientas permiten una migración sin problemas entre entornos limitados con resolución de dependencias y funciones de reversión.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13837">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-109695">Vínculo a la tarea JIRA del PRODUCTO</a>

* **Adjuntar fragmentos a elementos de decisión**: Journey Optimizer ahora proporciona la capacidad de adjuntar <strong>fragmentos</strong> a elementos de decisión que se pueden aprovechar en campañas de experiencia basadas en código mediante directivas de decisión.

  **Nota**: Publicada anteriormente en Disponibilidad limitada, esta mejora ya está disponible para todos los entornos (Disponibilidad general).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13418">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-110282">Vínculo a la tarea JIRA del PRODUCTO</a>

#### Recorridos

* **Aprovechar una carga de respuesta de error en Acciones personalizadas de recorrido**. Ahora puede definir una <strong>carga de respuesta de error</strong> opcional para las acciones personalizadas. Cuando falla una llamada, la carga útil de error se expone en el contexto de recorrido y está disponible en la rama de tiempo de espera/error para admitir una lógica de reserva y una depuración más completas.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13977">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113125">Vínculo a la tarea JIRA del PRODUCTO</a>

* **Combinar acciones de mensajes nativas y de Adobe Campaign**: Journey Optimizer ahora le permite combinar acciones de mensajes de Adobe Campaign v7/v8 con acciones de canal nativo en el mismo recorrido.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13974">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113103">Vínculo a la tarea JIRA del PRODUCTO</a>

* **validación del tamaño de la carga útil de Recorrido en recorrido**: Journey Optimizer ahora proporciona <strong>validación del tamaño de la carga útil</strong> para ayudar a garantizar un rendimiento óptimo y la estabilidad del sistema. Al crear o publicar recorridos, recibirá advertencias y errores claros si el tamaño de la carga útil se aproxima o supera los límites recomendados, junto con instrucciones procesables para optimizar la configuración del recorrido. Esta validación proactiva le ayuda a identificar problemas potenciales de forma temprana y a mantener el rendimiento del recorrido.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13840">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-122236">Vínculo a la tarea JIRA del PRODUCTO</a>

* **Varias acciones entrantes en recorrido**: para simplificar la orquestación de recorrido, ahora puede definir <strong>varias acciones entrantes</strong> en un solo recorrido. Esta capacidad, que antes estaba disponible en las campañas de, le permite ofrecer varias experiencias basadas en código, mensajes en la aplicación, tarjetas de contenido o acciones web en diferentes ubicaciones al mismo tiempo, y cada acción contiene un contenido específico.

  **Nota**: Publicada anteriormente en Disponibilidad limitada, esta mejora ya está disponible para todos los entornos (Disponibilidad general).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13453">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">Vínculo a la tarea JIRA del PRODUCTO</a>

#### Campañas orquestadas

* **Seleccionar atributos y copiar valores de distribución**: ahora puede seleccionar o copiar valores directamente desde la vista de distribución de valores en campañas organizadas.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13973">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105244">Vínculo a la tarea JIRA del PRODUCTO</a>

* **Herencia de etiquetas de uso de datos para audiencias**: las <strong>etiquetas de uso de datos</strong> aplicadas en Adobe Experience Platform ahora se transfieren automáticamente al guardar audiencias en campañas orquestadas, lo que reduce el etiquetado DULE manual.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13972">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-120769">Vínculo a la tarea JIRA del PRODUCTO</a>

* **Filtros de retargeting predefinidos**. Para admitir un retargeting más sencillo en los casos de uso de campañas orquestadas, esta versión introduce nuevos <strong>filtros de retargeting</strong>. Estos filtros le permiten dirigirse directamente a las audiencias en función de la participación en el mensaje, como enviado, abierto solo, abierto o hecho clic, o abierto y hecho clic, y seleccionar la campaña específica o la campaña en transición que desea redireccionar.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13971">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-116701">Vínculo a la tarea JIRA del PRODUCTO</a>

* **Filtros predefinidos con parámetros**: ahora puede crear <strong>filtros con parámetros</strong> en campañas orquestadas para reglas reutilizables y editables.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13970">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-115431">Vínculo a la tarea JIRA del PRODUCTO</a>

* **Confirmación de mensaje antes del envío**: un <strong>paso de confirmación</strong> ahora está habilitado de forma predeterminada antes de enviar campañas orquestadas para reducir los envíos accidentales.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13927">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-87219">Vínculo a la tarea JIRA del PRODUCTO</a>

* **Compatibilidad con metadatos generados por el usuario**: la función <strong>executionMetadata helper</strong> ya está disponible en el editor de personalización para campañas orquestadas, lo que le permite adjuntar información contextual a cualquier acción nativa y almacenarla en un conjunto de datos para exportarla a sistemas externos.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13923">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-112697">Vínculo a la tarea JIRA del PRODUCTO</a>

* **Botón de reinicio**: las campañas orquestadas ahora incluyen un <strong>botón de reinicio</strong> para que pueda reiniciar rápidamente las ejecuciones cuando sea necesario antes de publicar la campaña.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13920">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-106020">Vínculo a la tarea JIRA del PRODUCTO</a>

* **Compatibilidad con control de tarifa**: las campañas orquestadas ahora admiten <strong>control de tarifa</strong> para ayudarle a espaciar las entregas y alinearse con las restricciones de volumen.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13764">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113254">Vínculo a la tarea JIRA del PRODUCTO</a>

#### Permisos

* **Impedir la autoaprobación para recorridos y campañas**: ahora es necesario que los creadores no puedan aprobar sus propios recorridos o campañas, lo que mejora la <strong>separación de tareas</strong> en los flujos de trabajo de aprobación.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13472">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99957">Vínculo a la tarea JIRA del PRODUCTO</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95676">Vínculo a la tarea JIRA del PRODUCTO</a>

## Próximamente {#jan-26-01-coming-soon}

En los próximos días, está programado el lanzamiento de las siguientes funciones y mejoras. **La información está sujeta a cambios**. Los vínculos, las pantallas y la documentación actualizados se compartirán una vez que estas actualizaciones estén activas en la producción.

<table>
<thead>
<tr>
<th><strong>Generación de contenido en Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con tecnología de Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> está disponible en Journey Optimizer y le permite analizar recorridos a través de una interfaz de lenguaje natural. Ahora también puede generar y administrar contenido específico del canal directamente en Journey Agent, creando contenido para canales como correo electrónico y push, aplicando y previsualizando plantillas, refinando el tono y el estilo mediante mensajes y abriendo contenido en Content Designer para la edición en contexto.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13980">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111882">Vínculo a la tarea JIRA del PRODUCTO</a></p>
<p>Fecha de disponibilidad: martes, 02 de febrero de 2026</p>
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
<p>Ahora puede incluir <strong>ofertas personalizadas</strong> en sus recorridos a través de una actividad de decisión de contenido en el lienzo de recorrido y usarlas en actividades de recorrido, incluidas condiciones y acciones personalizadas.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12902">Vincular a tarea DOCAC JIRA</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99223">Vínculo a la tarea JIRA del PRODUCTO</a></p>
<p>Fecha de disponibilidad: martes, 02 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>
