---
solution: Journey Optimizer
product: journey optimizer
title: Propiedades del recorrido
description: Más información sobre las propiedades del recorrido
feature: Journeys
role: Developer
level: Experienced
keywords: recorrido, expresión, editor, propiedades
exl-id: eb1ab0ed-90bd-4613-b63d-b28693947db2
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/f2FVDYuWN9tawdgRdCffwnXNXoI-e-ZAuYAaozoHd3g
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1103
ht-degree: 1%

---

# atributos de propiedades de recorrido {#journey-properties}

En el [editor de expresiones simple](../conditions.md#about_condition) y en el [editor de expresiones avanzadas](../expression/expressionadvanced.md), debajo de las categorías **Evento** y **Fuente de datos**, puede tener acceso a la categoría **Propiedades del Recorrido**. Esta categoría contiene campos técnicos relacionados con el recorrido de un perfil determinado. Esta es la información recuperada por el sistema de las recorridos activas, como el ID de recorrido, o los errores específicos encontrados.

![](../assets/journey-properties.png)

Contiene información, por ejemplo, sobre:

* versión de recorrido: uid de recorrido, uid de versión de recorrido, uid de instancia, etc.
* errores: captura de datos, ejecución de acciones, etc.
* paso actual, último paso actual, etc.
* perfiles descartados

  La lista de campos está disponible [en esta sección](#journey-properties-fields).

Puede utilizar estos campos para crear expresiones. Durante la ejecución del recorrido, los valores se recuperan directamente del recorrido.

A continuación se muestran algunos ejemplos de casos de uso:

* **Registrar perfiles descartados**: puede enviar todos los perfiles excluidos de un mensaje mediante una regla de límite a un sistema de terceros para realizar el registro. Para ello, se configura una ruta en caso de tiempo de espera y error y se añade una condición para filtrar por un tipo de error específico, por ejemplo: &quot;descartar personas por regla de límite&quot;. A continuación, puede insertar los perfiles descartados en un sistema de terceros mediante una acción personalizada.

* **Enviar alertas en caso de errores**: puede enviar una notificación a un sistema de terceros cada vez que se produzca un error en un mensaje. Para ello, se configura una ruta en caso de error, se añade una condición y una acción personalizada. Puede enviar una notificación en un canal de Slack, por ejemplo, con la descripción del error encontrado.

* **Refinar errores en los informes** : en lugar de tener una sola ruta para los mensajes erróneos, puede definir una condición por tipo de error. Esto le permitirá refinar los informes y ver todos los datos de tipos de errores.

## Lista de campos {#journey-properties-fields}

| Categoría | Nombre del campo | Etiqueta | Descripción |
|---|---|---|------------|
| Versión de recorrido | journeyUID | Identificador de recorrido | |
| | journeyVersionUID | Identificador de versión de recorrido | |
| | journeyVersionName | Nombre de versión de recorrido | |
| | journeyVersionDescription | Descripción de versión de recorrido | |
| | journeyVersion | Versión de recorrido | |
| Instancia de recorrido | instanceUID | Identificador de instancia de recorrido | ID de la instancia |
| | externalKey | Clave externa | Identificador individual que activa el recorrido |
| | organizationId | Identificador de organización | Organización de la marca |
| | sandboxName | Nombre de zona protegida | Nombre de la zona protegida |
| Identidad | profileId | Identificador de identidad del perfil | Identificador del perfil en el recorrido |
| | namespace | Área de nombres de identidad de perfil | Área de nombres del perfil en la recorrido (ejemplo: ECID) |
| Nodo actual | currentNodeId | Identificador del nodo actual | Identificador de la actividad actual (nodo) |
| | currentNodeName | Nombre del nodo actual | Nombre de la actividad actual (nodo) |
| Nodo anterior | previousNodeId | Identificador de nodo anterior | Identificador de la actividad anterior (nodo) |
| | previousNodeName | Nombre de nodo anterior | Nombre de la actividad anterior (nodo) |
| Errores | lastNodeUIDInError | Último identificador de nodo con error | Identificador de la actividad (nodo) más reciente con error |
| | lastNodeNameInError | Último nombre de nodo con error | Nombre de la última actividad (nodo) con error |
| | lastNodeTypeInError | Último tipo de nodo con error | Tipo de error de la actividad (nodo) más reciente. Tipos posibles:<ul><li>Eventos: Eventos, Reacciones, SQ (ejemplo: Calificación de audiencias)</li><li>Control de flujo: Fin, condición, espera</li><li>Acciones: Acciones de ACS, Salto, Acción personalizada</li></ul> |
| | lastErrorCode | Último código de error | Código de error de la última actividad (nodo). Posibles errores: <ul><li>Códigos de error HTTP</li><li>tapado</li><li>timeout</li><li>error (ejemplo: predeterminado en caso de error inesperado. (No debería suceder/muy raramente)</li></ul> |
| | lastExecutedActionErrorCode | Código de error de la última acción ejecutada | Código de error de la última acción por error |
| | lastDataFetchErrorCode | Último código de error de recuperación de datos | Código de error de la última recuperación de datos de las fuentes de datos |
| Fecha | lastActionExecutionElapsedTime | Tiempo transcurrido en la última ejecución de la acción | Tiempo empleado para ejecutar la acción más reciente |
| | lastDataFetchElapsedTime | Tiempo transcurrido en la última recuperación de datos | Tiempo empleado para ejecutar la captura de datos más reciente de las fuentes de datos |

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página describe la categoría Propiedades de Recorrido en el editor de expresiones: un conjunto de campos técnicos sobre la instancia de recorrido activa (ID, errores, nodos actuales/anteriores, tiempos transcurridos) que se pueden utilizar para generar expresiones para el registro, las alertas y los informes específicos de errores.

**Intenciones:**

* Acceda a los campos Propiedades de Recorrido en el editor de expresiones simples o avanzadas para hacer referencia a los metadatos de recorrido en directo
* Cree una condición que filtre los perfiles descartados por tipo de error para enrutarlos a un sistema de registro de terceros
* Enviar alertas de error a un canal externo (por ejemplo, Slack) haciendo referencia al último código de error y al nombre del nodo en una acción personalizada
* Restrinja el informe de errores de recorrido creando rutas de condición independientes por tipo de error con `lastNodeTypeInError` y `lastErrorCode`
* Identificadores de versión de recorrido de referencia, identificadores de instancia y nombre de zona protegida en expresiones para seguimiento y auditoría

**Glosario:**

* **Propiedades de Recorrido**: categoría del editor de expresiones que contiene campos de metadatos técnicos para la instancia de ejecución de recorrido actual *(específica del producto)*
* **instanceUID**: El identificador único de la instancia de recorrido para la ejecución de un perfil determinado *(específico del producto)*
* **lastErrorCode**: El código de error de la actividad fallida más reciente en el recorrido; los valores posibles incluyen códigos HTTP, `capped`, `timedOut` y `error` *(específico del producto)*
* **lastNodeTypeInError**: El tipo de la última actividad que encontró un error; puede ser Eventos, Control de flujo o Acciones *(específicas del producto)*
* **externalKey**: El identificador individual (por ejemplo, el identificador de perfil) que activó la instancia de recorrido *(específica del producto)*

**Protecciones:**

* Los valores del campo Propiedades de recorrido se recuperan directamente de la recorrido activa en el momento de la ejecución y no están disponibles para la validación previa a la ejecución
* El campo `lastErrorCode` utiliza valores predefinidos: códigos de error HTTP, `capped`, `timedOut` y `error`
* Las Propiedades de recorrido están disponibles en los editores de expresiones simples y avanzados, en la categoría Propiedades de Recorrido

**Terminología:**

* Nombre canónico: Propiedades de Recorrido — Acrónimo: none — variantes: campos técnicos de recorrido, campos de metadatos de recorrido
* Sinónimos: &quot;Propiedades de Recorrido&quot; = &quot;Campos técnicos de recorrido&quot;; &quot;instanceUID&quot; = &quot;Identificador de instancia de recorrido&quot;
* No confunda: journeyUID (identifica la definición del recorrido) ≠ instanceUID (identifica la ejecución del recorrido por parte de un perfil específico)

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Dónde se encuentran los campos Propiedades de Recorrido en el editor de expresiones?** — Aparecen en los editores de expresiones simples y avanzados en la categoría Propiedades del Recorrido, debajo de Eventos y Fuentes de datos.
* **Q: ¿Cómo puedo registrar los perfiles descartados por una regla de límite?** — Añada un filtro de condición de ruta de error en `lastErrorCode == "capped"` e inserte esos perfiles en un sistema de terceros mediante una acción personalizada.
* **Q: ¿Cuál es la diferencia entre `journeyUID` y `instanceUID`?** — `journeyUID` identifica la definición de recorrido; `instanceUID` identifica una instancia de ejecución específica para un perfil determinado.
* **Q: ¿Qué código de error se devolvió por un error inesperado del sistema?** — El código `error`, que se usa como predeterminado para errores inesperados y que rara vez debería producirse.
* **Q: ¿Puedo usar los campos de Propiedades de Recorrido para enviar alertas de Slack sobre errores de acción?** — Sí; hacer referencia a `lastNodeNameInError` y `lastErrorCode` en una acción personalizada para incluir detalles de error en una notificación de Slack.

+++
