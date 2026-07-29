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
source-git-commit: c58b70fa5f792e2fa1448034559ad7210e3e10d4
workflow-type: tm+mt
source-wordcount: 967
ht-degree: 21%

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

<table>
<thead>
<tr>
<th><strong>Channel optimization (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add multiple outbound channels (Email, Push, SMS) to a single journey action and let Journey Optimizer automatically deliver through the best channel for each customer. Three optimization modes are available: manual ranking, customer profile preference (XDM attribute), and AI model-based ranking using propensity scores. When the top-ranked channel is unavailable, the system falls back to the next available channel.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../building-journeys/channel-optimization.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## Notas previas al lanzamiento de julio de 2026 {#july-26-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican una vez que los cambios estén disponibles en producción. Aunque la mayoría de los cambios se entregan en la fecha de lanzamiento, algunos pueden implementarse más adelante.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de la versión**: 28 y 29 de julio de 2026

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

En esta versión se ha añadido la siguiente mejora a los recorridos de.

<!-- Documentation link: TBD -->

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

<!--
<table>
<thead>
<tr>
<th><strong>Inbound experience simulation in Action campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now simulate inbound channel actions in Action campaigns before going live. Use simulation mode to test your configuration with simulated users and preview the rendered experience, including a generated URL and QR code, so you can validate rules, decisioning, and content rendering end-to-end.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
[GIF placeholder: to be added]
[Documentation link: TBD]
</td>
</tr>
</tbody>
</table>

-->

### Campañas orquestadas {#july-26-oc}

En esta versión se han añadido las siguientes mejoras a las campañas orquestadas.


<!--
* **Send messages in waves** - You can now schedule outbound messages from orchestrated campaigns to be delivered in controlled batches over time. Ideal for high-volume or time-sensitive campaigns, wave sending also supports better deliverability and helps maintain a strong sender reputation by reducing the risk of being flagged as spam.
-->

<!--
### Optimization {#july-26-optimization}

<table>
<thead>
<tr>
<th><strong>Channel optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now configure a journey or campaign action to include multiple outbound channels (Email, Push, SMS) and let Journey Optimizer automatically deliver through the best channel for each customer. Three optimization modes are available:</p>
<ul>
<li>Manual ranking: specify your preferred channel order.</li>
<li>Customer preference: use the customer's preferred channel from their profile (Experience Data Model Consents & Preferences attribute).</li>
<li>AI model-based ranking: use machine learning propensity scores to infer the most effective channel per customer.</li>
</ul>
<p>When the top-ranked channel is unavailable (not opted-in, frequency-capped, or not configured), the system falls back to the next available channel.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>
-->

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
<p>Journey Optimizer ahora presenta Canales personalizados, una nueva funcionalidad que permite a los administradores introducir cualquier canal de mensajería saliente basado en HTTP, como WeChat, Kakao Talk, Messenger o un proveedor propietario, directamente en Journey Optimizer a través de un Generador de canales sin código.</p >
<p>Una vez configurados, los canales personalizados están disponibles en todas las campañas, recorridos y campañas orquestadas, con el mismo conjunto completo de funcionalidades que los canales nativos: personalización con el editor de expresiones, experimentación de contenido, previsualización y prueba, creación de informes predeterminada y aplicación de consentimiento y gobernanza.</p>
<p>Esto llena un hueco que anteriormente se solucionaba con las acciones personalizadas, que se limitan únicamente a los recorridos y carecen de funcionalidades de canal dedicadas.</p>
<p>Actualmente, los canales salientes personalizados están disponibles como disponibilidad limitada. Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Complemento de rendimiento para el rendimiento - Push** - Hay un nuevo modo de mensajería transaccional de alto rendimiento disponible en las campañas activadas por API. Este modo está diseñado para la mensajería transaccional a gran escala y en tiempo real y admite hasta 5000 transacciones por segundo con una mayor disponibilidad. Antes solo estaba disponible para el canal de correo electrónico, pero ahora también lo está para el canal push, para organizaciones que han adquirido la oferta de complementos de mensajería transaccional de alto rendimiento de Adobe. Póngase en contacto con su representante de Adobe para obtener más información. <!-- Documentation link: TBD -->



### Toma de decisiones {#july-26-decisioning}

En esta versión se han añadido las siguientes mejoras a Decisioning.

* **Personalization en el nivel de oferta**: los atributos personalizados del elemento de decisión ahora se pueden personalizar en el momento de la entrega mediante datos de perfil, contextuales y de audiencia. Esto elimina la necesidad de mantener ofertas duplicadas para variaciones de contenido menores, lo que permite a los especialistas en marketing administrar menos elementos de decisión más flexibles. <!-- Documentation link: TBD -->

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### Gestión de contenidos {#july-26-content}

En esta versión se han añadido las siguientes mejoras a la administración de contenido.

* **Compatibilidad con fragmentos de expresión en `<head>` de plantillas de correo electrónico**. Ahora se pueden usar fragmentos de expresión en `<head>` de plantillas de correo electrónico. Esto le permite centralizar el estilo de cualquier código personalizado en un solo fragmento y reutilizarlo en varias plantillas. Cuando se actualiza y vuelve a publicar un fragmento, todos los correos electrónicos creados a partir de plantillas que hacen referencia a él heredan automáticamente el código más reciente, lo que elimina la necesidad de actualizar manualmente cada correo electrónico de forma individual. <!-- Documentation link: TBD -->
<!-- Documentation link: TBD -->



<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### Personalización {#july-26-personalization}

En esta versión se han añadido las siguientes mejoras a la personalización.

* **Administrar dominios para la personalización completa/base de URL**: ahora puede crear y administrar dominios aprobados para la personalización completa y base de URL directamente desde la configuración de administración en Adobe Journey Optimizer, sin tener que ponerse en contacto con el Soporte técnico de Adobe. <!-- Documentation link: TBD -->

<!-- Documentation link: TBD -->

### Diseñador de correo electrónico {#july-26-email}

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
<p>El diseñador de correo electrónico ahora incluye una biblioteca de módulos de diseño listos para usar, como encabezados, tarjetas de producto, bloques de información y pies de página, que puede arrastrar y soltar directamente en el lienzo del correo electrónico.</p>
<p>Cada módulo viene preconfigurado con propiedades editables (imagen, título, texto, botón, vínculos) y se puede personalizar completamente a través de la interfaz de WYSIWYG, lo que acelera la creación de correos electrónicos sin necesidad de crear estructuras desde cero.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>


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

### Mejoras de uso {#july-26-usability}

En esta versión se incluyen las siguientes mejoras en la facilidad de uso.

* **Métodos abreviados de inicio rápido para los canales SMS, Push, In-App y Codebase en las plantillas de contenido**: el botón **Más acciones** de la lista Plantillas de contenido ahora proporciona métodos abreviados adicionales específicos del canal. En el caso de las plantillas SMS, edite rápidamente el mensaje o compruebe el recuento o los segmentos de caracteres. En las plantillas push, edite el título, el cuerpo o los medios. Para las plantillas en la aplicación, edite el encabezado del mensaje, el cuerpo del mensaje o la URL de medios. Para las plantillas de canal de Codebase, edite el código directamente. Estos métodos abreviados amplían los métodos abreviados de inicio rápido del canal de correo electrónico que ya están disponibles. <!-- Documentation link: TBD -->
