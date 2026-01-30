---
title: Introducción a la toma de decisiones
description: Más información sobre la toma de decisiones
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
version: Journey Orchestration
source-git-commit: 21de0b9616c414db204a3eafebc6a8184028a1e1
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 22%

---

# Introducción a la toma de decisiones {#get-started-experience-decisioning}

>[!CONTEXTUALHELP]
>id="ajo_email_enable_experience_decisioning"
>title="¿Qué es la toma de decisiones?"
>abstract="La toma de decisiones es una nueva herramienta, además de la gestión de decisiones, para elegir los mejores elementos del motor de decisión y entregarlos a cada individuo. Requiere una configuración adicional para poderla utilizar."

## Qué es Decisioning {#about}

La toma de decisiones simplifica la personalización al ofrecer un catálogo centralizado de ofertas de marketing conocidas como “elementos de decisión” y un motor de decisión sofisticado. Este motor aprovecha las reglas y los criterios de clasificación para seleccionar y presentar a cada persona los elementos de decisión más relevantes.

Estos elementos de decisión se integran perfectamente en una amplia gama de superficies de entrada a través del [canal de experiencia basado en código](../code-based/get-started-code-based.md), al que se puede acceder desde [!DNL Adobe Journey Optimizer] campañas.

>[!IMPORTANT]
>
>Las políticas de decisión están disponibles para su uso únicamente en campañas de experiencia basadas en código y de correo electrónico.

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

1. **Cree una política de decisión e incrústela en su recorrido/campaña de correo electrónico o basado en código**: las políticas de decisión combinan varias estrategias de selección para determinar los elementos de decisión aptos que se mostrarán a la audiencia deseada.

   ➡️ [Aprenda a trabajar con directivas de decisión](create-decision.md)
➡️ Para entregar correctamente la oferta a través del canal de experiencia basado en código, siga los pasos de implementación de [esta sección](../code-based/code-based-implementation-samples.md).

## Recursos adicionales

* **[Crear elementos de decisión](items.md)**: aprenda a crear y administrar elementos de decisión, incluidas ofertas, variaciones de contenido y experiencias.
* **[Configurar catálogos de decisiones](catalogs.md)**: aprenda a organizar los elementos de decisión en catálogos para mejorar la administración.
* **[Definir estrategias de selección](selection-strategies.md)**: descubra cómo crear estrategias de selección con reglas de elegibilidad y métodos de clasificación.
* **[Crear directivas de decisión](create-decision-policy.md)**: aprenda a crear directivas de decisión que combinen estrategias y restricciones.
* **[Modelos de clasificación e IA](ranking/ranking.md)**: fórmulas de clasificación maestras y modelos de IA para la toma de decisiones personalizada.
* **[Protecciones para la toma de decisiones](decisioning-guardrails.md)**: revise las limitaciones importantes y las prácticas recomendadas para la implementación de decisiones.
* **[Tutoriales de toma de decisiones](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/decision-capabilities/decisioning/introduction-to-decisioning){target="_blank"}**: explore tutoriales de vídeo paso a paso sobre las funciones de toma de decisiones y las prácticas recomendadas.

## Vídeo práctico {#video}

Obtenga información sobre las funcionalidades de Decisioning en Adobe Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3451101?quality=12)
