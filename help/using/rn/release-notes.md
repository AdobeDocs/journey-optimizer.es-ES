---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: f07a46e6fc42afb80275557dfe8bd27f51e4fad9
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 57%

---

# Notas de la versión {#release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión.

Las notas de la versión anteriores están disponibles en [esta página](release-notes-2022.md). También puede consultar la página de las [últimas actualizaciones de la documentación](documentation-updates.md) para ver más cambios.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.


## Notas de la versión anticipadas de febrero de 2023 {#feb-2023}

Esta sección contiene información previa al lanzamiento. Las fechas del lanzamiento, las características y otras informaciones están sujetas a cambios sin previo aviso. La documentación detallada estará disponible en la fecha de lanzamiento.

Disponibilidad: **22 de febrero de 2023**

### Mejoras {#feb-2023-improvements}

**Recorridos**

* La variable **Período de espera de reentrada** se ha añadido al campo de propiedades del recorrido. Este campo le permite definir el tiempo de espera antes de permitir que un perfil vuelva a entrar en el recorrido en recorridos unitarios (empezando por un evento o una calificación de segmento). Esto evita que los recorridos se activen varias veces por error para el mismo evento. De forma predeterminada, el campo se establece en 5 minutos.

* Se han realizado mejoras para **Fechas de inicio y finalización del recorrido**. Si no ha especificado una fecha de inicio, esta se añade automáticamente en el momento de la publicación. Para **Leer segmento** recorridos, ahora puede añadir una fecha de finalización. Esto permite a los perfiles salir automáticamente cuando se llega a la fecha.

* El lienzo de Recorrido se ha mejorado para que la experiencia del usuario sea más sencilla y mejorada. Al final de cada ruta en el lienzo, se han eliminado los marcadores de posición vacíos. Ahora puede simplemente agregar sus actividades arrastrándolas a cualquier lugar entre nodos.

* Se ha mejorado la administración de tiempos de espera y errores en recorridos. Las rutas de tiempo de espera y de error ahora siempre se añaden en el lienzo. Hay disponible un nuevo botón de la barra de herramientas para mostrar u ocultar estas rutas.

* Se ha introducido un nuevo tipo de alerta del sistema. Ahora puede recibir notificaciones cuando falla una acción personalizada.


**Administración**

* **Lista de permitidos** - Ahora puede descargar la lista de permitidos como archivo .csv .

* **Superficie de correo electrónico** - Se ha añadido una comprobación adicional a la configuración de la superficie del correo electrónico: si el registro MX del subdominio utilizado en la variable **Responder a la dirección (correo electrónico)** o en el **Dirección de correo electrónico CCO** no está configurado correctamente, ya no se puede crear la superficie del correo electrónico. Debe tenerlo configurado o usar otro.

* **Superficie de correo electrónico** - En la sección de parámetros de seguimiento de URL de la configuración de la superficie del correo electrónico, el límite de cada **Valor** se ha actualizado de 255 caracteres a 5 KB para compatibilidad con el seguimiento de Adobe Analytics.

**Gestión de decisiones**

* **Ubicaciones** - Se han añadido parámetros adicionales en la pantalla de creación de ubicaciones. Permiten controlar si una oferta se puede duplicar en varias ubicaciones y especificar si el contenido y los metadatos de la oferta se deben incluir en la respuesta de API.

* **Personalización de URL** : Al añadir direcciones URL como contenido a las representaciones de las ofertas, ahora puede personalizar estas direcciones URL con el Editor de expresiones.



## Lanzamiento de enero de 2023 {#jan-2023-release}

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
<p>Obtenga información sobre cómo crear, editar y utilizar plantillas de contenido en <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html?lang=es">este vídeo</a>. Para obtener más información, consulte la <a href="../email/content-templates.md">documentación detallada</a>.
</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#jan-2023-improvements}

**Recorridos**

<!--
* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)
-->

* Al añadir **Clasificación del segmento** o **Leer segmento** en un recorrido, el área de nombres ahora se rellena previamente, de forma predeterminada, con la última utilizada. Consulte las secciones [Clasificación del segmento](../building-journeys/segment-qualification-events.md#about-segment-qualification) y [Leer segmento](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

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

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**Personalización**

* Hay disponibles nuevas funciones de ayuda: formatCurrency, charCodeAt, stringToDate, toString, formatNumber y toHexString. Además, la función toDateTimeOnly ahora acepta tipos de campo de cadena, fecha, larga e int. [Más información](../personalization/functions/functions.md)
