---
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ad04aeddac78a6910258d924148fceca8fd7b6d9
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 18%

---

# Notas de la versión {#release-notes}

En esta página se enumeran todas las nuevas funciones y mejoras de [!DNL Journey Optimizer]. También puede consultar la página de las [últimas actualizaciones de la documentación](documentation-updates.md) para ver más cambios.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.

## Versión de septiembre de 2022{#sept-2022-release}

### Nuevas funciones{#sept-2022-features}


<!--
<table>
<thead>
<tr>
<th><strong>Dynamic content & new conditional rule builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create dynamic content to adapt the content of your messages based on conditional rules.</p> 
<p>Conditional rules are created using a visual rule builder within the Expression Editor, where you can store them for further reuse across your journeys and campaigns.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>For more information, refer to the <a href="../personalization/get-started-dynamic-content.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>
-->

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
<p>Mediante el control de acceso basado en atributos, los administradores pueden controlar el acceso a objetos específicos en función de determinados atributos. Estos atributos pueden ser metadatos agregados a un objeto, como etiquetas. A partir de esta versión, los administradores también pueden definir funciones de usuario que solo tengan acceso a campos u objetos específicos, y datos que correspondan a esos campos u objetos.</p>
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
<th><strong>Administración de datos y privacidad</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con su marco de control de etiquetado y aplicación del uso de los datos (Data Usage Labeling and Enforcement, DULE), Journey Optimizer ahora puede aprovechar las políticas de control de Adobe Experience Platform para evitar que los campos confidenciales se exporten a sistemas de terceros mediante acciones personalizadas. Si el sistema identifica un campo restringido en los parámetros de acción personalizados, se muestra un error que le impide publicar el recorrido.</p>
<p>El uso del etiquetado y aplicación del uso de los datos (Data Usage Labeling and Enforcement, DULE) está actualmente restringido a los clientes seleccionados y se implementará en todos los entornos en una versión futura.</p>
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
<p>Adobe Experience Platform le permite adoptar y aplicar fácilmente políticas de marketing que respeten las preferencias de consentimiento de sus clientes. Las políticas de consentimiento se definen en Adobe Experience Platform. En Journey Optimizer, puede aplicar estas directivas de consentimiento a sus acciones personalizadas. Por ejemplo, puede definir políticas de consentimiento para excluir a los clientes que no hayan aceptado recibir comunicaciones por correo electrónico, push o SMS.
<p>Actualmente, la aplicación automática del consentimiento solo está disponible para las organizaciones que han adquirido la oferta adicional Escudo de atención sanitaria.</p>
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
<p>Journey Optimizer admite la definición de funciones de usuario y políticas de acceso para administrar permisos para funciones y objetos. Hasta <strong>Permisos de Adobe Experience Cloud</strong>, puede crear y administrar funciones, así como asignar los permisos de recursos deseados para estas funciones. Los permisos también le permiten administrar las etiquetas, los entornos limitados y los usuarios asociados a una función específica.</p>
<p> El uso de Permisos está restringido actualmente a clientes seleccionados y se implementará en todos los entornos en una versión futura.</p>
<p>Para obtener más información, consulte la <a href="../administration/attribute-based-access.md">documentación detallada</a>.
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
<p>Para obtener más información, consulte la <a href="../reports/alerts.md">documentación detallada</a>.
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

* La variable **Conjunto de datos de entidad** ya está disponible como un conjunto de datos predeterminado en Adobe Journey Optimizer. Este conjunto de datos de búsqueda incluye metadatos para enriquecer la información de los conjuntos de datos de seguimiento y comentarios. Esto le ayudará a mejorar sus informes y consultas con datos más comprensibles. [Más información](../start/datasets-query-examples.md#entity-dataset)
* Se ha añadido una nueva protección a los recorridos unitarios (comenzando por un evento o una calificación de segmento) para evitar que los recorridos se activen varias veces por error para el mismo evento. La reentrada del perfil se bloqueará temporalmente de forma predeterminada durante 5 minutos. [Más información](../start/guardrails.md#events-g)

**Administración**

* Al habilitar o deshabilitar la lista de permitidos, ahora se muestra una nueva advertencia para detallar los impactos de cada acción. [Más información](../configuration/allow-list.md#enable-allow-list)
* Se ha actualizado la interfaz de usuario para crear superficies de canal, crear grupos de IP, administrar la lista de supresión y la lista de permitidos y configurar el canal SMS.
* Ahora, al crear la primera superficie de canal para un subdominio determinado, el tiempo de procesamiento tardará de 10 minutos a 10 días y solo 3 horas para las superficies posteriores que utilicen ese subdominio. [Más información](../configuration/channel-surfaces.md#create-channel-surface)

<!--* Now when downloading the suppression list as a CSV file, you can choose the file that was previously generated, or generate a new file.-->
* Se ha actualizado la interfaz de usuario para crear ajustes preestablecidos de página de aterrizaje y subdominios de página de aterrizaje. [Más información](../configuration/lp-subdomains.md)

**Controles de auditoría**

* Con Journey Optimizer, puede identificar las acciones realizadas por los usuarios en el sistema en distintos servicios y funcionalidades, como campañas, recorridos, mensajes, páginas de aterrizaje, etc. Los recursos de registro de auditoría ahora incluyen cambios en varias otras acciones y se registran automáticamente cuando se produce la actividad. Obtenga más información [en esta página](../privacy/audit-logs.md).

**Soporte de archivado**

* El nuevo **Conjunto de datos de entidad** incluye un campo Template que permite exportar el formato y la estructura de los mensajes enviados en todos los canales para archivarlos. [Más información](../configuration/archiving-support.md)

**Páginas de aterrizaje**

* Ahora puede utilizar datos contextuales procedentes de otra página dentro de la misma página de aterrizaje. Por ejemplo, si vincula una casilla de verificación a una lista de suscripción en la página de aterrizaje principal, puede utilizar esa lista de suscripción en la subpágina &quot;gracias&quot;. [Más información](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Otros cambios{#sept-2022-other}

* El modo de ráfaga de recorrido se ha sustituido por el modo de envío rápido de Campaign. [Más información](../campaigns/create-campaign.md#rapid-delivery)
* Para mejorar el rendimiento, los grupos de campos de eventos de experiencia ya no se pueden utilizar en recorridos que comiencen por un segmento de lectura, una calificación de segmentos o una actividad de evento empresarial. Este cambio solo se aplica a los nuevos recorridos. Las existentes mantendrán el comportamiento actual. [Más información](../start/guardrails.md#expression-editor)
* Se ha eliminado la limitación de 1 hora para los recorridos de segmentos de lectura programados. Estos recorridos ahora se pueden ejecutar sin demora.

