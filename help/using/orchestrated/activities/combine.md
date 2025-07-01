---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Combinar
description: Aprenda a utilizar la actividad Combinar
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: af3c3a9c-8172-43b0-bba1-4a3d068b9a9e
source-git-commit: cb335fd5610d70d801ae1c32dfe4d3ca9d1160ab
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 69%

---

# Combinar {#combine}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine"
>title="Actividad de combinación"
>abstract="La actividad **Combinar** permite realizar la segmentación de la población entrante. Por lo tanto, puede combinar varias poblaciones, excluir parte de ellas o solo mantener datos comunes para varias poblaciones destinatarias."

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](../configuration-steps.md)<br/><br/>[Pasos clave para la creación de campañas orquestadas](../gs-campaign-creation.md) | [Crear una campaña orquestada](../create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](../orchestrate-activities.md)<br/><br/>[Enviar mensajes con campañas orquestadas](../send-messages.md)<br/><br/>[Iniciar y supervisar la campaña](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabaje con el Modeler de consultas](../orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](../build-query.md)<br/><br/>[Editar expresiones](../edit-expressions.md) | [Empiece con las actividades](about-activities.md)<br/><br/>Actividades:<br/>[Y únase](and-join.md) - [Generar audiencia](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Combinar](combine.md) - [Anulación de duplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [División](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

La actividad **[!UICONTROL Combinar]** es un tipo de actividad de **[!UICONTROL Segmentación]** que le permite segmentar eficazmente la población entrante. Permite combinar varias poblaciones, excluir segmentos específicos o conservar solo los datos compartidos entre varios objetivos.

Estas son las opciones de segmentación disponibles:

* **[!UICONTROL Union]**: combina los resultados de varias actividades en un solo destino unificado.

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
>abstract="Seleccione cómo combinar audiencias. La **Unión** le permite reagrupar el resultado de varias actividades en un solo destinatario. La **Intersección** le permite mantener solo los elementos comunes a las diferentes poblaciones entrantes de la actividad. La **Exclusión** permite excluir elementos de una población según determinados criterios. "

Siga estos pasos comunes para comenzar a configurar la actividad **[!UICONTROL Combinar]**:

![](../assets/orchestrated-combine.png)

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

En la actividad **[!UICONTROL Combinar]**, puede configurar una **[!UICONTROL Unión]**. Para ello, debe seleccionar **[!UICONTROL Tipo de reconciliación]** para definir cómo se gestionan los duplicados:

* **[!UICONTROL Solo claves]**: este es el modo predeterminado. La actividad solo mantiene un elemento cuando los elementos de las distintas transiciones entrantes tienen la misma clave. Puede usar esta opción solo si las poblaciones entrantes son homogéneas.
* **[!UICONTROL Una selección de columnas]**: seleccione esta opción para definir la lista de columnas a las que desea aplicar la reconciliación de datos. Primero debe seleccionar el conjunto principal (el que contiene los datos de origen) y luego las columnas que se utilizarán para la unión.

En el ejemplo siguiente, se usa una actividad **[!UICONTROL Combinar]** y se agrega una **[!UICONTROL Unión]** para recuperar todos los perfiles de las dos consultas: Miembros socio y Compradores para formar una audiencia mayor.

![](../assets/orchestrated-union-example.png)

## Intersección {#combine-intersection}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_reconciliation_options"
>title="Opciones de reconciliación de intersección"
>abstract="Seleccione el **Tipo de reconciliación** para definir cómo gestionar duplicados. De manera predeterminada, la opción **Claves** está activada, lo que significa que la actividad solo mantiene un elemento cuando los elementos de las diferentes transiciones de entrada tienen la misma clave. Utilice la opción **Una selección de columnas** para definir la lista de columnas a las que desea aplicar la reconciliación de datos."

En la actividad **[!UICONTROL Combinar]**, puede configurar una **[!UICONTROL intersección]**. Para ello, debe seguir los pasos adicionales a continuación:

1. Seleccione el **[!UICONTROL Tipo de reconciliación]** para definir cómo se gestionan los duplicados. Consulte la sección [Unión](#union).
1. Seleccione la opción **[!UICONTROL Generar complemento]** si desea procesar la población restante. El complemento contendrá la unión de los resultados de todas las actividades entrantes menos la intersección. A continuación, se añadirá una transición saliente adicional a la actividad.

El ejemplo siguiente muestra la **[!UICONTROL intersección]** entre dos actividades de consulta. Se está utilizando aquí para recuperar perfiles con una membresía de Fidelidad y cuya última compra fue hace menos de un mes.

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

En la actividad **[!UICONTROL Combinar]**, puede configurar una **[!UICONTROL Exclusión]**. Para ello, debe seguir los pasos adicionales a continuación:

1. En la sección **[!UICONTROL Conjuntos que unir]**, seleccione el **[!UICONTROL Conjunto principal]** de las transiciones entrantes. Es el conjunto desde el que se excluyen los elementos. Los demás conjuntos coinciden con elementos antes de excluirse del conjunto principal.
1. Si es necesario, puede manipular las tablas entrantes. De hecho, para excluir un público destinatario de otra dimensión, se debe devolver este público destinatario a la misma dimensión de segmentación que el público destinatario principal. Para ello, haga clic en **[!UICONTROL Añadir una regla]** en la sección **[!UICONTROL Reglas de exclusión]** y especifique las condiciones del cambio de dimensión. La reconciliación de datos se lleva a cabo mediante un atributo o una unión.
1. Seleccione la opción **[!UICONTROL Generar complemento]** si desea procesar la población restante. Consulte la sección [Intersección](#intersection).

El siguiente ejemplo de **[!UICONTROL exclusión]** muestra dos consultas configuradas para filtrar perfiles que compraron un producto. Los perfiles que no son miembros socio se excluyen del primer conjunto.

Por qué: Estás llevando a cabo una campaña de lealtad, por lo que los no miembros son irrelevantes.

![](../assets/orchestrated-exclusion-example.png)

