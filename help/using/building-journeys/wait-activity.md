---
solution: Journey Optimizer
product: journey optimizer
title: Actividad Esperar
description: Obtenga información sobre cómo configurar la actividad de espera
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: espera, actividad, recorrido, siguiente, lienzo
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 12%

---

# Actividad Esperar {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Actividad Esperar"
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

Utilice estas recomendaciones para mantener las esperas predecibles y seguras.

### Varias actividades de espera {#multiple-wait-activities}

Cuando use varias actividades **Wait** en un recorrido, tenga en cuenta que el tiempo de espera [global](journey-properties.md#global_timeout) para recorridos es de 91 días, lo que significa que los perfiles siempre abandonan el máximo de recorrido 91 días después de que ingresaron al mismo. Obtenga más información en [esta página](journey-properties.md#global_timeout).

Un individuo puede ingresar a una actividad **Wait** solo si le queda tiempo suficiente en el recorrido recorrido para completar la espera antes del tiempo de espera de 91 días.

### Espera y reentrada {#wait-reentrance}

Una práctica recomendada es no usar las actividades **Wait** para bloquear la reentrada. En su lugar, use la opción **Permitir la reentrada** en el nivel de propiedades de recorrido. Obtenga más información en [esta página](../building-journeys/journey-properties.md#entrance).

### Modo de espera y prueba {#wait-test-mode}

En el modo de prueba, el parámetro **[!UICONTROL Tiempo de espera en prueba]** le permite definir el tiempo que durará cada actividad de **Wait**. El tiempo predeterminado es 10 segundos. Esto garantizará que obtenga los resultados de la prueba rápidamente. Obtenga más información en [esta página](../building-journeys/testing-the-journey.md).

### Canales de espera y móviles {#wait-mobile-channels}

Si desea mostrar un [mensaje en la aplicación](../in-app/create-in-app.md) poco después de enviar una [notificación push](../../rp_landing_pages/push-landing-page.md), use una actividad de **Espera** para permitir que se propague el tiempo de carga del mensaje en la aplicación. Normalmente se recomienda una espera de 5 a 15 minutos, pero los tiempos exactos pueden variar según la complejidad de la carga útil y las necesidades de personalización.

## Configuración {#wait-configuration}

Configure la duración y el tiempo de espera aquí.

### Duración de espera {#duration}

Seleccione el tipo **Duration** para establecer la duración relativa de la espera antes de la ejecución de la siguiente actividad. La duración máxima es de **90 días**.

![Definir la duración de la espera](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![Wait activity configuration panel with duration and fixed date options](assets/journey56.png)

-->

### Espera personalizada {#custom}

Seleccione el tipo **Custom** para definir una fecha personalizada, usando una expresión avanzada basada en un campo proveniente de un evento o una respuesta de acción personalizada. No puede definir una duración relativa directamente, por ejemplo, 7 días, pero puede utilizar funciones para calcularla si es necesario (p. ej.: 2 días después de la compra).

![Definir una espera personalizada con una expresión](assets/journey57.png)

La expresión en el editor debe proporcionar un formato `dateTimeOnly`. Consulte [esta página](expression/expressionadvanced.md). Para obtener más información sobre el formato dateTimeOnly, consulte [esta página](expression/data-types.md).

Una práctica recomendada es utilizar fechas personalizadas específicas para los perfiles y evitar utilizar la misma fecha para todos. Por ejemplo, no defina `toDateTimeOnly('2024-01-01T01:11:00Z')`, sino `toDateTimeOnly(@event{Event.productDeliveryDate})`, que es específico de cada perfil. Tenga en cuenta que el uso de fechas fijas puede causar problemas en la ejecución del recorrido. Obtenga más información acerca del impacto de las actividades de espera en la tasa de procesamiento de recorrido en [esta sección](entry-management.md#wait-activities-impact).


>[!NOTE]
>
>Puede aprovechar una expresión `dateTimeOnly` o usar una función para convertir a `dateTimeOnly`. Por ejemplo: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, el campo del evento tiene el formato 2023-08-12T09:46:06Z.
>
>Se espera la **zona horaria** en las propiedades del recorrido. Como resultado, desde la interfaz de usuario, no es posible señalar directamente una marca de tiempo ISO-8601 completa que mezcle la hora y el desplazamiento de zona horaria como 2023-08-12T09:46:06.982-05. [Más información](../building-journeys/timezone-management.md).

>[!CAUTION]
>
>Al crear una expresión de espera personalizada con `toDateTimeOnly()`, evite anexar &quot;Z&quot; o cualquier desplazamiento de zona horaria (por ejemplo, &quot;-05:00&quot;) en el resultado de la expresión. La expresión debe utilizar una sintaxis de fecha y hora ISO válida que haga referencia a la zona horaria configurada del recorrido sin designadores de zona horaria explícitos.
>
>**Ejemplo correcto:** `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00"))`
>
>**Ejemplo incorrecto:** `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00Z"))` ❌ (contiene &quot;Z&quot;)
>
>El uso de designadores de zona horaria no admitidos puede hacer que los perfiles permanezcan atascados en la actividad de espera en lugar de avanzar según lo esperado.

Para validar que la actividad de espera funciona según lo esperado, puede utilizar eventos de paso. [Más información](../reports/query-examples.md#common-queries).

## Actualización de perfil tras esperar {#profile-refresh}

Cuando un perfil está estacionado en una actividad **Wait** en un recorrido que comienza con una actividad **Read Audience**, el recorrido actualiza automáticamente los atributos del perfil desde el servicio Unified Profile Service (UPS) para recuperar los datos disponibles más recientes.

* **En la entrada de recorrido**: los perfiles utilizan valores de atributo de la instantánea de audiencia que se evaluó cuando se inició el recorrido.
* **Después de un nodo de espera**: el recorrido realiza una búsqueda para recuperar los datos de perfil más recientes de UPS, no los datos de instantánea más antiguos. Esto significa que los atributos del perfil pueden haber cambiado desde que comenzó el recorrido.

Este comportamiento garantiza que las actividades descendentes utilicen la información de perfil actual después de un periodo de espera. Sin embargo, puede producir resultados inesperados si espera que el recorrido utilice únicamente los datos de instantánea originales durante la ejecución.

Ejemplo: Si un perfil se califica para una audiencia de &quot;cliente plata&quot; al inicio del recorrido, pero se actualiza a &quot;cliente oro&quot; durante una espera de 3 días, las actividades posteriores a la espera verán el estado actualizado de &quot;cliente oro&quot;.

## Nodo de espera automático  {#auto-wait-node}

>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="Acerca del nodo de espera automático"
>abstract="Se agrega automáticamente una actividad de **Espera** después de esta actividad. Se establece para 3 días. Puede eliminarla o configurarla según sea necesario."

Cada actividad de experiencia entrante (mensaje en la aplicación, experiencia basada en código o tarjeta) viene con una actividad de **Espera** de 3 días. Como los mensajes entrantes finalizan automáticamente cuando un perfil llega al final del recorrido, suponemos que desea que los usuarios lo vean al menos durante 3 días. Puede quitar esta actividad **Wait** o cambiar su configuración si es necesario.
