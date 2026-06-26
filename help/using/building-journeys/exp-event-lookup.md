---
solution: Journey Optimizer
product: journey optimizer
title: Búsqueda de eventos de experiencia en recorrido
description: Aprenda a utilizar la búsqueda de eventos de experiencia en recorrido
exl-id: 35e2e347-0669-44a3-92ba-aee52e54c219
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/kVO36LmCfr9cYVq3EHRy8OpqPCZDq20mXTEA49TIRTI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: e23d48b5-7858-4d45-9c56-9e2b4be8500eid: fa683eda-48de-4558-af32-2673edcd44fe
topic_v2: id: c4147b6e-073b-4d3c-9ab1-d60f2f4434efid: e0eb8757-182f-49f3-94a4-1587d16f5094id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1717
ht-degree: 4%

---

# Búsqueda de eventos de experiencia en recorrido {#ee-journeys}

>[!BEGINSHADEBOX]

**En esta página:** Conozca patrones escalables y prácticas recomendadas para usar Eventos de experiencia en recorridos con el fin de suprimir, calificar o personalizar perfiles en función de su comportamiento y atributos de evento.

>[!ENDSHADEBOX]

>[!CAUTION]
>
>A partir del 8 de julio de 2025, en las nuevas organizaciones de clientes, la creación de expresiones mediante eventos de experiencia ya no se admite en el editor de expresiones utilizado en las condiciones de recorrido. Como resultado, no se pueden usar eventos de experiencia en la [fuente de datos de Experience Platform](../datasource/adobe-experience-platform-data-source.md) para crear expresiones.
>
>A partir del 1 de abril de 2026, el uso de atributos de evento de experiencia en expresiones de recorrido dejará de ser compatible con las organizaciones que no hayan utilizado esta capacidad en los últimos 90 días. A continuación, se hace referencia a enfoques alternativos y prácticas recomendadas para crear expresiones/lógica con eventos de experiencia.
>
>¿Necesita más información? [Lea las preguntas frecuentes](#faq-ee).

Esta página describe patrones comunes y enfoques escalables para ayudarle a aprovechar al máximo los eventos de experiencia en [!DNL Adobe Journey Optimizer]. Estos casos de uso están diseñados para ayudarle a resolver los desafíos frecuentes, como administrar las exclusiones, controlar la frecuencia de los mensajes, personalizar el contenido en función del comportamiento del usuario y reaccionar a las señales en tiempo real.

Al aprovechar estas estrategias, puede convertir los datos de comportamiento en acciones significativas: suprimir, calificar o excluir perfiles en función de los eventos que almacenan en déclencheur o los atributos que llevan. Tanto si desea crear una lógica para los umbrales de compra como para los déclencheur de abandono o la gestión de devoluciones, estos ejemplos le ofrecen directrices prácticas que puede adaptar a sus necesidades.

A medida que evalúe qué enfoque se adapta mejor, tenga en cuenta los requisitos de latencia del caso de uso para garantizar que los recorridos sigan siendo interactivos y eficaces.

## Supresión de la exclusión

Para suprimir perfiles que se han excluido de las comunicaciones de marketing, utilice la administración de consentimiento integrada. Las preferencias de exclusión se capturan automáticamente en los campos de consentimiento del perfil; se puede hacer referencia a ellas directamente en las condiciones de recorrido y Journey Optimizer las aplica automáticamente durante la entrega del mensaje.

Más información:

* [Administrar el consentimiento](../privacy/opt-out.md)
* [Administración de exclusión de correo electrónico](../email/email-opt-out.md)
* [Administración de la exclusión para mensajes de dispositivos móviles](../mobile/mobile-opt-out.md)


## Supresión basada en devoluciones

Para excluir perfiles que han experimentado devoluciones de correo electrónico, aproveche la lista de supresión automática de [!DNL Adobe Journey Optimizer] para direcciones devueltas. Este mecanismo integrado garantiza que los correos electrónicos no válidos o inaccesibles se excluyan de futuros envíos sin requerir lógica personalizada.

Más información:

* [Administrar la lista de supresión](../configuration/manage-suppression-list.md)


## Supresión genérica

Para suprimir perfiles que han demostrado ciertos comportamientos, utilice audiencias por lotes con lógica basada en eventos para capturar perfiles que cumplan los criterios de supresión. Hacer referencia a esta audiencia en condiciones de recorrido.

Más información:

* [!DNL Adobe Experience Platform] [Generador de segmentos - Eventos](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Generador de segmentos - Restricciones de tiempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Uso de audiencias en condiciones](../building-journeys/conditions.md#using-a-segment)

* [Función inAudience()](../building-journeys/functions/functioninaudience.md)


## Exclusión de comunicaciones recibidas

Para evitar el envío de mensajes a perfiles que han recibido comunicaciones en un período de tiempo reciente:

* Utilice audiencias por lotes con criterios basados en el tiempo y haga referencia a ellas en condiciones de recorrido.
* Aplique reglas comerciales de límite de frecuencia para aplicar límites de mensajes diarios o semanales.


Más información sobre el uso de las audiencias:

* [!DNL Adobe Experience Platform] [Generador de segmentos - Eventos](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Generador de segmentos - Restricciones de tiempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Uso de audiencias en condiciones](../building-journeys/conditions.md#using-a-segment)

* [Función inAudience()](../building-journeys/functions/functioninaudience.md)


Consulte también:

* [Restricción de frecuencia por canal y tipo de comunicación](../conflict-prioritization/channel-capping.md)



## Inclusión/exclusión específica del mensaje

Para incluir o excluir perfiles en función de si han recibido un mensaje específico, cree audiencias por lotes que encapsulen esta lógica y hagan referencia a ellas en condiciones de recorrido.


Más información:

* [!DNL Adobe Experience Platform] [Generador de segmentos - Eventos](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Generador de segmentos - Restricciones de tiempo](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Uso de audiencias en condiciones](../building-journeys/conditions.md#using-a-segment)

* [Función inAudience()](../building-journeys/functions/functioninaudience.md)

## Personalización de abandono del carro o exploración

Para personalizar las comunicaciones en función del carro de compras más reciente o examinar los eventos en varios tipos de carros de compras o vistas de productos:

* Si tiene acceso a [[!DNL Adobe Experience Platform] Data Distiller](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/overview){target="_blank"}, configure consultas automatizadas para extraer los datos necesarios del evento, manipule el evento para que se ajuste al caso de uso y escríbalo de nuevo en un [conjunto de datos con perfil habilitado](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} para su activación.
* Si los datos de abandono se pueden modelar en el perfil con atributos escalares, considere la posibilidad de utilizar atributos calculados para capturar la información más reciente y luego hacer referencia a estos atributos en el recorrido para construir la comunicación. [Obtenga más información en [!DNL Adobe Experience Platform] documentación](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}


## Salida de recorrido basada en el comportamiento

Para eliminar perfiles de la recorrido cuando muestren un comportamiento determinado, utilice criterios de salida para salir del perfil de la recorrido cuando se reciba un evento determinado o cuando el perfil cumpla los requisitos de una audiencia específica.

Más información:

* [Establezca las propiedades del recorrido: criterios de salida](journey-properties.md#exit-criteria)

## Calificación basada en compras con umbrales de valor

Para almacenar en déclencheur los recorridos según las compras y suprimir si el valor está por encima o por debajo de un umbral, defina atributos calculados para sumar compras durante un período de tiempo específico. Cree una audiencia que incluya perfiles cuya cantidad de gasto cumpla determinados criterios.

Más información:

* [!DNL Adobe Experience Platform] [Resumen de atributos calculados](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## Preguntas frecuentes {#faq-ee}

Estas preguntas frecuentes se centran en la cronología para retirar el uso de eventos de experiencia en expresiones de recorrido y en quién se ve afectado. Para obtener instrucciones sobre enfoques alternativos, consulte los casos de uso y las prácticas recomendadas que se han indicado anteriormente.

¿Necesita más información? Usa las opciones de comentarios de la parte inferior de esta página para plantear tu pregunta o conectar con la [[!DNL Adobe Journey Optimizer] comunidad](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=es){target="_blank"}.

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

A partir del 8 de julio de 2025, las nuevas organizaciones de clientes no podrán crear expresiones mediante atributos de evento de experiencia. A partir del 1 de abril de 2026, las organizaciones que no hayan accedido a eventos de experiencia a través de expresiones de recorrido en los últimos 90 días dejarán de tener acceso a esta capacidad.

+++

+++Tengo una nueva organización de Adobe. ¿Cómo puedo resolver mi caso de uso que requiere datos de evento de experiencia? 

Más arriba se encuentran disponibles enfoques alternativos y prácticas recomendadas que implican eventos de experiencia para lograr los casos de uso deseados.

+++

+++ ¿Qué sucede si los enfoques alternativos no funcionan para mi caso de uso?

Si su caso de uso no se puede resolver mediante uno de los enfoques alternativos enumerados arriba, póngase en contacto con su representante de Adobe.

+++

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página describe patrones alternativos y prácticas recomendadas para usar datos de evento de experiencia en recorridos de Adobe Journey Optimizer, en el contexto de la obsolescencia de la búsqueda de evento de experiencia directa en el editor de expresiones de recorrido.

**Intenciones:**

* Suprimir perfiles de exclusión mediante la administración de consentimiento integrada en lugar de expresiones de evento de experiencia
* Excluir direcciones de correo electrónico rechazadas mediante la lista de supresión automática de AJO
* Generar lógica de supresión genérica utilizando audiencias por lotes con criterios basados en eventos
* Evite la sobrecomunicación mediante la aplicación de reglas de límite de frecuencia o condiciones de audiencia basadas en el tiempo
* Personalice el carro de compras abandonado o explore las comunicaciones mediante AEP Data Distiller o atributos calculados

**Glosario:**

* **Evento de experiencia**: registro inmutable con marca de tiempo de una acción o comportamiento del cliente almacenado en Adobe Experience Platform *(específico del producto)*
* **Atributo calculado**: atributo de nivel de perfil derivado de agregar o resumir datos de evento de experiencia a lo largo del tiempo, disponible para su uso en expresiones de recorrido *(específicas del producto)*
* **Lista de supresión**: la lista integrada de direcciones de correo electrónico de AJO se excluye automáticamente de futuros envíos debido a rechazos graves o quejas de spam *(específico del producto)*
* **Límite de frecuencia**: Regla de negocio que limita la cantidad de mensajes que un perfil puede recibir en un período de tiempo definido *(específico del producto)*
* **Data Distiller**: una funcionalidad de AEP que permite que las consultas por lotes basadas en SQL extraigan y transformen datos de evento en conjuntos de datos con perfil habilitado *(específicos de producto)*

**Protecciones:**

* A partir del 8 de julio de 2025, las nuevas organizaciones de clientes no podrán crear expresiones mediante atributos de evento de experiencia en el editor de expresiones de recorrido.
* A partir del 1 de abril de 2026, las organizaciones que no hayan utilizado atributos de evento de experiencia en expresiones de recorrido en los últimos 90 días perderán acceso a esta capacidad.
* Se está retirando la búsqueda de eventos de experiencia directa en condiciones de recorrido; las alternativas incluyen audiencias por lotes, atributos calculados y AEP Data Distiller.
* Entre las capacidades que NO se ven afectadas por la retirada se incluyen: la activación de recorridos con eventos, la escucha de eventos dentro de un recorrido, el uso de datos de contexto de recorrido de eventos de déclencheur, la configuración de eventos y la detección de eventos de reacción.

**Terminología:**

* Nombre canónico: Búsqueda de eventos de experiencia — Acrónimo: Búsqueda de EE — variantes: expresiones de eventos de experiencia, búsqueda de atributos de evento
* Sinónimos: &quot;audiencia por lotes con lógica basada en eventos&quot; = &quot;segmento basado en eventos&quot; como mecanismo de supresión/inclusión
* No confunda: &quot;búsqueda de eventos de experiencia en el editor de expresiones&quot; ≠ &quot;activación de un recorrido con un evento&quot;: NO se retira la activación de recorridos con eventos

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Todavía puedo almacenar en déclencheur un recorrido mediante un evento de experiencia?** — Sí, este cambio no afecta a la activación de recorridos con eventos unitarios o empresariales.
* **Q: ¿Cuál es el reemplazo recomendado para la búsqueda de eventos de experiencia en condiciones de recorrido?** — Utilice audiencias por lotes creadas con la lógica basada en eventos del Generador de segmentos de AEP, los atributos calculados o el Distiller de datos de AEP para transformaciones complejas.
* **Q: ¿Se ve afectada mi organización actual en este momento?** — Las nuevas organizaciones se ven afectadas a partir del 8 de julio de 2025. Las organizaciones existentes se verán afectadas a partir del 1 de abril de 2026 solo si no han utilizado la capacidad en los últimos 90 días.
* **Q: ¿Cómo puedo manejar la personalización del abandono del carro de compras sin la búsqueda de eventos directa?** — Utilice AEP Data Distiller para extraer y escribir datos de evento en un conjunto de datos con perfil habilitado, o utilice Atributos calculados para capturar el último estado de abandono en el perfil.
* **Q: ¿Qué capacidades NO se ven afectadas por esta obsolescencia?** — La activación de recorridos con eventos, la escucha de eventos dentro de recorridos, el uso de datos de contexto de eventos de déclencheur en expresiones, la configuración de eventos y la detección de eventos de reacción (por ejemplo, las aperturas de correo electrónico) no se ven afectados.

+++
