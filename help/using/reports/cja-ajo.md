---
solution: Journey Optimizer
product: journey optimizer
title: Uso de Customer Journey Analytics
description: Introducción a Customer Journey Analytics
feature: Reporting, Integrations
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: c2f2dde40385f56ea86be15a5857fa9e5e2e2fed
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 11%

---

# Uso de [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] integración con [!DNL Customer Journey Analytics] proporciona una vista integral de todos sus recorridos con una distribución automatizada de informes y visualizaciones personalizadas de los datos.

![](assets/cja.png)

Después de crear el recorrido en [!DNL Journey Optimizer], puede importar los datos de clientes a [!DNL Customer Journey Analytics] para iniciar informes y comprender el impacto de cada interacción que un cliente tiene con sus recorridos.

➡️ [Customer Journey Analytics de Discover](https://docs.adobe.com/content/help/es-ES/experience-cloud/user-guides/home.translate.html){target="_blank"}

>[!NOTE]
>
>Además de esta integración, también puede exportar el contenido de los conjuntos de datos de Adobe Journey Optimizer a ubicaciones de almacenamiento en la nube y utilizar esta información con fines de informes o análisis. [Obtenga información sobre cómo exportar conjuntos de datos a ubicaciones de almacenamiento en la nube](../data/export-datasets.md)
>
>Tenga en cuenta que la función de exportación de conjuntos de datos se encuentra actualmente en fase beta y está disponible para todos los usuarios de Adobe Journey Optimizer. Póngase en contacto con su representante de Adobe para obtener acceso a los destinos si todavía no tiene acceso.

Antes de usar [!DNL Customer Journey Analytics] para los recorridos, primero debe configurar esta integración:

1. [Crear una conexión](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=es) in [!DNL Customer Journey Analytics] con el **[!UICONTROL Conjunto de datos]** desea enviar a Adobe Experience Platform.

   Lo siguiente [!DNL Journey Optimizer] se puede configurar:
   * [Evento de paso de recorrido](../data/datasets-query-examples.md#journey-step-event): le permite ver quién entra en los recorridos y hasta dónde llegan.
   * [Conjuntos de datos de seguimiento/comentarios de mensajes](../data/datasets-query-examples.md#message-feedback-event-dataset): le permite ver la información de envío de sus mensajes enviados a través de [!DNL Journey Optimizer].
   * [Conjuntos de datos de entidad y Recorrido](../data/datasets-query-examples.md#entity-dataset): le permite buscar nombres descriptivos y utilizarlos en los informes.

1. [Creación de una vista de datos](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=es) para configurar las dimensiones y métricas que desee utilizar para el informe.

   Puede crear métricas específicas de Journey Optimizer para reflejar mejor los datos de sus recorridos. [Más información](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

Uso de [!DNL Journey Optimizer] con [!DNL Customer Journey Analytics] podría provocar algunas discrepancias en los datos de los informes causadas por:

* **Ambos [!DNL Journey Optimizer] y [!DNL Customer Journey Analytics] sincronizar datos de Azure Data Lake Storage (ADLS) para la creación de informes.**

  El tiempo de procesamiento de los datos entrantes puede ser ligeramente diferente entre los productos. Debido a esto, es posible que los datos no coincidan al mostrar los informes de una fecha determinada al día actual. Para reducir las discrepancias, utilice intervalos de fechas que excluyan el día actual.

* **Entrada [!DNL Journey Optimizer] Informes, la métrica Enviada también incluye la métrica Reintento.**

  **[!UICONTROL Reintentos]** no se incluirá en **[!UICONTROL Enviado]** Métrica en [!DNL Customer Journey Analytics]. Esto provocará [!DNL Customer Journey Analytics] **[!UICONTROL Enviado]** métricas para mostrar valores inferiores a [!DNL Journey Optimizer]. Sin embargo, los datos de reintentos convergen en la variable **[!UICONTROL Mensajes enviados correctamente]** o **[!UICONTROL Devoluciones]** métrica.
Para reducir las discrepancias, utilice intervalos de fechas de hace una semana o incluso más tarde.

* **Los informes se proporcionan desde una fuente de datos diferente.**

  Esto podría provocar discrepancias de datos de entre el 1 y el 2 % entre los productos.
