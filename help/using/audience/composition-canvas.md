---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con el lienzo de composición
description: Aprenda a trabajar con el lienzo de composición
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 3eb9466e-9d88-4470-a22f-5e24a29923ae
badge: label="Beta" type="Informative"
source-git-commit: 6f6fd6c032be7f86dca239d43732f3ab37223093
workflow-type: tm+mt
source-wordcount: '1345'
ht-degree: 24%

---

# Trabajo con el lienzo de composición {#composition-canvas}

Composición de audiencia proporciona un lienzo visual que le permite crear audiencias y utilizar varias actividades (dividir, enriquecer, etc.).

Los pasos para componer una audiencia en el lienzo son los siguientes:

1. [Definición de la audiencia o audiencias de inicio](#starting-audience)
1. [Añada una o varias actividades](#action-activities)
1. [Guardar los resultados en una audiencia nueva](#save)

## Selección de la audiencia inicial {#starting-audience}

El primer paso para crear una composición es seleccionar una o varias audiencias existentes como base de la composición.

1. Seleccione el **[!UICONTROL Audiencia]** a continuación, proporcione una etiqueta para la actividad.

1. Elija la audiencia a la que desee dirigirse:

   * Haga clic en **[!UICONTROL Añadir audiencia]** para seleccionar una o varias audiencias existentes,
   * Haga clic en **[!UICONTROL Generar regla]** para crear una nueva definición de audiencia con el botón [Servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

   ![](assets/audiences-choose-audience.png)

1. Si se seleccionan varias audiencias, especifique cómo se deben combinar los perfiles de estas audiencias:

* **[!UICONTROL Union]**: incluir todos los perfiles de las audiencias seleccionadas,
* **[!UICONTROL Intersección]**: incluye perfiles que son comunes a todas las audiencias seleccionadas.
* **[!UICONTROL Excluir superposición]**: incluye perfiles que pertenecen a una de las audiencias solamente. No se incluirán los perfiles que pertenezcan a más de una audiencia.

En este ejemplo, queremos segmentar todos los perfiles pertenecientes a las audiencias oro y plata.

![](assets/audiences-starting-audience.png)

Una vez seleccionadas las audiencias, el número estimado de perfiles se muestra en la parte inferior de la actividad.

## Añadir actividades {#action-activities}

Añada actividades después de seleccionar la audiencia de inicio para restringir la selección.

Para ello, haga clic en el botón + de la ruta de composición y seleccione la actividad que desee. Se abre el panel derecho, que le permite configurar la actividad recién agregada.

![](assets/audiences-select-activity.png)

Las actividades disponibles son:

* [Audiencia](#audience): incluir perfiles adicionales que pertenecen a una o varias audiencias existentes,
* [Excluir](#exclude): excluir perfiles pertenecientes a una audiencia existente o excluir perfiles basados en atributos específicos,
* [Enriquecer](#enrich): enriquezca la audiencia con atributos adicionales procedentes de conjuntos de datos de Adobe Experience Platform,
* [Rango](#rank): clasifique perfiles en función de un atributo específico, especifique el número de perfiles que desea conservar e inclúyalos en la composición.
* [Split](#split): divida la composición en varias rutas en función de porcentajes aleatorios o atributos.

Puede añadir tantas como desee **[!UICONTROL Audiencia]** y **[!UICONTROL Excluir]** actividades según sea necesario en la composición. Sin embargo, no se puede añadir ninguna actividad adicional después de **[!UICONTROL Rango]** y **[!UICONTROL Split]** actividades.

Puede quitar una actividad del lienzo en cualquier momento haciendo clic en el botón Eliminar en el panel derecho.  Si la actividad que desea eliminar es una actividad principal de otras actividades de la composición, se muestra un mensaje que le permite especificar si desea eliminar solamente la actividad seleccionada o todas sus actividades secundarias.

### Actividad de audiencia {#audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="Actividad de audiencia"
>abstract="La actividad de audiencia permite incluir en su composición perfiles adicionales que pertenecen a una audiencia existente."

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="Tipos de combinación"
>abstract="Especifique cómo se deben combinar los perfiles de las audiencias seleccionadas."

El **[!UICONTROL Audiencia]** La actividad de le permite incluir en la composición perfiles adicionales que pertenecen a una audiencia existente.

La configuración de esta actividad es idéntica a la del inicio [Actividad de audiencia](#starting-audience).

### Actividad de exclusión {#exclude}

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="Tipo de exclusión"
>abstract="Utilice el tipo Excluir audiencia para excluir perfiles pertenecientes a una audiencia existente. El tipo de atributo de exclusión permite excluir perfiles según un atributo específico."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="Actividad de exclusión"
>abstract="La actividad de exclusión permite excluir perfiles de la composición seleccionando una audiencia existente o utilizando una regla."

El **[!UICONTROL Excluir]** esta actividad le permite excluir perfiles de la composición. Hay dos tipos de exclusión disponibles:

* **[!UICONTROL Excluir audiencia]**: Excluya perfiles pertenecientes a una audiencia existente.

  Haga clic en **[!UICONTROL Añadir audiencia]** y, a continuación, seleccione la audiencia que desee excluir.

  ![](assets/audiences-exclude-audience.png)

* **[!UICONTROL Excluir mediante atributo]**: excluir perfiles en función de un atributo específico.

  Seleccione el atributo que desea buscar y especifique el valor que desea excluir. En este ejemplo, se excluyen de la composición perfiles cuya dirección postal está en Japón.

  ![](assets/audiences-exclude-attribute.png)

### Enriquecer {#enrich}

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich"
>title="Actividad de enriquecimiento"
>abstract="Utilice la actividad Enrich para enriquecer la audiencia con atributos adicionales procedentes de conjuntos de datos de Adobe Experience Platform. Por ejemplo, puede añadir información relacionada con el producto comprado, como su nombre, precio o ID de fabricante, y aprovechar esta información para personalizar las entregas enviadas a la audiencia."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_dataset"
>title="Conjunto de datos de enriquecimiento"
>abstract="Seleccione el conjunto de datos de enriquecimiento que contiene los datos que desea asociar a la audiencia."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_criteria"
>title="Criterios de enriquecimiento"
>abstract="Seleccione los campos que se utilizarán como clave de reconciliación entre el conjunto de datos de origen, es decir, la audiencia y el conjunto de datos de enriquecimiento."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_attributes"
>title="Atributos de enriquecimiento"
>abstract="Seleccione uno o varios atributos del conjunto de datos de enriquecimiento para asociarlos a la audiencia. Una vez publicada la composición, estos atributos se asocian a la audiencia y se pueden aprovechar en campañas para personalizar envíos."

El **[!UICONTROL Enriquecer]** La actividad de le permite enriquecer su audiencia con atributos adicionales procedentes de conjuntos de datos de Adobe Experience Platform. Por ejemplo, puede añadir información relacionada con el producto comprado, como su nombre, precio o ID de fabricante, y aprovechar esta información para personalizar las entregas enviadas a la audiencia.

>[!IMPORTANT]
>
>Por ahora, las etiquetas del conjunto de datos, ya sea en el nivel del conjunto de datos o de campo, no se propagan a la audiencia recién creada. Esto puede afectar al control de acceso o al control de datos de la audiencia resultante. Por este motivo, al componer audiencias, utilice únicamente datos de prueba.

Para configurar la actividad, siga estos pasos:

1. Seleccione el **[!UICONTROL Conjunto de datos de enriquecimiento]** que contenga los datos que desee asociar a la audiencia.

1. En el **[!UICONTROL Criterios de enriquecimiento]** , seleccione los campos que se utilizarán como clave de reconciliación entre el conjunto de datos de origen, es decir, la audiencia y el conjunto de datos de enriquecimiento. En este ejemplo, utilizamos el ID del producto comprado como clave de reconciliación.

1. Haga clic en **[!UICONTROL Añadir atributos]** a continuación, seleccione uno o varios atributos del conjunto de datos de enriquecimiento para asociarlos a la audiencia.

   ![](assets/audiences-enrich-activity.png)

Una vez publicada la composición, los atributos seleccionados se asocian a la audiencia y se pueden aprovechar en campañas para personalizar las entregas.

### Actividad de clasificación {#rank}

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="Actividad de clasificación"
>abstract="La actividad de clasificación permite clasificar perfiles según un atributo específico e incluirlos en su composición. Por ejemplo, incluya los 50 perfiles con la mayor cantidad de puntos de fidelidad."

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="Añadir límite de perfil"
>abstract="Active esta opción para especificar el número máximo de perfiles que desea incluir en la composición."

El **[!UICONTROL Rango]** la actividad le permite clasificar perfiles en función de un atributo específico e incluirlos en la composición. Por ejemplo, puede incluir los 50 perfiles con la mayor cantidad de puntos de lealtad.

1. Seleccione el atributo que desea buscar y especifique un orden de clasificación (ascendente o descendente).

   >[!NOTE]
   >
   >Puede seleccionar atributos con los siguientes tipos de datos: entero, números, corto <!--(other?)-->

1. Alternar el **[!UICONTROL Añadir límite de perfil]** y especifique un número máximo de perfiles para incluir en la composición.

   ![](assets/audiences-rank.png)

### Actividad de división {#split}

<!-- [!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Control Group"
>abstract="Use control groups to isolate a portion of the profiles. This allows you to measure the impact of a marketing activity and make a comparison with the behavior of the rest of the population."-->

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="Actividad de división"
>abstract="La actividad de división permite dividir la composición en varias rutas. Al publicar la composición, se guardará una audiencia en Adobe Experience Platform para cada ruta."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="Tipo de división"
>abstract="Utilice el tipo de división Porcentaje para dividir aleatoriamente los perfiles en varias rutas. El tipo de división Atributo permite dividir perfiles según un atributo específico."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_otherprofiles_text"
>title="Otros perfiles"
>abstract="Active esta opción para crear una ruta adicional con los perfiles restantes que no coinciden con ninguna de las condiciones especificadas en las otras rutas."

El **[!UICONTROL Split]** la actividad le permite dividir la composición en varias rutas.

Esta operación añade automáticamente un **[!UICONTROL Guardar]** actividad al final de cada ruta. Al publicar la composición, se guardará una audiencia en Adobe Experience Platform para cada ruta.

Hay dos tipos de operaciones de división disponibles:

* **[!UICONTROL División porcentual]**: divida aleatoriamente los perfiles en dos o más rutas. Por ejemplo, puede dividir los perfiles en dos rutas distintas del 50 % cada una. <!--and add an additional path for control group.-->

  ![](assets/audiences-split-percentage.png)

* **[!UICONTROL División de atributos]**: divida los perfiles en función de un atributo específico. En este ejemplo, dividimos los perfiles en función de sus preferencias de tipo de habitación.

  ![](assets/audiences-split.png)

  >[!NOTE]
  >
  >El **[!UICONTROL Otros perfiles]** permite crear una ruta adicional con los perfiles restantes que no coinciden con ninguna de las condiciones especificadas en las otras rutas.

## Guarde las audiencias {#save}

Configure las audiencias resultantes que se guardarán en Adobe Experience Platform.

Para ello, seleccione la **[!UICONTROL Guardar audiencia]** actividad al final de cada ruta y, a continuación, especifique el nombre de la nueva audiencia que desea crear.

![](assets/audiences-publish.png)

Una vez preparada la composición, puede publicarla. [Aprenda a crear composiciones](create-compositions.md)
