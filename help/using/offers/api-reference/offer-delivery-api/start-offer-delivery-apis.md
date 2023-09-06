---
title: Introducción a las API de envío de ofertas
description: Obtenga más información sobre las API disponibles para ofrecer ofertas personalizadas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: ccc3ad2b186a64b9859a5cc529fe0aefa736fc00
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 4%

---

# Introducción a las API de envío de ofertas {#about-decisioning-apis}

Puede enviar ofertas utilizando las opciones **Decisioning** o el **Edge Decisioning** API. Además, la variable **Toma de decisiones por lotes** La API permite enviar ofertas a todos los perfiles de una audiencia determinada en una llamada. El contenido de la oferta para cada perfil de la audiencia se coloca en un conjunto de datos de Adobe Experience Platform, donde está disponible para flujos de trabajo por lotes personalizados.

En esta página, encontrará información sobre las funcionalidades específicas disponibles con el **Decisioning** y **Edge Decisioning** API. Aunque ambos le permiten enviar ofertas a sus clientes, recomendamos utilizar el **Edge Decisioning** API siempre que sea posible para casos de uso entrantes y para garantizar una mejor latencia y rendimiento en su plataforma.


Para obtener más información sobre cómo trabajar con las API, consulte estas secciones:
* [API de decisiones](decisioning-api.md)
* [API de Edge Decisioning](edge-decisioning-api.md)
* [API de decisiones por lotes](batch-decisioning-api.md)

## Funciones de API de Edge Decisioning {#edge}

**Solicitud única de eventos de experiencia y solicitudes de toma de decisiones**

Con la API de Edge Decisioning, puede enviar en una sola solicitud el propio evento de experiencia junto con la solicitud de toma de decisiones, en lugar de tener dos solicitudes diferentes.

Por ejemplo, si un cliente visita su sitio web, la solicitud incluirá el evento de experiencia (la visita del cliente a la página) y recuperará una oferta para rellenar la página visitada.

**Almacenamiento de datos de contexto en Adobe Experience Platform**

Los datos de contexto hacen referencia a datos que solo conoce en el momento en que desea recuperar una oferta. Por ejemplo, el color del artículo comprado, el tiempo en el momento de la compra, etc.

Al pasar datos de contexto con una solicitud de API de Edge Decisioning, los datos se almacenan en el perfil de Adobe Experience Platform, lo que permite su reutilización en el futuro.

>[!NOTE]
>
>Para que se almacenen los datos de contexto, debe tener configurado un esquema XDM dedicado.

## Funciones de API de decisiones {#decisioning}

Las funcionalidades enumeradas a continuación solo están disponibles con la API de Decisioning. Si necesita aprovechar uno de ellos para satisfacer sus necesidades, utilice la API de decisiones. De lo contrario, recomendamos utilizar las API de Edge Decisioning.

* **Eventos de experiencia**: aproveche los eventos de experiencia para crear reglas de toma de decisiones.
* **Contenido y características de la oferta**: puede optar por no devolver el contenido y las características de una oferta mediante una opción dedicada.
* **Metadatos de ofertas**: active una opción para devolver los metadatos de una oferta.
* **Política de combinación**: utilice en la solicitud una política de combinación diferente de la asociada a la zona protegida.
* **Eventos de toma de decisiones y límite de frecuencia**: bloquee la toma de decisiones para que los eventos se cuenten mediante cualquier límite de frecuencia que se produzca.
* **Duplicar propuestas**: active una opción para no deduplicar propuestas.
