---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión 2022
description: Notas de la versión de Journey Optimizer 2022
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '3479'
ht-degree: 0%

---

# Notas de la versión 2022 {#release-notes-2022}

Esta página enumera todas las funciones y mejoras de [!DNL Journey Optimizer] lanzado en 2022.


## Versión de septiembre de 2022{#sept-2022-release}

### Nuevas funciones{#sept-2022-features}

<table>
<thead>
<tr>
<th><strong>Contenido dinámico y nuevo generador de reglas condicionales</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear contenido dinámico para adaptar el contenido de los mensajes en función de reglas condicionales.</p> 
<p>Las reglas condicionales se crean mediante un generador de reglas visual dentro del Editor de expresiones, donde puede almacenarlas para su reutilización en los recorridos y campañas.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>Para obtener más información, consulte <a href="../personalization/get-started-dynamic-content.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campañas activadas por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Además de las campañas programadas existentes, ahora puede crear campañas activadas por API en Journey Optimizer e invocarlas desde un sistema externo mediante API.</p>
<p>Esto le permite cubrir diversas necesidades operativas y de mensajería transaccional, como los restablecimientos de contraseña, el token OTP, entre otras.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Para obtener más información, consulte <a href="../campaigns/api-triggered-campaigns.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Control de acceso a datos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mediante el control de acceso basado en atributos, los administradores pueden controlar el acceso a objetos específicos en función de determinados atributos. Estos atributos pueden ser metadatos agregados a un objeto, como etiquetas. A partir de esta versión, los administradores también pueden definir funciones de usuario que solo tengan acceso a campos u objetos específicos, y datos que correspondan a esos campos u objetos.</p>
<p> El uso del control de acceso basado en atributos está actualmente restringido a clientes seleccionados y se implementará en todos los entornos en una versión futura.</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>Para obtener más información, consulte <a href="../administration/object-based-access.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Administración de datos y privacidad</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con su marco de control de etiquetado y aplicación del uso de los datos (Data Usage Labeling and Enforcement, DULE), Journey Optimizer puede aprovechar las políticas de control de Adobe Experience Platform para evitar que los campos confidenciales se exporten a sistemas de terceros mediante acciones personalizadas. Si el sistema identifica un campo restringido en los parámetros de acción personalizados, se muestra un error que le impide publicar el recorrido.</p>
<p>El uso del etiquetado y aplicación del uso de los datos (Data Usage Labeling and Enforcement, DULE) está actualmente restringido a los clientes seleccionados y se implementará en todos los entornos en una versión futura.</p>
<p>Para obtener más información, consulte <a href="../action/action-privacy.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aplicación del consentimiento automatizada (políticas de consentimiento)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform le permite adoptar y aplicar fácilmente políticas de marketing que respeten las preferencias de consentimiento de sus clientes. Las políticas de consentimiento se definen en Adobe Experience Platform. En Journey Optimizer, puede aplicar estas políticas de consentimiento a sus acciones personalizadas. Por ejemplo, puede definir políticas de consentimiento para excluir a los clientes que no hayan aceptado recibir comunicaciones por correo electrónico, push o SMS.
<p>Actualmente, la aplicación automática del consentimiento solo está disponible para las organizaciones que han adquirido la oferta adicional Escudo de atención sanitaria.</p>
<p>Para obtener más información, consulte <a href="../action/consent.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Administración de permisos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer admite la definición de funciones de usuario y políticas de acceso para administrar permisos para funciones y objetos. Hasta <strong>Permisos de Adobe Experience Cloud</strong>, puede crear y administrar funciones, así como asignar los permisos de recursos deseados para estas funciones. Los permisos también le permiten administrar las etiquetas, los entornos limitados y los usuarios asociados a una función específica.</p>
<p> El uso de Permisos está restringido actualmente a clientes seleccionados y se implementará en todos los entornos en una versión futura.</p>
<p>Para obtener más información, consulte <a href="../administration/attribute-based-access.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alerta y supervisión</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Como usuario de Journey Optimizer, ahora puede acceder a las alertas del sistema a través de la interfaz de usuario para recibir notificaciones cuando los recorridos no funcionan como se esperaba. Puede ver las alertas disponibles y suscribirse a ellas. La primera alerta disponible con esta versión le avisará si una actividad Leer segmento no ha procesado ningún perfil durante el lapso de tiempo definido. Más información vendrá ahora que este flujo de trabajo está desbloqueado.</p>
<p>Para obtener más información, consulte <a href="../reports/alerts.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### Mejoras{#sept-2022-improvements}

**Recorridos**

* La variable **Conjunto de datos de entidad** ya está disponible como un conjunto de datos integrado en Adobe Journey Optimizer. Este conjunto de datos de búsqueda incluye metadatos para enriquecer la información de los conjuntos de datos de seguimiento y comentarios. Esto le ayudará a mejorar sus informes y consultas con datos más comprensibles. [Más información](../data/datasets-query-examples.md#entity-dataset)
* Se ha añadido una nueva protección a los recorridos unitarios (comenzando por un evento o una calificación de segmento) para evitar que los recorridos se activen varias veces por error para el mismo evento. La reentrada del perfil se bloqueará temporalmente de forma predeterminada durante 5 minutos. [Más información](../start/guardrails.md#events-g)

**Administración**

* Al activar o desactivar la lista de permitidos, ahora se muestra una nueva advertencia para detallar los impactos de cada acción. [Más información](../configuration/allow-list.md#enable-allow-list)
* Se ha actualizado la interfaz de usuario para crear superficies de canal, crear grupos de IP, administrar la lista de supresión y la lista permitida y configurar el canal SMS.
* Ahora, al crear la primera superficie de canal para un subdominio determinado, el tiempo de procesamiento tardará de 10 minutos a 10 días y solo 3 horas para las superficies posteriores que utilicen ese subdominio. [Más información](../configuration/channel-surfaces.md#create-channel-surface)
* Se ha actualizado la interfaz de usuario para crear ajustes preestablecidos de página de aterrizaje y subdominios de página de aterrizaje. [Más información](../landing-pages/lp-subdomains.md)

**Controles de auditoría**

* Con Journey Optimizer, puede identificar las acciones realizadas por los usuarios en el sistema en distintos servicios y capacidades, como campañas, recorridos, mensajes, páginas de aterrizaje, etc. Los recursos de registro de auditoría ahora incluyen cambios en varias otras acciones y se registran automáticamente cuando se produce la actividad. Más información [en esta página](../privacy/audit-logs.md).

**Soporte de archivado**

* El nuevo **Conjunto de datos de entidad** incluye un campo Template que permite exportar el formato y la estructura de los mensajes enviados en todos los canales para archivarlos. [Más información](../configuration/archiving-support.md)

**Páginas de aterrizaje**

* Ahora puede utilizar datos contextuales procedentes de otra página dentro de la misma página de aterrizaje. Por ejemplo, si vincula una casilla de verificación a una lista de suscripción en la página de aterrizaje principal, puede utilizar esa lista de suscripción en la subpágina &quot;gracias&quot;. [Más información](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Otros cambios{#sept-2022-other}

* El modo de ráfaga de recorrido se ha sustituido por el modo de envío rápido de Campaign. [Más información](../campaigns/create-campaign.md#rapid-delivery)
* Para mejorar el rendimiento, los grupos de campos de eventos de experiencia ya no se pueden utilizar en los recorridos que comienzan por un segmento de lectura, una calificación de segmentos o una actividad de evento empresarial. Este cambio solo se aplica a los recorridos nuevos. Las existentes mantendrán el comportamiento actual. [Más información](../start/guardrails.md#expression-editor)
* Se ha eliminado el límite de 1 hora para los recorridos programados del segmento de lectura. Ahora estos recorridos se pueden ejecutar sin demora.




## Versión de agosto de 2022 {#aug-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Crear y administrar campañas en Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilice las campañas de Journey Optimizer para ofrecer contenido único a un segmento específico mediante varios canales. Cuando se utilizan recorridos, las acciones están diseñadas para ejecutarse en secuencia. Con las campañas, las acciones se realizan simultáneamente, ya sea inmediatamente o en función de una programación especificada. </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>Obtenga información sobre cómo crear una campaña en <a href="../campaigns/get-started-with-campaigns.md">documentación detallada</a> y <a href="https://video.tv.adobe.com/v/346680">vídeo de funciones</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Enviar SMS a sus usuarios (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear, personalizar y enviar SMS en Journey Optimizer mediante una integración con <b>Sinch</b> o <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Aprenda a crear y enviar un SMS en esta <a href="../sms/create-sms.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Mejoras

**Informes**

* La tabla y el gráfico de políticas de consentimiento ahora están disponibles en los informes globales de recorrido. Estas utilidades permiten rastrear los perfiles excluidos de las políticas en sus acciones personalizadas. [Más información](../reports/journey-global-report.md#journey-global)

   Para tener acceso a las últimas utilidades, tenga en cuenta que tendrá que restablecer los distintos paneles de informes. Para obtener más información sobre la personalización de tableros, consulte [la documentación detallada](../reports/global-report.md).

**Administración**

* Ahora es posible actualizar el número de teléfono principal para utilizarlo en el canal SMS. [Más información](../configuration/primary-email-addresses.md)


## Versión de julio de 2022 {#july-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Nuevo flujo de mensajería en línea</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer proporciona un nuevo flujo para la creación de mensajes en recorridos. La mensajería en línea ahorrará a los usuarios un tiempo considerable y optimizará el proceso de flujo de trabajo para crear y enviar un correo electrónico, una notificación push o un SMS en Journey Optimizer. Al eliminar los mensajes como un paso independiente y, en su lugar, hacerlos editables en línea como parte de una acción en el Lienzo de recorrido, los usuarios deberán hacer clic en menos botones y navegar por menos pantallas para diseñar y editar su contenido.</p>
<img src="assets/do-not-localize/inline.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Control de acceso basado en atributos (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede identificar campos de esquema con etiquetas que definen ámbitos organizativos o de uso de datos. Los administradores pueden utilizar la interfaz Permisos para definir políticas de acceso que cubran los campos de esquema XDM y administrar mejor el acceso dado a usuarios o grupos de usuarios (usuarios internos, externos o de terceros), y administrar el acceso a tipos de datos específicos (es decir, datos personales confidenciales/SPD).</p>
<p>El uso del control de acceso basado en atributos está actualmente restringido a usuarios seleccionados y se implementará en todos los entornos en una versión futura.</p>
<p>Para obtener más información, consulte <a href="../administration/attribute-based-access.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Trabajos de toma de decisiones por lotes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede ejecutar trabajos de toma de decisiones por lotes desde la interfaz de usuario, de modo que no necesite un desarrollador para ejecutar trabajos de api por lotes y pueda reducir el tiempo necesario para el marketing. Esta nueva interfaz le permite crear trabajos y administrar trabajos actuales o anteriores.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Para obtener más información, consulte <a href="../offers/batch-delivery.md">documentación detallada.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilizar automáticamente la oferta de mejor rendimiento en sus decisiones (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar sistemas de modelos de optimización personalizados en la administración de decisiones. Este nuevo tipo de modelo le permite optimizar y personalizar ofertas en función de segmentos y ofrecer rendimiento.</p>
<p>El uso de modelos de IA de optimización personalizados está actualmente restringido a usuarios seleccionados y se implementará en todos los entornos en una versión futura.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Para obtener más información, consulte <a href="../offers/ranking/personalized-optimization-model.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

**Recorridos**

* **Finalización de un recorrido** - En el lienzo del recorrido, el **Fin** se ha eliminado de la paleta. Las etiquetas finales ahora se añaden de forma predeterminada al final de cada ruta y no se pueden eliminar. Esta mejora permite obtener mejores informes sobre dónde abandonó un cliente el recorrido, sin que se requiera ninguna acción por parte del practicante del recorrido. Consulte la [documentación](../building-journeys/end-journey.md) y [vídeo de funciones](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}.


* La variable **Zona horaria del perfil** ahora está desactivada de forma predeterminada en las propiedades del recorrido. [Más información](../building-journeys/timezone-management.md#timezone-from-profiles)

**Mensajes**

* Los mensajes preestablecidos ya están **superficies de canal**. [Más información](../configuration/channel-surfaces.md)

**Administración**

* **Edición de registro de PTR** - Ahora, al actualizar un registro PTR, el tiempo de procesamiento solo tardará 3 horas. [Más información](../configuration/ptr-records.md#processing)

* **Interfaz de usuario de lista permitida** : Ahora puede utilizar la interfaz de usuario de Journey Optimizer para agregar nuevas direcciones de correo electrónico o dominios a la lista de dominios permitidos. [Más información](../configuration/allow-list.md)

* **Actualización de lógica de lista permitida** - Ahora la lógica de lista permitida se aplica en cuanto la función está habilitada, incluso si la lista está vacía. [Más información](../configuration/allow-list.md#logic)

* **Parámetros de seguimiento de URL** - Ahora puede utilizar el Editor de expresiones para configurar los parámetros de seguimiento de URL en sus superficies de correo electrónico (es decir, ajustes preestablecidos). [Más información](../email/email-settings.md#url-tracking)

**Gestión de decisiones**

* **Tamaño de la audiencia** : Ahora se muestra un nuevo componente de estimación del tamaño de la audiencia en la interfaz de usuario al crear una regla de decisión, al seleccionar un segmento o una regla para establecer la idoneidad de una oferta o al añadir un segmento o una regla al ámbito de decisión.


## Versión de junio de 2022 {#june-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Enviar SMS a los usuarios (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear, personalizar y enviar SMS en Journey Optimizer mediante una integración con <b>Sinch</b> o <b>Twilio</b>.</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>Actualmente, el canal SMS solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, póngase en contacto con su representante de Adobe.</p>
<p>Aprenda a crear y enviar un SMS en esta <a href="../sms/create-sms.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Encuentre imágenes más impactantes más rápido con la integración de Adobe Stock</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El complemento de integración del Diseñador de correo electrónico de Adobe Stock y Adobe Journey Optimizer proporciona a los clientes una manera sencilla de navegar, obtener licencias y guardar imágenes para utilizarlas en la creación de mensajes. </br> El nuevo <b>Buscar fotos similares de Stock</b> también le permite localizar fotos de almacenamiento que coincidan con el contenido, el color y la composición de las imágenes. </p>
<!--img src="assets/do-not-localize/stock-rn.gif"/-->
<p>Para obtener más información, consulte <a href="../email/stock.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilice el correo electrónico CCO en todos sus correos electrónicos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar la capacidad Email BCC (copia de seguridad ciega) para almacenar correos electrónicos enviados por Adobe Journey Optimizer. Active esta opción en los ajustes preestablecidos de correo electrónico para que cada correo electrónico enviado se copie de forma ciega en su dirección de CCO.</p>
<!--img src="assets/do-not-localize/bcc-rn.gif"/-->
<p>Para obtener más información, consulte <a href="../configuration/archiving-support.md#bcc-email">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Copiar objetos entre entornos limitados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede volver a crear las experiencias de un simulador para pruebas de Journey Optimizer a otro, por ejemplo, de un simulador para pruebas que no sean de producción a un simulador para pruebas de producción. Esta nueva capacidad copia un Recorrido completo, incluidos los objetos de los que depende el Recorrido para ejecutarse correctamente, de un entorno a otro. Además de Recorridos, también puede copiar otros componentes, como Ofertas, Mensajes, Esquemas, Conjuntos de datos, Fuentes de datos, Eventos y Acciones.</p>
<p>Para obtener más información, consulte <a href="../building-journeys/copy-to-sandbox.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>




### Mejoras

**Gestión de decisiones**

* **Compatibilidad con archivos HTML y JSON** : Ahora puede arrastrar y soltar archivos HTML y JSON externos de la biblioteca de recursos de Adobe Experience Cloud en el contenido de representación de ofertas. [Más información](../offers/offer-library/add-representations.md#html-json)


**Correo electrónico**

* **Guardar como plantilla** - Ahora puede guardar un contenido de correo electrónico como plantilla y reutilizarlo al crear otros mensajes. [Más información](../email/email-templates.md)


**Administración**

* **Vista previa de los parámetros de URL de seguimiento** : Al configurar un ajuste preestablecido de mensaje, si define parámetros de seguimiento de URL, ahora se muestra una vista previa dinámica de la URL de seguimiento resultante. [Más información](../email/email-settings.md#url-tracking)

* **Edición preestablecida de mensajes** - Ahora, al actualizar un ajuste preestablecido de mensaje, el tiempo de procesamiento solo puede tardar hasta 3 horas. [Más información](../configuration/channel-surfaces.md#edit-channel-surface)

* **Edición de grupos de IP** - Ahora, al actualizar un grupo de IP, el tiempo de procesamiento solo puede tardar hasta 3 horas. [Más información](../configuration/ip-pools.md#edit-ip-pool)




## Versión de mayo de 2022 {#may-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Reglas de frecuencia de mensaje</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede establecer reglas comerciales multicanal que excluyan automáticamente los perfiles saturados de mensajes y acciones.</p>
<!--img src="assets/do-not-localize/frequency-rn.gif"/-->
<p>Para obtener más información, consulte <a href="../configuration/frequency-rules.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Administración de decisiones: modelo de optimización automática de la clasificación de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar sistemas de modelos formados en Administración de decisiones. Esta nueva capacidad clasifica las ofertas que se muestran para un perfil determinado.</p>
<!--img src="assets/do-not-localize/optimization.gif"/-->
<p>Para obtener más información, consulte <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Registros de auditoría de Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede monitorizar las acciones realizadas por los usuarios en los recursos de Adobe Journey Optimizer.</p>
<!--img src="assets/do-not-localize/audit-rn.gif"/-->
<p>Para obtener más información, consulte <a href="../privacy/audit-logs.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

**Personalización**

* **Nueva función de ayuda para la ocultación de caracteres** - El `mask` la función de ayuda le permite reemplazar una parte de una cadena con caracteres &quot;X&quot;. [Más información](../personalization/functions/string.md#mask)

**Páginas de aterrizaje**

* **Páginas de aterrizaje sin formulario** - Ahora puede crear y publicar una página de aterrizaje que no contenga un formulario y que no requiera que los visitantes realicen ninguna acción.
* **Plantillas de página de aterrizaje** : Ahora puede guardar una página de aterrizaje como plantilla y reutilizarla al crear otras páginas de aterrizaje. [Más información](../landing-pages/lp-templates.md)
* **Volver a la página principal** - Ahora puede agregar un vínculo a la página principal desde cualquier subpágina dentro de la misma página de aterrizaje.
* **Compatibilidad con JavaScript personalizado** - Ahora puede agregar JavaScript personalizado al contenido de la página de aterrizaje para realizar estilos avanzados o agregar comportamientos personalizados a las páginas de aterrizaje.    [Más información](../landing-pages/lp-custom-js.md)

**Recorridos**

* **Leer segmento** - Los recorridos del segmento de lectura de una sola toma ahora pasan al estado Finalizado 30 días después de la ejecución del recorrido. Para segmentos de lectura programados, son 30 días después de la ejecución de la última incidencia. [Más información](../building-journeys/read-segment.md)
* **Editor de expresiones** - El [límite](../building-journeys/functions/functionlimit.md) para permitirle limitar el número de elementos de una lista. La variable [sort](../building-journeys/functions/functionsort.md) ahora permite ordenar un objeto de lista. La compatibilidad de listObject también se ha agregado al [disctinct](../building-journeys/functions/functiondistinct.md) y [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) funciones.

**Administración**

* **Actualización del panel de uso de licencias** - El panel de uso de licencias disponible en el [!DNL Adobe Journey Optimizer] la interfaz de usuario de ahora refleja el valor preciso del **Con licencia** Promedio de riqueza de perfiles. Verá una caída en esta representación de métrica, lo que significa que el límite de licencias ahora se registra correctamente. [Más información](../segment/license-usage.md)


## Versión de abril de 2022 {#april-2022-release}

### Mejoras

**Páginas de aterrizaje**

* **Nueva opción para casillas de verificación de inclusión/exclusión** - Ahora puede insertar una sola casilla de verificación para la inclusión/exclusión en las páginas de aterrizaje de suscripción. Los usuarios deben marcar la casilla de verificación para el consentimiento (inclusión) y desmarque para eliminar su consentimiento (exclusión). [Más información](../landing-pages/design-lp.md#define-lp-specific-content)

* **Rellenar previamente campos de páginas de aterrizaje** : Ahora es posible proporcionar a los usuarios la capacidad de rellenar previamente los campos de la página de aterrizaje con información de perfil. [Más información](../landing-pages/create-lp.md#configure-primary-page)

**Gestión de decisiones**

* **API de decisiones en Edge** - La API de Edge Decisioning puede entregar y procesar ofertas personalizadas que se administran en la administración de decisiones. Puede crear sus ofertas y otros objetos relacionados mediante la interfaz de usuario (IU) o las API de administración de decisiones. [Más información](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Administración**

* **Duración de envío de PTR** - La duración de la edición de PTR para que sea efectiva es ahora de unas pocas horas. [Más información](../configuration/ptr-records.md#processing)

**Diseño de correo electrónico**

* **20 nuevas plantillas de correo electrónico** ya están disponibles para diseñar su contenido de correo electrónico en Journey Optimizer.

**Interfaz de usuario**

* **Ayuda contextual en la interfaz de usuario de Journey Optimizer** - Se han agregado vínculos de ayuda contextual a varias páginas en Journey Optimizer. Cuando esté disponible, haga clic en el icono &quot;i&quot; para ver una descripción rápida de la funcionalidad actual y acceder a los artículos relacionados.

**Integración con Adobe Campaign Standard**

Como cliente de Adobe Campaign Standard, ahora puede enviar correos electrónicos, notificaciones push y SMS mediante Journey Optimizer. Utilice las nuevas acciones integradas para aprovechar las capacidades de mensajería transaccional de Campaign Standard en Journey Optimizer.  [Más información](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Versión de marzo de 2022 {#march-2022-release}

### Mejoras

**Recorridos**

* Para evitar tener campos innecesarios en el esquema de perfil unificado, el esquema de evento de paso del recorrido ya no está habilitado para perfiles de forma predeterminada. Si es necesario, puede activarlo. [Más información](../reports/sharing-overview.md)
* Journey Optimizer envía a Adobe Experience Platform nuevos eventos de paso relacionados con los trabajos de exportación. Se han añadido ejemplos de consultas a la documentación. [Más información](../reports/query-examples.md)

**Gestión de decisiones**

* Ahora puede especificar si el límite de oferta se aplica a todos los usuarios o a un perfil específico, así como a todas las ubicaciones o ubicaciones. [Más información](../offers/offer-library/add-constraints.md#capping)
* La API de decisiones por lotes permite a las organizaciones utilizar la funcionalidad de administración de decisiones para todos los perfiles de un segmento determinado en una llamada. El contenido de la oferta para cada perfil del segmento se coloca en un conjunto de datos de AEP, donde está disponible para flujos de trabajo por lotes personalizados. [Más información](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Administración**

* Ahora puede habilitar/deshabilitar el vínculo de cancelación de suscripción en/desde el encabezado de correo electrónico en el nivel de ajuste preestablecido de mensaje y establecer una URL de cancelación de suscripción personalizada en el nivel de mensaje. [Más información](../configuration/channel-surfaces.md#list-unsubscribe)
* La lista permitida ahora se puede habilitar y deshabilitar a través de la variable [!DNL Journey Optimizer] en entornos limitados de producción y sin producción. [Más información](../configuration/allow-list.md#enable-allow-list)

**Personalización**

* Ahora puede guardar más de 40 expresiones de personalización en la biblioteca . [Más información](../personalization/personalization-library.md)

## Versión de febrero de 2022 {#feb-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Páginas de aterrizaje de suscripción</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear y diseñar páginas de aterrizaje en Journey Optimizer y dirigir a los usuarios a formularios en línea en los que pueden aceptar o rechazar la recepción de comunicaciones, o suscribirse a un servicio específico, como un boletín informativo.</p>
<p>Para obtener más información, consulte <a href="../landing-pages/create-lp.md">documentación detallada</a> y relacionados <a href="../landing-pages/lp-use-cases.md">ejemplo de uso</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nueva biblioteca de expresiones de personalización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora proporciona una biblioteca en la que puede acceder a las expresiones de personalización predefinidas. Estas expresiones las configuran los usuarios administradores.</p>
<p>Para obtener más información, consulte <a href="../personalization/personalization-library.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs' feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Pasar información para realizar un seguimiento de los mensajes con parámetros de seguimiento de UTM</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En el contenido del mensaje de Journey Optimizer, ahora puede añadir parámetros de UTM a sus vínculos: pueden proporcionar datos adicionales sobre ese vínculo y ayudarle a identificar dónde y por qué hizo clic una persona en él.</p>
<p>Para obtener más información, consulte <a href="../configuration/channel-surfaces.md#configure-email-settings">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

**Recorridos**

* Para optimizar el rendimiento, todos los recorridos en modo de prueba que no se hayan activado durante una semana volverán al estado Borrador . [Más información](../building-journeys/testing-the-journey.md#important_notes)
* La integración entre Journey Optimizer y Adobe Campaign Classic se ha optimizado para mejorar el rendimiento. La configuración predeterminada de límite se ha cambiado a 4000 llamadas / 5 minutos.    [Más información](../action/acc-action.md#important-notes)

**Informes**

* Ahora se pueden filtrar los envíos en función de su estado:
   * Desde la lista Ejecución de mensajes, ahora puede excluir pruebas de la lista de envíos.
   * Desde los informes activos/globales, puede elegir excluir los eventos de prueba.

* Ahora puede acceder a los informes sobre los datos de optimización del tiempo de envío: el número de personas que fueron mensajes inmediatamente y el número de personas que recibieron mensajes con optimización de 1 hora, optimización de 2 horas, etc.

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Gestión de decisiones**

* Las clasificaciones y la clasificación AI ahora se agrupan en una sola pestaña.

## Versión de enero de 2022 {#january-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Recorridos: optimice su IP ramp up con las condiciones del límite del perfil</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Al configurar un <strong>Condición</strong> en un recorrido, ahora puede definir un límite de perfil. Este nuevo tipo de condición le permite establecer un número máximo de perfiles para una ruta de recorrido. Cuando se alcanza este límite, los perfiles que se introducen toman una ruta alternativa. Esto le permite aumentar el volumen de los envíos (aumento de IP). Por ejemplo, puede que desee ampliar las entregas en un dominio dividiendo la ejecución: enviar 1000 mensajes el día 1, 2000 el día 2, etc.</p>
<p>Para obtener más información, consulte <a href="../building-journeys/condition-activity.md#profile_cap">documentación detallada</a> y relacionados <a href="../building-journeys/ramp-up-deliveries-uc.md">ejemplo de uso</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Recorridos: mejora de segmentos de lectura</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La variable <strong>Lectura incremental</strong> se ha añadido a <strong>Leer segmento</strong> actividades. Esta opción le permite dirigirse únicamente a las personas que ingresaron al segmento desde la última ejecución del recorrido. La primera ejecución siempre se dirige a todos los miembros del segmento.</p>
<p>Para obtener más información, consulte <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>

### Mejoras

**Recorridos**

* Los eventos de paso de Journey Optimizer ahora se pueden vincular a otros conjuntos de datos en [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html). La variable **profileID** , en el esquema integrado de Evento de paso de recorrido, ahora se define como un campo de identidad. [Más información](../reports/sharing-overview.md#integration-cja)

**Gestión de decisiones**

* Al actualizar una oferta, una oferta de reserva, una recopilación de ofertas o una decisión de oferta a la que se hace referencia directa o indirectamente en un mensaje publicado, las actualizaciones ahora se reflejan automáticamente en el mensaje correspondiente, sin necesidad de volver a publicarlas. [Más información](../offers/offers-e2e.md#insert-decision-in-email)

* Al simular qué ofertas se enviarán para un perfil de prueba determinado, ahora puede modificar los ajustes de simulación predeterminados y ver el código correspondiente a las simulaciones que se pueden utilizar para solucionar problemas. [Más información](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administración**

* Los administradores ahora pueden editar registros PTR con un subdominio CNAME configurado. [Más información](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalización**

* **Agregar a favoritos** - Para ayudar a mejorar la eficacia al trabajar con la personalización, hemos introducido el concepto de guardar favoritos. Añadir atributos diferentes al menú de favoritos permite acceder rápidamente a los elementos más utilizados. [Más información](../personalization/personalize.md#fav)
