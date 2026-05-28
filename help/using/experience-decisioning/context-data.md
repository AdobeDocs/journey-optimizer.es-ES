---
title: Aprovechamiento de datos de contexto en Decisioning
description: Aprenda a aprovechar los datos de contexto en Decisioning
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: ddc4b681-020b-4433-b4b3-3791c41907c9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/tL3mwS9sDtSkSVljry1EeqPnYn4U34TvXCg5jX2ej3M
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# Aprovechamiento de datos de contexto en Decisioning {#context}

Con Decisioning, puede aprovechar cualquier información disponible en Adobe Experience Platform para realizar diversas acciones, como crear [reglas de decisión](rules.md) o [fórmulas de clasificación](ranking/ranking.md).

Por ejemplo, puede diseñar una regla de decisión que requiera que el clima actual sea de ≥80 grados en el momento en que se realice la solicitud de decisión.

>[!NOTE]
>
>Los datos de contexto se definen en Adobe Experience Platform y se envían en el momento de una solicitud de decisión. No incluye datos históricos.

Para utilizar datos de contexto, primero debe definir los datos que desea que estén disponibles en Decisioning. Una vez finalizado, estos datos se integran perfectamente con Decisioning en la pestaña **[!UICONTROL Datos de contexto]** disponible al crear una regla de decisión. También puede aprovechar los datos al editar una fórmula de clasificación.

![](assets/decision-rules-context.png)

Los pasos para alimentar Decisioning con datos de Adobe Experience Platform son los siguientes:

1. Crear un **esquema de evento de experiencia** en Adobe Experience Platform y su **conjunto de datos** asociado. [Aprenda a crear esquemas](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. Cree una nueva secuencia de datos de Adobe Experience Platform:

   1. Vaya al menú **[!UICONTROL Secuencias de datos]** y seleccione **[!UICONTROL Nueva secuencia de datos]**.

   1. En la lista desplegable **[!UICONTROL Esquema de evento]**, seleccione el esquema de evento de experiencia creado anteriormente y haga clic en **[!UICONTROL Guardar]**.

      ![](assets/decision-rule-context-datastream.png)

   1. Haga clic en **[!UICONTROL Agregar servicio]** y seleccione &quot;Adobe Experience Platform&quot; como servicio. En la lista desplegable **[!UICONTROL Conjunto de datos de evento]**, seleccione el conjunto de datos de evento creado anteriormente y habilite la opción **[!UICONTROL Adobe Journey Optimizer]**.

      ![](assets/decision-rules-context-datastream-service.png)

Una vez guardado el conjunto de datos, la información del conjunto de datos seleccionado se recupera automáticamente y se integra en Decisioning, lo que generalmente está disponible en aproximadamente 24 horas.

Para obtener más información sobre cómo trabajar con Adobe Experience Platform, explore los siguientes recursos:

* [Esquemas del modelo de datos de experiencia (XDM)](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [Conjuntos de datos](https://experienceleague.adobe.com/es/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [Secuencias de datos](https://experienceleague.adobe.com/es/docs/experience-platform/datastreams/overview){target="_blank"}
