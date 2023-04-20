---
solution: Journey Optimizer
product: journey optimizer
title: Crear un experimento de contenido
description: Aprenda a crear un experimento de contenido en sus campañas
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: contenido, experimento, varios, audiencia, tratamiento
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
badge: label="Beta" type="Informative"
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 9%

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

El experimento de contenido de Journey Optimizer le permite definir varios tratamientos de envío para medir cuál ofrece el mejor rendimiento para la audiencia objetivo. Puede elegir entre variar el contenido de la entrega, el asunto o el remitente. La audiencia de interés se asigna aleatoriamente a cada tratamiento para determinar cuál funciona mejor en términos de la métrica especificada.

>[!NOTE]
>
>Antes de empezar con el experimento de contenido, asegúrese de que la configuración de informes esté configurada para sus conjuntos de datos personalizados. Obtenga más información en [esta sección](reporting-configuration.md).

En el siguiente ejemplo, el objetivo de la entrega se ha dividido en dos grupos, cada uno de los cuales representa el 45 % de la población de destino, y un grupo de exclusión del 10 %, que no recibe la entrega.

Cada persona de la audiencia de destino recibirá una versión de un correo electrónico, con una línea de asunto que es una de las dos siguientes:

* una que promociona directamente una oferta del 10 % sobre la nueva colección y una imagen.
* el otro solo anuncia una oferta especial sin especificar el 10 % de descuento sin ninguna imagen.

El objetivo aquí es ver si los destinatarios interactuarán con el correo electrónico según el experimento recibido. Por lo tanto, elegiremos **[!UICONTROL Aperturas de correo electrónico]** como métrica objetivo principal en este experimento de contenido.

![](assets/content_experiment.png)

## Cree la campaña {#campaign-experiment}

1. En el **[!UICONTROL Campañas]** página, haga clic en **[!UICONTROL Crear campaña]**.

   ![](assets/content_experiment_1.png)

<!--
1. In the **[!UICONTROL Properties]** section, choose your **[!UICONTROL Campaign type]**:

    * **[!UICONTROL Scheduled]**: designed to send marketing messages and can be executed immediately or at a specified date.

    * **[!UICONTROL API-Triggered]**: designed to send transactional messages, such as password reset notifications or cart abandonment reminders. 
    
        To execute an API-triggered campaign, you will need to make an API call. [Learn more](api-triggered-campaigns.md)
-->
1. Seleccione el canal y, a continuación, el **[!UICONTROL Superficie]** desea utilizar para este envío y haga clic en **[!UICONTROL Crear]**. Para obtener más información, consulte [Superficies de canal](../configuration/channel-surfaces.md) página.

   ![](assets/content_experiment_2.png)

1. Configure el **[!UICONTROL Propiedades]** del envío:
   * **[!UICONTROL Nombre]**
   * **[!UICONTROL Descripción]**

1. Defina la audiencia objetivo. Para ello, haga clic en el botón **[!UICONTROL Seleccionar la audiencia]** para mostrar la lista de segmentos de Adobe Experience Platform disponibles. [Más información sobre los segmentos](../segment/about-segments.md)

   En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado. [Más información](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. En el **[!UICONTROL Seguimiento de acciones]** , especifique si desea rastrear cómo reaccionan los destinatarios a su envío: puede rastrear clics o aperturas.

   Una vez ejecutada la campaña, se podrá acceder a los resultados de seguimiento desde el informe de campaña.

1. Para ejecutar la campaña en una fecha específica o con una frecuencia recurrente, configure la variable **[!UICONTROL Programación]** para obtener más información. [Más información](create-campaign.md)

1. Haga clic en **[!UICONTROL Editar contenido]** para comenzar a personalizar el envío. [Más información](../email/content-from-scratch.md)

   ![](assets/content_experiment_17.png)

1. En el **[!UICONTROL Editar contenido]** , empiece a personalizar el tratamiento A.

   Para este tratamiento, especificaremos la oferta especial directamente en la línea de asunto y añadiremos la personalización.

   ![](assets/content_experiment_5.png)

## Configurar el experimento de contenido {#configure-experiment}

1. Cuando la entrega se haya personalizado, en la página de resumen de Campaign, haga clic en **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido.

   ![](assets/content_experiment_3.png)

1. Seleccione el **[!UICONTROL Métrica de éxito]** desea configurar para el experimento.

   Para nuestro experimento, seleccionamos **[!UICONTROL Apertura de correo electrónico]** para comprobar si los destinatarios abrirán sus correos electrónicos si el código de promoción está en la línea de asunto.

   ![](assets/content_experiment_11.png)

1. Haga clic en **[!UICONTROL Agregar tratamiento]** para crear tantos tratamientos nuevos como sea necesario.

   ![](assets/content_experiment_8.png)

1. Cambie el **[!UICONTROL Título]** de su tratamiento para diferenciarlos mejor.

1. Elija agregar una **[!UICONTROL Holdout]** a su envío. Este grupo no recibirá ningún contenido de esta campaña.

   Si activa la barra de alternancia, se tomará automáticamente el 10 % de la población; puede ajustar este porcentaje si es necesario.

   ![](assets/content_experiment_12.png)

1. A continuación, puede elegir asignar un porcentaje preciso a cada **[!UICONTROL Tratamiento]** o simplemente encienda el **[!UICONTROL Distribuir uniformemente]** barra de herramientas.

   ![](assets/content_experiment_13.png)

1. Haga clic en **[!UICONTROL Crear]** cuando la configuración esté configurada.

## Diseño de tratamientos {#treatment-experiment}

1. En el **[!UICONTROL Editar contenido]** seleccione el tratamiento B para cambiar el contenido.

   Aquí, elegimos no especificar la oferta en la **[!UICONTROL Línea de asunto]**.

   ![](assets/content_experiment_18.png)

1. Haga clic en **[!UICONTROL Editar cuerpo del correo electrónico]** para personalizar aún más su tratamiento B.

   ![](assets/content_experiment_9.png)

1. Después de diseñar los tratamientos, haga clic en **[!UICONTROL Más acciones]** para acceder a las opciones relacionadas con sus tratamientos: **[!UICONTROL Cambiar nombre]**, **[!UICONTROL Duplicar]** y **[!UICONTROL Eliminar]**.

   ![](assets/content_experiment_7.png)

1. Si es necesario, acceda al **[!UICONTROL Configuración del experimento]** para cambiar la configuración de los tratamientos.

   ![](assets/content_experiment_19.png)

1. Una vez definido el contenido del mensaje, haga clic en el botón **[!UICONTROL Simular contenido]** para controlar la renderización de la entrega y comprobar la configuración de personalización con perfiles de prueba. [Más información](../email/preview.md)

1. Cuando el experimento de contenido esté listo, desde la página de resumen de Campaign, puede hacer clic en **[!UICONTROL Revisar para activar]** para mostrar un resumen de la campaña. Las alertas se muestran si algún parámetro es incorrecto o falta.

   ![](assets/content_experiment_15.png)

1. Compruebe que la campaña esté correctamente configurada y haga clic en **[!UICONTROL Activar]** para iniciarlo.

   ![](assets/content_experiment_14.png)

Después de configurar la experimentación y la campaña, puede seguir el éxito de la entrega con el informe de campaña.

## Informe Objetivos {#objectives-global}

>[!AVAILABILITY]
>
>Actualmente, la función de experimento de contenido solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

![](assets/performance_report.gif)

La variable **[!UICONTROL Objetivos]** del informe de Campaign le permite ajustar mejor los informes de las entregas mediante la segmentación de una métrica específica.

La variable **[!UICONTROL Objetivos]** están vinculados a **[!UICONTROL Conjuntos de datos]** que definen una conexión con un sistema para recuperar información adicional. Una lista de elementos integrados **[!UICONTROL Objetivos]** está disponible, pero puede agregar el suyo propio añadiendo **[!UICONTROL Conjunto de datos]**. Para ver el procedimiento detallado, consulte esta [sección](reporting-configuration.md).

Después de seleccionar los objetivos sobre los que desea establecer el objetivo, los dos **[!UICONTROL Información general sobre el rendimiento]** y **[!UICONTROL Objetivo de la campaña]** Las utilidades proporcionan un resumen detallado del rendimiento de su envío.

Con la variable **[!UICONTROL Objetivo de la campaña]** , también puede elegir comparar su objetivo principal con otra métrica.

Tenga en cuenta que cada utilidad se puede cambiar de tamaño y eliminar si es necesario. Para obtener más información, consulte [sección](../reports/global-report.md#modify-dashboard).

## Informe de experimentación {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Métrica de éxito"
>abstract="El valor total de la métrica de éxito, previamente seleccionada al crear los experimentos, dividido por el número de perfiles."

>[!AVAILABILITY]
>
>Actualmente, la función de experimento de contenido solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

![](assets/experimentation_report_3.png)

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL Experimento]** La pestaña detalla la información principal en relación con el rendimiento de cada variante y si hay un mejor rendimiento.

Tenga en cuenta que la definición del mejor ejecutante puede tardar algún tiempo, y que se representará con este icono ![](assets/experimentation_report_1.png).

La variable **[!UICONTROL Resultado del experimento]** widget detalla el rendimiento de cada variante. Puede cambiar su línea base seleccionando uno de los tratamientos de la **[!UICONTROL Línea de base]** la lista desplegable . El mejor tratamiento se representará con un icono de estrella.

La tabla presenta las siguientes métricas:

* **[!UICONTROL Perfiles]**: Número de perfiles objetivo para este tratamiento.

* **[!UICONTROL Clics salientes únicos]**: Recuento total de clics en los canales salientes.

* **[!UICONTROL Recuento por perfil]**: Valor total de la métrica de objetivo Experimento dividido por el número de perfiles.

* **[!UICONTROL Intervalo de confianza]**: Diferencia porcentual en el rendimiento entre el valor basal y el tratamiento de mejor rendimiento. [Más información](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Alza promedio]**: Mejora porcentual en la tasa de conversión de un tratamiento determinado respecto al valor basal. [Más información](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Confianza]**: Evidencia de que un tratamiento determinado es el mismo que el tratamiento basal. [Más información](../campaigns/experiment-calculations.md#understand-confidence)

Para profundizar en estos resultados y cómo interpretarlos, consulte [esta página](../campaigns/get-started-experiment.md#interpret-results).
