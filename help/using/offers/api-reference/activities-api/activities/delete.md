---
title: Eliminar decisiones
description: Una decisión contiene la lógica que indica la selección de una oferta.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 3%

---

# Eliminar una decisión

Ocasionalmente puede ser necesario eliminar (DELETE) una decisión (anteriormente conocida como actividad de oferta). Solo se pueden eliminar las decisiones que se creen en el contenedor de inquilino. Para ello, realiza una solicitud de DELETE a la API [!DNL Offer Library] utilizando el $id de la oferta de reserva que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las decisiones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID de instancia de la decisión. | `f88c9be0-1245-11eb-8622-b77b60702882` |

**Solicitud**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 202 (sin contenido) y un cuerpo en blanco.

Puede confirmar la eliminación intentando realizar una solicitud de búsqueda (GET) a la decisión. Deberá incluir un encabezado Accept en la solicitud, pero recibirá un estado HTTP 404 (no encontrado) porque la decisión se ha eliminado del contenedor.
