---
solution: Journey Optimizer
product: journey optimizer
title: Uso de datos de Adobe Experience Platform
description: Aprenda a utilizar conjuntos de datos de Adobe Experience Platform en las  [!DNL Journey Optimizer] capacidades de toma de decisiones y personalización.
feature: Personalization, Rules
topic: Personalization
role: Developer
level: Intermediate
keywords: expresión, editor
mini-toc-levels: 1
exl-id: 44a8bc87-5ab0-45cb-baef-e9cd75432bde
source-git-commit: 41364a89289f0657a2b7646c5daa45a369936e57
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 5%

---

# Uso de datos de Adobe Experience Platform {#aep-data}

>[!CONTEXTUALHELP]
>id="lookup-aep-data"
>title="Habilitar para búsqueda"
>abstract="Al habilitar un conjunto de datos para la búsqueda, puede aprovechar sus datos dentro de las funciones de personalización, toma de decisiones y orquestación de recorrido de Journey Optimizer."

[!DNL Journey Optimizer] le permite aprovechar los datos de [!DNL Adobe Experience Platform] con capacidades de personalización, toma de decisiones y orquestación de recorrido. Para ello, los conjuntos de datos basados en registros necesarios para la personalización de la búsqueda deben habilitarse primero para el servicio de búsqueda como se describe a continuación.

Obtenga más información sobre cómo acceder a los conjuntos de datos y trabajar con ellos en esta sección: [Introducción a los conjuntos de datos](../data/get-started-datasets.md)

## Lectura obligatoria

### Protecciones y directrices {#guidelines}

Antes de empezar, revise las siguientes restricciones y directrices:

* **No hay PII en los conjuntos de datos**. Los conjuntos de datos habilitados para la búsqueda no deben contener información de identificación personal (PII).

* **Riesgo de eliminación**: los conjuntos de datos utilizados en la personalización no están protegidos contra eliminación. Debe realizar un seguimiento de los conjuntos de datos que se utilizan para asegurarse de que no se eliminan.

* **Tipo de esquema**: los conjuntos de datos deben estar asociados con un esquema que sea **NO** de tipo perfil o evento.

* **Mantener la opción de búsqueda activada**: evite activar y desactivar conjuntos de datos repetidamente. Al hacerlo, se puede producir un comportamiento de indexación inesperado. La práctica recomendada es dejar el conjunto de datos habilitado durante el tiempo que desee utilizarlo para búsquedas.

* **Región de activación de Edge**: los conjuntos de datos habilitados para la búsqueda solo están disponibles para la activación entrante basada en Edge en la región donde reside la zona protegida del conjunto de datos (por ejemplo, NLD2 o VA7). Puede ver la región de zona protegida en la interfaz de usuario junto al nombre de la zona protegida.

* **Lote de eliminación de datos**: al eliminar un lote de datos del conjunto de datos, se eliminan por completo todas las claves coincidentes del servicio de búsqueda. Por ejemplo:

  **Lote 1**: Sku1, Sku2, Sku3\
  **Lote 2**: Sku1, Sku2, Sku3, Sku4, Sku5, Sku6\
  **Lote 3**: Sku7, Sku8, Sku9, Sku10

  Si elimina **Lote 1**, Sku1, Sku2 y Sku3 se quitarán del almacén de búsqueda. Los datos de búsqueda resultantes contendrán: Sku4, Sku5, Sku6, Sku7, Sku8, Sku9, Sku10.

* **No hay búsquedas encadenadas**: las búsquedas de conjuntos de datos no se pueden encadenar. En otras palabras, no se puede utilizar el resultado de una búsqueda como variable para luego convertirse en la clave para realizar una segunda búsqueda.

### Derecho al servicio de búsqueda

| Componente de función | Límites | Notas |
| ------- | ------- | ------- |
| Conjuntos de datos de búsqueda habilitados | Máx. 10 por organización | Número máximo de conjuntos de datos que se pueden configurar para la búsqueda en un momento determinado. Este límite se aplica al número total combinado de conjuntos de datos de búsqueda en los entornos limitados de producción y desarrollo de la instancia del cliente. |
| Recuento de registros de conjuntos de datos | Hasta 2 millones de registros por conjunto de datos | Número máximo de registros permitidos en un único conjunto de datos, calculado como el recuento total en todos los lotes dentro de ese conjunto de datos. |
| Tamaño de registro | Hasta 2 KB por registro | Se admite el tamaño máximo de registro predeterminado. |
| Tamaño del conjunto de datos | Hasta 4 GB | El tamaño máximo de un conjunto de datos individual, no el tamaño combinado en todos los conjuntos de datos de una zona protegida. Los límites de recuento de registros y tamaño del conjunto de datos son protecciones independientes; ambas deben cumplirse. |
| Actualizaciones de frecuencia de conjuntos de datos | Hasta 5 actualizaciones al día por conjunto de datos | Frecuencia máxima de operaciones de actualización permitidas para un único conjunto de datos por día. |

>[!NOTE]
>
>Si se necesitan volúmenes adicionales más allá de las protecciones enumeradas anteriormente, póngase en contacto con su representante de Adobe.

## Habilitar un conjunto de datos para la búsqueda de datos {#enable}

Para aprovechar los datos del conjunto de datos para la personalización, debe habilitar el conjunto de datos para la búsqueda.

### Requisitos previos {#prerequisites-enable}

El esquema asociado con el conjunto de datos que desea habilitar para la búsqueda debe ser del tipo registro. El esquema NO debe ser de perfil ni de clase de evento.

+++Ejemplo

![](assets/data-lookup-schema.png)

+++

El esquema debe tener una identidad principal definida.

+++Ejemplo

![](assets/data-lookup-primary.png)

+++

Si aún no se ha definido un área de nombres personalizada, asegúrese de que la identidad sea un identificador que no sea una persona.

+++Ejemplo

![](assets/aep-data-namespace.png)

+++

### Habilitar el conjunto de datos para la búsqueda en la interfaz de administración de conjuntos de datos

En la interfaz de usuario de administración de conjuntos de datos, utilice la opción para habilitar el conjunto de datos para la búsqueda.

![](assets/aep-data-enable.png)

### Método de API

Siga las instrucciones detalladas en [esta documentación](https://developer.adobe.com/journey-optimizer-apis/references/authentication/) para configurar su entorno y enviar comandos de API.

#### Requisitos previos

* El proyecto de desarrollador debe tener las API de Adobe Journey Optimizer y Adobe Experience Platform añadidas a su proyecto.

  ![](assets/aep-data-api.png)

* Debe tener permiso para administrar conjuntos de datos como parte de la función.

* El esquema en el que se basa el conjunto de datos debe contener una identidad principal que pueda actuar como clave de búsqueda.

#### Estructura de llamadas API

```shell
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}" 
```

Donde:

* La URL es `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`
* El ID del conjunto de datos es el conjunto de datos para el que desea habilitar.
* La acción está habilitada O deshabilitada.
* El token de acceso se puede recuperar de Developer Console.
* La clave de API se puede recuperar de Developer Console.
* El ID de organización de IMS es su organización de Adobe.
* Nombre de zona protegida es el nombre de la zona protegida en la que se encuentra el conjunto de datos (es decir, prod, dev, etc.).

>[!NOTE]
>
>Si aparece el siguiente error al intentar realizar una llamada a una API para habilitar conjuntos de datos, intente eliminar las API de Adobe Journey Optimizer de su proyecto de consola del desarrollador y, a continuación, vuelva a agregarlas:
>
>`"error_code": "403003",`
>`"message": "Api Key is invalid"`

## Monitorización de conjuntos de datos

Una vez que un conjunto de datos se haya habilitado para la búsqueda, puede revisar el estado de la ingesta en el servicio de búsqueda. Para ello, vaya al menú **[!UICONTROL Supervisión]** y seleccione la pestaña **[!UICONTROL Journey Optimizer]**.

Este indicador de proceso ayuda a comprender cuándo están disponibles nuevos lotes de datos en el servicio de búsqueda.

![](assets/aep-data-monitoring.png)

## Próximos pasos

Una vez habilitado un conjunto de datos para la búsqueda mediante una llamada de API, puede utilizar los datos con las capacidades de personalización y toma de decisiones de [!DNL Journey Optimizer]. Para obtener más información, consulte estas secciones:

* [Uso de datos de Adobe Experience Platform para la personalización](../personalization/aep-data-perso.md)
* [Uso de datos de Adobe Experience Platform para las decisiones](../experience-decisioning/aep-data-exd.md)
* [Usar datos de Adobe Experience Platform para la orquestación de recorrido](../building-journeys/dataset-lookup.md)
