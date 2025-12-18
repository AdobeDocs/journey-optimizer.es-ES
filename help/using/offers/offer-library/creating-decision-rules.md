---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Crear reglas de decisión
description: Obtenga información sobre cómo crear reglas de decisión para definir a quién se pueden mostrar las ofertas
badge: label="Heredado" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 11%

---

# Crear reglas de decisión {#create-decision-rules}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../experience-decisioning/gs-experience-decisioning.md)

## Acerca de las reglas decisión {#about}

Puede crear reglas de decisión de ofertas basadas en los datos disponibles en Adobe Experience Platform. Las reglas de decisión determinan a quién se puede mostrar una oferta.

Por ejemplo, puede especificar que solo desea que se muestre una &quot;Oferta de ropa de invierno femenina&quot; cuando (Sexo = &quot;Mujer&quot;) y (Región = &quot;Noreste&quot;).

➡️ [Descubra esta funcionalidad en vídeo](#video)

Esta es una lista de limitaciones que deben tenerse en cuenta al trabajar con reglas de decisión:

* Edge Decisioning utiliza el perfil Edge que no almacena eventos, por lo que cualquier regla utilizada en una decisión Edge no será válida.
* Al crear una regla de decisión, no se admite retroceder a un período de tiempo anterior. Por ejemplo, si especifica un evento de experiencia que se produjo en el último mes como componente de la regla. Cualquier intento de incluir un periodo retrospectivo durante la creación de la regla generará un déclencheur de error al guardarla.
  <!--* Decision requests that use the hub profile will look at the last 100 experience events on the profile to evaluate rules that reference historical experience events.-->

## Crear una regla de decisión {#create}

Se puede acceder a la lista de reglas de decisión creadas en el menú **[!UICONTROL Componentes]**.

![](../assets/decision_rules_list.png)

Para crear una regla de decisión, siga estos pasos:

1. Vaya a la pestaña **[!UICONTROL Reglas]** y luego haga clic en **[!UICONTROL Crear regla]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Asigne un nombre a la regla, proporcione una descripción y, a continuación, configure la regla según sus necesidades.

   Para ello, está disponible el **Generador de segmentos** de Adobe Experience Platform que le ayudará a generar las condiciones de la regla. [Obtenga información sobre cómo generar definiciones de segmentos](../../audience/creating-a-segment-definition.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >El Generador de segmentos proporcionado para crear reglas de decisión presenta algunas características específicas en comparación con el utilizado con el servicio **[!UICONTROL Segmentation]**. Sin embargo, el proceso global descrito en la documentación de [Generador de segmentos](../../audience/creating-a-segment-definition.md) sigue siendo válido para generar reglas de decisiones de ofertas. Obtenga más información en la [documentación del Servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=es).

1. A medida que agrega y configura nuevos campos en el área de trabajo, el panel **[!UICONTROL Propiedades de la audiencia]** muestra información sobre los perfiles estimados que pertenecen a la audiencia. Haga clic en **[!UICONTROL Actualizar estimación]** para actualizar los datos.

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >Las estimaciones de perfil no están disponibles cuando los parámetros de regla incluyen datos que no están en el perfil, como datos de contexto. Por ejemplo, una regla de idoneidad que requiere que el clima actual sea de ≥80 grados.

1. Haga clic en **[!UICONTROL Guardar]** para confirmar.

1. Una vez creada la regla, se muestra en la lista **[!UICONTROL Reglas]**. Puede seleccionarlo para mostrar sus propiedades y editarlo o eliminarlo.

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>Actualmente no se admiten ofertas basadas en eventos en [!DNL Journey Optimizer]. Si crea una regla de decisión basada en un [evento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=es#events){target="_blank"}, no podrá aprovecharla en una oferta.

## Tutorial en vídeo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
