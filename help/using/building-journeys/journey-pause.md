---
solution: Journey Optimizer
product: journey optimizer
title: Pausar un recorrido
description: Aprenda a pausar y reanudar un recorrido en directo
feature: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Disponibilidad limitada" type="Informative"
keywords: publicar, recorrido, en directo, validez, comprobar
source-git-commit: cd85b58350b4f8829aa1bc925c151be9b061b170
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 3%

---

# Pausar un recorrido {#journey-pause}

Puede pausar los recorridos activos, realizar todos los cambios necesarios y reanudarlos de nuevo en cualquier momento. Un recorrido se puede pausar durante un máximo de 14 días. Puede elegir si el recorrido se reanuda al final del período de pausa o si se detiene por completo.


>[!AVAILABILITY]
>
>Esta versión solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.


## Ventajas principales {#journey-dry-run-benefits}

Los recorridos de pausa y reanudación proporcionan a los especialistas en marketing un mayor control y flexibilidad al permitir que los recorridos en directo se suspendan temporalmente sin interrumpir la experiencia del cliente. Cuando está en pausa, no se envían comunicaciones y los perfiles permanecen en estado suspendido hasta que se reanuda la recorrido.

Esta capacidad reduce el riesgo de enviar mensajes no deseados durante errores o actualizaciones (p. ej.: cambio en el contenido del mensaje), admite una administración más segura del recorrido y aumenta la confianza del profesional. La visibilidad de los recorridos en pausa y su estado directamente en la IU mejora aún más la transparencia y la agilidad operativa.

>[!CAUTION]
>
>Los permisos para pausar y reanudar recorridos están restringidos a los usuarios con el permiso de alto nivel **[!DNL Publish journeys]**. Obtenga más información acerca de la administración de los derechos de acceso de los usuarios de [!DNL Journey Optimizer] en [esta sección](../administration/permissions-overview.md).

## Mecanismos de protección y recomendaciones

* Una versión de recorrido se puede pausar durante un máximo de 14 días.
* Los recorridos en pausa se consideran en todas las reglas de negocio, del mismo modo que si estuvieran activos.
* Los perfiles se &quot;descartan&quot; en un recorrido pausado cuando llegan a una actividad de acción. Si permanecen en espera durante el tiempo en que se pone en pausa un recorrido y abandonan esa espera cuando se reanuda, continuarán con el recorrido y no se descartarán.
* Incluso después de la pausa, a medida que los eventos se siguen procesando, estos eventos se contarán hacia una cuota de 5 ktps, después de lo cual la restricción se obtiene por unitaria.
* Los perfiles que habían entrado en el recorrido pero que se descartaron durante la pausa se contarían como perfiles atractivos.
* Cuando los perfiles se mantienen en un recorrido pausado, en el momento de la reanudación se actualizan los atributos del perfil
* Las condiciones se siguen ejecutando en recorridos pausados, por lo que si un recorrido se ha pausado debido a problemas de calidad de datos, cualquier condición anterior a un nodo de acción se puede evaluar con datos incorrectos.
* Para el recorrido de audiencia de lectura incremental basado en audiencias, se tiene en cuenta la duración de la pausa. Por ejemplo, para un recorrido diario, si se pausó el 2 y se reanudó el 5 del mes, la ejecución del 6 tomará todos los perfiles que se hayan clasificado del 1 al 6. Este no es el caso de la calificación de audiencias o de los recorridos basados en eventos (si se recibe una calificación de audiencia o un evento durante una pausa, esos eventos se descartan).
* Los recorridos en pausa se cuentan hacia la cuota de recorridos activos.
* El tiempo de espera global de recorrido sigue aplicándose a los recorridos en pausa. Por ejemplo, si un perfil estuvo en un recorrido durante 90 días y el recorrido está en pausa, este perfil seguirá saliendo del recorrido el día 91.
* Hay un nuevo estado de recorrido **Reanudando** disponible cuando se reanuda un recorrido. Empieza a escuchar eventos de recorrido de nuevo cuando hace clic en **Reanudar**.  Hay algunos retrasos en la reanudación de los perfiles en el recorrido. Cuando el recorrido pasa de **Reanudando** a **Activo**, significa que todos los perfiles se han reanudado. **Reanudar** puede llevar algún tiempo.
* Si los perfiles se mantienen en un recorrido y este recorrido se reanuda automáticamente pasados XX días, los perfiles continúan el recorrido y no se pierden. Si desea soltarlos, debe reanudar manualmente la recorrido.
  <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

## Pausa de un recorrido {#journey-pause-steps}

Puede pausar cualquier recorrido activo.

Para pausar el recorrido, siga estos pasos:

1. Abra el recorrido en el que desee hacer una pausa.
1. Haga clic en el botón **...Más** de la sección superior derecha del lienzo de recorrido y seleccione **Pausar**.

   ![Pausar el botón de recorrido](assets/pause-journey-button.png)

1. Seleccione cómo administrar los perfiles que están actualmente en el recorrido.

   ![Pausar opciones de recorrido](assets/pause-confirm.png){width="50%" align="left"}

   Puede hacer lo siguiente:

   * Mantener perfiles
   * Descartar perfiles

1. Haga clic en el botón **Pausar** para confirmar.

Un recorrido se puede pausar durante un máximo de 14 días.

## Cómo reanudar un recorrido pausado {#journey-resume-steps}

Los recorridos en pausa se pueden reanudar manualmente en cualquier momento.

Para reanudar un recorrido, siga estos pasos:

1. Abra el recorrido que desea reanudar.
1. Haga clic en el botón **...Más** de la sección superior derecha del lienzo de recorrido y seleccione **Reanudar**.




