---
title: Eliminar una fórmula de clasificación
description: Las fórmulas de clasificación permiten definir las funciones de puntuación, que se utilizan para clasificar elementos.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 5%

---

# Eliminar una fórmula de clasificación {#delete-selection-strategy}

En ocasiones puede ser necesario eliminar (DELETE) una fórmula de clasificación. Para ello, realice una petición DELETE a la API de la biblioteca de ofertas utilizando el ID de la fórmula de clasificación que desee eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | El ID de la entidad que desea eliminar. | `rankingFormula1234` |

**Solicitud**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 200 y un cuerpo en blanco.

Puede confirmar la eliminación intentando una solicitud de búsqueda (GET) a la fórmula de clasificación. Debe recibir el estado HTTP 404 (no encontrado) porque la fórmula de clasificación se ha eliminado.

