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
hide: true
hidefromtoc: true
source-git-commit: 4b7d406e39328571a157b2d4c7b17f2adba77cdf
workflow-type: tm+mt
source-wordcount: '1869'
ht-degree: 1%

---

# Enviar correos electrónicos solo entre semana {#send-emails-only-on-weekdays}

Este caso de uso muestra cómo configurar un recorrido en Adobe Journey Optimizer que envía correos electrónicos solo entre semana (de lunes a viernes). Para los perfiles que entran en el recorrido los fines de semana (sábado o domingo), los correos electrónicos se ponen en cola automáticamente y se envían el lunes a una hora especificada. Esto garantiza una participación óptima al enviar mensajes durante la semana laboral.

## Resumen del caso de uso

**El desafío**: garantizar que los correos electrónicos se envíen solo entre semana, aunque los perfiles puedan entrar al recorrido los fines de semana. Para las entradas de fin de semana, los correos electrónicos deben colocarse en la cola y enviarse el lunes a una hora específica.

**La solución**: use una actividad de condición para identificar el día de la semana. Para las entradas de fin de semana, las actividades de espera con fórmulas personalizadas retrasan el correo electrónico hasta el lunes. Las entradas de día de la semana proceden directamente al paso de envío de correo electrónico.

Este método muestra cómo utilizar una actividad de condición para comprobar si el día actual es sábado o domingo, implementar actividades de espera con fórmulas personalizadas para entradas de fin de semana, poner en cola correos electrónicos de fin de semana para entregas de lunes a una hora específica y enviar correos electrónicos inmediatamente para entradas de día laborable (lunes a viernes).

Este método es ideal para campañas de correo electrónico de empresa a empresa (B2B), boletines informativos y comunicaciones profesionales, anuncios relacionados con la empresa, actualizaciones de productos relacionadas con el trabajo y cualquier campaña de marketing en la que no se desee realizar la entrega los fines de semana.

Vea el [tutorial de vídeo](#how-to-video) paso a paso en la parte inferior de esta página para ver la implementación completa.

## Requisitos previos

Para implementar este caso de uso, necesita una instancia de Adobe Journey Optimizer activa con una [superficie de canal de correo electrónico](../configuration/channel-surfaces.md) configurada, una [audiencia](../audience/about-audiences.md) o [evento](../event/about-events.md) para almacenar en déclencheur el recorrido y una comprensión básica de [condiciones de recorrido](condition-activity.md) y [expresiones](expression/expressionadvanced.md).

## Pasos de implementación

### Paso 1: Crear el recorrido

1. Vaya a **[!UICONTROL Administración de Recorrido]** > **[!UICONTROL Recorridos]** en Adobe Journey Optimizer.

1. Haga clic en **[!UICONTROL Crear Recorrido]** para crear un recorrido nuevo. [Más información sobre cómo crear recorridos](journey-gs.md)

1. Configure las propiedades del recorrido:
   * **Nombre**: Campaña De Correo Electrónico Entre Semana
   * **Descripción**: envía correos electrónicos solo de lunes a viernes
   * Establezca el área de nombres adecuada para su caso de uso

[Más información sobre las propiedades del recorrido](journey-properties.md)

1. Elija su punto de entrada de recorrido:
   * **[Leer audiencia](read-audience.md)**: para campañas por lotes dirigidas a una audiencia específica
   * **[Evento](../event/about-events.md)**: para recorridos activados en tiempo real basados en el comportamiento del cliente

### Paso 2: Añadir una actividad de Condición para comprobar el día de la semana

Justo después del inicio del recorrido, agrega una actividad **[!UICONTROL Condición]** para comprobar si el día actual es sábado o domingo. Esto bifurcará el flujo de trabajo en consecuencia.

1. Arrastre y suelte una actividad **[!UICONTROL Condition]** en el lienzo después del punto de entrada. [Más información sobre las actividades de condición](condition-activity.md)

1. Haga clic en la actividad Condición para abrir su panel de configuración.

1. En la sección **[!UICONTROL Tipo de condición]**, seleccione **[!UICONTROL Condición de Source de datos]**. [Más información sobre los tipos de condición](condition-activity.md#data_source_condition)

### Paso 3: Configurar la condición para identificar el sábado

Cree la primera ruta de condición para identificar las entradas del sábado.

1. Haga clic en **[!UICONTROL Modo avanzado]** para abrir el editor de expresiones. [Más información sobre el editor de expresiones](expression/expressionadvanced.md)

1. Introduzca la siguiente expresión para comprobar si el día actual es sábado:

   ```javascript
   dayOfWeek(now()) == 7
   ```

   Utiliza la función `dayOfWeek()` con `now()` para obtener el día actual. [Más información sobre las funciones de fecha](functions/date-functions.md)

   ![Configuración de la condición Saturday en el editor de expresiones](assets/weekday-email-uc-condition-expression.png)

1. Haga clic en **[!UICONTROL Aceptar]** para guardar la condición.

1. Etiquete esta ruta como &quot;sábado&quot;.

### Paso 4: Añadir una segunda ruta de condición para el domingo

1. En la actividad Condición, haga clic en **[!UICONTROL Agregar una ruta]** para crear una segunda condición.

1. En el editor de expresiones de la segunda ruta, introduzca:

   ```javascript
   dayOfWeek(now()) == 1
   ```

   Esto comprueba si el día actual es domingo.

1. Etiquete esta ruta como &quot;Domingo&quot;.

1. Marque **[!UICONTROL Mostrar ruta de acceso para otros casos que no sean los anteriores]** para crear una ruta de acceso para las entradas de días laborables (de lunes a viernes).

**Valores de día de la semana:**

| Valor | Day |
|-------|-----|
| 1 | Domingo |
| 2 | Lunes |
| 3 | Martes |
| 4 | Miércoles |
| 5 | Jueves |
| 6 | Viernes |
| 7 | Sábado |

>[!NOTE]
>
>La función `dayOfWeek()` devuelve un entero que representa el día de la semana, donde 1 es domingo y 7 es sábado. Esto sigue el estándar ISO-8601 para la numeración de días.

### Paso 5: Configurar actividades de espera para entradas de fin de semana

Para los perfiles que introducen datos el sábado o el domingo, utilice Actividades de espera con fórmulas personalizadas para retrasar el correo electrónico hasta el lunes a la hora deseada.

![Recorrido con tres rutas de condición: sábado, domingo y días laborables](assets/weekday-email-uc-paths.png)

**Para la ruta de acceso del sábado:**

1. Agregue una actividad **[!UICONTROL Wait]**. [Más información sobre las actividades de espera](wait-activity.md)

1. Seleccione **[!UICONTROL Duration]** como tipo de espera.

1. Haga clic en **[!UICONTROL Modo avanzado]** para escribir una fórmula personalizada.

1. Introduzca la siguiente fórmula para esperar hasta el lunes a las 9 a. m.:

   ```javascript
   toDuration("PT" + (48 - getHourOfDay(now())) + "H")
   ```

   O use esta fórmula alternativa:

   ```javascript
   setHours(nowWithDelta(2, "days"), 9)
   ```

   **Explicación**: Esta fórmula calcula el tiempo de espera de sábado a lunes a las 9 a. m. El valor X=2 representa 2 días hacia delante (sábado + 2 días = lunes). [Más información sobre las funciones de fecha](functions/date-functions.md#nowWithDelta)

**Para la ruta dominical:**

1. Agregue una actividad **[!UICONTROL Wait]**.

1. Seleccione **[!UICONTROL Duration]** como tipo de espera.

1. Haga clic en **[!UICONTROL Modo avanzado]** para escribir una fórmula personalizada.

1. Introduzca la siguiente fórmula para esperar hasta el lunes a las 9 a. m.:

   ```javascript
   setHours(nowWithDelta(1, "days"), 9)
   ```

   **Explicación**: Esta fórmula espera 1 día (domingo + 1 día = lunes) y establece la hora en 9 AM. El valor X=1 representa 1 día hacia adelante y H=9 representa 9 a. m.

>[!TIP]
>
>Puede personalizar el parámetro de hora (H) a cualquier momento en el que desee que se envíe el correo electrónico el lunes. Por ejemplo, cambie 9 a 10 para 10 a. m. o a 14 para 2 p. m.

### Paso 6: Configuración de la ruta del día de la semana

Para la ruta de acceso **Día de la semana** (de lunes a viernes):

1. Continúe directamente para agregar una actividad de acción **[!UICONTROL Correo electrónico]**. No se necesita ninguna actividad de espera para las entradas de días laborables. [Más información sobre las acciones de correo electrónico](journeys-message.md)

1. Configure su mensaje de correo electrónico:
   * Seleccione o cree su [contenido de correo electrónico](../email/get-started-email-design.md)
   * Configurar los [parámetros de correo electrónico](../email/email-settings.md)
   * Configure [personalización](../personalization/personalize.md) según sea necesario

1. Agregue una actividad **[!UICONTROL End]** después del correo electrónico.

### Paso 7: Combinar rutas de fin de semana con correo electrónico

Después de las actividades de Espera en las rutas de sábado y domingo, fusiónelas con la misma actividad de acción de correo electrónico:

1. En la actividad Espera de sábado, agregue una acción **[!UICONTROL Correo electrónico]**.

1. En la actividad Espera de domingo, conéctese a la misma acción de correo electrónico.

1. La ruta del día de la semana también debe fluir a esta acción de correo electrónico.

### Paso 8: Prueba del recorrido

Antes de publicar, pruebe exhaustivamente la lógica de recorrido en el modo de prueba de Adobe Journey Optimizer para confirmar que todo funciona según lo esperado:

1. Haga clic en el botón **[!UICONTROL Probar]** en la esquina superior derecha.

1. Active el modo de prueba. [Aprenda a probar su recorrido](testing-the-journey.md)

1. Crear [perfiles de prueba](../audience/creating-test-profiles.md) con horas de entrada simuladas en diferentes días de la semana:
   * **Entrada del sábado**: comprueba que el perfil sigue la ruta del sábado, espera y recibe correo electrónico el lunes a la hora especificada
   * **Entrada de domingo**: comprueba que el perfil sigue la ruta de domingo, espera y recibe correo electrónico el lunes a la hora especificada
   * **Entradas de lunes a viernes**: compruebe que los correos electrónicos se envían inmediatamente sin ninguna espera

1. Revise la visualización del recorrido para asegurarse de que los perfiles siguen las rutas condicionales correctas (sábado, domingo o día de la semana).

1. Compruebe si hay errores o advertencias en el recorrido. [Obtenga información sobre la solución de problemas de recorridos](troubleshooting.md)

1. Compruebe que las fórmulas de Wait calculan la duración correcta para la hora de entrega del lunes deseada.

>[!IMPORTANT]
>
>Pruebe siempre exhaustivamente la lógica de recorrido antes de publicar en producción. Utilice el modo de prueba para simular diferentes escenarios de entrada y validar que las entradas de fin de semana estén correctamente en cola para la entrega del lunes. [Más información acerca de las prácticas recomendadas para las pruebas de recorrido](testing-the-journey.md)

### Paso 9: Publicar el recorrido

Una vez finalizada la prueba:

1. Haga clic en **[!UICONTROL Publicar]** en la esquina superior derecha.

1. Confirme la publicación. [Más información acerca de la publicación de recorridos](publish-journey.md)

1. Monitorice el rendimiento del recorrido usando [informes de Recorrido](report-journey.md) e [informes en vivo](../reports/journey-live-report.md).

## Prácticas recomendadas y consideraciones

+++**Optimizar flujo de trabajo con fórmulas mejoradas**

Para mejorar el flujo de trabajo y gestionar requisitos comerciales más complejos, puede ampliar las fórmulas para tener en cuenta los días festivos, los husos horarios o el horario laboral específico más allá de la comprobación básica de días laborables. Ajuste el parámetro de hora (H) en la fórmula Espera para que coincida con el tiempo de envío óptimo; por ejemplo, si 10 a. m. muestra mejores tasas de participación, cambie la fórmula para utilizar la hora 10. Para la compatibilidad con varios husos horarios, considere la posibilidad de crear recorridos independientes para diferentes regiones geográficas a fin de garantizar la entrega los lunes en el huso horario local de cada destinatario.

+++

+++**Administración de husos horarios**

La función `now()` y la ejecución del recorrido utilizan la zona horaria configurada en el nivel de recorrido. Asegúrese de que la zona horaria del recorrido coincida con sus necesidades configurándolo en las propiedades del recorrido antes de publicar ([Más información acerca de la administración de la zona horaria](timezone-management.md)). Si la audiencia abarca varias zonas horarias, tenga en cuenta que la comprobación del día de la semana se realiza en la zona horaria configurada del recorrido, no en la del destinatario. Para las entregas específicas del huso horario, cree recorridos independientes para diferentes regiones o utilice la configuración del huso horario en la actividad Leer audiencia.

+++

+++**entrada de Recorrido y temporización**

Para los recorridos por lotes, [programe la lectura de la audiencia](read-audience.md#schedule) para que entre en déclencheur a una hora que tenga sentido para su audiencia; las ejecuciones por la mañana temprano (por ejemplo, 6:00 a.m.) son comunes en las comunicaciones comerciales. Para los recorridos basados en eventos, la condición se evaluará inmediatamente cuando se reciba el evento y los perfiles que entren los fines de semana esperarán automáticamente hasta el lunes ([Más información acerca de los eventos](../event/about-events.md)). Asegúrese de que su [configuración de tiempo de espera de recorrido](journey-properties.md#timeout) se ajuste al período de espera máximo (hasta 2 días de sábado a lunes).

+++

+++**Las pruebas son esenciales**

Como se destaca en la guía de implementación, pruebe siempre la lógica de recorrido para confirmar que todo funciona según lo esperado. Use **Modo de prueba** para simular diferentes escenarios de entrada sin enviar correos electrónicos reales. Pruebe las tres rutas (entradas de sábado, domingo y día de la semana), compruebe que los cálculos de Wait duration son correctos, confirme que la entrega del lunes se produce a la hora especificada y compruebe la visualización del recorrido para garantizar un enrutamiento de ruta adecuado.

+++

+++**Reentrada y frecuencia**

Para campañas recurrentes, establece correctamente la configuración de **[!UICONTROL Reentrada]** ([Más información acerca de la configuración de reentrada](entry-management.md)). Si los perfiles pueden volver a entrar en el recorrido, estarán sujetos a la comprobación de día de la semana cada vez, lo que garantiza que las entradas de fin de semana siempre se mantengan en cola para los lunes. Considere la posibilidad de agregar [reglas de límite de frecuencia](../conflict-prioritization/journey-capping.md) para evitar mensajes excesivos si los perfiles pueden volver a entrar con frecuencia.

+++

## Variaciones avanzadas

+++**Segmentación por día específico**

Para enviar correos electrónicos solo en días específicos (como martes y jueves), modifique la condición:

```javascript
dayOfWeek(now()) == 3 or dayOfWeek(now()) == 5
```

Para el resto de días, agregue una actividad Wait que calcule el número de días hasta el martes o el jueves siguientes.

+++

+++**Diferentes tiempos de envío para diferentes días**

Puede crear varias rutas con diferentes fórmulas de espera para diferentes comportamientos de fin de semana. Por ejemplo, use `nowWithDelta(4, "days")` para la entrega de sábado a miércoles o `nowWithDelta(2, "days")` para la entrega de domingo a martes. Esto permite una mayor flexibilidad en la programación de envíos.

+++

+++**Envío en horario laboral**

Para garantizar la entrega durante el horario laboral, ajuste el parámetro hour en la fórmula Wait. Por ejemplo, para la entrega a las 2 p. m. en lugar de a las 9 a. m.:

```javascript
setHours(nowWithDelta(1, "days"), 14)
```

También puede agregar una segunda condición después de Esperar para comprobar si la hora actual se encuentra dentro del horario laboral antes de enviarla.

+++

+++**Exclusión por vacaciones**

Para excluir festivos, añada una ruta de condición adicional que compruebe fechas específicas:

```javascript
toDateTimeOnly(now()) == toDateTimeOnly("2024-12-25T00:00:00")
```

Si la condición coincide con un día festivo, añada una actividad Wait para retrasarla hasta el siguiente día laborable. [Más información acerca de las funciones de comparación de fechas](functions/date-functions.md)

+++

## Temas relacionados

| Tema | Descripción |
|-------|-------------|
| [Acerca de las actividades de condición](condition-activity.md) | Aprenda a crear diferentes rutas en el recorrido |
| [Usar condiciones en un recorrido](conditions.md) | Guía detallada sobre las condiciones de recorrido |
| [Actividad Esperar](wait-activity.md) | Configuración de duraciones de espera y fórmulas |
| [Funciones de fecha](functions/date-functions.md) | Referencia completa para funciones de fecha y hora |
| [Editor de expresiones](expression/expressionadvanced.md) | Crear expresiones complejas |
| [Probar el recorrido](testing-the-journey.md) | Validar la lógica de recorrido antes de publicar |
| [Administración de husos horarios](timezone-management.md) | Gestión de diferentes zonas horarias en recorridos |
| [Prácticas recomendadas de Recorrido](journey-gs.md#best-practices) | Enfoques recomendados para el diseño de recorridos |

## Vídeo práctico

Aprenda a enviar correos electrónicos solo entre semana con Adobe Journey Optimizer. Este vídeo muestra la implementación paso a paso de actividades de condición y fórmulas de Espera para poner en cola las entradas de fin de semana para la entrega del lunes.

>[!VIDEO](https://video.tv.adobe.com/v/3469330?quality=12&learn=on)

## Recursos adicionales

| Recurso | Descripción |
|----------|-------------|
| [Documentación del editor de expresiones](expression/expressionadvanced.md) | Generar y validar expresiones de recorrido |
| [guía de diseñador de Recorrido](using-the-journey-designer.md) | Dominar el lienzo de recorrido |
| [información general sobre casos de uso de Recorrido](jo-use-cases.md) | Explore más patrones de recorrido y ejemplos |
| [Publicación de blog de la comunidad: cómo enviar correos electrónicos solo los días laborables](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/how-to-send-emails-only-on-weekdays-in-adobe-journey-optimizer/ba-p/760400?profile.language=es){target="_blank"} | Publicación de blog original con ejemplos detallados |

