---
title: Aprovechamiento de los datos de contexto en Experience Decisioning
description: Aprenda a aprovechar los datos de contexto en Experience Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilidad limitada"
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# Aprovechamiento de los datos de contexto en Experience Decisioning {#context}

Con Experience Decisioning, puede aprovechar cualquier información disponible en Adobe Experience Platform para realizar varias acciones, como crear [reglas de decisión](rules.md) o [clasificación de fórmulas](ranking.md). Por ejemplo, puede diseñar una regla de decisión que requiera que el clima actual sea de ≥80 grados en el momento en que se realice la solicitud de decisión.

>[!NOTE]
>
>Los datos de contexto se definen en Adobe Experience Platform y se envían en el momento de una solicitud de decisión. No incluye datos históricos.

Para utilizar datos de contexto, primero debe definir los datos que desea que estén disponibles en Experience Decisioning. Una vez finalizado, estos datos se integran perfectamente en Experience Decisioning en la **[!UICONTROL Datos de contexto]** pestaña disponible al crear una regla de decisión. También puede aprovechar los datos al editar una fórmula de clasificación.

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
