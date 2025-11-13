---
solution: Journey Optimizer
product: journey optimizer
title: Pasos de configuración
description: Obtenga información sobre cómo crear un esquema relacional en Adobe Experience Platform cargando un DDL
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
version: Campaign Orchestration
source-git-commit: 059670c143595b9cacdf7e82a8a5c3efda78f30b
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 1%

---


# Introducción a esquemas y conjuntos de datos relacionales{#gs-schemas}

Esta guía muestra el proceso de creación de un esquema relacional, configuración de un conjunto de datos para campañas organizadas e ingesta de datos.

![esquema](assets/do-not-localize/schema_admin.png){zoomable="yes"}

## Conceptos clave

En el contexto de las campañas orquestadas, un **conjunto de datos** es una construcción de almacenamiento y administración para una colección de datos, normalmente una tabla, que contiene un esquema (filas) y campos (columnas). Los datos que se incorporan correctamente a Experience Platform se almacenan dentro del lago de datos como conjuntos de datos.

Un **esquema** representa y valida la estructura y el formato de los datos. Proporciona una definición abstracta de un objeto del mundo real (como una persona) y describe qué datos deben incluirse en cada instancia de ese objeto (como nombre, cumpleaños, etc.).

Un **modelo de datos** es el modelo conceptual para normalizar los datos

Describe lo siguiente:

* Las entidades (por ejemplo, cliente, campaña, segmento)
* Los atributos de esas entidades (por ejemplo, Nombre del cliente, Fecha de inicio de la campaña)
* Las relaciones entre entidades (por ejemplo, Los clientes pertenecen a Segmentos, Campañas, Segmentos de destino)

Un modelo de datos es lógico y conceptual, no está vinculado a una implementación física en Orchestrated Campaign

En un **modelo de datos relacional**, los datos están organizados en tablas relacionadas con otras tablas.

* Cada tabla tiene filas (registros) y columnas (atributos)
* Cada tabla tiene una clave principal para identificar filas de forma exclusiva
* Las relaciones entre tablas se expresan mediante claves externas

Un **esquema relacional** es la definición formal del modelo de datos relacional.

Especifica lo siguiente:

* El conjunto de tablas
* Las columnas de cada tabla
* Las restricciones
* Las relaciones entre tablas

La organización de esquemas o tablas en un modelo de datos relacional consiste en estructurar los datos en varias tablas. Asegúrese de que cada tabla almacene un tipo de entidad/esquemas

➡️ [Obtenga más información acerca de los esquemas en la documentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas#create-model-based-schema)

## Pasos de implementación {#implementation}

Para introducir datos y crear un esquema relacional, siga estos pasos:

1. Crear [esquema relacional manualmente](manual-schema.md) o [con un archivo DDL](file-upload-schema.md)

   Defina la estructura del modelo de datos, incluidas las tablas, los atributos y las relaciones. Elija crear el esquema manualmente en la interfaz de usuario o cargar un archivo DDL para una configuración más rápida.

   Al crear el esquema manualmente, el conjunto de datos también debe crearse y habilitarse manualmente. Al utilizar un archivo DDL, la creación y la activación de conjuntos de datos son automáticas.

1. [Vincular esquemas](file-upload-schema.md)

   Establezca relaciones entre los esquemas para garantizar la coherencia de los datos y habilitar consultas entre entidades. Por ejemplo, vincule las transacciones de lealtad a los destinatarios o las recompensas a las marcas.

1. [Crear conjunto de datos](manual-schema.md#dataset)

   Después de definir el esquema, debe crear un conjunto de datos basado en él. Este conjunto de datos actúa como almacenamiento para los datos ingeridos.

1. [Habilitar campañas organizadas](manual-schema.md#enable)

   El conjunto de datos almacena los datos ingeridos y debe estar habilitado para las campañas orquestadas a fin de garantizar que sea accesible en Adobe Journey Optimizer.

1. [Ingesta de datos](ingest-data.md)

   Incluya datos en Adobe Experience Platform desde fuentes compatibles como SFTP, almacenamiento en la nube o bases de datos.

