---
title: Limitaciones de recorrido
description: Obtenga más información sobre las limitaciones de Recorrido
feature: Recorridos
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: 12623f6f8a9571673b2b498a02da39608344ef1e
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Limitaciones {#journey-limitations}

Estas son limitaciones relacionadas con el uso de recorridos.

## Limitaciones generales de acciones

* No hay restricciones de envío. 
* En caso de error, se realizan tres reintentos de forma sistemática. No se puede ajustar el número de reintentos según el mensaje de error recibido. 
* El evento **Reaction** integrado le permite reaccionar ante las acciones integradas (consulte esta [página](../building-journeys/reaction-events.md)). Si desea reaccionar a un mensaje enviado mediante una acción personalizada, debe configurar un evento dedicado. 
* No puede colocar dos acciones en paralelo, debe agregarlas una tras otra.

## Limitaciones de las acciones del mensaje

* Al añadir un mensaje multicanal, se envían dos mensajes.

## Limitaciones de las versiones de recorrido {#journey-versions-limitations}

* Un recorrido que comience con una actividad de evento en v1 no puede comenzar con otra cosa que un evento en versiones posteriores. No se puede iniciar un recorrido con un evento **Segment Qualification**.
* Un recorrido que comience con una actividad **Segment Qualification** en v1 siempre debe comenzar con **Segment Qualification** en versiones posteriores.
* El segmento y el área de nombres elegidos en **Segment Qualification** (primer nodo) no se pueden cambiar en las nuevas versiones.
* La regla de reentrada debe ser la misma en todas las versiones de recorrido.
* Un recorrido que comience por un **segmento de lectura** no puede comenzar con otro evento en las versiones siguientes.
 

## Limitaciones de acciones personalizadas

* La dirección URL de acción personalizada no admite parámetros dinámicos. 
* Solo se admiten métodos de llamada de POST y PUT. 
* El nombre del parámetro de consulta o del encabezado no debe comenzar por &quot;.&quot; o &quot;$&quot;. 
* No se permiten direcciones IP. 
* Direcciones de Adobe internas (.adobe). no están permitidos.
 

## Limitaciones de eventos

* En el caso de los eventos generados por el sistema, los datos de flujo utilizados para iniciar un recorrido de cliente deben configurarse primero en Journey Optimizer para obtener un ID de organización único. Este ID de organización debe añadirse a la carga útil de flujo continuo que llega a Adobe Experience Platform. Esta limitación no se aplica a los eventos basados en reglas.
 

## Limitaciones de las fuentes de datos

* Las fuentes de datos externas se pueden aprovechar dentro de un recorrido de clientes para buscar datos externos en tiempo real. Estas fuentes deben utilizarse mediante la API de REST, admiten JSON y pueden gestionar el volumen de solicitudes.

## Recorridos que comienzan al mismo tiempo que una creación de perfil {#journeys-limitation-profile-creation}

Hay un retraso asociado a la creación/actualización de perfiles basado en API en Adobe Experience Platform. El objetivo de nivel de servicio (SLT) en términos de latencia es &lt; 1 min desde la ingesta hasta el perfil unificado para el percentil 95 de las solicitudes, a un volumen de 20 000 solicitudes por segundo (RPS).

Si un Recorrido se activa simultáneamente para crear un perfil y comprueba o recupera inmediatamente la información del servicio de perfil, es posible que no funcione correctamente.

Puede elegir entre una de estas dos soluciones:

* Agregue una actividad de espera después del primer evento para que Adobe Experience Platform tenga el tiempo necesario para realizar la ingesta en el servicio de perfil.

* Configure un recorrido que no aproveche inmediatamente el perfil. Por ejemplo, si el recorrido está diseñado para confirmar la creación de una cuenta, el evento de experiencia podría contener la información necesaria para enviar el primer mensaje de confirmación (nombre, apellidos, dirección de correo electrónico, etc.).

## Leer limitaciones de segmentos

* No es posible realizar el déclencheur de un recorrido basado en segmentos en un lapso de tiempo inferior a 1 hora.
* Los segmentos transmitidos siempre están actualizados, pero los segmentos por lotes no se calcularán en el momento de la recuperación. Solo se evalúan diariamente a la hora diaria de evaluar el lote.
