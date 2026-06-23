---
solution: Journey Optimizer
product: journey optimizer
title: Creación de su primer recorrido
description: Pasos clave para generar su primer recorrido con  [!DNL Adobe Journey Optimizer]
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, primero, inicio, inicio rápido, audiencia, evento, acción
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/7zNDOi2SUTyttgR6I1iOYQb61ejxpqLYznweU8alnPw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5520579-b31f-4df7-9281-f0d9f91e2edcid: c1579802-ddd4-4214-8a91-97b2066abe11id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 0bbbbf94550d4cb762ecca300932620c8d3da50e
workflow-type: tm+mt
source-wordcount: 2143
ht-degree: 8%

---

# Creación de su primer recorrido {#jo-quick-start}

>[!BEGINSHADEBOX]

**En esta página:** Conozca los pasos clave para crear su primer recorrido en Adobe Journey Optimizer, desde definir la audiencia o el evento de entrada hasta agregar acciones y publicarlo en vivo.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Creación de recorridos"
>abstract="**[!DNL Adobe Journey Optimizer]** crea casos de uso de orquestación en tiempo real aprovechando los datos contextuales almacenados en eventos o fuentes de datos."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Recorridos"
>abstract="Los recorridos del cliente ofrecen experiencias personalizadas y contextuales. Journey Optimizer permite crear casos prácticos de orquestación en tiempo real con información contextual almacenada en eventos o fuentes de datos. La pestaña **Información general** muestra un panel de control con métricas clave relacionadas con los recorridos. La pestaña **Examinar** muestra la lista de recorridos existentes."

[!DNL Adobe Journey Optimizer] incluye un lienzo de orquestación omnicanal que permite a los especialistas en marketing armonizar el alcance de marketing con la participación individual del cliente. La interfaz de usuario de le permite arrastrar y soltar fácilmente actividades de la paleta en el lienzo para crear su recorrido. La interfaz de usuario de recorrido se detalla en [esta página](journey-ui.md).

![muestra de lienzo de recorrido](assets/journey38.png)

Los pasos principales para crear un recorrido se detallan en esta página. Se racionalizan de la siguiente manera:

![Pasos de creación de recorrido: crear, diseñar, probar y publicar](assets/journey-creation-process.png)

En esta guía debe hacer lo siguiente:

* Definir un punto de entrada de recorrido: un segmento de audiencia o un evento en tiempo real
* Añada acciones de mensaje en todos los canales: correo electrónico, push, SMS, en la aplicación, web, experiencia basada en código, tarjeta de contenido y mucho más. [Ver canales admitidos](journey-action.md)
* Pruebe el recorrido con perfiles de prueba antes de la activación
* Publique el recorrido y monitorice su rendimiento

Cree recorridos de cliente de varios pasos para iniciar una secuencia de interacciones, ofertas y mensajes en varios canales en tiempo real. Este enfoque garantiza que los clientes se involucren en los momentos óptimos en función de sus acciones y señales comerciales relevantes.

<!--
>[!TIP]
>
>Not sure whether to use a journey or a campaign? [Learn how to choose the right approach](../start/journeys-vs-campaigns.md).
-->

## Antes de comenzar {#prerequisites}

Lo que debe configurar antes de crear depende de cómo se active el recorrido. La mayoría de los recorridos comienzan desde uno de estos dos puntos de entrada:

* **Entrada basada en audiencias**: el recorrido se ejecuta para un conjunto definido de perfiles a una hora programada. [Cree una audiencia](../audience/about-audiences.md) en Adobe Experience Platform antes de generar su recorrido. Este es el punto de partida recomendado si es su primera vez en Journey Optimizer.

* **Entrada basada en eventos**: el recorrido se activa en tiempo real cuando un individuo realiza una acción, como una compra o un registro. [Configura un evento](../event/about-events.md) para definir el déclencheur y los datos que lleva.

**¿No está seguro de qué punto de entrada usar?** La siguiente tabla asigna los casos de uso más comunes a la actividad de inicio correcta.

| Punto de entrada | Usar cuando... | Introducir perfiles |
|---|---|---|
| **[Leer audiencia](read-audience.md)** | Desea enviar un mensaje programado o recurrente a un conjunto definido de perfiles (boletines informativos, promociones, series de incorporación). | Todos los perfiles de una audiencia por lotes, a la vez o según una programación. |
| **[Calificación de audiencias](audience-qualification-events.md)** | Debe reaccionar en tiempo real cuando un perfil entra o sale de una audiencia (actualización del nivel de fidelidad, indicador de riesgo de pérdida). | Un perfil a la vez, en cuanto se clasifique en una audiencia de streaming. |
| **Evento unitario** | Una acción de perfil genera un déclencheur de respuesta inmediata (confirmación de compra, envío de formulario, inicio de sesión en la aplicación). | Perfil a perfil, en tiempo real. |
| **[Evento empresarial](../event/about-creating-business.md)** | Un evento que no es de perfil afecta a varias personas a la vez (cancelación de vuelos, reabastecimiento de existencias, alerta de noticias de última hora). | Todos los perfiles asociados con el evento, a través de un paso automático Leer audiencia. |

Los siguientes elementos son opcionales, pero pueden ser necesarios según el caso de uso:

* **Fuente de datos**: para enriquecer las condiciones del recorrido o la personalización con datos de un sistema externo, configure una [fuente de datos](../datasource/about-data-sources.md).

* **Acción personalizada**: si envía mensajes a través de un sistema de terceros en lugar de los canales integrados, configure una [acción personalizada](../action/action.md).

>[!NOTE]
>
>* Si usted es un ingeniero de datos responsable de la configuración técnica (eventos, fuentes de datos y acciones), consulte [esta sección](../configuration/about-data-sources-events-actions.md).
>
>* Las limitaciones y protecciones de recorrido se detallan en [esta página](../start/guardrails.md).

## Crear un recorrido {#jo-build}

Para crear un recorrido de varios pasos, siga estos pasos:

1. En la sección de menú ADMINISTRACIÓN DE RECORRIDO, haga clic en **[!UICONTROL Recorridos]**.

1. Haga clic en el botón **[!UICONTROL Crear Recorrido]** para crear un recorrido nuevo.

1. Edite el panel de configuración del recorrido para definir el nombre del recorrido y sus propiedades. Aprenda a establecer las propiedades de su recorrido en [esta página](journey-properties.md).

   >[!TIP]
   >
   >**¿Qué tipo de recorrido debo elegir?** Si es nuevo en Journey Optimizer, empiece con un recorrido basado en audiencias usando una actividad de **[!UICONTROL Leer audiencia]**; no requiere ninguna configuración de evento anterior y es la manera más sencilla de familiarizarse con el lienzo. Para experiencias en tiempo real activadas por eventos (por ejemplo, reaccionar ante una compra o un envío de formulario), configure primero un evento y utilice una entrada basada en eventos. ¿Listo para profundizar? [Descubra todos los tipos de recorrido y sus reglas de entrada](entry-management.md#types-of-journeys).

   ![Panel de propiedades del Recorrido con opciones de configuración y configuración](assets/jo-properties.png)

A continuación, puede empezar a diseñar el recorrido.

## Diseño del recorrido {#jo-design}

El diseñador de recorridos le permite crear recorridos de varios pasos con una interfaz intuitiva de arrastrar y soltar. Las actividades de la paleta izquierda están organizadas en tres categorías: **Eventos**, **Orquestación** y **Acciones**. Para obtener una descripción general completa del lienzo y sus controles, consulte [esta página](using-the-journey-designer.md).

![Interfaz de diseñador de Recorrido con paleta y lienzo de actividades](assets/journey38.png)

Siga estos pasos para diseñar el recorrido:

1. **Agregar un punto de entrada** — Arrastre un evento o una actividad de **[!UICONTROL Leer audiencia]** desde la paleta al lienzo. Define la forma en la que los perfiles entran en el recorrido: individualmente en tiempo real (basado en eventos) o todos a la vez desde una audiencia definida (basado en audiencias).

   ![Leer la configuración de actividades de Audiencia para seleccionar la audiencia objetivo](assets/read-segment.png)

1. **Agregar acciones de mensaje**: en la sección **[!UICONTROL Acciones]** de la paleta, arrastre una acción de canal al lienzo para enviar mensajes a los perfiles que fluyen por el recorrido. Las acciones están disponibles para correo electrónico, notificaciones push, SMS y más.

1. **Agregar actividades de orquestación**: use una actividad **[!UICONTROL Condición]** para bifurcar el recorrido en varias rutas de acceso según el comportamiento o los atributos del perfil. Use una actividad **[!UICONTROL Wait]** para establecer un tiempo de espera entre pasos.

>[!TIP]
>
>Para los recorridos con varias fases o varios puntos de contacto, considere la posibilidad de dividir el flujo de extremo a extremo en subrecorridos más pequeños conectados con la actividad **[!UICONTROL Jump]**. Esto reduce la complejidad y facilita las pruebas independientes de cada recorrido secundario. Más información en [Estrategia de diseño: recorridos secundarios](jump.md#jump-strategy).

## Prueba del recorrido {#jo-test}

Una vez creado el recorrido, pruébelo antes de publicarlo. Journey Optimizer ofrece **Modo de prueba** como una forma de ver los perfiles de prueba a medida que se mueven por el recorrido, detectando posibles errores antes de la activación. La ejecución de pruebas rápidas garantiza que los recorridos funcionen correctamente para que pueda publicarlos con confianza. Aprenda a probar su recorrido [en esta sección](testing-the-journey.md)

También puede ejecutar su recorrido en **Ejecución en seco**. El ensayo del recorrido es un modo especial de publicación de recorrido de Adobe Journey Optimizer que permite a los profesionales de recorridos probar un recorrido utilizando datos de producción reales sin ponerse en contacto con clientes reales ni actualizar la información de perfil. Esta función ayuda a los profesionales de recorridos a confiar en el diseño del recorrido y en la segmentación del público antes de publicarlo en vivo. Obtenga información sobre cómo publicar un recorrido en el modo de ejecución en seco [en esta sección](journey-dry-run.md).

## Publicación del recorrido {#jo-pub}

Debe publicar un recorrido para activarlo y hacer que esté disponible para que los nuevos perfiles lo introduzcan. Antes de publicar el recorrido, compruebe que es válido y que no hay errores. No se puede publicar un recorrido con errores. Obtenga más información acerca de la publicación de recorrido en esta [sección](publish-journey.md).

![Flujo de recorrido completo con audiencia, condiciones y acciones](assets/jo-journeyuc2_32bis.png)

Una vez publicado, puede monitorizar su recorrido mediante las herramientas de sistema de informes específicas para medir la efectividad de su recorrido.

![informe de análisis de Recorrido que muestra métricas y estadísticas de rendimiento](assets/jo-dynamic_report_journey_12.png)

Obtenga más información acerca de los informes de recorrido en esta [sección](../reports/live-report.md).

## Casos de uso comunes {#use-cases}

¿No estás seguro de por dónde empezar? Estos son tres escenarios típicos en los que los recorridos proporcionan el mayor valor:

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
      <a href="https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding" target="_blank">
        <img src="../assets/do-not-localize/icon-quick-start.svg" width="35px">
      </a>
      <div><strong>Serie de bienvenida</strong><br/>Incorpore automáticamente nuevos usuarios con una secuencia de mensajes después de registrarse, guiándolos a través de su producto o servicio.</div>
    </td>
    <td>
      <a href="https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart" target="_blank">
        <img src="../assets/do-not-localize/icon-campaign.svg" width="35px">
      </a>
      <div><strong>Abandono del carro de compras</strong><br/>Vuelva a atraer a los clientes que se fueron sin completar una compra y envíenos un recordatorio oportuno con contenido personalizado.</div>
    </td>
    <td>
      <a href="jo-use-cases.md">
        <img src="../assets/do-not-localize/icon-content.svg" width="35px">
      </a>
      <div><strong>Reparticipación</strong><br/>Recupere usuarios inactivos con ofertas o actualizaciones segmentadas basadas en su último comportamiento conocido.</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding" target="_blank"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart" target="_blank"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="jo-use-cases.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
  </tr>
</table>

## Recursos adicionales

* **[tipos de Recorrido y entrada de perfil](entry-management.md)**: comprenda todos los tipos de recorrido (evento unitario, evento empresarial, audiencia de lectura, calificación de audiencia) y cómo los perfiles entran, vuelven a entrar y fluyen por los recorridos.
* **[Descripción general del diseñador de Recorridos](using-the-journey-designer.md)**: domine la interfaz de lienzo de recorrido para diseñar y organizar los recorridos de los clientes.
* **[actividades de Recorrido](about-journey-activities.md)**: descubra todas las actividades disponibles, incluidos eventos, acciones y componentes de orquestación.
* **[recorridos de prueba](testing-the-journey.md)**: aprenda a probar las recorridos mediante el modo de prueba antes de publicarlas en producción.
* **[recorridos de publicación](publish-journey.md)**: comprenda el proceso de publicación de recorridos y cómo administrar recorridos activos.
* **[Informes de Recorridos](report-journey.md)** - Rastree y analice el rendimiento de los recorridos con métricas y perspectivas detalladas.
* **[recorridos para solucionar problemas](troubleshooting.md)**: encuentre soluciones a problemas comunes de recorridos y prácticas recomendadas para la depuración.
* **[Tutoriales de Recorrido](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"}**: Explore tutoriales de vídeo paso a paso sobre la creación de recorridos y las prácticas recomendadas.

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explican los cuatro pasos clave para crear un primer recorrido en Adobe Journey Optimizer (definir un punto de entrada, diseñar el lienzo, realizar pruebas con el modo de prueba o Ejecución en seco y publicar) junto con instrucciones para elegir el tipo de entrada correcto.

**Intenciones:**
* Cree un nuevo recorrido y configure sus propiedades en el menú Administración de Recorrido
* Elija el punto de entrada correcto (lectura de audiencia, calificación de audiencia, evento unitario o evento empresarial) para un caso de uso determinado
* Diseñe un recorrido de varios pasos arrastrando y soltando eventos, actividades de orquestación y acciones de canal en el lienzo
* Pruebe un recorrido mediante Simulación, Modo de prueba con perfiles de prueba de AEP persistentes o Ejecución en seco antes de publicar
* Ejecute una ejecución en seco para validar la segmentación de audiencia con datos de producción reales sin ponerse en contacto con los clientes
* Publique un recorrido para activarlo y supervisar su rendimiento con herramientas de creación de informes

**Glosario:**
* **Leer audiencia**: una actividad de entrada que procesa todos los perfiles de una audiencia por lotes a la vez o según una programación *(específica del producto)*
* **Calificación de audiencias**: una actividad de entrada se desencadenó en tiempo real cuando un perfil entra o sale de una audiencia de flujo continuo *(específica del producto)*
* **Evento unitario**: déclencheur en tiempo real que introduce un perfil cada vez en un recorrido cuando se produce una acción específica *(específico del producto)*
* **Evento empresarial**: un evento sin perfil (por ejemplo, cancelación de vuelo, reabastecimiento de existencias) que déclencheur un recorrido para varios perfiles simultáneamente mediante un paso de lectura automática de audiencia *(específico del producto)*
* **Modo de prueba**: Un modo de validación que usa perfiles de prueba Adobe Experience Platform persistentes (marcados explícitamente como perfiles de prueba) para recorrer un recorrido de borrador antes de la publicación *(específico del producto)*
* **Simulación**: modo de validación que utiliza usuarios simulados temporales generados sobre la marcha; los usuarios simulados no persisten en Adobe Experience Platform *(específico del producto)*
* **Ejecución en seco**: Modo de publicación especial que utiliza datos de producción real para validar la lógica de recorrido sin ponerse en contacto con clientes reales ni actualizar perfiles *(específicos del producto)*

**Protecciones:**
* Un recorrido no se puede publicar si contiene errores; primero se deben resolver todos los errores
* Un ingeniero de datos debe completar la configuración de eventos (para entradas basadas en eventos) antes de poder crear el recorrido
* Las limitaciones y protecciones de recorrido se documentan por separado y deben revisarse antes de diseñarlas a escala
* La creación de audiencias en Adobe Experience Platform es un requisito previo para los recorridos basados en audiencias

**Terminología:**
* Nombre canónico: Recorrido — Acrónimo: none — variantes: recorrido del cliente, flujo de orquestación
* Sinónimos: &quot;Modo de prueba&quot; = &quot;Prueba de recorrido&quot;; &quot;Ejecución en seco&quot; = &quot;Modo de ejecución en seco&quot;
* No confunda: &quot;Simulación&quot; ≠ &quot;Modo de prueba&quot; ≠ &quot;Ejecución en seco&quot;: la simulación utiliza usuarios simulados temporales; el modo de prueba utiliza perfiles de prueba AEP persistentes; la ejecución en seco utiliza datos de producción reales sin ponerse en contacto con los clientes ni actualizar perfiles

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Qué es lo primero que necesito hacer antes de crear un recorrido activado por evento?** — Configure el evento con un ingeniero de datos para definir el déclencheur y los datos que lleva; a continuación, haga referencia al evento como punto de entrada de recorrido.
* **Q: ¿Qué punto de entrada se recomienda para alguien nuevo en Journey Optimizer?** — Comience con un recorrido basado en audiencias usando una actividad Leer audiencia — no requiere ninguna configuración de evento previa y es la manera más sencilla de familiarizarse con el lienzo.
* **Q: ¿Puedo probar mi recorrido antes de que se active?** — Sí; utilice Simulación con usuarios simulados temporales, Modo de prueba con perfiles de prueba AEP persistentes o Ejecución en seco para ejecutar datos de producción reales sin enviar comunicaciones.
* **Q: ¿Qué sucede si mi recorrido tiene errores cuando intento publicar?** — No se puede publicar un recorrido con errores; todos los errores de configuración deben resolverse antes de la publicación.
* **Q: ¿Cómo se puede dividir un recorrido complejo con muchos pasos?** — Utilice la actividad de salto para conectar subrecorridos más pequeños, reduciendo la complejidad y facilitando las pruebas independientes de cada recorrido.

+++
