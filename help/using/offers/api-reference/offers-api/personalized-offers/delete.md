---
title: Eliminar ofertas personalizadas
description: Una oferta personalizada es un mensaje de marketing personalizable basado en reglas y restricciones de idoneidad.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 6%

---

# Eliminar una oferta personalizada

En ocasiones puede ser necesario eliminar (DELETE) una oferta personalizada. Solo se pueden eliminar las ofertas personalizadas que cree en el contenedor de inquilino. Para ello, realiza una solicitud de DELETE a la API [!DNL Offer Library] utilizando el $id de la oferta personalizada que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las ofertas personalizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitud**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0f4bc230-13df-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 202 (sin contenido) y un cuerpo en blanco.

Puede confirmar la eliminación intentando realizar una solicitud de búsqueda (GET) a la oferta personalizada. Deberá incluir un encabezado Accept en la solicitud, pero recibirá un estado HTTP 404 (No encontrado) porque la oferta personalizada se ha eliminado del contenedor.
