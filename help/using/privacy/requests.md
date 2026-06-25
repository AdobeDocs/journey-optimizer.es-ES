---
solution: Journey Optimizer
product: journey optimizer
title: Solicitudes de privacidad
description: Obtenga más información sobre las solicitudes de privacidad y Privacy Service.
feature: Privacy
role: User
level: Intermediate
exl-id: 19ec3410-761e-4a9c-a277-f105fc446d7a
TQID: https://experienceleague.adobe.com/eZC9hzg7Yf9sZ17idMlFYOX-Rn7lwGL6J2AyFaj0CV4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
subfeature_v2:
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
  - id: f365ec33-2b99-4b7f-b4ee-c743dd7f615f
  - id: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
source-git-commit: cbcb1cb0abbb8d4c6ea173c4deff071d0081da4e
workflow-type: tm+mt
source-wordcount: 573
ht-degree: 95%

---

# Solicitudes de privacidad {#track-changes}

>[!BEGINSHADEBOX]

**En esta página:** utilice Adobe Experience Platform Privacy Service para enviar y administrar solicitudes de acceso y eliminación de datos para Adobe Journey Optimizer, de modo que pueda cumplir los derechos del interesado y automatizar el cumplimiento de las regulaciones de privacidad.

>[!ENDSHADEBOX]

**Privacy Service** de Adobe Experience Platform proporciona una API de RESTful y una interfaz de usuario para ayudarle a administrar las solicitudes de datos de los clientes. Con Privacy Service, puede enviar solicitudes para acceder a datos personales de clientes y eliminarlos de aplicaciones de [!DNL Adobe CX Enterprise], lo que facilita el cumplimiento automatizado de las regulaciones de privacidad legales y organizativas.

Las solicitudes de privacidad se pueden crear y administrar desde el menú **[!UICONTROL Solicitudes]**.

![](assets/requests.png)

Para obtener más información sobre Privacy Service y cómo crear y administrar las solicitudes de privacidad, consulte la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=es){target="_blank"}.

<!--
* [Privacy Service overview](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)
* [Managing privacy jobs in the Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html)
-->

## Administración de las solicitudes de privacidad de datos individuales que puede enviar a Adobe Journey Optimizer {#data-privacy-requests}

Puede enviar solicitudes individuales para acceder a los datos de consumo y eliminarlos de Adobe Journey Optimizer de dos formas:

* A través de la **IU de Privacy Service**. [Más información](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=es){target="_blank"}
* A través de la **API de Privacy Service**. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/privacy/api/overview){target="_blank"}
  <!--More specific information on Privacy Service API [here](https://developer.adobe.com/experience-platform-apis/references/privacy-service/#_blank).-->

Privacy Service admite dos tipos de solicitudes: **acceso a datos** y **eliminación de datos**.

Para las **solicitudes de acceso**, especifique “**Adobe Journey Optimizer**” en la interfaz de usuario (o “**CJM**” como código de producto en la API).

Para las **solicitudes de eliminación**, además de la solicitud “**Adobe Journey Optimizer**”, también debe enviar solicitudes de eliminación a **tres servicios ascendentes** para evitar que Journey Optimizer vuelva a insertar los datos eliminados. Si no se especifican estos servicios ascendentes, la solicitud de “Adobe Journey Optimizer” permanecerá en el estado “procesando” hasta que se creen solicitudes de eliminación para los servicios ascendentes.

Los tres servicios ascendentes son los siguientes:

* Perfil (código de producto: “profileService”)
* Lago de datos de AEP (código de producto: “AdobeCloudPlatform”)
* Identidad (código de producto: “identidad”)

>[!NOTE]
>
>Esta guía solo explica cómo realizar solicitudes de privacidad para [!UICONTROL Adobe Journey Optimizer].
>
>* Si también planea realizar solicitudes de privacidad para el lago de datos de Platform, consulte esta [guía](https://experienceleague.adobe.com/es/docs/experience-platform/catalog/privacy) además de este tutorial.
>
>* Para el perfil del cliente en tiempo real, consulte esta [guía](https://experienceleague.adobe.com/es/docs/experience-platform/profile/privacy).
>* Para el servicio de identidad, consulte esta [guía](https://experienceleague.adobe.com/es/docs/experience-platform/identity/privacy).
>
>Para las solicitudes de eliminación y de acceso, debe llamar a estos sistemas individuales para asegurarse de que cada uno de ellos gestiona las solicitudes. Realizar una solicitud de privacidad a [!DNL Adobe Journey Optimizer] no quitará los datos de todos estos sistemas.

## Creación de solicitudes de acceso y eliminación

### Requisitos previos

Para realizar solicitudes de acceso y eliminación de datos para Adobe Journey Optimizer, deberá poseer lo siguiente:

* un ID de organización de Adobe
* un identificador de identidad de la persona sobre la que desea actuar y las áreas de nombres correspondientes. Para obtener más información sobre áreas de nombres de identidad en Adobe Journey Optimizer y Experience Platform, consulte la [información general del espacio de nombres de identidad](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/namespaces).

>[!IMPORTANT]
>
>Al enviar solicitudes de privacidad, asegúrese de especificar “[!DNL '**Adobe Journey Optimizer**]” como nombre de producto de destino y **todos los espacios de nombres de identidad** (como “Correo electrónico”, “ECID” o “ID de lealtad”) asociados con los datos de perfil a los que hay que acceder o que hay que eliminar. En particular, para las solicitudes de eliminación, si no incluye explícitamente el nombre del producto y todos los espacios de nombres aplicables, los datos no se eliminan de [!DNL Adobe Journey Optimizer].

### Valores de campo requeridos en Journey Optimizer para las solicitudes de API

```json
"companyContexts":
    "namespace": imsOrgID
    "value": <Your Adobe Organization ID Value>

"users":
    "action": either access or delete

    "userIDs":
        "namespace": e.g. email, aaid, ecid, etc.
        "type": standard
        "value": <Data Subject's Identity Identifier>

"include":
    CJM (which is the Adobe product code for Adobe Journey Optimizer)
    profileService (product code for Profile)
    AdobeCloudPlatform (product code for AEP Data Lake)
    identity (product code for Identity)

"regulation":
    gdpr, ccpa, pdpa, lgpd_bra, or nzpa_nzl (which is the privacy regulation that applies to the request)
```


### Ejemplo de solicitud de acceso al RGPD:

Desde la interfaz de usuario:

![](assets/accessrequest.png){width="60%" align="center"}

A través de la API:

```json
// JSON Request
{
   "companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"745F37C35E4B776E0A49421B@AdobeOrg"
      }
   ],
   "users":[
      {
         "action":[
            "access"
         ],
         "userIDs":[
            {
               "namespace":"ecid",
               "value":"38400000-8cf0-11bd-b23e-10b96e40000d",
               "type":"standard"
            },
            {
               "namespace":"email",
               "value":"johndoe4@gmail.com",
               "type":"standard"
            }
         ]
      }
   ],
   "include":[
      "CJM"
   ],
   "regulation":"gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "access"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```

### Ejemplo de solicitud de eliminación de RGPD:

Desde la interfaz de usuario:

![](assets/deleterequest.png){width="60%" align="center"}

A través de la API:

```json
// JSON Request
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "745F37C35E4B776E0A49421B@AdobeOrg"
    }
  ],
  "users": [
    {
      "action": [
          "delete"
      ],
      "userIDs": [
        {
          "namespace": "ecid",
          "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
          "type": "standard"
        },
                {
          "namespace": "email",
          "value": "johndoe4@gmail.com",
          "type": "standard"
        }
      ]
    }
  ],
  "include": [
    "CJM", "profileService", "AdobeCloudPlatform", "identity"
  ],
  "regulation": "gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "delete"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```
