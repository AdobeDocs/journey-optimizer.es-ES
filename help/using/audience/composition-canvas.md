---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con el lienzo de composición
description: Aprenda a trabajar con el lienzo de composición
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 3eb9466e-9d88-4470-a22f-5e24a29923ae
source-git-commit: 01c14590fe55d8f11c1ff2b18141933b0b3dd5ca
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 28%

---

# Trabajo con el lienzo de composición {#composition-canvas}

>[!BEGINSHADEBOX]

Esta documentación proporciona información detallada sobre cómo trabajar con la composición de públicos en Adobe Journey Optimizer. Si no usa Adobe Journey Optimizer, [haga clic aquí](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=es){target="_blank"}.

>[!ENDSHADEBOX]

Composición de audiencia proporciona un lienzo visual que le permite crear audiencias y utilizar varias actividades (dividir, enriquecer, etc.).

Los pasos para componer una audiencia en el lienzo son los siguientes:

1. [Definición de la audiencia o audiencias de inicio](#starting-audience)
1. [Añada una o varias actividades](#action-activities)
1. [Guardar los resultados en una nueva audiencia](#save)

## Selección de la audiencia inicial {#starting-audience}

El primer paso para crear una composición es seleccionar una o varias audiencias existentes como base de la composición.

1. Seleccione la actividad **[!UICONTROL Audience]** y proporcione una etiqueta para la actividad.

1. Elija la audiencia a la que desee dirigirse:

   * Haga clic en el botón **[!UICONTROL Agregar audiencia]** para seleccionar una o varias audiencias existentes,
   * Haga clic en el botón **[!UICONTROL Generar regla]** para crear una nueva definición de audiencia con el [servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=es).

   ![](assets/audiences-choose-audience.png)

1. Si se seleccionan varias audiencias, especifique cómo se deben combinar los perfiles de estas audiencias:

* **[!UICONTROL Union]**: incluye todos los perfiles de las audiencias seleccionadas,
* **[!UICONTROL Intersección]**: incluye perfiles que son comunes a todas las audiencias seleccionadas,
* **[!UICONTROL Excluir superposición]**: incluye perfiles que pertenecen a una de las audiencias solamente. No se incluirán los perfiles que pertenezcan a más de una audiencia.

En este ejemplo, queremos segmentar todos los perfiles pertenecientes a las audiencias oro y plata.

![](assets/audiences-starting-audience.png)

Una vez seleccionadas las audiencias, el número estimado de perfiles se muestra en la parte inferior de la actividad.

## Añadir actividades {#action-activities}

Añada actividades después de seleccionar la audiencia de inicio para restringir la selección.

Para ello, haga clic en el botón + de la ruta de composición y seleccione la actividad que desee. Se abre el panel derecho, que le permite configurar la actividad recién agregada.

![](assets/audiences-select-activity.png)

Las actividades disponibles son:

* [Audiencia](#audience): incluye perfiles adicionales que pertenecen a una o varias audiencias existentes,
* [Excluir](#exclude): excluir perfiles que pertenecen a una audiencia existente o excluir perfiles según atributos específicos.
* [Enriquecer](#enrich): enriquezca la audiencia con atributos adicionales procedentes de conjuntos de datos de Adobe Experience Platform,
* [Rango](#rank): clasifique perfiles en función de un atributo específico, especifique el número de perfiles que desea conservar e inclúyalos en la composición.
* [Split](#split): divide tu composición en varias rutas según porcentajes aleatorios o atributos.

Puede agregar tantas actividades **[!UICONTROL Audience]** y **[!UICONTROL Exclude]** como sea necesario en la composición. Sin embargo, no se puede agregar ninguna actividad adicional después de las actividades **[!UICONTROL Rank]** y **[!UICONTROL Split]**.

Puede quitar una actividad del lienzo en cualquier momento haciendo clic en el botón Eliminar en el panel derecho.  Si la actividad que desea eliminar es una actividad principal de otras actividades de la composición, se muestra un mensaje que le permite especificar si desea eliminar sólo la actividad seleccionada o todas sus actividades secundarias.

### Actividad de audiencia {#audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="Actividad de audiencia"
>abstract="La actividad de audiencia permite incluir en su composición perfiles adicionales que pertenecen a una audiencia existente."

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="Tipos de combinación"
>abstract="Especifique cómo se deben combinar los perfiles de las audiencias seleccionadas."

La actividad **[!UICONTROL Audience]** le permite incluir en la composición perfiles adicionales que pertenecen a una audiencia existente.

La configuración de esta actividad es idéntica a la [actividad de audiencia](#starting-audience) inicial.

### Actividad de exclusión {#exclude}

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="Tipo de exclusión"
>abstract="Utilice el tipo Excluir audiencia para excluir perfiles pertenecientes a una audiencia existente. El tipo de atributo de exclusión permite excluir perfiles según un atributo específico."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="Actividad de exclusión"
>abstract="La actividad de exclusión permite excluir perfiles de la composición seleccionando una audiencia existente o utilizando una regla."

La actividad **[!UICONTROL Excluir]** le permite excluir perfiles de su composición. Hay dos tipos de exclusión disponibles:

* **[!UICONTROL Excluir audiencia]**: excluya perfiles que pertenezcan a una audiencia existente.

  Haga clic en el botón **[!UICONTROL Agregar audiencia]** y luego seleccione la audiencia que desee excluir.

  ![](assets/audiences-exclude-audience.png)

* **[!UICONTROL Excluir mediante atributo]**: Excluya perfiles basados en un atributo específico.

  Seleccione el atributo que desea buscar y especifique el valor que desea excluir. En este ejemplo, se excluyen de la composición perfiles cuya dirección postal está en Japón.

  >[!NOTE]
  >
  >Solo se puede especificar un valor de exclusión.

  ![](assets/audiences-exclude-attribute.png)

### Actividad de enriquecimiento {#enrich}

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich"
>title="Actividad de enriquecimiento"
>abstract="Utilice la actividad Enriquecer para enriquecer al público con atributos adicionales procedentes de los conjuntos de datos de Adobe Experience Platform. Por ejemplo, puede añadir información relacionada con el producto comprado, como el nombre, precio o ID de fabricante y utilizar esta información para personalizar los envíos enviados al público."

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
>abstract="Seleccione uno o varios atributos del conjunto de datos de enriquecimiento para asociarlos a la audiencia. Una vez publicada la composición, estos atributos se asocian al público y se pueden aprovechar en campañas de Journey Optimizer para personalizar envíos."

La actividad **[!UICONTROL Enrich]** le permite enriquecer su audiencia con atributos adicionales procedentes de conjuntos de datos de Adobe Experience Platform. Por ejemplo, puede añadir información relacionada con el producto comprado, como el nombre, precio o ID de fabricante y utilizar esta información para personalizar los envíos enviados al público.

Tenga en cuenta las siguientes limitaciones al trabajar con la actividad **[!UICONTROL Enrich]**:

* **Los conjuntos de datos** para el enriquecimiento deben ser de tipo de registro (a diferencia del tipo de evento) y no pueden ser un conjunto de datos del sistema ni estar marcados para un perfil. Deben tener menos de 1 GB.
* **El enriquecimiento admite una combinación 1:1**. Esto significa que si las claves de unión tienen más de una coincidencia en el conjunto de datos de enriquecimiento, el sistema selecciona una de las coincidencias y la utiliza para la unión 1:1.
* **Las audiencias se pueden activar en destinos RTCDP**, pero sus atributos de enriquecimiento, si los hay, no.
* Los atributos de enriquecimiento aún no están integrados con el servicio de aplicación de políticas. Por lo tanto, las etiquetas de uso de datos que aplique a los atributos de enriquecimiento no se aplicarán a las campañas o recorridos de Journey Optimizer.

Para configurar la actividad, siga estos pasos:

1. Seleccione el **[!UICONTROL conjunto de datos de enriquecimiento]** que contiene los datos que desea asociar a la audiencia.

1. En la sección **[!UICONTROL Criterios de enriquecimiento]**, seleccione los campos que se usarán como clave de reconciliación entre el conjunto de datos de origen, es decir, la audiencia y el conjunto de datos de enriquecimiento. En este ejemplo, utilizamos el ID del producto comprado como clave de reconciliación.

1. Haga clic en el botón **[!UICONTROL Agregar atributos]** y, a continuación, seleccione uno o varios atributos del conjunto de datos de enriquecimiento para asociarlos a la audiencia.

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

La actividad **[!UICONTROL Rank]** le permite clasificar perfiles en función de un atributo específico e incluirlos en la composición. Por ejemplo, puede incluir los 50 perfiles con la mayor cantidad de puntos de lealtad.

1. Seleccione el atributo que desea buscar y especifique un orden de clasificación (ascendente o descendente).

   >[!NOTE]
   >
   >Puede seleccionar atributos con los siguientes tipos de datos: entero, números, corto <!--(other?)-->

1. Active la opción **[!UICONTROL Agregar límite de perfiles]** y especifique el número máximo de perfiles que se incluirán en la composición.

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

La actividad **[!UICONTROL Split]** le permite dividir la composición en varias rutas.

Esta operación agrega automáticamente una actividad **[!UICONTROL Guardar]** al final de cada ruta. Al publicar la composición, se guardará una audiencia en Adobe Experience Platform para cada ruta.

Hay dos tipos de operaciones de división disponibles:

* **[!UICONTROL División porcentual]**: los perfiles se dividen aleatoriamente en dos o más rutas. Por ejemplo, puede dividir los perfiles en dos rutas distintas del 50 % cada una. <!--and add an additional path for control group.-->

  ![](assets/audiences-split-percentage.png)

* **[!UICONTROL División de atributos]**: los perfiles de división se basan en un atributo específico. En este ejemplo, dividimos los perfiles en función de sus preferencias de tipo de habitación.

  ![](assets/audiences-split.png)

  Para configurar una actividad de división basada en atributos, siga estos pasos:

   1. Haga clic en el botón situado junto al campo **[!UICONTROL Atributo]** para seleccionar el atributo que desea utilizar como criterio de división.
   1. Añada tantas rutas como sea necesario. Para cada ruta, proporcione una etiqueta y especifique el valor que se utilizará para determinar qué perfiles deben incluirse en esa ruta en particular.

      >[!NOTE]
      >
      >Solo se puede especificar un valor para cada ruta.

   1. Active la opción **[!UICONTROL Otros perfiles]** para crear una ruta adicional con los perfiles restantes que no coincidan con ninguna de las condiciones especificadas en las otras rutas.

## Guarde las audiencias {#save}

Configure las audiencias resultantes que se guardarán en Adobe Experience Platform.

Para ello, seleccione la actividad **[!UICONTROL Guardar audiencia]** al final de cada ruta y luego especifique el nombre de la nueva audiencia que desea crear.

![](assets/audiences-publish.png)

Una vez preparada la composición, puede publicarla. [Aprenda a crear composiciones](create-compositions.md)
