---
title: eliminar ubicaciones
description: Las ubicaciones son contenedores que se utilizan para mostrar sus ofertas.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 9%

---

# Eliminar una ubicación {#delete-placement}

Ocasionalmente puede ser necesario eliminar (DELETE) una ubicación. Esto se hace realizando una solicitud de DELETE a [!DNL Offer Library] API con el ID de la ubicación que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/placements/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | El ID de instancia de la ubicación que desea actualizar. | `offerPlacement1234` |

**Solicitud**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 200 y un cuerpo en blanco.

Puede confirmar la eliminación intentando una solicitud de búsqueda (GET) en la ubicación y debe recibir un estado HTTP 404 (no encontrado) porque la ubicación se ha eliminado.
