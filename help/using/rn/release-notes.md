---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 68033e08fb57cad65a721540e530cfb7cc884a3b
workflow-type: tm+mt
source-wordcount: '1984'
ht-degree: 28%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] sigue un modelo de envío continuo, lo que permite a Adobe ofrecer nuevas funciones, mejoras y correcciones de forma continua. Este enfoque permite un despliegue escalable y gradual de las funciones para garantizar el rendimiento y la estabilidad en todos los entornos.

Debido a este modelo, las notas de la versión se actualizan entre versiones mensuales. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Notas previas al lanzamiento de enero de 2026 {#latest-rn}

**Fecha de lanzamiento**: miércoles, 27 de enero de 2026

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican en las notas de la versión en la fecha de lanzamiento.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

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
<p><strong>Nota</strong>: No se admiten horas tranquilas en las campañas orquestadas.</p>
<p>Esta función, lanzada anteriormente en disponibilidad limitada, ya está disponible para todos los entornos. Con esta versión de Disponibilidad general, la función ahora incluye la capacidad para que el cliente ponga en cola una acción de campaña hasta que se completen las horas tranquilas y la capacidad de previsualizar la regla de horas silenciosas activada.</p>
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
<p><strong>Nota</strong>: las notificaciones silenciosas aún no son compatibles con las notificaciones push web.</p>
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
<p>Ahora hay disponible una nueva funcionalidad <strong>Message Export</strong> para canales de correo electrónico y SMS. Esta función le permite exportar automáticamente el contenido de los mensajes enviados a un conjunto de datos de Experience Platform dedicado, lo que le permite:</p>
<ul>
<li>Cumplir los requisitos de cumplimiento normativo (como HIPAA)</li>
<li>Archivar mensajes para reclamaciones legales y consultas de atención al cliente</li>
<li>Conservar copias del contenido personalizado enviado a particulares</li>
</ul>
<p>Los registros se conservan en el conjunto de datos de exportación de mensajes de AJO durante <strong>7 días naturales desde la ingesta</strong>. Durante este período de retención, puede exportar los datos a su propio almacenamiento a través de destinos de Experience Platform. La función se habilita en el nivel de configuración de canal, lo que le proporciona un control granular sobre los mensajes que se exportan.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: Creación de un Recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Recorrido Crear agente permite a los usuarios de Journey Optimizer crear y configurar recorridos de marketing mediante una interfaz de lenguaje natural. Con Recorrido Crear agente, los profesionales pueden crear recorridos rápidamente al describir sus necesidades en mensajes de conversación. El agente optimiza la creación de recorridos, lo que permite a los especialistas en marketing centrarse en la estrategia en lugar de en la configuración técnica.</p>
<p><a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">Más información</a></p>
<p>Fecha de disponibilidad: martes, 12 de enero de 2026</p>
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
<p>Fecha de disponibilidad: jueves, 05 de noviembre de 2025</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#jan-26-01-improv}

A continuación, se describen las mejoras incluidas en esta versión.

#### IA

* **Comprobaciones de calidad del contenido del Asistente de IA**: además de la alineación de marca, ahora puede evaluar la <strong>calidad del contenido</strong> en general para descubrir posibles problemas con legibilidad, coherencia y eficacia, independientemente de las directrices de marca. Estas comprobaciones automatizadas ayudan a identificar mensajes poco claros, tonos incoherentes o lagunas estructurales.

* **Actualice las marcas con una nueva ficha de colores**: las directrices de marca garantizan que la marca se presente de manera coherente en todos los puntos de contacto. La nueva <strong>sección Colores</strong> define los estándares para el sistema de colores de su marca y describe cómo se seleccionan, organizan y aplican los colores en todas las experiencias. Garantiza el uso coherente de los colores primarios, secundarios, acentuados y neutros para apoyar una identidad de marca cohesiva, accesible y reconocible.

#### Campañas

* **Programar campaña usando la zona horaria del perfil**. La programación de campañas ahora puede usar la <strong>zona horaria</strong> de cada perfil para enviar mensajes a la hora local prevista. La programación mediante zonas horarias de perfil está disponible para los canales Email, Push, SMS, WhatsApp y LINE.

  **Nota**: esta mejora solo está disponible para un conjunto de organizaciones (disponibilidad limitada).


#### Experience Decisioning

* **API de herramientas de migración de autoservicio**: hay un nuevo conjunto de <strong>API de herramientas de migración</strong> disponibles para migrar entidades de Administración de ofertas a Experience Decisioning. Las herramientas permiten una migración sin problemas entre entornos limitados con resolución de dependencias y funciones de reversión.

* **Adjuntar fragmentos a elementos de decisión**: Journey Optimizer ahora proporciona la capacidad de adjuntar <strong>fragmentos</strong> a elementos de decisión que se pueden aprovechar en campañas de experiencia basadas en código mediante directivas de decisión.

  **Nota**: Publicada anteriormente en Disponibilidad limitada, esta mejora ya está disponible para todos los entornos (Disponibilidad general).

#### Recorridos

* **Aprovechar una carga de respuesta de error en Acciones personalizadas de recorrido**. Ahora puede definir una <strong>carga de respuesta de error</strong> opcional para las acciones personalizadas. Cuando falla una llamada, la carga útil de error se expone en el contexto de recorrido y está disponible en la rama de tiempo de espera/error para admitir una lógica de reserva y una depuración más completas.

* **Combinar acciones de mensajes nativas y de Adobe Campaign**: Journey Optimizer ahora le permite combinar acciones de mensajes de Adobe Campaign v7/v8 con acciones de canal nativo en el mismo recorrido.

* **validación del tamaño de la carga útil de Recorrido en recorrido**: Journey Optimizer ahora proporciona <strong>validación del tamaño de la carga útil</strong> para ayudar a garantizar un rendimiento óptimo y la estabilidad del sistema. Al crear o publicar recorridos, recibirá advertencias y errores claros si el tamaño de la carga útil se aproxima o supera los límites recomendados, junto con instrucciones procesables para optimizar la configuración del recorrido. Esta validación proactiva le ayuda a identificar problemas potenciales de forma temprana y a mantener el rendimiento del recorrido.

* **Varias acciones entrantes en recorrido**: para simplificar la orquestación de recorrido, ahora puede definir <strong>varias acciones entrantes</strong> en un solo recorrido. Esta capacidad, que antes estaba disponible en las campañas de, le permite ofrecer varias experiencias basadas en código, mensajes en la aplicación, tarjetas de contenido o acciones web en diferentes ubicaciones al mismo tiempo, y cada acción contiene un contenido específico.

  **Nota**: Publicada anteriormente en Disponibilidad limitada, esta mejora ya está disponible para todos los entornos (Disponibilidad general).

#### Campañas orquestadas

* **Seleccionar atributos y copiar valores de distribución**: ahora puede seleccionar o copiar valores directamente desde la vista de distribución de valores en campañas organizadas.

* **Herencia de etiquetas de uso de datos para audiencias**: las <strong>etiquetas de uso de datos</strong> aplicadas en Adobe Experience Platform ahora se transfieren automáticamente al guardar audiencias en campañas orquestadas, lo que reduce el etiquetado DULE manual.

* **Filtros de retargeting predefinidos**. Para admitir un retargeting más sencillo en los casos de uso de campañas orquestadas, esta versión introduce nuevos <strong>filtros de retargeting</strong>. Estos filtros le permiten dirigirse directamente a las audiencias en función de la participación en el mensaje, como enviado, abierto solo, abierto o hecho clic, o abierto y hecho clic, y seleccionar la campaña específica o la campaña en transición que desea redireccionar.

* **Filtros predefinidos con parámetros**: ahora puede crear <strong>filtros con parámetros</strong> en campañas orquestadas para reglas reutilizables y editables.

* **Confirmación de mensaje antes del envío**: un <strong>paso de confirmación</strong> ahora está habilitado de forma predeterminada antes de enviar campañas orquestadas para reducir los envíos accidentales.

* **Compatibilidad con metadatos generados por el usuario**: la función <strong>executionMetadata helper</strong> ya está disponible en el editor de personalización para campañas orquestadas, lo que le permite adjuntar información contextual a cualquier acción nativa y almacenarla en un conjunto de datos para exportarla a sistemas externos.

* **Botón de reinicio**: las campañas orquestadas ahora incluyen un <strong>botón de reinicio</strong> para que pueda reiniciar rápidamente las ejecuciones cuando sea necesario antes de publicar la campaña.

* **Compatibilidad con control de tarifa**: las campañas orquestadas ahora admiten <strong>control de tarifa</strong> para ayudarle a espaciar las entregas y alinearse con las restricciones de volumen.

#### Permisos

* **Impedir la autoaprobación para recorridos y campañas**: ahora es necesario que los creadores no puedan aprobar sus propios recorridos o campañas, lo que mejora la <strong>separación de tareas</strong> en los flujos de trabajo de aprobación.

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
<p>Esta capacidad estará disponible para todos los entornos (disponibilidad general).</p>
<p>Fecha de disponibilidad: miércoles, 03 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>
