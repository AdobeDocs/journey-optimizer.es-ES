---
solution: Journey Optimizer
product: journey optimizer
title: Utilice el actividad de prueba en las campañas organizadas
description: Aprenda a utilizar el actividad de prueba
hide: true
hidefromtoc: true
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 16%

---

# Prueba {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Actividad de prueba"
>abstract="La actividad **Prueba** es una actividad de **Control de flujo**. Permite habilitar transiciones en función de condiciones especificadas."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Condiciones"
>abstract="La actividad **Prueba** puede tener varias transiciones de salida. Durante la ejecución campaña orquestada, cada condición se prueba secuencialmente hasta que se cumple una de ellas. Si no se cumple ninguna de las condiciones, la campaña orquestada continúa por la ruta de la **[!UICONTROL condición]** predeterminada. Si no se activa ninguna condición predeterminada, la campaña orquestada se detiene en este punto."

La actividad **Prueba** es una actividad de **Control de flujo**. Permite habilitar transiciones en función de condiciones especificadas.

## Configurar el actividad de prueba {#test-configuration}

Siga estos pasos para configurar el **actividad de prueba** :

1. añadir un actividad de **prueba** a su campaña orquestado.

1. De forma predeterminada, el **[!UICONTROL actividad de prueba]** presenta un prueba booleano simple. Si se cumple la condición definida en el transición &quot;True&quot;, se activará este transición. De lo contrario, se activará un transición predeterminado &quot;False&quot;.

1. Para configurar la condición asociada a un transición, haga clic en el icono de **[!UICONTROL diálogo Abrir]** personalización. Utilice el editor expresión para definir las reglas necesarias para activar este transición. También puede impulsar evento variables, condiciones y funciones de fecha y hora. [Aprenda a trabajar con variables evento y con el expresión editor](../event-variables.md)

   Además, puede modificar el **[!UICONTROL campo Etiquetar]** para personalizar el nombre del transición en el lienzo del campaña orquestado.

   ![](../assets/workflow-test-default.png)

1. Puede agregar varias transiciones de salida a una **[!UICONTROL actividad de prueba]** . Para ello, haga clic en el botón condición **** de añadir y configure la etiqueta y la condición asociada para cada transición.
v
1. Durante la ejecución campaña orquestada, cada condición se prueba secuencialmente hasta que se cumple una de ellas. Si no se cumple ninguna de las condiciones, las campañas orquestadas continúan por la ruta de la **[!UICONTROL condición]** predeterminada. Si no se activa ninguna condición predeterminada, el flujo de trabajo se detienen en este punto.

## Ejemplo {#example}

En este ejemplo, se activan diferentes transiciones en función del número de perfiles segmentados por un **[!UICONTROL actividad de audiencia]** de compilación:

* Si se segmentan más de 10000 perfiles, se envía un mensaje correo electrónico.
* Se envía un SMS para 1000 a 10.000 perfiles.
* Si los perfiles objetivo son inferiores a 1.000, se les dirige a un transición de &quot;no contacto&quot;.

![](../assets/workflow-test-example.png)

Para ello, se ha aprovechado el `vars.recCount` variable evento en las condiciones &quot;correo electrónico&quot; y &quot;sms&quot; para contar el número de perfiles objetivo y activar el transición adecuado.

![](../assets/workflow-test-example-config.png)
