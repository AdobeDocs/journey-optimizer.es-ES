---
title: Eliminar una fórmula de clasificación
description: Las fórmulas de clasificación permiten definir las funciones de puntuación, que se utilizan para clasificar elementos.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 4ea50481-b1b9-4e0c-ad4e-c4139891bfdf
source-git-commit: 6378c4a8cb911088c685166b9c1b29a1773d47b7
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
