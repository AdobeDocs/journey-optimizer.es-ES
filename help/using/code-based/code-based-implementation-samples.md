---
title: Ejemplos de implementación basada en código
description: Esta página muestra ejemplos del método de implementación para la función basada en código de Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: e5ae8b4e-7cd2-4a1d-b2c0-8dafd5c4cdfd
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '823'
ht-degree: 7%

---

# Ejemplos de métodos de implementación basados en código {#implementation-samples}

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción al canal basado en código](get-started-code-based.md)
* [Requisitos previos basados en código](code-based-prerequisites.md)
* **[Ejemplos de implementación basada en código](code-based-implementation-samples.md)**
* [Creación de experiencias basadas en código](create-code-based.md)

>[!ENDSHADEBOX]

La experiencia basada en código admite cualquier tipo de implementación del cliente. En esta página puede encontrar ejemplos para cada método de implementación:

* [Lado del cliente](#client-side-implementation)
* [Lado del servidor](#server-side-implementation)
* [Híbrido](#hybrid-implementation)

También puede seguir a [este vínculo](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} para encontrar implementaciones de muestra para diferentes casos de uso de personalización y experimentación. Compruébelos y ejecútelos para comprender mejor cuáles son los pasos de implementación necesarios y cómo funciona el flujo de personalización de principio a fin.

## Implementación del lado del cliente {#client-side-implementation}

Si tiene una implementación del lado del cliente, puede utilizar uno de los SDK de cliente de AEP: SDK web de AEP o SDK móvil de AEP. Los pasos siguientes describen el proceso de recuperar el contenido publicado en Edge por las campañas de experiencia basadas en código en una implementación de SDK web de muestra y mostrar el contenido personalizado.

### Funcionamiento

1. [SDK web](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es){target="_blank"} se incluye en la página.

1. Debe utilizar el `sendEvent` y especifique el URI de superficie para recuperar contenido de personalización.

   ```javascript
   alloy("sendEvent", {
   renderDecisions: true,
   personalization: {
       surfaces: ["#sample-json-content"],
   },
   }).then(applyPersonalization("#sample-json-content"));
   ```

1. Los elementos de experiencia basados en código deben aplicarse manualmente mediante el código de implementación (utilizando el [`applyPersonalization`](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/ajo/personalization-client-side/public/script.js){target="_blank"} método) para actualizar el DOM en función de la decisión.

1. Para las campañas de experiencia basadas en código, los eventos de visualización deben enviarse manualmente para indicar cuándo se ha mostrado el contenido. Esto se realiza mediante la variable `sendEvent` comando.

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

### Observaciones clave

**Cookies**

Las cookies se utilizan para mantener la identidad del usuario y la información de clúster. Al utilizar una implementación del lado del cliente, el SDK web gestiona el almacenamiento y el envío de estas cookies automáticamente durante el ciclo vital de la solicitud.

| Cookie | Finalidad | Almacenado por | Enviado por |
| ------------------------ | -------------------------------------------------------------------------- | --------- | ------- |
| kndctr_AdobeOrg_identity | Contiene detalles de identidad del usuario | SDK web | SDK web |
| kndctr_AdobeOrg_cluster | Indica qué clúster de Experience Edge se debe usar para cumplir las solicitudes | SDK web | SDK web |

**Solicitar ubicación**

Las solicitudes a la API de Adobe Experience Platform son necesarias para obtener propuestas y enviar una notificación de visualización. Al utilizar una implementación del lado del cliente, el SDK web realiza estas solicitudes cuando el `sendEvent` se utiliza el comando.

| Solicitud | Realizado por |
| ---------------------------------------------- | ----------------------------------- |
| interactuar solicitud para obtener propuestas | SDK web mediante el comando sendEvent |
| interactuar solicitud para enviar notificaciones de visualización | SDK web mediante el comando sendEvent |

**Diagrama de flujo**

![](assets/code-based-client-side-implementation.png)

## Implementación del lado del servidor {#server-side-implementation}

Si tiene una implementación del lado del servidor, puede utilizar una de la API de red de AEP Edge. Los pasos siguientes describen el proceso de recuperar el contenido publicado en Edge por las campañas de experiencia basadas en código en una implementación de API de red perimetral de ejemplo para una página web y mostrar el contenido personalizado.

### Funcionamiento

1. La página web se solicita y cualquier cookie previamente almacenada por el explorador lleva el prefijo `kndctr_` están incluidos.
1. Cuando se solicita la página desde el servidor de aplicaciones, se envía un evento a [punto final de recopilación de datos interactivos](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html) para recuperar contenido de personalización. Esta aplicación de ejemplo utiliza algunos métodos de ayuda para simplificar la creación y el envío de solicitudes a la API (consulte [aepEdgeClient.js](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/common/aepEdgeClient.js){target="_blank"}). Pero la solicitud es simplemente una `POST` con una carga útil que contiene un evento y una consulta. Las cookies (si están disponibles) del paso anterior se incluyen con la solicitud en el `meta>state>entries` matriz.

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

1. La experiencia JSON de la campaña de experiencia basada en código se lee desde la respuesta y se utiliza al producir la respuesta del HTML.
1. Para las campañas de experiencia basadas en código, los eventos de visualización deben enviarse manualmente en la implementación para indicar cuándo se ha mostrado el contenido de la campaña. En este ejemplo, la notificación se envía del lado del servidor durante el ciclo de vida de la solicitud.

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

| Cookie | Finalidad | Almacenado por | Enviado por |
| ------------------------ | -------------------------------------------------------------------------- | ------------------ | ------------------ |
| kndctr_AdobeOrg_identity | Contiene detalles de identidad del usuario | servidor de aplicaciones | servidor de aplicaciones |
| kndctr_AdobeOrg_cluster | Indica qué clúster de Experience Edge se debe usar para cumplir las solicitudes | servidor de aplicaciones | servidor de aplicaciones |

**Solicitar ubicación**

Las solicitudes a la API de Adobe Experience Platform son necesarias para obtener propuestas y enviar una notificación de visualización. Al utilizar una implementación del lado del cliente, el SDK web realiza estas solicitudes cuando el `sendEvent` se utiliza el comando.

| Solicitud | Realizado por |
| ---------------------------------------------- | ------------------------------------------------------------ |
| interactuar solicitud para obtener propuestas | servidor de aplicaciones llamando a la API de Adobe Experience Platform |
| interactuar solicitud para enviar notificaciones de visualización | servidor de aplicaciones llamando a la API de Adobe Experience Platform |

**Diagrama de flujo**

![](assets/code-based-server-side-implementation.png)

## Implementación híbrida {#hybrid-implementation}

Si tiene una implementación híbrida, consulte los vínculos siguientes.

* Adobe Tech Blog: [Personalización híbrida en el SDK web de Adobe Experience Platform](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}
* Documentación de SDK: [Personalización híbrida mediante SDK web y API de servidor de red perimetral](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/hybrid-personalization.html){target="_blank"}
