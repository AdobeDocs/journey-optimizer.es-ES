---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: f1a8305d0f9cc93ae5dc93d73c8ed9513733d1a2
workflow-type: tm+mt
source-wordcount: '4190'
ht-degree: 84%

---

# Notas de la versión {#release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión.

Las notas de la versión anteriores están disponibles en [esta página](release-notes-2022.md). También puede consultar la página de las [últimas actualizaciones de la documentación](documentation-updates.md) para ver más cambios.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.


## Notas de la versión de septiembre de 2023 {#sept-rn-2023}

### Nuevas funciones{#sept-2023-features}

Esta versión incorpora las nuevas funciones que se enumeran a continuación.

<table>
<thead>
<tr>
<th><strong>Atributos calculados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los atributos calculados permiten resumir fácilmente los datos de evento en atributos de perfil a través de una interfaz de usuario intuitiva para mejorar la segmentación, personalización y activación basada en el comportamiento. Con esta función, puede crear atributos calculados de forma automática, administrarlos y utilizarlos en segmentación, destinos de perfil del cliente en tiempo real o Journey Optimizer.<br/><br/>
Además, los atributos calculados simplifican la segmentación y los flujos de trabajo de recorrido para ayudarle a ofrecer sin problemas experiencias relevantes. Obtenga más información en la <a href="../audience/computed-attributes.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/computed-attributes.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Informes de canales consolidados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La función Informe de canal ofrece a analistas y expertos en marketing una descripción general completa de las métricas de tráfico y participación a nivel de canal.</p>
<p>Para acceder a <b>Informe</b> menú, debe tener el <b>Ver informes de canal</b> permiso.</p>
<img src="assets/channel-reports.png"/>
<p>Para obtener más información, consulte la <a href="../reports/channel-report.md">documentación detallada</a>, y <a href="../reports/channel-report.md#channel-report-video">vídeo explicativo</a>.</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Destinos de exportación de conjuntos de datos (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La exportación de conjuntos de datos de Journey Optimizer a destinos de almacenamiento en la nube ya está disponible de forma general. Ahora, puede establecer una conexión activa con las ubicaciones de almacenamiento en la nube para exportar el contenido de los conjuntos de datos.</p>
<img src="../data/assets/dataset-export-setup.png">
<p>Para obtener más información, consulte la <a href="../data/export-datasets.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Almacenamiento de credenciales de aplicación móvil por zona protegida</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta nueva función le permite administrar y asociar fácilmente credenciales push con una zona protegida dedicada en las superficies de la aplicación.</p>
<p>Para obtener más información, consulte la <a href="../in-app/inapp-configuration.md#channel-prerequisites">documentación detallada</a>.</p>
</tr>
</tbody>
</table>

### Mejoras {#sept-2023-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Personalización**

* Además de los fragmentos visuales, ahora es posible crear, guardar y reutilizar fragmentos de expresiones desde la interfaz de Journey Optimizer a través del Editor de expresiones. Los fragmentos de expresión reemplazan a las expresiones guardadas anteriormente. [Más información](../personalization/use-expression-fragments.md)

**Alerta**

* Se ha introducido un nuevo tipo de alerta del sistema. Ahora puede recibir una notificación cuando **Leer audiencia** falla la actividad. [Más información](../reports/alerts.md).

**Canal web**

* SPA Ahora, las aplicaciones de una sola página () se pueden crear en el editor visual web, lo que le permite seleccionar a qué vistas específicas desea aplicar las modificaciones de la página web. Una vista puede definirse como un sitio completo o como un grupo de elementos visuales en un sitio, como la página de inicio, la totalidad del sitio de productos o el marco de preferencias de envío en todas las páginas de cierre de compra. Se necesita una configuración de desarrollador única para definir las vistas en la implementación del SDK web de Adobe Experience Platform; esto permite a los especialistas en marketing crear y ejecutar campañas web de Adobe Journey Optimizer SPA en el momento de la creación de las campañas web de la. [Más información](../web/web-spa.md)

* Al editar una página con el diseñador web, ahora puede agregar nuevos cambios al contenido directamente desde el panel Modificaciones, sin necesidad de seleccionar un componente y editarlo desde la interfaz del diseñador. [Más información](../web/manage-web-modifications.md#add-modifications)

* Al configurar subdominios web, ahora tiene la opción de agregar su propio subdominio, además de utilizar un subdominio ya delegado al Adobe. [Más información](../web/web-delegated-subdomains.md#web-configure-new-subdomain)

**Recorridos**

* Al duplicar un recorrido, ahora puede definir el nombre de la copia de recorrido. [Más información](../building-journeys/journey-gs.md#uplicate-a-journey)



* La compatibilidad con las respuestas de acciones personalizadas ahora es GA. Esta capacidad le permite aprovechar las respuestas de llamadas de API en acciones personalizadas y organizar su recorrido en función de estas respuestas. Además, se ha añadido una nueva protección para limitar todas las acciones aduaneras a 15 000 llamadas en 30 segundos por punto final. [Más información](../action/action-response.md)
<!--
* The maximum duration that you can define in the Wait activity is now 29 days instead of 30.
-->

**Canal de correo electrónico**

* Una nueva opción en la configuración de la superficie de correo electrónico permite elegir enviar mensajes transaccionales a perfiles incluso si sus direcciones de correo electrónico están en el Adobe [!DNL Journey Optimizer] lista de supresión. [Más información](../email/email-settings.md#send-to-suppressed-email-addresses)

**Canal de SMS**

* Dos campos nuevos, **Mensaje de inclusión** y **Mensaje de ayuda**, se han agregado a la pantalla de configuración de la API, lo que permite a los usuarios personalizar las respuestas para palabras clave entrantes. Tenga en cuenta que esto solo está disponible para el proveedor de SMS de Sinch. [Más información](../sms/sms-configuration.md#create-api)

* La exclusión de SMS ya no se administra en el nivel de canal. Ahora es específico para un número, lo que significa que si algunos perfiles se excluyen de un número determinado o código corto, aún puede enviarles mensajes de otros números que pueda utilizar para enviar mensajes SMS. Una nueva opción permite seleccionar el **Número de exclusión** que desee utilizar para una superficie determinada. [Más información](../sms/sms-configuration.md#message-preset-sms)

**Canal de correo directo**

* Ahora puede cifrar archivos destinados a sus proveedores de correo postal cuando se transfieren a un servidor. Para ello, hay un nuevo campo disponible en la pantalla de configuración de enrutamiento de archivos, que le permite copiar y pegar la clave de cifrado. [Más información](../direct-mail/direct-mail-configuration.md)

**Creación de informes**

* Ahora puede exportar informes de Journey Optimizer como archivo CSV. Obtenga más información en la [documentación detallada](../reports/global-report.md#export-reports) y el [vídeo explicativo](../reports/global-report.md#video-csv).

**Recursos**

* Una nueva opción para Recursos le permite elegir el repositorio de sus Recursos en Journey Optimizer. Puede optar por un repositorio de Assets Essentials o un repositorio as a Cloud Service de Assets, siempre que sea el propietario de esta solución. [Más información](../content-management/assets-essentials.md)

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->

## Notas de la versión de agosto de 2023 {#aug-rn-2023}

### Nuevas funciones{#aug-2023-features}

Esta versión incorpora las nuevas funciones que se enumeran a continuación.

<table>
<thead>
<tr>
<th><strong>Envío de mensajes en la aplicación en los recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, puede enviar mensajes personalizados en la aplicación a la gente que use la aplicación y esté en un recorrido. Utilice Journey Optimizer para diseñar notificaciones y personalizar el diseño, la visualización, el texto y los botones del mensaje para crear una experiencia perfecta.</p>
<img src="assets/do-not-localize/in-app-jo.gif"/>
<p>Para obtener más información, consulte la <a href="../in-app/create-in-app.md">documentación detallada</a>.</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Validación de correos electrónicos con listas semilla</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear y administrar listas semilla en Journey Optimizer. Una lista semilla consiste en direcciones internas que se pueden añadir al público real y recibir el mismo mensaje que los perfiles objetivo en el momento de la ejecución del envío. Utilice esta capacidad para monitorizar las comunicaciones enviadas y asegurarse de que todos los formatos de visualización, direcciones URL, imágenes y vínculos son correctos.</p>
<img src="../configuration/assets/seed-list-details.png">
<p>Para obtener más información, consulte la <a href="../configuration/seed-lists.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Generate text and images with the Content assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the Content assistant. You can now use the Content assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
<p>This capability is currently available as a private beta.</p>
<img src="assets/gen-ai-image-2.png"/>
<p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->



### Mejoras {#aug-2023-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

<!--
**APIs**

A new API to create and manage Content Fragments is now available. [Learn more](https://developer.adobe.com/journey-optimizer-apis/references/content-templates/#tag/Content-fragment-API){target="_blank"}.-->

<!--**Email channel**

A new option is available in the email surface settings to include email addresses suppressed due to spam complaint in your transactional messages audiences. Even if they marked marketing messages as spam, these profiles can then receive transactional messages, such as password reset or account statements. This option is disabled by default.-->

**Recorridos**

* Ahora puede utilizar las respuestas de llamadas de API en acciones personalizadas y organizar su recorrido en función de estas respuestas. Actualmente, esta función está disponible como una versión beta privada. [Más información](../action/action-response.md).
* Se ha introducido un nuevo tipo de alerta del sistema. Ahora puede recibir notificaciones cuando falle una acción personalizada. [Más información](../reports/alerts.md).
  <!--* When duplicating a journey, you can now define the name of the journey copy.-->


**Correo directo**

* Azure ahora se puede seleccionar como tipo de servidor en la configuración de enrutamiento de archivos. [Más información](../direct-mail/direct-mail-configuration.md#file-routing-configuration)
* El ampersand está ahora disponible como campo separador de columnas en la configuración de superficie de correo postal. [Más información](../direct-mail/direct-mail-configuration.md#direct-mail-surface)




## Notas de la versión de julio de 2023 {#july-rn-2023}

### Nuevas funciones{#july-2023-features}

<table>
<thead>
<tr>
<th><strong>Composición de audiencia</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear flujos de trabajo de composición para combinar audiencias de Adobe Experience Platform existentes en un lienzo visual y aprovechar varias actividades (división, enriquecer) para crear audiencias nuevas. Las audiencias recién creadas se vuelven a guardar en Adobe Experience Platform junto con las audiencias existentes y se pueden aprovechar en las campañas de Journey Optimizer para dirigirse a los clientes.</p>
<img src="assets/do-not-localize/gif-ao.gif"/>
<p>Para obtener más información, consulte la <a href="../audience/get-started-audience-orchestration.md">documentación detallada</a>.</p>
<p>La composición de audiencia viene totalmente integrada con el nuevo menú "Audiences" de Adobe Experience Platform, que sirve como portal centralizado para los públicos. Ahora puede utilizar una página de exploración que incluya un nuevo panel con tendencias de segmentos y superposiciones para encontrar nuevos insights y explorar las herramientas organizativas para la carpeta y el etiquetado. Esta experiencia incluye controles de gobernanza para el etiquetado de público estandarizado, así como funciones de administración del ciclo vital de los públicos para administrar los flujos de trabajo de activación. Con esta nueva experiencia de administración, ahora puede administrar públicos de forma fácil y segura desde un solo lugar. Para obtener más información, consulte la <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=es" target="_blank">Documentación de Adobe Experience Platform</a>.</p></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de correo directo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede añadir mensajes de correo postal en sus campañas. El correo postal es un canal sin conexión que le permite personalizar y generar los archivos necesarios para que los proveedores de correo postal envíen correo a sus clientes.</p>
<p>Al preparar un envío de correo postal, Journey Optimizer genera un archivo con todos los perfiles de destino y la información de contacto elegida (por ejemplo, una dirección postal). Después, puede enviar este archivo al proveedor de correo postal que se encarga de la entrega real.</p>
<p>Por ahora, el canal de correo directo no está disponible para las organizaciones que han adquirido la oferta complementaria Adobe Healthcare Shield</p>
<img src="assets/do-not-localize/gif-dm.gif"/>
<p>Para obtener más información, consulte la <a href="../direct-mail/get-started-direct-mail.md">documentación detallada</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conversión del contenido del HTML para el diseñador de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede importar y convertir cualquier contenido de HTML en el editor de correo electrónico de Journey Optimizer. Los bloques de contenido se identifican automáticamente y están disponibles en el diseñador de correo electrónico: utilice sus potentes funciones de diseño para actualizarlos y personalizarlos.</p>
<img src="assets/html-convert.png">
<p>Para obtener más información, consulte la <a href="../email/existing-content.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Uso de etiquetas en Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Además de las campañas y los recorridos, ahora puede asignar etiquetas unificadas de Adobe Experience Platform a sus páginas de aterrizaje, plantillas de contenido, fragmentos y listas de suscripción. Esto le permite clasificarlas fácilmente y mejorar la búsqueda y la navegación en todas las listas. </p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Para obtener más información, consulte la <a href="../start/search-filter-categorize.md#tags">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>API de plantillas de contenido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear y administrar plantillas de contenido de Adobe Journey Optimizer mediante API dedicadas, lo que proporciona una integración perfecta con su sistema de contenido existente.</p>
<p>Para obtener más información, consulte la <a href="https://developer.adobe.com/journey-optimizer-apis/references/content/">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#july-2023-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.


**Campañas**

Los eventos contextuales relacionados con campañas ya están disponibles para su uso en el menú &quot;Atributos contextuales&quot; del editor de personalización.


**Audiences**

Se han realizado mejoras en el selector de públicos en recorridos o campañas, añadiendo nuevas columnas que muestran el origen y la frecuencia de actualización de los públicos. Con el lanzamiento del portal de composición de audiencia, Adobe Experience Platform y Adobe Journey Optimizer han actualizado el uso de &quot;públicos&quot; y &quot;segmento&quot; dentro del sistema y la documentación.

* Audiencia: conjunto de personas, cuentas, hogares u otras entidades que comparten características y comportamientos comunes.
* Definición del segmento: en Adobe Experience Platform, las reglas utilizadas para describir las características clave o el comportamiento de un público destinatario. Este término se conocía anteriormente como &quot;segmento&quot;.

Como resultado, dentro de Adobe Journey Optimizer y de la IU de Adobe Experience Platform, los &quot;Segmentos&quot; se sustituyen por &quot;Públicos&quot; para reflejar esta nueva ruta de creación y administración de públicos.

**API**

El método JWT para generar tokens de acceso para la autenticación de API de Adobe Journey Optimizer ha quedado obsoleto. Todas las nuevas integraciones deben crearse con el método de autenticación de servidor a servidor OAuth. Adobe también recomienda migrar las integraciones existentes al método OAuth. [Más información](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.


**Otros cambios**

La exportación de conjuntos de datos de Journey Optimizer a destinos de almacenamiento en la nube ya está disponible para todos los clientes como beta pública. Ahora, puede establecer una conexión activa con las ubicaciones de almacenamiento en la nube para exportar el contenido de los conjuntos de datos. [Más información](../data/export-datasets.md)





## Notas de la versión de junio de 2023 {#june-rn-2023}

<table>
<thead>
<tr>
<th><strong>Campañas activadas por API para casos de uso de marketing</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar las API para activar las campañas de marketing en Adobe Journey Optimizer desde un sistema externo.</p>
<p>Hasta esta versión, la capacidad de campañas activadas por API cubría varias necesidades operativas y de mensajería transaccional, como los restablecimientos de contraseña o el token OTP, pero no se podía utilizar para crear campañas de marketing. Los canales disponibles para las campañas activadas por API son: correo electrónico, SMS y mensajes push.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Para obtener más información, consulte la <a href="../campaigns/api-triggered-campaigns.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>

<!--
### Improvements {#june-2023-improvements}


**Audiences**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.

**Journeys**

You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.
-->

<!--
## June 2023 early release notes {#june-rn-2023}

Information below is subject to change without prior notice until the release availability date. Updated documentation will be published at the release date, and direct links will be added in this page.

**Audiences**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    


**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.     

* A new type of system alert has been introduced. You can now get notified when a custom action fails.
-->

## Notas de la versión de mayo de 2023 {#may-rn-2023}

### Nuevas funciones{#may-2023-features}



<table>
<thead>
<tr>
<th><strong>Experimentación de contenido en campañas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ahora admite experimentos en campañas. Los experimentos son ensayos aleatorios, lo que en el contexto de las pruebas en línea significa que expone a algunos usuarios seleccionados aleatoriamente a una variación determinada de un mensaje y a otro conjunto de usuarios seleccionados aleatoriamente a otra variación o tratamiento. Después de la exposición, puede medir las métricas de resultado que le interesan, como aperturas de correos electrónicos, suscripciones o compras.</p>
<img src="assets/do-not-localize/experiment.gif"/>
<p>Para obtener más información, consulte la <a href="../campaigns/content-experiment.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Objective reporting and performance measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the Objectives tab of your campaign reports.</p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../reports/campaign-global-report.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->


<table>
<thead>
<tr>
<th><strong>Creación y uso de fragmentos en el contenido del correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear, utilizar y administrar fragmentos para montar rápidamente sus correos electrónicos y plantillas de contenido. Un fragmento es un componente reutilizable creado previamente al que se puede hacer referencia en varios correos electrónicos en campañas y recorridos de Journey Optimizer para un proceso de diseño mejorado y acelerado.</p>
<img src="assets/do-not-localize/fragments.gif"/>
<p>Para obtener más información, consulte la <a href="../content-management/fragments.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Uso de etiquetas en las campañas (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede asignar Etiquetas unificadas de Adobe Experience Platform a sus campañas. Esto le permite clasificarlos fácilmente y mejorar la búsqueda desde la lista de campañas. Tenga en cuenta que la función de etiquetas unificadas está actualmente en versión beta.</p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Para obtener más información, consulte la <a href="../start/search-filter-categorize.md#tags">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Modelo de clasificación de IA de optimización personalizada (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los modelos de clasificación de IA de optimización personalizada ahora están disponibles de forma general en Gestión de decisiones. Este nuevo tipo de modelo le permite optimizar y personalizar ofertas en función de las audiencias y ofrecer rendimiento.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Para obtener más información, consulte la <a href="../offers/ranking/personalized-optimization-model.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>



### Mejoras {#may-2023-improvements}

**Audiencias**

* Como preparación para la disponibilidad general de la función de Audience Portal, Adobe Experience Platform está actualizando el uso de &quot;audiencias&quot; y &quot;segmentos&quot; en el sistema y la documentación.

   * Audiencia: conjunto de personas, cuentas, hogares u otras entidades que comparten características y comportamientos comunes.
   * Definición del segmento: en Adobe Experience Platform, las reglas utilizadas para describir las características clave o el comportamiento de un público destinatario. Este término se conocía anteriormente como &quot;segmento&quot;.

  Como resultado, dentro de Adobe Journey Optimizer y de la IU de Adobe Experience Platform, verá &quot;Segmentos&quot; reemplazado por &quot;Audiencias&quot; para reflejar esta nueva ruta de creación y administración de audiencias.

  Las traducciones del término &quot;audiencia&quot; al referirse a un grupo de perfiles destinados a recibir un mensaje se armonizaron en todos los productos de Digital Experience para algunos idiomas:

   * Alemán: Zielgruppe
   * Portugués brasileño: público-alvo
   * Español: público destinatario

<!--* Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.-->

**Canal de SMS**

* Infobip se ha agregado como proveedor al configurar las superficies de canal de SMS. [Más información](../sms/sms-configuration.md)
* Twillio: La configuración de credenciales de API ahora incluye la capacidad de agregar el SID del servicio de mensajería para una integración perfecta con su cuenta de Twillio. [Más información](../sms/sms-configuration.md)

**Canal en la aplicación**

* Se han añadido nuevas reglas de activación de mensajes para el servicio Places de Adobe. [Más información](../in-app/inapp-configuration.md)
* Se han añadido nuevas funciones de Adobe Experience Platform Assurance para capturar eventos de dispositivo para añadirlos como reglas de activación.

<!--
**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.
-->

**Campañas**

* Ahora es posible duplicar una campaña desde la pantalla del inventario utilizando el menú de acción de los tres puntos. [Más información](../campaigns/modify-stop-campaign.md#duplicate)
* Ahora puede eliminar borradores de modificaciones en una campaña en directo.
* Los pasos para activar una campaña se han simplificado. [Más información](../campaigns/modify-stop-campaign.md)

**Gestión de decisiones**

* Ahora puede editar la restricción de frecuencia si la oferta tiene el estado **[!UICONTROL Borrador]** y nunca antes se había publicado con la restricción de frecuencia habilitada. [Más información](../offers/offer-library/add-constraints.md#frequency-capping)

**Personalización**

* Ahora puede seleccionar e insertar referencias de recursos directamente desde el Editor de personalización cuando trabaja en contenido de HTML.

### Correcciones{#may-2023-fixes}

* Mensajes en la aplicación: se ha corregido un problema por el que la programación de campañas entraba en conflicto con la configuración de frecuencia de mensajes.


## Notas de la versión de abril de 2023 {#apr-rn-2023}

<!--Information below is subject to change without prior notice until the release availability date. Updated documentation will be published at the release date, and direct links will be added in this page.

**Release date**: April 27, 2023-->

### Nuevas funciones{#apr-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal web (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer está ampliando sus funciones en todos los canales añadiendo compatibilidad con canales web. Ahora puede crear, cambiar y previsualizar experiencias web como cualquier otro canal mediante una interfaz visual inteligente e intuitiva para personalizar la experiencia de los usuarios finales. Tenga en cuenta que actualmente en Journey Optimizer solo puede crear experiencias web en campañas.</p>
<img src="assets/do-not-localize/web-authoring.gif"/>
<p>Para obtener más información, consulte la <a href="../web/get-started-web.md">documentación detallada</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Flujo de trabajo de inicio rápido de incorporación al dispositivo móvil (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ya está disponible el nuevo flujo de trabajo de inicio rápido de incorporación al dispositivo móvil. Utilice esta nueva función de producto para configurar rápidamente el SDK móvil y empezar a recopilar y validar datos de eventos móviles, así como enviar notificaciones push móviles con Adobe Journey Optimizer. Se puede acceder a esta funcionalidad a través de la página de inicio de recopilación de datos como una versión beta pública.</p>
<img src="../push/assets/mobile-wf-home.png"/>
<p>Para obtener más información, consulte la <a href="../push/mobile-onboarding-wf.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nuevo tablero de recorrido (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> El tablero de recorrido ahora se divide en dos pestañas:</p>
<ul><li>Utilice la pestaña <strong>Información general</strong> para acceder a un nuevo tablero que muestra métricas clave relacionadas con sus recorridos.</li>
<li>Utilice la pestaña <strong>Examinar</strong> para acceder a la lista de todos los recorridos.</li></ul>
<p>Se puede acceder a esta funcionalidad en todos los recorridos como una versión beta pública.</p>
<img src="assets/do-not-localize/journey-dashboard.gif"/>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-gs.md#journey-access">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#april-2023-improvements}

**Recorridos**

* El lienzo del recorrido muestra ahora el ID de actividad en las actividades de mensajes y las etiquetas finales. Esto mejora la creación de informes y la segmentación
* Se ha mejorado el diseño del panel de configuración, que aparece en acciones, fuentes de datos, eventos y recorridos.
* Nuevo conocimiento del número de nodos en lienzo con garantías para ayudar a crecer: mantenga los recorridos fáciles de leer, realice controles de calidad y solucione problemas con un número máximo de nodos por recorrido a 50. [Más información](../start/guardrails.md#journeys-guardrails-journeys)
* Al añadir un [Correo electrónico](../email/create-email.md), [SMS](../sms/create-sms.md) o [Push](../push/create-push.md) en un recorrido, la superficie se rellena ahora previamente, de forma predeterminada, con la última superficie utilizada para dicho canal, en el recorrido actual.
* Ahora puede definir parámetros de consulta estáticos o dinámicos en sus acciones personalizadas. [Más información](../action/about-custom-action-configuration.md#url-configuration)

**Creación de informes**

* Ahora puede exportar informes de Journey Optimizer como PDF. [Más información](../reports/global-report.md#export-reports)

**Diseñador de contenido**

* Se ha actualizado el Diseñador de contenido de Adobe Journey Optimizer y ahora es más fácil acceder a los estilos y componentes de diseño. Esta nueva versión ofrece una experiencia de usuario mejorada e incluye un mayor rendimiento, compatibilidad parcial en modo oscuro y compatibilidad con nuevos estándares de accesibilidad.



## Notas de la versión de marzo de 2023 {#mar-2023}

### Nuevas funciones{#mar-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal en la aplicación (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, puede enviar mensajes personalizados en la aplicación a los usuarios de la aplicación dentro de una campaña. Utilice Journey Optimizer para diseñar notificaciones y personalizar el diseño, la visualización, el texto y los botones del mensaje para crear una experiencia perfecta.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Para obtener más información, consulte la <a href="../in-app/get-started-in-app.md">documentación detallada</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Rastreo de clics de SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con el rastreo de clics de SMS, puede monitorizar el rendimiento de las URL acortadas, identificar quién hizo clic en ellas y utilizar estos datos para redirigirse a esos clientes con campañas posteriores.</p>
<img src="assets/do-not-localize/sms-tracking.gif"/>
<p>Para obtener más información, consulte la <a href="../sms/create-sms.md#sms-content">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Uso de etiquetas en los recorridos (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Como profesional de Journey Optimizer, ahora puede organizar los objetos de negocio mediante etiquetas. Las etiquetas son una forma rápida y sencilla de clasificar objetos para mejorar la búsqueda. Actualmente, esta funcionalidad está en versión beta y solo está disponible para recorridos.</p>
<p>Para obtener más información, consulte la <a href="../start/search-filter-categorize.md#tags">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#mar-2023-improvements}

**Recorridos**

* La nueva **API de limitación** le permite establecer un límite en la cantidad de eventos enviados por segundo, lo que evita picos de tráfico abrumadores en sus sistemas externos o API. Cuando se alcanza el límite establecido, todas las llamadas a la API subsiguientes se ponen en cola y se procesan lo antes posible en el orden en que se recibieron. Tenga en cuenta que esta función solo admite una configuración de limitación en todas las zonas protegidas. [Más información](../configuration/external-systems.md)
* El lienzo de recorrido se ha mejorado para que la experiencia del usuario sea más sencilla y mejorada. Al final de cada ruta en el lienzo, se han eliminado los marcadores vacíos. Ahora puede simplemente agregar sus actividades arrastrándolas al final de una ruta.
* En el lienzo del recorrido, la etiqueta de **Fin** ya no se configura automáticamente con el nombre de la actividad anterior. Los usuarios pueden agregar manualmente una etiqueta personalizada si es necesario.
* El tiempo de espera predeterminado y la duración del error en las propiedades del recorrido han cambiado de 5 a 30 segundos. [Más información](../configuration/external-systems.md#timeout)
* La tasa de limitación predeterminada en las actividades de lectura de audiencia ha cambiado de 20 000 a 5000 mensajes por segundo. [Más información](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Se ha añadido un mecanismo de protección al modo de prueba para escuchar solo los eventos enviados a través de la interfaz. Los eventos enviados a través de una herramienta externa no se tienen en cuenta. [Más información](../building-journeys/testing-the-journey.md)


<!-- 
* When adding an Email, SMS or Push action in a journey, the surface is now pre-filled, by default, with the last used surface for that channel.
* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)
* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)
* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->

**Gestión de decisiones**

* Para evitar cualquier posible confusión con la reciente versión de la funcionalidad de etiquetas en Adobe Experience Platform, se ha cambiado el nombre de las etiquetas de Gestión de decisiones a &quot;Calificadores de colección&quot;.

  Tenga en cuenta que, aunque el término &quot;etiqueta&quot; ya no se utiliza en la interfaz de usuario de Gestión de decisiones, se sigue utilizando en servicios backend como API y conjuntos de datos.

* Ahora puede restablecer el contador de límite de oferta diariamente, semanalmente o mensualmente. [Más información](../offers/offer-library/add-constraints.md#capping)

* También puede elegir qué evento de Adobe Experience Platform se debe tener en cuenta para el límite de Offer Decisioning. [Más información](../offers/offer-library/add-constraints.md#capping)

* Se han añadido parámetros adicionales en la pantalla de creación de ubicaciones. Permiten controlar si una oferta se puede duplicar en varias ubicaciones y especificar si el contenido y los metadatos de la oferta se deben incluir en la respuesta de API. [Más información](../offers/offer-library/creating-placements.md)

**Personalización**

* Ahora puede incluir texto alternativo predeterminado para atributos de perfil basados en cadenas en el Editor de expresiones. Estos valores se mostrarán si los atributos seleccionados no devuelven ningún resultado. [Más información](../personalization/personalization-build-expressions.md#add)

**Creación de informes**

* La funcionalidad del widget de creación de informes se ha mejorado con la capacidad de personalizar la forma en que los usuarios ven sus datos. Con esta mejora, los usuarios ahora pueden elegir entre varias opciones de visualización, incluidos gráficos, tablas y gráficos circulares.

  Para tener acceso a las últimas utilidades, tenga en cuenta que tendrá que restablecer los distintos paneles de creación de informes. Para obtener más información sobre la personalización de tableros, consulte la [documentación detallada](../reports/global-report.md#modify-dashboard).

## Notas de la versión de febrero de 2023 {#feb-2023}

### Nuevas funciones{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal en la aplicación (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, puede enviar mensajes personalizados en la aplicación a los usuarios de la aplicación dentro de una campaña. Utilice Journey Optimizer para diseñar notificaciones y personalizar el diseño, la visualización, el texto y los botones del mensaje para crear una experiencia perfecta.</p>
<p><strong>Precaución</strong>: Actualmente, esta funcionalidad está en versión beta y solo está disponible para los clientes de la versión beta. Para unirse al programa beta, póngase en contacto con el Servicio de atención al cliente de Adobe.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Para obtener más información, consulte la <a href="../in-app/get-started-in-app.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Exportación de los conjuntos de datos de Journey Optimizer a los destinos de almacenamiento en la nube (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, puede establecer una conexión activa con las ubicaciones de almacenamiento en la nube para exportar el contenido de los conjuntos de datos. Los destinos disponibles son: almacenamiento en la nube Amazon S3, Azure Blob, Azure Data Lake Gen 2, zona de aterrizaje de datos, almacenamiento en la nube de Google, SFTP.</p>
<p><strong>Precaución</strong>: Esta funcionalidad está actualmente en versión beta y está disponible para todos los usuarios de Adobe Journey Optimizer. Póngase en contacto con su representante de Adobe para obtener acceso a los destinos si todavía no tiene acceso.</p>
<img src="assets/do-not-localize/gif-destinations.gif"/>
<p>Para obtener más información, consulte la <a href="../data/export-datasets.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--

<table>
<thead>
<tr>
<th><strong>Performance Measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the <strong>Objective</strong> tab of your campaign reports. </p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

+++ Learn more about Performance Measurement

The **[!UICONTROL Objective]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric. With this feature, you can effectively track and analyze your campaign's performance and make informed decisions to improve your results.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of pre-configured **[!UICONTROL Objectives]** is available, but you can also customize your report by adding new **[!UICONTROL Datasets]** and defining your own objectives. 

By selecting the desired Objectives, the **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets provide a comprehensive and insightful summary of your delivery performance, allowing you to closely monitor and evaluate the success of your campaign.

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your primary objective against another performance metric.

Note that each widget can be resized and deleted as needed.
+++




<table>
<thead>
<tr>
<th><strong>Use Tags in your Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer practitioner, you can now organize your business objects using tags. Tags are a quick and easy way of classifying objects to improve search. Tags are currently only available for Journeys.</p>
</td>
</tr>
</tbody>
</table>

-->

### Mejoras {#feb-2023-improvements}

**Recorridos**

* El campo **Período de espera de reentrada** se ha añadido a las propiedades del recorrido. Este campo permite definir el tiempo de espera antes de permitir que un perfil vuelva a entrar en el recorrido en el caso de recorridos unitarios (empezando con un evento o una calificación de audiencia). Esto evita que los recorridos se activen varias veces por error para el mismo evento. De forma predeterminada, el campo se establece en 5 minutos. [Más información](../building-journeys/journey-gs.md#entrance)

* Se han realizado mejoras para las **fechas de inicio y finalización del recorrido**. Si no ha especificado una fecha de inicio, se añadirá ahora automáticamente en el momento de la publicación. Para los recorridos de **Leer audiencia**, ahora puede añadir una fecha de finalización. Esto permite que los perfiles salgan automáticamente cuando se alcanza la fecha. [Más información](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**Administración**

* **Lista de permitidos**: ahora, puede descargar la lista de permitidos como un archivo .csv. [Más información](../configuration/allow-list.md#download-allowed-list)

* **Superficie de correo electrónico**: se ha añadido una comprobación adicional a la configuración de la superficie del correo electrónico: si el registro MX del subdominio utilizado en el campo **Responder a la dirección (correo electrónico)** o **Dirección de correo electrónico en CCO** no está configurado correctamente, la superficie del correo electrónico ya no se podrá crear más. Debe tenerlo configurado o utilizar otro. [Más información](../email/email-settings.md#reply-to-email)

* **Superficie de correo electrónico**: en la sección **Parámetros de seguimiento de URL** de la configuración de la superficie del correo electrónico, el límite de cada campo **Valor** se ha actualizado de 255 caracteres a 5 KB para la compatibilidad con el seguimiento de Adobe Analytics. [Más información](../email/email-settings.md#url-tracking)

**Gestión de decisiones**

* **Ubicaciones**: se han añadido parámetros adicionales en la pantalla de creación de ubicaciones. Permiten controlar si una oferta se puede duplicar en varias ubicaciones y especificar si el contenido y los metadatos de la oferta se deben incluir en la respuesta de API. [Más información](../offers/offer-library/creating-placements.md)

* **Personalización de URL**: al añadir direcciones URL como contenido a las representaciones de las ofertas, ahora puede personalizar estas direcciones URL con el Editor de expresiones. [Más información](../offers/offer-library/add-representations.md)

## Notas de la versión de enero de 2023{#jan-2023-release}

### Nuevas funciones{#jan-2023-features}

<table>
<thead>
<tr>
<th><strong>Higiene de los datos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform proporciona un conjunto de funcionalidades de higiene de datos que le permiten administrar los datos almacenados mediante eliminaciones programáticas de registros de consumidores y conjuntos de datos. Esta funcionalidad ya está disponible para Adobe Journey Optimizer. </p>
<p>Puede administrar los almacenes de datos para asegurarse de que la información se utiliza según lo esperado, se actualiza cuando es necesario corregir datos incorrectos y se elimina cuando las políticas organizativas lo consideran necesario.</p>
<p><strong>Precaución</strong>: Actualmente, las funcionalidades de higiene de los datos solo están disponibles para las organizaciones que han adquirido las ofertas de complementos <strong>Escudo de atención sanitaria</strong> y <strong>Escudo de seguridad y privacidad</strong>.</p><p>Para obtener más información, consulte la <a href="../privacy/data-hygiene.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Plantillas de contenido de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear plantillas de contenido independientes que se pueden aprovechar en distintos recorridos y campañas para que las pueda reutilizar rápidamente.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>Obtenga información sobre cómo crear, editar y utilizar plantillas de contenido en <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html?lang=es">este vídeo</a>. Para obtener más información, consulte la <a href="../content-management/content-templates.md">documentación detallada</a>.
</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#jan-2023-improvements}

**Recorridos**

* Al añadir **Calificación de audiencia** o **Leer audiencia** en un recorrido, el área de nombres ahora se rellena previamente con la última utilizada de forma predeterminada. Consulte las secciones [Calificación de audiencia](../building-journeys/audience-qualification-events.md#about-segment-qualification) y [Leer audiencia](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* En el lienzo del recorrido, hay un nuevo botón disponible en la barra de herramientas que le permite descargar una captura de pantalla del recorrido.

**Diseñador de correos electrónicos**

* Ahora puede exportar el contenido del correo electrónico desde el menú **Exportar HTML**. Los archivos exportados están disponibles en un archivo de compresión (.ZIP).

**Administración**

* Una nueva subsección ofrece recomendaciones sobre la creación de la dirección **Responder a (correo electrónico)** y la gestión adecuada de las respuestas. [Más información](../email/email-settings.md#reply-to-email)

* Al crear o editar **Grupos de IP**, los registros PTR asociados ahora se muestran en la lista de IP y al pasar el ratón por encima de las direcciones IP seleccionadas. [Más información](../configuration/ip-pools.md#create-ip-pool)

* Después de seleccionar un grupo de IP en una superficie de canal, la información de registro PTR ahora es visible al pasar el ratón por encima de las direcciones IP. [Más información](../email/email-settings.md#subdomains-and-ip-pools)

* La interfaz de usuario para editar [Registros PTR](../configuration/ptr-records.md#edit-ptr-record) y [campos de ejecución](../configuration/primary-email-addresses.md) se ha actualizado.

* Se ha mejorado la interfaz de usuario para crear y editar subdominios. [Más información](../configuration/delegate-subdomain.md)

* La lista de supresión **Cargas recientes** se ha actualizado. [Más información](../configuration/manage-suppression-list.md#recent-uploads)

**Campañas**

* Ahora se genera automáticamente una solicitud cURL de ejemplo que permite la ejecución de campañas activadas por API y está disponible en la pantalla de la campaña. [Más información](../campaigns/api-triggered-campaigns.md)


**Personalización**

* Hay disponibles nuevas funciones de ayuda: formatCurrency, charCodeAt, stringToDate, toString, formatNumber y toHexString. Además, la función toDateTimeOnly ahora acepta tipos de campo de cadena, fecha, larga e int. [Más información](../personalization/functions/functions.md)
