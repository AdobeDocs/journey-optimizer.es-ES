---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 7284814029465a8806b78640b8ffe6c44ad030a7
workflow-type: tm+mt
source-wordcount: '3902'
ht-degree: 16%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las capacidades existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] sigue un modelo de envío continuo, lo que permite a Adobe ofrecer nuevas funciones, mejoras y correcciones de forma continua. Este enfoque permite un despliegue escalable y gradual de las funciones para garantizar el rendimiento y la estabilidad en todos los entornos.

Debido a este modelo, las notas de la versión se actualizan entre versiones mensuales. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Notas de la versión preliminar de abril de 2026 {#april-26-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican en las notas de la versión en la fecha de lanzamiento.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

Las nuevas funciones y mejoras publicadas a principios de abril se anuncian con su fecha de disponibilidad.

**Fecha de publicación**: 28 y 29 de abril de 2026

### Nuevas funciones {#april-26-features}

<table>
<thead>
<tr>
<th><strong>simulación de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede establecer su recorrido en <strong>Simulación</strong>. Este modo le permite validar su lógica usando <strong>usuarios simulados</strong>. Son perfiles temporales creados específicamente para la simulación, lo que le permite realizar pruebas libremente sin necesidad de administrar perfiles de prueba persistentes en Adobe Experience Platform.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Parámetros de remitente en el encabezado del correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con Journey Optimizer, ahora puede enviar correos electrónicos donde la entidad transmisora (Remitente) difiera de la entidad creadora (De). Los clientes de correo electrónico que admitan esta función generalmente la representan como "Remitente en nombre de Desde" o muestran un indicador "a través de". Rellene los campos <strong>Encabezados de remitente</strong> opcionales en la configuración del canal de correo electrónico para configurar esta capacidad.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campo CC en la configuración del canal de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede configurar un campo CC (copia de carbón) opcional en la configuración del canal de correo electrónico. A diferencia de CCO, los destinatarios de CC son visibles para el destinatario principal, lo que permite una comunicación transparente y una propiedad más clara.</p>
<p>Esto le permite copiar automáticamente la parte interesada correcta en cada mensaje, como un administrador de relaciones o un propietario de cuenta, al tiempo que se garantiza que el cliente sepa con quién ponerse en contacto para realizar el seguimiento.</p>
<p>El campo CC admite la personalización, de modo que una sola configuración puede enrutar copias de forma dinámica en función de los datos de perfil, lo que las hace escalables en varios casos de uso sin necesidad de una configuración adicional.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vínculos profundos en el Designer de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora es posible añadir vínculos profundos al contenido del correo electrónico a través de una opción específica en la Designer de correo electrónico. Esto garantiza que los usuarios sean llevados directamente al contenido correcto en la aplicación, en lugar de ser redirigidos a navegadores o tiendas de aplicaciones, preservando el contexto y la participación.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integración del agente de Journey Optimizer AI mediante MCP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ahora proporciona un servidor <strong>MCP (Model Context Protocol)</strong> que muestra las operaciones de campaña, lealtad, configuración de canal y zona protegida directamente dentro de cualquier aplicación compatible con MCP. Con esta integración, diferentes personas pueden colaborar en torno a los mismos datos de orquestación. En lugar de escribir consultas contra la API de REST de Adobe Journey Optimizer o navegar por varias pantallas de interfaz de usuario, puede describir su intención de forma conversacional y permitir que el LLM invoque las herramientas de MCP adecuadas. Actualmente, esta funcionalidad está disponible en Claude Web y Desktop.</p>
<p>Esta capacidad está disponible para todos los clientes en Public Beta.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Copiar campañas orquestadas en entornos limitados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La herramienta de zona protegida ahora admite el empaquetado y la copia de campañas orquestadas de una zona protegida a otra. Esto elimina la necesidad de reconstruir manualmente las campañas en cada entorno. Cuando se empaqueta una campaña, sus objetos dependientes principales, como las políticas de combinación y los mensajes, se incluyen automáticamente, de modo que la campaña importada llega lista para configurarse y validarse. Para proteger los entornos de producción, todas las campañas importadas se colocan en estado de borrador en la zona protegida de Target, lo que proporciona a los equipos un paso de revisión y aprobación antes de que cualquier campaña se ponga en marcha.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actividad de consulta incremental en campañas organizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Las campañas orquestadas</strong> ahora admiten una actividad de <strong>Consulta incremental</strong> que se dirige únicamente a perfiles o eventos que son recién elegibles desde la última ejecución.

Esto mantiene las campañas recurrentes centradas en nuevas audiencias de red (nuevos registros, miembros de fidelidad recién calificados y segmentos similares), al tiempo que reduce las cargas de trabajo de consultas y evita envíos redundantes a lo largo del tiempo.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Arbitraje de recorrido: modelos de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede usar <strong>modelos de IA</strong> en sus fórmulas de clasificación para aumentar automáticamente las puntuaciones de prioridad de recorrido en función de atributos de perfil del cliente y factores contextuales, asegurándose de que los clientes ingresen los recorridos más relevantes.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integración de Adobe Express</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La <b>integración de Adobe Express</b> en Adobe Journey Optimizer le permite utilizar las herramientas de edición de Adobe Express directamente durante la creación de contenido, lo que le permite cambiar el tamaño, eliminar fondos, recortar y convertir recursos a JPEG o PNG.
</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p><img src="assets/do-not-localize/express_resize.gif"></p>
<p>Para obtener más información, consulte la <a href="../integrations/express.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 23 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Optimización del correo electrónico para bandejas de entrada AI</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ahora incluye una nueva funcionalidad que garantiza que los correos electrónicos estén estructurados de forma óptima para bandejas de entrada con tecnología de IA como Apple Intelligence y Google Gemini en Gmail.</p>
<p>A medida que los asistentes de IA controlan cada vez más la forma en que los destinatarios leen y actúan en el correo electrónico, esta función le ayuda a generar y crear contenido que se comporta bien en las tareas de IA descendentes, incluidas las de resumen, clasificación, priorización y extracción por intención.</p>
<p><img src="assets/do-not-localize/optimize-for-ai.gif"></p>
<p>Para obtener más información, consulte <a href="../email/llm-email-optimizer.md">Optimizar correo electrónico para bandejas de entrada de IA</a>.</p>
<p>Fecha de disponibilidad: 17 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Asistente de IA para expresiones Personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] ahora incluye <strong>Asistente de IA</strong> directamente en el editor de personalización que convierte los mensajes en lenguaje natural en expresiones de personalización válidas y lógica condicional, no se requiere experiencia en sintaxis. Describa la personalización que desea lograr y la IA generará un código listo para usar que puede aplicar inmediatamente o perfeccionar mediante mensajes de seguimiento.</p>
<p>El ayudante también trabaja a la inversa. Seleccione cualquier expresión existente y pídale que explique la lógica, identifique problemas o sugiera mejoras. Esto lo hace útil no solo para crear nuevas expresiones, sino para revisar y depurar las existentes en todo el equipo.</p>
<p><img src="assets/do-not-localize/assistant-perso.gif"></p>
<p>Para obtener más información, consulte <a href="../content-management/generative-personalization-expressions.md">Asistente de IA para expresiones Personalization</a>.</p>
<p>Fecha de disponibilidad: 13 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentación de ruta de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use el nuevo nodo <strong>Optimize</strong> para ejecutar pruebas A/B o experimentos de bandidos multibrazo a fin de determinar la mejor ruta para cumplir con los KPI centrados en la empresa. Esta herramienta le permite probar y variar, así como personalizar las comunicaciones, la secuencia y el tiempo para llegar mejor a sus clientes.
</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Como parte de General Availability, esta versión incluye la selección de <strong>tipo de experimento</strong> (bandido A/B o multibrazo) y <strong>Escalar el ganador</strong> para recorridos unitarios.</p>
<p><img src="assets/do-not-localize/optimize-experiment.gif"></p>
<p>Para obtener más información, consulte la <a href="../building-journeys/path-experimentation.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 7 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Bandeja de entrada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Bandeja de entrada</strong> es una funcionalidad móvil disponible con tarjetas de contenido que permite a los clientes crear una ubicación centralizada dentro de su aplicación o sitio web para mostrar los mensajes enviados a sus usuarios. Esto amplía la duración de las comunicaciones de marketing y garantiza que los mensajes permanezcan accesibles incluso después de descartarlos.</p>
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>Para obtener más información, consulte la <a href="../inbox/inbox-gs.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 7 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Optimize email text for AI inboxes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now includes a new capability that ensures your emails are optimally structured for AI-powered inboxes such as Apple Intelligence and Google Gemini in Gmail.</p>
<p>As AI assistants increasingly control how recipients read and act on email, this feature helps you author content that performs well across downstream AI tasks including summarization, triage, prioritization, and intent extraction.</p>
<p><img src="assets/do-not-localize/text-optimizer.gif"></p>
<p>For more information, refer to <a href="../email/llm-email-optimizer.md">Optimize email text for AI inboxes</a>.</p>
<p>Availability date: April 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Compatibilidad con decisiones en el canal de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede usar <strong>Decisioning</strong> para personalizar y optimizar el contenido de sus mensajes de correo electrónico. Aproveche las puntuaciones de prioridad, las fórmulas o los modelos de IA para mostrar las ofertas y el contenido más relevantes a cada destinatario.</p>
<p>Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general). Con esta versión de General Availability, ahora se admiten las páginas espejo.</p>
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>Para obtener más información, consulte la <a href="../experience-decisioning/create-decision-policy.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 6 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#april-26-improv}

#### IA

* **Puntuación de alineación de marca en el panel de campañas**: ahora puede evaluar la puntuación de alineación de marca directamente en el panel de campañas para asegurarse de que el contenido no modifique la marca. Esto le permite comprobar las directrices de un vistazo sin tener que abrir el diseñador de contenido.

* **Mejora del Asistente de mensajes**: cuando un mensaje es vago, incompleto o combina varios objetivos, **El Asistente de mensajes** ahora puede hacer preguntas aclaratorias centradas o sugerir una reescritura más clara de la solicitud antes de la generación, lo que le ayuda a fijar lo que necesita antes de que el asistente responda, lo que mejora la coherencia y reduce los reintentos. [Más información](../content-management/ai-assistant-prompting-guide.md)

#### Toma de decisiones

* **Adjuntar fragmentos a elementos de decisión**: Journey Optimizer ahora proporciona la capacidad de adjuntar fragmentos a elementos de decisión que se pueden aprovechar en campañas de correo electrónico y experiencia basadas en código mediante directivas de decisión. Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).

* **Se omiten los fragmentos que no están disponibles temporalmente**: al utilizar fragmentos en elementos de decisión, si un fragmento no está disponible temporalmente en Edge, se omitirá y el recorrido o la campaña continuará procesando en lugar de dar error. [Más información](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  Fecha de disponibilidad: 14 de abril de 2026

#### Push

* **Personalizar el ID de la aplicación en la configuración del canal**: en la configuración del canal push, ahora puede personalizar el campo **ID de la aplicación** para que cada destinatario pueda recibir una notificación push de la marca adecuada en función de su información de perfil.

#### SMS

* **Recuento de caracteres**: en Adobe Journey Optimizer, ahora puede usar el Recuento de caracteres para monitorizar la longitud de sus mensajes SMS en tiempo real. Le ayuda a ver cuándo se dividirá un mensaje en varios segmentos para administrar mejor el formato y evitar aumentos inesperados en los costes de envío. [Más información](../sms/create-sms.md)

* **Exclusión y consentimiento en el número de teléfono y remitente**: para SMS, Journey Optimizer ahora registra el consentimiento de marketing y la exclusión en el nivel tanto del número de teléfono como del código corto del perfil.

  Actualmente, esta capacidad solo está disponible para configuraciones de SMS de Sinch. [Más información](../sms/sms-configuration-sinch.md)

* **SMS inbounds to a custom dataset** - In **SMS API credentials**, route **inbound SMS** to a **custom, profile-enabled Experience Event dataset** you select instead of only the default tracking dataset. [Más información](../sms/sms-webhook.md)

* **Webhook interface enhancement** - When configuring SMS webhooks, the user interface now includes a built-in setup guide with practical examples, making it easier to align provider payloads and troubleshoot issues without leaving the configuration flow. [Más información](../sms/sms-webhook.md)

#### WhatsApp

* **WhatsApp interactive buttons and tracking** - WhatsApp in Journey Optimizer now supports interactive buttons required by your templates and use cases, along with built-in interaction tracking so you can measure engagement and analyze performance alongside your other channel reporting.

#### Adobe Experience Manager Integrations

* **Adobe Experience Manager Content fragment Varition Support** - You can select **Content Fragment variations** (for example language or channel variants) when inserting Adobe Experience Manager Content Fragments, with improved handling for locale and multilingual scenarios. [Más información](../integrations/aem-fragments.md#aem-variations)

  Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

  Availability date: April 3, 2026

* **Adobe Experience Manager Content Fragment context while authoring** - Your Content Fragment selection stays active as you move between text fields and content blocks, so you can add more fragment fields without reopening **Open AEM Content advisor** each time. [Más información](../integrations/aem-fragments.md)

  Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

  Availability date: April 1, 2026

#### Configuración

* **Specific permissions for URL parameter encryption keys** - To access and manage keys for URL parameter encryption, new permissions have been created. You must now have the **View Key Registry** and **Manage Key Registry** permissions granted.

#### Campañas orquestadas

* **Data Modeler enhancements** - Orchestrated relational schemas now support composite keys spanning multiple fields. Loading a schema from a DDL file also brings in enumerations, and loading from either a DDL or Excel file automatically creates composite relationships between tables. In the entity relationship view, composite links now display the full set of field pairings between tables after a file is uploaded.

* **Global variables in Orchestrated Campaigns** - Orchestrated Campaigns now support global variables that can be defined once and reused across all activities within a workflow, simplifying configuration and ensuring consistency in dynamic values, expressions, and content personalization.

#### Email design

* **Advanced HTML editor for email content** - Advanced HTML mode lets you edit the HTML source of your content in the Email Designer, add advanced expressions (such as conditions) in the source, and toggle between HTML view and Desktop view without losing your changes.

  Previously available for email content templates only, this capability is now deployed to **email** content in the Email Designer (for example, emails authored in journeys and campaigns), in addition to email content templates. It is currently in Limited Availability — contact your Adobe representative to gain access. [Más información](../email/email-expert-mode.md)

  Availability date: April 9, 2026

* **AI Assistant for personalization expressions in the Email Designer** - In the Email Designer, select a component and use **Add expression** in the contextual toolbar to describe the personalization you need in plain language, review the generated expression, and insert it without leaving the designer. [Más información](../content-management/generative-personalization-expressions.md#generate-email-designer)

  Availability date: April 15, 2026

#### Journey Path Optimization

* **Experiment type** - You can now choose between A/B experiment (fixed split at the start) or Multi-armed bandit (automatic split with weekly weight updates) when configuring a path experiment. [Más información](../building-journeys/path-experimentation.md)

  Availability date: April 7, 2026

* **Path experimentation: Scale the Winner** - You can now automatically or manually roll out the winning path of an experiment to your full audience. Una vez que se determina un ganador, puede amplificar su alcance y efectividad sin monitorear constantemente el experimento. [Más información](../building-journeys/path-experimentation.md#scale-winner)

  Esta funcionalidad solo está disponible en recorridos unitarios (cualificaciones de audiencia y activadas por eventos). No está disponible para recorridos de audiencia de lectura.

  Fecha de disponibilidad: 7 de abril de 2026

* **Condiciones** - La actividad [Optimizar](../building-journeys/optimize.md) es el nuevo vehículo para crear rutas condicionales en recorridos. Reemplaza la actividad **Condition** anterior, que se ha eliminado de la interfaz de usuario. Toda la lógica condicional se conserva y ahora se gestiona mediante las condiciones de la actividad **Optimize**. [Más información](../building-journeys/conditions.md)

  Esta funcionalidad, lanzada anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).

  Fecha de disponibilidad: 7 de abril de 2026


## Notas de la versión de marzo de 2026 {#march-26-rn}

Las secciones [Nuevas funcionalidades](#march-26-features) y [Mejoras](#march-26-improv) abarcan funcionalidades que ya están disponibles. <!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in March.-->

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
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
<ul><li> <strong>Modelo Adobe</strong> (con tecnología Firefly Image Model 4) para generar imágenes inmediatamente sin necesidad de configuración adicional</li><li> <strong>Modelo de socio</strong> (con tecnología Gemini 2.5 Flash) para funciones especializadas</li><li><strong>Modelos personalizados</strong> (modelos específicos de la marca entrenados en sus propios recursos) para la generación sin marca que se ajuste con precisión a su identidad de marca, estilo y directrices visuales.</li></ul>
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
<p>Para obtener más información, consulte la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html" target="_blank">documentación detallada</a>.</p>
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
