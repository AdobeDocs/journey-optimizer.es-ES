---
solution: Journey Optimizer
product: journey optimizer
title: Notas de la versión
feature: Release Notes
topic: Content Management
description: Notas de la versión de Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: c54ad4cddeb7115f9a069102c67c41f0850a11ed
workflow-type: tm+mt
source-wordcount: '1601'
ht-degree: 89%

---

# Notas de la versión {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novedades"
>abstract="**Adobe Journey Optimizer** ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión."

[!DNL Adobe Journey Optimizer] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan la última semana de cada mes en estas notas de la versión. [!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Actualizaciones del 24 de octubre {#24-10-rn}

Próxima **fecha de la versión**: 28-30 de octubre de 2024

Las [funcionalidades](#24-10-features) y [mejoras](#24-10-improvements) que se enumeran a continuación se publicaron este mes.

### Nuevas funciones {#24-10-features}

<table>
<thead>
<tr>
<th><strong>Experiencia actualizada de creación de informes (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La creación de informes de Journey Optimizer ya está disponible de forma general (GA) y ofrece una interoperabilidad mejorada con funciones de Customer Journey Analytics, estandarización de los informes en ambas plataformas y mejora de la coherencia y fiabilidad de los datos. Esta integración perfecta entre Journey Optimizer y Customer Journey Analytics proporciona una visión más clara de las métricas de rendimiento, lo que permite a los usuarios tomar decisiones más informadas.</p>
<p>Con la disponibilidad general, se introducen cuatro nuevas funciones: la capacidad de crear métricas sencillas, crear y publicar audiencias, hacer preguntas específicas mediante Insight Builder y programar informes para que se envíen automáticamente por correo electrónico a los destinatarios clave.</p>
<p>Para obtener más información, consulte la <a href="../reports/report-cja-manage.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Fecha de disponibilidad: 16 de octubre de 2024</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experiencias basadas en código en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con el canal de experiencia basado en código, Adobe Journey Optimizer le permite realizar personalizaciones y pruebas avanzadas para cualquiera de sus propiedades de entrada, lo que permite ofrecer experiencias adaptadas en diversos puntos de contacto, como aplicaciones web, aplicaciones móviles, aplicaciones de escritorio, consolas de vídeo, servicios conectados a TV, televisores inteligentes, quioscos, cajeros automáticos, dispositivos IoT y mucho más. El canal de experiencia basado en código ya está disponible en el lienzo de recorrido.</p>
<p>Para obtener más información, consulte la <a href="../code-based/create-code-based.md">documentación detallada</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
<p>Fecha de disponibilidad: 1 de octubre de 2024</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experiencias web en recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con el canal web, Adobe Journey Optimizer permite personalizar la experiencia web que ofrece a sus clientes a través de recorridos web entrantes. El canal web ahora está disponible en el lienzo de recorrido.</p>
<p>Para obtener más información, consulte la <a href="../web/create-web.md">documentación detallada</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
<p>Fecha de disponibilidad: 1 de octubre de 2024</p>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>La experiencia actual de creación de informes se eliminará a partir de enero de 2025. Después de esta fecha, la nueva experiencia de creación de informes pasará a ser el estándar. Recomendamos que se familiarice con las nuevas funciones y características para garantizar una transición sin problemas.
>
> [Aprenda a empezar con la nueva interfaz de creación de informes de Journey Optimizer](../reports/report-gs-cja.md)

### Mejoras {#24-10-improvements}

**Recorridos**: fecha de disponibilidad: 3 de octubre de 2024

* **Parámetros en acciones personalizadas**: ahora se admiten parámetros NULL y opcionales en las acciones personalizadas. [Más información](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Gobernanza de datos y políticas de consentimiento**: fecha de disponibilidad: 7 de octubre de 2024

* La aplicación de las **políticas de control de datos** ahora se aplica en todos los canales de Journey Optimizer. Para los clientes que han creado políticas en Adobe Experience Platform, estas se aplican a las acciones de marketing como parte de la configuración de canales. Al crear contenido con una configuración, el sistema comprueba todos los campos de personalización para detectar cualquier infracción de la gobernanza de datos. Si se encuentra una infracción, no será posible publicar un recorrido o una campaña. [Más información](../action/action-privacy.md)

* Las **políticas de consentimiento personalizado** ahora se aplican a todos los canales de Journey Optimizer. Al aplicar la ley antes de enviar un mensaje o de entregar una experiencia entrante, el sistema comprueba que el usuario haya dado su consentimiento para utilizar campos de personalización en el contenido que va a recibir. Si no se da ningún consentimiento, la experiencia no se muestra. [Más información](../action/consent.md)

  >[!NOTE]
  >
  >Actualmente, las políticas de consentimiento solo están disponibles para las organizaciones que han adquirido las ofertas sobre el programa **Healthcare Shield** y el programa **Privacy and Security Shield**.

**Públicos**: fecha de disponibilidad: 8 de octubre de 2024

* Al segmentar el público de un archivo CSV, ahora puede utilizar atributos del archivo en el editor de personalización y en el generador de reglas de recorridos y campañas. [Más información](../audience/about-audiences.md)

* El uso de públicos y atributos de cargas personalizadas (archivos CSV) no está disponible en la actualidad para su uso con el programa Healthcare Shield ni Privacy and Security Shield.

## Versión de septiembre de 2024 {#24-9-rn}

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

**Fecha de la versión**: 24-26 de septiembre de 2024

### Nuevas funciones {#24-9-features}

Esta versión incorpora las nuevas funciones que se indican a continuación.

<table>
<thead>
<tr>
<th><strong>Tarjetas de contenido para aplicaciones móviles y sitios web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Las tarjetas de contenido son una nueva función de mensajería digital de Adobe Journey Optimizer que ofrece contenido personalizado y atractivo directamente en aplicaciones móviles y sitios web. A diferencia de las notificaciones push tradicionales, las tarjetas de contenido se integran perfectamente en la interfaz de usuario y ofrecen actualizaciones persistentes y no intrusivas que mejoran la interacción y experiencia del usuario.</p>
<p>Esta función permite a los especialistas en marketing presentar a los usuarios contenido con medios enriquecidos y relevantes, para aumentar la participación y garantizar que se vean mensajes importantes sin distraer al usuario del recorrido.</p>
<p>Para obtener más información, consulte la <a href="../content-card/get-started-content-card.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/content-card.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aprobaciones en recorridos y campañas (LA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Con las políticas de aprobación, ahora puede configurar un proceso de aprobación dentro de Journey Optimizer que permita a los equipos de marketing asegurarse de que las campañas y los recorridos sean revisados y firmados por las partes interesadas correspondientes antes de que se activen.</p>
<p>Ahora mismo, las políticas de aprobación solo están disponibles para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.</p>
<p>Para obtener más información, consulte la <a href="../test-approve/gs-approval.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Email Content Locking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now allows you to lock content in email templates, either by locking the entire template or specific structures and component. This allows you to prevent unintentional edits or deletions, giving you greater control over template customization, and improving the efficiency and reliability of your email campaigns.</p>
<p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Criterios de salida globales en los recorridos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede definir los criterios de salida en el nivel de recorrido. Al añadir criterios de salida, hace que los perfiles salgan del recorrido en cuanto se produce un evento (p. ej.: compra) o cumplen los requisitos para un público. Esto evitará que el usuario reciba más comunicaciones del recorrido.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/journey-properties.md#exit-criteria">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Acelerador de contenido del Asistente de IA </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Una vez creado y personalizado el mensaje, lleve el contenido al siguiente nivel con el acelerador de contenido del asistente de IA en Journey Optimizer. Ahora puede utilizar el asistente de IA para optimizar el impacto de su mensaje experimentando con diferentes títulos e imágenes principales. Cada variante se gestiona como un tratamiento único para medir y comparar qué título genera más clics de forma efectiva.</p>
<p>Láncese a una experiencia práctica inmersiva con <a href="https://experienceleague.adobe.com/es/apps/journey-optimizer/ai-assistant-content-accelerator">nuestra vista previa en directo</a>, diseñada para permitirle explorar sus funciones en primera persona y comprender plenamente sus capacidades.</a></p>
<p>Para obtener más información, consulte la <a href="../content-management/gs-generative.md">documentación detallada</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/>
<p>Fecha de disponibilidad: 12 de septiembre de 2024</p>
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
<p>Fecha de disponibilidad: 3 de septiembre de 2024</p>
</br>
</td>
</tr>
</tbody>
</table>


### Mejoras {#24-9-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

**Públicos**: fecha de disponibilidad: 17 de septiembre de 2024

**Uso de licencias**: el panel Uso de licencias ahora muestra perfiles interesados, en lugar de públicos interesados. [Más información](../audience/license-usage.md)

**Administración de contenido**

Ahora puede exportar plantillas de contenido y fragmentos entre zonas protegidas. [Más información](../configuration/copy-objects-to-sandbox.md)

**Recorridos**

* **Mejoras en la creación de informes en directo**: la creación de informes en directo proporciona información sobre el rendimiento de sus recorridos en las últimas 24 horas. La hemos mejorado añadiendo nuevas métricas (perfiles de entrada, salida y descartados y perfiles erróneos), lo que le permite comprender mejor el comportamiento y el rendimiento del usuario directamente desde el lienzo de recorrido. [Más información](../building-journeys/report-journey.md)


* (Fecha de disponibilidad: 10 de septiembre) **Reintentos automáticos de Leer público**: los reintentos ahora se aplican de forma predeterminada a los recorridos activados por públicos (empezando con una actividad **Leer público** o **Evento empresarial**) cuando se recupera el trabajo de exportación. Si se produce un error durante la creación del trabajo de exportación, se realizarán reintentos cada 10 minutos, hasta un máximo de 1 hora. Después de esto, se considerará como un error. Por lo tanto, estos tipos de recorridos se pueden ejecutar hasta una hora después de la hora programada. [Más información](../building-journeys/read-audience.md#retries)

**Canal de correo electrónico**

* **Encabezado de mensaje en el correo electrónico enviado y copia CCO**: se ha añadido un nuevo encabezado a todos los mensajes de correo electrónico. El valor de este encabezado es único para cada correo electrónico enviado y para su copia de correo electrónico CCO correspondiente. Este encabezado también se almacena en los conjuntos de datos del mensaje y en los comentarios CCO, lo que permite reconciliar la copia CCO y la información de correo electrónico enviado correspondiente. [Más información](../configuration/archiving-support.md#bcc-header)

* **Puntuación de correo no deseado** (GA): ahora puede comprobar la puntuación de correo no deseado de su contenido en un **informe específico**. Utilizando SpamAssassin, Adobe Journey Optimizer ahora puede probar el contenido de su correo electrónico y darle una puntuación para indicar si los ISP o los proveedores de buzones lo considerarán correo no deseado o no. [Más información](../content-management/spam-report.md)

**Canal de SMS**

* **Editar credenciales de API**: ahora puede editar la configuración en las credenciales de API de SMS, incluidas las actualizaciones de las palabras clave de inclusión/exclusión y las respuestas.

**API**

* **API de simulación de campaña**: use esta API para activar el trabajo de prueba de una campaña. El envío de la prueba de una campaña es un proceso asincrónico, la API devuelve un proofJobId que se puede utilizar para comprobar el estado de la prueba. [Más información](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}

* (Fecha de disponibilidad: 10 de septiembre) La [documentación de la API de Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} ahora es interactiva. Explore los extremos de la API directamente desde las páginas de documentación para obtener comentarios inmediatos y acelerar la implementación técnica. 


  Todas las páginas de referencia de la API ahora tienen una funcionalidad **Probar** que puede usar para probar las llamadas de la API directamente en la página del sitio web de documentación. [Obtenga las credenciales de autenticación requeridas](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} y empiece a usar la funcionalidad para explorar los extremos de la API.

  Utilice esta nueva funcionalidad para explorar las solicitudes y las respuestas de los extremos de la API, obtener comentarios inmediatos y acelerar la implementación técnica. 

  >[!CAUTION]
  >
  >Tenga en cuenta que, al utilizar la funcionalidad de API interactiva en las páginas de documentación, está realizando llamadas de API reales a los puntos finales. Tenga esto en cuenta al experimentar con zonas protegidas de producción.

Configuración de ****

* **Planes de calentamiento de IP**: esta capacidad ya está disponible para todos los clientes, incluidas las organizaciones que han adquirido las ofertas complementarias **Healthcare Shield** o **Privacy and Security Shield** de Adobe. [Más información](../configuration/ip-warmup-gs.md)


![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.