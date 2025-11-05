---
product: journey optimizer
title: inAudience, función
description: Obtenga información sobre la función Adobe Experience Platform en Audience
feature: Journeys
role: Developer
level: Experienced
keywords: inAudience, función, expresión, recorrido, audiencia, segmentación
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: 4f653c0bd3f6998dd54deeae996b7b0427a1744e
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 2%

---

# inAudience, función {#inAudience}

La función `inAudience` es una función de Adobe Experience Platform que le permite comprobar si un individuo del recorrido pertenece a una audiencia específica. Esta potente función le permite crear rutas de recorrido personalizadas basadas en la pertenencia a audiencias, lo que permite una segmentación y un direccionamiento sofisticados dentro de las experiencias de los clientes.

Utilice la función `inAudience` cuando necesite:

* Rutas de recorrido de ramas basadas en la pertenencia a audiencias. [Más información](../condition-activity.md#using-a-segment)
* Aplique una lógica condicional que dependa de si un perfil pertenece a un segmento específico
* Segmente a grupos específicos de clientes con experiencias personalizadas
* Evaluar la participación de audiencias en tiempo real dentro de las condiciones de recorrido
* Combinar varias comprobaciones de audiencia para crear reglas de segmentación complejas

La función evalúa la pertenencia de la audiencia en tiempo real y devuelve un valor booleano, lo que la hace ideal para nodos de decisión y expresiones condicionales. Las audiencias se definen y administran en [Adobe Experience Platform](https://platform.adobe.com/audience/overview){target="_blank"} (obtenga más información sobre [cómo trabajar con audiencias](../../audience/about-audiences.md) en Journey Optimizer) y el editor de expresiones proporciona sugerencias de autocompletar para ayudarle a hacer referencia a ellas con precisión.

**Estado de audiencia:**

Las audiencias pueden tener dos estados de participación:

* **Realizado**: el individuo cumple los requisitos para la definición de audiencia y es un miembro activo
* **Salido**: el usuario ha abandonado la audiencia y ya no cumple los requisitos

Solo las personas con el estado **Realized** se considerarán como miembros activos de la audiencia. Cuando la función devuelve `true`, confirma que el individuo tiene estado realizado; cuando devuelve `false`, indica estado saliente. Para obtener más información sobre la evaluación de audiencias, consulte la [documentación del servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

+++Sintaxis

`inAudience(<parameter>)`

+++

+++Parámetros

| Parámetro | Descripción | Tipo |
|--- |--- |--- |
| Público | El nombre de la audiencia | `<string>` |

**Restricciones importantes:**

* El nombre de la audiencia debe ser una constante de cadena
* No puede ser una referencia de campo o una expresión
* Puede recuperar hasta 100 audiencias en un solo recorrido

+++

+++Firma y tipo devuelto

`inAudience(<string>)`

Devuelve un valor booleano:
* `true`: el individuo es miembro de la audiencia (estado realizado)

* `false`: el individuo no es miembro de la audiencia (estado de salida)

+++

+++Ejemplos

`inAudience("men over 50")`

Devuelve **true** si el individuo de la instancia de recorrido es parte de la audiencia de Adobe Experience Platform denominada &quot;hombres de más de 50 años&quot;, **false** en caso contrario.

**Casos de uso prácticos:**

```
// Simple audience check in a condition
inAudience("Premium Customers") == true

// Multiple audience evaluation
inAudience("High Value Customers") == true AND inAudience("Active Last 30 Days") == true

// Negation check
inAudience("Unsubscribed") == false
```

+++

## Mecanismos de protección y limitaciones {#guardrails}

Cuando use la función `inAudience` en los recorridos, tenga en cuenta las siguientes limitaciones y protecciones:

**Límite de recuperación de audiencia:**
* Puede recuperar hasta 100 audiencias en un solo recorrido
* El editor de expresiones proporciona una lista autocompletada de audiencias disponibles para ayudarle a hacer referencia a ellas correctamente

**Restricciones de parámetro:**
* El nombre de la audiencia debe ser una constante de cadena
* Las referencias y expresiones de campo no se admiten como parámetros

**Cambios en el nombre de la audiencia:**
* Cambiar el nombre de una audiencia existente en Adobe Experience Platform no actualiza automáticamente ninguna referencia a esa audiencia en las expresiones de recorrido
* Si el nodo de condición utiliza `inAudience('oldAudienceName')`, debe editar manualmente la expresión para utilizar el nuevo nombre
* Si no se actualiza el nombre de la audiencia, la condición de recorrido se romperá y puede dar como resultado un comportamiento de recorrido incorrecto

**Consideraciones de políticas de combinación:**
* Cuando se utilizan varias audiencias con la función `inAudience`, las incoherencias con las políticas de combinación pueden provocar errores o alertas
* Consulte [propiedades de Recorrido](../journey-properties.md) para obtener más información sobre el comportamiento de la política de combinación

## Temas relacionados

Obtenga más información sobre el uso de audiencias en Adobe Journey Optimizer:

* **[Acerca de las audiencias](../../audience/about-audiences.md)**: Descubra cómo funcionan las audiencias en Adobe Experience Platform y Journey Optimizer, y cómo crearlas y administrarlas
* **[Leer actividad de audiencia](../read-audience.md)** - Use audiencias para almacenar en déclencheur la entrada de recorrido y hacer que todos los miembros de la audiencia ingresen a un recorrido
* **[Eventos de calificación de audiencias](../audience-qualification-events.md)**: escuche las entradas y salidas de perfiles de audiencias para déclencheur las acciones de recorrido en tiempo real
* **[Uso de audiencias en condiciones](../condition-activity.md#using-a-segment)**: cree rutas de recorrido condicionales basadas en la pertenencia a audiencias mediante la actividad Condición
* **[Propiedades del Recorrido - Políticas de combinación](../journey-properties.md)** - Comprenda cómo funcionan las políticas de combinación al utilizar varias audiencias con la función inAudience

