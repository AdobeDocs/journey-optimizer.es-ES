---
title: Ejemplos de implementación basada en código
description: Esta página muestra ejemplos del método de implementación para la función basada en código de Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
exl-id: e5ae8b4e-7cd2-4a1d-b2c0-8dafd5c4cdfd
source-git-commit: bf0a6fa496a08348be16896a7f2313882eb97c06
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 2%

---

# Ejemplos de métodos de implementación basados en código {#implementation-samples}

La experiencia basada en código admite cualquier tipo de implementación del cliente. En esta página puede encontrar ejemplos para cada método de implementación:

* [Lado del cliente](#client-side-implementation)
* [Del lado del servidor](#server-side-implementation)
* [Híbrido](#hybrid-implementation)

>[!IMPORTANT]
>
>Siga [este vínculo](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} para encontrar implementaciones de muestra para diferentes casos de uso de personalización y experimentación. Compruébelos y ejecútelos para comprender mejor cuáles son los pasos de implementación necesarios y cómo funciona el flujo de personalización de principio a fin.

## Implementación del lado del cliente {#client-side-implementation}

Si tiene una implementación del lado del cliente, puede utilizar uno de los SDK de cliente de AEP: SDK web de AEP o SDK móvil de AEP.

* Los pasos [debajo de](#client-side-how) describen el proceso de recuperar el contenido publicado en el perímetro por los recorridos de experiencia basados en código y las campañas en una implementación de muestra de **SDK web** y la visualización del contenido personalizado.

* Los pasos para implementar el canal basado en código mediante **SDK móvil** se describen en [este tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"}.

  >[!NOTE]
  >
  >Hay implementaciones de muestra disponibles para casos de uso móvil para [aplicación iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} y [aplicación Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}.

### Cómo funciona: SDK web {#client-side-how}

1. [El SDK web](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"} se incluye en la página.

1. Debe usar el comando `sendEvent` y especificar el [URI de superficie](code-based-surface.md)<!--( or location/path)--> para recuperar contenido de personalización.

   ```javascript
   alloy("sendEvent", {
   renderDecisions: true,
   personalization: {
       surfaces: ["#sample-json-content"],
   },
   }).then(applyPersonalization("#sample-json-content"));
   ```

1. El código de implementación debe aplicar manualmente los elementos de experiencia basados en código (mediante el método [`applyPersonalization`](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/ajo/personalization-client-side/public/script.js){target="_blank"}) para actualizar el DOM según la decisión.

1. Para las campañas y los recorridos de experiencias basados en código, los eventos de visualización deben enviarse manualmente para indicar cuándo se ha mostrado el contenido. Esto se realiza mediante el comando `sendEvent`.

   ```javascript
   function sendDisplayEvent(decision) {
     const { id, scope, scopeDetails = {} } = decision;
   
     alloy("sendEvent", {
   
       xdm: {
         eventType: "decisioning.propositionDisplay",
         _experience: {
           decisioning: {
             propositions: [
               {
                 id: id,
                 scope: scope,
                 scopeDetails: scopeDetails,
               },
             ],
           },
         },
       },
     });
   }
   ```

1. En el caso de las campañas y los recorridos de experiencias basados en código, los eventos de interacción deben enviarse manualmente para indicar cuándo un usuario ha interactuado con el contenido. Esto se realiza mediante el comando `sendEvent`.

   ```javascript
   function sendInteractEvent(label, proposition) {
     const { id, scope, scopeDetails = {} } = proposition;
   
     alloy("sendEvent", {
   
       xdm: {
         eventType: "decisioning.propositionInteract",
         _experience: {
           decisioning: {
             propositions: [
               {
                 id: id,
                 scope: scope,
                 scopeDetails: scopeDetails,
               },
             ],
             propositionEventType: {
               interact: 1
             },
             propositionAction: {
               label: label
             },
           },
         },
       },
     });
   }
   ```

### Observaciones clave

**Cookies**

Las cookies se utilizan para mantener la identidad del usuario y la información de clúster. Al utilizar una implementación del lado del cliente, el SDK web gestiona el almacenamiento y el envío de estas cookies automáticamente durante el ciclo vital de la solicitud.

| Cookie | Objetivo | Almacenado por | Enviado por |
| ------------------------ | -------------------------------------------------------------------------- | --------- | ------- |
| kndctr_AdobeOrg_identity | Contiene detalles de identidad del usuario | SDK web | SDK web |
| kndctr_AdobeOrg_cluster | Indica qué clúster de Experience Edge se debe usar para cumplir las solicitudes | SDK web | SDK web |

**Solicitar ubicación**

Las solicitudes a la API de Adobe Experience Platform son necesarias para obtener propuestas y enviar una notificación de visualización. Al utilizar una implementación del lado del cliente, el SDK web realiza estas solicitudes cuando se utiliza el comando `sendEvent`.

| Solicitud | Realizado por |
| ---------------------------------------------- | ----------------------------------- |
| interactuar solicitud para obtener propuestas | SDK web mediante el comando sendEvent |
| interactuar solicitud para enviar notificaciones de visualización | SDK web mediante el comando sendEvent |

**Diagrama de flujo**

![](assets/code-based-client-side-implementation.png)

## Implementación del lado del servidor {#server-side-implementation}

Si tiene una implementación del lado del servidor, puede utilizar una en la API de Edge Network de AEP.

Los pasos siguientes describen el proceso de recuperar el contenido publicado en Edge por los recorridos de experiencia basados en código y las campañas en una implementación de API de Edge Network de muestra para una página web y mostrar el contenido personalizado.

### Funcionamiento

1. Se solicita la página web y se incluyen todas las cookies almacenadas anteriormente por el explorador con el prefijo `kndctr_`.
1. Cuando se solicita la página desde el servidor de aplicaciones, se envía un evento al [extremo interactivo de recopilación de datos](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html) para recuperar el contenido de personalización. Esta aplicación de ejemplo utiliza algunos métodos de ayuda para simplificar la generación y el envío de solicitudes a la API (consulte [aepEdgeClient.js](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/common/aepEdgeClient.js){target="_blank"}). Pero la solicitud es simplemente un `POST` con una carga útil que contiene un evento y una consulta. Las cookies (si están disponibles) del paso anterior se incluyen con la solicitud en la matriz `meta>state>entries`.

   ```javascript
   fetch(
     "https://edge.adobedc.net/ee/v2/interact?dataStreamId=abc&requestId=123",
     {
       headers: {
         accept: "*/*",
         "accept-language": "en-US,en;q=0.9",
         "cache-control": "no-cache",
         "content-type": "text/plain; charset=UTF-8",
         pragma: "no-cache",
         "sec-fetch-dest": "empty",
         "sec-fetch-mode": "cors",
         "sec-fetch-site": "cross-site",
         "sec-gpc": "1",
         "Referrer-Policy": "strict-origin-when-cross-origin",
         Referer: "https://localhost/",
       },
       body: JSON.stringify({
         event: {
           xdm: {
             eventType: "decisioning.propositionFetch",
             web: {
               webPageDetails: {
                 URL: "https://localhost/",
               },
               webReferrer: {
                 URL: "",
               },
             },
             identityMap: {
               FPID: [
                 {
                   id: "xyz",
                   authenticatedState: "ambiguous",
                   primary: true,
                 },
               ],
             },
             timestamp: "2022-06-23T22:21:00.878Z",
           },
           data: {},
         },
         query: {
           identity: {
             fetch: ["ECID"],
           },
           personalization: {
             schemas: [
               "https://ns.adobe.com/personalization/default-content-item",
               "https://ns.adobe.com/personalization/html-content-item",
               "https://ns.adobe.com/personalization/json-content-item",
               "https://ns.adobe.com/personalization/redirect-item",
               "https://ns.adobe.com/personalization/dom-action",
             ],
             surfaces: ["web://localhost/","web://localhost/#sample-json-content"],
           },
         },
         meta: {
           state: {
             domain: "localhost",
             cookiesEnabled: true,
             entries: [
               {
                 key: "kndctr_XXX_AdobeOrg_identity",
                 value: "abc123",
               },
               {
                 key: "kndctr_XXX_AdobeOrg_cluster",
                 value: "or2",
               },
             ],
           },
         },
       }),
       method: "POST",
     }
   ).then((res) => res.json());
   ```

1. La experiencia JSON de los recorridos de experiencia basados en código y la campaña se lee desde la respuesta y se utiliza al producir la respuesta del HTML.

1. Para las campañas y los recorridos de experiencias basados en código, los eventos de visualización deben enviarse manualmente en la implementación para indicar cuándo se ha mostrado el recorrido o el contenido de la campaña. En este ejemplo, la notificación se envía del lado del servidor durante el ciclo de vida de la solicitud.

   ```javascript
   function sendDisplayEvent(aepEdgeClient, req, propositions, cookieEntries) {
     const address = getAddress(req);
   
     aepEdgeClient.interact(
       {
         event: {
           xdm: {
             web: {
               webPageDetails: { URL: address },
               webReferrer: { URL: "" },
             },
             timestamp: new Date().toISOString(),
             eventType: "decisioning.propositionDisplay",
             _experience: {
               decisioning: {
                 propositions: propositions.map((proposition) => {
                   const { id, scope, scopeDetails } = proposition;
   
                   return {
                     id,
                     scope,
                     scopeDetails,
                   };
                 }),
               },
             },
           },
         },
         query: { identity: { fetch: ["ECID"] } },
         meta: {
           state: {
             domain: "",
             cookiesEnabled: true,
             entries: [...cookieEntries],
           },
         },
       },
       {
         Referer: address,
       }
     );
   }
   ```

1. Cuando se devuelve la respuesta del HTML, el servidor de aplicaciones establece las cookies de identidad y de clúster en la respuesta.

### Observaciones clave

**Cookies**

Las cookies se utilizan para mantener la identidad del usuario y la información de clúster. Al utilizar una implementación del lado del servidor, el servidor de aplicaciones debe gestionar el almacenamiento y el envío de estas cookies durante el ciclo vital de la solicitud.

| Cookie | Objetivo | Almacenado por | Enviado por |
| ------------------------ | -------------------------------------------------------------------------- | ------------------ | ------------------ |
| kndctr_AdobeOrg_identity | Contiene detalles de identidad del usuario | servidor de aplicaciones | servidor de aplicaciones |
| kndctr_AdobeOrg_cluster | Indica qué clúster de Experience Edge se debe usar para cumplir las solicitudes | servidor de aplicaciones | servidor de aplicaciones |

**Solicitar ubicación**

Las solicitudes a la API de Adobe Experience Platform son necesarias para obtener propuestas y enviar una notificación de visualización. Al utilizar una implementación del lado del cliente, el SDK web realiza estas solicitudes cuando se utiliza el comando `sendEvent`.

| Solicitud | Realizado por |
| ---------------------------------------------- | ------------------------------------------------------------ |
| interactuar solicitud para obtener propuestas | servidor de aplicaciones llamando a la API de Adobe Experience Platform |
| interactuar solicitud para enviar notificaciones de visualización | servidor de aplicaciones llamando a la API de Adobe Experience Platform |

**Diagrama de flujo**

![](assets/code-based-server-side-implementation.png)

## Implementación híbrida {#hybrid-implementation}

Si tiene una implementación híbrida, consulte los vínculos siguientes.

* Blog técnico de Adobe: [Personalization híbrido en el SDK web de Adobe Experience Platform](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}
* Documentación del SDK: [Personalización híbrida mediante SDK web y API de servidor Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/hybrid-personalization.html){target="_blank"}
