---
title: Configuración de tarjetas de contenido en Web SDK
description: Configuración de la compatibilidad con tarjetas de contenido en SDK web
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: bb67b55f-2eac-4775-a9f5-78288009477e
source-git-commit: 37862682a25843ce138c076e443f6d9b6229ece3
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 4%

---

# Configuración de la compatibilidad con tarjetas de contenido en SDK web {#content-card-configuration-sdk}

Este ejemplo muestra cómo recuperar tarjetas de contenido de Adobe Journey Optimizer (AJO) mediante Adobe Experience Platform. Al aprovechar [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/home), el contenido de personalización se recupera y se procesa por completo en el lado del cliente.

Tras la carga inicial de la página, la página muestra su estado predeterminado. Sin embargo, si interactúa con los botones **Depositar fondos** o **Compartir en medios sociales**, aparecerán tarjetas de contenido adicionales. Estas tarjetas se activan por condiciones del lado del cliente, lo que garantiza que se muestren solo cuando se realizan acciones específicas.

![](assets/content-card-web-1.png)

## Ejecución del ejemplo {#run-sample}

>[!PREREQUISITES]
>
>Debe instalar node y npm. [Consulte esta documentación](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)


1. Configure los certificados SSL locales para HTTPS. Estos ejemplos requieren certificados SSL firmados localmente para proporcionar contenido a través de HTTPS:

   1. Instale `mkcert` en su equipo.

   1. Después de la instalación, ejecute `mkcert -install` para instalar el certificado `mkcert root`.

1. Clone el repositorio en el equipo local.

1. Abra un terminal y vaya a la carpeta del ejemplo.

1. Instale las dependencias requeridas ejecutando `npm install`.

1. Inicie la aplicación ejecutando `npm start`.

1. Abra el explorador web y vaya a `https://localhost`.

## Funcionamiento {#setup}

1. Incluya y configure [Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/home) en la página con la configuración del archivo `.env` en la carpeta de ejemplo.

   ```
   <script src="https://cdn1.adoberesources.net/alloy/2.18.0/alloy.min.js" async></script>
   alloy("configure", {
       defaultConsent: "in",
       edgeDomain: "{{edgeDomain}}",
       edgeConfigId: "{{edgeConfigId}}",
       orgId:"{{orgId}}",
       debugEnabled: false,
       personalizationStorageEnabled: true,
       thirdPartyCookiesEnabled: false
   });
   ```

1. Utilice el comando `sendEvent` para obtener contenido personalizado.

   ```
   alloy("sendEvent", {
       renderDecisions: true,
       personalization: {
           surfaces: ["web://alloy-samples.adobe.com/#content-cards-sample"],
       },
   });
   ```

1. Suscríbase a tarjetas de contenido para una superficie específica mediante el comando `subscribeRulesetItems`. Cada vez que se evalúen los conjuntos de reglas, controle el objeto de resultado en la llamada de retorno, que contendrá `propositions` con datos de la tarjeta de contenido.

   ```
   const contentCardManager = createContentCardManager("content-cards");
   
   alloy("subscribeRulesetItems", {
       surfaces: ["web://alloy-samples.adobe.com/#content-cards-sample"],
       schemas: ["https://ns.adobe.com/personalization/message/content-card"],
       callback: (result, collectEvent) => {
           const { propositions = [] } = result;
           contentCardManager.refresh(propositions, collectEvent);
       },
   });
   ```

1. Administre la representación de tarjetas de contenido y envíe `interact` y `display` eventos utilizando el objeto `contentCardsManager` encontrado en `script.js`. Extraer, ordenar y procesar tarjetas de contenido de las propuestas recibidas.

   ```
   const createContentCard = (proposition, item) => {
       const { data = {}, id } = item;
       const {
           content = {},
           meta = {},
           publishedDate,
           qualifiedDate,
           displayedDate,
       } = data;
   
       return {
           id,
           ...content,
           meta,
           qualifiedDate,
           displayedDate,
           publishedDate,
           getProposition: () => proposition,
       };
   };
   
   const extractContentCards = (propositions) =>
       propositions
           .reduce((allItems, proposition) => {
           const { items = [] } = proposition;
   
           return [
               ...allItems,
               ...items.map((item) => createContentCard(proposition, item)),
           ];
       }, [])
       .sort(
           (a, b) =>
               b.qualifiedDate - a.qualifiedDate || b.publishedDate - a.publishedDate
       );
   
   const contentCards = extractContentCards(propositions);
   ```

1. Procese las tarjetas de contenido en función de los detalles definidos para cada campaña. Cada tarjeta incluye `title`, `body`, `imageUrl` y otros valores de datos personalizados.

   ```
   const renderContentCards = () => {
       const contentCardsContainer = document.getElementById(containerElementId);
       contentCardsContainer.addEventListener("click", handleContentCardClick);
   
       let contents = "";
   
       contentCards.forEach((card) => {
           const { id, title, body, imageUrl, meta = {} } = card;
           const { buttonLabel = "" } = meta;
   
           contents += `
               <div class="col">
                   <div data-id="${id}" class="card h-100">
                       <img src="${imageUrl}" class="card-img-top" alt="...">
                       <div class="card-body d-flex flex-column">
                           <h5 class="card-title">${title}</h5>
                           <p class="card-text">${body}</p>
                           <a href="#" class="mt-auto btn btn-primary">${buttonLabel}</a>
                       </div>
                   </div>
                </div>
            `;
       });
   
       contentCardsContainer.innerHTML = contents;
       collectEvent(
           "display",
           contentCards.map((card) => card.getProposition())
        );
   };
   ```

1. Cuando se invoca la llamada de retorno `subscribeRulesetItems`, también se proporciona una función de conveniencia llamada `collectEvent`. Esta función se utiliza para enviar eventos de Experience Edge para rastrear interacciones, visualizaciones y otras acciones del usuario. En este ejemplo, collectEvent rastrea cuándo se hace clic en una tarjeta de contenido. Además, si se hace clic en el botón de la tarjeta de contenido, el explorador se dirigirá al `actionUrl` especificado por la campaña.

   ```
   const handleContentCardClick = (evt) => {
       const cardEl = evt.target.closest(".card");
   
       if (!cardEl) {
           return;
       }
   
       const isAnchor = evt.target.nodeName === "A";
       const card = contentCards.find((card) => card.id === cardEl.dataset.id);
   
       if (!card) {
           return;
       }
   
       collectEvent("interact", [card.getProposition()]);
   
       if (isAnchor) {
           evt.preventDefault();
           evt.stopImmediatePropagation();
           const { actionUrl } = card;
           if (actionUrl && actionUrl.length > 0) {
               window.location.href = actionUrl;
           }
       }
   };
   ```

## Observaciones clave {#key-observations}

### personalizationStorageEnabled

La opción `personalizationStorageEnabled` se ha establecido en `true` en el comando `configure`. Esto garantiza que las tarjetas de contenido cualificadas anteriormente se almacenen y sigan mostrándose en las sesiones de los usuarios.

### Activadores

Las tarjetas de contenido admiten déclencheur personalizados evaluados por el cliente. Cuando se cumple una regla de déclencheur, se muestran tarjetas de contenido adicionales. Este ejemplo utiliza cuatro campañas diferentes, una para cada tarjeta de contenido, todas compartiendo la misma superficie: `web://alloy-samples.adobe.com/#content-cards-sample`. La siguiente tabla describe las reglas de déclencheur para cada campaña y cómo satisfacerlas.

<table>
    <tr>
        <th>Regla de activación</th>
        <th>Tarjeta</th>
        <th>Cómo cumplir la regla de déclencheur</th>
    </tr>
    <tr>
        <td>Ninguna</td>
        <td><img src="assets/content-card-web-2.png"></td>
        <td>comando sendEvent. No hay ninguna regla del lado del cliente que satisfacer.</td>
    </tr>
    <tr>
        <td>Ninguna</td>
        <td><img src="assets/content-card-web-3.png"></td>
        <td>comando sendEvent. No hay ninguna regla del lado del cliente que satisfacer.</td>
    </tr>
    <tr>
        <td><img src="assets/content-card-web-4.png"></td>
        <td><img src="assets/content-card-web-5.png"></td>
        <td><img src="assets/content-card-web-6.png"></td>
    </tr>
    <tr>
        <td><img src="assets/content-card-web-7.png"></td>
        <td><img src="assets/content-card-web-8.png"></td>
        <td><img src="assets/content-card-web-9.png"></td>
    </tr>
</table>

El comando `evaluateRulesets` se activa al hacer clic en los botones &quot;Depositar fondos&quot; y &quot;Compartir en medios sociales&quot;. Cada botón especifica los `decisionContext` relevantes para cumplir las reglas definidas para las campañas correspondientes.

```
document.getElementById("action-button-1").addEventListener("click", () => {
    alloy("evaluateRulesets", {
        renderDecisions: true,
        personalization: {
            decisionContext: {
                action: "deposit-funds",
            },
        },
    });
});

document.getElementById("action-button-2").addEventListener("click", () => {
    alloy("evaluateRulesets", {
        renderDecisions: true,
        personalization: {
            decisionContext: {
                action: "social-media",
            },
        },
    });
});
```
