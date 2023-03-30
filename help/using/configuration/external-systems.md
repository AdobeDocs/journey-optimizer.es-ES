---
solution: Journey Optimizer
product: journey optimizer
title: Integración de Journey Optimizer con sistemas externos
description: Conozca las prácticas recomendadas al integrar Journey Optimizer con sistemas externos
role: User
level: Beginner
keywords: externa, API, optimizer, restricción
exl-id: 27859689-dc61-4f7a-b942-431cdf244455
source-git-commit: 65da82fd67442cfa2b5d45ec753fb3c5a86d4cc7
workflow-type: tm+mt
source-wordcount: '1197'
ht-degree: 3%

---

# Integración con sistemas externos {#external-systems}

Esta página presenta las diferentes protecciones proporcionadas por Journey Optimizer al integrar un sistema externo, así como las prácticas recomendadas: cómo optimizar la protección del sistema externo mediante la API de límite, cómo configurar el tiempo de espera del recorrido y cómo funcionan los reintentos.

Journey Optimizer le permite configurar conexiones a sistemas externos mediante fuentes de datos y acciones personalizadas. Esto le permite, por ejemplo, enriquecer sus recorridos con datos procedentes de un sistema de reservas externo o enviar mensajes mediante un sistema de terceros como Epsilon o Facebook.

Al integrar un sistema externo, puede encontrar varios problemas, el sistema puede ser lento, puede dejar de responder o puede no ser capaz de manejar un gran volumen. Journey Optimizer ofrece varias barreras para proteger el sistema de sobrecarga.

Todos los sistemas externos son diferentes en términos de rendimiento. Debe adaptar la configuración a sus casos de uso.

Cuando Journey Optimizer ejecuta una llamada a una API externa, las protecciones técnicas se ejecutan de la siguiente manera:

1. Se aplican reglas de restricción o restricción: si se alcanza la tasa máxima, las llamadas restantes se descartan o se ponen en cola.

2. Tiempo de espera y reintento: si se cumple la regla de límite, Journey Optimizer intenta realizar la llamada hasta que se alcance el final del tiempo de espera.

## Restricción y restricción de las API {#capping}

### Acerca de las API de restricción y restricción

Al configurar una fuente de datos o una acción, se establece una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos o enviar mensajes o llamadas API.

Las API de Recorrido admiten hasta 5000 eventos por segundo, pero es posible que algunos sistemas externos o API no tengan un rendimiento equivalente. Para evitar sobrecargar estos sistemas, puede usar la variable **Restricción** y **Restricción** para limitar el número de eventos enviados por segundo.

Cada vez que recorrido realiza una llamada a la API, esta pasa por el motor de API. Si se alcanza el límite establecido en la API, la llamada de se rechaza si utiliza la API de restricción o se pone en cola y se procesa lo antes posible en el orden en que se recibieron si utiliza la API de restricción.

Por ejemplo, supongamos que ha definido una regla de límite o restricción de 100 llamadas por segundo para su sistema externo. Una acción personalizada llama al sistema en 10 recorridos diferentes. Si un recorrido recibe 200 llamadas por segundo, utilizará las 100 ranuras disponibles y descartará o pondrá en cola las 100 ranuras restantes. Como la velocidad máxima se ha superado, los otros 9 recorridos no tendrán ninguna ranura. Esta granularidad ayuda a proteger el sistema externo de sobrecargas y caídas.

>[!IMPORTANT]
>
>**Reglas de restricción** se configuran en el nivel de entorno limitado, para un punto final específico (la dirección URL denominada) pero global para todos los recorridos de ese entorno limitado.
>
>**Reglas de restricción** solo están configuradas en entornos limitados de producción, para un punto final específico pero globales para todos los recorridos de todos los entornos limitados. Solo puede tener una configuración de regulación por organización.

Para obtener más información sobre cómo trabajar con las API, consulte estas secciones:

* [Captación de API](capping.md)
* [API de restricción](throttling.md)

Puede encontrar una descripción detallada de las API en [Documentación de las API de Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)

### Fuentes de datos y capacidad de acciones personalizadas {#capacity}

Para **fuentes de datos externas**, el número máximo de llamadas por segundo está limitado a 15. Si se supera este límite, las llamadas adicionales se descartan o se ponen en cola según la API en uso. Es posible aumentar este límite para las fuentes de datos externas privadas poniéndose en contacto con el Adobe para incluir el punto final en la lista de permitidos, pero esta no es una opción para las fuentes de datos externas públicas. * [Obtenga información sobre cómo configurar fuentes de datos](../datasource/about-data-sources.md).

>[!NOTE]
>
>Si una fuente de datos utiliza una autenticación personalizada con un extremo diferente al que se usa para la fuente de datos, debe ponerse en contacto con Adobe para incluir también ese extremo en la lista de permitidos.

Para **acciones personalizadas**, debe evaluar la capacidad de su API externa. Por ejemplo, si Journey Optimizer envía 1000 llamadas por segundo y el sistema solo puede admitir 100 llamadas por segundo, debe definir una configuración de límite o de regulación para que el sistema no se satura. [Obtenga información sobre cómo configurar acciones](../action/action.md)

## Tiempo de espera y reintentos{#timeout}

Si se cumple la regla de restricción o restricción, se aplica la regla de tiempo de espera.

En cada recorrido, puede definir una duración de tiempo de espera. Esto le permite establecer una duración máxima al llamar a un sistema externo. La duración del tiempo de espera se configura en las propiedades de un recorrido. Consulte [esta página](../building-journeys/journey-gs.md#timeout_and_error).

Este tiempo de espera es global para todas las llamadas externas (llamadas de API externas en acciones personalizadas y fuentes de datos personalizadas). De forma predeterminada, se establece en 30 segundos.

Durante el tiempo de espera definido, Journey Optimizer intenta llamar al sistema externo. Después de la primera llamada, se puede realizar un máximo de tres reintentos hasta que se alcance el final del tiempo de espera. El número de reintentos no se puede cambiar.

Cada reintento utiliza una ranura. Si tiene un límite de 100 llamadas por segundo y cada una de sus llamadas requiere dos reintentos, la tasa baja a 30 llamadas por segundo (cada llamada utiliza 3 ranuras: la primera llamada y dos reintentos).

El valor de duración de tiempo de espera depende del caso de uso. Si desea enviar el mensaje rápidamente, por ejemplo, cuando el cliente entra en la tienda, no desea configurar un tiempo de espera largo. Además, cuanto más tiempo sea el tiempo de espera, más elementos se colocarán en cola. Esto puede afectar en gran medida al rendimiento. Si Journey Optimizer realiza 1000 llamadas por segundos, mantener 5 o 15 segundos de datos puede sobrecargar rápidamente el sistema.

Veamos un ejemplo para un tiempo de espera de 5 segundos.

* La primera llamada dura menos de 5 segundos: la llamada se ha realizado correctamente y no se ha realizado ningún reintento.
* La primera llamada dura más de 5 segundos: la llamada se cancela y no hay reintento. Se cuenta como un error de tiempo de espera en los informes.
* La primera llamada falla después de 2 segundos (el sistema externo devuelve un error): Quedan 3 segundos para los reintentos, si hay ranuras de límite disponibles.
   * Si uno de los tres reintentos se realiza correctamente antes del final de los 5 segundos, la llamada se realiza y no hay error.
   * Si se alcanza el final de la duración del tiempo de espera durante los reintentos, la llamada se cancela y se cuenta como un error de tiempo de espera en los informes.

## Preguntas frecuentes{#faq}

**¿Cómo puedo configurar una regla de restricción o restricción? ¿Hay una regla predeterminada?**

De forma predeterminada, no hay ninguna regla de restricción o restricción. Las reglas se definen a nivel de entorno limitado para un punto final específico (la URL denominada) mediante el uso de la API de restricción o restricción. Consulte [esta sección](../configuration/external-systems.md#capping).

**¿Cuántos reintentos se realizan? ¿Puedo cambiar el número de reintentos o definir un periodo de espera mínimo entre los reintentos?**

Para una llamada determinada, se puede realizar un máximo de tres reintentos después de la primera llamada, hasta que se alcance el final de la duración del tiempo de espera. El número de reintentos y el tiempo entre cada reintento no se pueden cambiar. Consulte [esta sección](../configuration/external-systems.md#timeout).

**¿Dónde puedo configurar el tiempo de espera? ¿Hay un valor máximo?**

En cada recorrido, puede definir una duración de tiempo de espera. La duración del tiempo de espera se configura en las propiedades de un recorrido. La duración del tiempo de espera debe estar entre 1 segundo y 30 segundos. Consulte [esta sección](../configuration/external-systems.md#timeout) y [esta página](../building-journeys/journey-gs.md#timeout_and_error).