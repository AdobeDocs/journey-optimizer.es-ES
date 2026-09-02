---
product: journey optimizer
title: inSegment
description: Obtenga información sobre la función en Segmento
feature: Journeys
role: Developer
level: Experienced
keywords: inSegment, function, expression, recorrido
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 521
ht-degree: 2%

---

# inSegment {#inSegment}

Comprueba si un individuo pertenece a una audiencia determinada.

>[!NOTE]
>
>Puede recuperar hasta 100 audiencias.

El nombre de la audiencia debe ser una constante de cadena. No puede ser una referencia de campo ni una expresión.

Las audiencias se definen en [Adobe Experience Platform](https://platform.adobe.com/audience/overview). El editor de expresiones proporciona una lista autocompletada de audiencias.

Las audiencias pueden tener dos estados:

* realizado: la entidad cumple los requisitos para la definición del segmento.
* saliente: la entidad sale de la definición del segmento.

Solo las personas con el estado de participación de audiencia **Realized** se considerarán miembros de la audiencia. Para obtener más información sobre cómo evaluar una audiencia, consulte la [documentación del servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results).

`inSegment('segmentName') == true` significa que tiene un segmentMembership con el estado introducido/existente.

`inSegment('segmentName') == false` significa que usted tiene un segmentMembership del estado saliente.

## Categoría

Adobe Experience Platform

## Sintaxis de función

`inSegment(<parameter>)`

## Parámetros

| Parámetro | Descripción | Tipo |
|--- |--- |--- |
| Segmento | El nombre de la audiencia | `<string>` |

## Firma y tipo devuelto

`inSegment(<string>)`

Devuelve un valor booleano.

## Ejemplo

`inSegment("men over 50")`

Explicación:

La función devolverá **[!UICONTROL true]** si el individuo de la instancia de recorrido es parte de la audiencia de Adobe Experience Platform denominada &quot;hombres de más de 50 años&quot;, **[!UICONTROL false]** en caso contrario.

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página documenta la función heredada `inSegment`, que comprueba si un perfil de recorrido pertenece a una audiencia de Adobe Experience Platform con nombre y devuelve un valor booleano.

**Intenciones:**
* Compruebe si un perfil es un miembro activo de una audiencia con nombre que usa `inSegment`
* Use `inSegment('name') == true` para confirmar la pertenencia a una audiencia realizada (activa) en una condición de recorrido
* Use `inSegment('name') == false` para confirmar la pertenencia a una audiencia saliente (inactiva)

**Glosario:**
* **Realizado**: el estado de participación de audiencia significa que la entidad cumple actualmente los requisitos para la definición de segmento *(específico del producto)*
* **Salido**: el estado de participación de audiencia significa que la entidad se va o ha salido de la definición de segmento *(específico del producto)*

**Protecciones:**
* Se pueden recuperar hasta 100 audiencias en un solo recorrido
* El nombre de la audiencia debe ser una constante de cadena; las referencias de campo y las expresiones no se admiten como parámetros

**Terminología:**
* Nombre canónico: inSegment — Acrónimo: none — variantes: inAudience (función preferida actual)
* Sinónimos: &quot;inSegment&quot; = &quot;comprobación de pertenencia a audiencia&quot; (heredado)
* No confunda: &quot;inSegment&quot; (función heredada/obsoleta) ≠ &quot;inAudience&quot; (función recomendada actual)
* No confunda: &quot;realizado&quot; (miembro activo) ≠ &quot;saliente&quot; (ya no es miembro)

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Cuál es la diferencia entre `inSegment` y `inAudience`?** — `inSegment` es el nombre de función heredada; `inAudience` es la función recomendada actual. Ambos comprueban la pertenencia a la audiencia, pero `inAudience` tiene documentación más completa que incluye protecciones y detalles de tiempo de propagación.
* **Q: ¿Qué significa `inSegment('name') == true`?** — Significa que el perfil tiene el estado &quot;realizado&quot; segmentMembership, es decir, la persona es un miembro activo de la audiencia.
* **Q: ¿Puedo pasar una expresión dinámica como nombre de audiencia?** — No, el nombre de audiencia debe ser una constante de cadena; no se admiten referencias de campo ni expresiones.
* **Q: ¿Cuántas audiencias puedo evaluar en un recorrido?** — Se pueden recuperar hasta 100 audiencias en un solo recorrido.

+++
