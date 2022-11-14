---
title: Enviar ofertas mediante la API de Edge Decisioning
description: El SDK web de Adobe Experience Platform le permite recuperar y procesar ofertas personalizadas que haya creado mediante API o la Biblioteca de ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 4e2dc0d6-4610-4a2f-8388-bc58182b227f
source-git-commit: a2d05c7f2c00172a6f4e7b9d9f60d1732c91af8a
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 2%

---

# Enviar ofertas mediante la API de Edge Decisioning {#edge-decisioning-api}

## Introducción y requisitos previos {#edge-overview-and-prerequisites}

La variable [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview) es una biblioteca JavaScript del lado del cliente que permite a los clientes de Adobe Experience Cloud interactuar con los distintos servicios del Experience Cloud a través de la red perimetral del Experience Platform.

El SDK web del Experience Platform admite la consulta de las soluciones de personalización en el Adobe, incluida la gestión de decisiones, lo que le permite recuperar y procesar ofertas personalizadas que haya creado mediante API o la biblioteca de ofertas. Para obtener instrucciones más detalladas, consulte la documentación de [creación de una oferta](../../get-started/starting-offer-decisioning.md).

Existen dos maneras de implementar la administración de decisiones con la variable [SDK web de plataforma](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview). Una forma está dirigida a los desarrolladores y requiere conocimiento de los sitios web y programación. La otra forma es utilizar la interfaz de usuario de Adobe Experience Platform para configurar ofertas, que solo requiere que se haga referencia a una pequeña secuencia de comandos en el encabezado de la página del HTML.

Consulte la documentación de [gestión de decisiones](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=en#enabling-offer-decisioning) para obtener más información sobre cómo ofrecer ofertas personalizadas mediante el SDK web de Adobe Experience Platform.

>[!NOTE]
>
>El uso de Administración de decisiones en el SDK web de Adobe Experience Platform solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Si desea aprovechar esta función, póngase en contacto con el administrador de cuentas de Adobe.

## SDK web de Adobe Experience Platform {#aep-web-sdk}

El SDK web de Platform sustituye a los siguientes SDK:

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

El SDK no combinó estas bibliotecas y es una nueva implementación desde cero. Para utilizarla, primero debe seguir estos pasos:

1. Asegúrese de que su organización tiene los permisos adecuados para utilizar el SDK y de que ha configurado los permisos correctamente.

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [Configurar el conjunto de datos](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=en) en la ficha Recopilación de datos de su cuenta en Adobe Experience Cloud.

1. Instale el SDK. Existen varios métodos para hacerlo, que se tratan en la [Instalación de la página SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en). Esta página continuará con cada método de implementación diferente.

Para utilizar el SDK, debe tener un [esquema](../../../data/get-started-schemas.md) y [datastream](../../../start/get-started-datasets.md) definida.

<!-- ****TODO - Configure schema**** -->

Para personalizar ofertas, debe configurar separadamente la personalización o los perfiles.

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

Para configurar el SDK para la administración de decisiones, siga cualquiera de los dos pasos siguientes:

## Opción 1: Instalar la extensión y la implementación de etiquetas con Launch

Esta opción es más fácil de usar para las personas que tengan menos experiencia en codificación.

1. [Crear una propiedad de etiqueta](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en)

1. [Añadir el código de incrustación de ](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=en)

1. Instale y configure la extensión del SDK web de Adobe Experience Platform con el Datastream que ha creado seleccionando la configuración en la lista desplegable &quot;Datastream&quot;. Consulte la documentación sobre [extensiones](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en).

   ![SDK web de Adobe Experience Platform](../../assets/installed-catalog-web-sdk.png)

   ![Configurar extensión](../../assets/configure-sdk-extension.png)

1. Cree los elementos necesarios [Elementos de datos](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=en). Como mínimo, debe crear un mapa de identidad del SDK web de plataforma y un elemento de datos de objeto XDM del SDK web de plataforma .

   ![Mapa de identidad](../../assets/sdk-identity-map.png)

   ![Objeto XDM](../../assets/xdm-object.png)

1. Cree su [Reglas](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=en):

   Añada una acción de Platform Web SDK Send Event y añada los decisionScopes relevantes a la configuración de esa acción

   ![Renderizar oferta](../../assets/rule-render-offer.png)

   ![Solicitar oferta](../../assets/rule-request-offer.png)

1. [Crear y publicar](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en) una biblioteca que contiene todas las reglas, elementos de datos y extensiones relevantes que ha configurado.

## Opción 2: Implementar manualmente con la versión independiente prediseñada

Estos son los pasos necesarios para utilizar la administración de decisiones mediante la instalación independiente prediseñada del SDK web. En esta guía se supone que es la primera vez que implementa el SDK, por lo que es posible que no se le apliquen todos los pasos. Esta guía también asume alguna experiencia de desarrollo.

Incluya el siguiente fragmento de JavaScript de la Opción 2: La versión independiente prediseñada en [esta página](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en) en el `<head>` de su página HTML.

```
javascript
    <script>
        !function(n,o){o.forEach(function(o){n[o]||((n.__alloyNS=n.__alloyNS||
        []).push(o),n[o]=function(){var u=arguments;return new Promise(
        function(i,l){n[o].q.push([i,l,u])})},n[o].q=[])})}
        (window,["alloy"]);
    </script>
    <script src="https://cdn1.adoberesources.net/alloy/2.6.4/alloy.js" async></script>
```

Necesitará dos ID de su cuenta de Adobe para configurar la configuración del SDK: edgeConfigId y orgId. edgeConfigId es el mismo que su ID de almacén de datos, que debería haber configurado en los requisitos previos.

Para encontrar su ID edgeConfigID/datastream, vaya a Recopilación de datos y seleccione su Datastream. Para encontrar su orgId, vaya a su perfil.

Configure el SDK en JavaScript siguiendo las instrucciones de esta página. Siempre usará edgeConfigId y orgId en la función de configuración. La documentación también describe qué parámetros opcionales existen para la configuración. La configuración final puede tener este aspecto:

```
javascript
    alloy("configure", {
        "edgeConfigId": "12345678-0ABC-DEF-GHIJ-KLMNOPQRSTUV",                            
        "orgId":"ABCDEFGHIJKLMNOPQRSTUVW@AdobeOrg",
        "debugEnabled": true,
        "edgeDomain": "edge.adobedc.net",
        "clickCollectionEnabled": true,
        "idMigrationEnabled": true,
        "thirdPartyCookiesEnabled": true,
        "defaultConsent":"in"  
    });
```

Instale la extensión de Chrome de Debugger para utilizarla con la depuración. Se puede encontrar aquí: <https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob>

A continuación, inicie sesión en la cuenta dentro de Debugger. A continuación, vaya a Registros y asegúrese de que está conectado al espacio de trabajo correcto. Ahora, copie la versión codificada base64 del ámbito de decisión de su oferta.

Al editar el sitio web, incluya el script con la configuración y la variable `sendEvent` para enviar el ámbito de decisión al Adobe.

**Ejemplo**:

```
javascript
    alloy("sendEvent", {
        "decisionScopes": 
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    });
```

Consulte el siguiente ejemplo sobre cómo gestionar la respuesta:

```
javascript
    alloy("sendEvent", {
        "decisionScopes":
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    }).then(function(result) {
        Object.entries(result).forEach(([key, value]) => {
            console.log(key, value);
        });
    });
```

Puede utilizar el depurador para comprobar que se ha conectado correctamente a la red de Edge.

>[!NOTE]
>
>Si no ve una conexión con el borde en los registros, es posible que tenga que deshabilitar el bloqueador de anuncios.

Consulte de nuevo cómo creó la oferta y el formato utilizado. Según los criterios que se cumplan en la decisión, se le devolverá una oferta que contenga la información especificada al crearla en Adobe Experience Platform.

En este ejemplo, el JSON que se va a devolver es:

```
json
{
   "name":"ABC Test",
   "description":"This is a test offer", 
   "link":"https://sampletesting.online/",
   "image":"https://sample-demo-URL.png"
}
```

Gestione el objeto Response y analice los datos que necesite. Como puede enviar varios ámbitos de decisión en uno `sendEvent` , su respuesta puede ser ligeramente diferente.

```
json
    {
        "id": "abrxgl843d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"ABC Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
]
}
```

```
json
{
    "propositions": 
    [
    {
        "renderAttempted": false,
        "id": "e15ecb09-993e-4b66-93d8-0a4c77e3d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"Claire Hubacek Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
    ]
}
```

En este ejemplo, la ruta necesaria para gestionar y utilizar los detalles específicos de la oferta en la página web era: `result['decisions'][0]['items'][0]['data']['content']`

Para establecer las variables JS:

```
javascript
const offer = JSON.parse(result['decisions'][0]['items'][0]['data']['content']);

let offerURL = offer['link'];
let offerDescription = offer['description'];
let offerImageURL = offer['image'];

document.getElementById("offerDescription").innerHTML = offerDescription;
document.getElementById('offerImage').src = offerImageURL;
```

## Limitaciones

Algunas restricciones de oferta actualmente no son compatibles con los flujos de trabajo móviles de Experience Edge, por ejemplo, Restricción. El valor del campo Restricción especifica el número de veces que se puede presentar una oferta en todos los usuarios. Para obtener más información, consulte [Adición de restricciones a una oferta](../../offer-library/add-constraints.md#capping).
