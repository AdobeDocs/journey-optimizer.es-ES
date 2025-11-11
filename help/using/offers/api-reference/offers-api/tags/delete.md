---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Eliminar calificadores de colección
description: Los calificadores de colección le permiten organizar y ordenar mejor sus ofertas.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 9%

---


# Eliminación de un cualificador de colección {#delete-tag}

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

Para confirmar la eliminación, intente una solicitud de búsqueda (GET) en el calificador de recopilación. Debe recibir el estado HTTP 404 (no encontrado) porque se ha eliminado el calificador de recopilación.