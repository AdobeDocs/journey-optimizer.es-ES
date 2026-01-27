---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 79e9023a9b555a75a13c4f5da2db1b7dbb04c344
workflow-type: tm+mt
source-wordcount: '1726'
ht-degree: 17%

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

**Fecha de la versión**: 27 y 28 de enero de 2026

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican en las notas de la versión en la fecha de lanzamiento.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

### Nuevas funciones {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Horas tranquilas (exclusiones basadas en el tiempo)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las horas tranquilas le permiten definir <strong>exclusiones basadas en el tiempo</strong> para los canales de correo electrónico, SMS, Push y WhatsApp. Garantizan que no se envíen mensajes durante períodos específicos, lo que le ayuda a respetar las preferencias de los clientes y los requisitos de cumplimiento. Puede aplicar horas tranquilas a través de <strong>conjuntos de reglas</strong>, que se pueden asignar a acciones individuales en campañas o recorridos para un control preciso.</p>
<p>Esta función, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general). Con esta versión de Disponibilidad general, la función ahora incluye la capacidad para que los clientes pongan en cola una acción de campaña hasta que se complete el Tiempo de inactividad y la capacidad de previsualizar la regla de Tiempo de inactividad activada.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de correo directo en recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente limitado a campañas, el <strong>canal de correo postal</strong> ya está disponible en el lienzo del recorrido, lo que le permite incorporar el correo postal en sus recorridos. Ahora, el correo postal se puede utilizar en escenarios de recorrido por lotes y 1:1, con compatibilidad con la configuración de extracción de archivos y los ajustes de frecuencia basados en el tiempo.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de correo directo en campañas orquestadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El canal de correo postal ya está disponible en campañas orquestadas. La <strong>actividad de correo postal</strong> facilita el envío de correo postal dentro de su campaña orquestada tanto para mensajes recurrentes como únicos. Automatiza la generación del <strong>archivo de extracción</strong> requerido por los proveedores de correo postal. Puede combinar actividades de canal en el lienzo de campaña orquestado para crear campañas en canales múltiples que almacenen en déclencheur las acciones en función del comportamiento y los datos del cliente.</p>
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
<p>Ahora puede agregar <strong>políticas de decisión</strong> a los recorridos y campañas de SMS. Las políticas de decisión son contenedores para sus ofertas que aprovechan el motor de Decisioning para devolver dinámicamente el mejor contenido para entregar a cada miembro del público.</p>
<p>Esta capacidad está disponible en disponibilidad limitada para un conjunto de organizaciones. Póngase en contacto con su representante de Adobe. </p>
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
<th><strong>Journey Agent: Creación de un Recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent ahora ofrece funcionalidades de creación, lo que permite a los usuarios de Journey Optimizer crear y configurar recorridos de marketing a través de una <strong>interfaz en lenguaje natural</strong>. Los profesionales pueden crear recorridos rápidamente al describir sus necesidades en mensajes de conversación. Esto optimiza el proceso de creación de recorridos, lo que permite a los especialistas en marketing centrarse en la estrategia en lugar de en la configuración técnica.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#jan-26-01-improv}

A continuación, se describen las mejoras incluidas en esta versión.

#### IA

* **Comprobaciones de calidad del contenido del Asistente de IA**: además de la alineación de marca, ahora puede evaluar la <strong>calidad del contenido</strong> en general para descubrir posibles problemas con legibilidad, coherencia y eficacia, independientemente de las directrices de marca. Estas comprobaciones automatizadas ayudan a identificar mensajes poco claros, tonos incoherentes o lagunas estructurales.

* **Actualice las marcas con una nueva ficha de colores**: las directrices de marca garantizan que la marca se presente de manera coherente en todos los puntos de contacto. La nueva <strong>sección Colores</strong> define los estándares para el sistema de colores de su marca y describe cómo se seleccionan, organizan y aplican los colores en todas las experiencias. Garantiza el uso coherente de los colores primarios, secundarios, acentuados y neutros para apoyar una identidad de marca cohesiva, accesible y reconocible.

#### Canales

#### Campañas

* **Programar campaña usando la zona horaria del perfil**. La programación de campañas ahora puede usar la <strong>zona horaria</strong> de cada perfil para enviar mensajes a la hora local prevista.

  **Nota**: esta mejora solo está disponible para un conjunto de organizaciones (disponibilidad limitada).


#### Experience Decisioning

* **Adjuntar fragmentos a elementos de decisión**: Journey Optimizer ahora proporciona la capacidad de adjuntar <strong>fragmentos</strong> a elementos de decisión, que se pueden aprovechar en campañas de experiencia basadas en código mediante directivas de decisión.

  **Nota**: Publicada anteriormente en Disponibilidad limitada, esta mejora ya está disponible para todos los entornos (Disponibilidad general).

#### Recorridos

* **Aprovechar una carga de respuesta de error en Acciones personalizadas de recorrido**. Ahora puede definir una <strong>carga de respuesta de error</strong> opcional para las acciones personalizadas. Cuando falla una llamada, la carga útil del error se expone en el contexto de recorrido y está disponible en la rama de tiempo de espera/error, junto con `jo_status_code`, para admitir una lógica de reserva y una depuración más completas.

* **Combinar acciones de mensajes nativas y de Adobe Campaign**: Journey Optimizer ahora le permite combinar acciones de mensajes de Adobe Campaign v7/v8 con acciones de canal nativo en el mismo recorrido.

* **Validación del tamaño de carga útil de Recorrido en recorrido**: Journey Optimizer ahora valida los tamaños de carga útil de recorrido para ayudar a garantizar un rendimiento óptimo y la estabilidad del sistema. Al crear o publicar recorridos, recibirá advertencias y errores claros si el tamaño de la carga útil se aproxima o supera los límites recomendados, junto con instrucciones procesables para optimizar la configuración del recorrido. Esta validación proactiva le ayuda a identificar problemas potenciales de forma temprana y a mantener el rendimiento del recorrido.

#### Campañas orquestadas

* **Seleccionar atributos y copiar valores de distribución**: ahora puede seleccionar o copiar valores directamente desde la vista de distribución de valores en campañas organizadas.

* **Herencia de etiquetas de uso de datos para audiencias**: las etiquetas aplicadas en Adobe Experience Platform ahora se transfieren automáticamente al guardar audiencias en campañas orquestadas, lo que reduce el etiquetado DULE manual.

* **Filtros de redireccionamiento predefinidos**: para admitir un redireccionamiento más sencillo en los casos de uso de campañas orquestadas, esta versión introduce nuevos <strong>filtros de comentarios de campaña</strong>. Estos filtros le permiten dirigirse directamente a las audiencias en función de la participación en el mensaje, como enviado, abierto solo, abierto o hecho clic, o abierto y hecho clic, y seleccionar la campaña específica o la campaña en transición que desea redireccionar.

* **Filtros predefinidos con parámetros**: ahora puede crear filtros predefinidos con <strong>parámetros</strong> en campañas orquestadas para reglas reutilizables y editables.

* **Confirmación de mensaje antes del envío**: un <strong>paso de confirmación</strong> ahora está habilitado de forma predeterminada antes de enviar campañas orquestadas para reducir los envíos accidentales.

* **Compatibilidad con metadatos generados por el usuario**: la función <strong>executionMetadata helper</strong> ya está disponible en el editor de personalización para campañas orquestadas, lo que le permite adjuntar información contextual a cualquier acción nativa y almacenarla en un conjunto de datos para exportarla a sistemas externos.

* **Botón de reinicio**: las campañas orquestadas ahora incluyen un <strong>botón de reinicio</strong> para que pueda reiniciar rápidamente las ejecuciones cuando sea necesario antes de publicar la campaña.

* **Compatibilidad con control de tarifa**: las campañas orquestadas ahora admiten <strong>control de tarifa</strong> para ayudarle a espaciar las entregas y alinearse con las restricciones de volumen.

#### Permisos

* **Impedir la autoaprobación para recorridos y campañas**: se agregó una opción al crear o establecer la directiva de aprobación para evitar que los creadores de recorridos o campañas aprueben sus propios objetos.

## Próximamente {#jan-26-01-coming-soon}

En los próximos días, está programado el lanzamiento de las siguientes funciones y mejoras. **La información está sujeta a cambios**. Los vínculos, las pantallas y la documentación actualizados se compartirán una vez que estas actualizaciones estén activas en la producción.

<table>
<thead>
<tr>
<th><strong>Exportación de mensajes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Habrá disponible una nueva funcionalidad <strong>Message Export</strong> para canales de correo electrónico y SMS. Esta función le permite exportar automáticamente el contenido de los mensajes enviados a un conjunto de datos de Experience Platform dedicado, lo que le permite:</p>
<ul>
<li>Cumplir los requisitos de cumplimiento normativo (como HIPAA)</li>
<li>Archivar mensajes para reclamaciones legales y consultas de atención al cliente</li>
<li>Conservar copias del contenido personalizado enviado a particulares</li>
</ul>
<p>Los registros se conservan en el conjunto de datos de exportación de mensajes de AJO durante 7 días naturales a partir de la ingesta. Durante este período de retención, puede exportar los datos a su propio almacenamiento a través de destinos de Experience Platform. La función se habilita en el nivel de configuración de canal, lo que le proporciona un control granular sobre los mensajes que se exportan.</p>
<p>Esta funcionalidad solo está disponible para el canal de correo electrónico y SMS, para organizaciones que han adquirido la oferta del complemento Exportación de mensajes. Para obtener más información, contacte con su representante de Adobe.</p>
<p>Fecha de disponibilidad: jueves, 28 de enero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Webhooks de SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Los enlaces web</strong> serán compatibles con todos los proveedores de SMS. Podrá configurar cada webhook en función de su propósito: Webhooks entrantes para capturar mensajes entrantes y webhooks de comentarios para recibir confirmaciones de entrega, actualizaciones de estado y otros eventos relacionados con mensajes.</p>
<p>Fecha de disponibilidad: jueves, 28 de enero de 2026</p>
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
<p>Adobe Journey Optimizer admitirá <strong>notificaciones push web</strong>, lo que expandirá el canal push más allá del móvil. Podrá enviar notificaciones tanto a navegadores móviles como de escritorio, lo que permite llegar a los clientes directamente en sus dispositivos sin necesidad de una aplicación. Esta mejora le ayudará a atraer a los usuarios con mensajes personalizados y oportunos en tiempo real, aprovechando los mismos flujos de trabajo de creación y las mismas capacidades de direccionamiento ya disponibles para las notificaciones push móviles.</p>
<p>Esta funcionalidad, lanzada anteriormente en Beta, estará disponible para todos los entornos (disponibilidad general).</p>
<p>Fecha de disponibilidad: jueves, 28 de enero de 2026</p>
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
<p><strong>Las API de herramientas de migración</strong> estarán disponibles para migrar mediante programación las entidades de Administración de decisiones a Decisioning, que incluyen:</p>
<ul>
<li>Ámbitos de migración flexibles (zona protegida, nivel de oferta o de decisión)</li>
<li>Análisis y validación de dependencias automatizadas</li>
<li>Compatibilidad con reversiones para migraciones completadas</li>
<li>Informes de migración detallados con asignaciones de objetos</li>
</ul>
<p>Fecha de disponibilidad: jueves, 28 de enero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Generación de contenido en Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con tecnología de Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> estará disponible en Journey Optimizer y le permitirá analizar los recorridos a través de una interfaz de lenguaje natural. Podrá generar y administrar contenido específico del canal directamente en Journey Agent, creando contenido para canales como correo electrónico y push, aplicando y previsualizando plantillas, refinando el tono y el estilo a través de mensajes y abriendo contenido en <strong>Content Designer</strong> para la edición en contexto.</p>
<p>Fecha de disponibilidad: martes, 02 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Compatibilidad con decisiones en el canal push</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Podrá personalizar y optimizar el contenido de sus mensajes push con <strong>Decisioning</strong>. Use <strong>puntuaciones de prioridad</strong>, fórmulas o modelos de IA para mostrar el mejor contenido a sus clientes.</p>
<p>Fecha de disponibilidad: miércoles, 03 de febrero de 2026</p>
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
<p>Habrá disponible una nueva <strong>actividad de decisión de contenido</strong> en el lienzo de recorrido para integrar ofertas personalizadas directamente en las recorridos de los clientes. Esta actividad le permite entregar contenido basado en decisiones y hacer referencia a esas ofertas en todo el recorrido, en condiciones para crear ramas basadas en la idoneidad, en acciones personalizadas para pasar datos de ofertas a sistemas externos y en otras actividades para crear experiencias de cliente totalmente personalizadas.</p>
<p>Esta capacidad estará disponible para todos los entornos (disponibilidad general).</p>
<p>Fecha de disponibilidad: miércoles, 03 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>
