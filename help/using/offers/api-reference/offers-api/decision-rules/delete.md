---
title: Eliminar reglas de decisión
description: Las reglas de decisión son restricciones agregadas a una oferta personalizada y aplicadas a un perfil para determinar la elegibilidad.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 9%

---

# Eliminar una regla de decisión {#delete-decision-rule}

En ocasiones puede ser necesario eliminar (DELETE) una regla de decisión. Para ello, realice una solicitud de DELETE a la API [!DNL Offer Library] mediante el `id` de la regla de decisión que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | El ID de la entidad que desea eliminar. | `offerRule1234` |

**Solicitud**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 200 y un cuerpo en blanco.

Puede confirmar la eliminación intentando una solicitud de consulta (GET) a la regla de decisión y debe recibir un estado HTTP 404 (no encontrado) porque la regla de decisión se ha eliminado.
