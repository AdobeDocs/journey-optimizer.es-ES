---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los recorridos
description: 'Introducción a recorrido: Obtenga información acerca de los tipos de recorrido, el flujo de trabajo, las funcionalidades y las prácticas recomendadas para crear experiencias personalizadas con los clientes en Adobe Journey Optimizer'
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: recorrido, detección, inicio, unitario, leer audiencia, calificación de audiencia, evento empresarial, tiempo real, programado, por lotes, activado por evento, flujo de trabajo, orquestación, personalización, multicanal
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 522dba0516268a17e72f56c0f28205ba60709d78
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 3%

---


# Introducción a los recorridos{#jo-general-principle}

Adobe Journey Optimizer le permite crear recorridos de cliente personalizados y de varios pasos que se adaptan en tiempo real al comportamiento y las necesidades de su audiencia. Con un lienzo intuitivo de arrastrar y soltar, puede orquestar mensajes y acciones en varios canales, aprovechando los datos contextuales y la segmentación de audiencia para lograr el máximo impacto.

Esta guía proporciona una hoja de ruta clara para ayudarle a comprender los aspectos básicos del recorrido, elegir el tipo de recorrido adecuado para su caso de uso y diseñar recorridos con confianza que proporcionen experiencias del cliente significativas y oportunas.

## ¿Qué son los recorridos?

Los **Recorridos** son experiencias de cliente automatizadas y de varios pasos que organizan interacciones personalizadas entre canales en respuesta a la conducta del cliente, eventos comerciales o campañas programadas.

Use [!DNL Journey Optimizer] para:

* Cree **casos de uso de orquestación en tiempo real** usando datos contextuales almacenados en eventos o fuentes de datos
* Diseñe **escenarios avanzados de varios pasos** que respondan dinámicamente al comportamiento de los clientes y a los eventos empresariales
* Entregar **1:1 experiencias personalizadas** a escala en correo electrónico, push, SMS, en la aplicación, web y más

![Interfaz del diseñador de Recorrido con panel de paleta, lienzo y propiedades](assets/journey38.png)

➡️ **¿Listo para empezar a crear?** [Crea tu primer recorrido](journey-gs.md) en 5 minutos.

### Recorridos vs. Campañas: Cuándo usar cada uno {#journeys-vs-campaigns-intro}

Adobe Journey Optimizer ofrece tres métodos para llegar a los clientes: **Recorrido** (1:1 orquestación en tiempo real), **Campañas** (entrega simple por lotes o desencadenada por API) y **Campañas orquestadas** (flujos de trabajo por lotes de lienzo con datos de varias entidades).

**Decisión rápida:**

* Use **Recorridos** para experiencias de varios pasos impulsadas por el comportamiento en las que cada cliente progresa a su propio ritmo
* Use **Campañas de acción/API** para enviar mensajes simples, programados o activados a las audiencias
* Use **Campañas orquestadas** para flujos de trabajo por lotes complejos que requieren segmentación de varias entidades y recuentos exactos de preenvío

<!-- waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability-->

## Elija su tipo de recorrido {#journey-types}

Adobe Journey Optimizer admite cuatro tipos de recorridos, cada uno diseñado para diferentes mecanismos de entrada y escenarios empresariales:

* **recorridos unitarios**: experiencias activadas por eventos en tiempo real (confirmaciones de pedidos, correos electrónicos de bienvenida)
* **Leer recorridos de audiencias**: Comunicaciones por lotes programadas para segmentos de audiencia (boletines informativos, campañas promocionales)
* **recorridos de calificación de audiencias**: respuestas en tiempo real a cambios de pertenencia a audiencias (actualizaciones de VIP, renovación de participación)
* **recorridos de eventos empresariales**: condiciones empresariales que afectan a varios clientes (alertas de inventario, ventas flash)

<!-- waiting for DOCAC-13912 
➡️ **[Journey types and selection guide](journey-types-selection.md)** - Detailed comparison, decision tree, and feature compatibility matrix -->

## Compilar con el diseñador de recorrido {#journey-designer}

El **[diseñador de recorridos](using-the-journey-designer.md)** es el lienzo visual para crear experiencias de cliente. Con una intuitiva interfaz de arrastrar y soltar, puede organizar cada paso del recorrido sin necesidad de escribir código.

![Interfaz del diseñador de Recorrido con panel de paleta, lienzo y propiedades](assets/journey38.png)

### Lo que puede hacer en el diseñador:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Definir puntos de entrada**

Elija cómo introducen los clientes: a través de un evento, segmento de audiencia o calificación de audiencia.

[Más información sobre la administración de entradas](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**Envío de mensajes**

Utilice acciones de canal integradas para correo electrónico, push, SMS/MMS, en la aplicación, web y mucho más, todas diseñadas en Journey Optimizer.

[Envío de mensajes en recorridos](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**Agregar lógica y condiciones**

Ramifique su recorrido en función de atributos de perfil, pertenencia a audiencias o eventos en tiempo real.

[Condiciones de uso](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**Aprovechar datos**

Utilice datos contextuales de eventos, Adobe Experience Platform o servicios API de terceros.

[Trabajo con fuentes de datos](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Conectar sistemas externos**

Cree acciones personalizadas para integrar sistemas de terceros para enviar mensajes o activar flujos de trabajo.

[Configurar acciones personalizadas](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Agregar actividades de orquestación**

Utilice tiempos de espera, saltos, actualizaciones de perfiles y gestión de público para crear flujos sofisticados.

[Explorar todas las actividades](about-journey-activities.md)
:::

::::

➡️ **Aprendizaje práctico:** [Vea el vídeo del diseñador de recorridos](#video) o [explore casos de uso de extremo a extremo](jo-use-cases.md)

## Flujo de trabajo de creación de recorridos {#workflow}

La creación de recorridos exitosos sigue un proceso claro y repetible. Este es su flujo de trabajo paso a paso:

**1. Plan** → **2. Diseño** → **3. Prueba** → **4. Publicar** → **5. Monitor** → **6. Optimizar**

### &#x200B;1. Planifique su recorrido {#plan}

Antes de abrir el diseñador, aclare sus objetivos:

* **¿Cuál es el objetivo?** (por ejemplo, incorporar nuevos clientes, volver a atraer usuarios inactivos)
* **¿Quién es la audiencia?** (segmento específico, individuos impulsados por evento)
* **¿Qué tipo de recorrido encaja?** (ver [tipos de recorrido](#journey-types) más arriba)
* **¿Qué canales usará?** (correo electrónico, push, SMS, etc.)

### &#x200B;2. Diseño en el lienzo {#design}

Utilice el diseñador de recorridos para crear el flujo:

* **Establecer condiciones de entrada** - Definir cómo entran los perfiles (evento, audiencia, calificación)
* **Agregar lógica de orquestación**: incluya tiempos de espera, condiciones y puntos de decisión
* **Configurar mensajes**: diseñe sus comunicaciones o aproveche las plantillas existentes
* **Configurar acciones** - Configurar acciones integradas o personalizadas para ejecutar
* **Definir criterios de salida**: especifique cuándo y cómo completan el recorrido los perfiles

[Aprenda a utilizar la → de diseñador de recorrido](using-the-journey-designer.md)

### &#x200B;3. Pruebe antes de empezar {#test}

Pruebe siempre el recorrido para detectar problemas antes de que los clientes los experimenten:

* Usar **modo de prueba** para simular el recorrido con perfiles de prueba
* Utilice **ejecución en seco** para obtener una vista previa de la ejecución del recorrido sin afectar a los datos reales ni enviar mensajes
* Compruebe que todas las condiciones, mensajes y acciones funcionan según lo esperado
* Compruebe el tiempo, los flujos de datos y la personalización

[Prueba tu recorrido →](testing-the-journey.md) | [Más información sobre la ejecución en seco →](journey-dry-run.md)

### &#x200B;4. Publique el recorrido {#publish}

Una vez finalizada la prueba, publique para que el recorrido esté activo:

* Revisar la configuración y las propiedades finales
* Publicación para activarla para clientes reales
* Nota: Los recorridos activos se pueden detener, pero no editar (debe crear una nueva versión)

[Publicación del → de recorrido](publish-journey.md)

### &#x200B;5. Monitorización del rendimiento {#monitor}

Realice un seguimiento del rendimiento de su recorrido en el mundo real:

* Ver informes y análisis de recorrido
* Monitorizar las tasas de entrada, finalización y error
* Configurar alertas para problemas críticos

[Supervisar e informar →](report-journey.md) | [Configurar alertas →](../reports/alerts.md)

### &#x200B;6. Optimizar e iterar {#optimize}

Use perspectivas para mejorar:

* Analizar métricas de participación y tasas de conversión
* Probar la optimización del tiempo de envío
* Creación de nuevas versiones de recorrido con mejoras
* Uso de recomendaciones con tecnología de IA

[Optimizar los recorridos →](optimize.md) | [→ de optimización del tiempo de envío](send-time-optimization.md)

➡️ **¿Listo para comenzar?** [Cree su primer recorrido ahora →](journey-gs.md)

## Casos de uso reales {#use-cases}

Aprenda con ejemplos prácticos que muestran cómo aplicar conceptos de recorrido para solucionar desafíos de marketing comunes:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**Bienvenido/a a nuevos suscriptores**

Cuando un cliente se suscriba a su servicio, déclencheur un recorrido de bienvenida que le anime a completar los pasos de incorporación.

[Ver → de casos de uso](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg)

**Optimización del tiempo de envío**

Utilice la IA para enviar correos electrónicos cuando sea más probable que cada cliente interactúe, lo que maximiza las tasas de apertura y de clics.

[Ver → de casos de uso](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Aumento de envíos**

Aumente gradualmente el volumen del mensaje para aumentar la reputación de su envío y evitar problemas de envío.

[Ver → de casos de uso](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**Segmentar por día laborable**

Envíe contenido diferente en función del día de la semana en el que los clientes escriban su recorrido para mejorar la relevancia.

[Ver → de casos de uso](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Campañas multicanal**

Orqueste experiencias sin problemas en canales de correo electrónico, push, SMS y web en un solo recorrido.

[Ver → de casos de uso](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg)

**Todos los casos de uso**

Explore la biblioteca completa de casos de uso de recorrido con implementaciones paso a paso.

[Examinar todos los →](jo-use-cases.md) | [Biblioteca de casos de uso →](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Explorar las funcionalidades de recorrido {#capabilities}

A medida que se sienta más cómodo con la creación de recorridos, explore estas potentes funciones para crear experiencias de cliente sofisticadas:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Expresiones avanzadas**

Cree condiciones dinámicas y personalización mediante el editor de expresiones para la manipulación de datos y la lógica compleja.

[Más información sobre expresiones](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg)

**Administración de husos horarios**

Gestionar audiencias globales con ajustes automáticos de zona horaria y tiempos de envío óptimos.

[Administrar zonas horarias](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

**Modo de prueba y ejecución en seco**

Valide los recorridos con perfiles de prueba antes de activarlos y previsualice la ejecución sin afectar a los datos reales.

[Utilizar simulacro](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**Copiar a zona protegida**

Duplique los recorridos en los entornos limitados para optimizar los flujos de trabajo de prueba e implementación.

[Copiar recorridos](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg)

**Etiquetas y organización**

Utilice etiquetas para categorizar y filtrar recorridos para una mejor administración a escala.

[Organización con etiquetas](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Control de rendimiento**

Limite el rendimiento del mensaje para administrar la reputación de envío y evitar sistemas abrumadores.

[Control del rendimiento](limit-throughput.md)
:::

::::

[Ver todas las funcionalidades de recorrido →](/help/rp_landing_pages/manage-journey-landing-page.md)

## Aprenda mirando {#video}

Obtenga una introducción visual a los componentes de recorrido y aprenda los conceptos básicos de la creación de recorridos en el lienzo:

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

➡️ **Quiere más vídeos?** [Explorar tutoriales de vídeo de recorrido](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## Preguntas frecuentes {#common-questions}

+++ ¿Cuál es la diferencia entre un recorrido y una campaña?

Adobe Journey Optimizer ofrece tres métodos:

* **Recorridos**: 1:1 orquestación en tiempo real donde cada perfil viaja a través de pasos a su propio ritmo. Ideal para experiencias de varios pasos y basadas en el comportamiento con lógica condicional (por ejemplo, incorporación, abandono del carro de compras).

* **Campañas (activadas por acción y API)**: entrega de mensaje simple a las audiencias, que se ejecutan simultáneamente en todos los perfiles según lo programado o mediante el déclencheur de API. Ideal para campañas promocionales, boletines informativos y mensajes transaccionales.

* **Campañas orquestadas**: Flujos de trabajo por lotes de varios pasos con segmentación compleja que utiliza datos relacionales (perfiles + productos/tiendas/reservas). Todos los perfiles procesados junto con los recuentos exactos de preenvío. Ideal para promociones de temporada, lanzamientos de productos y campañas que requieren datos de varias entidades.

**Diferencia clave**: los Recorridos mantienen el estado de cliente individual para acciones en tiempo real; las campañas de acción/API entregan mensajes simples en lote; las campañas orquestadas proporcionan lienzo de flujo de trabajo en lote con capacidades de segmentación de varias entidades.

<!-- waiting for DOCAC-13912 - [See detailed comparison](#journeys-vs-campaigns) -->
[Obtenga información sobre las campañas organizadas](../orchestrated/gs-orchestrated-campaigns.md)

+++

<!-- Waiting for DOCAC-13912
+++ Which journey type should I use?

Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.

+++
-->

+++ ¿Puedo editar un recorrido en directo?

Puede editar elementos limitados (nombre, contenido del mensaje), pero los cambios estructurales requieren la creación de una nueva versión. [Más información sobre las versiones de recorrido](publish-journey.md#journey-versions)

+++

➡️ **Más preguntas?** [Ver las preguntas frecuentes sobre el Recorrido completo](journey-faq.md) con más de 40 respuestas detalladas

## ¿Necesita ayuda? {#help}

### Vínculos rápidos para tareas comunes

* **[Crea tu primer recorrido](journey-gs.md)** - Guía paso a paso para principiantes
* **[Preguntas frecuentes sobre el Recorrido](journey-faq.md)** - Preguntas frecuentes respondidas
* **[Solución de problemas](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnosticar y corregir problemas
* **[Referencia de códigos de error](error-codes-reference.md)** - Comprender los mensajes de error
* **[Protecciones y limitaciones](../start/guardrails.md)**: límites técnicos y prácticas recomendadas

### Recibir notificaciones sobre problemas

Configura **[recorridos](../reports/alerts.md)** para recibir notificaciones en tiempo real cuando los recorridos encuentren errores o patrones inusuales.

### Recursos adicionales

* **[hub de administración de Recorrido](/help/rp_landing_pages/manage-journey-landing-page.md)**: herramientas para filtrado, optimización y administración de perfiles
* **[Referencia de actividades de Recorrido](/help/rp_landing_pages/about-journey-building-landing-page.md)**: guía completa para todos los tipos de actividades
* **[Solucionar problemas de ejecución](troubleshooting-execution.md)** - Problemas de ejecución del recorrido de depuración
* **[Solución de problemas de actividades entrantes](troubleshooting-inbound.md)** - Corregir problemas de entrada y calificación

**¿Listo para compilar su primer recorrido?** [Empiece ahora →](journey-gs.md)
