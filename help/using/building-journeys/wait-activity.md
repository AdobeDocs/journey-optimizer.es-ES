---
solution: Journey Optimizer
product: journey optimizer
title: Actividad de espera
description: Obtenga información sobre cómo configurar la actividad de espera
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: espera, actividad, recorrido, siguiente, lienzo
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: e5b32629dac368855df09313edaad55e3bc143dc
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 15%

---

# Actividad de espera {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Actividad de espera"
>abstract="Si desea esperar antes de ejecutar la siguiente actividad en la ruta, puede utilizar una actividad de espera. Permite definir el momento en el que se ejecutará la siguiente actividad. Hay dos opciones disponibles: duración y personalizado."

Puede usar un **[!UICONTROL Esperar]** actividad para definir una duración antes de ejecutar la siguiente actividad.  La duración máxima de espera es **29 días**.

Puede establecer dos tipos de **Esperar** actividad:

* Una espera basada en una duración relativa. [Más información](#duration)
* Una fecha personalizada, con funciones para calcularla. [Más información](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Recomendaciones {#wait-recommendations}

### Varias actividades de espera {#multiple-wait-activities}

Cuando se usan varios **Esperar** actividades en un recorrido, tenga en cuenta que la variable [tiempo de espera global](journey-properties.md#global_timeout) para recorridos es 91 días, lo que significa que los perfiles siempre abandonan el recorrido máximo 91 días después de introducirlo. Obtenga más información en [esta página](journey-properties.md#global_timeout).

Un individuo puede introducir una **Esperar** actividad solo si le queda tiempo suficiente en el recorrido recorrido para completar la espera antes del tiempo de espera de 91 días.

### Espera y vuelve a entrar {#wait-re-entrance}

Una práctica recomendada que no debe utilizar **Esperar** actividades para bloquear la reentrada. En su lugar, utilice el **Permitir la reentrada** en el nivel de propiedades del recorrido. Obtenga más información en [esta página](../building-journeys/journey-properties.md#entrance).

### Modo de espera y prueba {#wait-test-modd}

En el modo de prueba, la variable **[!UICONTROL Tiempo de espera en la prueba]** permite definir la hora a la que cada **Esperar** la actividad durará. El tiempo predeterminado es 10 segundos. Esto garantizará que obtenga los resultados de la prueba rápidamente. Obtenga más información en [esta página](../building-journeys/testing-the-journey.md).

## Configuración {#wait-configuration}

### Duración de espera {#duration}

Seleccione el **Duración** escriba para establecer la duración relativa de la espera antes de la ejecución de la siguiente actividad. La duración máxima es **29 días**.

![Definición de la duración de espera](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### Espera personalizada {#custom}

Seleccione el **Personalizado** escriba para definir una fecha personalizada, utilizando una expresión avanzada basada en un campo proveniente de un evento o una respuesta de acción personalizada. No puede definir una duración relativa directamente, por ejemplo, 7 días, pero puede utilizar funciones para calcularla si es necesario (p. ej.: 2 días después de la compra).

![Definir una espera personalizada con una expresión](assets/journey57.png)

La expresión del editor debe proporcionar un `dateTimeOnly` formato. Consulte [esta página](expression/expressionadvanced.md). Para obtener más información sobre el formato dateTimeOnly, consulte [esta página](expression/data-types.md).

Una práctica recomendada es utilizar fechas personalizadas específicas para los perfiles y evitar utilizar la misma fecha para todos. Por ejemplo, no defina `toDateTimeOnly('2024-01-01T01:11:00Z')` sino más bien `toDateTimeOnly(@event{Event.productDeliveryDate})` que es específico de cada perfil. Tenga en cuenta que el uso de fechas fijas puede causar problemas en la ejecución del recorrido.


>[!NOTE]
>
>Puede aprovechar una `dateTimeOnly` expresión o utilice una función para convertirla en una `dateTimeOnly`. Por ejemplo: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, el campo en el evento tiene el formato 2023-08-12T09:46:06Z.
>
>El **zona horaria** se espera en las propiedades del recorrido. Como resultado, desde la interfaz de usuario, no es posible apuntar directamente a una marca de tiempo ISO-8601 completa que mezcle la hora y el desplazamiento de zona horaria como 2023-08-12T09:46:06.982-05. [Más información](../building-journeys/timezone-management.md).


Para validar que la actividad de espera funciona según lo esperado, puede utilizar eventos de paso. [Más información](../reports/query-examples.md#common-queries).

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
