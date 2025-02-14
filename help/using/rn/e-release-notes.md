---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión preliminar
description: Notas de la primera versión de Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 4e405fe395c8432ed22d64887631b222df83a3e9
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 21%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento**. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md) y en la fecha.

## Notas de la versión anteriores de febrero de 2025 {#25-02-rn}

### Nuevas funciones {#25-02-features}

A continuación se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Crear y administrar reglas de negocio</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear reglas de negocio utilizando conjuntos de reglas. Los conjuntos de reglas son grupos de reglas que ayudan a limitar los mensajes enviados dentro de las campañas y las acciones de recorrido entre canales, así como para controlar las entradas de perfiles en los recorridos.<p>
<p><ul><li>Cree conjuntos de reglas de canal para restringir el número de mensajes enviados a través de uno o varios canales. Aplíquelas a campañas o acciones de recorrido para aplicar las reglas definidas en el conjunto de reglas. El conjunto de reglas de canal le permite aplicar reglas de límite basadas en tipos de comunicación. Por ejemplo, defina una regla para limitar los "mensajes promocionales" y otra para los "boletines". Aplique el conjunto de reglas adecuado en la campaña o acción de recorrido según el tipo de comunicación que envíe.</li>
<li> Cree conjuntos de reglas de recorrido para controlar las entradas de perfil en los recorridos. Limite la frecuencia con la que un perfil puede entrar en un recorrido dentro de un periodo determinado o el número de recorridos en los que se puede inscribir un perfil simultáneamente. Aplíquelas en el nivel de recorrido para garantizar una administración de entrada adecuada.</li></p>
<p>Anteriormente disponibles para un conjunto de organizaciones (LA), las reglas empresariales ahora están disponibles para todos los usuarios (GA).</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Compatibilidad multiregional con SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede administrar el envío de mensajes SMS desde puntos de conexión multirregionales anulando las direcciones URL de envío, comentarios, entrada y devolución de llamada. Para admitir esto, se ha agregado un nuevo campo Anular URL a la configuración de Credenciales de API. Este cambio solo está disponible con el proveedor Sinch.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Generación de páginas de aterrizaje con el asistente de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El asistente de IA ya está disponible con las entregas de la página de aterrizaje, lo que le permite generar texto, imágenes o diseños de página completos.</p>
<!--img src="assets/do-not-localize/ai-lp.gif">
<p>For more information on AI Assistant, refer to the <a href="../email/generative-lp.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Directrices de marca (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede establecer sus propias directrices de marca para definir la identidad visual y verbal de su marca. Tenga en cuenta que la función Marcas se presenta como una versión beta privada y estará disponible de forma progresiva para todos los clientes en futuras versiones.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Evaluación flexible de audiencias (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La evaluación de audiencias flexible le permite ejecutar un trabajo de segmentación bajo demanda para audiencias seleccionadas, lo que garantiza que siempre tenga los datos de audiencia más actualizados antes de segmentarlos en recorridos y campañas de Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Para obtener más información, consulte la <a href="../audience/about-audiences.md#flexible">documentación detallada</a>.</p>
<p> La evaluación flexible de audiencias solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Fecha de disponibilidad: 28 de enero de 2025</p>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Plantillas de Customer Journey Analytics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora tiene la opción de mejorar los informes de Journey Optimizer mediante plantillas de Customer Journey Analytics. Esta nueva función le permite optimizar el proceso de creación de informes con plantillas prediseñadas adaptadas a sus necesidades de análisis.
</p>
<img src="assets/do-not-localize/cja-templates.gif">
<p>Para obtener más información, consulte la <a href="../reports/report-cja-manage.md#cja-template">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: a partir del 15 de enero de 2025</p>
</tr>
</tbody>
</table>




### Mejoras {#25-02-improvements}

Las mejoras que se indican a continuación se proporcionan con la actualización de febrero.

* **Recorridos**: ahora puede probar sus acciones personalizadas enviando llamadas de API desde la sección de administración. Esta nueva funcionalidad le ayuda a solucionar problemas de las acciones personalizadas antes o después de usarlas en un recorrido.

* **Tiempo de vida del conjunto de datos (TTL)**: a partir de este mes, se implementará una protección de tiempo de vida (TTL) en los conjuntos de datos generados por el sistema de Journey Optimizer en los nuevos entornos limitados y en las nuevas organizaciones de la siguiente manera:

   * 90 días para los datos en el almacén de perfiles
   * 13 meses para los datos en el lago de datos

  Este cambio se implementará en las zonas protegidas de clientes existentes en una fase posterior.

  Obtenga más información sobre esta actualización en [estas preguntas frecuentes](../data/datasets-ttl.md#frequently-asked-questions).

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **Correo postal**: ahora se admite un nuevo tipo de servidor, la zona de aterrizaje de datos, para el enrutamiento de archivos en la configuración del canal de correo postal.

**Personalización**

<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->

* Fecha de disponibilidad: 29 de enero de 2025. Hay nuevas funciones de ayuda de fecha y hora disponibles para su uso en el editor de personalización. [Más información](../personalization/functions/dates.md)

**Configuración de correo electrónico** - Fecha de disponibilidad: 12 de febrero de 2025

* Si administra el consentimiento fuera de Adobe, ahora puede establecer una dirección de correo electrónico personalizada para cancelar la suscripción y una URL personalizada para cancelar la suscripción con un solo clic como parte de la configuración de su canal de correo electrónico. [Más información](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

**Toma de decisiones** - Fecha de disponibilidad: 28 de enero de 2025

* La toma de decisiones ahora admite tipos de datos de objeto al editar el esquema del catálogo de elementos. [Más información](../experience-decisioning/catalogs.md)