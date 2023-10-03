---
title: Eliminar calificadores de colección
description: Los calificadores de colección le permiten organizar y ordenar mejor sus ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: 54b92b19f2e3a6afa6557ffeff0d971a4c411510
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 9%

---

# Eliminación de un cualificador de colección {#delete-tag}

En ocasiones puede ser necesario quitar (DELETE) un calificador de colección (anteriormente conocido como &quot;etiqueta&quot;). Esto se hace realizando una solicitud de DELETE a [!DNL Offer Library] API que utiliza el ID del calificador de recopilación que desea eliminar.

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

Puede confirmar la eliminación intentando una solicitud de búsqueda (GET) al calificador de recopilación y debe recibir un estado HTTP 404 (no encontrado) porque se ha eliminado.