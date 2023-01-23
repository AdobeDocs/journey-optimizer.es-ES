---
solution: Journey Optimizer
product: journey optimizer
title: Acerca de las fuentes de datos
description: Obtenga información sobre cómo configurar una fuente de datos
feature: Data Sources
topic: Administration
role: Admin, Developer
level: Intermediate
keywords: datos, origen, recorrido, plataforma
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 83%

---

# Acerca de las fuentes de datos {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Acerca de las fuentes de datos"
>abstract="La configuración de la fuente de datos siempre la realiza un usuario técnico. La configuración de la fuente de datos permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos para definición de condición, parámetro y datos de personalización en acciones, definición de espera personalizada, definición de zona horaria personalizada."

La configuración de la fuente de datos permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos, para:

* [definición de condición](../building-journeys/condition-activity.md)
* datos de parámetros y personalización en [acciones](../action/action.md)
* [definición de espera personalizada](../building-journeys/wait-activity.md#custom)
* [definición de zona horaria](../building-journeys/timezone-management.md)

➡️ [Descubra esta función en vídeo](#video)

Esta configuración no es necesaria si los recorridos solo aprovechan los datos locales procedentes de una carga útil de evento. Por ejemplo, si el recorrido está compuesto por un evento seguido de una actividad de acción de canal que solo utiliza datos del evento, no es necesario configurar una fuente de datos.

Existen dos tipos de fuentes de datos:

* Fuente de datos preconfigurada de Adobe Experience Platform que define la conexión al servicio perfil de cliente en tiempo real. Constituye una fuente de datos integrada. Consulte [esta página](../datasource/adobe-experience-platform-data-source.md).
* Las fuentes de datos externas que permiten definir una conexión con sistemas externos. Estos son los que puede crear. Consulte [esta página](../datasource/external-data-sources.md).

Para cada fuente de datos, se define la información que se recuperará mediante grupos de campos. Los grupos de campos son conjuntos de campos que se pueden recuperar desde una fuente de datos. Consulte [esta página](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Las relaciones de esquema no son compatibles con los orígenes de datos.

Para obtener más información sobre cómo configurar una fuente de datos de Adobe Experience Platform y una fuente de datos externa, y cómo buscar y usar los datos en un recorrido, vea este [vídeo tutorial](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target="_blank"}.

## Vídeo explicativo {#video}

Comprenda qué es una fuente de datos y aprenda a configurar fuentes de datos de Experience Platform y externas.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

