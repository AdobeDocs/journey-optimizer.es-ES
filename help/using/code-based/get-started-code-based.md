---
title: Introducción a las experiencias basadas en código
description: Obtenga información sobre las experiencias basadas en código en Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: 4b822eb45857556359ba9444e9bf7379608f1dff
workflow-type: ht
source-wordcount: '719'
ht-degree: 100%

---

# Introducción al canal basado en código {#get-sarted-code-based}

[!DNL Journey Optimizer] le permite personalizar y probar las experiencias que desee ofrecer a sus clientes en todos sus puntos de contacto, como aplicaciones web, móviles y de escritorio, vídeoconsolas, servicios conectados al TV, televisores inteligentes, quioscos, cajeros automáticos, asistentes de voz, dispositivos IoT, etc.

Con la funcionalidad de la **experiencia basada en código** puede definir las experiencias entrantes mediante un editor no visual, sencillo e intuitivo. Permite insertar y editar elementos específicos en ubicaciones individuales y más granulares de sus aplicaciones o páginas web, independientemente del tipo de aplicaciones que tenga, en lugar de aplicar modificaciones a todo un contenido.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>Las protecciones específicas y las recomendaciones para experiencias basadas en código se detallan en [esta página](code-based-prerequisites.md).


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
<a href="code-based-prerequisites.md"><strong>Mecanismos de protección y limitaciones</strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="Poco frecuente" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong>Creación de una experiencia basada en código</strong></a>
</div>
<p></td>
<td>
<a href="code-based-implementation-samples.md">
<img alt="Validación" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong>Muestras de implementación</strong></a>
</div>
<p>
</td>
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

## Cuándo usar canales basados en código o en otros canales {#code-based-vs-other-channels}

### Canales basados en código o en otros canales

¿Cuándo utilizar el canal basado en código en lugar de otros canales de [!DNL Journey Optimizer]?

* Puede considerar la posibilidad de utilizar experiencias basadas en código siempre que no haya accedido a su propiedad digital a través de un explorador web o una aplicación móvil, casos en los que probablemente puede interesarle más utilizar el [canal web](../web/get-started-web.md){target="_blank"} de [!DNL Journey Optimizer] o el canal de [mensajería en la aplicación](../in-app/get-started-in-app.md){target="_blank"} de [!DNL Journey Optimizer].

* Puede utilizar el canal basado en código como alternativa al canal web de [!DNL Journey Optimizer] si no puede cargar su sitio web en el editor visual del [diseñador web](../web/web-visual-editor.md){target="_blank"} o si no puede usar la [extensión del explorador](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} que hace posible la creación visual para el canal web.

* También puede utilizar el canal basado en código como alternativa a los canales web o de la aplicación de [!DNL Journey Optimizer] en caso de que tenga una implementación basada en API, sin encabezado o del lado del servidor.

### Canal basado en código frente a canal web {#code-based-vs-web}

Para ejecutar casos de uso web, puede utilizar el canal web o la experiencia basada en código, pero según el contexto, una es más apropiada que la otra. Las principales diferencias se enumeran a continuación para que pueda tomar una decisión informada sobre qué utilizar y cuándo.

**Web**

* Edite el contenido utilizando el editor visual del [diseñador web](../web/web-visual-editor.md){target="_blank"}.
* Necesita la implementación de [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"} y la extensión [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} instalada en el explorador web. [Más información](../web/web-prerequisites.md){target="_blank"}
* El canal web permite modificar todo lo que hay en la página y tiene una lista predefinida de acciones que puede utilizar para realizar cambios. [Más información](../web/web-visual-editor.md){target="_blank"}
* Es fácil de configurar y poner en marcha rápidamente.
* Se centra en el experto en marketing.

**Experiencia basada en código**

* Edite el contenido utilizando el [editor de personalización](create-code-based.md#edit-code).
* La experiencia basada en código requiere un trabajo de desarrollo previo en la implementación para garantizar que las aplicaciones puedan interpretar y entregar el contenido publicado en el perímetro por [!DNL Journey Optimizer] para estas ubicaciones. [Más información](code-based-configuration.md#surface-definition)
* Requiere más planificación y solo puede cambiar las cosas que especifican los desarrolladores. Por lo tanto, es esencial identificar los componentes (banner principal, imagen principal, barra de menús, etc.) en las aplicaciones que deben modificarse para la personalización o para pruebas, y trabajar con el equipo de desarrollo para crear la implementación necesaria para gestionar estos cambios.
* Le permite utilizar contenido con código JSON.
* Se centra en el desarrollador.

## Funcionamiento {#how-it-works}

>[!CAUTION]
>
>Esta funcionalidad es para desarrolladores y/o usuarios experimentados. Puede ser utilizado por vendedores con algunas habilidades de escritura de código, siempre que las configuraciones de los canales y la configuración inicial corran a cargo de su equipo de desarrollo.

Para editar el contenido utilizando la funcionalidad de experiencia basada en código de [!DNL Journey Optimizer], sus páginas o aplicaciones deben estar instrumentadas. Para ello, debe declarar por adelantado las ubicaciones individuales específicas (denominadas “[superficies](code-based-configuration.md#surface-definition)”) donde desee insertar o reemplazar contenido.

>[!NOTE]
>
>Actualmente, el contenido asociado a una configuración solo puede ser HTML o JSON.

Los pasos clave para implementar una campaña basada en código se explican a continuación.

1. Defina una [superficie](code-based-configuration.md#surface-definition) en la implementación de su aplicación, que es básicamente la ubicación donde quiera añadir su experiencia basada en código, y crea una configuración de canal de experiencia basada en código que haga referencia a esa ubicación. [Descubra cómo](code-based-configuration.md#create-code-based-configuration)

1. Crea un recorrido o campaña en [!DNL Journey Optimizer] utilizando esta configuración. [Descubra cómo](create-code-based.md#create-code-based-campaign)

1. Componga una experiencia especificando contenido para la configuración seleccionada mediante el editor de personalización de [!DNL Journey Optimizer]. [Descubra cómo](create-code-based.md#edit-code)

1. El equipo de implementación de la aplicación realiza llamadas explícitas a la API o SDK para recuperar el contenido de las superficies con nombre, como “Texto del titular” o “Bandeja de recomendaciones 1”, o los puntos de decisión no relacionados con la interfaz de usuario en una aplicación, como, por ejemplo, los “parámetros de algoritmo de búsqueda”. En este caso, el equipo de implementación es responsable de procesar o interpretar de otra manera y actuar sobre el contenido devuelto. [Más información](code-based-implementation-samples.md)
