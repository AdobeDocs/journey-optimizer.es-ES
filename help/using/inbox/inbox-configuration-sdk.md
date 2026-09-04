---
title: Configuración de la compatibilidad con la bandeja de entrada en Web SDK
description: Obtenga información sobre cómo crear una bandeja de entrada de mensajes persistentes en Adobe Journey Optimizer mediante campañas de tarjeta de contenido y bandeja de entrada con Adobe Experience Platform Web SDK.
feature: Content Cards
topic: Content Management
role: Developer
level: Experienced
source-git-commit: 1ee6fd3ed3523635ea7dbe46dbae0e2403246818
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 1%

---

# Configuración de la compatibilidad con la bandeja de entrada en el SDK web {#inbox-configuration-sdk}

>[!BEGINSHADEBOX]

**En esta página:** Configure y ejecute un ejemplo que combine una campaña de tarjeta de contenido y una campaña de bandeja de entrada con Adobe Experience Platform Web SDK, de modo que pueda enviar una bandeja de entrada de notificaciones persistentes a su sitio web.

>[!ENDSHADEBOX]

Una bandeja de entrada de mensaje es una bandeja de entrada de notificaciones persistentes dirigida por dos campañas de Adobe Journey Optimizer dirigidas a la misma superficie:

* Una **campaña de tarjeta de contenido** que envía elementos de notificación individuales a la bandeja de entrada.
* Una **campaña en la bandeja de entrada**, que ofrece configuración como el título, la copia de estado vacío y el diseño.


## Configurar Adobe Journey Optimizer {#ajo-setup}

Antes de implementar Web SDK, configure el conjunto de datos, los canales y las campañas de Journey Optimizer que envían contenido a la bandeja de entrada.

1. Configure un **conjunto de datos** configurado con **Adobe Experience Platform** como servicio, con **Journey Optimizer** habilitado y un **conjunto de datos de evento** seleccionado.

1. Cree dos configuraciones de canal que compartan la misma superficie: un canal de **Tarjetas de contenido** y un canal de **Bandeja de entrada**. [Aprenda a configurar un canal de tarjeta de contenido](../content-card/content-card-configuration.md) y [aprenda a configurar un canal de bandeja de entrada](inbox-configuration.md).

   Establezca la **URL de la página** y la **ubicación en la página** de ambos canales en la superficie que definió en los requisitos previos. Esta ubicación debe coincidir con la superficie que se consulta en el código Web SDK.

1. [Cree una campaña de tarjeta de contenido](../content-card/create-content-card.md) que use el canal Tarjetas de contenido para la configuración de su tarjeta de contenido.

   En el caso de los mensajes que se deben enviar según las acciones del usuario en la página web, habilite **Reglas de envío adicionales** en la acción relevante y establezca las condiciones de evento y valor que determinan cuándo aparece el mensaje. Repita este proceso para cada tipo de notificación que deba recibir la bandeja de entrada.

1. [Crear una campaña en la Bandeja de entrada](inbox-create.md) que use el canal Bandeja de entrada. Esta campaña envía los metadatos que configuran el propio shell de la bandeja de entrada.

   Haga coincidir la configuración de audiencia y programación de la campaña de la bandeja de entrada con la campaña de la tarjeta de contenido, de modo que ambas estén activas para el mismo usuario al mismo tiempo.

1. Active ambas campañas.

## Implementación de Web SDK {#web-sdk-implementation}

La bandeja de entrada se basa en dos comandos de Web SDK:

* `subscribeRulesetItems` registra una llamada de retorno que se ejecuta cada vez que cambian las propuestas elegibles para la visualización.

* `sendEvent` recupera esas propuestas. Puede enviar eventos adicionales más adelante para actualizar qué mensajes cumplen los requisitos para su visualización.

1. Defina los esquemas de la tarjeta de contenido y de la bandeja de entrada, y la superficie que coincida con la configuración del canal de AJO:

   ```javascript
   const CONTENT_CARD_SCHEMA = "https://ns.adobe.com/personalization/message/content-card";
   const INBOX_SCHEMA        = "https://ns.adobe.com/personalization/message/inbox";
   const SURFACE             = "web://your-site.example/#message-inbox";
   ```

1. Configure Web SDK con su secuencia de datos:

   ```javascript
   alloy("configure", {
     datastreamId: "YOUR_DATASTREAM_ID",
     orgId: "YOUR_ORG_ID@AdobeOrg",
     defaultConsent: "in", // May not be usable in your implementation, but should be used for testing
     personalizationStorageEnabled: true,
   })
   ```

1. Suscríbase a elementos de conjuntos de reglas para la superficie y los esquemas y proporcione una llamada de retorno que administre las propuestas de tarjetas de contenido a medida que cambien:

   ```javascript
   alloy("subscribeRulesetItems", {
     surfaces: [SURFACE],
     schemas: [CONTENT_CARD_SCHEMA, INBOX_SCHEMA],
     callback: (result, collectEvent) => {
       const { propositions = [] } = result;
       const notifications = propositions
         .filter((p) => p.items?.[0]?.schema === CONTENT_CARD_SCHEMA)
         .map((proposition) => {
           const content = proposition.items[0]?.data?.content ?? {};
           return {
             id: proposition.scopeDetails.activity.id,
             title: content.title?.content ?? content.title ?? "",
             description: content.body?.content ?? content.body ?? "",
             proposition,
           };
         });
       renderNotifications(notifications, collectEvent);
     },
   });
   ```

1. A medida que los usuarios interactúen con la aplicación, envíe eventos para actualizar qué propuestas de tarjetas de contenido se deben mostrar:

   ```javascript
   alloy("sendEvent", {
     renderDecisions: true,
     personalization: { surfaces: [SURFACE] },
   });
   ```

1. Utilice la función `collectEvent` proporcionada por la llamada de retorno `subscribeRulesetItems` para informar de las interacciones a AJO. Esto mantiene la precisión de los informes de campaña:

   ```javascript
   // When a notification is displayed in the detail view:
   collectEvent("display", [notification.proposition]);
   
   // When a user clicks or interacts with a notification:
   collectEvent("interact", [notification.proposition]);
   
   // When a user dismisses a notification without reading it:
   collectEvent("dismiss", [notification.proposition]);
   
   // When a user deletes a notification:
   collectEvent("interact", [notification.proposition]);
   collectEvent("delete",   [notification.proposition]);
   ```

1. En el caso de las tarjetas con reglas de envío adicionales, como `action = deposit-funds`, llame a `evaluateRulesets` con el `decisionContext` correspondiente para almacenarlas en déclencheur, ya que no aparecen solo en `sendEvent`:

   ```javascript
   alloy("evaluateRulesets", {
     renderDecisions: true,
     personalization: {
       decisionContext: { action: "deposit-funds" },
     },
   });
   ```

   La llamada de retorno `subscribeRulesetItems` se ejecuta nuevamente con cualquier tarjeta recién calificada incluida junto con las existentes.

1. Instale las dependencias e inicie el servidor de ejemplo:

   ```bash
   npm install
   npm start
   ```

1. Abra `https://localhost` en su explorador.

1. Actualice la constante `datastreamId`, `orgId` y `SURFACE` en `src/app/page.js` para que apunte a su entorno de AJO antes de realizar la prueba.

{{$include /help/_includes/do-not-localize/inbox/ai-augmented-inbox-configuration-sdk.md}}
