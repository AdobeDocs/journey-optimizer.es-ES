---
title: Introducción a las experiencias basadas en código
description: Obtenga información sobre las experiencias basadas en código en Journey Optimizer
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: 60c74bcc5e33afa354a2380d3e6f490a4c2c3e6d
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 7%

---

# Introducción al canal basado en código {#get-sarted-code-based}

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* **[Introducción al canal basado en código](get-started-code-based.md)**
* [Requisitos previos basados en código](code-based-prerequisites.md)
* [Ejemplos de implementación basada en código](code-based-implementation-samples.md)
* [Crear experiencias basadas en código](create-code-based.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>El canal de experiencia basado en código está disponible actualmente como una versión beta solo para usuarios seleccionados. Para unirse al programa beta, póngase en contacto con el Servicio de atención al cliente de Adobe.

[!DNL Journey Optimizer] le permite personalizar y probar las experiencias que desea ofrecer a sus clientes en todos sus puntos de contacto, como aplicaciones web, aplicaciones móviles, aplicaciones de escritorio, videoconsolas, dispositivos conectados a TV, televisores inteligentes, quioscos, cajeros automáticos, asistentes de voz, dispositivos IoT, etc.

Con el **experiencia basada en código** puede definir las experiencias entrantes mediante un editor no visual sencillo e intuitivo. Permite insertar y editar elementos específicos en ubicaciones individuales y más granulares de sus aplicaciones o páginas web, independientemente del tipo de aplicaciones que tenga, en lugar de aplicar modificaciones a todo un contenido.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

Cuando usted [creación de una campaña](../campaigns/create-campaign.md#configure), seleccione **Experiencia basada en código (Beta)** como su acción y defina la configuración básica.

>[!NOTE]
>
>Si es la primera vez que crea una experiencia web, asegúrese de seguir los requisitos previos descritos en [esta sección](code-based-prerequisites.md).

<!--Discover the detailed steps to create a code-based campaign in this video.-->

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="#how-it-works">
<img alt="Posible cliente" src="../assets/do-not-localize/privacy-audit.jpeg">
</a>
<div><a href="#how-it-works"><strong>Funcionamiento</strong>
</div>
<p>
</td>
<td>
<a href="code-based-prerequisites.md">
<img alt="Validación" src="../assets/do-not-localize/web-prerequisites.jpg">
</a>
<div>
<a href="code-based-prerequisites.md"><strong>Requisitos previos</strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="Poco frecuente" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong>Crear una experiencia basada en código</strong></a>
</div>
<p></td>
<td>
<a href="create-code-based.md#edit-code">
<img alt="Validación" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="create-code-based.md#edit-code"><strong>Edite el código</strong></a>
</div>
<p>
</td>
</tr></table>



<!--[Learn how to create a code-based campaign in this video](#video)-->

## Cuándo usar canales basados en código o en otros canales {#code-based-vs-other-channels}

### Basado en código frente a otros canales

Cuándo utilizar el canal basado en código en lugar del otro [!DNL Journey Optimizer] canales?

* Puede considerar la posibilidad de utilizar experiencias basadas en código en cualquier momento en el que no se acceda a su propiedad digital a través de un explorador web o una aplicación móvil, casos en los que probablemente pueda utilizar mejor el [!DNL Journey Optimizer] [canal web](../web/get-started-web.md){target="_blank"} or the [!DNL Journey Optimizer] [in-app messaging](../in-app/get-started-in-app.md){target="_blank"} canal.

* Puede utilizar el canal basado en código como alternativa al [!DNL Journey Optimizer] canal web si el sitio web no se puede cargar en [editor visual web](../web/author-web.md){target="_blank"} or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} que potencia la creación visual para el canal web.

* También puede utilizar el canal basado en código como alternativa al [!DNL Journey Optimizer] canales web o en la aplicación en caso de que tenga una implementación basada en API, sin encabezado o del lado del servidor.

### Canal basado en código frente a canal web

Para ejecutar casos de uso web, puede utilizar el canal web o la experiencia basada en código, pero según el contexto, una sería más apropiada que la otra. Las principales diferencias se enumeran a continuación para que pueda tomar una decisión informada sobre qué utilizar cuando.

**Web**
* Edite el contenido con la variable [editor visual](../web/author-web.md){target="_blank"}.
* Necesita el [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"} implementation and the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}
* El canal web permite modificar todo lo que hay en la página y tiene una lista predefinida de acciones que puede utilizar para realizar cambios. [Más información](../web/author-web.md){target="_blank"}
* Es fácil de configurar y ponerse en marcha rápidamente.
* Se centra en el experto en marketing.

**Experiencia basada en código**
* Edite el contenido con la variable [Editor de expresiones](create-code-based.md#edit-code).
* La experiencia basada en código requiere un trabajo de desarrollo previo en la implementación para garantizar que las superficies puedan interpretar y entregar el contenido publicado en Edge de la siguiente manera [!DNL Journey Optimizer] para estas superficies. [Más información](#surface-definition)
* Requiere más planificación y solo puede cambiar las cosas que especifican los desarrolladores. Por lo tanto, es esencial identificar los componentes (titular de inicio, imagen a pantalla completa, barra de menús, etc.) en las superficies que deben modificarse para la personalización o la prueba, y trabaje con su equipo de desarrollo para crear la implementación necesaria para gestionar estos cambios.
* Le permite utilizar contenido con código JSON.
* Se centra en el desarrollador-persona.

## Funcionamiento {#how-it-works}

>[!CAUTION]
>
>Esta función es para usuarios experimentados o con personalidad de desarrollador. Los especialistas en marketing con algunas habilidades de escritura de código pueden utilizarla, siempre y cuando el equipo de desarrollo gestione las implementaciones de superficie y la configuración inicial.

Para editar el contenido con [!DNL Journey Optimizer] función de experiencia basada en código, sus páginas o aplicaciones deben estar instrumentadas. Para ello, debe declarar por adelantado las ubicaciones individuales específicas (denominadas &quot;[superficies](#surface-definition)&quot;) donde desee insertar o reemplazar contenido<!--HOW??-->.

>[!NOTE]
>
>Actualmente, el contenido asociado a una superficie solo puede ser HTML o JSON. <!--WILL COME LATER: text, image or another format depending on the application-->

Los pasos clave para implementar una campaña basada en código son los siguientes.

1. Defina un [emerger](#surface-definition), que es básicamente la ubicación en la que desea añadir la experiencia basada en código y crear una campaña en [!DNL Journey Optimizer] utilizando esta superficie. [Descubra cómo](create-code-based.md#create-code-based-campaign)

1. Componga una experiencia especificando contenido para la superficie seleccionada utilizando [!DNL Journey Optimizer] Editor de expresiones. [Descubra cómo](create-code-based.md#edit-code)

1. El equipo de implementación de la aplicación realiza llamadas explícitas de API o SDK para recuperar contenido para las superficies con nombre, como &quot;Texto del titular&quot; o &quot;Bandeja de Recommendations 1&quot;, o puntos de decisión no relacionados con la interfaz de usuario en una aplicación, como &quot;parámetros de algoritmo de búsqueda&quot;. En este caso, el equipo de implementación es responsable de procesar o interpretar de otra manera y actuar sobre el contenido devuelto.<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## ¿Qué es una superficie? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Definir una superficie de experiencia basada en código"
>abstract="Una superficie basada en código es cualquier entidad diseñada para la interacción del usuario o del sistema, que se identifica de forma exclusiva mediante un URI."

A **superficie de experiencia basada en código** es cualquier entidad diseñada para la interacción del usuario o del sistema<!--ask Robert to explain further-->, que se identifica de forma exclusiva mediante una **URI**.

En otras palabras, una superficie puede verse como un contenedor en cualquier nivel de jerarquía con una entidad (punto de contacto) que existe.<!--good idea to illustrate how it can be seen, but to clarify-->

* Puede ser una página web, una aplicación móvil, una aplicación de escritorio o una ubicación de contenido específica dentro de una entidad más grande (por ejemplo, una `div`) o un patrón de visualización no estándar (por ejemplo, un quiosco o un banner de aplicación de escritorio).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* También se puede ampliar a fragmentos específicos de contenedores de contenido para fines de no visualización o de visualización abstracta (por ejemplo, blobs JSON entregados a servicios de ).

* También puede ser una superficie comodín que coincida con una variedad de definiciones de superficie de cliente (por ejemplo, una ubicación de imagen a pantalla completa en cada página del sitio web podría traducirse en un URI de superficie como: web://mydomain.com/*#hero_image).

Básicamente, un URI de superficie está compuesto por varias secciones:
1. **Tipo**: web, aplicación móvil, servicio, quiosco, tvcd, etc.
1. **Propiedad**: dominio o paquete de aplicaciones
1. **Ruta**: actividad de página/aplicación ± ubicación en la actividad de página/aplicación <!--to clarify-->

En la tabla siguiente se muestran algunos ejemplos de definiciones de URI de superficie para varios dispositivos.

| Tipo | URI | Descripción |
| --------- | ----------- | ------- |   
| Web | web://domain.com/path/page.html | Representa una ruta de acceso y una página individuales de un sitio web. |
| Web | web://domain.com/path/page.html#element | Representa un elemento individual dentro de una página específica de un dominio específico. |
| Web | web://domain.com/*#element | Superficie comodín: representa un elemento individual en cada una de las páginas bajo un dominio específico. |
| Escritorio | desktop://com.vendor.bundle | Representa una aplicación de escritorio específica. |
| Escritorio | desktop://com.vendor.bundle#element | Representa un elemento específico dentro de una aplicación, como un botón, un menú, un banner a pantalla completa, etc. |
| Aplicación iOS | ios://com.vendor.bundle | Representa una aplicación móvil específica para una sola plataforma, en este caso una aplicación de iOS. |
| Aplicación iOS | ios://com.vendor.bundle/activity | Representa una actividad específica (vista) dentro de una aplicación móvil. |
| Aplicación iOS | ios://com.vendor.bundle/activity#element | Representa un elemento específico dentro de una actividad, como un botón u otro elemento de vista. |
| aplicación de Android | android://com.vendor.bundle | Representa una aplicación móvil específica para una sola plataforma, en este caso una aplicación de Android. |
| aplicación de tvOS | tvos://com.vendor.bundle | Representa una aplicación de tvOS específica. |
| aplicación de TV | tvcd://com.vendor.bundle | Representa una aplicación de dispositivo conectada a una TV inteligente o TV específica: ID de paquete. |
| Service | service://servicename | Representa un proceso del lado del servidor u otra entidad manual. |
| Quiosco | kiosk://location/screen | Ejemplo de posibles tipos de superficie adicionales que se pueden añadir fácilmente. |
| ATM | atm://location/screen | Ejemplo de posibles tipos de superficie adicionales que se pueden añadir fácilmente. |