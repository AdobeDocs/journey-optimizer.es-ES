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
source-git-commit: 596426f3b75a2e6f2d68e5b9218863c2d8887cca
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 1%

---

# Bienvenido al Diseñador de Recorridos mejorado {#new-canvas}

>[!CONTEXTUALHELP]
>id="ajo_new_canvas"
>title="Novedades"
>abstract="Nuevo lienzo"

Bienvenido al diseñador de recorridos mejorado.

Hemos desarrollado un **modelo de recorrido simplificado** que busca mejorar los procesos internos. Aunque este nuevo modelo supone una mejora del servidor, nuestro equipo aprovechó la oportunidad para añadir funciones que son visibles y beneficiosas para los usuarios de Journey Optimizer:

* A **lienzo de recorrido rediseñado** diseñado para una experiencia de interfaz de usuario modernizada
* A **live reporting** IU directamente disponible en el lienzo del recorrido

>[!AVAILABILITY]
>
>Tenga en cuenta que el despliegue de esta función será progresivo. Es posible que no vea los cambios de inmediato.

## Actualizaciones en el modelo de recorrido

El nuevo modelo de recorrido vivirá junto al existente, lo que significa que habrá recorridos utilizando **dos modelos diferentes**:

* El antiguo, llamado &quot;v1&quot;
* Y el nuevo, llamado &quot;v2&quot;

Todos los recorridos de la versión 1 permanecerán en la versión 1. Aún puede editarlos, probarlos o publicarlos. Cualquier nueva versión creada a partir de una versión 1 también permanecerá en la versión 1. No hay **sin cambios funcionales** alrededor de recorridos v1.

Como puede ver en la siguiente captura de pantalla, los nodos tienen forma redondeada, que es la interfaz de usuario antigua para recorridos del modelo v1.

![](assets/new-canvas.png)

Sin embargo, cuando **Crear un nuevo recorrido** o **duplicar uno existente**, será un recorrido v2.  Planeamos seguir admitiendo los recorridos de la versión 1 hasta que la mayoría de los clientes pasen a los recorridos de la versión 2.

El nuevo modelo de recorrido tiene una limitación: **no se pueden copiar y pegar actividades de un recorrido v1 en un v2 y viceversa**. Si desea hacerlo, le recomendamos que duplique el recorrido de la versión 1 para convertirlo en una versión 2 y, a continuación, copie las actividades.

En la siguiente captura de pantalla, puede ver la interfaz de usuario rediseñada para el lienzo de recorrido (solo disponible con el modelo v2):

![](assets/new-canvas2.png)

**Cualquier nueva función añadida al diseñador de recorridos (incluidos los informes en directo) solo estará disponible para los recorridos de la versión 2 a partir de este momento.**

## Diseño de lienzo de recorrido mejorado

Con el nuevo modelo de recorrido presentamos un nuevo y mejorado **IU del lienzo de recorrido**, que se adapta perfectamente al ecosistema de soluciones y aplicaciones de Adobe Experience Cloud, lo que ofrece una experiencia de usuario intuitiva y eficaz. Cualquier recorrido de la pila de la versión 2 se basará en ese nuevo diseño.

![](assets/new-canvas3.gif)

Las actividades ahora se representan mediante cuadros cuadrados con las siguientes capacidades:

* La primera línea que representa el tipo de actividad que a menudo se sobrescribe con información más contextual (p. ej.: en Audiencias leídas, contendrá el nombre de la audiencia seleccionada) o con una etiqueta personalizada si define una.
* La segunda línea siempre representa el tipo de actividad.

![](assets/new-canvas4.png)

Esta nueva interfaz de usuario mejora la legibilidad del lienzo de recorrido al proporcionar lo siguiente **etiquetas y tipos de actividades más claros**.

También permite al equipo de productos añadir más información en el lienzo con menos clics. Un ejemplo de &quot;más información&quot; sería la inclusión de informes en directo en el lienzo de recorrido, donde puede ver perfiles que entran y salen de sus actividades debido a errores.

![](assets/new-canvas5.png)


## Creación de informes en directo en el lienzo de recorrido

Junto con el diseño mejorado de lona de recorrido, estamos introduciendo la capacidad de ver **últimas 24 horas métricas de informes** (lo que se denomina creación de informes en directo) directamente en el lienzo de recorrido.

![](assets/new-canvas6bis.png)

Con cada recorrido en vivo del nuevo modelo, podrás ver, **en cada actividad**, el número de perfiles que ingresaron a esa actividad y el número que salieron debido a un error:

![](assets/new-canvas8.png)

<!--`
With every live journey on the new model, you will be able to see two types of "last 24 hours" reporting information:

* On a **new insert**, you will see:
    * The number of profiles that have been exported for audience-triggered journeys. You will see the number of profiles available in the last export job alongside the time when that export has been made.
    * The number of profiles who exited the journey
    * The percentage of errors
    ![](assets/new-canvas7.png)
* **On each activity**, you will see the number of profiles who entered that activity and the number who exited because of an error:
    ![](assets/new-canvas8.png)
-->

La interfaz de usuario se actualiza automáticamente cada minuto.

<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->
