---
solution: Journey Optimizer
product: journey optimizer
title: Utilice acciones personalizadas para escribir eventos de Recorrido en AEP
description: Utilice acciones personalizadas para escribir eventos de Recorrido en AEP
feature: Journeys, Use Cases, Custom Actions
topic: Content Management
role: Developer, Data Engineer
level: Experienced
exl-id: 890a194f-f54d-4230-863a-fb2b924d716a
source-git-commit: 778ef71a531346774c5e10e296dbf1112fed891d
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Caso de uso: Uso de acciones personalizadas para escribir eventos de Recorrido en Experience Platform{#custom-action-aep}

En este caso de uso se explica cómo escribir eventos personalizados en Adobe Experience Platform desde Recorridos mediante acciones personalizadas y llamadas autenticadas.

## Configuración de un proyecto de IO

1. En la consola de Adobe Developer, haga clic en **Proyecto** y abra el proyecto de IO.

1. En el **Credenciales** , haga clic en **Servidor a servidor OAuth**.

   ![](assets/custom-action-aep-1.png)

1. Clic **Ver comando cURL**.

   ![](assets/custom-action-aep-2.png)

1. Copie el comando cURL y almacene client_id, client_secret, grant_type y el ámbito.

```
curl -X POST 'https://ims-na1.adobelogin.com/ims/token/v3' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=client_credentials&client_id=1234&client_secret=5678&scope=openid,AdobeID,read_organizations,additional_info.projectedProductContext,session'
```

>[!CAUTION]
>
>Después de crear el proyecto en la consola de Adobe Developer, asegúrese de otorgar al desarrollador y al control de acceso de la API los permisos adecuados. Obtenga más información en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication#grant-developer-and-api-access-control){target="_blank"}

## Configurar el origen mediante la entrada de la API HTTP

1. Cree un extremo en Adobe Experience Platform para escribir los datos de los recorridos.

1. En Adobe Experience Platform, haga clic en **Fuentes**, en **Conexiones** en el menú izquierdo. En **API HTTP**, haga clic en **Añadir datos**.

   ![](assets/custom-action-aep-3.png)

1. Seleccionar **Nueva cuenta** y habilite la autenticación. Haga clic en **Conectar con el origen**.

   ![](assets/custom-action-aep-4.png)

1. Haga clic en **Siguiente** y seleccione el Conjunto de datos donde desea escribir los datos. Clic **Siguiente** y **Finalizar**.

   ![](assets/custom-action-aep-5.png)

1. Abra el flujo de datos recién creado. Copie la carga útil del esquema y guárdela en el bloc de notas.

```
{
"header": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
},
"imsOrgId": "<org_id>",
"datasetId": "<dataset_id>",
"source": {
"name": "Custom Journey Events"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
}
},
"xdmEntity": {
"_id": "test1",
"<your_org>": {
"journeyVersionId": "",
"nodeId": "", "customer_Id":""
},
"eventMergeId": "",
"eventType": "",
"producedBy": "self",
"timestamp": "2018-11-12T20:20:39+00:00"
}
}
}
```

## Configuración de la acción personalizada

1. Abra Adobe Journey Optimizer y haga clic en **Configuraciones**, en **Administration** en el menú izquierdo. En **Acciones**, haga clic en **Administrar** y haga clic en **Crear acción**.

1. Establezca la dirección URL y seleccione el método Post.

   `https://dcs.adobedc.net/collection/<collection_id>?syncValidation=false`

1. Asegúrese de que los encabezados (Content-Type, Charset, sandbox-name) estén configurados.

   ![](assets/custom-action-aep-7bis.png)

### Configurar la autenticación

1. Seleccione el **Tipo** as **Personalizado** con la siguiente carga útil.

1. Pegue client_secret, client_id, scope y grant_type (desde la carga útil del proyecto de IO utilizada anteriormente).

   ```
   {
   "type": "customAuthorization",
   "authorizationType": "Bearer",
   "endpoint": "https://ims-na1.adobelogin.com/ims/token/v3",
   "method": "POST",
   "headers": {},
   "body": {
   "bodyType": "form",
   "bodyParams": {
   "grant_type": "client_credentials",
   "client_secret": "********",
   "client_id": "<client_id>",
   "scope": "openid,AdobeID,read_organizations,additional_info.projectedProductContext,session"
   }
   },
   "tokenInResponse": "json://access_token",
   "cacheDuration": {
   "duration": 28000,
   "timeUnit": "seconds"
   }
   }
   ```

1. Utilice el **Haga clic en para probar la autenticación** para probar la conexión.

   ![](assets/custom-action-aep-8.png)

### Configuración de la carga útil

1. En el **Solicitud** y **Respuesta** , pegue la carga útil de la conexión de origen utilizada anteriormente.

   ```
   {
   "xdmMeta": {
   "schemaRef": {
   "id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
   "contentType": "application/vnd.adobe.xed-full+json;version=1.0"
   }
   },
   "xdmEntity": {
   "_id": "/uri-reference",
   "<your_org>": {
   "journeyVersionId": "Sample value",
   "nodeId": "Sample value",
   "customer_Id":""
   },
   "eventMergeId": "Sample value",
   "eventType": "advertising.completes,
   "producedBy": "self",
   "timestamp": "2018-11-12T20:20:39+00:00"
   }
   }
   ```

1. Cambiar la configuración del campo de **Constante** hasta **Variable** para campos que se rellenarán dinámicamente. Guarde la acción personalizada.

##  Recorrido 

1. Finalmente, utilice esta acción personalizada en un recorrido para escribir los eventos de recorrido personalizados.

1. Rellene los atributos ID de versión de Recorrido, ID de nodo, Nombre de nodo y otros según su caso de uso.

   ![](assets/custom-action-aep-9.png)
