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
source-git-commit: 68a115d3075f7953501b10f2057b5aa87e0fcf92
workflow-type: tm+mt
source-wordcount: '2004'
ht-degree: 0%

---

# Pausar un recorrido {#journey-pause}

>[!CONTEXTUALHELP]
>id="ajo_journey_pause"
>title="Pausar el recorrido"
>abstract="Pausar un recorrido activo para evitar que entren nuevos perfiles. Elija si desea descartar los perfiles que están actualmente en la recorrido o mantenerlos en su lugar. Si se retienen, se reanudará la ejecución en la siguiente actividad de acción una vez que se reinicie el recorrido. Perfecto para actualizaciones o paradas de emergencia sin perder progreso."

Puede pausar los recorridos activos, realizar todos los cambios necesarios y reanudarlos de nuevo en cualquier momento.<!--You can choose whether the journey is resumed at the end of the pause period, or whether it stops completely. --> Durante la pausa, puede [aplicar filtros globales](#journey-global-filters) para excluir perfiles en función de sus atributos. El recorrido se reanuda automáticamente al final del período de pausa. También puede [reanudarlo manualmente](#journey-resume-steps).

>[!AVAILABILITY]
>
>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una versión futura.


## Ventajas principales {#journey-pause-benefits}

Los recorridos de pausa y reanudación proporcionan a los profesionales del recorrido un mayor control y flexibilidad al permitir que los recorridos en directo se suspendan temporalmente sin interrumpir la experiencia del cliente. Cuando está en pausa, no se envían comunicaciones y los perfiles permanecen en estado suspendido hasta que se reanuda la recorrido.

Esta capacidad reduce el riesgo de enviar mensajes no deseados durante errores o actualizaciones (p. ej.: cambio en el contenido del mensaje), admite una administración más segura del recorrido y aumenta la confianza del profesional. La visibilidad de los recorridos en pausa y su estado directamente en la IU mejora aún más la transparencia y la agilidad operativa.

>[!CAUTION]
>
>* Los permisos para pausar y reanudar recorridos están restringidos a los usuarios con el permiso de alto nivel **[!DNL Publish journeys]**. Obtenga más información acerca de la administración de los derechos de acceso de los usuarios de [!DNL Journey Optimizer] en [esta sección](../administration/permissions-overview.md).
>
>* Antes de empezar a usar la capacidad de pausa/reanudación, [lea las protecciones y limitaciones](#journey-pause-guardrails).


## Pausa de un recorrido {#journey-pause-steps}

Puede pausar cualquier recorrido de **Live**.

Para pausar el recorrido, siga estos pasos:

1. Abra el recorrido en el que desee hacer una pausa.
1. Haga clic en el botón **...Más** de la sección superior derecha del lienzo de recorrido y seleccione **Pausar**.

   ![Pausar el botón de recorrido](assets/pause-journey-button.png){width="80%" align="left"}

1. Seleccione cómo administrar los perfiles que están actualmente en el recorrido.

   ![Pausar opciones de recorrido](assets/pause-confirm.png){width="50%" align="left"}

   Puede hacer lo siguiente:

   * **Retener** perfiles: los perfiles esperarán a que se reanude el recorrido
   * **Descartar** perfiles: los perfiles se excluirán del recorrido en el siguiente nodo de acción

1. Haga clic en el botón **Pausar** para confirmar.

Desde la lista de recorridos, puede pausar uno o varios recorridos **Live**. Para pausar un grupo de recorridos (_pausa masiva_), selecciónelos en la lista y haga clic en el botón **Pausar** de la barra azul en la parte inferior de la pantalla. El botón **Pausar** solo está disponible cuando se seleccionan **recorridos en vivo**.

![Pausa masiva de dos recorridos activos desde la barra inferior](assets/bulk-pause-journeys.png)

### Comportamiento en recorridos pausados

Cuando un recorrido está en pausa, las entradas nuevas siempre se descartan, independientemente del modo Mantener/Descartar.

La administración de perfiles cuando se pausa un recorrido depende de la actividad. Los comportamientos se detallan a continuación. Para obtener información completa, vea también esta [muestra de extremo a extremo](#journey-pause-sample).

| Actividad de recorrido | Administración de perfiles |
|-------------------------|--------------------------------------------------|
| [Calificación de audiencias](audience-qualification-events.md) | En el primer nodo: descartado <br> En otros nodos: igual que en un recorrido activo, sin embargo, si la calificación de audiencia es después de una actividad de acción y el usuario está en pausa en esa acción, la calificación de audiencia se descarta. |
| [Evento unitario](general-events.md) | En el primer nodo: descartado <br>En otros nodos: igual que en un recorrido activo, sin embargo, si el evento es después de una actividad de acción y el usuario está en pausa en esa acción, el evento se descarta. |
| [Leer audiencia](read-audience.md) | Igual comportamiento que en un recorrido activo, con algunas características específicas: <br>1.  Si se presionó <strong>Pausa</strong> después de que se iniciara la actividad de <strong>Leer audiencia</strong>, los perfiles que hayan entrado en el recorrido continuarán (hasta la siguiente actividad de <strong>Acción</strong>). A medida que el recorrido lee audiencias a una velocidad determinada, si la audiencia completa aún no ha entrado, los perfiles restantes en la cola se descartarán.   <br>2. Para ejecuciones únicas: no se muestra ningún error en el momento de la reanudación si la fecha programada era anterior a la fecha de reanudación. Ese horario sería ignorado. <br>3. Para recorridos incrementales: <br>- Si la pausa se produce antes de la primera aparición, al reanudar la audiencia completa se reproduciría. <br>: si se produce una pausa, por ejemplo, en el cuarto día de una periodicidad diaria y el recorrido permanece en pausa hasta el noveno día, al reanudar, se incluirán todos los perfiles que hayan entrado del cuarto al noveno |
| [Reacción](reaction-events.md) | Se trata del mismo comportamiento que en un recorrido activo; sin embargo, si la reacción se produce después de una actividad de acción y el usuario está en pausa para dicha acción, el evento se descarta. |
| [Espera](wait-activity.md) | Mismo comportamiento que en un recorrido activo |
| [Condición](condition-activity.md) | Mismo comportamiento que en un recorrido activo |
| Decisión de contenido | Los perfiles se aparcan o se descartan en función de lo que el usuario haya elegido cuando el recorrido se ha pausado |
| [Acción de canal](journeys-message.md) | Los perfiles se aparcan o se descartan en función de lo que el usuario haya elegido cuando el recorrido se ha pausado |
| [Acción personalizada](../action/action.md) | Los perfiles se aparcan o se descartan en función de lo que el usuario haya elegido cuando el recorrido se ha pausado |
| [Actualizar perfil](update-profiles.md) y [Saltar](jump.md) | Mismo comportamiento que en un recorrido activo |
| [Source de datos externos](../datasource/external-data-sources.md) | Mismo comportamiento que en un recorrido activo |
| [Criterios de salida](journey-properties.md#exit-criteria) | Mismo comportamiento que en un recorrido activo |

## Cómo reanudar un recorrido pausado {#journey-resume-steps}

>[!CONTEXTUALHELP]
>id="ajo_journey_resume"
>title="Reanudar el recorrido"
>abstract="Reanude un recorrido pausado para permitir que los nuevos perfiles vuelvan a entrar. Si los perfiles estaban esperando durante la pausa, continuarán con su recorrido. Ideal para reiniciar los recorridos de forma segura después de actualizaciones o pausas."

Los recorridos en pausa se reanudan automáticamente al final del período máximo de pausa de 14 días. Se pueden reanudar manualmente en cualquier momento. Reanudar un recorrido pausado permite que los nuevos perfiles vuelvan a entrar. Si los perfiles estaban esperando durante la pausa, continuarán con su recorrido. Ideal para reiniciar los recorridos de forma segura después de actualizaciones o pausas.

Para reanudar un recorrido en pausa y comenzar a escuchar eventos de recorrido de nuevo, siga estos pasos:

1. Abra el recorrido que desea reanudar.
1. Haga clic en el botón **...Más** de la sección superior derecha del lienzo de recorrido y seleccione **Reanudar**.

   El recorrido cambia al estado **Reanudando**. Cuando el recorrido se reanuda, las nuevas entradas comienzan en un minuto. La reanudación de los perfiles retenidos puede llevar algún tiempo.  Ya que todos los perfiles deben reanudarse para que el recorrido vuelva a estar **Activo**, la transición del estado **Reanudando** al **Activo** puede tomar algún tiempo.

1. Haga clic en el botón **Reanudar** para confirmar.


Desde la lista de sus recorridos, puede reanudar uno o varios **recorridos pausados**. Para reanudar un grupo de recorridos (_reanudación masiva_), selecciónelos y haga clic en el botón **Reanudar** ubicado en la barra azul en la parte inferior de la pantalla. Tenga en cuenta que el botón **Reanudar** solo estará disponible cuando se seleccionen **recorridos en pausa**.


## Aplicación de un filtro global a perfiles en un recorrido pausado  {#journey-global-filters}

Cuando un recorrido está en pausa, puede aplicar un filtro global basado en atributos de perfil. Este filtro habilita la exclusión de perfiles que coinciden con la expresión definida en el momento de la reanudación. Una vez establecido el filtro global, se aplica a los nodos de acción, incluso para la entrada de nuevos perfiles. Los perfiles que coincidan con los criterios y los nuevos perfiles que entren se excluirán del recorrido **en el siguiente nodo de acción** que encuentren.

Por ejemplo, para excluir todos los clientes franceses de un recorrido en pausa, siga estos pasos:

1. Desplácese hasta el recorrido en pausa que desee modificar.

1. Haga clic en el icono **Criterios de salida y filtro global**.

   ![Agregar un filtro global a un recorrido en pausa](assets/add-global-filter.png){width="50%" align="left"}

1. En la configuración de **Criterios de salida y filtro global**, haga clic en **Agregar filtro global** para definir un filtro basado en atributos de perfil.

1. Establezca la expresión para excluir perfiles donde el atributo de país sea igual a Francia.

   ![Agregar un filtro global a un recorrido en pausa](assets/add-country-filter.png){width="50%" align="left"}

1. Guarde el filtro y haga clic en el botón **Actualizar recorrido** para aplicar los cambios.

1. [Reanudar el recorrido](#journey-resume-steps).

   En el momento de la reanudación, todos los perfiles con el atributo de país establecido en Francia se excluirán automáticamente del recorrido en el siguiente nodo de acción. Cualquier nuevo perfil con el atributo de país establecido en Francia que intente entrar en el recorrido se bloqueará en el siguiente nodo de acción.

Tenga en cuenta que las exclusiones de perfiles para perfiles que se encuentran actualmente en la recorrido y para perfiles nuevos solo se producirán cuando lleguen a un nodo de acción.

>[!CAUTION]
>
>* Solo puede establecer **un** filtro global por recorrido.
>
>* Solo puede crear, actualizar o eliminar un filtro global en **recorridos pausados**.

## Mecanismos de protección y limitaciones {#journey-pause-guardrails}

* Una versión de recorrido se puede pausar durante un máximo de 14 días.
* Los recorridos en pausa se consideran en todas las reglas de negocio, del mismo modo que si estuvieran activos.
* Los perfiles se &quot;descartan&quot; en un recorrido pausado cuando llegan a una actividad de acción. Si permanecen en espera durante el tiempo en que se pausa un recorrido y salen después de que se haya reanudado, continuarán con el recorrido y no se descartarán.
* Incluso después de la pausa, a medida que los eventos se siguen procesando, estos eventos se contarán hacia el número de Eventos de Recorrido por segundo de cuota, después de lo cual la restricción se obtiene por unitaria.
* Los perfiles que habían entrado en el recorrido pero que se descartaron durante la pausa se contarían como perfiles atractivos.
* Cuando los perfiles se mantienen en un recorrido pausado, en el momento de la reanudación se actualizan los atributos del perfil
* Las condiciones se siguen ejecutando en recorridos pausados, por lo que si un recorrido se ha pausado debido a problemas de calidad de datos, cualquier condición anterior a un nodo de acción se puede evaluar con datos incorrectos.
* Para el recorrido de audiencia de lectura incremental basado en audiencias, se tiene en cuenta la duración de la pausa. Por ejemplo, para un recorrido diario, si se pausó el 2 y se reanudó el 5 del mes, la ejecución del 6 tomará todos los perfiles que se hayan clasificado del 1 al 6. Este no es el caso de la calificación de audiencias o de los recorridos basados en eventos (si se recibe una calificación de audiencia o un evento durante una pausa, esos eventos se descartan).
* Los recorridos en pausa se cuentan hacia la cuota de recorridos activos.
* El tiempo de espera global de recorrido sigue aplicándose a los recorridos en pausa. Por ejemplo, si un perfil estuvo en un recorrido durante 90 días y el recorrido está en pausa, este perfil seguirá saliendo del recorrido el día 91.
* Si los perfiles se mantienen en un recorrido y este recorrido se reanuda automáticamente pasados unos días, los perfiles continúan con el recorrido y no se pierden. Si desea soltarlos, debe detener el recorrido.
* En los recorridos en pausa, las alertas no se activan para las alertas de segmentos por lotes.
* No hay registros de auditoría en el sistema cuando el estado de pausa de la recorrido después de 14 días finaliza.
* Algunos perfiles descartados pueden ser visibles en el Evento de paso de Recorrido, pero no en los informes. Por ejemplo: descartar eventos empresariales para la audiencia de lectura, los trabajos de audiencia de lectura se pierden debido a un recorrido pausado, los eventos descartados cuando la actividad de evento fue después de una acción en la que el perfil estaba esperando.
  <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

## Muestra de extremo a extremo {#journey-pause-sample}

Veamos el ejemplo del recorrido siguiente:

![Muestra de un recorrido](assets/pause-journey-sample.png)

Al pausar este recorrido, selecciona si los perfiles son **Descartados** o **Retenidos** y luego la administración de perfiles es la siguiente:

1. Actividad **AddToCart**: todas las entradas de perfiles nuevos están bloqueadas. Si un perfil ya ha entrado en el recorrido antes de una pausa, continuará hasta el siguiente nodo de acción.
1. Actividad **Wait**: los perfiles siguen esperando normalmente en el nodo y lo cerrarán, incluso si el recorrido está en pausa.
1. **Condición**: los perfiles siguen atravesando condiciones y se mueven a la rama derecha, según la expresión definida en la condición.
1. Actividades **Push**/**Email**: durante un recorrido en pausa, los perfiles comienzan a esperar o se descartan (según la elección hecha por el usuario en el momento de la pausa) en el siguiente nodo de acción. Por lo tanto, los perfiles empezarán a esperar o se descartarán allí.
1. **Eventos** después de nodos de acción: si un perfil está esperando en un nodo de acción y hay un evento después de él, si ese evento se activa, el perfil se descartará.

Según este comportamiento, puede ver que los números de perfiles aumentan cuando se pausa el recorrido, principalmente en las actividades antes de las acciones. Por ejemplo, en ese ejemplo, Wait se ignora, lo que aumenta el número de perfiles que pasan por la actividad Condition.

Cuando reanude este recorrido:

1. Las nuevas entradas al recorrido comienzan en un minuto
1. Los perfiles que estaban esperando actualmente en el recorrido de actividades de acción se reanudan a una velocidad de 5000 tps. A continuación, se introduce la acción que se estaba esperando y se continúa con el recorrido.
