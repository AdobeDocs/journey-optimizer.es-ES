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
source-git-commit: b6b3f710d08fb7f0949e75521ce126fa43d6cdc5
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 1%

---

# Bienvenido al Diseñador de Recorridos mejorado {#new-canvas}

Journey Optimizer ahora ofrece un **modelo de recorrido simplificado** que tiene como objetivo mejorar la experiencia del usuario y los procesos internos. A partir de la versión de abril, podrá beneficiarse de las siguientes funciones:

* A **lienzo de recorrido rediseñado** diseñado para una experiencia de interfaz de usuario modernizada
* A **live reporting** IU directamente disponible en el lienzo del recorrido

>[!NOTE]
>
>Tenga en cuenta que el despliegue de esta función será progresivo. Es posible que no vea los cambios de inmediato.

## Actualizaciones en el modelo de recorrido

El nuevo modelo de recorrido vivirá junto al existente, lo que significa que habrá recorridos utilizando **dos modelos diferentes**:

* El modelo heredado
* El nuevo modelo

Todos los recorridos del modelo heredado permanecerán en él. Aún puede editarlos, probarlos o publicarlos. Cualquier nueva versión creada a partir de un recorrido en el modelo heredado también permanecerá en él. No hay **sin cambios funcionales** alrededor de esos recorridos.

Como puede ver en la siguiente captura de pantalla, los nodos tienen forma redondeada, que es la interfaz de usuario antigua para recorridos en el modelo heredado.

![](assets/new-canvas.png)

Sin embargo, cuando **crear un nuevo recorrido** o **duplicar uno existente**, estará en el nuevo modelo. Los recorridos en el modelo heredado seguirán siendo compatibles hasta que la mayoría de los clientes pasen al nuevo.

El nuevo modelo de recorrido tiene una limitación: **no se pueden copiar y pegar actividades del modelo heredado en el nuevo y viceversa**. Si desea hacerlo, le recomendamos que duplique el recorrido heredado para cambiarlo al nuevo modelo y, a continuación, copie las actividades.

En la siguiente captura de pantalla, puede ver la interfaz de usuario rediseñada para el lienzo de recorrido (solo disponible con el nuevo modelo):

![](assets/new-canvas2.png)

**Cualquier nueva función añadida al diseñador de recorridos (incluidos los informes en directo) solo estará disponible para los recorridos del nuevo modelo a partir de este momento.**

## Diseño de lienzo de recorrido mejorado

Con el nuevo modelo de recorrido, presentamos un nuevo y mejorado **IU del lienzo de recorrido**, que se adapta perfectamente al ecosistema de soluciones y aplicaciones de Adobe Experience Cloud, lo que ofrece una experiencia de usuario intuitiva y eficaz. Cualquier recorrido en el nuevo modelo estará en ese nuevo diseño.

![](assets/new-canvas3.gif)

Las actividades ahora se representan mediante cuadros cuadrados con las siguientes capacidades:

* La primera línea que representa el tipo de actividad que a menudo se sobrescribe con información más contextual (en Leer audiencias, contendrá el nombre de la audiencia seleccionada) o con una etiqueta personalizada, si define una.
* La segunda línea siempre representa el tipo de actividad.

![](assets/new-canvas4.png)

Esta nueva interfaz de usuario mejora la legibilidad del lienzo de recorrido al proporcionar lo siguiente **etiquetas y tipos de actividades más claros**.

También permite al equipo de productos añadir más información en el lienzo con menos clics. Un ejemplo de &quot;más información&quot; sería la inclusión de informes en directo en el lienzo de recorrido, donde puede ver perfiles que entran y salen de sus actividades debido a errores.

![](assets/new-canvas5.png)


## Creación de informes en directo en el lienzo de recorrido

Además de la presentación mejorada del lienzo de recorrido, se está introduciendo una nueva función para permitir a los usuarios ver las métricas de informes en tiempo real de **las últimas 24 horas**, denominados informes en directo, directamente en el lienzo del recorrido.

Para cada actividad dentro de cada recorrido activo que utilice el nuevo modelo, tiene acceso a:

* Recuento de perfiles que entran en esta actividad.
* Recuento de perfiles que salen de esta actividad debido a un error.

![](assets/new-canvas6bis.png)

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
<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->
