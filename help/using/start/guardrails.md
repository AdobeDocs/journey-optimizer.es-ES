---
solution: Journey Optimizer
product: journey optimizer
title: Limitaciones y mecanismos de protección de Journey Optimizer
description: Obtenga más información acerca de los mecanismos de protección de Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
mini-toc-levels: 1
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 2da5443e6927d0696cefbedee4f56a397208bc1c
workflow-type: tm+mt
source-wordcount: '2648'
ht-degree: 99%

---

# Protecciones y limitaciones {#limitations}

A continuación, encontrará limitaciones y mecanismos de protección adicionales al utilizar [!DNL Adobe Journey Optimizer].

Los derechos, limitaciones de productos y protección del rendimiento se enumeran en la [página de descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.


>[!CAUTION]
>
>* Los [mecanismos de protección de los datos del perfil del cliente en tiempo real](https://experienceleague.adobe.com/es/docs/experience-platform/profile/guardrails){target="_blank"} también se aplican a Adobe Journey Optimizer.
>
>* Consulte también [Mecanismos de protección para la ingesta de datos en el perfil del cliente en tiempo real](https://experienceleague.adobe.com/es/docs/experience-platform/ingestion/guardrails){target="_blank"}


## Navegadores admitidos {#browsers}

La interfaz de Adobe [!DNL Journey Optimizer] está diseñada para funcionar de forma óptima en la última versión de Google Chrome. Es posible que tenga problemas al utilizar determinadas funciones en versiones anteriores u otros navegadores.

## Mecanismos de protección de los conjuntos de datos {#datasets-guardrails}

A partir de febrero de 2025, se implementará gradualmente un mecanismo de protección de tiempo de vida (TTL) en los conjuntos de datos generados por el sistema de Journey Optimizer en las **nuevas zonas protegidas y organizaciones** de la siguiente manera:

* 90 días para los datos en el almacén de perfiles,
* 13 meses para los datos en el lago de datos.

Este cambio se implementará en las **zonas protegidas de clientes existentes** en una fase posterior. [Obtenga más información sobre los mecanismos de protección de tiempo de vida (Time-To-Live, TTL) de los conjuntos de datos](../data/datasets-ttl.md)

## Protecciones de canales {#channel-guardrails}

>[!NOTE]
>
>En circunstancias excepcionales, las interrupciones temporales en una región específica pueden provocar que se excluyan perfiles válidos de los recorridos o que los correos electrónicos se marquen incorrectamente como rechazos. Una vez restaurados los servicios, vuelva a comprobar los registros del recorrido, compruebe los campos de perfil de consentimiento y vuelva a publicar el recorrido si fuera necesario. En caso de una interrupción de ISP, aprenda a quitar perfiles de la lista de supresión en [esta sección](../configuration/manage-suppression-list.md#remove-from-suppression-list).
>

### Protecciones de correo electrónico {#message-guardrails}

Las siguientes limitaciones se aplican a la actividad [canal de correo electrónico](../email/get-started-email.md):

* No pueden agregar archivos adjuntos a un correo electrónico con [!DNL Journey Optimizer].
* No puede utilizar el mismo dominio de envío para enviar mensajes desde [!DNL Adobe Journey Optimizer] y desde otro producto, como [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage], por ejemplo.

### Protecciones de los SMS {#sms-guardrails}

Las siguientes limitaciones se aplican a la actividad [canal de SMS](../sms/get-started-sms.md):

* Los archivos multimedia para MMS se pueden incluir a través de una dirección URL compatible. Asegúrese de que el archivo multimedia se cargue por separado.
* Actualmente, la sincronización de comentarios de mensajes no está disponible para MMS.
* La administración de consentimientos funciona en el nivel de canal SMS para MMS.

### Protecciones de canal web {#web-guardrails}

[Las campañas web de](../web/get-started-web.md) [!DNL Journey Optimizer] se dirigen a nuevos perfiles que no han interactuado antes en otros canales. Esto aumentará el recuento total de perfiles con los que es posible interactuar, lo que puede tener costes si se supera el número contractual de perfiles adquiridos. 

Las métricas de licencia de cada paquete se enumeran en la página [Descripción del producto Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

### Protecciones de canal basado en código {#code-based-guardrails}

Para usar acciones de experiencia basada en código en [!DNL Journey Optimizer] y entregar carga útil de contenido de código que puedan usar las aplicaciones, siga los requisitos previos detallados en [esta página](../code-based/code-based-prerequisites.md).

## Mecanismos de protección de las páginas de destino {#lp-guardrails}

Las siguientes limitaciones se aplican a las [páginas de destino](../landing-pages/get-started-lp.md):

* Solo se puede utilizar un componente **Formulario** en una sola página principal.
* El componente **Formulario** no se puede usar en subpáginas.
* No puede agregar un preencabezado a una página de destino.
* No puede seleccionar la opción **Programar usted mismo** al diseñar una página de aterrizaje principal.

## Protecciones de subdominios {#subdomain-guardrails}

Las protecciones y limitaciones aplicables a la delegación de subdominios en Journey Optimizer se detallan en [esta página](../configuration/delegate-subdomain.md#guardrails).

## Protecciones de fragmentos {#fragments-guardrails}

Las siguientes limitaciones se aplican a los [fragmentos](../content-management/fragments.md):

* Para crear, editar, archivar y publicar fragmentos, necesita los permisos **[!DNL Manage library items]** y **[Publicar fragmento]** incluidos en el perfil de producto **[!DNL Content Library Manager]**. [Más información](../administration/ootb-product-profiles.md#content-library-manager)
* Los fragmentos visuales solo están disponibles para el canal de correo electrónico.
* Los fragmentos de expresiones no están disponibles para el canal en la aplicación.
* Los fragmentos visuales no pueden superar los 100 KB. Los fragmentos de expresión no pueden superar los 200 KB.
* Para utilizar un fragmento de un recorrido o una campaña, debe tener el estado **Activo**.
* No se admiten [atributos contextuales](../personalization/personalization-build-expressions.md) en los fragmentos.
* Los fragmentos visuales no son compatibles entre los modos Usar temas y Estilo manual. Para poder utilizar un fragmento en un contenido en el que desee aplicar una temática, este fragmento debe crearse en el modo Usar temas. [Más información sobre los temas](../email/apply-email-themes.md)
* Cuando el seguimiento está habilitado en un recorrido o una campaña, si agrega vínculos a un fragmento y este se utiliza en un mensaje, se realiza el seguimiento de estos vínculos, al igual que todos los demás incluidos en el mensaje. [Más información sobre vínculos y seguimiento](../email/message-tracking.md)

## Protecciones de públicos {#audience}

Puede publicar hasta 10 composiciones de público en una zona protegida determinada. Si ha alcanzado este umbral, debe eliminar una composición para liberar espacio y publicar una nueva.

Más información sobre la composición de públicos en [esta página](../audience/get-started-audience-orchestration.md).

## Mecanismos de protección de gestión de decisiones y toma de decisiones {#decisioning-guardrails}

Las protecciones y limitaciones que se deben tener en cuenta al trabajar con toma de decisiones o gestión de decisiones se detallan en estas secciones de toma de decisiones y gestión de decisiones:

* [Limitaciones y protecciones de decisiones](../experience-decisioning/decisioning-guardrails.md)
* [Limitaciones y mecanismos de protección de gestión de decisiones](../offers/decision-management-guardrails.md)

## Mecanismos de protección de recorridos {#journeys-guardrails}

### Protecciones generales del recorrido {#journeys-guardrails-journeys}

* El número de actividades en un recorrido ahora está limitado a 50. El número de actividades se muestra en la sección superior izquierda del lienzo de recorrido. Esto ayudará en la legibilidad, el control de calidad y la resolución de problemas.
* De forma predeterminada, el número de recorridos de ejecución activos/en pausa/de ensayo simultáneos está limitado a 100.  El número actual de recorridos se muestra encima del lienzo del recorrido.
* A medida que publica recorridos, los ampliamos y ajustamos automáticamente para garantizar el máximo rendimiento y estabilidad. Cuando se aproxime al hito de 100 recorridos en directo al mismo tiempo, verá una notificación en la interfaz de usuario sobre este logro. Si recibe esta notificación y necesita extender sus recorridos más allá de los 100 recorridos en directo a la vez, cree un ticket para el servicio de atención al cliente y le ayudaremos a alcanzar sus objetivos.
* Cuando se utiliza una calificación de público en un recorrido, esa actividad de calificación de público puede tardar hasta 10 minutos en estar activa y en escuchar los perfiles que entran o salen del público.
* Una instancia de recorrido de un perfil tiene un tamaño máximo de 1 MB. Todos los datos recopilados como parte de la ejecución del recorrido se almacenan en esa instancia de recorrido. Por lo tanto, los datos de un evento entrante, la información de perfil recuperada de Adobe Experience Platform, las respuestas de acciones personalizadas, etc. se almacenan en esa instancia de recorrido y afectan al tamaño del recorrido. Se recomienda, cuando un recorrido comienza con un evento, limitar el tamaño máximo de esa carga útil de evento (p. ej.: por debajo de 800 KB) para evitar alcanzar ese límite después de unas pocas actividades, en la ejecución del recorrido. Cuando se alcanza ese límite, el perfil está en estado de error y se excluirá del recorrido.
* Además del tiempo de espera utilizado en las actividades del recorrido, también hay un tiempo de espera de recorrido global que no se muestra en la interfaz y no se puede cambiar. Este tiempo de espera global detiene el progreso de los particulares en el recorrido 91 días después de su entrada. [Más información](../building-journeys/journey-properties.md#global_timeout)

### Acciones generales {#general-actions-g}

Las siguientes limitaciones se aplican a las [Acciones](../building-journeys/about-journey-activities.md) en sus recorridos:

* En caso de error, se realizan tres reintentos de forma sistemática. No puede ajustar el número de reintentos según el mensaje de error recibido. Los reintentos se realizan para todos los errores HTTP excepto para HTTP 401, 403 y 404.
* El evento **Reacción** integrado le permite reaccionar a las acciones predeterminadas. Obtenga más información en [esta página](../building-journeys/reaction-events.md). Si desea reaccionar a un mensaje enviado mediante una acción personalizada, debe configurar un evento dedicado.
* No puede colocar dos acciones en paralelo, debe agregarlas una tras otra.
* Un perfil no puede estar presente varias veces en el mismo recorrido, al mismo tiempo, para todas las [versiones activas del recorrido](../building-journeys/publishing-the-journey.md#create-a-new-version-of-a-journey-journey-create-new-version). Si la reentrada está activada, un perfil puede volver a entrar en un recorrido, pero no puede hacerlo hasta que salga por completo de la instancia anterior del recorrido. [Más información](../building-journeys/end-journey.md)

### Versiones de recorridos {#journey-versions-g}

Las siguientes limitaciones se aplican a las [versiones del recorrido](../start/user-interface.md):

* Un recorrido que se inicia con una actividad de evento en v1 no puede comenzar con otra cosa que un evento en versiones posteriores. No puede iniciar un recorrido con un evento de **Calificación de público**.
* Un recorrido que se inicia con una actividad de **Calificación de público** en la versión 1 siempre debe comenzar con una **Calificación de público** en versiones posteriores.
* El público y el área de nombres elegidos en la **Calificación de públicos** (primer nodo) no se pueden cambiar en las versiones nuevas.
* La regla de reentrada debe ser la misma en todas las versiones del recorrido.
* El recorrido que comience con **Leer público** no puede comenzar con otro evento en las versiones siguientes.
* No se puede crear una nueva versión de un recorrido de lectura de público con lectura incremental. Debe duplicar el recorrido.

### Acciones personalizadas {#custom-actions-g}

Las siguientes limitaciones se aplican a las [Acciones personalizadas](../action/action.md) en sus recorridos:

* Se define un límite de 300 000 llamadas durante un minuto para todas las acciones personalizadas, por host y por zona protegida. Consulte [esta página](../action/about-custom-action-configuration.md). Este límite se ha establecido en función del uso de los clientes para proteger los extremos externos dirigidos por acciones personalizadas. Si es necesario, puede anular esta configuración definiendo un límite o restricción mayor mediante nuestras API de límite/restricción. Consulte [esta página](../configuration/external-systems.md).
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

Las siguientes limitaciones se aplican a los [Eventos](../event/about-events.md) en sus recorridos:

* Journey Optimizer admite un volumen máximo de 5000 eventos de recorrido entrantes por segundo.
* Los recorridos activados por eventos pueden tardar hasta 5 minutos en procesar la primera acción del recorrido.
* En el caso de los eventos generados por el sistema, los datos de streaming utilizados para iniciar un recorrido del cliente deben configurarse primero en Journey Optimizer para obtener un ID de orquestación único. Este ID de orquestación debe añadirse a la carga útil de streaming que llega a Adobe Experience Platform. Esta limitación no se aplica a los eventos basados en reglas.
* Los eventos empresariales no se pueden usar junto con eventos unitarios o actividades de calificación de público.
* Los recorridos unitarios (que se inician con un evento o una calificación de público) incluyen un mecanismo de protección que evita que los recorridos se activen varias veces de forma errónea para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante cinco minutos. Por ejemplo, si un evento activa un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.
* Journey Optimizer requiere que los eventos se transmitan al servicio principal de recopilación de datos (DCCS) para poder activar un recorrido. Los eventos consumidos por lotes o los eventos de conjuntos de datos internos de Journey Optimizer (comentarios de mensajes, seguimiento del correo electrónico, etc.) no se pueden utilizar para activar un recorrido. Para los casos de uso en los que no pueda obtener los eventos transmitidos, genere un público basado en dichos eventos y utilice la actividad **Público de lectura** en su lugar. Técnicamente, la calificación del público puede utilizarse, pero no se recomienda porque puede provocar problemas posteriores en función de las acciones utilizadas.

### Fuentes de datos {#data-sources-g}

Las siguientes limitaciones se aplican a las [Fuentes de datos](../datasource/about-data-sources.md) en sus recorridos:

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

Se aplican mecanismos de protección específicos a la actividad **[!UICONTROL Actualizar perfil]**. Se muestran en [esta página](../building-journeys/update-profiles.md).

### Leer público {#read-segment-g}

Las siguientes limitaciones se aplican a la actividad de recorrido [Público de lectura](../building-journeys/read-audience.md):

* Los públicos transmitidos siempre están actualizados, pero los públicos por lotes no se calcularán en el momento de la recuperación. Solo se evalúan cada día a la hora de evaluar el lote.
* Para los recorridos que utilizan una actividad **Leer público**, existe un número máximo de recorridos que pueden comenzar al mismo tiempo. El sistema realizará los reintentos, pero evite tener más de cinco recorridos (con **Leer público**, programados o que se inicien “lo antes posible”) que empiecen al mismo tiempo. Para ello, repártalos a lo largo del tiempo, por ejemplo, en intervalos de 5 y 10 minutos.
* La actividad **Leer público** no se puede utilizar con actividades de Adobe Campaign.
* La actividad **Leer público** solo puede utilizarse como primera actividad en un recorrido o después de una actividad de evento empresarial.
* Un recorrido solo puede tener una actividad **Leer público**.
* Vea también las recomendaciones acerca de cómo usar la actividad **Leer público** en [esta página](../building-journeys/read-audience.md).
* Los reintentos ahora se aplican de forma predeterminada en recorridos activados por públicos destinatarios (empezando con una actividad **Leer público** o **Evento empresarial**) cuando se recupera el trabajo de exportación. Si se produce un error durante la creación del trabajo de exportación, se realizarán reintentos cada 10 minutos, hasta un máximo de 1 hora. Después de esto, se considerará como un error. Por lo tanto, estos tipos de recorridos se pueden ejecutar hasta una hora después de la hora programada.


Consulte [esta página](../building-journeys/read-audience.md#must-read).

### Calificación de público {#audience-qualif-g}

El siguiente mecanismo de protección se aplica a la actividad de recorrido [Calificación de público](../building-journeys/audience-qualification-events.md):

* La actividad de calificación de público no se puede utilizar con actividades de Adobe Campaign.

### Editor de expresiones {#expression-editor}

Los siguientes mecanismos de protección se aplican al [editor de expresiones de recorrido](../building-journeys/expression/expressionadvanced.md):

* Los grupos de campos de eventos de experiencia no se pueden utilizar en recorridos que comiencen con Leer público, Calificación de público o una actividad de evento empresarial. Debe crear un público nuevo y utilizar una condición `inaudience` en el recorrido.
* Los atributos `timeSeriesEvents` no se pueden usar en el editor de expresiones. Para acceder a los eventos de experiencia a nivel de perfil, cree un nuevo grupo de campos basado en un esquema `XDM ExperienceEvent`.


### Actividad en la aplicación {#in-app-activity-limitations}

Las siguientes limitaciones se aplican a la acción **[!UICONTROL Mensaje en la aplicación]**. Obtenga más información sobre los mensajes in-app en [esta página](../in-app/create-in-app.md).

* Actualmente, esta función no está disponible para los clientes de Asistencia sanitaria.

* La personalización solo puede contener atributos de perfil.

* La actividad en la aplicación no se puede utilizar con actividades de Adobe Campaign.

* La visualización en la aplicación está ligada a la duración del recorrido, lo que significa que cuando el recorrido termina para un perfil, todos los mensajes en la aplicación dentro de ese recorrido dejan de mostrarse para ese perfil.  Por lo tanto, no es posible detener un mensaje en la aplicación directamente desde una actividad de recorrido. En su lugar, deberá finalizar todo el recorrido para que los mensajes en la aplicación no se muestren en el perfil.

* En el modo de prueba, la visualización en la aplicación depende de la duración del recorrido. Para evitar que el recorrido termine demasiado pronto durante la prueba, ajuste el valor **[!UICONTROL Tiempo de espera]** para sus actividades de **[!UICONTROL Espera]**.

* Las actividades de **[!UICONTROL Reacción]** no se pueden utilizar para reaccionar ante una apertura o un clic en la aplicación.

* Puede producirse un retraso de activación entre el momento en que un perfil de usuario alcanza una actividad en la aplicación en el lienzo y la hora en que comienza a ver ese mensaje en la aplicación.

* El tamaño del contenido del mensaje en la aplicación está limitado a 2 Mb. La inclusión de imágenes grandes puede dificultar el proceso de publicación.

### Actividad de salto {#jump-g}

Especifique protecciones específicas de la actividad **[!UICONTROL Saltar]**. Se muestran en [esta página](../building-journeys/jump.md#jump-limitations).

### Actividades de campaña {#ac-g}

Los siguientes mecanismos de protección se aplican a las actividades **[!UICONTROL Campaign v7/v8]** y **[!UICONTROL Campaign Standard]**:

* Las actividades de Adobe Campaign no se pueden utilizar con un público de lectura o una actividad de calificación de público.
* Las actividades de la campaña no se pueden utilizar con las actividades de otros canales: Tarjeta, Experiencia basada en código, Correo electrónico, Push, SMS, Mensajes en la aplicación, Web.

## Protecciones en orquestación de campañas {#orchestration-guardrails}

Las protecciones y limitaciones que se deben tener en cuenta al trabajar con la orquestación de campañas se detallan en esta sección: [Limitaciones y protecciones en la gestión de decisiones](../orchestrated/guardrails.md).
