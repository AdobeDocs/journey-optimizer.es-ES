---
title: Configuración basada en código
description: Crear configuración basada en código
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 1aff2f6f-914c-4088-afd8-58bd9edfe07d
source-git-commit: 77e2892dc188ebdd79031792434b4f55913ee811
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 33%

---

# Configurar la experiencia basada en código {#code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="ID de la aplicación"
>abstract="Proporcione el ID de la aplicación para una identificación y configuración precisas dentro del entorno operativo de la aplicación, lo que garantiza una integración y funcionalidad sin problemas."

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="Ubicación en la página"
>abstract="La ubicación o ruta dentro del campo de la aplicación especifica el destino exacto dentro de la aplicación al que desea que accedan los usuarios. Podría ser una sección en particular o una página en la estructura de navegación de la aplicación."

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="URI de superficie"
>abstract="Un URI de superficie sirve como identificador preciso que dirige a distintos elementos o componentes de la interfaz de usuario dentro de una aplicación."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_mobile_url"
>title="URL de creación y previsualización predeterminadas"
>abstract="Este campo garantiza que las páginas generadas o coincidentes por la regla tengan una URL designada, esencial para crear y previsualizar contenido de forma eficaz."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_web_url"
>title="URL de creación y previsualización predeterminadas"
>abstract="Este campo garantiza que las páginas generadas o coincidentes por la regla tengan una URL designada, esencial para crear y previsualizar contenido de forma eficaz."

>[!CONTEXTUALHELP]
>id="ajo_admin_mobile_url_preview"
>title="URL de previsualización"
>abstract="Este campo es esencial para habilitar la simulación y la previsualización del contenido directamente en el dispositivo dentro de la aplicación."

## Crear una configuración de canal {#reatte-code-based-configuration}

Para crear una configuración de canal, siga estos pasos:

1. Acceda al menú **[!UICONTROL Canales]** > **[!UICONTROL Configuración general]** > **[!UICONTROL Configuraciones de canal]** y luego haga clic en **[!UICONTROL Crear configuración de canal]**.

   ![](assets/code_config_1.png)

1. Introduzca un nombre y una descripción (opcional) para la configuración.

   >[!NOTE]
   >
   > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos. También puede utilizar caracteres de guion bajo `_`, punto`.` y guión `-`.

1. Para asignar etiquetas de uso de datos principales o personalizadas a la configuración, puedes seleccionar **[!UICONTROL Administrar acceso]**. [Más información sobre el Control de acceso de nivel de objeto (OLAC)](../administration/object-based-access.md).

1. Seleccione **[!UICONTROL Acciones de marketing]** para asociar directivas de consentimiento a los mensajes que usan esta configuración. Todas las políticas de consentimiento asociadas con la acción de marketing se aprovechan para respetar las preferencias de los clientes. [Más información](../action/consent.md#surface-marketing-actions)

1. Seleccione el canal **Experiencia basada en código**.

   ![](assets/code_config_2.png)

1. Seleccione la plataforma para la que se aplicará la experiencia basada en código.

1. Para la web:

   * Especifique una **[!UICONTROL URL de página]** para aplicar los cambios exclusivamente a una sola página.

   * O bien, cree una **[!UICONTROL regla de coincidencia de páginas]** para dirigirla a varias direcciones URL que coincidan con la regla especificada. Por ejemplo, esto podría utilizarse para aplicar los cambios de forma universal en un sitio web, como actualizar un banner a pantalla completa en todas las páginas o añadir una imagen principal para mostrar en cada página de producto. [Más información](../web/web-configuration.md)

1. Para iOS y Android:

   * Escriba su **[!UICONTROL ID de aplicación]** y **[!UICONTROL ubicación o ruta de acceso dentro de la aplicación]**.

     ![](assets/code_config_3.png){width="500"}

1. Seleccione Otro como plataforma si la implementación no es para la web, iOS o Android, o si necesita segmentar URI específicos. Al elegir varias plataformas o agregar varios URI, el contenido se envía a todas las páginas o aplicaciones seleccionadas.

   * Escriba el **[!UICONTROL URI de superficie]**.

   >[!CAUTION]
   >
   >Asegúrese de que el URI de superficie utilizado en la campaña basada en código coincida con el utilizado en su propia implementación. De lo contrario, los cambios no se entregarán.

1. Rellene el campo **[!UICONTROL URL de vista previa]** para habilitar las vistas previas en el dispositivo. Esta dirección URL informa al servicio de vista previa de la dirección URL específica que se utiliza al activar una vista previa.

   * Para la web:

      * Si se introduce una dirección URL de una sola página, esa dirección URL se utilizará para la vista previa.
      * Si se selecciona una regla de coincidencia de página, se debe introducir una URL de vista previa predeterminada que se utilizará para obtener una vista previa de la experiencia en el explorador.

   * Para plataformas móviles (iOS/Android):

      * La URL de vista previa es un vínculo profundo configurado por el desarrollador de la aplicación dentro de la aplicación. Esto garantiza que cualquier dirección URL que coincida con el esquema de enlace profundo se abra en la aplicación en lugar de en un explorador web móvil. Póngase en contacto con el desarrollador de aplicaciones para obtener el esquema de vínculos profundos configurado para su aplicación.

+++  Los siguientes recursos pueden ayudarle a configurar vínculos profundos para la implementación de su aplicación

      * Para Android:

         * [Creación de vínculos profundos al contexto de la aplicación](https://developer.android.com/training/app-links/deep-linking)

      * Para iOS:

         * [Definición de un esquema de URL personalizado para la aplicación](https://developer.apple.com/documentation/xcode/defining-a-custom-url-scheme-for-your-app)

         * [Compatibilidad con vínculos universales en la aplicación](https://developer.apple.com/documentation/xcode/supporting-universal-links-in-your-app)

+++

   >[!NOTE]
   >
   >Si encuentra problemas al obtener una vista previa de la experiencia, consulte [esta documentación](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/troubleshooting#app-does-not-open-link).

1. Elija el formato que espera la aplicación en esa ubicación en particular. Se utilizará al crear la experiencia basada en código en campañas y recorridos.

1. Envíe los cambios.

Ahora puede seleccionar la configuración al crear su experiencia basada en código.


## ¿Qué es una superficie?  {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Defina una configuración de experiencia basada en código"
>abstract="Una configuración basada en código define la ruta y la ubicación dentro de la aplicación, identificada de forma exclusiva por un URI en la implementación de la aplicación, donde se enviará y consumirá el contenido."

Una **superficie de experiencia basada en código** es cualquier entidad diseñada para la interacción del usuario o del sistema, que se identifica de forma exclusiva mediante un URI. La superficie se especifica en la implementación de la aplicación y debe corresponder a la compuesta en la configuración del canal de experiencia basado en código.

Al crear una configuración de canal de experiencia basada en código: para plataformas web, iOS y Android, debe introducir una ruta y una ubicación para componer la superficie, mientras que si la plataforma es Otro, debe introducir el URI completo, como en los ejemplos siguientes.

Es decir, una superficie puede verse como un contenedor en cualquier nivel de jerarquía que existe con una entidad (punto de contacto).<!--good idea to illustrate how it can be seen, but to clarify-->

* Puede ser una página web, una aplicación móvil, una aplicación de escritorio o una ubicación de contenido específica dentro de una entidad más grande (por ejemplo, una `div`) o un patrón de visualización no estándar (por ejemplo, un quiosco o un titular de aplicación de escritorio).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* También se puede ampliar a fragmentos específicos de contenedores de contenido para fines de no visualización o de visualización abstracta (por ejemplo, blobs JSON entregados a servicios).

* También puede ser una superficie comodín que coincida con una variedad de definiciones de superficie de cliente (por ejemplo, una ubicación de imagen principal en cada página del sitio web podría traducirse en un URI de superficie como: web://mydomain.com/*#hero_image).

Básicamente, un URI de superficie está compuesto por varias secciones:
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
