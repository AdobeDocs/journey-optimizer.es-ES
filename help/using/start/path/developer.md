---
title: Introducción para los desarrolladores
description: Obtenga más información sobre cómo trabajar con Journey Optimizer como desarrollador
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: ed3246d0bd552fee9c4df01babe18a5c1acd3b5f
workflow-type: tm+mt
source-wordcount: '1886'
ht-degree: 2%

---

# Introducción para los desarrolladores {#get-started-developers}

Como **desarrollador**, eres responsable de implementar e integrar [!DNL Adobe Journey Optimizer] en tus aplicaciones y sistemas. Puede comenzar a trabajar con [!DNL Adobe Journey Optimizer] una vez que el [Administrador del sistema](administrator.md) y el [Ingeniero de datos](data-engineer.md) le hayan concedido acceso y preparado su entorno.

## Su función en el ecosistema de Journey Optimizer

Mientras que otros integrantes del equipo configuran Journey Optimizer a través de la interfaz de usuario, usted se centrará en:

* **Implementación de SDK** en aplicaciones móviles y web
* **Envío de eventos** desde las aplicaciones a los recorridos de déclencheur
* **Creando extremos de API** a los que Journey Optimizer puede llamar mediante acciones personalizadas
* **Integrar** Journey Optimizer con sus sistemas e infraestructura existentes
* **Prueba y depuración** de sus implementaciones

Su [ingeniero de datos](data-engineer.md) se encargará de los esquemas de datos, las configuraciones de eventos y las fuentes de datos. Su [administrador](administrator.md) configurará permisos y configuraciones de canal. [Los especialistas en mercadotecnia](marketer.md) diseñarán los recorridos y el contenido que usan sus implementaciones.

Esta guía cubre los pasos esenciales de la implementación técnica para empezar a utilizar Journey Optimizer. Tanto si está creando aplicaciones móviles como experiencias web o integraciones de API, siga las secciones a continuación para configurar su implementación.

## Requisitos previos {#prerequisites}

Antes de iniciar la implementación, asegúrese de lo siguiente:

| Categoría | Requisitos |
|----------|-------------|
| **Aptitudes técnicas** | * Experiencia con JavaScript (para Web SDK) o Swift/Kotlin (para Mobile SDK)<br>* Comprensión de las API de RESTful y JSON<br>* Familiaridad con la programación asíncrona y las arquitecturas impulsadas por eventos<br>* Conocimiento de la arquitectura de aplicaciones de su organización |
| **Acceso y herramientas** | * Acceso a [Adobe Developer Console](https://developer.adobe.com){target="_blank"} para credenciales de API<br>* Entorno de desarrollo con acceso al código base de su aplicación<br>* Herramientas de prueba como Postman para pruebas de API<br>* Herramientas para desarrolladores de explorador o herramientas de depuración móvil |
| **De otros integrantes del equipo** | * Acceso al entorno concedido por su [Administrador](administrator.md)<br>* esquemas XDM y definiciones de evento de sus [Requisitos y casos de uso del Ingeniero de datos](data-engineer.md)<br>* de sus [Especialistas en marketing](marketer.md) |

## Comprender la base técnica {#technical-foundation}

Antes de sumergirse en la implementación, familiarícese con los conceptos técnicos principales:

1. **Integración de Adobe Experience Platform**: Journey Optimizer se ha creado de forma nativa en Adobe Experience Platform. Comprender la arquitectura subyacente le ayudará a crear implementaciones más efectivas. Más información sobre [cómo funciona Journey Optimizer](../understanding-ajo.md).

1. **Modelos de datos XDM**: Journey Optimizer utiliza el Modelo de datos de experiencia (XDM) para estructurar los datos de eventos y perfiles. Como desarrollador, tendrás que entender cómo enviar datos que se ajusten a los esquemas configurados por tu [ingeniero de datos](data-engineer.md). Obtenga información sobre [esquemas XDM](../../data/get-started-schemas.md).

1. **Autenticación y seguridad**: todas las implementaciones requieren la autenticación adecuada. Obtenga información sobre cómo configurar la autenticación para SDK y API. Más información sobre la [autenticación de API](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

## Configuración de integraciones de aplicaciones móviles {#mobile-integration}

### Configuración de Adobe Experience Platform Mobile SDK

Para habilitar las notificaciones push, los mensajes en la aplicación y otras funciones móviles, integre Adobe Experience Platform Mobile SDK en sus aplicaciones móviles.

1. **Instale y configure Mobile SDK**: Siga la [documentación de Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"} para comenzar a usar la integración con SDK.

1. **Crear una propiedad móvil**: Configure una propiedad móvil en [!DNL Adobe Experience Platform Data Collection]. Aprenda a [crear y configurar una propiedad móvil](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}.

1. **Configurar notificaciones push**:
   * Para **aplicaciones de iOS**: registre su aplicación con APNS (servicio de notificaciones push de Apple). Obtenga más información en [Documentación de Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Para **aplicaciones de Android**: configure Firebase Cloud Messaging para su aplicación de Android. Obtenga más información en [Documentación de Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Pruebe su integración móvil**: Use el [flujo de trabajo de inicio rápido de la incorporación móvil](../../push/mobile-onboarding-wf.md) para configurar y probar rápidamente su configuración móvil.

Los pasos detallados para configurar las notificaciones push están disponibles en [esta página](../../push/push-configuration.md).

### Implementación de experiencias basadas en código (Mobile SDK)

Para la personalización nativa de aplicaciones móviles mediante experiencias basadas en código:

* Seguir [este tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} para la implementación de Mobile SDK
* Revise las implementaciones de muestra para [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} y [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Implementación de experiencias web {#web-implementation}

### Configuración de Adobe Experience Platform Web SDK

En implementaciones basadas en la web, Web SDK es el punto de integración principal:

1. **Instale Web SDK**: Siga la [guía de implementación de Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"} para configurar SDK en su sitio web.

1. **Configurar flujos de datos**: cree y configure un flujo de datos en [!DNL Adobe Experience Platform Data Collection] con Journey Optimizer habilitado. Obtenga más información en la [documentación de flujos de datos](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=es){target="_blank"}.

1. **Habilitar notificaciones push en la web** (opcional): configure la [propiedad pushNotifications](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"} en la configuración de Web SDK y use el [comando sendPushSubscription](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} para registrar suscripciones push.

### Implementar experiencias basadas en código (Web SDK)

Las experiencias basadas en código le permiten personalizar cualquier punto de contacto digital:

1. **Elija su método de implementación**: del lado del cliente, del lado del servidor o híbrido. Revise [ejemplos de implementación](../../code-based/code-based-implementation-samples.md) para cada enfoque.

1. **Definir superficies**: identifique las ubicaciones de la aplicación en las que desea enviar contenido personalizado. Obtenga información acerca de [configuración de superficie](../../code-based/code-based-surface.md).

1. **Implementar la representación de contenido**: Utilice Web SDK para recuperar y aplicar contenido de personalización. Ver [tutoriales de implementación basados en código](../../code-based/code-based-decisioning-implementations.md).

1. **Enviar eventos de visualización e interacción**: realiza un seguimiento de cuándo se muestra el contenido y cuándo los usuarios interactúan con él para realizar análisis y optimización.

Explore [implementaciones de muestra en GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} para ver las experiencias basadas en código en acción.

Más información sobre [cómo empezar a usar las experiencias basadas en código](../../code-based/get-started-code-based.md).

## Implementación de flujo de eventos {#event-streaming}

### Envío de eventos a los recorridos de déclencheur

Como desarrollador, implementará el código para enviar eventos que almacenen en déclencheur los recorridos. Su [ingeniero de datos](data-engineer.md) configurará los esquemas de eventos y las definiciones en Journey Optimizer.

1. **Comprenda la carga útil del evento**: Colabore con su ingeniero de datos para obtener el esquema de evento y la estructura de carga útil necesaria. La carga útil debe ajustarse al esquema XDM que han configurado. Obtenga información acerca de [requisitos de esquema de eventos](../../event/experience-event-schema.md).

1. **Implementar flujo de eventos**: Envíe eventos a Adobe Experience Platform mediante las [API de ingesta de transmisión](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=es){target="_blank"}. Conozca los [pasos para enviar eventos](../../event/additional-steps-to-send-events-to-journey.md).

1. **Controlar tipos de eventos**:
   * **Eventos unitarios**: Implemente el envío de eventos para acciones específicas de la persona (por ejemplo, clic en el botón, finalización de la compra).
   * **Eventos empresariales**: envía eventos empresariales (por ejemplo, actualizaciones de inventario o cambios de precio)

1. **Envío de eventos de prueba**: compruebe que los eventos se reciben correctamente y que los recorridos de déclencheur son los esperados. Obtenga información acerca de [solución de problemas de eventos](../../building-journeys/troubleshooting-inbound.md).

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

## Desarrollar extremos de acción personalizados {#custom-actions}

Las acciones personalizadas permiten que los recorridos llamen a sus API. Como desarrollador, creará los puntos finales de API que invocan las acciones personalizadas:

1. **Cree su extremo de API**: cree extremos de API RESTful a los que Journey Optimizer llamará durante la ejecución del recorrido. Su punto final debe:
   * Aceptar cargas JSON
   * Autenticar solicitudes (OAuth, clave de API o JWT)
   * Procesar solicitudes dentro de los límites de tiempo de espera adecuados
   * Devolver respuestas en el formato esperado

1. **Comprenda las capacidades de acción personalizadas**: las acciones personalizadas pueden conectarse a sistemas de terceros como Epsilon, Slack, Firebase o a sus propios servicios. Más información sobre las [acciones personalizadas](../../action/action.md).

1. **Trabaje con configuraciones de acción**: Su [administrador](administrator.md) o [ingeniero de datos](data-engineer.md) configurará la acción personalizada en Journey Optimizer, definiendo la dirección URL del extremo de API, el método de autenticación y los parámetros. Les proporcionará su especificación de API. Obtenga información acerca de [configuración de acción personalizada](../../action/about-custom-action-configuration.md).

1. **Devolver datos procesables**: diseñe su API para devolver datos que se puedan usar en pasos de recorrido posteriores. Obtenga información acerca de [respuestas de acción](../../action/action-response.md).

1. **Implementar limitación de velocidad**: Asegúrese de que los extremos puedan controlar el volumen esperado. Journey Optimizer aplica un límite de 5000 llamadas/segundo, pero el sistema debe ser flexible. Obtenga información sobre [límite y regulación](../../configuration/external-systems.md).

**Ejemplo de caso de uso**: [Escritura de eventos de recorrido en Experience Platform](../../building-journeys/custom-action-aep.md) mediante acciones personalizadas.

## Trabajo con las API de Journey Optimizer {#apis}

Journey Optimizer proporciona API de REST completas para el acceso mediante programación:

1. **Comprender las capacidades de la API**: las API de Journey Optimizer le permiten crear, leer, actualizar y eliminar varios recursos mediante programación. Más información sobre [las API de Journey Optimizer](../../configuration/ajo-apis.md).

1. **Autenticación**: siga [este tutorial](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} para configurar la autenticación de API mediante Adobe Developer Console.

1. **Explorar referencias de API**: Examine la documentación completa de la API y pruebe las API directamente en la [referencia de la API de Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

1. **Campañas activadas por API**: cree mensajes transaccionales con campañas activadas por API. Para escenarios de gran volumen (hasta 5000 TPS), explore [Modo de alto rendimiento](../../campaigns/api-triggered-high-throughput.md) (requiere licencia adicional).

1. **API de administración de decisiones**: use API especializadas para la administración y toma de decisiones de ofertas. Obtenga más información en la [Guía de API de administración de decisiones](../../offers/api-reference/getting-started.md).

## Pruebas y depuración {#testing}

1. **Implementación de Debug SDK**: Use Adobe Experience Platform Assurance para inspeccionar eventos de SDK, validar la recopilación de datos y solucionar problemas de integración en tiempo real. [Más información sobre Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html){target="_blank"}.

1. **Envío de eventos de prueba**: compruebe que Adobe Experience Platform y los recorridos de déclencheur reciben correctamente los eventos de su aplicación según lo esperado. Monitorice la ingesta de eventos y valide la estructura de carga útil.

1. **Validar integraciones de API**: pruebe los extremos de acción personalizados para asegurarse de que administran correctamente las solicitudes de Journey Optimizer, responden dentro de los límites de tiempo de espera y devuelven los formatos de datos esperados.

1. **Use el modo de prueba con perfiles de prueba**: trabaje con su [ingeniero de datos](data-engineer.md) para obtener acceso a los perfiles de prueba y, a continuación, valide su implementación mediante el modo de prueba de recorrido. Aprenda a [probar recorridos](../../building-journeys/testing-the-journey.md).

1. **Supervisar los registros de SDK**: habilite el registro de depuración en la implementación de SDK para solucionar problemas durante el desarrollo:
   * **SDK móvil**: Habilite el registro para ver eventos de SDK y llamadas a la API
   * **Web SDK**: utilice la consola del explorador para supervisar la actividad de SDK

1. **Verificar configuración del flujo de datos**: Asegúrese de que el flujo de datos esté configurado correctamente para enviar datos a Journey Optimizer. Compruebe que los eventos fluyen por el flujo de datos hasta los destinos correctos.

1. **Consultar datos de recorrido para el análisis**: use consultas SQL en el lago de datos para analizar eventos de pasos de recorrido, depurar problemas y supervisar el rendimiento de acciones personalizadas. Explorar [ejemplos de consultas para el análisis de recorrido](../../reports/query-examples.md), incluidos:
   * Razones de entrada/salida del perfil y de descarte
   * Métricas de rendimiento de acciones personalizadas (latencia, rendimiento, errores)
   * Entrega de eventos y patrones de error
   * estados de instancias de recorrido

## Temas avanzados para desarrolladores {#advanced-topics}

### Uso de datos contextuales y enriquecimiento

* **Iterar en matrices**: use la sintaxis de Handlebars para mostrar listas dinámicas de eventos, respuestas de acciones personalizadas y búsquedas de conjuntos de datos en mensajes. Obtenga información acerca de [repetir datos contextuales](../../personalization/iterate-contextual-data.md).
* **Búsqueda de conjuntos de datos**: Implemente búsquedas de conjuntos de datos para enriquecer los datos de recorrido de los conjuntos de datos de Adobe Experience Platform. Trabaje con su ingeniero de datos en la configuración. Obtenga información acerca de [búsqueda de conjuntos de datos](../../building-journeys/dataset-lookup.md).

### Uso del consentimiento y la gobernanza

Implementar políticas de gobernanza de datos y consentimiento en las integraciones:

* **Gobernanza de datos**: aplique directivas de uso de datos a las acciones personalizadas. Más información sobre [gobernanza de datos](../../action/action-privacy.md).
* **Administración de consentimiento**: Administre las preferencias de consentimiento del cliente en sus implementaciones. Más información sobre [consentimiento](../../action/consent.md).

### Optimización y prácticas recomendadas

* **Límite y regulación**: Comprenda los límites de velocidad e implemente un límite adecuado. Más información sobre [sistemas externos](../../configuration/external-systems.md).
* **Optimización de Recorrido**: siga las prácticas recomendadas para [Optimización de recorrido](../../building-journeys/optimize.md).
* **Control de errores**: Implemente un control de errores sólido. Revise [códigos de error](../../building-journeys/error-codes-reference.md) y [guías de solución de problemas](../../building-journeys/troubleshooting.md).

## Recursos adicionales {#additional-resources}

* **Developer Console**: accede a [Adobe Developer Console](https://developer.adobe.com){target="_blank"} para crear integraciones y administrar credenciales de API.
* **Código de muestra**: explore [implementaciones de muestra en GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **Vídeos de tutorial**: Aprenda con tutoriales prácticos en [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=es){target="_blank"}.
* **Comunidad de desarrolladores**: conéctese con otros desarrolladores y obtenga asistencia en los foros de la comunidad de Adobe.

## Colaboración entre funciones {#next-steps}

El trabajo de implementación se intersecta con otros integrantes del equipo:

>[!BEGINTABS]

>[!TAB Trabajar con ingenieros de datos]

Colaborar con [ingenieros de datos](data-engineer.md) en configuraciones de datos y eventos:

* Obtenga los esquemas XDM y las estructuras de eventos que necesita implementar
* Comprender qué eventos debe enviar y su formato de carga útil requerido
* Alinee los requisitos de recopilación de datos y los estándares de calidad de datos
* Prueba conjunta de la entrega de eventos y la ingesta de datos

>[!TAB Trabajar con administradores]

Colaborar con [administradores](administrator.md) en el acceso y las configuraciones:

* Proporcionar especificaciones de API para las acciones personalizadas que configurarán
* Solicite los permisos y credenciales de API necesarios
* Coordinar los requisitos de configuración de canal (por ejemplo, certificados push)
* Alinear en entornos de prueba y estrategia de zona protegida

>[!TAB Trabajar con especialistas en mercadotecnia]

Colaborar con [especialistas en mercadotecnia](marketer.md) en los requisitos y pruebas de recorrido:

* Comprender qué interacciones de usuario deben almacenar eventos en déclencheur
* Implementar el seguimiento para el rendimiento del contenido y la participación del usuario
* Prueba de compatibilidad de recorridos con las funciones implementadas
* Solución de problemas con el envío o la personalización de mensajes

>[!ENDTABS]

## Manténgase al día

Manténgase al tanto de las últimas funciones y cambios técnicos de Journey Optimizer:

* **[Notas de la versión](../../rn/release-notes.md)**: revise las nuevas características, los cambios de la API, las actualizaciones de SDK y las correcciones de errores publicadas todos los meses
* **[Actualizaciones de documentación](../../rn/documentation-updates.md)**: efectúe el seguimiento de los cambios recientes en la documentación técnica, incluidas las nuevas guías de implementación y los ejemplos de código
* **[Notificaciones de productos](../../rn/releases.md#staying-informed)**: Obtenga información sobre cómo suscribirse a alertas por correo electrónico y en el producto para actualizaciones de Journey Optimizer, incluidas nuevas versiones de SDK, cambios de API, cambios importantes y actualizaciones críticas de seguridad

## Comenzar implementación

¿Listo para empezar a construir? Elija su primera área de implementación en las secciones anteriores:

1. ¿Aplicación móvil **?** comienza con [integración de SDK móvil](#mobile-integration)
2. ¿Sitio web de **?** Comience con [Configuración de Web SDK](#web-implementation)
3. ¿Integración de API **?** Ir a [Trabajar con API](#apis)
4. **¿Sistema personalizado?** Desproteger [acciones personalizadas](#custom-actions)

Cada sección incluye vínculos a documentación técnica detallada, ejemplos de código y tutoriales que guiarán la implementación.
