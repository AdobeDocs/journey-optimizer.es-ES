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
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: ht
source-wordcount: '3117'
ht-degree: 100%

---

# Notas de la versión de 2025 {#release-notes-2025}

Esta página enumera todas las funciones y mejoras de [!DNL Journey Optimizer] lanzadas en 2025.


## Notas de la versión de mayo de 2025 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### Nuevas funciones {#25-05-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Vista de calendario para el inventario de campañas y recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una vista de calendario en las listas de recorridos y campañas. Permite visualizar todas las activaciones de recorridos y campañas en las listas respectivas.</p>
<p>Ahora mismo, esta función solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para solicitar acceso, utilice <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">este formulario</a>.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>Para obtener más información, consulte estas secciones: <a href="../building-journeys/journey-ui.md">Examinar y filtrar sus recorridos</a>, <a href="../campaigns/modify-stop-campaign.md">Acceso a campañas</a>.</p>
<p>Fecha de disponibilidad: 28 de mayo de 2025</p>
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
<p>Anteriormente disponible para un conjunto limitado de organizaciones (LA), esta funcionalidad ahora es de disponibilidad general (GA) con la siguiente mejora: ahora puede definir marcadores de posición y asignar valores de personalización dentro de la firma del fragmento mediante el modo Editor.</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li>
<li>Define placeholders and map personalization values within the fragment signature using the Editor mode.</li-->
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>Para obtener más información, consulte la <a href="../integrations/aem-fragments.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 23 de mayo de 2025</p>
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
<li>Administrar centralmente los recursos con actualizaciones en tiempo real.</li>
<li>Modificar la configuración de los recursos, como la anchura y la altura, al instante.</li>
<li>Personalizar las plantillas de Dynamic Media actualizando el contenido y añadiendo campos de personalización.</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../integrations/aem-dynamic.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 23 de mayo de 2025</p>
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
<p>Ahora puede activar recorridos utilizando un ID de perfil junto con otro identificador, como un ID de pedido, un ID de suscripción o un ID de prescripción, lo que permite que el mismo perfil esté en el mismo recorrido varias veces a la vez. Esto permite situaciones como administrar varios pedidos o suscripciones en paralelo, y que cada instancia siga su propia ruta a través del recorrido.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/supplemental-identifier.md">documentación detallada</a>.</p>
<p>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Fecha de disponibilidad: 23 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulación de variaciones de contenido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<!--p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p-->
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con la versión de Disponibilidad general, la función ahora incluye compatibilidad con el contenido multilingüe y experimentos de contenido, lo que permite probar variaciones en diferentes idiomas y tratamientos. Además, ahora admite atributos contextuales (además de los atributos de perfil), lo que permite realizar pruebas de contenido aún más dinámicas y adaptadas a cada situación.</p>
<img src="assets/do-not-localize/variants.gif">
<p>Para obtener más información, consulte la <a href="../test-approve/simulate-sample-input.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 23 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Sincronización de la programación de público de lectura con el trabajo de segmentación por lotes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede activar ejecuciones de recorrido diarias tras la finalización de la segmentación por lotes. Esta opción ahora está disponible en los recorridos programados diariamente para todos los clientes. Le permite definir un período de tiempo de hasta 6 horas de espera de los datos del público procedentes de los trabajos de segmentación por lotes, lo que garantiza que los recorridos se ejecuten con los datos más actualizados o se omitan si no están listos. </p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>Para obtener más información, consulte la <a href="../building-journeys/read-audience.md#schedule">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 20 de mayo de 2025</p>
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
<p>Journey Optimizer ahora permite configurar proveedores de SMS adicionales más allá de las opciones predeterminadas: Sinch, Infobip y Twilio. Con la configuración personalizada del proveedor de SMS, puede integrar proveedores de terceros directamente, aprovechar la personalización avanzada de la carga útil para la mensajería dinámica y administrar las preferencias de consentimiento (inclusión/exclusión) para garantizar el cumplimiento.</p>
<p>Para obtener más información, consulte la <a href="../sms/sms-configuration-custom.md">documentación detallada</a>.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
<p>Fecha de disponibilidad: 20 de mayo de 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temas del Diseñador de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede aplicar rápidamente temas aprobados anteriormente para garantizar la coherencia de marca en todos los correos electrónicos, acelerar el proceso de creación de campañas y producir de forma independiente correos electrónicos de alta calidad, al tiempo que se reduce la dependencia en los equipos de diseño.</p>
<p>Actualmente, esta función está en versión Beta y solo se encuentra disponible para los clientes de dicha versión. Para unirse al programa beta, póngase en contacto con su representante de Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Para obtener más información, consulte la <a href="../email/apply-email-themes.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 14 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisiones: nuevo generador de fórmulas de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear fórmulas de clasificación de decisiones específicas definiendo y combinando criterios a partir de una nueva interfaz mejorada. En lugar de depender únicamente de una prioridad de oferta estática, puede definir fórmulas de clasificación personalizadas que combinen puntuaciones del modelo de IA, prioridades de oferta, atributos de perfil, atributos de oferta y señales contextuales a través de una interfaz guiada.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Para obtener más información, consulte la <a href="../experience-decisioning/ranking/ranking-formulas.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 14 de mayo de 2025</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#25-05-improv}

A continuación, se describen las mejoras incluidas en esta versión.


* **Nueva compatibilidad con objetos de campaña para copias en zonas protegidas**. Fecha de disponibilidad: 15 de mayo de 2025

  Cuando se copian campañas en varias zonas protegidas limitadas mediante las funciones de exportación e importación de paquetes, ahora también se copian las siguientes dependencias: configuraciones de canal, variantes y configuración de experimento, políticas de decisión y elementos. [Más información](../configuration/copy-objects-to-sandbox.md)

* **Carpetas para páginas de aterrizaje**. Fecha de disponibilidad: 9 de mayo de 2025

  Para administrar con facilidad las páginas de aterrizaje, ahora puede utilizar las carpetas para organizarlas de forma más eficaz en una jerarquía estructurada. [Más información](../landing-pages/manage-lp.md)

* **Correo directo: compatibilidad con claves SSH para conexiones SFTP**. Fecha de disponibilidad: 5 de mayo de 2025

  En la configuración de enrutamiento del archivo de correo directo, además del SFTP existente con el tipo de autenticación por contraseña, ahora puede exportar el archivo de correo directo a un servidor SFTP con la autenticación por clave SSH. [Más información](../direct-mail/direct-mail-configuration.md)

* **Activación de cápsulas para la personalización**. Fecha de disponibilidad: 5 de mayo de 2025

  Se ha añadido el nuevo botón “píldoras” al editor de personalización. Cuando se habilita, los atributos contextuales y de perfil se muestran como píldoras, lo que mejora la legibilidad del código. [Más información](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >Esta capacidad se implementará gradualmente en todos los entornos en los próximos 30 días.

* **Compatibilidad con “Redireccionar a URL” en el canal web** - Fecha de disponibilidad: 20 de mayo de 2025

  El canal web de Journey Optimizer ahora le permite redirigir a los visitantes a otra URL existente, en lugar de crear una nueva variación en el editor visual. Esta funcionalidad se puede utilizar para ejecutar experimentos comparando dos páginas completamente diferentes en lugar de cambiar solo unos pocos elementos dentro de una página. [Más información](../web/create-web.md#web-redirect-to-url)

* **Carpetas para plantillas y fragmentos**: fecha de disponibilidad: 20 de mayo de 2025

  Las carpetas permiten organizar los objetos de forma más fácil y eficaz en una jerarquía estructurada. Las carpetas, que antes solo estaban disponibles para un conjunto de organizaciones (LA), ahora lo están para que todos los usuarios (GA) administren sus plantillas y fragmentos de contenido. Obtenga más información en las secciones [Plantillas de contenido](../content-management/access-content-templates.md#folders) y [Fragmentos](../content-management/manage-fragments.md#folders).

* **Rastreo de clics en plantillas de correo electrónico** - Fecha de disponibilidad: 20 de mayo de 2025

  El rastreo de clics en elementos `<area>` dentro de mapas de imagen en el contenido de correo electrónico ahora se admite de forma nativa en [!DNL Journey Optimizer]. Esto sirve para garantizar que las áreas de mapa de imagen reciban el mismo encapsulado de seguimiento, datos de seguimiento y parámetros añadidos que los hipervínculos estándar. [Obtenga más información sobre el seguimiento de mensajes](../email/message-tracking.md#manage-tracking).

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **Carril derecho en la lista de campañas** - Fecha de disponibilidad: 20 de mayo de 2025

  Al seleccionar una campaña de la lista, se abre el panel que muestra sus detalles.

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.-->

<!--* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->



## Notas de la versión de abril de 2025 {#25-4-rn}

**Fecha de lanzamiento**: del 29 al 30 de abril de 2025

### Nuevas funciones {#25-04-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Editor de personalización: Aprenda haciendo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ya está disponible un área de reproducción de personalización, donde puede experimentar con expresiones de personalización. Le permite explorar plantillas y cargas útiles de ejemplo para ayudarle a empezar y probar sus propias expresiones de personalización.</p>
<p>Para obtener más información, consulte la <a href="../personalization/personalize.md#playground">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 24 de abril de 2025</p>
<img src="assets/do-not-localize/templating-playground.gif"/>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Adobe Experience Manager as a Cloud Service integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The integration between Adobe Journey Optimizer and Adobe Experience Manager as a Cloud Service is now released in General Availability (GA). This integration enables seamless content sourcing and management for personalized customer journeys.</p>
<p>For more information, refer to the <a href="../integrations/aem-templates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>Simulate content variations (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>With the General Availability release, the feature now includes support for multilingual content and content experiments, enabling you to test variations across different languages and treatments. Additionally, it now supports contextual attributes (in addition to profile attributes), allowing for even more dynamic and situational content testing.</p>
<img src="assets/do-not-localize/variants.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Canal LINE</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ha ampliado sus funcionalidades en canales múltiples para incluir la compatibilidad con el canal LINE. Esta mejora le permite crear, editar y previsualizar experiencias de LINE, permitiendo interacciones más personalizadas y atractivas. Con LINE, puede conectarse con más clientes, enviar contenido relevante y mejorar su participación.</p>
<p>El canal LINE está habilitado para los clientes de Adobe Journey Optimizer previa solicitud. Póngase en contacto con el Servicio de atención al cliente de Adobe o con su representante de Adobe para activar la función para su organización.</p>
<p>Para obtener más información, consulte la <a href="../line/get-started-line.md">documentación detallada</a>.</p></td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Custom SMS provider (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports custom SMS providers, allowing you to integrate your preferred SMS services for enhanced communication flexibility.</p>
<p>For more information, refer to the <a href="../sms/sms-configuration-custom.md">detailed documentation</a>.</p></td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Métricas de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las métricas de recorrido ya están disponibles, lo que le permite medir el impacto de sus actividades en las métricas clave de su empresa y proporcionar una perspectiva más clara de su rendimiento.</p>
</br>
<img src="assets/do-not-localize/success-metric.gif"/>
<p>Para obtener más información, consulte la <a href="../building-journeys/success-metrics.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 9 de abril de 2025</p>
</td>
</tr>
</tbody>
</table>



<!--<table>
<thead>
<tr>
<th><strong>Calendar view for campaign and journey inventory (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new calendar view is now available for campaigns and journey activations. This feature provides a visual representation of scheduled activities, allowing you to view and manage your campaigns and journeys more effectively. Selecting a calendar item opens a right rail with detailed information. This feature is currently in Limited Availability.</p>
<img src="assets/do-not-localize/calendar.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Integración de Adobe Express (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ahora se integra con Adobe Express, lo que le permite conectar sin problemas sus recursos creativos con la orquestación de recorrido. Esta integración simplifica el proceso de diseño e implementación de contenido personalizado en todas las campañas. </p>
<p>Esta integración no está disponible actualmente para su uso con Healthcare Shield o Privacy and Security Shield.</p>
<img src="assets/do-not-localize/express_resize.gif">
<p>Para obtener más información, consulte la <a href="../integrations/express.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activación de ejecuciones de recorrido diarias tras la finalización de la segmentación por lotes (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En el caso de los recorridos programados diariamente, una nueva opción le permite definir un intervalo de tiempo de hasta 6 horas para esperar los datos de audiencia de los trabajos de segmentación por lotes, lo que garantiza que los recorridos se ejecuten con los datos más actualizados o se omitan si no están listos. La opción Activar tras evaluación de público por lotes solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/read-audience.md#schedule">documentación detallada</a>.</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Themes in the Email Designer (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply pre-approved styling themes to your email content to ensure brand consistency across all emails, speed up your campaign creation process and independently produce hight-quality emails while reducing dependency on design teams.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Puntuación de alineación con la marca (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La función de puntuación de alineación de marca proporciona comentarios claros directamente en el Diseñador de correo electrónico, lo que le ayuda a ver si el contenido se ajusta al tono, al estilo y a las directrices de la marca. Esta función está disponible en Beta.</p>
<p>Para obtener más información, consulte la <a href="../content-management/brands-score.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/brand-score.gif">
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decisioning - New AI formula builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create specific Decisioning ranking formulas by defining and combining criteria from a new improved interface. Ranking formulas allow you to define rules that will determine which decision items should be presented first, rather than taking into account the priority scores.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table>
-->

### Mejoras {#25-04-improv}

**API de vista previa de campañas**

Hay nuevas API disponibles para previsualizar campañas, además de las capacidades de envío de pruebas existentes. [Más información](https://developer.adobe.com/journey-optimizer-apis/references/simulations/#operation/createCampaignPreview){target="_blank"}.

**Herramientas de la zona protegida**

* **Herramientas de zona protegida para acciones personalizadas**

  Las acciones personalizadas ahora se incluyen en la lista de objetos de Adobe Journey Optimizer que se pueden copiar mediante la función de herramientas de zona protegida, lo que optimiza las pruebas y la implementación. [Más información](../configuration/copy-objects-to-sandbox.md)

* **Herramientas de zona protegida para campañas**. Fecha de disponibilidad: 3 de abril de 2025

  Ahora puede copiar campañas en varias zonas protegidas mediante las funciones de exportación e importación de paquetes. Las campañas se copian junto con todos los elementos relacionados con el perfil, el público, el esquema, los mensajes en línea y los objetos dependientes. Algunos elementos no se copian, como los elementos de decisión, las etiquetas de uso de datos y la configuración de idioma. [Más información](../configuration/copy-objects-to-sandbox.md#custom-actions)

**Personalización**

* **Nuevo atributo contextual**

  Ahora hay disponible un nuevo atributo contextual, **ID de perfil de mensaje**, que se puede seleccionar en el editor de personalización. Es un atributo orientado a mensajes que identifica de forma exclusiva cada mensaje enviado a cada perfil de destino en un envío. Este identificador único se puede utilizar, por ejemplo, como parámetro de seguimiento de URL para distinguir cada vínculo abierto o en el que los destinatarios hacen clic.

* **Atributos rellenados en el panel de atributos**. Fecha de disponibilidad: 2 de abril de 2025

  El panel de atributos del editor de personalización ahora muestra solo los atributos rellenados de forma predeterminada. Para ver todos los atributos, use el botón de configuración para desactivar la opción **[!UICONTROL Mostrar solo atributos rellenados]**. [Más información](../personalization/personalization-build-expressions.md)

**Canal de correo electrónico**

* **Seguimiento personalizado de URL**. Fecha de disponibilidad: 30 de abril de 2025

  Para obtener una mayor flexibilidad y control sobre la configuración del correo electrónico, ahora puede personalizar todos los parámetros de seguimiento de URL a la vez a nivel de configuración de canal de correo electrónico, en lugar de hacerlo en el Diseñador de correo electrónico para cada vínculo del contenido. [Más información](../email/surface-personalization.md#personalize-url-tracking)

* **Diseñador de correo electrónico**. Fecha de disponibilidad: 1 de abril de 2025

  Para mejorar la accesibilidad en Journey Optimizer, ahora hay dos campos nuevos disponibles en Diseñador de correo electrónico: se corresponden con el elemento `<title>` y el atributo `lang` en el elemento `<html>` del contenido del correo electrónico. Puede definir esta configuración, además del campo **[!UICONTROL Preencabezado]**, en la sección **[!UICONTROL Cuerpo]** del correo electrónico. [Más información](../email/email-metadata.md)

**Manuales de tácticas de casos de uso**

* **Creación y uso compartido de manuales de tácticas (Private Beta)**: ahora puede crear, administrar y compartir sus propios manuales de tácticas de casos de uso. Ahora mismo, esta función solo está disponible para un conjunto de organizaciones como Private Beta. Para obtener acceso, póngase en contacto con su representante de Adobe. [Más información](../start/playbooks.md)

**Navegación**

* **Administración de contenido**. Fecha de disponibilidad: 2 de abril de 2025

  Para administrar con facilidad los fragmentos y las plantillas de contenido, ahora puede utilizar carpetas para organizarlos de forma más eficaz en una jerarquía estructurada. Obtenga más información en las secciones [Fragmentos](../content-management/manage-fragments.md#folders) y [Plantillas de contenido](../content-management/access-content-templates.md#folders)

  >[!AVAILABILITY]
  >
  >Esta mejora solo está disponible para un conjunto de organizaciones (disponibilidad limitada).

<!--- **Folders for content templates and fragments** - Availability date: May 5, 2025

  Previously available for a set of organizations (LA), folders are now available to all users (GA) to manage their content templates and fragments. Folders let you organize your content templates and fragments more easily and effectively into a structured hierarchy.



<!--- **Right rail in campaigns list**  

  A right rail has been added to the campaigns list, providing detailed information when a campaign is selected.-->

<!--**Playbooks**

- **Create your own playbooks (Beta)**
  
  You can now create your own playbooks in Adobe Journey Optimizer, enabling greater customization and flexibility in journey planning.-->



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
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
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
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
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

Ahora puede usar la restricción de frecuencia diaria en recorridos y campañas con la segmentación por lotes. Para garantizar la precisión de las reglas de restricción de frecuencia diaria, asegúrese de elegir el espacio de nombres de prioridad más alta durante la creación de una campaña o recorrido. Obtenga más información sobre la prioridad del espacio de nombres en la [Guía del servicio de identidad de Platform](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}

Como recordatorio, la restricción de frecuencia diaria en los conjuntos de reglas solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

Para obtener más información sobre las reglas empresariales, consulte la [documentación detallada](../conflict-prioritization/rule-sets.md).

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
<p>Para obtener más información, consulte la <a href="../conflict-prioritization/rule-sets.md">documentación detallada</a>.</p>
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
<p>Ahora puede crear contenido atractivo para sus páginas de aterrizaje, incluidos diseños de página completa, texto personalizado e imágenes personalizadas, con la ayuda del Asistente de IA.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>Para obtener más información, consulte la <a href="../content-management/generative-lp.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Marcas con el asistente de IA (Beta)</strong><br/></th>
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
