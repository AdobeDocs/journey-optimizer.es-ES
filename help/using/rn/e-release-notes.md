---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la primera versión de Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: a0a4d39519f7f02265c52934db401e036ea12df6
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 16%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

Las notas de la primera versión están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md) y en la fecha.

## Notas de la versión anteriores de febrero de 2024 {#e-2024}

**Fecha de lanzamiento**: 21-22 de febrero de 2024

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
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Reglas de frecuencia para SMS y correo directo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear reglas de frecuencia para canales de SMS y de correo directo. Las reglas de frecuencia excluyen automáticamente los perfiles saturados de los mensajes y las acciones cuando se alcanza el límite de frecuencia. <br/><br/></p>
<img src="assets/do-not-localize/sms-dm-rules.gif">
</tr>
</tbody>
</table>

### Mejoras {#e-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Públicos**

* **Listas semilla** - Ahora se admiten variantes al utilizar **listas semilla**. Al igual que cada perfil de la audiencia de destino, las direcciones semilla reciben una copia de todas las variantes del mismo mensaje (como los diferentes tratamientos de un experimento de contenido).

Anteriormente disponible como Beta, las siguientes mejoras ya están disponibles para todos los usuarios:

* Ahora puede segmentar **audiencias creadas mediante composición de audiencia** y aprovechan los atributos de enriquecimiento en Recorrido. [Más información](../building-journeys/read-audience.md)

* Ahora puede segmentar **audiencias cargadas desde un archivo CSV** en recorridos y campañas. [Más información](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* El uso de audiencias y atributos de composición de audiencias y carga personalizada (archivo CSV) no está disponible actualmente para su uso con Healthcare Shield o Privacy and Security Shield.
  >* Tenga en cuenta que la carga de audiencias desde un archivo CSV se implementará gradualmente durante varios días después de la publicación inicial. Aunque algunos usuarios tendrán acceso inmediato, otros pueden experimentar un retraso antes de que esté disponible en sus cuentas.

**Recorridos**

* **Filtrar sus recorridos** - Ahora puede utilizar **fechas personalizadas para filtrar los recorridos** inventario, además de los filtros de fecha predefinidos existentes. Esto le permite refinar la lista mostrando los recorridos creados o publicados en una fecha específica, dentro de un mes en particular, a lo largo de un año completo o dentro de intervalos de tiempo especificados.
* **Acciones personalizadas** - Ahora puede actualizar el **content-type** encabezado. Esta nueva **content-type** debe hacer referencia al contenido JSON.
* **Configuración** - El atributo identityMap de stepEvents ya está rellenado previamente. La identidad principal se define como &quot;primary = true&quot;.
* **Interfaz de usuario** - La barra superior, en pantallas de recorrido, se ha reorganizado para mejorar la experiencia. Entre las diferentes actualizaciones, observe que el icono de &quot;lápiz&quot; que le permite acceder a las propiedades del recorrido ahora se muestra a la izquierda de la barra superior, junto al nombre del recorrido.

**Canal de SMS**

* **Palabras clave de inclusión/exclusión** : Al configurar el canal SMS, ahora puede personalizar la variable **Palabras clave de inclusión y exclusión** según sus preferencias. Journey Optimizer almacena en déclencheur la respuesta en función de estas palabras clave especificadas.

**Campañas**

* **Campañas activadas por API** : Se ha mejorado el código cURL generado después de activar una campaña activada por una API. Ahora incluye todas las variables de personalización (perfil y contexto) utilizadas en el mensaje.

**Gestión de decisiones**

* **Reglas de límite** - Ahora puede añadir **varias reglas de límite** para una oferta. Esto le permite aumentar el nivel de control sobre la forma en que se envían las ofertas.

**Plantillas de contenido**

* **Miniatura** - A **vista de miniaturas** ya está disponible para plantillas de contenido y fragmentos para mejorar el acceso visual.

  >[!AVAILABILITY]
  >
  >Esta capacidad se lanza con disponibilidad limitada (LA) para un pequeño conjunto de clientes.

* **Plantillas de varios canales** : las plantillas de contenido ya están disponibles para **todos los canales**, excepto Web. Para Correo electrónico, ahora puede seleccionar el tipo (HTML o Contenido).
