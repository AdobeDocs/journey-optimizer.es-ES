---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d7ac73800a793fa5fec5d402e15e4f84db084f89
workflow-type: tm+mt
source-wordcount: '1140'
ht-degree: 65%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión. [!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Actualizaciones de mayo de 2025 {#25-5-rn}

* **Temas en el Designer de correo electrónico (Beta)** - Fecha de disponibilidad: 14 de mayo de 2025

  Ahora puede aplicar rápidamente temas de estilo preaprobados al contenido del correo electrónico para garantizar la coherencia de la marca en todos los correos electrónicos, acelerar el proceso de creación de campañas y producir correos electrónicos de alta calidad de forma independiente, al tiempo que reduce la dependencia en los equipos de diseño. [Más información](../email/apply-email-themes.md)

  >[!AVAILABILITY]
  >
  >Actualmente, esta función está en versión beta y solo se encuentra disponible para los clientes de dicha versión. Para unirse al programa beta, póngase en contacto con su representante de Adobe.

  ![](assets/do-not-localize/themes.gif)

* **Decisioning - Nuevo generador de fórmulas de IA** - Fecha de disponibilidad: 14 de mayo de 2025

  Ahora puede crear fórmulas de clasificación de toma de decisiones específicas al definir y combinar criterios a partir de una nueva interfaz mejorada. En lugar de depender únicamente de una prioridad de oferta estática, puede definir fórmulas de clasificación personalizadas que combinen puntuaciones del modelo de IA, prioridades de oferta, atributos de perfil, atributos de oferta y señales contextuales a través de una interfaz guiada. [Más información](../experience-decisioning/exd-ranking-formulas.md)

  ![](assets/do-not-localize/formula-builder.gif)

* **Carpetas para páginas de aterrizaje**: fecha de disponibilidad: sábado, 09 de mayo de 2025

  Para administrar fácilmente las páginas de aterrizaje, ahora puede utilizar carpetas para organizarlas de forma más eficaz en una jerarquía optimizada.  [Más información](../landing-pages/manage-lp.md)

* Activación de **píldoras para personalización** - Fecha de disponibilidad: 5 de mayo de 2025

  Se ha añadido un nuevo botón &quot;Píldoras&quot; al editor de personalización. Cuando se habilita, los atributos contextuales y de perfil se muestran como píldoras, lo que mejora la legibilidad del código. [Más información](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >Esta capacidad se implementará gradualmente en todos los entornos en los próximos 30 días.

* **Nueva compatibilidad con objetos de campaña para la copia de zona protegida**. Fecha de disponibilidad: 15 de mayo de 2025

  Al copiar campañas en varios entornos limitados mediante las funciones de exportación e importación de paquetes, ahora también se copian las siguientes dependencias: configuraciones de canal, variantes y configuración de experimento, políticas de decisión y elementos. [Más información](../configuration/copy-objects-to-sandbox.md)

## Notas de la versión de abril de 2025 {#25-4-rn}

**Fecha de lanzamiento**: 29-30 de abril de 2025

### Nuevas funciones {#25-04-features}

A continuación, se enumeran las nuevas funciones incluidas en esta versión.

<table>
<thead>
<tr>
<th><strong>Editor de personalización: aprendizaje práctico</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ya está disponible un sitio de prueba de personalización, donde puede experimentar con expresiones de personalización. Le permite explorar plantillas y cargas útiles de muestra para empezar a probar sus propias expresiones de personalización.</p>
<p>Para obtener más información, consulte la <a href="../personalization/personalize.md#playground">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 24 de abril de 2025</p>
<img src="assets/do-not-localize/templating-playground.gif"/>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Adobe Experience Manager as a Cloud Service integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The integration between Adobe Journey Optimizer and Adobe Experience Manager as a Cloud Service is now released in General Availability (GA). This integration enables seamless content sourcing and management for personalized customer journeys.</p>
<p>For more information, refer to the <a href="../integrations/aem-templates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>Simulate content variations (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>With the General Availability release, the feature now includes support for multilingual content and content experiments, enabling you to test variations across different languages and treatments. Additionally, it now supports contextual attributes (in addition to profile attributes), allowing for even more dynamic and situational content testing.</p>
<img src="assets/do-not-localize/variants.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Canal LINE</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ha ampliado sus funcionalidades en canales múltiples para incluir la compatibilidad con el canal LINE. Esta mejora le permite crear, editar y previsualizar experiencias de LINE, permitiendo interacciones más personalizadas y atractivas. Con LINE, puede conectarse con más clientes, enviar contenido relevante y mejorar su participación.</p>
<p>El canal LINE está habilitado para los clientes de Adobe Journey Optimizer bajo petición. Póngase en contacto con el Servicio de atención al cliente de Adobe o con su representante de Adobe para activar la función para su organización.</p>
<p>Para obtener más información, consulte la <a href="../line/get-started-line.md">documentación detallada</a>.</p></td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Custom SMS provider (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports custom SMS providers, allowing you to integrate your preferred SMS services for enhanced communication flexibility.</p>
<p>For more information, refer to the <a href="../sms/sms-configuration-custom.md">detailed documentation</a>.</p></td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Métricas de recorrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las métricas de recorrido ya están disponibles, lo que le permite medir el impacto de sus actividades en las métricas clave de su empresa y proporcionar una perspectiva más clara de su rendimiento.</p>
</br>
<img src="assets/do-not-localize/success-metric.gif"/>
<p>Para obtener más información, consulte la <a href="../building-journeys/success-metrics.md">documentación detallada</a>.</p>
<p>Fecha de disponibilidad: 9 de abril de 2025</p>
</td>
</tr>
</tbody>
</table>



<!--<table>
<thead>
<tr>
<th><strong>Calendar view for campaign and journey inventory (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new calendar view is now available for campaigns and journey activations. This feature provides a visual representation of scheduled activities, allowing you to view and manage your campaigns and journeys more effectively. Selecting a calendar item opens a right rail with detailed information. This feature is currently in Limited Availability.</p>
<img src="assets/do-not-localize/calendar.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Integración de Adobe Express (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer ahora se integra con Adobe Express, lo que le permite conectar sin problemas sus recursos creativos con la orquestación de recorrido. Esta integración simplifica el proceso de diseño e implementación de contenido personalizado en todas las campañas. </p>
<p>Actualmente, esta integración no está disponible para su uso con Healthcare Shield o Privacy and Security Shield.</p>
<img src="assets/do-not-localize/express_resize.gif">
<p>Para obtener más información, consulte la <a href="../integrations/express.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activar las ejecuciones diarias después de la finalización de la segmentación por lotes (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En el caso de los recorridos programados diariamente, una nueva opción le permite definir un intervalo de tiempo de hasta 6 horas para esperar los datos del público procedentes de los trabajos de segmentación por lotes, lo que garantiza que los recorridos se ejecuten con los datos más actualizados o se omitan si no están listos. La opción Activar después de la evaluación del público por lotes solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/read-audience.md#schedule">documentación detallada</a>.</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Themes in the Email Designer (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply pre-approved styling themes to your email content to ensure brand consistency across all emails, speed up your campaign creation process and independently produce hight-quality emails while reducing dependency on design teams.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Puntuación de alineación con la marca (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La función de puntuación de alineación de marca proporciona comentarios claros directamente en el diseñador de correo electrónico, lo que le ayuda a ver si el contenido se ajusta al tono, el estilo y las directrices de la marca. Esta función está disponible en Beta.</p>
<p>Para obtener más información, consulte la <a href="../content-management/brands-score.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/brand-score.gif">
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decisioning - New AI formula builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create specific Decisioning ranking formulas by defining and combining criteria from a new improved interface. Ranking formulas allow you to define rules that will determine which decision items should be presented first, rather than taking into account the priority scores.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table>
-->

### Mejoras {#25-04-improv}

**API de vista previa de campañas**

Hay nuevas API disponibles para previsualizar campañas, además de las capacidades de envío de pruebas existentes. [Más información](https://developer.adobe.com/journey-optimizer-apis/references/simulations/#operation/createCampaignPreview){target="_blank"}.

**Herramientas de la zona protegida**

<!--- **Decisioning sandbox copy**

  Decisioning objects can now be copied between sandboxes, streamlining testing and deployment workflows.-->

* **Herramientas de la zona protegida para acciones personalizadas**

  Las acciones personalizadas ahora se incluyen en la lista de objetos de Adobe Journey Optimizer que se pueden copiar mediante la función de herramientas de la zona protegida, lo que optimiza las pruebas y la implementación. [Más información](../configuration/copy-objects-to-sandbox.md)

* **Herramientas de la zona protegida para campañas**. Fecha de disponibilidad: 3 de abril de 2025

  Ahora puede copiar campañas en varias zonas protegidas mediante las funciones de exportación e importación de paquetes. Las campañas se copian junto con todos los elementos relacionados con el perfil, el público, el esquema, los mensajes en línea y los objetos dependientes. Algunos elementos no se copian, como los elementos de decisión, las etiquetas de uso de datos y la configuración de idioma. [Más información](../configuration/copy-objects-to-sandbox.md#custom-actions)

**Personalización**

* **Nuevo atributo contextual**

  Ahora hay disponible un nuevo atributo contextual, **ID de perfil de mensaje**, que se puede seleccionar en el editor de personalización. Es un atributo orientado a los mensajes que identifica de forma exclusiva cada mensaje enviado a cada perfil de destinatario en un envío. Este identificador único se puede utilizar, por ejemplo, como parámetro de seguimiento de URL para distinguir cada vínculo abierto o en el que los destinatarios hacen clic.

* **Atributos rellenados en el panel de atributos**. Fecha de disponibilidad: 2 de abril de 2025

  El panel de atributos del editor de personalización ahora muestra solo los atributos rellenados de forma predeterminada. Para ver todos los atributos, use el botón de configuración para desactivar la opción **[!UICONTROL Mostrar solo atributos rellenados]**. [Más información](../personalization/personalization-build-expressions.md)

**Canal de correo electrónico**

* **Seguimiento personalizado de URL** - Fecha de disponibilidad: 30 de abril de 2025

  Para obtener una mayor flexibilidad y control sobre la configuración del correo electrónico, ahora puede personalizar todos los parámetros de seguimiento de URL a la vez en el nivel de configuración del canal de correo electrónico, en lugar de hacerlo en el Diseñador de correo electrónico para cada vínculo del contenido. [Más información](../email/surface-personalization.md#personalize-url-tracking)

* **Diseñador de correo electrónico**. Fecha de disponibilidad: 1 de abril de 2025

  Para mejorar la accesibilidad en Journey Optimizer, ahora hay dos campos nuevos disponibles en Diseñador de correo electrónico: se corresponden con el elemento `<title>` y el atributo `lang` en el elemento `<html>` del contenido del correo electrónico. Puede definir esta configuración, además del campo **[!UICONTROL Preencabezado]**, en la sección **[!UICONTROL Cuerpo]** del correo electrónico. [Más información](../email/email-metadata.md)

**Libros de casos de uso**

* **Creación y uso compartido de libros de reproducción (beta privada)**: ahora puede crear, administrar y compartir sus propios libros de reproducción de casos de uso. Actualmente, esta funcionalidad solo está disponible para un conjunto de organizaciones como una versión beta privada. Para obtener acceso, póngase en contacto con su representante de Adobe. [Más información](../start/playbooks.md)

**Navegación**

* **Administración de contenido**. Fecha de disponibilidad: 2 de abril de 2025

  Para administrar con facilidad los fragmentos y las plantillas de contenido, ahora puede utilizar carpetas para organizarlos de forma más eficaz en una jerarquía estructurada. Obtenga más información en las secciones [Fragmentos](../content-management/manage-fragments.md#folders) y [Plantillas de contenido](../content-management/access-content-templates.md#folders)

  >[!AVAILABILITY]
  >
  >Esta mejora solo está disponible para un conjunto de organizaciones (disponibilidad limitada).

<!--- **Folders for content templates and fragments** - Availability date: May 5, 2025

  Previously available for a set of organizations (LA), folders are now available to all users (GA) to manage their content templates and fragments. Folders let you organize your content templates and fragments more easily and effectively into a structured hierarchy.



<!--- **Right rail in campaigns list**  

  A right rail has been added to the campaigns list, providing detailed information when a campaign is selected.-->

<!--**Playbooks**

- **Create your own playbooks (Beta)**
  
  You can now create your own playbooks in Adobe Journey Optimizer, enabling greater customization and flexibility in journey planning.-->




