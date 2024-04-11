---
solution: Journey Optimizer
product: journey optimizer
title: Nueva interfaz de recorrido
feature: Release Notes
topic: Content Management
description: Nueva interfaz de recorrido
hide: true
hidefromtoc: true
exl-id: 03828fca-dde7-4b3b-b890-2c007d1245cc
source-git-commit: 3944c7b96baf227e4c0c1e7e1a225c1ce1ad0142
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# Nueva interfaz de recorrido {#new-canvas}

>[!CONTEXTUALHELP]
>id="ajo_new_canvas"
>title="Novedades"
>abstract="Nuevo lienzo"

Hemos trabajado en una simplificación del modelo de recorrido con el objetivo de facilitar algunos procesos internos. Este cambio de modelo por sí solo es transparente para usted, excepto que aprovechamos la oportunidad para introducir nuevas funciones junto con:

* Un nuevo diseño de lienzo de Recorrido
* Live Reporting en accesible en el lienzo de Recorrido
* Mejore la legibilidad del lienzo de recorrido y haga que el diseño de la actividad sea más escalable, lo que nos permite proporcionar más información a nivel de actividad para las mejoras actuales y futuras.

## Actualizaciones en el modelo de recorrido

El nuevo modelo de recorrido vivirá junto al existente, lo que significa que habrá recorridos que usarán dos modelos diferentes:

* El antiguo, llamado &quot;v1&quot;
* Y el nuevo, llamado &quot;v2&quot;

Todos los recorridos de la versión 1 permanecerán en la versión 1. Aún puede editarlos, probarlos o publicarlos. Cualquier nueva versión creada a partir de una versión 1 permanecerá en la versión 1. No hay cambios funcionales en los recorridos de la versión 1.

Se puede ver que un recorrido está en la versión 1 con su diseño de lienzo:

[CAPTURA DE PANTALLA]

Si contiene actividades de redondeo, es una versión 1.

Sin embargo, cuando cree un nuevo recorrido o duplique uno existente, será un recorrido de la versión 2. Debido a esto, esperamos ver cada vez menos recorridos de la versión 1 con el paso del tiempo. Asegúrese de que aún admitiremos los recorridos en directo de la versión 1 existentes.

Como hemos mencionado, este nuevo modelo es transparente para los usuarios, excepto por una limitación: no será posible copiar y pegar actividades de un recorrido v1 a un v2 y viceversa. Le recomendamos que duplique su recorrido de v1 para obtener automáticamente uno de v2.

Se puede ver que hay un recorrido en la versión 2 con el nuevo diseño de lienzo (véase más abajo):

[CAPTURA DE PANTALLA]

Cualquier nueva función alrededor del lienzo del recorrido (incluido Live Reporting) estará disponible exclusivamente en los recorridos de la versión 2.

## Nuevo diseño de lienzo de Recorrido

Con el nuevo modelo de recorrido presentamos un lienzo de Recorrido rediseñado, que se adapta perfectamente al ecosistema de soluciones y aplicaciones de Adobe Experience Cloud, lo que ofrece una experiencia de usuario intuitiva y eficaz. Cualquier recorrido de la pila de la versión 2 se basará en ese nuevo diseño.

[CAPTURA DE PANTALLA]

Las actividades ahora se representarán mediante cuadros cuadrados con:

* La primera línea que representa el tipo de actividad que a menudo se sobrescribe con información más contextual (p. ej.: en Audiencias leídas, contendrá el nombre de la audiencia seleccionada) o con una etiqueta personalizada si define una.
* El segundo activo siempre representa el tipo de actividad.

[CAPTURA DE PANTALLA]

Este nuevo diseño mejora la legibilidad del lienzo de recorrido al...

También es más escalable, lo que nos permite proporcionar más información a nivel de actividad, como empezamos a hacer con los informes en directo.

[CAPTURA DE PANTALLA]

¡Espere ver nuevos cambios en los próximos meses en torno a ese nuevo diseño!

## Informes en vivo

* GIF
* live reporting