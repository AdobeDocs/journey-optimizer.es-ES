---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Test en las campañas organizadas
description: Aprenda a utilizar la actividad Prueba
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
source-git-commit: 458e0b19725147e0a3ad34891ca55b61f1ac44a8
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 59%

---

# Prueba {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Actividad de prueba"
>abstract="La actividad **Prueba** es una actividad de **Control de flujo**. Permite habilitar transiciones en función de condiciones especificadas."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Condiciones"
>abstract="La actividad **Prueba** puede tener varias transiciones de salida. Durante la ejecución de una campaña orquestada, cada condición se prueba secuencialmente hasta que se cumpla una de ellas. Si no se cumple ninguna de las condiciones, la campaña orquestada continúa en la ruta de la **[!UICONTROL condición predeterminada]**. Si no se activa ninguna condición predeterminada, la campaña orquestada se detiene en este punto."

+++ Índice

| Bienvenido a campañas orquestadas | Inicie su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carga de archivos](../file-upload-schema.md)</li><li>[Ingesta de datos](../ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](../access-manage-orchestrated-campaigns.md) | [Pasos clave para crear una campaña orquestada](../gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](../create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](../orchestrate-activities.md)<br/><br/>[Inicie y supervise la campaña](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabajo con el generador de reglas](../orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](../build-query.md)<br/><br/>[Edición de expresiones](../edit-expressions.md)<br/><br/>[Resegmentación](../retarget.md) | [Introducción a las actividades](about-activities.md)<br/><br/>Actividades:<br/>[AND-join](and-join.md) - [Generar público](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Actividades del canal](channels.md) - [Combinar](combine.md) - [Deduplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [Guardar público](save-audience.md) - [División](split.md) - [Esperar](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

La actividad **[!UICONTROL Prueba]** es una actividad de **[!UICONTROL Control de flujo]**. Permite habilitar transiciones en función de condiciones especificadas.

## Configuración de la actividad Prueba {#test-configuration}

Siga estos pasos para configurar la actividad **[!UICONTROL Prueba]**:

1. Agregue una actividad **[!UICONTROL Test]** a su campaña orquestada.

1. De manera predeterminada, la actividad **[!UICONTROL Prueba]** presenta una prueba booleana simple. Si se cumple la condición definida en la transición &quot;Verdadero&quot;, se activará esta transición. De lo contrario, se activa la transición predeterminada “Falso”.

1. Para configurar la condición asociada a una transición, haga clic en el icono **[!UICONTROL Cuadro de diálogo Abrir personalización]**. Utilice el editor de expresiones para definir las reglas necesarias para activar esta transición. También puede aprovechar las variables de eventos, las condiciones y las funciones de fecha y hora.

   Además, puede modificar el campo **[!UICONTROL Label]** para personalizar el nombre de la transición en el lienzo de la campaña orquestada.

   ![](../assets/workflow-test-default.png)

1. Puede añadir varias transiciones de salida a una actividad **[!UICONTROL Prueba]**. Para ello, haga clic en el botón **[!UICONTROL Añadir condición]** y configure la etiqueta y la condición asociada para cada transición.
v
1. Durante la ejecución de una campaña orquestada, cada condición se prueba secuencialmente hasta que se cumpla una de ellas. Si no se cumple ninguna de las condiciones, las campañas orquestadas continúan en la ruta de la **[!UICONTROL condición predeterminada]**. Si no se activa ninguna condición predeterminada, la campaña se detiene en este momento.

## Ejemplo {#example}

En este ejemplo, se activan diferentes transiciones en función del número de perfiles a los que se dirige una actividad **[!UICONTROL Generar público]**:

* Si hay más de 10 000 perfiles de destino, se envía un mensaje de correo electrónico.
* Para 1000 a 10 000 perfiles, se envía un SMS.
* Si los perfiles destinados caen por debajo de 1000, se les dirige a la transición de “no contactar”.

![](../assets/workflow-test-example.png)

Para ello, se ha utilizado la variable de evento `vars.recCount` en las condiciones “correo electrónico” y “SMS” para contar el número de perfiles de destino y activar la transición adecuada.

![](../assets/workflow-test-example-config.png)
