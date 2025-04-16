---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Change dimension
description: Aprenda a utilizar la actividad de la dimensión Cambiar
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 22%

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

La actividad **Cambiar dimensión** es una actividad **Segmentación**. Esta actividad le permite cambiar la dimensión de segmentación mientras crea la campaña orquestada. Desplaza el eje en función de la plantilla de datos y la dimensión de entrada.

Por ejemplo, puede cambiar la dimensión de segmentación de una campaña orquestada de &quot;Destinatarios&quot; a &quot;Aplicación de suscriptores&quot; para enviar notificaciones push a los destinatarios objetivo.

>[!IMPORTANT]
>
>Tenga en cuenta que las actividades **[!UICONTROL Cambiar dimensión]** y **[!UICONTROL Cambiar fuente de datos]** no deben agregarse en una fila. Si necesita usar ambas actividades consecutivamente, asegúrese de incluir una actividad **[!UICONTROL Enrichement]** entre ellas. Esto garantiza una ejecución adecuada y evita posibles conflictos o errores.

## Configuración de la actividad Change dimension {#configure}

Siga estos pasos para configurar la actividad **Cambiar dimensión**:

1. Agregue una actividad **Change dimension** a su campaña orquestada.

   ![](../assets/workflow-change-dimension.png)

1. Defina **Nueva dimensión de destino**. Durante el cambio de dimensión, se guardan todos los registros. Otras opciones aún no están disponibles.

1. Ejecute la campaña orquestada para ver el resultado. Compare los datos de las tablas antes y después de la actividad de dimensión de cambio y compare la estructura de las tablas de campañas organizadas.

## Ejemplo {#example}

En este ejemplo, deseamos enviar un envío SMS a todos los perfiles que han realizado una compra. Para ello, en primer lugar utilizamos una actividad **[!UICONTROL Generar audiencia]** vinculada a una dimensión de segmentación personalizada &quot;Compra&quot; para segmentar todas las compras que se produjeron.

Luego usamos una actividad **[!UICONTROL Change dimension]** para cambiar la dimensión de segmentación de la campaña orquestada a &quot;Destinatarios&quot;. Esto nos permite segmentar los destinatarios que coincidan con la consulta.

![](../assets/workflow-change-dimension-example.png)
