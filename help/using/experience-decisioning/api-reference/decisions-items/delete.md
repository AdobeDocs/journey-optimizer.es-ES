---
title: Eliminación de un elemento de decisión
description: Los elementos de decisión son ofertas de marketing que se pueden crear y organizar en colecciones y catálogos.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 0fd608e0-df71-4e2d-8304-d7d5561c7c7a
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 6%

---

# Eliminación de un elemento de decisión {#delete-decision-item}

Para eliminar un elemento de decisión, realice una solicitud DELETE a la API de la biblioteca de ofertas con el ID del elemento de decisión que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/offer-items/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | El ID de la entidad que desea eliminar. | `offerItem1234` |

**Solicitud**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 200 y un cuerpo en blanco.

Para confirmar la eliminación, intente realizar una solicitud de búsqueda (GET) en el elemento de decisión. Debe recibir el estado HTTP 404 (no encontrado) porque el elemento de decisión se ha eliminado.
