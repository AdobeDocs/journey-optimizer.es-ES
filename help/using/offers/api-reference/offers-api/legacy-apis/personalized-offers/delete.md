---
title: Eliminar ofertas personalizadas
description: Una oferta personalizada es un mensaje de marketing personalizable basado en reglas de elegibilidad y restricciones.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 6ae37843-2679-48a3-96ef-bb93a5d4a333
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 7%

---

# Eliminar una oferta personalizada {#delete-personalized-offer}

En ocasiones puede ser necesario eliminar (DELETE) una oferta personalizada. Solo se pueden eliminar las ofertas personalizadas que cree en el contenedor de inquilino. Para ello, realice una petición DELETE a la API [!DNL Offer Library] utilizando el $id de la oferta personalizada que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | El contenedor donde se encuentran las ofertas personalizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitud**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0f4bc230-13df-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 202 (sin contenido) y un cuerpo en blanco.

Para confirmar la eliminación, intente una solicitud de búsqueda (GET) para la oferta personalizada. Deberá incluir un encabezado Aceptar en la solicitud, pero deberá recibir el estado HTTP 404 (no encontrado) porque la oferta personalizada se ha eliminado del contenedor.
