---
title: Introducción para los desarrolladores
description: Obtenga más información sobre cómo trabajar con Journey Optimizer como desarrollador
feature: Get Started
role: Developer
level: Intermediate
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
TQID: https://experienceleague.adobe.com/7fRI-CPkIeBAPjtXmDgFdyNKgB4WwEc01yKrGUXnc3U
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: cf815079d67f4a41c3647c6a6e381ef5f1c44e51
workflow-type: tm+mt
source-wordcount: 3490
ht-degree: 53%

---

# Introducción para desarrolladores {#get-started-developers}

>[!BEGINSHADEBOX]

**En esta página:** Implemente los SDK, el flujo de eventos, los extremos de acciones personalizadas y las API que conectan sus aplicaciones a Adobe Journey Optimizer para que sus recorridos puedan ejecutarse en los datos activos.

>[!ENDSHADEBOX]

Como **desarrollador**, es responsable de implementar e integrar [!DNL Adobe Journey Optimizer] en sus aplicaciones y sistemas. Puede comenzar a trabajar con [!DNL Adobe Journey Optimizer] una vez que la variable [Administrador del sistema](administrator.md) e [Ingeniero de datos](data-engineer.md) le conceda acceso y prepare su entorno.

>[!NOTE]
>
>**Orden de implementación:** [Administrador](administrator.md) → [Ingeniero de datos](data-engineer.md) → Usted está aquí: **Desarrollador** → [Especialista en marketing](marketer.md)
>
>Asegúrese de que los [esquemas y eventos de datos](data-engineer.md) estén configurados antes de implementar las integraciones móviles y web.

## Su función en el ecosistema de Journey Optimizer

Mientras que otros integrantes del equipo configuran Journey Optimizer a través de la interfaz de usuario, usted se centrará en:

* **Implementación de SDK** en aplicaciones móviles y web
* **Envío de eventos** desde las aplicaciones para la activación de recorridos
* **Generación de puntos finales de API** a los que Journey Optimizer puede llamar mediante acciones personalizadas
* **Integración** de Journey Optimizer con sus sistemas e infraestructura existentes
* **Prueba y depuración** de sus implementaciones

Su [ingeniero de datos](data-engineer.md) se encargará de los esquemas de datos, las configuraciones de eventos y las fuentes de datos. Su [administrador](administrator.md) configurará permisos y configuraciones de canal. Los [expertos en marketing](marketer.md) diseñarán los recorridos y el contenido que usan sus implementaciones.

Esta guía describe los pasos esenciales de la implementación técnica para empezar a utilizar Journey Optimizer. Tanto si está creando aplicaciones móviles como experiencias web o integraciones de API, siga las secciones a continuación para configurar su implementación.

## Requisitos previos {#prerequisites}

Antes de iniciar la implementación, asegúrese de lo siguiente:

| Categoría | Requisitos |
|----------|-------------|
| **Aptitudes técnicas** | * Experiencia con JavaScript (para Web SDK) o Swift/Kotlin (para Mobile SDK)<br>* Comprensión de las API de RESTful y JSON<br>* Familiaridad con la programación asíncrona y las arquitecturas impulsadas por eventos<br>* Conocimiento de la arquitectura de aplicaciones de su organización |
| **Acceso y permisos** | * Acceso a [Adobe Developer Console](https://developer.adobe.com){target="_blank"} para credenciales de API<br>* Entorno de desarrollo con acceso al código base de su aplicación<br>* Herramientas de prueba como Postman para pruebas de API<br>* Herramientas para desarrolladores de explorador o herramientas de depuración móvil |
| **De otros integrantes del equipo** | * Acceso al entorno concedido por su [Administrador](administrator.md)<br>* Esquemas XDM y definiciones de eventos de su [Ingeniero de datos](data-engineer.md)<br>* Requisitos y casos de uso de sus [Expertos en marketing](marketer.md) |

## Comprender los fundamentos técnicos {#technical-foundation}

Antes de sumergirse en la implementación, familiarícese con los conceptos técnicos básicos:

1. **Integración de Adobe Experience Platform**: Journey Optimizer se ha creado de forma nativa en Adobe Experience Platform. Comprender la arquitectura subyacente le ayudará a crear implementaciones más efectivas. Más información sobre [cómo funciona Journey Optimizer](../understanding-ajo.md).

1. **Modelos de datos XDM**: Journey Optimizer utiliza el Modelo de datos de experiencia (XDM) para estructurar los datos de eventos y perfiles. Como desarrollador, tendrá que aprender cómo enviar datos que se ajusten a los esquemas configurados por su [ingeniero de datos](data-engineer.md). Más información acerca de los [esquemas XDM](../../data/get-started-schemas.md).

1. **Autenticación y seguridad**: todas las implementaciones requieren la autenticación adecuada. Obtenga información sobre cómo configurar la autenticación para SDK y API. Más información sobre la [autenticación de API](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}.

## Configurar las integraciones de la aplicación móvil {#mobile-integration}

### Configurar el SDK móvil de Adobe Experience Platform

Mobile SDK es una colección de bibliotecas que puede incrustar directamente en la aplicación de iOS o Android. Actúa como la capa de comunicación entre la aplicación y Adobe Experience Platform: identifica a los usuarios, recopila eventos de comportamiento y envía instrucciones desde Journey Optimizer, incluidas notificaciones push, mensajes en la aplicación y contenido personalizado. Sin ella, Journey Optimizer no tiene visibilidad de lo que están haciendo los usuarios de la aplicación ni forma de ponerse en contacto con ellos.

1. **Instale y configure Mobile SDK**: siga la [documentación del SDK móvil de Adobe Experience Platform](https://developer.adobe.com/client-sdks/documentation/getting-started){target="_blank"} para comenzar a usar la integración de SDK.

1. **Creación de una propiedad móvil**: configure una propiedad móvil en [!DNL Adobe Experience Platform Data Collection]. Aprenda a [crear y configurar una propiedad móvil](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property){target="_blank"}.

1. **Configuración de notificaciones push**:
   * Para **aplicaciones de iOS**: registre su aplicación con APNs (servicio de notificaciones push de Apple). Obtenga más información en la [documentación de Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Para **aplicaciones de Android**: configure Firebase Cloud Messaging para su aplicación de Android. Obtenga más información en la [Documentación de Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Pruebe su integración móvil**: Use el [flujo de trabajo de inicio rápido de la incorporación móvil](../../push/mobile-onboarding-wf.md) para configurar y probar rápidamente su configuración móvil.

Los pasos detallados para configurar las notificaciones push están disponibles en [esta página](../../push/push-configuration.md).

### Implementación de experiencias basadas en código (SDK móvil)

Las experiencias basadas en código le permiten ofrecer contenido personalizado a cualquier superficie de su aplicación móvil nativa, desde pantallas de incorporación y páginas de detalles de productos hasta banners y indicadores de funcionalidades en la aplicación, sin necesidad de realizar un nuevo lanzamiento de la aplicación. Utilice Mobile SDK para recuperar y procesar contenido personalizado en tiempo de ejecución, lo que permite a su equipo un control total de la ubicación y la presentación:

* Siga [este tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial){target="_blank"} para la implementación del SDK móvil
* Revise las implementaciones de muestra para [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} y [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Implementación de experiencias web {#web-implementation}

### Configuración del SDK web de Adobe Experience Platform

Web SDK (`alloy.js`) es una sola biblioteca de JavaScript que reemplaza el mosaico de etiquetas Adobe independientes que el sitio podría necesitar de otro modo. Recopila datos de comportamiento, los transmite a Adobe Experience Platform a través de un conjunto de datos que usted configura y recibe instrucciones de personalización de nuevo, todo en un solo recorrido de red. Una vez implementado, Journey Optimizer puede identificar visitantes, déclencheur recorridos de sus acciones y ofrecer contenido personalizado a sus páginas inmediatamente.

1. **Instale el SDK web**: siga la [guía de implementación del SDK web](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"} para configurar el SDK en su sitio web.

1. **Configure secuencias de datos**: cree y configure una secuencia de datos en [!DNL Adobe Experience Platform Data Collection] con Journey Optimizer habilitado. Obtenga más información en la [documentación de secuencias de datos](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=es){target="_blank"}.

1. **Habilitar notificaciones push web** (opcional): las notificaciones push web ya están disponibles de forma general. Configure la propiedad [pushNotifications](https://experienceleague.adobe.com/es/docs/experience-platform/collection/js/commands/configure/pushnotifications){target="_blank"} en la configuración de su SDK web y utilice el comando [sendPushSubscription](https://experienceleague.adobe.com/es/docs/experience-platform/collection/js/commands/sendpushsubscription){target="_blank"} para registrar suscripciones push. [Más información acerca de la configuración de las notificaciones push web](../../push/push-configuration-web.md).

### Implementar experiencias basadas en código (Web SDK)

A diferencia de los canales visuales, donde los especialistas en marketing controlan el diseño por completo, las experiencias basadas en código le proporcionan la propiedad total de cómo se procesa el contenido personalizado en la página. Journey Optimizer devuelve una carga útil JSON con los datos de personalización; su código decide dónde y cómo mostrarlo. Este modelo funciona para cualquier superficie web (banners de pantalla completa, carruseles de recomendaciones, clasificaciones de resultados de búsqueda y variantes de prueba A/B) sin necesidad de un editor visual o flujo de trabajo de publicación de página.

1. **Elija su método de implementación**: del lado del cliente, del lado del servidor o híbrido. Revise [ejemplos de implementación](../../code-based/code-based-implementation-samples.md) para cada enfoque.

1. **Defina superficies**: identifique las ubicaciones de la aplicación en las que desea enviar contenido personalizado. Más información sobre la [configuración de superficie](../../code-based/code-based-surface.md).

1. **Implemente el renderizado de contenido**: utilice el SDK web para recuperar y aplicar contenido de personalización. Vea [tutoriales de implementación basados en código](../../code-based/code-based-decisioning-implementations.md).

1. **Envío de eventos de visualización e interacción**: realice un seguimiento de cuándo se muestra el contenido y cuándo los usuarios interactúan con él para realizar análisis y optimización.

Explore [implementaciones de muestra en GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} para ver las experiencias basadas en código en acción.

Más información sobre [cómo empezar a usar las experiencias basadas en código](../../code-based/get-started-code-based.md).

## Implementación de streaming de eventos {#event-streaming}

### Envío de eventos para la activación de recorridos

Recorridos que se ejecutan en eventos: un usuario inicia sesión, agrega un elemento al carro de compras, completa una compra y abandona un formulario. Su trabajo consiste en emitir esos eventos desde su aplicación en el momento justo. Cada evento es una carga útil JSON estructurada por XDM enviada a la API de ingesta de transmisión de Experience Platform; Journey Optimizer la recoge en milisegundos y enruta el perfil a cualquier recorrido coincidente. El esquema de eventos y la estructura de carga útil están definidos por el [Ingeniero de datos](data-engineer.md), coordínelos antes de empezar a codificar.

1. **Conozca la carga útil del evento**: colabore con su ingeniero de datos para obtener el esquema de evento y la estructura de carga útil necesaria. La carga útil debe ajustarse al esquema XDM que él ha configurado. Obtenga información acerca de [requisitos de esquema de eventos](../../event/experience-event-schema.md).

1. **Implementar streaming de eventos**: envíe eventos a Adobe Experience Platform mediante las [API de ingesta de streaming](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=es){target="_blank"}. Conozca los [pasos para enviar eventos](../../event/additional-steps-to-send-events-to-journey.md).

1. **Gestión de tipos de eventos**:
   * **Eventos unitarios**: implemente el envío de eventos para acciones específicas de la persona (por ejemplo, clic en el botón, finalización de la compra).
   * **Eventos empresariales**: envíe eventos empresariales (por ejemplo, actualizaciones de inventario o cambios de precio)

1. **Envío de eventos de prueba**: compruebe que los eventos se reciben correctamente y que activan recorridos según lo esperado. Más información sobre la [solución de problemas de eventos](../../building-journeys/troubleshooting-inbound.md).

**Implementación de ejemplo** para enviar un evento a través de API:

```javascript
POST https://{DATACOLLECTION_ENDPOINT}/collection/{DATASTREAM_ID}
Content-Type: application/json

{
  "header": {
    "datasetId": "{DATASET_ID}",
    "imsOrgId": "{ORG_ID}",
    "source": {
      "name": "Web SDK"
    }
  },
  "body": {
    "xdmMeta": {
      "schemaRef": {
        "id": "{SCHEMA_ID}"
      }
    },
    "xdmEntity": {
      "_id": "unique-event-id",
      "eventType": "purchase",
      "timestamp": "2024-01-01T12:00:00Z",
      // ... your event data
    }
  }
}
```

Más información acerca de [cómo trabajar con eventos de recorrido](../../event/about-events.md).

## Desarrollar puntos finales de acción personalizados {#custom-actions}

Cuando un recorrido alcanza un paso de acción personalizada, Journey Optimizer realiza una llamada HTTP saliente a una dirección URL que proporcione: su back-end, un CRM, una plataforma de fidelidad, cualquier extremo REST. Su trabajo consiste en crear y exponer ese punto final: definir el contrato de solicitud (forma de carga útil, método de autenticación, formato de respuesta), implementar la lógica empresarial subyacente y asegurarse de que puede gestionar el volumen de llamada que generará Journey Optimizer. A continuación, [el administrador](administrator.md) registra el extremo en Journey Optimizer para que los especialistas en marketing puedan utilizarlo como un paso en sus recorridos.

1. **Cree su punto final de API**: cree puntos finales de API RESTful a los que Journey Optimizer llamará durante la ejecución del recorrido. Su punto final debe:
   * Aceptar cargas útiles JSON
   * Autenticar solicitudes (OAuth, clave de API o JWT)
   * Procesar solicitudes dentro de los límites de tiempo de espera adecuados
   * Devolver respuestas en el formato esperado

1. **Conozca las capacidades de acción personalizadas**: las acciones personalizadas pueden conectarse a sistemas de terceros como Epsilon, Slack, Firebase o a sus propios servicios. Más información sobre las [acciones personalizadas](../../action/action.md).

1. **Trabaje con configuraciones de acción**: Su [administrador](administrator.md) o [ingeniero de datos](data-engineer.md) configurará la acción personalizada en Journey Optimizer, definiendo la dirección URL del punto final de API, el método de autenticación y los parámetros. Les proporcionará su especificación de API. Obtenga información sobre la [configuración de acciones personalizadas](../../action/about-custom-action-configuration.md). Puede definir una **carga útil de respuesta de error** opcional para una lógica de reserva más completa en las ramas de tiempo de espera/error.

1. **Devolver datos procesables**: diseñe su API para devolver datos que se puedan usar en pasos de recorrido posteriores. Obtenga información acerca de [respuestas de acción](../../action/action-response.md).

1. **Supervisar el estado de las acciones personalizadas**: use el panel de supervisión de acciones personalizadas para rastrear las llamadas, los errores, el rendimiento, los tiempos de respuesta y los tiempos de espera de cola correctos. Obtenga información sobre la [creación informes de acciones personalizadas](../../action/reporting.md).

1. **Implemente limitación de velocidad**: asegúrese de que los puntos finales puedan asumir el volumen esperado. Journey Optimizer aplica un límite de 5000 llamadas/segundo, pero el sistema debe ser flexible. Obtenga información sobre [límite y regulación](../../configuration/external-systems.md).

**Ejemplo de caso de uso**: [escritura de eventos de recorrido en Experience Platform](../../building-journeys/custom-action-aep.md) mediante acciones personalizadas.

## Trabajo con las API de Journey Optimizer {#apis}

No es necesario que todo ocurra a través de la interfaz de usuario de Journey Optimizer. A veces, debe almacenar en déclencheur una campaña desde su propio servidor, suprimir una dirección de correo electrónico después de una solicitud de privacidad o sincronizar plantillas de contenido desde un CMS externo. Las API de REST de Journey Optimizer le proporcionan acceso mediante programación a las funciones principales de la plataforma. Todas las llamadas utilizan la autenticación de servidor a servidor OAuth (el método JWT más antiguo está obsoleto).

1. **Comprenda las capacidades de la API**: las API de Journey Optimizer le permiten crear, leer, actualizar y eliminar varios recursos mediante programación. Más información sobre las [API de Journey Optimizer](../../configuration/ajo-apis.md).

1. **Autenticación**: siga [este tutorial](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"} para configurar la autenticación de API mediante Adobe Developer Console.

1. **Explore referencias de API**: examine la documentación completa de la API y pruebe las API directamente en la [referencia de la API de Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}.

1. **Campañas activadas por API**: cree mensajería transaccional con campañas activadas por API. Para escenarios de gran volumen (hasta 5000 TPS), explore el [Modo de alto rendimiento](../../campaigns/api-triggered-high-throughput.md) (requiere licencia adicional).

1. **API de gestión de decisiones**: use API especializadas para la gestión y toma de decisiones de ofertas. Obtenga más información en la [Guía de API de gestión de decisiones](../../offers/api-reference/getting-started.md).

1. **API de migración de decisiones**: migre mediante programación las entidades de Gestión de decisiones a Toma de decisiones con ámbitos flexibles, validación automatizada y compatibilidad con reversiones. Obtenga más información en la [Guía de API de migración de toma de decisiones](../../experience-decisioning/decisioning-migration-api.md).

1. **Webhooks de SMS**: configure los webhooks entrantes para capturar los mensajes entrantes y los webhooks de comentarios para recibir confirmaciones de envío y actualizaciones de estado. [Más información](../../mobile/mobile-webhook.md).

## Pruebas y depuración {#testing}

Antes de que la implementación se ponga en marcha, debe confiar en que los eventos se activan en el momento adecuado, los recorridos entran en déclencheur según lo esperado, las acciones personalizadas se comportan bajo una carga realista y el contenido personalizado se procesa correctamente. Esta sección cubre las herramientas y técnicas para detectar problemas de forma temprana, desde el inicio de sesión de SDK de bajo nivel hasta las ejecuciones de pruebas de recorrido de extremo a extremo con perfiles reales.

1. **Implementación de SDK de depuración**: use Adobe Experience Platform Assurance para inspeccionar eventos de SDK, validar la recopilación de datos y solucionar problemas de integración a medida que ocurran. [Obtenga más información sobre Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=es){target="_blank"}.

1. **Envío de eventos de prueba**: verifique que los eventos de su aplicación son recibidos correctamente por Adobe Experience Platform y activan los recorridos según lo previsto. Monitorice la ingesta de eventos y valide la estructura de carga útil.

1. **Validar integraciones de API**: pruebe los puntos finales de acción personalizados para asegurarse de que administran correctamente las solicitudes de Journey Optimizer, responden dentro de los límites de tiempo de espera y devuelven los formatos de datos esperados.

1. **Use el modo de prueba con perfiles de prueba**: trabaje con su [ingeniero de datos](data-engineer.md) para obtener acceso a los perfiles de prueba y, a continuación, valide su implementación mediante el modo de prueba de recorrido. Aprenda a [probar recorridos](../../building-journeys/testing-the-journey.md).

1. **Supervise los registros de SDK**: habilite el registro de depuración en la implementación de SDK para solucionar problemas durante el desarrollo:
   * **SDK móvil**: habilite el registro para ver eventos de SDK y llamadas a la API
   * **Web SDK**: utilice la consola del explorador para supervisar la actividad de SDK

1. **Verifique la configuración de la secuencia de datos**: asegúrese de que la secuencia de datos esté configurada correctamente para enviar datos a Journey Optimizer. Compruebe que los eventos fluyen a través de la secuencia de datos hasta los destinos correctos.

1. **Consulte datos de recorrido para el análisis**: use consultas SQL en el lago de datos para analizar eventos de pasos de recorrido, depurar problemas y supervisar el rendimiento de acciones personalizadas. Explore [ejemplos de consultas para el análisis de recorrido](../../reports/query-examples.md), incluidos:
   * Razones de entrada/salida del perfil y de descarte
   * Métricas de rendimiento de acciones personalizadas (latencia, rendimiento, errores)
   * Envío de eventos y patrones de error
   * Estados de instancias de recorrido

## Temas avanzados para desarrolladores {#advanced-topics}

Una vez que los SDK, los eventos y las API principales están implementados, estos temas le ayudan a ir más allá: enriquecimiento de los datos de recorrido en tiempo de ejecución sin sobrecargar el perfil, administración de señales de consentimiento para que las exclusiones se propaguen a través de cada integración y ajuste de la implementación para el rendimiento y la fiabilidad que exige la escala de producción.

### Uso de datos contextuales y enriquecimiento

Los recorridos suelen necesitar más datos que los que llegan en el evento de activación: un nombre de producto, un nivel de lealtad y una lista de elementos de línea de pedido. En lugar de precargar todo esto en cada perfil, el enriquecimiento contextual permite que el recorrido lo busque en tiempo de ejecución desde conjuntos de datos de AEP o lo transfiera desde una respuesta de acción personalizada. Los mensajes y las condiciones de las ramas pueden hacer referencia a esos datos sin que se almacenen de forma permanente en el perfil.

* **Iterar en matrices**: use la sintaxis de Handlebars para mostrar listas dinámicas de eventos, respuestas de acciones personalizadas y búsquedas de conjuntos de datos en mensajes. Obtenga información acerca de [iteración de datos contextuales](../../personalization/iterate-contextual-data.md).
* **Búsqueda de conjuntos de datos**: implemente búsquedas de conjuntos de datos para enriquecer los datos de recorrido de los conjuntos de datos de Adobe Experience Platform. Trabaje con su ingeniero de datos en la configuración. Obtenga información acerca de [búsqueda de conjuntos de datos](../../building-journeys/dataset-lookup.md).

### Uso del consentimiento y la gobernanza

Journey Optimizer aplica las políticas de consentimiento y gobernanza de datos en el nivel de plataforma, pero la integración también debe respetarlas. Cuando un cliente decide excluirse de las comunicaciones de marketing o cuando una etiqueta de uso de datos restringe cómo se puede utilizar un campo, esas reglas deben propagarse a través de las acciones personalizadas y las búsquedas de conjuntos de datos, no solo bloquear las acciones en la interfaz de usuario.

* **Gobernanza de datos**: aplique directivas de uso de datos a las acciones personalizadas. Más información sobre la [gobernanza de los datos](../../action/action-privacy.md).
* **Gestión del consentimiento**: administre las preferencias de consentimiento del cliente en sus implementaciones. Más información sobre el [consentimiento](../../action/consent.md).

### Optimización y prácticas recomendadas

Las implementaciones de Production Journey Optimizer administran regularmente millones de eventos y miles de ejecuciones de recorrido por segundo. Estos recursos le ayudan a ajustar la integración para esa escala: comprenda los límites de tasa antes de alcanzarlos, evite los escollos comunes del diseño de recorridos que sueltan perfiles en silencio y genere un control de errores que se degrade correctamente en lugar de fallar en forma opaca.

* **Límites y regulación**: conozca los límites de velocidad e implemente una regulación adecuada. Más información sobre [sistemas externos](../../configuration/external-systems.md).
* **Optimización de recorrido**: siga las prácticas recomendadas para [optimización de recorrido](../../building-journeys/optimize.md).
* **Control de errores**: implemente un control de errores sólido. Revise los [códigos de error](../../building-journeys/error-codes-reference.md) y las [guías de solución de problemas](../../building-journeys/troubleshooting.md).

## Llamar a las API de REST de Journey Optimizer {#rest-apis}

Además de implementar los SDK y la transmisión de eventos, también puede dirigir Journey Optimizer mediante programación desde sus propios sistemas. La referencia de API completa, las especificaciones de OpenAPI y ejemplos de código se encuentran en [Journey Optimizer developer portal](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}.

>[!NOTE]
>
>Todas las integraciones deben utilizar la autenticación de servidor a servidor OAuth (el método JWT está obsoleto). [Configurar autenticación](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}

### Ejecución de campañas activadas por API {#api-triggered}

Almacene en déclencheur mensajes transaccionales o de marketing de un sistema externo mediante la API de REST de ejecución de mensajes interactivos. Antes de llamar al extremo:

* La campaña debe estar **activada** antes de que el extremo acepte llamadas.
* Las llamadas tienen un tiempo de espera de **de 60 segundos**; los reintentos internos controlan los tiempos de espera inesperados.
* Si se configuran las fechas de inicio y finalización de la campaña, las llamadas a la API fuera de esas fechas fallarán.
* Para crear su carga útil, recupere la solicitud cURL de ejemplo generada desde la sección **solicitud cURL** de su campaña en directo en la interfaz de usuario de Journey Optimizer; incluye todas las variables de personalización para esa campaña.
* Las [campañas estándar y de alto rendimiento](../../campaigns/api-triggered-high-throughput.md) usan puntos de conexión diferentes.

[Referencia de API](https://developer.adobe.com/journey-optimizer-apis/references/messaging){target="_blank"} · [Muestras de código](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples){target="_blank"} · [Trabajar con campañas activadas por API](../../campaigns/api-triggered-campaigns.md)

### Límite y restricción para extremos externos {#capping-throttling}

Cuando los recorridos llaman a sistemas externos mediante acciones personalizadas o fuentes de datos, las API de restricción y límite protegen esos sistemas de la sobrecarga. El límite rechaza las llamadas que superan el límite configurado; la restricción las pone en cola durante un máximo de 6 horas (solo zonas protegidas de producción y acciones personalizadas).

[Referencia de API de límite](https://developer.adobe.com/journey-optimizer-apis/references/journeys-throttling){target="_blank"} · [Trabajar con la API de límite](../../configuration/capping.md) · [Trabajar con la API de limitación](../../configuration/throttling.md)

### Más API de REST {#more-rest-apis}

Más allá de la mensajería y el límite, Journey Optimizer expone los puntos finales REST para la administración de supresión, la creación de plantillas de contenido, la recuperación de campañas, la revisión y la ejecución de campañas organizadas. Utilícelos cuando necesite automatizar operaciones que, de lo contrario, requerirían pasos manuales en la interfaz de usuario, como la supresión masiva de direcciones después de una extracción de datos o la sincronización de plantillas de una canalización de contenido externo.

| Lo que tiene que hacer | Referencia de la API |
| ------------------- | ------------- |
| Excluir direcciones de correo electrónico o dominios del envío mediante programación | [API de supresión](https://developer.adobe.com/journey-optimizer-apis/references/suppression){target="_blank"} · [Administrar la lista de supresión](../../configuration/manage-suppression-list.md) |
| Recuperar metadatos de recorrido para auditoría o sincronización externa | [API de Recorridos](https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve){target="_blank"} |
| Crear y administrar plantillas de contenido y fragmentos desde una canalización externa | [API de contenido](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"} · [Plantillas](../../content-management/content-templates.md) · [Fragmentos](../../content-management/fragments.md) |
| Recuperación y filtrado de campañas de acción | [API de campañas](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"} |
| Previsualización de campañas y envío de pruebas mediante programación | [API de simulaciones](https://developer.adobe.com/journey-optimizer-apis/references/simulations){target="_blank"} |

>[!NOTE]
>
>La API de simulaciones está disponible para campañas de acción (programadas) y activadas por API. No es **compatible con campañas orquestadas**: use en su lugar el flujo de trabajo de vista previa y prueba en la interfaz de usuario de campañas orquestadas para esas campañas.

| Validación de conjuntos de datos y ejecución de campañas organizadas por déclencheur | [Validación de conjuntos de datos](https://developer.adobe.com/journey-optimizer-apis/references/orchestrated-campaign-dataset){target="_blank"} · [Déclencheur](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} · [Habilitar conjuntos de datos](../../orchestrated/manual-schema.md) |

## Recursos adicionales {#additional-resources}

* **Developer Console**: acceda a [Adobe Developer Console](https://developer.adobe.com){target="_blank"} para crear integraciones y administrar credenciales de API.
* **Código de muestra**: explore [implementaciones de muestra en GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **Vídeos de tutorial**: aprenda con tutoriales prácticos en [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=es){target="_blank"}.
* **Comunidad de desarrolladores**: conéctese con otros desarrolladores y obtenga asistencia en los foros de la comunidad de Adobe.

## Colaboración entre funciones {#next-steps}

El trabajo de implementación se intersecta con otros integrantes del equipo:

>[!BEGINTABS]

>[!TAB Trabajo con ingenieros de datos]

Colabora con [ingenieros de datos](data-engineer.md) en configuraciones de datos y eventos. Cada recorrido que reacciona al comportamiento del usuario depende de los eventos que envía (el ingeniero de datos define los esquemas, implementa el código que los produce).

* Obtenga los [esquemas XDM](../../data/get-started-schemas.md) y las estructuras de evento que necesita implementar
* Comprenda qué eventos debe enviar y su formato de carga útil requerido. Consulte [Uso de eventos de recorrido](../../event/about-events.md)
* Confirme qué campos son obligatorios y cuáles son opcionales en cada carga útil de evento, y qué sucede en los recorridos cuando faltan campos esperados o tienen un formato incorrecto. Consulte [requisitos de esquema](../../event/experience-event-schema.md#schema-requirements)
* Probar la entrega de eventos y la ingesta de datos juntos usando [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=es){target="_blank"}

>[!TAB Trabaje con administradores]

Colaborar con [administradores](administrator.md) en las configuraciones de acceso y canal. Los recorridos solo pueden llegar a los usuarios a través de los canales que el administrador haya configurado. Coordínelos antes para que el trabajo de SDK y su configuración estén sincronizados.

* Proporcione especificaciones de API para [acciones personalizadas](../../action/about-custom-action-configuration.md) que configurarán en Journey Optimizer
* Solicite los permisos y credenciales de la API necesarios a través de [Adobe Developer Console](https://developer.adobe.com){target="_blank"}
* Coordine los requisitos de configuración de canal: certificados push para [iOS](../../push/push-configuration.md) y Android, configuración de [web push](../../push/push-configuration-web.md), extremos de [webhook de SMS](../../mobile/mobile-webhook.md)
* Alinee la estrategia de la zona protegida y los entornos de prueba antes de ejecutar el [modo de prueba de recorrido](../../building-journeys/testing-the-journey.md)

>[!TAB Trabaje con expertos en marketing]

Colaborar con [especialistas en mercadotecnia](marketer.md) en el diseño y las pruebas de recorrido. Los especialistas en marketing crean recorridos y contenido que dependen totalmente de los eventos que envía y de las superficies que expone; cuanto más cerca esté de alinear, más rápido se activarán los recorridos.

* Revise juntos los diseños de recorrido de [Journey Optimizer](../../building-journeys/journey.md) para comprender qué interacciones de usuario deben almacenar eventos en déclencheur y qué superficies necesitan personalización
* Implemente el seguimiento para que los especialistas en marketing puedan medir [el rendimiento del contenido y la participación del usuario](../../reports/report-gs-cja.md)
* Ejecute [modo de prueba de recorrido](../../building-journeys/testing-the-journey.md) juntos usando perfiles de prueba para validar el flujo completo de extremo a extremo
* Solucionar problemas con el envío de mensajes, la personalización o las respuestas de [acción personalizada](../../action/action.md)

>[!ENDTABS]

## Comenzar la implementación

¿Listo para comenzar a crear? Elija su primera área de implementación en las secciones anteriores:

1. **¿Aplicación móvil?** Comience con [integración de SDK móvil](#mobile-integration)
2. **¿Sitio web?** Comience con [Configuración de Web SDK](#web-implementation)
3. **¿Integración de API?** Vaya a [Trabajar con API](#apis)
4. **¿Sistema personalizado?** Consulte [Acciones personalizadas](#custom-actions)

Cada sección incluye vínculos a documentación técnica detallada, ejemplos de código y tutoriales que guiarán la implementación.

## Otras guías de funciones {#other-role-guides}

| Función | Guía |
|------|-------|
| Administrador | [Introducción para administradores](administrator.md) |
| Ingeniero de datos | [Introducción para ingenieros de datos](data-engineer.md) |
| Desarrollador | [Introducción para desarrolladores](developer.md) |
| Experto en marketing | [Introducción para expertos en marketing](marketer.md) |

Volver a [Resumen de funciones y responsabilidades](../quick-start.md) · Volver a [Introducción](../../../rp_landing_pages/get-started-landing-page.md)
