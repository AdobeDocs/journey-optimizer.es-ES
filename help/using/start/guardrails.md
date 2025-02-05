---
solution: Journey Optimizer
product: journey optimizer
title: Limitaciones y mecanismos de protección de Journey Optimizer
description: Obtenga más información acerca de los mecanismos de protección de Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: aec3d79ad07ec6904e55afd6fc61ba9b4f403fc8
workflow-type: tm+mt
source-wordcount: '2361'
ht-degree: 98%

---

# Mecanismos de protección y limitaciones {#limitations}

Los derechos, limitaciones de productos y protección del rendimiento se enumeran en la [página de descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

También debe tener en cuenta las [protecciones para los datos del perfil del cliente en tiempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=es){target="_blank"} antes de comenzar.

A continuación, encontrará limitaciones y protecciones adicionales al utilizar [!DNL Adobe Journey Optimizer].

## Navegadores admitidos {#browsers}

La interfaz de Adobe [!DNL Journey Optimizer] está diseñada para funcionar de forma óptima en la última versión de Google Chrome. Es posible que tenga problemas al utilizar determinadas funciones en versiones anteriores u otros navegadores.

## Mecanismos de protección de mensajes {#message-guardrails}

* No pueden agregar archivos adjuntos a un correo electrónico con [!DNL Journey Optimizer].
* No puede utilizar el mismo dominio de envío para enviar mensajes desde [!DNL Adobe Journey Optimizer] y desde otro producto, como [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage], por ejemplo.

## Mecanismos de protección de las páginas de aterrizaje {#lp-guardrails}

* Solo se puede utilizar un componente **Formulario** en una sola página principal.
* El componente **Formulario** no se puede usar en subpáginas.
* No puede agregar un preencabezado a una página de aterrizaje.
* No puede seleccionar la opción **Programar usted mismo** al diseñar una página de aterrizaje principal.

## Protecciones de los SMS {#sms-guardrails}

* Los archivos multimedia para MMS se pueden incluir a través de una dirección URL compatible. Asegúrese de que el archivo multimedia se cargue por separado.
* Actualmente, la sincronización de comentarios de mensajes no está disponible para MMS.
* La administración de consentimientos funciona en el nivel de canal SMS para MMS.

### Protecciones de canal web {#web-guardrails}

Las campañas web de [!DNL Journey Optimizer] se dirigen a nuevos perfiles que no han interactuado anteriormente en otros canales. Esto aumentará el recuento total de perfiles con los que es posible interactuar, lo que puede tener costes si se supera el número contractual de perfiles adquiridos. Las métricas de licencia de cada paquete se enumeran en la página [Descripción del producto Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.


## Protecciones de subdominios {#subdomain-guardrails}

De forma predeterminada, [!DNL Journey Optimizer] permite delegar hasta 10 subdominios en total (que abarcan tanto el correo electrónico como los canales web).

Sin embargo, según el contrato de licencia, puede delegar hasta 100 subdominios. Póngase en contacto con la persona de contacto de Adobe para obtener más información sobre el número de subdominios a los que tiene derecho.

## Protecciones de fragmentos {#fragments-guardrails}

* Los fragmentos visuales solo están disponibles para el canal de correo electrónico.
* Los fragmentos de expresiones no están disponibles para el canal en la aplicación.

## Mecanismos de protección de recorridos {#journeys-guardrails}

### Protecciones generales del recorrido {#journeys-guardrails-journeys}

* El número de actividades en un recorrido ahora está limitado a 50. El número de actividades se muestra en la sección superior izquierda del lienzo de recorrido. Esto ayudará en la legibilidad, el control de calidad y la resolución de problemas.
* A medida que publica recorridos, los ampliamos y ajustamos automáticamente para garantizar el máximo rendimiento y estabilidad. Cuando se aproxime al hito de 100 recorridos en directo al mismo tiempo, verá una notificación en la interfaz de usuario sobre este logro. Si recibe esta notificación y necesita extender sus recorridos más allá de los 100 recorridos en directo a la vez, cree un ticket para el servicio de atención al cliente y le ayudaremos a alcanzar sus objetivos.
  <!-- DOCAC-10977 * As you publish journeys, we automatically scale and adjust to ensure maximum throughput and stability. As you near the milestone of 500 live journeys at one time, you will see a notification appear in the UI on this achievement. If you see this notification and have a need to extend your journeys beyond 500 live journeys at a time, please create a ticket for customer care and we will help you reach your goals.-->
* Cuando se utiliza una calificación de público en un recorrido, esa actividad de calificación de público puede tardar hasta 10 minutos en estar activa y en escuchar los perfiles que entran o salen del público.
* Una instancia de recorrido de un perfil tiene un tamaño máximo de 1 MB. Todos los datos recopilados como parte de la ejecución del recorrido se almacenan en esa instancia de recorrido. Por lo tanto, los datos de un evento entrante, la información de perfil recuperada de Adobe Experience Platform, las respuestas de acciones personalizadas, etc. se almacenan en esa instancia de recorrido y afectan al tamaño del recorrido. Se recomienda, cuando un recorrido comienza con un evento, limitar el tamaño máximo de esa carga útil de evento (p. ej.: por debajo de 800 KB) para evitar alcanzar ese límite después de unas pocas actividades, en la ejecución del recorrido. Cuando se alcanza ese límite, el perfil está en estado de error y se excluirá del recorrido.
* Además del tiempo de espera utilizado en las actividades del recorrido, también hay un tiempo de espera de recorrido global que no se muestra en la interfaz y no se puede cambiar. Este tiempo de espera global detiene el progreso de los particulares en el recorrido 91 días después de su entrada. [Más información](../building-journeys/journey-properties.md#global_timeout)


### Acciones generales {#general-actions-g}

* En caso de error, se realizan tres reintentos de forma sistemática. No puede ajustar el número de reintentos según el mensaje de error recibido. Los reintentos se realizan para todos los errores HTTP excepto para HTTP 401, 403 y 404.
* El evento **Reacción** le permite reaccionar a las acciones predeterminadas. Obtenga más información en [esta página](../building-journeys/reaction-events.md). Si desea reaccionar a un mensaje enviado mediante una acción personalizada, debe configurar un evento dedicado.
* No puede colocar dos acciones en paralelo, debe agregarlas una tras otra.
* Normalmente, un perfil no puede estar presente varias veces en el mismo recorrido y al mismo tiempo. Si la reentrada está activada, un perfil puede volver a entrar en un recorrido, pero no puede hacerlo hasta que salga por completo de la instancia anterior del recorrido. [Más información](../building-journeys/end-journey.md)

### Versiones de recorridos {#journey-versions-g}

* Un recorrido que se inicia con una actividad de evento en v1 no puede comenzar con otra cosa que un evento en versiones posteriores. No puede iniciar un recorrido con un evento de **Calificación de público**.
* Un recorrido que se inicia con una actividad de **Calificación de público** en la versión 1 siempre debe comenzar con una **Calificación de público** en versiones posteriores.
* El público y el área de nombres elegidos en la **Calificación de públicos** (primer nodo) no se pueden cambiar en las versiones nuevas.
* La regla de reentrada debe ser la misma en todas las versiones del recorrido.
* El recorrido que comience con **Leer público** no puede comenzar con otro evento en las versiones siguientes.
* No se puede crear una nueva versión de un recorrido de lectura de público con lectura incremental. Debe duplicar el recorrido.

### Acciones personalizadas {#custom-actions-g}

* Se define un límite de 300 000 llamadas durante un minuto para todas las acciones personalizadas, por host y por zona protegida. Consulte [esta página](../action/about-custom-action-configuration.md). Este límite se ha establecido en función del uso de los clientes para proteger los extremos externos dirigidos por acciones personalizadas. Debe tenerlo en cuenta en los recorridos basados en públicos definiendo una tasa de lectura adecuada (5.000 perfiles cuando se utilizan acciones personalizadas). Si es necesario, puede anular esta configuración definiendo un límite o restricción mayor mediante nuestras API de límite/restricción. Consulte [esta página](../configuration/external-systems.md).
* La URL de acción personalizada no admite parámetros dinámicos.
* Se admiten los métodos POST, PUT y llamada de GET
* El nombre del parámetro de consulta o del encabezado no debe comenzar con &quot;.&quot; o &quot;$&quot;
* No se permiten direcciones IP
* Las direcciones de Adobe internas (`.adobe.*`) no están permitidas en las direcciones URL y las API.
* Las acciones personalizadas integradas no se pueden eliminar.
* Las acciones personalizadas solo admiten el formato JSON cuando se utilizan cargas útiles de solicitud o respuesta. Consulte [esta página](../action/about-custom-action-configuration.md#custom-actions-limitations).
* Al elegir un extremo como destino mediante una acción personalizada, asegúrese de lo siguiente:

   * Este extremo puede admitir el rendimiento del recorrido mediante las configuraciones de la [API de límite](../configuration/throttling.md) o la [API de cierre](../configuration/capping.md) para limitarlo. Tenga cuidado ya que una configuración de limitación no puede estar por debajo de 200 TPS. Cualquier extremo segmentado debe admitir al menos 200 TPS.
   * Este extremo necesita tener un tiempo de respuesta lo más bajo posible. Según el rendimiento esperado, tener un tiempo de respuesta alto podría afectar al rendimiento real.

### Eventos {#events-g}

* En el caso de los eventos generados por el sistema, los datos de streaming utilizados para iniciar un recorrido del cliente deben configurarse primero en Journey Optimizer para obtener un ID de orquestación único. Este ID de orquestación debe añadirse a la carga útil de streaming que llega a Adobe Experience Platform. Esta limitación no se aplica a los eventos basados en reglas.
* Los eventos empresariales no se pueden usar junto con eventos unitarios o actividades de calificación de público.
* Los recorridos unitarios (que se inician con un evento o una calificación de público) incluyen un mecanismo de protección que evita que los recorridos se activen varias veces de forma errónea para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante cinco minutos. Por ejemplo, si un evento activa un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.
* Journey Optimizer requiere que los eventos se transmitan al servicio principal de recopilación de datos (DCCS) para poder activar un recorrido. Los eventos ingeridos en lote o los eventos de conjuntos de datos internos de Journey Optimizer (comentarios de mensajes, seguimiento de correo electrónico, etc.) no se pueden utilizar para almacenar en déclencheur un recorrido. Para los casos de uso en los que no pueda obtener los eventos transmitidos, genere un público basado en dichos eventos y utilice la actividad **Público de lectura** en su lugar. Técnicamente, la calificación del público puede utilizarse, pero no se recomienda porque puede provocar problemas posteriores en función de las acciones utilizadas.


### Fuentes de datos {#data-sources-g}

* Las fuentes de datos externas se pueden aprovechar dentro de un recorrido del cliente para buscar datos externos en tiempo real. Estas fuentes deben utilizarse mediante la API de REST, admiten JSON y pueden gestionar el volumen de solicitudes.
* Las direcciones de Adobe internas (`.adobe.*`) no están permitidas en las direcciones URL y las API.

>[!NOTE]
>
>Como las respuestas ahora son compatibles, debe utilizar acciones personalizadas en lugar de fuentes de datos para casos de uso de fuentes de datos externas.

### Creación de recorridos y perfiles {#journeys-limitation-profile-creation}

Hay un retraso asociado a la creación/actualización de perfiles basados en la API en Adobe Experience Platform. El destinatario de nivel de servicio (SLT) en términos de latencia es &lt;1 min desde la ingesta hasta el perfil unificado para el percentil 95 de las solicitudes, a un volumen de 20 000 solicitudes por segundo (RPS).

Si un recorrido se activa simultáneamente para crear un perfil y comprueba o recupera inmediatamente la información del servicio de perfil, es posible que no funcione de forma correcta.

Puede elegir entre una de estas dos soluciones:

* Agregue una actividad de espera después del primer evento para que Adobe Experience Platform tenga el tiempo necesario para realizar la ingesta en el servicio de perfil.

* Configure un recorrido que no utilice inmediatamente el perfil. Por ejemplo, si el recorrido está diseñado para confirmar la creación de una cuenta, el evento de experiencia podría contener la información necesaria para enviar el primer mensaje de confirmación (nombre, apellidos, dirección de correo electrónico, etc.).

### Actualización de perfil {#update-profile-g}

Se aplican mecanismos de protección específicos a la actividad **[!UICONTROL Actualizar perfil]**. Se muestran [en esta página](../building-journeys/update-profiles.md).


### Público de lectura {#read-segment-g}

Las siguientes limitaciones se aplican a la actividad **[!UICONTROL Público de lectura]**:

* Los públicos transmitidos siempre están actualizados, pero los públicos por lotes no se calcularán en el momento de la recuperación. Solo se evalúan cada día a la hora de evaluar el lote.
* Para los recorridos que utilizan una actividad **Leer público**, existe un número máximo de recorridos que pueden comenzar al mismo tiempo. El sistema realizará los reintentos, pero evite tener más de cinco recorridos (con **Leer público**, programados o que se inicien “lo antes posible”) que empiecen al mismo tiempo. Para ello, repártalos a lo largo del tiempo, por ejemplo, en intervalos de 5 y 10 minutos.
* La actividad **Leer público** no se puede utilizar con actividades de Adobe Campaign.
* La actividad **Leer público** solo puede utilizarse como primera actividad en un recorrido o después de una actividad de evento empresarial.
* Un recorrido solo puede tener una actividad **Leer público**.
* Vea también las recomendaciones acerca de cómo usar la actividad **Leer público** en [esta página](../building-journeys/read-audience.md).
* Los reintentos ahora se aplican de forma predeterminada en recorridos activados por públicos destinatarios (empezando con una actividad **Leer público** o **Evento empresarial**) cuando se recupera el trabajo de exportación. Si se produce un error durante la creación del trabajo de exportación, se realizarán reintentos cada 10 minutos, hasta un máximo de 1 hora. Después de esto, se considerará como un error. Por lo tanto, estos tipos de recorridos se pueden ejecutar hasta una hora después de la hora programada.


### Calificación de público {#audience-qualif-g}

El siguiente mecanismo de protección se aplica a la actividad **[!UICONTROL Calificación de público]**:

* La actividad de calificación de público no se puede utilizar con actividades de Adobe Campaign.


### Editor de expresiones {#expression-editor}

* Los grupos de campos de eventos de experiencia no se pueden utilizar en recorridos que comiencen con Leer público, Calificación de público o una actividad de evento empresarial. Debe crear un público nuevo y utilizar una condición dentro del público en el recorrido.


### Actividad en la aplicación {#in-app-activity-limitations}

* Actualmente, esta función no está disponible para los clientes de Asistencia sanitaria.

* La personalización solo puede contener atributos de perfil.

* La actividad en la aplicación no se puede utilizar con actividades de Adobe Campaign.

* La visualización en la aplicación está ligada a la duración del recorrido, lo que significa que cuando el recorrido termina para un perfil, todos los mensajes en la aplicación dentro de ese recorrido dejan de mostrarse para ese perfil.  Por lo tanto, no es posible detener un mensaje en la aplicación directamente desde una actividad de recorrido. En su lugar, deberá finalizar todo el recorrido para que los mensajes en la aplicación no se muestren en el perfil.

* En el modo de prueba, la visualización en la aplicación depende de la duración del recorrido. Para evitar que el recorrido termine demasiado pronto durante la prueba, ajuste el valor **[!UICONTROL Tiempo de espera]** para sus actividades de **[!UICONTROL Espera]**.

* Las actividades de **[!UICONTROL Reacción]** no se pueden utilizar para reaccionar ante una apertura o un clic en la aplicación.

* Puede producirse un retraso de activación entre el momento en que un perfil de usuario alcanza una actividad en la aplicación en el lienzo y la hora en que comienza a ver ese mensaje en la aplicación.

* El tamaño del contenido del mensaje en la aplicación está limitado a 2 Mb. La inclusión de imágenes grandes puede dificultar el proceso de publicación.



### Actividad de salto {#jump-g}

Especifique protecciones específicas de la actividad **[!UICONTROL Saltar]**. Se muestran [en esta página](../building-journeys/jump.md#jump-limitations).

### Actividades de campaña {#ac-g}

Los siguientes mecanismos de protección se aplican a las actividades **[!UICONTROL Campaign v7/v8]** y **[!UICONTROL Campaign Standard]**:

* Las actividades de Adobe Campaign no se pueden utilizar con un público de lectura o una actividad de calificación de público.
* Estas actividades no se pueden utilizar con actividades en la aplicación.

## Protecciones de públicos {#audience}

Puede publicar hasta 10 composiciones de público en una zona protegida determinada. Si ha alcanzado este umbral, debe eliminar una composición para liberar espacio y publicar una nueva.

## Mecanismos de protección de gestión de decisiones {#decision-management}

### Protecciones de rendimiento {#performance-guardrails}

El rendimiento de envío corresponde al número de respuestas de decisión que puede entregar el servicio de aplicaciones de gestión de decisiones en un período de tiempo especificado. En el cuadro que figura a continuación se indica el número de decisiones por segundo.

| API | Decisiones por segundo |
|---------|----------|
| Solicitudes de decisiones de API | 500 por segundo |
| Solicitudes de API de Edge Decisioning con segmentación de Edge | 1.500 por segundo |
| Solicitudes de API de Edge Decisioning sin segmentación de Edge | 5.000 por segundo |

### Limitaciones {#offers-limitations}

Las limitaciones de Gestión de decisiones se indican a continuación.

* **Ofertas personalizadas aprobadas + Ofertas de reserva**: hasta 10 000 ofertas personalizadas aprobadas combinadas y ofertas de reserva aprobadas.
* **Decisiones**: hasta 10.000 Decisiones.
* **Decisiones en directo**: el servicio de la aplicación Offer Decisioning admite hasta 1000 decisiones en directo.
* **Ofertas devueltas por respuesta**: Offer Decisioning admite hasta 100 ofertas devueltas por solicitud en todos los ámbitos de decisión de la solicitud.
* **Colecciones**: hasta 10 000 colecciones.
* **Colecciones por decisión**: hasta 30 colecciones por decisión.
* **Reglas de decisión + Funciones de clasificación** Hasta 10 000 reglas de decisión y funciones de clasificación combinadas.
* **Ubicaciones**: hasta 1000 ubicaciones.
* **Ubicaciones por decisión**: hasta 30 ubicaciones por decisión.
* **Método de clasificación por decisión**: el servicio de aplicación Offer Decisioning admite hasta 30 funciones de clasificación por decisión.
* **Modelo de clasificaciones de IA**: el servicio de aplicación Offer Decisioning admite hasta 5 modelos de clasificaciones de IA.
* **Calificador de colección por oferta o colección**: el servicio de aplicación Offer Decisioning admite hasta 20 Calificadores de colección en cualquier Oferta personalizada o Colección única.
* **Calificadores de colección total**: el servicio de aplicaciones Offer Decisioning admite hasta 1000 Calificadores de colección.