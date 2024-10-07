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
source-git-commit: d4dce7b31d898d86c330048e6d0a1587e87a617c
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 13%

---

# Creación de un experimento de contenido {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="Experimento de contenido"
>abstract="Puede elegir entre modificar el contenido del mensaje, el asunto o el remitente para definir varios tratamientos y determinar la mejor combinación para sus públicos."

>[!NOTE]
>
>Antes de empezar con Experimento de contenido, asegúrese de que la configuración de la creación de informes está establecida para sus conjuntos de datos personalizados. Obtenga más información en [esta sección](../reports/reporting-configuration.md).

El Experimento de contenido de Journey Optimizer le permite definir varios tratamientos de entrega para medir cuál ofrece el mejor rendimiento para la audiencia de destino. Puede elegir entre variar el contenido de la entrega, el asunto o el remitente. La audiencia de interés se asigna aleatoriamente a cada tratamiento para determinar cuál funciona mejor en términos de la métrica especificada.

![](../rn/assets/do-not-localize/experiment.gif)

En el siguiente ejemplo, el destinatario del envío se ha dividido en dos grupos, cada uno de los cuales representa el 45 % de la población objetivo, y un grupo de exclusión del 10 %, que no reciben el envío.

Cada persona de la audiencia de destino recibe una versión de un correo electrónico, con una línea de asunto que es una de las dos siguientes:

* uno que promociona directamente una oferta del 10% en la nueva colección y una imagen.
* el otro solo anuncia una oferta especial sin especificar el 10% de descuento sin ninguna imagen.

El objetivo aquí es ver si los destinatarios interactuarán con el correo electrónico según el experimento recibido. Por lo tanto, elegiremos **[!UICONTROL Aperturas de correo electrónico]** como métrica de objetivo principal en este experimento de contenido.

![](assets/content_experiment.png)

## Cree su contenido {#campaign-experiment}

1. Comience creando y configurando su notificación por correo electrónico, SMS o push [campaign](../campaigns/create-campaign.md) o [recorrido](../building-journeys/journeys-message.md) según sus necesidades.

   >[!AVAILABILITY]
   >
   >Actualmente, la experimentación en Recorrido solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

1. Desde la ventana **[!UICONTROL Editar contenido]**, empiece a personalizar el tratamiento A.

   Para este tratamiento, especificaremos la oferta especial directamente en la línea de asunto y añadiremos la personalización.

   ![](assets/content_experiment_5.png)

1. Cree o importe el contenido original y personalícelo según sea necesario.

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

1. Seleccione la **[!UICONTROL métrica de éxito]** que desee establecer para su experimento.

   Para este ejemplo, seleccione **[!UICONTROL Correo electrónico abierto]** para comprobar si los perfiles abren sus mensajes de correo electrónico si el código de la promoción está en la línea de asunto.

   ![](assets/content_experiment_11.png)

1. Al configurar un experimento utilizando el canal en la aplicación o web y elegir las **[!UICONTROL pulsaciones entrantes]**, los **[!UICONTROL clics entrantes únicos]**, las **[!UICONTROL vistas de página]** o las **[!UICONTROL métricas de vistas de página únicas]**, la lista desplegable de **[!UICONTROL acción de clic]** le permite rastrear y supervisar con precisión los clics y las vistas en páginas específicas.

   ![](assets/content_experiment_20.png)

1. Haga clic en **[!UICONTROL Agregar tratamiento]** para crear tantos tratamientos nuevos como sea necesario.

   ![](assets/content_experiment_8.png)

1. Cambie **[!UICONTROL Title]** del tratamiento para diferenciarlo mejor.

1. Elija agregar un grupo **[!UICONTROL Holdout]** a su entrega. Este grupo no recibirá ningún contenido de esta campaña.

   Al activar la barra de alternancia, se tomará automáticamente el 10% de su población, puede ajustar este porcentaje si es necesario.

   >[!IMPORTANT]
   >
   >Cuando se utiliza un grupo de exclusión en una acción para la experimentación de contenido, la asignación de exclusión solo se aplica a esa acción específica. Una vez finalizada la acción, los perfiles del grupo de exclusión seguirán por la ruta del recorrido y podrán recibir mensajes de otras acciones. Por lo tanto, asegúrese de que los mensajes posteriores no dependan de la recepción de un mensaje por un perfil que pueda estar en un grupo de exclusión. Si es así, es posible que tenga que eliminar la asignación de exclusión.

   ![](assets/content_experiment_12.png)

1. Puede elegir asignar un porcentaje preciso a cada **[!UICONTROL Tratamiento]** o simplemente cambiar en la barra de alternancia **[!UICONTROL Distribuir uniformemente]**.

   ![](assets/content_experiment_13.png)

1. Haga clic en **[!UICONTROL Crear]** cuando se establezca la configuración.

## Diseña tus tratamientos {#treatment-experiment}

1. En la ventana **[!UICONTROL Editar contenido]**, seleccione el tratamiento B para cambiar el contenido.

   Aquí, elegimos no especificar la oferta en la **[!UICONTROL línea de asunto]**.

   ![](assets/content_experiment_18.png)

1. Haga clic en **[!UICONTROL Editar cuerpo del correo electrónico]** para personalizar aún más el tratamiento B.

   ![](assets/content_experiment_9.png)

1. Después de diseñar los tratamientos, haga clic en **[!UICONTROL Más acciones]** para obtener acceso a las opciones relacionadas con los tratamientos: **[!UICONTROL Cambiar nombre]**, **[!UICONTROL Duplicar]** y **[!UICONTROL Eliminar]**.

   ![](assets/content_experiment_7.png)

1. Si es necesario, accede al menú **[!UICONTROL Configuración de experimentos]** para cambiar la configuración de los tratamientos.

   ![](assets/content_experiment_19.png)

1. Una vez definido el contenido del mensaje, haga clic en el botón **[!UICONTROL Simular contenido]** para controlar la renderización del envío y comprobar la configuración de personalización con perfiles de prueba. [Más información](../content-management/preview-test.md)

Después de configurar la experimentación, puede realizar un seguimiento del éxito de su envío con el informe. [Más información](../reports/campaign-global-report.md#experimentation-report)
