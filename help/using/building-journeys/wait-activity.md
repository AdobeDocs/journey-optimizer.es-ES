---
solution: Journey Optimizer
product: journey optimizer
title: Actividad de espera
description: Descubra más información sobre la actividad de espera
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: espera, actividad, recorrido, siguiente, lienzo
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 17%

---

# Actividad de espera{#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Actividad de espera"
>abstract="Si desea esperar antes de ejecutar la siguiente actividad en la ruta, puede utilizar una actividad de espera. Permite definir el momento en el que se ejecutará la siguiente actividad. Hay dos opciones disponibles: duración y personalizado."

Si desea esperar antes de ejecutar la siguiente actividad en la ruta, puede utilizar un **[!UICONTROL Esperar]** actividad. Permite definir el momento en el que se ejecutará la siguiente actividad. Las opciones disponibles son las siguientes:

* [Duración](#duration)
* [Personalizado](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Acerca de la actividad Espera{#about_wait}

La duración máxima de la espera es de 29 días. En el modo de prueba, la variable **[!UICONTROL Tiempo de espera en la prueba]** permite definir el tiempo que durará cada actividad de espera. El tiempo predeterminado es 10 segundos. Esto garantizará que obtenga los resultados de la prueba rápidamente. Consulte [esta página](../building-journeys/testing-the-journey.md).

Tenga cuidado al usar varias actividades de Espera en un recorrido, ya que el tiempo de espera de recorrido global es de 30 días, lo que significa que un perfil siempre abandonará el máximo de recorrido 30 días después de introducirlo. Consulte [esta página](../building-journeys/journey-gs.md#global_timeout).

Un individuo solo puede entrar a una actividad de espera si le queda tiempo suficiente en el recorrido recorrido para completar la duración de la espera antes del tiempo de espera de 30 días. Por ejemplo, si agrega dos actividades de espera configuradas a 20 días cada una, el sistema detectará que la segunda espera finaliza después del tiempo de espera de 30 días. Por lo tanto, la segunda espera se ignora y el individuo sale del recorrido antes de iniciarlo. En ese ejemplo, el cliente permanecerá 20 días en total en el recorrido.

Se recomienda no utilizar esperas para bloquear la reentrada. En su lugar, utilice el **Permitir la reentrada** en el nivel de propiedades del recorrido. Consulte [esta página](../building-journeys/journey-gs.md#entrance).

## Duración de espera{#duration}

Seleccione la duración de la espera antes de la ejecución de la siguiente actividad. La duración máxima es de 29 días.

![](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

## Espera personalizada{#custom}

Esta opción le permite definir una fecha personalizada, por ejemplo, el 12 de julio de 2023 a las 17:00, mediante una expresión avanzada basada en un campo proveniente de un evento o una fuente de datos. No permite definir una duración personalizada, por ejemplo, de 7 días. La expresión en el editor de expresiones debe proporcionar un formato dateTimeOnly. Consulte esta sección [página](expression/expressionadvanced.md). Para obtener más información sobre el formato dateTimeOnly, consulte esto [página](expression/data-types.md).

>[!NOTE]
>
>Puede aprovechar una expresión dateTimeOnly o utilizar una función para convertirla en dateTimeOnly. Por ejemplo: toDateTimeOnly(@event{Event.offerOpened.activity.endTime}), siendo el campo del evento del formulario 2023-08-12T09:46:06Z.
>
>El **zona horaria** se espera en las propiedades del recorrido. Como resultado, hoy en día no es posible desde la interfaz señalar directamente a una marca de tiempo ISO-8601 completa que mezcle la hora y el desplazamiento de zona horaria como 2023-08-12T09:46:06.982-05. Consulte [esta página](../building-journeys/timezone-management.md).

![](assets/journey57.png)

Para validar que la actividad de espera funciona según lo esperado, puede utilizar eventos de paso. Consulte [esta página](../reports/query-examples.md#common-queries).

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you'll be notified that the default time applies.

>[!NOTE]
>
>The first event of your journey must have a namespace.
>
>This capability is only available after an **[!UICONTROL Email]** activity. You need to have Adobe Campaign Standard.

1. In the **[!UICONTROL Amount of time]** field, define the number of hours to consider to optimize email sending.
1. In the **[!UICONTROL Optimization type]** field, choose if the optimization should increase clicks or opens.
1. In the **[!UICONTROL Default time]** field, define the default time to wait if the predictive send time score is not available.

    >[!NOTE]
    >
    >Note that the send time score can be unavailable because there is not enough data to perform the calculation. In this case, you will be informed, at publication time, that the default time applies.

![](assets/journey57bis.png)-->
