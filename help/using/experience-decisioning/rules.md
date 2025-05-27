---
title: Reglas de decisión
description: Aprenda a trabajar con reglas de decisión
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 8418b0c9251e090575671acb65f83bee911cd039
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 20%

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

Se puede acceder a la lista de reglas de decisión en el menú **[!UICONTROL Configuración de estrategia]**.

![](assets/decision-rules-list.png)

## Crear una regla de decisión {#create}

Para crear una regla de decisión, siga estos pasos:

1. Vaya a **[!UICONTROL Configuración de estrategia]** / **[!UICONTROL Reglas de decisión]** y haga clic en el botón **[!UICONTROL Crear regla]**.

1. Se abre la pantalla de creación de reglas de decisión. Especifique un nombre para la regla y una descripción.

1. Cree la regla de decisión que se adapte a sus necesidades con el Generador de segmentos de Adobe Experience Platform. Para ello, puede aprovechar varias fuentes de datos, como atributos de perfil, audiencias o datos de contexto procedentes de Adobe Experience Platform. [Aprenda a aprovechar los datos de contexto](#context-data)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >El Generador de segmentos que se proporciona para crear reglas de decisión presenta algunas particularidades en comparación con el que se utiliza con el servicio de segmentación de Adobe Experience Platform.  Sin embargo, el proceso global descrito en la documentación sigue siendo válido para generar reglas de decisiones. [Obtenga información sobre cómo generar definiciones de segmentos](../audience/creating-a-segment-definition.md)

1. A medida que agrega y configura nuevos campos en el área de trabajo, el panel **[!UICONTROL Propiedades de la audiencia]** muestra información sobre los perfiles estimados que pertenecen a la audiencia. Haga clic en **[!UICONTROL Actualizar estimación]** para actualizar los datos.

   >[!NOTE]
   >
   >Las estimaciones de perfil no están disponibles cuando los parámetros de regla incluyen datos que no están en el perfil, como datos de contexto.

1. Una vez que la regla de decisión esté lista, haga clic en **[!UICONTROL Guardar]**. La regla creada aparece en la lista y está disponible para su uso en elementos de decisión y estrategias de selección para regular la presentación de elementos de decisión a perfiles.

   >[!NOTE]
   >
   >La profundidad de anidación de una regla de idoneidad está limitada a 30 niveles. Esto se mide contando los `)` paréntesis de cierre en la cadena de PQL. Una cadena de regla puede tener un tamaño máximo de 15 KB para caracteres codificados en UTF-8. Esto equivale a 15 000 caracteres ASCII (1 byte cada uno) o a 3 750-7 500 caracteres no ASCII (2-4 bytes cada uno). [Más información sobre las limitaciones y protecciones de decisiones](gs-experience-decisioning.md#guardrails)
