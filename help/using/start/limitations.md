---
title: Limitaciones de Journey Optimizer
description: Obtenga más información sobre las limitaciones de Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 3c8c059e5e3953807b9fc2d8d0eded0d00e49003
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 3%

---

# Limitaciones {#limitations}

Los derechos, limitaciones de productos y protecciones de rendimiento se enumeran en[ Página de descripción del producto de Adobe Journey Optimizer](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html?lang=es){target=&quot;_blank&quot;}.

A continuación se indican algunas limitaciones adicionales al usar [!DNL Adobe Journey Optimizer].

## Limitaciones en los mensajes {#limitations-messages}

* No se pueden añadir archivos adjuntos a un correo electrónico con [!DNL Journey Optimizer].
* El CCO de correo electrónico no es compatible con [!DNL Journey Optimizer].
* No puede utilizar el mismo dominio de envío para enviar mensajes desde [!DNL Adobe Journey Optimizer] y de otro producto, como [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage] por ejemplo.

## Limitaciones en los recorridos {#limitations-journeys}

### Acciones generales {#general-actions}

* No hay restricciones de envío.
* En caso de error, se realizan tres reintentos de forma sistemática. No se puede ajustar el número de reintentos según el mensaje de error recibido.
* El **Reacción** le permite reaccionar a las acciones integradas. Obtenga más información en [esta página](../building-journeys/reaction-events.md). Si desea reaccionar a un mensaje enviado mediante una acción personalizada, debe configurar un evento dedicado.
* No puede colocar dos acciones en paralelo, debe agregarlas una tras otra.

### Acción de mensaje {#message-action}

* Al añadir un mensaje multicanal, se envían dos mensajes.

### Versiones de recorridos {#journey-versions-limitations}

* Un recorrido que comience con una actividad de evento en v1 no puede comenzar con otra cosa que un evento en versiones posteriores. No se puede iniciar un recorrido con un **Clasificación del segmento** evento.
* Un recorrido que comience por un **Clasificación del segmento** la actividad en v1 siempre debe comenzar con un **Clasificación del segmento** en versiones posteriores.
* El segmento y el área de nombres elegidos en **Clasificación del segmento** (primer nodo) no se puede cambiar en las versiones nuevas.
* La regla de reentrada debe ser la misma en todas las versiones de recorrido.
* Un recorrido que comience por un **Leer segmento** no puede comenzar con otro evento en las versiones siguientes.

### Acciones personalizadas {#custom-actions}

* La dirección URL de acción personalizada no admite parámetros dinámicos.
* Solo se admiten los métodos de llamada de POST y PUT
* El nombre del parámetro de consulta o del encabezado no debe comenzar por &quot;.&quot; o &quot;$&quot;
* No se permiten direcciones IP
* Direcciones de Adobe internas (.adobe). no están permitidos.

### Eventos {#events}

* En el caso de los eventos generados por el sistema, los datos de flujo utilizados para iniciar un recorrido de cliente deben configurarse primero en Journey Optimizer para obtener un ID de organización único. Este ID de organización debe añadirse a la carga útil de flujo continuo que llega a Adobe Experience Platform. Esta limitación no se aplica a los eventos basados en reglas.

### Fuentes de datos {#data-sources}

* Las fuentes de datos externas se pueden aprovechar dentro de un recorrido de clientes para buscar datos externos en tiempo real. Estas fuentes deben utilizarse mediante la API de REST, admiten JSON y pueden gestionar el volumen de solicitudes.

### Recorridos que comienzan al mismo tiempo que la creación de perfiles {#journeys-limitation-profile-creation}

Hay un retraso asociado a la creación/actualización de perfiles basado en API en Adobe Experience Platform. El objetivo de nivel de servicio (SLT) en términos de latencia es &lt; 1 min desde la ingesta hasta el perfil unificado para el percentil 95 de las solicitudes, a un volumen de 20 000 solicitudes por segundo (RPS).

Si un recorrido se activa simultáneamente para crear un perfil y comprueba o recupera inmediatamente la información del servicio de perfil, es posible que no funcione correctamente.

Puede elegir entre una de estas dos soluciones:

* Agregue una actividad de espera después del primer evento para que Adobe Experience Platform tenga el tiempo necesario para realizar la ingesta en el servicio de perfil.

* Configure un recorrido que no aproveche inmediatamente el perfil. Por ejemplo, si el recorrido está diseñado para confirmar la creación de una cuenta, el evento de experiencia podría contener la información necesaria para enviar el primer mensaje de confirmación (nombre, apellidos, dirección de correo electrónico, etc.).

### Lectura de segmento {#read-segment}

* Los segmentos transmitidos siempre están actualizados, pero los segmentos por lotes no se calcularán en el momento de la recuperación. Solo se evalúan diariamente a la hora diaria de evaluar el lote.
