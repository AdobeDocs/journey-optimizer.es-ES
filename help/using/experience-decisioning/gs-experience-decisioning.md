---
title: Introducción a la toma de decisiones
description: Más información sobre la toma de decisiones
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/z-9FSXpQNMyy0KcGaLWgDYHqAx-BWhIEJYAq4wVqmv4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: c8d0f67628d61c05c2b062831f382156fd212e7b
workflow-type: tm+mt
source-wordcount: 751
ht-degree: 22%

---

# Introducción a la toma de decisiones {#get-started-experience-decisioning}

>[!CONTEXTUALHELP]
>id="ajo_email_enable_experience_decisioning"
>title="¿Qué es la toma de decisiones?"
>abstract="La toma de decisiones es una nueva herramienta, además de la gestión de decisiones, para elegir los mejores elementos del motor de decisión y entregarlos a cada individuo. Requiere una configuración adicional para poderla utilizar."

## Qué es Decisioning {#about}

La toma de decisiones simplifica la personalización al ofrecer un catálogo centralizado de ofertas de marketing conocidas como “elementos de decisión” y un motor de decisión sofisticado. Este motor aprovecha las reglas y los criterios de clasificación para seleccionar y presentar a cada persona los elementos de decisión más relevantes.

Estos elementos de decisión se integran perfectamente en los mensajes y experiencias de [!DNL Adobe Journey Optimizer] canales: [experiencia basada en código](../code-based/get-started-code-based.md), correo electrónico, SMS, notificaciones push y [correo directo](batch-decisioning-direct-mail.md) para la toma de decisiones por lotes y las exportaciones personalizadas de correo directo. La compatibilidad de Experience Decisioning con el correo postal es una nueva funcionalidad; anteriormente, el motor de decisión no estaba disponible para los archivos de extracción de correo postal.

>[!IMPORTANT]
>
>Las directivas de decisión están disponibles para todos los clientes para los canales **Experiencia basada en código**, **Correo electrónico**, **Notificación push**, **SMS** y **Correo directo**.

➡️ [Descubra esta funcionalidad en vídeo](#video)

➡️ En [esta sección](experience-decisioning-uc.md) se presenta un caso de uso de extremo a extremo que muestra cómo crear decisiones y utilizarlas en experimentos de contenido con el canal de experiencia basado en código.

## Pasos clave de decisiones {#steps}

Los pasos principales para trabajar con Decisioning son los siguientes:

1. **Asigne los permisos adecuados**. La toma de decisiones solo está disponible para los usuarios con acceso a un **[!UICONTROL rol]** relacionado con la toma de decisiones, como los administradores de decisiones. Si no puede acceder a Decisioning, debe ampliar los permisos.

   +++Obtenga información sobre cómo asignar la función Administradores de decisiones

   1. Para asignar una función a un usuario en el producto [!DNL Permissions], vaya a la pestaña **[!UICONTROL Funciones]** y seleccione Administradores de decisiones.

      ![](assets/decision_permission_1.png)

   1. En la pestaña **[!UICONTROL Usuarios]**, haga clic en **[!UICONTROL Añadir usuario]**.

      ![](assets/decision_permission_2.png)

   1. Introduzca el nombre o la dirección de correo electrónico del usuario o seleccione el usuario en la lista y haga clic en **[!UICONTROL Guardar]**.

      Si el usuario no se ha creado previamente, consulte la [documentación de Añadir usuarios](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   El usuario debería recibir entonces un correo electrónico que le redirija a su instancia.

   +++

1. **Configurar atributos personalizados**: adapte el catálogo de artículos a sus necesidades específicas configurando atributos personalizados en el esquema del catálogo.

   ➡️ [Aprenda a configurar el catálogo de artículos](catalogs.md)

1. **Cree elementos de decisión** para mostrarlos a la audiencia de destino.

   ➡️ [Aprenda a crear elementos de decisión](items.md) en la interfaz de usuario (y en la [documentación de API](api-reference/decisions-items/create.md))

1. **Organizar con colecciones**: Use colecciones para categorizar los elementos de decisión según las reglas basadas en atributos. Incorpore colecciones en las estrategias de selección para determinar qué colección de elementos de decisión se debe tener en cuenta.

   ➡️ [Obtenga información sobre cómo administrar colecciones de elementos](collections.md) en la interfaz de usuario (y en la [documentación de API](api-reference/items-collections/create.md))

1. **Crear reglas de decisión**: Las reglas de decisión se utilizan en elementos de decisión o estrategias de selección para determinar a quién se puede mostrar un elemento de decisión.

   ➡️ [Obtenga información sobre cómo crear reglas de decisión](rules.md)

1. **Implementar métodos de clasificación**: Cree métodos de clasificación y aplíquelos dentro de las estrategias de selección para determinar el orden de prioridad para seleccionar elementos de decisión.

   ➡️ [Aprenda a crear métodos de clasificación](ranking/ranking.md)

1. **Crear estrategias de selección**: genere estrategias de selección que aprovechen colecciones, reglas de decisión y métodos de clasificación para identificar los elementos de decisión adecuados para mostrarlos a los perfiles.

   ➡️ [Aprenda a crear estrategias de selección en la interfaz de usuario](selection-strategies.md) en la interfaz de usuario (y en la [documentación de API](api-reference/selection-strategies/create.md))

1. **Cree una política de decisión e incrústela en su recorrido o campaña** (experiencia basada en código, correo electrónico, SMS o push): las políticas de decisión combinan varias estrategias de selección para determinar los elementos de decisión aptos que se mostrarán a la audiencia deseada.

   ➡️ [Aprenda a trabajar con directivas de decisión](create-decision.md)
➡️ Para entregar correctamente la oferta a través del canal de experiencia basado en código, siga los pasos de implementación de [esta sección](../code-based/code-based-implementation-samples.md).

## Proceso de toma de decisiones {#process}

El siguiente gráfico resume el proceso de toma de decisiones de extremo a extremo: desde la administración de elementos de decisión y la configuración de estrategias de selección hasta la incrustación de políticas de decisión en un recorrido de experiencias o una campaña basados en código.

![](assets/decisioning-process.png){zoomable="yes"}

## Recursos adicionales {#additional-resources}

* **[Crear elementos de decisión](items.md)**: aprenda a crear y administrar elementos de decisión, incluidas ofertas, variaciones de contenido y experiencias.
* **[Configurar catálogos de decisiones](catalogs.md)**: aprenda a organizar los elementos de decisión en catálogos para mejorar la administración.
* **[Definir estrategias de selección](selection-strategies.md)**: descubra cómo crear estrategias de selección con reglas de elegibilidad y métodos de clasificación.
* **[Crear directivas de decisión](create-decision-policy.md)**: aprenda a crear directivas de decisión que combinen estrategias y restricciones.
* **[Modelos de clasificación e IA](ranking/ranking.md)**: fórmulas de clasificación maestras y modelos de IA para la toma de decisiones personalizada.
* **[Migrar desde Administración de decisiones](migrate-to-decisioning.md)**: comprenda los beneficios de migrar a la toma de decisiones y utilice las API de herramientas de migración.
* **[Protecciones para la toma de decisiones](decisioning-guardrails.md)**: revise las limitaciones importantes y las prácticas recomendadas para la implementación de decisiones.
* **[Tutoriales de toma de decisiones](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/decision-capabilities/decisioning/introduction-to-decisioning){target="_blank"}**: explore tutoriales de vídeo paso a paso sobre las funciones de toma de decisiones y las prácticas recomendadas.

## Vídeo práctico {#video}

Obtenga información sobre las funcionalidades de Decisioning en Adobe Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3475866?captions=spa&quality=12)
