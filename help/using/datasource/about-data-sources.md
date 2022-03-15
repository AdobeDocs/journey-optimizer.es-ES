---
title: Acerca de las fuentes de datos
description: Obtenga información sobre cómo configurar una fuente de datos
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: d9f7c64358be3c3355337ba0db12e5b8c17bba4c
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 74%

---

# Acerca de las fuentes de datos {#about-data-sources}

>[!CONTEXTUALHELP]
>id="jo_datasources"
>title="Acerca de las fuentes de datos"
>abstract="La configuración de la fuente de datos siempre la realiza un usuario técnico. La configuración de la fuente de datos permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos para definición de condición, parámetro y datos de personalización en acciones, definición de espera personalizada, definición de zona horaria personalizada."

La configuración de la fuente de datos permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos, para:

* [definición de condición](../building-journeys/condition-activity.md)
* datos de parámetros y personalización en [acciones](../action/action.md)
* [definición de espera personalizada](../building-journeys/wait-activity.md#custom)
* [definición de zona horaria](../building-journeys/timezone-management.md)

➡️ [Descubra esta función en vídeo](#video)

Esta configuración no es necesaria si los recorridos solo aprovechan los datos locales procedentes de una carga útil de evento. Por ejemplo, si el recorrido está compuesto por un evento seguido de una actividad de mensaje que solo utiliza datos del evento, no es necesario configurar una fuente de datos.

Existen dos tipos de fuentes de datos:

* Fuente de datos preconfigurada de Adobe Experience Platform que define la conexión al servicio perfil de cliente en tiempo real. Constituye una fuente de datos integrada. Consulte [esta página](../datasource/adobe-experience-platform-data-source.md).
* Las fuentes de datos externas que permiten definir una conexión con sistemas externos. Estos son los que puede crear. Consulte [esta página](../datasource/external-data-sources.md).

Para cada fuente de datos, se define la información que se recuperará mediante grupos de campos. Los grupos de campos son conjuntos de campos que se pueden recuperar desde una fuente de datos. Consulte [esta página](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Ahora se admiten relaciones de esquema para orígenes de datos.

Para obtener más información sobre cómo configurar una fuente de datos de Adobe Experience Platform y una fuente de datos externa, y cómo buscar y utilizar datos en un recorrido, consulte esta [videotutorial](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/configure-data-sources.html){target=&quot;_blank&quot;}.

## Vídeo explicativo {#video}

Comprenda qué es una fuente de datos y aprenda a configurar fuentes de datos de Experience Platform y externas.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

