---
solution: Journey Optimizer
product: journey optimizer
title: Actividad de decisión de contenido
description: Descubra más información sobre la actividad de decisión de contenido
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
badge: label="Disponibilidad limitada" type="Informative"
keywords: actividad, toma de decisiones, decisión de contenido, política de decisión, lienzo, recorrido
exl-id: 6188644a-6a3b-4926-9ae9-0c6b42c96bae
version: Journey Orchestration
source-git-commit: 74723337f97c8196b506ccc1ace11077710494ea
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 3%

---

# Actividad de decisión de contenido {#content-decision}

>[!AVAILABILITY]
>
>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una futura versión.

[!DNL Journey Optimizer] le permite incluir ofertas en sus recorridos a través de la actividad **decisión de contenido** específica en el lienzo de recorrido. A continuación, puede agregar otras actividades (como [acciones personalizadas](../action/about-custom-action-configuration.md)) a sus recorridos para dirigirse a sus audiencias con estas ofertas personalizadas.

>[!NOTE]
>
>La salida de una actividad de decisión de contenido no se puede utilizar en actividades de canal nativas.

Para aprovechar esta capacidad, cree un recorrido donde agregue una [actividad de decisión de contenido](#add-content-decision-activity) para definir las ofertas que desea presentar a los perfiles aptos.

A continuación, puede utilizar la salida de la actividad de decisión de contenido en:

* una [actividad de condición](#add-condition-activity), para mover perfiles a rutas específicas en función de las ofertas recuperadas;

* una [acción personalizada](#add-custom-action), donde puede enviar esas ofertas a sistemas externos.

## Configuración de una actividad de decisión de contenido {#add-content-decision-activity}

Con la actividad de decisión de contenido, puede definir una política de decisión que le permita elegir los mejores elementos de [!DNL Journey Optimizer] decisiones y enviarlos a la audiencia correcta.

<!--Their goal is to select the best offers for each profile, while the campaign/journey authoring allows you to indicate how the selected decision items should be presented, including which item attributes to be included in the message.-->

Para configurar la actividad **[!UICONTROL Decisión de contenido]**, siga los pasos a continuación.

1. Despliegue la categoría **[!UICONTROL Orchestration]** y suelte una actividad **[!UICONTROL Content decision]** en el lienzo.

   ![Agregar una decisión de contenido al recorrido](assets/journey-content-decision.png){width=100%}

1. De forma opcional, añada una etiqueta y una descripción a la actividad.

1. Haga clic en **[!UICONTROL Agregar directiva de decisión]**. [Más información sobre las políticas de decisión](../experience-decisioning/create-decision.md)

   >[!NOTE]
   >
   >Los permisos de toma de decisiones son necesarios para crear una directiva de decisión. [Más información](../experience-decisioning/gs-experience-decisioning.md#steps)

1. Seleccione el número de elementos que desea que se devuelvan. Por ejemplo, si selecciona 2, se presentarán las 2 mejores ofertas aptas. Haga clic en **[!UICONTROL Next]**.

1. En la sección **[!UICONTROL Secuencia de estrategia]**, seleccione los elementos de decisión y/o las estrategias de selección que desea presentar con la directiva de decisión. [Más información](../experience-decisioning/create-decision.md#select)

1. Organice el orden de evaluación según sea necesario.

   Al agregar varios elementos de decisión y/o estrategias, se evalúan en orden secuencial, indicados con números a la izquierda de cada objeto o grupo de objetos. Para cambiar la secuencia predeterminada, puede arrastrar y soltar los objetos o los grupos para reordenarlos como desee. [Más información](../experience-decisioning/create-decision.md#evaluation-order)

1. (opcional) Añada una oferta de reserva. [Más información](../experience-decisioning/create-decision.md#fallback)

1. Revise y guarde la directiva de decisión.

   ![Resumen de directivas de decisión](assets/journey-content-decision-policy.png){width=70%}<!--reshoot or change screen-->

Ya está listo para aprovechar el resultado de esta actividad de decisión de contenido en su recorrido.

## Mecanismos de protección y limitaciones {#guardrails}

**Políticas de consentimiento**

Las actualizaciones de las directivas de consentimiento tardan hasta 48 horas en surtir efecto. Si una directiva de decisión hace referencia a un atributo vinculado a una directiva de consentimiento actualizada recientemente, los cambios no se aplican inmediatamente.

Del mismo modo, si se añaden nuevos atributos de perfil sujetos a una directiva de consentimiento a una directiva de decisión, se pueden utilizar, pero la directiva de consentimiento asociada a ellos no se aplicará hasta que haya pasado el retraso.

Las políticas de consentimiento solo están disponibles para las organizaciones con el complemento Adobe Healthcare Shield o Privacy and Security Shield.

## Usar la salida de la actividad de decisión de contenido {#use-content-decision-output}

El resultado de una decisión de contenido se puede utilizar en varias actividades de recorrido. Por ejemplo, puede usar una [actividad de condición](#add-condition-activity) para mover perfiles a ramas específicas del recorrido, según el número de ofertas recuperadas para ellas.

También puede agregar una [acción personalizada](#add-custom-action) al recorrido para compartir las ofertas de la actividad de decisión de contenido con un sistema externo.

### En una actividad de condición {#add-condition-activity}

Para aprovechar el resultado de una actividad de decisión de contenido, puede agregar una condición al recorrido, donde define expresiones para mover perfiles a rutas específicas, utilizando datos de esas ofertas. Siga los pasos a continuación.

1. Desde la categoría **[!UICONTROL Orchestration]**, suelte una actividad **[!UICONTROL Condition]** en el lienzo. [Más información](condition-activity.md#add-condition-activity)

1. (opcional) Cambie el nombre de **[!UICONTROL Path1]**, que corresponde a la primera expresión que defina, por una etiqueta más relevante.

1. Para esta primera ruta, haga clic dentro del campo **[!UICONTROL Expression]** o use el icono Editar para agregar una expresión.

   ![Agregue una condición y edite la expresión](assets/journey-content-decision-condition.png){width=80%}

1. En la ventana emergente que se abre, cambie a **[!UICONTROL Modo avanzado]** para usar el [editor de expresiones avanzadas](expression/expressionadvanced.md).

   >[!CAUTION]
   >
   >El resultado de un nodo de decisión de contenido solo está disponible en **[!UICONTROL modo avanzado]**.

1. Despliegue el nodo **[!UICONTROL Context]** y vaya a la directiva de decisiones para mostrar todos los atributos disponibles en el esquema de [catálogo de ofertas](../experience-decisioning/catalogs.md#access-catalog-schema).

   ![Agregue una condición y edite la expresión](assets/journey-content-decision-context.png)

   >[!NOTE]
   >
   >Cualquier etiqueta restringida definida en un atributo, ya sea en un evento de experiencia de recorrido utilizado en una regla de decisión (como datos de contexto) o en el esquema de [ofertas](../experience-decisioning/catalogs.md#access-catalog-schema), produce una infracción de directiva para DULE o para el consentimiento. Obtenga más información sobre las directivas de gobernanza de datos en [esta sección](../action/action-privacy.md)

1. Para comprobar si se ha devuelto alguna oferta para los perfiles que entran en el recorrido, use la función [listSize](functions/list-functions.md#listSize) con la siguiente sintaxis: `listSize(@decision{ContentdecisionName.items})>0`

   >[!NOTE]
   >
   >En este ejemplo, `Name` es la etiqueta de la decisión de contenido que agregó a su recorrido.

   ![Agregar una condición con la lista](assets/journey-content-decision-condition-list.png)

1. Haga clic en **[!UICONTROL Ok]**.

1. Añada más rutas para definir otras condiciones según sea necesario.

   También puede crear otra ruta de acceso para perfiles que no cumplan la primera condición marcando **[!UICONTROL Mostrar ruta de acceso para otros casos que no sean los anteriores]**. <!--These profiles will then exit the journey if no other activity is added in that path.-->

1. Guarde la actividad de condición.

### En una acción personalizada {#add-custom-action}

Para aprovechar el resultado de una actividad de decisión de contenido, puede agregar una acción personalizada al recorrido, en la que compartirá las ofertas definidas en un sistema externo. Siga los pasos a continuación.

1. Añada una acción personalizada al recorrido. [Más información](../action/about-custom-action-configuration.md)

1. Introduzca una etiqueta para la acción.

1. En la sección **[!UICONTROL Parámetros de solicitud]**, seleccione el parámetro que desee asignar a atributos de las ofertas que se han recuperado.

   Haga clic dentro del campo de texto editable y seleccione cualquier parámetro que desee asignar a atributos de las ofertas recuperadas.

   ![Editar los parámetros de solicitud de la acción personalizada](assets/journey-content-decision-custom-action-param.png)

1. Cambie a **[!UICONTROL Modo avanzado]** en la ventana emergente que se abre. En el [editor de expresiones avanzadas](expression/expressionadvanced.md), despliegue el nodo **[!UICONTROL Contexto]** para mostrar todos los elementos de la directiva de decisión.

   >[!CAUTION]
   >
   >El resultado de un nodo de decisión de contenido solo está disponible en **[!UICONTROL modo avanzado]**.

1. Examine el esquema [ofertas del catálogo](../experience-decisioning/catalogs.md#access-catalog-schema) mediante la matriz `items`. Por ejemplo, use `itemName` de la primera oferta recuperada y `itemName` de la segunda oferta recuperada.

   ![Parámetros de solicitud de acción personalizada que incluyen la directiva de decisión](assets/journey-content-decision-custom-action-param-ex.png)

1. Haga clic en **[!UICONTROL Aceptar]** para guardar la expresión.

1. **[!UICONTROL Guarde]** su configuración de acción personalizada.

### Ejemplo de extremo a extremo {#use-case}

A continuación se muestra el ejemplo completo de un recorrido que utiliza una actividad de decisión de contenido combinada con una actividad de condición y una acción personalizada, como se ha descrito anteriormente.

![recorrido completo](assets/journey-content-decision-full-journey.png)

<!--When all activities are properly configured and saved, [publish](publish-journey.md) your journey.-->

Una vez que el recorrido esté [activado](publish-journey.md):

<!--* Profiles who enter the journey and are eligible for at least one offer are targeted by the custom action.

* If no offer is returned for a profile, they are excluded from the custom action.-->

1. Cada vez que un perfil se califica para esa audiencia, entra en el recorrido.

1. A través de la actividad de decisión de contenido, [!DNL Journey Optimizer] recupera las ofertas relevantes para cada perfil.

1. Solo los perfiles para los que se ha recuperado al menos una oferta continúan la recorrido (a través de la ruta Perfiles aptos ).

1. Si se cumple la condición, las ofertas correspondientes se envían a un sistema externo a través de la acción personalizada.
