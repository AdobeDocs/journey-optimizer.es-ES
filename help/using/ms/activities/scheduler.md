---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Planificador
description: Aprenda a utilizar la actividad Planificador en una campaña orquestada
hide: true
hidefromtoc: true
exl-id: da77a0bf-7b17-40fc-b2cb-2f0940152e64
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 20%

---

# Planificador {#scheduler}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Actividad planificador"
>abstract="La actividad **Scheduler** le permite programar el inicio de la campaña orquestada. La actividad debe considerarse como un inicio programado. Solo se puede utilizar como la primera actividad de la campaña orquestada."


La actividad **Scheduler** es una actividad **Flow control**. Le permite programar cuándo se inicia la campaña orquestada. La actividad debe considerarse como un inicio programado. Solo se puede utilizar como la primera actividad de la campaña orquestada.

## Prácticas recomendadas{#scheduler-best-practices}

* No programe una campaña orquestada para que se ejecute durante más de 15 minutos, ya que podría limitar el rendimiento general del sistema y crear bloques en la base de datos.
* Si desea realizar una entrega de una sola toma en la campaña orquestada, puede agregar una actividad de planificador y configurarla para que se ejecute **Una vez**. También puede definir **Schedule** en la configuración de la entrega.
* Si desea realizar un envío recurrente en la campaña orquestada, debe utilizar una actividad **Scheduler** y establecer la frecuencia de ejecución. La actividad de entrega recurrente no permite definir una programación.

## Configure la actividad Planificador {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_validity"
>title="Validez del planificador"
>abstract="Puede definir un período de validez para el planificador. Puede ser permanente (predeterminado) o válido hasta una fecha específica."


>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_options"
>title="Opciones del planificador"
>abstract="Defina la frecuencia del planificador. Se puede ejecutar en un momento específico, una o varias veces al día, a la semana o al mes."

Siga estos pasos para configurar la actividad **Planificador**:

![](../assets/workflow-scheduler.png)

1. Agregue una actividad **Scheduler** a su campaña orquestada.

1. Configure **Frecuencia de ejecución**:

   * **Una vez**: la campaña orquestada se ejecuta una sola vez.

   * **Diario**: la campaña orquestada se ejecuta a una hora específica una vez al día.

   * **Varias veces al día:** la campaña orquestada se ejecuta regularmente varias veces al día. Puede configurar ejecuciones en momentos específicos o de forma periódica.

   * **Semanal**: la campaña orquestada se ejecuta en un momento determinado una o varias veces a la semana.

   * **Mensual**: la campaña orquestada se ejecuta en un momento determinado una o varias veces al mes. Puede seleccionar meses cuando necesite que se ejecute la campaña orquestada. También puede configurar ejecuciones en días de semana del mes específicos, como el segundo martes de mes.

1. Defina los detalles de ejecución según la frecuencia seleccionada. Los campos de detalle pueden variar según la frecuencia utilizada (tiempo, frecuencia de repetición, días especificados, etc.).

1. Haga clic en **Previsualizar horas de inicio** para comprobar la programación de las siguientes diez ejecuciones de la campaña orquestada.

1. Defina el periodo de validez del planificador:

   * **Permanente (nunca caduca)**: la campaña orquestada se ejecuta según la frecuencia especificada, sin límites en el lapso de tiempo ni número de iteraciones.

   * **Período de validez**: la campaña orquestada se ejecuta según la frecuencia especificada, hasta una fecha específica. Debe especificar las fechas de inicio y finalización.

>[!NOTE]
>
>Si desea iniciar la campaña orquestada de inmediato, puede hacer clic en **Ejecutar tarea pendiente** en la barra de acciones superior del planificador. Este botón solo está disponible cuando ha iniciado la campaña orquestada.

## Ejemplo{#scheduler-example}

En el siguiente ejemplo, la actividad se configura de modo que la campaña orquestada se ejecute varias veces al día a las 9 y las 12 de la mañana, todos los días de la semana del 1 de octubre de 2025 al 1 de enero de 2026.

![](../assets/workflow-scheduler2.png)
