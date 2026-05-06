---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión 2026
description: Notas de la versión de Journey Optimizer 2026
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 65ca94cf-8e17-4a25-90f3-238083f81477
source-git-commit: 70a9be0c253bbed319510058f7f249f5919bf7b8
workflow-type: tm+mt
source-wordcount: '4254'
ht-degree: 46%

---

# Notas de la versión 2026 {#release-notes-2026}

Esta página enumera todas las características y mejoras de [!DNL Journey Optimizer] publicadas en 2026.

## Notas de la versión de marzo de 2026 {#march-26-rn}

Las secciones [Nuevas funcionalidades](#march-26-features) y [Mejoras](#march-26-improv) abarcan funcionalidades que ya están disponibles. <!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in March.-->

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform pre-release notes](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

**Fecha de la versión**: 24 y 25 de marzo de 2026

### Nuevas funciones {#march-26-features}

<table>
<thead>
<tr>
<th><strong>Cifrado de parámetro de URL</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los parámetros de URL en los vínculos de seguimiento y de página de aterrizaje añadidos a los mensajes de correo electrónico ahora se pueden cifrar, lo que proporciona una capa adicional de seguridad para los datos de parámetros confidenciales.</p>
<ul>
<li>Registre y administre claves de cifrado en el registro <strong>Administration</strong> dedicado.</li>
<li>Utilice la nueva función de ayuda Encrypt en expresiones para cifrar datos confidenciales en direcciones URL para los parámetros de consulta que desea proteger en el momento del procesamiento.</li>
</ul>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p><img src="assets/do-not-localize/encrypt-helper.gif"></p>
<p>Para obtener más información, consulte la <a href="../personalization/url-parameter-encryption.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 31 de marzo de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conversión de imágenes en plantillas de contenido de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede convertir imágenes en plantillas de contenido de correo electrónico directamente en Journey Optimizer. Utilice el análisis con tecnología de IA para generar automáticamente plantillas de HTML estructuradas a partir de referencias visuales, lo que reduce significativamente el tiempo de diseño del correo electrónico.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><img src="assets/do-not-localize/image-converter.gif"></p>
<p>Para obtener más información, consulte la <a href="../content-management/image-to-html.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 31 de marzo de 2026</p>
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
<p>Con [!DNL Journey Optimizer], puede capturar atributos de perfil mediante sus páginas de aterrizaje.</p>
<p>Cree, diseñe y administre formularios personalizados adaptados a sus necesidades en función de un conjunto de datos específico. A continuación, puede utilizar estos formularios en páginas de aterrizaje para añadir los atributos de perfil que elija al conjunto de datos definido para cada formulario.</p>
<p>Esta capacidad, que se publicó anteriormente en Disponibilidad limitada para clientes de Estados Unidos y Australia, ya está disponible en todos los entornos (Disponibilidad general).</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>Para obtener más información, consulte la <a href="../landing-pages/lp-forms.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 26 de marzo de 2026.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actividad de prueba en campañas organizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ya está disponible una nueva actividad <strong>Test</strong> en las campañas orquestadas. Esta actividad enruta la ejecución del flujo de trabajo a diferentes ramas en función de condiciones definidas, lo que permite validar la lógica y las configuraciones de la campaña antes de activar los envíos en directo.</p>
<p><img src="../orchestrated/assets/test-1.png"></p>
<p>Para obtener más información, consulte la <a href="../orchestrated/activities/test.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Compatibilidad con la búsqueda de conjuntos de datos en recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una nueva actividad <strong>Búsqueda de conjuntos de datos</strong> en recorrido le permite recuperar dinámicamente datos de conjuntos de datos de registros de Adobe Experience Platform en tiempo de ejecución, lo que le permite acceder a información que no forma parte del perfil o la carga útil de evento, de modo que las interacciones de los clientes sigan siendo relevantes y oportunas.</p>
<p>Publicada anteriormente en Disponibilidad limitada para un conjunto restringido de organizaciones, la actividad Búsqueda de conjuntos de datos en recorrido ahora está disponible para todos los clientes con derecho a [búsqueda de conjuntos de datos](../data/lookup-aep-data.md), mientras permanece en Disponibilidad limitada.</p>
<p><img src="../building-journeys/assets/aep-data-activity.png"></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/dataset-lookup.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>La actividad de acción reemplaza las actividades de recorrido específicas del canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Tras la disponibilidad general de la <strong>actividad de acción</strong> en febrero de 2026, las actividades de canal nativo heredadas (correo electrónico, push, SMS, en la aplicación, web, experiencia basada en código y tarjeta de contenido) en el lienzo de recorrido ya no se utilizan.</p>
<p>Ahora debe utilizar la actividad Acción única para configurar todas las acciones del canal, sustituyendo la necesidad de nodos específicos del canal independientes.</p>
<p>Los recorridos existentes que utilizan actividades de canal heredadas siguen funcionando sin necesidad de realizar cambios ni migraciones.</p>
<p><img src="assets/do-not-localize/action-activity.gif"></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-action.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Editor de HTML avanzado para plantillas de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El modo avanzado de HTML para plantillas de contenido de correo electrónico permite editar el origen de HTML del contenido en el Designer de correo electrónico, añadir expresiones avanzadas (como condiciones) en el origen y alternar entre la vista de HTML y la vista de escritorio sin perder los cambios.</p>
<p>Esta capacidad solo está disponible en plantillas de contenido para el canal de correo electrónico. Actualmente está en disponibilidad limitada: póngase en contacto con su representante de Adobe para obtener acceso.</p>
<p><img src="assets/do-not-localize/expert-mode.gif"/></p>
<p>Para obtener más información, consulte la <a href="../email/email-expert-mode.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 10 de marzo de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integración de modelos de Firefly personalizados y modelos de generación de imágenes de terceros</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permita la integración total de modelos de Firefly estándar y personalizados, junto con modelos de imagen de terceros aprobados, para proporcionar mayor flexibilidad, control y alineación de marca al generar imágenes.</p>
<p>Elija el modelo adecuado para sus necesidades:</p>
<ul><li> <strong>Modelo de Adobe</strong> (con tecnología Firefly Image Model 4) para generar imágenes inmediatamente sin necesidad de configuración adicional</li><li> <strong>Modelo de partner</strong> (con tecnología Gemini 2.5 Flash) para funciones especializadas</li><li><strong>Modelos personalizados</strong> (modelos específicos de la marca entrenados en sus propios recursos) para la generación coherente con la marca que se ajuste con precisión a la identidad, estilo y directrices visuales de la marca.</li></ul>
<p>Para obtener más información, consulte la <a href="../content-management/generative-models.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 2 de marzo de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actividad en directo para iOS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Lleve las experiencias en tiempo real directamente a Lock Screens y Dynamic Island de sus clientes con <strong>iOS Live Activity</strong> en Adobe Journey Optimizer. Proporcione actualizaciones en directo, desde el seguimiento de pedidos y el estado de los vuelos hasta la cuenta atrás de eventos, las puntuaciones en directo y el progreso de los envíos, sin que sea necesario que los usuarios abran la aplicación. Mantenga a su audiencia informada y comprometida exactamente en el momento adecuado, justo donde está.</p>
<p>Esta funcionalidad, que se publicó anteriormente en la versión beta, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../mobile-live/get-started-mobile-live.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 3 de marzo de 2026</p>
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
<p>Con tecnología de <strong>Adobe Experience Platform Agent Orchestrator</strong>, <strong>Journey Agent</strong> está disponible en Journey Optimizer y le permite analizar recorridos a través de una interfaz de lenguaje natural. Ahora también puede generar y administrar contenido específico del canal directamente en Journey Agent, creando contenido para canales como correo electrónico y push, aplicando y previsualizando plantillas, refinando el tono y el estilo mediante mensajes y abriendo contenido en <strong>Content Designer</strong> para la edición en contexto.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html?lang=es" target="_blank">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 4 de marzo de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Supervisión del modelo de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora le permite monitorizar el estado, el estado de formación y el rendimiento de sus modelos de IA de decisiones. Esto le permite verificar el éxito de la formación, solucionar problemas de errores y comprender el impacto en los resultados para seleccionar las mejores ofertas para cada cliente que utiliza IA. Tenga en cuenta que esta capacidad solo está disponible para <strong>Decisioning</strong> (no para los modelos de Administración de decisiones heredados).</p>
<p>Actualmente, esta funcionalidad solo está disponible para <strong>modelos de optimización personalizada</strong> (no para la optimización automática).</p>
<p><img src="assets/do-not-localize/ai-model-observability.gif"/></p>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/ranking/ai-model-observability.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 9 de marzo de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Déclencheur Orquestación de campañas mediante una señal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, las campañas orquestadas se pueden activar mediante una <strong>señal API</strong>. Para configurarlo, configure la campaña de Target como <strong>Activada por una señal</strong>, publíquela y luego actívela mediante una llamada de API. Cualquier parámetro incluido en la llamada de API está disponible como variable dentro de la campaña en ejecución. Tenga en cuenta que las campañas orquestadas activadas por señales siguen siendo <strong>campañas por lotes</strong> y son distintas de las campañas activadas por API.</p>
<p><img src="assets/do-not-localize/oc-triggered.gif"></p>
<p>Para obtener más información, consulte la <a href="../orchestrated/trigger-orchestrated-campaign.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Categoría transaccional en campañas organizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En Campañas orquestadas, ahora puede establecer una actividad de canal en la categoría <strong>Transaccional</strong>. Esto aplica configuraciones de canal transaccional a esa actividad y resulta útil cuando no deben aplicarse reglas comerciales o cuando no se requiere la inclusión de los clientes.</p>
<p><img src="assets/do-not-localize/oc-transactional.gif"></p>
<p>Para obtener más información, consulte la <a href="../orchestrated/activities/channels.md#add">documentación detallada</a>.</p>
<p>Esta capacidad se implementará gradualmente en todas las regiones en los próximos días.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#march-26-improv}

A continuación, se describen las mejoras incluidas en esta versión.

#### Personalización

* **Personalización completa/básica de la dirección URL**: puede personalizar las direcciones URL de destino mediante atributos de perfil (por ejemplo, para el dominio o la ruta). Para habilitar esta capacidad, proporcione a Adobe su lista de dominios aceptados. [Más información](../personalization/personalization-build-expressions.md#where)

  Esta capacidad, que se publicó anteriormente en Disponibilidad limitada para utilizarla en recorrido, ya está disponible en todos los entornos (disponibilidad general).

  Fecha de disponibilidad: 1 de abril de 2026

#### Creación de informes

* **Optimización del tiempo de envío: la ubicación de los controles actualizados y el nuevo informe de alza** - Los controles de Optimización del tiempo de envío (STO) se han reubicado en el menú de configuración Acción. Además, ahora hay disponible un nuevo informe de alza en los informes de Recorrido para medir el impacto de STO en las métricas de rendimiento de la campaña. [Más información](../reports/channel-report-cja.md#optimization-models)

  Fecha de disponibilidad: 27 de marzo de 2026

<!--
* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.

#### Email Designer

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.

* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment.

  **Caution:** When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered—both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.
-->

#### Configuración

<!--* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.-->

* **No se pudo renovar correctamente los certificados de dominio de AJO**. Ahora puede suscribirse para recibir alertas del sistema, ya sea por correo electrónico o en el centro de notificaciones de Journey Optimizer, cuando un certificado de dominio utilizado para la entrega de correo electrónico esté a punto de expirar o ya haya expirado. [Más información](../reports/alerts.md#alert-certificates-renewal-unsuccessful)

  Fecha de disponibilidad: 26 de marzo de 2026

* **Nombre del conjunto de datos de evento de comentarios secundarios de AJO** - Se ha cambiado el nombre del conjunto de datos `AJO Email BCC Feedback Event` a `AJO Secondary Recipient Feedback Event`. El impacto varía según la situación:

   * **Usuarios existentes**: solo se actualiza el nombre para mostrar. El nombre de la tabla subyacente permanece sin cambios.
   * **Nuevos usuarios y zonas protegidas**: Tanto el nombre para mostrar como el nombre de tabla reflejan el nuevo nombre.
   * **Usuarios existentes con zonas protegidas nuevas**: tanto el nombre para mostrar como el nombre de tabla se actualizarán al nuevo nombre.

  >[!NOTE]
  >
  >Los nuevos conjuntos de datos muestran el nuevo nombre inmediatamente. Para los nombres de conjuntos de datos más antiguos, el relleno y la reconciliación avanzan gradualmente y pueden tardar varias semanas en completarse.

  Fecha de disponibilidad: 2 de marzo de 2026


#### Recorridos

* **Acción de actualización de perfil: compatibilidad con varios atributos de perfil**. La actividad de acción **Actualizar perfil** ahora admite la actualización de hasta cinco atributos de perfil en un solo nodo. Anteriormente, cada acción solo podía actualizar un atributo a la vez, lo que requería que varios nodos actualizaran varios atributos. Use el nuevo botón **Actualizar otro campo** para agregar pares de campo/valor adicionales, lo que reduce la complejidad del lienzo y mejora el rendimiento. [Más información](../building-journeys/update-profiles.md)

* **Envío masivo de mensajes salientes en recorridos**: ahora puede programar mensajes de recorridos de Journey Optimizer para que se entreguen en lotes controlados a lo largo del tiempo. [Más información](../building-journeys/send-using-waves.md)

  Esta capacidad, que se publicó anteriormente en Disponibilidad limitada para utilizarla en recorrido, ya está disponible en todos los entornos (disponibilidad general).

  Fecha de disponibilidad: 16 de marzo de 2026

* **Detalles técnicos de pausa y reanudación en recorrido** - Los **detalles técnicos del recorrido** ahora incluyen información adicional de pausa y reanudación: la fecha y hora de la última pausa y reanudación, el nombre para mostrar y el identificador interno del usuario que realizó cada acción, y un conjunto completo de configuraciones de recorrido en pausa como el comportamiento de pausa, la duración máxima de la pausa y el estado de reanudación automática. [Más información](../building-journeys/journey-properties.md)

  Fecha de disponibilidad: 2 de marzo de 2026

#### Toma de decisiones

* **Migración de decisiones — atributos de oferta y contexto** - La asignación de entidad de la API de migración ahora enumera **atributos de oferta** (`migratedofferattributes` en el esquema de elemento de oferta personalizado) y **atributos de contexto** (`migratedcontextattributes` en el esquema del conjunto de datos de migración). [Más información](../experience-decisioning/decisioning-migration-api.md#entity-mapping)

  Fecha de disponibilidad: 31 de marzo de 2026

<!--
## Coming soon {#coming-soon}

The features and improvements below are planned for release later in March/early April. Release dates and scope are **subject to change without prior notice**.


WAITING RELEASE DATE CONFIRMATION * **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.


WAITING RELEASE DATE CONFIRMATION
* **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->


## Notas de la versión de febrero de 2026 {#feb-26-01-rn}

### Nuevas funciones {#feb-26-01-features}


<table>
<thead>
<tr>
<th><strong>arbitraje de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede usar <strong>fórmulas de clasificación</strong> para aumentar automáticamente las puntuaciones de prioridad de recorridos en función de los atributos de perfil del cliente y los factores contextuales, asegurándose de que los clientes ingresen los recorridos más relevantes.</p>
<p><img src="assets/do-not-localize/journey-arbitration-formulas.gif"/></p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../conflict-prioritization/journey-ranking-formulas.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 24 de febrero de 2026</p>
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
<p>Journey Optimizer admite una nueva actividad <strong>Action</strong> genérica que permite configurar tanto acciones únicas como grupos de acciones entrantes de varias acciones, lo que permite una configuración de acciones optimizada dentro del lienzo de recorrido. En particular, esta nueva función permite lo siguiente:</p>
<ul>
<li>Una configuración de acción nativa simplificada dentro del lienzo de recorrido.</li>
<li>La capacidad para crear grupos de acciones entrantes de varias acciones.</li>
<li>Capacidad de añadir optimización a cualquier acción de canal integrada.</li>
<li>La capacidad de añadir opciones de experimentación y multilingües a cualquier acción.</li>
</ul>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-action.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 20 de febrero de 2026</p>
<p><strong>Nota:</strong> Ahora se puede acceder a todos los canales nativos a través de la actividad recorrido de acción. Las actividades heredadas del canal nativo quedarán obsoletas con la versión de marzo. Los recorridos existentes que incluyen acciones heredadas seguirán funcionando tal cual; no se requiere ninguna migración.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Envío de ondas de mensajes salientes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede programar mensajes de campañas de Journey Optimizer o recorridos para que se entreguen en lotes controlados a lo largo del tiempo.</p>
<p>El envío de ondas ofrece las siguientes ventajas:</p>
<ul>
<li>Mejor capacidad de entrega: la propagación envía con el tiempo para ayudar a mantener una sólida reputación del remitente y reducir el riesgo de ser marcado como correo no deseado.</li>
<li>Control de carga: evite saturar los sistemas descendentes (por ejemplo, centros de llamadas, páginas de aterrizaje) limitando la cantidad de mensajes que se emiten a la vez.</li>
<li>Casos de uso de gran volumen y sensibles al tiempo: adecuados para audiencias grandes o cuando necesite controlar el tiempo (por ejemplo, capacidad del centro de llamadas, ampliación u ofertas con límite de tiempo).</li>
</ul>
<p><img src="assets/do-not-localize/waves.gif"/></p>
<p>En <strong>campañas</strong>, esta capacidad está disponible para todos los entornos (disponibilidad general). Para obtener más información, consulte la <a href="../campaigns/send-using-waves.md">documentación detallada</a>.</p>

<p>En <strong>recorridos</strong>, esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada): para obtener acceso, póngase en contacto con su representante de Adobe. Para obtener más información, consulte la <a href="../building-journeys/send-using-waves.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 19 de febrero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Migrar subdominios a delegación personalizada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede migrar subdominios utilizando el modo de delegación CNAME a delegación personalizada directamente desde la interfaz, de modo que pueda cumplir políticas de seguridad más estrictas en línea con las directrices de su empresa sin volver a crear configuraciones de canal.</p>
<p><img src="assets/do-not-localize/subdomain-migration.gif"/></p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../configuration/custom-subdomain-migration.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 19 de febrero de 2026</p>
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
<p>Adobe Journey Optimizer ahora admite <strong>notificaciones push web</strong>, lo que expande el canal push más allá del móvil. Puede enviar notificaciones sin problemas a <strong>exploradores móviles y de escritorio</strong>, lo que permite llegar a los clientes directamente a través de sus dispositivos sin necesidad de una aplicación. Esta mejora le permite atraer a los usuarios con mensajes personalizados y oportunos en tiempo real, aprovechando los mismos flujos de trabajo de creación y las mismas funcionalidades de segmentación ya disponibles para las notificaciones push móviles.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Esta funcionalidad, lanzada anteriormente en Beta, estará disponible para todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../push/push-configuration-web.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 13 de febrero de 2026</p>
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
<p>Ahora hay disponible una nueva <strong>actividad de decisión de contenido</strong> en el lienzo de recorrido para integrar ofertas personalizadas directamente en las recorridos de los clientes. Esta actividad le permite entregar contenido basado en decisiones y hacer referencia a esas ofertas en todo el recorrido: en condiciones para crear ramas basadas en la idoneidad, en acciones personalizadas para pasar datos de ofertas a sistemas externos y en otras actividades para crear experiencias de cliente totalmente personalizadas.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/content-decision.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 10 de febrero de 2026</p>
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
<p>Las API de herramientas de migración ya están disponibles para migrar mediante programación las entidades de <strong>Administración de decisiones</strong> a <strong>Toma de decisiones</strong>, que incluyen:</p>
<ul>
<li>Ámbitos de migración flexibles (zona protegida, nivel de oferta o de decisión)</li>
<li>Análisis y validación de dependencias automatizadas</li>
<li>Compatibilidad con reversiones para migraciones completadas</li>
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
<p>Obtenga información más detallada de insight sobre el estado y el rendimiento de los extremos de las acciones personalizadas con un nuevo tablero de monitorización y datos de eventos de pasos de recorrido enriquecidos. Rastree las llamadas, los errores, el rendimiento, los tiempos de respuesta y los tiempos de espera de cola correctos para comprender rápidamente cuándo, dónde y por qué se producen anomalías.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
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
<p>Ahora puede personalizar y optimizar el contenido de sus mensajes SMS con Decisioning. Utilice puntuaciones de prioridad, fórmulas o modelos de IA para mostrar el mejor contenido a sus clientes.</p>
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

#### Administración de contenido

<!--
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors</strong> section defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity. [Read more](../content-management/brands.md)
-->

* **Usar temáticas para convertir imágenes en plantillas de correo electrónico**: al convertir una imagen en una plantilla de correo electrónico en Journey Optimizer, ahora puede usar una temática como entrada para que el HTML generado siga los parámetros de su marca. El estilo, como el color de fondo, el color del botón, las fuentes, el interlineado, los márgenes y el relleno, se aplica automáticamente, lo que reduce el trabajo de diseño manual y proporciona una plantilla lista para usar con ediciones mínimas. [Más información](../content-management/image-to-html.md)

  Fecha de disponibilidad: 17 de febrero de 2026.

<!--* **Text mode for fragments** - You can now create and manage text versions of your fragments, supporting workflows that rely on plain text content and providing the same flexibility as in email content. [Read more](../content-management/create-fragments.md)-->

#### Diseñador de correo electrónico

* **Sangría de texto**: ahora puede aplicar sangría izquierda personalizable a la primera línea de párrafos de los componentes de texto directamente desde el panel de propiedades. <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. -->Esto mejora la legibilidad del contenido de formato largo, como editoriales y artículos. [Más información](../email/get-started-email-style.md)

  Fecha de disponibilidad: 18 de febrero de 2026.

#### Toma de decisiones

* **Compatibilidad de entrada de Edge con el uso de datos de Adobe Experience Platform en Decisioning**. El uso de datos de Adobe Experience Platform en Decisioning ahora admite casos de uso de entrada perimetral, además de acciones personalizadas y de correo electrónico en recorrido. [Más información](../experience-decisioning/aep-data-exd.md)

  Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

* **Vista previa de decisiones en el canal de experiencia basado en código**: ahora puede obtener una vista previa de los elementos de decisión al configurar Decisioning con el canal de experiencia basada en código. La vista previa está disponible directamente en la interfaz de creación antes de lanzarse. [Más información](../code-based/test-code-based.md#preview-code-based)

  Fecha de disponibilidad: 18 de febrero de 2026

<!--
THIS WAS FINALLY NOT RELEASED IN FEBRUARY

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach fragments to decision items which can be leveraged in code-based experience campaigns through decision policies. [Read more](../experience-decisioning/fragments-decision-policies.md)

  Previously released in Limited Availability, this capability is now available to all environments (General Availability).

  Availability date: February 12, 2026.
-->

#### Personalización

* **Asistente para metadatos de ejecución** - La función de ayuda `executionMetadata` ya está disponible para todos los clientes de Journey Optimizer. Utilícela para anexar dinámicamente información contextual a cualquier acción nativa y capturarla en un conjunto de datos para exportarla a sistemas externos. [Más información](../personalization/functions/helpers.md#execution-metadata)

  Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).

  Fecha de disponibilidad: 20 de febrero de 2026.

#### SMS

* **Webhooks de SMS**: ahora se admiten los webhooks en todos los proveedores de SMS. Puede configurar cada webhook en función de su objetivo: Los webhooks entrantes capturan los mensajes entrantes y los webhooks de comentarios para recibir las confirmaciones de entrega, las actualizaciones de estado y otros eventos relacionados con los mensajes. [Más información](../sms/sms-webhook.md)

  Fecha de disponibilidad: 2 de febrero de 2026.



## Notas de la versión de enero de 2026 {#jan-26-rn}

<!--**Release date**: January 27-28, 2026-->

### Nuevas funciones {#jan-26-01-features}


<table>
<thead>
<tr>
<th><strong>Compatibilidad con decisiones en el canal push</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede personalizar y optimizar el contenido de sus <strong>notificaciones push</strong> con <strong>Decisioning</strong>. Utilice puntuaciones de prioridad, fórmulas o modelos de IA para mostrar el mejor contenido a sus clientes.</p>
<p>Experience Decisioning con notificaciones push requiere una versión específica de Mobile SDK. Antes de implementar esta característica, compruebe <a href="https://developer.adobe.com/client-sdks/home/release-notes" target="_blank">las notas de la versión</a> para identificar la versión requerida y asegúrese de haber actualizado según corresponda. También puede ver todas las versiones de SDK disponibles para su plataforma en <a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions" target="_blank">esta sección</a>.</p>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/create-decision.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 30 de enero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de correo directo en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente limitado a las campañas, el canal de <strong>correo directo</strong> ya está disponible en el lienzo del recorrido, lo que le permite incorporar correo directo a los recorridos. Ahora se puede usar el correo directo en <strong>escenarios de recorrido 1:1 y por lotes</strong>, con compatibilidad con la configuración de extracción de archivos y la configuración de frecuencia basada en el tiempo.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><img src="assets/do-not-localize/dm-journey.gif"/></p>
<p>Para obtener más información, consulte la <a href="../direct-mail/get-started-direct-mail.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: viernes, 29 de enero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Horas tranquilas (exclusiones basadas en el tiempo)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Las horas tranquilas</strong> le permiten definir exclusiones basadas en el tiempo para los canales de correo electrónico, SMS, push y WhatsApp. Garantizan que no se envíen mensajes durante períodos de tiempo específicos, lo que le ayuda a respetar las preferencias de los clientes y los requisitos de cumplimiento. Puede aplicar horas tranquilas a través de <strong>conjuntos de reglas</strong>, que se pueden asignar a acciones individuales en campañas o recorridos para un control preciso.</p>
<p>Esta función, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de disponibilidad general, la función ahora incluye la posibilidad de que el cliente ponga en cola una acción de campaña hasta que se completen las horas tranquilas y también de previsualizar la regla de horas silenciosas activada.</p>
<p><img src="assets/do-not-localize/quiet-hour-ga.gif"/></p>
<p>Para obtener más información, consulte la <a href="../conflict-prioritization/quiet-hours.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: viernes, 29 de enero de 2026</p>
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
<p>Ahora hay disponible una nueva funcionalidad <strong>Exportación de mensajes</strong> para canales de correo electrónico y SMS. Esta función le permite exportar automáticamente el contenido de los mensajes enviados a un conjunto de datos de Experience Platform dedicado, lo que le permite:</p>
<ul>
<li>Cumplir los requisitos de cumplimiento normativo (como HIPAA)</li>
<li>Archivar mensajes para reclamaciones legales y consultas del servicio de atención al cliente</li>
<li>Conservar copias del contenido personalizado enviado a particulares</li>
</ul>
<p>Los registros se conservan en el conjunto de datos de exportación de mensajes de AJO durante 7 días naturales a partir de la ingesta. Durante este período de retención, puede exportarlas a su propio almacenamiento a través de destinos de Experience Platform. La característica se habilita a nivel de configuración de canal, lo que le proporciona <strong>control granular</strong> sobre los mensajes que se exportan.</p>
<p>Esta funcionalidad solo está disponible para el canal de correo electrónico y SMS, para organizaciones que han adquirido la oferta de complemento de Exportación de mensajes. Para obtener más información, contacte con su representante de Adobe.</p>
<p><img src="assets/do-not-localize/message-export.gif"/></p>
<p>Para obtener más información, consulte la <a href="../configuration/message-export.md#message-export">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 28 de enero de 2026</p>
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
<p>El canal de correo directo ya está disponible para campañas orquestadas. La <strong>actividad de correo directo</strong> facilita el envío de correo directo dentro de la campaña orquestada, tanto para mensajes únicos como recurrentes. Sirve para automatizar el proceso de generación del <strong>archivo de extracción</strong> requerido por los proveedores de correo directo. Puede combinar actividades de canal en el lienzo de la campaña orquestada para crear campañas en canales múltiples que puedan activar acciones basadas en el comportamiento y los datos del cliente.</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>Para obtener más información, consulte la <a href="../orchestrated/activities/channels.md#channel">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 28 de enero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: creación de un recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent ahora ofrece funcionalidades de creación, lo que permite a los usuarios de Journey Optimizer crear y configurar recorridos de marketing a través de una <strong>interfaz en lenguaje natural</strong>. Con estas nuevas habilidades, los profesionales pueden crear recorridos rápidamente con solo describir sus necesidades en <strong>indicaciones de conversación</strong>. Esta innovación optimiza el proceso de creación de recorridos, lo que permite a los especialistas en marketing centrarse en la estrategia en lugar de en la configuración técnica.</p>
<p>Para obtener más información, consulte la <a href="../start/ai-features.md#journey-agent">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 12 de enero de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API de recuperación de campaña de acción</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ya está disponible una nueva API de Journey Optimizer, que le permite recuperar e inspeccionar mediante programación <strong>datos relacionados</strong> con la campaña, como detalles, versiones y configuraciones.</p>
<p>Para obtener más información, consulte la <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve" target="_blank">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 24 de noviembre de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temas del diseñador de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aplicar rápidamente <strong>temas aprobados anteriormente</strong> para garantizar la <strong>coherencia de marca</strong> en todos los correos electrónicos, acelerar el proceso de creación de campañas y producir de forma independiente correos electrónicos de alta calidad, mientras que se reduce la dependencia en los equipos de diseño.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>Esta funcionalidad, que se publicó anteriormente en la versión Beta, ya está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../email/apply-email-themes.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 5 de noviembre de 2025</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#jan-26-01-improv}

#### IA

* **Comprobaciones de calidad del contenido del Asistente de IA**: además de la alineación de marca, ahora puede evaluar la <strong>calidad del contenido</strong> general para descubrir posibles problemas con la <strong>legibilidad</strong>, la coherencia y la eficacia, independientemente de las directrices de marca. Estas comprobaciones automatizadas ayudan a identificar mensajes poco claros, tonos incoherentes o lagunas estructurales. [Más información](../content-management/brands-score.md#validate-quality).

  [Descubra esta función en vídeo](https://video.tv.adobe.com/v/3470544/?learn=on).

#### Recorridos

* **Combinar acciones de mensajes nativas y de Adobe Campaign**: Journey Optimizer ahora le permite combinar acciones de mensajes de <strong>las versiones 7 y 8 de Adobe Campaign</strong> con <strong>acciones de canales nativos</strong> en el mismo recorrido. [Más información](../building-journeys/using-adobe-campaign-v7-v8.md)

  Fecha de disponibilidad: miércoles, 27 de enero de 2026.

* **Carga útil de respuesta de error de acción personalizada**: ahora puede definir una <strong>carga útil de respuesta de error</strong> opcional para las acciones personalizadas. Cuando falla una llamada, la carga útil del error se expone en el contexto de recorrido (bajo el nodo errorResponse de la acción) y está disponible en la <strong>rama de tiempo de espera/error</strong>, junto con `jo_status_code`, para admitir una lógica de reserva y una depuración más completas. [Más información](../action/about-custom-action-configuration.md#define-the-message-parameters)

  Fecha de disponibilidad: miércoles, 27 de enero de 2026.

* **Validación del tamaño de la carga útil de Journey en recorridos**: Journey Optimizer ahora valida <strong>los tamaños de carga útil</strong> para ayudar a garantizar un rendimiento óptimo y la estabilidad del sistema. Al crear o publicar recorridos, recibe <strong>advertencias y errores</strong> si el tamaño de la carga útil se acerca o supera los límites recomendados, junto con instrucciones procesables para optimizar la configuración de la recorrido. Esta validación proactiva le ayuda a identificar problemas potenciales de forma temprana y a mantener el rendimiento del recorrido. [Más información](../start/guardrails.md#journey-payload-size)

  Fecha de disponibilidad: miércoles, 27 de enero de 2026.


* **Alertas de recorrido**: hay nuevas <strong>alertas preconfiguradas</strong> disponibles para los recorridos.
   * <strong>Se ha superado la tasa de descarte de perfiles</strong>: la proporción de descartes de perfil para los perfiles introducidos durante los últimos 5 minutos ha superado el límite
   * <strong>Se ha superado la tasa de errores de acciones personalizadas</strong>: la proporción de errores de acciones personalizadas respecto a las llamadas HTTP correctas durante los últimos 5 minutos ha superado el límite
   * <strong>Se ha superado la tasa de errores de perfiles</strong>: la proporción de perfiles erróneos respecto a los perfiles introducidos durante los últimos 5 minutos ha superado el límite

  Para obtener más información, consulte la [documentación detallada](../reports/alerts.md).

  Fecha de disponibilidad: 14 de octubre de 2025.

#### Campañas orquestadas

* **Herencia de etiquetas de uso de datos para públicos**: las etiquetas aplicadas en Adobe Experience Platform ahora se transfieren automáticamente al guardar <strong>público</strong> en campañas orquestadas, lo que reduce el <strong>etiquetado DULE</strong> manual. [Más información](../orchestrated/activities/save-audience.md)

* **Filtros predefinidos con parámetros**: ahora puede crear <strong>filtros predefinidos</strong> con <strong>parámetros</strong> en campañas orquestadas para reglas reutilizables y editables. [Más información](../orchestrated/predefined-filters.md)

* **Seleccionar atributos y copiar valores de distribución**: ahora puede <strong>seleccionar o copiar valores</strong> directamente desde la vista <strong>distribución de valores</strong> en campañas orquestadas. [Más información](../orchestrated/build-query.md)

* **Confirmación de mensaje antes del envío**: se ha habilitado un <strong>paso de confirmación</strong> de forma predeterminada antes de enviar campañas orquestadas para reducir los envíos accidentales. [Más información](../orchestrated/activities/channels.md#confirm-message-sending)

* **Filtros de redireccionamiento predefinidos**: para admitir una resegmentación más sencilla en los casos de uso de campañas orquestadas, esta versión introduce los nuevos <strong>filtros de comentarios de campaña</strong>. Estos filtros le permiten segmentar público destinatario directamente según la <strong>participación del mensaje</strong>, como enviado, abierto solamente, abierto o hecho clic, o abierto y hecho clic, y seleccionar la campaña específica o la campaña en transición que desea redireccionar. [Más información](../orchestrated/retarget.md)

* **Compatibilidad con control de tarifa**: las campañas orquestadas ahora admiten <strong>control de tarifa</strong> para ayudarle a acelerar los envíos y alinearse con las <strong>restricciones de volumen</strong>. [Más información](../orchestrated/activities/channels.md#rate-control)

* **Botón de reinicio**: las campañas orquestadas ahora incluyen un <strong>botón de reinicio</strong> para que pueda <strong>reiniciar ejecuciones</strong> cuando sea necesario antes de publicar la campaña. [Más información](../orchestrated/start-monitor-campaigns.md)

* **Compatibilidad con metadatos generados por el usuario**: <strong>la función de ayuda executionMetadata</strong> ya está disponible en el editor de personalización para campañas orquestadas, lo que le permite adjuntar información contextual a cualquier acción nativa y almacenarla en un conjunto de datos para exportarla a sistemas externos. [Más información](../personalization/functions/helpers.md#execution-metadata)

  Fecha de disponibilidad: miércoles, 27 de enero de 2026.

* **Revertir campañas en vivo al estado de borrador**: ahora puede revertir las campañas orquestadas en vivo al estado de borrador cuando encuentren errores de ejecución o cuando necesite modificar las campañas programadas antes de que comiencen a ejecutarse. Esta opción está disponible hasta que se envía el primer mensaje. [Más información](../orchestrated/start-monitor-campaigns.md#back-to-draft)

#### Campañas

* **Programar campaña con la zona horaria del perfil**: la programación de campañas ahora puede usar la <strong>zona horaria</strong> de cada perfil para enviar mensajes a la hora local prevista. [Más información](../campaigns/campaign-schedule.md)

  **Nota**: esta mejora solo está disponible para un conjunto de organizaciones (disponibilidad limitada).

  Fecha de disponibilidad: miércoles, 27 de enero de 2026.

#### Permisos

* **Evitar la autoaprobación para recorridos y campañas**: se ha añadido una opción al crear o establecer <strong>directivas de aprobación</strong> para evitar que los creadores de recorridos o campañas <strong>aprueben sus propios objetos</strong>. [Más información](../test-approve/approval-policies.md)

  Fecha de disponibilidad: miércoles, 27 de enero de 2026.
