---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 951056d22975a34af50faa450859d635b542f90f
workflow-type: tm+mt
source-wordcount: '1235'
ht-degree: 35%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión. [!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Notas de la versión de mayo de 2025 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### Nuevas funciones {#25-05-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Vista de calendario para el inventario de campañas y Recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una vista de calendario en las listas de recorridos y campañas. Permite visualizar todas las activaciones de recorridos y campañas en las listas respectivas.</p>
<p>Actualmente, este cambio solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para solicitar acceso, use <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">este formulario</a>.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>Para obtener más información, consulte estas secciones: <a href="../building-journeys/journey-ui.md">Examine y filtre sus recorridos</a>, <a href="../campaigns/modify-stop-campaign.md">Acceso a campañas</a>.</p>
<p>Fecha de disponibilidad: jueves, 28 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integración de fragmentos de contenido de Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con la integración de Adobe Experience Manager y Adobe Journey Optimizer, ahora puede utilizar sin esfuerzo fragmentos de contenido de Adobe Experience Manager dentro de su contenido de Journey Optimizer. Esta conexión perfecta facilita el acceso y el uso del contenido de AEM directamente en Journey Optimizer.</p>
<p>Esta capacidad, que antes estaba disponible para un conjunto limitado de organizaciones (LA), ahora es GA con la siguiente mejora:</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li-->
<li>Defina los marcadores de posición y asigne los valores de personalización dentro de la firma del fragmento con el modo Editor.</li>
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>Para obtener más información, consulte la <a href="../integrations/aem-fragments.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: sábado, 23 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integración de Dynamic Media de Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los recursos de Dynamic Media ahora están disponibles y son accesibles directamente en Journey Optimizer. Esta actividad le permite lo siguiente:</p>
<ul>
<li>Administre los recursos de forma centralizada con actualizaciones en tiempo real.</li>
<li>Modifique la configuración de los recursos, como la anchura y la altura, instantáneamente.</li>
<li>Personalice las plantillas de Dynamic Media actualizando el contenido y añadiendo campos de personalización.</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../integrations/aem-dynamic.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: sábado, 23 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>ID suplementario para recorridos activados por eventos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede almacenar en déclencheur los recorridos utilizando un ID de perfil junto con otro identificador, como un ID de pedido, un ID de suscripción o un ID de prescripción, lo que permite que el mismo perfil esté en el mismo recorrido varias veces a la vez. Esto permite situaciones como administrar varios pedidos o suscripciones en paralelo, y cada instancia sigue su propia ruta a través del recorrido.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/supplemental-identifier.md">documentación detallada</a>.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Fecha de disponibilidad: sábado, 23 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simular variaciones de contenido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente disponible en la versión Beta, ahora la simulación de variaciones de contenido ya está disponible de forma general (GA). Le permite obtener una vista previa de diferentes variaciones del contenido usando los datos de entrada de muestra cargados desde un archivo CSV o JSON o añadidos manualmente. El sistema detecta automáticamente todos los atributos utilizados en el contenido para la personalización y los puede utilizar en las pruebas para crear varias variantes.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de Disponibilidad general, la función ahora es compatible con experimentos de contenido y contenido multilingües, lo que le permite probar variaciones en diferentes idiomas y tratamientos. Además, ahora admite atributos contextuales (además de los atributos de perfil), lo que permite realizar pruebas de contenido aún más dinámicas y adaptadas a cada situación.</p>
<img src="assets/do-not-localize/variants.gif">
<p>Para obtener más información, consulte la <a href="../test-approve/simulate-sample-input.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: sábado, 23 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Sincronizar programación de lectura de audiencia con trabajo de segmentación por lotes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede almacenar en déclencheur las ejecuciones de recorridos diarias después de la finalización de la segmentación por lotes. Esta opción ahora está disponible en recorridos programados diariamente para todos los clientes. Permite definir para una ventana de tiempo de hasta 6 horas a la espera de datos de audiencia de trabajos de segmentación por lotes, lo que garantiza que los recorridos se ejecuten con los datos más actualizados o se omitan si no están listos.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>Para obtener más información, consulte la <a href="../building-journeys/read-audience.md#schedule">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: miércoles, 20 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Proveedor de SMS personalizado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora le permite configurar proveedores de SMS adicionales más allá de las opciones predeterminadas: Sinch, Infobip y Twilio. Con la configuración personalizada del proveedor de SMS, puede integrar proveedores de terceros directamente, aprovechar la personalización avanzada de la carga útil para la mensajería dinámica y administrar las preferencias de consentimiento (inclusión/exclusión) para garantizar el cumplimiento.</p>
<p>Para obtener más información, consulte la <a href="../sms/sms-configuration-custom.md">documentación detallada</a>.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Fecha de disponibilidad: miércoles, 20 de mayo de 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temas en el Designer de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aplicar rápidamente temas preaprobados para garantizar la coherencia de la marca en todos los correos electrónicos, acelerar el proceso de creación de campañas y producir correos electrónicos de alta calidad de forma independiente, al tiempo que reduce la dependencia en los equipos de diseño.</p>
<p>Actualmente, esta función está en versión beta y solo se encuentra disponible para los clientes de dicha versión. Para unirse al programa beta, póngase en contacto con su representante de Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Para obtener más información, consulte la <a href="../email/apply-email-themes.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: jueves, 14 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning: nuevo generador de fórmulas de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear fórmulas de clasificación de toma de decisiones específicas al definir y combinar criterios a partir de una nueva interfaz mejorada. En lugar de depender únicamente de una prioridad de oferta estática, puede definir fórmulas de clasificación personalizadas que combinen puntuaciones del modelo de IA, prioridades de oferta, atributos de perfil, atributos de oferta y señales contextuales a través de una interfaz guiada.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Para obtener más información, consulte la <a href="../experience-decisioning/exd-ranking-formulas.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: jueves, 14 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Conflict & prioritization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer, managing the volume and timing of campaigns and journeys is essential to avoid overwhelming customers with too many interactions. Journey Optimizer now offers several tools for conflict management and prioritization - previously available only to limited-access (LA) organizations - that are now generally available (GA).</p>
<p>Previously released in Limited Availability, this capability is now available to all environments. With this General Availability release, the following enhancements have been introduced:</p>
<ul>
<li>Expanded Support: Conflict management tools now support both Unitary Journeys and Audience Qualification Journeys, in addition to Read audience journeys.</li>
<li>Improved Troubleshooting: Two new step event fields are now available in the Query Service, enabling you to analyze why a profile was rejected from a journey or campaign.</li>
<li>Enhanced Reporting: Reports now indicate which specific rule excluded a profile from a journey or campaign, providing greater transparency and actionable insights.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>For more information, refer to the <a href="../conflict-prioritization/gs-conflict-prioritization.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->


<!--table>
<thead>
<tr>
<th><strong>Scale your Experimentation winner</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Scale the Winner enables you to automatically or manually roll out the winning variation of an experiment to your full audience. This feature ensures that, once a top performer is identified, you can maximize its reach and effectiveness without constant manual oversight.</p>
</td>
</tr>
</tbody>
</table-->


### Mejoras {#25-05-improv}

Las mejoras incluidas en esta versión se enumeran a continuación.


* **Nueva compatibilidad con objetos de campaña para la copia de zona protegida**. Fecha de disponibilidad: 15 de mayo de 2025

  Al copiar campañas en varios entornos limitados mediante las funciones de exportación e importación de paquetes, ahora también se copian las siguientes dependencias: configuraciones de canal, variantes y configuración de experimento, políticas de decisión y elementos. [Más información](../configuration/copy-objects-to-sandbox.md)

  <!--* **Decisioning** - Availability date: May 16, 2025

    Decisioning objects can now be copied between sandboxes, streamlining testing and deployment workflows. [Read more](../configuration/copy-objects-to-sandbox.md#decisioning)-->

* **Carpetas para páginas de aterrizaje** - Fecha de disponibilidad: 9 de mayo de 2025

  Para administrar fácilmente las páginas de aterrizaje, ahora puede utilizar carpetas para organizarlas de forma más eficaz en una jerarquía estructurada. [Más información](../landing-pages/manage-lp.md)

* **Correo directo: compatibilidad con claves SSH para conexiones SFTP**. Fecha de disponibilidad: 5 de mayo de 2025

  En la configuración de enrutamiento de archivos de correo postal, además del SFTP existente con tipo de autenticación por contraseña, ahora puede exportar el archivo de correo postal a un servidor SFTP con autenticación por clave SSH. [Más información](../direct-mail/direct-mail-configuration.md)

* Activación de **píldoras para personalización** - Fecha de disponibilidad: 5 de mayo de 2025

  Se ha añadido el nuevo botón “píldoras” al editor de personalización. Cuando se habilita, los atributos contextuales y de perfil se muestran como píldoras, lo que mejora la legibilidad del código. [Más información](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >Esta capacidad se implementará gradualmente en todos los entornos en los próximos 30 días.

* Compatibilidad con **&#39;Redireccionar a dirección URL&#39; en el canal Web** - Fecha de disponibilidad: 20 de mayo de 2025

  El canal Web de Journey Optimizer ahora permite redirigir a los visitantes a otra URL existente, en lugar de crear una nueva variación en el editor visual. Esta capacidad se puede utilizar para ejecutar experimentos comparando dos páginas completamente diferentes en lugar de cambiar solo unos pocos elementos dentro de una página. [Más información](../web/create-web.md#web-redirect-to-url)

* **Carpetas para plantillas y fragmentos** - Fecha de disponibilidad: 20 de mayo de 2025

  Las carpetas permiten organizar los objetos de forma más fácil y eficaz en una jerarquía estructurada. Las carpetas, que antes solo estaban disponibles para un conjunto de organizaciones (LA), ahora lo están para que todos los usuarios (GA) administren sus plantillas y fragmentos de contenido. Obtenga más información en las secciones [Plantillas de contenido](../content-management/access-content-templates.md#folders) y [Fragmentos](../content-management/manage-fragments.md#folders).

* **Seguimiento de clics en plantillas de correo electrónico** - Fecha de disponibilidad: 20 de mayo de 2025

  El rastreo de clics en `<area>` elementos dentro de los mapas de imagen en el contenido del correo electrónico ahora se admite de forma nativa en [!DNL Journey Optimizer]. Esto sirve para garantizar que las áreas de mapa de imagen reciban el mismo ajuste de seguimiento, datos de seguimiento y parámetros añadidos que los hipervínculos estándar. [Más información sobre el seguimiento de mensajes](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **Carril derecho en la lista de campañas** - Fecha de disponibilidad: 20 de mayo de 2025

  En la lista de campañas, al seleccionar una campaña, ahora se abre un panel que muestra sus detalles.

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.

* **Decision item attribute support for decisioning rules**
  
  You can now leverage decision item attributes to create decisioning rules.

* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->

