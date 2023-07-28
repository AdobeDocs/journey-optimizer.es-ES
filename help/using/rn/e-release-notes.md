---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la primera versión de Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 97%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

Las notas de la primera versión están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md), en la fecha de la versión.

## Notas de la primera versión de julio de 2023 {#july-rn-2023}

**Fecha de la versión**: 26 -27 de julio

### Nuevas funciones{#july-2023-features}

Esta versión incorpora las nuevas funciones que se enumeran a continuación.

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
<p>Para obtener más información, consulte la <a href="../audience/get-started-audience-orchestration.md">documentación detallada</a>.</p>
<p>La composición de audiencia viene totalmente integrada con el nuevo menú "Audiences" de Adobe Experience Platform, que sirve como portal centralizado para los públicos. Ahora puede utilizar una página de exploración que incluya un nuevo panel con tendencias de segmentos y superposiciones para encontrar nuevos insights y explorar las herramientas organizativas para la carpeta y el etiquetado. Esta experiencia incluye controles de gobernanza para el etiquetado de público estandarizado, así como funciones de administración del ciclo vital de los públicos para administrar los flujos de trabajo de activación. Con esta nueva experiencia de administración, ahora puede administrar públicos de forma fácil y segura desde un solo lugar. Para obtener más información, consulte la <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=es" target="_blank">Documentación de Adobe Experience Platform</a>.</p></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
<img src="assets/do-not-localize/gif-dm.gif"/>
<p>For more information, refer to the <a href="../direct-mail/create-direct-mail.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table-->

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
<img src="../email/assets/html-imported_2.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
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
<!--<p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


### Mejoras {#july-2023-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

<!--
**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.-->
* Se ha introducido un nuevo tipo de alerta del sistema. Ahora puede recibir notificaciones cuando falle una acción personalizada.
—>

**Campañas**

* Los eventos contextuales relacionados con campañas ya están disponibles para su uso en el menú &quot;Atributos contextuales&quot; del editor de personalización.


**Audiences**

Se han realizado mejoras en el selector de públicos en recorridos o campañas, añadiendo nuevas columnas que muestran el origen y la frecuencia de actualización de los públicos.

Con el lanzamiento del portal de composición de audiencia, Adobe Experience Platform y Adobe Journey Optimizer han actualizado el uso de &quot;públicos&quot; y &quot;segmento&quot; dentro del sistema y la documentación.

* Audiencia: conjunto de personas, cuentas, hogares u otras entidades que comparten características y comportamientos comunes.
* Definición del segmento: en Adobe Experience Platform, las reglas utilizadas para describir las características clave o el comportamiento de un público destinatario. Este término se conocía anteriormente como &quot;segmento&quot;.

Como resultado, dentro de Adobe Journey Optimizer y de la IU de Adobe Experience Platform, verá &quot;Segmentos&quot; reemplazado por &quot;Audiencias&quot; para reflejar esta nueva ruta de creación y administración de audiencias.

**API**

Autenticación de API de Adobe Journey Optimizer: el método JWT para generar tokens de acceso ha quedado obsoleto. Todas las nuevas integraciones deben crearse con el método de autenticación de servidor a servidor OAuth. Adobe también recomienda migrar las integraciones existentes al método OAuth. [Más información](https://developer.adobe.com/journey-optimizer-apis/references/authentication/)


**Otros cambios**

La exportación de conjuntos de datos de Journey Optimizer a destinos de almacenamiento en la nube ya está disponible para todos los clientes como una versión beta pública. Ahora, puede establecer una conexión activa con las ubicaciones de almacenamiento en la nube para exportar el contenido de los conjuntos de datos. [Más información](../data/export-datasets.md)




