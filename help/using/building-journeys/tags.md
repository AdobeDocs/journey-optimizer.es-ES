---
solution: Journey Optimizer
product: journey optimizer
title: Administración de etiquetas en recorrido
description: Administración de etiquetas en recorrido
feature: Journeys, Tags
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, etiquetas
exl-id: 44c255d1-121c-47d4-b407-161626ca3cb4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/O8Igbj-JJGr0aej8xbSvZ51xkcJq8LeJ9JiveyBjBqQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1152
ht-degree: 7%

---

# Administración de etiquetas en recorrido {#journey_tags}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a organizar recorridos con etiquetas y categorías de etiquetas para que pueda clasificar, filtrar y encontrar sus recorridos más fácilmente que con las convenciones de nomenclatura.

>[!ENDSHADEBOX]

Como profesional de Journey Optimizer, puede organizar sus recorridos mediante etiquetas. Las etiquetas son una forma rápida y sencilla de clasificar objetos para mejorar la búsqueda.

## Convenciones de etiquetas y nomenclatura {#tags-vs-naming}

Los equipos suelen depender de convenciones de nomenclatura complejas para almacenar metadatos directamente en los nombres de recorrido; por ejemplo: *Marketing del ciclo vital - Educación - Incorporación del cliente V2 - Educación de aplicaciones - T3 2025*. Aunque bien intencionado, este enfoque tiene una debilidad clave: a medida que el trabajo se escala entre los miembros del equipo, la convención rara vez se aplica de manera consistente, y las listas de recorrido se vuelven difíciles de navegar.

**Las categorías de etiquetas** en Journey Optimizer ofrecen una alternativa mejor. En lugar de codificar los metadatos en el nombre, se adjuntan etiquetas clasificadas a cada recorrido (por ejemplo, equipo, objetivo, fase, trimestre) y se utilizan filtros para localizarlos. Los nombres de los recorridos pueden centrarse en lo que realmente importa: el hito del cliente que se está impulsando.

Ventajas de las categorías de etiquetas sobre las convenciones de nomenclatura:

* **Consistencia**: las etiquetas se seleccionan de una lista controlada, no se escriben libremente.
* **Filtrabilidad**: cualquier combinación de valores de etiqueta se puede usar para cortar la lista de recorrido instantáneamente.
* **Claridad**: los nombres de los recorridos son cortos y se centran en los hitos.
* **Escalabilidad**: agregar una nueva dimensión de metadatos implica crear una nueva categoría de etiquetas, no volver a escribir una convención de nombres.

Para ver un flujo de trabajo de configuración recomendado, consulte [Configurar categorías de etiquetas para la administración de recorrido](#tags-setup) a continuación.

## Adición de etiquetas a un recorrido

El campo **Etiquetas**, en las propiedades del recorrido, le permite definir etiquetas para el recorrido. Puede seleccionar una etiqueta existente o crear una nueva. Empiece a escribir el nombre de la etiqueta deseada y selecciónela en la lista. Si no está disponible, haz clic en **Crear** para crear uno nuevo y agregarlo al recorrido. Puede definir tantas etiquetas como sea necesario.

![Panel Etiquetas en las propiedades de recorrido para la categorización y organización](assets/tags1.png)

La lista de etiquetas definidas se muestra debajo del campo **Etiquetas** campo.

>[!NOTE]
>
> Las etiquetas distinguen entre mayúsculas y minúsculas
> 
> Si duplica o crea una nueva versión de un recorrido, las etiquetas se conservan.

## Filtrar por etiquetas

La lista de Recorridos muestra una columna específica para que pueda visualizar fácilmente las etiquetas.

También hay un filtro disponible para mostrar solo los recorridos con determinadas etiquetas.

![Menú desplegable de selección de etiquetas con etiquetas disponibles para la clasificación de recorrido](assets/tags2.png)

Puede añadir o quitar recorridos de cualquier tipo (activo, borrador, etc.). Haga clic en el icono **Más acciones** que está junto al recorrido y seleccione **Editar etiquetas**.

![Lista de Recorridos filtrada por etiquetas que muestran recorridos categorizados](assets/tags3.png)

## Administrar etiquetas

Los administradores pueden eliminar etiquetas y organizarlas por categorías utilizando la variable **Etiquetas** en **ADMINISTRACIÓN**. Consulte esta [documentación](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/overview.html?lang=es).

>[!NOTE]
>
> Las etiquetas definidas en recorridos se añaden a la categoría &quot;Sin categoría&quot; integrada.

## Configuración de categorías de etiquetas para la administración de recorridos {#tags-setup}

Siga estos pasos para reemplazar una convención de nombres compleja con un enfoque basado en etiquetas en todo su equipo.

**Paso 1 — Crear categorías de etiquetas (Administrador)**

En **[!UICONTROL Administración]** > **[!UICONTROL Etiquetas]**, cree una categoría para cada atributo de metadatos que su equipo codifique actualmente en nombres de recorrido; por ejemplo: *Equipo*, *Objetivo de marketing*, *Campaña*, *Fase*, *Trimestre*.

**Paso 2: Rellene cada categoría con valores de etiqueta (Administrador)**

Dentro de cada categoría, cree las etiquetas que representen todos los valores posibles. Por ejemplo, la categoría *Fase* puede contener: *Conocimiento*, *Incorporación*, *Retención*, *Recuperación*.

**Paso 3: Aplicar etiquetas al crear recorridos (Profesionales)**

Cada vez que cree un nuevo recorrido, seleccione la etiqueta adecuada de cada categoría en las propiedades del recorrido. Un recorrido normalmente lleva una etiqueta por categoría.

**Paso 4: nombrar los recorridos del hito y filtrar por etiquetas**

Mantenga el nombre del recorrido centrado en el hito de cliente que marca (p. ej. *Primera transacción de fidelidad*). Utilice filtros de etiquetas en la lista de recorrido para localizar recorridos mediante cualquier combinación de metadatos, sin depender del análisis de nombres.

>[!TIP]
>
>Para un análisis más amplio de este enfoque y sus ventajas a escala, consulte [Prácticas recomendadas para recorridos avanzados en Journey Optimizer](https://experienceleague.adobe.com/es/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica cómo agregar, filtrar y administrar etiquetas en recorridos en Adobe Journey Optimizer, y por qué las categorías de etiquetas son una mejor alternativa a las convenciones de nomenclatura complejas para organizar listas de recorridos grandes.

**Intenciones:**
* Añadir etiquetas a un recorrido desde el campo de propiedades de recorrido Etiquetas
* Filtre la lista de recorridos por una o más etiquetas para localizar rápidamente recorridos específicos
* Editar etiquetas en recorridos existentes de cualquier estado (activo, borrador, etc.) mediante Más acciones
* Cree y organice categorías de etiquetas como administrador para aplicar metadatos coherentes
* Reemplace una convención de nombres de recorrido compleja con un enfoque estructurado basado en etiquetas

**Glosario:**
* **Etiquetas**: Etiquetas adjuntas a recorridos para clasificarlos y filtrarlos; no distingue entre mayúsculas y minúsculas y se conservan cuando un recorrido está duplicado o tiene versiones *(específico del producto)*
* **Categorías de etiquetas**: agrupaciones de valores de etiquetas relacionados creadas por administradores en Administración > Etiquetas, lo que permite la clasificación de metadatos estructurada *(específica del producto)*
* **Categoría sin categoría**: La categoría predeterminada integrada a la que se asignan automáticamente las etiquetas creadas directamente en los recorridos *(específica del producto)*

**Protecciones:**
* Las etiquetas no distinguen entre mayúsculas y minúsculas
* Las etiquetas definidas en recorrido se añaden automáticamente a la categoría &quot;Sin categoría&quot; integrada a menos que un administrador las asigne a una categoría con nombre
* Solo los administradores pueden eliminar etiquetas y administrar las categorías de etiquetas a través del menú Administración > Etiquetas
* Las etiquetas se conservan cuando se duplica un recorrido o se crea una nueva versión

**Terminología:**
* Nombre canónico: Tags — Acrónimo: none — variantes: etiquetas de recorrido, etiquetas administrativas
* Nombre canónico: Categorías de etiquetas — Acrónimo: none — variantes: grupos de etiquetas
* No confunda: &quot;Etiquetas&quot; (etiquetas de clasificación de recorrido) ≠ &quot;convenciones de nomenclatura&quot; (metadatos codificados directamente en nombres de recorrido)

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Cómo se agrega una etiqueta a un recorrido?** — En las propiedades del recorrido, escriba el nombre de la etiqueta en el campo Etiquetas y selecciónela en la lista, o bien haga clic en Crear para añadir una etiqueta nueva.
* **Q: ¿Puedo agregar etiquetas a un recorrido activo?** — Sí. Haga clic en el icono de Más acciones situado junto al recorrido en la lista y seleccione Editar etiquetas para añadir o quitar etiquetas en cualquier recorrido independientemente del estado.
* **Q: ¿Las etiquetas distinguen entre mayúsculas y minúsculas?** — No. Las etiquetas no distinguen entre mayúsculas y minúsculas.
* **Q: ¿Qué les sucede a las etiquetas cuando duplico un recorrido o creo una nueva versión?** — Las etiquetas se conservan en el duplicado o en la nueva versión.
* **Q: ¿Quién puede eliminar etiquetas o crear categorías de etiquetas?** — Solo los administradores pueden eliminar etiquetas y administrar las categorías de etiquetas mediante el menú Administración > Etiquetas.
* **Q: ¿Por qué usar categorías de etiquetas en lugar de convenciones de nomenclatura?** — Las categorías de etiquetas refuerzan la coherencia a través de una lista controlada, permiten un filtrado multidimensional instantáneo, mantienen los nombres de los recorridos cortos y centrados en los hitos y escalan fácilmente añadiendo nuevas categorías sin reescribir las reglas de nomenclatura.

+++
