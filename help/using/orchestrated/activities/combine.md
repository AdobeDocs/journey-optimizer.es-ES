---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Combinar
description: Aprenda a utilizar la actividad Combinar
exl-id: af3c3a9c-8172-43b0-bba1-4a3d068b9a9e
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 100%

---


# Combinar {#combine}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine"
>title="Actividad de combinación"
>abstract="La actividad **Combinar** permite realizar la segmentación de la población entrante. Por lo tanto, puede combinar varias poblaciones, excluir parte de ellas o solo mantener datos comunes para varias poblaciones destinatarias."

La actividad **[!UICONTROL Combinar]** es un tipo de actividad de **[!UICONTROL Segmentación]** que le permite segmentar eficazmente la población entrante. Permite combinar varias poblaciones, excluir segmentos específicos o conservar solo los datos compartidos entre varios objetivos.

Las opciones de segmentación disponibles son las siguientes:

* **[!UICONTROL Unión]**: combina el resultado de varias actividades en un solo destinatario unificado.

* **[!UICONTROL Intersección]**: conserva únicamente los elementos que son comunes en todas las poblaciones de entrada.

* **[!UICONTROL Exclusión]**: elimina elementos de una población en función de criterios especificados.

## Configuración de la actividad de combinación {#combine-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_merging_options"
>title="Opciones de combinación de intersección"
>abstract="La intersección permite mantener solo los elementos comunes a las diferentes poblaciones entrantes en la actividad. En la sección Conjuntos que unir, compruebe todas las actividades anteriores que desee unir."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_exclusion_merging_options"
>title="Opciones de combinación de exclusión"
>abstract="La exclusión permite excluir elementos de una población según determinados criterios. En la sección Conjuntos que unir, compruebe todas las actividades anteriores que desee unir."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_options"
>title="Selección del tipo de segmentación"
>abstract="Seleccione cómo combinar públicos. La **Unión** le permite reagrupar el resultado de varias actividades en un solo destinatario. La **Intersección** le permite mantener solo los elementos comunes a las diferentes poblaciones entrantes de la actividad. La **Exclusión** permite excluir elementos de una población según determinados criterios. "

Siga estos pasos comunes para comenzar a configurar la actividad **[!UICONTROL Combinar]**:

![](../assets/orchestrated-union.png)

1. Añada varias actividades, como actividades **[!UICONTROL Generar público destinatario]** para formar al menos dos ramas de ejecución diferentes.
1. Añada una actividad **[!UICONTROL Combinar]** a cualquiera de las ramas anteriores.
1. Seleccione el tipo de segmentación: [unión](#union), [intersección](#intersection) o [exclusión](#exclusion).
1. Haga clic en **[!UICONTROL Continuar]**.
1. En la sección **[!UICONTROL Conjuntos que unir]**, compruebe todas las actividades anteriores que desee unir.

## Unión {#combine-union}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_reconciliation"
>title="Opciones de reconciliación"
>abstract="Seleccione el **Tipo de reconciliación** para definir cómo gestionar duplicados. De manera predeterminada, la opción **Claves** está activada, lo que significa que la actividad solo mantiene un elemento cuando los elementos de las diferentes transiciones de entrada tienen la misma clave. Utilice la opción **Una selección de columnas** para definir la lista de columnas a las que desea aplicar la reconciliación de datos."

Dentro de la actividad **[!UICONTROL Combinar]**, puede configurar una **[!UICONTROL Unión]** seleccionando un **[!UICONTROL Tipo de reconciliación]** para determinar cómo se administran los registros duplicados:

* **[!UICONTROL Solo claves]** (predeterminado): conserva un único registro cuando varias transiciones entrantes comparten la misma clave. Esta opción solo se puede usar si las poblaciones entrantes son homogéneas.

* **[!UICONTROL Una selección de columnas]**: le permite especificar qué columnas se utilizan para la reconciliación de datos. Seleccione **[!UICONTROL Añadir atributo]**.

En el ejemplo siguiente, se usa una actividad **[!UICONTROL Combinar]** con una **[!UICONTROL Unión]** para combinar los resultados de dos consultas, **Miembros de lealtad** y **Compradores** en un solo público más amplio que incluye todos los perfiles de ambos segmentos.

![](../assets/orchestrated-union-example.png)

## Intersección {#combine-intersection}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_reconciliation_options"
>title="Opciones de reconciliación de intersección"
>abstract="Seleccione el **Tipo de reconciliación** para definir cómo gestionar duplicados. De manera predeterminada, la opción **Claves** está activada, lo que significa que la actividad solo mantiene un elemento cuando los elementos de las diferentes transiciones de entrada tienen la misma clave. Utilice la opción **Una selección de columnas** para definir la lista de columnas a las que desea aplicar la reconciliación de datos."

En la actividad **[!UICONTROL Combinar]**, puede configurar una **[!UICONTROL Intersección]**. Para ello, debe seguir los pasos adicionales que se indican a continuación:

1. Seleccione el **[!UICONTROL Tipo de reconciliación]** para definir cómo se gestionan los duplicados.

   * **[!UICONTROL Solo claves]** (predeterminado): conserva un único registro cuando varias transiciones entrantes comparten la misma clave. Esta opción solo se puede usar si las poblaciones entrantes son homogéneas.

   * **[!UICONTROL Una selección de columnas]**: le permite especificar qué columnas se utilizan para la reconciliación de datos. Seleccione **[!UICONTROL Añadir atributo]**.

1. Seleccione la opción **[!UICONTROL Generar complemento]** si desea procesar la población restante. El complemento contiene la unión de todos los resultados de la actividad entrante, excluida la intersección. A continuación, se añadirá una transición de salida adicional a la actividad.

El siguiente ejemplo muestra la **[!UICONTROL Intersección]** entre dos actividades de consulta. Se usa para identificar los perfiles que son **miembros de lealtad** y que han hecho una compra en el último mes.

![](../assets/orchestrated-intersection-example.png)


## Exclusión {#combine-exclusion}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_exclusion_options"
>title="Reglas de inclusión"
>abstract="Si es necesario, puede manipular las tablas entrantes. De hecho, para excluir un público destinatario de otra dimensión, se debe devolver este público destinatario a la misma dimensión de segmentación que el público destinatario principal. Para ello, haga clic en Añadir una regla en la sección Reglas de exclusión y especifique las condiciones del cambio de dimensión. La reconciliación de datos se lleva a cabo mediante un atributo o una unión."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_sets"
>title="Selección de conjuntos para combinar"
>abstract="En la sección **Conjuntos que unir**, seleccione el **Conjunto principal** de las transiciones entrantes. Es el conjunto desde el que se excluyen los elementos. Los demás conjuntos coinciden con elementos antes de excluirse del conjunto principal."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_exclusion"
>title="Reglas de inclusión"
>abstract="Si es necesario, puede manipular las tablas entrantes. De hecho, para excluir un público destinatario de otra dimensión, se debe devolver este público destinatario a la misma dimensión de segmentación que el público destinatario principal. Para ello, haga clic en Añadir una regla en la sección Reglas de exclusión y especifique las condiciones del cambio de dimensión. La reconciliación de datos se lleva a cabo mediante un atributo o una unión."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_complement"
>title="Complemento de generación de combinación"
>abstract="Active la opción Generar complemento para procesar la población restante en una transición adicional."

En la actividad **[!UICONTROL Combinar]**, puede configurar una **[!UICONTROL Exclusión]**. Para ello, debe seguir los pasos adicionales que se indican a continuación:

1. En la sección **[!UICONTROL Conjuntos a unir]**, seleccione el **[!UICONTROL Conjunto principal]** que representa la población principal. Los registros encontrados en los demás conjuntos se excluyen de este conjunto principal.

1. Si es necesario, puede ajustar las tablas entrantes para alinear los destinos de distintas dimensiones. Para excluir un destinatario de otra dimensión, primero se lo debe llevar a la misma dimensión de segmentación que la población principal. Para ello, haga clic en **[!UICONTROL Añadir una regla]** y defina las condiciones para cambiar la dimensión. A continuación, se realiza la reconciliación mediante un atributo o una combinación.

1. Seleccione la opción **[!UICONTROL Generar complemento]** si desea procesar la población restante. El complemento contiene la unión de todos los resultados de la actividad entrante, excluida la intersección. A continuación, se añadirá una transición de salida adicional a la actividad.

El siguiente ejemplo de **[!UICONTROL exclusión]** muestra dos consultas configuradas para filtrar perfiles que compraron un producto. Los perfiles que no son miembros de lealtad se excluyen del primer conjunto.

![](../assets/orchestrated-exclusion-example.png)

