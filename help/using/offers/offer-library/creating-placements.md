---
title: Creación de ubicaciones
description: Obtenga información sobre cómo crear ubicaciones para las ofertas
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
>abstract="Una ubicación es un contenedor que se utiliza para mostrar ofertas. Ayuda a garantizar que se muestra el contenido de oferta correcto en la ubicación correcta dentro del mensaje. Las ubicaciones se crean desde el menú “Componentes”."

Una ubicación ayuda a garantizar que el contenido de oferta correcto se muestre en la ubicación correcta dentro del mensaje. Al agregar contenido a una oferta, se le pedirá que seleccione una ubicación en la que se pueda mostrar dicho contenido.

➡️ [Obtenga información sobre cómo crear ubicaciones en este vídeo](#video)

En el ejemplo siguiente, hay tres ubicaciones que corresponden a diferentes tipos de contenido (imagen, texto, HTML).

![](../assets/offers_placement_schema.png)

Se puede acceder a la lista de ubicaciones en el **[!UICONTROL Componentes]** menú. Los filtros están disponibles para ayudarle a recuperar ubicaciones según un canal o contenido específico.

![](../assets/placements_filter.png)

Para crear una ubicación, siga estos pasos:

1. Clic **[!UICONTROL Crear ubicación]**.

   ![](../assets/offers_placement_creation.png)

1. Defina las propiedades de la ubicación:

   * **[!UICONTROL Nombre]**: nombre de la ubicación. Asegúrese de definir un nombre significativo para recuperarlo más fácilmente.
   * **[!UICONTROL Tipo de canal]**: Canal para el que se utilizará la ubicación.
   * **[!UICONTROL Tipo de contenido]**: Tipo de contenido que se permitirá mostrar en la ubicación: texto, HTML, vínculo de imagen o JSON.
   * **[!UICONTROL Descripción]**: una descripción de la ubicación (opcional).

   ![](../assets/offers_placement_creation_properties.png)


1. El **[!UICONTROL Solicitar configuración]** y **[!UICONTROL Formato de respuesta]** Las secciones de proporcionan parámetros adicionales:

   * **[!UICONTROL Permitir duplicados entre ubicaciones]**: Controle si la misma oferta se puede proponer varias veces en diferentes ubicaciones. Si se habilita, el sistema considerará la misma oferta para varias ubicaciones. De forma predeterminada, el parámetro se establece en false.

      Si esta opción se establece en false para cualquier ubicación de una solicitud de toma de decisiones, todas las ubicaciones de la solicitud heredarán la configuración &quot;false&quot;.

   * **[!UICONTROL Solicitar oferta]**: De forma predeterminada, se devuelve una oferta del ámbito de decisión para cada perfil. Puede ajustar el número de ofertas devueltas mediante esta opción. Por ejemplo, si selecciona 2, se mostrarán las 2 mejores ofertas para el ámbito de decisión seleccionado.

   * **[!UICONTROL Incluir contenido]** / **[!UICONTROL Incluir metadatos]**: especifique si el contenido y los metadatos de la oferta deben devolverse en la respuesta de la API. Solo puede incluir todos los metadatos o campos específicos. De forma predeterminada, el valor Include metadata se establece en true.
   Estos parámetros también se pueden configurar directamente en la solicitud de API si trabaja con [API de decisiones](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html). Sin embargo, configurarlos en la interfaz de usuario puede ayudarle a ahorrar tiempo, ya que no tendrá que pasarlos en cada solicitud de API. Tenga en cuenta que si configura los parámetros tanto en la interfaz de usuario como en la solicitud de API, los valores de la solicitud de API prevalecerán sobre los de la interfaz.

   >[!NOTE]
   >
   >Si está trabajando con [API de Edge Decisioning](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?)No obstante, no puede establecer estos parámetros en la solicitud. Debe definirlos en esta pantalla.
   >
   >Si está trabajando con [API de decisiones por lotes](../api-reference/offer-delivery-api/batch-decisioning-api.md), puede establecer estos parámetros en esta pantalla o en su solicitud de API. Si hay una discrepancia en los valores de parámetros entre la pantalla y la solicitud de API, se utilizan los valores de solicitud.

1. Haga clic en **[!UICONTROL Guardar]** para confirmar.

1. Una vez creada la ubicación, se muestra en la lista de ubicaciones. Puede seleccionarlo para mostrar sus propiedades y editarlo.

   ![](../assets/placement_created.png)

## Vídeo explicativo{#video}

Obtenga información sobre cómo crear ubicaciones en la administración de decisiones.

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

