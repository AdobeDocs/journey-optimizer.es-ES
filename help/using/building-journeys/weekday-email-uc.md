---
solution: Journey Optimizer
product: journey optimizer
title: Enviar correos electrónicos solo entre semana
description: Obtenga información sobre cómo configurar un recorrido para enviar correos electrónicos solo entre semana en Adobe Journey Optimizer
feature: Journeys, Use Cases, Email
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, caso de uso, días de la semana, condición, correo electrónico, programación
version: Journey Orchestration
source-git-commit: 970712614b0d4da37d9ecbe45701f93147b1428c
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 1%

---

# Enviar correos electrónicos solo entre semana {#send-emails-only-on-weekdays}

Este caso de uso muestra cómo configurar un recorrido en Adobe Journey Optimizer que envía correos electrónicos solo entre semana (de lunes a viernes). Para los perfiles que entran en el recorrido los fines de semana (sábado o domingo), los correos electrónicos se ponen en cola automáticamente y se envían el lunes a una hora especificada. Esto garantiza una participación óptima al enviar mensajes durante la semana laboral.

## Resumen del caso de uso

**El desafío**: garantizar que los correos electrónicos se envíen solo entre semana, aunque los perfiles puedan entrar al recorrido los fines de semana. Para las entradas de fin de semana, los correos electrónicos deben colocarse en la cola y enviarse el lunes a una hora específica.

**La solución**: use una actividad de condición para identificar el día de la semana. Para las entradas de fin de semana, las actividades de espera con fórmulas personalizadas retrasan el correo electrónico hasta el lunes. Las entradas de día de la semana proceden directamente al paso de envío de correo electrónico.

Este método muestra cómo utilizar una actividad de condición para comprobar si el día actual es sábado o domingo, implementar actividades de espera con fórmulas personalizadas para entradas de fin de semana, poner en cola correos electrónicos de fin de semana para entregas de lunes a una hora específica y enviar correos electrónicos inmediatamente para entradas de día laborable (lunes a viernes).

Este método es ideal para campañas de correo electrónico de empresa a empresa (B2B), boletines informativos y comunicaciones profesionales, anuncios relacionados con la empresa, actualizaciones de productos relacionadas con el trabajo y cualquier campaña de marketing en la que no se desee realizar la entrega los fines de semana.

>[!NOTE]
>
>Para implementar este caso de uso, necesita una instancia de Adobe Journey Optimizer activa con una [superficie de canal de correo electrónico](../configuration/channel-surfaces.md) configurada, una [audiencia](../audience/about-audiences.md) o [evento](../event/about-events.md) para almacenar en déclencheur el recorrido y una comprensión básica de [condiciones de recorrido](condition-activity.md) y [expresiones](expression/expressionadvanced.md).


## Pasos de implementación

### Paso 1: Crear el recorrido

1. Vaya a **[!UICONTROL Administración de Recorrido]** > **[!UICONTROL Recorridos]** en Adobe Journey Optimizer.

1. Haga clic en **[!UICONTROL Crear Recorrido]** para [crear un nuevo recorrido](journey-gs.md).

1. Configure las [propiedades de recorrido](journey-properties.md).

1. Elija su punto de entrada de recorrido:
   * **[Leer audiencia](read-audience.md)**: para campañas por lotes dirigidas a una audiencia específica
   * **[Evento](../event/about-events.md)**: para recorridos activados en tiempo real basados en el comportamiento del cliente

### Paso 2: Añadir una actividad de Condición para comprobar el día de la semana

Justo después del inicio del recorrido, agrega una actividad **[!UICONTROL Condición]** para comprobar si el día actual es sábado o domingo. Esto bifurcará el flujo de trabajo en consecuencia.

1. Arrastre y suelte una actividad [**[!UICONTROL Condition ]**](condition-activity.md) en el lienzo después del punto de entrada.

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

### Paso 3: Configurar actividades de espera para entradas de fin de semana

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

Antes de publicar, pruebe exhaustivamente la lógica de recorrido en el modo de prueba de Adobe Journey Optimizer para confirmar que todo funciona según lo esperado:

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

* [Actividades de condición](condition-activity.md): aprenda a crear diferentes rutas en su recorrido
* [Condiciones de uso en un recorrido](conditions.md): guía detallada sobre las condiciones de recorrido
* [Actividad de espera](wait-activity.md) - Configurar duraciones y fórmulas de espera
* [Funciones de fecha](functions/date-functions.md) - Referencia completa para funciones de fecha y hora
* [Editor de expresiones](expression/expressionadvanced.md) - Generar expresiones complejas
* [Prácticas recomendadas de Recorrido](journey-gs.md#best-practices) - Enfoques recomendados para el diseño de recorridos
