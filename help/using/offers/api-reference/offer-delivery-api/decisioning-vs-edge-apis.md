---
title: API de decisiones y Edge Decisioning
description: La administración de decisiones es una colección de servicios y programas de interfaz de usuario que permiten a los especialistas en marketing crear y ofrecer experiencias de oferta personalizadas para el usuario final en canales y aplicaciones mediante lógica empresarial y reglas de decisión.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: dc56f2dc461a11c9706b3572ccd4b9e0feb6f055
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 1%

---

# API de decisiones y Edge Decisioning {#about-decisioning-apis}

Puede enviar ofertas utilizando la variable **Decisioning** o **Edge Decisioning** API.

En esta página, encontrará información sobre funcionalidades específicas disponibles con cada API. Aunque ambos le permiten entregar ofertas a sus clientes, recomendamos utilizar la variable **Edge Decisioning** siempre que sea posible para casos de uso entrantes y para garantizar una mejor latencia y rendimiento en su plataforma.

|  | Solicitudes/s | Latencia |
|---|---|---|
| API de decisiones | 2000 | &lt;500ms |
| API de Edge Decisioning | 5000 | &lt;250ms |

Para obtener más información sobre cómo trabajar con las API, consulte estas secciones:
* [API de decisiones](decisioning-api.md)
* [API de Edge Decisioning](edge-decisioning-api.md)

## Funciones de la API de Edge Decisioning {#edge}

**Solicitud única para eventos de experiencia y solicitudes de toma de decisiones**

Con la API de Edge Decisioning, puede enviar en una sola solicitud el propio evento de experiencia junto con la solicitud de toma de decisiones, en lugar de tener dos solicitudes diferentes.

Por ejemplo, si un cliente visita su sitio web, la solicitud incluirá el evento de la experiencia (la visita del cliente a la página) y obtendrá una oferta para rellenar la página visitada.

**Almacenamiento de datos de contexto en Adobe Experience Platform**

Los datos de contexto hacen referencia a datos que solo se conocen en el momento en que se desea que se devuelva una oferta. Por ejemplo, el color del artículo comprado, el clima en el momento de la compra, etc.

Al pasar datos de contexto con una solicitud de API de Edge Decisioning, los datos se almacenan en el perfil de Adobe Experience Platform, lo que permite su reutilización futura.

>[!NOTE]
>
>Para que se almacenen los datos de contexto, debe tener configurado un esquema XDM dedicado.

## Funciones de API de decisiones {#decisioning}

Las funcionalidades enumeradas a continuación solo están disponibles con la API de decisiones. Si necesita aprovechar uno de ellos para satisfacer sus necesidades, use la API de decisiones. De lo contrario, se recomienda utilizar las API de Edge Decisioning.

* **Eventos de experiencias**: aproveche los eventos de experiencia para crear reglas de decisión.
* **Contenido y características de la oferta**: puede optar por no devolver el contenido y las características de una oferta mediante una opción dedicada.
* **Metadatos de la oferta**: active una opción para devolver los metadatos de una oferta.
* **Combinar directiva**: utilice en la solicitud una política de combinación diferente de la asociada al entorno limitado.
* **Eventos de decisión y restricción de frecuencia**: impedir que los eventos de decisiones de bloques se cuenten mediante cualquier restricción de frecuencia que se produzca.
* **Duplicar propuestas**: active una opción para no deduplicar propuestas.
