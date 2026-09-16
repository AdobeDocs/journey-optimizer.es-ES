---
solution: Journey Optimizer
product: journey optimizer
title: Herramientas de administración de contenido de CX Coworker
description: Descubra las herramientas de administración de contenido de CX Coworker disponibles para detectar, crear y administrar recursos de contenido de Journey Optimizer, con instrucciones detalladas y muestras de mensajes.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 9f23a6f5-7221-4f87-95cd-047955ca33d5
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
    internal-label: Content management
subfeature_v2:
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
    internal-label: Templates
source-git-commit: 1d3f1b700dc00187365abf614f0992522172253c
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 2%
---

# Herramientas de administración de contenido de CX Coworker {#content-management-coworker-skills}

>[!BEGINSHADEBOX]

**En esta página:** Descubra las herramientas de administración de contenido de CX Coworker disponibles en Adobe Journey Optimizer para examinar, crear, actualizar, clonar y publicar plantillas de contenido, fragmentos, páginas de aterrizaje y contenido en línea de recorrido/campaña, con instrucciones detalladas, mensajes de ejemplo y prácticas recomendadas.

Más información:

* [Aptitudes de CX Coworker para Journey Optimizer](ai-features.md#cx-coworker-skills): información general sobre las aptitudes de CX Coworker en todos los Recorridos, lealtad y administración de contenido en Journey Optimizer.
* [Documentación de CX Coworker](https://experienceleague.adobe.co/es/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"}: Información general sobre las funciones de campañas, chat y proyectos de los compañeros.
* [Guía de la interfaz de usuario de Coworker Chat](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"}: cómo acceder y navegar por Coworker Chat.

>[!ENDSHADEBOX]

## Herramientas de administración de contenido {#content-management}

>[!AVAILABILITY]
>
>La administración de contenido está disponible para todos los clientes que tienen acceso a CX Coworker.

Los usuarios de Journey Optimizer pueden detectar y administrar recursos de contenido (plantillas de contenido, fragmentos, páginas de aterrizaje y contenido de mensajes en línea de recorrido/campaña) directamente desde CX Coworker con indicaciones en lenguaje natural. Permite pasar de &quot;hablarme sobre mi contenido&quot; a &quot;compilarlo, actualizarlo y publicarlo&quot;, sin abandonar la conversación. Esta capacidad está equipada con 15 herramientas de MCP con capacidad de lectura y escritura para el contenido de Journey Optimizer.

### Casos de uso clave

1. **Examinar e inspeccionar contenido**

   * Enumere las plantillas de contenido, los fragmentos o las páginas de aterrizaje disponibles y recupere su estructura, metadatos y estado.
   * Recupere el contenido del mensaje en línea configurado en un nodo de recorrido o de acción de campaña.

   Ejemplos de mensajes:
   * &quot;Enumerar mis plantillas de contenido de correo electrónico&quot;.
   * &quot;Mostrarme los fragmentos disponibles para mi campaña de verano&quot;.
   * &quot;Obtenga los detalles de la página de aterrizaje página-123&quot;.
   * &quot;¿Qué contenido está configurado para la variante de correo electrónico del nodo de acción en campaign camp-789?&quot;

1. **Crear plantillas de contenido**

   * Cree una nueva plantilla de contenido para cualquier canal.

   Ejemplos de mensajes:
   * &quot;Cree una plantilla de correo electrónico denominada Rebajas de verano con este contenido de HTML&quot;.
   * &quot;Cree una nueva plantilla de SMS llamada Alerta Flash&quot;.

1. **Actualizar plantillas de contenido**

   * Reemplazar completamente el contenido de una plantilla existente.

   Ejemplos de mensajes:
   * &quot;Actualice la plantilla abc-123 con este nuevo cuerpo de HTML&quot;.

1. **Crear, actualizar, clonar y publicar fragmentos**

   * Cree un nuevo HTML o fragmento de expresión.
   * Actualizar el contenido o los metadatos de un fragmento existente.
   * Clonar un fragmento existente con un nombre nuevo.
   * Envíe un fragmento de borrador para su publicación.

   Ejemplos de mensajes:
   * &quot;Cree un fragmento de HTML llamado Banner de promoción con este marcado&quot;.
   * &quot;Actualice el fragmento frag-456 para cambiar su nombre a Banner promocional V2.&quot;
   * &quot;Clonar el fragmento abc-123 como titular de la promoción - Verano (Variante B).&quot;
   * &quot;Publicar fragmento frag-456&quot;.

1. **Actualizar contenido de mensaje en línea**

   * Reemplace una variante de canal en el mensaje en línea de un nodo de acción de recorrido o campaña.
   * Enumerar las variantes de canal definidas en un nodo de recorrido o de acción de campaña.

   Ejemplos de mensajes:
   * &quot;Actualice la variante de correo electrónico del nodo de acción en campaign camp-789 con este nuevo contenido&quot;.
   * &quot;¿Qué variantes de canal se definen en este nodo de acción?&quot;

### En ámbito

La administración de contenido admite las siguientes funciones:

* **Enumerar y obtener plantillas de contenido**: Examine las plantillas de contenido y recupere su estructura y metadatos.
* **Enumerar y obtener fragmentos**: Examine fragmentos de contenido y expresión y recupere sus detalles.
* **Enumerar y obtener páginas de aterrizaje**: Examine páginas de aterrizaje y recupere sus metadatos y contenido de página.
* **Obtener contenido en línea de campaña/recorrido**: recupere el contenido del mensaje en línea configurado en un nodo de acción de campaña o recorrido, incluidas las variantes multilingües.
* **Crear plantillas de contenido**: cree una nueva plantilla para cualquier canal.
* **Actualizar plantillas de contenido**: reemplace completamente el contenido de una plantilla existente.
* **Crear, actualizar, clonar y publicar fragmentos**: cree nuevos fragmentos, actualice los existentes, clone un fragmento con un nuevo nombre y envíe un borrador de fragmento para su publicación.
* **Actualizar contenido de mensajes en línea**: reemplace una variante de canal en el mensaje en línea de un nodo de acción de campaña/recorrido, incluidas las variantes multilingües, y enumere las variantes de canal definidas en un nodo de acción.

### Fuera de ámbito

Actualmente no se admiten las siguientes funcionalidades:

* **Búsqueda de texto completo en plantillas o fragmentos**
* **Validación de plantilla o fragmento** (referencias huérfanas, vínculos rotos, componentes obsoletos)
* **Creando o publicando páginas de aterrizaje**
* **Eliminando plantillas de contenido, fragmentos o páginas de aterrizaje**

### Impulso de las prácticas recomendadas

1. **ID de referencia conocidos**: proporcione la plantilla, el fragmento, la página de aterrizaje o el ID de campaña/recorrido cuando solicite obtener, actualizar, clonar o publicar un recurso específico.
1. **Sea explícito sobre el canal**: Al crear una plantilla o un fragmento, especifique el canal o el tipo de contenido (correo electrónico, fragmento de HTML, fragmento de expresión).
1. **Confirmar antes de publicar**: revise el contenido de un fragmento después de crearlo o actualizarlo antes de pedir a su compañero que lo publique.
1. **Proporcionar contenido de reemplazo completo**: las operaciones de actualización reemplazan el contenido por completo, de modo que incluya el cuerpo completo de HTML o el contenido de variante en el mensaje.

{{$include /help/_includes/do-not-localize/start/ai-augmented-content-management-coworker-skills.md}}
