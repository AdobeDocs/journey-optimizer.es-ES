---
solution: Journey Optimizer
product: journey optimizer
title: Acerca de las fuentes de datos
description: Obtenga información sobre cómo configurar una fuente de datos
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: datos, fuente, recorrido, plataforma
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 0738443c024499079d8527fe2cc1c80f42f4f476
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 66%

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

Esta configuración no es necesaria si los recorridos solo aprovechan los datos locales procedentes de una carga útil de evento. Por ejemplo, si el recorrido está compuesto por un evento seguido de una actividad de acción del canal que solo utiliza datos del evento, no es necesario configurar ninguna fuente de datos.

Existen dos tipos de fuentes de datos:

* Fuente de datos preconfigurada de Adobe Experience Platform que define la conexión al servicio perfil de cliente en tiempo real. Constituye una fuente de datos integrada. Consulte [esta página](../datasource/adobe-experience-platform-data-source.md).
* Las fuentes de datos externas que permiten definir una conexión con sistemas externos. Estos son los que puede crear. Consulte [esta página](../datasource/external-data-sources.md).

>[!NOTE]
>
>Como las respuestas ahora son compatibles, debe utilizar acciones personalizadas en lugar de fuentes de datos para casos de uso de fuentes de datos externas. Para obtener más información sobre las respuestas, consulte [sección](../action/action-response.md)

Para cada fuente de datos, se define la información que se recuperará mediante grupos de campos. Los grupos de campos son conjuntos de campos que se pueden recuperar desde una fuente de datos. Consulte [esta página](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Las relaciones de esquema no son compatibles con las fuentes de datos.

Para obtener más información sobre cómo configurar una fuente de datos de Adobe Experience Platform y una fuente de datos externa, y cómo buscar y utilizar datos en un recorrido, consulte esta sección [tutorial en vídeo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target="_blank"}.

## Vídeo explicativo {#video}

Comprenda qué es una fuente de datos y aprenda a configurar fuentes de datos de Experience Platform y externas.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

