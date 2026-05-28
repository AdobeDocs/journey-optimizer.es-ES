---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Eliminar calificadores de colección
description: Los calificadores de colección le permiten organizar y ordenar mejor sus ofertas.
feature: Decision Management, API
badge: label="Heredado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-GtK6nikASk8kLb0uPAsEpaSGKYdlu3m0u-jG2qxHT0
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 21%

---

# Eliminación de un cualificador de colección {#delete-tag}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../../../experience-decisioning/gs-experience-decisioning.md)


En ocasiones puede ser necesario quitar (DELETE) un calificador de recopilación (anteriormente conocido como &quot;etiqueta&quot;). Para ello, realice una petición DELETE a la API de la biblioteca de ofertas con el ID del calificador de colección que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | El ID de la entidad que desea eliminar. | `tag1234` |

**Solicitud**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 200 y un cuerpo en blanco.

Puede confirmar la eliminación intentando una solicitud de búsqueda (GET) al calificador de recopilación. Debe recibir el estado HTTP 404 (no encontrado) porque se ha eliminado el calificador de recopilación.
