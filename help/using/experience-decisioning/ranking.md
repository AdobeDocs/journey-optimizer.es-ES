---
title: Métodos de clasificación
description: Aprenda a trabajar con métodos de clasificación
feature: Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 07704f99aff7d92e8db76755f6617345bac56590
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 5%

---

# Métodos de clasificación {#rankings}

Los métodos de clasificación permiten clasificar los elementos que se muestran en un perfil determinado. Una vez creado un método de clasificación, puede asignarlo a una estrategia de selección para definir qué elementos se deben seleccionar primero.

Hay dos tipos de métodos de clasificación disponibles:

* **Las fórmulas** le permiten definir reglas que determinan qué elemento se debe presentar primero, en lugar de tener en cuenta las puntuaciones de prioridad del elemento.

* **modelos de IA** le permiten usar sistemas de modelos entrenados que aprovecharán varios puntos de datos para determinar qué elemento se debe presentar primero.

## Creación de métodos de clasificación {#create}

Para crear un método de clasificación, siga estos pasos:

1. Vaya al menú **[!UICONTROL Configuración de estrategia]** y, a continuación, seleccione el menú **[!UICONTROL Fórmulas]** o **[!UICONTROL Modelos de IA]** según el tipo de clasificación que desee utilizar.

1. Haga clic en el botón **[!UICONTROL Crear fórmula]** o **[!UICONTROL Crear modelo de IA]** en la esquina superior derecha de la pantalla.

   ![](assets/ranking-create.png)

1. Configure la fórmula o el modelo de IA para adaptarlo a sus necesidades y, a continuación, guárdelo.

   Encontrará información detallada sobre cómo crear fórmulas de clasificación y modelos de IA en la documentación de administración de decisiones:

   * [Fórmulas de clasificación](exd-ranking-formulas.md)
   * [Modelos de IA](../offers/ranking/ai-models.md)

   >[!NOTE]
   >
   >La profundidad de anidación en una fórmula de clasificación está limitada a 30 niveles. Esto se mide contando los `)` paréntesis de cierre en la cadena de PQL. Una cadena de regla puede tener un tamaño máximo de 8 KB para caracteres codificados con UTF-8. Esto equivale a 8.000 caracteres ASCII (1 byte cada uno) o a 2.000-4.000 caracteres no ASCII (2-4 bytes cada uno). [Más información sobre las limitaciones y protecciones de decisiones](gs-experience-decisioning.md#guardrails)

Una política de decisión admite hasta 10 estrategias de selección y elementos de decisión combinados. [Más información sobre las limitaciones y protecciones de decisiones](gs-experience-decisioning.md#guardrails)

+++ Optimizando modelos en métricas [!DNL Customer Journey Analytics] personalizadas

>[!NOTE]
>
>Esta capacidad solo está disponible para [!DNL Customer Journey Analytics] clientes con derechos de administrador.
>
>Antes de empezar, asegúrese de que ha integrado Journey Optimizer con Customer Journey Analytics para exportar los conjuntos de datos de Journey Optimizer a sus vistas de datos predeterminadas. [Aprenda a aprovechar [!DNL Journey Optmizer] los datos en [!DNL Customer Journey Analytics]](../reports/cja-ajo.md)

Los modelos de optimización personalizados son un tipo de modelo de IA que le permite definir objetivos comerciales y utiliza datos de clientes para entrenar modelos orientados a negocios para servir ofertas personalizadas y maximizar KPI. Encontrará información detallada sobre cómo crear un modelo de IA personalizado en la [documentación de administración de decisiones](../offers/ranking/personalized-optimization-model.md).

De forma predeterminada, los modelos de optimización personalizados utilizan **clics en ofertas** como métrica de optimización. Si está trabajando con [!DNL Customer Journey Analytics], [!DNL Decisioning] le permite aprovechar sus propias métricas personalizadas para optimizar su modelo en.

Para ello, acceda a la pantalla de creación personalizada del modelo de IA y expanda la lista desplegable **[!UICONTROL Evento de conversión]**. Todas las métricas de su [!DNL Customer Journey Analytics] [vista de datos](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"} predeterminada se muestran en la lista. Seleccione la métrica en la que desea optimizar el modelo y, a continuación, complete la creación del modelo de IA como de costumbre.

![](assets/ai-ranking-custom-metrics.png)

>[!NOTE]
>
>De manera predeterminada, las métricas de [!DNL Customer Journey Analytics] utilizan un modelo de atribución &quot;Último contacto&quot;, que asigna el 100% del crédito al punto de contacto que se produce más recientemente antes de la conversión.
>
>Aunque es posible modificar el modelo de atribución, no todos los modelos de atribución son ideales para la optimización del modelo de IA. Recomendamos seleccionar cuidadosamente un modelo de atribución que se ajuste a sus objetivos de optimización para garantizar la precisión y el rendimiento del modelo.
>
>Para obtener más información sobre los modelos de atribución disponibles y las instrucciones de uso, consulte la [[!DNL Customer Journey Analytics] documentación](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/attribution){target="_blank"}

+++

## Aprovechamiento de atributos de elementos de decisión en fórmulas {#items}

Las fórmulas de clasificación se expresan en **sintaxis de PQL** y pueden aprovechar varios atributos, como atributos de perfil, [datos de contexto](context-data.md) y atributos relacionados con los elementos de decisión.

>[!NOTE]
>
>Para obtener más información sobre cómo usar la sintaxis de PQL, consulte la [documentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=es)

Para aprovechar los atributos relacionados con los elementos de decisión en las fórmulas, asegúrese de seguir la sintaxis siguiente en el código de la fórmula de clasificación. Expanda cada sección para obtener más información:

+++Aproveche los atributos estándar de los elementos de decisión

![](assets/formula-attribute.png)

+++

+++Aproveche los atributos personalizados de los elementos de decisión

![](assets/formula-attribute-custom.png)

+++
