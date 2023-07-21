---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la versión anteriores de Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: c75664f9b4d58fff1b073c385bcb839e9c11c8ec
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 20%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en la [notas de la versión](release-notes.md).

Las notas de la versión anticipadas que se indican a continuación están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento. Los vínculos, las pantallas y la documentación actualizada se publican en la [notas de la versión](release-notes.md), en la fecha de lanzamiento.


## Notas de la versión anteriores de julio de 2023 {#july-rn-2023}

**Fecha de lanzamiento**: Del 26 al 27 de julio

### Nuevas funciones{#july-2023-features}

Esta versión incorpora las nuevas funciones que se enumeran a continuación.

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


<table>
<thead>
<tr>
<th><strong>Composición de audiencia</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear flujos de trabajo de composición para combinar audiencias de Adobe Experience Platform existentes en un lienzo visual y aprovechar varias actividades (dividir, enriquecer...) para crear nuevas audiencias. Las audiencias recién creadas se vuelven a guardar en Adobe Experience Platform junto con las audiencias existentes y se pueden aprovechar en campañas de Journey Optimizer para clientes de destino.</p>
<img src="../audience/assets/audiences-publish.png"/>
<p>Para obtener más información, consulte la <a href="../audience/get-started-audience-orchestration.md">documentación detallada</a>.</p>
<p>La composición de audiencias viene totalmente integrada con el nuevo menú "Audiencias" de Adobe Experience Platform, que sirve como portal centralizado para las audiencias. Ahora puede utilizar una página de exploración que incluya un nuevo panel con tendencias de segmentos y superposiciones para encontrar nuevas perspectivas y explorar las herramientas organizativas para la carpeta y el etiquetado. Esta experiencia incluye controles de gobernanza para el etiquetado de audiencias estandarizado, así como funciones de administración del ciclo vital de las audiencias para administrar los flujos de trabajo de activación. Con esta nueva experiencia de administración, ahora puede administrar audiencias de forma fácil y segura desde un solo lugar. Para obtener más información, consulte <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html" target="_blank">Documentación de Adobe Experience Platform</a>.</p></p>
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
<p>Ahora puede agregar mensajes de correo postal en sus campañas. El correo postal es un canal sin conexión que le permite personalizar y generar los archivos necesarios para que los proveedores de correo postal envíen correo a sus clientes.</p>
<p>Al preparar una entrega de correo postal, Journey Optimizer genera un archivo que incluye todos los perfiles de destino y la información de contacto elegida (por ejemplo, una dirección postal). Después, puede enviar este archivo al proveedor de correo postal que se encarga de la entrega real.</p>
<img src="../direct-mail/assets/direct-mail-properties.png">
<p>Para obtener más información, consulte la <a href="../direct-mail/create-direct-mail.md">documentación detallada</a>.</p>
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
<p>Además de las campañas y los recorridos, ahora puede asignar Adobe Experience Platform Unified Tags a sus páginas de aterrizaje, plantillas de contenido, fragmentos y listas de suscripción. Esto le permite clasificarlas fácilmente y mejorar la búsqueda y la navegación en todas las listas. </p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Para obtener más información, consulte la <a href="../start/search-filter-categorize.md#tags">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


### Mejoras {#july-2023-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Recorridos**

<!--* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.-->
* Se ha introducido un nuevo tipo de alerta del sistema. Ahora puede recibir notificaciones cuando falle una acción personalizada.


**Campañas**

* Los eventos contextuales relacionados con campañas ya están disponibles para su uso en el menú &quot;Atributos contextuales&quot; del editor de personalización.


**Audiencias**

Se han realizado mejoras en el selector de audiencias en recorridos o campañas, con la adición de nuevas columnas que muestran el origen y la frecuencia de actualización de las audiencias.

Con el lanzamiento del portal de composición de audiencias, Adobe Experience Platform y Adobe Journey Optimizer han actualizado el uso de &quot;audiencias&quot; y &quot;segmentos&quot; dentro del sistema y la documentación.

* Audiencia: conjunto de personas, cuentas, hogares u otras entidades que comparten características y comportamientos comunes.
* Definición del segmento: en Adobe Experience Platform, las reglas utilizadas para describir las características clave o el comportamiento de un público destinatario. Este término se conocía anteriormente como &quot;segmento&quot;.

Como resultado, dentro de Adobe Journey Optimizer y de la IU de Adobe Experience Platform, verá &quot;Segmentos&quot; reemplazado por &quot;Audiencias&quot; para reflejar esta nueva ruta de creación y administración de audiencias.

**API**

Autenticación de API de Adobe Journey Optimizer: el método JWT para generar tokens de acceso ha quedado obsoleto. Todas las nuevas integraciones deben crearse con el método de autenticación de servidor a servidor OAuth. Adobe también recomienda migrar las integraciones existentes al método OAuth. [Más información](https://developer.adobe.com/journey-optimizer-apis/references/authentication/)


**Otros cambios**

La exportación de conjuntos de datos de Journey Optimizer a destinos de almacenamiento en la nube ya está disponible para todos los clientes. Esta función le permite establecer una conexión activa con ubicaciones de almacenamiento en la nube para exportar el contenido de sus conjuntos de datos. [Más información](../data/export-datasets.md)

>[!AVAILABILITY]
>
>Esta función se encuentra actualmente en versión beta y sujeta a cambios.</p>
