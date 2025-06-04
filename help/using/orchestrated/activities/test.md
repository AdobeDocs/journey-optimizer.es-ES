---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Test en las campañas orquestadas
description: Descubra más información sobre cómo utilizar la actividad Test
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
source-git-commit: c46c202d68613f08e2d2b23ea882fb6561669b08
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 28%

---

# Prueba {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Actividad de prueba"
>abstract="La actividad **Prueba** es una actividad de **Control de flujo**. Permite habilitar transiciones en función de condiciones especificadas."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Condiciones"
>abstract="La actividad **Prueba** puede tener varias transiciones de salida. Durante la ejecución de la campaña orquestada, cada condición se prueba secuencialmente hasta que se cumpla una de ellas. Si no se cumple ninguna de las condiciones, la campaña orquestada continúa por la ruta de la **[!UICONTROL Condición predeterminada]**. Si no se activa ninguna condición predeterminada, la campaña orquestada se detiene en este punto."

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicie su primera campaña orquestada | Consultar la base de datos | Actividades de campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](../configuration-steps.md)<br/><br/>[Pasos clave para la creación de campañas orquestadas](../gs-campaign-creation.md) | [Crear una campaña orquestada](../create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](../orchestrate-activities.md)<br/><br/>[Enviar mensajes con campañas orquestadas](../send-messages.md)<br/><br/>[Iniciar y supervisar la campaña](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabaje con el Modeler de consultas](../orchestrated-query-modeler.md)<br/><br/>[Cree su primera consulta](../build-query.md)<br/><br/>[Editar expresiones](../edit-expressions.md) | [Empiece con las actividades](about-activities.md)<br/><br/>Actividades:<br/>[Y únase](and-join.md) - [Generar audiencia](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Combinar](combine.md) - [Anulación de duplicación](/deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [División](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

La actividad **Prueba** es una actividad de **Control de flujo**. Permite habilitar transiciones en función de condiciones especificadas.

## Configuración de la actividad Test {#test-configuration}

Siga estos pasos para configurar la actividad **Test**:

1. Agregue una actividad **Test** a su campaña organizada.

1. De manera predeterminada, la actividad **[!UICONTROL Test]** presenta una prueba booleana simple. Si se cumple la condición definida en la transición &quot;True&quot;, se activa esta transición. De lo contrario, se activa una transición predeterminada &quot;False&quot;.

1. Para configurar la condición asociada a una transición, haga clic en el icono **[!UICONTROL Abrir cuadro de diálogo de personalización]**. Utilice el editor de expresiones para definir las reglas necesarias para activar esta transición. También puede aprovechar variables de eventos, condiciones y funciones de fecha y hora.

   Además, puede modificar el campo **[!UICONTROL Label]** para personalizar el nombre de la transición en el lienzo de campaña organizado.

   ![](../assets/workflow-test-default.png)

1. Puede agregar varias transiciones de salida a una actividad **[!UICONTROL Test]**. Para ello, haga clic en el botón **[!UICONTROL Agregar condición]** y configure la etiqueta y la condición asociada para cada transición.
v
1. Durante la ejecución de la campaña orquestada, cada condición se prueba secuencialmente hasta que se cumpla una de ellas. Si no se cumple ninguna de las condiciones, las campañas orquestadas continúan en la ruta de la **[!UICONTROL condición predeterminada]**. Si no se activa ninguna condición predeterminada, el flujo de trabajo se detienen en este punto.

## Ejemplo {#example}

En este ejemplo, se activan diferentes transiciones en función del número de perfiles objetivo por una actividad **[!UICONTROL Generar audiencia]**:

* Si hay más de 10 000 perfiles de destino, se envía un mensaje de correo electrónico.
* Para entre 1000 y 10 000 perfiles, se envía un SMS.
* Si los perfiles objetivo caen por debajo de 1000, se les dirige a una transición de &quot;no contactar&quot;.

![](../assets/workflow-test-example.png)

Para ello, la variable de evento `vars.recCount` se ha aprovechado en las condiciones &quot;correo electrónico&quot; y &quot;sms&quot; para contar el número de perfiles de destino y activar la transición adecuada.

![](../assets/workflow-test-example-config.png)
