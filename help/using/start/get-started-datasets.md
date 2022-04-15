---
title: Introducción a los conjuntos de datos
description: Obtenga información sobre cómo utilizar conjuntos de datos de Adobe Experience Platform en Adobe Journey Optimizer
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 9ebcfd6c41c17fe3be0423822209443fc55244a7
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 11%

---

# Introducción a los conjuntos de datos {#datasets-gs}

Todos los datos que se incorporan en Adobe Experience Platform se conservan dentro del lago de datos como conjuntos de datos. Un conjunto de datos es una construcción de almacenamiento y administración para una colección de datos, normalmente una tabla, que contiene un esquema (columnas) y campos (filas).

## Acceso a conjuntos de datos{#access-datasets}

La variable **Conjuntos de datos** espacio de trabajo en [!DNL Adobe Journey Optimizer] la interfaz de usuario de le permite explorar datos y crear conjuntos de datos.

Select **Conjuntos de datos** en el panel de navegación izquierdo para abrir el tablero Conjuntos de datos .

![](assets/datasets-home.png)

Añadir datos a Adobe Experience Platform es la base para crear un perfil. A continuación, podrá aprovechar los perfiles en [!DNL Adobe Journey Optimizer]. En primer lugar, defina esquemas, utilice herramientas de ETL para preparar y estandarizar sus datos y, a continuación, cree conjuntos de datos basados en sus esquemas.

Seleccione el **Examinar** para mostrar la lista de todos los conjuntos de datos disponibles para su organización. Se muestran los detalles de cada conjunto de datos enumerado, incluido su nombre, el esquema al que se adhiere el conjunto de datos y el estado de la ejecución de ingesta más reciente.

De forma predeterminada, solo se muestran los conjuntos de datos que ha introducido en . Si desea ver los conjuntos de datos generados por el sistema, habilite la variable **Mostrar conjuntos de datos del sistema** desde el filtro.

![](assets/ajo-system-datasets.png)

Seleccione el nombre de un conjunto de datos para acceder a la pantalla de actividad de conjunto de datos y ver los detalles del conjunto de datos seleccionado. La pestaña actividad incluye un gráfico que visualiza la tasa de consumo de los mensajes, así como una lista de lotes correctos y fallidos.

## Crear conjuntos de datos{#create-datasets}

Para crear un nuevo conjunto de datos, comience seleccionando **Crear conjunto de datos** en el tablero Conjuntos de datos .

Puede:

* Crear conjunto de datos a partir del esquema. [Obtenga más información en esta documentación](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target=&quot;_blank&quot;}
* Cree un conjunto de datos a partir del archivo CSV. [Obtenga más información en esta documentación](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=es){target=&quot;_blank&quot;}


Vea este vídeo para aprender a crear un conjunto de datos, asignarlo a un esquema, agregarle datos y confirmar que se han introducido los datos.

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)


Obtenga información sobre cómo crear un esquema, un conjunto de datos y la ingesta de datos para añadir perfiles de prueba en Adobe Journey Optimizer en [esta muestra completa](../segment/creating-test-profiles.md)

Obtenga más información sobre la creación de conjuntos de datos en [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}.

Aprenda a utilizar la interfaz de usuario de conjuntos de datos en la [Documentación general de la ingesta de datos](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=es){target=&quot;_blank&quot;}.


**Consulte también**

* [Crear un esquema, un conjunto de datos e introducir datos para añadir perfiles de prueba en Journey Optimizer](../segment/creating-test-profiles.md)
* [Información general sobre la ingesta de flujos](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=es){target=&quot;_blank&quot;}
* [Ingesta de datos en Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html){target=&quot;_blank&quot;}
