---
solution: Journey Optimizer
product: journey optimizer
title: Enviar correos electrónicos solo entre semana
description: Aprenda a configurar un recorrido para enviar correos electrónicos solo entre semana en  [!DNL Adobe Journey Optimizer]
feature: Journeys, Use Cases, Email
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, caso de uso, días de la semana, condición, correo electrónico, programación
version: Journey Orchestration
exl-id: 2f313e59-ee50-473c-9346-8859889346ec
TQID: https://experienceleague.adobe.com/qUt7t5LTYSQW278Pafx2-1t-DboRz9tU5IRpVhuEqLc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4ebid: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2: id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1622
ht-degree: 0%

---

# Enviar correos electrónicos solo entre semana {#send-emails-only-on-weekdays}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a configurar un recorrido que envíe correos electrónicos solo entre semana, a poner en cola las entradas de fin de semana para la entrega del lunes mediante una actividad de condición y a realizar actividades de espera con fórmulas personalizadas.

>[!ENDSHADEBOX]

Este caso de uso muestra cómo configurar un recorrido en [!DNL Adobe Journey Optimizer] que envíe correos electrónicos solamente en días de semana (de lunes a viernes). Para los perfiles que entran en el recorrido los fines de semana (sábado o domingo), los correos electrónicos se ponen en cola automáticamente y se envían el lunes a una hora especificada. Esto garantiza una participación óptima al enviar mensajes durante la semana laboral.

## Resumen del caso de uso

**El desafío**: garantizar que los correos electrónicos se envíen solo entre semana, aunque los perfiles puedan entrar al recorrido los fines de semana. Para las entradas de fin de semana, los correos electrónicos deben colocarse en la cola y enviarse el lunes a una hora específica.

**La solución**: use una actividad de condición para identificar el día de la semana. Para las entradas de fin de semana, las actividades de espera con fórmulas personalizadas retrasan el correo electrónico hasta el lunes. Las entradas de día de la semana proceden directamente al paso de envío de correo electrónico.

Este método muestra cómo utilizar una actividad de condición para comprobar si el día actual es sábado o domingo, implementar actividades de espera con fórmulas personalizadas para entradas de fin de semana, poner en cola correos electrónicos de fin de semana para entregas de lunes a una hora específica y enviar correos electrónicos inmediatamente para entradas de día laborable (lunes a viernes).

Este método es ideal para campañas de correo electrónico de empresa a empresa (B2B), boletines informativos y comunicaciones profesionales, anuncios relacionados con la empresa, actualizaciones de productos relacionadas con el trabajo y cualquier campaña de marketing en la que no se desee realizar la entrega los fines de semana.

>[!NOTE]
>
>Para implementar este caso de uso, necesita una instancia de Adobe Journey Optimizer activa con una [superficie de canal de correo electrónico](../configuration/channel-surfaces.md) configurada, una [audiencia](../audience/about-audiences.md) o [evento](../event/about-events.md) para almacenar en déclencheur el recorrido y una comprensión básica de [condiciones de recorrido](conditions.md) y [expresiones](expression/expressionadvanced.md).

## Pasos de implementación

Siga estos pasos para crear el flujo de correo electrónico solo entre semana.

### Paso 1: Crear el recorrido

1. Vaya a **[!UICONTROL Administración de Recorrido]** > **[!UICONTROL Recorridos]** en [!DNL Adobe Journey Optimizer].

1. Haga clic en **[!UICONTROL Crear Recorrido]** para [crear un nuevo recorrido](journey-gs.md).

1. Configure las [propiedades de recorrido](journey-properties.md).

1. Elija su punto de entrada de recorrido:
   * **[Leer audiencia](read-audience.md)**: para campañas por lotes dirigidas a una audiencia específica
   * **[Evento](../event/about-events.md)**: para recorridos activados en tiempo real basados en el comportamiento del cliente

### Paso 2: añadir una actividad de condición para comprobar el día de la semana

Justo después del inicio del recorrido, agrega una actividad **[!UICONTROL Condición]** para comprobar si el día actual es sábado o domingo. Esto bifurcará el flujo de trabajo en consecuencia.

1. Arrastre y suelte una actividad [**[!UICONTROL Optimize ]**](optimize.md) en el lienzo después del punto de entrada.

1. Haga clic en la actividad **[!UICONTROL Condición]** para abrir su panel de configuración.

1. Seleccione **[!UICONTROL Condición de tiempo]** como tipo de condición.

1. Seleccione **[!UICONTROL Día de la semana]** como opción de filtrado de tiempo.

1. Para la **primera ruta (sábado)**, seleccione solo **sábado**. Etiquete esta ruta como &quot;sábado&quot;.

1. Haga clic en **[!UICONTROL Agregar una ruta]** para crear una segunda condición.

1. Para la **segunda ruta (domingo)**, seleccione **[!UICONTROL Día de la semana]** y elija **domingo** solamente. Etiquete esta ruta como &quot;Domingo&quot;.

   ![Configuración de las condiciones sábado y domingo en el editor de expresiones](assets/weekday-email-uc-condition-expression.png)


1. Marque **[!UICONTROL Mostrar ruta de acceso para otros casos que no sean los anteriores]** para crear una ruta de acceso para las entradas de días laborables (de lunes a viernes).

>[!NOTE]
>
>La zona horaria utilizada para la evaluación del día de la semana se define en el nivel de recorrido en las propiedades del recorrido, no en el nivel de condición. La zona horaria [timezone](timezone-management.md) de recorrido que se usa es la del recorrido, no la del destinatario.

### Paso 3: configurar actividades de espera para entradas de fin de semana

Para los perfiles que ingresan el sábado o el domingo, use las actividades **[!UICONTROL Wait]** con fórmulas personalizadas para retrasar el correo electrónico hasta el lunes a la hora deseada.

En la actividad **[!UICONTROL Wait]**, use la fórmula siguiente:

```javascript
toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))
```

Donde:

* **X** es el número de días de espera:
   * Usar **2** para el sábado (esperar hasta el lunes)
   * Usar **1** para el domingo (esperar hasta el lunes)
* **H** es la hora que deseas enviar (por ejemplo, **9** por 9 AM)


**Ejemplo para el sábado:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))
```

**Ejemplo para domingo:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))
```

Para implementar esto en el recorrido:

1. En la ruta del **sábado**, agregue una actividad **[!UICONTROL Esperar]** después de la condición.

1. Seleccione **[!UICONTROL Duration]** como tipo de espera.

1. Haga clic en **[!UICONTROL Modo avanzado]** para escribir la fórmula personalizada.

1. Escriba: `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))`

   ![Recorrido con tres rutas de condición: sábado, domingo y días laborables](assets/weekday-email-uc-paths.png)

1. Repita los mismos pasos para la **ruta dominical**, con: `toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))`

>[!TIP]
>
>Para horarios comerciales más complejos (por ejemplo, enviar solo entre 9 a. m. y 5 p. m. en días laborables), puede mejorar aún más la fórmula y las condiciones.

### Paso 4: Rama de día de la semana

Para los perfiles que entran de lunes a viernes, continúe con el paso de envío de correo electrónico como de costumbre.

1. En la ruta de **día de la semana** (la ruta de &quot;otros casos&quot;), continúe directamente para agregar una actividad de acción **[!UICONTROL Correo electrónico]**. No se necesita ninguna actividad **[!UICONTROL Wait]** para las entradas entre semana.

1. Configure su mensaje de correo electrónico según sea necesario.

### Paso 5: Completar el flujo de recorrido

Después de las actividades **[!UICONTROL Wait]** en las rutas de sábado y domingo, las tres rutas (sábado, domingo y días de la semana) deben fluir a la misma actividad de acción **[!UICONTROL Email]**. Agregue una actividad **[!UICONTROL End]** después del correo electrónico.

### Introducción al flujo de trabajo visual

El flujo de trabajo del recorrido completo sigue esta lógica:

* **Inicio** → **[!UICONTROL Condición]**: ¿Es sábado o domingo?
   * **Sí (sábado):** **[!UICONTROL Esperar]** hasta el lunes 9 a.m. → **[!UICONTROL Enviar correo electrónico]**
   * **Sí (domingo):** **[!UICONTROL Esperar]** hasta el lunes 9 a.m. → **[!UICONTROL Enviar correo electrónico]**
   * **No (de lunes a viernes):** **[!UICONTROL Enviar correo electrónico]** inmediatamente

Esto garantiza que todos los correos electrónicos se envíen solo entre semana, con las entradas de fin de semana en cola automáticamente para la entrega del lunes.

### Paso 6: Prueba del recorrido

Antes de publicar, pruebe exhaustivamente la lógica de recorrido en el modo de prueba de [!DNL Adobe Journey Optimizer] para confirmar que todo funciona según lo esperado:

1. Haga clic en el botón **[!UICONTROL Probar]** en la esquina superior derecha.

1. Habilitar [modo de prueba](testing-the-journey.md).

1. Crear [perfiles de prueba](../audience/creating-test-profiles.md) con horas de entrada simuladas en diferentes días de la semana:
   * **Entrada del sábado**: comprueba que el perfil sigue la ruta del sábado, espera y recibe correo electrónico el lunes a la hora especificada
   * **Entrada de domingo**: comprueba que el perfil sigue la ruta de domingo, espera y recibe correo electrónico el lunes a la hora especificada
   * **Entradas de lunes a viernes**: compruebe que los correos electrónicos se envían inmediatamente sin ninguna espera

1. Revise la visualización del recorrido para asegurarse de que los perfiles siguen las rutas condicionales correctas (sábado, domingo o día de la semana).

1. Compruebe si hay [errores o advertencias](troubleshooting.md) en el recorrido.

1. Compruebe que las fórmulas de Wait calculan la duración correcta para la hora de entrega del lunes deseada.

>[!IMPORTANT]
>
>Pruebe siempre la lógica de recorrido en el modo de prueba para asegurarse de que las actividades de Espera se comportan según lo esperado. Utilice el modo de prueba para simular diferentes escenarios de entrada y validar que las entradas de fin de semana estén correctamente en cola para la entrega del lunes. Consulte [Prácticas recomendadas de pruebas de recorrido](testing-the-journey.md) para obtener más información.

### Paso 7: Publicar el recorrido

Una vez finalizada la prueba:

1. Haga clic en **[!UICONTROL Publicar]** en la esquina superior derecha.

1. Confirme la [publicación](publish-journey.md).

1. Monitorice el rendimiento del recorrido usando [informes de Recorrido](report-journey.md) e [informes en vivo](../reports/journey-live-report.md).


## Temas relacionados

* [Optimizar actividades](optimize.md): aprenda a crear diferentes rutas en su recorrido
* [Condiciones de uso en un recorrido](conditions.md): guía detallada sobre las condiciones de recorrido
* [Actividad de espera](wait-activity.md) - Configurar duraciones y fórmulas de espera
* [Funciones de fecha](functions/date-functions.md) - Referencia completa para funciones de fecha y hora
* [Editor de expresiones](expression/expressionadvanced.md) - Generar expresiones complejas
* [Prácticas recomendadas de Recorrido](journey-gs.md#best-practices) - Enfoques recomendados para el diseño de recorridos

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página proporciona un caso de uso paso a paso para configurar un recorrido que envía correos electrónicos solo entre semana mediante una condición de día de la semana y fórmulas de espera personalizadas para retrasar las entradas de fin de semana hasta el lunes.

**Intenciones:**

* Configure una actividad Condition para ramificar un recorrido según el día de la semana (sábado, domingo o día de la semana)
* Escribir expresiones de espera personalizadas usando `toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))` para retrasar los perfiles de fin de semana hasta el lunes
* Cree un recorrido de tres rutas que combine todas las rutas en una sola acción de correo electrónico
* Prueba de la lógica de correo electrónico solo entre semana con perfiles de prueba con diferentes días de entrada simulados
* Publicación y monitorización de un recorrido que suprime la entrega de correo electrónico durante el fin de semana

**Glosario:**

* **Condición de tiempo**: un tipo de actividad de condición en Journey Optimizer que ramifica las rutas de recorrido según criterios de fecha y hora, como el día de la semana *(específico del producto)*
* **nowWithDelta**: una función de expresión que devuelve el desplazamiento de fecha y hora actual por un número especificado de días u otras unidades *(específico del producto)*
* **setHours**: una función de expresión que establece una hora específica en un valor de fecha y hora determinado *(específico del producto)*
* **toDateTimeOnly**: una función de expresión que convierte un valor al formato `dateTimeOnly` requerido por las actividades de espera personalizadas *(específicas del producto)*

**Protecciones:**

* La zona horaria utilizada para la evaluación del día de la semana es la zona horaria configurada por el recorrido (configurada en las propiedades del recorrido), no la del destinatario individual.
* Para implementar este caso de uso, se necesita una superficie de canal de correo electrónico activa y una audiencia o evento para almacenar el recorrido en déclencheur.
* Un requisito previo es la comprensión básica de las condiciones de recorrido y el editor de expresiones avanzadas.
* Pruebe siempre el recorrido en modo de prueba antes de publicar para comprobar que las fórmulas de Espera producen la hora de entrega del lunes correcta.

**Terminología:**

* Nombre canónico: Programación de correo electrónico del día de la semana — Acrónimo: none — variantes: correos electrónicos solo entre semana, envío de correo electrónico en horario laboral
* Sinónimos: &quot;Ruta del sábado&quot; / &quot;Ruta del domingo&quot; = &quot;Rutas del fin de semana&quot;; &quot;Otra ruta de casos&quot; = &quot;Ruta del día laborable&quot;
* No confundir: zona horaria de recorrido (utilizada para la evaluación del día de la semana) ≠ la del destinatario

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Qué fórmula retrasa una entrada de sábado hasta el lunes a las 9 AM?** — Usar `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))` en la ruta de acceso del sábado (2 días hacia delante aterriza el lunes).
* **Q: ¿Qué fórmula retrasa una entrada de domingo hasta el lunes a las 9 AM?** — Usar `toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))` en la ruta de acceso del domingo (el lunes se adelanta 1 día).
* **Q: ¿Qué zona horaria se usa al evaluar la condición de día de la semana?** — La zona horaria configurada del recorrido definida en las propiedades del recorrido; no es la zona horaria local del destinatario.
* **Q: ¿Las entradas de días laborables necesitan una actividad de espera?** — No, los perfiles que entran de lunes a viernes proceden directamente a la actividad de acción Correo electrónico sin ninguna espera.
* **Q: ¿Cómo puedo probar que las entradas de fin de semana estén en cola correctamente?** — En modo de prueba, cree perfiles de prueba con horas de entrada simuladas de sábado y domingo y verifique que siguen la ruta condicional correcta y reciban el correo electrónico el lunes a la hora configurada.

+++
