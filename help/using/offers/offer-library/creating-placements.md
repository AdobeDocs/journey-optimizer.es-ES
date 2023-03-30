---
title: Creación de ubicaciones
description: Aprenda a crear ubicaciones para sus ofertas
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: dfaf887e-d4b3-45b0-8297-bffdb0abff4d
source-git-commit: 51f93270c969875e94cc3e98919149d67d764ed1
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 12%

---

# Creación de ubicaciones {#create-placements}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement"
>title="Colocación"
>abstract="Una ubicación es un contenedor que se utiliza para mostrar ofertas. Ayuda a garantizar que el contenido de oferta correcto se presenta en la ubicación adecuada dentro del mensaje. Las ubicaciones se crean desde el menú Componentes."

Una ubicación ayuda a garantizar que el contenido de oferta correcto se muestre en la ubicación correcta dentro del mensaje. Al agregar contenido a una oferta, se le pedirá que seleccione una ubicación en la que se pueda mostrar dicho contenido.

➡️ [Aprenda a crear ubicaciones en este vídeo](#video)

En el ejemplo siguiente, hay tres ubicaciones que corresponden a diferentes tipos de contenido (imagen, texto, HTML).

![](../assets/offers_placement_schema.png)

Se puede acceder a la lista de ubicaciones desde la **[!UICONTROL Componentes]** para abrir el Navegador. Los filtros están disponibles para ayudarle a recuperar las ubicaciones según un canal o contenido específico.

![](../assets/placements_filter.png)

Para crear una ubicación, siga estos pasos:

1. Haga clic en **[!UICONTROL Crear ubicación]**.

   ![](../assets/offers_placement_creation.png)

1. Defina las propiedades de la ubicación:

   * **[!UICONTROL Nombre]**: Nombre de la ubicación. Asegúrese de definir un nombre significativo para recuperarlo más fácilmente.
   * **[!UICONTROL Tipo de canal]**: Canal para el que se utilizará la colocación.
   * **[!UICONTROL Tipo de contenido]**: Tipo de contenido que se permitirá mostrar en la ubicación: Texto, HTML, vínculo de imagen o JSON.
   * **[!UICONTROL Descripción]**: Descripción de la colocación (opcional).

   ![](../assets/offers_placement_creation_properties.png)


1. La variable **[!UICONTROL Configuración de solicitud]** y **[!UICONTROL Formato de respuesta]** las secciones proporcionan parámetros adicionales:

   * **[!UICONTROL Permitir duplicados entre ubicaciones]**: Controle si la misma oferta se puede proponer varias veces en diferentes ubicaciones. Si está habilitada, el sistema considerará la misma oferta para varias ubicaciones. De forma predeterminada, el parámetro se establece en false.

      Si esta opción se establece en false en cualquier ubicación de una solicitud de toma de decisiones, todas las ubicaciones de la solicitud heredarán la configuración &quot;false&quot;.

   * **[!UICONTROL Solicitud de oferta]**: De forma predeterminada, se devuelve una oferta del ámbito de decisión para cada perfil. Puede ajustar el número de ofertas devueltas mediante esta opción. Por ejemplo, si selecciona 2, se mostrarán las 2 mejores ofertas para el ámbito de decisión seleccionado.

   * **[!UICONTROL Incluir contenido]** / **[!UICONTROL Incluir metadatos]**: especifique si el contenido y los metadatos de la oferta deben devolverse en la respuesta de la API. Puede incluir todos los metadatos o solo campos específicos. De forma predeterminada, el valor Include metadata está establecido en true.
   Estos parámetros también se pueden configurar directamente en la solicitud de API si está trabajando con la variable [API de decisiones](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html). Sin embargo, configurarlas en la interfaz de usuario puede ayudarle a ahorrar tiempo, ya que no tendrá que pasarlas en cada solicitud de API. Tenga en cuenta que si configura los parámetros tanto en la interfaz de usuario como en la solicitud de API, los valores de la solicitud de API prevalecerán sobre los de la interfaz.

   >[!NOTE]
   >
   >Si está trabajando con la variable [API de Edge Decisioning](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?), no puede establecer estos parámetros en la solicitud de . Debe definirlos en esta pantalla.
   >
   >Si está trabajando con la variable [API de decisiones por lotes](../api-reference/offer-delivery-api/batch-decisioning-api.md), puede configurar estos parámetros en esta pantalla o en su solicitud de API. Si no coinciden los valores de parámetro entre la pantalla y la solicitud APi, se utilizarán los valores de solicitud.

1. Haga clic en **[!UICONTROL Guardar]** para confirmar.

1. Una vez creada la ubicación, esta se muestra en la lista de ubicaciones. Puede seleccionarlo para mostrar sus propiedades y editarlo.

   ![](../assets/placement_created.png)

## Vídeo explicativo{#video}

Aprenda a crear ubicaciones en la administración de decisiones.

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

