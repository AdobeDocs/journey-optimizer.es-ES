---
solution: Journey Optimizer
product: journey optimizer
title: Limitaciones y mecanismos de protección de Journey Optimizer
description: Obtenga más información acerca de los mecanismos de protección de Journey Optimizer
feature: Guardrails
role: User
level: Intermediate
mini-toc-levels: 2
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
TQID: https://experienceleague.adobe.com/k4DqGogrTZ9QrnqyFGwdgDeUI9ivpOd1iSI0c5comuU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
subfeature_v2:
  - id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: e588992f914e67f482d6736d55c5a705da8d465f
workflow-type: tm+mt
source-wordcount: 4606
ht-degree: 94%

---


# Mecanismos de protección y limitaciones {#limitations}

>[!BEGINSHADEBOX]

**En esta página:** revise los límites de sistema, recorrido, público, canal y contenido de Adobe Journey Optimizer para que pueda planificar implementaciones que se escalen sin que se produzcan errores.

>[!ENDSHADEBOX]

A continuación encontrará mecanismos de protección y limitaciones adicionales cuando utilice [!DNL Adobe Journey Optimizer].

Los derechos, limitaciones de productos y protección del rendimiento se enumeran en la [página de descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

>[!CAUTION]
>
>* Los [mecanismos de protección de los datos del perfil del cliente en tiempo real](https://experienceleague.adobe.com/es/docs/experience-platform/profile/guardrails){target="_blank"} también se aplican a Adobe Journey Optimizer.
>
>* Consulte también [Mecanismos de protección para la ingesta de datos en el perfil del cliente en tiempo real](https://experienceleague.adobe.com/es/docs/experience-platform/ingestion/guardrails){target="_blank"}


## Sistema y plataforma {#system-platform}

### Navegadores admitidos {#browsers}

La interfaz de Adobe [!DNL Journey Optimizer] está diseñada para funcionar de forma óptima en la última versión de Google Chrome. Es posible que tenga problemas al utilizar determinadas funciones en versiones anteriores u otros navegadores.

### Mecanismos de protección de los conjuntos de datos {#datasets-guardrails}

A partir de febrero de 2025, se implementará gradualmente un mecanismo de protección de tiempo de vida (TTL) en los conjuntos de datos generados por el sistema de Journey Optimizer en las **nuevas zonas protegidas y organizaciones** de la siguiente manera:

* **90 días** para los datos en el almacén de perfiles
* **13 meses** para los datos en el lago de datos

Este cambio se implementará en las **zonas protegidas de clientes existentes** en una fase posterior. [Obtenga más información sobre los mecanismos de protección de tiempo de vida (Time-To-Live, TTL) de los conjuntos de datos](../data/datasets-ttl.md)

## Recorridos {#journeys-guardrails}

Esta sección trata de las protecciones y limitaciones de los recorridos, incluidas las limitaciones generales de recorrido, los componentes de recorrido (acciones, eventos, fuentes de datos), las actividades de recorrido y las funciones específicas como las acciones personalizadas y el editor de expresiones.

### Protecciones generales del recorrido {#journeys-guardrails-journeys}

* El número de actividades en un recorrido ahora está limitado a **50**. El número de actividades se muestra en la sección superior izquierda del lienzo de recorrido.

  A medida que los recorridos se acercan a este límite, el rendimiento de la edición y la de publicación puede degradarse y pueden producirse errores al guardar o validar. Si esto sucede, divida el recorrido en subrecorridos más pequeños mediante [actividades de salto](../building-journeys/jump.md) o vuelva a crearlo en una nueva versión. El límite de la actividad no se puede aumentar.

* El número de recorridos activos, cerrados, pausados y de ejecución en seco que pueden estar activos al mismo tiempo se limita a **200** en zonas protegidas de producción y a **100** en zonas protegidas de desarrollo. Este límite se aplica cuando publica un recorrido. El número actual de recorridos se muestra encima del lienzo del recorrido.

  A medida que publica recorridos, los ampliamos y ajustamos automáticamente para garantizar el máximo rendimiento y estabilidad. Los recorridos cerrados se cuentan únicamente si se crean después de desplegar esta protección.

>[!NOTE]
>
>Para las protecciones de tiempo de publicación, las organizaciones que ya exceden un límite cuando se introduce la protección reciben una excepción. Los recorridos existentes no se ven afectados.

* Cuando se utiliza una calificación de público en un recorrido, esa actividad de calificación de público puede tardar hasta **10 minutos** en estar activa y en escuchar los perfiles que entran o salen del público.

* Una instancia de recorrido de un perfil tiene un tamaño máximo de **1 MB**. Todos los datos recopilados como parte de la ejecución del recorrido se almacenan en esa instancia de recorrido. Por lo tanto, los datos de un evento entrante, la información de perfil recuperada de Adobe Experience Platform, las respuestas de acciones personalizadas, etc. se almacenan en esa instancia de recorrido y afectan al tamaño del recorrido. Se recomienda, cuando un recorrido comienza con un evento, limitar el tamaño máximo de esa carga útil de evento (p. ej., por debajo de **800 KB**) para evitar alcanzar ese límite después de unas pocas actividades, en la ejecución del recorrido. Cuando se alcanza ese límite, el perfil está en estado de error y se excluirá del recorrido.

* Para cada perfil y versión de recorrido, el tiempo de ejecución del recorrido mantiene una cola interna de hasta **10 eventos pendientes** mientras se procesa uno. Si se alcanza este límite, los eventos adicionales se descartan con el motivo `maxInstanceStackEventsReached` hasta que se agote la pila. Consulte [Eventos descartados debido a una instancia de recorrido bloqueada](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached).

* Además del tiempo de espera utilizado en las actividades del recorrido, también hay un tiempo de espera de recorrido global que no se muestra en la interfaz y no se puede cambiar. Este tiempo de espera global detiene el progreso de los particulares en el recorrido **91 días** después de su entrada. [Más información](../building-journeys/journey-properties.md#global_timeout)

>[!TIP]
>
>**Lo que esto significa para usted:** El **límite de 50 actividades** y el **límite de recorridos activos** son las dos barreras que la mayoría de los equipos encuentran primero al escalar. Planifique la división anticipada del recorrido y extienda las horas de inicio de la lectura del público con una diferencia mínima de entre 5 y 10 minutos para evitar la contención del rendimiento de la zona protegida.

#### Validación del tamaño de la carga útil del recorrido {#journey-payload-size}

Al guardar o publicar un recorrido, Journey Optimizer valida el tamaño total de la carga útil del recorrido para conservar la estabilidad y el rendimiento.

| Situación | Umbral | Comportamiento |
|---|---|---|
| Carga útil &lt; 90 % del límite | Advertencia a continuación | El recorrido se guarda y se publica correctamente. No se muestran advertencias ni errores. |
| Carga útil entre el 90 y el 99 % del límite | Advertencia (leve) | El recorrido se guarda y se publica con una advertencia: **Advertencia**: el tamaño de la carga útil del recorrido está cerca del límite. Nodo más grande: &#39;[NodeName]&#39; (tipo: &#39;[NodeType]&#39;, tamaño: [N] bytes). |
| Carga útil ≥ el 100 % del límite | **Error (crítico)** | Guardar o publicar está bloqueado. Devuelve **HTTP 413 Request Entity Too Large**. Error: el tamaño de la carga útil del recorrido supera el límite. Nodo más grande: &#39;[NodeName]&#39; (tipo: &#39;[NodeType]&#39;, tamaño: [N] bytes). |

**Configuración predeterminada**

* **Tamaño máximo de solicitud predeterminado**: **2 MB** (2.000.000 bytes). Algunas organizaciones pueden tener límites personalizados configurados por Adobe.
* **Umbral de advertencia**: 90% del límite máximo.
* **Umbral de error**: 100% del límite máximo.

**Resolución de problemas y recomendaciones**

* Revise el nodo más grande resaltado en la advertencia o el error.
* Simplifique las condiciones, reduzca las asignaciones de datos y elimine pasos o parámetros innecesarios.
* Considere la posibilidad de dividir el recorrido en recorridos más pequeños si es necesario.
* Si cree que su organización necesita un límite más alto, póngase en contacto con su representante de Adobe.

Para monitorizar el tamaño de la carga útil actual del recorrido antes de publicarlo, utilice el indicador **[!UICONTROL Tamaño de carga útil del recorrido actual]** en el panel de propiedades del recorrido. [Aprenda a comprobar el tamaño de la carga útil de su recorrido](../building-journeys/journey-properties.md#journey-payload-size)

### Comparación de paquetes de licencias {#select-package-limitations}

>[!NOTE]
>
>La limitación del paquete Select a continuación no se aplica a los recorridos Leer público o Evento empresarial. Si necesita una lógica de recorrido más compleja con varias acciones, condiciones o actividades de espera, considere la posibilidad de actualizar el paquete de licencias o utilizar recorridos de Leer público cuando corresponda.

Para los clientes que usan el paquete de licencia **Select**, las siguientes limitaciones adicionales se aplican específicamente a recorridos unitarios (recorridos que comienzan con un evento o una calificación de público):

| Limitación | Código de error | Descripción |
|---|---|---|
| Solo se permite una acción | `ERR_PKG_SELECT_8` | Los recorridos unitarios solo pueden contener **una** actividad de acción. No se permiten varias actividades de correo electrónico, push, SMS u otras acciones dentro del mismo recorrido. |
| No se permiten ninguna condición | `ERR_PKG_SELECT_7` | Las actividades de condición no se pueden utilizar en recorridos unitarios. El recorrido debe seguir una única ruta lineal sin lógica de ramificación. |
| No hay actividades de espera | `ERR_PKG_SELECT_6` | No se pueden añadir actividades de espera a recorridos unitarios. Las acciones deben ejecutarse inmediatamente sin retrasos. |
| Las transiciones de tiempo de espera/error deben ir al nodo final | `ERR_PKG_SELECT_2` | Si configura transiciones de tiempo de espera o error para una acción (p. ej., una acción de correo electrónico), estas rutas deben apuntar directamente a un nodo final. No pueden conectarse a otras actividades o acciones del recorrido. |

>[!TIP]
>
>**Lo que esto significa para usted:** si se encuentra en el paquete Select y necesita lógica de ramificación, actividades de espera o varias acciones, debe usar un recorrido público de lectura o ponerse en contacto con su representante de Adobe para actualizar el paquete.

### Versiones de recorridos {#journey-versions-g}

Las siguientes limitaciones se aplican a las [versiones del recorrido](../start/user-interface.md):

* Un recorrido que se inicia con una actividad de evento en v1 no puede comenzar con otra cosa que un evento en versiones posteriores. No puede iniciar un recorrido con un evento de **Calificación de público**.
* Un recorrido que se inicia con una actividad de **Calificación de público** en la versión 1 siempre debe comenzar con una **Calificación de público** en versiones posteriores.
* El público y el espacio de nombres elegidos en la **Calificación de públicos** (primer nodo) no se pueden cambiar en las versiones nuevas.
* La regla de reentrada debe ser la misma en todas las versiones del recorrido.
* El recorrido que comience con **Leer público** no puede comenzar con otro evento en las versiones siguientes.
* No se puede crear una nueva versión de un recorrido de lectura de público con lectura incremental. Debe duplicar el recorrido.

### Creación de recorridos y perfiles {#journeys-limitation-profile-creation}

Hay un retraso asociado a la creación/actualización de perfiles basados en la API en Adobe Experience Platform. El objetivo a nivel de servicio (SLT) en términos de latencia es &lt; 1 min desde la ingesta hasta el perfil unificado para el percentil 95 de las solicitudes, a un volumen de **20 000 solicitudes por segundo (RPS)**.

Si un recorrido se activa simultáneamente para crear un perfil y comprueba o recupera inmediatamente la información del servicio de perfil, es posible que no funcione de forma correcta.

Puede elegir entre una de estas dos soluciones:

* Agregue una actividad de espera después del primer evento para que Adobe Experience Platform tenga el tiempo necesario para realizar la ingesta en el servicio de perfil.

* Configure un recorrido que no utilice inmediatamente el perfil. Por ejemplo, si el recorrido está diseñado para confirmar la creación de una cuenta, el evento de experiencia podría contener la información necesaria para enviar el primer mensaje de confirmación (nombre, apellidos, dirección de correo electrónico, etc.).

### Eventos {#events-g}

Las siguientes limitaciones se aplican a los [Eventos](../event/about-events.md) en sus recorridos:

* Journey Optimizer admite un volumen máximo de **5.000 eventos de recorrido entrantes por segundo** para eventos unitarios y **5.000 eventos de recorrido entrantes por segundo** para eventos de recorrido basados en Audiencias de lectura en todas las zonas protegidas. Obtenga más información acerca de esta limitación [en esta página](../event/about-events.md#event-thoughput).
* Los recorridos activados por eventos pueden tardar hasta **5 minutos** en procesar la primera acción del recorrido.
* En el caso de los eventos generados por el sistema, los datos de streaming utilizados para iniciar un recorrido del cliente deben configurarse primero en Journey Optimizer para obtener un ID de orquestación único. Este ID de orquestación debe añadirse a la carga útil de streaming que llega a Adobe Experience Platform. Esta limitación no se aplica a los eventos basados en reglas.
* Los eventos empresariales no se pueden usar junto con eventos unitarios o actividades de calificación de público.
* Se puede hacer referencia a un solo evento en un máximo de **25** recorridos al mismo tiempo. Cuando se alcanza este límite, se bloquea la publicación de cualquier recorrido adicional que utilice ese evento.
* Se puede hacer referencia a un único esquema XDM mediante un máximo de **100** eventos en todos los recorridos activos y cerrados a la vez. Cuando se alcanza este límite, se bloquea la publicación de cualquier recorrido con un nodo de evento que haga referencia a ese esquema.
* Los recorridos unitarios (que se inician con un evento o una calificación de público) incluyen un mecanismo de protección que evita que los recorridos se activen varias veces de forma errónea para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante **5 minutos**. Por ejemplo, si un evento activa un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.
* Journey Optimizer requiere que los eventos se transmitan al servicio principal de recopilación de datos (DCCS) para poder activar un recorrido. Los eventos importados por lotes, los eventos insertados a través de **Query Service** o los eventos procedentes de conjuntos de datos internos de Journey Optimizer (comentarios sobre mensajes, seguimiento de correos electrónicos, etc.) no se puede usar para activar un recorrido. Para los casos de uso en los que no pueda obtener los eventos transmitidos, genere un público basado en dichos eventos y utilice la actividad **Público de lectura** en su lugar. Técnicamente, la calificación del público puede utilizarse, pero no se recomienda porque puede provocar problemas posteriores en función de las acciones utilizadas.

### Fuentes de datos {#data-sources-g}

Las siguientes limitaciones se aplican a las [Fuentes de datos](../datasource/about-data-sources.md) en sus recorridos:

* Las fuentes de datos externas se pueden aprovechar dentro de un recorrido del cliente para buscar datos externos en tiempo real. Estas fuentes deben utilizarse mediante la API de REST, admiten JSON y pueden gestionar el volumen de solicitudes.
* Las direcciones de Adobe internas (`.adobe.*`) no están permitidas en las direcciones URL y las API.

>[!NOTE]
>
>Como las respuestas ahora son compatibles, debe utilizar acciones personalizadas en lugar de fuentes de datos para casos de uso de fuentes de datos externas.

### Acciones generales {#general-actions-g}

Las siguientes limitaciones se aplican a las [Acciones](../building-journeys/about-journey-activities.md) en sus recorridos:

* En caso de error, se realizan tres reintentos de forma sistemática. No puede ajustar el número de reintentos según el mensaje de error recibido. Los reintentos se realizan para todos los errores HTTP excepto para HTTP 401, 403 y 404.
* El evento **Reacción** integrado le permite reaccionar a las acciones predeterminadas. Obtenga más información en [esta página](../building-journeys/reaction-events.md). Si desea reaccionar a un mensaje enviado mediante una acción personalizada, debe configurar un evento dedicado.
* No puede colocar dos acciones en paralelo, debe agregarlas una tras otra.
* Un perfil no puede estar presente varias veces en el mismo recorrido, al mismo tiempo, para todas las [versiones activas del recorrido](../building-journeys/publish-journey.md#journey-create-new-version). Si la reentrada está habilitada, un perfil puede volver a entrar en un recorrido, pero no puede hacerlo hasta que salga por completo de la instancia anterior del recorrido. [Más información](../building-journeys/end-journey.md)

### Acciones personalizadas {#custom-actions-g}

Las siguientes limitaciones se aplican a las [Acciones personalizadas](../action/action.md) en sus recorridos:

* Se define un límite de **300 000 llamadas durante un minuto** para todas las acciones personalizadas, por host y por zona protegida. Este límite se aplica como una ventana deslizante por zona protegida y por punto final para puntos finales con tiempos de respuesta inferiores a 0,75 segundos. Para los puntos finales con tiempos de respuesta superiores a 0,75 segundos, se aplica un límite independiente de **150 000 llamadas cada 30 segundos** (también una ventana deslizante).
* La URL de acción personalizada no admite parámetros dinámicos.
* Se admiten los métodos de llamada POST, PUT y GET.
* El nombre del parámetro de consulta o del encabezado no debe comenzar con &quot;.&quot; o “$”.
* Las direcciones IP no están permitidas en las URL. En su lugar, utilice nombres de host.
* Las direcciones de Adobe internas (`.adobe.*`) no están permitidas en las direcciones URL y las API.
* Las acciones personalizadas integradas no se pueden eliminar.
* Las acciones personalizadas solo admiten el formato JSON cuando se utilizan cargas útiles de solicitud o respuesta. Consulte [esta página](../action/about-custom-action-configuration.md#custom-actions-limitations).
* Cualquier punto final segmentado por una acción personalizada debe admitir al menos 200 TPS **&#x200B;**. Tenga cuidado ya que una configuración de limitación no puede estar por debajo de 200 TPS. Según el rendimiento esperado, tener un tiempo de respuesta alto podría afectar al rendimiento real.

>[!TIP]
>
>**Lo que esto significa para usted:** el límite predeterminado de 300 000 llamadas/min protege sus puntos finales externos de verse desbordados por el rendimiento del recorrido. Si el punto final puede gestionar más carga, puede aumentar este límite con la [API de límite](../configuration/capping.md) o la [API de restricción](../configuration/throttling.md). Para obtener una información general más amplia de cómo se conecta Journey Optimizer a sistemas externos, consulte [esta página](../configuration/external-systems.md). Póngase en contacto con su representante de Adobe si necesita un límite organizativo más alto.

### Identificadores adicionales {#supplemental}

Se aplican mecanismos de protección específicos al uso de identificadores suplementarios en los recorridos. Se muestran [en esta página](../building-journeys/supplemental-identifier.md#guardrails).

### Editor de expresiones {#expression-editor}

Los siguientes mecanismos de protección se aplican al [editor de expresiones de recorrido](../building-journeys/expression/expressionadvanced.md):

* Los grupos de campos de eventos de experiencia no se pueden utilizar en recorridos que comiencen con Leer público, Calificación de público o una actividad de evento empresarial. Debe crear un público nuevo y utilizar una condición `inaudience` en el recorrido.
* Los atributos `timeSeriesEvents` no se pueden usar en el editor de expresiones. Para acceder a los eventos de experiencia a nivel de perfil, cree un nuevo grupo de campos basado en un esquema `XDM ExperienceEvent`.

### Actividades de recorrido {#activities}

#### Actividad de calificación de público {#audience-qualif-g}

Las siguientes limitaciones se aplican a la actividad de recorrido [Calificación de audiencias](../building-journeys/audience-qualification-events.md):

* La actividad de calificación de público no se puede utilizar con actividades de Adobe Campaign.
* No se admiten identificadores suplementarios para los recorridos de calificación de público.
* Una zona protegida puede incluir un máximo de **300** nodos de calificación de audiencia en todos los recorridos activos y cerrados. Cuando se alcanza este límite, se bloquean las recorridos de publicación con nodos de calificación de audiencia adicionales.

Obtenga más información acerca de las tasas de procesamiento de recorrido y los límites de rendimiento en [esta sección](../building-journeys/entry-management.md#journey-processing-rate).

En [esta página](../building-journeys/audience-qualification-events.md#audience-qualification-guardrails) se enumeran protecciones adicionales, incluidas recomendaciones sobre públicos de streaming frente a públicos por lotes y limitaciones de público de composición.

#### Actividades de campaña {#ac-g}

Los siguientes mecanismos de protección se aplican a las actividades **[!UICONTROL Campaign v7/v8]** y **[!UICONTROL Campaign Standard]**:

* Las actividades de Adobe Campaign no se pueden utilizar con un público de lectura o una actividad de calificación de público.
* Las actividades de **[!UICONTROL Campaign Standard]** no se pueden utilizar con las actividades de otros canales: tarjeta, experiencia basada en código, correo electrónico, push, SMS, mensajes en la aplicación, web.
* Las actividades de **[!UICONTROL las versiones 7 y 8 de Campaign]** se pueden usar junto con las actividades de canal nativo en el mismo recorrido.

#### Eventos de reacción {#reaction-events-g}

Se aplican mecanismos de protección específicos a los eventos de **[!UICONTROL Reacción]**, incluido el requisito de colocar la actividad inmediatamente después de una acción del canal y la incapacidad de rastrear los mensajes enviados en un recorrido diferente. Se muestran en [esta página](../building-journeys/reaction-events.md#guardrails-limitations).

#### Actividad en la aplicación {#in-app-activity-limitations}

Las siguientes limitaciones se aplican a la acción **[!UICONTROL Mensaje en la aplicación]**. Obtenga más información sobre los mensajes in-app en [esta página](../in-app/create-in-app.md).

* Actualmente, esta función no está disponible para los clientes de Asistencia sanitaria.

* La personalización solo puede contener atributos de perfil.

* La actividad en la aplicación no se puede utilizar con actividades de **[!UICONTROL Campaign Standard]**.

* La visualización en la aplicación está ligada a la duración del recorrido, lo que significa que cuando el recorrido termina para un perfil, todos los mensajes en la aplicación dentro de ese recorrido dejan de mostrarse para ese perfil. Por lo tanto, no es posible detener un mensaje en la aplicación directamente desde una actividad de recorrido. En su lugar, deberá finalizar todo el recorrido para que los mensajes en la aplicación no se muestren en el perfil.

* En el modo de prueba, la visualización en la aplicación depende de la duración del recorrido. Para evitar que el recorrido termine demasiado pronto durante la prueba, ajuste el valor **[!UICONTROL Tiempo de espera]** para sus actividades de **[!UICONTROL Espera]**.

* Las actividades de **[!UICONTROL Reacción]** no se pueden utilizar para reaccionar ante una apertura o un clic en la aplicación.

* Puede producirse un retraso de activación entre el momento en que un perfil de usuario alcanza una actividad en la aplicación en el lienzo y la hora en que comienza a ver ese mensaje en la aplicación.

* El tamaño del contenido del mensaje en la aplicación está limitado a **2 MB**. La inclusión de imágenes grandes puede dificultar el proceso de publicación.

#### Actividad de decisión de contenido {#content-decision-g}

Se aplican mecanismos de protección específicos a la actividad **[!UICONTROL Decisión de contenido]**, incluido un retraso de 48 horas antes de que las políticas de consentimiento actualizadas entren en vigor en las directivas de decisión. Se muestran en [esta página](../building-journeys/content-decision.md#guardrails).

#### Actividad de salto {#jump-g}

Especifique protecciones específicas de la actividad **[!UICONTROL Saltar]**. Se muestran en [esta página](../building-journeys/jump.md#jump-limitations).

#### Actividad Leer público {#read-segment-g}

Las siguientes limitaciones se aplican a la actividad de recorrido [Público de lectura](../building-journeys/read-audience.md):

* Los públicos transmitidos siempre están actualizados, pero los públicos por lotes no se calcularán en el momento de la recuperación. Solo se evalúan cada día a la hora de evaluar el lote.
* En la entrada de recorrido, los perfiles utilizan valores de atributo de la instantánea de público por lotes. Sin embargo, cuando un perfil alcanza una actividad de **Espera**, el recorrido actualiza automáticamente los atributos del perfil al recuperar los datos más recientes del Servicio de perfil unificado (UPS). Esto significa que los atributos de perfil pueden cambiar durante la ejecución del recorrido.
* La actividad **Leer público** no se puede utilizar con actividades de Adobe Campaign.
* La actividad **Leer público** solo puede utilizarse como primera actividad en un recorrido o después de una actividad de evento empresarial.
* Un recorrido solo puede tener una actividad **Leer público**.
* La actividad **Leer público** solo puede dirigirse a un público por recorrido. Si se requieren varios públicos, combínelos primero en uno solo. [Aprenda a combinar públicos mediante flujos de trabajo de composición](../audience/get-started-audience-orchestration.md).
* Cada organización puede ejecutar hasta **cinco** instancias **Público de lectura** simultáneamente (programadas o activadas por evento empresarial) en todas las zonas protegidas y recorridos. Evite tener más de cinco recorridos con **Leer audiencia** que comiencen al mismo tiempo; sepárelos con una diferencia de 5 a 10 minutos. Obtenga más información sobre las tasas de procesamiento de recorridos en [esta sección](../building-journeys/entry-management.md#journey-processing-rate).
* Rendimiento de la zona protegida: el sistema administra el procesamiento por zona protegida con un máximo de **20 000 perfiles por segundo** compartidos en todas las actividades de **Público de lectura**. Las actividades individuales se pueden configurar de **500 a 20 000 perfiles por segundo**. Si se alcanzan los límites de la zona protegida, los trabajos pueden ponerse en cola.
* Tiempo de espera de procesamiento de trabajo: trabajos de **Público de lectura** que no se pueden procesar en un plazo de **12 horas** se limpian automáticamente y no se ejecutarán.
* Los reintentos ahora se aplican de forma predeterminada en recorridos activados por públicos cuando se recupera el trabajo de exportación. Si se produce un error durante la creación del trabajo de exportación, se realizarán reintentos cada 10 minutos, hasta un máximo de **1 hora**. Después, el recorrido se considera fallido y, por lo tanto, se puede ejecutar hasta 1 hora después de la hora programada.
* En el caso de los recorridos que utilizan ID suplementarios, la tasa de la actividad **Públicos de lectura** para cada instancia de recorrido está limitada a un máximo de **500 perfiles por segundo**.

>[!TIP]
>
>**Lo que esto significa para usted:** el límite de 5 instancias simultáneas es un tope fijo para toda la organización. Si varios equipos programan recorridos de Público de lectura, coordine las horas de inicio con cuidado. Los trabajos que no cumplen la ventana de procesamiento de 12 horas se descartan de forma silenciosa; confirme siempre la ejecución correcta en los registros del recorrido.

Consulte también [recomendaciones y configuración](../building-journeys/read-audience.md#must-read) para la actividad Leer audiencia.

#### Actualizar actividad de perfil {#update-profile-g}

Se aplican mecanismos de protección específicos a la actividad **[!UICONTROL Actualizar perfil]**. Se muestran en [esta página](../building-journeys/update-profiles.md).

#### Pausa del recorrido {#pause-g}

Se aplican mecanismos de protección específicos a **recorridos en pausa**, incluida una duración máxima de pausa de **14 días** y un límite de perfil de **10 millones** en todos los recorridos en pausa de su organización. Se muestran en [esta página](../building-journeys/journey-pause.md#journey-pause-guardrails).

#### Ensayo del recorrido {#dry-run-g}

Se aplican mecanismos de protección específicos a **Ensayo de recorrido**, incluyendo el recuento hacia un perfil atractivo y cuotas de recorrido en vivo. Se muestran en [esta página](../building-journeys/journey-dry-run.md#journey-dry-run-limitations).

#### Fragmentos del recorrido {#fragments-journey-g}

Se aplican mecanismos de protección específicos a **Fragmentos de Recorrido**, incluidos un máximo de **20 nodos por fragmento** y **200 fragmentos activos por zona protegida**. Se muestran en [esta página](../building-journeys/journey-fragments.md#guardrails).

#### Envío mediante olas {#waves-g}

Existen mecanismos de protección específicos para **el envío de olas en recorridos**, que incluyen un intervalo de ondas de 2 a 10 y un **intervalo mínimo de 30 minutos** entre olas. Se muestran en [esta página](../building-journeys/send-using-waves.md#limitations-guardrails).

#### Simulación de recorrido {#simulation-g}

Se aplican mecanismos de protección específicos a la **simulación del recorrido**. Se muestran en [esta página](../building-journeys/simulate-journey.md#limitations).

## Públicos y perfiles {#audiences-profiles}

Esta sección abarca los aspectos relativos a la gestión de públicos, el manejo de perfiles y las consideraciones sobre los perfiles atractivos.

### Mecanismos de protección de público y perfil {#audience}

* Puede publicar hasta **10 composiciones de público** en una zona protegida determinada. Si ha alcanzado este umbral, debe eliminar una composición para liberar espacio y publicar una nueva.

  Más información sobre la composición de públicos en [esta página](../audience/get-started-audience-orchestration.md).

* Al introducir datos, los correos electrónicos distinguen entre mayúsculas y minúsculas. Significa que se pueden crear perfiles duplicados (por ejemplo, un perfil para Juan.Greene@luma.com y otro perfil para juan.greene@luma.com) y utilizarse al segmentar el destinatario correspondiente en sus recorridos y campañas de [!DNL Journey Optimizer].

* Cuando se dirija a perfiles seudónimos (visitantes no autenticados) con canales de entrada, considere la posibilidad de establecer un tiempo de vida (TTL) para la eliminación automática de perfiles a fin de administrar el recuento de perfiles atractivos y los costes asociados. [Más información](#profile-management-inbound)

## Canales y mensajería {#channel-guardrails}

Esta sección cubre las protecciones para todos los canales de comunicación, incluidos el correo electrónico, los SMS, los canales entrantes (web, en la aplicación, basados en código, tarjetas de contenido) y los mensajes transaccionales.

>[!NOTE]
>
>En circunstancias excepcionales, las interrupciones temporales en una región específica pueden provocar que se excluyan perfiles válidos de los recorridos o que los correos electrónicos se marquen incorrectamente como rechazos. Una vez restaurados los servicios, vuelva a comprobar los registros del recorrido, compruebe los campos de perfil de consentimiento y vuelva a publicar el recorrido si fuera necesario. En caso de una interrupción de ISP, aprenda a quitar perfiles de la lista de supresión en [esta sección](../configuration/manage-suppression-list.md#remove-from-suppression-list).

### Protecciones de correo electrónico {#message-guardrails}

Las siguientes limitaciones se aplican a la actividad [canal de correo electrónico](../email/get-started-email.md):

* No puede utilizar el mismo dominio de envío para enviar mensajes de correo electrónico desde [!DNL Adobe Journey Optimizer] y desde otro producto, como [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage], por ejemplo.

Al diseñar mensajes de correo electrónico, el sistema comprueba la configuración de las claves y muestra alertas para detectar advertencias (recomendaciones y prácticas recomendadas) y errores (problemas de bloqueo que impiden realizar pruebas o activaciones). Obtenga más información acerca de las alertas de correo electrónico y los requisitos de validación en [esta sección](../email/create-email.md#check-email-alerts).

#### Tamaño del contenido del mensaje para la publicación de recorrido {#message-content-size}

Al publicar recorridos que contienen mensajes de correo electrónico, el tamaño total del contenido del mensaje no debe superar los **2 MB** después del procesamiento del back-end. Durante la publicación, el sistema procesa automáticamente el contenido del mensaje aplicando parches a los vínculos e imágenes y aplicando transformaciones, lo que aumenta el tamaño de la carga útil por encima del tamaño del contenido creado.

>[!CAUTION]
>
>Si el contenido final del mensaje procesado supera los **2 MB**, fallará la publicación del recorrido. Mantenga el contenido del mensaje creado por debajo de 2 MB (preferiblemente por debajo de **1 MB**) para disponer de un margen de entre 300 y 400 KB para la sobrecarga de procesamiento en el back-end.

**Prácticas recomendadas para evitar errores de publicación:**

* Mantener el contenido del correo electrónico creado por debajo de **1 MB**
* Minimizar el número de variantes de contenido
* Optimizar y comprimir imágenes antes de añadirlas a los mensajes
* Eliminar recursos no utilizados y elementos de HTML innecesarios
* Compruebe el tamaño del mensaje antes de publicar recorridos en producción

Si la publicación del recorrido falla debido al tamaño del contenido, reduzca el contenido del mensaje y vuelva a publicar el recorrido.

### Mecanismos de protección de SMS {#sms-guardrails}

Las siguientes limitaciones se aplican a la actividad [canal de SMS](../mobile/get-started-mobile.md):

* Los archivos multimedia para MMS se pueden incluir a través de una dirección URL compatible. Asegúrese de que el archivo multimedia se cargue por separado.
* Actualmente, la sincronización de comentarios de mensajes no está disponible para MMS.
* La administración de consentimientos funciona en el nivel de canal SMS para MMS.

### Mecanismos de protección de canal de entrada {#inbound-guardrails}

* Para utilizar las acciones de [experiencia basada en código](../code-based/get-started-code-based.md) en [!DNL Journey Optimizer] y entregar carga útil de contenido de código que pueda ser utilizada por sus aplicaciones, siga los requisitos previos detallados en [esta página](../code-based/code-based-prerequisites.md).

* Para poder obtener acceso a [páginas web](../web/get-started-web.md) y crearlas en la interfaz de usuario de [!DNL Journey Optimizer], siga los requisitos previos enumerados en [esta página](../web/web-prerequisites.md).

* Para enviar mensajes en la aplicación en sus recorridos y campañas con [!DNL Journey Optimizer], siga los requisitos previos de envío que se enumeran en [esta página](../in-app/inapp-configuration.md).

* Para que Adobe Journey Optimizer muestre correctamente las tarjetas de contenido, debe establecer la configuración de Adobe Experience Platform que aparece en [esta página](../content-card/content-card-configuration-prereq.md).

* Journey Optimizer admite un volumen máximo de **5000 eventos de recorrido entrantes por segundo**. Este mecanismo de protección se aplica a todas las solicitudes entrantes, que pueden proceder de cualquiera de los canales entrantes admitidos por Journey Optimizer ([web](../web/get-started-web.md), [en la aplicación](../in-app/get-started-in-app.md), [experiencias basadas en código](../code-based/get-started-code-based.md), [tarjetas de contenido](../../rp_landing_pages/content-card-landing-page.md)).

* Journey Optimizer admite un máximo de **500 acciones entrantes activas** en cualquier momento. Estas acciones de entrada se cuentan si forman parte de una campaña activa o si son un nodo usado en un recorrido activo. Una vez alcanzado este número, debe desactivar las campañas o recorridos más antiguos que utilicen acciones entrantes antes de poder iniciar nuevas.

#### Administración de perfiles con canales de entrada {#profile-management-inbound}

Los canales de entrada de [!DNL Journey Optimizer] se pueden dirigir a perfiles seudónimos, es decir, perfiles que no se han autenticado o que aún no se conocen porque no se han utilizado anteriormente en otros canales. Este es el caso, por ejemplo, al dirigirse a todos los visitantes o públicos en función de ID temporales como ECID.

Esto aumenta el recuento total de perfiles interesados, lo que puede tener implicaciones de costes si se supera el número contractual de perfiles interesados que ha adquirido. Las métricas de licencia de cada paquete se enumeran en la página [Descripción del producto de Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Puede comprobar el número de perfiles interesados en el [panel de control de uso de licencias](../audience/license-usage.md).

Para mantener los perfiles interesados dentro de límites razonables, Adobe recomienda establecer un período de vida (TTL, Time-To-Live) para eliminar automáticamente los perfiles seudónimos del perfil del cliente en tiempo real si no se han visto ni han interactuado en un intervalo de tiempo específico. Adobe recomienda establecer el valor TTL en **14 días** para que coincida con el TTL del perfil de Edge actual.

>[!NOTE]
>
>Aprenda a configurar la caducidad de los datos de los perfiles seudónimos en la [documentación de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}.

### Mecanismos de protección de mensajes transaccionales {#transactional-message-guardrails}

Journey Optimizer admite un volumen máximo de **500 mensajes transaccionales por segundo** en las campañas.

## Contenido y recursos {#content-assets}

Esta sección trata de las reglas para la creación y administración de contenido, incluidas las páginas de destino, subdominios y fragmentos.

### Mecanismos de protección del asistente de IA {#ai-assistant-g}

Los mecanismos de protección y las limitaciones para la **generación de contenido del Asistente de IA**, incluidos los canales admitidos (correo electrónico, push, web, SMS) y las limitaciones del editor de personalización, se enumeran en [esta página](../content-management/gs-generative.md#generative-guardrails).

### Mecanismos de protección de las páginas de destino {#lp-guardrails}

Las siguientes limitaciones se aplican a las [páginas de destino](../landing-pages/get-started-lp.md):

* Solo se puede utilizar un componente **Formulario** en una sola página principal.
* El componente **Formulario** no se puede usar en subpáginas.
* No puede agregar un preencabezado a una página de destino.
* No puede seleccionar la opción **Programar usted mismo** al diseñar una página de aterrizaje principal.

### Protecciones de subdominios {#subdomain-guardrails}

Las protecciones y limitaciones aplicables a la delegación de subdominios en Journey Optimizer se detallan en [esta página](../configuration/delegate-subdomain.md#guardrails).

### Protecciones de fragmentos {#fragments-guardrails}

Las siguientes limitaciones se aplican a los [fragmentos](../content-management/fragments.md):

* Para crear, editar, archivar y publicar fragmentos, necesita los permisos **[!DNL Manage library items]** y **[Publicar fragmento]** incluidos en el perfil de producto **[!DNL Content Library Manager]**. [Más información](../administration/ootb-product-profiles.md#content-library-manager)
* Los fragmentos visuales solo están disponibles para el canal de correo electrónico.
* Los fragmentos de expresiones no están disponibles para el canal en la aplicación.
* Los fragmentos visuales no pueden superar los **100 KB**. Los fragmentos de expresión no pueden superar los **200 KB**.
* Para utilizar un fragmento de un recorrido o una campaña, debe tener el estado **Activo**.
* No se admiten [atributos contextuales](../personalization/personalization-build-expressions.md) en los fragmentos.
* Los fragmentos visuales no son compatibles entre los modos Usar temas y Estilo manual. Para poder utilizar un fragmento en un contenido en el que desee aplicar una temática, este fragmento debe crearse en el modo Usar temas. [Más información sobre los temas](../email/apply-email-themes.md)
* Cuando el seguimiento está habilitado en un recorrido o una campaña, si agrega vínculos a un fragmento y este se utiliza en un mensaje, se realiza el seguimiento de estos vínculos, al igual que todos los demás incluidos en el mensaje. [Más información sobre vínculos y seguimiento](../email/message-tracking.md)

## Gestión de decisiones {#decision-management}

### Mecanismos de protección de gestión de decisiones y toma de decisiones {#decisioning-guardrails}

Las reglas y limitaciones que se deben tener en cuenta al trabajar con toma de decisiones o gestión de decisiones se detallan en estas secciones de toma de decisiones y gestión de decisiones:

* [Limitaciones y protecciones de decisiones](../experience-decisioning/decisioning-guardrails.md)
* [Limitaciones y mecanismos de protección de gestión de decisiones](../offers/decision-management-guardrails.md)

## Orquestación de campañas {#campaign-orchestration}

### Mecanismos de protección en orquestación de campañas {#orchestration-guardrails}

Los mecanismos de protección y las limitaciones que se deben tener en cuenta al trabajar con la orquestación de campañas se detallan en esta sección: [Mecanismos de protección y limitaciones](../orchestrated/guardrails.md).
