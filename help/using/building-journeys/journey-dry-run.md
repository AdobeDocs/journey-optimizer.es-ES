---
solution: Journey Optimizer
product: journey optimizer
title: Ensayo del recorrido
description: Obtenga información sobre cómo publicar un recorrido en el modo de ejecución en seco
feature: Journeys
role: User
level: Intermediate
badge: label="Disponibilidad limitada" type="Informative"
keywords: publicar, recorrido, en directo, validez, comprobar
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
source-git-commit: 8f3d619adfb7b2f3dd876da7a3a6eba1fda6dd6b
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 4%

---

# Ensayo del recorrido {#journey-dry-run}

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="Modo de ejecución en seco"
>abstract="Este recorrido está en Dry run. Recorrido Dry run es un modo especial de publicación de recorrido en Adobe Journey Optimizer que permite a los profesionales del recorrido probar un recorrido utilizando datos de producción reales sin ponerse en contacto con clientes reales ni actualizar información de perfil.  Esta función ayuda a los profesionales del recorrido a confiar en el diseño del recorrido y la segmentación de audiencia antes de publicarla en directo."


>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run_start"
>title="Publicación de un recorrido en modo de ejecución en seco"
>abstract="Recorrido Dry run es un modo especial de publicación de recorrido en Adobe Journey Optimizer que permite a los profesionales del recorrido probar un recorrido utilizando datos de producción reales. Una vez que haya diseñado su recorrido, pruébelo para confirmar que es funcional y asegurarse de que los pasos sean correctos. Este modo de publicación le permite probar un recorrido sin enviar comunicaciones a los perfiles."

Recorrido Dry run es un modo especial de publicación de recorrido en Adobe Journey Optimizer que permite a los profesionales del recorrido probar un recorrido utilizando datos de producción reales sin ponerse en contacto con clientes reales ni actualizar información de perfil.  Esta función ayuda a los profesionales del recorrido a confiar en el diseño del recorrido y la segmentación de audiencia antes de publicarla en directo.


>[!AVAILABILITY]
>
>Esta funcionalidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada) y se implementará globalmente en una versión futura.


## Ventajas principales {#journey-dry-run-benefits}

Recorrido La ejecución en seco aumenta la confianza del profesional y el éxito del recorrido al permitir pruebas seguras y basadas en datos de los recorridos del cliente utilizando datos de producción reales, sin el riesgo de ponerse en contacto con los clientes o alterar la información del perfil. Esta función permite a los profesionales del recorrido validar el alcance de la audiencia y la lógica de rama antes de lanzarse, lo que garantiza que los recorridos se alineen con los objetivos empresariales deseados.

Con la ejecución en seco de Recorrido, obtiene la capacidad de identificar problemas de forma temprana, optimizar las estrategias de segmentación y mejorar el diseño del recorrido en función de datos reales, no de suposiciones. Integrado directamente en el lienzo del recorrido, Dry run ofrece informes intuitivos y visibilidad sobre los indicadores de rendimiento clave, lo que permite a los equipos iterar con confianza y optimizar los flujos de trabajo de aprobación. Esto mejora la eficacia operativa, reduce el riesgo de inicio y mejora los resultados de participación del cliente.

En última instancia, esta función mejora el tiempo de respuesta al valor y reduce los errores de recorrido.

Recorrido Dry run trae:

1. **Entorno de prueba seguro**: no se establece contacto con los perfiles en modo de ejecución en seco, lo que garantiza que no haya riesgo de enviar comunicaciones ni de afectar a los datos activos.
1. **Perspectivas de audiencias**: los profesionales del Recorrido pueden predecir la accesibilidad de la audiencia en varios nodos de recorrido, incluidas las exclusiones, las exclusiones y otras condiciones.
1. **Comentarios en tiempo real**: las métricas se muestran directamente en el lienzo del recorrido, de forma similar a los informes en vivo, lo que permite a los profesionales del recorrido refinar su diseño de recorrido.


>[!CAUTION]
>
>* Los permisos para iniciar la ejecución en seco están restringidos a los usuarios con el permiso de alto nivel **[!DNL Publish journeys]**. Los permisos para detener la ejecución en seco están restringidos a los usuarios con el permiso de alto nivel **[!DNL Manage journeys]**. Obtenga más información acerca de la administración de los derechos de acceso de los usuarios de [!DNL Journey Optimizer] en [esta sección](../administration/permissions-overview.md).
>
>* Antes de empezar a usar la capacidad de ejecución en seco, [lea las protecciones y limitaciones](#journey-dry-run-limitations).


## Iniciar una ejecución en seco {#journey-dry-run-start}

Puede utilizar la capacidad de ejecución en seco en cualquier recorrido de borrador sin errores.

Para activar la ejecución en seco, siga estos pasos:

1. Abra el recorrido que desee probar.
1. Haz clic en el botón **Ejecutar en seco**.

   ![Iniciar la ejecución en seco del recorrido](assets/dry-run-button.png)

1. Confirme la publicación.

   Aparece un mensaje de estado, **Activando la ejecución en seco**, mientras se produce la transición.

1. Una vez activado, el recorrido entra en modo **Ejecución en seco**.

## Monitorización de una ejecución en seco {#journey-dry-monitor}

Una vez iniciada la publicación en modo seco, puede visualizar la ejecución del recorrido y cómo progresan los perfiles a través de las ramas y nodos del recorrido.

Las métricas se muestran directamente en el lienzo del recorrido.

![Supervisar la ejecución de la ejecución en seco de recorrido](assets/dry-run-metrics.png)

Para cada actividad, puede comprobar lo siguiente:

* **[!UICONTROL Ingresado]**: Cantidad total de personas que ingresaron a esta actividad.
* **[!UICONTROL Salidas (se cumplen los criterios de salida)]**: Número total de personas que salieron del recorrido de esa actividad debido a un criterio de salida.
* **[!UICONTROL Salida forzada]**: Número total de personas que salieron del recorrido mientras estaba en pausa debido a una configuración del profesional del recorrido. Esta métrica siempre es igual a cero para los recorridos en el modo de ejecución en seco.
* **[!UICONTROL Error]**: Número total de personas que tuvieron un error en esa actividad.


En el nivel de recorrido, puede comprobar lo siguiente:

* Número total de **perfiles ingresados**
* Número total de **perfiles abandonados**
* Número total de **perfiles con error**
* Número total de **perfiles descartados** en el recorrido

También puede acceder a los **informes de las últimas 24 horas** y a los **informes permanentes** de la ejecución en seco. Para acceder a estos informes, haga clic en el botón **Ver informe** en la esquina superior derecha del lienzo de recorrido.

![Acceda a los informes para la ejecución de la ejecución en seco de recorrido](assets/dry-run-report.png)

>[!CAUTION]
>
> Los datos de informes solo están disponibles cuando la ejecución en seco está **activa**.  Una vez que se detenga, ya no se podrá acceder a los datos de informes. Utilice el botón **Exportar** situado encima de los informes para descargarlos si es necesario.


## Detener una carrera en seco {#journey-dry-run-stop}

Los recorridos de ejecución en seco **deben** detenerse manualmente.

Haga clic en el botón **Cerrar** para finalizar la prueba y luego haga clic en **Volver al borrador** para confirmar.

<!-- After 14 days, Dry run journeys automatically transition to the **Draft** status.-->

## Mecanismos de protección y limitaciones {#journey-dry-run-limitations}

* El modo de ejecución en seco no está disponible para recorridos que contengan eventos de reacción
* Los perfiles en el modo de ejecución en seco se contabilizan como perfiles atractivos
* Los recorridos en el modo de ejecución en seco se cuentan hacia la cuota de recorrido en directo
* Los recorridos de ejecución en seco no afectan a las reglas empresariales
* Al crear una nueva versión de recorrido, si una versión de recorrido anterior es **Live**, la activación de ejecución en seco no está permitida en la nueva versión.
* Recorrido La ejecución en seco genera stepEvents. Estos stepEvents tienen un indicador específico y un ID de ejecución seca:
   * `_experience.journeyOrchestration.stepEvents.inDryRun` devuelve `true` si la ejecución en seco está activada y `false` en caso contrario
   * `_experience.journeyOrchestration.stepEvents.dryRunID` devuelve el ID de una instancia de ejecución en seco

* Durante la ejecución en seco, el recorrido se ejecuta con las siguientes especificidades:

   * **No se ejecutan los nodos de acción del canal**, incluidas las notificaciones por correo electrónico, SMS o push
   * **Las acciones personalizadas** se deshabilitaron durante la ejecución en seco y sus respuestas se establecieron en null
   * **Los nodos de espera** se omiten durante la ejecución en seco.
     <!--You can override the wait block timeouts, then if you have wait blocks duration longer than allowed dry run journey duration, then that branch will not execute completely.-->
   * **Las fuentes de datos**, incluidas las fuentes de datos externas, se ejecutan de manera predeterminada