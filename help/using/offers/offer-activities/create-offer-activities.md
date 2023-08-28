---
title: Crear decisiones
description: Aprenda a crear decisiones
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: fd035fdd956c76d9183acbd0dddf6462890c4f44
workflow-type: tm+mt
source-wordcount: '2164'
ht-degree: 2%

---

# Crear decisiones {#create-offer-activities}

Las decisiones son contenedores para sus ofertas que aprovecharán el motor de decisión de ofertas para elegir la mejor y ofrecerla, según el objetivo de la entrega.

➡️ [Aprenda a crear actividades de oferta en este vídeo](#video)

Se puede acceder a la lista de decisiones en la **[!UICONTROL Ofertas]** menú > **[!UICONTROL Decisiones]** pestaña. Los filtros están disponibles para ayudarle a recuperar decisiones según su estado o fechas de inicio y finalización.

![](../assets/activities-list.png)

Antes de crear una decisión, asegúrese de que los componentes siguientes se hayan creado en la Biblioteca de ofertas:

* [Ubicaciones](../offer-library/creating-placements.md)
* [Colecciones](../offer-library/creating-collections.md)
* [Ofertas personalizadas](../offer-library/creating-personalized-offers.md)
* [Ofertas de reserva](../offer-library/creating-fallback-offers.md)

## Creación de la decisión {#create-activity}

1. Acceda a la lista de decisiones y haga clic en **[!UICONTROL Crear decisión]**.

1. Especifique el nombre de la decisión.

1. Defina una fecha y una hora de inicio y finalización si es necesario y haga clic en **[!UICONTROL Siguiente]**.

   ![](../assets/activities-name.png)

1. Para asignar etiquetas de uso de datos personalizadas o principales a la decisión, seleccione **[!UICONTROL Administrar acceso]**. [Obtenga más información sobre el Control de acceso de nivel de objeto (OLAC)](../../administration/object-based-access.md)

## Definir ámbitos de decisión {#add-decision-scopes}

1. Seleccione una ubicación en la lista desplegable. Se añadirá al primer ámbito de decisión de la decisión.

   ![](../assets/activities-placement.png)

1. Clic **[!UICONTROL Añadir]** para seleccionar criterios de evaluación para esta ubicación.

   ![](../assets/activities-evaluation-criteria.png)

   Cada criterio consiste en una colección de ofertas asociada con una restricción de elegibilidad y un método de clasificación para determinar las ofertas que se mostrarán en la ubicación.

   >[!NOTE]
   >
   >Se requiere al menos un criterio de evaluación.

1. Seleccione la colección de ofertas que contiene las ofertas que se van a tener en cuenta y haga clic en **[!UICONTROL Añadir]**.

   ![](../assets/activities-collection.png)

   >[!NOTE]
   >
   >Puede hacer clic en **[!UICONTROL Abrir colecciones de ofertas]** para mostrar la lista de colecciones en una nueva pestaña, lo que le permite examinar las colecciones y las ofertas que contienen.

   La colección seleccionada se agrega a los criterios.

   ![](../assets/activities-collection-added.png)

1. Utilice el **[!UICONTROL Idoneidad]** para restringir la selección de ofertas para esta ubicación.

   Esta restricción se puede aplicar mediante una **regla de decisión**, o uno o varios **Audiencias de Adobe Experience Platform**. Ambos se detallan en [esta sección](../offer-library/add-constraints.md#segments-vs-decision-rules).

   * Para restringir la selección de las ofertas a los miembros de una audiencia de Experience Platform, seleccione **[!UICONTROL Audiencias]**, luego haga clic en **[!UICONTROL Añadir audiencias]**.

     ![](../assets/activity_constraint_segment.png)

     Añada una o varias audiencias desde el panel izquierdo y combínelas con el **[!UICONTROL Y]** / **[!UICONTROL O]** operadores lógicos.

     ![](../assets/activity_constraint_segment2.png)

     Aprenda a trabajar con audiencias en [esta sección](../../audience/about-audiences.md).

   * Si desea añadir una restricción de selección con una regla de decisión, utilice la variable **[!UICONTROL Regla de decisión]** y seleccione la regla que desee.

     ![](../assets/activity_constraint_rule.png)

     Obtenga información sobre cómo crear una regla de decisión en [esta sección](../offer-library/creating-decision-rules.md).

1. Al seleccionar públicos o reglas de decisión, puede ver información sobre los perfiles cualificados estimados. Clic **[!UICONTROL Actualizar]** para actualizar los datos.

   >[!NOTE]
   >
   >Las estimaciones de perfil no están disponibles cuando los parámetros de regla incluyen datos que no están en el perfil, como datos de contexto. Por ejemplo, una regla de idoneidad que requiere que el clima actual sea de ≥80 grados.

   ![](../assets/activity_constraint-estimate.png)

1. Defina el método de clasificación que desee utilizar para seleccionar la mejor oferta para cada perfil. [Más información](../offer-activities/configure-offer-selection.md).

   ![](../assets/activity_ranking-method.png)

   * De forma predeterminada, si pueden utilizarse varias ofertas para esta ubicación, la variable **[!UICONTROL Prioridad de ofertas]** Este método utiliza el valor definido en las ofertas: la oferta con la puntuación de prioridad más alta se envía al usuario.

   * Si desea utilizar una puntuación calculada específica para elegir qué oferta apta para enviar, seleccione **[!UICONTROL Fórmula]** o **[!UICONTROL modelo de IA]**. [Más información](../offer-activities/configure-offer-selection.md).

1. Clic **[!UICONTROL Añadir]** para definir más criterios para la misma ubicación.

   ![](../assets/activity_add-collection.png)

1. Cuando se añaden varios criterios, estos se evalúan en un orden específico. La primera colección que se añadió a la secuencia se evaluará primero, y así sucesivamente. [Más información](#evaluation-criteria-order)

   Para cambiar la secuencia predeterminada, puede arrastrar y soltar las colecciones para reordenarlas como desee.

   ![](../assets/activity_reorder-collections.png)

1. También puede evaluar varios criterios al mismo tiempo. Para ello, arrastre y suelte la colección encima de otra.

   ![](../assets/activity_move-collection.png)

   Ahora tienen el mismo rango y, por lo tanto, se evaluarán al mismo tiempo. [Más información](#evaluation-criteria-order)

   ![](../assets/activity_same-rank-collections.png)

1. Para agregar otra ubicación para sus ofertas como parte de esta decisión, utilice el **[!UICONTROL Nuevo ámbito]** botón. Repita los pasos anteriores para cada ámbito de decisión.

   ![](../assets/activity_new-scope.png)

   >[!NOTE]
   >
   >Al agregar varios ámbitos de decisión, el orden de los criterios de evaluación se verá afectado. [Más información](#multiple-scopes)

### Orden de criterios de evaluación {#evaluation-criteria-order}

Como se ha descrito anteriormente, un criterio de evaluación consta de una colección, restricciones de elegibilidad y un método de clasificación. Puede establecer el orden secuencial que desee para que se evalúen los criterios de evaluación, pero también puede combinar varios criterios de evaluación para que se evalúen juntos y no por separado.

#### Con un ámbito {#one-scope}

Dentro de un único ámbito de decisión, varios criterios y su agrupación determinan la prioridad de los criterios y la clasificación de las ofertas aptas. El primer criterio tiene la prioridad más alta y los criterios combinados dentro del mismo &quot;grupo&quot; tienen la misma prioridad.

Por ejemplo, tiene dos colecciones, una en los criterios de evaluación A y otra en los criterios de evaluación B. La solicitud es para que se devuelvan dos ofertas. Digamos que hay dos ofertas elegibles de los criterios de evaluación A y tres ofertas elegibles de los criterios de evaluación B.

* Si los dos criterios de evaluación son **sin combinar** y/o en orden secuencial (1 y 2), las dos ofertas aptas principales de los criterios de evaluación se devolverán en la primera fila. Si no hay dos ofertas aptas para los primeros criterios de evaluación, el motor de decisión pasará al siguiente criterio de evaluación en secuencia para encontrar tantas ofertas que aún se necesiten y, finalmente, devolverá una reserva si es necesario.

  ![](../assets/activity_consecutive-rank-collections.png)

* Si las dos colecciones son **evaluado al mismo tiempo** Sin embargo, como hay dos ofertas elegibles de los criterios de evaluación A y tres ofertas elegibles de los criterios de evaluación B, las cinco ofertas se apilarán en base al valor determinado por los métodos de clasificación respectivos. Se solicitan dos ofertas, por lo que se devolverán las dos ofertas aptas principales de estas cinco ofertas.

  ![](../assets/activity_same-rank-collections.png)

+++ **Ejemplo con varios criterios**

Veamos un ejemplo en el que tiene varios criterios para un único ámbito dividido en diferentes grupos.

Ha definido tres criterios. Los criterios 1 y 2 se combinan en el grupo 1 y el criterio 3 es independiente (grupo 2).

Las ofertas elegibles para cada criterio y su prioridad (utilizadas en la evaluación de la función de clasificación) son las siguientes:

* Grupo 1:
   * Criterios 1 - (Oferta 1, Oferta 2, Oferta 3) - Prioridad 1
   * Criterios 2 - (Oferta 3, Oferta 4, Oferta 5) - Prioridad 1

* Grupo 2:
   * Criterios 3 - (Oferta 5, Oferta 6) - Prioridad 0

Las ofertas de criterios de mayor prioridad se evalúan primero y se añaden a la lista de ofertas clasificadas.

**Iteración 1:**

Las ofertas de Criterios 1 y Criterio 2 se evalúan juntas (Oferta 1, Oferta 2, Oferta 3, Oferta 4, Oferta 5). Digamos que el resultado es:

Oferta 1 - 10 Oferta 2 - 20 Oferta 3 - 30 de Criterios 1, 45 de Criterios 2. Se tendrá en cuenta el más alto de ambos, por lo que se tienen en cuenta 45.
Oferta 4 - 40 Oferta 5 - 50

Las ofertas clasificadas ahora son las siguientes: Oferta 5, Oferta 3, Oferta 4, Oferta 2, Oferta 1.

**Iteración 2:**

Se evalúan las ofertas de Criterios 3 (oferta 5, oferta 6). Digamos que el resultado es:

* Oferta 5: no se evaluará porque ya existe en el resultado anterior.
* Oferta 6 - 60

Las ofertas clasificadas ahora son las siguientes: Oferta 5 , Oferta 3, Oferta 4, Oferta 2, Oferta 1, Oferta 6.

+++

#### Con varios ámbitos {#multiple-scopes}

**Si la duplicación está desactivada**

Cuando se agregan varios ámbitos de decisión a una decisión y no se permite la duplicación entre ubicaciones, las ofertas aptas se seleccionan secuencialmente en el orden de los ámbitos de decisión de la solicitud.

>[!NOTE]
>
>El **[!UICONTROL Permitir duplicados entre ubicaciones]** El parámetro se define en el nivel de ubicación. Si la duplicación se establece en &quot;False&quot; para cualquier ubicación en una solicitud de toma de decisiones, todas las ubicaciones de la solicitud heredarán la configuración &quot;False&quot;. [Más información sobre los parámetros de duplicación](../offer-library/creating-placements.md)

Veamos un ejemplo en el que agregó dos ámbitos de decisión como:

* Ámbito 1: hay cuatro ofertas aptas (Oferta 1, Oferta 2, Oferta 3, Oferta 4) y la solicitud es de dos ofertas para enviarse de vuelta.
* Ámbito 2: hay cuatro ofertas aptas (Oferta 1, Oferta 2, Oferta 3, Oferta 4) y la solicitud es de dos ofertas para enviarse de vuelta.

+++ **Ejemplo 1**

La selección es la siguiente:

1. Se devolverán las dos ofertas principales aptas del ámbito 1 (Oferta 1, Oferta 2).
1. Se devolverán las dos ofertas principales elegibles restantes del ámbito 2 (oferta 3, oferta 4).

+++

+++ **Ejemplo 2**

En este ejemplo, la oferta 1 ha alcanzado su límite de frecuencia. [Más información sobre la restricción de frecuencia](../offer-library/add-constraints.md#capping)

La selección es la siguiente:

1. Se devolverán las dos ofertas principales elegibles restantes del ámbito 1 (oferta 2, oferta 3).
1. Se devuelve la oferta elegible restante del ámbito 2 (oferta 4).

+++

+++ **Ejemplo 3**

En este ejemplo, la oferta 1 y la oferta 3 alcanzaron su límite de frecuencia. [Más información sobre la restricción de frecuencia](../offer-library/add-constraints.md#capping)

La selección es la siguiente:

1. Se devolverán las dos ofertas principales elegibles restantes del ámbito 1 (oferta 2, oferta 4).
1. No quedan ofertas elegibles para el ámbito 2, por lo que la variable [oferta de reserva](#add-fallback) se devuelve.

+++

**Si la duplicación está activada**

Cuando se permite la duplicación en todas las ubicaciones, la misma oferta se puede proponer varias veces en diferentes ubicaciones. Si se habilita, el sistema considerará la misma oferta para varias ubicaciones. [Más información sobre los parámetros de duplicación](../offer-library/creating-placements.md)

Veamos el mismo ejemplo que arriba, donde agregó dos ámbitos de decisión, como:

* Ámbito 1: hay cuatro ofertas aptas (Oferta 1, Oferta 2, Oferta 3, Oferta 4) y la solicitud es de dos ofertas para enviarse de vuelta.
* Ámbito 2: hay cuatro ofertas aptas (Oferta 1, Oferta 2, Oferta 3, Oferta 4) y la solicitud es de dos ofertas para enviarse de vuelta.

+++ **Ejemplo 1**

La selección es la siguiente:

1. Se devolverán las dos ofertas principales aptas del ámbito 1 (Oferta 1, Oferta 2).
1. Se devolverán las dos mismas ofertas principales aptas del ámbito 2 (Oferta 1, Oferta 2).

+++

+++ **Ejemplo 2**

En este ejemplo, la oferta 1 ha alcanzado su límite de frecuencia. [Más información sobre la restricción de frecuencia](../offer-library/add-constraints.md#capping)

La selección es la siguiente:

1. Se devolverán las dos ofertas principales elegibles restantes del ámbito 1 (oferta 2, oferta 3).

1. Se devolverán las dos ofertas principales elegibles restantes del ámbito 2 (oferta 2, oferta 3).

+++

+++ **Ejemplo 3**

En este ejemplo, la oferta 1 y la oferta 3 alcanzaron su límite de frecuencia. [Más información sobre la restricción de frecuencia](../offer-library/add-constraints.md#capping)

La selección es la siguiente:

1. Se devolverán las dos ofertas principales elegibles restantes del ámbito 1 (oferta 2, oferta 4).

1. Se devolverán las dos ofertas principales elegibles restantes del ámbito 2 (oferta 2, oferta 4).

+++

## Añadir una oferta de reserva {#add-fallback}

Una vez definidos los ámbitos de decisión, defina la oferta de reserva que se presentará como último recurso a los clientes que no coincidan con las restricciones y reglas de idoneidad de las ofertas.

Para ello, selecciónela en la lista de ofertas de reserva disponibles para las ubicaciones definidas en la decisión y, a continuación, haga clic en **[!UICONTROL Siguiente]**.

![](../assets/add-fallback-offer.png)

>[!NOTE]
>
>Puede hacer clic en **[!UICONTROL Abrir biblioteca de ofertas]** para mostrar la lista de ofertas en una nueva pestaña.

## Revisar y guardar la decisión {#review}

Si todo está configurado correctamente, se muestra un resumen de las propiedades de la decisión.

1. Asegúrese de que la decisión esté lista para utilizarse para presentar ofertas a los clientes. Se muestran todos los ámbitos de decisión y la oferta de reserva que contiene.

   ![](../assets/review-decision.png)

1. Puede expandir o contraer cada ubicación. Puede previsualizar las ofertas disponibles, los detalles de idoneidad y la clasificación de cada ubicación. También puede mostrar información sobre los perfiles cualificados estimados. Clic **[!UICONTROL Actualizar]** para actualizar los datos.

   ![](../assets/review-decision-details.png)

1. Haga clic en **[!UICONTROL Finalizar]**.
1. Seleccionar **[!UICONTROL Guardar y activar]**.

   ![](../assets/save-activities.png)

   También puede guardar la decisión como borrador para editarla y activarla más adelante.

La decisión se muestra en la lista con el **[!UICONTROL Activo]** o **[!UICONTROL Borrador]** estado, en función de si lo activó o no en el paso anterior.

Ahora está listo para utilizarse para entregar ofertas a los clientes.

## Lista de decisiones {#decision-list}

En la lista de decisiones, puede seleccionar la decisión para mostrar sus propiedades. Desde allí también puede editarlo, cambiar su estado (**Borrador**, **Activo**, **Completar**, **Archivado**), duplique la decisión o elimínela.

![](../assets/decision_created.png)

Seleccione el **[!UICONTROL Editar]** para volver al modo de edición de decisiones, donde puede modificar el [detalles](#create-activity), [ámbitos de decisión](#add-decision-scopes) y [oferta de reserva](#add-fallback).

>[!IMPORTANT]
>
>Si se realizan cambios en una decisión de oferta que se está utilizando en el mensaje de un recorrido, debe cancelar la publicación del recorrido y volver a publicarlo.  Esto garantizará que los cambios se incorporen al mensaje del recorrido y que el mensaje sea coherente con las últimas actualizaciones.

Seleccione una decisión activa y haga clic en **[!UICONTROL Desactivar]** para volver a establecer el estado de decisión en **[!UICONTROL Borrador]**.

Para volver a establecer el estado en **[!UICONTROL Activo]**, seleccione la **[!UICONTROL Activar]** botón que ahora se muestra.

![](../assets/decision_activate.png)

El **[!UICONTROL Más acciones]** habilita las acciones que se describen a continuación.

![](../assets/decision_more-actions.png)

* **[!UICONTROL Completar]**: establece el estado de la decisión en **[!UICONTROL Completar]**, lo que significa que ya no se puede tomar la decisión. Esta acción solo está disponible para decisiones activadas. La decisión aún está disponible en la lista, pero no puede volver a establecer su estado en **[!UICONTROL Borrador]** o **[!UICONTROL Aprobado]**. Solo puede duplicarlo, eliminarlo o archivarlo.

* **[!UICONTROL Duplicar]**: crea una decisión con las mismas propiedades, ámbitos de decisión y ofertas de reserva. De forma predeterminada, la nueva decisión tiene el **[!UICONTROL Borrador]** estado.

* **[!UICONTROL Eliminar]**: elimina la decisión de la lista.

  >[!CAUTION]
  >
  >Ya no se podrá acceder a la decisión ni a su contenido. No se puede deshacer esta acción.
  >
  >Si la decisión se utiliza en otro objeto, no se puede eliminar.

* **[!UICONTROL Archivar]**: establece el estado de la decisión en **[!UICONTROL Archivado]**. La decisión aún está disponible en la lista, pero no puede volver a establecer su estado en **[!UICONTROL Borrador]** o **[!UICONTROL Aprobado]**. Solo puede duplicarlo o eliminarlo.

También puede eliminar o cambiar el estado de varias decisiones al mismo tiempo seleccionando las casillas de verificación correspondientes.

![](../assets/decision_multiple-selection.png)

Si desea cambiar el estado de varias decisiones con diferentes estados, solo se cambiarán los estados relevantes.

![](../assets/decision_change-status.png)

Una vez creada una decisión, puede hacer clic en su nombre desde la lista.

![](../assets/decision_click-name.png)

Esto le permite acceder a información detallada para esa decisión. Seleccione el **[!UICONTROL Registro de cambios]** pestaña a [monitorizar todos los cambios](../get-started/user-interface.md#changes-log) que se han tomado en la decisión.

![](../assets/decision_information.png)

## Vídeo explicativo{#video}

Obtenga información sobre cómo crear actividades de oferta en administración de decisiones.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)


