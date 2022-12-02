---
solution: Journey Optimizer
product: journey optimizer
title: Limitaciones y protecciones de Journey Optimizer
description: Obtenga más información acerca de las protecciones de Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 9b4ab81a362c38dce5ff4b10fb301c81ed117688
workflow-type: ht
source-wordcount: '856'
ht-degree: 100%

---

# Protecciones y limitaciones {#limitations}

Los derechos, limitaciones de productos y protecciones de rendimiento se enumeran en la [página de descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}.

A continuación, encontrará limitaciones y protecciones adicionales al utilizar [!DNL Adobe Journey Optimizer].

## Protecciones de mensajes {#message-guardrails}

* No pueden agregar archivos adjuntos a un correo electrónico con [!DNL Journey Optimizer].
* No puede utilizar el mismo dominio de envío para enviar mensajes desde [!DNL Adobe Journey Optimizer] y desde otro producto, como [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage], por ejemplo.


## Protecciones de gestión de decisiones {#offer-guardrails}

Las protecciones de rendimiento y los límites estáticos para la toma de decisiones se enumeran en la [página de descripción del producto del servicio de aplicaciones de Offer decisioning de Adobe](https://helpx.adobe.com/es/legal/product-descriptions/offer-decisioning-app-service.html){target=&quot;_blank&quot;}.


## Protecciones de las páginas de aterrizaje {#lp-guardrails}

* Solo se puede utilizar un componente **Formulario** en una sola página principal.
* El componente **Formulario** no se puede usar en subpáginas.
* No puede agregar un preencabezado a una página de aterrizaje.
* No puede seleccionar la opción **Programar usted mismo** al diseñar una página de aterrizaje principal.

## Protecciones de recorridos {#journeys-guardrails}

### Acciones generales {#general-actions-g}

* No hay restricciones de envío.
* En caso de error, se realizan tres reintentos de forma sistemática. No puede ajustar el número de reintentos según el mensaje de error recibido.
* El evento **Reacción** le permite reaccionar a las acciones predeterminadas. Obtenga más información en [esta página](../building-journeys/reaction-events.md). Si desea reaccionar a un mensaje enviado mediante una acción personalizada, debe configurar un evento dedicado.
* No puede colocar dos acciones en paralelo, debe agregarlas una tras otra.
* Normalmente, un perfil no puede estar presente varias veces en el mismo recorrido y al mismo tiempo. Si la reentrada está activada, un perfil puede volver a entrar en un recorrido, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido. [Más información](../building-journeys/end-journey.md)

### Versiones de recorridos {#journey-versions-g}

* Un recorrido que se inicia con una actividad de evento en v1 no puede comenzar con otra cosa que un evento en versiones posteriores. No puede iniciar un recorrido con un evento de **Calificación de segmentos**.
* Un recorrido que se inicia con una actividad de **Calificación de segmentos** en v1 siempre debe comenzar con una **Calificación de segmentos** en versiones posteriores.
* El segmento y el área de nombres elegidos en **Calificación de segmentos** (primer nodo) no se puede cambiar en las versiones nuevas.
* La regla de reentrada debe ser la misma en todas las versiones del recorrido.
* Un recorrido que comience por un **Segmento de lectura** no puede comenzar con otro evento en las versiones siguientes.

### Acciones personalizadas {#custom-actions-g}

* La URL de acción personalizada no admite parámetros dinámicos.
* Solo se admiten los métodos de llamada de POST y PUT
* El nombre del parámetro de consulta o del encabezado no debe comenzar con &quot;.&quot; o &quot;$&quot;
* No se permiten direcciones IP
* Las direcciones de Adobe internas (.adobe.) no se permiten.

### Eventos {#events-g}

* En el caso de los eventos generados por el sistema, los datos de streaming utilizados para iniciar un recorrido del cliente deben configurarse primero en Journey Optimizer para obtener un ID de orquestación único. Este ID de orquestación debe añadirse a la carga útil de streaming que llega a Adobe Experience Platform. Esta limitación no se aplica a los eventos basados en reglas.
* Los eventos empresariales no se pueden usar junto con eventos unitarios o actividades de calificación de segmentos.
* Los recorridos unitarios (que se inician con un evento o una calificación de segmentos) incluyen una protección que evita que los recorridos se activen varias veces de forma errónea para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante cinco minutos. Por ejemplo, si un evento activa un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.

### Fuentes de datos {#data-sources-g}

* Las fuentes de datos externas se pueden aprovechar dentro de un recorrido del cliente para buscar datos externos en tiempo real. Estas fuentes deben utilizarse mediante la API de REST, admiten JSON y pueden gestionar el volumen de solicitudes.

### Creación de recorridos y perfiles {#journeys-limitation-profile-creation}

Hay un retraso asociado a la creación/actualización de perfiles basados en la API en Adobe Experience Platform. El destinatario de nivel de servicio (SLT) en términos de latencia es &lt;1 min desde la ingesta hasta el perfil unificado para el percentil 95 de las solicitudes, a un volumen de 20 000 solicitudes por segundo (RPS).

Si un recorrido se activa simultáneamente para crear un perfil y comprueba o recupera inmediatamente la información del servicio de perfil, es posible que no funcione de forma correcta.

Puede elegir entre una de estas dos soluciones:

* Agregue una actividad de espera después del primer evento para que Adobe Experience Platform tenga el tiempo necesario para realizar la ingesta en el servicio de perfil.

* Configure un recorrido que no utilice inmediatamente el perfil. Por ejemplo, si el recorrido está diseñado para confirmar la creación de una cuenta, el evento de experiencia podría contener la información necesaria para enviar el primer mensaje de confirmación (nombre, apellidos, dirección de correo electrónico, etc.).

### Lectura de segmento {#read-segment-g}

* Los segmentos transmitidos siempre están actualizados, pero los segmentos por lotes no se calcularán en el momento de la recuperación. Solo se evalúan cada día a la hora de evaluar el lote.
* Para los recorridos que utilizan una actividad Leer segmento, existe un número máximo de recorridos que pueden comenzar al mismo tiempo. El sistema realizará los reintentos, pero evite tener más de cinco recorridos (con Leer segmento, programados o que se inicien “lo antes posible”) que empiecen al mismo tiempo. Para ello, repártalos a lo largo del tiempo, por ejemplo, en intervalos de 5 y 10 minutos.

### Editor de expresiones {#expression-editor}

* Los grupos de campos de eventos de experiencia no se pueden utilizar en recorridos que comiencen por un segmento de lectura, una calificación de segmentos o una actividad de evento empresarial.

