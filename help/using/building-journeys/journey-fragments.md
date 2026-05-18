---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos de recorrido
description: Aprenda a crear y utilizar fragmentos de recorrido para guardar y reutilizar conjuntos de nodos de recorrido en varios recorridos en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: fragmentos, recorrido, reutilizar, nodos, lienzo, inventario, reutilizable
badge: label="Disponibilidad limitada" type="Informative"
version: Journey Orchestration
source-git-commit: 5e806bf6931a5c067adde232f61ff446bee18cca
workflow-type: tm+mt
source-wordcount: '1484'
ht-degree: 9%

---


# Fragmentos de recorrido {#journey-fragments}

>[!AVAILABILITY]
>Actualmente, esta capacidad está en disponibilidad limitada. Para solicitar acceso, póngase en contacto con su representante de Adobe.

Los fragmentos de recorrido son conjuntos reutilizables de nodos de recorrido que puede generar una vez y soltarlos en cualquier recorrido de la zona protegida. Tanto si se trata de una comprobación de elegibilidad, una lógica de enrutamiento de canal preferida o una secuencia de bienvenida, los fragmentos ayudan a los equipos a moverse más rápido y a mantener la coherencia, sin volver a crear la misma lógica desde cero cada vez. [Vea ejemplos de casos de uso.](#examples)

Una vez creados, los fragmentos se almacenan en un **[!UICONTROL inventario de fragmentos]** específico y se pueden insertar en cualquier recorrido mediante la actividad **[!UICONTROL fragmentos de Recorrido]**.

>[!NOTE]
>los fragmentos de recorrido usan un **comportamiento de copia**: al insertar un fragmento en un recorrido, se crea una copia estática de los nodos originales. Las actualizaciones realizadas en el fragmento original no se reflejan en los recorridos que ya lo han utilizado.

## Permisos {#journey-fragments-permissions}

Para trabajar con fragmentos de recorrido, necesita los siguientes [permisos](../administration/permissions.md):

* **Administrar Recorridos**: necesario para crear, editar y eliminar fragmentos.
* **Publicar Recorridos**: necesario para activar un fragmento.

## Acceso al inventario de fragmentos {#journey-fragments-inventory}

Se puede acceder a los fragmentos de recorrido desde la sección **[!UICONTROL Recorridos]**. Abra la pestaña **[!UICONTROL Fragmentos]** para examinar todos los fragmentos disponibles en la zona protegida.

Puede filtrar la lista por nombre de fragmento, estado, fecha de creación, creador, fecha de última modificación o etiqueta.

## Crear un fragmento de recorrido {#create-journey-fragment}

>[!CONTEXTUALHELP]
>id="ajo_journey_fragment_create_canvas"
>title="Guardar como fragmento de recorrido"
>abstract="Introduzca un nombre único para el fragmento y haga clic en Guardar. Los nodos seleccionados se guardarán como un fragmento reutilizable disponible en el inventario de fragmentos."

Puede crear un fragmento de recorrido de dos formas: directamente desde el lienzo de recorrido (recomendado) o desde el inventario de fragmentos.

>[!BEGINTABS]

>[!TAB Desde el lienzo de recorrido]

Para guardar nodos de recorrido como un fragmento directamente desde el lienzo de recorrido:

1. Abra un recorrido y seleccione uno o varios nodos conectados en el lienzo.
1. Haga clic en el icono **[!UICONTROL Guardar como fragmento]** de la barra de herramientas.

   ![Icono para insertar un fragmento de recorrido](assets/journey-fragment-icon.png)

1. Introduzca un nombre único para el fragmento dentro de la zona protegida.

   ![Guardar nodos como un fragmento desde el lienzo de recorrido](assets/journey_fragment_create_canvas.png)

1. Haga clic en **[!UICONTROL Guardar]**. El fragmento se guardará como borrador.

>[!TIP]
>
>Si crea un fragmento a partir de un recorrido, [pruebe o simule su recorrido](testing-the-journey.md) **antes** de guardar el fragmento para asegurarse de que los nodos seleccionados se comportan según lo esperado.

>[!TAB Del inventario de fragmentos]

Para crear un fragmento directamente desde el inventario:

1. Vaya a **[!UICONTROL Recorridos]** > **[!UICONTROL Fragmentos de Recorrido]** en la pestaña.
1. Haga clic en **[!UICONTROL Crear fragmento de recorrido]**.
1. En el lienzo de creación de fragmentos, añada y configure actividades de recorrido.
1. Cuando termine, haga clic en **[!UICONTROL Guardar]** para guardar el fragmento como borrador.

>[!CAUTION]
>
>El modo de prueba y la simulación no están disponibles en el editor de fragmentos. Esto significa que no puede validar el comportamiento de las actividades configuradas antes de activar el fragmento e insertarlo en un recorrido. En el caso de los fragmentos en los que la precisión lógica es crítica, considere primero [crear y probar o simular los nodos en un recorrido completo](testing-the-journey.md) y, a continuación, guárdelos como un fragmento desde la pestaña de lienzo de arriba.

>[!ENDTABS]

## Edición de un fragmento {#edit-journey-fragment}

>[!CONTEXTUALHELP]
>id="ajo_journey_fragment_properties"
>title="Propiedades del fragmento de recorrido"
>abstract="Abra un fragmento del inventario para modificar sus nodos, propiedades, etiquetas o etiquetas. Los fragmentos activos deben desactivarse para poder editarlos."

Para editar un fragmento, ábralo desde el **[!UICONTROL Inventario de fragmentos]** haciendo clic en su nombre. En la IU de creación de fragmentos puede hacer lo siguiente:

* Agregar, quitar o modificar actividades.
* Establezca o actualice las propiedades del fragmento: nombre, etiquetas y etiquetas.

>[!NOTE]
>
>* Solo se pueden editar fragmentos de **[!UICONTROL Borrador]**. Para modificar un fragmento **[!UICONTROL Activo]**, desactívelo primero.
>
>* El modo de prueba y la simulación no están disponibles en el editor de fragmentos. Pruebe o simule cualquier lógica de nivel de recorrido en el recorrido completo antes de guardar nodos como un fragmento.
>
>* No se permiten actividades [Jump](jump.md) dentro de un fragmento.

## Administrar sus fragmentos {#manage-journey-fragments}

### Estados de fragmento {#fragment-statuses}

Los fragmentos de recorrido siguen un ciclo vital con los siguientes estados:

| Estado | Descripción |
|---|---|
| **[!UICONTROL Borrador]** | El fragmento se está creando y aún no está disponible para su uso en recorridos. |
| **[!UICONTROL Activo]** | El fragmento está listo para utilizarse en recorridos. |
| **[!UICONTROL Archivado]** | El fragmento se ha archivado y ya no está disponible para su uso en recorridos. |

Las siguientes reglas se aplican a las transiciones de estado de fragmento:

* Solo se pueden activar los fragmentos **[!UICONTROL Borrador]**. Abra un fragmento de borrador y use el icono **[!UICONTROL Activar]**.
* Solo se pueden desactivar o archivar **[!UICONTROL fragmentos activos]**.
* Solo se pueden desarchivar **[!UICONTROL fragmentos archivados]**. Al desarchivar un fragmento, se devuelve al estado **[!UICONTROL Borrador]**.
* Solo se pueden eliminar **[!UICONTROL Borradores]** fragmentos.

>[!NOTE]
>Al activar un fragmento, se aplican la mayoría de las mismas comprobaciones de validación que se ejecutan durante la publicación del recorrido. Sin embargo, **los atributos contextuales no se validan** y las **directivas de gobernanza no se aplican** en el momento de la activación; ambas se evalúan cuando el fragmento se inserta y se utiliza en un recorrido.

### Acciones de fragmento {#fragment-actions}

Desde el inventario de fragmentos, puede realizar las siguientes acciones en un fragmento:

* **[!UICONTROL Abrir]**: edite el fragmento haciendo clic en su nombre.
* **[!UICONTROL Duplicado]**: cree una copia del fragmento a partir de **[!UICONTROL Más acciones]** (...) icono.
* **[!UICONTROL Archivar]**: archivar un fragmento (disponible solo para **[!UICONTROL fragmentos activos]**), de **[!UICONTROL Más acciones]** (...) icono. Los fragmentos archivados ya no están disponibles en el selector de fragmentos.
* **[!UICONTROL Desarchivar]**: restaure un fragmento archivado (disponible solo para **[!UICONTROL Fragmentos archivados]**), a partir de **[!UICONTROL Más acciones]** (...) icono. El fragmento vuelve al estado **[!UICONTROL Borrador]**.
* **[!UICONTROL Eliminar]**: elimine permanentemente un fragmento (disponible solo para **[!UICONTROL Borrador]** fragmentos), de **[!UICONTROL Más acciones]** (...) icono.
* **[!UICONTROL Editar etiquetas]**: agregue o quite etiquetas de un fragmento, de las **[!UICONTROL acciones más]** (...) icono.

## Uso de un fragmento en un recorrido {#use-journey-fragment}

>[!CONTEXTUALHELP]
>id="ajo_journey_fragment_add"
>title="Añadir un fragmento de recorrido"
>abstract="Solo los fragmentos **[!UICONTROL activos]** están disponibles en el selector. Al insertar un fragmento, se crea una **copia estática** de sus nodos — las actualizaciones del fragmento original no se reflejan en el recorrido."

Para insertar un fragmento en un recorrido:

1. Abra el recorrido y arrastre la actividad **[!UICONTROL fragmentos de Recorrido]** desde el carril izquierdo.
1. Colóquelo en una rama existente o en un lienzo vacío. Aparecerá un selector de fragmentos.
1. Busque el fragmento que desee utilizar o haga una búsqueda. Puede obtener una vista previa de un fragmento o abrirlo en otra pestaña antes de insertarlo.
1. Seleccione el fragmento. Sus nodos se copian en el lienzo en el punto de colocación.

>[!NOTE]
>Solo los fragmentos **[!UICONTROL activos]** están disponibles en el selector. Al insertar un fragmento, se crea una **copia estática** de sus nodos; las actualizaciones posteriores del fragmento original no se reflejarán en el recorrido.
>
>Al soltar un fragmento en un lienzo vacío, el fragmento debe comenzar con un nodo **[!UICONTROL Leer audiencia]**, **[!UICONTROL Calificación de audiencias]** o **[!UICONTROL Evento]** (la misma regla que al iniciar cualquier recorrido).

## Mecanismos de protección y limitaciones {#guardrails}

Las siguientes protecciones se aplican a los fragmentos de recorrido:

**Creación de fragmentos**

* Los nombres de fragmento deben ser **únicos por zona protegida**.
* Un fragmento solo puede tener **una ruta de acceso de entrada**. Las selecciones con más de un punto de entrada no se pueden guardar como un fragmento.
* Solo **nodos conectados** se pueden guardar juntos como un fragmento.
* Un fragmento **no puede contener una actividad [Jump](jump.md)**.
* Un fragmento puede contener **un máximo de 20 nodos**.
* Una zona protegida puede tener un máximo de **200 fragmentos activos**.

**Uso del fragmento**

* Solo se pueden insertar **[!UICONTROL fragmentos activos]** en un recorrido.
* Al insertar un fragmento, se crea una **copia estática** de sus nodos. Las actualizaciones del fragmento original no se propagan a los recorridos en los que se ha utilizado.
* Un fragmento se puede soltar en una rama existente o en un lienzo vacío. Cuando se coloca en un lienzo vacío, el fragmento debe comenzar con un nodo **[!UICONTROL Leer audiencia]**, **[!UICONTROL Calificación de audiencias]** o **[!UICONTROL Evento]**.

**General**

* Los fragmentos se pueden encontrar usando la barra [Búsqueda unificada](../start/search-filter-categorize.md) en la categoría **[!UICONTROL Fragmentos de Recorrido]**.
* [Etiquetas](tags.md) y **Etiquetas** son compatibles con los fragmentos.
* Se admiten [registros de auditoría](../privacy/audit-logs.md).
* Los recorridos que se ejecutan en la pila antigua (con campañas en línea) no admiten fragmentos de recorrido. Duplique un recorrido de este tipo para pasar a la nueva pila antes de utilizar esta función.

## Ejemplos de casos de uso {#examples}

Los siguientes ejemplos ilustran patrones de recorrido comunes que se pueden guardar y reutilizar como fragmentos de recorrido.

**Comprobaciones de idoneidad**

Un patrón de entrada estándar (como un nodo [Leer audiencia](read-audience.md) seguido de filtros de elegibilidad) se puede encapsular en un fragmento. Esto permite a los equipos mantener la coherencia en la forma en que los perfiles introducen recorridos, a la vez que reducen el tiempo de configuración. El fragmento puede ser solo la actividad [Optimize](optimize.md) o la actividad Read Audience and Optimize juntas.

![Ejemplo de fragmento de comprobación de idoneidad](assets/journey-fragments-uc-eligibility-check.png)

**Canal preferido**

Un fragmento puede evaluar el canal de comunicación preferido de un perfil (correo electrónico, push o SMS) y enrutar el perfil en consecuencia. Esta lógica se puede reutilizar en cualquier recorrido que implique mensajes salientes, lo que garantiza una administración coherente de las preferencias de canal. El fragmento puede incluir la actividad [Optimizar](optimize.md) y las tres ramas de canal.

![Ejemplo de fragmento de canal preferido](assets/journey-fragments-uc-preferred-channel.png)

**Secuencia de bienvenida de incorporación**

Una secuencia de bienvenida temporizada, como una serie de tres mensajes que presentan un producto o servicio, se puede guardar como un fragmento. Esto resulta útil para incorporar nuevos usuarios en diferentes segmentos de audiencia o líneas de productos. El fragmento puede incluir las actividades [Wait](wait-activity.md) y los nodos de mensajes.

![Ejemplo de fragmento de secuencia de bienvenida de incorporación](assets/journey-fragments-uc-welcome-sequence.png)

**Espera y recordatorio basados en reacciones**

Un fragmento puede encapsular una actividad de correo electrónico seguida de una [reacción](reaction-events.md), esperando a que el perfil abra el correo electrónico en un número determinado de días y enviando un recordatorio si no lo hicieron. Esta lógica se reutiliza comúnmente en los recorridos de nutrición y en los flujos de conversión de prueba. El fragmento puede incluir las actividades Correo electrónico y Reacción.

![Ejemplo de fragmento de recordatorio basado en reacciones](assets/journey-fragments-uc-reminder.png)
