---
solution: Journey Optimizer
product: journey optimizer
title: Uso y configuración de vínculos profundos en mensajes de correo electrónico y SMS
description: Obtenga información sobre cómo añadir vínculos profundos al contenido de correo electrónico y SMS y cómo implementar la gestión de vínculos profundos en aplicaciones de iOS y Android.
feature: Email, SMS
topic: Content Management
role: User, Developer
level: Intermediate
keywords: vínculo profundo, vínculo profundo, vínculos universales, vínculos de aplicación, correo electrónico, sms
source-git-commit: accdbd5bd5023ed8352ca6fba58a26e797ac1d68
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 1%

---


# Uso y configuración de vínculos profundos en correos electrónicos y SMS {#deeplinks}

Los vínculos profundos le ayudan a llevar los destinatarios de un mensaje de correo electrónico o SMS a una pantalla o fragmento de contenido específico en su aplicación móvil. Ayuda a llevar a las personas directamente a la experiencia en la aplicación deseada, sin enrutarlas a través de un explorador web o una tienda de aplicaciones, de modo que el recorrido sigue siendo relevante y se adapta a la marca.

Cuando los destinatarios hacen clic en el vínculo profundo, se les redirige directamente al contenido previsto en la aplicación: **siempre que haya completado**:

* los [pasos de configuración](#configuration) en Journey Optimizer;

* los pasos de la [implementación de la aplicación móvil](#mobile-implementation) para iOS y Android en su aplicación móvil.

>[!NOTE]
>
>[!DNL Adobe Journey Optimizer] admite la vinculación profunda tanto para iOS como para Android mediante direcciones URL rastreadas (`/ee/v1/mclick/*`) para garantizar la compatibilidad y el rastreo de clics.

## Creación de vínculos profundos {#authoring}

### Correo electrónico {#authoring-email}

Para los mensajes de correo electrónico, tiene dos opciones para insertar un vínculo profundo:

* **Enviar correo electrónico a Designer**: Asegúrate de que el seguimiento de [vínculos está habilitado](message-tracking.md#enable-tracking). Seleccione el elemento que desea vincular (texto, botón o imagen), haga clic en **[!UICONTROL Insertar vínculo]** en la barra de herramientas contextual y elija **[!UICONTROL Vínculo profundo]** para introducir su URL de vínculo profundo. [Más información sobre cómo insertar vínculos](message-tracking.md#insert-links)

* **Editor de Personalization (código)**: inserte el vínculo profundo directamente en HTML utilizando el siguiente fragmento de código:

  ```html
  <a class="arc-link" data-nl-type="DEEPLINK" href="<<deeplink_url>>" id="acr-link-7821368" style="text-decoration:underline;" target="_blank" data-tracking-type="DEEPLINK">Click Here</a>
  ```

  Reemplace `<<deeplink_url>>` por su dirección URL de vinculación profunda real y utilice un `id` único para cada bloque a fin de evitar conflictos.

### SMS {#authoring-sms}

Para los SMS, los vínculos profundos se crean mediante la función de ayuda **Url** en el editor de personalización. Más información sobre cómo agregar vínculos al contenido de SMS en [esta sección](../mobile/create-mobile-message.md#sms-content).

Para insertar vínculos profundos en contenido SMS, utilice la siguiente sintaxis:

```
{{url originalUrl='<<url>>' type='DEEPLINK' action='CLICK'}}
```

Reemplace `<<url>>` por su dirección URL de vinculación profunda real.

## Configuración en Journey Optimizer {#configuration}

Para poder utilizar vínculos profundos en correos electrónicos y SMS para sus aplicaciones móviles, complete los pasos de configuración a continuación.

>[!NOTE]
>
>Esta sección se aplica cuando usa **vínculos universales (iOS)** y **vínculos de aplicación (Android)** (vínculos profundos basados en HTTPS).

1. En Journey Optimizer, delegue el subdominio donde la vinculación profunda esté habilitada. [Más información](../configuration/delegate-subdomain.md)

1. Aloje el archivo AASA para iOS y el archivo assetLinks.json para Android en su subdominio. Póngase en contacto con el servicio de atención al cliente de [Adobe](https://helpx.adobe.com/es/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} o con su representante de Adobe y proporcione los siguientes detalles:

   * **Para iOS (AASA)**:
      * Subdominio delegado
      * ID de paquete de aplicaciones
   * **Para Android (assetLinks.json)**:
      * Subdominio delegado
      * ID de paquete de aplicaciones
      * Huella digital del certificado SHA-256

>[!IMPORTANT]
>
>La vinculación profunda a través de la infraestructura de Adobe se aplica cuando el seguimiento de vínculos está habilitado para su mensaje: en la [configuración de seguimiento de correo electrónico](message-tracking.md#enable-tracking) o en la sección **[!UICONTROL Seguimiento de acciones]** para campañas de SMS. El rastreo de clics en vínculos profundos utiliza direcciones URL en `/ee/v1/mclick/*`, que Adobe aloja y resuelve.
>
>Para **vínculos sin seguimiento**, la dirección URL no se reescribe a través de los sistemas de Adobe. Debe configurar los vínculos universales y los de la aplicación en sus propios dominios y alojamiento para que se abran correctamente en la aplicación.

## Implementación de aplicación móvil {#mobile-implementation}

En esta sección se explica cómo implementar vínculos profundos móviles con [!DNL Adobe Journey Optimizer] de modo que, en una configuración típica de **HTTPS** (vínculos universales y de aplicación), una sola dirección URL pueda:

* Abra una pantalla específica dentro de la aplicación móvil cuando esta esté instalada, o
* Abra el sitio web como alternativa cuando la aplicación no esté instalada.

Cuando el seguimiento de vínculos está habilitado para el mensaje, [!DNL Journey Optimizer] continúa realizando el seguimiento de estos clics, los incluye en los informes y puede usarlos en [experimentos de contenido](../content-management/content-experiment.md) si los ejecuta en el mensaje.

Esta sección proporciona patrones de implementación comunes para los vínculos profundos. La configuración exacta depende de la arquitectura de la aplicación y del marco de enrutamiento.

### iOS (vínculos universales) {#ios-implementation}

1. En Xcode, seleccione su destino mediante **[!UICONTROL Firma y capacidades]** > **[!UICONTROL + capacidad]** > **[!UICONTROL Dominios asociados]**.
1. Agregue entradas para los subdominios delegados, por ejemplo:

   ```text
   applinks:www.mybusiness.com
   applinks:data.email.mybusiness.com
   ```

1. Controle los vínculos universales en la aplicación y obtenga el vínculo original del encabezado de respuesta.

   +++ Ejemplo: iOS 13+ con escenas

   ```swift
   class SceneDelegate: UIResponder, UIWindowSceneDelegate {
   
       func scene(_ scene: UIScene,
                 continue userActivity: NSUserActivity) {
           guard userActivity.activityType == NSUserActivityTypeBrowsingWeb,
                 let incomingURL = userActivity.webpageURL else {
               return
           }
   
           handleUniversalLink(url: incomingURL)
       }
   
       private func handleUniversalLink(url: URL) {
           // Only handle AJO tracked mobile clicks
           guard url.host == "data.email.mybusiness.com",
                 url.path.hasPrefix("/ee/v1/mclick") else {
               // Could also handle direct www.mybusiness.com links here
               return
           }
   
           resolveTrackedUrlAndRoute(url)
       }
   
       private func resolveTrackedUrlAndRoute(_ trackedUrl: URL) {
           var request = URLRequest(url: trackedUrl)
           request.httpMethod = "GET"
   
           URLSession.shared.dataTask(with: request) { _, response, error in
               guard error == nil,
                     let httpResponse = response as? HTTPURLResponse,
                     let locationValue = httpResponse.allHeaderFields["Location"] as? String,
                     let finalUrl = URL(string: locationValue) else {
                   return
               }
   
               DispatchQueue.main.async {
                   self.routeToDestination(finalUrl)
               }
           }.resume()
       }
   
       private func routeToDestination(_ url: URL) {
           // Example: map URL paths to screens
           // https://www.mybusiness.com/dashboard/offers/coupons
           // → OffersViewController for Coupons
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>La aplicación debe realizar un **GET** en la dirección URL `mclick`, leer el encabezado **`Location`** y luego enrutar según la dirección URL **final**.
>
>No abra simplemente la dirección URL `mclick` en Safari, ya que esto no cumple el propósito de la vinculación profunda.

### Android (vínculos de la aplicación) {#android-implementation}

1. Añada el filtro de intención Vínculo de aplicación en la aplicación de Android.

   ```xml
   <activity
       android:name=".DeepLinkActivity"
       android:exported="true">
   
       <intent-filter android:autoVerify="true">
           <action android:name="android.intent.action.VIEW" />
           <category android:name="android.intent.category.DEFAULT" />
           <category android:name="android.intent.category.BROWSABLE" />
   
           <data
               android:scheme="https"
               android:host="data.email.mybusiness.com"
               android:pathPrefix="/ee/v1/mclick" />
       </intent-filter>
   
   </activity>
   ```

1. Implemente el controlador de vínculos profundos.

   +++ En Kotlin:

   ```kotlin
   class DeepLinkActivity : AppCompatActivity() {
   
       override fun onCreate(savedInstanceState: Bundle?) {
           super.onCreate(savedInstanceState)
   
           val trackedUri = intent?.data
           if (trackedUri == null ||
               trackedUri.host != "data.email.mybusiness.com" ||
               !trackedUri.path.orEmpty().startsWith("/ee/v1/mclick")) {
               finish()
               return
           }
   
           resolveTrackedUrlAndRoute(trackedUri)
       }
   
       private fun resolveTrackedUrlAndRoute(trackedUri: Uri) {
           lifecycleScope.launch(Dispatchers.IO) {
               try {
                   val finalUrl = followRedirect(trackedUri.toString())
                   withContext(Dispatchers.Main) {
                       routeToDestination(finalUrl)
                       finish()
                   }
               } catch (e: Exception) {
                   // Optionally log error, fallback to browser
                   finish()
               }
           }
       }
   
       private fun followRedirect(trackedUrl: String): Uri {
           val client = OkHttpClient.Builder()
               .followRedirects(false) // We want to read Location ourselves
               .build()
   
           val request = Request.Builder()
               .url(trackedUrl)
               .get()
               .build()
   
           client.newCall(request).execute().use { response ->
               val location = response.header("Location")
                   ?: throw IllegalStateException("Missing Location header")
               return Uri.parse(location)
           }
       }
   
       private fun routeToDestination(finalUri: Uri) {
           // Example: interpret https://www.mybusiness.com/dashboard/offers/coupons
           // and open the correct Activity / Fragment
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>Al igual que iOS, la aplicación debe llamar a la dirección URL `mclick` y utilizar el encabezado **`Location`** para determinar el destino final.
>
>Use `followRedirects(false)` para controlar la administración de redirecciones y poder registrar análisis con precisión si es necesario.
>
>La lógica de enrutamiento es específica de la aplicación. Defina una asignación clara entre las direcciones URL y las pantallas.

## Prácticas recomendadas {#deeplink-best-practices}

* **Usar rutas estables**: prefiere rutas resistentes a los cambios en la interfaz de usuario de la aplicación (por ejemplo, `/account/orders` en lugar de `/tab/3/view/2`).
* **Cuenta para rutas de acceso rastreadas**: Cuando el seguimiento de vínculos está habilitado, el vínculo en el que se hizo clic puede usar patrones de ruta rastreada (por ejemplo `/ee/v1/mclick/`). Asegúrese de que el enrutador pueda analizar la dirección URL final después de resolver el vínculo rastreado.
* **Mantener parámetros predecibles**: defina un esquema de parámetros coherente (por ejemplo, `?orderId=12345`).
* **Evite los datos confidenciales en las direcciones URL**: no coloque secretos ni datos personales directamente en la dirección URL de vinculación profunda.
* **Pruebe su enlace profundo**: Envíe una prueba y haga clic en el enlace profundo en un dispositivo donde la aplicación esté instalada.
* **Validar en dispositivos reales**: Los vínculos universales y los comportamientos de resolución de vínculos rastreados son más fiables de validar en dispositivos físicos que en simuladores.
* **Validar el enrutamiento del lado de la aplicación**: Si el vínculo profundo no abre la pantalla esperada, valide el enrutamiento del lado de la aplicación y el formato de URL (host/ruta/consulta y codificación de URL).
* **Tenga en cuenta la inicialización de la aplicación**: El comportamiento de los vínculos universales y de la aplicación es más confiable después de que la aplicación se haya instalado y abierto al menos una vez.

## Resolución de problemas y preguntas frecuentes {#troubleshooting-faq}

+++ La aplicación no se abre al pulsar el vínculo profundo.

* Compruebe que la dirección URL coincida con los patrones de host y ruta que administra su aplicación, incluidas las rutas de clics seguidos cuando el seguimiento de vínculos está habilitado (por ejemplo, las rutas en `/ee/v1/mclick/`).
* Para los vínculos universales iOS y los vínculos de la aplicación Android, confirme que la asociación de dominios (AASA / `assetlinks.json`) está configurada correctamente y es accesible.
* Realizar pruebas en un dispositivo real (los simuladores/emuladores pueden comportarse de forma diferente para la asociación de vínculos).

+++

+++ La aplicación se abre, pero no navega a la pantalla esperada.

* Confirme que el enrutador del lado de la aplicación analiza correctamente la ruta o consulta de la URL.
* Comprobar codificación de URL: los caracteres reservados deben estar codificados en URL.
* Valide los nombres y valores de los parámetros para que coincidan con lo que espera el enrutador.

+++

+++ ¿Qué sucede si la aplicación no está instalada?

* Si el sitio web puede proporcionar la misma URL HTTPS, el vínculo puede abrir una página web como alternativa cuando la aplicación no está instalada (configure el destino web y el enrutamiento en consecuencia).

+++

+++ ¿Cómo puedo incluir de forma segura caracteres especiales en los parámetros?

Valores de parámetro de consulta de codificación de URL. Esto reduce los problemas de envío y procesamiento y ayuda a evitar errores de análisis en la aplicación.

+++

+++ ¿Cómo probamos de extremo a extremo?

* Cree una prueba con un vínculo profundo y haga clic en ella en dispositivos iOS y Android (escenarios instalados y no instalados).
* Validar:
   * El valor final del vínculo de correo electrónico o SMS (host/ruta/consulta)
   * La asociación a nivel del sistema operativo (si se utilizan vínculos universales o de aplicación)
   * El resultado del enrutamiento en la aplicación

+++

+++ Tengo una aplicación, pero diferentes subdominios para la organización. ¿Debo solicitar que se cree AASA y assetLinks.json para cada subdominio?

Sí. Si desea vincular en profundidad todos los subdominios delegados, solicite la configuración AASA y `assetlinks.json` para cada subdominio que admita la función.

+++

+++ ¿La dirección URL que configuro debe tener un formato de vinculación profunda (por ejemplo, `appname://path`)?

Puede utilizar un esquema de dirección URL personalizado (por ejemplo, `appname://path`), pero el método recomendado es un vínculo universal o de aplicación (`https://`), que coincide con la configuración basada en HTTPS de las secciones de configuración e implementación de esta página.

+++

+++ ¿Estarán disponibles los parámetros de UTM de la dirección URL en la aplicación móvil de Analytics?

Sí. Los parámetros de UTM que configuró en [!DNL Journey Optimizer] se incluyen en la dirección URL final devuelta en el encabezado `Location` cuando la aplicación realiza una GET en la dirección URL `mclick`, de modo que puede utilizarlos para el análisis en la aplicación.

+++

+++ ¿Cuál es la experiencia del usuario con las URL de `/ee/v1/click/`?

El vínculo se abre en el explorador web predeterminado del dispositivo (comportamiento estándar de rastreo de clics), en lugar de tratarse como un vínculo profundo de la aplicación a través del flujo `mclick` descrito en esta página.

+++
