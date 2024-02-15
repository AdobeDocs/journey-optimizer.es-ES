---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la primera versión de Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 8d3dac39a0f4ea9982c5a8475d310ae0c3be68b1
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 18%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

Las notas de la primera versión están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md) y en la fecha.

## Notas de la versión anteriores de febrero de 2024 {#e-2024}

**Fecha de lanzamiento**: 20-21 de febrero de 2024

### Nuevas funciones{#e-features}

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
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Reglas empresariales (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear reglas de restricción de frecuencia que se apliquen a los canales de SMS y correo directo. Además, puede establecer reglas de límite de frecuencia por tipo de comunicación.<br/><br/></p>
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>



### Mejoras {#e-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Públicos**

* **Listas semilla** - Ahora se admiten variantes al utilizar **listas semilla**. Al igual que cada perfil de la audiencia de destino, las direcciones semilla reciben una copia de todas las variantes del mismo mensaje (como los diferentes tratamientos de un experimento de contenido).

Anteriormente disponible como Beta, las siguientes mejoras ya están disponibles para todos los usuarios:

* Ahora puede segmentar **audiencias cargadas desde un archivo CSV** en recorridos y campañas. [Más información](../audience/about-audiences.md#segments-in-journey-optimizer)
* Ahora puede segmentar **audiencias creadas mediante composición de audiencia** y aprovechan los atributos de enriquecimiento en Recorrido. [Más información](../building-journeys/read-audience.md)

>[!AVAILABILITY]
>
>El uso de audiencias y atributos de composición de audiencias y carga personalizada (archivo CSV) no está disponible actualmente para su uso con Healthcare Shield o Privacy and Security Shield.

**Recorridos**

* **Filtrar sus recorridos** - Ahora puede utilizar **fechas personalizadas para filtrar los recorridos** inventario, además de los filtros de fecha predefinidos existentes. Esto le permite refinar la lista mostrando recorridos publicados en una fecha específica, dentro de un mes en particular, a lo largo de un año completo o dentro de intervalos de tiempo especificados.
* **Acciones personalizadas** - Ahora puede actualizar el encabezado &quot;tipo de contenido&quot; en **acciones personalizadas**.
* **Configuración** - El atributo identityMap de stepEvents ya está rellenado previamente. La identidad principal se define como &quot;primary = true&quot;.
* **Interfaz de usuario** - La barra superior, en pantallas de recorrido, se ha reorganizado para mejorar la experiencia. Entre las diferentes actualizaciones, observe que el icono de &quot;lápiz&quot; que le permite acceder a las propiedades del recorrido ahora se muestra a la izquierda de la barra superior, junto al nombre del recorrido.

**Canal de SMS**

* **Palabras clave de inclusión/exclusión** : Al configurar el canal SMS, ahora puede personalizar la variable **Palabras clave de inclusión y exclusión** según sus preferencias. Journey Optimizer almacena en déclencheur la respuesta en función de estas palabras clave especificadas.

**Campañas**

* **Campañas activadas por API** - Se ha añadido información en la **Solicitud cURL** sección de **Campañas activadas por API** que se encuentran en **Borrador** para especificar que la solicitud cURL de ejemplo solo sea visible una vez que se ha publicado y ejecutado la campaña.

**Gestión de decisiones**

* **Reglas de límite** - Ahora puede añadir **varias reglas de límite** para una oferta. Esto le permite aumentar el nivel de control sobre la forma en que se envían las ofertas.

**Plantillas de contenido**

* **Miniatura** - A **vista de miniaturas** ya está disponible para plantillas de contenido y fragmentos para mejorar el acceso visual.
* **Plantillas de varios canales** : las plantillas de contenido ya están disponibles para **todos los canales**, excepto Web.