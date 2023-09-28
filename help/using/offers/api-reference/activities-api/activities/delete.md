---
title: Eliminar decisiones
description: Una decisión contiene la lógica que indica la selección de una oferta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 9%

---

# Eliminar una decisión {#delete-decision}

Ocasionalmente puede ser necesario eliminar (DELETE) una decisión. Esto se hace realizando una solicitud de DELETE a [!DNL Offer Library] API con el `id` de la decisión que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/offer-decisions/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | El ID de la entidad que desea eliminar. | `offerDecision1234` |

**Solicitud**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-decisions/offerDecision1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 200 y un cuerpo en blanco.

Para confirmar la eliminación, intente realizar una solicitud de búsqueda (GET) para confirmar la decisión. Debe recibir el estado HTTP 404 (no encontrado) porque la decisión se ha eliminado.
