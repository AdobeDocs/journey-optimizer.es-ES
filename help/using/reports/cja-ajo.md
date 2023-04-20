---
solution: Journey Optimizer
product: journey optimizer
title: Uso de Customer Journey Analytics
description: Introducción a Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 0e45d6e4995f4f21dc5122203b715ae999e2b760
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 11%

---

# Uso de [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] integración con [!DNL Customer Journey Analytics] proporciona una vista holística de todos sus recorridos con distribución automatizada de informes y visualizaciones personalizadas de los datos.

![](assets/cja.png)

Después de crear el recorrido en [!DNL Journey Optimizer], puede importar los datos de cliente a [!DNL Customer Journey Analytics] para iniciar informes y comprender el impacto de cada interacción que un cliente tiene con sus recorridos.

➡️ [Customer Journey Analytics de Discover](https://docs.adobe.com/content/help/es-ES/experience-cloud/user-guides/home.translate.html){target="_blank"}

>[!NOTE]
>
>Además de esta integración, también puede exportar el contenido de los conjuntos de datos de Adobe Journey Optimizer a ubicaciones de almacenamiento en la nube y utilizar esta información para realizar informes o análisis. [Obtenga información sobre cómo exportar conjuntos de datos a ubicaciones de almacenamiento en la nube](../data/export-datasets.md)
>
>Tenga en cuenta que la función de exportación de conjuntos de datos está actualmente en fase beta y disponible para todos los usuarios de Adobe Journey Optimizer. Póngase en contacto con su representante de Adobe para obtener acceso a los destinos si todavía no tiene acceso.

Antes de usar [!DNL Customer Journey Analytics] para sus recorridos, primero debe configurar esta integración:

1. [Crear una conexión](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=es) en [!DNL Customer Journey Analytics] con la variable **[!UICONTROL Conjunto de datos]** desea enviar a Adobe Experience Platform.

   Lo siguiente [!DNL Journey Optimizer] se puede configurar:
   * [Evento de paso de recorrido](../data/datasets-query-examples.md#journey-step-event): permite ver quién entra en los recorridos y hasta dónde llegan.
   * [Comentarios del mensaje/Seguimiento de conjuntos de datos](../data/datasets-query-examples.md#message-feedback-event-dataset): permite ver información de envío sobre los mensajes enviados [!DNL Journey Optimizer].
   * [Conjuntos de datos de entidades y Recorridos](../data/datasets-query-examples.md#entity-dataset): permite buscar nombres descriptivos y utilizarlos en los informes.

1. [Creación de una vista de datos](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=es) para configurar las dimensiones y métricas que desee usar en el informe.

   Puede crear métricas específicas de Journey Optimizer para reflejar mejor los datos de sus recorridos. [Más información](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

Uso [!DNL Journey Optimizer] con [!DNL Customer Journey Analytics] puede provocar algunas discrepancias en los datos de los informes debido a:

* **Ambas [!DNL Journey Optimizer] y [!DNL Customer Journey Analytics] sincronice datos de Azure Data Lake Storage (ADLS) para crear informes.**

   El tiempo de procesamiento de los datos entrantes puede ser ligeramente diferente entre los productos. Debido a esto, es posible que los datos no coincidan al mostrar informes desde una fecha determinada hasta el día actual. Para reducir las discrepancias, utilice intervalos de fechas que excluyan el día actual.

* **En [!DNL Journey Optimizer] informes, la métrica Enviado también incluye la métrica Reintento.**

   **[!UICONTROL Reintentos]** no se incluirá en **[!UICONTROL Enviado]** métrica en [!DNL Customer Journey Analytics]. Esto causará que [!DNL Customer Journey Analytics] **[!UICONTROL Enviado]** métricas que muestran valores inferiores a [!DNL Journey Optimizer]. Sin embargo, los datos de reintentos se convierten en **[!UICONTROL Mensajes enviados correctamente]** o **[!UICONTROL Devoluciones]** métrica.
Para reducir las discrepancias, utilice intervalos de fechas desde hace una semana o incluso después.

* **Los informes se proporcionan desde una fuente de datos diferente.**

   Esto podría provocar entre un 1 y un 2 % de discrepancias de datos entre productos.
