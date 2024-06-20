---
title: Reglas de decisión
description: Aprenda a trabajar con reglas de decisión
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilidad limitada"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 24%

---

# Reglas de decisión {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Crear reglas de decisión"
>abstract="Las reglas de decisión permiten definir el público de los elementos de decisión mediante la aplicación de restricciones, ya sea directamente en el nivel del elemento de decisión o dentro de una estrategia de selección específica. Esto le permite controlar con precisión qué elementos se deben presentar y a quién se deben presentar."

## Acerca de las reglas decisión {#about}

Las reglas de decisión permiten definir el público de los elementos de decisión mediante la aplicación de restricciones, ya sea directamente en el nivel del elemento de decisión o dentro de una estrategia de selección específica. Esto le permite controlar con precisión qué elementos se deben presentar y a quién se deben presentar.

Por ejemplo, consideremos un escenario en el que tenga elementos de decisión que presenten productos relacionados con el yoga diseñados para mujeres. Con las reglas de decisión, puede especificar que estos elementos solo deben mostrarse a perfiles cuyo sexo sea &quot;Mujer&quot; y que hayan indicado un &quot;Punto de interés&quot; en &quot;Yoga&quot;.

>[!NOTE]
>
>Además de las reglas de decisión a nivel de elemento y de estrategia de selección, también puede definir la audiencia a nivel de campaña. [Más información](../campaigns/create-campaign.md#audience)

Se puede acceder a la lista de reglas de decisión en la **[!UICONTROL Configuración de estrategia]** menú.

![](assets/decision-rules-list.png)

## Crear una regla de decisión {#create}

Para crear una regla de decisión, siga estos pasos:

1. Vaya a **[!UICONTROL Configuración de estrategia]** / **[!UICONTROL Reglas de decisión]** luego haga clic en **[!UICONTROL Crear regla]** botón.

1. Se abre la pantalla de creación de reglas de decisión. Especifique un nombre para la regla y una descripción.

1. Cree la regla de decisión que se adapte a sus necesidades con el Generador de segmentos de Adobe Experience Platform. Para ello, puede aprovechar varias fuentes de datos, como atributos de perfil, audiencias o datos de contexto procedentes de Adobe Experience Platform. [Aprenda a aprovechar los datos de contexto](#context-data)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >El Generador de segmentos que se proporciona para crear reglas de decisión presenta algunas particularidades en comparación con el que se utiliza con el servicio de segmentación de Adobe Experience Platform.  Sin embargo, el proceso global descrito en la documentación sigue siendo válido para generar reglas de decisiones. [Obtenga información sobre cómo crear definiciones de segmentos](../audience/creating-a-segment-definition.md)

1. Al añadir y configurar nuevos campos en el espacio de trabajo, la variable **[!UICONTROL Propiedades de audiencia]** Este panel muestra información sobre los perfiles estimados que pertenecen a la audiencia. Clic **[!UICONTROL Actualizar estimación]** para actualizar los datos.

   >[!NOTE]
   >
   >Las estimaciones de perfil no están disponibles cuando los parámetros de regla incluyen datos que no están en el perfil, como datos de contexto.

1. Una vez preparada la regla de decisión, haga clic en **[!UICONTROL Guardar]**. La regla creada aparece en la lista y está disponible para su uso en elementos de decisión y estrategias de selección para regular la presentación de elementos de decisión a perfiles.

