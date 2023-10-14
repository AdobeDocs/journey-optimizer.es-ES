---
title: Eliminar una colección
description: Las colecciones son subconjuntos de ofertas basados en condiciones predefinidas definidas definidas por un experto en marketing, como la categoría de la oferta.
feature: Offers, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 11%

---

# Eliminar una colección {#delete-collection}

Ocasionalmente puede ser necesario eliminar (DELETE) una colección. Esto se hace realizando una solicitud de DELETE a [!DNL Offer Library] API con el `id` de la colección que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/offer-collections/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | El ID de la entidad que desea eliminar. | `offerCollection1234` |

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

Para confirmar la eliminación, intente realizar una solicitud de búsqueda (GET) en la colección. Debe recibir el estado HTTP 404 (no encontrado) porque la colección se ha eliminado.
