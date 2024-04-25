---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la primera versión de Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: acd195e669d653b52ba7722e9e01db28a5a7d2b7
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 34%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md) y en la fecha.

## Notas de la versión anteriores de abril de 2024 {#e-2024}

**Fecha de lanzamiento**: 30 de abril de 2024

### Nuevas funciones {#e-features}

Esta versión incorpora las nuevas funciones detalladas a continuación.

<!--table>
<thead>
<tr>
<th><strong>Business rules - Private Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>It is now possible to create and apply rule sets to your marketing communications.  </p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Experience Decisioning: disponibilidad limitada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experience Decisioning simplifica la personalización al ofrecer un catálogo centralizado de ofertas de marketing conocidas como "elementos de decisión" y un motor de decisión sofisticado. Este motor aprovecha las reglas y los criterios de clasificación para seleccionar y presentar los elementos de decisión más relevantes a cada individuo.</p>
<p>Estos elementos de decisión se integran perfectamente en una amplia gama de superficies entrantes a través del nuevo canal de experiencia basado en código, ahora accesible dentro de las campañas de Journey Optimizer. Las políticas de decisión de Experience Decisioning solo están disponibles para su uso en campañas de experiencia basadas en código.</p>
<p>Actualmente, Experience Decisioning solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con el representante del Adobe.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Personalization - Local Lookups - Multi-Entity Support - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>TBD</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Servicio de mensajes multimedia (MMS) con Infobip</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con el canal SMS, ahora puede mejorar su comunicación enviando mensajes del servicio de mensajes multimedia (MMS), lo que le permite compartir imágenes, GIF o vídeos con sus clientes. Esta función, que antes solo estaba disponible con Sinch, ahora también está disponible con Infobip.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow - LA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now easily perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### Mejoras {#e-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

<!--
* **Experience Decisioning + Code-based experiences (LA)**: You can now leverage the Experience decisioning feature to use decision items in your code-based campaigns. Note: The Code-based experience channel and Experience decisioning are not available for organizations that have purchased the Adobe Healthcare Shield and Privacy and Security Shield add-on offerings.
-->
<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**Gestión de decisiones**

* El **Registro de cambios** que le permite ver todos los cambios realizados en una oferta o que se ha eliminado una decisión. Los cambios relacionados con ofertas y decisiones ahora se pueden ver en la **Auditorías** menú.

**Experience Decisioning**

De la versión beta a LA, se han agregado las siguientes mejoras:

* Ahora puede aprovechar los datos de contexto de Adobe Experience Platform en las reglas de decisión utilizando **Datos de contexto** pestaña.
* Ya está disponible un nuevo permiso para &quot;Administrar decisiones de experiencia&quot; para el recurso Administración de decisiones. Permite administrar derechos relacionados con Experience Decisioning.
* Ahora puede agregar varias reglas de límite para una oferta. De este modo, aumenta el nivel de control sobre la forma en que se envían las ofertas.
* Ahora puede agregar varias reglas de límite para un elemento de decisión determinado en Experience Decisioning. De este modo, aumenta el nivel de control sobre la forma en que se envían las ofertas.
* Ahora puede crear paneles de informes personalizados de campañas de Experience Decisioning mediante [!DNL Customer Journey Analytics].

**Recorridos**

* **Diseñador de Recorridos mejorado**

   * La interfaz de usuario del lienzo mejorada proporciona una experiencia de usuario más intuitiva y eficaz.
   * Las actividades son más claras y presentan más información en el lienzo del recorrido con menos clics.

* **Nuevos informes en directo**: Ahora se puede acceder directamente a los informes de recorrido de las últimas 24 horas en el lienzo de Recorrido.

Configuración de ****

* Ahora puede seleccionar una acción de marketing en el nivel de superficie de canal. Cuando se utilizan en una superficie, todas las políticas de consentimiento asociadas con esa acción de marketing se aprovechan para respetar las preferencias de los clientes.
* El uso del Control de acceso de nivel de objeto ya está disponible para superficies de canal.

