---
title: Eliminar una oferta de reserva
description: Se envía una oferta de reserva a los clientes si no cumplen los requisitos para otras ofertas
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5e97a1fd-7542-4c9a-8234-21c1fa419671
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---

# Eliminar una oferta de reserva {#delete-fallback-offer}

En ocasiones puede ser necesario eliminar (DELETE) una oferta de reserva. Solo se pueden eliminar las ofertas de reserva que cree en el contenedor de inquilino. Para ello, realice una petición DELETE a la API [!DNL Offer Library] usando el $id de la oferta de reserva que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las ofertas de reserva. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | El ID de instancia de la oferta de reserva. | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**Solicitud**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/b3966680-13ec-11eb-9c20-8323709cfc65' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 202 (sin contenido) y un cuerpo en blanco.

Puede confirmar la eliminación intentando una solicitud de búsqueda (GET) a la oferta de reserva. Deberá incluir un encabezado Aceptar en la solicitud, pero deberá recibir el estado HTTP 404 (no encontrado) porque la oferta de reserva se ha eliminado del contenedor.
