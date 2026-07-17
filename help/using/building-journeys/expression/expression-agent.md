---
solution: Journey Optimizer
product: journey optimizer
title: Generar expresiones con el Asistente de expresiones
description: Aprenda a utilizar el Ayudante de expresiones en Adobe Journey Optimizer para generar expresiones directamente en el editor de expresiones avanzadas de Recorrido utilizando indicaciones de lenguaje natural.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Beta pública" type="Informative"
mini-toc-levels: 2
feature_v2: []
subfeature_v2: []
source-git-commit: 9551133fab06cfa5e056ba98da73dcbf066916fc
workflow-type: tm+mt
source-wordcount: 1090
ht-degree: 2%

---


# Generar expresiones con el Asistente de expresiones {#expression-agent}

>[!AVAILABILITY]
>
>Esta característica se encuentra actualmente en **versión beta pública**. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](../../rn/releases.md).
>
>Antes de usar el Ayudante de expresiones, lea las [protecciones y limitaciones](../../content-management/gs-generative.md#generative-guardrails) relacionadas que se aplican a las características de IA generativa en Journey Optimizer.

El Ayudante de expresiones es una función con tecnología de IA integrada en el editor de expresiones avanzadas de Recorrido. Le ayuda a generar expresiones válidas a partir de peticiones de datos en lenguaje sencillo.

Está disponible dondequiera que se abra el Recorrido **[!UICONTROL Editor de expresiones avanzadas]**. Por ejemplo, al configurar condiciones y enrutamiento dentro de una **[actividad de optimización](../optimize.md)**, o al configurar una actividad de [**[!UICONTROL Espera &#x200B;]**](../wait-activity.md) que usa una fecha personalizada y necesita una expresión `dateTimeOnly`.

## Generar una expresión {#generate}

Para generar una expresión con el Ayudante de expresiones:

1. Abra el **[!UICONTROL editor de expresiones avanzadas]** en el recorrido, por ejemplo, desde una condición de ramificación, una actividad de **[!UICONTROL Optimize]** o una actividad de **[!UICONTROL Wait]** con una fecha personalizada.

   ![](../assets/expression-assistant-pane.png)

1. En el campo de texto, describa la expresión que desea generar en lenguaje sin formato. Por ejemplo:

   * *&quot;Usuarios de EE. UU. mayores de 18 años&quot;*
   * *&quot;Clientes que han realizado una compra en los últimos 30 días&quot;*

   Consulte [Mensajes de ejemplo](#example-prompts) al final de esta página para obtener ideas.

1. Haga clic en **[!UICONTROL Generar]** para enviar la solicitud.

   El asistente comienza a generar la expresión correspondiente y muestra los mensajes de estado de progreso mientras la generación está en curso.

   >[!NOTE]
   >
   >Si el asistente no puede generar una expresión válida (por ejemplo, si el mensaje hace referencia a campos que no existen en orígenes de datos disponibles), aparecerá un mensaje de error. Cuando esto sucede, revise la solicitud para utilizar nombres de campo y fuentes de datos disponibles en la configuración de recorrido y, a continuación, vuelva a generar.

1. Una vez que la expresión esté lista, revise el resultado en el panel.

   ![](../assets/expression-assistant-result.png)

   * Haga clic en el icono ![Vista previa](../assets/do-not-localize/generation-preview.svg) antes de aplicar para revisar el resultado del asistente para el escenario solicitado.

   * Haga clic en **[!UICONTROL Aplicar]** para insertar la expresión generada directamente en el editor de expresiones avanzadas (la misma ubicación en la que pegaría manualmente).
   * Utilice el control de copia para capturar el texto de expresión sugerido y pegarlo en otro lugar si es necesario.

## Ejemplos de peticiones {#example-prompts}

Las siguientes listas son solo ideas rápidas. No muestran la sintaxis de expresión generada, el resultado exacto depende de los campos y las actividades definidos en el recorrido.

### Evento de recorrido y acción personalizada {#example-prompts-event-action}

* *&quot;evento con un precio de pedido total superior a 100&quot;*
* *&quot;evento donde se creó el pedido en los últimos 7 días&quot;*
* *&quot;evento donde el tipo de evento es una compra comercial&quot;*
* *&quot;evento con pedido creado en la última hora&quot;*
* *&quot;el evento con un precio de pedido total superior a 200 y una respuesta de acción tiene un código de estado&quot;*

### Expresiones de actividad de espera {#example-prompts-datetime}

Cuando una actividad **[!UICONTROL Wait]** usa una fecha personalizada, usted define cuándo continúa el perfil creando una expresión `dateTimeOnly` en el **[!UICONTROL editor de expresiones avanzadas]**. Por ejemplo, desde un atributo de perfil, una marca de tiempo de evento, datos de calificación de segmentos o un desplazamiento calculado desde la hora actual. Para obtener información sobre cómo configurar esperas personalizadas y límites aplicables, consulte [Esperas personalizadas](../wait-activity.md#custom).

* *&quot;usar la última fecha de pedido del cliente solo como fecha y hora&quot;*
* *&quot;usar la hora del correo electrónico de consentimiento como solo fecha y hora&quot;*
* *&quot;convertir pertenencia a segmento última hora de calificación hasta la fecha solo hora&quot;*
* *&quot;nodo de espera: una semana después de Navidad de 2024 solo como fecha y hora&quot;*
* *&quot;nodo de espera: dentro de 30 días a las 10 p.m. solo como fecha y hora&quot;*
* *&quot;esperar hasta las 9 a. m. de hoy en la zona horaria UTC, devolver solo como fecha y hora&quot;*

## Recursos relacionados {#related}

* [Trabajar con el editor de expresiones avanzadas](expressionadvanced.md): Información general sobre la interfaz del editor de expresiones y sintaxis admitida.
* [Introducción al Asistente de IA en Journey Optimizer](../../content-management/gs-generative.md): protecciones generales, acceso y configuración para las funciones de IA generativa.

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica el Ayudante de expresiones, una característica con tecnología de IA del editor de expresiones avanzadas de Recorrido que genera expresiones de recorrido válidas a partir de mensajes de lenguaje sencillo.

**Intenciones:**

* Generación de una expresión de recorrido a partir de una descripción en lenguaje natural mediante el Ayudante de expresiones
* Aplique una expresión generada directamente en el editor de expresiones avanzadas con el botón Aplicar
* Utilice el Ayudante de expresiones dentro de Optimizar actividades, Actividades de condición y Actividades de espera con fecha personalizada
* Proporcione peticiones de ejemplo para condiciones basadas en eventos y `dateTimeOnly` expresiones de espera
* Solucione los problemas de generación fallida revisando las indicaciones para hacer referencia a nombres de campo y fuentes de datos válidos

**Glosario:**

* **Ayudante de expresiones**: característica generativa con tecnología de IA incrustada en el editor de expresiones avanzadas de Recorrido que convierte los mensajes de texto sin formato en expresiones de recorrido válidas *(específicas del producto)*
* **Editor de expresiones avanzadas**: La interfaz de Journey Optimizer para escribir expresiones complejas en condiciones, actividades de espera y asignación de parámetros de acción *(específico del producto)*
* **dateTimeOnly**: un tipo de expresión de fecha y hora sin zona horaria, necesaria para las actividades de espera de fecha personalizada *(específica del producto)*
* **Optimizar actividad**: una actividad de recorrido que admite condiciones de ramificación configurables mediante el editor de expresiones avanzadas *(específico del producto)*

**Protecciones:**

* El Ayudante de expresiones se encuentra actualmente en **versión beta pública**; la disponibilidad y el comportamiento pueden cambiar
* A esta función se aplican las limitaciones y protecciones de IA generativas de la documentación principal del asistente de IA
* Si el asistente hace referencia a campos que no están presentes en las fuentes de datos del recorrido, devuelve un error: revise el mensaje para utilizar los nombres de campo disponibles
* La sintaxis de la expresión generada exacta depende de los campos y las actividades configurados en el recorrido específico

**Terminología:**

* Nombre canónico: Ayudante de expresiones — Acrónimo: none — variantes: IA de expresión, generador de expresiones de recorrido
* Sinónimos: &quot;Ayudante de expresiones&quot; = &quot;Generador de expresiones de IA&quot;
* No confundir: Ayudante de expresiones (generador con tecnología de IA) ≠ Editor de expresiones avanzadas (el editor de código manual en sí)

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Dónde está disponible el Asistente para expresiones?** — Está disponible dondequiera que se abra el editor de expresiones avanzadas de Recorrido, incluidas las actividades Condición, Optimizar actividades y Actividades de espera con una fecha personalizada.
* **Q: ¿Qué sucede si el asistente no puede generar una expresión válida?** — Aparecerá un mensaje de error; deberá revisar la solicitud para que utilice nombres de campo y fuentes de datos que existan en la configuración de recorrido.
* **Q: ¿Cómo inserto una expresión generada en el editor?** — Haga clic en el botón **Aplicar** del panel del asistente para insertarlo directamente en la posición actual del cursor en el editor de expresiones avanzadas.
* **Q: ¿Puede el Ayudante de expresiones generar expresiones `dateTimeOnly` para las actividades de espera?** — Sí; por ejemplo, si se solicita &quot;dentro de 30 días a las 10 p.m. solo hora de fecha&quot;, se generará la expresión `dateTimeOnly` adecuada.
* **Q: ¿Está disponible el Ayudante de expresiones de forma general?** — No; actualmente está en versión beta pública. Consulte la página Ciclo de versiones de Journey Optimizer para ver las actualizaciones de disponibilidad.

+++
