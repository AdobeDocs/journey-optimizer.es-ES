---
title: Eliminar una regla de idoneidad
description: Las reglas de elegibilidad le permiten definir los candidatos elegibles en función de lo que desee segmentar, como atributos de perfil y audiencias.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 19baf888-23b7-46de-9d3c-9a0fa8ab2297
version: Journey Orchestration
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 127
ht-degree: 5%

---

# Eliminar una regla de idoneidad {#delete-eligibility-rule}

En ocasiones puede ser necesario eliminar (DELETE) una regla de elegibilidad. Para ello, realice una petición DELETE a la API de la biblioteca de ofertas utilizando el ID de la regla de idoneidad que desee eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/eligibility-rules/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | El ID de la entidad que desea eliminar. | `rule1234` |

**Solicitud**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 200 y un cuerpo en blanco.

Puede confirmar la eliminación intentando una solicitud de búsqueda (GET) a la regla. Debe recibir el estado HTTP 404 (no encontrado) porque la regla se ha eliminado.
