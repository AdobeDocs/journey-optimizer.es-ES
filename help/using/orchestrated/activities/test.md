---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Test en las campañas organizadas
description: Aprenda a utilizar la actividad Prueba
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
version: Campaign Orchestration
source-git-commit: b6b74e357029f4924f9699c05af3a0fcd7fcefd6
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 28%

---


# Prueba {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Actividad Prueba"
>abstract="La actividad **Prueba** es una actividad de **Control de flujo**. Permite habilitar transiciones en función de condiciones especificadas."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Condiciones"
>abstract="La actividad **Prueba** puede tener varias transiciones de salida. Durante la ejecución de la campaña orquestada, cada condición se prueba secuencialmente hasta que se cumpla una de ellas. Si no se cumple ninguna de las condiciones, la campaña orquestada continúa por la ruta de la **[!UICONTROL Condición predeterminada]**. Si no se activa ninguna condición predeterminada, la campaña orquestada se detiene en este punto."

La actividad **[!UICONTROL Prueba]** es una actividad de **[!UICONTROL Control de flujo]**. Utilícelo para bifurcar el flujo de campaña activando distintas transiciones según las condiciones definidas. Cada condición puede evaluar los datos de la transición entrante y puede elegir qué transición se ejecuta primero según el orden en que se evalúan las condiciones.

## Configuración de la actividad Prueba {#test-configuration}

Para configurar la actividad **[!UICONTROL Test]**:

1. Suelte una actividad **[!UICONTROL Test]** en el lienzo de la campaña orquestada.

1. De forma predeterminada, la actividad proporciona una sola prueba booleana: cuando se cumple la condición &quot;True&quot;, esa transición se activa; de lo contrario, se activa la transición &quot;False&quot; (predeterminada).

   ![](../assets/test-1.png)

1. Defina la condición para una transición completando estos campos:

   * **Etiqueta**: un nombre para la transición para que pueda identificarla en el lienzo.

   * **Tipo de condición**: Los datos que se van a evaluar, de manera predeterminada, en el recuento de población.

   * **Operador**: La comparación que se va a aplicar, por ejemplo, igual a, mayor que, menor que. La lista de operadores depende del tipo de datos del tipo de condición.

   * **Valor**: Valor con el que comparar el tipo de condición.

   ![](../assets/test-2.png)

1. Para bifurcar más de dos resultados, haga clic en **[!UICONTROL Agregar condición]** y defina una etiqueta y una condición para cada transición adicional.

1. En tiempo de ejecución, la campaña evalúa las condiciones en orden y sigue a la primera que coincide. Cuando no coincide ninguna condición, la ejecución sigue **[!UICONTROL Condición predeterminada]** si se establece una; de lo contrario, la campaña se detiene en la actividad **[!UICONTROL Test]**.

## Ejemplo {#example}

En este ejemplo, se activan diferentes transiciones en función del número de perfiles objetivo por una actividad **[!UICONTROL Generar audiencia]**. Las condiciones se evalúan en orden; la última transición es la predeterminada y se utiliza cuando no coincide ninguna condición anterior.

* Si hay más de 10 000 perfiles de destino, se envía un mensaje de correo electrónico.
* Default (sin coincidencia de condición): cuando el recuento es de 10 000 o menos, la población se dirige a una transición de &quot;no contactar&quot;.

![](../assets/workflow-test-example.png)
