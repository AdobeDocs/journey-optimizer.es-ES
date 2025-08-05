---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Cambiar dimensión
description: Aprenda a utilizar la actividad Cambiar dimensión
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 74%

---


# Cambiar dimensión {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Generación de un complemento"
>abstract="Puede generar una transición saliente adicional con la población restante, que se excluyó como duplicado. Para ello, active la opción **Generar complemento**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Actividad cambiar dimensión"
>abstract="Esta actividad le permite cambiar la dimensión de segmentación a medida que genera un público. Desplace el eje en función de la plantilla de datos y la dimensión de entrada. Por ejemplo, puede cambiar de la dimensión “contratos” a la dimensión “clientes”."

Como especialista en marketing, puede mejorar la segmentación de audiencia cambiando de una entidad de datos a una relacionada dentro de una campaña orquestada. Esto le permite ir más allá de los perfiles de usuario y centrarse en comportamientos específicos, como compras, reservas u otras interacciones.

Para lograrlo, use la actividad **[!UICONTROL Cambiar dimensión]**. Permite ajustar la dimensión de segmentación durante la campaña orquestada.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Configuración de la actividad Cambiar dimensión {#configure}

Siga estos pasos para configurar la actividad **[!UICONTROL Cambiar dimensión]**:

1. Agregue una actividad **[!UICONTROL Cambiar dimensión]** a su campaña orquestada.

   ![](../assets/orchestrated-change-dimension.png)

1. Defina la **[!UICONTROL Nueva dimensión de público destinatario]**. Se guardan todos los registros durante el cambio de dimensión.


## Ejemplo {#example}

Este caso de uso se centra en enviar un SMS a los perfiles que hayan creado una lista de deseos durante el mes pasado.

Comience con la actividad **[!UICONTROL Generarr público]**, usando la dimensión de segmentación **[!UICONTROL Lista de deseos]** para identificar todas las listas de deseos relevantes.

A continuación, añada la actividad **[!UICONTROL Cambiar dimensión]** para cambiar la dimensión de segmentación de **[!UICONTROL Lista de deseos]** a **[!UICONTROL Destinatarios].** Este paso garantiza que los objetivos de la campaña orquestada sean los perfiles correctos vinculados a esas listas de deseos, lo que permite enviar el SMS a los perfiles deseados.

![](../assets/orchestrated-change-dimension-example.png)
