---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión preliminar
description: Notas de la primera versión de Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: eff3f2fb4d1c369e77a22013ae1576b57449a8b7
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 35%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento**. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md) y en la fecha.


## Notas de la versión anteriores de junio de 2025 {#25-6-rn}


**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento**. Los vínculos, las pantallas y la documentación actualizada se publican en la fecha de la versión.

**Fecha de lanzamiento**: jueves, 18 de junio de 2025


### Nuevas funciones {#25-06-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.




<table>
<thead>
<tr>
<th><strong>Mensajería RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La mensajería RCS (servicios de comunicación enriquecidos) ahora es compatible con Journey Optimizer, lo que permite las siguientes funciones de mensajería mejoradas sujetas a la compatibilidad del proveedor y el operador:</p>
<ul>
<li>Compatibilidad con remitentes de marca y verificados: envía mensajes utilizando perfiles comerciales verificados con elementos de marca (logotipo, nombre del remitente, etc.).</li>
<li>Perspectivas de entrega de mensajes: reciba informes de entrega detallados que incluyan actualizaciones del estado del mensaje (por ejemplo, enviado, entregado, leído).</li>
<li>Seguimiento de vínculos: incruste y rastree direcciones URL en mensajes RCS para el análisis de participación.</li>
<li>Volver a SMS: volver automáticamente a SMS cuando el dispositivo del perfil no admite RCS o no se puede acceder a él temporalmente mediante RCS.</li>
<li>Composición básica de mensajes: envía mensajes RCS basados en texto con medios opcionales y elementos enriquecidos, según la compatibilidad del proveedor.</li>
</ul>
<!--p>For more information, refer to the <a href="../sms/sms-configuration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>True Multi-Tenant Unitary Delivery</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Campos de formulario en contenido de experiencia basado en código</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir campos editables específicos en plantillas de contenido JSON o HTML que permitan a los usuarios no técnicos editar fácilmente el contenido en experiencias basadas en código sin necesidad de manipular el código.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Método de delegación personalizado para subdominios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Además de la delegación completa y el método CNAME, ahora está disponible un nuevo método de configuración de subdominios: el método de delegación personalizado, que le permite ser el propietario total del control y el mantenimiento de todos los aspectos de DNS necesarios para enviar, procesar y rastrear mensajes.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos (disponibilidad general).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Actividad de Content Decisioning en recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede incluir ofertas personalizadas en los recorridos a través de una actividad de Content Decisioning específica en el lienzo de recorrido y utilizarlas en actividades de recorrido, incluidas condiciones y acciones personalizadas.</p>
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una versión futura.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Experience Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->



<table>
<thead>
<tr>
<th><strong>Recorrido Dry run</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Recorrido Dry run es un modo especial de publicación de recorrido en Adobe Journey Optimizer que permite a los profesionales del recorrido probar un recorrido utilizando datos de producción reales sin ponerse en contacto con clientes reales ni actualizar información de perfil. Esta función ayuda a los profesionales del recorrido a confiar en el diseño del recorrido y la segmentación de audiencia antes de publicarla en directo.</p>
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una versión futura.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Pausar y reanudar recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede pausar y reanudar las recorridos. Esta capacidad proporciona a los profesionales del recorrido un mayor control y flexibilidad al permitir que los recorridos en directo se suspendan temporalmente sin interrumpir la experiencia del cliente. Cuando está en pausa, no se envían comunicaciones y los perfiles permanecen en estado suspendido hasta que se reanuda la recorrido.</p>
<p>Puede pausar y reanudar solo un recorrido, o realizar pausas masivas y reanudar operaciones en un grupo de recorridos.</p>
<p>Además, puede aplicar filtros globales a recorridos en pausa para excluir perfiles en función de sus atributos.</p>
<p>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una versión futura.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Escalar el ganador de la experimentación</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Escalar el ganador de un experimento permite desplegar automática o manualmente la variación ganadora de un experimento en toda la audiencia. Esta función garantiza que, una vez que se identifique al que tenga el mayor rendimiento, pueda maximizar su alcance y eficacia sin una supervisión manual constante.</p>
<p>Para obtener más información, consulte la <a href="../content-management/content-experiment.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 2 de junio de 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflicto y priorización</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En Journey Optimizer, administrar el volumen y la cronología de las campañas y los recorridos es esencial para evitar abrumar a los clientes con demasiadas interacciones. Journey Optimizer ahora ofrece varias herramientas para la administración de conflictos y la priorización - antes disponibles solo para organizaciones de acceso limitado (LA) que ahora están disponibles de forma general (GA).</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de disponibilidad general, se han introducido las siguientes mejoras:</p>
<ul>
<li>Compatibilidad ampliada: las herramientas de administración de conflictos ahora admiten tanto los recorridos unitarios como los recorridos de calificación de público, además de los recorridos de público de lectura.</li>
<li>Solución de problemas mejorada: ahora hay dos nuevos campos de evento de paso disponibles en el servicio de consultas, lo que le permite analizar por qué se rechazó un perfil de un recorrido o una campaña.</li>
<li>Informes mejorados: ahora los informes indican qué regla específica excluyó un perfil de un recorrido o campaña, lo que proporciona una mayor transparencia e información útil.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Para obtener más información, consulte la <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 3 de junio de 2025</p>
</td>
</tr>
</tbody>
</table>


### Mejoras {#25-06-improv}

A continuación, se describen las mejoras incluidas en esta versión.

* **Conjuntos de reglas de canal**

   * **Ventana de duración personalizada** para límite: ahora hay disponible un nuevo campo **Recuento de repeticiones** en la pantalla de configuración de conjuntos de reglas de canal, que le permite aplicar reglas de límite de frecuencia durante varios días, semanas o meses, según la duración especificada.

   * **Duración por hora**: ahora puede aplicar un límite por hora a los conjuntos de reglas de canal.

* **Experiencias basadas en código**

  Las políticas de decisión ya están disponibles en las plantillas de contenido de experiencia basadas en código y en el carril derecho del editor de código.

* **Diseñador de correos electrónicos**

   * **Compatibilidad con CSS personalizado**: Journey Optimizer ahora le permite agregar CSS personalizado al contenido del correo electrónico directamente dentro del Diseñador de correo electrónico.
   * **Compatibilidad con modo oscuro**: El diseñador de correo electrónico de Journey Optimizer ahora ofrece la capacidad de cambiar al modo oscuro, en el que puede definir configuraciones específicas.


* **Decisión** - Fecha de disponibilidad: 3 de junio de 2025

  Ahora, los objetos de decisiones se pueden copiar entre zonas protegidas, lo que optimiza los flujos de trabajo de prueba e implementación. [Más información](../configuration/copy-objects-to-sandbox.md#decisioning)

* **Compatibilidad con atributos de elementos de decisión para reglas de toma de decisiones**. Fecha de disponibilidad: 4 de junio de 2025

  Ahora puede aprovechar los atributos de elementos de decisión para crear reglas de toma de decisiones. [Más información](../experience-decisioning/rules.md#create)

* **Actualización interactiva de la API de ejecución de mensajes** - Fecha de disponibilidad: 6 de junio de 2025

  La API de ejecución de mensajes interactiva ahora le permite eliminar la programación de la próxima ejecución de campañas. [Más información](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}