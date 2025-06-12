---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad de anulación de duplicación
description: Aprenda a utilizar la actividad de anulación de duplicación
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
source-git-commit: 5872e192c849b7a7909f0b50caa1331b15490d79
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 35%

---

# Deduplicación {#deduplication}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_fields"
>title="Campos para identificar duplicados"
>abstract="En la sección **Campos para identificar duplicados**, haga clic en el botón **Añadir atributo** para especificar los campos para los que los valores idénticos permiten identificar los duplicados, tales como: dirección de correo electrónico, nombre, apellidos, etc. El orden de los campos permite especificar los que se procesarán en primer lugar."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication"
>title="Actividad de deduplicación"
>abstract="La actividad de **deduplicación permite** eliminar duplicados en los resultados de las actividades entrantes. Se utiliza principalmente después de actividades de segmentación y antes de actividades que permiten el uso de datos direccionados."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_complement"
>title="Generación de un complemento"
>abstract="Puede generar una transición saliente adicional con la población restante, que se excluyó como duplicado. Para ello, active la opción **Generar complemento**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_settings"
>title="Configuración de la deduplicación"
>abstract="Para eliminar duplicados en los datos entrantes, defina el método de deduplicación en los campos siguientes. De forma predeterminada, solo se guarda un registro. También debe seleccionar el modo de deduplicación en función de una expresión o un atributo. De forma predeterminada, el registro que se va a excluir de los duplicados se selecciona de forma aleatoria."

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicie su primera campaña orquestada | Consultar la base de datos | Actividades de campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](../configuration-steps.md)<br/><br/>[Pasos clave para la creación de campañas orquestadas](../gs-campaign-creation.md) | [Crear una campaña orquestada](../create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](../orchestrate-activities.md)<br/><br/>[Enviar mensajes con campañas orquestadas](../send-messages.md)<br/><br/>[Iniciar y supervisar la campaña](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabaje con el Modeler de consultas](../orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](../build-query.md)<br/><br/>[Editar expresiones](../edit-expressions.md) | [Empiece con las actividades](about-activities.md)<br/><br/>Actividades:<br/>[Y únase](and-join.md) - [Generar audiencia](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Combinar](combine.md) - [Anulación de duplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [División](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

La actividad **Deduplication** es una actividad de **segmentación**. Esta actividad le permite eliminar duplicados en los resultados de las actividades entrantes, por ejemplo perfiles duplicados en la lista de destinatarios. La actividad **Deduplication** se utiliza generalmente después de actividades de segmentación y antes de actividades que permiten el uso de datos de destino.

## Configuración de la actividad de anulación de duplicación{#deduplication-configuration}

Siga estos pasos para configurar la actividad **Deduplication**:


1. Agregue una actividad **Deduplication** a su campaña orquestada.

1. En la sección **Campos para identificar duplicados**, haga clic en el botón **Añadir atributo** para especificar los campos para los que los valores idénticos permiten identificar los duplicados, tales como: dirección de correo electrónico, nombre, apellidos, etc. El orden de los campos permite especificar los que se procesarán en primer lugar.

![](../assets/deduplication-1.png)

1. En la sección **Configuración de anulación de duplicación**, elija cuántos registros únicos debe seguir usando el campo Duplicados que mantener. El valor predeterminado es 1, que mantiene un registro por grupo duplicado. Configúrelo en 0 para mantener todos los duplicados.

   Por ejemplo, si los registros A y B son duplicados de Y y el registro C es un duplicado de Z:

   * **Si el valor del campo es 1**: solo se guardan los registros Y y Z.
   * **Si el valor del campo es 0**: se guardan todos los registros (A, B, C, Y, Z).
   * **Si el valor del campo es 2**: se conservan C y Z, además de dos valores de A, B e Y, aleatoriamente o en función del método de deduplicación.

1. Elija un **método de deduplicación**, que define cómo el sistema decide qué registros se deben conservar de cada grupo de duplicados:

   * **Selección aleatoria**: Selecciona aleatoriamente el registro que se va a excluir de los duplicados.
   * **Uso de una expresión**: Mantiene los registros con el valor más alto o más bajo basándose en una expresión definida.
   * **Valores no vacíos**: Mantiene registros donde el campo seleccionado no está vacío, por ejemplo, conserva solo perfiles con un número de teléfono.
   * **Siguiendo una lista de valores**: Permite priorizar valores específicos para uno o más campos, por ejemplo, puede dar prioridad a los registros con &quot;País&quot; establecido en Francia. Haga clic en **Atributo** para elegir un campo o crear una expresión personalizada. Use el **botón Agregar** para escribir los valores preferidos en el orden de prioridad.

   ![](../assets/deduplication-2.png)

1. Seleccione la opción **Generate complement** si desea utilizar la población restante. El complemento está formado por todos los duplicados. A continuación, se agregará una transición adicional a la actividad.

## Ejemplo{#deduplication-example}

En el ejemplo siguiente, se usa una actividad **Deduplication** para eliminar registros duplicados de la audiencia de destino antes de realizar una entrega. La audiencia se filtra primero para incluir solo perfiles con un campo de correo electrónico que no esté vacío. A continuación, la actividad **Deduplication** utiliza la dirección de correo electrónico para identificar y excluir duplicados.

![](../assets/deduplication-3.png)
