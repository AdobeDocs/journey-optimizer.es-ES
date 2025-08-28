---
solution: Journey Optimizer
product: journey optimizer
title: Pasos de configuración
description: Obtenga información sobre cómo crear un esquema relacional en Adobe Experience Platform cargando un DDL
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
source-git-commit: c1201025af216f8f3019e7696b6eb906962b681b
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 31%

---


# Introducción a esquemas relacionales y conjuntos de datos{#gs-schemas}

Esta guía muestra el proceso de creación de un esquema relacional, configuración de un conjunto de datos para campañas organizadas e ingesta de datos.

![](assets/do-not-localize/schema_admin.png)

Un conjunto de datos es una construcción de almacenamiento y administración para una colección de datos, normalmente una tabla, que contiene un esquema (columnas) y campos (filas). Los datos que se incorporan correctamente a Experience Platform se almacenan dentro del lago de datos como conjuntos de datos.

Un esquema representa y valida la estructura y el formato de los datos. Proporciona una definición abstracta de un objeto del mundo real (por ejemplo, una persona) y describe qué datos deben incluirse en cada instancia de ese objeto (como, por ejemplo, nombre, cumpleaños, etc.).


1. Crear [esquema relacional manualmente](manual-schema.md) o [con un archivo DDL](file-upload-schema.md)

   Defina la estructura del modelo de datos, incluidas las tablas, los atributos y las relaciones. Elija crear el esquema manualmente en la interfaz de usuario o cargar un archivo DDL para una configuración más rápida.

   Al crear el esquema manualmente, el conjunto de datos también debe crearse y habilitarse manualmente. Al utilizar un archivo DDL, la creación y la activación de conjuntos de datos son automáticas.

1. [Vínculo del esquema](file-upload-schema.md)

   Establezca relaciones entre los esquemas para garantizar la coherencia de los datos y habilitar consultas entre entidades. Por ejemplo, vincule las transacciones de lealtad a los destinatarios o las recompensas a las marcas.

1. [Ingesta de datos](ingest-data.md)

   Incluya datos en Adobe Experience Platform desde fuentes compatibles como SFTP, almacenamiento en la nube o bases de datos.

