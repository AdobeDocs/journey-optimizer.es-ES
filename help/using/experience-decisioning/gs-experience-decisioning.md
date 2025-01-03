---
title: Introducción a Decisioning
description: Más información sobre las Decisiones
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 616e1dd9fbfd029f7209356d5c19cfff9d4b4f06
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 15%

---

# Introducción a Decisioning {#get-started-experience-decisioning}

## Qué es Decisioning {#about}

Decisioning simplifica la personalización al ofrecer un catálogo centralizado de ofertas de marketing conocidas como “elementos de decisión” y un motor de decisión sofisticado. Este motor aprovecha las reglas y los criterios de clasificación para seleccionar y presentar a cada persona los elementos de decisión más relevantes.

Estos elementos de decisión se integran a la perfección en una amplia gama de superficies de entrada a través del [nuevo canal de experiencia basado en código](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/get-started-code-based), ahora accesible desde las campañas de Journey Optimizer. Las políticas de decisión solo están disponibles para su uso en campañas de experiencia basadas en código.

## Mecanismos de protección y limitaciones {#guardrails}

Para garantizar un uso óptimo de Decisioning, tenga en cuenta las siguientes limitaciones y protecciones:

### Protecciones generales {#general}

* **Elementos de oferta**: Cada colección de elementos puede contener hasta 500 elementos de oferta.
* **Atributos personalizados**: un elemento de decisión puede incluir un máximo de 100 atributos personalizados.
* **Estrategias de selección y elementos de decisión por directiva**: una directiva de decisión admite hasta 10 estrategias de selección y elementos de decisión combinados.

### Reglas de elegibilidad {#eligibility}

* **Niveles de anidación**: la profundidad de anidación está limitada a 30 niveles. Esto se mide contando los `)` paréntesis de cierre en la cadena de PQL.
* **Tamaño de cadena de regla**: una cadena de regla puede tener un tamaño máximo de 15 KB para caracteres codificados en UTF-8. Esto equivale a 15 000 caracteres ASCII (1 byte cada uno) o a 3 750-7 500 caracteres no ASCII (2-4 bytes cada uno).

### Fórmulas de clasificación {#ranking}

* **Niveles de anidación**: la profundidad de anidación está limitada a 30 niveles. Esto se mide contando los `)` paréntesis de cierre en la cadena de PQL.
* **Tamaño de cadena de fórmula**: una cadena de regla puede tener un tamaño máximo de 8 KB para caracteres codificados en UTF-8. Esto equivale a 8.000 caracteres ASCII (1 byte cada uno) o a 2.000-4.000 caracteres no ASCII (2-4 bytes cada uno).

## Pasos clave de decisiones {#steps}

Los pasos principales para trabajar con Decisioning son los siguientes:

1. **Asigne los permisos adecuados**. La toma de decisiones solo está disponible para los usuarios con acceso a un **[!UICONTROL rol]** relacionado con la toma de decisiones, como los administradores de decisiones. Si no puede acceder a Decisioning, debe ampliar los permisos.

   +++Obtenga información sobre cómo asignar la función Administradores de decisiones

   1. Para asignar una función a un usuario en el producto [!DNL Permissions], vaya a la pestaña **[!UICONTROL Funciones]** y seleccione Administradores de decisiones.

      ![](assets/decision_permission_1.png)

   1. En la pestaña **[!UICONTROL Usuarios]**, haga clic en **[!UICONTROL Añadir usuario]**.

      ![](assets/decision_permission_2.png)

   1. Introduzca el nombre o la dirección de correo electrónico del usuario o selecciónelo de la lista y haga clic en **[!UICONTROL Guardar]**.

      Si el usuario no se ha creado previamente, consulte la [documentación de Añadir usuarios](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   El usuario debería recibir entonces un correo electrónico que le redirija a su instancia.

+++

1. **Configurar atributos personalizados**: adapte el catálogo de artículos a sus necesidades específicas configurando atributos personalizados en el esquema del catálogo.

   ➡️ [Obtenga información sobre cómo configurar el catálogo de artículos](catalogs.md)

1. **Cree elementos de decisión** para mostrarlos a la audiencia de destino.

   ➡️ [Obtenga información sobre cómo crear elementos de decisión](items.md) ([documentación de API](api-reference/decisions-items/create.md))

1. **Organizar con colecciones**: Use colecciones para categorizar los elementos de decisión según las reglas basadas en atributos. Incorpore colecciones en las estrategias de selección para determinar qué colección de elementos de decisión se debe tener en cuenta.

   ➡️ [Obtenga información sobre cómo administrar colecciones de elementos](collections.md) ([documentación de API](api-reference/items-collections/create.md))

1. **Crear reglas de decisión**: Las reglas de decisión se utilizan en elementos de decisión o estrategias de selección para determinar a quién se puede mostrar un elemento de decisión.

   ➡️ [Obtenga información sobre cómo crear reglas de decisión](rules.md)

1. **Implementar métodos de clasificación**: Cree métodos de clasificación y aplíquelos dentro de las estrategias de decisión para determinar el orden de prioridad para seleccionar elementos de decisión.

   ➡️ [Aprenda a crear métodos de clasificación](ranking.md)

1. **Crear estrategias de selección**: genere estrategias de selección que aprovechen colecciones, reglas de decisión y métodos de clasificación para identificar los elementos de decisión adecuados para mostrarlos a los perfiles.

   ➡️ [Obtenga información sobre cómo crear estrategias de selección](selection-strategies.md) ([documentación de API](api-reference/selection-strategies/create.md))

1. **Cree una política de decisión e incrústela en su campaña basada en código**: las políticas de decisión combinan varias estrategias de selección para determinar los elementos de decisión aptos para mostrar a la audiencia deseada.

   ➡️ [Aprenda a trabajar con directivas de decisión](create-decision.md)
