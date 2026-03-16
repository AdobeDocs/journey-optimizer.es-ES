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
source-git-commit: 302db58525a7b2648bb9c44bc9b42da787ca9c43
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 11%

---

# Administración de etiquetas en recorrido {#journey_tags}

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
