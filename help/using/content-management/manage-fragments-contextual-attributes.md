---
solution: Journey Optimizer
product: journey optimizer
title: Añadir atributos contextuales a fragmentos publicados
description: Aprenda a añadir atributos contextuales a los fragmentos publicados (disponibilidad limitada)
feature: Fragments
topic: Content Management
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
source-git-commit: 69efe0254aae3cb067f2c9f89db6aa4fe0a50549
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 4%

---

# Añadir atributos contextuales a fragmentos publicados {#adding-contextual-attributes}

>[!AVAILABILITY]
>
>Esta capacidad solo está disponible para clientes seleccionados e implica riesgos significativos. Confirme con su representante de Adobe que esta capacidad está habilitada para su organización.

De manera predeterminada, no se admite agregar nuevos [atributos de personalización](../personalization/personalization-build-expressions.md) a un fragmento publicado. Una vez publicado un fragmento, el conjunto de atributos contextuales o de perfil se bloquea para todas las campañas y recorridos.

Sin embargo, para clientes seleccionados, es posible agregar **atributos contextuales** solo a fragmentos publicados.

>[!WARNING]
>
>Al añadir atributos de personalización a un fragmento publicado, el proceso de validación es menos estricto y es posible que no se detecten errores. Esto podría provocar interrupciones no deseadas en los recorridos y campañas que utilicen ese fragmento a escala.

## Mecanismos de protección y limitaciones {#limitations}

* Asegúrese de que todos los recorridos y campañas que utilizan actualmente el fragmento puedan gestionar los nuevos atributos contextuales.
* No se pueden agregar atributos de perfil a los fragmentos publicados. Solo se admiten atributos contextuales.
* Los atributos contextuales deben introducirse manualmente en el editor de código; no se pueden seleccionar desde la interfaz de usuario del editor de personalización.
* Al agregar atributos personalizados a fragmentos activos, las validaciones se relajan, lo que significa que es posible que no se detecten errores y que se produzcan roturas no deseadas a escala.
* Una vez publicado, los errores afectarán inmediatamente a todas las comunicaciones que utilicen ese fragmento.

## Añadir atributos contextuales {#add-contextual-attributes}

Para añadir atributos contextuales a un fragmento publicado, siga los pasos a continuación.

>[!IMPORTANT]
>
>Solo continúe si [comprende completamente el impacto](#limitations) en los recorridos y campañas que hacen referencia al fragmento.

1. Vaya a **[!UICONTROL Administración de contenido]** > **[!UICONTROL Fragmentos]**.

1. Seleccione el fragmento publicado y haga clic en **[!UICONTROL Modificar]** para crear una versión de borrador.

   ![](assets/fragment-live-modify.png){width="70%" align="left"}

1. Haga clic en **[!UICONTROL Editar]** para abrir el editor de contenido del fragmento.

1. Cambie a **[!UICONTROL Editor de código]** o a **[!UICONTROL Modo avanzado]** en el editor de personalización.

1. Escriba o copie y pegue manualmente el atributo contextual con la sintaxis `{{context.attribute_name}}`:

   Ejemplo de un atributo `promotionCode`:

   ```
   {{context.promotionCode}}
   ```

   >[!CAUTION]
   >
   >Compruebe la precisión de la ruta del atributo. Es posible que no se detecten errores y que se interrumpan las comunicaciones de recorrido o campaña a escala.

1. Guarde los cambios.

1. Una vez confirmado, haz clic en **[!UICONTROL Publicar]** para activar los cambios.

>[!NOTE]
>Para evitar interrupciones no deseadas entre recorridos y campañas, puede probar las rutas de atributos contextuales en un entorno que no sea de producción.

## Temas relacionados {#related-topics}

* [Administración de fragmentos](manage-fragments.md)
* [Edición de un fragmento](manage-fragments.md#edit-fragments)
* [Campañas activadas por API](../campaigns/api-triggered-campaigns.md)
* [Sintaxis de personalización](../personalization/personalization-syntax.md)

