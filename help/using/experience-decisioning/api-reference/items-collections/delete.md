---
title: Eliminar una colección de elementos
description: Aprenda a categorizar las decisiones de grupo en colecciones.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 7290c857-cbc7-4197-ae13-430adcf1649b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/JpZKEp0CnLg30ExvgHamm6dknBlr9vB1QlAlwMNAZKI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 6%

---

# Eliminar una colección de elementos {#delete-decision-item}

En ocasiones puede ser necesario eliminar (DELETE) una colección de elementos. Para ello, realice una petición DELETE a la API de la biblioteca de ofertas con el ID de la colección de elementos que desea eliminar.

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
