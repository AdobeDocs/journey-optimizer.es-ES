---
title: Comenzar con API de Decisioning
description: Obtenga información sobre cómo empezar a utilizar las API de decisiones para administrar mediante programación los elementos de decisión y entregar ofertas personalizadas.
feature: API, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 78ed06a3-7787-4aab-8373-df7eb40c1727
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/01NgEXGvNxeb1MNkjeB55VNFZFuSiTfQMKeNahfuHWE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 339
ht-degree: 5%

---

# Guía para desarrolladores de API de decisiones {#decisioning-api-developer-guide}

Las API de decisiones permiten crear y administrar mediante programación los componentes utilizados para ofrecer ofertas personalizadas a los clientes. Estas API de RESTful proporcionan operaciones completas de CRUD (crear, leer, actualizar, eliminar) para elementos de decisión, estrategias de selección, reglas de elegibilidad y otros componentes de toma de decisiones.

## Autenticación {#authentication}

Antes de usar las API de Decisioning, debe configurar la autenticación para acceder a los extremos de la API. Puede consultar la [guía de autenticación de Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"} para obtener instrucciones paso a paso.

## Operaciones de API disponibles {#available-operations}

Las API de decisiones proporcionan funcionalidades de administración completas para los componentes de toma de decisiones. Están disponibles las siguientes categorías de operaciones:

* **Elementos de decisión**: cree, lea, actualice, elimine y enumere elementos de decisión que representen las ofertas o el contenido que desea entregar a los clientes.

  ➡️ [Obtenga información sobre cómo administrar los elementos de decisión](decisions-items/create.md)

* **Colecciones de elementos**: organice los elementos de decisión en colecciones para facilitar la administración y el direccionamiento mediante reglas de elegibilidad.

  ➡️ [Más información sobre cómo administrar las colecciones de elementos](items-collections/create.md)

* **Estrategias de selección**: defina cómo se seleccionan y clasifican los elementos de decisión cuando se cumplen los requisitos para la entrega de varios elementos.

  ➡️ [Aprenda a administrar estrategias de selección](selection-strategies/create.md)

* **Reglas de elegibilidad**: establezca condiciones que determinen qué perfiles cumplen los requisitos para recibir elementos de decisión específicos.

  ➡️ [Aprenda a administrar las reglas de elegibilidad](eligibility-rules/create.md)

* **Fórmulas de clasificación**: cree una lógica de clasificación personalizada para determinar el orden en que se presentan los elementos de decisión.

  ➡️ [Aprenda a administrar fórmulas de clasificación](ranking-formulas/create.md)

* **Ubicaciones**: defina las ubicaciones o los contextos en los que se pueden mostrar los elementos de decisión en las experiencias.

  ➡️ [Aprenda a administrar ubicaciones](exd-placements/create.md)

## Próximos pasos {#next-steps}

Ahora que comprende los conceptos básicos de las API de decisiones, puede continuar con las operaciones específicas:

* [Creación de elementos de decisión](decisions-items/create.md)
* [Enumerar elementos de decisión](decisions-items/decision-items-list.md)
* [Creación de estrategias de selección](selection-strategies/create.md)
* [Crear reglas de elegibilidad](eligibility-rules/create.md)

Para obtener más información sobre el uso de la toma de decisiones en campañas y recorridos, consulte la [Documentación sobre la toma de decisiones](../gs-experience-decisioning.md).

>[!NOTE]
>
>Si necesita migrar objetos de Administración de decisiones existentes a Decisioning, use la API de migración de [Decisioning dedicada](../decisioning-migration-api.md). Esta API especializada proporciona funciones automatizadas de resolución de dependencias y reversión diseñadas específicamente para tomar decisiones sobre la migración de entidades en entornos limitados.
