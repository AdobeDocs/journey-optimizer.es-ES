---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d971d857a480868f5ef502f3a3f2c209afc93cca
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 70%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.

## Notas de la primera versión de agosto de 2024 {#e-2024}

**Fecha de lanzamiento**: 20-21 de agosto de 2024

>[!CAUTION]
>
>**Las notas de la versión anticipadas que se indican a continuación están sujetas a cambios sin previo aviso hasta la fecha de lanzamiento**. Los vínculos, las pantallas y la documentación actualizada se publican en la fecha del lanzamiento.
>

### Nuevas funciones {#e-features}

Esta versión incorpora las nuevas funciones que se indican a continuación.

<!--table>
<thead>
<tr>
<th><strong>Guided Channel Setup</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Guided Channel Setup enables you to automate and validate channel setup in a unified experience, speeding up the process of getting started with Journey Optimizer. This new guided setup streamlines rapid channel configuration, ensuring all necessary resources are readily installed and working within Experience Platform, Journey Optimizer, and Data Collection. This enables marketing, product and data engineering teams to quickly begin with campaign and journey creation.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Content Cards</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content card is a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Improved Channel Configurations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The current channel surface capabilities have been enhanced for a consistent approach across all channels. You can now define, manage, and reuse these configurations for any of your channels, including Web, In-app messaging, or Code-based experience.</p>
<p><ul>
<li>Channel surfaces are now renamed to <strong>Channel configurations</strong></li>
<li>You can attach one or multiple marketing actions to enforce consent and data governance policies</li>
<li>Object level access control (OLAC) is now available for each channel configuration, allowing you to decide which of your users are allowed to create or use specific configurations</li>
<li>For some channels, you can create channel configurations that target multiple platforms. An example here would be an In-app messaging channel configuration that can target a web page, an iOS app and an Android app.</li>
</ul></p>
</td>
</tr>
</tbody>
</table-->

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


### Mejoras {#e-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Recorridos**

<!--* In the **Condition** activity, by default, the Time condition is now set by hour, from 00:00 to 12:00. [Read more](../building-journeys/condition-activity.md#time_condition)-->
* Al crear las alertas, estas ahora se muestran en una lista desplegable para alinearse con las recorridos de la campaña y ofrecer una experiencia de usuario coherente. [Más información](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* Se han mejorado las opciones de zoom en la barra de herramientas de recorrido: el porcentaje de zoom ahora está visible y ahora puede restablecer fácilmente el valor de zoom al 100 %.

**Públicos**

* El uso de audiencias de carga personalizada (archivo CSV) ya está disponible para su uso con el complemento Escudo de seguridad y privacidad.
* Al segmentar una audiencia de carga personalizada (archivo CSV), ahora puede utilizar atributos del archivo en sus campañas y recorridos. Estos atributos están disponibles en el editor de personalización para personalizar los mensajes y en el editor de expresiones avanzadas de recorrido.

## Notas de la versión de julio de 2024 {#24-7-2024}

**Fecha de la versión**: 30-31 de julio de 2024

### Nuevas funciones {#27-4-features}

Esta versión incorpora las nuevas funciones que se enumeran a continuación.

<table>
<thead>
<tr>
<th><strong>Canal de SMS con cualquier proveedor (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede configurar proveedores de SMS adicionales en Journey Optimizer, además de los proveedores predeterminados Sinch, Infobip y Twilio.</p>
<img src="assets/do-not-localize/byo_sms.gif"/>
<p>Para obtener más información, consulte la <a href="../sms/sms-configuration-custom.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Composición de público federado (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La composición de público federado ya está disponible en Adobe Journey Optimizer. Permite a las empresas componer datos para una mejor utilización en varios casos de uso. Con este nuevo enfoque, como usuario de Adobe Real-time Customer Data Platform y/o Adobe Journey Optimizer, puede federar conjuntos de datos directamente desde su almacén de datos existente para generar y enriquecer públicos y atributos de Adobe Experience Platform en un solo sistema.</p>
<p>Para obtener más información, consulte la <a href="https://experienceleague.adobe.com/es/docs/federated-audience-composition/using/home"  target="_blank">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Mejoras {#27-4-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Recorridos**

* (Fecha de disponibilidad: 8 de julio) **Editor de expresiones avanzadas de la configuración de eventos del recorrido**: ahora puede aprovechar el editor de expresiones avanzadas mientras configura un evento, lo que le permite definir expresiones más complejas o utilizar funciones en la condición de ID de evento. [Más información](../event/about-creating.md#adv-exp-editor)

