---
title: Eliminar una colección de elementos
description: Las colecciones le permiten categorizar y agrupar elementos de decisión según sus preferencias.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: dc47e2835379fbb2afb768beea6e4a1596f70ee9
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 5%

---


# Eliminar una colección de elementos {#delete-decision-item}

En ocasiones puede ser necesario eliminar (DELETE) una colección de elementos. Para ello, realice una solicitud del DELETE a la API de la biblioteca de ofertas utilizando el ID de la colección de elementos que desee eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/item-collections/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | El ID de la entidad que desea eliminar. | `itemCollections1234` |

**Solicitud**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 200 y un cuerpo en blanco.

Para confirmar la eliminación, intente realizar una solicitud de búsqueda (GET) en la colección de elementos. Debe recibir el estado HTTP 404 (no encontrado) porque se ha quitado la colección de elementos.
