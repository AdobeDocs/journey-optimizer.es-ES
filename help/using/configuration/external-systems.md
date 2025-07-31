---
solution: Journey Optimizer
product: journey optimizer
title: Integración de Journey Optimizer con sistemas externos
description: Conozca las prácticas recomendadas al integrar Journey Optimizer con sistemas externos
feature: Integrations
role: User
level: Beginner
keywords: externo, API, optimizador, límite
exl-id: 27859689-dc61-4f7a-b942-431cdf244455
source-git-commit: 0a6db9c9537563fea5d56289d78b9ed49d703734
workflow-type: tm+mt
source-wordcount: '1352'
ht-degree: 26%

---

# Integración con sistemas externos {#external-systems}

Esta página presenta las diferentes protecciones proporcionadas por Journey Optimizer al integrar un sistema externo, así como las prácticas recomendadas: cómo optimizar la protección del sistema externo mediante la API de límite, cómo configurar el tiempo de espera de recorrido y cómo funcionan los reintentos.

Journey Optimizer le permite configurar conexiones a sistemas externos mediante fuentes de datos y acciones personalizadas. Esto le permite, por ejemplo, enriquecer sus recorridos con datos procedentes de un sistema de reservas externo o enviar mensajes mediante un sistema de terceros como Epsilon o Facebook.

Al integrar un sistema externo, puede encontrar varios problemas, el sistema puede ser lento, puede dejar de responder o es posible que no pueda gestionar un volumen grande. Journey Optimizer ofrece varias protecciones para proteger el sistema de la sobrecarga.

Todos los sistemas externos son diferentes en términos de rendimiento. Debe adaptar la configuración a sus casos de uso.

Cuando Journey Optimizer ejecuta una llamada a una API externa, las protecciones técnicas se ejecutan de la siguiente manera:

1. Se aplican reglas de límite o restricción: si se alcanza la tasa máxima, las llamadas restantes se descartan o se ponen en cola.

1. Tiempo de espera y reintento: si se cumple la regla de límite o regulación, Journey Optimizer intenta realizar la llamada hasta que se alcanza el final de la duración del tiempo de espera.

>[!TIP]
>
>Se recomienda dejar al menos un minuto de búfer entre el período de caducidad del token de la API externa y la configuración de Journey Optimizer [`cacheDuration` ](../datasource/external-data-sources.md#custom-authentication-access-token), especialmente en cargas de trabajo pesadas, para evitar discrepancias de caducidad y errores 401.

## API de límite y restricción {#capping}

### Acerca de las API de restricción y límite

Al configurar una fuente de datos o una acción, se establece una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos o enviar mensajes o llamadas de API.

Las API de recorridos admiten hasta 5.000 eventos por segundo, pero es posible que algunos sistemas externos o API no tengan un rendimiento equivalente. Para evitar sobrecargar estos sistemas, puede usar las API **Límite** y **Aceleración** para limitar el número de eventos enviados por segundo.

Cada vez que recorrido realiza una llamada a la API, esta pasa por el motor de API. Si se alcanza el límite establecido en la API, la llamada se rechaza si se utiliza la API de límite, o se pone en cola durante un máximo de 6 horas y se procesa lo antes posible en el orden en que se recibió si se utiliza la API de limitación.

Por ejemplo, supongamos que ha definido una regla de límite o restricción de 200 llamadas por segundo para el sistema externo. Una acción personalizada llama al sistema en 10 recorridos diferentes. Si un recorrido recibe 300 llamadas por segundo, utilizará las 200 ranuras disponibles y descartará o pondrá en cola las 100 restantes. Como la velocidad máxima se ha superado, los otros 9 recorridos no tendrán ninguna ranura. Esta granularidad ayuda a proteger el sistema externo de sobrecargas y caídas.

>[!IMPORTANT]
>
>**Las reglas de límite** se configuran en el nivel de zona protegida, para un extremo específico (la dirección URL llamada) pero global para todos los recorridos de dicha zona protegida. El límite está disponible tanto en fuentes de datos como en acciones personalizadas.
>
>Las **Reglas de limitación** solo están configuradas en zonas protegidas de producción, para un extremo específico, pero de forma global para todos los recorridos de todas las zonas protegidas. Solo puede tener una configuración de restricción por organización. La restricción solo está disponible en acciones personalizadas.
>
>El valor **maxCallsCount** debe ser mayor que 1.

Para obtener más información sobre cómo trabajar con las API, consulte estas secciones:

* [API de límite](capping.md)
* [API de limitación](throttling.md)

Hay disponible una descripción detallada de las API en [Documentación de las API de Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)

### Capacidad de fuentes de datos y acciones personalizadas {#capacity}

Para **fuentes de datos externas**, el número máximo de llamadas por segundo está limitado a 15. Si se supera este límite, las llamadas adicionales se descartan o se ponen en cola según la API en uso. Es posible aumentar este límite para las fuentes de datos externas privadas poniéndose en contacto con Adobe para incluir en la lista de permitidos el extremo, pero esto no es una opción para las fuentes de datos externas públicas. * [Obtenga información sobre cómo configurar fuentes de datos](../datasource/about-data-sources.md).

>[!NOTE]
>
>Si una fuente de datos utiliza una autenticación personalizada con un extremo diferente al que se usa para la fuente de datos, debe ponerse en contacto con Adobe para incluir en la lista de permitidos también este.

Para **acciones personalizadas**, debe evaluar la capacidad de su API externa. Por ejemplo, si Journey Optimizer envía 1000 llamadas por segundo y el sistema solo puede admitir 200, debe definir una configuración de límite o de limitación para que el sistema no se sature. [Obtenga información sobre cómo configurar acciones](../action/action.md)

>[!NOTE]
>
>Como las respuestas ahora son compatibles, debe utilizar acciones personalizadas en lugar de fuentes de datos para casos de uso de fuentes de datos externas. Para obtener más información sobre las respuestas, consulte esta [sección](../action/action-response.md)

## Tiempo de espera y reintentos{#timeout}

Si se cumple la regla de límite o restricción, se aplica la regla de tiempo de espera.

En cada recorrido, puede definir una duración de tiempo de espera. Esto le permite establecer una duración máxima al llamar a un sistema externo. La duración del tiempo de espera se configura en las propiedades de un recorrido. Consulte [esta página](../building-journeys/journey-properties.md#timeout_and_error).

Este tiempo de espera es global para todas las llamadas externas (llamadas a API externas en acciones personalizadas y fuentes de datos personalizadas). De forma predeterminada, se establece en 30 segundos.

Durante el tiempo de espera definido, Journey Optimizer intenta llamar al sistema externo. Después de la primera llamada, se puede realizar un máximo de tres reintentos hasta que se alcance el final de la duración del tiempo de espera. No se puede cambiar el número de reintentos.

Cada reintento utiliza una ranura. Si tiene un límite de 100 llamadas por segundo y cada una de las llamadas requiere dos reintentos, la tasa cae a 30 llamadas por segundo (cada llamada utiliza 3 ranuras: la primera llamada y dos reintentos).

El valor de duración del tiempo de espera depende del caso de uso. Si desea enviar el mensaje rápidamente, por ejemplo, cuando el cliente entra en el almacén, no desea configurar un tiempo de espera largo. Además, cuanto más tiempo de espera sea, más elementos se pondrán en cola. Esto puede afectar en gran medida al rendimiento. Si Journey Optimizer realiza 1000 llamadas por segundo, mantener 5 o 15 segundos de datos puede saturar rápidamente al sistema.

Veamos un ejemplo para un tiempo de espera de 5 segundos.

* La primera llamada dura menos de 5 segundos: la llamada se realiza correctamente, no se realiza ningún reintento.
* La primera llamada dura más de 5 segundos: la llamada se cancela y no hay reintento. Se cuenta como un error de tiempo de espera en los informes.
* La primera llamada falla después de 2 segundos (el sistema externo devuelve un error): quedan 3 segundos para los reintentos, si están disponibles los espacios de límite.
   * Si uno de los tres reintentos se realiza correctamente antes del final de los 5 segundos, se realiza la llamada y no hay ningún error.
   * Si se alcanza el final de la duración del tiempo de espera durante los reintentos, la llamada se cancela y se cuenta como un error de tiempo de espera en el sistema de informes.

## Preguntas frecuentes{#faq}

**¿Cómo puedo configurar una regla de restricción o límite? ¿Hay una regla predeterminada?**

Para crear reglas de restricción o límite, consulte [esta sección](../configuration/external-systems.md#capping). De forma predeterminada, no hay ninguna regla de restricción, pero se establece un límite de 300 000 llamadas durante un minuto para todas las acciones personalizadas, por host y por zona protegida. Este límite se ha establecido en función del uso de los clientes para proteger los extremos externos dirigidos por acciones personalizadas. Si es necesario, puede anular esta configuración definiendo un límite o restricción mayor mediante nuestras API de límite/restricción.

**¿Cuántos reintentos se realizan? ¿Puedo cambiar el número de reintentos o definir un período de espera mínimo entre reintentos?**

Para una llamada determinada, se puede realizar un máximo de tres reintentos después de la primera llamada, hasta que se alcance el final de la duración del tiempo de espera. No se puede cambiar el número de reintentos ni el tiempo entre cada reintento. Consulte [esta sección](../configuration/external-systems.md#timeout).

**¿Dónde puedo configurar el tiempo de espera? ¿Hay un valor máximo?**

En cada recorrido, puede definir una duración de tiempo de espera. La duración del tiempo de espera se configura en las propiedades de un recorrido. La duración del tiempo de espera debe estar entre 1 segundo y 30 segundos. Consulte [esta sección](../configuration/external-systems.md#timeout) y [esta página](../building-journeys/journey-properties.md#timeout_and_error).