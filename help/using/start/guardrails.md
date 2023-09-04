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
source-git-commit: d56053d9db3d7c07d629069c985640e694b32ce1
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 99%

---

# Mecanismos de protección y limitaciones {#limitations}

Los derechos, limitaciones de productos y protección del rendimiento se enumeran en la [página de descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

También debe tener en cuenta los [mecanismos de protección para los datos del perfil del cliente en tiempo real antes de comenzar](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=es){target="_blank"}.

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

## Mecanismos de protección de recorridos {#journeys-guardrails}

### Protecciones generales del recorrido {#journeys-guardrails-journeys}

* El número de actividades en un recorrido ahora está limitado a 50. El número de actividades se muestra en la sección superior izquierda del lienzo de recorrido. Esto ayudará en la legibilidad, el control de calidad y la resolución de problemas.
* A medida que publica recorridos, los ampliamos y ajustamos automáticamente para garantizar el máximo rendimiento y estabilidad. Cuando se aproxime al hito de 100 recorridos en directo al mismo tiempo, verá una notificación en la interfaz de usuario sobre este logro. Si recibe esta notificación y necesita extender sus recorridos más allá de los 100 recorridos en directo a la vez, cree un ticket para el servicio de atención al cliente y le ayudaremos a alcanzar sus objetivos.

### Acciones generales {#general-actions-g}

* En caso de error, se realizan tres reintentos de forma sistemática. No puede ajustar el número de reintentos según el mensaje de error recibido. Los reintentos se realizan para todos los errores HTTP excepto para HTTP 401, 403 y 404.
* El evento **Reacción** le permite reaccionar a las acciones predeterminadas. Obtenga más información en [esta página](../building-journeys/reaction-events.md). Si desea reaccionar a un mensaje enviado mediante una acción personalizada, debe configurar un evento dedicado.
* No puede colocar dos acciones en paralelo, debe agregarlas una tras otra.
* Normalmente, un perfil no puede estar presente varias veces en el mismo recorrido y al mismo tiempo. Si la reentrada está activada, un perfil puede volver a entrar en un recorrido, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido. [Más información](../building-journeys/end-journey.md)

### Versiones de recorridos {#journey-versions-g}

* Un recorrido que se inicia con una actividad de evento en v1 no puede comenzar con otra cosa que un evento en versiones posteriores. No puede iniciar un recorrido con un evento de **Calificación de audiencia**.
* Un recorrido que se inicia con una actividad de **Calificación de audiencia** en la versión 1 siempre debe comenzar con una **Calificación de audiencia** en versiones posteriores.
* La audiencia y el área de nombres elegidos en la **Calificación de audiencias** (primer nodo) no se pueden cambiar en las versiones nuevas.
* La regla de reentrada debe ser la misma en todas las versiones del recorrido.
* El recorrido que comience con **Leer audiencia** no puede comenzar con otro evento en las versiones siguientes.
* No se puede crear una nueva versión de un recorrido de lectura de audiencia con lectura incremental. Debe duplicar el recorrido.

### Acciones personalizadas {#custom-actions-g}

* La URL de acción personalizada no admite parámetros dinámicos.
* Se admiten los métodos POST, PUT y llamada de GET
* El nombre del parámetro de consulta o del encabezado no debe comenzar con &quot;.&quot; o &quot;$&quot;
* No se permiten direcciones IP
* Las direcciones de Adobe internas (`.adobe.*`) no están permitidas en las direcciones URL y las API.
* Las acciones personalizadas integradas no se pueden eliminar.

### Eventos {#events-g}

* En el caso de los eventos generados por el sistema, los datos de streaming utilizados para iniciar un recorrido del cliente deben configurarse primero en Journey Optimizer para obtener un ID de orquestación único. Este ID de orquestación debe añadirse a la carga útil de streaming que llega a Adobe Experience Platform. Esta limitación no se aplica a los eventos basados en reglas.
* Los eventos empresariales no se pueden usar junto con eventos unitarios o actividades de calificación de audiencia.
* Los recorridos unitarios (que se inician con un evento o una calificación de audiencia) incluyen un mecanismo de protección que evita que los recorridos se activen varias veces de forma errónea para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante cinco minutos. Por ejemplo, si un evento activa un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.
* Journey Optimizer requiere que los eventos se transmitan al servicio principal de recopilación de datos (DCCS) para poder activar un recorrido. Eventos consumidos por lotes o eventos de conjuntos de datos internos de Journey Optimizer (comentarios de mensajes, seguimiento del correo electrónico, etc.) no se puede usar para activar un recorrido. Para los casos de uso en los que no pueda obtener los eventos transmitidos, genere una audiencia basado en esos eventos y use la actividad **Leer audiencia** en su lugar. Técnicamente, la calificación de la audiencia puede utilizarse, pero puede provocar problemas posteriores en función de las acciones utilizadas.

### Fuentes de datos {#data-sources-g}

* Las fuentes de datos externas se pueden aprovechar dentro de un recorrido del cliente para buscar datos externos en tiempo real. Estas fuentes deben utilizarse mediante la API de REST, admiten JSON y pueden gestionar el volumen de solicitudes.
* Las direcciones de Adobe internas (`.adobe.*`) no están permitidas en las direcciones URL y las API.

### Creación de recorridos y perfiles {#journeys-limitation-profile-creation}

Hay un retraso asociado a la creación/actualización de perfiles basados en la API en Adobe Experience Platform. El destinatario de nivel de servicio (SLT) en términos de latencia es &lt;1 min desde la ingesta hasta el perfil unificado para el percentil 95 de las solicitudes, a un volumen de 20 000 solicitudes por segundo (RPS).

Si un recorrido se activa simultáneamente para crear un perfil y comprueba o recupera inmediatamente la información del servicio de perfil, es posible que no funcione de forma correcta.

Puede elegir entre una de estas dos soluciones:

* Agregue una actividad de espera después del primer evento para que Adobe Experience Platform tenga el tiempo necesario para realizar la ingesta en el servicio de perfil.

* Configure un recorrido que no utilice inmediatamente el perfil. Por ejemplo, si el recorrido está diseñado para confirmar la creación de una cuenta, el evento de experiencia podría contener la información necesaria para enviar el primer mensaje de confirmación (nombre, apellidos, dirección de correo electrónico, etc.).

### Lectura de audiencia {#read-segment-g}

* Las audiencias transmitidas siempre están actualizadas, pero las audiencias por lotes no se calcularán en el momento de la recuperación. Solo se evalúan cada día a la hora de evaluar el lote.
* Para los recorridos que utilizan la actividad Leer audiencia, existe un número máximo de recorridos que pueden comenzar al mismo tiempo. El sistema realizará los reintentos, pero evite tener más de cinco recorridos (con Leer audiencia, programados o que se inicien “lo antes posible”) que empiecen al mismo tiempo. Para ello, repártalos a lo largo del tiempo, por ejemplo, en intervalos de 5 y 10 minutos.

### Editor de expresiones {#expression-editor}

* Los grupos de campos de eventos de experiencia no se pueden utilizar en recorridos que comiencen con Leer audiencia, Calificación de audiencia o una actividad de evento empresarial. Debe crear una audiencia nueva y utilizar una condición dentro de la audiencia en el recorrido.


### Limitaciones de actividad en la aplicación {#in-app-activity-limitations}

* Actualmente, esta función no está disponible para los clientes de Asistencia sanitaria.

* La personalización solo puede contener atributos de perfil.

* La visualización en la aplicación está ligada a la duración del recorrido, lo que significa que cuando el recorrido termina para un perfil, todos los mensajes en la aplicación dentro de ese recorrido dejan de mostrarse para ese perfil.  Por lo tanto, no es posible detener un mensaje en la aplicación directamente desde una actividad de recorrido. En su lugar, deberá finalizar todo el recorrido para que los mensajes en la aplicación no se muestren en el perfil.

* En el modo de prueba, la visualización en la aplicación depende de la duración del recorrido. Para evitar que el recorrido termine demasiado pronto durante la prueba, ajuste el valor **[!UICONTROL Tiempo de espera]** para sus actividades de **[!UICONTROL Espera]**.

* Las actividades de **[!UICONTROL Reacción]** no se pueden utilizar para reaccionar ante una apertura o un clic en la aplicación.

* Puede producirse un retraso de activación entre el momento en que un perfil de usuario alcanza una actividad en la aplicación en el lienzo y la hora en que comienza a ver ese mensaje en la aplicación.

* El tamaño del contenido del mensaje en la aplicación está limitado a 2 Mb. La inclusión de imágenes grandes puede dificultar el proceso de publicación.
