---
solution: Journey Optimizer
product: journey optimizer
title: Solucionar problemas de actividades activas
description: Obtenga información sobre cómo solucionar problemas de actividades en directo en Journey Optimizer para casos de uso unitarios y de difusión, incluidos problemas de token de perfil, configuración de campaña y errores de entrega
role: User
level: Intermediate
exl-id: f0f83bd2-7c2b-4d9b-b455-e1df12dfa175
source-git-commit: 016d905840a3ccc05ca1d2a934130b53c1108e7c
workflow-type: tm+mt
source-wordcount: '4503'
ht-degree: 1%

---

# Solucionar problemas de actividades activas {#troubleshoot-mobile-live}

Las actividades en directo en Adobe Journey Optimizer permiten actualizaciones dinámicas en tiempo real en las pantallas de bloqueo de iOS y en las islas dinámicas. Solo se pueden activar y administrar mediante campañas activadas por API.

**Tipos de casos de uso:**

* **Unitario**: segmentado individualmente, transaccional (campañas transaccionales activadas por API)
* **Difusión**: Entrega en masa dirigida a audiencias (campañas de marketing activadas por API)

Un desafío frecuente con las actividades en directo es cuando la llamada de la API para almacenar en déclencheur o actualizar una actividad en directo devuelve una **respuesta correcta (200 OK)**, pero la actividad en directo no aparece ni se actualiza en el dispositivo del usuario. Esta desconexión entre la confirmación de la API y el comportamiento real del dispositivo se puede producir en varios puntos de la canalización de envíos. Esta guía proporciona un enfoque sistemático de solución de problemas para identificar dónde falla el envío, y examina cada fase desde la validación de la solicitud de API hasta el procesamiento del dispositivo.

## Requisitos previos

Antes de efectuar la localización de averías, asegúrese de que dispone de:

* &#x200B;
  +++ Configuración de una sesión de Assurance

  Configure una **sesión de Assurance** para capturar eventos de SDK e inspeccionar la canalización de envíos. Assurance proporciona visibilidad sobre:

   * Solicitudes y respuestas de Edge Network
   * Eventos de calificación de perfiles
   * Registro de token push
   * Eventos de ciclo vital de actividad activos

  Aprenda a configurar Assurance en la [documentación de Adobe Experience Platform Assurance](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance).

  **Nota**: Para la actividad de iOS Live, asegúrate de que la aplicación se esté ejecutando en un dispositivo iOS físico (iOS 16.1 o posterior) o en un simulador Xcode (iOS 16.1 o posterior).

  +++

* &#x200B;
  +++ Recopilar detalles de la campaña activada por API

  Vaya a la API de la campaña activada en Journey Optimizer y recupere lo siguiente:

   * Nombre de la campaña
   * ID de campaña encontrado en la URL o en las propiedades de la campaña
   * Versión de la campaña si corresponde
   * Configuración de superficie, superficie de la aplicación de iOS utilizada para la actividad en directo

  +++

* &#x200B;
  +++ Recopilar información de solicitud de API

  Al realizar la llamada de API para almacenar en déclencheur la actividad en directo, guarde lo siguiente:

   * Carga útil de solicitud de API, incluidos los identificadores de perfil y los datos de actividad en directo
   * Respuesta de API que incluye código de estado, ID de mensaje e ID de solicitud
   * Marca de tiempo del momento en el que se llamó a la API
   * Punto de conexión utilizado, p. ej. `/campaign/{CAMPAIGN_ID}/execute`

  +++

* &#x200B;
  +++ Identificación del perfil de prueba

  En la solicitud de API, recupere:

   * Área de nombres del perfil, por ejemplo, ECID, correo electrónico, ID de cliente
   * ID de perfil utilizado en la llamada de API

  Asegúrese de que puede buscar este perfil en Adobe Experience Platform. Aprenda a [buscar un perfil en la documentación de Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide.html).

  +++

* &#x200B;
  +++ Información del dispositivo y la aplicación

  Recopile lo siguiente del dispositivo de prueba:

   * Modelo de dispositivo, por ejemplo, iPhone 14 Pro
   * Versión de iOS
   * Identificador del paquete de aplicaciones
   * Token push de APNS
   * Estado de conectividad de red en el momento de la prueba

  +++

## Casos comunes

### Problemas de perfil o token push {#profile-issue}

[!BADGE Se aplica a los casos de uso unitario y de difusión]{type=Positive}

La API devuelve el valor HTTP 200, pero la actividad Live no aparece. Causas frecuentes:

* El perfil no existe en Adobe Experience Platform.
* El token push de la actividad activa no se ha sincronizado con el perfil.
* Los detalles de inserción de la actividad activa se sincronizan, pero contienen una configuración incorrecta, como `appId` o `attributeType` incorrectos.

**Nota para casos de uso de difusión**: Si a algunos perfiles de su audiencia les faltan tokens, solo esos perfiles no recibirán la actividad en directo. Muestre varios perfiles de su audiencia para diagnosticar problemas de tokens. Esto solo se aplica a eventos de inicio remotos, no a eventos de actualización o finalización.

#### Comprobaciones previas

* Requisitos de la aplicación iOS:
   * iOS 16.1+
   * `NSSupportsLiveActivities` se estableció en `YES` en `Info.plist`
   * `ActivityAttributes` se implementó correctamente.
* Integración de SDK móvil:
   * Adobe Experience Platform Mobile SDK (mensajería SDK 5.11.0+)
   * `Messaging.registerLiveActivities` implementado y llamado con el token de inserción de actividad en vivo.

#### Pasos de depuración

1. &#x200B;
   +++ Comprobar que el perfil existe en Adobe Experience Platform

   1. En Journey Optimizer, vaya a **Cliente** `>` **Perfiles**.
   1. Busque utilizando el área de nombres y el valor de identidad de la solicitud de API.
   1. Si no se encuentra el perfil, este no existe o la ingesta no se ha completado. Cree el perfil o espere a que se produzca la ingesta antes de activar la actividad Live.
   1. Si se encuentra un perfil, continúe con el paso 2 a continuación para comprobar si el token push está sincronizado.

      +++

1. &#x200B;
   +++ Compruebe si el token push de la actividad en directo está sincronizado

   Puede utilizar Assurance para verificar el registro de tokens:

   1. En Assurance, en la lista **Eventos**, filtre o busque los eventos `eventType = "liveActivity.pushToStart"`.
   1. Seleccione **Event** e inspeccione la carga útil.
   1. Compruebe que los valores de token, appId y attributeType estén presentes.
   1. Confirme si el evento se envió correctamente.

   También puede registrar el perfil de Adobe Experience Platform.

   1. En Adobe Experience Platform, desde tu **perfil**, accede a la pestaña **Eventos**.
   1. Busque `liveActivity.pushToStart` eventos.
   1. Compruebe la marca de tiempo par y la carga útil.

   Si no se encuentran eventos, la aplicación móvil no está llamando a `Messaging.registerLiveActivity` correctamente. Debe corregir la integración de SDK.

   +++

1. &#x200B;
   +++ Validar detalles de token en el perfil

   1. Desde tu **perfil**, accede a la pestaña **Atributos**.
   1. Busque `liveActivityPushNotificationDetails`.
   1. Compruebe la configuración del token:

      ```json
      {
        "liveActivityPushNotificationDetails": [
          {
            "appId": "com.example.myapp",
            "token": "abc123def456...",
            "platform": "apns",
            "denylisted": false,
            "attributeType": "OrderTrackingAttributes",
            "identity": {}
          }
        ]
      }
      ```

   **Validar cada campo:**

   | Campo | Requisito | Problema común |
   |-|-|-|
   | `appId` | Debe coincidir exactamente con el identificador del paquete iOS | Disparidad entre los ID del paquete dev/prod |
   | `attributeType` | Debe coincidir exactamente con el nombre de estructura de Swift `ActivityAttributes` (con distinción de mayúsculas y minúsculas) | Error al escribir o nombre de estructura incorrecto |
   | `platform` | Debe ser `"apns"` o `"apnsSandbox"` | Valor de plataforma incorrecto |
   | `denylisted` | Debe ser `false` | Token marcado como no válido o exclusión del usuario |
   | `token` | Token push de APN válido | Token caducado o aplicación reinstalada |

   Si algún campo es incorrecto: actualice la aplicación móvil, vuelva a registrarse con `Messaging.registerLiveActivities`, espere de 5 a 10 minutos y vuelva a realizar la comprobación.

   Si falta `liveActivityPushNotificationDetails`: el token aún no se ha sincronizado. Espere de 5 a 10 minutos después de ver el evento `liveActivity.pushToStart` en Assurance.

   +++

### Problemas de configuración de Campaign y carga útil {#payload-issues}

[!BADGE Se aplica a los casos de uso unitario y de difusión]{type=Positive}

El perfil existe con tokens válidos, pero la actividad en directo no aparece. Esto puede deberse a lo siguiente:

* Configuración de superficie o canal incorrecta.
* Estructura de carga útil de API incorrecta.
* `content-state` y `attributes` no coinciden con la implementación de iOS `ActivityAttributes`.
* Antiguo `timestamp` (crítico para la actualización/finalización).

**Nota para casos de uso de difusión**: la campaña debe ser **Marketing activado por API** (no transaccional). La carga útil utiliza `audience` en lugar de `profile` individual. Consulte [esta sección](#broadcast-config) para obtener información sobre la estructura de carga útil específica de difusión y [documentación de Adobe Developer](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMAudienceMessageExecution) para obtener especificaciones completas de la API.

#### Comprobaciones previas

* La campaña es **Transaccional activada por API** (unitaria) o **Marketing activada por API** (difusión) y la opción **Alto rendimiento** debe estar **no** habilitada ya que es incompatible con la actividad en directo.
* Asegúrese de que el perfil existe y de que los tokens se sincronizan correctamente usando el [escenario anterior](#profile-issue).

#### Pasos de depuración

1. &#x200B;
   +++ Verifique la configuración de campaña

   1. En Journey Optimizer, abra su **Campaña** y vaya al menú **Acciones**.
   1. Comprueba tu **configuración de actividad en vivo**. La superficie debe configurarse para la aplicación de iOS con un identificador de paquete que coincida con el `appId` en `liveActivityPushNotificationDetails` de su perfil. Por ejemplo, si su perfil tiene `"appId": "com.example.myapp"`, la superficie debe segmentar esa misma aplicación.
   1. Compruebe que el **tipo de actividad** de la configuración de su campaña coincida exactamente con el `attributeType` del `liveActivityPushNotificationDetails` de su perfil. Por ejemplo, si su perfil tiene `"attributeType": "FoodDeliveryLiveActivityAttributes"`, la campaña debe especificar este mismo tipo de actividad.

      +++

1. &#x200B;
   +++Validar estructura de carga útil de API

   Al ejecutar la campaña a través de la API, asegúrese de que la carga útil sigue la estructura correcta.

   **Carga útil unitaria:**

   ```json
   {
     "campaignId": "your-campaign-id",
     "recipients": [{
       "type": "aep",
       "userId": "user@example.com",
       "namespace": "email",
       "context": {
         "requestPayload": {
           "aps": {
             "content-available": 1,
             "timestamp": 1756984054,
             "event": "start",
             "attributes-type": "FoodDeliveryLiveActivityAttributes",
             "content-state": { ... },
             "attributes": { ... }
           }
         }
       }
     }]
   }
   ```

   **Problemas comunes de carga útil:**

   | Campo | Requisito | Problema común |
   |-|-|-|
   | `attributes-type` | Debe coincidir con el tipo de actividad de campaña y el perfil `attributeType` | Discordancia o error tipográfico |
   | `campaignId` | Debe coincidir con el ID de campaña activado | ID de campaña incorrecto o no presente |
   | `content-available` | Debe ser `1` | Falta un valor o es incorrecto |
   | `event` | Debe ser `"start"`, `"update"` o `"end"` | Tipo de evento no válido |
   | `timestamp` | Siempre debe ser la hora actual/más reciente de Unix epoch en segundos | Usar marca de tiempo antigua/en caché |
   | `userId` / `namespace` | Debe coincidir con un perfil existente en AEP | El identificador de perfil no coincide |

   **Crítico: usar siempre la última marca de tiempo**

   * El campo `timestamp` debe **siempre** ser el **tiempo actual de Unix epoch** (en segundos) en el momento en que se realiza cada llamada de API.
   * Esto se aplica a **todos los tipos de eventos**: `start`, `update` y **especialmente a`end`**.
   * **Impacto en las actualizaciones/solicitudes de finalización**: el uso de una marca de tiempo antigua o obsoleta provocará que las solicitudes de actualización y finalización no se realicen correctamente o que el dispositivo las ignore.
   * **NOT** reutiliza marcas de tiempo de solicitudes anteriores o usa valores almacenados en caché.
   * Genere una nueva marca de tiempo para cada llamada de API.

   **Campos opcionales (todos los tipos de eventos):**

   * `requestId`: Identificador único para seguimiento (recomendado).
   * `alert`: objeto con `title` y `body` para notificación (útil para llamar la atención sobre las actualizaciones).

   **Acerca de `dismissal-date`:**

   * Campo opcional que contiene Unix epoch time (seconds).
   * **Solo es relevante cuando`event: "end"`**.
   * Especifica cuándo se debe eliminar automáticamente la actividad en directo del dispositivo.
   * Si no se proporciona en el evento Fin, la actividad Live permanece visible hasta que el usuario la descarta.
   * Debe ser una marca de tiempo futura (posterior a `timestamp`).

     +++

1. &#x200B;
   +++ Alinear la carga útil con la implementación de iOS

   Asegúrese de que la carga útil de la API coincida con la implementación de la aplicación de iOS `ActivityAttributes`. El protocolo `LiveActivityAttributes` de Adobe SDK amplía iOS `ActivityAttributes` y requiere una propiedad `liveActivityData`.

   **Validar la asignación:**

   1. Su `ActivityAttributes` debe implementar el protocolo `LiveActivityAttributes` de Adobe. Por ejemplo:

      ```swift
      struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
       public struct ContentState: Codable, Hashable {
           var orderStatus: String
           var estimatedDeliveryTime: String
       }
      
       // Adobe SDK requirement
       var liveActivityData: LiveActivityData
      
       // Your custom attributes
       var restaurantName: String
      }
      ```

      **Tenga en cuenta** que Adobe SDK requiere el campo `liveActivityData` y que debe incluirse en todas las implementaciones.

   1. La carga útil de la API debe reflejar la estructura de iOS:

      ```json
      {
        "aps": {
           "event": "start",
           "timestamp": 1756984054,
           "attributes-type": "FoodDeliveryLiveActivityAttributes",
           "content-state": {
           "orderStatus": "Preparing",
           "estimatedDeliveryTime": "20 mins"
        },
        "attributes": {
          "liveActivityData": {
            "liveActivityID": "order-12345"
          },
          "restaurantName": "Pizza Palace"
        }
        }
      }
      ```

   **Lista de comprobación de validación:**

   * Incluir todos los `ContentState` campos en `content-state` (requerido para todos los tipos de eventos).
   * Incluir todos los campos de `LiveActivityAttributes` en `attributes` (solo eventos de inicio), incluidos:
      * `liveActivityData` (obligatorio; normalmente contiene `liveActivityID` o un identificador similar)
      * Todos los campos personalizados de la estructura
   * Haga coincidir los nombres de los campos exactamente (con distinción de mayúsculas y minúsculas).
   * Hacer coincidir tipos de datos (String, Int, Bool, objetos anidados).
   * Conservar la estructura de objetos anidados.

   **Errores comunes:**

   | Problema | Impacto | Se ha corregido un problema que hacía que se mostrara |
   |-------|--------|-----|
   | Faltan `liveActivityData` en los atributos | La actividad en directo no se inicia | Incluir siempre el objeto `liveActivityData` en el evento de inicio |
   | Falta un campo obligatorio en el evento de inicio | La actividad en directo no se inicia | Añadir todos los campos de la estructura de iOS |
   | Nombre de campo incorrecto (error tipográfico/caso) | Campo omitido o error de análisis | Igualar exactamente los nombres de los campos de iOS |
   | Tipo de datos incorrecto | Error de análisis | Hacer coincidir tipos de datos de iOS |
   | Falta un objeto anidado | Datos incompletos | Incluir todas las estructuras anidadas |
   | Incluyendo `attributes` en actualización/fin | Innecesario, pero generalmente ignorado | Incluir solo `attributes` en el evento de inicio |
   | Marca de tiempo antigua al actualizar/finalizar | El dispositivo ignora la actualización o el final | Generar siempre nueva marca de tiempo |

   Para obtener más ejemplos, consulte [Crear página de actividad en vivo](create-mobile-live.md).

   +++

1. &#x200B;
   +++ Prueba con Assurance

   Compruebe la ejecución de la API y la entrega de carga útil mediante Assurance:

   1. Abra la sesión de Assurance.
   1. Ejecute la llamada de la API para almacenar en déclencheur la actividad en directo.
   1. En **Lista de eventos**, compruebe lo siguiente:
      * Eventos de ejecución de Campaign.
      * Eventos de entrega de actividad en directo.
      * Eventos de error de validación de carga útil.
   1. Revise las cargas útiles de evento para verificar:
      * La carga útil se ha procesado correctamente.
      * No se han producido errores de validación.
      * La actividad en directo se ha enviado a APNS.

      +++

### Errores de entrega y análisis de errores

[!BADGE Se aplica a los casos de uso unitario y de difusión]{type=Positive}

En este caso, todas las comprobaciones anteriores han pasado:

* El perfil existe con [tokens de inserción de actividad en directo válidos](#profile-issue)
* La campaña se ha [configurado correctamente con la carga útil adecuada](#payload-issues)
* [Se sincronizan los tokens de actualización](#token-not-synced) (solo para eventos de actualización/finalización, caso de uso unitario)

Pero la actividad en directo sigue sin aparecer, actualizarse ni finalizar según lo esperado. El problema puede deberse al sistema de entrega de Adobe o al proveedor de servicios de notificaciones push (APN).

**Nota para casos de uso de difusión**: los informes muestran métricas entre todos los miembros de la audiencia. Algunos perfiles pueden tener éxito mientras que otros fallan.

**Comprobaciones previas**

* **Escenarios Anteriores Validados:**
   * El perfil existe con `liveActivityPushNotificationDetails` correctos
   * La superficie de campaña y el tipo de actividad son correctos
   * La carga útil de API es válida con la marca de tiempo actual
   * Los tokens de actualización se sincronizan (para eventos de actualización/finalización)

* **Llamada API confirmada:**

   * La llamada de API devolvió HTTP 200 (correcto)
   * El ID de campaña y los detalles del destinatario son correctos

#### Pasos de depuración

1. &#x200B;
   +++ Comprobación de informes de campaña

   1. Vaya a su **Actividad en directo en Campaign**.
   1. Haga clic en el botón **Informes**.
   1. Seleccione **Ver informe de todo el tiempo**.
   1. Revise las secciones siguientes:

      1. Compruebe las métricas **Estadísticas de envío** para comprender el éxito de la entrega:

         | Métrica | Lo que significa | Qué se debe buscar |
         |-|-|-|
         | Segmentado | Número de perfiles cualificados para la audiencia | Debe incluir el perfil de prueba |
         | Envíos | Total de notificaciones push intentadas | Debe coincidir con sus llamadas a la API |
         | Entregados | Entregado correctamente a los dispositivos | Comparar con Envíos para ver la tasa de éxito |
         | Enviar errores | Notificaciones push que no se han enviado | Números altos |
         | Envío de exclusiones | Perfiles excluidos por Adobe Journey Optimizer | Compruebe si su perfil se ha excluido |

      1. Si Enviar errores > 0, consulte la tabla **Motivos del error** para ver los códigos de error y los mensajes específicos:

         | Error común | Significado | Resolución |
         |-|-|-|
         | Token no válido | El token de inserción no es válido o ha caducado | Volver a registrar tokens de actividad activos desde el dispositivo |
         | Token no encontrado | No hay ningún token válido asociado al perfil | Comprobar que `liveActivityPushNotificationDetails` existe |
         | APNS rechazadas | El servicio de notificaciones push de Apple rechazó la notificación push | Comprobación del certificado de APNS, ID de paquete, entorno |
         | Tiempo de espera de red | No se puede acceder a APNS | Problema transitorio; vuelva a intentar la llamada de API |

      1. Si **Enviar exclusiones** > 0, compruebe la tabla **Motivos de exclusión**:

         | Exclusión común | Significado | Resolución |
         |-|-|-|
         | Perfil excluido | El usuario ha excluido las notificaciones | Comprobar estado de consentimiento del perfil |
         | Token | Token marcado como no válido | Volver a registrar el token o comprobar el estado de la lista de bloqueados de la |
         | Perfil no apto | El perfil no cumple los criterios de la campaña | Revisar reglas de audiencia de campaña |

   Obtenga más información en la [página de informe de campaña de actividades en vivo](../reports/campaign-global-report-cja-activity.md).

   +++

1. &#x200B;
   +++ Comprobación de eventos de comentarios de mensajes en el perfil

   1. Vaya a **Cliente** > **Perfiles** en Journey Optimizer.
   1. Busque y abra el perfil.
   1. Seleccione la ficha **Eventos**.
   1. Filtre o busque eventos con `eventType = "message.feedback"`.
   1. Busque eventos de comentarios que coincidan con el tipo `liveActivityID` y `event` de su actividad en directo.
   1. Revise los siguientes campos clave:

      | Campo | Valores posibles | Lo que significa |
      |-|-|-|
      | `feedbackStatus` | `sent`, `error`, `denylist` | Resultado del envío del proveedor de servicios |
      | `serviceProvider` | `apns/apnsSandbox` | Debe ser APNS para actividades de iOS Live |
      | `errorCode` | Código numérico para `null` | Código de error específico de APNS si falla |
      | `errorMessage` | Descripción del error para `null` | Mensaje de error legible por un ser humano |

   1. **Si `feedbackStatus: "error"`:**
      * Compruebe si hay errores APN específicos en `errorCode` y `errorMessage`
      * Los errores comunes de APNS incluyen token caducado, certificado no válido e ID de paquete incorrecto

   1. **Si no se encuentra ningún evento de comentarios:**
      * Es posible que no se haya intentado la notificación push
      * Compruebe si el perfil se ha excluido en los informes de campaña tal como se detalla en el paso 1 anterior.

      +++

1. &#x200B;
   +++ Verificación de la entrega de actividades en directo a APNS en Assurance

   1. Abra la sesión de Assurance, debe estar activa durante la llamada de API.
   1. Ejecute la llamada de API (inicio, actualización o finalización).
   1. En **Lista de eventos**, busque Eventos de entrega de actividades en directo.
   1. Busque eventos relacionados con la entrega push de APNS.
   1. Compruebe la existencia de las luces testigo siguientes:
      * **Solicitud push a APNS**: Confirma que Adobe envió la notificación push a los servidores de Apple
      * **Respuesta de APN**: Muestra si APN aceptó o rechazó la notificación push
      * **Estado de entrega**: Indicación de éxito o error
   1. Si se encuentran problemas, consulte los siguientes problemas comunes de entrega de APN:

      | Problema | Síntoma en Assurance | Resolución |
      |-|-|-|
      | Certificado de APNS caducado | Error de autenticación | Renovar y cargar un nuevo certificado de APN |
      | Entorno incorrecto (dev vs prod) | Error de coincidencia de tokens | Asegúrese de que el certificado coincida con el tipo de creación de aplicación |
      | ID de paquete no coincidente | Identificador de paquete no válido | Verificar que el ID del paquete de certificados coincida con la aplicación |
      | Token caducado | Error InvalidToken de APNS | Volver a registrar tokens de actividad activos |
      | Limitación de velocidad | Demasiadas solicitudes | Reducir frecuencia de llamada de API |

      +++

1. &#x200B;
   +++ Pasar a comprobaciones de diagnóstico adicionales

   1. Compruebe las métricas del ciclo vital de la actividad en directo en el informe de Campaign.

      En el informe de campaña, revise la sección **Ciclo de vida de la actividad en directo**:

      | Métrica | Qué comprobar |
      |-|-|
      | Inicios remotos | Debe mostrar el recuento de inicios activados por API |
      | Actualizaciones | Debe mostrar el recuento de eventos de actualización |
      | Finaliza | Debe mostrar el recuento de eventos finales |
      | Recuento de totales | Volumen general del evento de actividad en directo |

      Si estas métricas son cero o no coinciden con sus llamadas de API, hay un problema de envío entre Adobe y APNS.

   1. Si Adobe muestra un envío correcto pero el dispositivo no muestra la actividad en directo:

      * Compruebe si hay errores de actividad en directo en los registros de dispositivos iOS.
      * Verifique que la aplicación esté en primer o segundo plano (no finalizada).
      * Confirme que el dispositivo tiene conectividad de red.
      * Realice pruebas en varios dispositivos para descartar problemas específicos del dispositivo.
      * Compruebe que la versión de iOS sea 16.1 o posterior.

      +++

1. &#x200B;
   +++ Escalación al Soporte de Adobe

   Si ha completado todos los pasos y el problema sigue sin resolverse, póngase en contacto con el Servicio de atención al cliente de Adobe con:

   **Información necesaria:**

   * ID y nombre de la campaña
   * Área de nombres e ID de perfil
      * `liveActivityID` de carga útil de API
   * Marcas de hora de llamadas API
   * Capturas de pantalla de:
      * Informes De Campaña (Estadísticas De Envío, Motivos De Error, Motivos De Exclusión)
      * Eventos de perfil (`liveActivity.updateToken`, `message.feedback`)
      * Sesión de Assurance que muestra eventos de envío
   * Carga útil de solicitud de API completa
   * Detalles del certificado de APNS (caducidad, entorno, ID de paquete)

     +++

## Situaciones específicas unitarias

### Token de actualización de actividad activa no sincronizado{#token-not-synced}

La actividad Live se inicia correctamente en el dispositivo, pero las llamadas a la API `update` o `end` subsiguientes (que devuelven HTTP 200) no se pueden actualizar o descartar la actividad Live. Esto ocurre cuando el **token de actualización de la actividad en directo** no está sincronizado correctamente con el sistema de Adobe.

**Explicación de los tokens de actualización**

Cuando se inicia una actividad Live en un dispositivo, iOS genera un token de actualización único para esa instancia de actividad Live específica. Este token es necesario para lo siguiente:

* Envío de actualizaciones a la actividad en directo
* Finalización remota de la actividad Live

Cada instancia de actividad Live tiene su propio token de actualización único. Adobe necesita este token para entregar eventos de actualización y finalización.

**Comportamiento esperado**

Para que funcionen los eventos update y end, debe ocurrir lo siguiente:

1. La actividad en directo se inicia correctamente en el dispositivo.
1. El dispositivo genera un token de actualización para esa instancia de actividad en directo.
1. Mobile SDK captura y envía el token de actualización a Adobe.
1. El token de actualización se sincroniza y almacena en el sistema de Adobe.
1. Las llamadas de API posteriores para la actualización/finalización utilizan este token para la entrega.

**Comprobaciones previas:**

* **Permiso de usuario**: La primera vez que se inicia una actividad en directo en un dispositivo, iOS muestra un mensaje del sistema: &quot;¿Permitir que [Nombre de aplicación] proporcione actualizaciones de actividades en directo?&quot; El usuario **debe pulsar &quot;Permitir&quot;** para que se generen y sincronicen los tokens de actualización. Si el usuario pulsa &quot;No permitir&quot;, no se crea ningún token de actualización y las solicitudes de actualización/finalización fallarán. Se trata de un permiso único por aplicación.
* **Validación de perfiles y campañas**: complete las comprobaciones de [Escenario 1](#profile-issue) y [Escenario 2](#payload-issues) para garantizar que la configuración del perfil, los tokens y la campaña sea correcta.

#### Pasos de depuración

1. &#x200B;
   +++ Verificar la sincronización del token de actualización en Assurance

   1. Abra la sesión de Assurance.
   1. Asegúrese de que la sesión esté activa cuando se inició la actividad en directo en el dispositivo.
   1. Filtre o busque eventos con `eventType = "liveActivity.updateToken"`.
   1. Seleccione el evento e inspeccione la carga útil:

      * Compruebe que el campo `token` contenga una cadena de token de actualización válida.
      * Compruebe que `liveActivityID` coincida con su instancia de actividad en directo.
      * Confirme que `activityType` coincide con su `attributes-type`.

   1. Si no se encuentra el evento:

      * SDK no ha generado ni capturado el token de actualización.
      * Compruebe si el usuario ha concedido permisos de actividad en directo.
      * Compruebe que la actividad Live se haya iniciado correctamente en el dispositivo.
      * Confirme que el SDK móvil está correctamente integrado para capturar los tokens de actualización.

   1. Si se encuentra el evento, continúe con el paso 2.

      +++

2. &#x200B;
   +++ Verificar el token de actualización en los eventos de perfil

   1. Vaya a **Cliente** > **Perfiles** en Journey Optimizer.
   1. Busque y abra el perfil.
   1. Seleccione la ficha **Eventos**.
   1. Busque `liveActivity.updateToken` eventos.
   1. Compruebe los detalles del evento:

      * Compruebe que la marca de tiempo sea reciente (coincide con el momento en el que se inició la actividad en directo).
      * Confirme que `token` y `liveActivityID` están presentes.
      * Asegúrese de que `activityType` sea correcto.

   1. Si el evento no se encuentra en el perfil:

      * Es posible que el evento de token de actualización aún no se haya introducido en el perfil.
      * Espere de 5 a 10 minutos y vuelva a efectuar la comprobación.
      * Si sigue faltando después de 15 minutos, puede haber un problema de ingesta de evento.

   1. Si se encuentra el evento, se ha sincronizado el token de actualización. Puede continuar con el paso 3.

      +++

3. &#x200B;
   +++ Compruebe los eventos de entrega de actividades en directo en Assurance

   1. En la sesión de Assurance, ejecute una actualización o termine la llamada a la API.
   1. En la **Lista de eventos**, busque Eventos de entrega de actividades en directo (eventos push de APN).
   1. Compruebe si hay eventos que indiquen:
      * Notificación push enviada a APNS.
      * Respuesta de APNS (éxito o error).
      * Confirmación de envío.
   1. Si el evento de envío de APNS está presente: Se envió la notificación push. Si el dispositivo sigue sin actualizarse, el problema puede estar en el dispositivo (la aplicación no gestiona la notificación push, los problemas de red, etc.).
   1. Si falta el evento de envío de APNS: es posible que el token de actualización no se almacene correctamente o no esté asociado al perfil en el sistema de Adobe.
   1. Si hay eventos de error: inspeccione los detalles del error por motivos de error específicos (token no válido, APN rechazados, etc.).

      +++

## Situaciones específicas de difusión

### Problemas de configuración de campañas de difusión y carga útil{#broadcast-config}

Esta sección cubre la resolución de problemas específicos de las actividades de difusión en directo, que requieren diferentes enfoques de depuración que las campañas unitarias.

Cuando los perfiles tienen tokens válidos pero la actividad en directo no aparece, actualiza ni se comporta como se espera para los miembros de la audiencia, el problema suele deberse a uno de los siguientes motivos:

* La campaña no está configurada como marketing activado por API.
* La carga útil de la API usa una estructura de difusión incorrecta (faltan `audience` o `input-push-channel`).
* Los campos `content-state` y `attributes` no coinciden con la implementación de iOS `ActivityAttributes`.
* `input-push-channel` no se creó correctamente en el portal para desarrolladores de Apple.

Este escenario de solución de problemas se aplica a todos los eventos de actividad en directo de las campañas de difusión: `start`, `update` y `end`.

**Comprobaciones previas:**

* **Tipo de campaña**:
   * Compruebe que la campaña se ha creado como marketing activado por API (necesario para las campañas de difusión/basadas en audiencia).
   * Confirme que se ha definido una audiencia en la configuración de la campaña.
* **Validación de perfil y token**: muestree varios perfiles de la audiencia para comprobar que tienen `liveActivityPushNotificationDetails` válidos. Para ver los pasos de validación detallados, siga [Ejemplo 1](#profile-issue).

#### Pasos de depuración

1. &#x200B;
   +++ Verificar configuración de audiencia de campaña

   1. Abra **Campaña de marketing activada por API** en Journey Optimizer.
   1. Vaya a la sección **Audiencia** y verifique:
      * Se selecciona una audiencia para la campaña.
      * El ID de audiencia coincide con el utilizado en la carga útil de la API.
      * La audiencia contiene los perfiles esperados.
   1. Vaya a la sección **Acciones**.
   1. Compruebe la **configuración de actividad activa**:
      * La configuración debe establecerse para la aplicación de iOS con el identificador de paquete correcto.
      * El tipo de actividad debe coincidir con `attributes-type` en su carga útil de API. Por ejemplo, si la carga útil contiene `"attributes-type": "AirplaneTrackingAttributes"`, la campaña debe especificar este mismo tipo de actividad.

      +++

1. &#x200B;
   +++ Validar estructura de carga útil de API de difusión

   La estructura de carga útil de difusión difiere de las campañas unitarias. Compruebe que la carga útil sigue el formato de difusión correcto.

   **Campos obligatorios para la difusión:**

   ```json
   {
     "campaignId": "878a11d4-b519-47bd-8313-fecfee19857b",
     "audience": {
       "id": "8c3dbdea-2957-401f-acf0-3966fba1601e"
     },
     "context": {
       "requestPayload": {
         "aps": {
           "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
           "content-available": 1,
           "timestamp": 1771829292,
           "event": "update",
           "attributes-type": "AirplaneTrackingAttributes",
           "content-state": { ... },
           "attributes": { ... }
         }
       }
     }
   }
   ```

   **Problemas comunes de carga útil:**

   | Campo | Requisito | Problema común |
   |-|-|-|
   | `campaignId` | Debe coincidir con el ID de campaña de marketing activado | ID de campaña incorrecto o uso de una campaña transaccional |
   | `audience.id` | Debe coincidir con una audiencia existente en AEP | El ID de audiencia o la audiencia no son correctos |
   | `input-push-channel` | Necesario para difusión: identificador único de esta instancia de difusión | Falta o no coincide con `channelID` en `liveActivityData` |
   | `timestamp` | Siempre debe ser la hora actual/más reciente de Unix epoch en segundos | Usar marca de tiempo antigua/en caché |
   | `event` | Debe ser `"start"`, `"update"` o `"end"` | Tipo de evento no válido |
   | `attributes-type` | Debe coincidir con el tipo de actividad de campaña | Discordancia o error tipográfico |
   | `content-available` | Debe ser `1` | Falta un valor o es incorrecto |

   **Campos críticos específicos de difusión:**

   * **`input-push-channel`**
      * Necesario para todas las actividades de difusión en directo.
      * Sirve como identificador único para esta instancia de difusión específica.
      * Todos los perfiles de la audiencia reciben actividades en directo vinculadas a este canal.
      * Debe coincidir con `channelID` en `liveActivityData.channelID` (consulte el paso 3).
      * El cliente debe crear para `appID` en Apple Developer Portal.
      * Solo se pueden usar los canales creados para `appID` en concreto para difundir una actividad en directo en esa aplicación.

   * **`audience.id`**
      * Debe hacer referencia a un segmento de audiencia válido creado en Adobe Experience Platform.
      * Todos los perfiles de esta audiencia están segmentados para la actividad en directo.
      * La audiencia debe estar activada y contener perfiles con `liveActivityPushNotificationDetails` válidos.

   **Usar siempre la marca de tiempo más reciente:**

   * El campo `timestamp` debe ser siempre el tiempo de Unix epoch actual (en segundos) para cada llamada de API.
   * Este requisito se aplica a todos los tipos de eventos: `start`, `update` y `end`.
   * **Crítico para actualizaciones/finalización**: el uso de marcas de tiempo antiguas provoca que las solicitudes de actualización y finalización fallen.
   * Genere una nueva marca de tiempo para cada llamada de API de difusión.

   **Campos opcionales:**

   * `dismissal-date`: tiempo de Unix Epoch para el despido automático (solo relevante para `end` eventos)
   * `alert`: objeto con `title` y `body` para notificación

   Consulte la [documentación de la API de mensajería Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/messaging) para obtener especificaciones completas de la API.

   +++

1. &#x200B;
   +++ Alinee contenido-estado, atributos y entrada-canal-push con la implementación de iOS

   Asegúrese de que los campos de carga útil coincidan con la implementación `ActivityAttributes` de su aplicación iOS y de que `input-push-channel` coincida con `channelID` en `liveActivityData`.

   1. Revise la definición de Atributos de actividad de iOS.

   Su estructura `ActivityAttributes` personalizada debe implementar el protocolo `LiveActivityAttributes` de Adobe:

   ```swift
   struct AirplaneTrackingAttributes: LiveActivityAttributes {
    public struct ContentState: Codable, Hashable {
        var journeyProgress: Int
    }
   
    // Adobe SDK requirement
    var liveActivityData: LiveActivityData
   
    // Your custom attributes
    var arrivalAirport: String
    var departureAirport: String
    var arrivalTerminal: String
   }
   ```

   1. Asigne campos de iOS a la carga útil de la API de difusión.

   Para todos los eventos, incluya `attributes` y `content-state`:

   ```json
         {
         "aps": {
          "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
          "event": "start",
          "timestamp": 1771829292,
          "attributes-type": "AirplaneTrackingAttributes",
          "content-state": {
            "journeyProgress": 0
          },
          "attributes": {
            "arrivalAirport": "DEL",
            "departureAirport": "MUM",
            "arrivalTerminal": "T1",
            "liveActivityData": {
              "channelID": "FEt0NgvLEfEAAOqA6AXdIQ=="
            }
          }
         }
         }
   ```

   **Crítico: `input-push-channel` debe coincidir con`channelID`**

   * El valor `input-push-channel` en la raíz de `aps` debe coincidir exactamente con `channelID` en `liveActivityData`.
   * En el ejemplo anterior, ambos valores son `"FEt0NgvLEfEAAOqA6AXdIQ=="`.
   * Esta coincidencia vincula la instancia de difusión con los datos de la actividad en directo.
   * Un desajuste provoca errores de entrega.

   **Puntos de validación clave:**

   * Incluir todos los `ContentState` campos en `content-state` para todos los tipos de eventos.
   * Incluir todos los campos personalizados `LiveActivityAttributes` en `attributes` solo para eventos de inicio.
   * Para los eventos de inicio, `liveActivityData.channelID` debe coincidir con `input-push-channel`.
   * Los nombres de campo distinguen entre mayúsculas y minúsculas y deben coincidir exactamente.
   * Los tipos de datos deben coincidir (String, Int, Bool, objetos anidados, etc.).
   * Para los eventos de actualización/finalización, use el mismo `input-push-channel` que el evento de inicio original.

   **Errores comunes:**

   | Problema | Impacto | Se ha corregido un problema que hacía que se mostrara |
   |-|-|-|
   | Falta `input-push-channel` | La difusión no funcionará | Agregar un ID de canal único para cada difusión |
   | `input-push-channel` no coincide con `channelID` | La actividad en directo no se inicia | Asegúrese de que ambos valores sean idénticos |
   | Diferente `input-push-channel` para actualizar/finalizar | La actualización o el final no llegarán a las actividades activas. | Usar el mismo ID de canal durante el ciclo vital |
   | Falta `liveActivityData.channelID` | La actividad en directo no se vinculará a la difusión | Incluir `channelID` en atributos para el evento de inicio |
   | Falta un campo obligatorio en el evento de inicio | La actividad en directo no se inicia | Añadir todos los campos de la estructura de iOS |
   | Nombre de campo incorrecto (error tipográfico/caso) | Campo omitido o error de análisis | Igualar exactamente los nombres de los campos de iOS |
   | Marca de tiempo antigua al actualizar/finalizar | Los dispositivos ignoran la actualización o el final | Generar siempre nueva marca de tiempo |

   +++

1. &#x200B;
   +++ Prueba con Assurance

   Compruebe la ejecución de la API y la entrega de carga útil mediante Assurance:

   1. Abra la sesión de Assurance en un dispositivo de prueba que forme parte de la audiencia.
   1. Ejecute la llamada de API de difusión.
   1. En **Lista de eventos**, busque:
      * Eventos de ejecución de Campaign.
      * Eventos de entrega de actividad en directo.
      * Eventos de error que indican errores de validación de carga útil.
   1. Inspeccione las cargas útiles de eventos para confirmar:
      * La carga útil se ha procesado correctamente.
      * El `input-push-channel` está presente.
      * No se han producido errores de validación.
      * Se han enviado actividades activas a APNS para miembros de la audiencia.

      +++

### El perfil no está en la audiencia o en una instantánea de audiencia antigua

En esta situación, la campaña y la carga útil están correctamente configuradas, pero los perfiles específicos no reciben la actividad en directo. Esto suele ocurrir cuando:

* El perfil no es miembro de la audiencia vinculada a la campaña.
* La audiencia es una audiencia por lotes y contiene una instantánea obsoleta de los datos del perfil.
* Los tokens de actividad en directo del perfil se añadieron recientemente, pero aún no se han reflejado en la instantánea de audiencia.

Este escenario de solución de problemas se aplica específicamente a las campañas de difusión que utilizan direccionamiento basado en audiencias.

**Explicación de la evaluación de audiencias**

Adobe Experience Platform utiliza diferentes métodos de evaluación de audiencias que determinan cuándo se reflejan las actualizaciones de perfil en la audiencia:

| Método | Frecuencia de evaluación | Actualización de datos | Mejor para |
|-|-|-|--|
| Lote | Una vez al día (programado) | Puede tardar hasta 24 horas en quedar obsoleto | Audiencias grandes, sin distinción de tiempo |
| Streaming | Tiempo real (sin cambios de perfil) | Casi en tiempo real para perfiles actualizados | Con distinción de tiempo, requiere actualizaciones de perfil |

**Comprobaciones previas:**

* **Validación de campaña y carga útil**:
   * Complete las comprobaciones en [este escenario](#broadcast-config) para asegurarse de que la campaña y la carga útil sean correctas.
   * Compruebe que `audience.id` en la carga útil de la API coincida con la configuración de la campaña.
* **El perfil existe**: confirme que el perfil existe en AEP con `liveActivityPushNotificationDetails` válido.

#### Pasos de depuración

1. &#x200B;
   +++ Verificar que el perfil esté en la audiencia

   En primer lugar, confirme si el perfil que debe recibir la actividad en directo es realmente parte de la audiencia.

   1. Vaya a **Audiencias** en Adobe Experience Platform.
   1. Busque y abra la audiencia usando `audience.id` de su campaña.
   1. Haga clic en **Examinar** o **Perfiles de muestra** para ver los miembros de la audiencia.
   1. Busque el perfil de prueba con el área de nombres y el valor de identidad.
   1. **Si no se encuentra el perfil en la audiencia:**
      * El perfil no cumple los criterios de audiencia ni las reglas de segmentos.
      * Revise la definición de la audiencia para comprender los requisitos de pertenencia.
      * Actualice los datos del perfil o la definición de audiencia para incluir el perfil.
      * Espere a que se complete la evaluación de audiencias (consulte el paso 2).
   1. **Si el perfil se encuentra en la audiencia:** Continúe con el paso 2 para comprobar la actualización de los datos.

      +++

2. &#x200B;
   +++ Comprobar el tipo y la programación de evaluación de audiencia

   Identifique si la audiencia utiliza la evaluación por lotes o de flujo continuo, ya que esto determina la actualización de los datos.

   1. En la página **Detalles de audiencia**, compruebe el **método de evaluación**:
      * **Lote**: evaluado una vez al día según una programación.
      * **Transmisión en tiempo real**: se evalúa en tiempo real cuando se producen actualizaciones de perfil.
      * **Edge**: evaluado en ubicaciones de Edge en tiempo real.

   Siga los pasos adecuados para la resolución de problemas según el método de evaluación:

   **Si la audiencia usa la evaluación por lotes:**

   1. **Comprenda las limitaciones de audiencia por lotes:**
      * Las audiencias por lotes se evalúan una vez al día (normalmente de la noche a la mañana).
      * La instantánea de audiencia puede tener hasta 24 horas de antigüedad.
      * Si un perfil ha registrado recientemente tokens de actividad en directo, es posible que esos tokens no estén en la instantánea actual.
      * Las actualizaciones de los perfiles no se reflejarán hasta la siguiente evaluación por lotes.

   1. **Comprobar cuándo se produjo la última evaluación:**
      * En los detalles de la audiencia, busque la marca de tiempo **Última evaluación**.
      * Si las `liveActivityPushNotificationDetails` del perfil se actualizaron después de esta marca de tiempo, la audiencia tiene datos obsoletos.

   1. **Resolver datos obsoletos:**
      1. **Opción 1: esperar la evaluación programada por lotes**
         * La siguiente evaluación por lotes incluirá los datos de perfil actualizados.
         * Esto sucede automáticamente una vez al día.
         * Ideal para escenarios no urgentes.

      1. **Opción 2: evaluación de audiencia bajo demanda de Déclencheur**
         1. Vaya a **Audiencias** en AEP.
         1. Seleccione el público.
         1. Haga clic en **Evaluar ahora** o en **Activar bajo demanda**.
         1. Espere a que se complete la evaluación (esto puede tardar entre minutos y horas según el tamaño de la audiencia).
         1. Compruebe que el perfil tiene ahora datos actualizados en la instantánea de audiencia.
         1. Vuelva a intentar la llamada de API de difusión.

   **Si la audiencia usa la evaluación de transmisión:**

   1. **Comprender el comportamiento de la audiencia de streaming:**
      * Las audiencias de streaming evalúan en tiempo real cuándo se producen actualizaciones de perfil.
      * **Nuevos perfiles**: Se califican poco después de la creación si cumplen los criterios del segmento.
      * **Perfiles actualizados**: Califique o descalifique poco después de ser actualizado.
      * **Perfiles existentes sin cambios**: No se vuelven a evaluar a menos que se produzca una actualización.

   1. **Identificar el problema:**
      * Si un perfil ya existe y cumple los criterios del segmento, pero no se produce ninguna actualización en ese perfil, es posible que no se añada a una audiencia de streaming recién creada.
      * El perfil debe recibir una actualización (cualquier cambio de atributo) para volver a evaluar los déclencheur.

   1. **Resolver el problema:**
      * **Para nuevos perfiles**: Se califican automáticamente si se cumplen los criterios. No se necesita ninguna acción.
      * **Para perfiles existentes sin actualizaciones recientes:**
         * Realice una actualización menor del perfil (por ejemplo, actualice un campo de marca de tiempo).
         * Esto déclencheur la evaluación de la transmisión y añade el perfil a la audiencia.
         * Alternativa: Utilice una audiencia por lotes o una audiencia perimetral para los perfiles existentes.

      +++
