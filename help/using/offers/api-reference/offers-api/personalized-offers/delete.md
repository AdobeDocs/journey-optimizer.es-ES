---
title: Eliminar ofertas personalizadas
description: Una oferta personalizada es un mensaje de marketing personalizable basado en reglas de elegibilidad y restricciones.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 9%

---

# Eliminar una oferta personalizada {#delete-personalized-offer}

En ocasiones puede ser necesario eliminar (DELETE) una oferta personalizada. Para ello, realice una petición DELETE a la API [!DNL Offer Library] con el ID de la oferta personalizada que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | El ID de la entidad que desea eliminar. | `personalizedOffer1234` |

**Solicitud**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 200 y un cuerpo en blanco.

Puede confirmar la eliminación intentando una solicitud de consulta (GET) a la oferta personalizada y debe recibir el estado HTTP 404 (no encontrado) porque la oferta personalizada se ha eliminado.
