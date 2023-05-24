---
solution: Journey Optimizer
product: journey optimizer
title: Crear un experimento de contenido
description: Aprenda a crear un experimento de contenido en sus campañas
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: contenido, experimento, múltiple, audiencia, tratamiento
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
badge: label="Beta" type="Informative"
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 10%

---

# Creación de un experimento de contenido {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="Experimento de contenido"
>abstract="Puede elegir entre modificar el contenido del envío, el asunto o el remitente para definir varios tratamientos de envío y determinar la mejor combinación para sus audiencias."

>[!BEGINSHADEBOX]

Lo que encontrará en esta documentación:

* [Introducción al experimento de contenido](get-started-experiment.md)
* **[Creación de un experimento de contenido](content-experiment.md)**
* [Comprensión de los cálculos estadísticos](experiment-calculations.md)
* [Configurar informes de experimentación](reporting-configuration.md)
* [Cálculos estadísticos en el informe de experimentación](experiment-report-calculations.md)

>[!ENDSHADEBOX]

El Experimento de contenido de Journey Optimizer le permite definir varios tratamientos de entrega para medir cuál ofrece el mejor rendimiento para la audiencia de destino. Puede elegir entre variar el contenido de la entrega, el asunto o el remitente. La audiencia de interés se asigna aleatoriamente a cada tratamiento para determinar cuál funciona mejor en términos de la métrica especificada.

>[!NOTE]
>
>Antes de empezar con Experimento de contenido, asegúrese de que la configuración de la creación de informes está establecida para sus conjuntos de datos personalizados. Obtenga más información en [esta sección](reporting-configuration.md).

En el siguiente ejemplo, el destinatario del envío se ha dividido en dos grupos, cada uno de los cuales representa el 45 % de la población objetivo, y un grupo de exclusión del 10 %, que no reciben el envío.

Cada persona de la audiencia de destino recibe una versión de un correo electrónico, con una línea de asunto que es una de las dos siguientes:

* uno que promociona directamente una oferta del 10% en la nueva colección y una imagen.
* el otro solo anuncia una oferta especial sin especificar el 10% de descuento sin ninguna imagen.

El objetivo aquí es ver si los destinatarios interactuarán con el correo electrónico según el experimento recibido. Por lo tanto, elegiremos **[!UICONTROL Aperturas de correo electrónico]** como métrica de objetivo principal en este experimento de contenido.

![](assets/content_experiment.png)

## Creación de la campaña {#campaign-experiment}

1. Desde el **[!UICONTROL Campañas]** página, haga clic en **[!UICONTROL Crear campaña]**.

   ![](assets/content_experiment_1.png)

<!--
1. In the **[!UICONTROL Properties]** section, choose your **[!UICONTROL Campaign type]**:

    * **[!UICONTROL Scheduled]**: designed to send marketing messages and can be executed immediately or at a specified date.

    * **[!UICONTROL API-Triggered]**: designed to send transactional messages, such as password reset notifications or cart abandonment reminders. 
    
        To execute an API-triggered campaign, you will need to make an API call. [Learn more](api-triggered-campaigns.md)
-->
1. Seleccione el canal y, a continuación, la **[!UICONTROL Superficie]** que desee utilizar para este envío y haga clic en **[!UICONTROL Crear]**. Para obtener más información, consulte [Superficies de canal](../configuration/channel-surfaces.md) página.

   ![](assets/content_experiment_2.png)

1. Configure las variables **[!UICONTROL Propiedades]** del envío:
   * **[!UICONTROL Nombre]**
   * **[!UICONTROL Descripción]**

1. Defina la audiencia a la que se dirige. Para ello, haga clic en el **[!UICONTROL Seleccionar audiencia]** para mostrar la lista de segmentos de Adobe Experience Platform disponibles. [Más información sobre los segmentos](../segment/about-segments.md)

   En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a los individuos del segmento seleccionado. [Más información](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. En el **[!UICONTROL Seguimiento de acciones]** , especifique si desea rastrear cómo reaccionan los destinatarios a su envío: puede rastrear clics o aperturas.

   Se podrá acceder a los resultados de seguimiento desde el informe de campaña una vez que se haya ejecutado la campaña.

1. Para ejecutar la campaña en una fecha específica o en una frecuencia recurrente, configure el **[!UICONTROL Programación]** sección. [Más información](create-campaign.md)

1. Clic **[!UICONTROL Editar contenido]** para comenzar a personalizar la entrega. [Más información](../email/content-from-scratch.md)

   ![](assets/content_experiment_17.png)

1. Desde el **[!UICONTROL Editar contenido]** , empiece a personalizar el tratamiento A.

   Para este tratamiento, especificaremos la oferta especial directamente en la línea de asunto y añadiremos la personalización.

   ![](assets/content_experiment_5.png)

## Configuración del experimento de contenido {#configure-experiment}

1. Cuando la entrega se haya personalizado, en la página de resumen de Campaign, haga clic en **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido.

   ![](assets/content_experiment_3.png)

1. Seleccione el **[!UICONTROL Métrica de éxito]** que desea configurar para el experimento.

   Para nuestro experimento, seleccionamos **[!UICONTROL Correo electrónico abierto]** para probar si los destinatarios abrirán sus correos electrónicos si el código de promoción está en la línea de asunto.

   ![](assets/content_experiment_11.png)

1. Clic **[!UICONTROL Agregar tratamiento]** para crear tantos tratamientos nuevos como sea necesario.

   ![](assets/content_experiment_8.png)

1. Cambie el **[!UICONTROL Título]** de su tratamiento para diferenciarlos mejor.

1. Elija añadir una **[!UICONTROL Holdout]** para su envío. Este grupo no recibirá ningún contenido de esta campaña.

   Al activar la barra de alternancia, se tomará automáticamente el 10% de su población, puede ajustar este porcentaje si es necesario.

   ![](assets/content_experiment_12.png)

1. A continuación, puede elegir asignar un porcentaje preciso a cada uno **[!UICONTROL Tratamiento]** o simplemente encienda la **[!UICONTROL Distribuir uniformemente]** barra de alternancia.

   ![](assets/content_experiment_13.png)

1. Clic **[!UICONTROL Crear]** cuando se establezca la configuración.

## Diseña tus tratamientos {#treatment-experiment}

1. Desde el **[!UICONTROL Editar contenido]** , seleccione el tratamiento B para cambiar el contenido.

   Aquí, elegimos no especificar la oferta en la **[!UICONTROL Línea de asunto]**.

   ![](assets/content_experiment_18.png)

1. Clic **[!UICONTROL Editar cuerpo del correo electrónico]** para personalizar aún más su tratamiento B.

   ![](assets/content_experiment_9.png)

1. Después de diseñar los tratamientos, haga clic en **[!UICONTROL Más acciones]** para acceder a las opciones relacionadas con sus tratamientos: **[!UICONTROL Cambiar nombre]**, **[!UICONTROL Duplicar]** y **[!UICONTROL Eliminar]**.

   ![](assets/content_experiment_7.png)

1. Si es necesario, acceda al **[!UICONTROL Configuración del experimento]** menú para cambiar la configuración de los tratamientos.

   ![](assets/content_experiment_19.png)

1. Una vez definido el contenido del mensaje, haga clic en **[!UICONTROL Simular contenido]** para controlar la renderización del envío y comprobar la configuración de personalización con perfiles de prueba. [Más información](../email/preview.md)

1. Cuando el experimento de contenido esté listo, puede hacer clic en en la página de resumen de Campaign **[!UICONTROL Revisar para activar]** para mostrar un resumen de la campaña. Las alertas se muestran si algún parámetro es incorrecto o falta.

   ![](assets/content_experiment_15.png)

1. Compruebe que la campaña esté configurada correctamente y haga clic en **[!UICONTROL Activar]** para iniciarlo.

   ![](assets/content_experiment_14.png)

Después de configurar la experimentación y la campaña, puede realizar un seguimiento del éxito de su envío con el informe de Campaign.

## Informe Objetivos {#objectives-global}

>[!AVAILABILITY]
>
>Actualmente, la función Experimento de contenido solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

![](assets/performance_report.gif)

El **[!UICONTROL Objetivos]** de su informe de Campaign le permite ajustar mejor los informes de las entregas dirigiéndose a una métrica específica.

El **[!UICONTROL Objetivos]** los elementos enumerados están vinculados a **[!UICONTROL Conjuntos de datos]** que definen una conexión a un sistema para recuperar información adicional. Una lista de componentes integrados **[!UICONTROL Objetivos]** está disponible, pero puede agregar los suyos propios agregando nuevos **[!UICONTROL Conjunto de datos]**. Para ver el procedimiento detallado, consulte [sección](reporting-configuration.md).

Después de seleccionar los Objetivos en los que desea centrarse, se muestran los dos **[!UICONTROL Resumen de rendimiento]** y **[!UICONTROL Objetivo de campaña]** los widgets proporcionan un resumen detallado del rendimiento de su envío.

Con el **[!UICONTROL Objetivo de campaña]** , también puede optar por comparar su objetivo principal con otra métrica.

Tenga en cuenta que se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](../reports/global-report.md#modify-dashboard).

## Informe de experimentación {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Métrica de éxito"
>abstract="El valor total de la métrica de éxito, previamente seleccionada al crear los experimentos, dividido por el número de perfiles."

>[!AVAILABILITY]
>
>Actualmente, la función Experimento de contenido solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

![](assets/experimentation_report_3.png)

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL Experimentación]** La pestaña detalla la información principal relativa al rendimiento de cada variante y si hay un mejor rendimiento.

Tenga en cuenta que la definición del mejor ejecutante puede llevar algún tiempo y se representará mediante este icono ![](assets/experimentation_report_1.png).

El **[!UICONTROL Resultado del experimento]** widget detalla el rendimiento de cada variante. Puede cambiar la línea de base seleccionando uno de los tratamientos en la **[!UICONTROL Línea base]** la lista desplegable. El mejor tratamiento se representará con un icono de estrella.

La tabla presenta las siguientes métricas:

* **[!UICONTROL Perfiles]**: Número de perfiles objetivo para este tratamiento.

* **[!UICONTROL Clics salientes únicos]**: Recuento total de clics en los canales salientes.

* **[!UICONTROL Recuento por perfil]**: Valor total de la métrica del objetivo Experimento dividido por el número de perfiles.

* **[!UICONTROL Intervalo de confianza]**: Diferencia porcentual de rendimiento entre el punto de referencia y el tratamiento con mejor rendimiento. [Más información](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Alza media]**: Mejora porcentual de la tasa de conversión de un tratamiento determinado respecto al valor basal. [Más información](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Confianza]**: Evidencia de que un tratamiento dado es el mismo que el tratamiento basal. [Más información](../campaigns/experiment-calculations.md#understand-confidence)

Para profundizar en estos resultados y en cómo interpretarlos, consulte [esta página](../campaigns/get-started-experiment.md#interpret-results).
