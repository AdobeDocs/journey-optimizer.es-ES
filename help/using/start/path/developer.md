---
title: Introducción para los desarrolladores
description: Obtenga más información sobre cómo trabajar con Journey Optimizer como desarrollador
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: 2d699fe8a3320400dad2d5d962028d6e2a5425f8
workflow-type: ht
source-wordcount: '1816'
ht-degree: 100%

---

# Introducción para los desarrolladores {#get-started-developers}

Como **desarrollador**, es responsable de implementar e integrar [!DNL Adobe Journey Optimizer] en sus aplicaciones y sistemas. Puede comenzar a trabajar con [!DNL Adobe Journey Optimizer] una vez que la variable [Administrador del sistema](administrator.md) e [Ingeniero de datos](data-engineer.md) le conceda acceso y prepare su entorno.

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

1. **Autenticación y seguridad**: todas las implementaciones requieren la autenticación adecuada. Obtenga información sobre cómo configurar la autenticación para SDK y API. Más información sobre la [autenticación de API](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

## Configurar las integraciones de la aplicación móvil {#mobile-integration}

### Configurar el SDK móvil de Adobe Experience Platform

Para habilitar las notificaciones push, los mensajes en la aplicación y otras funciones móviles, integre Adobe Experience Platform Mobile SDK en sus aplicaciones móviles.

1. **Instale y configure Mobile SDK**: siga la [documentación del SDK móvil de Adobe Experience Platform](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"} para comenzar a usar la integración de SDK.

1. **Creación de una propiedad móvil**: configure una propiedad móvil en [!DNL Adobe Experience Platform Data Collection]. Aprenda a [crear y configurar una propiedad móvil](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}.

1. **Configuración de notificaciones push**:
   * Para **aplicaciones de iOS**: registre su aplicación con APNs (servicio de notificaciones push de Apple). Obtenga más información en la [documentación de Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Para **aplicaciones de Android**: configure Firebase Cloud Messaging para su aplicación de Android. Obtenga más información en la [Documentación de Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Pruebe su integración móvil**: Use el [flujo de trabajo de inicio rápido de la incorporación móvil](../../push/mobile-onboarding-wf.md) para configurar y probar rápidamente su configuración móvil.

Los pasos detallados para configurar las notificaciones push están disponibles en [esta página](../../push/push-configuration.md).

### Implementación de experiencias basadas en código (SDK móvil)

Para la personalización nativa de aplicaciones móviles mediante experiencias basadas en código:

* Siga [este tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} para la implementación del SDK móvil
* Revise las implementaciones de muestra para [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} y [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Implementación de experiencias web {#web-implementation}

### Configuración del SDK web de Adobe Experience Platform

En implementaciones basadas en la web, el SDK web es el punto de integración principal:

1. **Instale el SDK web**: siga la [guía de implementación del SDK web](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"} para configurar el SDK en su sitio web.

1. **Configure secuencias de datos**: cree y configure una secuencia de datos en [!DNL Adobe Experience Platform Data Collection] con Journey Optimizer habilitado. Obtenga más información en la [documentación de secuencias de datos](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=es){target="_blank"}.

1. **Habilite notificaciones push en la web** (opcional): configure la [propiedad pushNotifications](https://experienceleague.adobe.com/es/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"} en la configuración de Web SDK y use el [comando sendPushSubscription](https://experienceleague.adobe.com/es/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} para registrar suscripciones push.

### Implementar experiencias basadas en código (Web SDK)

Las experiencias basadas en código le permiten personalizar cualquier punto de contacto digital:

1. **Elija su método de implementación**: del lado del cliente, del lado del servidor o híbrido. Revise [ejemplos de implementación](../../code-based/code-based-implementation-samples.md) para cada enfoque.

1. **Defina superficies**: identifique las ubicaciones de la aplicación en las que desea enviar contenido personalizado. Más información sobre la [configuración de superficie](../../code-based/code-based-surface.md).

1. **Implemente el renderizado de contenido**: utilice el SDK web para recuperar y aplicar contenido de personalización. Vea [tutoriales de implementación basados en código](../../code-based/code-based-decisioning-implementations.md).

1. **Envío de eventos de visualización e interacción**: realice un seguimiento de cuándo se muestra el contenido y cuándo los usuarios interactúan con él para realizar análisis y optimización.

Explore [implementaciones de muestra en GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} para ver las experiencias basadas en código en acción.

Más información sobre [cómo empezar a usar las experiencias basadas en código](../../code-based/get-started-code-based.md).

## Implementación de streaming de eventos {#event-streaming}

### Envío de eventos para la activación de recorridos

Como desarrollador, implementará el código para enviar eventos que activen los recorridos. Su [ingeniero de datos](data-engineer.md) configurará los esquemas y las definicionesde eventos en Journey Optimizer.

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

Las acciones personalizadas permiten que los recorridos llamen a sus API. Como desarrollador, creará los puntos finales de API que invocan las acciones personalizadas:

1. **Cree su punto final de API**: cree puntos finales de API RESTful a los que Journey Optimizer llamará durante la ejecución del recorrido. Su punto final debe:
   * Aceptar cargas útiles JSON
   * Autenticar solicitudes (OAuth, clave de API o JWT)
   * Procesar solicitudes dentro de los límites de tiempo de espera adecuados
   * Devolver respuestas en el formato esperado

1. **Conozca las capacidades de acción personalizadas**: las acciones personalizadas pueden conectarse a sistemas de terceros como Epsilon, Slack, Firebase o a sus propios servicios. Más información sobre las [acciones personalizadas](../../action/action.md).

1. **Trabaje con configuraciones de acción**: Su [administrador](administrator.md) o [ingeniero de datos](data-engineer.md) configurará la acción personalizada en Journey Optimizer, definiendo la dirección URL del punto final de API, el método de autenticación y los parámetros. Les proporcionará su especificación de API. Obtenga información sobre la [configuración de acciones personalizadas](../../action/about-custom-action-configuration.md).

1. **Devolver datos procesables**: diseñe su API para devolver datos que se puedan usar en pasos de recorrido posteriores. Obtenga información acerca de [respuestas de acción](../../action/action-response.md).

1. **Implemente limitación de velocidad**: asegúrese de que los puntos finales puedan asumir el volumen esperado. Journey Optimizer aplica un límite de 5000 llamadas/segundo, pero el sistema debe ser flexible. Obtenga información sobre [límite y regulación](../../configuration/external-systems.md).

**Ejemplo de caso de uso**: [escritura de eventos de recorrido en Experience Platform](../../building-journeys/custom-action-aep.md) mediante acciones personalizadas.

## Trabajo con las API de Journey Optimizer {#apis}

Journey Optimizer proporciona API de REST completas para el acceso mediante programación:

1. **Comprenda las capacidades de la API**: las API de Journey Optimizer le permiten crear, leer, actualizar y eliminar varios recursos mediante programación. Más información sobre las [API de Journey Optimizer](../../configuration/ajo-apis.md).

1. **Autenticación**: siga [este tutorial](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} para configurar la autenticación de API mediante Adobe Developer Console.

1. **Explore referencias de API**: examine la documentación completa de la API y pruebe las API directamente en la [referencia de la API de Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

1. **Campañas activadas por API**: cree mensajería transaccional con campañas activadas por API. Para escenarios de gran volumen (hasta 5000 TPS), explore el [Modo de alto rendimiento](../../campaigns/api-triggered-high-throughput.md) (requiere licencia adicional).

1. **API de gestión de decisiones**: use API especializadas para la gestión y toma de decisiones de ofertas. Obtenga más información en la [Guía de API de gestión de decisiones](../../offers/api-reference/getting-started.md).

## Pruebas y depuración {#testing}

1. **Implementación de SDK de depuración**: use Adobe Experience Platform Assurance para inspeccionar eventos de SDK, validar la recopilación de datos y solucionar problemas de integración en tiempo real. [Obtenga más información sobre Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=es){target="_blank"}.

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

### Uso de datos contextuales y enriquecimiento

* **Iterar en matrices**: use la sintaxis de Handlebars para mostrar listas dinámicas de eventos, respuestas de acciones personalizadas y búsquedas de conjuntos de datos en mensajes. Obtenga información acerca de [iteración de datos contextuales](../../personalization/iterate-contextual-data.md).
* **Búsqueda de conjuntos de datos**: implemente búsquedas de conjuntos de datos para enriquecer los datos de recorrido de los conjuntos de datos de Adobe Experience Platform. Trabaje con su ingeniero de datos en la configuración. Obtenga información acerca de [búsqueda de conjuntos de datos](../../building-journeys/dataset-lookup.md).

### Uso del consentimiento y la gobernanza

Implementación de políticas de gobernanza de datos y consentimiento en las integraciones:

* **Gobernanza de datos**: aplique directivas de uso de datos a las acciones personalizadas. Más información sobre la [gobernanza de los datos](../../action/action-privacy.md).
* **Gestión del consentimiento**: administre las preferencias de consentimiento del cliente en sus implementaciones. Más información sobre el [consentimiento](../../action/consent.md).

### Optimización y prácticas recomendadas

* **Límites y regulación**: conozca los límites de velocidad e implemente una regulación adecuada. Más información sobre [sistemas externos](../../configuration/external-systems.md).
* **Optimización de recorrido**: siga las prácticas recomendadas para [optimización de recorrido](../../building-journeys/optimize.md).
* **Control de errores**: implemente un control de errores sólido. Revise los [códigos de error](../../building-journeys/error-codes-reference.md) y las [guías de solución de problemas](../../building-journeys/troubleshooting.md).

## Recursos adicionales {#additional-resources}

* **Developer Console**: acceda a [Adobe Developer Console](https://developer.adobe.com){target="_blank"} para crear integraciones y administrar credenciales de API.
* **Código de muestra**: explore [implementaciones de muestra en GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **Vídeos de tutorial**: aprenda con tutoriales prácticos en [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=es){target="_blank"}.
* **Comunidad de desarrolladores**: conéctese con otros desarrolladores y obtenga asistencia en los foros de la comunidad de Adobe.

## Colaboración entre funciones {#next-steps}

El trabajo de implementación se intersecta con otros integrantes del equipo:

>[!BEGINTABS]

>[!TAB Trabajo con ingenieros de datos]

Colabore con [ingenieros de datos](data-engineer.md) en configuraciones de datos y eventos:

* Obtenga los esquemas XDM y las estructuras de eventos que necesita implementar
* Aprenda qué eventos debe enviar y su formato de carga útil requerido
* Alinee los requisitos de recopilación de datos y los estándares de calidad de datos
* Pruebe conjuntamente la entrega de eventos y la ingesta de datos

>[!TAB Trabaje con administradores]

Colabore con [administradores](administrator.md) en el acceso y las configuraciones:

* Proporcione especificaciones de API para las acciones personalizadas que configurarán
* Solicite los permisos y credenciales de API necesarios
* Coordine los requisitos de configuración de canal (por ejemplo, certificados push)
* Alinear en entornos de prueba y estrategia de zona protegida

>[!TAB Trabaje con expertos en marketing]

Colabore con [expertos en marketing](marketer.md) en los requisitos y pruebas de recorrido:

* Aprenda qué interacciones de usuario deben activar eventos
* Implementación del seguimiento para el rendimiento del contenido y la participación del usuario
* Prueba de compatibilidad de recorridos con las funciones implementadas
* Solución de problemas con el envío o la personalización de mensajes

>[!ENDTABS]

## Comenzar la implementación

¿Listo para comenzar a crear? Elija su primera área de implementación en las secciones anteriores:

1. **¿Aplicación móvil?** Comience con [integración de SDK móvil](#mobile-integration)
2. **¿Sitio web?** Comience con [Configuración de Web SDK](#web-implementation)
3. **¿Integración de API?** Vaya a [Trabajar con API](#apis)
4. **¿Sistema personalizado?** Consulte [Acciones personalizadas](#custom-actions)

Cada sección incluye vínculos a documentación técnica detallada, ejemplos de código y tutoriales que guiarán la implementación.
