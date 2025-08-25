---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a Composición de públicos
description: Más información sobre la composición de audiencias
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: af71d24d-77eb-44df-8216-b0aeaf4c4fa4
source-git-commit: 060d65e8d3fb1442b04626170a35d463d1faa514
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 51%

---

# Introducción a Composición de públicos {#get-start-audience-composition}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_composition"
>title="Crear una composición"
>abstract="Cree un flujo de trabajo de composición para combinar los públicos de Adobe Experience Platform existentes en un lienzo visual y aproveche varias actividades (división, exclusión…) para crear nuevos públicos."

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Publicar la audiencia"
>abstract="Publique la composición para guardar las audiencias resultantes en Adobe Experience Platform."

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="Actividad de audiencia"
>abstract="La actividad de audiencia permite incluir en su composición perfiles adicionales que pertenecen a una audiencia existente."

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="Tipos de combinación"
>abstract="Especifique cómo se deben combinar los perfiles de las audiencias seleccionadas."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="Tipo de exclusión"
>abstract="Utilice el tipo Excluir audiencia para excluir perfiles pertenecientes a una audiencia existente. El tipo de atributo de exclusión permite excluir perfiles según un atributo específico."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="Actividad de exclusión"
>abstract="La actividad de exclusión permite excluir perfiles de la composición seleccionando una audiencia existente o utilizando una regla."

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

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="Actividad de clasificación"
>abstract="La actividad de clasificación permite clasificar perfiles según un atributo específico e incluirlos en su composición. Por ejemplo, incluya los 50 perfiles con la mayor cantidad de puntos de lealtad."

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="Añadir límite de perfil"
>abstract="Active esta opción para especificar el número máximo de perfiles que desea incluir en la composición."

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

>[!BEGINSHADEBOX]

Esta documentación proporciona información detallada sobre cómo trabajar con la composición de públicos en Adobe Journey Optimizer. Si solo es cliente del Perfil del cliente en tiempo real y no utiliza Adobe Journey Optimizer, [haga clic aquí](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=es){target="_blank"}.

>[!ENDSHADEBOX]

La composición de audiencias le permite crear **flujos de trabajo de composición**, donde puede combinar audiencias de Adobe Experience Platform existentes en un lienzo visual y aprovechar diversas actividades (dividir, excluir...) para crear nuevas audiencias.

Una vez finalizado, las **audiencias resultantes** se guardan y se copian en Adobe Experience Platform junto con las audiencias existentes, y se pueden aprovechar en campañas y recorridos de Journey Optimizer para segmentar clientes. Obtenga información sobre cómo segmentar audiencias en Journey Optimizer
![](assets/audiences-process.png)

>[!IMPORTANT]
>
>* El uso de audiencias y atributos de la composición de audiencias no está disponible actualmente para su uso con Healthcare Shield o Privacy and Security Shield.
>
>* Los atributos de enriquecimiento aún no están integrados con el servicio de aplicación de políticas. Por lo tanto, las etiquetas de uso de datos que aplique a los atributos de enriquecimiento no se aplicarán a las campañas o recorridos de Journey Optimizer.

Se puede acceder a la composición de públicos desde el menú **[!UICONTROL Públicos]** de Adobe Journey Optimizer:

![](assets/audiences-browse.png)

* La pestaña **[!UICONTROL Información general]** proporciona un tablero específico con métricas clave relacionadas con los datos del público de su organización. Para obtener más información, consulte [Guía de tableros de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/segments.html?lang=es).

* La pestaña **[!UICONTROL Examinar]** lista todos los públicos existentes almacenados en Adobe Experience Platform.

* La pestaña **[!UICONTROL Composiciones]** le permite crear flujos de trabajo de composición en los que puede combinar y organizar públicos para crear otros nuevos.

## Crear un flujo de trabajo de composición {#create}

Para crear un flujo de trabajo de maquetación, siga estos pasos:

1. Acceda al menú **[!UICONTROL Audiencias]** y seleccione **[!UICONTROL Crear audiencia]**.

1. Seleccione **[!UICONTROL Componer audiencia]**.

   ![](assets/audiences-create.png)

1. El lienzo de composición se muestra con dos actividades predeterminadas:

   * **[!UICONTROL Audiencia]**: el punto de partida de la composición. Esta actividad le permite seleccionar una o varias audiencias como base para el flujo de trabajo,

   * **[!UICONTROL Guardar]**: el último paso de la composición. Esta actividad le permite guardar el resultado del flujo de trabajo en una nueva audiencia.

1. Abra las propiedades de la composición para especificar un título y una descripción.

   Si no se define ningún título en las propiedades, la etiqueta de la composición se define en &quot;Composición&quot; seguida de su fecha y hora de creación.

   ![](assets/audiences-properties.png)

1. Configure su composición agregando tantas actividades como sea necesario entre las actividades **[!UICONTROL Audience]** y **[!UICONTROL Save]**. Para obtener más información sobre cómo crear una composición, consulte la [documentación de composición de audiencias](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/ui/audience-composition).

   ![](assets/audiences-publish.png)

1. Una vez que la composición esté lista, haga clic en el botón **[!UICONTROL Publicar]** para publicar la composición y guardar las audiencias resultantes en Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >Puede publicar hasta 10 composiciones en una zona protegida determinada. Si ha alcanzado este umbral, debe eliminar una composición para liberar espacio y publicar una nueva.

   Si se produce algún error durante la publicación, las alertas se mostrarán con información sobre cómo resolver el problema.

   ![](assets/audiences-alerts.png)

1. La composición se publica. Las audiencias resultantes se guardan en Adobe Experience Platform y están listas para segmentarse en Journey Optimizer. [Aprenda a segmentar audiencias en Journey Optimizer](../audience/about-audiences.md#segments-in-journey-optimizer)

>[!NOTE]
>
>Las audiencias de **composición de audiencias** se ejecutan a diario, por lo que es posible que tenga que esperar hasta 24 horas para usarlas en Journey Optimizer. Los atributos enriquecidos en las audiencias de composición de audiencia son tan recientes como la última ejecución de composición, que pueden tardar hasta 24 horas en el pasado.

## Acceso a composiciones {#access}

Se puede acceder a todas las composiciones creadas desde la pestaña **[!UICONTROL Composiciones]**. Puede duplicar o eliminar una composición existente en cualquier momento mediante el botón de puntos suspensivos de la lista.

Las composiciones pueden tener varios estados:

* **[!UICONTROL Borrador]**: la composición está en curso y no se ha publicado.
* **[!UICONTROL Publicado]**: la composición se ha publicado, las audiencias resultantes se han guardado y están disponibles para su uso.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>La composición de audiencia no está integrada actualmente con la capacidad de restablecimiento de la zona protegida. Antes de iniciar el restablecimiento de una zona protegida, debe eliminar las composiciones manualmente para asegurarse de que los datos de audiencia asociados se limpien correctamente. Encontrará información detallada en [Documentación de espacio aislado](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=es#delete-audience-compositions) de Adobe Experience Platform
