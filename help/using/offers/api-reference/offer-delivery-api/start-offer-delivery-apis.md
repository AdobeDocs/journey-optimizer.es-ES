---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Introducción a las API de envío de ofertas
description: Obtenga más información sobre las API disponibles para ofrecer ofertas personalizadas.
badge: label="Heredado" type="Informative"
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 7%

---

# Introducción a las API de envío de ofertas {#about-decisioning-apis}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../../experience-decisioning/gs-experience-decisioning.md)

Puede entregar ofertas mediante la API **Decisioning** o **Edge Decisioning**. Además, la API **Batch Decisioning** le permite entregar ofertas a todos los perfiles de una audiencia determinada en una llamada. El contenido de la oferta para cada perfil de la audiencia se coloca en un conjunto de datos de Adobe Experience Platform, donde está disponible para flujos de trabajo por lotes personalizados.

En esta página, encontrará información sobre funcionalidades específicas disponibles con las API **Decisioning** y **Edge Decisioning**. Aunque ambos le permiten ofrecer ofertas a sus clientes, recomendamos utilizar la API **Edge Decisioning** siempre que sea posible para casos de uso entrantes y para garantizar una mejor latencia y rendimiento en su plataforma.

Para obtener más información sobre cómo trabajar con las API, consulte estas secciones:

* [API de decisiones](decisioning-api.md)
* [API de Edge Decisioning](edge-decisioning-api.md)
* [API de decisiones por lotes](batch-decisioning-api.md)

## Funcionalidades de la API de Edge Decisioning {#edge}

**Solicitud única de eventos de experiencia y solicitudes de toma de decisiones**

Con la API de Edge Decisioning, puede enviar en una sola solicitud el propio evento de experiencia junto con la solicitud de toma de decisiones, en lugar de tener dos solicitudes diferentes.

Por ejemplo, si un cliente visita su sitio web, la solicitud incluirá el evento de experiencia (la visita del cliente a la página) y recuperará una oferta para rellenar la página visitada.

**Almacenamiento de datos de contexto en Adobe Experience Platform**

Los datos de contexto hacen referencia a datos que solo conoce en el momento en que desea recuperar una oferta. Por ejemplo, el color del artículo comprado, el tiempo en el momento de la compra, etc.

Al pasar datos de contexto con una solicitud de API de Edge Decisioning, los datos se almacenan en el perfil de Adobe Experience Platform, lo que permite su reutilización en el futuro.

>[!NOTE]
>
>Para que se almacenen los datos de contexto, debe tener configurado un esquema XDM dedicado.

**Actualización del contador de límite de frecuencia**

Si se ha habilitado el límite de frecuencia para algunas de las ofertas a fin de definir la frecuencia con la que se restablece su recuento de límite, el contador se actualiza y está disponible en una decisión de API de Edge Decisioning en menos de 3 segundos. [Aprenda a agregar restricciones a una oferta](../../offer-library/add-constraints.md)

## Funciones de API de decisiones {#decisioning}

Las funcionalidades enumeradas a continuación solo están disponibles con la API de Decisioning. Si necesita aprovechar uno de ellos para satisfacer sus necesidades, utilice la API de decisiones. De lo contrario, se recomienda utilizar las API de Edge Decisioning.

* **Contenido y características de la oferta**: puede optar por no devolver el contenido y las características de una oferta mediante una opción dedicada.
* **Metadatos de ofertas**: habilita una opción para devolver los metadatos de una oferta.
* **Política de combinación**: use en su solicitud una política de combinación diferente a la asociada a su zona protegida.
* **Eventos de toma de decisiones y límite de frecuencia**: impida que se cuenten los eventos de toma de decisiones mediante cualquier límite de frecuencia que se produzca.
* **Proposiciones duplicadas**: habilite una opción para no anular la duplicación de propuestas.
