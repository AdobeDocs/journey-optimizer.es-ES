---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del canal de actividad en directo
description: Obtenga información sobre cómo configurar la integración de Adobe Experience Platform Mobile SDK
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 1%

---


# Integración de actividades en directo con Adobe Experience Platform Mobile SDK {#mobile-live-config-sdk}

>[!BEGINSHADEBOX]

* [Introducción a la actividad en directo](get-started-mobile-live.md)
* [Configuración de actividades activas](mobile-live-configuration.md)
* **[Integración de actividades en vivo con Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**
* [Crear una actividad en directo](create-mobile-live.md)
* [Preguntas frecuentes](mobile-live-faq.md)
* [Informe de campaña de actividad en directo](../reports/campaign-global-report-cja-activity.md)


>[!ENDSHADEBOX]

Adobe Experience Platform Mobile SDK ofrece compatibilidad integrada con las actividades en directo de Apple. Esto permite que la aplicación muestre actualizaciones dinámicas en tiempo real directamente en la pantalla de bloqueo y en Dynamic Island sin necesidad de abrir la aplicación.

1. [Importación de módulos necesarios](#import)

   Importe los siguientes módulos: **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**.

1. [Definir atributos](#attributes)

   Cumplir con `LiveActivityAttributes`, incluir `LiveActivityData` y un atributo `ContentState`.

1. [Registrar actividades activas](#register)

   Use `Messaging.registerLiveActivity()` después de la inicialización de SDK.

1. [Crear configuración de widget](#widget)

   Implemente `ActivityConfiguration` tanto para la pantalla bloqueada como para la interfaz de Dynamic Island.

1. [Iniciar una actividad Live localmente (opcional)](#local)

   Las actividades activas se pueden iniciar de forma remota a través de Journey Optimizer o de forma local dentro del código de la aplicación.

1. [Agregar compatibilidad de depuración (opcional)](#debug)

   Implementar `LiveActivityAssuranceDebuggable` para Assurance.

Compruebe que están instaladas las siguientes versiones mínimas para garantizar una configuración y compatibilidad correctas.

>[!BEGINSHADEBOX]

**Requisitos previos:**

* **iOS:**
   * **iOS16.1 o posterior**: Funcionalidad básica de actividad en directo
   * **iOS 17.2+**: compatibilidad con push-to-start
   * **iOS 18+**: compatibilidad con el canal de difusión
* **Xcode:** 14.0 o posterior
* **Swift:** 5.7 o posterior
* **Dependencias:** AEPCore, AEPMessaging, AEPMessagingLiveActivity, ActivityKit

>[!ENDSHADEBOX]

## Paso 1: Importar los módulos necesarios {#import}

Para empezar, primero debe importar los siguientes módulos: **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]**.

```swift
import AEPMessaging
import AEPMessagingLiveActivity
import ActivityKit
```

## Paso 2: Definir los atributos de la actividad Live {#attributes}

Cree una estructura que se ajuste al protocolo `LiveActivityAttributes`. Esto define tanto los datos estáticos como el estado del contenido dinámico para su actividad en directo.

Los componentes clave incluyen:

* **`liveActivityData`** (obligatorio) que contiene datos específicos de Adobe Experience Platform.
   * Para usuarios individuales: use `LiveActivityData(liveActivityID: "unique-id")`
   * Para difusión: usar `LiveActivityData(channelID: "channel-id")`

* Atributos estáticos, propiedades personalizadas específicas del caso de uso, por ejemplo `restaurantName`.

* **`ContentState`**, que define los datos dinámicos que se pueden actualizar durante el ciclo vital de la actividad. Debe ajustarse a `Codable` y `Hashable`.

* La enumeración `LiveActivityOrigin` especifica si una actividad se inició localmente en la aplicación o de forma remota mediante una notificación push-to-start, admitida en iOS 17.2 y versiones posteriores. Este valor permite a SDK diferenciar entre actividades en directo iniciadas localmente y activadas de forma remota durante la recopilación de datos.

**Ejemplos**

```swift
@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
    // Mandatory: AEP Integration Data
    var liveActivityData: LiveActivityData
    
    // Static Attributes: Custom properties that do not change
    var restaurantName: String
    
    // Dynamic Content State: Data that can be updated
    struct ContentState: Codable, Hashable {
        var orderStatus: String
    }
}
```

```swift
@available(iOS 16.1, *)
public struct LiveActivityData: Codable {
    /// Unique identifier for broadcast Live activity channels
    public let channelID: String?
     
    /// Unique identifier for individual Live activities
    public let liveActivityID: String?
     
    /// Indicates local vs remote creation
    public let origin: LiveActivityOrigin?
     
    // Initializers
    public init(channelID: String)        // For broadcast Live activities
    public init(liveActivityID: String)   // For individual Live activities
}
```

También puede registrar varios tipos de actividades en directo para la aplicación:

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(AirplaneTrackingAttributes.self)
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
    Messaging.registerLiveActivity(GameScoreLiveActivityAttributes.self)
}
```

## Paso 3: Registro de actividades activas {#register}

Registre los tipos de actividades de Live en su `AppDelegate` después de la inicialización de SDK, esto le permite:

* Habilita la recopilación automática de tokens de push-to-start (iOS 17.2+)
* Recopila automáticamente tokens de actualización de actividades en directo
* Habilita la administración del ciclo vital y el seguimiento de eventos

**Ejemplo de una actividad de entrega de alimentos en directo:**

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
}
```

## Paso 4: Crear widgets de actividad activos {#widgets}

Las actividades activas se muestran a través de widgets, debe crear un paquete de widgets y una configuración:

**Ejemplo de una actividad de entrega de alimentos en directo:**

```swift
@main
struct FoodDeliveryWidgetBundle: WidgetBundle {
    var body: some Widget {
        FoodDeliveryLiveActivityWidget()
    }
}

@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityWidget: Widget {
    var body: some WidgetConfiguration {
        ActivityConfiguration(for: FoodDeliveryLiveActivityAttributes.self) { context in
            // Lock Screen UI
            VStack {
                Text("Order from \(context.attributes.restaurantName)")
                Text("Status: \(context.state.orderStatus)") // possible status may include "Ordered", "Order accepted", "Preparing", "On the Way","Delivered"
            }
        } dynamicIsland: { context in
            // Dynamic Island UI
            DynamicIsland {
                // Expanded UI
            } compactLeading: {
                // Compact leading UI
            } compactTrailing: {
                // Compact trailing UI
            } minimal: {
                // Minimal UI
            }
        }
    }
}
```

## Paso 5: Inicio de una actividad Live localmente (opcional) {#local}

Aunque Journey Optimizer puede iniciar actividades Live de forma remota, también puede iniciarlas localmente:

**Ejemplo de una actividad de entrega de alimentos en directo:**

```swift
let attributes = FoodDeliveryLiveActivityAttributes(
    liveActivityData: LiveActivityData(liveActivityID: "order123"),
    restaurantName: "Pizza Palace"
)

let contentState = FoodDeliveryLiveActivityAttributes.ContentState(
    orderStatus: "Ordered"
)

let activity = try Activity<FoodDeliveryLiveActivityAttributes>.request(
    attributes: attributes,
    contentState: contentState,
    pushType: .token
)
```

## Paso 6: Agregar compatibilidad de depuración (opcional) {#debug}

Si es necesario, puede depurar los esquemas de actividad en directo en Adobe Assurance:

**Ejemplo de una actividad de entrega de alimentos en directo:**

```swift
@available(iOS 16.1, *)
extension FoodDeliveryLiveActivityAttributes: LiveActivityAssuranceDebuggable {
    static func getDebugInfo() -> (attributes: FoodDeliveryLiveActivityAttributes, state: ContentState) {
        return (
            FoodDeliveryLiveActivityAttributes(
                liveActivityData: LiveActivityData(liveActivityID: "debug-order-123"),
                restaurantName: "Debug Restaurant"
            ),
            ContentState(orderStatus: "Ordered")
        )
    }
}
```


