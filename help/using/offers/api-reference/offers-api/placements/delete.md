---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: eliminar ubicaciones
description: Las ubicaciones son contenedores que se utilizan para mostrar sus ofertas.
feature: Decision Management, API
badge: label="Heredado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 22%

---

# Eliminar una ubicación {#delete-placement}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../experience-decisioning/gs-experience-decisioning.md)


En ocasiones puede ser necesario eliminar (DELETE) una ubicación. Para ello, realice una petición DELETE a la API [!DNL Offer Library] con el ID de la ubicación que desee eliminar.

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
