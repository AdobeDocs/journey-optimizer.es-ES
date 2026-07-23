---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 5c5b42ec6cf86a942f2affb681e9c8143734c7ab
workflow-type: tm+mt
source-wordcount: 2034
ht-degree: 13%

---


# Notas de la versión preliminar {#e-release-notes}

Adobe Journey Optimizer ofrece de forma continua nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.




### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## Notas previas al lanzamiento de julio de 2026 {#july-26-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican una vez que los cambios estén disponibles en producción. Aunque la mayoría de los cambios se entregan en la fecha de lanzamiento, algunos pueden implementarse más adelante.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de la versión**: 28 y 29 de julio de 2026

### Lealtad {#july-26-loyalty}

Journey Optimizer presenta Loyalty, una nueva funcionalidad de esta versión.

<table>
<thead>
<tr>
<th><strong>Desafíos de fidelización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los Desafíos de lealtad convierten las iniciativas de lealtad en experiencias atractivas y entretenidas que motivan a los clientes a realizar acciones valiosas, como realizar compras, escribir críticas o participar en medios sociales.</p>
<p>Los administradores pueden usar el menú de administración de Fidelidad para conectar Journey Optimizer con su ecosistema de fidelidad, incluidas las API de cumplimiento de recompensas, las definiciones de eventos, el inventario de productos, las exclusiones y la configuración de identidad. Los especialistas en marketing pueden diseñar desafíos estándar, de racha o secuenciales, definir tareas y recompensas, ofrecer tarjetas de contenido de marca y mensajes, y monitorizar el rendimiento con paneles de informes integrados. Journey Optimizer genera los recorridos que organizan cada desafío en segundo plano, de modo que los equipos puedan centrarse en la experiencia del cliente y los objetivos empresariales.</p>
<p>La lealtad también introduce una habilidad de Coworker que permite a los equipos realizar operaciones de desafío clave de forma más eficiente, incluida la creación de desafíos, la configuración de propiedades de desafío, la administración de audiencias y la configuración relacionada, y la revisión de perspectivas para monitorizar la participación en el desafío y recompensar el rendimiento.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<!--

### Onboarding {#july-26-onboarding}

Journey Optimizer introduces the Onboarding Assistant, a new capability in this release.

<table>
<thead>
<tr>
<th><strong>Onboarding Assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### Recorridos {#july-26-journeys}

En esta versión se han añadido las siguientes funciones y mejoras a los recorridos.

<table>
<thead>
<tr>
<th><strong>Optimización de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede configurar una acción de recorrido para incluir varios canales salientes (correo electrónico, push, SMS) y permitir que Journey Optimizer realice envíos automáticamente a través del mejor canal para cada cliente. Hay tres modos de optimización disponibles:</p>
<ul>
<li>Clasificación manual: especifique el orden de canal preferido.</li>
<li>Preferencia del cliente: utilice el canal preferido del cliente desde su perfil (atributo Consentimientos y preferencias del modelo de datos de experiencia ).</li>
<li>Clasificación basada en modelos de IA: utilice puntuaciones de tendencia de aprendizaje automático para deducir el canal más efectivo por cliente.</li>
</ul>
<p>Cuando el canal de mayor clasificación no está disponible (no está incluido, limitado por frecuencia o no está configurado), el sistema vuelve al siguiente canal disponible.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Compatibilidad de documentos con audiencias externas: composición de audiencias federadas en la simulación de Recorrido**. La simulación de Recorrido ahora admite audiencias externas. Al simular recorridos dirigidos a audiencias de Composición de audiencia federada, puede burlar atributos de enriquecimiento de esas audiencias directamente a través del formulario de la interfaz de usuario o una importación JSON. La interfaz de usuario muestra dinámicamente solo los atributos de enriquecimiento específicos utilizados en la lógica de recorrido, lo que permite la validación precisa de las ramas de decisión y las reglas de personalización antes de su lanzamiento. <!-- Documentation link: TBD -->

* **Fechas de inicio y finalización en el encabezado del recorrido**: cuando las fechas de inicio o finalización se configuran en un recorrido activo, ahora aparecen en el encabezado del recorrido junto al distintivo de estado activo. La etiqueta mostrada se adapta en función de si cada fecha es próxima o ya ha pasado. <!-- Documentation link: TBD -->

### Campañas {#july-26-campaigns}

En esta versión se han añadido las siguientes funcionalidades y mejoras a las campañas de.

<table>
<thead>
<tr>
<th><strong>Archivos adjuntos personalizados de PDF en correos electrónicos activados por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora admite la asociación de hasta cinco PDF específicos de destinatarios por correo electrónico en campañas activadas por API. Los archivos PDF se recuperan de forma segura desde el almacenamiento de Azure o AWS y se adjuntan en el momento del envío, con la ubicación de cada archivo pasada directamente en la carga útil de la API. Esto permite que los sistemas existentes de generación de documentos de subida permanezcan en su sitio, con Journey Optimizer gestionando la entrega.</p>
<p>Los casos de uso admitidos incluyen facturas, extractos, tickets, contratos, etiquetas de envío y documentos similares que varían según el destinatario. Los archivos adjuntos personalizados de PDF solo están disponibles en campañas activadas por API y no son compatibles con recorridos u otros tipos de campañas (de acción, organizadas).</p>
<p>Los volúmenes y tamaños de archivos adjuntos más grandes son compatibles mediante el complemento de archivos adjuntos de PDF. Para obtener más información, póngase en contacto con su representante de Adobe.</p>
<p></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulación de experiencia entrante en campañas de acción</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede simular acciones de canal entrante en campañas de acción antes de lanzarlas. Utilice el modo de simulación para probar la configuración con usuarios simulados y previsualizar la experiencia procesada, incluida una URL y un código QR generados, para poder validar reglas, decisiones y el procesamiento de contenido de principio a fin.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

* **Carpetas para campañas**: ahora puede organizar sus campañas en carpetas para mejorar la navegación y la administración en la interfaz. <!-- Documentation link: TBD -->

* **Anular el campo de ejecución predeterminado en las campañas**: antes disponible en el nivel de recorrido, ahora se puede anular el campo de ejecución predeterminado establecido globalmente para las entregas de correo electrónico, SMS y WhatsApp en los parámetros de campaña. <!-- Documentation link: TBD -->

* **Puntuación de alineación de marca en el panel de control de campañas**: ahora puede evaluar la puntuación de alineación con la marca directamente en el panel de control de campañas para asegurarse de que el contenido sea coherente con la marca. Esto le permite comprobar las directrices de un vistazo sin tener que abrir el diseñador de contenido. <!-- Documentation link: TBD -->

### Campañas orquestadas {#july-26-oc}

En esta versión se ha añadido la siguiente mejora a las campañas orquestadas.

* **Ver transiciones de campaña orquestadas permiso** - Se ha agregado un nuevo permiso **Ver transiciones de campaña orquestadas** para reemplazar la opción **Ver archivo en campañas orquestadas** heredada. Este cambio le permite ocultar los resultados de la vista previa en las transiciones de campaña para cumplir con la información de identificación personal.

<!--
<table>
<thead>
<tr>
<th><strong>Quiet Hours support for orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now apply quiet hours to Orchestrated campaigns. Quiet hours let you define time-based exclusions to prevent messages from being sent during specific periods, helping you respect customer preferences and compliance requirements across campaign orchestration use cases.</p>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

* **Ability to Manage Profile Target Dimensions** - You can now delete a Profile Target Dimension or edit and swap its configured identity namespace, providing greater control and flexibility over your data setups.

* **Support for Line** - You can now add LINE actions directly into your Orchestrated campaigns. This new activity allows you to build and deliver highly personalized content, including text, stickers, images, videos, location data, and rich Flex Messages, to engage your customers seamlessly on the LINE platform. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

* **New Orchestrated campaigns public APIs** - New API specifications are now available for Orchestrated campaigns. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines.

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address. Header values can be set at the channel level and overridden per campaign using contextual data for more precise control. Documentation link: TBD

* **Target dimension simplification in Orchestrated campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.

-->

### Toma de decisiones {#july-26-decisioning}

En esta versión se han añadido las siguientes mejoras a Decisioning.

* **Creación de reglas de toma de decisiones a partir de la expresión de lenguaje natural**: ahora puede describir la regla de toma de decisiones que desea crear en lenguaje sin formato y permitir que la inteligencia artificial la genere por usted. Esta funcionalidad está disponible para los clientes con acceso a las funcionalidades de Adobe AI. <!-- Documentation link: TBD -->

* **Simulación de reglas de decisión y fórmulas de clasificación**: ahora puede simular las reglas de decisión y las fórmulas de clasificación directamente desde el editor de reglas o fórmulas. Agregue variantes de prueba manuales o genérelas mediante IA y, a continuación, ejecute la expresión con los datos de prueba para validar la idoneidad y revisar los resultados de clasificación, todo antes de implementarlos en producción. La generación de variantes está disponible para los clientes con acceso a las funciones de Adobe AI. <!-- Documentation link: TBD -->

* **Personalization en el nivel de oferta**: los atributos personalizados del elemento de decisión ahora se pueden personalizar en el momento de la entrega mediante datos de perfil, contextuales y de audiencia. Esto elimina la necesidad de mantener ofertas duplicadas para variaciones de contenido menores, lo que permite a los especialistas en marketing administrar menos elementos de decisión más flexibles. <!-- Documentation link: TBD -->

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### Gestión de contenidos {#july-26-content}

En esta versión se han añadido las siguientes mejoras a la administración de contenido.

* **Compatibilidad con fragmentos de expresión en `<head>` de plantillas de correo electrónico**. Ahora se pueden usar fragmentos de expresión en `<head>` de plantillas de correo electrónico. Esto le permite centralizar el estilo de cualquier código personalizado en un solo fragmento y reutilizarlo en varias plantillas. Cuando se actualiza y vuelve a publicar un fragmento, todos los correos electrónicos creados a partir de plantillas que hacen referencia a él heredan automáticamente el código más reciente, lo que elimina la necesidad de actualizar manualmente cada correo electrónico de forma individual. <!-- Documentation link: TBD -->

* Se cambió el nombre de **&quot;Asistente de IA&quot; a &quot;Generar contenido&quot;**. Se cambió el nombre del Asistente de IA a Generar contenido en Adobe Journey Optimizer. Esta actualización se limita a los nombres y la terminología; no se han introducido cambios funcionales. Se ha cambiado el nombre de las etiquetas de navegación, los botones, los menús y los cuadros de diálogo para la generación de contenido, la generación de imágenes, las expresiones de personalización y la experimentación de contenido de &quot;Ayudante de IA&quot; a &quot;Generar contenido&quot;. <!-- Documentation link: TBD -->

* **Abastecimiento flexible de imágenes para la generación de contenido de IA**: la generación de contenido en Journey Optimizer ahora obtiene imágenes aprobadas por la marca directamente desde Adobe Experience Manager Assets Essentials y versiones posteriores. Tres modos controlan el equilibrio: Assets (origen predeterminado de Digital Asset Management), Equilibrado (primero Digital Asset Management, rellena los huecos de IA) y Creative (primero de IA). Esto garantiza que cada imagen sea precisa, compatible con la marca y lista para la producción para recorridos y campañas. <!-- Documentation link: TBD -->

* **Mejoras multilingües**: ahora se puede duplicar la configuración de idioma a partir de una configuración activa existente, por lo que ya no es necesario reconstruir completamente una configuración para realizar cambios. También puede copiar una condición de una configuración regional a otra durante la creación de la Configuración de idioma, lo que optimiza la configuración para sitios con muchos idiomas.

<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### Personalización {#july-26-personalization}

En esta versión se han añadido las siguientes mejoras a la personalización.

* **Administrar dominios para la personalización completa/base de URL**: ahora puede crear y administrar dominios aprobados para la personalización completa y base de URL directamente desde la configuración de administración en Adobe Journey Optimizer, sin tener que ponerse en contacto con el Soporte técnico de Adobe. <!-- Documentation link: TBD -->

* **Nuevas funciones de ayuda en las expresiones de personalización**. Las nuevas funciones de ayuda ya están disponibles en las expresiones de personalización:

  * `appendQueryParams`: anexa un parámetro de consulta a una dirección URL o lo reemplaza si la clave ya existe.
  * `dateBetween`: comprueba si una fecha se encuentra dentro de un intervalo de fechas de inicio y finalización (incluido).
  * `equalsAnyIgnoreCase`: devuelve el valor &quot;True&quot; cuando una cadena coincide con cualquier valor proporcionado, omitiendo mayúsculas y minúsculas.
  * `getUrlFragment`: extrae la parte de fragmento de una dirección URL (la parte posterior a #).
  * `join`: concatena elementos de matriz en una sola cadena utilizando un separador.
  * `decode64`: descodifica una cadena codificada en Base64. Si la entrada no es Base64 válida, la cadena de entrada original se devuelve sin cambiar.
  * `parseJson`: analiza una cadena JSON en una variable estructurada que se puede utilizar en la plantilla.
  * `valueAtPath`: asigna un valor de una ruta de datos a una variable de plantilla, con indexación opcional para extraer un elemento específico de matrices o colecciones.

  La función `concat` también se ha mejorado y ahora admite dos o más argumentos.

  Además, las siguientes funciones de migración de plantillas ya están disponibles para ayudarle a migrar plantillas existentes a Journey Optimizer:

  * `ampCompare`: compara dos valores utilizando el operador de comparación especificado.
  * `ampSubstr`: devuelve una parte de una cadena entre los índices de inicio y fin especificados.
  * `compareTo`: compara dos cadenas lexicográficamente.

<!-- Documentation link: TBD -->

### Canal de correo electrónico {#july-26-email}

En esta versión se ha añadido la siguiente funcionalidad al canal de correo electrónico.

<table>
<thead>
<tr>
<th><strong>Módulos en el diseñador de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El diseñador de correo electrónico ahora incluye una biblioteca de módulos de diseño listos para usar, como encabezados, tarjetas de producto, bloques de información y pies de página, que puede arrastrar y soltar directamente en el lienzo del correo electrónico. Cada módulo viene preconfigurado con propiedades editables (imagen, título, texto, botón, vínculos) y se puede personalizar completamente a través de la interfaz de WYSIWYG, lo que acelera la creación de correos electrónicos sin necesidad de crear estructuras desde cero.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Canales {#july-26-channels}

En esta versión se han añadido las siguientes funcionalidades y mejoras a los canales.

<table>
<thead>
<tr>
<th><strong>Canal saliente personalizado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora presenta Canales personalizados, una nueva funcionalidad que permite a los administradores introducir cualquier canal de mensajería saliente basado en HTTP, como WeChat, Kakao Talk, Messenger o un proveedor propietario, directamente en Journey Optimizer a través de un Generador de canales sin código. Una vez configurados, los canales personalizados están disponibles en Campañas, Recorridos y Campañas orquestadas, con el mismo conjunto completo de funcionalidades que los canales nativos: personalización con el editor de expresiones, experimentación de contenido, previsualización y prueba, informes predeterminados y aplicación de consentimiento y gobernanza. Esto llena un hueco que anteriormente solucionaban las acciones personalizadas, que se limitan únicamente a los Recorridos y carecen de funcionalidades de canal dedicadas.</p>
<p>Actualmente, los canales salientes personalizados están disponibles como disponibilidad limitada. Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Canal de WhatsApp: admite plantillas de flujo de WhatsApp**. Ahora puedes enviar plantillas de flujo de WhatsApp en Adobe Journey Optimizer para ofrecer experiencias interactivas en varias pantallas, como encuestas y captura de posibles clientes. Las respuestas se capturan al enviarlas y se almacenan como cargas JSON sin procesar en el nuevo conjunto de datos de evento de seguimiento de canal de Journey Optimizer. <!-- Documentation link: TBD -->

* **Complemento de rendimiento para el rendimiento - Push** - Hay un nuevo modo de mensajería transaccional de alto rendimiento disponible en las campañas activadas por API. Este modo está diseñado para la mensajería transaccional a gran escala y en tiempo real y admite hasta 5000 transacciones por segundo con una mayor disponibilidad. Antes solo estaba disponible para el canal de correo electrónico, pero ahora también lo está para el canal push, para organizaciones que han adquirido la oferta de complementos de mensajería transaccional de alto rendimiento de Adobe. Póngase en contacto con su representante de Adobe para obtener más información. <!-- Documentation link: TBD -->

* **Integraciones mejoradas de proveedores personalizados - Móvil** - Las integraciones de proveedores personalizados ahora ofrecen una mayor flexibilidad con mensajes clave y actualizaciones de encabezados:

  * Personalización del encabezado: ahora puede editar el valor predeterminado del encabezado Content-Type y añadir hasta 10 parámetros de encabezado personalizados.

  * Compatibilidad con carga útil SMS: se ha agregado compatibilidad con las funciones de ayuda de Adobe Journey Optimizer en la carga útil SMS, incluida encode64.

### Administración {#july-26-administration}

En esta versión se han añadido las siguientes funcionalidades a la administración.

<table>
<thead>
<tr>
<th><strong>Lista blanca de IP del cortafuegos de aplicaciones web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ahora admite la lista de direcciones IP permitidas del cortafuegos de aplicaciones web para las páginas de destino, lo que permite a las organizaciones exigir que todas las solicitudes entrantes se enruten exclusivamente a través de la infraestructura configurada del cortafuegos de aplicaciones web. Con esta mejora, los clientes pueden configurar Journey Optimizer para que rechace cualquier solicitud directa que omita el nivel del cortafuegos de aplicaciones web, asegurándose de que las políticas de seguridad definidas en herramientas como Imperva se apliquen de forma coherente.</p>
<p>Esta capacidad refuerza la postura de seguridad de las empresas con requisitos estrictos de acceso a la red, lo que les permite un control total del flujo de tráfico a sus páginas de aterrizaje alojadas en Journey Optimizer.</p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>
