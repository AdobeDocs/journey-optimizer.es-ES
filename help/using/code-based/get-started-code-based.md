---
title: Introducción a las experiencias basadas en código
description: Obtenga información sobre las experiencias basadas en código en Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: 4d7ad2c3ed71801298f1afe31d0e29d7bb1d5c7f
workflow-type: ht
source-wordcount: '771'
ht-degree: 100%

---

# Introducción al canal basado en código {#get-sarted-code-based}

[!DNL Journey Optimizer] le permite personalizar y probar las experiencias que desee ofrecer a sus clientes en todos sus puntos de contacto, como aplicaciones web, móviles y de escritorio, vídeoconsolas, servicios conectados al TV, televisores inteligentes, quioscos, cajeros automáticos, asistentes de voz, dispositivos IoT, etc.

Con la funcionalidad de la **experiencia basada en código** puede definir las experiencias entrantes mediante un editor no visual, sencillo e intuitivo. Permite insertar y editar elementos específicos en ubicaciones individuales y más granulares de sus aplicaciones o páginas web, independientemente del tipo de aplicaciones que tenga, en lugar de aplicar modificaciones a todo un contenido.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>Las recomendaciones específicas para las experiencias basadas en código se detallan en [esta página](code-based-prerequisites.md).


<!--Discover the detailed steps to create a code-based campaign in this video.-->

<!--[Learn how to create a code-based campaign in this video](#video)-->

➡️ En [esta sección](../experience-decisioning/experience-decisioning-uc.md) se presenta un caso de uso de extremo a extremo que muestra cómo usar experimentos de contenido para comparar las decisiones con el canal de experiencia basado en código.

## Cuándo usar canales basados en código o en otros canales {#code-based-vs-other-channels}

### Canales basados en código o en otros canales

¿Cuándo utilizar el canal basado en código en lugar de otros canales de [!DNL Journey Optimizer]?

* Puede considerar la posibilidad de utilizar experiencias basadas en código siempre que no haya accedido a su propiedad digital a través de un explorador web o una aplicación móvil, casos en los que probablemente puede interesarle más utilizar el [canal web](../web/get-started-web.md){target="_blank"} de [!DNL Journey Optimizer] o el canal de [mensajería en la aplicación](../../rp_landing_pages/in-app-landing-page.md){target="_blank"} de [!DNL Journey Optimizer].

<!--* You can use the code-based channel as an alternative to the [!DNL Journey Optimizer] web channel if your website cannot be loaded into the [web designer](../web/web-visual-editor.md){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} that powers visual authoring for web channel.-->

* También puede utilizar el canal basado en código como alternativa a los canales web o en la aplicación de [!DNL Journey Optimizer] en caso de que tenga una implementación basada en API, sin encabezado o del lado del servidor.

* También puede aprovechar el canal basado en código en aplicaciones móviles nativas como alternativa al canal en la aplicación si desea modificar el contenido dentro de la aplicación nativa en lugar de mostrar modelos, ventanas emergentes o superposiciones.

### Canal basado en código frente a canal web {#code-based-vs-web}

Para ejecutar casos de uso web, puede utilizar el canal web o la experiencia basada en código, pero según el contexto, una es más apropiada que la otra. Las principales diferencias se enumeran a continuación para que pueda tomar una decisión bien fundada sobre qué utilizar y cuándo.

**Web**

* Edite el contenido con el editor visual del [diseñador web](../web/web-visual-editor.md){target="_blank"} o el [editor no visual](../web/web-non-visual-editor.md) web.
* Necesita el [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"}, una implementación del lado del cliente.
  <!--* You need the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}-->
* El canal web permite modificar todo lo que hay en la página y tiene una lista predefinida de acciones que puede utilizar para realizar cambios. [Más información](../web/web-visual-editor.md){target="_blank"}
* Es fácil de configurar y poner en marcha rápidamente.
* Se centra en el experto en marketing.

**Experiencia basada en código**

* Edite el contenido utilizando el [editor de personalización](create-code-based.md#edit-code).
* Necesita el [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"}, una implementación del lado del cliente, o la [API del servidor Edge Network de AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=es){target="_blank"}, una implementación del lado del servidor.
* La experiencia basada en código requiere un trabajo de desarrollo previo en la implementación para garantizar que las aplicaciones puedan interpretar y entregar el contenido publicado en el perímetro por [!DNL Journey Optimizer] para estas ubicaciones. [Más información](code-based-surface.md)
* Requiere más planificación y solo puede cambiar las cosas que especifican los desarrolladores. Por lo tanto, es esencial identificar los componentes (banner principal, imagen principal, barra de menús, etc.) en las aplicaciones que deben modificarse para la personalización o para pruebas, y trabajar con el equipo de desarrollo para crear la implementación necesaria para gestionar estos cambios.
* Le permite utilizar contenido con código JSON.
* Se centra en el desarrollador.

## Funcionamiento {#how-it-works}

>[!CAUTION]
>
>Esta funcionalidad es para desarrolladores y/o usuarios experimentados. Puede ser utilizado por vendedores con algunas habilidades de escritura de código, siempre que las configuraciones de los canales y la configuración inicial corran a cargo de su equipo de desarrollo.

Para editar el contenido utilizando la funcionalidad de experiencia basada en código de [!DNL Journey Optimizer], sus páginas o aplicaciones deben estar instrumentadas. Para ello, debe declarar por adelantado las ubicaciones individuales específicas (denominadas “[superficies](code-based-surface.md)”) donde desee insertar o reemplazar contenido.

>[!NOTE]
>
>Actualmente, el contenido asociado a una configuración solo puede ser HTML o JSON.

Los pasos clave para crear y ofrecer una experiencia basada en código se indican a continuación.

1. Asegúrese de seguir los requisitos previos específicos del canal. [Más información](code-based-prerequisites.md)

1. Defina una [superficie](code-based-surface.md#surface-definition) en la implementación de su aplicación, que básicamente es la ubicación donde desea añadir su experiencia.

1. Cree una configuración de canal basada en código que haga referencia a esa ubicación. [Descubra cómo](code-based-configuration.md#create-code-based-configuration)

1. Crea un recorrido o campaña en [!DNL Journey Optimizer] utilizando esta configuración. [Descubra cómo](create-code-based.md#create-code-based-campaign)

1. Componga una experiencia especificando contenido para la configuración seleccionada mediante el editor de personalización de [!DNL Journey Optimizer]. [Descubra cómo](create-code-based.md#edit-code)

1. Pruebe la experiencia basada en código. [Descubra cómo](test-code-based.md)

1. Publíquela. [Descubra cómo](publish-code-based.md)

1. Cuando su campaña o el recorrido de experiencias basadas en código estén activos, la implementación de la aplicación o página que solicita contenido para la superficie tiene que estar lista para poder recuperar y mostrar el contenido. 

   >[!INFO]
   >
   >Para garantizarlo, el equipo de implementación de la aplicación realiza llamadas explícitas a la API o al SDK para recuperar el contenido de la superficie definida en la configuración basada en código, como “Texto del titular” o “Bandeja de recomendaciones 1”, o puntos de decisión no relacionados con la interfaz de usuario de una aplicación, como, por ejemplo, los “parámetros de algoritmo de búsqueda”. <!--In this case, the implementation team is responsible for rendering or otherwise interpreting and acting on the returned content.--> [Más información](code-based-implementation-samples.md)

