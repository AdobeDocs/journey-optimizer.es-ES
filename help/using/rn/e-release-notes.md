---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la primera versión de Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 0ed72b947c176b54220b5e00cdae6ccf91aac9a8
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 100%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

Las notas de la primera versión están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md), en la fecha de la versión.

## Notas de la primera versión de agosto de 2023 {#aug-rn-2023}

**Fecha de lanzamiento**: 23-24 de agosto de 2023

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
<img src="assets/in_app_journey_1.png"/>
<p>Para obtener más información, consulte la <a href="../in-app/get-started-in-app.md">documentación detallada</a>.</p>
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
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
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

**API**

Ya está disponible una nueva API para crear y administrar fragmentos de contenido. [Más información](https://developer.adobe.com/journey-optimizer-apis/references/content-templates/#tag/Content-fragment-API){target="_blank"}.

**Canal de correo electrónico**

Hay una nueva opción disponible en la configuración de la superficie de correo electrónico para incluir las direcciones de correo electrónico suprimidas debido a las quejas de spam del público de mensajes transaccionales. Incluso si han marcado los mensajes de marketing como spam, estos perfiles pueden recibir mensajes transaccionales, como de restablecimiento de la contraseña o extractos de la cuenta. Esta opción está desactivada de forma predeterminada.

**Recorridos**

* Ahora puede utilizar las respuestas de llamadas de API en acciones personalizadas y organizar su recorrido en función de estas respuestas. Actualmente, esta función está disponible como una versión beta privada.
<!--* A new type of system alert has been introduced. You can now get notified when a custom action fails.
* When duplicating a journey, you can now define the name of the journey copy.-->


**Correo directo**

* Azure ahora se puede seleccionar como tipo de servidor en la configuración de enrutamiento de archivos.
* El ampersand está ahora disponible como campo separador de columnas en la configuración de superficie de correo postal.