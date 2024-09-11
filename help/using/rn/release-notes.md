---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 633d2f423301680a7aff83b748a08a6f1a1bbf16
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 83%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.

## Actualizaciones de septiembre {#9-2024}

<table>
<thead>
<tr>
<th><strong>Ayudante de IA en el optimizador de Recorrido: acelerador de contenido </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una vez creado y personalizado el mensaje, lleve el contenido al siguiente nivel con el asistente de IA de Journey Optimizer para la aceleración de contenido. Ahora puede utilizar el asistente de IA para optimizar el impacto de su mensaje experimentando con diferentes títulos e imágenes principales. Cada variante se gestiona como un tratamiento único para medir y comparar qué título genera más clics de forma efectiva.</p>
<p>Sumérjase en una experiencia práctica con <a href="https://experienceleague.adobe.com/en/apps/journey-optimizer/ai-assistant-content-accelerator">nuestra vista previa de características en vivo</a>, diseñada para que explore sus características de primera mano y comprenda plenamente sus capacidades.</a>.</p>
<p>Para obtener más información, consulte la <a href="../content-management/gs-generative.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Configuración de canales guiada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La configuración de canales guiada le permite automatizar y validar la configuración del canal en una experiencia unificada, lo que acelera el proceso de introducción a Journey Optimizer. Esta nueva configuración guiada optimiza la configuración de canal rápida, lo que garantiza que todos los recursos necesarios se instalen y funcionen fácilmente en Experience Platform, Journey Optimizer y recopilación de datos. Esto permite a los equipos de marketing, productos e ingeniería de datos empezar rápidamente en la creación de campañas y recorridos.</p>
<p>Para obtener más información, consulte la <a href="../configuration/set-mobile-config.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/guided-setup.gif"/>
<p>Fecha de disponibilidad: 3 de septiembre</p>
</br>
</td>
</tr>
</tbody>
</table>

**Recorridos**

(Fecha de disponibilidad: 10 de septiembre) **Capacidad de reintento**: los reintentos ahora se aplican de forma predeterminada en recorridos activados por la audiencia (a partir de **Leer audiencia** o un **Evento empresarial**) al recuperar el trabajo de exportación. Si se produce un error durante la creación del trabajo de exportación, se realizarán reintentos cada 10 minutos, hasta un máximo de 1 hora. Después de eso, lo consideraremos como un fracaso. Por lo tanto, estos tipos de recorridos se pueden ejecutar hasta 1 hora después de la hora programada. [Más información](../building-journeys/read-audience.md#retries)

## Notas de la versión de agosto de 2024 {#8-2024}

**Fecha de lanzamiento**: 20-21 de agosto de 2024

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

### Nuevas funciones {#8-features}

Esta versión incorpora las nuevas funciones que se indican a continuación.

<!--
<table>
<thead>
<tr>
<th><strong>Content Cards (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content cards are a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</br>
<p>Content card are currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->

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
<li>Se ha cambiado el nombre de las superficies de canal a <strong>Configuraciones de canal</strong></li>
<li>Puede adjuntar una o varias acciones de marketing para aplicar políticas de consentimiento y gobernanza de datos</li>
<li>El control de acceso a nivel de objeto (OLAC) ya está disponible para cada configuración de canal, lo que le permite decidir cuál de sus usuarios puede crear o utilizar configuraciones específicas</li>
<li>Para algunos canales, puede crear configuraciones de canal dirigidas a varias plataformas. Un ejemplo sería una configuración de canal de mensajería en la aplicación que pueda dirigirse a una página web, una aplicación de iOS y a una aplicación de Android.</li>
</ul></p>
<p>Para obtener más información, consulte la <a href="../configuration/channel-surfaces.md">documentación detallada</a>.</p>
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
<p>Para obtener más información, consulte la <a href="../action/marketo-engage.md">documentación detallada</a>.</p>
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
<p>Las variables globales de fragmentos realzan la funcionalidad de fragmentos existente para mejorar la eficacia en los casos de uso de scripts y reutilización de contenido. Los fragmentos ahora pueden utilizar variables de entrada y crear variables de salida utilizables en el contenido de campaña y recorrido. Los fragmentos ahora pueden consumir variables de entrada, tanto en <a href="../personalization/use-expression-fragments.md">fragmentos de expresión</a> como en <a href="../email/use-visual-fragments.md">fragmentos visuales</a>. Se pueden utilizar esas variables para personalizar el contenido y los parámetros de los mensajes, en sus campañas y recorridos.</p>
<p>Para obtener más información, consulte la <a href="../personalization/use-expression-fragments.md">documentación detallada</a>.</p>
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

### Mejoras {#8-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Recorridos**

* En la actividad **Condición**, de forma predeterminada, la **[!UICONTROL condición Tiempo]** se establece ahora por hora, de 00:00 a 12:00. [Más información](../building-journeys/condition-activity.md#time_condition)
* Al crear los recorridos, las alertas se muestran ahora en el botón **Alertas** para alinearse con otras alertas y ofrecer una experiencia de usuario coherente. [Más información](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* Se han mejorado las opciones de zoom en la barra de herramientas del recorrido. El porcentaje del zoom ahora es visible y se puede restablecer su valor más fácilmente.

<!--**Audiences and Profiles**-->

<!--* The use of audiences from custom upload (CSV file) is now available for use with Privacy and Security Shield add-on.-->
<!--* When targeting a custom upload (CSV file) audience, you can now use attributes from the file in your campaigns and journeys. These attributes are available in the personalization editor, to personalize your messages, and the journey advanced expression editor.-->
<!--* The License usage dashboard now shows the count of Engageable Profiles. [Read more](../audience/license-usage.md)-->

**Canal push**

* Ahora puede añadir las credenciales push de la aplicación móvil en los ajustes de configuración del canal de Adobe Journey Optimizer. Ya no es necesario crear una superficie de aplicación en la recopilación de datos de Adobe Experience Platform.

### Otros cambios {#changes}

**Creación de informes**

* La experiencia actual de creación de informes se eliminará a partir de la versión de octubre. Después de esta fecha, la nueva experiencia de creación de informes pasará a ser el estándar. Recomendamos que se familiarice con las nuevas funciones y características para garantizar una transición sin problemas.

[Introducción a la nueva interfaz de sistema de creación de informes de Journey Optimizer](../reports/report-gs-cja.md)

* Se han añadido nuevos casos de uso a la nueva experiencia de creación de informes:

   * Cree métricas calculadas personalizadas directamente en los informes.
   * Cree un público a partir de los datos de creación del informe.
   * Use la herramienta de análisis exploratorio para crear fácilmente tablas y visualizaciones a partir de las **[!UICONTROL Dimensiones]** y las **[!UICONTROL Métricas]** que haya seleccionado.

  Para obtener más información, consulte la [documentación detallada](../reports/report-cja-manage.md).
