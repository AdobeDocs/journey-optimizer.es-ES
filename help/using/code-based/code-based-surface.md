---
title: Superficie basada en código
description: Descubra qué es una superficie de experiencia basada en código
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 07ec74fb-7fbc-48c6-a8fc-f58f24a60723
source-git-commit: d3f15c09194a50b95107fb84d680606a468f8644
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 50%

---

# Superficies de la experiencia basada en código {#code-based-surface}

## ¿Qué es una superficie?  {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="Añada el URI de superficie del componente"
>abstract="Si la implementación no es para web, iOS ni Android, o si necesita dirigirse a URI específicos, introduzca un URI de superficie, que es un identificador único que dirige a la entidad en la que desea ofrecer la experiencia. Asegúrese de introducir un URI de superficie que coincida con el utilizado en su propia implementación."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-configuration#other" text="Cree una configuración de experiencia basada en código para Otras plataformas"

Una experiencia basada en código **surface** es cualquier entidad diseñada para la interacción de usuarios o sistemas, identificada de forma exclusiva por un [URI](#surface-uri). La superficie está especificada en la [implementación de aplicación](code-based-prerequisites.md#implementation-prerequisites) y debe coincidir con la superficie a la que se hace referencia en la [configuración de canal de experiencia basada en código](code-based-configuration.md).

Una superficie puede verse como un contenedor en cualquier nivel de jerarquía con una entidad (punto de contacto) que existe.

* Puede ser una página web, una aplicación móvil, una aplicación de escritorio o una ubicación de contenido específica dentro de una entidad más grande (por ejemplo, una `div`) o un patrón de visualización no estándar (por ejemplo, un quiosco o un titular de aplicación de escritorio).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* También se puede ampliar a fragmentos específicos de contenedores de contenido para fines de no visualización o de visualización abstracta (por ejemplo, blobs JSON entregados a servicios).

* También puede ser una superficie comodín que coincida con una variedad de definiciones de superficie de cliente (por ejemplo, una ubicación de imagen principal en cada página del sitio web podría traducirse en un URI de superficie como: web://mydomain.com/*#hero_image).

>[!NOTE]
>
>Cuando se ejecutan varias acciones de experiencia basadas en código en la misma superficie, la **[!UICONTROL puntuación de prioridad]** de la campaña o el recorrido determina qué se envía al usuario final si cumple los requisitos para más de una acción. [Más información sobre las puntuaciones de prioridad](../conflict-prioritization/priority-scores.md)

## Identificador de superficie {#surface-uri}

Un **URI de superficie** sirve como identificador preciso que dirige a distintos elementos o componentes de la interfaz de usuario dentro de una aplicación. Básicamente, un URI de superficie está compuesto por varias secciones:

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

## Composición URI {#uri-composition}

En [!DNL Journey Optimizer], el canal de experiencia basado en código admite dos tipos de implementaciones de clientes:

* Basado en [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"} para sus sitios web o en [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} para sus aplicaciones móviles;
* Lado del servidor o híbrido que usa [API de servidor de AEP Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=es){target="_blank"}.

>[!NOTE]
>
>Obtenga más información acerca de los requisitos previos de implementación en [esta sección](code-based-prerequisites.md#implementation-prerequisites).

Con experiencias basadas en código, puede modificar el contenido en ubicaciones granulares <!--(such as a specific location on a page, or inside a mobile native app)-->que han sido identificadas de forma exclusiva por [!DNL Journey Optimizer] mediante [URI de superficie](#surface-uri).

Estos URI de superficie se componen y gestionan según el método de implementación:

* **Web/Mobile SDK**: el desarrollador web/móvil debe definir estas ubicaciones granulares como cadenas simples, ya que Web/Mobile SDK es capaz de componer automáticamente el URI de superficie basándose en la dirección URL/ID de aplicación actuales y en la cadena de ubicación.

* **API de Edge Network**: el desarrollador de la aplicación/página debe definir URI de superficie completos que incluyan la ruta de acceso completa y la ubicación donde se consumirá el contenido, ya que los URI completos son necesarios en este tipo de implementación.

Por este motivo, al crear una [configuración de canal de experiencia basada en código](code-based-configuration.md), tiene dos maneras de especificar la superficie según la plataforma seleccionada:

* Para las plataformas **[!UICONTROL Web]**, **[!UICONTROL iOS]** y **[!UICONTROL Android]**, debe introducir la **URL/ID de aplicación** y una **ubicación o ruta** para componer la superficie. Obtenga más información sobre cómo configurar experiencias basadas en código para las plataformas [web](code-based-configuration.md#web) y [móvil](code-based-configuration.md#mobile)

* Si la plataforma es **[!UICONTROL Other]**, debes ingresar el **URI de superficie** completo, como en los ejemplos [anteriores](#surface-uri). Obtenga más información sobre cómo configurar experiencias basadas en código para [otras](code-based-configuration.md#other) plataformas
