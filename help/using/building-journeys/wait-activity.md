---
title: Actividad de espera
description: Descubra la actividad de espera
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 8a68d1e6d498ef3055c703d4e73471ab6d7bff40
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 7%

---

# Actividad de espera{#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Actividad de espera"
>abstract="Si desea esperar antes de ejecutar la siguiente actividad en la ruta, puede utilizar una actividad Wait . Le permite definir el momento en el que se ejecutará la siguiente actividad. Hay tres opciones disponibles: duración, fecha fija y personalizado."

Si desea esperar antes de ejecutar la siguiente actividad en la ruta, puede utilizar un **[!UICONTROL Wait]** actividad. Le permite definir el momento en el que se ejecutará la siguiente actividad. Hay tres opciones disponibles:

* [Duración](#duration)
* [Fecha fija](#fixed_date)
* [Personalizado](#custom)

<!--* [Email send time optimization](#email_send_time_optimization)-->

## Acerca de la actividad Wait{#about_wait}

La duración máxima de espera es de 30 días. En el modo de prueba, la variable **[!UICONTROL Wait time in test]** permite definir el tiempo que durará cada actividad de espera. El valor del tiempo predeterminado es de 10 segundos. Esto garantizará que los resultados de la prueba se obtengan rápidamente. Consulte [esta página](../building-journeys/testing-the-journey.md)

Tenga cuidado al usar varias actividades de Espera en un recorrido, ya que el tiempo de espera de recorrido global es de 30 días, lo que significa que un perfil siempre saldrá del recorrido como máximo 30 días después de que lo haya introducido.

## Espera de duración{#duration}

Seleccione la duración de la espera antes de la ejecución de la siguiente actividad.

![](assets/journey55.png)

## Fecha de espera fija{#fixed_date}

Seleccione la fecha para la ejecución de la siguiente actividad.

![](assets/journey56.png)

## Espera personalizada{#custom}

Esta opción permite definir una fecha personalizada, por ejemplo, 12 de julio de 2020 a las 17:00, mediante una expresión avanzada basada en un campo procedente de un evento o una fuente de datos. No permite definir una duración personalizada, por ejemplo, 7 días. La expresión en el editor de expresiones debe proporcionar un formato dateTimeOnly . Consulte [esta página](expression/expressionadvanced.md). Para obtener más información sobre el formato dateTimeOnly, consulte esta [página](expression/data-types.md).

>[!NOTE]
>
>Puede aprovechar una expresión dateTimeOnly o utilizar una función para convertir a dateTimeOnly. Por ejemplo: toDateTimeOnly(@{Event.offerOpened.activity.endTime}), el campo en el suceso es del formulario 2016-08-12T09:46:06Z.
>
>La variable **zona horaria** se espera en las propiedades del recorrido. Como resultado, hoy en día no es posible desde la interfaz señalar directamente a una marca de tiempo ISO-8601 completa mezclando el tiempo y el desplazamiento de zona horaria como 2016-08-12T09:46:06.982-05. Consulte [esta página](../building-journeys/timezone-management.md).

![](assets/journey57.png)

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you’ll be notified that the default time applies.

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
