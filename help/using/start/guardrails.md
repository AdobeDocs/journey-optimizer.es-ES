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
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 74%

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

### Acciones generales {#general-actions-g}

* No hay restricciones de envío.
* En caso de error, se realizan tres reintentos de forma sistemática. No puede ajustar el número de reintentos según el mensaje de error recibido.
* El evento **Reacción** le permite reaccionar a las acciones predeterminadas. Obtenga más información en [esta página](../building-journeys/reaction-events.md). Si desea reaccionar a un mensaje enviado mediante una acción personalizada, debe configurar un evento dedicado.
* No puede colocar dos acciones en paralelo, debe agregarlas una tras otra.
* Normalmente, un perfil no puede estar presente varias veces en el mismo recorrido y al mismo tiempo. Si la reentrada está activada, un perfil puede volver a entrar en un recorrido, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido. [Más información](../building-journeys/end-journey.md)

### Versiones de recorridos {#journey-versions-g}

* Un recorrido que se inicia con una actividad de evento en v1 no puede comenzar con otra cosa que un evento en versiones posteriores. No se puede iniciar un recorrido con un **Calificación de audiencias** evento.
* Un recorrido que comienza con un **Calificación de audiencias** la actividad en v1 siempre debe comenzar con una **Calificación de audiencias** en versiones posteriores.
* La audiencia y el área de nombres elegidos en **Calificación de audiencias** (primer nodo) no se puede cambiar en las nuevas versiones.
* La regla de reentrada debe ser la misma en todas las versiones del recorrido.
* Un recorrido que comienza con un **Leer audiencia** no puede comenzar con otro evento en las versiones siguientes.
* No se puede crear una nueva versión de un recorrido de audiencia de lectura con lectura incremental. Debe duplicar el recorrido.

### Acciones personalizadas {#custom-actions-g}

* La URL de acción personalizada no admite parámetros dinámicos.
* Solo se admiten los métodos de llamada de POST y PUT
* El nombre del parámetro de consulta o del encabezado no debe comenzar con &quot;.&quot; o &quot;$&quot;
* No se permiten direcciones IP
* Las direcciones de Adobe internas (`.adobe.*`) no están permitidas en las direcciones URL y las API.
* Las acciones personalizadas integradas no se pueden eliminar.

### Eventos {#events-g}

* En el caso de los eventos generados por el sistema, los datos de streaming utilizados para iniciar un recorrido del cliente deben configurarse primero en Journey Optimizer para obtener un ID de orquestación único. Este ID de orquestación debe añadirse a la carga útil de streaming que llega a Adobe Experience Platform. Esta limitación no se aplica a los eventos basados en reglas.
* Los eventos empresariales no se pueden usar junto con eventos unitarios o actividades de calificación de audiencia.
* Los recorridos unitarios (que comienzan con un evento o una calificación de audiencia) incluyen una protección que evita que los recorridos se activen varias veces por error para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante cinco minutos. Por ejemplo, si un evento activa un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.
* Journey Optimizer requiere que los eventos se transmitan al servicio principal de recopilación de datos (DCCS) para poder activar un recorrido. Eventos consumidos por lotes o eventos de conjuntos de datos internos de Journey Optimizer (comentarios de mensajes, seguimiento del correo electrónico, etc.) no se puede usar para activar un recorrido. Para los casos de uso en los que no pueda obtener eventos de flujo continuo, cree una audiencia basada en esos eventos y use **Leer audiencia** actividad en su lugar. Técnicamente, la calificación de audiencias puede utilizarse, pero puede provocar desafíos descendentes en función de las acciones utilizadas.

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
* En el caso de los recorridos que utilizan una actividad Leer audiencia, existe un número máximo de recorridos que pueden comenzar al mismo tiempo. El sistema realizará los reintentos, pero evite tener más de cinco recorridos (con Leer audiencia, programados o que se inicien &quot;lo antes posible&quot;) que empiecen al mismo tiempo. Para ello, repártalos a lo largo del tiempo, por ejemplo, en intervalos de 5 y 10 minutos.

### Editor de expresiones {#expression-editor}

* Los grupos de campos de evento de experiencia no se pueden usar en recorridos que comiencen por una audiencia de lectura, una calificación de audiencia o una actividad de evento empresarial. Debe crear una audiencia nueva y utilizar una condición dentro del segmento en el recorrido.


