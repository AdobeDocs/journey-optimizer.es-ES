---
title: Administración de conflictos y priorización
description: Obtenga información sobre cómo previsualizar y probar el contenido.
feature: Preview, Proofs
role: User
level: Beginner
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 0322a13304875c4ba9ae8a9e7710fa2e71e459b3
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 26%

---


# Administración de conflictos y priorización {#conflict-prioritization}

>[!AVAILABILITY]
>
>Actualmente, las herramientas de administración de conflictos y priorización solo están disponibles como una versión beta para usuarios seleccionados.

En Journey Optimizer, administrar el volumen y el tiempo de las campañas y los recorridos es esencial para evitar abrumar a los clientes con demasiadas interacciones. Las dos secciones siguientes presentan herramientas clave para ayudarle a mantener el equilibrio y priorizar las comunicaciones de forma eficaz.

## Ver posibles conflictos en recorridos y campañas {#conflict}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_conflict"
>title="Visualizador de conflictos en campañas"
>abstract="Esta herramienta puede ayudarle a determinar la superposición con otros recorridos, campañas o configuraciones de canal. Si desea identificar superposiciones en público, fecha de inicio y de finalización, configuración de canal, canal o el conjunto de reglas, puede ver posibles conflictos aquí."

>[!CONTEXTUALHELP]
>id="ajo_journey_conflict"
>title="Visualizador de conflictos en recorridos"
>abstract="Esta herramienta puede ayudarle a determinar la superposición con otros recorridos, campañas o configuraciones de canal. Si desea identificar superposiciones en público, fecha de inicio y de finalización, configuración de canal, canal o el conjunto de reglas, puede ver posibles conflictos aquí."

A medida que los especialistas en marketing aumentan el volumen de campañas y Recorridos en Journey Optimizer, se hace cada vez más difícil para un experto en marketing saber si está bombardeando a sus clientes con demasiadas interacciones de marketing. por lo tanto, es esencial identificar fácilmente cuándo hay campañas y recorridos superpuestos para garantizar que logren el equilibrio adecuado en las comunicaciones de marketing y, al mismo tiempo, mitigar el riesgo de fatiga de los clientes.

Las áreas clave para monitorizar la posible superposición son las siguientes:

* **Cronología** (fechas de inicio y finalización): ¿se están ejecutando demasiados recorridos simultáneamente?
* **Audiencia**: ¿Qué porcentaje de mi audiencia de recorrido también es parte de otros recorridos?
* **Canal**: ¿Hay otras comunicaciones programadas para el mismo periodo de tiempo y, si es así, cuántas?
* **Conjunto de reglas de límite**: ¿Qué tipos de recorridos limito y hay superposición dentro de ellos?
* **Configuración del canal**: ¿Hay otros recorridos o campañas que usen esta configuración de canal y que podrían impedir que se muestre esta campaña al usuario?

Journey Optimizer le permite comprobar si hay alguna posibilidad de superposición con otros recorridos o campañas. Para ello, siga estos pasos:

1. En el momento de crear un recorrido o una campaña, haga clic en el botón **[!UICONTROL Ver conflictos potenciales]** en las propiedades del recorrido o de la campaña.

   ![](assets/view-conflicts.png)

   >[!NOTE]
   >
   >El botón **[!UICONTROL Ver conflictos potenciales]** está disponible para su selección en cuanto se asigne cualquiera de las siguientes opciones de configuración: **[!UICONTROL Fecha de inicio/finalización]**, **[!UICONTROL Audiencia]**, **[!UICONTROL Canal]**, **[!UICONTROL Configuración de canal]** y **[!UICONTROL Conjunto de reglas]**. Asegúrese de seleccionar **[!UICONTROL Guardar]** después de asignar esta configuración, ya que el botón no se podrá seleccionar hasta que se guarden los cambios.

1. Se abre la ventana **[!UICONTROL Potential conflicts]**, que le permite visualizar todos los elementos que se superponen con el recorrido o la campaña actual.

   Puede abrir un recorrido o una campaña superpuestos directamente desde esta pantalla seleccionando su nombre.

   ![](assets/potential-conflicts.png)

>[!NOTE]
>
>Para restringir aún más la búsqueda de posibles superposiciones, puede filtrar la lista de campañas y recorridos en función de los campos que sean relevantes. Para ello, seleccione el icono de filtro en la vista de inventario. [Aprenda a trabajar con filtros](../start/search-filter-categorize.md#filter-lists)

Una vez identificadas las posibles superposiciones, Journey Optimizer proporciona varias formas de solucionarlas.

* Ajuste las **fechas de inicio y finalización** para evitar campañas o recorridos superpuestos.
* Restrinja **la segmentación de audiencia** para minimizar la superposición entre recorridos.
* Implemente **límites de frecuencia** para evitar que los clientes reciban demasiadas comunicaciones.
* Reduzca la cantidad de **recorridos activos** para administrar la experiencia del cliente de manera más efectiva.
* Establezca **prioridades** en las acciones entrantes para asegurarse de que se muestre la acción más importante a los clientes.

Al aprovechar estas capacidades, puede asegurarse de que los esfuerzos de marketing estén alineados y de que mantiene el equilibrio adecuado en su estrategia de comunicaciones.

## Asignar puntuaciones de prioridad a recorridos y campañas {#priority}

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Prioridad"
>abstract="Asigne una puntuación de prioridad de recorrido comprendida entre 0 y 100. Un número mayor indica una prioridad mayor. El valor de prioridad insertado aquí lo heredan las acciones entrantes (como in-app) contenidas en este recorrido. En el caso de situaciones en las que esta misma configuración de canal entrante se utiliza en otras campañas o recorridos, se muestra al destinatario la acción entrante con la puntuación de prioridad más alta. Si varios recorridos o campañas tienen la misma puntuación, se elige el elemento que se ha modificado más recientemente."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Prioridad"
>abstract="Asigne una puntuación de prioridad a la campaña, de 0 a 100. Un número mayor indica una prioridad mayor. En el caso de situaciones en las que esta misma configuración de canal entrante (como in-app) se utiliza en otras campañas o recorridos, se muestra al destinatario la acción entrante con la puntuación de prioridad más alta. Si varios recorridos o campañas tienen la misma puntuación, se elige el elemento que se ha modificado más recientemente."

Journey Optimizer le permite asignar una puntuación de prioridad a un recorrido o campaña. La prioridad es esencial para priorizar un recorrido, una campaña o una acción cuando hay una restricción impuesta (como un límite de frecuencia). En situaciones en las que un cliente cumple los requisitos para muchos recorridos, campañas o comunicaciones y desea ser selectivo sobre qué debe introducir y recibir, debe utilizar este campo.

>[!NOTE]
>
>La puntuación de prioridad está disponible para canales entrantes: canales web, en la aplicación y basados en código. En recorrido, la puntuación de prioridad solo está disponible para los canales **en la aplicación** y **basados en código**.

Asignar una puntuación de prioridad es crucial para la comunicación entrante, como web, móvil y en la aplicación. Si tiene varias campañas con la misma configuración de canal (por ejemplo, un banner en la parte superior de la página web), esto podría resultar problemático, ya que solo se puede mostrar contenido de una campaña de forma factible. La puntuación de prioridad es donde insertará su preferencia para la campaña que debe mostrarse cuando el destinatario pueda cumplir los requisitos para más de una campaña.

Para asignar una puntuación de prioridad a un recorrido o campaña, escriba un valor numérico (de 0 a 100) en el campo **[!UICONTROL Puntuación de prioridad]** ubicado en las propiedades de recorrido o campaña. Tenga en cuenta que, cuanto mayor sea el número, mayor será la prioridad. Si fuera el autor de esta campaña y quisiera asegurarse de que se muestra su contenido, le daría una puntuación de 100.

![](assets/priority-score.png)

En situaciones en las que dos campañas tienen la misma puntuación de prioridad, se muestra la campaña activada menos recientemente.
