---
title: Actualizar las reglas de decisión
description: Las reglas de decisión son restricciones agregadas a una oferta personalizada y aplicadas a un perfil para determinar la idoneidad.
feature: Ofertas
topic: Integraciones
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 9%

---

# Actualizar una regla de decisión

Puede modificar o actualizar las reglas de decisión en el contenedor realizando una solicitud de PATCH a la API [!DNL Offer Library] .

Para obtener más información sobre JSON Patch, incluidas las operaciones disponibles, consulte la documentación oficial de [JSON Patch](http://jsonpatch.com/).

## Encabezados Accept y Content-Type

La tabla siguiente muestra los valores válidos que comprenden los campos *Content-Type* y *Accept* en el encabezado de la solicitud:

| Nombre del encabezado | Valor |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"` |

**Formato de API**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las reglas de decisión. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID de instancia de la regla de decisión que desea actualizar. | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**Solicitud**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/ab574eca-f7a9-38d0-b3d9-297376ca9ee2/instances/eaa5af90-13d9-11eb-9472-194dee6dc381' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
        "op": "replace",
        "path": "/_instance/xdm:name",
        "value": "Sales and discounts rule"
        }
    ]'
```

| Parámetro | Descripción |
| --------- | ----------- |
| `op` | La llamada de operación utilizada para definir la acción necesaria para actualizar la conexión. Las operaciones incluyen: `add`, `replace` y `remove`. |
| `path` | Ruta del parámetro que se va a actualizar. |
| `value` | El nuevo valor con el que desea actualizar el parámetro. |

**Respuesta**

Una respuesta correcta devuelve los detalles actualizados de la regla de decisión, incluido su ID de instancia única y la regla de decisión `@id`.

```json
{
    "instanceId": "eaa5af90-13d9-11eb-9472-194dee6dc381",
    "@id": "xcore:eligibility-rule:124e0faf5b8ee89b",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-21T20:13:43.048666Z",
    "repo:lastModifiedDate": "2020-10-21T20:25:43.705861Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
