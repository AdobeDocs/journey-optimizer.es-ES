---
title: eliminar ubicaciones
description: Las ubicaciones son contenedores que se utilizan para mostrar sus ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
source-git-commit: 54b92b19f2e3a6afa6557ffeff0d971a4c411510
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 6%

---

# Eliminar una ubicación {#delete-placement}

Ocasionalmente puede ser necesario eliminar (DELETE) una ubicación. Solo se pueden eliminar las ubicaciones que cree en el contenedor de inquilino. Esto se hace realizando una solicitud de DELETE a [!DNL Offer Library] API que utiliza el ID de instancia de la ubicación que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | El contenedor donde se encuentran las ubicaciones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | El ID de instancia de la ubicación que desea actualizar. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**Solicitud**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 202 (sin contenido) y un cuerpo en blanco.

Para confirmar la eliminación, intente una solicitud de búsqueda (GET) en la ubicación. Deberá incluir un encabezado Aceptar en la solicitud, pero deberá recibir el estado HTTP 404 (no encontrado) porque la ubicación se ha eliminado del contenedor.
