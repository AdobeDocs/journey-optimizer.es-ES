---
solution: Journey Optimizer
product: journey optimizer
title: Búsqueda de eventos de experiencia en recorrido
description: Aprenda a utilizar la búsqueda de eventos de experiencia en recorrido
exl-id: 35e2e347-0669-44a3-92ba-aee52e54c219
version: Journey Orchestration
source-git-commit: c4f6b7754255ce3bf0229702b10955abf9843548
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 6%

---

# Búsqueda de eventos de experiencia en recorrido {#ee-journeys}

>[!CAUTION]
>
>A partir del 8 de julio de 2025, en las nuevas organizaciones de clientes, la creación de expresiones mediante eventos de experiencia ya no se admite en el editor de expresiones utilizado en las condiciones de recorrido. Como resultado, no se pueden usar eventos de experiencia en la [fuente de datos de Experience Platform](../datasource/adobe-experience-platform-data-source.md) para crear expresiones. A continuación, se hace referencia a enfoques alternativos y prácticas recomendadas para crear expresiones/lógica con eventos de experiencia.
>
>¿Necesita más detalles? [Lea las preguntas frecuentes](#faq-ee).

Esta página describe patrones comunes y enfoques escalables para ayudarle a sacar el máximo partido a los eventos de experiencia en Adobe Journey Optimizer. Estos casos de uso están diseñados para ayudarle a resolver los desafíos frecuentes, como administrar las exclusiones, controlar la frecuencia de los mensajes, personalizar el contenido en función del comportamiento del usuario y reaccionar a las señales en tiempo real.

Al aprovechar estas estrategias, puede convertir los datos de comportamiento en acciones significativas: suprimir, calificar o excluir perfiles en función de los eventos que almacenan en déclencheur o los atributos que llevan. Tanto si desea crear una lógica para los umbrales de compra como para los déclencheur de abandono o la gestión de devoluciones, estos ejemplos le ofrecen directrices prácticas que puede adaptar a sus necesidades.

A medida que evalúe qué enfoque se adapta mejor, tenga en cuenta los requisitos de latencia del caso de uso para garantizar que los recorridos sigan siendo interactivos y eficaces.

## Supresión de la exclusión

Para suprimir perfiles que se han excluido de las comunicaciones de marketing, utilice la administración de consentimiento integrada. Las preferencias de exclusión se capturan automáticamente en los campos de consentimiento del perfil; se puede hacer referencia a ellas directamente en las condiciones de recorrido y Journey Optimizer las aplica automáticamente durante la entrega del mensaje.

Más información:

* [Administrar el consentimiento](../privacy/opt-out.md)
* [Administración de exclusión de correo electrónico](../email/email-opt-out.md)
* [Administración de la exclusión para mensajes de texto](../sms/sms-opt-out.md)


## Supresión basada en devoluciones

Para excluir perfiles que han experimentado devoluciones de correo electrónico, aproveche la lista de supresión automática de Adobe Journey Optimizer para direcciones devueltas. Este mecanismo integrado garantiza que los correos electrónicos no válidos o inaccesibles se excluyan de futuros envíos sin requerir lógica personalizada.

Más información:

* [Administrar la lista de supresión](../configuration/manage-suppression-list.md)


## Supresión genérica

Para suprimir perfiles que han demostrado ciertos comportamientos, utilice audiencias por lotes con lógica basada en eventos para capturar perfiles que cumplan los criterios de supresión. Hacer referencia a esta audiencia en condiciones de recorrido.

Más información:

* Adobe Experience Platform [Generador de segmentos - Eventos](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [Generador de segmentos - Restricciones de tiempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Uso de audiencias en condiciones](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [Función inAudience()](../building-journeys/functions/functioninaudience.md)


## Exclusión de comunicaciones recibidas

Para evitar el envío de mensajes a perfiles que han recibido comunicaciones en un período de tiempo reciente:

* Utilice audiencias por lotes con criterios basados en el tiempo y haga referencia a ellas en condiciones de recorrido.
* Aplique reglas comerciales de límite de frecuencia para aplicar límites de mensajes diarios o semanales.


Más información sobre el uso de las audiencias:

* Adobe Experience Platform [Generador de segmentos - Eventos](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [Generador de segmentos - Restricciones de tiempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Uso de audiencias en condiciones](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [Función inAudience()](../building-journeys/functions/functioninaudience.md)


Consulte también:

* [Restricción de frecuencia por canal y tipo de comunicación](../conflict-prioritization/channel-capping.md)



## Inclusión/exclusión específica del mensaje

Para incluir o excluir perfiles en función de si han recibido un mensaje específico, cree audiencias por lotes que encapsulen esta lógica y hagan referencia a ellas en condiciones de recorrido.


Más información:

* Adobe Experience Platform [Generador de segmentos - Eventos](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [Generador de segmentos - Restricciones de tiempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Uso de audiencias en condiciones](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [Función inAudience()](../building-journeys/functions/functioninaudience.md)

## Personalización de abandono del carro o exploración

Para personalizar las comunicaciones en función del carro de compras más reciente o examinar los eventos en varios tipos de carros de compras o vistas de productos:

* Si tiene acceso a [Adobe Experience Platform Data Distiller](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/overview){target="_blank"}, configure consultas automatizadas para extraer los datos necesarios del evento, manipule el evento para que se ajuste al caso de uso y escríbalo de nuevo en un conjunto de datos con perfil habilitado para su activación.
* Si los datos de abandono se pueden modelar en el perfil con atributos escalares, considere la posibilidad de utilizar atributos calculados para capturar la información más reciente y luego hacer referencia a estos atributos en el recorrido para construir la comunicación. [Más información en la documentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}.


## Salida de recorrido basada en el comportamiento

Para eliminar perfiles de la recorrido cuando muestren un comportamiento determinado, utilice criterios de salida para salir del perfil de la recorrido cuando se reciba un evento determinado o cuando el perfil cumpla los requisitos de una audiencia específica.

Más información:

* [Establezca las propiedades del recorrido: criterios de salida](journey-properties.md#exit-criteria)

## Calificación basada en compras con umbrales de valor

Para almacenar en déclencheur los recorridos según las compras y suprimir si el valor está por encima o por debajo de un umbral, defina atributos calculados para sumar compras durante un período de tiempo específico. Cree una audiencia que incluya perfiles cuya cantidad de gasto cumpla determinados criterios.

Más información:

* Adobe Experience Platform [Descripción general de atributos calculados](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## Preguntas frecuentes {#faq-ee}

A continuación, encontrará las preguntas más frecuentes sobre la búsqueda de eventos de Experience en recorrido.

¿Necesita más detalles? Usa las opciones de comentarios de la parte inferior de esta página para plantear tu pregunta o conectar con la [comunidad de Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}.

+++¿Qué capacidades específicas se ven afectadas? 

Solo se ve afectada la búsqueda de eventos de experiencia en el editor de expresiones. Las siguientes capacidades se vieron afectadas **no** y siguen siendo las mismas:

* Observación de los eventos de experiencia asociados a un perfil específico en la IU del perfil

* Uso de eventos de experiencia en reglas de atributos calculados y acceso a los atributos calculados en un recorrido

* Activación de un recorrido con un evento unitario o empresarial

* Uso de datos de contexto de recorrido de los eventos que almacenan el recorrido en déclencheur en los editores de expresiones y personalización

* Escucha de un evento dentro de un recorrido

* Configuración de eventos para almacenar en déclencheur un recorrido

* Detección de eventos de reacción del usuario final en las comunicaciones de marketing (por ejemplo, correo electrónico abierto)

+++

+++¿Se ve afectada mi organización de Adobe existente por esta actualización? 

Su organización de Adobe solo se ve afectada si aún no estaba utilizando la búsqueda de eventos de experiencia. Si ya está utilizando eventos de experiencia en la [fuente de datos de Experience Platform](../datasource/adobe-experience-platform-data-source.md), su organización de Adobe sigue admitiendo la búsqueda de eventos de experiencia.

+++

+++Tengo una nueva organización de Adobe. ¿Cómo puedo resolver mi caso de uso que requiere datos de evento de experiencia? 

Más arriba se encuentran disponibles enfoques alternativos y prácticas recomendadas que implican eventos de experiencia para lograr los casos de uso deseados.

+++

+++ ¿Qué sucede si los enfoques alternativos no funcionan para mi caso de uso?

Si su caso de uso no se puede resolver mediante uno de los enfoques alternativos enumerados arriba, póngase en contacto con su representante de Adobe.

+++
