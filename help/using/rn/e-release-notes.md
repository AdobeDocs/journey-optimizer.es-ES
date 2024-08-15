---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
description: Notas de la primera versión de Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 128a56b543f470bf967fd195fde73ff7b32b2a17
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 34%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

**Las notas de la versión preliminar están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento**. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md) y en la fecha.

## Notas de la primera versión de agosto de 2024 {#e-2024}

**Fecha de lanzamiento**: 20-21 de agosto de 2024

### Nuevas funciones {#e-features}

Esta versión incorpora las nuevas funciones que se indican a continuación.


<table>
<thead>
<tr>
<th><strong>Configuración de canal guiado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La configuración guiada de canales le permite automatizar los pasos de la configuración del canal móvil de forma unificada para empezar a utilizar Journey Optimizer con mayor rapidez. Esta configuración facilita la configuración rápida de los canales de marketing, lo que garantiza que todos los recursos necesarios estén fácilmente disponibles en Experience Platform, Journey Optimizer y la recopilación de datos. Esto permite a su equipo de marketing iniciar inmediatamente la creación de campañas y recorridos.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Tarjetas de contenido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La tarjeta de contenido es una nueva función de mensajería digital de Adobe Journey Optimizer que ofrece contenido personalizado y atractivo directamente en aplicaciones móviles y sitios web. A diferencia de las notificaciones push tradicionales, las tarjetas de contenido se integran perfectamente en la interfaz de usuario, ofreciendo actualizaciones persistentes y no intrusivas que mejoran la interacción y experiencia del usuario.</p>
<p>Esta función permite a los especialistas en marketing presentar contenido multimedia relevante y enriquecido a los usuarios, lo que aumenta la participación y garantiza que se vean mensajes importantes sin interrumpir el recorrido del usuario.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Configuraciones de canal mejoradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las funciones actuales de superficie de canal se han mejorado para lograr un enfoque coherente en todos los canales. Ahora puede definir, administrar y reutilizar estas configuraciones para cualquiera de sus canales.</p>
<p><ul>
<li>Ahora se cambió el nombre de las superficies de canal a <strong>Configuraciones de canal</strong></li>
<li>Desde el inventario de configuraciones de canal, ahora puede crear configuraciones de canal reutilizables para todos los canales, incluso ahora mensajería web, en la aplicación o experiencia basada en código</li>
<li>El control de acceso a nivel de objeto (OLAC) ya está disponible para cada configuración de canal, lo que le permite decidir cuál de sus usuarios puede crear o utilizar configuraciones específicas</li>
<li>Para algunos canales, puede crear configuraciones de canal dirigidas a varias plataformas. Un ejemplo sería una configuración de canal de mensajería en la aplicación que puede dirigirse a una página web, una aplicación de iOS y una aplicación de Android.</li>
</ul></p>
<p>Para obtener más información, consulte la <a href="../configuration/ip-warmup-gs.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Acción personalizada de Marketo Engage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede integrar Adobe Journey Optimizer con Adobe Marketo Engage para crear sus casos de uso B2B. Desde un recorrido, una nueva acción personalizada le permite introducir datos en Marketo.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Variables en fragmentos de contenido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Los fragmentos ahora pueden consumir variables de entrada, tanto en <a href="../personalization/use-expression-fragments.md">fragmentos de expresión</a> como en <a href="../email/use-visual-fragments.md">fragmentos visuales</a>. Puede utilizar esas variables para personalizar el contenido y los parámetros de los mensajes, en sus campañas y recorridos.</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Flujo de trabajo de calentamiento de IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Fecha de disponibilidad: 13 de agosto</p>
<p>Si envía un correo electrónico a una dirección de IP completamente nueva, ahora puede ejecutar fácilmente los flujos de trabajo de calentamiento de IP directamente desde la interfaz de usuario. Adobe Journey Optimizer ofrece una forma estandarizada y eficaz de añadir las direcciones IP que siguen las prácticas recomendadas para lograr una entrega óptima.</p>
<p>Para obtener más información, consulte la <a href="../configuration/ip-warmup-gs.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Mejoras {#e-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Recorridos**

* En la actividad **Condition**, de forma predeterminada, la condición Time ahora se establece por hora, de 00:00 a 12:00. [Más información](../building-journeys/condition-activity.md#time_condition)
* Al crear las alertas, estas ahora se muestran en una lista desplegable para alinearse con las recorridos de la campaña y ofrecer una experiencia de usuario coherente. [Más información](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* Se han mejorado las opciones de zoom en la barra de herramientas de recorrido: el porcentaje de zoom ahora está visible y ahora puede restablecer fácilmente el valor de zoom al 100 %.

**Públicos**

* El uso de públicos de carga personalizada (archivo CSV) ya está disponible para su uso con Privacy and Security Shield.
* Al segmentar una audiencia de carga personalizada (archivo CSV), ahora puede utilizar atributos del archivo en sus campañas y recorridos. Estos atributos están disponibles en el editor de personalización para personalizar los mensajes y en el editor de expresiones avanzadas de recorrido.

<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
