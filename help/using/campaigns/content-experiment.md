---
solution: Journey Optimizer
product: journey optimizer
title: Crear un experimento de contenido
description: Aprenda a crear un experimento de contenido en sus campañas
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: efea1bbd5154d378daf1f52315384156b6d23ae3
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 0%

---

# Creación de un experimento de contenido {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="Experimento de contenido"
>abstract="TBC"

>[!AVAILABILITY]
>
>La variable **Experimento de contenido** Actualmente, esta función solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, póngase en contacto con su representante de Adobe.

Utilice el experimento de contenido de Journey Optimizer para definir varios tratamientos de envío. La audiencia de interés se asigna aleatoriamente a cada tratamiento para determinar cuál tiene mejor rendimiento con respecto a la métrica de interés. Puede elegir entre variar el contenido de la entrega, el asunto o el remitente.

>[!NOTE]
>
>Antes de empezar con el experimento de contenido, asegúrese de que la configuración de informes esté configurada para sus conjuntos de datos personalizados. Obtenga más información en [esta sección](reporting-configuration.md).

En el siguiente ejemplo, el objetivo de la entrega se ha dividido en dos grupos, cada uno de los cuales representa el 45 % de la población de destino, y un grupo de exclusión del 10 %, que no recibe la entrega.

Cada persona de la audiencia de destino recibirá una versión de un correo electrónico, con una línea de asunto que es una de las dos siguientes:

* una que promociona directamente una oferta del 10 % sobre la nueva colección y una imagen.
* el otro solo anuncia una oferta especial sin especificar el 10 % de descuento sin ninguna imagen.

El objetivo aquí es ver si los destinatarios interactuarán con el correo electrónico según el experimento recibido. Por lo tanto, elegiremos **[!UICONTROL Email Opens]** como métrica objetivo principal en este experimento de contenido.

![](assets/content_experiment.png)

## Cree la campaña {#campaign-experiment}

1. En el **[!UICONTROL Campaigns]** página, haga clic en **[!UICONTROL Create campaign]**.

   ![](assets/content_experiment_1.png)

1. Seleccione el canal y, a continuación, el **[!UICONTROL Surface]** desea utilizar para este envío. Para obtener más información, consulte [Superficies de canal](../configuration/channel-surfaces.md) página.

   ![](assets/content_experiment_2.png)

1. Haga clic en **[!UICONTROL Create]**.

1. Configure el **[!UICONTROL Properties]** del envío:
   * **[!UICONTROL Title]**
   * **[!UICONTROL Description]**
   * **[!UICONTROL Category]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transactional]**

1. Para iniciar el experimento de contenido, active la opción **[!UICONTROL Content experiment]** . La variable **[!UICONTROL Content experiment]** aparece.

   ![](assets/content_experiment_3.png)

1. Defina la audiencia objetivo. Para ello, haga clic en el botón **[!UICONTROL Select audience]** para mostrar la lista de segmentos disponibles de Adobe Experience Platform. [Más información sobre los segmentos](../segment/about-segments.md)

   En el **[!UICONTROL Identity namespace]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado. [Más información](get-started-experiment.md#content-experiment-work)

1. Para ejecutar la campaña en una fecha específica o con frecuencia recurrente, configure la sección Programar . [Más información](create-campaign.md)

1. Haga clic en **[!UICONTROL Edit content]** para comenzar a personalizar los diferentes **[!UICONTROL Treatments]**.

   ![](assets/content_experiment_4.png)

## Cree sus tratamientos {#treatment-experiment}

1. En el **[!UICONTROL Edit content]** , empiece a personalizar su tratamiento A.

   Para este tratamiento, especificaremos la oferta especial directamente en la línea de asunto.

   ![](assets/content_experiment_5.png)

1. Después de diseñar su primer tratamiento, desde la **[!UICONTROL More actions]** botón, haga clic en **[!UICONTROL Duplicate]**.

   También puede elegir iniciar un nuevo tratamiento desde cero haciendo clic en el botón **[!UICONTROL Content experiment]** botón ![](assets/content_experiment_16.png) para acceder a las opciones avanzadas, **[!UICONTROL Add treatment]**.

   ![](assets/content_experiment_7.png)

1. Cambie el **[!UICONTROL Title]** de su tratamiento para diferenciarlos mejor.

   ![](assets/content_experiment_8.png)

1. Personalice su segundo tratamiento según sea necesario.

   Aquí, elegimos no especificar la oferta en la **[!UICONTROL Subject line]**.

   ![](assets/content_experiment_9.png)

Una vez que los tratamientos estén personalizados, puede empezar a configurar el Experimento de contenido.

## Configurar el experimento de contenido {#configure-experiment}

1. Cuando ambos envíos están personalizados, desde la **[!UICONTROL Edit content]** ventana, seleccione **[!UICONTROL Configure content experiment]**.

   ![](assets/content_experiment_10.png)

1. Seleccione los objetivos que desee configurar para el experimento.

   Para nuestro experimento, seleccionamos **[!UICONTROL Email open]** para comprobar si los destinatarios abrirán sus correos electrónicos si el código de promoción está en la línea de asunto.

   ![](assets/content_experiment_11.png)

1. Elija agregar una **[!UICONTROL Holdout]** a su envío. Este grupo no recibirá ningún contenido de esta campaña.

   Si activa la barra de alternancia, se tomará automáticamente el 10 % de la población; puede ajustar este porcentaje si es necesario.

   ![](assets/content_experiment_12.png)

1. A continuación, puede elegir asignar un porcentaje preciso a cada **[!UICONTROL Treatment]** o simplemente encienda el **[!UICONTROL Distribute evenly]** barra de herramientas.

   ![](assets/content_experiment_13.png)

1. Haga clic en **[!UICONTROL Save]** cuando la configuración esté configurada.

1. Cuando el experimento de contenido esté listo, puede hacer clic en **[!UICONTROL Review to activate]** para mostrar un resumen de la campaña. Las alertas se muestran si algún parámetro es incorrecto o falta.

   ![](assets/content_experiment_15.png)

1. Compruebe que la campaña esté correctamente configurada y haga clic en **[!UICONTROL Activate]** para iniciarlo.

   ![](assets/content_experiment_14.png)

Después de configurar la experimentación y la campaña, puede seguir el éxito de la entrega con el informe de campaña.

## Informe Objetivos {#objectives-global}

>[!AVAILABILITY]
>
>Actualmente, la función de experimento de contenido solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, póngase en contacto con su representante de Adobe.

![](assets/performance_report.gif)

La variable **[!UICONTROL Objectives]** del informe de Campaign le permite ajustar mejor los informes de las entregas mediante la segmentación de una métrica específica.

La variable **[!UICONTROL Objectives]** están vinculados a **[!UICONTROL Datasets]** que definen una conexión con un sistema para recuperar información adicional. Una lista de elementos integrados **[!UICONTROL Objectives]** está disponible, pero puede agregar el suyo propio añadiendo **[!UICONTROL Dataset]**. Para ver el procedimiento detallado, consulte esta [sección](reporting-configuration.md).

Después de seleccionar los objetivos sobre los que desea establecer el objetivo, los dos **[!UICONTROL Performance overview]** y **[!UICONTROL Campaign objective]** Las utilidades proporcionan un resumen detallado del rendimiento de su envío.

Con la variable **[!UICONTROL Campaign objective]** , también puede elegir comparar su objetivo principal con otra métrica.

Tenga en cuenta que cada utilidad se puede cambiar de tamaño y eliminar si es necesario. Para obtener más información, consulte [sección](../reports/global-report.md#modify-dashboard).

## Informe de experimentación {#experimentation-global}

>[!AVAILABILITY]
>
>Actualmente, la función de experimento de contenido solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, póngase en contacto con su representante de Adobe.

![](assets/experimentation_report_3.png)

Desde la campaña **[!UICONTROL Global report]**, el **[!UICONTROL Experimentation]** La pestaña detalla la información principal en relación con el rendimiento de cada variante y si hay un mejor rendimiento.

Tenga en cuenta que la definición del mejor ejecutante puede tardar algún tiempo, y que se representará con este icono ![](assets/experimentation_report_1.png).

La variable **[!UICONTROL Experiment result]** widget detalla el rendimiento de cada variante. Puede cambiar su línea base seleccionando uno de los tratamientos de la **[!UICONTROL Baseline]** la lista desplegable . El mejor tratamiento se representará con un icono de estrella.

La tabla presenta las siguientes métricas:

* **[!UICONTROL Profiles]**: Número de perfiles objetivo para este tratamiento.

* **[!UICONTROL Unique outbound clicks]**: Recuento total de clics en los canales salientes.

* **[!UICONTROL Count per profile]**: Valor total de la métrica de objetivo Experimento dividido por el número de perfiles.

* **[!UICONTROL Confidence interval]**: Diferencia porcentual en el rendimiento entre el valor basal y el tratamiento de mejor rendimiento. [Más información](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Average lift]**: Mejora porcentual en la tasa de conversión de un tratamiento determinado respecto al valor basal. [Más información](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Confidence]**: Evidencia de que un tratamiento determinado es el mismo que el tratamiento basal. [Más información](../campaigns/experiment-calculations.md#understand-confidence)

Para profundizar en estos resultados y cómo interpretarlos, consulte [esta página](../campaigns/get-started-experiment.md#interpret-results).
