---
solution: Journey Optimizer
product: journey optimizer
title: Limitaciones de recorrido
description: Más información sobre las limitaciones de Recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: recorridos, limitación
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: aced11ffd80bcc0d79ef2e094b05dde8cb9a6248
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 65%

---

# Limitaciones {#journey-limitations}

Estas son las limitaciones relacionadas con el uso de recorridos.

## Limitaciones generales de las acciones {#action-limitations}

* No hay restricciones de envío. 
* En caso de error, se realizan tres reintentos de forma sistemática. No puede ajustar el número de reintentos según el mensaje de error recibido. 
* La función integrada **Reacción** Este evento le permite reaccionar a las acciones listas para usar (consulte esto [página](../building-journeys/reaction-events.md)). Si desea reaccionar a un mensaje enviado mediante una acción personalizada, debe configurar un evento dedicado. 
* No puede colocar dos acciones en paralelo, debe agregarlas una tras otra.

## Limitaciones de versiones de recorrido {#journey-versions-limitations}

* Un recorrido que se inicia con una actividad de evento en v1 no puede comenzar con otra cosa que un evento en versiones posteriores. No se puede iniciar un recorrido con un **Calificación de audiencias** evento.
* Un recorrido que comienza con un **Calificación de audiencias** la actividad en v1 siempre debe comenzar con una **Calificación de audiencias** en versiones posteriores.
* La audiencia y el área de nombres elegidos en **Calificación de audiencias** (primer nodo) no se puede cambiar en las nuevas versiones.
* La regla de reentrada debe ser la misma en todas las versiones del recorrido.
* Un recorrido que comienza con un **Leer audiencia** no puede comenzar con otro evento en las versiones siguientes.
 
## Limitaciones de acciones personalizadas {#custom-actions-limitations}

* La URL de acción personalizada no admite parámetros dinámicos. 
* Solo se admiten los métodos de llamada de POST y PUT. 
* El nombre del parámetro de consulta o del encabezado no debe comenzar con &quot;.&quot; o &quot;$&quot;. 
* No se permiten direcciones IP. 
* Las direcciones de Adobe internas (.adobe.) no se permiten.
 
## Limitaciones de eventos {#events-limitations}

* En el caso de los eventos generados por el sistema, los datos de streaming utilizados para iniciar un recorrido del cliente deben configurarse primero en Journey Optimizer para obtener un ID de orquestación único. Este ID de orquestación debe añadirse a la carga útil de streaming que llega a Adobe Experience Platform. Esta limitación no se aplica a los eventos basados en reglas.
 
## Limitaciones de fuentes de datos {#data-sources-limitations}

* Las fuentes de datos externas se pueden aprovechar dentro de un recorrido de cliente para buscar datos externos en tiempo real. Estas fuentes deben utilizarse mediante la API de REST, admiten JSON y pueden gestionar el volumen de solicitudes.

## Recorridos que comienzan al mismo tiempo que la creación de un perfil {#journeys-limitation-profile-creation}

Hay un retraso asociado a la creación/actualización de perfiles basados en la API en Adobe Experience Platform. El destinatario de nivel de servicio (SLT) en términos de latencia es &lt;1 min desde la ingesta hasta el perfil unificado para el percentil 95 de las solicitudes, a un volumen de 20 000 solicitudes por segundo (RPS).

Si un Recorrido se activa simultáneamente para crear un perfil y comprueba o recupera inmediatamente la información del servicio de perfil, es posible que no funcione correctamente.

Puede elegir entre una de estas dos soluciones:

* Agregue una actividad de espera después del primer evento para que Adobe Experience Platform tenga el tiempo necesario para realizar la ingesta en el servicio de perfil.

* Configure un recorrido que no utilice inmediatamente el perfil. Por ejemplo, si el recorrido está diseñado para confirmar la creación de una cuenta, el evento de experiencia podría contener la información necesaria para enviar el primer mensaje de confirmación (nombre, apellidos, dirección de correo electrónico, etc).

## Leer las limitaciones de audiencia {#read-audiences-limitations}

* Las audiencias transmitidas siempre están actualizadas, pero las audiencias por lotes no se calcularán en el momento de la recuperación. Solo se evalúan cada día a la hora de evaluar el lote.
