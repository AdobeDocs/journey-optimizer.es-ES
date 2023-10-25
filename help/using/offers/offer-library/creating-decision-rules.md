---
title: Crear reglas de decisión
description: Obtenga información sobre cómo crear reglas de decisión para definir a quién se pueden mostrar las ofertas
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 91f52af0c2e42556c4456be9b6b0cb84378c2a23
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 14%

---

# Crear reglas de decisión {#create-decision-rules}

## Acerca de las reglas decisión {#about}

Puede crear reglas de decisión de ofertas basadas en los datos disponibles en Adobe Experience Platform. Las reglas de decisión determinan a quién se puede mostrar una oferta.

Por ejemplo, puede especificar que solo desea que se muestre una “Oferta de ropa de invierno femenina” cuando (Sexo = &#39;Mujer&#39;) y (Región = &#39;Noreste&#39;).

➡️ [Descubra esta función en vídeo](#video)

Esta es una lista de limitaciones que deben tenerse en cuenta al trabajar con reglas de decisión:

* La toma de decisiones perimetral utiliza el perfil perimetral que no almacena eventos, por lo que cualquier regla utilizada en una decisión perimetral no será válida.
* Al crear una regla de decisión, no se admite retroceder a un período de tiempo anterior. Por ejemplo, si especifica un evento de experiencia que se produjo en el último mes como componente de la regla. Cualquier intento de incluir un periodo retrospectivo durante la creación de la regla generará un déclencheur de error al guardarla.
  <!--* Decision requests that use the hub profile will look at the last 100 experience events on the profile to evaluate rules that reference historical experience events.-->

## Crear una regla de decisión {#create}

Se puede acceder a la lista de reglas de decisión creadas en el **[!UICONTROL Componentes]** menú.

![](../assets/decision_rules_list.png)

Para crear una regla de decisión, siga estos pasos:

1. Vaya a la **[!UICONTROL Reglas]** y haga clic en **[!UICONTROL Crear regla]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Asigne un nombre a la regla, proporcione una descripción y, a continuación, configure la regla según sus necesidades.

   Para ello, utilice la Adobe Experience Platform **Generador de segmentos** está disponible para ayudarle a crear las condiciones de la regla. [Obtenga información sobre cómo crear definiciones de segmentos](../../audience/creating-a-segment-definition.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >El Generador de segmentos que se proporciona para crear reglas de decisión presenta algunas particularidades en comparación con el que se utiliza con **[!UICONTROL Segmentación]** servicio. Sin embargo, el proceso global descrito en la [Generador de segmentos](../../audience/creating-a-segment-definition.md) La documentación de sigue siendo válida para generar reglas de decisiones de ofertas. Obtenga más información en la [documentación del Servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=es).

1. Al añadir y configurar nuevos campos en el espacio de trabajo, la variable **[!UICONTROL Propiedades de audiencia]** Este panel muestra información sobre los perfiles estimados que pertenecen a la audiencia. Clic **[!UICONTROL Actualizar estimación]** para actualizar los datos.

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >Las estimaciones de perfil no están disponibles cuando los parámetros de regla incluyen datos que no están en el perfil, como datos de contexto. Por ejemplo, una regla de idoneidad que requiere que el clima actual sea de ≥80 grados.

1. Haga clic en **[!UICONTROL Guardar]** para confirmar.

1. Una vez creada la regla, se muestra en el **[!UICONTROL Reglas]** lista. Puede seleccionarlo para mostrar sus propiedades y editarlo o eliminarlo.

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>Actualmente no se admiten ofertas basadas en eventos en [!DNL Journey Optimizer]. Si crea una regla de decisión basada en un [evento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#events){target="_blank"}, no podrá aprovecharlo en una oferta de.

## Tutorial en vídeo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
