---
title: Métodos de clasificación
description: Aprenda a trabajar con métodos de clasificación
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilidad limitada"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 27%

---

# Métodos de clasificación {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Crear fórmulas de clasificación"
>abstract="Fórmulas le permite definir reglas que determinarán qué elemento se debe presentar primero, en lugar de tener en cuenta las puntuaciones de prioridad del elemento. Una vez creado un método de clasificación, puede asignarlo a una estrategia de selección para definir qué elementos se deben seleccionar primero."

Los métodos de clasificación permiten clasificar los elementos que se muestran en un perfil determinado. Una vez creado un método de clasificación, puede asignarlo a una estrategia de selección para definir qué elementos se deben seleccionar primero.

Hay dos tipos de métodos de clasificación disponibles:

* **Fórmulas** permite definir reglas que determinan qué elemento debe presentarse primero, en lugar de tener en cuenta las puntuaciones de prioridad del elemento.

* **modelos de IA** le permite utilizar sistemas de modelos formados que aprovecharán varios puntos de datos para determinar qué elemento se debe presentar primero.

## Creación de métodos de clasificación {#create}

Para crear un método de clasificación, siga estos pasos:

1. Vaya a **[!UICONTROL Configuración de estrategia]** y, a continuación, seleccione **[!UICONTROL Fórmulas]** o **[!UICONTROL modelos de IA]** según el tipo de clasificación que desee utilizar.

1. Haga clic en **[!UICONTROL Crear fórmula]** o **[!UICONTROL Crear modelo de IA]** en la esquina superior derecha de la pantalla.

   ![](assets/ranking-create.png)

1. Configure la fórmula o el modelo de IA para adaptarlo a sus necesidades y, a continuación, guárdelo.

   Encontrará información detallada sobre cómo crear fórmulas de clasificación y modelos de IA en la documentación de administración de decisiones:

   * [Fórmulas de clasificación](../offers/ranking/create-ranking-formulas.md)
   * [modelos de IA](../offers/ranking/ai-models.md)


## Aprovechamiento de atributos de elementos de decisión en fórmulas {#items}

Las fórmulas de clasificación se expresan en **Sintaxis PQL** y pueden aprovechar varios atributos, como atributos de perfil, [datos de contexto](context-data.md) y atributos relacionados con los elementos de decisión.

Para aprovechar los atributos relacionados con los elementos de decisión en las fórmulas, asegúrese de seguir la sintaxis siguiente en el código de la fórmula de clasificación. Expanda cada sección para obtener más información:

+++Aproveche los atributos estándar de los elementos de decisión

![](assets/formula-attribute.png)

+++

+++Aproveche los atributos personalizados de los elementos de decisión

![](assets/formula-attribute-custom.png)

+++
