---
title: Eliminar una estrategia de selección
description: Las estrategias de selección consisten en colecciones asociadas con restricciones y métodos de clasificación para determinar ofertas.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 774f3773-bc39-46c4-b32c-143abbd45696
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 5%

---

# Eliminar una estrategia de selección {#delete-selection-strategy}

En ocasiones puede ser necesario quitar (DELETE) una estrategia de selección. Para ello, realice una petición DELETE a la API de la biblioteca de ofertas con el ID de la estrategia de selección que desee eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | El ID de la entidad que desea eliminar. | `selectionStrategy1234` |

**Solicitud**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 200 y un cuerpo en blanco.

Para confirmar la eliminación, intente realizar una solicitud de búsqueda (GET) a la estrategia de selección. Debe recibir el estado HTTP 404 (no encontrado) porque se ha eliminado la estrategia de selección.
