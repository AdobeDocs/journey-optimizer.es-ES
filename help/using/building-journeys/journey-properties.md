---
solution: Journey Optimizer
product: journey optimizer
title: Defina las propiedades de su recorrido
description: Obtenga información sobre cómo establecer las propiedades del recorrido con  [!DNL Adobe Journey Optimizer]
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, configuración, propiedades
exl-id: 6c21371c-6cbc-4d39-8fe6-39f1b8b13280
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/fDzEwuisEjAKvpIs9SKoz-9IIJXJQ-md9FlCbWQOJz8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: ba62ad25-65cb-4ea9-b7aa-0fa87c4a9fa0id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 4990
ht-degree: 10%

---

# Establecimiento de las propiedades del recorrido {#jo-properties}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a establecer las propiedades globales de un recorrido, incluido su nombre, reglas de entrada, huso horario, fechas de inicio y finalización, tiempo de espera, criterios de salida y administración de conflictos, desde el carril derecho durante la creación.

>[!ENDSHADEBOX]

Utilice las propiedades del recorrido para definir la configuración global del recorrido, incluido el nombre, las reglas de entrada, la zona horaria, las fechas de inicio y finalización, la duración del tiempo de espera, los criterios de salida y la administración de conflictos. Se puede acceder a las propiedades desde el carril derecho en cualquier fase de la creación del recorrido.

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Propiedades del recorrido"
>abstract="Las propiedades del recorrido contienen las opciones globales de este recorrido, incluidos el nombre, las etiquetas, las reglas de entrada, el huso horario, las fechas, el tiempo de espera y la administración de conflictos. Los parámetros de solo lectura están ocultos de forma predeterminada. Las opciones disponibles varían en función del estado del recorrido, los permisos y la configuración del producto."

## Acceso a las propiedades de un recorrido {#access-properties}

Las propiedades de un recorrido están centralizadas en el carril derecho. Esta sección se muestra de forma predeterminada al crear un nuevo recorrido. Para los recorridos existentes, haga clic en el icono de lápiz situado junto al nombre del recorrido para abrirlo.

En esta sección, defina el nombre del recorrido, añada una descripción y defina las propiedades globales del recorrido.

Puede hacer lo siguiente:

* Asigne etiquetas unificadas [!DNL Adobe Experience Platform] al recorrido para clasificarlas fácilmente y mejorar la búsqueda desde la lista de campañas. [Descubra cómo trabajar con campañas](../start/search-filter-categorize.md#tags)
* Seleccione las métricas de recorridos. [Aprenda a configurar y rastrear sus métricas de recorridos](success-metrics.md)
* Administrar [entrada y reentrada](#entrance). La administración de la entrada del perfil depende del tipo de recorrido. Los detalles están disponibles en [esta página](entry-management.md)
* Administrar [acceso a datos](#manage-access)
* Seleccione el recorrido y el perfil [husos horarios](#timezone)
* Elija [fechas de inicio y finalización](#dates) personalizadas
* Defina un tiempo de espera de [timeout duration](#timeout) en las actividades de recorrido (solo para usuarios administradores)
* Supervise el [tamaño actual de carga útil de recorrido](#journey-payload-size) para evitar errores de publicación
* Supervise los conflictos y dé prioridad a sus recorridos con [herramientas de administración de conflictos](#conflict)

![panel de configuración de propiedades de Recorrido con configuración general y opciones avanzadas](assets/new-journey-properties.png){width="80%"}{zoomable="yes"}

>[!NOTE]
>
>Para los recorridos activos, esta pantalla muestra solo la fecha de publicación y el nombre del usuario que publicó el recorrido.

La opción **Copiar detalles técnicos** le permite copiar información técnica sobre el recorrido que el equipo de soporte técnico puede usar para solucionar problemas. Se copia la siguiente información:

**General**

* `JourneyVersion UID`: identificador único de esta versión del recorrido
* `OrgID` - Identificador de su organización (IMS)
* `orgName` - Nombre de su organización
* `sandboxName`: nombre de la zona protegida donde se ejecuta el recorrido
* `lastDeployedBy` - Usuario que publicó el recorrido por última vez
* `lastDeployedAt` - Fecha y hora de la última publicación


**Pausar y reanudar** (incluido cuando el recorrido se ha pausado al menos una vez)

* `lastPausedAt` - Fecha y hora de la última vez que se pausó el recorrido
* `lastPausedBy` - Nombre para mostrar del usuario que realizó la última pausa
* `lastPausedById`: identificador interno del usuario que realizó la última pausa
* `lastResumedAt` - Fecha y hora de la última vez que se reanudó el recorrido
* `lastResumedBy` - Nombre para mostrar del usuario que realizó el último currículo
* `lastResumedById`: identificador interno del usuario que realizó el último currículo

**Configuración de recorrido en pausa** (en `pausedJourneySettings`, cuando el recorrido está o se ha pausado)

* `pauseBehavior`: qué les sucede a los perfiles del recorrido cuando se pausa (por ejemplo, deséchelos o manténgalos en su lugar)
* `maxPauseDurationInMinutes`: duración máxima de la pausa en minutos, después de la cual la recorrido se reanuda automáticamente (por ejemplo, 20160 = 14 días)
* `transitionStateForAutoResume`: estado aplicado cuando el recorrido se reanuda automáticamente al final del período de pausa (por ejemplo, detener o continuar)
* `pauseId`: identificador único de la instancia de pausa actual

Obtenga más información acerca de los campos técnicos relacionados con un recorrido para un perfil determinado y cómo usarlos [en esta página](expression/journey-properties.md).

## Entrada y reentrada {#entrance}

El modo de entrada de perfil se define en el nivel de recorrido, en el panel de configuración derecho. A continuación se describe la configuración.

La administración de la entrada del perfil depende del tipo de recorrido. Obtenga más información acerca de la administración de entrada y reentrada de perfiles en [esta página](entry-management.md). Obtenga más información acerca de las tasas de procesamiento de recorridos y cómo fluyen los perfiles entre los recorridos en [esta sección](entry-management.md#journey-processing-rate).

### Permitir la reentrada  {#allow-reentrance}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_entrance"
>title="Permitir la reentrada"
>abstract="De forma predeterminada, los nuevos recorridos permiten la reentrada. Desmarcar la opción **Permitir reentrada** impide que una persona vuelva a iniciar el recorrido, por ejemplo, si quiere ofrecer un regalo único cuando una persona entra en una tienda."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="Administración de la entrada del perfil"

De forma predeterminada, los nuevos recorridos permiten la reentrada. Puede desmarcar la opción **Permitir la reentrada** para recorridos de &quot;una sola vez&quot;, por ejemplo, si desea ofrecer un regalo de una sola vez cuando una persona entra a una tienda.

### Período de espera de reentrada  {#reentrance-wait}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_re-entrance_wait"
>title="Período de espera de reentrada"
>abstract="El período de espera de reentrada es el tiempo de espera antes de que un perfil pueda volver a entrar en recorridos unitarios. Evita que los usuarios vuelvan a entrar en el recorrido durante un tiempo determinado. Duración máxima: 90 días."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="Administración de la entrada del perfil"

Cuando se activa la opción **Permitir la reentrada**, se muestra el campo **Período de espera de reentrada**. Este campo permite definir el tiempo de espera antes de permitir que un perfil vuelva a entrar en el recorrido en el caso de recorridos unitarios (empezando con un evento o una calificación de público). Esto evita que los recorridos se activen varias veces por error para el mismo evento. De forma predeterminada, el campo se establece en 5 minutos. La duración máxima es de 90 días.

## Administrar acceso {#manage-access}

Puede limitar el acceso a un recorrido en función de las etiquetas de acceso.

Para asignar al recorrido etiquetas de uso de datos personalizadas, haga clic en el icono **[!UICONTROL Administrar etiquetas de acceso]** y seleccione una o varias etiquetas.

[Más información sobre el Control de acceso de nivel de objeto (OLAC)](../administration/object-based-access.md)

## Tamaño de la carga útil del recorrido {#journey-payload-size}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_payload_size"
>title="Tamaño actual de la carga útil del recorrido"
>abstract="Muestra el tamaño actual de la carga útil del recorrido en comparación con el límite configurado. Este indicador monitoriza la complejidad del recorrido antes de la publicación y evita errores producidos por un exceso del límite de tamaño de la carga útil."

El campo **[!UICONTROL Tamaño de carga útil del recorrido actual]** del panel de propiedades del recorrido muestra el tamaño actual de la carga útil del recorrido en relación con el límite configurado; por ejemplo, *1,5 MB (de 2 MB)*. Este indicador de solo lectura es visible en cualquier fase de la creación del recorrido.

![Indicador de tamaño de carga útil de recorrido actual en el panel de propiedades de recorrido](assets/journey-payload-size.png){width="50%" zoomable="yes"}

Utilice esta información para monitorizar la complejidad del recorrido antes de publicarlo. Si el tamaño de la carga útil se aproxima o supera el límite, se produce un error en la publicación del recorrido. Para reducir el tamaño, considere la posibilidad de simplificar la lógica de recorrido o reducir el número de actividades.

El límite predeterminado es de 4 MB. Póngase en contacto con el Servicio de atención al cliente de Adobe si necesita solicitar un límite más alto para su organización.

Para obtener información detallada sobre los umbrales, los mensajes de advertencia y error y los pasos para la solución de problemas, consulte [validación del tamaño de la carga útil de Recorrido](../start/guardrails.md#journey-payload-size) y [protecciones generales de recorrido](../start/guardrails.md#journeys-guardrails-journeys).

## Zonas horarias de recorrido y perfil {#timezone}

La zona horaria se define en el nivel de recorrido. Puede escribir una zona horaria fija o usar [!DNL Adobe Experience Platform] perfiles para definir la zona horaria de recorrido. Si se define una zona horaria en el perfil [!DNL Adobe Experience Platform], se puede recuperar en la recorrido.

[Más información sobre la administración de huso horario](../building-journeys/timezone-management.md)

## Fecha de inicio y de finalización {#dates}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_start_date"
>title="Fecha de inicio"
>abstract="La fecha de inicio en la que los perfiles pueden empezar a entrar en el recorrido. Si no se establece ninguna fecha de inicio, la predeterminada es la fecha de publicación del recorrido."

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_end_date"
>title="Fecha de finalización"
>abstract="La fecha de finalización es cuando finaliza el recorrido. En esta fecha, los perfiles activos saldrán automáticamente del recorrido y no se permitirán nuevas entradas."

De forma predeterminada, los perfiles pueden entrar en el recorrido en cuanto se publique y pueden permanecer hasta que se alcance el [tiempo de espera de recorrido global](#global_timeout). La única excepción son los recorridos de lectura recurrentes con **Forzar reentrada en repetición** activada, que terminan en la fecha de inicio de la siguiente ocurrencia.

Si es necesario, puede definir **fecha de inicio** y **fecha de finalización** personalizadas. Esto permite a los perfiles introducir el recorrido en una fecha específica y salir automáticamente cuando se llega a la fecha de finalización.

## Tiempo de espera {#timeout}

La configuración del tiempo de espera controla cuánto tiempo espera un recorrido a que se ejecute la actividad y cuánto tiempo pueden permanecer los perfiles en un recorrido.

### Tiempo de espera en actividades de recorrido {#timeout_and_error}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_timeout"
>title="Tiempo de espera o error"
>abstract="La opción **Tiempo de espera o error** define una ruta alternativa en el recorrido cuando la acción agota el tiempo de espera o devuelve un error, de modo que los perfiles continúan con una ruta de reserva, en lugar de detenerse en este paso. Los valores recomendados están entre 1 y 30 segundos."

Al editar una actividad de acción o condición, puede definir una ruta alternativa en caso de error o tiempo de espera. Si el procesamiento de la actividad que busca un sistema de terceros supera el tiempo de espera definido en el campo **[!UICONTROL Tiempo de espera o error]** de las propiedades del recorrido, se elegirá la segunda ruta para realizar una posible acción de reserva.

Los valores recomendados están entre 1 y 30 segundos.

Le recomendamos que defina un valor muy corto de **[!UICONTROL Tiempo de espera o error]** si su recorrido distingue entre tiempo y minúsculas (por ejemplo: reacción a la ubicación en tiempo real de una persona) porque no puede retrasar su acción más de unos segundos. Si el recorrido distingue menos del tiempo, puede utilizar un valor más largo para dar más tiempo al sistema llamado para enviar una respuesta válida.

Recorrido también utiliza un tiempo de espera global como se detalla a continuación.

### Tiempo de espera de recorrido global {#global_timeout}

Además del tiempo de espera [timeout](#timeout_and_error) utilizado en las actividades de recorrido, se aplica un tiempo de espera de recorrido global. No se muestra en la interfaz y no se puede cambiar.

Este tiempo de espera global detiene el progreso de los individuos en el recorrido **91 días** después de que ingresan. Esto significa que el recorrido de una persona no puede durar más de 91 días. Después de este período de tiempo de espera, se eliminan los datos del individuo. Las personas que sigan fluyendo en el recorrido al final del periodo de tiempo de espera se detendrán y no se tendrán en cuenta en los informes. Por lo tanto, podría ver más personas entrando en el recorrido que saliendo.

>[!NOTE]
>
>La definición exacta de cuándo se considera que un recorrido ha finalizado varía según el tipo de recorrido. [Ver criterios detallados](end-journey.md#journey-finished-definition).

Debido al tiempo de espera de recorrido de 91 días, cuando no se permite la reentrada al recorrido, no podemos asegurarnos de que el bloqueo de reentrada funcione más de 91 días. De hecho, al eliminar toda la información sobre las personas que ingresaron al recorrido 91 días después de su entrada, no podemos saber la persona ingresada anteriormente, hace más de 91 días.

Una persona solo puede entrar en una actividad de espera si le queda tiempo suficiente en el recorrido para completar la duración de la espera antes del tiempo de espera de 91 días. Consulte [esta página](../building-journeys/wait-activity.md).

### Preguntas frecuentes sobre el tiempo de vida (TTL) y la retención de datos {#timeout-faq}

A partir de la versión de [!DNL Adobe Journey Optimizer] de junio de 2024, el tiempo de espera global de recorrido ha pasado de 30 a 91 días. Los impactos se enumeran en las preguntas frecuentes a continuación:

**Para Recorridos Unitarios**

<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>¿Qué sucede con los recorridos publicados después de que se implemente la extensión TTL?</p>
    </td>
    <td>
      <p>Los perfiles que entren en el nuevo recorrido tendrán automáticamente un TTL de 91 días.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>¿Qué sucede con un perfil que introduce un recorrido publicado antes del lanzamiento de la extensión TTL?</p>
    </td>
    <td>
      <p>El perfil tendrá un TTL de 30 días (7 días para HIPAA), coherente con el momento en que se publicó originalmente el recorrido.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>¿Qué les sucede a los perfiles que ya han entrado en un recorrido cuando se inicia la extensión TTL?</p>
    </td>
    <td>
      <p>El perfil conservará un TTL de 30 días (7 días para HIPAA), según la hora de publicación original del recorrido.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>¿Qué sucede con un perfil de una versión de recorrido anterior que se vuelve a publicar después del lanzamiento de la extensión TTL?</p>
    </td>
    <td>
      <p>El perfil mantendrá un TTL de 30 días (7 días para HIPAA), alineado con el tiempo de publicación de la versión del recorrido original.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>¿Qué sucede si un nuevo perfil introduce una versión de recorrido republicada después del inicio de la extensión TTL?</p>
    </td>
    <td>
      <p>El perfil tendrá un TTL de 91 días, que coincide con el TTL de la versión del recorrido recién publicada.</p>
    </td>
  </tr>
</table>

**Para Recorridos de Déclencheur de segmentos**

<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>¿Qué sucede con los nuevos recorridos únicos publicados después de la extensión TTL?</p>
    </td>
    <td>
      <p>Los perfiles que entren en el nuevo recorrido tendrán un TTL de 91 días automáticamente.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>¿Qué sucede con los nuevos recorridos recurrentes sin reentrada forzada publicados después de la extensión TTL?</p>
    </td>
    <td>
      <p>Los perfiles que entren en el nuevo recorrido tendrán un TTL de 91 días automáticamente.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>¿Qué sucede con los nuevos recorridos recurrentes con reentrada forzada publicados después de la extensión TTL?</p>
    </td>
    <td>
      <p>Los perfiles que entren en el nuevo recorrido tendrán un TTL igual al periodo de periodicidad. Por ejemplo, si el recorrido se ejecuta a diario, el TTL será de 1 día.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>¿Qué sucede con un perfil que introduce un recorrido publicado antes del lanzamiento de la extensión TTL?</p>
    </td>
    <td>
      <p>El perfil tendrá un TTL de 30 días (7 días para HIPAA), coherente con el tiempo de publicación original. Para los recorridos recurrentes con reentrada forzada, el TTL coincidirá con el período de periodicidad.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>¿Qué sucede con un perfil que se ejecuta a través de un recorrido cuando se inicia la extensión TTL?</p>
    </td>
    <td>
      <p>El perfil conservará un TTL de 30 días (7 días para HIPAA), según la hora de publicación original del recorrido. Para los recorridos recurrentes con reentrada forzada, el TTL coincidirá con el período de periodicidad.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>¿Qué sucede con un perfil en ejecución en una versión de recorrido anterior que se vuelve a publicar después del lanzamiento de la extensión TTL?</p>
    </td>
    <td>
      <p>El perfil mantendrá un TTL de 30 días (7 días para HIPAA), alineado con el tiempo de publicación de la versión del recorrido original. Para los recorridos recurrentes con reentrada forzada, el TTL coincidirá con el período de periodicidad.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>¿Qué sucede si un nuevo perfil introduce una versión de recorrido republicada después del inicio de la extensión TTL?</p>
    </td>
    <td>
      <p>El perfil tendrá un TTL de 91 días, que coincide con el TTL de la versión del recorrido recién publicada. Para los recorridos recurrentes con reentrada forzada, el TTL coincidirá con el período de periodicidad.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>¿Se detendrá mi recorrido de lectura de audiencia recurrente siempre activo después de 91 días?</p>
    </td>
    <td>
      <p>No. Un recorrido de audiencia de lectura recurrente sin fecha de finalización permanece <strong>activo</strong> mientras se publique. Pasa al estado <strong>Finalizado</strong> solo 91 días después de la ejecución de su <strong>última incidencia</strong>. El tiempo de espera global de 91 días se aplica a perfiles individuales que fluyen por la recorrido (duración activa máxima por perfil), no al estado Activo del recorrido.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>¿Cuál es la diferencia entre el tiempo de espera de recorrido de 91 días y la ventana de creación de informes de 91 días?</p>
    </td>
    <td>
      <p>Estos son dos conceptos separados. El tiempo de espera global de <strong>recorrido</strong> (91 días) es el tiempo máximo que un perfil individual puede permanecer activo en un recorrido: después de 91 días, se sale del perfil y se eliminan sus datos. La <strong>ventana de informes</strong> (aproximadamente 91 días) es un límite de visualización en la interfaz de usuario: los datos de rendimiento anteriores a ~91 días ya no son visibles en los informes, pero el recorrido en sí sigue ejecutándose y siguen entrando nuevos perfiles.</p>
    </td>
  </tr>
</table>

## Política de combinación {#merge-policies}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_merge_policy"
>title="Política de combinación"
>abstract="La directiva de combinación se recupera automáticamente en función del evento o el público seleccionados. Esta directiva de combinación se utiliza en todo el recorrido."

[!DNL Adobe Journey Optimizer] usa políticas de combinación al recuperar datos de perfil de [!DNL Adobe Experience Platform]. Según el tipo de recorrido, se utilizan distintas políticas de combinación:

* En **[recorridos de lectura de audiencia](read-audience.md)** o **[calificación de audiencia](audience-qualification-events.md)**: se usa la política de combinación de la audiencia
* En **[recorridos de evento unitario](../event/about-events.md)**: se usa la política de combinación predeterminada
* En **[evento empresarial](../event/about-creating-business.md)** recorridos: se usa la política de combinación de la audiencia de destino en la siguiente actividad Leer audiencia

[!DNL Adobe Journey Optimizer] aplica la política de combinación utilizada en todo el recorrido. Por lo tanto, si se usan varias audiencias en un recorrido (por ejemplo, usando en [`inAudience` funciones](functions/functioninaudience.md)), se crean incoherencias con la política de combinación utilizada por el recorrido, se genera un error y se bloquea la publicación. Sin embargo, si se utiliza una audiencia incoherente en la personalización de mensajes, no se genera una alerta, a pesar de la incoherencia. Por este motivo, es muy recomendable comprobar la política de combinación asociada a su audiencia cuando esta audiencia se utiliza en la personalización de mensajes.

Para obtener más información sobre las políticas de combinación, consulte [[!DNL Adobe Experience Platform] documentación](https://experienceleague.adobe.com/es/docs/experience-platform/profile/merge-policies/overview){target="_blank"}.

>[!NOTE]
>
>Cuando se actualiza una política de combinación de audiencias, cualquier recorrido activo que haga referencia a esa audiencia debe volver a publicarse (o duplicarse). Cambiar la política de combinación crea de forma efectiva una audiencia &quot;nueva&quot; a la que el recorrido en curso no puede acceder, lo que garantiza la coherencia de los datos.

## Criterios de salida {#exit-criteria}

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="Criterios de salida"
>abstract="En esta sección se muestran las opciones de criterios de salida, en las que se pueden definir una o varias reglas de criterios de salida y filtros para el recorrido."

### Recorrido Criterios de salida {#exit-criteria-desc}

Al añadir criterios de salida, se hace que los perfiles salgan del recorrido en cuanto se produce un evento (por ejemplo, la compra) o que cumplan los requisitos para una audiencia. Esto evitará que el usuario reciba más comunicaciones del recorrido.

Es posible que desee eliminar perfiles de un recorrido cuando ya no cumplan el propósito del recorrido. Esto se puede lograr mediante **criterios de salida globales**, que están estrechamente asociados con la administración de objetivos.

>[!TIP]
>
>¿Busca orientación práctica con ejemplos reales? Consulte nuestra [guía completa de criterios de entrada y salida de recorrido](entry-exit-criteria-guide.md), que incluye casos de uso completos con configuraciones de entrada y salida, prácticas recomendadas y estrategias de optimización.

**Caso de uso de ejemplo**

Un experto en marketing tiene un recorrido promocional que tiene una serie de comunicaciones. Cada una de estas comunicaciones tiene como objetivo impulsar al cliente a realizar una compra. Tan pronto como se realice la compra, el cliente no debe recibir el resto de los mensajes de la serie. Al definir un criterio de salida, los perfiles que hayan realizado una compra se eliminan de la recorrido.

### Configuración y uso {#exit-criteria-config}

Los criterios de salida se establecen en el nivel de recorrido. Un recorrido puede tener varios criterios de salida. Si ha establecido varios criterios de salida, la evaluación se realizará de arriba abajo con una lógica de `OR`. Por lo tanto, si tiene los criterios de salida A y B, se evaluará como A **O** B. Los criterios se evalúan en cada paso del recorrido.

Para **crear** un criterio de salida, siga estos pasos:

1. Abra el recorrido.

1. Haga clic en el icono ![Mostrar criterios de salida](assets/do-not-localize/Smock_UserCheckedOut_18_N.svg) **[!UICONTROL Mostrar criterios de salida]** ubicado en la sección superior derecha del lienzo de recorrido.

1. Seleccione **[!UICONTROL Agregar criterios de salida]**.

1. Escriba una **Etiqueta** y seleccione si los criterios de salida se basan en un **Evento** o en una **Audiencia**.

   * Para los criterios de Salida basados en un evento, como descargar una aplicación o agregar un producto al carro de compras, elija solo evento unitario.
   * Para los criterios de Salida basados en una audiencia, como una audiencia que comprueba si un cliente ha realizado compras en las últimas 24 horas, seleccione una audiencia. Nota: Los criterios de salida que utilizan una audiencia pueden tardar hasta 10 minutos en ser efectivos.

Puede agregar varios criterios de salida. Los criterios de salida ahora están activos y se evaluarán en cada paso del recorrido.

![Panel de criterios de salida que muestra las condiciones de audiencia para la finalización del recorrido](assets/exitcriteria-sample.png){width="40%"}


### Criterios de salida basados en atributos de perfil {#profile-exit-criteria}

Los criterios de salida basados en atributos de perfil le proporcionan un mayor control sobre los recorridos en pausa, ya que le permiten definir reglas que quitan automáticamente perfiles específicos antes de que se reanude el recorrido. Puede establecer condiciones de salida basadas en atributos de perfil (como ubicación, estado o preferencias) para garantizar que solo los perfiles relevantes continúen en el recorrido después de reanudarlo.

Por ejemplo, puede [pausar un recorrido](journey-pause.md), agregar una condición de salida para quitar todos los perfiles ubicados en Francia y reanudar el recorrido sabiendo que esos perfiles se excluirán en el siguiente paso de acción. Esta lógica se aplica tanto a los perfiles que ya están en la recorrido como a cualquier perfil nuevo que se califique después de que se reanude la recorrido.

Esta función funciona junto con la funcionalidad Pausa/Reanudar, lo que le ayuda a administrar recorridos de forma más segura y flexible. Minimice la intervención manual, reduzca el riesgo de enviar comunicaciones irrelevantes o no conformes y mantenga la lógica de recorrido alineada con los requisitos comerciales actuales.

Consulte esta sección para aprender a [usar criterios de salida de atributos de perfil en recorridos en pausa](journey-pause.md#journey-pause-sample).

### Mecanismos de protección y limitaciones {#exit-criteria-guardrails}

Las siguientes limitaciones y protecciones se aplican a la capacidad [Criterios de salida de Recorrido](#exit-criteria-desc):

* Los criterios de salida solo se definen en estado de borrador
* Recorrido de coherencia de área de nombres entre eventos y criterios de salida basados en eventos

Se aplican las siguientes limitaciones al usar la capacidad [Criterios de salida basados en atributos de perfil](#profile-exit-criteria):

* **Se aplican criterios de salida en el nivel de acción**\
  Los criterios de salida de &quot;Atributo de perfil&quot; solo se evalúan en pasos de acción. A diferencia de otros tipos de criterios de salida, no se aplican globalmente en todo el recorrido.\
  Si reanuda un recorrido y algunos perfiles cumplen la condición de salida, esos perfiles se excluyen en el siguiente nodo de acción.\
  Los nuevos perfiles que entren en el recorrido después de reanudarlo también se evaluarán y excluirán en su primer nodo de acción, si cumplen la condición.

* **Una regla de salida basada en perfiles por recorrido**\
  Solo puede definir un criterio de salida de &quot;Atributo de perfil&quot; por recorrido. Esta limitación ayuda a mantener la claridad y evita conflictos en la lógica de recorrido.

* **Solo disponible en recorridos pausados**\
  Solo puede agregar o editar los criterios de salida del &quot;Atributo de perfil&quot; cuando el recorrido está en pausa.

   * En un **recorrido de borrador**, la opción *Atributo de perfil* aparece deshabilitada (solo lectura), mientras que las opciones *Evento* y *Audiencia* permanecen activas.
   * En un **recorrido pausado**, la opción *Atributo de perfil* se vuelve editable, y las opciones *Evento* y *Audiencia* se vuelven de solo lectura.

### Temas relacionados {#exit-criteria-related}

* [Guía de criterios de entrada y salida de Recorrido](entry-exit-criteria-guide.md): guía completa con ejemplos reales y prácticas recomendadas
* [Administración de entrada de perfiles](entry-management.md): configure el modo en que los perfiles escriben recorridos
* [Cómo terminan los recorridos](end-journey.md) - Comprender la finalización natural de los recorridos
* [Pausar un recorrido con criterios de salida de atributo de perfil](journey-pause.md#journey-exit-criteria) - Usar criterios de salida al pausar recorridos

## programación de recorrido {#schedule}

La sección **[!UICONTROL Programar]** solo está disponible cuando se ha quitado una actividad **[!UICONTROL Leer audiencia]** en el lienzo. Permite definir una fecha/hora y una frecuencia específicas en las que se debe ejecutar el recorrido. [Aprenda a programar un recorrido de lectura-audiencia](read-audience.md#schedule)

>[!TIP]
>
>Al programar el recorrido, también puede configurar el envío de oleadas para enviar acciones de recorrido por lotes a lo largo del tiempo. [Aprenda a enviar mediante olas en recorridos](send-using-waves.md)


## Administración de conflictos {#conflict}

La sección **[!UICONTROL Administración de conflictos]** de las propiedades del recorrido le permite supervisar los conflictos y priorizar los recorridos. Puede hacer lo siguiente:

* Aplique un **conjunto de reglas** para excluir este recorrido a parte de su audiencia según las reglas de límite. [Descubra cómo trabajar con conjuntos de reglas](../conflict-prioritization/rule-sets.md)

* Asigne una **puntuación de prioridad** al recorrido, de 0 a 100. Un número mayor indica una prioridad mayor. El valor de prioridad insertado aquí lo heredan las acciones entrantes (como in-app) contenidas en este recorrido. [aprenda a trabajar con puntuaciones de prioridad](../conflict-prioritization/priority-scores.md)

  En el caso de situaciones en las que esta misma configuración de canal entrante se utiliza en otras campañas o recorridos, se muestra al destinatario la acción entrante con la puntuación de prioridad más alta. Si varios recorridos o campañas tienen la misma puntuación, se elige el elemento que se modificó más recientemente.

* **Ver conflictos** con otros recorridos, campañas o configuraciones de canal. Si desea identificar la superposición en la audiencia, la fecha de inicio y finalización, la configuración del canal, el canal o el conjunto de reglas, puede ver posibles conflictos aquí. [Aprenda a identificar posibles conflictos en el recorrido](../conflict-prioritization/conflicts.md)

## Preguntas frecuentes {#faq}

**¿Dónde encuentro las propiedades de un recorrido?**

Las propiedades se encuentran en el carril derecho del lienzo de recorrido. Aparecen de forma predeterminada al crear un nuevo recorrido. Para un recorrido existente, haga clic en el icono de lápiz situado junto al nombre del recorrido para abrirlo. Para los recorridos activos, el panel muestra solo la fecha de publicación y el nombre del usuario que publicó el recorrido. Ver [Acceso a las propiedades de un recorrido](#access-properties).

**¿Puedo cambiar las propiedades de un recorrido activo?**

La mayoría de las propiedades son de solo lectura una vez que el recorrido está activo. Para modificarlos, cree una nueva versión del recorrido o duplique el recorrido, realice los cambios en el borrador y [vuelva a publicar](publish-journey.md).

**¿Cuál es la diferencia entre la configuración de reentrada y el período de espera de reentrada?**

**[Permitir la reentrada](#allow-reentrance)** controla si un perfil puede entrar en el recorrido más de una vez. El **[período de espera de reentrada](#reentrance-wait)** (que se muestra solo cuando se permite la reentrada) define cuánto tiempo se debe esperar antes de que el mismo perfil pueda volver a introducir un recorrido unitario. El valor predeterminado es 5 minutos y el máximo es 90 días. Para obtener más información, consulte [Administración de entrada de perfil](entry-management.md).

**¿Cuánto tiempo puede un perfil permanecer en un recorrido?**

Un tiempo de espera de recorrido global de [1} detiene un perfil **91 días** después de que ingresa, ya que el recorrido de un individuo no puede durar más de ese tiempo. ](#global_timeout)Este tiempo de espera no se muestra en la interfaz y no se puede cambiar. Como los datos de perfil se eliminan pasados 91 días, no se puede garantizar el bloqueo de reentrada más allá de ese período. Ver también [Cómo terminan los recorridos](end-journey.md#journey-finished-definition).

**¿Por qué no se puede publicar mi recorrido debido al tamaño de la carga útil?**

El indicador **[!UICONTROL Tamaño de carga útil del recorrido actual]** muestra la carga útil del recorrido con respecto al límite configurado (4 MB de forma predeterminada). Si la carga útil se aproxima o supera el límite, la publicación falla. Reduzca el tamaño simplificando la lógica de recorrido o reduciendo el número de actividades, o póngase en contacto con el Servicio de atención al cliente de Adobe para solicitar un límite superior. Ver [tamaño de carga útil de Recorrido](#journey-payload-size), [validación del tamaño de carga útil de Recorrido](../start/guardrails.md#journey-payload-size) y [protecciones generales de recorrido](../start/guardrails.md#journeys-guardrails-journeys).

**¿Qué política de combinación utiliza mi recorrido?**

Depende del tipo de recorrido: los recorridos [Leer audiencia](read-audience.md) y [Calificación de audiencias](audience-qualification-events.md) utilizan la política de combinación de la audiencia, los recorridos [evento unitario](../event/about-events.md) utilizan la política de combinación predeterminada y los recorridos [evento empresarial](../event/about-creating-business.md) utilizan la política de combinación de la audiencia de destino en la siguiente actividad Leer audiencia. La misma política de combinación se aplica a todo el recorrido. Si se actualiza una política de combinación de audiencias, cualquier recorrido activo que haga referencia a esa audiencia debe volver a publicarse o duplicarse. Consulte [Política de combinación](#merge-policies).

**¿Cuál es la diferencia entre el tiempo de espera de recorrido de 91 días y la ventana de informes de 91 días?**

Son conceptos separados. El tiempo de espera global de **[recorrido](#global_timeout)** (91 días) es el tiempo máximo que un perfil individual puede permanecer activo en un recorrido, después del cual el perfil se cierra y se eliminan sus datos. La **ventana de informes** (aproximadamente 91 días) es un límite de visualización de la interfaz de usuario: los datos de rendimiento anteriores a ~91 días ya no son visibles, pero el recorrido sigue ejecutándose y siguen entrando nuevos perfiles. Para obtener detalles de TTL y retención de datos, consulte las [Preguntas frecuentes sobre tiempo de vida (TTL) y retención de datos](#timeout-faq).

## Temas relacionados {#related-topics}

* [Administración de entrada de perfiles](entry-management.md): configure el modo en que los perfiles escriben y vuelven a introducir recorridos
* [Guía de criterios de entrada y salida de Recorrido](entry-exit-criteria-guide.md): guía completa con ejemplos reales y prácticas recomendadas
* [Cómo terminan los recorridos](end-journey.md): Comprender la finalización natural de recorridos y la salida de perfiles
* [Pausar un recorrido](journey-pause.md): pausar y reanudar recorridos con criterios de salida de atributos de perfil
* [Administración de zonas horarias](timezone-management.md): configure las zonas horarias de recorrido y perfil
* [Administración y priorización de conflictos](../conflict-prioritization/conflicts.md): identifique y resuelva conflictos entre recorridos y campañas

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica cómo configurar y administrar toda la configuración global de un recorrido, incluidas las reglas de entrada, las zonas horarias, las fechas de inicio y finalización, el comportamiento del tiempo de espera, los criterios de salida, el tamaño de la carga útil y la administración de conflictos.

**Intenciones:**

* Configuración de las reglas de entrada y reentrada de recorrido para perfiles
* Establezca las fechas de inicio y finalización para controlar cuándo los perfiles pueden entrar o salir de un recorrido
* Defina criterios de salida para eliminar automáticamente perfiles cuando se cumpla una condición empresarial
* Administrar el acceso a un recorrido mediante las etiquetas de control de acceso de nivel de objeto
* Supervisar el tamaño de la carga útil del recorrido para evitar errores de publicación
* Resolución de conflictos y asignación de puntuaciones de prioridad entre recorridos y campañas

**Glosario:**

* **propiedades de Recorrido**: panel de configuración global (carril derecho) que controla el nombre, las reglas de entrada, la zona horaria, las fechas, el tiempo de espera, el tamaño de carga útil y la administración de conflictos de un recorrido. *(específico del producto)*
* **Período de espera de reentrada**: tiempo mínimo que un perfil debe esperar antes de que se le permita volver a entrar en un recorrido unitario; el máximo es de 90 días. *(específico del producto)*
* **Tiempo de espera de recorrido global (TTL)**: El tiempo máximo que un perfil puede permanecer activo en un recorrido (actualmente, 91 días), después del cual se sale del perfil y se eliminan sus datos. *(específico del producto)*
* **Criterios de salida**: reglas definidas en el nivel de recorrido que quitan automáticamente perfiles de un recorrido cuando se produce un evento especificado o se cumple una condición de audiencia. *(específico del producto)*
* **Criterios de salida basados en atributos de perfil**: Reglas de salida basadas en atributos de perfil (por ejemplo: ubicación o estado) que se evalúan en los pasos de acción y que solo se pueden editar cuando se pausa un recorrido. *(específico del producto)*
* **Política de combinación**: conjunto de reglas utilizado por Adobe Experience Platform para combinar datos de perfil de varios orígenes; aplicadas de forma coherente en todo el recorrido. *(específico del producto)*
* **Administración de conflictos**: herramientas en propiedades de recorrido para asignar puntuaciones de prioridad, aplicar conjuntos de reglas e identificar recorridos o campañas superpuestos. *(específico del producto)*
* **Tamaño de carga útil de Recorrido**: El tamaño actual de la carga útil de definición del recorrido en comparación con el límite configurado; al exceder el límite, se bloquea la publicación. *(específico del producto)*
* **OLAC (Control de acceso de nivel de objeto)**: modelo de permisos que restringe el acceso a recorridos individuales que utilizan etiquetas de uso de datos.

**Protecciones:**

* El período máximo de espera de reentrada es de 90 días
* El tiempo de espera de recorrido global es de 91 días; después de este periodo, los datos de perfil se eliminan y el perfil se cierra
* El límite predeterminado de carga útil de recorrido es de 4 MB; si se supera, se impide la publicación. Póngase en contacto con el Servicio de atención al cliente de Adobe para obtener un límite superior
* Los criterios de salida solo se pueden configurar en estado de borrador (tipos de evento/audiencia); los criterios de salida de atributos de perfil solo se pueden editar cuando el recorrido está en pausa
* Solo se permite una regla de criterios de salida de atributo de perfil por recorrido
* Los criterios de salida de atributos de perfil solo se evalúan en pasos de acción, no de forma global
* Cuando se actualiza una política de combinación de audiencias, cualquier recorrido activo que haga referencia a esa audiencia debe volver a publicarse
* Políticas de combinación incoherentes en una publicación de bloque de recorrido; las incoherencias en la personalización de los mensajes no avisan
* En el caso de los recorridos activos, el panel de propiedades muestra solo la fecha de publicación y el nombre del editor

**Terminología:**

* Nombre canónico: propiedades de Recorrido — Acrónimo: none — variantes: configuración de recorrido, panel de configuración de recorrido
* Sinónimos: &quot;tiempo de espera de recorrido global&quot; = &quot;TTL&quot; = &quot;Tiempo de vida&quot;
* No confunda: &quot;tiempo de espera de recorrido global (91 días)&quot; ≠ &quot;ventana de informes (~91 días)&quot;: el tiempo de espera limita la duración del perfil individual en un recorrido; la ventana de informes es un límite de visualización de la interfaz de usuario para los datos de análisis

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Cuánto tiempo puede un perfil permanecer en un recorrido?** — Un máximo de 91 días (el tiempo de espera de recorrido global); después de este período, el perfil se abandona automáticamente y se eliminan sus datos.
* **Q: ¿Puedo editar las propiedades del recorrido mientras el recorrido está activo?** — En el caso de los recorridos activos, el panel de propiedades muestra únicamente la fecha de publicación y el nombre del editor; los cambios estructurales requieren una nueva versión.
* **Q: ¿Qué sucede cuando se configuran varios criterios de salida?** — Se evalúan de arriba a abajo con la lógica OR en cada paso del recorrido; un perfil existe cuando se cumple un criterio.
* **Q: ¿Cómo evito que un perfil vuelva a entrar en un recorrido?** — Desmarque la opción &quot;Permitir reentrada&quot; en las propiedades del recorrido; esto es adecuado para experiencias únicas, como una oferta de regalo.
* **Q: ¿Cuál es la diferencia entre el tiempo de espera del recorrido y la fecha de finalización?** — La fecha de finalización detiene todas las nuevas entradas y sale automáticamente de los perfiles activos en esa fecha específica; el tiempo de espera global de 91 días se aplica por perfil desde el momento en que ingresa, independientemente de la fecha de finalización del recorrido.
* **Q: ¿Cómo se determina la política de combinación para un recorrido?** — Depende del tipo de recorrido: Leer audiencia y recorridos de calificación de audiencia utilizan la política de combinación de la audiencia; recorridos de eventos unitarios utilizan la política de combinación predeterminada; recorridos de eventos empresariales utilizan la política de combinación de la audiencia de destino en la actividad de lectura de audiencia posterior.

+++
