---
title: Eliminar calificadores de colección
description: Los calificadores de colección le permiten organizar y ordenar mejor sus ofertas.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: cc67519e-7a80-49c7-8c8b-c777be633026
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 6%

---

# Eliminación de un cualificador de colección {#delete-tag}

En ocasiones puede ser necesario quitar (DELETE) un calificador de recopilación (anteriormente conocido como &quot;etiqueta&quot;). Solo se pueden eliminar los calificadores de colección que cree en el contenedor de inquilino. Para ello, realice una petición DELETE a la API [!DNL Offer Library] usando el $id del calificador de recopilación que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | El contenedor donde se encuentran los calificadores de colección. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | El ID de instancia del calificador de recopilación que desea actualizar. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**Solicitud**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve el estado HTTP 202 (sin contenido) y un cuerpo en blanco.

Para confirmar la eliminación, intente una solicitud de búsqueda (GET) en el calificador de recopilación. Deberá incluir un encabezado Aceptar en la solicitud, pero deberá recibir el estado HTTP 404 (no encontrado) porque el calificador de recopilación se ha eliminado del contenedor.
