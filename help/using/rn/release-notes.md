---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: a326d0869f5d195c4a2b4be930e981c11a15afd9
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 47%

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

<table>
<thead>
<tr>
<th><strong>Configuración de canal guiado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La configuración guiada de canales le permite automatizar la configuración de canales en una experiencia unificada, lo que acelera el proceso de introducción a Journey Optimizer. Esta nueva configuración guiada optimiza la configuración rápida de canales, lo que garantiza que todos los recursos necesarios estén fácilmente disponibles en Experience Platform, Journey Optimizer y la recopilación de datos. Esto permite a los equipos de marketing, producto e ingeniería de datos empezar rápidamente con la creación de campañas y recorridos.</p>
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
<p>Las funciones actuales de superficie de canal se han mejorado para lograr un enfoque coherente en todos los canales. Ahora puede definir, administrar y reutilizar estas configuraciones para cualquiera de sus canales, incluidos la web, la mensajería en la aplicación o la experiencia basada en código.</p>
<p><ul>
<li>Ahora se cambió el nombre de las superficies de canal a <strong>Configuraciones de canal</strong></li>
<li>Puede adjuntar una o varias acciones de marketing para aplicar políticas de consentimiento y control de datos</li>
<li>El control de acceso a nivel de objeto (OLAC) ya está disponible para cada configuración de canal, lo que le permite decidir cuál de sus usuarios puede crear o utilizar configuraciones específicas</li>
<li>Para algunos canales, puede crear configuraciones de canal dirigidas a varias plataformas. Un ejemplo sería una configuración de canal de mensajería en la aplicación que puede dirigirse a una página web, una aplicación de iOS y una aplicación de Android.</li>
</ul></p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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


### Mejoras {#e-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Recorridos**

* En la actividad **Condition**, de forma predeterminada, la condición Time ahora se establece por hora, de 00:00 a 12:00. [Más información](../building-journeys/condition-activity.md#time_condition)
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

