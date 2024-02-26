---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ee33923ff5bfb73974935864c7e241ea4b0353c5
workflow-type: tm+mt
source-wordcount: '1140'
ht-degree: 54%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras de las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.

## Notas de la versión de febrero de 2024 {#feb-2024}

**Fecha de lanzamiento**: 21-22 de febrero de 2024

### Nuevas funciones{#feb-features}

Esta versión incorpora las nuevas funciones que se enumeran a continuación.


<table>
<thead>
<tr>
<th><strong>Mensajería en la aplicación web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar la nueva capacidad Mensajería en la aplicación web para mostrar contenido personalizado directamente en sitios web, a través de mensajes de superposición modal. Esta función le permite interactuar de forma eficaz con los visitantes web, lo que mejora la interacción del usuario, la retención y las tasas de conversión.<br/><br/></p>
<p>Para obtener más información, consulte la <a href="../in-app/create-in-app-web.md">documentación detallada</a>.<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Plantillas de contenido multicanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Además del correo electrónico, las plantillas de contenido ya están disponibles para los siguientes canales: push, en la aplicación, SMS y correo directo, y cada canal tiene tipos de plantilla dedicados. Para Correo electrónico, ahora puede seleccionar el Tipo de contenido, que le permite guardar la línea de asunto como parte de la plantilla de correo electrónico. <br/><br/></p>
<p>Para obtener más información, consulte la <a href="../content-management/content-templates.md">documentación detallada</a>.<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif">
</tr>
</tbody>
</table>


### Mejoras {#feb-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Públicos**

* **Listas semilla** - Ahora se admiten variantes al utilizar **listas semilla**. Las direcciones semilla reciben una copia de todas las variantes del mismo mensaje (como los diferentes tratamientos de un experimento de contenido). [Más información](../configuration/seed-lists.md)

Anteriormente disponible como Beta, las siguientes mejoras ya están disponibles para todos los usuarios:

* Ahora puede segmentar **audiencias creadas mediante composición de audiencia** y aprovechan los atributos de enriquecimiento en Recorrido. [Más información](../building-journeys/read-audience.md)

* Ahora puede segmentar **audiencias cargadas desde un archivo CSV** en recorridos y campañas. [Más información](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* El uso de audiencias y atributos de composición de audiencias y carga personalizada (archivo CSV) no está disponible actualmente para su uso con Healthcare Shield o Privacy and Security Shield.
  >* El **carga de audiencias desde un archivo CSV** la mejora se está implementando gradualmente en el transcurso de varios días después de la publicación inicial. Aunque algunos usuarios tienen acceso inmediato, otros pueden experimentar un retraso antes de que esté disponible en su entorno.

**Recorridos**

* **Filtrar sus recorridos** - Ahora puede utilizar **fechas personalizadas para filtrar los recorridos** inventario, además de los filtros de fecha predefinidos existentes. Esto le permite refinar la lista mostrando los recorridos creados o publicados en una fecha específica, dentro de un mes en particular, a lo largo de un año completo o dentro de intervalos de tiempo especificados. [Más información](../building-journeys/journey-gs.md#filter)
* **Acciones personalizadas** - Ahora puede actualizar el **content-type** encabezado. Esta nueva **content-type** debe hacer referencia al contenido JSON. [Más información](../action/about-custom-action-configuration.md#url-configuration)
* **Configuración** - El atributo identityMap de stepEvents ya está rellenado previamente. La identidad principal se define como &quot;primary = true&quot;. [Más información](../reports/sharing-field-list.md)
* **Interfaz de usuario** - La barra superior, en pantallas de recorrido, se ha reorganizado para mejorar la experiencia. Entre las diferentes actualizaciones, observe que el icono de &quot;lápiz&quot; que le permite acceder a las propiedades del recorrido ahora se muestra a la izquierda de la barra superior, junto al nombre del recorrido. [Más información](../building-journeys/journey-gs.md#change-properties)

**Canal de SMS**

* **Palabras clave de inclusión/exclusión** : Al configurar el canal SMS, ahora puede personalizar la variable **Palabras clave de inclusión y exclusión** según sus preferencias. Journey Optimizer almacena en déclencheur la respuesta en función de estas palabras clave especificadas. [Más información](../sms/sms-configuration.md#create-api)

**Campañas**

* **Campañas activadas por API** : Se ha mejorado el código cURL generado después de activar una campaña activada por una API. Ahora incluye todas las variables de personalización (perfil y contexto) utilizadas en el mensaje. [Más información](../campaigns/api-triggered-campaigns.md#execute)

**Reglas de frecuencia**

* Además de Correo electrónico y push, ahora puede crear reglas de frecuencia para canales de SMS y de correo directo. Las reglas de frecuencia excluyen automáticamente los perfiles saturados de los mensajes y las acciones cuando se alcanza el límite de frecuencia. [Más información](../configuration/frequency-rules.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->

<!--
**Content templates**

* **Thumbnails** - A **Grid view** is now available for content templates for improved visual access.

   >[!AVAILABILITY]
   >
   >This capability is released in Limited Availability (LA) for a small set of customers.
-->


## Notas de la versión de enero de 2024 {#jan-2024}

**Fecha de la versión**: 30-31 de 2024

### Nuevas funciones{#jan24-features}

Esta versión incorpora las nuevas funciones que se enumeran a continuación.

<table>
<thead>
<tr>
<th><strong>Actualizaciones sobre la entregabilidad</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ahora admite la tecnología de autenticación DMARC.</p>
<p>A partir del 1 de febrero de 2024, Google y Yahoo! requiere que tenga un registro DMARC para cualquier dominio que utilice para enviarles correo electrónico. Asegúrese de tener configurado el registro DMARC para todos los subdominios que haya delegado a Adobe en Journey Optimizer.</p>
<p>Para obtener más información, consulte la <a href="../configuration/dmarc-record-update.md">documentación detallada</a>.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Manuales de tácticas de casos de uso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aproveche un catálogo de libros de casos de uso específicos del sector en Real-Time CDP y Journey Optimizer para abordar casos de uso comunes que puede realizar con Adobe Experience Platform y Adobe Journey Optimizer.</p><p>Una vez que haya elegido el manual de tácticas que mejor se adapte a sus necesidades, puede habilitarlo para generar los recursos necesarios compatibles con su caso de uso, como recorridos, mensajes, esquemas o segmentos, y personalizarlos según su esquema para acelerar la obtención de valor.</p>
<p>Para obtener más información, consulte la <a href="../start/playbooks.md">documentación detallada</a>.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Mejoras {#jan24-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Creación de informes**

* **Nuevos widgets de desglose basados en dominios**: se han añadido nuevos widgets para mejorar los informes de Campaign y Journey. Los widgets **Motivos del rechazo por dominio**, **Enviados y entregados por dominios**, **Aperturas y clics por dominio** y **Rechazos y errores por dominio** proporcionan un desglose detallado a nivel de dominio para las métricas clave de envío y seguimiento de correo electrónico. [Más información](../reports/channel-report.md)

**Canal de SMS**

* **Inclusión doble**: el flujo de trabajo de inclusión doble para SMS garantiza que los usuarios acepten explícitamente recibir mensajes cuando la solicitud se inicia desde su dispositivo. Los usuarios inician el proceso de consentimiento enviando un mensaje SMS entrante. Al confirmar su consentimiento, se envía un mensaje de seguimiento en el que se solicita la verificación final. Si no existe ningún perfil de usuario, se crea tras una confirmación correcta. [Más información](../sms/sms-configuration.md#create-api)

  Tenga en cuenta que esta capacidad está disponible con proveedores de SMS de Sinch e Infobip.

**Recorridos**

* **Duración de los eventos de reacción**: la duración máxima que se puede definir en los **Eventos de reacción** ahora es de 29 días en lugar de 30. [Más información](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Leer público**: la actividad **Leer público** ahora depende del conjunto de datos de instantánea de perfil para segmentos por lotes, que solo se genera una vez al día después de ejecutar el trabajo por lotes diario programado, por lo que los datos se actualizarán hasta ese último trabajo por lotes diario. [Más información](../building-journeys/read-audience.md)

* **Grupos de campos**: esta versión soluciona un problema que impedía que los grupos de campo se guardaran en determinados casos.

* Se ha modificado la compatibilidad con `<listObject>` en varias funciones.

**Reglas de frecuencia**

* **Límite de frecuencia semanal y diaria**: ahora puede especificar el número máximo de mensajes enviados a un perfil de cliente en una semana o un día, además del mes. El límite de frecuencia se basa en el período de calendario seleccionado y se restablece al principio del lapso de tiempo correspondiente. [Más información](../configuration/frequency-rules.md#create-new-rule)


**Gestión de decisiones**

* **Restricción de frecuencia en Edge**: el contador de restricción de frecuencia ahora se ha actualizado y está disponible en una decisión de API de Edge Decisioning en menos de 3 segundos. [Más información](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
