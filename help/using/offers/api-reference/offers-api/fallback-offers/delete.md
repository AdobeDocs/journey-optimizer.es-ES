---
title: Eliminar una oferta de reserva
description: Se envía una oferta de reserva a los clientes si no cumplen los requisitos para otras ofertas
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 12%

---


# Eliminar una oferta de reserva {#delete-fallback-offer}

En ocasiones puede ser necesario eliminar (DELETE) una oferta de reserva. Para ello, realice una petición DELETE a la API [!DNL Offer Library] con el ID de la oferta de reserva que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | El ID de la entidad que desea eliminar. | `fallbackOffer1234` |

**Solicitud**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 200 y un cuerpo en blanco.

Puede confirmar la eliminación intentando una solicitud de búsqueda (GET) para la oferta y debe recibir el estado HTTP 404 (no encontrado) porque se ha eliminado la oferta de reserva.
