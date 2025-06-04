---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Change dimension
description: Aprenda a utilizar la actividad de la dimensión Cambiar
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 7f535b87e415ae9191199b34476adb5c977b66e9
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 23%

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

Como especialista en marketing, puede cambiar la dimensión objetivo de una entidad a otra entidad vinculada dentro de una campaña orquestada y refinar la segmentación de audiencia en función de diferentes conjuntos de datos, como pasar de la generación de perfiles de usuarios a la segmentación de sus acciones o reservas específicas.

Para ello, usa la actividad de segmentación **Change dimension**. Esta actividad le permite cambiar la dimensión de segmentación mientras crea la campaña orquestada. Desplaza el eje en función de la plantilla de datos y la dimensión de entrada.

Por ejemplo, puede cambiar la dimensión de segmentación de una campaña orquestada de &quot;Perfil&quot; a &quot;Contratos&quot; para enviar mensajes al propietario del contrato de destino.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Configuración de la actividad Change dimension {#configure}

Siga estos pasos para configurar la actividad **Cambiar dimensión**:

1. Agregue una actividad **Change dimension** a su campaña orquestada.

   ![](../assets/change-dimension.png)

1. Defina **Nueva dimensión de destino**. Durante el cambio de dimensión, se guardan todos los registros.

1. Ejecute la campaña orquestada para ver el resultado. Compare los datos de las tablas antes y después de la actividad de dimensión de cambio y compare la estructura de las tablas de campañas organizadas.

## Ejemplo {#example}

En este ejemplo, deseamos enviar un envío SMS a todos los perfiles que han realizado una compra. Para ello, en primer lugar utilizamos una actividad **[!UICONTROL Generar audiencia]** vinculada a una dimensión de segmentación personalizada &quot;Compra&quot; para segmentar todas las compras que se produjeron.

Luego usamos una actividad **[!UICONTROL Change dimension]** para cambiar la dimensión de segmentación de la campaña orquestada a &quot;Destinatarios&quot;. Esto nos permite segmentar los destinatarios que coincidan con la consulta.

![](../assets/change-dimension-example.png)
