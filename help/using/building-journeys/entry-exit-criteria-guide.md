---
solution: Journey Optimizer
product: journey optimizer
title: Criterios de entrada y salida de recorrido
description: Aprenda a administrar de forma eficaz los casos en los que los perfiles entran y salen de recorridos con ejemplos reales y prácticas recomendadas
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: entrada, salida, criterios, recorrido, perfil, reentrada, prácticas recomendadas
version: Journey Orchestration
source-git-commit: a60ea57ffed3fa9e11dc202f26889d05862604d9
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 0%

---


# Trabajar con criterios de entrada y salida de recorrido {#entry-exit-criteria-guide}

En Customer Experience Orchestration, para enviar el mensaje correcto en el momento adecuado se requiere un control preciso sobre el momento en el que los clientes entran y salen de las recorridos. Comprender y configurar correctamente los criterios de entrada y salida puede marcar la diferencia entre una campaña exitosa y atractiva y las oportunidades perdidas o la fatiga del mensaje.

Esta guía proporciona orientación práctica, ejemplos reales y prácticas recomendadas para administrar los criterios de entrada y salida de recorrido en Adobe Journey Optimizer.

## ¿Cuáles son los criterios de entrada y salida? {#what-are-criteria}

**Los criterios de entrada** determinan las condiciones bajo las cuales un [perfil de cliente](../audience/get-started-profiles.md) cumple los requisitos para ingresar un recorrido específico. Los perfiles pueden entrar en función de lo siguiente:

* déclencheur **[Comportamiento del cliente](../event/about-events.md)**: acciones realizadas por los clientes que registran la entrada de recorridos en tiempo real, como realizar una compra, abandonar un carro de compras o abrir una aplicación móvil.

* **[Atributos de perfil](../audience/get-started-profiles.md)**: las características del cliente determinan la idoneidad en función de los datos almacenados en su perfil, como el nivel de lealtad, la ubicación, la edad o las preferencias de comunicación.

* **[Eventos externos](../event/about-creating-business.md)**: déclencheur empresariales o ambientales que afectan a varios clientes simultáneamente, como alertas de inventario bajo, condiciones meteorológicas o cambios de precios.

* **[Pertenencia a audiencia](../audience/about-audiences.md)**: pertenecer a un segmento de audiencia específico habilita los recorridos de destino para grupos como clientes de alto valor, usuarios inactivos o nuevos suscriptores.

**Los criterios de salida** definen cuándo y cómo un perfil sale o se elimina de un recorrido:

* **Finalización de Recorrido**: los perfiles se cierran automáticamente cuando llegan al [final de todas las rutas de recorrido](end-journey.md), lo que completa la experiencia diseñada.

* **Logro de la métrica de éxito**: los perfiles se eliminan cuando completan el [objetivo de recorrido](success-metrics.md), como realizar una compra o descargar una aplicación, lo que elimina comunicaciones de seguimiento innecesarias.

* **Basado en condiciones**: los perfiles se eliminan cuando se cumplen [condiciones específicas](condition-activity.md), como inactividad durante un período establecido o cambios en los atributos del perfil.

* **Basado en eventos**: los perfiles se cierran cuando ocurren [eventos específicos](../event/about-events.md), como la cancelación de la suscripción o la devolución del producto.

* **Descalificación de audiencias**: los perfiles se cierran cuando ya no cumplen los [criterios de audiencia de destino](../audience/about-audiences.md), lo que garantiza que los mensajes sigan siendo relevantes.

## Por qué importan los criterios de entrada y salida {#why-they-matter}

Definir correctamente los criterios de entrada y salida proporciona un valor comercial significativo:

* **Relevancia**: Solo los clientes adecuados entran al recorrido, lo que aumenta las tasas de participación y conversión al dirigirse a la audiencia más adecuada en el momento óptimo.

* **Eficiencia**: evita que los clientes permanezcan en recorridos irrelevantes, reduciendo las comunicaciones innecesarias, los costos operativos y la molestia de los clientes.

* **Personalization**: habilita la personalización dinámica de experiencias basada en datos y comportamiento en tiempo real, lo que crea interacciones de clientes más significativas.

* **Cumplimiento**: Ayuda a administrar la restricción de frecuencia y a evitar la comunicación excesiva, respetando las preferencias de los clientes y los requisitos regulatorios, al mismo tiempo que se mantiene la reputación de la marca.

## Ejemplos reales de entrada y salida de recorridos {#real-world-examples}

Estos son escenarios comunes que muestran cómo funcionan en la práctica los criterios de entrada y salida:

**Campaña de bienvenida para nuevos suscriptores**

Cree una primera impresión personalizada guiando automáticamente a los nuevos suscriptores a través de una introducción a su marca, productos y servicios.

* **Entrada**: los perfiles entran en el recorrido cuando se suscriben a un boletín informativo
* **Salida**: los perfiles se salen una vez que han completado una serie de correos electrónicos de bienvenida o después de una hora establecida si no interactúan
* **Beneficio**: Garantiza que los nuevos suscriptores reciban incorporación oportuna y, al mismo tiempo, evita los mensajes repetitivos

**Recuperación del carro de compras abandonado**

Recupere los ingresos perdidos recordándoles a los clientes los artículos que dejaron y ofreciéndoles incentivos para completar su compra.

* **Entrada**: Los clientes ingresan al recorrido si agregan artículos al carro de compras pero no finalizan el cierre de compra en un plazo de 24 horas
* **Salida**: Los perfiles se retiran cuando completan la compra o después de 7 días si no se realiza ninguna compra
* **Beneficio**: impulsa las conversiones mediante recordatorios oportunos sin enviar spam a clientes que no estén interesados

**Participación en el programa de fidelización**

Recompense a sus clientes más valiosos con ventajas exclusivas y comunicaciones personalizadas que fortalecen la lealtad de la marca y aumentan el valor de por vida.

* **Entrada**: Los clientes se unen al recorrido después de alcanzar un determinado umbral de puntos de lealtad
* **Salir**: Los perfiles se salen después de canjear las recompensas o si están inactivos durante 60 días
* **Beneficio**: mantiene a los clientes de alto valor comprometidos con las ofertas personalizadas y evita la fatiga de la comunicación

**Recopilación de comentarios sobre el producto**

Recopile información sobre la satisfacción del cliente y el rendimiento del producto solicitando comentarios en el momento óptimo después de la entrega.

* **Entrada**: Los clientes entran al recorrido después de recibir un evento de confirmación de entrega de producto
* **Salir**: los perfiles se salen una vez que se envían los comentarios o después de 10 días si no hay respuesta
* **Beneficio**: Captura comentarios valiosos de inmediato sin molestar a los clientes con solicitudes persistentes

## Configuración de los criterios de entrada de recorrido {#configure-entry}

>[!BEGINSHADEBOX]

**Aprenda todo lo que necesita saber sobre los criterios de entrada aquí:**

* **[Déclencheur basados en eventos](../event/about-events.md)**: use eventos como &quot;creación de perfiles&quot;, &quot;transacción completada&quot; o eventos personalizados para iniciar un recorrido. [Configurar eventos](../event/about-creating.md) en **[!UICONTROL Administración]** > **[!UICONTROL Eventos]**, definir [campos y esquema de eventos](../event/experience-event-schema.md) y luego agregar el evento desde la paleta **[!UICONTROL Eventos]** en el [diseñador de recorridos](using-the-journey-designer.md).

* **[Entrada basada en audiencias](read-audience.md)**: El destino envía recorridos a perfiles que pertenecen a audiencias específicas, ya sea como un lote único o en una programación recurrente. [Crear audiencias](../audience/creating-a-segment-definition.md) en el menú de **[!UICONTROL Audiencias]**, luego agrega una actividad de **[!UICONTROL Leer audiencia]** y [configura la programación](journey-properties.md#schedule).

* **[Entrada de calificación de audiencia](audience-qualification-events.md)**: Déclencheur los recorridos cuando los perfiles cumplen los requisitos o salen de audiencias específicas en tiempo real. Defina [audiencias de transmisión por secuencias](../audience/about-audiences.md), agregue un evento de **[!UICONTROL Calificación de audiencias]** desde la paleta **[!UICONTROL Eventos]** y elija el tipo de déclencheur.

* **[Filtros de atributos](condition-activity.md)**: perfeccione los criterios de entrada combinando eventos o audiencias con atributos de perfil y contexto mediante la lógica AND/OR. Use [condiciones](conditions.md) para hacer referencia a [atributos de perfil](../audience/get-started-profiles.md), eventos o [datos externos](../datasource/about-data-sources.md).

* **[Ventanas de tiempo y programación](journey-properties.md#schedule)**: establezca restricciones temporales para mantener los recorridos oportunos y relevantes. Configure [programaciones en actividades de audiencia de lectura](read-audience.md), use [actividades de espera](wait-activity.md) y agregue [condiciones basadas en el tiempo](conditions.md) para controlar el tiempo.

>[!ENDSHADEBOX]

## Configuración de los criterios de salida del recorrido {#configure-exit}

>[!BEGINSHADEBOX]

**Obtenga información acerca de los criterios de salida aquí:**

* **[Finalización de Recorrido](end-journey.md)**: Los perfiles se cierran automáticamente después de llegar al último paso del recorrido. Diseñe rutas de recorrido para finalizar en **[!UICONTROL End]** actividades.

* **[Logro de métrica de éxito](journey-properties.md#exit-criteria)**: defina métricas de éxito (como compras o suscripciones) y perfiles de salida al finalizar. Haga clic en **[!UICONTROL Mostrar criterios de salida]**, seleccione **[!UICONTROL Agregar criterios de salida]** y elija un [Evento](../event/about-events.md) o una [Audiencia](../audience/about-audiences.md) como déclencheur de salida.

* **[Tiempos de espera de inactividad](wait-activity.md)**: perfiles de salida si no se produce ninguna participación dentro de un intervalo de tiempo establecido. Use [Criterios de salida](journey-properties.md#exit-criteria) con audiencias que comprueben la fecha de la última participación, establezcan [Actividades de espera](wait-activity.md) con duraciones definidas y usen [condiciones](condition-activity.md) para comprobar la actividad.

* **[Reglas de reentrada](entry-management.md)**: decida si los perfiles pueden volver a entrar en el recorrido varias veces o solo una vez, según la estrategia de campaña. Defina la configuración de **[!UICONTROL Reentrada]** en el recorrido **[!UICONTROL Propiedades]** para establecer períodos de espera, habilitar la reentrada forzada o usar [identificadores suplementarios](supplemental-identifier.md) para la reentrada específica del contexto.

>[!ENDSHADEBOX]

## Ejemplos de recorrido detallados {#journey-examples}

Para obtener instrucciones de implementación paso a paso con detalles técnicos completos, explore estos casos de uso documentados:

* **[recorrido de incorporación del cliente](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)**: cree experiencias de bienvenida personalizadas con calificación de audiencia, tiempo de espera de evento y salidas basadas en objetivos

* **[Recuperación del carro de compras abandonado](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)**: recupere las ventas perdidas con recorridos activados por eventos, libros de reproducción y enrutamiento de canales

* **[Campañas de renovación de participación](https://experienceleague.adobe.com/es/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)**: recupera clientes inactivos con direccionamiento según el comportamiento y activación de medios de pago

* **[Enviar mensajes a los suscriptores](message-to-subscribers-uc.md)** - Listas de suscripción de Target con Audiencia de lectura y contenido personalizado

* **[Enviar mensajes multicanal](journeys-uc.md)** - Combinar correo electrónico y push con eventos de reacción y lógica de múltiples rutas

* **[Enviar correos electrónicos solo entre semana](weekday-email-uc.md)** - Programar comunicaciones con condiciones basadas en el tiempo y fórmulas de espera

>[!TIP]
>
>Examine todos los casos de uso disponibles en la [biblioteca de casos de uso de Recorrido](jo-use-cases.md) para ver más patrones e implementaciones, incluidos los [envíos más rápidos](ramp-up-deliveries-uc.md), los [patrones de eventos de experiencia](exp-event-lookup.md) y la [eliminación de perfiles de recorridos activos](journey-pause.md#apply-an-exit-criteria-in-a-paused-journey).

## Prácticas recomendadas para administrar entradas y salidas {#best-practices}

**Borrar definición**

* Documente la lógica de entrada y salida antes de crear recorridos para alinear los equipos de marketing y análisis
* Creación de diagramas de flujo que muestren los puntos de entrada, las rutas de recorrido y las condiciones de salida
* Defina las reglas comerciales claramente: &quot;Los perfiles se cierran cuando ocurre X O después de Y días&quot;
* Utilice etiquetas descriptivas: &quot;Salida - Compra completada&quot; no &quot;Salida 1&quot;
* [Etiquetar recorridos](../start/search-filter-categorize.md#tags) de forma consistente para generar informes y filtrar

**Evitar recorridos superpuestos**

* [Auditar recorridos activos](journey-ui.md) antes de iniciar otros similares para evitar conflictos
* Aproveche [la administración de conflictos](../conflict-prioritization/conflicts.md) y [las puntuaciones de prioridad](../conflict-prioritization/priority-scores.md) para resolver superposiciones y priorizar recorridos
* Diseñar recorridos que se complementen en lugar de competir entre sí

>[!NOTE]
>
>En escenarios avanzados como la eliminación automática de perfiles cuando cumplen los requisitos para los recorridos de prioridad más alta, use [límite y arbitraje de recorrido](../conflict-prioritization/journey-capping.md) en lugar de los criterios de salida.

**Supervisar y optimizar**

* Rastrear la tasa de entrada, la tasa de salida y la tasa de finalización de cada recorrido mediante [informes de recorrido](../reports/journey-global-report-cja.md)
* Supervisar [métricas de éxito](success-metrics.md): porcentaje de salida a través de finalización de métrica de éxito frente a tiempo de espera
* [Probar criterios de entrada y salida](testing-the-journey.md) con varios escenarios de perfil antes del inicio
* Ajustar según los datos: si las salidas tempranas son altas, revise la relevancia de los criterios de entrada; si la métrica de éxito es baja, finalice, analice el contenido y el tiempo
* Revisar todos los recorridos activos trimestralmente

**Respetar límites de frecuencia**

* Establezca [periodos de espera de reentrada](entry-management.md) adecuados o deshabilite la reentrada para recorridos de una sola vez
* Use [reglas de límite de frecuencia](../conflict-prioritization/rule-sets.md) para evitar la sobrecomunicación
* Monitorizar las métricas de frecuencia en los informes para garantizar el cumplimiento

>[!NOTE]
>
>Para administrar límites de frecuencia y límites de entrada de recorrido en varios recorridos, usa [límite y arbitraje de recorrido](../conflict-prioritization/journey-capping.md) y [límite de frecuencia por canal](../conflict-prioritization/channel-capping.md).

## Conclusión {#conclusion}

Los criterios de entrada y salida de recorrido son fundamentales para ofrecer experiencias del cliente personalizadas, oportunas y efectivas con Adobe Journey Optimizer. Al crear cuidadosamente estas condiciones, los especialistas en marketing pueden aumentar la participación, reducir la fricción y crear relaciones de cliente más sólidas.

Comience asignando claramente los déclencheur del cliente y los puntos de salida, realice pruebas exhaustivas y supervise los resultados para refinar continuamente la orquestación de recorrido.

## Recursos relacionados {#related-resources}

**Documentación técnica**

[Administración de entrada de perfil](entry-management.md) | [propiedades de Recorrido y criterios de salida](journey-properties.md) | [Cómo terminan los recorridos](end-journey.md) | [Identificadores adicionales](supplemental-identifier.md) | [diseñador de Recorrido](using-the-journey-designer.md)

**Tutoriales y ejemplos**

[casos de uso de Recorrido](jo-use-cases.md) | [Vídeo de incorporación del cliente](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding) | [Vídeo de carro abandonado](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart) | [Blog comunitario: Criterios de entrada y salida](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/mastering-journey-entry-and-exit-criteria-in-adobe-journey/ba-p/760958)

**Funciones relacionadas**

[Eventos de calificación de audiencia](audience-qualification-events.md) | [Métricas de éxito y objetivos](success-metrics.md) | [Administración de conflictos](../conflict-prioritization/conflicts.md) | [Límite de frecuencia](../conflict-prioritization/rule-sets.md) | [recorridos de prueba](testing-the-journey.md) | [Actividad de condición](condition-activity.md) | [Eventos de reacción](reaction-events.md) | [Actividad de espera](wait-activity.md)
