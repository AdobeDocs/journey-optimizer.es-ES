---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 299b34dec2e864fff5eb874b3fd491da80bc0c16
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 100%

---

# Notas de la versión {#release-notes}


>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras de las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión.

Las notas de la versión anteriores están disponibles en [esta página](release-notes-2023.md). También puede consultar la página de las [últimas actualizaciones de la documentación](documentation-updates.md) para ver más cambios.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.

## Notas de la versión de octubre de 2023 {#oct-rn-2023}

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
<p>Para obtener más información, consulte la <a href="../building-journeys/copy-to-sandbox.md">documentación detallada</a>.</p>
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
<th><strong>Servicio de mensajes multimedia (MMS) en SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con el canal SMS, ahora puede mejorar su comunicación enviando mensajes del servicio de mensajes multimedia (MMS), lo que le permite compartir imágenes, GIF o vídeos con sus clientes. Tenga en cuenta que esta funcionalidad solo está disponible actualmente con Sinch.</p>
<img src="assets/do-not-localize/mms.gif"/>
<p>Para obtener más información, consulte la <a href="../sms/create-sms.md#mms-content">documentación detallada</a>.</p>
</tr>
</tbody>
</table>

### Mejoras {#oct-2023-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Públicos**

* Ahora puede dirigirse a públicos destinatarios cargados desde un archivo CSV en recorridos y campañas. [Más información](../audience/about-audiences.md#segments-in-journey-optimizer)
* Ahora puede dirigirse a públicos destinatarios creados mediante la composición de públicos y aprovechar los atributos de enriquecimiento de los recorridos. [Más información](../building-journeys/read-audience.md)

>[!AVAILABILITY]
>
>Estas funcionalidades están disponibles actualmente como una versión Private Beta.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**Campañas**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* Cuando se produce un error en una de las campañas, ahora aparece un icono de advertencia en la lista de campañas junto con el estado de la campaña. [Más información](../campaigns/modify-stop-campaign.md#statuses)

**Recorridos**

* La duración máxima que puede definir en cualquier tiempo de espera ahora es de 29 días, en lugar de 30. Esta mejora se ha introducido para evitar que la duración de la espera supere los 30 días de vida útil del recorrido. Esto se aplica a:

   * el campo **Cantidad de tiempo** en la [actividad de espera](../building-journeys/wait-activity.md)
   * el **Período de espera de reentrada** en [propiedades del recorrido](../building-journeys/journey-gs.md#entrance)
   * el campo **Esperar a** en la definición de tiempo de espera de las [actividades de eventos](../building-journeys/general-events.md#events-specific-time).

<!--
**Consent in channel configuration**

* You can now select a marketing action at the channel surface level. When used in a surface, all consent policies associated with that marketing action are leveraged in order to respect the preferences of your customers.-->

**Gestión de decisiones**

* Se han actualizado varias etiquetas relacionadas con el límite de ofertas en la interfaz de gestión de decisiones. [Más información](../offers/offer-library/add-constraints.md#capping)

