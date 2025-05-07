---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión de 2025
description: Notas de la versión de Journey Optimizer 2025
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: aa8c74de-748b-4947-a972-14703f6ab4a7
source-git-commit: 0f3191a3d7c5c78e1d8fac2e587e26522f02f8f5
workflow-type: tm+mt
source-wordcount: '1237'
ht-degree: 100%

---

# Notas de la versión de 2025 {#release-notes-2025}

Esta página enumera todas las funciones y mejoras de [!DNL Journey Optimizer] lanzadas en 2025.

## Notas de la versión de marzo de 2025 {#25-3-rn}

### Nuevas funciones {#25-03-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<!--table>
<thead>
<tr>
<th><strong>Integration with Adobe Express (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Adobe Express integration in Adobe Journey Optimizer lets you use Adobe Express's editing tools directly during content creation, enabling you to resize, remove backgrounds, crop, and convert assets to JPEG or PNG.<p>
<p>Adobe Express integration in Adobe Journey Optimizer is currently only available for a set of organizations (Limited Availability). It cannot be deployed for use with Healthcare Shield or Privacy and Security Shield.</p>
<p>For more information, refer to the <a href="../integrations/express.md">detailed documentation</a>.</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Journey metrics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey metrics are now available, allowing you to measure the impact of your activities across the key metrics of your business and to provide clearer insights into your performance.</p>
<p>For more information, refer to the <a href="../building-journeys/success-metrics.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table-->

<!-- table>
<thead>
<tr>
<th><strong>Calendar view for journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A calendar view is now available in Journey Optimizer to visualize all journeys activations. From this view, you can browse your journeys and check details and properties.<p>
<p>This change is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Integración con Dynamic Media (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los recursos de Dynamic Media ahora están disponibles y son accesibles directamente en Journey Optimizer. Esta actividad le permite lo siguiente:
<ul>
<li>Administrar centralmente los recursos con actualizaciones en tiempo real</li>
<li>Modificar la configuración de los recursos, como la anchura y la altura, al instante</li>
<li>Personalizar las plantillas de Dynamic Media actualizando el contenido y añadiendo campos de personalización</li>
</ul>
<p>
<p>Esta integración solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../integrations/aem-dynamic.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Integración con Adobe GenStudio (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Para mejorar la eficacia del marketing y mantener la coherencia de marca, ahora puede integrar sin problemas las experiencias de GenStudio for Performance Marketing con Journey Optimizer. Esto le permite aprovechar la creación de contenido con tecnología de IA de GenStudio junto con las funcionalidades de orquestación avanzadas de Journey Optimizer.<p>
<p>El uso de la integración de GenStudio en Journey Optimizer no está disponible actualmente con Healthcare Shield o Privacy and Security Shield (disponibilidad limitada).</p>
<p>Para obtener más información, consulte la <a href="../integrations/genstudio.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Evaluación de público flexible (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente disponible para un conjunto de organizaciones (LA), la evaluación de público flexible ya está disponible para todos los usuarios (GA). Esta función le permite ejecutar un trabajo de segmentación bajo demanda para los públicos seleccionados, lo que garantiza que siempre tenga los datos de público más actualizados antes de segmentarlos en recorridos y campañas de Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Para obtener más información, consulte la <a href="../audience/creating-a-segment-definition.md#flexible">documentación detallada</a>.</p>
</tr>
</tbody>
</table>
</table>

<!--table>
<thead>
<tr>
<th><strong>LINE channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer has expanded its cross-channel capabilities to include support for the LINE channel. This enhancement allows you to create, edit, and preview LINE experiences enabling more personalized and engaging interactions. With LINE, you can connect with more customers, send relevant content, and improve your engagement.<p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


### Mejoras {#25-03-improv}

**Editor de personalización** (fecha de disponibilidad: 12 de marzo)

El editor de personalización de Journey Optimizer se ha actualizado con nuevas funciones:
* **Diseño actualizado del editor de código**: una interfaz más clara y moderna para mejorar la facilidad de uso y el enfoque.
* **Buscar y reemplazar**: funcionalidad añadida para buscar y reemplazar contenido rápidamente en el editor.
* **Compatibilidad con Deshacer y Rehacer**: permite revertir o volver a aplicar fácilmente los cambios.
* **Tamaño de fuente personalizable**: habilita el ajuste del tamaño de fuente del editor para mejorar la legibilidad.
* **Validación JSON en línea**: proporciona validación en tiempo real del lado del cliente para el contenido JSON a fin de acelerar la detección de errores.
* **Completar automáticamente atributos de perfil y contexto**: ofrece sugerencias inteligentes para optimizar la creación de contenido.
* **Resaltado de sintaxis mejorado**: mejora la legibilidad al hacer que la estructura del código quede visualmente más diferenciada.

![Vídeo que muestra la nueva función en el editor de personalización](assets/do-not-localize/personalization-editor.gif)

Para obtener más información, consulte la [documentación detallada](../personalization/personalization-build-expressions.md).

**Aprobaciones**

Al definir las condiciones de una directiva de aprobación, ahora tiene la opción de filtrar por etiqueta o categoría de objeto.

Para obtener más información, consulte la [documentación detallada](../test-approve/approval-policies.md).

**Configuración**

* Ahora puede asignar las etiquetas unificadas de Adobe Experience Platform a las configuraciones de canal. Esto le permite clasificarlas con facilidad y mejorar la búsqueda y la navegación en todas las listas. [Más información](../configuration/channel-surfaces.md#channel-config-tags)

* Al configurar o editar un subdominio de correo electrónico en Journey Optimizer, ahora puede elegir administrar el registro DMARC asociado por su cuenta, si está disponible en el dominio principal. [Más información](../configuration/dmarc-record.md#set-up-dmarc)

**Reglas empresariales**

Ahora puede usar la restricción de frecuencia diaria en recorridos y campañas con la segmentación por lotes. Para garantizar la precisión de las reglas de restricción de frecuencia diaria, asegúrese de elegir el espacio de nombres de prioridad más alta durante la creación de una campaña o recorrido. Obtenga más información sobre la prioridad del espacio de nombres en la [guía del servicio de identidad de Platform](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}

Como recordatorio, la restricción de frecuencia diaria en los conjuntos de reglas solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

Para obtener más información sobre las reglas empresariales, consulte la [documentación detallada](../configuration/rule-sets.md).

**Plantillas de contenido**

Las plantillas de contenido de tipo HTML ya no se utilizan. Tenga en cuenta que aún puede usar plantillas de contenido de HTML existentes creadas anteriormente en [!DNL Journey Optimizer]. [Más información sobre las plantillas de contenido](../content-management/content-templates.md)


<!--**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->




## Notas de la versión de febrero de 2025 {#25-02-rn}

**Fecha de lanzamiento**: 18-19 de febrero de 2025


### Nuevas funciones {#25-02-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Crear y administrar reglas empresariales</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear reglas empresariales utilizando conjuntos de reglas. Los conjuntos de reglas son grupos de reglas que ayudan a limitar los mensajes enviados dentro de las campañas y las acciones de recorrido entre canales, así como para controlar las entradas de perfiles en los recorridos.<p>
<p><ul><li>Cree conjuntos de reglas de canal para restringir el número de mensajes enviados a través de uno o varios canales. Aplíquelas a campañas o acciones de recorrido para aplicar las reglas definidas en el conjunto de reglas. El conjunto de reglas de canal le permite aplicar reglas de límite basadas en tipos de comunicación. Por ejemplo, defina una regla para limitar los “mensajes promocionales” y otra para los “boletines”. Aplique el conjunto de reglas adecuado en la campaña o acción de recorrido según el tipo de comunicación que envíe.</li>
<li> Cree conjuntos de reglas de recorrido para controlar las entradas de perfil en los recorridos. Limite la frecuencia con la que un perfil puede entrar en un recorrido dentro de un período determinado o el número de recorridos en los que se puede inscribir un perfil simultáneamente. Aplíquelas en el nivel de recorrido para garantizar una administración de entrada adecuada.</li></ul></p>
<p>Las reglas empresariales, que anteriormente estaban disponibles para un conjunto de organizaciones (LA), ya están disponibles para todos los usuarios (GA). Las reglas empresariales del dominio de recorrido siguen estando disponibles únicamente para un conjunto limitado de organizaciones (LA).</p>
<p>Para obtener más información, consulte la <a href="../configuration/rule-sets.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Generación de páginas de aterrizaje con el Asistente de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear contenido atractivo para sus páginas de aterrizaje, incluidos diseños de página completa, texto personalizado y elementos visuales personalizados, con la ayuda del Asistente de IA.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>Para obtener más información, consulte la <a href="../content-management/generative-lp.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Marcas con el Asistente de IA (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede configurar sus propias marcas para definir la identidad visual y verbal de su marca. </p>
<p>Esta capacidad se presenta como una versión beta privada para un conjunto limitado de clientes. Estará disponible de forma progresiva para todos los clientes en futuras versiones.</p>
<p>Para obtener más información, consulte la <a href="../content-management/brands.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Resolución de problemas de acciones personalizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede validar una configuración de acción personalizada realizando llamadas de API reales directamente desde Adobe Journey Optimizer. Esta nueva funcionalidad le ayuda a solucionar los problemas de las acciones personalizadas antes o después de utilizarlas en un recorrido.  </p>
<p>Para obtener más información, consulte la <a href="../action/troubleshoot-custom-action.md">documentación detallada</a>.</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Evaluación de público flexible (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La evaluación de público flexible le permite ejecutar un trabajo de segmentación bajo demanda para los públicos seleccionados, lo que garantiza que siempre tenga los datos de público más actualizados antes de segmentarlos en recorridos y campañas de Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Para obtener más información, consulte la <a href="../audience/creating-a-segment-definition.md#flexible">documentación detallada</a>.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Fecha de disponibilidad: 28 de enero de 2025</p>
</tr>
</tbody>
</table>
</table>


### Mejoras {#25-02-improvements}

Las mejoras que se muestran a continuación están incluidas en la actualización de febrero.

* **Tiempo de vida del conjunto de datos (TTL)**: a partir de este mes, se implementará un mecanismo de protección de tiempo de vida (TTL) en los conjuntos de datos generados por el sistema de Journey Optimizer en las nuevas zona protegidas y organizaciones de la siguiente manera:

   * 90 días para los datos en el almacén de perfiles
   * 13 meses para los datos en el lago de datos

  Este cambio se implementará en las zonas protegidas de clientes existentes en una fase posterior. 

  Obtenga más información sobre esta actualización en [las preguntas más frecuentes](../data/datasets-ttl.md#frequently-asked-questions).

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **Correo postal**: ahora se admite un nuevo tipo de servidor, la zona de aterrizaje de datos, para el enrutamiento de archivos en la configuración del canal de correo postal. [Más información](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **SMS**: ahora puede administrar el envío de mensajes SMS desde puntos finales multiregionales anulando las direcciones URL de envío, comentarios, entrada y devolución de llamada. Para admitir esto, se ha añadido nuevo campo Anular URL a la configuración de Credenciales de API. Este cambio solo está disponible con el proveedor Sinch. [Más información](../sms/sms-configuration-sinch.md)

* **Personalización** (fecha de disponibilidad: 29 de enero de 2025): hay nuevas funciones de ayuda de fecha y hora disponibles para usar en el editor de personalización. [Más información](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **Configuración de correo electrónico**: si administra el consentimiento fuera de Adobe, ahora puede establecer una dirección de correo electrónico de cancelación de suscripción personalizada y una URL de cancelación de suscripción de un solo clic personalizada como parte de los ajustes de la configuración de canal de correo electrónico.[Más información](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Toma de decisiones** (fecha de disponibilidad: 28 de enero de 2025): la toma de decisiones ahora admite tipos de datos de objeto al editar el esquema del catálogo de elementos. [Más información](../experience-decisioning/catalogs.md)
