---
title: Reglas de decisión
description: Aprenda a trabajar con reglas de decisión
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 29228a17176421ccf29598d6ebba815b800db7a2
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 16%

---

# Reglas de decisión {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Crear reglas de decisión"
>abstract="Las reglas de decisión permiten definir el público de los elementos de decisión mediante la aplicación de restricciones, ya sea directamente en el nivel del elemento de decisión o dentro de una estrategia de selección específica. Esto le permite controlar con precisión qué elementos se deben presentar a quién."

>[!BEGINSHADEBOX &quot;Lo que encontrará en esta guía de documentación&quot;]

* [Introducción a Experience Decisioning](gs-experience-decisioning.md)
* Administrar los elementos de decisión: [Configurar el catálogo de artículos](catalogs.md) - [Crear elementos de decisión](items.md) - [Administrar colecciones de elementos](collections.md)
* Configurar la selección de elementos: **[Creación de reglas de decisión](rules.md)** - [Crear métodos de clasificación](ranking.md)
* [Creación de estrategias de selección](selection-strategies.md)
* [Creación de políticas de decisión](create-decision.md)

>[!ENDSHADEBOX]

Las reglas de decisión permiten definir el público de los elementos de decisión mediante la aplicación de restricciones, ya sea directamente en el nivel del elemento de decisión o dentro de una estrategia de selección específica. Esto le permite controlar con precisión qué elementos se deben presentar a quién.

Por ejemplo, consideremos un escenario en el que tenga elementos de decisión que presenten productos relacionados con el yoga diseñados para mujeres. Con las reglas de decisión, puede especificar que estos elementos solo deben mostrarse a perfiles cuyo sexo sea &quot;Mujer&quot; y que hayan indicado un &quot;Punto de interés&quot; en &quot;Yoga&quot;.

>[!NOTE]
>
>Además de las reglas de decisión a nivel de elemento y de estrategia de selección, también puede definir la audiencia a nivel de campaña. [Más información](../campaigns/create-campaign.md#audience)

Se puede acceder a la lista de reglas de decisión en la **[!UICONTROL Configuración]** / **[!UICONTROL Reglas de decisiones]** menú.

![](assets/decision-rules-list.png)

## Crear una regla de decisión {#create}

Para crear una regla de decisión, siga estos pasos:

1. Vaya a **[!UICONTROL Configuración]** / **[!UICONTROL Reglas de decisión]** luego haga clic en **[!UICONTROL Crear regla]** botón.

1. Se abre la pantalla de creación de reglas de decisión. Especifique un nombre para la regla y una descripción.

1. Cree la regla de decisión que se adapte a sus necesidades con el Generador de segmentos de Adobe Experience Platform. Para ello, puede aprovechar varias fuentes de datos, como atributos de perfil, audiencias o datos de contexto procedentes de Adobe Experience Platform. [Aprenda a aprovechar los datos de contexto en las reglas de decisión](#context-data)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >El Generador de segmentos que se proporciona para crear reglas de decisión presenta algunas particularidades en comparación con el que se utiliza con el servicio de segmentación de Adobe Experience Platform.  Sin embargo, el proceso global descrito en la documentación sigue siendo válido para generar reglas de decisiones. [Obtenga información sobre cómo crear definiciones de segmentos](../audience/creating-a-segment-definition.md)

1. Al añadir y configurar nuevos campos en el espacio de trabajo, la variable **[!UICONTROL Propiedades de audiencia]** Este panel muestra información sobre los perfiles estimados que pertenecen a la audiencia. Clic **[!UICONTROL Actualizar estimación]** para actualizar los datos.

   >[!NOTE]
   >
   >Las estimaciones de perfil no están disponibles cuando los parámetros de regla incluyen datos que no están en el perfil, como datos de contexto.

1. Una vez preparada la regla de decisión, haga clic en **[!UICONTROL Guardar]**. La regla creada aparece en la lista y está disponible para su uso en elementos de decisión y estrategias de selección para regular la presentación de elementos de decisión a perfiles.

## Aprovechamiento de los datos de contexto en reglas de decisión {#context-data}

La pantalla de creación de reglas de Experience Decisioning le permite aprovechar cualquier información disponible en Adobe Experience Platform para crear reglas de decisión. Por ejemplo, puede diseñar una regla de decisión que requiera que el clima actual sea de ≥80 grados.

Para ello, primero debe definir los datos que desea que estén disponibles en Experience Decisioning. Una vez finalizado, estos datos se integran perfectamente en Experience Decisioning en la **[!UICONTROL Datos de contexto]** pestaña disponible al crear una regla de decisión.

![](assets/decision-rules-context.png)

Los pasos para alimentar Experience Decisioning con datos de Adobe Experience Platform son los siguientes:

1. Crear un **Esquema de evento de experiencia**  en Adobe Experience Platform y sus aplicaciones asociadas **conjunto de datos**. [Aprenda a crear esquemas](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. Cree una nueva secuencia de datos de Adobe Experience Platform:

   1. Vaya a **[!UICONTROL Datastreams]** y seleccione **[!UICONTROL Nueva secuencia de datos]**.

   1. En el **[!UICONTROL Esquema de evento]** , seleccione el esquema de Experience Event creado anteriormente y haga clic en **[!UICONTROL Guardar]**.

      ![](assets/decision-rule-context-datastream.png)

   1. Clic **[!UICONTROL Añadir servicio]** y seleccione &quot;Adobe Experience Platform&quot; como servicio. En el **[!UICONTROL Conjunto de datos de evento]** , seleccione el conjunto de datos de evento creado anteriormente y habilite la variable **[!UICONTROL Adobe Journey Optimizer]** opción.

      ![](assets/decision-rules-context-datastream-service.png)

Una vez guardada la secuencia de datos, la información del conjunto de datos seleccionado se recupera automáticamente y se integra en Experience Decisioning, y normalmente está disponible en un plazo aproximado de 24 horas.

Para obtener más información sobre cómo trabajar con Adobe Experience Platform, explore los siguientes recursos:

* [Esquemas del modelo de datos de experiencia (XDM)](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [Conjuntos de datos](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [Datastreams](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
