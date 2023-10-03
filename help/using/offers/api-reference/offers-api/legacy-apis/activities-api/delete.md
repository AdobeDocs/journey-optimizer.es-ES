---
title: Eliminar decisiones
description: Una decisión contiene la lógica que indica la selección de una oferta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: ef22b6183c7646cca8636f4a7e4dd87c8f88e8ce
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 10%

---


# Eliminar una decisión {#delete-decision}

Ocasionalmente puede ser necesario eliminar (DELETE) una decisión. Solo se pueden eliminar las decisiones que cree en el contenedor de inquilino. Esto se hace realizando una solicitud de DELETE a [!DNL Offer Library] API que utiliza el $id de la oferta de reserva que desea eliminar.

**Formato de API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | El contenedor en el que se encuentran las decisiones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | El ID de instancia de la decisión. | `f88c9be0-1245-11eb-8622-b77b60702882` |

**Solicitud**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
	@@ -37,6 +35,6 @@ curl -X DELETE \

**Response**

A successful response returns HTTP status 202 (No Content) and a blank body.

You can confirm the deletion by attempting a lookup (GET) request to the decision. You will need to include an Accept header in the request, but should receive an HTTP status 404 (Not Found) because the decision has been removed from the container.

