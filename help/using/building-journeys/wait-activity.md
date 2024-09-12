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
source-git-commit: f81fde0076fc8689c689fae7a0ee8c7aa9fdbeed
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 13%

---

# Actividad de espera {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Actividad de espera"
>abstract="Si desea esperar antes de ejecutar la siguiente actividad en la ruta, puede utilizar una actividad de espera. Permite definir el momento en el que se ejecutará la siguiente actividad. Hay dos opciones disponibles: duración y personalizado."

Puede usar una actividad **[!UICONTROL Wait]** para definir una duración antes de ejecutar la siguiente actividad.  La duración máxima de espera es de **90 días**.

Puede establecer dos tipos de actividad **Wait**:

* Una espera basada en una duración relativa. [Más información](#duration)
* Una fecha personalizada, con funciones para calcularla. [Más información](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Recomendaciones {#wait-recommendations}

### Varias actividades de espera {#multiple-wait-activities}

Cuando use varias actividades **Wait** en un recorrido, tenga en cuenta que el tiempo de espera [global](journey-properties.md#global_timeout) para recorridos es de 91 días, lo que significa que los perfiles siempre abandonan el máximo de recorrido 91 días después de que ingresaron al mismo. Obtenga más información en [esta página](journey-properties.md#global_timeout).

Un individuo puede ingresar a una actividad **Wait** solo si le queda tiempo suficiente en el recorrido recorrido para completar la espera antes del tiempo de espera de 91 días.

### Espera y vuelve a entrar {#wait-re-entrance}

Una práctica recomendada es no usar las actividades **Wait** para bloquear la reentrada. En su lugar, use la opción **Permitir la reentrada** en el nivel de propiedades de recorrido. Obtenga más información en [esta página](../building-journeys/journey-properties.md#entrance).

### Modo de espera y prueba {#wait-test-modd}

En el modo de prueba, el parámetro **[!UICONTROL Tiempo de espera en prueba]** le permite definir el tiempo que durará cada actividad de **Wait**. El tiempo predeterminado es 10 segundos. Esto garantizará que obtenga los resultados de la prueba rápidamente. Obtenga más información en [esta página](../building-journeys/testing-the-journey.md).

## Configuración {#wait-configuration}

### Duración de espera {#duration}

Seleccione el tipo **Duration** para establecer la duración relativa de la espera antes de la ejecución de la siguiente actividad. La duración máxima es de **90 días**.

![Definir la duración de la espera](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### Espera personalizada {#custom}

Seleccione el tipo **Custom** para definir una fecha personalizada, usando una expresión avanzada basada en un campo proveniente de un evento o una respuesta de acción personalizada. No puede definir una duración relativa directamente, por ejemplo, 7 días, pero puede utilizar funciones para calcularla si es necesario (p. ej.: 2 días después de la compra).

![Definir una espera personalizada con una expresión](assets/journey57.png)

La expresión en el editor debe proporcionar un formato `dateTimeOnly`. Consulte [esta página](expression/expressionadvanced.md). Para obtener más información sobre el formato dateTimeOnly, consulte [esta página](expression/data-types.md).

Una práctica recomendada es utilizar fechas personalizadas específicas para los perfiles y evitar utilizar la misma fecha para todos. Por ejemplo, no defina `toDateTimeOnly('2024-01-01T01:11:00Z')`, sino `toDateTimeOnly(@event{Event.productDeliveryDate})`, que es específico de cada perfil. Tenga en cuenta que el uso de fechas fijas puede causar problemas en la ejecución del recorrido.


>[!NOTE]
>
>Puede aprovechar una expresión `dateTimeOnly` o usar una función para convertir a `dateTimeOnly`. Por ejemplo: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, el campo del evento tiene el formato 2023-08-12T09:46:06Z.
>
>Se espera la **zona horaria** en las propiedades del recorrido. Como resultado, desde la interfaz de usuario, no es posible señalar directamente una marca de tiempo ISO-8601 completa que mezcle la hora y el desplazamiento de zona horaria como 2023-08-12T09:46:06.982-05. [Más información](../building-journeys/timezone-management.md).


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

## Nodo de espera automático  {#auto-wait-node}


>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="Acerca del nodo de espera automática"
>abstract="Se agrega automáticamente una actividad **Wait** después de esta actividad. Se establece para 3 días. Puede eliminarlo o configurarlo según sea necesario."

Cada actividad de mensaje entrante (mensaje en la aplicación, experiencia basada en código o tarjeta) viene con una actividad de **Espera** de 3 días. Como los mensajes entrantes finalizan automáticamente cuando un perfil llega al final del recorrido, suponemos que desea que los usuarios lo vean al menos durante 3 días. Puede quitar esta actividad **Wait** o cambiar su configuración si es necesario.