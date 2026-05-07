---
title: Code-based surface
description: Learn what a code-based experience surface is
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 07ec74fb-7fbc-48c6-a8fc-f58f24a60723
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 52%

---

# Superficies de la experiencia basada en código {#code-based-surface}

## ¿Qué es una superficie? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="Añada el URI de superficie del componente"
>abstract="Si la implementación no es para web, iOS ni Android, o si necesita dirigirse a URI específicos, introduzca un URI de superficie, que es un identificador único que dirige a la entidad en la que desea ofrecer la experiencia. Asegúrese de introducir un URI de superficie que coincida con el utilizado en su propia implementación."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-configuration#other" text="Cree una configuración de experiencia basada en código para Otras plataformas"

A code-based experience **surface** is any entity designed for user or system interaction, uniquely identified by an [URI](#surface-uri). The surface is specified in the [application implementation](code-based-prerequisites.md#implementation-prerequisites) and must match the surface referenced in your [code-based experience channel configuration](code-based-configuration.md).

A surface can be seen as a container at any level of hierarchy with an entity (touchpoint) that exists.

* Puede ser una página web, una aplicación móvil, una aplicación de escritorio o una ubicación de contenido específica dentro de una entidad más grande (por ejemplo, una `div`) o un patrón de visualización no estándar (por ejemplo, un quiosco o un titular de aplicación de escritorio).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* También se puede ampliar a fragmentos específicos de contenedores de contenido para fines de no visualización o de visualización abstracta (por ejemplo, blobs JSON entregados a servicios).

* También puede ser una superficie comodín que coincida con una variedad de definiciones de superficie de cliente (por ejemplo, una ubicación de imagen principal en cada página del sitio web podría traducirse en un URI de superficie como: web://mydomain.com/*#hero_image).

>[!NOTE]
>
>When you have multiple code-based experience actions running on the same surface, the campaign or journey&#39;s **[!UICONTROL Priority score]** determines what is delivered to the end-user if they qualify for more than one action. [Learn more on priority scores](../conflict-prioritization/priority-scores.md)

## Surface identifier {#surface-uri}

A **surface URI** serves as a precise identifier directing to distinct user interface elements or components within an application. Basically, a surface URI is composed of multiple sections:

1. **Tipo**: web, aplicación móvil, atm, quiosco, tvcd, servicio etc.
1. **Propiedad**: URL de página o paquete de aplicaciones
1. **Contenedor**: ubicación en la actividad de la página/aplicación

En la tabla siguiente se muestran algunos ejemplos de definiciones de URI de superficie para varios dispositivos.

**Web y móvil**

| Tipo | URI | Descripción |
| --------- | ----------- | ------- |
| Web | `web://domain.com/path/page.html#element` | Representa un elemento individual dentro de una página específica de un dominio específico, donde un elemento puede ser una etiqueta como en los ejemplos siguientes: hero_banner, top_nav, menu, footer, etc. |
| Aplicación iOS | `mobileapp://com.vendor.bundle/activity#element` | Representa un elemento específico dentro de una actividad, como un botón u otro elemento de vista. |
| Aplicación de Android | `mobileapp://com.vendor.bundle/#element` | Representa un elemento específico dentro de una aplicación nativa. |

**Otros tipos de dispositivos**

| Tipo | URI | Descripción |
| --------- | ----------- | ------- |
| Escritorio | `desktop://com.vendor.bundle/#element` | Representa un elemento específico dentro de una aplicación, como un botón, un menú, un banner principal, etc. |
| Aplicación de TV | `tvcd://com.vendor.bundle/#element` | Representa un elemento específico en una TV inteligente o TV conectado a una aplicación de dispositivo: ID de paquete. |
| Servicio | `service://servicename/#element` | Representa un proceso del lado del servidor u otra entidad manual. |
| Quiosco | `kiosk://location/screen#element` | Ejemplo de posibles tipos de superficie adicionales que se pueden añadir fácilmente. |
| ATM | `atm://location/screen#element` | Ejemplo de posibles tipos de superficie adicionales que se pueden añadir fácilmente. |

**Superficies comodín**

| Tipo | URI | Descripción |
| --------- | ----------- | ------- |
| Web comodín | `wildcard:web://domain.com/*#element` | Superficie comodín: representa un elemento individual en cada una de las páginas bajo un dominio específico. |
| Web comodín | `wildcard:web://*domain.com/*#element` | Superficie comodín: representa un elemento individual en cada una de las páginas bajo todos los dominios que acaba con &quot;domain.com&quot;. |

## URI composition {#uri-composition}

In [!DNL Journey Optimizer], the code-based experience channel supports two types of customer implementations:

* Based on the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"} for your websites, or on the [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation){target="_blank"} for you mobile apps;
* Server-side or hybrid using [AEP Edge Network Server APIs](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=es){target="_blank"}.

>[!NOTE]
>
>Learn more about the implementation prerequisites in [this section](code-based-prerequisites.md#implementation-prerequisites).

Using code-based experiences, you can modify content on granular locations <!--(such as a specific location on a page, or inside a mobile native app)-->which are uniquely identified by [!DNL Journey Optimizer] using [surface URIs](#surface-uri).

These surface URIs are composed and handled depending on the implementation method:

* **Web/Mobile SDK**: Your web/mobile developer needs to define these granular locations as simple strings, because the Web/Mobile SDK is capable of automatically compose the surface URI based on the current URL/app ID and the location string.

* **Edge Network APIs**: The app/page developer must define full surface URIs that include the full path and location where the content will be consumed, because the full URIs are required in this type of implementation.

This is why, when creating a [code-based experience channel configuration](code-based-configuration.md), you have two ways to specify the surface according to the selected platform:

* For **[!UICONTROL Web]**, **[!UICONTROL iOS]** and **[!UICONTROL Android]** platforms, you need to the enter the **URL/app ID** and a **location or path** to compose the surface. Learn more about configuring code-based experiences for [web](code-based-configuration.md#web) and [mobile](code-based-configuration.md#mobile) platforms

* If the platform is **[!UICONTROL Other]**, you need to enter the full **surface URI**, like in the examples [above](#surface-uri). Learn more about configuring code-based experiences for [other](code-based-configuration.md#other) platforms
