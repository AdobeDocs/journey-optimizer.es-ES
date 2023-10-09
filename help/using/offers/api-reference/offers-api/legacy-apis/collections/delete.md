---
title: Eliminar una colección
description: Las colecciones son subconjuntos de ofertas basados en condiciones predefinidas definidas definidas por un experto en marketing, como la categoría de la oferta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 351d1f44-f3dc-49f9-bc3d-c775dad3cad4
source-git-commit: d312410ce2a91d3084d99e3caceb53ce4ada87b8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 8%

---

# Eliminar una colección {#delete-collection}

Ocasionalmente puede ser necesario eliminar (DELETE) una colección. Solo se pueden eliminar las colecciones que cree en el contenedor de inquilino. Esto se hace realizando una solicitud de DELETE a [!DNL Offer Library] API que utiliza el $id de la colección que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | El contenedor donde se encuentran las colecciones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | El ID de instancia de la colección que desea actualizar. | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

**Solicitud**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0bf31c20-13f1-11eb-a752-e58fd7dc4cb3' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 202 (sin contenido) y un cuerpo en blanco.

Para confirmar la eliminación, intente realizar una solicitud de búsqueda (GET) en la colección. Deberá incluir un encabezado Aceptar en la solicitud, pero deberá recibir el estado HTTP 404 (no encontrado) porque la colección se ha eliminado del contenedor.
