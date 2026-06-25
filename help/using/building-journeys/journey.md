---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los recorridos
description: 'Introducción a los recorridos: obtenga información acerca de los tipos de recorrido, el flujo de trabajo, las funcionalidades y las prácticas recomendadas para crear experiencias personalizadas con los clientes en  [!DNL Adobe Journey Optimizer]'
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: recorrido, detección, inicio, unitario, leer público, calificación de público, evento empresarial, tiempo real, programado, por lotes, activado por evento, flujo de trabajo, orquestación, personalización, multicanal
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/FsZLMlzVj6CcTqVp9BPUmiCf2piZL8zaj2WfWv8FMSQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 6f35d9b951850220382e3662502b9e1d7ad6b990
workflow-type: tm+mt
source-wordcount: 2278
ht-degree: 70%

---

# Introducción a los recorridos {#jo-general-principle}

>[!BEGINSHADEBOX]

**En esta página:** Conozca los aspectos básicos de los recorridos en Adobe Journey Optimizer, incluidos los tipos de recorridos, el flujo de trabajo de diseño, las funciones clave y las prácticas recomendadas para crear experiencias personalizadas para los clientes.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_canvas"
>title="Crear un recorrido"
>abstract="El lienzo de tipo arrastrar y soltar orquesta mensajes y acciones en varios canales al aprovechar los datos contextuales y la segmentación del público para lograr el máximo impacto."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/orchestrate-journeys/create-journey/journey-gs" text="Creación de su primer recorrido"


[!DNL Adobe Journey Optimizer] le permite crear recorridos para el cliente personalizados que constan de varios pasos y que se adaptan en tiempo real al comportamiento y las necesidades de su público. Con un lienzo intuitivo de tipo arrastrar y soltar, puede orquestar mensajes y acciones en varios canales, aprovechando los datos contextuales y la segmentación del público para lograr el máximo impacto.

Esta guía proporciona una hoja de ruta clara para ayudarle a comprender los aspectos básicos del recorrido, elegir el tipo de recorrido adecuado para su caso de uso y diseñar recorridos con confianza que proporcionen experiencias del cliente significativas y oportunas.

## ¿Qué son los recorridos?

Los **recorridos** son experiencias de cliente automatizadas y de varios pasos que organizan interacciones personalizadas entre canales en respuesta a la conducta del cliente, eventos empresariales o campañas programadas.

Use [!DNL Journey Optimizer] para:

* Crear casos de uso de **orquestación en tiempo real** aprovechando los datos contextuales almacenados en eventos o fuentes de datos
* Diseñar **casos avanzados de varios pasos** que respondan dinámicamente al comportamiento de los clientes y a los eventos empresariales
* Ofrecer **1:1 experiencias personalizadas** a escala en correo electrónico, push, SMS, en la aplicación, web y más

![Interfaz del diseñador de recorrido con panel de paleta, lienzo y propiedades](assets/journey38.png)

➡️ **¿Todo listo para comenzar a crear?** [Cree su primer recorrido](journey-gs.md) en 5 minutos.

### Recorridos vs. Campañas: cuándo usar cada uno {#journeys-vs-campaigns-intro}

[!DNL Adobe Journey Optimizer] ofrece tres métodos para llegar a los clientes: **Recorridos** (1:1 orquestación en tiempo real), **Campañas** (envío simple por lotes o desencadenado por API) y **Campañas orquestadas** (flujos de trabajo por lotes de lienzo con datos de varias entidades).

**Decisión rápida:**

* Use **Recorridos** para experiencias de varios pasos impulsadas por el comportamiento en las que cada cliente progresa a su propio ritmo
* Use **Campañas de acción/desencadenado por API** para enviar mensajes simples, programados o desencadenados a los públicos
* Use **Campañas orquestadas** para flujos de trabajo por lotes complejos que requieren segmentación de varias entidades y recuentos exactos previos al envío

<!--
 waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability
-->

## Elija su tipo de recorrido {#journey-types}

[!DNL Adobe Journey Optimizer] admite cuatro tipos de recorridos, cada uno diseñado para diferentes mecanismos de entrada y casos empresariales:

* **recorridos unitarios**: experiencias activadas por eventos en tiempo real (recuperación del abandono del carro de compras, correos electrónicos de bienvenida)
* **Leer recorridos de públicos**: Comunicaciones por lotes programadas para segmentos de público (boletines informativos, campañas promocionales)
* **Recorridos de calificación de públicos**: respuestas en tiempo real a cambios de pertenencia a públicos (actualizaciones de VIP, renovación de participación)
* **Recorridos de eventos empresariales**: condiciones empresariales que afectan a varios clientes (alertas de inventario, ventas flash)

<!--
 waiting for DOCAC-13912 
➡️ **[Journey types: choose the right one](journey-types-selection.md)** - Detailed comparison, decision guide, and feature compatibility matrix 
-->

## Crear con el diseñador de recorridos {#journey-designer}

El **[diseñador de recorridos](using-the-journey-designer.md)** es el lienzo visual para crear experiencias de cliente. Con una interfaz intuitiva de arrastrar y soltar, puede organizar cada paso del recorrido sin necesidad de escribir código.

![Interfaz del diseñador de recorrido con panel de paleta, lienzo y propiedades](assets/journey38.png)

### Lo que puede hacer en el diseñador:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=es)

**Definir puntos de entrada**

Elegir cómo entran los clientes: a través de un evento, segmento de público o calificación de público.

[Conozca la gestión de entrada](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=es)

**Envío de mensajes**

Utilice acciones de canal integradas para correo electrónico, notificaciones push, SMS/RCS/MMS, en la aplicación, la web y mucho más, todas ellas diseñadas en Journey Optimizer.

[Envío de mensajes en recorridos](journey-action.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=es)

**Añadir lógica y condiciones**

Ramifique su recorrido en función de atributos de perfil, pertenencia a públicos o eventos en tiempo real.

[Condiciones de uso](conditions.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=es)

**Aprovechamiento de datos**

Utilice datos contextuales de eventos, [!DNL Adobe Experience Platform] o servicios API de terceros.

[Trabajo con paquetes de datos](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=es)

**Conectar sistemas externos**

Cree acciones personalizadas para integrar sistemas de terceros para enviar mensajes o activar flujos de trabajo.

[Configurar acciones personalizadas](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=es)

**Añada actividades de orquestación**

Utilice tiempos de espera, saltos, actualizaciones de perfiles y gestión de público para crear flujos sofisticados.

[Explorar todas las actividades](about-journey-activities.md)
:::

::::

➡️ **Aprendizaje práctico:** [Vea el vídeo del diseñador de recorridos](#video) o [explore casos de uso de extremo a extremo](jo-use-cases.md)

## Su flujo de trabajo de creación de recorridos {#workflow}

La creación de recorridos exitosos sigue un proceso claro y repetible. Este es su flujo de trabajo paso a paso:

**1. Planificación** → **2. Diseño** → **3. Prueba** → **4. Publicación** → **5. Supervisión** → **6. Optimización**

### &#x200B;1. Planifique su recorrido {#plan}

Antes de abrir el diseñador, tenga claros sus objetivos:

* **¿Cuál es el objetivo** (por ejemplo, incorporar nuevos clientes, volver a atraer usuarios inactivos)
* **¿Quién es el público?** (segmento específico, individuos impulsados por evento)
* **¿Qué tipo de recorrido encaja?** (Ver [tipos de recorrido](#journey-types) más arriba)
* **¿Qué canales usará?** (correo electrónico, push, SMS, etc.)

### &#x200B;2. Diseñe en el lienzo {#design}

Utilice el diseñador de recorridos para crear el flujo:

* **Establezca condiciones de entrada**: defina cómo entran los perfiles (evento, público, calificación)
* **Añada una lógica de orquestación**: incluya tiempos de espera, condiciones y puntos de decisión
* **Configure mensajes**: diseñe sus comunicaciones o utilice las plantillas existentes
* **Configure acciones**: configure acciones integradas o personalizadas para ejecutar
* **Defina criterios de salida**: especifique cuándo y cómo completan el recorrido los perfiles

[Aprenda a utilizar el diseñador de recorrido →](using-the-journey-designer.md)

### &#x200B;3. Pruebe antes de activarlos {#test}

Pruebe siempre el recorrido para detectar problemas antes de que los clientes lo experimenten:

* Use **modo de prueba** para simular el recorrido con perfiles de prueba
* Utilice la **ejecución en seco** para obtener una vista previa de la ejecución del recorrido sin afectar a los datos reales ni enviar mensajes
* Compruebe que todas las condiciones, mensajes y acciones funcionan según lo esperado
* Compruebe la sincronización, los flujos de datos y la personalización

[Pruebe su recorrido →](testing-the-journey.md) | [Más información sobre el ensayo de recorrido →](journey-dry-run.md)

### &#x200B;4. Publique el recorrido {#publish}

Una vez finalizada la prueba, publique para que el recorrido esté activo:

* Revisar la configuración y las propiedades finales
* Publique para activarlo para clientes reales
* Nota: Los recorridos activos se pueden detener, pero no editar (debe crear una nueva versión)

[Publique su recorrido →](publish-journey.md)

### &#x200B;5. Supervise el rendimiento {#monitor}

Realice un seguimiento del rendimiento de su recorrido en el mundo real:

* Vea informes y análisis del recorrido
* Monitorice las tasas de entrada, finalización y error
* Configure alertas para problemas críticos

[Supervise e informe →](report-journey.md) | [Configure alertas →](../reports/alerts.md)

### &#x200B;6. Optimice e itere {#optimize}

Use perspectivas para mejorar:

* Analice métricas de participación y tasas de conversión
* Pruebe la optimización del tiempo de envío
* Cree nuevas versiones de recorrido con mejoras
* Use recomendaciones con tecnología de IA

[Optimice los recorridos →](optimize.md) | [→ Optimización del tiempo de envío](send-time-optimization.md)

➡️ **¿Todo listo para comenzar?** [Cree su primer recorrido ahora →](journey-gs.md)

## Casos de uso reales {#use-cases}

Aprenda con ejemplos prácticos que muestran cómo aplicar conceptos de recorrido para solucionar retos de marketing comunes:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=es)

**Dé la bienvenida a nuevos suscriptores**

Cuando un cliente se suscriba a su servicio, active un recorrido de bienvenida que le anime a completar los pasos de incorporación.

[Ver caso de uso →](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=es)

**Optimización del tiempo de envío**

Utilice la IA para enviar correos electrónicos cuando sea más probable que cada cliente interactúe, lo que maximiza las tasas de apertura y de clics.

[Ver caso de uso →](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=es)

**Aumento de envíos**

Aumente gradualmente el volumen del mensaje para aumentar la reputación de su envío y evitar problemas de entregabilidad.

[Ver caso de uso →](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=es)

**Segmente por día laborable**

Envíe contenido diferente en función del día de la semana en el que los clientes entren en su recorrido para mejorar la relevancia.

[Ver caso de uso →](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=es)

**Campañas multicanal**

Orqueste experiencias optimizadas en canales de correo electrónico, push, SMS y web en un solo recorrido.

[Ver caso de uso →](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=es)

**Todos los casos de uso**

Explore la biblioteca completa de casos de uso de recorrido con implementaciones paso a paso.

[Ver todo →](jo-use-cases.md) | [Biblioteca de casos de uso →](../../rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Explorar las funciones del recorrido {#capabilities}

A medida que se vaya familiarizando con la creación de recorridos, explore estas potentes funciones para crear experiencias de cliente sofisticadas:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=es)

**Expresiones avanzadas**

Cree condiciones dinámicas y personalización mediante el editor de expresiones para la manipulación de datos y la lógica compleja.

[Más información sobre expresiones](../../rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=es)

**Administración de husos horarios**

Gestione públicos globales con ajustes automáticos de zona horaria y tiempos de envío óptimos.

[Administrar zonas horarias](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=es)

**Modo de prueba y ensayo**

Valide los recorridos con perfiles de prueba antes de activarlos y previsualice la ejecución sin afectar a los datos reales.

[Utilice el ensayo](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=es)

**Copie a la zona protegida**

Duplique los recorridos en las zonas protegidas para optimizar los flujos de trabajo de prueba e implementación.

[Copie los recorridos](../configuration/copy-objects-to-sandbox.md#objects)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=es)

**Etiquetas y organización**

Utilice etiquetas para categorizar y filtrar recorridos para una mejor administración a escala.

[Organización con etiquetas](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=es)

**Control de rendimiento**

Limite el rendimiento del mensaje para administrar la reputación de envío y evitar sistemas abrumadores.

[Control del rendimiento](limit-throughput.md)
:::

::::

[Vea todas las funcionalidades de recorrido →](../../rp_landing_pages/manage-journey-landing-page.md)

## Aprenda mirando {#video}

Obtenga una introducción visual a los componentes del recorrido y aprenda los conceptos básicos de la creación de recorridos en el lienzo:

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

➡️ **¿Quiere más vídeos?** [Explorar tutoriales de vídeo de recorrido](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## Preguntas frecuentes {#common-questions}

+++ ¿Cuál es la diferencia entre un recorrido y una campaña?

[!DNL Adobe Journey Optimizer] ofrece tres enfoques:

* **Recorridos**: 1:1 orquestación en tiempo real en la que cada perfil recorre los pasos a su propio ritmo. Ideal para experiencias de varios pasos y basadas en el comportamiento con lógica condicional (por ejemplo, incorporación, abandono del carro de compras).

* **Campañas (activadas por acción y API)**: envío de mensaje simple a los públicos, que se ejecuta simultáneamente en todos los perfiles según lo programado o mediante el activador de API. Ideal para campañas promocionales, boletines informativos y mensajes transaccionales.

* **Campañas orquestadas**: flujos de trabajo por lotes de varios pasos con segmentación compleja que utiliza datos relacionales (perfiles + productos/tiendas/reservas). Todos los perfiles procesados junto con los recuentos exactos de preenvío. Ideal para promociones de temporada, lanzamientos de productos y campañas que requieren datos de varias entidades.

**Diferencia clave**: los recorridos mantienen el estado de cliente individual para acciones en tiempo real; las campañas de acción/desencadenadas por API entregan mensajes simples en lote; las campañas orquestadas proporcionan lienzo de flujo de trabajo en lote con capacidades de segmentación de varias entidades.

<!-- waiting for DOCAC-13912 - [See detailed comparison](#journeys-vs-campaigns) -->
[Más información sobre las campañas orquestadas](../orchestrated/gs-orchestrated-campaigns.md)

+++

<!--
 Waiting for DOCAC-13912
+++ Which journey type should I use?

Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.

+++
-->

+++ ¿Puedo editar un recorrido en directo?

Puede editar elementos limitados (nombre, contenido del mensaje), pero los cambios estructurales requieren la creación de una nueva versión. [Más información sobre las versiones de un recorrido](publish-journey.md#journey-versions)

+++

➡️ **¿Más preguntas?** [Vea la lista completa de preguntas frecuentes sobre el recorrido](journey-faq.md) con más de 40 respuestas detalladas

## ¿Necesita ayuda? {#help}

Utilice estos vínculos para encontrar instrucciones, soluciones de problemas y recursos.

### Vínculos rápidos para tareas comunes

* **[Cree su primer recorrido](journey-gs.md)**: guía paso a paso para principiantes
* **[Preguntas frecuentes sobre el recorrido](journey-faq.md)**: preguntas comunes respondidas
* **[Solución de problemas](../../rp_landing_pages/troubleshoot-journey-landing-page.md)**: diagnóstico y corrección de problemas
* **[Referencia de códigos de error](error-codes-reference.md)**: explicación de los mensajes de error
* **[Protecciones y limitaciones](../start/guardrails.md)**: límites técnicos y prácticas recomendadas

### Recibir notificaciones sobre problemas

Configure **[alertas de recorridos](../reports/alerts.md)** para recibir notificaciones en tiempo real cuando los recorridos encuentren errores o patrones inusuales.

### Recursos adicionales

* **[Hub de administración de Recorrido](../../rp_landing_pages/manage-journey-landing-page.md)**: herramientas para filtrado, optimización y administración de perfiles
* **[Referencia de actividades de recorrido](../../rp_landing_pages/about-journey-building-landing-page.md)**: guía completa para todos los tipos de actividades
* **[Solucionar problemas de ejecución](troubleshooting-execution.md)**: problemas de ejecución del recorrido de depuración
* **[Solución de problemas de actividades entrantes](troubleshooting-inbound.md)**: corrija problemas de entrada y calificación

**¿Todo listo para crear su primer recorrido?** [Empiece ahora →](journey-gs.md)

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página es el concentrador de introducción para Adobe Journey Optimizer recorrido, donde se explica cuáles son los recorridos, los cuatro tipos de recorridos, el flujo de trabajo de creación de seis pasos, los casos de uso reales y los vínculos a funciones avanzadas.

**Intenciones:**

* Comprenda cuáles son los recorridos y en qué se diferencian de las campañas y las campañas orquestadas
* Elija el tipo de recorrido adecuado (Unitario, Leer audiencia, Calificación de audiencia o Evento empresarial) para un caso de uso
* Siga el flujo de trabajo de creación de recorridos de seis pasos: Planificar, Diseñar, Probar, Publicar, Supervisar, Optimizar
* Utilice Simulación, Modo de prueba o Ejecución en seco para validar un recorrido antes de activarlo
* Publicar un recorrido y supervisar el rendimiento mediante informes y alertas
* Explore funciones avanzadas como expresiones, administración de huso horario, copia a zona protegida y control de rendimiento

**Glosario:**

* **Recorrido**: una experiencia de cliente automatizada y de varios pasos que organiza interacciones personalizadas entre canales en respuesta a la conducta de los clientes, eventos empresariales o campañas programadas. *(específico del producto)*
* **Diseñador de Recorridos**: el lienzo visual de arrastrar y soltar de AJO que se usa para generar y configurar flujos de recorridos sin escribir código. *(específico del producto)*
* **Modo de prueba**: Un modo de validación de recorrido que usa perfiles de prueba Adobe Experience Platform persistentes (marcados explícitamente como perfiles de prueba) para recorrer un recorrido de borrador antes de publicarlo. *(específico del producto)*
* **Ejecución en seco**: Modo de publicación especial que ejecuta el recorrido con datos de producción reales sin enviar comunicaciones ni actualizar perfiles. *(específico del producto)*
* **Simulación**: Modo de validación que utiliza usuarios simulados temporales generados sobre la marcha; los usuarios simulados no persisten en Adobe Experience Platform. *(específico del producto)*
* **Campañas orquestadas**: flujos de trabajo por lotes de varios pasos en AJO que utilizan datos relacionales (perfiles + productos/tiendas/reservas) y procesan todos los perfiles con recuentos exactos de preenvío. *(específico del producto)*

**Protecciones:**

* Los recorridos activos no se pueden editar estructuralmente; los cambios requieren la creación de una nueva versión
* El modo de prueba y la ejecución en seco deben usarse antes de publicar para detectar problemas

**Terminología:**

* Nombre canónico: Recorrido — Acrónimo: none — variantes: recorrido del cliente, recorrido de AJO
* Sinónimos: &quot;diseñador de recorridos&quot; = &quot;lienzo&quot; = &quot;lienzo de recorrido&quot;
* No confunda: &quot;Recorrido&quot; ≠ &quot;Campaña&quot;: los Recorridos mantienen el estado de cliente individual para experiencias en tiempo real impulsadas por comportamientos de varios pasos; las campañas envían mensajes en lote a las audiencias según una programación o mediante el déclencheur de API
* No confunda: &quot;Simulación&quot; ≠ &quot;Modo de prueba&quot; ≠ &quot;Ejecución en seco&quot;: la simulación utiliza usuarios simulados temporales; el modo de prueba utiliza perfiles de prueba AEP persistentes en un recorrido de borrador; la ejecución en seco se ejecuta con datos de producción reales sin ponerse en contacto con los clientes ni actualizar perfiles

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Cuál es la diferencia entre un recorrido y una campaña en Journey Optimizer?** — Los Recorridos proporcionan una orquestación en tiempo real de 1:1 en la que cada perfil progresa a su propio ritmo mediante lógica condicional; las campañas envían mensajes simultáneamente a una audiencia en una programación o mediante un déclencheur de API; las campañas orquestadas son flujos de trabajo de lienzo por lotes para una segmentación compleja de varias entidades.
* **Q: ¿Puedo editar un recorrido activo?** — Se pueden editar elementos limitados como el nombre y el contenido del mensaje; los cambios estructurales requieren la creación de una nueva versión del recorrido.
* **Q: ¿Cuáles son los pasos para generar un recorrido?** — El flujo de trabajo de seis pasos es: Planificar, Diseño en el lienzo, Prueba (modo de prueba o ejecución en seco), Publicar, Monitorizar rendimiento y Optimizar/iterar.
* **Q: ¿Cómo valido un recorrido sin enviar mensajes reales?** : utilice Simulation (usuarios simulados temporales), Test mode (perfiles de prueba AEP persistentes) o Dry run (datos de producción reales sin contacto de cliente ni actualizaciones de perfil). Los perfiles de ejecución en seco se contabilizan en Perfiles atractivos y cuota de recorrido en directo.
* **Q: ¿Qué tipo de recorrido debo usar para un correo electrónico de bienvenida activado por una suscripción?** — Utilizar un recorrido unitario, activado por un evento individual específico, como la suscripción.

+++
