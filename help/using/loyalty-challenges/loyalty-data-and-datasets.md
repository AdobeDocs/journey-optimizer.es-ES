---
solution: Journey Optimizer
product: journey optimizer
title: Datos y conjuntos de datos de fidelización
description: Descubra qué datos de perfil de Adobe Experience Platform y conjuntos de datos requiere Desafíos de lealtad, y cómo afecta el tiempo de vida (TTL) de los conjuntos de datos a la retención.
feature: Journeys
topic: Content Management
role: Admin, Developer
level: Intermediate
hide: true
badge: label="Beta privada" type="Informative"
mini-toc-levels: 1
exl-id: a7c4e1b2-8f3d-4a6c-9e0b-1d2e3f4a5b6c
source-git-commit: 894dd7f811e87a8551f92654e5b913a459c1382e
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 5%

---

# Datos y conjuntos de datos de fidelización {#loyalty-data-and-datasets}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización**

[Introducción a los retos de fidelización](get-started.md)

+++Crear y administrar desafíos

* [Acceder y administrar desafíos y tareas](access-loyalty-challenges.md)
* [Crear desafíos](create-challenges.md)
* [Creación de tareas](create-tasks.md)
* [Monitorización del rendimiento del desafío de fidelidad](loyalty-reporting.md)

+++

+++Configuración e integración

<!-- * [Configure loyalty challenges](loyalty-admin.md) -->
* **Conjuntos de datos y datos de fidelización** ◀︎ **Usted está aquí**
* [Referencia de API de retos de fidelización](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

+++

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica se encuentra actualmente en **versión beta privada**. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](../rn/releases.md).

## Información general {#overview}

Los desafíos de fidelidad dependen de Adobe Experience Platform para la identidad, los atributos de perfil, los eventos de experiencia y las audiencias. Utilice esta página para conocer qué datos preparar, qué conjuntos de datos están involucrados y cómo **tiempo de vida (TTL)** afecta la retención antes de crear desafíos o usar las API de desafíos de fidelidad.

Póngase en contacto con su administrador de Adobe para configurar el programa de Journey Optimizer (satisfacción de recompensas y asignación de eventos). Para obtener los extremos REST y la autenticación, consulte la [Referencia de la API de retos de fidelidad](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}.

## Datos de Adobe Experience Platform {#aep-data}

### Atributos de perfil {#profile-attributes}

Las audiencias de desafío, la personalización y los perfiles de uso de informes se encuentran en la clase **[!DNL XDM Individual Profile]**. Alinee la identidad [área de nombres](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/namespaces){target="_blank"} que usa para los retos de fidelidad con la forma en que se identifican los miembros en los datos de perfil.

Para los atributos de fidelidad estándar del perfil (puntos, nivel, programa, estado y campos relacionados), utilice el grupo de campos de esquema **[Detalles de fidelidad](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}** de Experience Platform. Ese grupo de campos define el objeto `loyalty` y sus propiedades (por ejemplo, `points`, `tier`, `program` y `status`).

➡️ [grupo de campos de esquema de detalles de fidelización](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}

### Eventos de experiencia {#experience-events}

Las tareas **[!UICONTROL Compra]**, **[!UICONTROL Gasto]** y **[!UICONTROL Evento personalizado]** dependen de los eventos de experiencia ingeridos en Adobe Experience Platform. Para las tareas **[!UICONTROL Custom Event]**, el administrador debe configurar las definiciones de evento coincidentes (ruta de identificador, ID de esquema XDM opcional, esquema y transformador) para que pueda seleccionarlas en el generador de tareas.

Asegúrese de que las cargas útiles de evento utilicen el mismo área de nombres de identidad que la configuración de Retos de fidelidad para que el progreso se pueda atribuir al perfil correcto.

### Audiencias e informes {#audiences-reporting}

Los especialistas en marketing seleccionan la plataforma [audiencias](../audience/about-audiences.md) al configurar la idoneidad para el desafío. Los paneles de informes de fidelización utilizan Adobe Customer Journey Analytics. [Aprenda a monitorizar el rendimiento del desafío de lealtad](loyalty-reporting.md)

## Tiempo de vida del conjunto de datos (TTL) {#dataset-ttl}

Los retos de fidelización almacenan datos operativos y de informes en conjuntos de datos de Adobe Experience Platform (incluidos conjuntos de datos relacionados con eventos y personalización creados para su programa). El conjunto de datos **tiempo de vida (TTL)** controla cuánto tiempo se retienen los datos en el lago de datos y, cuando corresponde, en el almacén de perfiles.

Journey Optimizer aplica protecciones TTL a muchos conjuntos de datos generados por el sistema. Los conjuntos de datos relacionados con la fidelización siguen el mismo modelo de retención de Platform para la zona protegida.

➡️ [protecciones de tiempo de vida (TTL) de conjuntos de datos en Journey Optimizer](../data/datasets-ttl.md)

>[!NOTE]
>
>La configuración de lealtad en el nivel de organización puede incluir la configuración de archivo y retención (por ejemplo, la duración del archivo) administrada mediante el servicio de metadatos de lealtad. Póngase en contacto con el administrador de Adobe si necesita ajustar la retención de su entorno beta privado.

<!-- For UI-based setup (reward providers, event definitions, product inventory, and exclusions), see [Configure loyalty challenges](loyalty-admin.md). -->
