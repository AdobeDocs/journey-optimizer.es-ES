---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la experimentación en la optimización de mensajes
description: Aprenda a utilizar experimentos de contenido para probar varias versiones de contenido y determinar cuál tiene el mejor rendimiento.
role: User
level: Intermediate
keywords: experimentación, optimización, pruebas A/B, experimento de contenido, tratamientos
source-git-commit: f4eb982ba0840acfe336e759fcbf9cfd47b3b98c
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 2%

---

# Uso de la experimentación {#experimentation}

>[!NOTE]
>
>Esta página proporciona información general sobre cómo utilizar la experimentación en la optimización de contenido. Para obtener información detallada sobre los experimentos de contenido, incluidas las opciones de configuración, las métricas y los análisis, consulte la [documentación del experimento de contenido](../content-management/get-started-experiment.md).

La experimentación le permite probar varias versiones de contenido para determinar cuál tiene el mejor rendimiento en función de las métricas de éxito predefinidas.

Para configurar la experimentación, siga los pasos a continuación.

Supongamos que desea probar los siguientes mensajes promocionales en una campaña:

* **Tratamiento A**: &quot;20% de descuento en tu próxima compra&quot;
* **Tratamiento B**: &quot;Envío gratuito en pedidos superiores a $50&quot;
* **Tratamiento C**: &quot;Recibe tu tarjeta de regalo de $10&quot;

Para configurar la experimentación y determinar qué mensaje genera la mayor cantidad de compras, siga los pasos a continuación.

1. Crear un [recorrido](../building-journeys/journey-gs.md#jo-build) o una [campaña](../campaigns/create-campaign.md).

   >[!NOTE]
   >
   >Si está en un recorrido, agregue una actividad **[!UICONTROL Action]**, elija una actividad de canal y seleccione **[!UICONTROL Configure action]**. [Más información](../building-journeys/journey-action.md#add-action)

1. En la ficha **[!UICONTROL Acciones]**, seleccione dos acciones entrantes, por ejemplo [experiencia basada en código](../code-based/get-started-code-based.md) y [En la aplicación](../../rp_landing_pages/in-app-landing-page.md).

1. En la sección **[!UICONTROL Optimización]**, seleccione **[!UICONTROL Crear experimento]**.

   ![](../campaigns/assets/msg-optimization-select-experiment.png){width=85%}

1. Diseñe y configure el experimento de contenido como desee. [Descubra cómo](../content-management/content-experiment.md)

   ![](../campaigns/assets/msg-optimization-create-experiment.png){width=85%}

   Una vez definido el experimento, se aplica a todas las acciones insertadas en esa campaña o a través de la actividad de recorrido **[!UICONTROL Action]**, lo que significa que los mismos clientes ven las mismas ofertas en todas las superficies.

   >[!NOTE]
   >
   >Puede seleccionar otras acciones: la experimentación se aplica a todas las acciones agregadas a la campaña o a la [actividad de acción](../building-journeys/journey-action.md) del recorrido.

1. [Activar](../campaigns/review-activate-campaign.md) tu recorrido o campaña.

Una vez que el recorrido/campaña está activo, los usuarios tienen asignadas aleatoriamente las diferentes variaciones de contenido. [!DNL Journey Optimizer] hace un seguimiento de qué variación genera más compras y proporciona perspectivas procesables.

Sigue el éxito de tu campaña con los informes [recorrido](../reports/journey-global-report-cja.md) y [campaña](../reports/campaign-global-report-cja-experimentation.md). <!--Link to Experimentation journey reportis missing-->

