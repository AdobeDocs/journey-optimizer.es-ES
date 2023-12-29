---
solution: Journey Optimizer
product: journey optimizer
title: Crear un experimento de contenido
description: Aprenda a crear un experimento de contenido en sus campañas
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: contenido, experimento, múltiple, audiencia, tratamiento
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 12%

---

# Creación de un experimento de contenido {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="Experimento de contenido"
>abstract="Puede elegir entre modificar el contenido del mensaje, el asunto o el remitente para definir varios tratamientos y determinar la mejor combinación para sus públicos."

>[!NOTE]
>
>Antes de empezar con Experimento de contenido, asegúrese de que la configuración de la creación de informes está establecida para sus conjuntos de datos personalizados. Obtenga más información en [esta sección](reporting-configuration.md).

El Experimento de contenido de Journey Optimizer le permite definir varios tratamientos de entrega para medir cuál ofrece el mejor rendimiento para la audiencia de destino. Puede elegir entre variar el contenido de la entrega, el asunto o el remitente. La audiencia de interés se asigna aleatoriamente a cada tratamiento para determinar cuál funciona mejor en términos de la métrica especificada.

![](../rn/assets/do-not-localize/experiment.gif)


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

   En este ejemplo, elegimos enviar una campaña por correo electrónico.

   ![](assets/content_experiment_2.png)

1. Configure las variables **[!UICONTROL Propiedades]** del envío:
   * **[!UICONTROL Nombre]**
   * **[!UICONTROL Descripción]**

1. Defina la audiencia a la que se dirige. Para ello, haga clic en el **[!UICONTROL Seleccionar audiencia]** para mostrar la lista de audiencias de Adobe Experience Platform disponibles. [Más información sobre los públicos](../audience/about-audiences.md)

   En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a los individuos de la audiencia seleccionada. [Más información](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. En el **[!UICONTROL Seguimiento de acciones]** , especifique si desea rastrear cómo reaccionan los destinatarios a su envío: puede rastrear clics o aperturas.

   Se podrá acceder a los resultados de seguimiento desde el informe de campaña una vez que se haya ejecutado la campaña.

1. Para ejecutar la campaña en una fecha específica o en una frecuencia recurrente, configure el **[!UICONTROL Programación]** sección. [Más información](create-campaign.md)

1. Clic **[!UICONTROL Editar contenido]** para comenzar a personalizar la entrega.

   ![](assets/content_experiment_17.png)

1. Desde el **[!UICONTROL Editar contenido]** , empiece a personalizar el tratamiento A.

   Para este tratamiento, especificaremos la oferta especial directamente en la línea de asunto y añadiremos la personalización.

   ![](assets/content_experiment_5.png)

## Configuración del experimento de contenido {#configure-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_dimension"
>title="Dimensión"
>abstract="Elija la dimensión específica que desea rastrear para el experimento, como clics específicos o vistas de páginas específicas."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_success_metric"
>title="Métrica de éxito"
>abstract="La métrica de éxito se utiliza para rastrear y evaluar el tratamiento con mejor rendimiento de un experimento. Asegúrese de configurar su conjunto de datos para determinadas métricas antes de utilizarlo."

1. Cuando el mensaje esté personalizado, en la página de resumen de la campaña, haga clic en **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido.

   ![](assets/content_experiment_3.png)

1. Seleccione el **[!UICONTROL Métrica de éxito]** que desea configurar para el experimento.

   Para este ejemplo, seleccione **[!UICONTROL Correo electrónico abierto]** para probar si los perfiles abren sus correos electrónicos si el código de promoción está en la línea de asunto.

   ![](assets/content_experiment_11.png)

1. Al configurar un experimento con el canal en la aplicación o web y elegir la variable **[!UICONTROL Clics entrantes]**, **[!UICONTROL Clics entrantes únicos]** , **[!UICONTROL Vistas de página]** , o **[!UICONTROL Métricas de vistas de página únicas]** , el **[!UICONTROL Acción de clic]**  Esta lista desplegable le permite rastrear y monitorizar con precisión los clics y las vistas en páginas específicas.

   ![](assets/content_experiment_20.png)

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

1. Una vez definido el contenido del mensaje, haga clic en **[!UICONTROL Simular contenido]** para controlar la renderización del envío y comprobar la configuración de personalización con perfiles de prueba. [Más información](../content-management/preview-test.md)

1. Cuando el experimento de contenido esté listo, puede hacer clic en en la página de resumen de Campaign **[!UICONTROL Revisar para activar]** para mostrar un resumen de la campaña. Las alertas se muestran si algún parámetro es incorrecto o falta.

   ![](assets/content_experiment_15.png)

1. Compruebe que la campaña esté configurada correctamente y haga clic en **[!UICONTROL Activar]** para iniciarlo.

   ![](assets/content_experiment_14.png)

Después de configurar la experimentación y la campaña, puede realizar un seguimiento del éxito de su envío con el informe de Campaign. [Más información](../reports/campaign-global-report.md#experimentation-report)
