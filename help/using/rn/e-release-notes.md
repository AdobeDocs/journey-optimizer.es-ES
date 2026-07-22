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
source-git-commit: 8b3d97e7af3008418337f6afb3f6027bbc51c128
workflow-type: tm+mt
source-wordcount: 1972
ht-degree: 18%

---


# Notas de la versión preliminar {#e-release-notes}

Adobe Journey Optimizer ofrece de forma continua nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.




### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## Notas previas al lanzamiento de julio de 2026 {#july-26-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican una vez que los cambios estén disponibles en producción. Aunque la mayoría de los cambios se entregan en la fecha de lanzamiento, algunos pueden implementarse más adelante.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de la versión**: 28 de julio de 2026

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
<p>Los Desafíos de lealtad convierten las iniciativas de lealtad en experiencias atractivas y entretenidas que motivan a los clientes a realizar acciones valiosas, como realizar compras, escribir críticas, participar en medios sociales o recomendar amigos.</p>
<p>Los administradores pueden usar el menú de administración de Fidelidad para conectar Journey Optimizer con su ecosistema de fidelidad, incluidas las API de cumplimiento de recompensas, las definiciones de eventos, el inventario de productos, las exclusiones y la configuración de identidad. Los especialistas en marketing pueden diseñar desafíos estándar, de racha o secuenciales, definir tareas y recompensas, ofrecer tarjetas de contenido de marca y mensajes, y monitorizar el rendimiento con paneles de informes integrados. Journey Optimizer genera los recorridos que organizan cada desafío en segundo plano, de modo que los equipos puedan centrarse en la experiencia del cliente y los objetivos empresariales.</p>
<!-- GIF placeholder: to be added -->
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14019">DOCAC-14019</a></p>
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
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-15180">DOCAC-15180</a></p>
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
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14900">DOCAC-14900</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Compatibilidad de documentos con audiencias externas (valores separados por comas y composición de audiencias federada) en la simulación de Recorrido**: la simulación de Recorrido ahora admite audiencias externas. Al simular recorridos dirigidos a valores separados por comas o audiencias de Composición de audiencia federada, puede burlar atributos de enriquecimiento de esas audiencias directamente a través del formulario de la interfaz de usuario o una importación JSON. La interfaz de usuario muestra dinámicamente solo los atributos de enriquecimiento específicos utilizados en la lógica de recorrido, lo que permite la validación precisa de las ramas de decisión y las reglas de personalización antes de su lanzamiento. ([DOCAC-15074](https://jira.corp.adobe.com/browse/DOCAC-15074)) <!-- Documentation link: TBD -->

* **Fechas de inicio y finalización en el encabezado del recorrido**: cuando las fechas de inicio o finalización se configuran en un recorrido activo, ahora aparecen en el encabezado del recorrido junto al distintivo de estado activo. La etiqueta mostrada se adapta en función de si cada fecha es próxima o ya ha pasado. ([DOCAC-14702](https://jira.corp.adobe.com/browse/DOCAC-14702)) <!-- Documentation link: TBD -->

### Campañas orquestadas {#july-26-oc}

En esta versión se ha añadido la siguiente mejora a las campañas orquestadas.

* **Ver transiciones de campaña orquestadas permiso** - Se ha agregado un nuevo permiso **Ver transiciones de campaña orquestadas** para reemplazar la opción **Ver archivo en campañas orquestadas** heredada. Este cambio le permite ocultar los resultados de la vista previa en las transiciones de campaña para cumplir con la información de identificación personal. ([DOCAC-14924](https://jira.corp.adobe.com/browse/DOCAC-14924))

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
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14054">DOCAC-14054</a></p>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Action campaigns inbound channels simulation mode</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now simulate inbound channel actions in Action campaigns before going live. Use simulation mode to test your configuration with simulated users and preview the rendered experience, including a generated URL and QR code, so you can validate rules, decisioning, and content rendering end-to-end.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<GIF placeholder: to be added>
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-15166">DOCAC-15166</a></p>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

* **Ability to Manage Profile Target Dimensions** - You can now delete a Profile Target Dimension or edit and swap its configured identity namespace, providing greater control and flexibility over your data setups. ([DOCAC-15018](https://jira.corp.adobe.com/browse/DOCAC-15018)) 

* **Support for Line** - You can now add LINE actions directly into your Orchestrated campaigns. This new activity allows you to build and deliver highly personalized content, including text, stickers, images, videos, location data, and rich Flex Messages, to engage your customers seamlessly on the LINE platform. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative. ([DOCAC-14905](https://jira.corp.adobe.com/browse/DOCAC-14905))

* **New Orchestrated campaigns public APIs** - New API specifications are now available for Orchestrated campaigns. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines. ([DOCAC-14308](https://jira.corp.adobe.com/browse/DOCAC-14308))

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address. Header values can be set at the channel level and overridden per campaign using contextual data for more precise control. ([DOCAC-13761](https://jira.corp.adobe.com/browse/DOCAC-13761)) Documentation link: TBD 

* **Target dimension simplification in Orchestrated campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level. ([DOCAC-13554](https://jira.corp.adobe.com/browse/DOCAC-13554))

-->

### Campañas {#july-26-campaigns}

En esta versión se han añadido las siguientes funcionalidades y mejoras a las campañas de.

<table>
<thead>
<tr>
<th><strong>Archivo adjunto de PDF personalizado para mensajería transaccional en campañas activadas por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede adjuntar hasta cinco PDF dinámicos personalizados por correo electrónico en campañas transaccionales activadas por API pasando las ubicaciones de los archivos en la carga útil de la API. Esto permite a industrias como la aviación enviar tarjetas de embarque o confirmaciones de viaje, servicios financieros para entregar facturas o declaraciones individualizadas y venta minorista para incluir recibos de pedidos o etiquetas de devolución (cada documento adaptado al destinatario en el momento de la entrega).</p>
<p>Los archivos adjuntos personalizados y estáticos de PDF comparten la misma cuota; para superar el límite de uso razonable, es necesario el complemento de archivos adjuntos de PDF. Esta función no está disponible en campañas de recorrido o de acción.</p>
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-15186">DOCAC-15186</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Carpetas para campañas**: ahora puede organizar sus campañas en carpetas para mejorar la navegación y la administración en la interfaz. ([DOCAC-15098](https://jira.corp.adobe.com/browse/DOCAC-15098)) <!-- Documentation link: TBD -->

* **Anular el campo de ejecución predeterminado en las campañas**: anteriormente disponible en el nivel de recorrido, ahora se puede anular el campo de ejecución predeterminado establecido globalmente para los envíos de correo electrónico, SMS y WhatsApp en los parámetros de la campaña. ([DOCAC-14718](https://jira.corp.adobe.com/browse/DOCAC-14718)) <!-- Documentation link: TBD -->

* **Puntuación de alineación de marca en el panel de control de campañas**: ahora puede evaluar la puntuación de alineación con la marca directamente en el panel de control de campañas para asegurarse de que el contenido sea coherente con la marca. Esto le permite comprobar las directrices de un vistazo sin tener que abrir el diseñador de contenido. ([DOCAC-14516](https://jira.corp.adobe.com/browse/DOCAC-14516)) <!-- Documentation link: TBD -->

### Toma de decisiones {#july-26-decisioning}

En esta versión se han añadido las siguientes mejoras a Decisioning.

* **Creación de reglas de decisión y fórmulas de clasificación a partir de la expresión en lenguaje natural**: ahora puede describir la regla de decisión o la fórmula de clasificación que desea crear en lenguaje sencillo y permitir que el Asistente de IA la genere por usted. Esta funcionalidad está disponible para los clientes con acceso a las funcionalidades de Adobe AI. ([DOCAC-15231](https://jira.corp.adobe.com/browse/DOCAC-15231)) <!-- Documentation link: TBD -->

* **Simulación de reglas de decisión y fórmulas de clasificación**: ahora puede simular las reglas de decisión y las fórmulas de clasificación directamente desde el editor de reglas o fórmulas. Agregue variantes de prueba manuales o genérelas mediante IA y, a continuación, ejecute la expresión con los datos de prueba para validar la idoneidad y revisar los resultados de clasificación, todo antes de implementarlos en producción. La generación de variantes está disponible para los clientes con acceso a las funciones de Adobe AI. ([DOCAC-15227](https://jira.corp.adobe.com/browse/DOCAC-15227)) <!-- Documentation link: TBD -->

* **Atributos de oferta dinámicos**: los atributos personalizados de elemento de decisión ahora se pueden personalizar en el momento de la entrega mediante datos de perfil, contextuales y de audiencia. Esto elimina la necesidad de mantener ofertas duplicadas para variaciones de contenido menores, lo que permite a los especialistas en marketing administrar menos elementos de decisión más flexibles. ([DOCAC-14899](https://jira.corp.adobe.com/browse/DOCAC-14899)) <!-- Documentation link: TBD -->

### Gestión de contenidos {#july-26-content}

En esta versión se han añadido las siguientes mejoras a la administración de contenido.

* **Compatibilidad con fragmentos de expresión en `<head>` de plantillas de correo electrónico**. Ahora se pueden usar fragmentos de expresión en `<head>` de plantillas de correo electrónico. Esto le permite centralizar el estilo de cualquier código personalizado en un solo fragmento y reutilizarlo en varias plantillas. Cuando se actualiza y vuelve a publicar un fragmento, todos los correos electrónicos creados a partir de plantillas que hacen referencia a él heredan automáticamente el código más reciente, lo que elimina la necesidad de actualizar manualmente cada correo electrónico de forma individual. ([DOCAC-15257](https://jira.corp.adobe.com/browse/DOCAC-15257)) <!-- Documentation link: TBD -->

* Se cambió el nombre de **&quot;Asistente de IA&quot; a &quot;Generar contenido&quot;**. Se cambió el nombre del Asistente de IA a Generar contenido en Adobe Journey Optimizer. Esta actualización se limita a los nombres y la terminología; no se han introducido cambios funcionales. Se ha cambiado el nombre de las etiquetas de navegación, los botones, los menús y los cuadros de diálogo para la generación de contenido, la generación de imágenes, las expresiones de personalización y la experimentación de contenido de &quot;Asistente de IA&quot; a &quot;Generar contenido&quot;. ([DOCAC-15230](https://jira.corp.adobe.com/browse/DOCAC-15230)) <!-- Documentation link: TBD -->

* **Abastecimiento flexible de imágenes para la generación de contenido de IA**: la generación de contenido en Journey Optimizer ahora obtiene imágenes aprobadas por la marca directamente desde Adobe Experience Manager Assets Essentials y versiones posteriores. Tres modos controlan el equilibrio: Assets (origen predeterminado de Digital Asset Management), Equilibrado (primero Digital Asset Management, rellena los huecos de IA) y Creative (primero de IA). Esto garantiza que cada imagen sea precisa, compatible con la marca y lista para la producción para recorridos y campañas. ([DOCAC-14761](https://jira.corp.adobe.com/browse/DOCAC-14761)) <!-- Documentation link: TBD -->

* **Mejoras multilingües**: ahora se puede duplicar la configuración de idioma a partir de una configuración activa existente, por lo que ya no es necesario reconstruir completamente una configuración para realizar cambios. También puede copiar una condición de una configuración regional a otra durante la creación de la Configuración de idioma, lo que optimiza la configuración para sitios con muchos idiomas.
([DOCAC-15268](https://jira.corp.adobe.com/browse/DOCAC-15268))

<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. ([DOCAC-13801](https://jira.corp.adobe.com/browse/DOCAC-13801)) [Documentation link: TBD]
-->

### Canal de correo electrónico {#july-26-email}

En esta versión se han añadido las siguientes funciones al canal de correo electrónico.

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
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14877">DOCAC-14877</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Personalización {#july-26-personalization}

En esta versión se han añadido las siguientes mejoras a la personalización.

* **Administrar dominios para la personalización completa/base de URL**: ahora puede crear y administrar dominios aprobados para la personalización completa y base de URL directamente desde la configuración de administración en Adobe Journey Optimizer, sin tener que ponerse en contacto con el Soporte técnico de Adobe. ([DOCAC-15187](https://jira.corp.adobe.com/browse/DOCAC-15187)) <!-- Documentation link: TBD -->

* **Nuevas funciones de ayuda en las expresiones de personalización**. Las nuevas funciones de ayuda ya están disponibles en las expresiones de personalización:

  * `appendQueryParams`: anexa un parámetro de consulta a una dirección URL o lo reemplaza si la clave ya existe.
  * `dateBetween`: comprueba si una fecha se encuentra dentro de un intervalo de fechas de inicio y finalización (incluido).
  * `equalsAnyIgnoreCase`: devuelve el valor &quot;True&quot; cuando una cadena coincide con cualquier valor proporcionado, omitiendo mayúsculas y minúsculas.
  * `getUrlFragment`: extrae la parte de fragmento de una dirección URL (la parte posterior a #).
  * `join`: concatena elementos de matriz en una sola cadena utilizando un separador.
  * `decode64`: descodifica una cadena codificada en Base64. Si la entrada no es Base64 válida, la cadena de entrada original se devuelve sin cambiar.

  La función `concat` también se ha mejorado y ahora admite dos o más argumentos.

  Además, las siguientes funciones de migración de plantillas ya están disponibles para ayudarle a migrar plantillas existentes a Journey Optimizer:

  * `ampCompare`: compara dos valores utilizando el operador de comparación especificado.
  * `ampSubstr`: devuelve una parte de una cadena entre los índices de inicio y fin especificados.
  * `compareTo`: compara dos cadenas lexicográficamente.

  ([DOCAC-15099](https://jira.corp.adobe.com/browse/DOCAC-15099)) <!-- Documentation link: TBD -->

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
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-11381">DOCAC-11381</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Canal de WhatsApp: admite plantillas de flujo de WhatsApp**. Ahora puedes enviar plantillas de flujo de WhatsApp en Adobe Journey Optimizer para ofrecer experiencias interactivas en varias pantallas, como encuestas y captura de posibles clientes. Las respuestas se capturan al enviarlas y se almacenan como cargas JSON sin procesar en el nuevo conjunto de datos de evento de seguimiento de canal de Journey Optimizer. ([DOCAC-15223](https://jira.corp.adobe.com/browse/DOCAC-15223)) <!-- Documentation link: TBD -->

* **Complemento de rendimiento para el rendimiento - Push** - Hay un nuevo modo de mensajería transaccional de alto rendimiento disponible en las campañas activadas por API. Este modo está diseñado para la mensajería transaccional a gran escala y en tiempo real y admite hasta 5000 transacciones por segundo con una mayor disponibilidad. Antes solo estaba disponible para el canal de correo electrónico, pero ahora también lo está para el canal push, para organizaciones que han adquirido la oferta de complementos de mensajería transaccional de alto rendimiento de Adobe. Póngase en contacto con su representante de Adobe para obtener más información. ([DOCAC-14717](https://jira.corp.adobe.com/browse/DOCAC-14717)) <!-- Documentation link: TBD -->

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
<p>Jira: <a href="https://jira.corp.adobe.com/browse/DOCAC-14814">DOCAC-14814</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>
