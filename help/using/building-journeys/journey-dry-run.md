---
solution: Journey Optimizer
product: journey optimizer
title: Ensayo del recorrido
description: Obtenga información sobre cómo publicar un recorrido en el modo de ejecución en seco
feature: Journeys
role: User
level: Intermediate
keywords: publicar, recorrido, en directo, validez, comprobar
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/a7qFw84obtkCRDmiqMxQNgvqhI4b6t5suROeF7ZPh1I
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4ebid: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9id: b32bb433-f8c6-4931-8e52-e657230a3bf2id: cfba2953-2ce9-4b00-a00c-71cd338ae63fid: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5520579-b31f-4df7-9281-f0d9f91e2edcid: d00e9f03-e50b-4162-b143-0c0817c937c2id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1946
ht-degree: 8%

---

# Ensayo del recorrido {#journey-dry-run}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a publicar un recorrido en modo de ejecución en seco para probarlo con datos de producción reales sin ponerse en contacto con clientes reales ni actualizar perfiles, de modo que pueda validar su diseño antes de publicarlo.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="Modo de ensayo"
>abstract="Este recorrido está en modo de ensayo. El ensayo del recorrido es un modo especial de publicación de recorrido de [!DNL Adobe Journey Optimizer] que permite a los profesionales de recorridos probarlos utilizando datos de producción reales sin ponerse en contacto con clientes reales ni actualizar la información de perfil.  Esta función ayuda a los profesionales de recorridos a confiar en el diseño del recorrido y en la segmentación del público antes de publicarlo en vivo."


>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run_start"
>title="Publicación de un recorrido en modo de ensayo"
>abstract="El ensayo del recorrido es un modo especial de publicación de recorrido de [!DNL Adobe Journey Optimizer] que permite a los profesionales de recorridos probarlos utilizando datos de producción reales. Una vez diseñado un recorrido, una ejecución en seco confirma que funciona y garantiza que los pasos son correctos. Este modo de publicación le permite realizar una prueba preliminar de un recorrido sin enviar comunicaciones a los perfiles."

El ensayo del recorrido es un modo especial de publicación de recorrido de [!DNL Adobe Journey Optimizer] que permite a los profesionales de recorridos probarlos utilizando datos de producción reales sin ponerse en contacto con clientes reales ni actualizar la información de perfil.  Esta función ayuda a los profesionales de recorridos a confiar en el diseño del recorrido y en la segmentación del público antes de publicarlo en vivo.

➡️ [Obtenga más información acerca de la ejecución sin recorrido en este vídeo](#dry-run-video)

## Ventajas principales {#journey-dry-run-benefits}

Recorrido La ejecución en seco aumenta la confianza del profesional y el éxito del recorrido al permitir pruebas seguras y basadas en datos de los recorridos del cliente utilizando datos de producción reales, sin el riesgo de ponerse en contacto con los clientes o alterar la información del perfil. Esta función permite a los profesionales del recorrido validar el alcance de la audiencia y la lógica de rama antes de lanzarse, lo que garantiza que los recorridos se alineen con los objetivos empresariales deseados.

Con la ejecución en seco de Recorrido, obtiene la capacidad de identificar problemas de forma temprana, optimizar las estrategias de segmentación y mejorar el diseño del recorrido en función de datos reales, no de suposiciones. Integrado directamente en el lienzo del recorrido, Dry run ofrece informes intuitivos y visibilidad sobre los indicadores de rendimiento clave, lo que permite a los equipos iterar con confianza y optimizar los flujos de trabajo de aprobación. Esto mejora la eficacia operativa, reduce el riesgo de inicio y mejora los resultados de participación del cliente.

En última instancia, esta función mejora el tiempo de respuesta al valor y reduce los errores de recorrido.

Recorrido Dry run trae:

1. **Entorno de prueba seguro**: no se establece contacto con los perfiles en modo de ejecución en seco, lo que garantiza que no haya riesgo de enviar comunicaciones ni de afectar a los datos activos.
1. **Perspectivas de audiencias**: los profesionales del Recorrido pueden predecir la accesibilidad de la audiencia en varios nodos de recorrido, incluidas las exclusiones y las exclusiones basadas en condiciones de Recorrido.
1. **Comentarios en tiempo real**: las métricas se muestran directamente en el lienzo del recorrido, de forma similar a los informes en vivo, lo que permite a los profesionales del recorrido refinar su diseño de recorrido.

## Lógica de ejecución de ejecución en seco {#journey-dry-run-exec}

Durante la ejecución en seco, el recorrido se ejecuta en modo de simulación, aplicando los siguientes comportamientos específicos a cada actividad de recorrido sin activar acciones reales:

* **Los nodos de acción del canal**, incluidas las notificaciones por correo electrónico, SMS o push, no se ejecutan.
* **Las acciones personalizadas** se deshabilitaron durante la ejecución en seco y sus respuestas se establecieron en null.

  Para mejorar la legibilidad, las acciones personalizadas y las actividades de canal aparecen atenuadas durante la ejecución de una ejecución en seco.

  ![Actividades de acción atenuadas en un recorrido de ejecución en seco](assets/dry-run-greyed-activities.png){width="80%"}

* Las **fuentes de datos**, incluidas las fuentes de datos externas, y las actividades **Espera** están deshabilitadas de manera predeterminada durante la ejecución en seco. Sin embargo, puede cambiar este comportamiento [al activar el modo de ejecución en seco](#journey-dry-run-start).

* Los nodos **Reaction** no se han ejecutado: todos los perfiles que entren en ellos se cerrarán correctamente. Sin embargo, se aplican las siguientes reglas de prioridad:

   * Si se usa un nodo **Reaction** con uno o varios nodos **unitary event** en paralelo, los perfiles siempre pasarán por el evento de reacción.
   * Si se usa un nodo **Reaction** con uno o varios nodos **reaction event** en paralelo, los perfiles siempre pasarán por el primero del lienzo (el de arriba).

>[!CAUTION]
>
>* Los permisos para iniciar una ejecución en seco están restringidos a los usuarios con el permiso de alto nivel **[!DNL Publish journeys]**. Los permisos para detener una ejecución en seco están restringidos a los usuarios con el permiso de alto nivel **[!DNL Manage journeys]**. Obtenga más información acerca de la administración de los derechos de acceso de los usuarios de [!DNL Journey Optimizer] en [esta sección](../administration/permissions-overview.md).
>
>* Antes de empezar a usar la capacidad de ejecución en seco, [lea las protecciones y limitaciones](#journey-dry-run-limitations).

## Iniciar una ejecución en seco {#journey-dry-run-start}

Puede utilizar la capacidad de ejecución en seco en cualquier recorrido de borrador sin errores.

Para activar la ejecución en seco, siga estos pasos:

1. Abra el recorrido que desee probar.
1. Seleccione el botón **[!UICONTROL Ejecutar en seco]**.

   ![Iniciar la ejecución en seco del recorrido](assets/dry-run-button.png)

1. Seleccione si desea habilitar o deshabilitar las actividades **Wait** y las llamadas de **External data sources**, y confirme la publicación Dry run.

   ![Confirmar la publicación de la ejecución en seco de recorrido](assets/dry-run-publish.png){width="50%"}

   Aparece un mensaje de estado, **[!UICONTROL Activando la ejecución en seco]**, mientras se produce la transición.

1. Una vez activado, el recorrido entra en modo **[!UICONTROL Ejecución en seco]**.


## Monitorización de una ejecución en seco {#journey-dry-monitor}

Una vez iniciada la publicación en modo seco, puede visualizar la ejecución del recorrido y cómo progresan los perfiles a través de las ramas y nodos del recorrido.

Las métricas se muestran directamente en el lienzo del recorrido. Obtenga más información acerca de las métricas y los informes en directo de recorrido en [Informe en vivo en el lienzo de recorrido](report-journey.md).

![Supervisar la ejecución de la ejecución en seco de recorrido](assets/dry-run-metrics.png)

También puede acceder a los **informes de las últimas 24 horas** y a los **informes permanentes** de la ejecución en seco. Para acceder a estos informes, haga clic en el botón **Ver informe** en la esquina superior derecha del lienzo de recorrido.

![Acceda a los informes para la ejecución de la ejecución en seco de recorrido](assets/dry-run-report.png)

>[!CAUTION]
>
> Los datos de informes solo están disponibles cuando la ejecución en seco está **activa**.  Una vez que se detenga, ya no se podrá acceder a los datos de informes. Utilice el botón **Exportar** situado encima de los informes para descargarlos si es necesario.


## Detener una carrera en seco {#journey-dry-run-stop}

Después de 14 días, los recorridos de ejecución en seco pasan automáticamente al estado **[!UICONTROL Borrador]**.

Los recorridos de ejecución en seco también se pueden detener manualmente. Para desactivar el modo de ejecución en seco, siga estos pasos:

1. Abra el recorrido de ejecución en seco que desee detener.
1. Seleccione el botón **[!UICONTROL Cerrar]** para finalizar la prueba.
Los vínculos a las últimas 24 horas y todos los informes de tiempo están disponibles en la pantalla de confirmación.

   ![Detener la ejecución de la ejecución en seco de recorrido](assets/dry-run-stop.png){width="50%"}

1. Haga clic en **[!UICONTROL Volver al borrador]** para confirmar.


## Mecanismos de protección y limitaciones {#journey-dry-run-limitations}

* Los perfiles en modo de ejecución en seco se cuentan hacia [Perfiles atractivos](../audience/license-usage.md)
* Los recorridos en el modo de ejecución en seco se cuentan hacia la cuota de recorrido en directo
* Los recorridos de ejecución en seco no afectan a las reglas empresariales
  <!--* When creating a new journey version, if a previous journey version is **Live**, then the Dry run activation is not allowed on the new version.-->
* **Las acciones Jump** no están habilitadas en la ejecución en seco.
Cuando un recorrido de origen déclencheur un evento **Jump** a uno de destino, ese evento de salto no sería aplicable a una versión de recorrido de ejecución en seco. Por ejemplo, si la última versión de un recorrido está en Dry run y la anterior es **Live**, entonces el evento de salto ignoraría la versión de Dry run y solo sería aplicable para la versión de **Live**.

## Eventos de paso de recorrido y simulación {#journey-step-events}

Recorrido La ejecución en seco genera **stepEvents**. Estos stepEvents tienen un indicador específico y un ID de ejecución en seco: `inDryRun` y `dryRunID`.

![atributos de esquema de ejecución en seco de Recorrido](assets/dry-run-attributes.png)

* `_experience.journeyOrchestration.stepEvents.inDryRun` devuelve `true` cuando el recorrido está en modo de ejecución en seco y `null` para recorridos de prueba o activos (ejecución en seco).
* `_experience.journeyOrchestration.stepEvents.dryRunID` devuelve el identificador de la instancia de ejecución en seco cuando se encuentra en modo de ejecución en seco; para recorridos de prueba o en directo, es `null`.


Si exporta datos stepEvent a **sistemas externos**, puede filtrar las ejecuciones en seco utilizando el indicador `inDryRun`.

Al analizar **métricas de informes de recorridos** mediante el servicio de consultas [!DNL Adobe Experience Platform], se deben excluir los eventos de paso generados por la ejecución en seco. Para ello, excluya los eventos de paso donde `inDryRun` es `true` (es decir, incluya solo eventos donde `inDryRun` es `null` o `false`).

## Preguntas frecuentes {#faq}

**¿Una ejecución en seco envía mensajes a clientes reales?**

No. La ejecución en seco utiliza datos de producción reales, pero no contacta con perfiles ni actualiza información de perfiles. Las acciones del canal (correo electrónico, SMS, push) no se ejecutan y las acciones personalizadas se deshabilitan con sus respuestas establecidas en `null`.

**¿Qué permisos necesito para iniciar o detener una ejecución en seco?**

El inicio de una ejecución en seco requiere el permiso de alto nivel **[!DNL Publish journeys]**. Detener una ejecución en seco requiere el permiso de alto nivel **[!DNL Manage journeys]**. Obtenga más información en la [sección de permisos](../administration/permissions-overview.md).

**¿En qué recorridos puedo ejecutar una ejecución en seco?**

Puede utilizar la ejecución en seco en cualquier recorrido **[!UICONTROL Draft]** que no contenga errores.

**¿Cuánto dura una ejecución en seco?**

Después de 14 días, los recorridos de ejecución en seco vuelven automáticamente al estado **[!UICONTROL Borrador]**. También puede detener una ejecución en seco manualmente en cualquier momento.

**¿Se ejecutan las actividades de espera y los orígenes de datos externos durante una ejecución en seco?**

De manera predeterminada, las actividades **Wait** y **Data sources** (incluidas las fuentes de datos externas) están deshabilitadas durante una ejecución en seco. Puede cambiar este comportamiento al [activar el modo de ejecución en seco](#journey-dry-run-start).

**¿Los perfiles y recorridos de ejecución en seco se contabilizan en mis cuotas?**

Sí. Los perfiles en el modo de ejecución en seco se contabilizan en [Perfiles atractivos](../audience/license-usage.md) y los recorridos en el modo de ejecución en seco se contabilizan en la cuota de recorrido en directo. Sin embargo, los recorridos de ejecución en seco no afectan a las reglas empresariales.

**¿Puedo seguir accediendo a los informes de ejecución en seco después de detener la prueba?**

No. Los datos de informes solo están disponibles mientras la ejecución en seco esté **activa**. Una vez detenidos, ya no se puede acceder a los datos: use el botón **Exportar** situado encima de los informes para descargarlos de antemano si es necesario.

**¿Cómo excluyo los datos de ejecución en seco de mis informes?**

La ejecución en seco genera **stepEvents** marcados con `inDryRun` y un `dryRunID`. Cuando analice métricas de informes de recorrido con el servicio de consultas [!DNL Adobe Experience Platform], excluya eventos de paso donde `inDryRun` sea `true` (incluya solo eventos donde `inDryRun` sea `null` o `false`).

## Vídeo práctico {#dry-run-video}

Aprenda a secar los recorridos en este vídeo.

>[!VIDEO](https://video.tv.adobe.com/v/3464681/?learn=on&enablevpops)

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica Recorrido Dry run, un modo especial de publicación que permite a los profesionales probar un recorrido utilizando datos de producción reales sin ponerse en contacto con los clientes ni modificar perfiles, y explica cómo iniciar, supervisar, detener y filtrar eventos de paso de ejecución en seco.

**Intenciones:**
* Active el modo de ejecución en seco en un recorrido Borrador para validar la lógica de alcance y rama de la audiencia con datos de producción reales
* Monitorizar las métricas de ejecución de recorrido en el lienzo durante una ejecución en seco
* Detener una ejecución en seco manualmente y devolver el recorrido al estado Borrador
* Filtrar los eventos de paso de ejecución en seco de las consultas de informes mediante el indicador `inDryRun`
* Comprender qué actividades se desactivan o simulan durante una ejecución en seco

**Glosario:**
* **Ejecución en seco**: Modo de publicación de recorrido especial que ejecuta el recorrido con datos de producción reales sin enviar comunicaciones ni actualizar la información de perfil *(específica del producto)*
* **stepEvent**: un registro de conjunto de datos generado automáticamente que captura cada paso que realiza un perfil en un recorrido; los eventos de paso de ejecución en seco llevan `inDryRun=true` y un `dryRunID` *(específico del producto)*
* **Indicador inDryRun**: Un campo booleano en stepEvents que es `true` para ejecuciones de ejecución en seco y `null` para recorridos en directo o de prueba *(específicos del producto)*

**Protecciones:**
* En el modo de ejecución en seco solo se pueden activar los recorridos de borrador sin errores
* Para iniciar una ejecución en seco se requiere el permiso **Publicar recorridos**; para detenerla se requiere **Administrar recorridos**
* Los recorridos de ejecución en seco vuelven automáticamente a Borrador después de 14 días
* Los perfiles procesados durante una ejecución en seco se contabilizan como Perfiles atractivos y la cuota de recorrido activo
* Los nodos de acción del canal (correo electrónico, SMS, push) y las acciones personalizadas no se ejecutan durante la ejecución en seco
* Las acciones de salto no están habilitadas en la ejecución en seco
* Los datos de informes solo están disponibles mientras la ejecución en seco está activa; una vez detenida, los datos ya no están accesibles
* Los recorridos de ejecución en seco no afectan a las reglas empresariales

**Terminología:**
* Nombre canónico: Recorrido Dry run — Acrónimo: none — variantes: dry run mode, Dry run publication mode
* Sinónimos: &quot;Dry run&quot; = &quot;prueba de humo&quot; (informalmente)
* No confundir: &quot;Ejecución en seco&quot; ≠ &quot;Modo de prueba&quot;: la ejecución en seco utiliza datos de producción reales y cuenta para las cuotas; el modo de prueba utiliza perfiles de prueba sintéticos y no

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿La ejecución en seco realmente envía correos electrónicos o notificaciones push a los clientes?** — No; todos los nodos de acción de canal y las acciones personalizadas se desactivan y no se ejecutan durante una ejecución en seco.
* **Q: ¿Cuánto tiempo dura una ejecución en seco antes de que se detenga automáticamente?** — 14 días, después de los cuales el recorrido vuelve automáticamente al estado Borrador.
* **Q: ¿Cómo excluyo los datos de ejecución en seco de mis consultas de análisis de recorrido?** — Filtrar eventos de paso donde `inDryRun` es `true`; incluir solo eventos donde `inDryRun` es `null` o `false`.
* **Q: ¿Se cuentan los perfiles con respecto a algún límite durante una ejecución en seco?** — Sí; los perfiles se contabilizan en Perfiles atractivos y el recorrido de Ejecución en seco se contabiliza en la cuota de recorrido activo.
* **Q: ¿Puedo habilitar las actividades de espera y las llamadas a fuentes de datos externas durante una ejecución en seco?** — Ambos están desactivados de forma predeterminada, pero puede elegir activarlos o desactivarlos al activar la ejecución en seco.

+++
