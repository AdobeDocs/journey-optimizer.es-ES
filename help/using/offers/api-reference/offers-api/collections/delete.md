---
title: Eliminar una colección
description: Las colecciones son subconjuntos de ofertas basados en condiciones predefinidas definidas definidas por un especialista en marketing, como la categoría de la oferta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 8%

---

# Eliminar una colección {#delete-collection}

Ocasionalmente puede ser necesario eliminar (DELETE) una colección. Solo se pueden eliminar las colecciones creadas en el contenedor de inquilino. Para ello, realiza una solicitud de DELETE al [!DNL Offer Library] API que utiliza el $id de la colección que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las colecciones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID de instancia de la colección que desea actualizar. | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

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

Puede confirmar la eliminación intentando realizar una solicitud de búsqueda (GET) a la colección. Deberá incluir un encabezado Accept en la solicitud, pero recibirá un estado HTTP 404 (No encontrado) porque la colección se ha eliminado del contenedor.
