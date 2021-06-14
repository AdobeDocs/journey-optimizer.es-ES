---
title: Eliminar una colección
description: Las colecciones son subconjuntos de ofertas basados en condiciones predefinidas definidas definidas por un especialista en marketing, como la categoría de la oferta.
feature: Ofertas
topic: Integraciones
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 8%

---

# Eliminar una colección

Ocasionalmente puede ser necesario eliminar (DELETE) una colección. Solo se pueden eliminar las colecciones creadas en el contenedor de inquilino. Para ello, realiza una solicitud de DELETE a la API [!DNL Offer Library] utilizando el $id de la colección que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las colecciones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID de instancia de la colección que desea actualizar. | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

**Solicitud**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0bf31c20-13f1-11eb-a752-e58fd7dc4cb3' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 202 (sin contenido) y un cuerpo en blanco.

Puede confirmar la eliminación intentando realizar una solicitud de búsqueda (GET) a la colección. Deberá incluir un encabezado Accept en la solicitud, pero recibirá un estado HTTP 404 (No encontrado) porque la colección se ha eliminado del contenedor.
