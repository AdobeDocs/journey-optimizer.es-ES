---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión 2022
description: Notas de la versión de Journey Optimizer 2022
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hidefromtoc: true
hide: true
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: 8ff4f970796218451996bd5ed1938d33fa818495
workflow-type: tm+mt
source-wordcount: '3599'
ht-degree: 99%

---

# Notas de la versión 2022 {#release-notes-2022}

Esta página enumera todas las funciones y mejoras de [!DNL Journey Optimizer] lanzado en 2022.



## Versión de octubre de 2022 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### Mejoras {#oct-2022-improvements}

**Recorridos**

* La opción **Forzar reentrada en repetición** se ha añadido en los parámetros de programación de lectura de público recurrentes. Esta opción le permite hacer que todos los perfiles que aún están presentes en el recorrido se cierren automáticamente en la siguiente ejecución. Cuando la opción está desactivada, los perfiles deben finalizar el recorrido antes de poder volver a entrar en otra ocurrencia. [Más información](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**Administración**

* Se ha agregado un mensaje a la interfaz de usuario para advertir que las configuraciones de subdominio, subdominio de página de destino, registro PTR y grupo de IP son comunes a todas las zonas protegidas, por lo que cualquier modificación en una de estas configuraciones también afectará a las zonas protegidas de producción.
* Se han modificado los pasos para cargar la lista de supresión como archivo CSV desde la interfaz de usuario. [Más información](../configuration/manage-suppression-list.md#download-suppression-list)

**Campañas**

* Ahora puede archivar las campañas completadas y detenidas. [Más información](../campaigns/modify-stop-campaign.md#archive)


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
<p>Para obtener más información, consulte la <a href="../personalization/get-started-dynamic-content.md">documentación detallada</a>.
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
<p>Esto le permite cubrir diversas necesidades operativas y de mensajería transaccional, como los restablecimientos de contraseña, el token OTP, etc.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Para obtener más información, consulte la <a href="../campaigns/api-triggered-campaigns.md">documentación detallada</a>.
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
<p>Mediante el control de acceso basado en atributos, los administradores pueden controlar el acceso a objetos específicos en función de determinados atributos. Estos atributos pueden ser metadatos añadidos a un objeto, como etiquetas. A partir de esta versión, los administradores también pueden definir funciones de usuario que solo tengan acceso a campos u objetos específicos, y datos que correspondan a esos campos u objetos.</p>
<p> El uso del control de acceso basado en atributos está actualmente restringido a clientes seleccionados y se implementará en todos los entornos en una versión futura.</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>Para obtener más información, consulte la <a href="../administration/object-based-access.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Gobernanza de datos y privacidad</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con su marco de trabajo de gobernanza de etiquetado y aplicación del uso de datos (Data Usage Labeling and Enforcement, DULE), Journey Optimizer ahora puede aprovechar las políticas de gobernanza de Adobe Experience Platform para evitar que los campos confidenciales se exporten a sistemas de terceros mediante acciones personalizadas. Si el sistema identifica un campo restringido en los parámetros de acción personalizados, se muestra un error que le impide publicar el recorrido.</p>
<p>El uso de etiquetado y aplicación del uso de datos (Data Usage Labeling and Enforcement, DULE) está actualmente restringido a los clientes seleccionados y se implementará en todos los entornos en una versión futura.</p>
<p>Para obtener más información, consulte la <a href="../action/action-privacy.md">documentación detallada</a>.
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
<p>Actualmente, la aplicación automática del consentimiento solo está disponible para las organizaciones que han adquirido la oferta complementaria Escudo de atención sanitaria.</p>
<p>Para obtener más información, consulte la <a href="../action/consent.md">documentación detallada</a>.
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
<p>Journey Optimizer admite la definición de funciones de usuario y políticas de acceso para administrar permisos para funcionalidades y objetos. Mediante <strong>Permisos de Adobe Experience Cloud</strong>, puede crear y administrar funciones, así como asignar los permisos de recursos deseados para estas. Los permisos también le permiten administrar las etiquetas, las zonas protegidas y los usuarios asociados a una función específica.</p>
<p> El uso de Permisos está actualmente restringido a usuarios seleccionados y se implementará en todos los entornos en una versión futura.</p>
<p>Para obtener más información, consulte la <a href="../administration/attribute-based-access.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alerta y monitorización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Como usuario de Journey Optimizer, ahora puede acceder a las alertas del sistema a través de la interfaz de usuario para recibir notificaciones cuando los recorridos no funcionan según lo esperado. Puede ver las alertas disponibles y suscribirse a ellas. La primera alerta disponible con esta versión le avisará si la actividad Leer público no ha procesado ningún perfil durante el lapso de tiempo definido. Habrá más ahora que se ha desbloqueado este flujo de trabajo.</p>
<!--p>For more information, refer to the <a href="../reports/alerts.md">detailed documentation</a>.</p-->
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
<p>For more information, refer to the <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### Mejoras{#sept-2022-improvements}

**Recorridos**

* El **Conjunto de datos de entidad** ya está disponible como un conjunto de datos predeterminado en Adobe Journey Optimizer. Este conjunto de datos de búsqueda incluye metadatos para enriquecer la información de los conjuntos de datos de seguimiento y comentarios. Esto le ayudará a mejorar sus informes y consultas con datos más comprensibles. [Más información](../data/datasets-query-examples.md#entity-dataset)
* Se ha añadido un nuevo mecanismo de protección a los recorridos unitarios (que comiencen por un evento o una calificación de público) para evitar que los recorridos se activen varias veces por error para el mismo evento. La reentrada del perfil se bloqueará temporalmente de forma predeterminada durante 5 minutos. [Más información](../start/guardrails.md#events-g)

**Administración**

* Al activar o desactivar la lista de permitidos, ahora se muestra una nueva advertencia para detallar los impactos de cada acción. [Más información](../configuration/allow-list.md#enable-allow-list)
* Se ha actualizado la interfaz de usuario para crear configuraciones de canal, crear grupos de IP, administrar la lista de supresión y la lista de permitidos y configurar el canal de SMS.
* Ahora, al crear la primera configuración de canal para un subdominio determinado, el tiempo de procesamiento tardará de 10 minutos a 10 días, y solo hasta 3 horas para las superficies posteriores que utilicen ese subdominio. [Más información](../configuration/channel-surfaces.md#create-channel-surface)
* Se ha actualizado la interfaz de usuario para crear ajustes preestablecidos de página de destino y subdominios de página de destino. [Más información](../landing-pages/lp-subdomains.md)

**Controles de auditoría**

* Con Journey Optimizer, puede identificar las acciones ejecutadas por los usuarios en el sistema en distintos servicios y funcionalidades como campañas, recorridos, mensajes, páginas de destino, etc. Los recursos de registros de auditorías ahora incluyen cambios en otras múltiples acciones y se registran automáticamente cuando se produce la actividad. Obtenga más información [en esta página](../privacy/audit-logs.md).

**Soporte de archivado**

* El nuevo **Conjunto de datos de entidad** incluye un campo de plantilla que permite exportar el formato y la estructura de los mensajes enviados en todos los canales para archivarlos. [Más información](../configuration/archiving-support.md)

**Páginas de destino**

* Ahora puede utilizar datos contextuales procedentes de otra página dentro de la misma página de destino. Por ejemplo, si vincula una casilla de verificación a una lista de suscripción en la página de destino principal, puede utilizar esa lista de suscripción en la subpágina &quot;gracias&quot;. [Más información](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Otros cambios{#sept-2022-other}

* El modo de ráfaga de recorrido se ha sustituido por el modo de envío rápido de Campaign. [Más información](../push/create-push.md#rapid-delivery)
* Para mejorar el rendimiento, los grupos de campos de eventos de experiencia ya no se pueden utilizar en recorridos que comiencen con las actividades Leer público, Calificación de público o evento empresarial. Este cambio solo se aplica a los nuevos recorridos. Los existentes mantendrán el comportamiento actual. [Más información](../start/guardrails.md#expression-editor)
* Se ha eliminado la limitación de una hora para los recorridos de lectura de público programados. Estos recorridos ahora se pueden ejecutar sin demora.




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
<p>Utilice las campañas de Journey Optimizer para ofrecer contenido único a un público específico mediante varios canales. Cuando se utilizan recorridos, las acciones están diseñadas para ejecutarse en secuencia. Con las campañas, las acciones se realizan simultáneamente, ya sea de forma inmediata o en función de una programación especificada. </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>Obtenga información sobre cómo crear una campaña en <a href="../campaigns/get-started-with-campaigns.md">documentación detallada</a> y <a href="https://video.tv.adobe.com/v/346680">vídeo de funciones</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Envío de SMS a los usuarios (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear, personalizar y enviar SMS en Journey Optimizer mediante una integración con <b>Sinch</b> o <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Aprenda a crear y enviar un SMS con esta <a href="../sms/create-sms.md">documentación detallada</a>.</p>
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
<p>For more information, refer to the <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Mejoras

**Creación de informes**

* La tabla y el gráfico de políticas de consentimiento ya están disponibles en los informes globales de Recorrido. Estas utilidades permiten rastrear los perfiles excluidos de las políticas en sus acciones personalizadas. [Más información](../reports/journey-global-report-cja.md#journey-global)

  Para tener acceso a las últimas utilidades, tenga en cuenta que tendrá que restablecer los distintos paneles de creación de informes. Para obtener más información sobre la personalización de tableros, consulte la [documentación detallada](../reports/report-gs-cja.md).

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
<p>Journey Optimizer proporciona un nuevo flujo para la creación de mensajes en recorridos. La mensajería en línea ahorrará a los usuarios un tiempo considerable y optimizará el proceso de flujo de trabajo para crear y enviar un correo electrónico, una notificación push o un SMS en Journey Optimizer. Al eliminar los mensajes como un paso independiente y, en su lugar, hacerlos editables en línea como parte de una acción en el lienzo del recorrido, los usuarios deberán hacer clic en menos botones y navegar por menos pantallas para diseñar y editar su contenido.</p>
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
<p>Ahora puede identificar campos de esquema con etiquetas que definen ámbitos organizativos o de uso de datos. Los administradores pueden utilizar la interfaz Permisos para definir políticas de acceso que cubran los campos de esquema XDM y administrar mejor el acceso dado a usuarios o grupos de usuarios (usuarios internos, externos o de terceros), así como gestionar el acceso a tipos de datos específicos (es decir, datos personales confidenciales).</p>
<p>El uso del control de acceso basado en atributos está actualmente restringido a usuarios seleccionados y se implementará en todos los entornos en una versión futura.</p>
<p>Para obtener más información, consulte la <a href="../administration/attribute-based-access.md">documentación detallada</a>.</p>
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
<p>Ahora puede ejecutar trabajos de toma de decisiones por lotes desde la interfaz de usuario, de modo que no necesite un desarrollador para ejecutar trabajos de API por lotes y pueda reducir el tiempo necesario para el marketing. Esta nueva interfaz le permite crear trabajos y administrar los actuales o anteriores.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Para obtener más información, consulte la <a href="../offers/batch-delivery.md">documentación detallada.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Uso automático de la oferta con mejor rendimiento en sus decisiones (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar sistemas de modelos de optimización personalizados en la gestión de decisiones. Este nuevo tipo de modelo le permite optimizar y personalizar ofertas en función de los públicos y ofrecer rendimiento.</p>
<p>El uso de modelos de IA de optimización personalizados está actualmente restringido a usuarios seleccionados y se implementará en todos los entornos en una versión futura.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Para obtener más información, consulte la <a href="../offers/ranking/personalized-optimization-model.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

**Recorridos**

* **Finalización de un recorrido**: en el lienzo del recorrido, la actividad **Fin** se ha eliminado de la paleta. Las etiquetas finales ahora se añaden de forma predeterminada al final de cada ruta y no se pueden eliminar. Esta mejora permite informar mejor sobre dónde abandonó un cliente el recorrido, sin que se requiera ninguna acción por parte del profesional del recorrido. Consulte la [documentación](../building-journeys/end-journey.md) y el [vídeo de funcionalidades](https://video.tv.adobe.com/v/345376){target="_blank"}.


* La opción **Zona horaria del perfil** ahora está desactivada de forma predeterminada en las propiedades del recorrido. [Más información](../building-journeys/timezone-management.md#timezone-from-profiles)

**Mensajes**

* Los ajustes preestablecidos de mensaje ahora son **configuraciones de canal**. [Más información](../configuration/channel-surfaces.md)

**Administración**

* **Edición de registros de PTR**: ahora, al actualizar un registro PTR, el tiempo de procesamiento solo será de tres horas, como máximo. [Más información](../configuration/ptr-records.md#processing)

* **IU de lista de permitidos**: ahora puede utilizar la interfaz de usuario de Journey Optimizer para añadir nuevas direcciones de correo electrónico o dominios a la lista de permitidos. [Más información](../configuration/allow-list.md)

* **Actualización de la lógica de lista de permitidos**: ahora la lógica de lista de permitidos se aplica en cuanto se habilita la función, incluso si la lista está vacía. [Más información](../configuration/allow-list.md#logic)

* **Parámetros de seguimiento de URL**: ahora puede utilizar el Editor de expresiones para configurar los parámetros de seguimiento de URL en sus superficies de correo electrónico (es decir, ajustes preestablecidos). [Más información](../email/email-settings.md#url-tracking)

**Gestión de decisiones**

* **Tamaño del público**: ahora se muestra un nuevo componente de estimación del tamaño del público en la interfaz de usuario al crear una regla de decisión, al seleccionar un público o una regla para establecer la idoneidad de una oferta o al añadir un público o una regla a un ámbito de decisión.


## Lanzamiento de junio de 2022 {#june-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Envío de SMS a los usuarios (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear, personalizar y enviar SMS en Journey Optimizer mediante una integración con <b>Sinch</b> o <b>Twilio</b>.</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>Ahora mismo, el canal SMS solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.</p>
<p>Aprenda a crear y enviar un SMS en esta <a href="../sms/create-sms.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Encuentre imágenes más impactantes más rápido con la integración con Adobe Stock</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El complemento de integración del Diseñador de correo electrónico de Adobe Journey Optimizer y Adobe Stock proporciona a los clientes una forma sencilla de navegar, obtener licencias y guardar imágenes para utilizarlas en la creación de mensajes. </br> La nueva opción <b>Buscar fotografías similares de Stock</b> también le permite localizar fotos de Stock que coincidan con el contenido, el color y la composición de sus imágenes. </p>
<p>Para obtener más información, consulte la <a href="../integrations/stock.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Uso de CCO del correo electrónico en todos los correos electrónicos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar la capacidad CCO del correo electrónico (copia de carbón oculta) para almacenar correos electrónicos enviados por Adobe Journey Optimizer. Active esta opción en los ajustes preestablecidos de correo electrónico para que cada correo electrónico enviado se copie de forma oculta en su dirección de CCO.</p>
<p>Para obtener más información, consulte la <a href="../configuration/archiving-support.md#bcc-email">documentación detallada</a>.</p>
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
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on audiences and offer performance.</p>
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
<th><strong>Copia de objetos entre zonas protegidas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede recrear las experiencias de una zona protegida de Journey Optimizer en otra, por ejemplo, de una que no sea de producción a una de producción. Esta nueva funcionalidad copia un recorrido completo, incluidos los objetos de los que depende para ejecutarse correctamente, de un entorno a otro. Además de los recorridos, también puede copiar otros componentes, como Ofertas, Mensajes, Esquemas, Conjuntos de datos, Fuentes de datos, Eventos y Acciones.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/copy-to-sandbox.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>




### Mejoras

**Gestión de decisiones**

* **Compatibilidad con archivos HTML y JSON**: ahora puede arrastrar y soltar archivos HTML y JSON externos de la biblioteca de recursos de Adobe Experience Cloud en el contenido de la representación de la oferta. [Más información](../offers/offer-library/add-representations.md#html-json)


**Correo electrónico**

* **Guardar como plantilla**: ahora puede guardar un contenido de correo electrónico como plantilla y reutilizarlo al crear otros mensajes. [Más información](../content-management/content-templates.md#save-as-template)


**Administración**

* **Previsualizar parámetros de URL de seguimiento**: al configurar un ajuste preestablecido de mensaje, si define parámetros de seguimiento de URL, ahora se muestra la vista previa dinámica de la URL de seguimiento resultante. [Más información](../email/email-settings.md#url-tracking)

* **Edición de ajustes preestablecidos de mensajes**: ahora, al actualizar un ajuste preestablecido de mensaje, el tiempo de procesamiento solo puede ser de hasta tres horas. [Más información](../configuration/channel-surfaces.md#edit-channel-surface)

* **Edición de grupos de IP**: ahora, al actualizar un grupo de IP, el tiempo de procesamiento solo puede ser de hasta tres horas. [Más información](../configuration/ip-pools.md#edit-ip-pool)




## Lanzamiento de mayo de 2022 {#may-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Reglas de frecuencia de los mensajes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede establecer reglas empresariales multicanal que excluyan automáticamente los perfiles saturados de mensajes y acciones.</p>
<p>Para obtener más información, consulte la <a href="../conflict-prioritization/rule-sets.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestión de decisiones: modelo de optimización automática de la clasificación de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar sistemas de modelos formados en Gestión de decisiones. Esta nueva capacidad clasifica las ofertas que se muestran para un perfil determinado.</p>
<p>Para obtener más información, consulte la <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">documentación detallada</a>.</p>
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
<p>Para obtener más información, consulte la <a href="../privacy/audit-logs.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

**Personalización**

* **Nueva función de ayuda para la ocultación de caracteres**. La `mask` función de ayuda le permite reemplazar una parte de una cadena con caracteres &quot;X&quot;. [Más información](../personalization/functions/string.md#mask)

**Páginas de destino**

* **Páginas de destino sin formulario**: ahora puede crear y publicar una página de aterrizaje que no contenga un formulario y que no requiera que los visitantes realicen ninguna acción.
* **Plantillas de página de aterrizaje**: ahora puede guardar una página de aterrizaje como plantilla y reutilizarla al crear otras páginas de destino. [Más información](../landing-pages/lp-templates.md)
* **Volver a la página principal**: ahora puede agregar un vínculo a la página principal desde cualquier subpágina dentro de la misma página de destino.
* **Compatibilidad con JavaScript personalizado**: ahora puede agregar JavaScript personalizado al contenido de la página de aterrizaje para realizar estilos avanzados o agregar comportamientos personalizados a las páginas de destino.    [Más información](../landing-pages/lp-custom-js.md)

**Recorridos**

* **Leer público**: los recorridos de Leer público de una sola toma ahora pasan al estado Finalizado 30 días después de la ejecución del recorrido. Para recorridos de Leer público programados será 30 días después de la ejecución de la última ocurrencia. [Más información](../building-journeys/read-audience.md)
* **Editor de expresiones**: la función [límite](../building-journeys/functions/functionlimit.md) para permitirle limitar el número de elementos de una lista. La función [ordenar](../building-journeys/functions/functionsort.md) ahora permite ordenar un objeto de lista. La compatibilidad de listObject también se ha agregado a las funciones [disctinct](../building-journeys/functions/functiondistinct.md) y [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md).

**Administración**

* **Actualización del estado del tablero de uso de licencias**: el tablero de uso de licencias disponible en la [!DNL Adobe Journey Optimizer] interfaz de usuario ahora refleja el valor preciso de la riqueza del perfil promedio **Con licencia**. Verá una caída en esta representación de métrica, lo que significa que el límite de licencias ahora se registra correctamente. [Más información](../audience/license-usage.md)


## Versión de abril de 2022 {#april-2022-release}

### Mejoras

**Páginas de destino**

* **Nueva opción para casillas de verificación de inclusión/exclusión.** Ahora puede insertar una sola casilla de verificación para la inclusión/exclusión en las páginas de destino de suscripción. Los usuarios deben marcar la casilla de verificación para el consentimiento (inclusión) y desmarcar para eliminar su consentimiento (exclusión). [Más información](../landing-pages/design-lp.md#define-lp-specific-content)

* **Rellenar previamente campos de páginas de destino.** Ahora es posible proporcionar a los usuarios la capacidad de rellenar previamente los campos de la página de aterrizaje con información del perfil. [Más información](../landing-pages/create-lp.md#configure-primary-page)

**Gestión de decisiones**

* **API de decisiones en Edge**: la API de decisiones en Edge puede entregar y procesar ofertas personalizadas que se gestionan en la gestión de decisiones. Puede crear sus ofertas y otros objetos relacionados mediante la interfaz de usuario (IU) o las API de gestión de decisiones. [Más información](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Administración**

* **Duración de envío de PTR.** La duración de la edición de PTR para que sea efectiva es ahora de unas pocas horas. [Más información](../configuration/ptr-records.md#processing)

**Diseño de correo electrónico**

* **Veinte nuevas plantillas de correo electrónico** ya están disponibles para diseñar el contenido de su correo electrónico en Journey Optimizer.

**Interfaz de usuario**

* **Ayuda contextual en la interfaz de usuario de Journey Optimizer.** Se han agregado vínculos de ayuda contextual a varias páginas en Journey Optimizer. Cuando esté disponible, haga clic en el icono “i” para ver una descripción rápida de la funcionalidad actual y acceder a los artículos relacionados.

**Integración con Adobe Campaign Standard**

Como cliente de Adobe Campaign Standard, ahora puede enviar correos electrónicos, notificaciones push y SMS mediante Journey Optimizer. Utilice las nuevas acciones integradas para aprovechar las capacidades de mensajería transaccional de Campaign Standard en Journey Optimizer.  [Más información](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Lanzamiento de marzo de 2022 {#march-2022-release}

### Mejoras

**Recorridos**

* Para evitar tener campos innecesarios en el esquema de perfil unificado, el esquema de Evento de paso de recorrido ya no está habilitado para perfiles de forma predeterminada. Si es necesario, puede activarlo. [Más información](../reports/sharing-overview.md)
* Journey Optimizer ahora envía a Adobe Experience Platform nuevos eventos relacionados con los trabajos de exportación. Se han añadido ejemplos de consultas a la documentación. [Más información](../reports/query-examples.md)

**Gestión de decisiones**

* Ahora puede especificar si el límite de oferta se aplica a todos los usuarios o a un perfil específico, así como a todas las ubicaciones o a una. [Más información](../offers/offer-library/add-constraints.md#capping)
* La API de decisiones por lotes permite a las organizaciones utilizar la funcionalidad de gestión de decisiones para todos los perfiles de un público determinado en una llamada. El contenido de la oferta para cada perfil del público se coloca en un conjunto de datos de AEP, donde está disponible para los flujos de trabajo por lotes personalizados. [Más información](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Administración**

* Ahora puede habilitar/deshabilitar el vínculo de cancelación de suscripción en/desde el encabezado de correo electrónico en el nivel de ajuste preestablecido de mensaje y establecer una URL de cancelación de suscripción personalizada en el nivel de mensaje. [Más información](../configuration/channel-surfaces.md#list-unsubscribe)
* Ahora, la lista de permitidos se puede habilitar y deshabilitar a través de la interfaz [!DNL Journey Optimizer] en zonas protegidas de producción y sin producción. [Más información](../configuration/allow-list.md#enable-allow-list)

**Personalización**

* Ahora puede guardar más de 40 expresiones de personalización en la biblioteca. [Más información](../personalization/use-expression-fragments.md)

## Lanzamiento de febrero de 2022 {#feb-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Páginas de destino de suscripción</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear y diseñar páginas de destino en Journey Optimizer y dirigir a los usuarios a formularios en línea en los que pueden optar por su inclusión o exclusión en la recepción de comunicaciones, o suscribirse a un servicio específico, como una newsletter.</p>
<p>Para obtener más información, consulte la <a href="../landing-pages/create-lp.md">documentación detallada</a> y el <a href="../landing-pages/lp-use-cases.md">caso de uso de muestra</a> relacionado.</p>
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
<p>Journey Optimizer ahora proporciona una biblioteca en la que puede acceder a expresiones de personalización predefinidas. Estas expresiones las configuran los usuarios administradores.</p>
<p>Para obtener más información, consulte la <a href="../personalization/use-expression-fragments.md">documentación detallada</a>.</p>
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
The suppression list helps you with honoring the ISPs' feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you do not send mails to customers from your development sandbox.</p>
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
<p>En el contenido del mensaje de Journey Optimizer, ahora puede añadir parámetros UTM a sus vínculos: pueden proporcionar datos adicionales sobre ese vínculo y ayudarle a identificar dónde y por qué hizo clic una persona en él.</p>
<p>Para obtener más información, consulte la <a href="../configuration/channel-surfaces.md#configure-email-settings">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras

**Recorridos**

* Para optimizar el rendimiento, todos los recorridos en modo de prueba que no se hayan activado durante una semana volverán al estado Borrador. [Más información](../building-journeys/testing-the-journey.md#important_notes)
* La integración entre Journey Optimizer y Adobe Campaign v7/v8 se ha optimizado para mejorar el rendimiento. La configuración predeterminada de límite ha cambiado a 4000 llamadas / 5 minutos. [Más información](../action/acc-action.md#important-notes)

**Creación de informes**

* Ahora se pueden filtrar los envíos en función de su estado:
   * Desde la lista Ejecución de mensajes, ahora puede excluir pruebas de la lista de envíos.
   * Desde los informes activos/globales, puede elegir excluir los eventos de prueba.

* Ahora puede acceder a los informes sobre los datos de optimización del tiempo de envío: el número de personas que recibieron mensajes inmediatamente y el número de personas que recibieron mensajes con optimización de una hora, dos horas, etc.

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Gestión de decisiones**

* Las clasificaciones y la clasificación de IA ahora se agrupan en una sola pestaña.

## Lanzamiento de enero de 2022 {#january-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Recorridos: optimice la ampliación de su IP con las condiciones del límite del perfil</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Al configurar una actividad de <strong>Condición</strong> en un recorrido, ahora puede definir un límite de perfil. Este nuevo tipo de condición le permite establecer un número máximo de perfiles para una ruta de recorrido. Cuando se alcanza este límite, los perfiles que se introducen toman una ruta alternativa. Esto le permite aumentar el volumen de los envíos (aumento de IP). Por ejemplo, puede que desee ampliar los envíos en un dominio dividiendo la ejecución: enviar 1000 mensajes el día 1, 2000 el día 2, etc.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/condition-activity.md#profile_cap">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Recorridos: mejora de Leer público</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La opción <strong>Lectura incremental</strong> se ha añadido a las actividades <strong>Leer público</strong> recurrentes. Esta opción le permite dirigirse únicamente a los particulares que entraron al público desde la última ejecución del recorrido. La primera ejecución siempre se dirige a todos los miembros del público.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>

### Mejoras

**Recorridos**

* Los eventos de paso de Journey Optimizer ahora se pueden vincular a otros conjuntos de datos en [Customer Journey Analytics de Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=es). El campo **profileID**, en el esquema integrado de Evento de paso de recorrido, ahora se define como un campo de identidad. [Más información](../reports/sharing-overview.md#integration-cja)

**Gestión de decisiones**

* Al actualizar una oferta, una oferta de reserva, una colección de ofertas o una decisión de oferta a la que se hace referencia directa o indirectamente en un mensaje publicado, las actualizaciones ahora se reflejan automáticamente en el mensaje correspondiente, sin necesidad de volver a publicarlas. [Más información](../offers/offers-e2e.md#insert-decision-in-email)

* Al simular qué ofertas se enviarán para un perfil de prueba determinado, ahora puede modificar los ajustes de simulación predeterminados y ver el código correspondiente a las simulaciones que se pueden utilizar para solucionar problemas. [Más información](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administración**

* Los administradores ahora pueden editar registros PTR con un subdominio CNAME configurado. [Más información](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalización**

* **Agregar a favoritos**: para ayudar a mejorar la eficacia al trabajar con la personalización, hemos introducido el concepto de guardado de favoritos. Añadir atributos diferentes al menú de favoritos permite acceder rápidamente a los elementos más frecuentes. [Más información](../personalization/personalize.md#fav)
