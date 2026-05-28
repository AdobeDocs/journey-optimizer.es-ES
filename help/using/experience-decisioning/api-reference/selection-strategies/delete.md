---
title: Eliminar una estrategia de selección
description: Las estrategias de selección consisten en colecciones asociadas con restricciones y métodos de clasificación para determinar ofertas.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 774f3773-bc39-46c4-b32c-143abbd45696
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/KnyhVoNWfjSIIMw2q7OZkBG--wgaBU4JXn7A9i41Vf8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 121
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

Puede confirmar la eliminación intentando una solicitud de búsqueda (GET) a la estrategia de selección. Debe recibir el estado HTTP 404 (no encontrado) porque se ha eliminado la estrategia de selección.
