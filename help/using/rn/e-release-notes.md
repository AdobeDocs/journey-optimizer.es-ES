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
source-git-commit: 004eb41b084f32993ec437f589e4e3d2cf7500d3
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 100%

---

# Notas de la versión preliminar {#e-release-notes}

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en las [notas de la versión](release-notes.md).

Las notas de la primera versión están sujetas a cambios sin previo aviso hasta la fecha de disponibilidad del lanzamiento. Los vínculos, las pantallas y la documentación actualizada se publican en las [notas de la versión](release-notes.md), en la fecha de la versión.

## Notas de la versión preliminar de octubre de 2023 {#oct-rn-2023}

**Fecha de la versión**: 25-26 de octubre de 2023

### Nuevas funciones{#oct-2023-features}

Esta versión incorpora las nuevas funciones que se enumeran a continuación.

<table>
<thead>
<tr>
<th><strong>Herramientas de zona protegida</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las herramientas de zona protegida permiten copiar objetos en varias zonas protegidas aprovechando la exportación e importación de paquetes. Un paquete puede constar de un único objeto o de varios objetos. Los objetos incluidos en un paquete deben pertenecer a la misma zona protegida.</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>Servicio de mensajes multimedia (MMS) en SMS (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con el canal SMS, ahora puede mejorar su comunicación enviando mensajes del servicio de mensajes multimedia (MMS), lo que le permite compartir imágenes, GIF o vídeos con sus clientes. Tenga en cuenta que esta función solo está disponible actualmente en versión beta con Sinch.</p>
<!--img src="assets/channel-reports.png"/-->
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

### Mejoras {#oct-2023-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Públicos**

* Ahora puede segmentar públicos destinatarios cargados desde un archivo CSV en recorridos y campañas.
* Ahora puede dirigirse a públicos destinatarios creados mediante la composición de públicos y aprovechar los atributos de enriquecimiento de los recorridos.

>[!AVAILABILITY]
>
>Estas funcionalidades están disponibles actualmente como una versión Private Beta.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**Campañas**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* Cuando se produce un error en una de las campañas, ahora aparece un icono de advertencia en la lista de campañas junto con el estado de la campaña.

**Recorridos**

* La duración máxima que puede definir en cualquier tiempo de espera ahora es de 29 días, en lugar de 30. Esto se aplica a:

   * el campo **Cantidad de tiempo** en la [actividad de espera](../building-journeys/wait-activity.md)
   * el **Período de espera de reentrada** en [propiedades del recorrido](../building-journeys/journey-gs.md#entrance)
   * el campo **Esperar a** en la definición de tiempo de espera de los eventos [general](../building-journeys/general-events.md#events-specific-time) y [reacción](../building-journeys/reaction-events.md).

**Consentimiento en la configuración del canal**

* Ahora puede seleccionar una acción de marketing en el nivel de superficie de canal. Cuando se utilizan en una superficie, todas las políticas de consentimiento asociadas con esa acción de marketing se aprovechan para respetar las preferencias de los clientes.

**Gestión de decisiones**

* Se han actualizado varias etiquetas relacionadas con el límite de ofertas en la interfaz de gestión de decisiones.
