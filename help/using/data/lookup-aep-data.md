---
solution: Journey Optimizer
product: journey optimizer
title: Uso de datos de Adobe Experience Platform (Beta)
description: Aprenda a utilizar conjuntos de datos de Adobe Experience Platform en las  [!DNL Journey Optimizer] capacidades de toma de decisiones y personalización.
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expresión, editor
exl-id: 44a8bc87-5ab0-45cb-baef-e9cd75432bde
source-git-commit: 416f82a932f0b484d8463ff24090a7061461822f
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 2%

---

# Uso de datos de Adobe Experience Platform {#aep-data}

>[!AVAILABILITY]
>
>Actualmente, esta función está disponible para todos los clientes como una versión beta pública.
>
>Para utilizar esta capacidad, primero debe aceptar los términos beta para su organización.

Journey Optimizer le permite aprovechar los datos de Adobe Experience Platform en [!DNL Journey Optimizer]. Para ello, los conjuntos de datos necesarios para la personalización de la búsqueda deben habilitarse primero mediante una llamada de API como se describe a continuación. Una vez finalizado, puede utilizar sus datos con las capacidades de personalización y toma de decisiones de [!DNL Journey Optimizer].

## Restricciones y directrices de Beta {#guidelines}

Antes de empezar, revise las siguientes restricciones y directrices:

* **El tamaño del conjunto de datos** está limitado a 5 GB para conjuntos de datos de producción y a 1 GB para conjuntos de datos de zonas protegidas para desarrollo
* **Se puede habilitar un máximo de 50 conjuntos de datos** para la búsqueda por organización en cualquier momento.
* **Número de registros** está restringido a 5 millones en conjuntos de datos de producción y a 1 millones en conjuntos de datos de zonas protegidas de desarrollo.
* **Etiquetado y aplicación del uso de datos** no se impone en este momento para los conjuntos de datos habilitados para la búsqueda.
* **Los conjuntos de datos habilitados para la búsqueda y utilizados en la personalización no están protegidos de la eliminación**. Depende de usted realizar un seguimiento de qué conjuntos de datos se están utilizando para la personalización a fin de asegurarse de que no se eliminen ni se eliminen.

## Habilitar un conjunto de datos para la búsqueda de datos {#enable}

Para aprovechar los datos del conjunto de datos para la personalización, debe utilizar una llamada de API para recuperar su estado y habilitar el servicio de búsqueda.

### Requisitos previos {#prerequisites-enable}

* Siga las instrucciones detalladas en [esta documentación](https://developer.adobe.com/journey-optimizer-apis/references/authentication/) para configurar su entorno y enviar comandos de API.
* El proyecto de desarrollador debe tener las API de Adobe Journey Optimizer y Adobe Experience Platform añadidas a su proyecto.

  ![](assets/aep-data-api.png)

* Debe tener permiso para administrar conjuntos de datos como parte de la función.
* El esquema en el que se basa el conjunto de datos debe contener una **identidad principal** que pueda actuar como clave de búsqueda.

### Estructura de llamadas API {#call}

```
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}"
```

Donde:

* **URL** es `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`
* **ID del conjunto de datos** es el conjunto de datos para el que desea habilitar.
* **Acción** está habilitada O deshabilitada.
* **Se puede recuperar el token de acceso** de Developer Console.
* **La clave de API** se puede recuperar de Developer Console.
* **ID de organización de IMS** es su organización de Adobe.
* **Nombre de zona protegida** es el nombre de la zona protegida en la que se encuentra el conjunto de datos (por ejemplo: prod, dev, etc.).

>[!NOTE]
>
>Si aparece el siguiente error al intentar realizar una llamada a una API para habilitar conjuntos de datos, intente eliminar las API de Adobe Journey Optimizer de su proyecto de consola del desarrollador y, a continuación, vuelva a agregarlas.
>
>```
>
>"error_code": "403003", 
>"message": "Api Key is invalid"
>
>```

Una vez que se ha habilitado un conjunto de datos para la búsqueda mediante una llamada de API, puede utilizar sus datos con las capacidades de personalización y toma de decisiones de [!DNL Journey Optimizer].

* [Uso de datos de Adobe Experience Platform para la personalización](../personalization/aep-data-perso.md)
* [Uso de datos de Adobe Experience Platform para la toma de decisiones](../experience-decisioning/aep-data-exd.md)
