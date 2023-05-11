---
title: Crear reglas de decisión
description: Aprenda a crear reglas de decisión para definir a quién se pueden mostrar las ofertas
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 12%

---

# Crear reglas de decisión {#create-decision-rules}

Puede crear reglas de decisión de oferta basadas en los datos disponibles en Adobe Experience Platform. Las reglas de decisión determinan a quién se puede mostrar una oferta.

Por ejemplo, puede especificar que solo desea que se muestre una “Oferta de ropa de invierno femenina” cuando (Sexo = &#39;Mujer&#39;) y (Región = &#39;Noreste&#39;).

➡️ [Descubra esta función en vídeo](#video)

Se puede acceder a la lista de reglas de decisión creadas en la **[!UICONTROL Componentes]** para abrir el Navegador.

![](../assets/decision_rules_list.png)

Para crear una regla de decisión, siga estos pasos:

1. Vaya a la **[!UICONTROL Reglas]** a continuación, haga clic en **[!UICONTROL Crear regla]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Asigne un nombre a la regla, proporcione una descripción y, a continuación, configure la regla según sus necesidades.

   Para ello, el **Generador de segmentos** está disponible para ayudarle a crear las condiciones de la regla. [Más información](../../segment/about-segments.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >El Generador de segmentos proporcionado para crear reglas de decisión presenta algunas características específicas en comparación con la que se usa con la variable **[!UICONTROL Segmentación]** servicio. Por ejemplo, la variable **[!UICONTROL Segmentos]** no está disponible para usar. Sin embargo, el proceso global descrito en el [Generador de segmentos](../../segment/about-segments.md) la documentación sigue siendo válida para crear reglas de decisiones de ofertas. Obtenga más información en la [Documentación del servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html).

1. Al añadir y configurar nuevos campos en el espacio de trabajo, la variable **[!UICONTROL Propiedades del segmento]** muestra información sobre los perfiles estimados que pertenecen al segmento. Haga clic en **[!UICONTROL Actualizar estimación]** para actualizar los datos.

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >Las estimaciones de perfil no están disponibles cuando los parámetros de regla incluyen datos que no están en el perfil, como los datos de contexto. Por ejemplo, una regla de aceptación que requiera que el clima actual sea ≥ 80 grados.

1. Haga clic en **[!UICONTROL Guardar]** para confirmar.

1. Una vez creada la regla, aparece en la sección **[!UICONTROL Reglas]** lista. Puede seleccionarlo para mostrar sus propiedades y editarlo o eliminarlo.

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>Actualmente, las ofertas basadas en eventos no son compatibles con [!DNL Journey Optimizer]. Si crea una regla de decisión basada en un [evento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}, no podrá aprovecharlo en una oferta.

## Tutorial en vídeo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
