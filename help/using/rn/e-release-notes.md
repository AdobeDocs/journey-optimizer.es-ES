---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versión preliminar de Journey Optimizer
description: Notas de versión preliminar de Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: ht
source-wordcount: '591'
ht-degree: 100%

---

# Notas de versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

**Las notas de versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md) y en la fecha.


## Notas de versión preliminar de agosto de 2025 {#25-7-rn}

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad de la versión**. Los vínculos, las pantallas y la documentación actualizada se publican en la fecha de la versión.

Véase también [Notas de la versión preliminar de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Fecha de lanzamiento**: miércoles, 19 de agosto de 2025


### Nuevas funciones {#Aug-25-8-features}

A continuación, se describen las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Pausar y reanudar recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede poner en pausa y reanudar los recorridos. Esta funcionalidad proporciona a los profesionales del recorrido un mayor control y flexibilidad al permitir que los recorridos en directo se suspendan temporalmente sin interrumpir la experiencia del cliente. Cuando están en pausa, no se envían comunicaciones y los perfiles permanecen en estado suspendido hasta que se reanuda el recorrido.</p>
<p>Puede poner en pausa y reanudar solo un recorrido, o realizar pausas masivas y reanudar operaciones en un grupo de recorridos.</p>
<p>Además, puede aplicar filtros globales a los recorridos en pausa para excluir perfiles en función de sus atributos.</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>Esta capacidad, que antes estaba disponible para un conjunto limitado de clientes (disponibilidad limitada), ahora está disponible en todos los entornos (disponibilidad general).</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-pause.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Vista de calendario</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora hay disponible una vista de calendario en las listas de recorridos y campañas. Permite visualizar todas las activaciones de recorridos y campañas en las listas respectivas.</p>
<p>Esta capacidad, que se lanzó anteriormente con disponibilidad limitada, ya está disponible en todos los entornos. Con esta versión de disponibilidad general, la función incluye:</p>
<ul>
<li>Mejoras de diseño para la navegación en fechas</li>
<li>La capacidad de ver borradores de campañas si ha establecido una fecha de inicio y de finalización</li>
<li>Una nueva configuración para ocultar y mostrar los elementos de calendario que se ejecutan durante mucho tiempo</li>
</ul>
<img src="assets/do-not-localize/calendar.gif">
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-ui.md#journeys-calendar">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modo oscuro en el Diseñador de correo electrónico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El Diseñador de correo electrónico de Journey Optimizer ahora permite cambiar a la vista en modo oscuro, donde además puede definir configuraciones personalizadas específicas que se mostrarán solo para los destinatarios que lean sus correos electrónicos en modo oscuro.</p>
<p>Tenga en cuenta lo siguiente:</p>
<ul>
<li>El renderizado final del modo oscuro puede variar y depende del cliente de correo electrónico del destinatario.</li>
<li>No todos los clientes de correo electrónico admiten el modo oscuro personalizado. Además, algunos clientes de correo electrónico solo aplican su propio modo oscuro predeterminado a todos los correos electrónicos recibidos. En ambos casos, no se puede procesar la configuración personalizada que definió en el Diseñador de correo electrónico.</li>
</ul>
<P>Actualmente, esta función está en versión Beta y solo se encuentra disponible para los clientes de dicha versión. Para unirse al programa beta, póngase en contacto con su representante de Adobe.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>Para obtener más información, consulte la <a href="../email/dark-mode.md">documentación detallada</a>. </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Optimización en campañas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora, Journey Optimizer le ofrece las herramientas necesarias para ofrecer contenido personalizado y optimizado al público de sus campañas, lo que le permite ejecutar experimentos de contenido, crear segmentación basada en reglas y utilizar combinaciones avanzadas de ambos para maximizar la eficacia de sus campañas.</p>
<p>Con Optimization, puede:</p>
<ul>
<li>Probar múltiples variaciones de contenido para identificar la mensajería más eficaz.</li>
<li>Ofrecer contenido personalizado basado en atributos de usuario y datos contextuales.</li>
<li>Combinar segmentación y experimentación para estrategias de campaña avanzadas.</li>
<li>Filtrar los usuarios que no coincidan con los criterios de variante.</li>
<li>Garantizar mecanismos de reserva para mantener la participación del usuario.</li>
</ul>
<P>Una vez que la campaña está activa, los perfiles se evalúan según los criterios definidos y, en función de los criterios coincidentes, se envían con la experiencia o el contenido adecuados de la campaña.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<!--p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p-->
</td>
</tr>
</tbody>
</table>

### Mejoras {#Aug-25-8-improv}

A continuación, se describen las mejoras incluidas en esta versión.