---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las fuentes de datos
description: Obtenga información sobre cómo empezar a usar fuentes de datos
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: datos, fuente, recorrido, plataforma
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
TQID: https://experienceleague.adobe.com/eG1QcfpHtxpabUt5e7RZiMIpSAJD6Z6bjO-4wtZEUOg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: dd51b532-b93f-4bcf-8dbf-0d007f593aca
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e366af78935405cd5acb15269194875098b20914
workflow-type: tm+mt
source-wordcount: 948
ht-degree: 29%

---

# Introducción a las fuentes de datos {#about-data-sources}

>[!BEGINSHADEBOX]

**En esta página:** Comprenda cuáles son las fuentes de datos y cómo elegir la estrategia de acceso a datos correcta para que pueda incluir datos adicionales en sus recorridos para condiciones, personalización y tiempo.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Acerca de las fuentes de datos"
>abstract="La configuración de la fuente de datos siempre la realiza un usuario técnico. La configuración de la fuente de datos permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos para definición de condición, parámetro y datos de personalización en acciones, definición de espera personalizada, definición de zona horaria personalizada."

>[!TIP]
>¿No tiene experiencia en la administración de datos en Journey Optimizer? Comience con la información general de [Introducción a la administración de datos](../data/gs-data.md) para comprender los esquemas, conjuntos de datos, identidades y cómo fluyen los datos antes de configurar las fuentes de datos.

La configuración de la fuente de datos permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos, para:

* [definición de condición](../building-journeys/conditions.md)
* datos de parámetros y personalización en [acciones](../action/action.md)
* [definición de espera personalizada](../building-journeys/wait-activity.md#custom)
* [definición de zona horaria](../building-journeys/timezone-management.md)

➡️ [Descubra esta funcionalidad en vídeo](#video)

Esta configuración no es necesaria si los recorridos solo aprovechan los datos locales procedentes de una carga útil de evento. Por ejemplo, si el recorrido está compuesto por un evento seguido de una actividad de acción del canal que solo utiliza datos del evento, no es necesario configurar ninguna fuente de datos.

Existen dos tipos de fuentes de datos:

* La fuente de datos de Adobe Experience Platform **preconfigurada** que define la conexión al servicio Perfil del cliente en tiempo real. Constituye una fuente de datos integrada. Consulte [esta página](../datasource/adobe-experience-platform-data-source.md).
* Las fuentes de datos **external** que le permiten definir una conexión con sistemas externos. Estos son los que puede crear. Consulte [esta página](../datasource/external-data-sources.md).

>[!NOTE]
>
>Como las respuestas ahora son compatibles, debe utilizar acciones personalizadas en lugar de fuentes de datos para casos de uso de fuentes de datos externas. Para obtener más información sobre las respuestas, consulte esta [sección](../action/action-response.md)

Para cada fuente de datos, se define la información que se recuperará mediante grupos de campos. Los grupos de campos son conjuntos de campos que se pueden recuperar desde una fuente de datos. Consulte [esta página](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Las relaciones de esquema no son compatibles con las fuentes de datos.

## Elija su estrategia de acceso a datos {#data-access-strategy}

Antes de configurar una fuente de datos, considere qué enfoque se adapta mejor a su caso de uso. Hay tres opciones disponibles, cada una con diferentes compensaciones en términos de persistencia, enriquecimiento de perfiles y reutilización. Para ver un análisis detallado de estas opciones, consulte [Prácticas recomendadas para recorridos avanzados en Journey Optimizer](https://experienceleague.adobe.com/en/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.

**Opción 1: acceder a datos externos mediante acciones personalizadas (sin lago de datos)**

Conéctese directamente a una API externa durante el tiempo de ejecución del recorrido sin mantener los datos en el lago de datos de Experience Platform. El más adecuado cuando:

* Los datos solo son útiles en el contexto del recorrido y no se necesitan en ninguna otra parte.
* Se puede acceder al sistema externo a través de un extremo de API que devuelve los atributos necesarios.

Más información acerca de [acciones personalizadas](../action/action.md) y [respuestas de acciones personalizadas](../action/action-response.md).

>[!TIP]
>
>Esta opción encaja bien si responde **sí** a ambas preguntas:
>* ¿Los datos solo son útiles dentro del contexto de recorrido y no se necesitan en ninguna otra parte? Si los datos también son necesarios para audiencias u otros canales, considere las Opciones 2 o 3.
>* ¿Se puede acceder al sistema externo a través de un extremo de API que devuelve los atributos necesarios? Si no es así, primero deberá ingerir los datos en el lago de datos.

**Opción 2: conjunto de datos en el lago de datos, no habilitado para el perfil**

Ingeste datos en un conjunto de datos para almacenar en déclencheur y personalizar recorridos basados en datos de evento contextuales, sin contribuir al Perfil del cliente en tiempo real. El más adecuado cuando:

* Los registros contienen un campo de identidad que puede utilizarse para acceder a los perfiles ya almacenados en Experience Platform.
* Los datos no son necesarios para la creación de audiencias o la vinculación de identidad fuera de Journey Optimizer.

>[!TIP]
>
>Esta opción encaja bien si responde **sí** a ambas preguntas:
>* ¿Los registros contienen un campo de identidad que se puede utilizar para acceder a los perfiles ya almacenados en Experience Platform? Si no es así, los recorridos no podrán acceder a los perfiles ni enviarlos.
>* ¿NO se necesitan los datos para la creación de [audiencia](../audience/about-audiences.md) o la vinculación de identidad fuera de Journey Optimizer? Si es así, utilice la opción 3 en su lugar.

**Opción 3 — Conjunto de datos habilitado para el perfil en el lago de datos**

Ingresa datos en un [conjunto de datos con perfil habilitado](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} para crear audiencias, enriquecer gráficos de identidad y aprovechar datos en varios recorridos y destinos de RT-CDP. El más adecuado cuando:

* Los datos son útiles para las definiciones de audiencia utilizadas en canales distintos de Journey Optimizer.
* Los datos contienen varias identidades que contribuyen a fragmentos de perfil más completos y vinculados.

>[!CAUTION]
>
>**Antes de habilitar un conjunto de datos para el perfil**, evalúe las áreas siguientes:
>* **Sincronización de datos**: las bases de datos externas deben sincronizarse, con alertas para identificar errores de ingesta.
>* **[Protecciones de perfil](https://experienceleague.adobe.com/es/docs/experience-platform/profile/guardrails){target="_blank"}**: se aplican protecciones específicas de perfil además de las [protecciones generales de ingesta de datos](https://experienceleague.adobe.com/es/docs/experience-platform/ingestion/guardrails){target="_blank"} para Experience Platform.
>* **Integridad de identidad**: los datos de identidad de sus sistemas de origen deben planificarse cuidadosamente para mantener gráficos de identidad correctos.
>* **Utilización del lago de datos**: el consumo de almacenamiento general, las relaciones de tabla y los perfiles direccionables deben evaluarse antes de la ingesta.

| | Datos almacenados en Data Lake | Conjunto de datos habilitado para el perfil |
| --- | --- | --- |
| **Opción 1**: datos externos mediante acciones personalizadas | No | No |
| **Opción 2** — Conjunto de datos no habilitado para el perfil | Sí | No |
| **Opción 3** — Conjunto de datos habilitado para el perfil | Sí | Sí |

Para obtener más información sobre cómo configurar una fuente de datos de Adobe Experience Platform y una fuente de datos externa, y cómo buscar y usar los datos en un recorrido, vea este [vídeo tutorial](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target="_blank"}.

## Vídeo práctico {#video}

Comprenda qué es una fuente de datos y aprenda a configurar fuentes de datos de Experience Platform y externas.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

