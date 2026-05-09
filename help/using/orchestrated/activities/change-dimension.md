---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Cambiar dimensión
description: Aprenda a utilizar la actividad Cambiar dimensión
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
version: Campaign Orchestration
source-git-commit: 384f4e4b4c3acd9f1f1d73d4b140845870b31289
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 50%

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
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.
-->

## Configuración de la actividad Cambiar dimensión {#configure}

Siga estos pasos para configurar la actividad **[!UICONTROL Cambiar dimensión]**:

1. Agregue una actividad **[!UICONTROL Cambiar dimensión]** a su campaña orquestada.

   ![](../assets/orchestrated-change-dimension.png)

1. Defina la **[!UICONTROL Nueva dimensión de público destinatario]**. El paso Cambiar dimensión utiliza una unión externa: pasan todos los registros de la población de entrada, incluidos los que no tienen ninguna entrada coincidente en la nueva dimensión.

   >[!IMPORTANT]
   >
   >Los registros que no tienen un perfil coincidente en la nueva dimensión de segmentación se **excluyen silenciosamente a la hora de envío del mensaje**. Esta exclusión no se refleja actualmente en los registros de exclusión. Para identificar registros no coincidentes de forma temprana, use la opción **Previsualizar resultados** en la transición después del paso Cambiar dimensión y compruebe que los recuentos de registros se alinean con las expectativas antes de continuar.


## Ejemplo {#example}

Este caso de uso se centra en enviar un SMS a los perfiles que hayan creado una lista de deseos durante el mes pasado.

Comience con la actividad **[!UICONTROL Generarr público]**, usando la dimensión de segmentación **[!UICONTROL Lista de deseos]** para identificar todas las listas de deseos relevantes.

A continuación, agregue una actividad **[!UICONTROL Change dimension]** para cambiar la dimensión de segmentación de **[!UICONTROL Wishlist]** a **[!UICONTROL Destinatario].** Este paso garantiza que la campaña orquestada se dirija a los perfiles correctos vinculados a esas listas de deseos, lo que permite enviar el SMS a los perfiles deseados.

![](../assets/orchestrated-change-dimension-example.png)
