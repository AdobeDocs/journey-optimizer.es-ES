---
solution: Journey Optimizer
product: journey optimizer
title: Limitaciones de recorrido
description: Más información sobre las limitaciones de Recorrido
feature: Journeys, Best Practices, Guardrails
topic: Content Management
role: User
level: Intermediate
keywords: recorridos, limitación
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1276
ht-degree: 20%

---

# Limitaciones {#journey-limitations}

>[!BEGINSHADEBOX]

**En esta página:** revise las limitaciones y protecciones que se aplican a los recorridos, incluidas las acciones, las versiones, las acciones personalizadas, los eventos y las fuentes de datos.

>[!ENDSHADEBOX]

Estas son las limitaciones relacionadas con el uso de recorridos.

## Limitaciones generales de las acciones {#action-limitations}

* No hay restricciones de envío.
* En caso de error, se realizan tres reintentos de forma sistemática. No puede ajustar el número de reintentos según el mensaje de error recibido.
* El evento **Reaction** integrado le permite reaccionar a las acciones listas para usar (consulte esta [página](../building-journeys/reaction-events.md)). Si desea reaccionar a un mensaje enviado mediante una acción personalizada, debe configurar un evento dedicado.
* No puede colocar dos acciones en paralelo, debe agregarlas una tras otra.


## Limitaciones de versiones de recorrido {#journey-versions-limitations}

* Un recorrido que se inicia con una actividad de evento en v1 no puede comenzar con otra cosa que un evento en versiones posteriores. No puede iniciar un recorrido con un evento **Calificación de audiencias**.
* Un recorrido que comience con una actividad de **Calificación de audiencias** en v1 siempre debe comenzar con una **Calificación de audiencias** en versiones posteriores.
* La audiencia y el área de nombres elegidos en **Calificación de audiencias** (primer nodo) no se pueden cambiar en las nuevas versiones.
* La regla de reentrada debe ser la misma en todas las versiones del recorrido.
* El recorrido que comience con **Leer público** no puede comenzar con otro evento en las versiones siguientes.

## Limitaciones de acciones personalizadas {#custom-actions-limitations}

* La URL de acción personalizada no admite parámetros dinámicos. 
* Solo se admiten los métodos de llamada de POST y PUT. 
* El nombre del parámetro de consulta o del encabezado no debe comenzar con &quot;.&quot; o &quot;$&quot;. 
* No se permiten direcciones IP. 
* Las direcciones internas de Adobe (.adobe.) no están permitidas.

## Limitaciones de eventos {#events-limitations}

* En el caso de los eventos generados por el sistema, los datos de streaming utilizados para iniciar un recorrido del cliente deben configurarse primero en Journey Optimizer para obtener un ID de orquestación único. Este identificador de orquestación debe agregarse a la carga útil de streaming que entra en [!DNL Adobe Experience Platform]. Esta limitación no se aplica a los eventos basados en reglas.

## Limitaciones de eventos de reacción {#reaction-limitations}

* Las actividades **[!UICONTROL Reaction]** deben colocarse inmediatamente después de una [actividad de acción del canal](../building-journeys/journey-action.md) en el lienzo de recorrido. No se admite la colocación de una actividad **[!UICONTROL Wait]** o cualquier otra actividad entre la acción del canal y la actividad **[!UICONTROL Reaction]**, lo que puede provocar que la reacción no funcione según lo esperado. Obtenga más información en [esta sección](../building-journeys/reaction-events.md).

## Limitaciones de fuentes de datos {#data-sources-limitations}

* Las fuentes de datos externas se pueden aprovechar dentro de un recorrido de cliente para buscar datos externos en tiempo real. Estas fuentes deben utilizarse mediante la API de REST, admiten JSON y pueden gestionar el volumen de solicitudes.

## Recorridos que comienzan al mismo tiempo que la creación de un perfil {#journeys-limitation-profile-creation}

Hay un retraso asociado a la creación/actualización de perfiles basados en API en [!DNL Adobe Experience Platform]. El destinatario de nivel de servicio (SLT) en términos de latencia es &lt;1 min desde la ingesta hasta el perfil unificado para el percentil 95 de las solicitudes, a un volumen de 20 000 solicitudes por segundo (RPS).

Si un Recorrido se activa simultáneamente para crear un perfil y comprueba o recupera inmediatamente la información del servicio de perfil, es posible que no funcione correctamente.

Puede elegir entre una de estas dos soluciones:

* Agregue una actividad de espera después del primer evento para que [!DNL Adobe Experience Platform] tenga el tiempo necesario para realizar la ingesta en el servicio de perfil.

* Configure un recorrido que no utilice inmediatamente el perfil. Por ejemplo, si el recorrido está diseñado para confirmar la creación de una cuenta, el evento de experiencia podría contener la información necesaria para enviar el primer mensaje de confirmación (nombre, apellidos, dirección de correo electrónico, etc.).

## Leer las limitaciones de audiencia {#read-audiences-limitations}

* Los públicos transmitidos siempre están actualizados, pero los públicos por lotes no se calcularán en el momento de la recuperación. Solo se evalúan cada día a la hora de evaluar el lote.

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se enumeran las limitaciones técnicas más estrictas que se aplican a las acciones de recorrido, las versiones de recorrido, las acciones personalizadas, los eventos, los eventos de reacción, las fuentes de datos y la lectura de audiencias en Adobe Journey Optimizer.

**Intenciones:**

* Comprender los límites de envío y reintentos de las acciones de recorrido
* Descubra qué transiciones de versión de recorrido se permiten o bloquean
* Identificar restricciones en la configuración de la dirección URL, el método y el encabezado de la acción personalizada
* Comprender los requisitos de fuentes de datos para la integración de sistemas externos
* Evite problemas de temporización al iniciar un recorrido en el mismo momento que la creación del perfil

**Glosario:**

* **Evento de reacción**: una actividad de recorrido que escucha la interacción de un perfil con una acción de canal (por ejemplo, un correo electrónico abierto o un clic); debe colocarse inmediatamente después de la actividad de acción de canal. *(específico del producto)*
* **Evento basado en reglas**: Tipo de evento en el que el déclencheur se define mediante una condición lógica en lugar de un identificador de orquestación generado por el sistema. *(específico del producto)*
* **SLT (Destinatario de nivel de servicio)**: El punto de referencia de latencia para la creación/actualización de perfiles basados en API en Adobe Experience Platform — menos de 1 minuto desde la ingesta hasta el Perfil unificado en el percentil 95 para 20.000 RPS.

**Protecciones:**

* No se aplica ninguna restricción de envío; se realizan tres reintentos automáticamente por error y no se pueden ajustar
* Dos acciones no se pueden ejecutar en paralelo; deben agregarse secuencialmente
* Un recorrido que comience con una actividad de evento en v1 no puede comenzar con una actividad que no sea de evento en versiones posteriores
* Un recorrido que comience con una Calificación de audiencias en v1 siempre debe comenzar con Calificación de audiencias en todas las versiones posteriores; la audiencia y el área de nombres no se pueden cambiar
* Un recorrido que comience por Leer audiencia no puede comenzar con un evento diferente en las versiones siguientes
* La URL de acción personalizada no admite parámetros dinámicos; solo se admiten los métodos de llamada POST y PUT
* El parámetro de consulta de acción personalizada y los nombres de encabezado no deben comenzar con &quot;&quot;. o &quot;$&quot;; direcciones IP y direcciones internas de Adobe (.adobe.) no se permiten
* Las actividades de reacción deben colocarse inmediatamente después de una actividad de acción del canal; no se admite la inserción de una actividad de espera u otra actividad entre ellas
* Las fuentes de datos externas deben ser accesibles a través de la API de REST, admiten JSON y administran el volumen de solicitud
* Las audiencias de lote solo se evalúan una vez al día a la hora de evaluar el lote diario; no se vuelven a calcular a la hora de recuperar los datos
* Cuando se activa un recorrido simultáneamente con la creación de un perfil, es posible que los datos de perfil aún no estén disponibles debido a la latencia de ingesta de Platform

**Terminología:**

* Nombre canónico: limitaciones de Recorrido — Acrónimo: none — variantes: barreras de recorrido, restricciones de recorrido
* No confunda: &quot;Limitación de eventos de reacción&quot; ≠ &quot;Limitación de acciones generales&quot;: el evento de reacción debe colocarse directamente después de una acción de canal; la limitación de acciones generales cubre reintentos, paralelismo y regulación

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Cuántas veces reintenta Journey Optimizer una acción fallida?** — Se realizan tres reintentos automáticamente; no se puede configurar el número de reintentos.
* **Q: ¿Puedo colocar una actividad de espera entre una acción del canal y un evento de reacción?** — No; el evento de reacción debe colocarse inmediatamente después de la actividad de acción del canal. No se admite la adición de ninguna actividad intermedia, lo que puede hacer que el evento de reacción no funcione según lo esperado.
* **Q: ¿Puedo cambiar el primer tipo de evento al crear una nueva versión del recorrido?** — No; el mecanismo de entrada establecido en v1 debe conservarse en todas las versiones posteriores. Un recorrido que comience por un evento debe continuar iniciándose con un evento y un recorrido que comience por Calificación de audiencias debe comenzar siempre con Calificación de audiencias.
* **Q: ¿Por qué podría no funcionar mi recorrido cuando se activa al mismo tiempo que se crea un perfil?** — La creación de perfiles mediante API tiene una latencia antes de que los datos estén disponibles en el perfil unificado (SLT &lt; 1 minuto con un percentil 95). Añadir una actividad de Espera después del primer evento da tiempo a Platform para completar la ingesta.
* **Q: ¿Las audiencias de streaming siempre están actualizadas en recorrido?** — Sí; las audiencias de streaming siempre están actualizadas. Las audiencias de lote, sin embargo, solo se evalúan una vez al día en el momento de la evaluación diaria del lote, no en el momento de la recuperación.

+++
