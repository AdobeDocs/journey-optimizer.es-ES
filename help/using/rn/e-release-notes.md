---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 86bd616a9331c5225c78ccf52c5d26a063fa8654
workflow-type: tm+mt
source-wordcount: '2080'
ht-degree: 29%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).


## Enero &#39;26 pre-Notas de la versión {#jan-26-01-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican en las notas de la versión en la fecha de lanzamiento.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de lanzamiento**: martes, 26 de enero de 2026

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
<th><strong>Supervisión de acciones personalizadas</strong><br/></th>
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
<p>Las horas de silencio le permiten definir <strong>exclusiones basadas en el tiempo para los</strong> canales de correo electrónico, SMS, push y WhatsApp. Garantizan que no se envíen mensajes durante períodos de tiempo específicos, lo que le ayuda a respetar las preferencias del cliente y los requisitos de cumplimiento. Puede aplicar horas de silencio a través <strong>de conjuntos</strong> de regla, que se pueden asignar a acciones individuales en campañas o viajes para un control preciso.</p>
<p>Esta característica, que anteriormente se publicaba en disponibilidad limitada, ahora está disponible en todos los entornos. Con esta versión de disponibilidad general, la función ahora incluye la capacidad para que el cliente cola una acción campaña hasta la finalización de las horas de silencio y la capacidad de previsualización el regla de horas de silencio activado.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>La canal del correo directo en los viajes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente limitada a Campañas, la <strong>canal</strong> Correo directo ahora está disponible en el lienzo<strong> del </strong>viaje, lo que le permite incorporar Correo Directo en sus viajes. Direct Mail ahora se puede usar en escenarios de viaje por lotes y 1:1, con compatibilidad con la configuración de extracción de archivos y ajustes de Frecuencia basados en el tiempo.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Notificaciones push web canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Systems Journey Optimizer ahora admite <strong>notificaciones</strong> Web Push, ampliando el canal push más allá del móvil. Puede enviar notificaciones sin problemas a navegadores móviles y escritorio, lo que le permite llegar a los clientes directamente en su dispositivos sin necesidad de una aplicación. Esta mejora le permite atraer a los usuarios con mensajes personalizados y oportunos en tiempo real, aprovechando los mismos flujos de trabajo de creación y las mismas capacidades de direccionamiento ya disponibles para las notificaciones push móviles.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mensajería básica de RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con el nuevo complemento <strong>RCS Basic</strong>, ahora puede ofrecer servicios básicos de comunicaciones enriquecidas (RCS) de mensajería en Journey Optimizer, lo que permite las siguientes funciones mejoradas de mensajería sujetas a la asistencia del proveedor y del operador:</p>
<ul>
<li>Compatibilidad con remitentes de marca y verificados: envía mensajes utilizando perfiles comerciales verificados con elementos de promoción de la marca (logotipo, nombre del remitente, etc.).</li>
<li>Información sobre el envío de mensajes: se reciben informes de envío detallados que incluyen actualizaciones del estado del mensaje (por ejemplo, enviado, entregado, leído).</li>
<li>Seguimiento de vínculos: incrusta y rastrea direcciones URL en mensajes RCS para el análisis de participación.</li>
<li>Reserva de SMS: recurre automáticamente a los SMS cuando el dispositivo del perfil no sea compatible con RCS o no se pueda acceder temporalmente mediante RCS.</li>
<li>Composición básica de mensajes: envía mensajes RCS básicos basados en texto.</li>
</ul>
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
<th><strong>correo postal canal en campañas orquestadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>correo postal canal ahora está disponible en campañas orquestadas. La <strong>correo postal actividad</strong> facilita correo directo envío dentro de su campaña orquestado, tanto para mensajes únicos como recurrentes. Sirve para automatizar el proceso de generación <strong>del archivo</strong> extracción requerido por los proveedores de correo directo. Puede combinar actividades de canal en el lienzo de la campaña orquestada para crear campañas en canales múltiples que puedan activar acciones basadas en el comportamiento y los datos del cliente.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Formularios personalizados de página de aterrizaje</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con Journey Optimizer, ahora puede capturar <strong>atributos de perfil</strong> a través de sus páginas de aterrizaje. Cree, diseñe y administre <strong>formularios personalizados</strong> adaptados a sus necesidades en función de un conjunto de datos específico. A continuación, puede utilizar estos formularios en páginas de aterrizaje para añadir los atributos de perfil que elija al conjunto de datos definido para cada formulario.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
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
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Enviar mensaje exportación</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora es posible exportar las <strong>entregas</strong> enviadas a un conjunto de datos específico, con fines de archivo y cumplimiento. Esta capacidad está disponible no solo para correo electrónico, sino también para otros canales como SMS. La retención de datos para el conjunto de datos de exportación de mensajes es ahora <strong>de 7 días</strong>.</p>
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
<p>Ya están disponibles tres nuevas <strong>alertas de viaje para ayudarle a monitor y realizar un seguimiento de los eventos del ciclo de vida del recorrido y el rendimiento de</strong> las acciones personalizadas:</p>
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
* **Actualice las marcas con una nueva ficha de colores**: las directrices de marca garantizan que la marca se presente de manera coherente en todos los puntos de contacto. La nueva <strong>sección</strong> Colores define los estándares para el sistema de color de su marca y describe cómo se seleccionan, organizan y aplican los colores a través de las experiencias. Asegura un uso consistente de colores primarios, secundarios, de acento y neutros para apoyar una identidad de marca cohesiva, accesible y reconocible.

#### Campañas

* **Programar Campaign utilizando la zona** horaria del perfil: Campaign programación ahora puede usar la zona horaria de <strong>cada perfil</strong> para entregar mensajes a la hora local deseada.

  **Nota**: Esta mejora solo está disponible para un conjunto de organizaciones (disponibilidad limitada).

#### Canales

* **Webhooks SMS: Fase II** - Descripción a proporcionar.

* **Oferta** de reventa de WhatsApp: Descripción debe proporcionarse.

#### Diseñador de correos electrónicos

* **Correcciones in situ en el Diseñador** de correo electrónico: <strong>las sugerencias</strong> de contenido automática impulsadas por IA ahora están disponibles en el Diseñador de correo electrónico cuando se detectan infracciones durante contenido validación. Si contenido se marca como desalineado con marca directrices o no cumple con los criterios de calidad, el sistema genera de manera proactiva alternativas corregidas que se pueden revisar y aplicar en línea, mejorando el cumplimiento y acelerando la producción.

#### Toma de decisiones de experiencia

* **arbitraje de Recorridos**: ahora puede usar <strong>fórmulas y modelos de IA</strong> para aumentar automáticamente las puntuaciones de prioridad de recorridos en función de los atributos de perfil del cliente y los factores contextuales, lo que garantiza que los clientes ingresen los recorridos más relevantes.

  **Nota**: esta mejora solo está disponible para un conjunto de organizaciones (disponibilidad limitada).

* **documentación de herramientas de zona protegida exd - actualizar** - Descripción que se proporcionará.

* **API de herramientas de migración de autoservicio**: hay un nuevo conjunto de <strong>API de herramientas de migración</strong> disponibles para migrar entidades de Administración de ofertas a Experience Decisioning. Las herramientas permiten una migración sin problemas entre entornos limitados con resolución de dependencias y funciones de reversión.

* **Adjuntar fragmentos a elementos de decisión**: Journey Optimizer ahora proporciona la capacidad de adjuntar <strong>fragmentos</strong> a elementos de decisión que se pueden aprovechar en campañas de experiencia basadas en código mediante directivas de decisión.

  **Nota**: Esta mejora, que antes se publicaba en disponibilidad limitada, ahora está disponible para todos los entornos (disponibilidad general).

#### Recorridos

* **Aprovechamiento de una carga útil de respuesta a errores en el recorrido Acciones personalizadas**: ahora puede definir una carga<strong> útil de respuesta de error opcional </strong>para las acciones personalizadas. Cuando se produce un error en una llamada, la carga útil de error se expone en el contexto del recorrido y está disponible en el Rama de tiempo de espera / error para admitir una lógica de reserva y una depuración más ricas.

* **Combinación de acciones** de mensajes nativa y Adobe Campaign: Journey Optimizer ahora le permite combinar acciones de mensajes Adobe Campaign v7/v8 con acciones de nativa canal en el mismo recorrido.

* **Tamaño de la carga útil de viaje validación en los viajes** : Journey Optimizer ahora proporciona <strong>validación</strong> de tamaño de carga útil para ayudar a garantizar un rendimiento óptimo y la estabilidad del sistema. Al crear o publicar viajes, recibirá advertencias y errores claros si los tamaños de carga útil se acercan o exceden los límites recomendados, junto con una guía procesable para optimizar la configuración de su viaje. Este validación proactivo le ayuda a identificar posibles problemas de forma temprana y a mantener el rendimiento del recorrido.

* **Varias acciones entrantes en los recorridos: para simplificar la organización del recorrido, ahora puede definir** varias acciones<strong> entrantes</strong> en un solo viaje. Anteriormente disponible en campañas, esta capacidad le permite entregar varias experiencias basadas en código, mensajes en la aplicación, tarjetas de contenido o acciones web a diferentes ubicaciones al mismo tiempo, cada acción con un contenido específico.

  **Nota**: Esta mejora, que antes se publicaba en disponibilidad limitada, ahora está disponible para todos los entornos (disponibilidad general).

#### Campañas orquestadas

* **Seleccionar atributos y copiar valores** de distribución: ahora puede seleccionar o copiar valores directamente desde la distribución de valores vista en campañas orquestadas.

* **Herencia de etiquetas de uso de datos para audiencias**: las <strong>etiquetas de uso de datos</strong> aplicadas en Adobe Experience Platform ahora se transfieren automáticamente al guardar audiencias en campañas orquestadas, lo que reduce el etiquetado DULE manual.

* **Filtros de retargeting predefinidos**. Para admitir un retargeting más sencillo en los casos de uso de campañas orquestadas, esta versión introduce nuevos <strong>filtros de retargeting</strong>. Estos filtros le permiten dirigirse directamente a las audiencias en función de la participación en el mensaje, como enviado, abierto solo, abierto o hecho clic, o abierto y hecho clic, y seleccionar la campaña específica o la campaña en transición que desea redireccionar.

* **Filtros predefinidos con parámetros**: ahora puede crear <strong>filtros con parámetros</strong> en campañas orquestadas para reglas reutilizables y editables.

* **Confirmación de mensaje antes del envío**: un <strong>paso de confirmación</strong> ahora está habilitado de forma predeterminada antes de enviar campañas orquestadas para reducir los envíos accidentales.

* **Compatibilidad con metadatos generados por el usuario**: la función <strong>executionMetadata helper</strong> ya está disponible en el editor de personalización para campañas orquestadas, lo que le permite adjuntar información contextual a cualquier acción nativa y almacenarla en un conjunto de datos para exportarla a sistemas externos.

* **Reiniciar botón**: las campañas orquestadas ahora incluyen un botón<strong> de </strong>reinicio para que pueda volver a ejecutar rápidamente iniciar cuando sea necesario antes de publicar el campaña.

* **Compatibilidad** con el control de tasas: las campañas orquestadas ahora admiten <strong>el control</strong> de tasas para ayudarle a ajustar el ritmo de las entregas y alinearse con las restricciones de volumen.

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
<p>Con tecnología de Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> está disponible en Journey Optimizer y le permite analizar recorridos a través de una interfaz de lenguaje natural. Ahora también puede generar y administrar contenido específicos de canal directamente en Journey Agent, creando contenido para canales como correo electrónico y push, aplicando y previsualizando plantillas, refinando el tono y el estilo a través de mensajes y abriendo contenido en Content Designer para edición en contexto.</p>
<p>Fecha de disponibilidad: martes, 02 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisión de contenido actividad</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede incluir <strong>ofertas</strong> personalizadas en sus recorridos a través de un actividad de decisión de contenido específico en el lienzo del recorrido y utilizarlas en las actividades del recorrido, incluidas las condiciones y las acciones personalizadas.</p>
<p>Fecha de disponibilidad: martes, 02 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>
