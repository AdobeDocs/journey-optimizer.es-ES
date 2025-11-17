---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los conjuntos de datos
description: Obtenga información sobre cómo utilizar conjuntos de datos de Adobe Experience Platform en Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: plataforma, lago de datos, crear, lago, conjuntos de datos, perfil
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '873'
ht-degree: 100%

---

# Introducción a los conjuntos de datos {#datasets-gs}

Todos los datos que se incorporan a Adobe Experience Platform se conservan dentro del lago de datos como conjuntos de datos. Un conjunto de datos es una construcción de almacenamiento y administración para una colección de datos, normalmente una tabla, que contiene un esquema (columnas) y campos (filas).

## Acceso a conjuntos de datos{#access-datasets}

El espacio de trabajo **Conjuntos de datos** en la interfaz de usuario de [!DNL Adobe Journey Optimizer] le permite explorar datos y crear conjuntos de datos.

Seleccione **Conjuntos de datos** en el panel de control de navegación izquierdo para abrir el panel de control Conjuntos de datos.

![](assets/datasets-home.png)

Añadir datos a [!DNL Adobe Experience Platform] es la base para crear un perfil. A continuación, podrá aprovechar los perfiles en [!DNL Adobe Journey Optimizer]. En primer lugar, defina esquemas, utilice herramientas de ETL para preparar y estandarizar sus datos y, a continuación, cree conjuntos de datos basados en sus esquemas.

Seleccione la pestaña **Examinar** para mostrar la lista de todos los conjuntos de datos disponibles para su organización. Se muestran los detalles de cada conjunto de datos enumerado, incluido su nombre, el esquema al que se adhiere el conjunto de datos y el estado de la ejecución de ingesta más reciente.

De forma predeterminada, solo se muestran los conjuntos de datos que ha introducido. Si desea ver los conjuntos de datos generados por el sistema, habilite el conmutador **Mostrar conjuntos de datos del sistema** desde el filtro.

![](assets/ajo-system-datasets.png)

>[!NOTE]
>
>A partir del 1 de noviembre de 2024, la segmentación de streaming ya no admite eventos de envío y apertura de conjuntos de datos de seguimiento y comentarios [!DNL Journey Optimizer]. Para implementar la restricción de frecuencia o la administración de fatiga, utilice reglas empresariales en su lugar. Puede encontrar más detalles en [esta sección](../conflict-prioritization/rule-sets.md), incluyendo una explicación de caso de uso para el límite diario [aquí](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510){target="_blank"}.
>
>Además, desde febrero de 2025, se implementa un mecanismo de protección de tiempo de vida (TTL) en los conjuntos de datos generados por el sistema de Journey Optimizer. [Más información](datasets-ttl.md)

Seleccione el nombre de un conjunto de datos para acceder a su pantalla de actividad de conjunto de datos y ver los detalles del conjunto de datos seleccionado. La pestaña actividad incluye un gráfico que visualiza la tasa de consumo de los mensajes, así como una lista de lotes correctos y fallidos.

A continuación se enumeran los conjuntos de datos del sistema para Adobe Journey Optimizer.

>[!CAUTION]
>
> Los conjuntos de datos del sistema **no se debe modificar**. Cualquier cambio se revierte automáticamente con cada actualización de producto.

**Creación de informes**

* _Informes: conjunto de datos del evento de comentarios de mensajes_: registros de envío de mensajes. Información sobre el envío de mensajes desde Journey Optimizer con fines de creación de informes y públicos. Los comentarios de los ISP de correo electrónico sobre los rechazos también se registran en este conjunto de datos.
* _Creación de informes: conjunto de datos de evento de experiencia de seguimiento del correo electrónico_: registros de interacción para el canal de correo electrónico que se utiliza para la creación de informes y públicos. La información almacenada se refiere a las acciones realizadas por el usuario final en el correo electrónico (aperturas, clics, etc.).
* _Creación de informes: conjunto de datos de evento de experiencia de seguimiento push_: registros de interacción para canales push que se utilizan con fines de creación de informes y públicos. La información almacenada informa sobre las acciones realizadas por el usuario final en las notificaciones push.
* _Informes: evento de paso de recorrido_: captura todos los eventos de experiencia de los pasos de Recorrido generados desde Journey Optimizer para que los consuman servicios como Informes. También es fundamental para crear informes en Customer Journey Analytics para análisis YoY. Vinculado a metadatos de recorrido.
* _Informes: recorridos_: información sobre el alojamiento del conjunto de datos de metadatos de cada paso de un recorrido.
* _Informes - CCO_: conjunto de datos del evento de comentarios que almacena los registros de envío de los correos electrónicos CCO. Se utilizarán para elaborar informes.

**Consentimiento**

* _Conjunto de datos del servicio de consentimiento_: almacena información de consentimiento de un perfil.

**Servicios inteligentes**

* _Puntuaciones de optimización del tiempo de envío/Puntuaciones de participación_: resultados de inteligencia artificial aplicada a la trayectoria.

Para ver la lista completa de campos y atributos para cada esquema, consulte el [diccionario del esquema de Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=es){target="_blank"}.

## Previsualizar conjuntos de datos{#preview-datasets}

En la pantalla de actividad Conjunto de datos, seleccione **Previsualizar conjunto de datos** junto a la esquina superior derecha de la pantalla para obtener una vista previa del lote correcto más reciente en este conjunto de datos. Cuando un conjunto de datos está vacío, el vínculo de previsualización se desactiva.

![](assets/dataset-preview.png)

## Crear conjuntos de datos{#create-datasets}

Para crear un nuevo conjunto de datos, empiece seleccionando **Crear conjunto de datos** en el panel de control Conjuntos de datos.

Puede hacer lo siguiente:

* Crear conjunto de datos a partir de esquema. [Obtenga más información en esta documentación](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=es#schema){target="_blank"}
* Cree un conjunto de datos a partir del archivo CSV. [Obtenga más información en esta documentación](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=es){target="_blank"}

Obtenga información sobre cómo crear un conjunto de datos, asignarlo a un esquema, añadirle datos y confirmar que estos se han introducido.

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)

## Gobernanza de datos

En un conjunto de datos, examine la pestaña **Gobernanza de datos** para comprobar las etiquetas en el conjunto de datos y en el nivel de campo. La gobernanza de datos categoriza los datos según el tipo de políticas que se apliquen.

Una de las funciones principales de [!DNL Adobe Experience Platform] es reunir los datos de varios sistemas empresariales para permitir que los especialistas en marketing identifiquen, comprendan e interactúe mejor con los clientes. Estos datos pueden estar sujetos a restricciones de uso definidas por su organización o por la normativa legal. Por lo tanto, es importante asegurarse de que sus operaciones de datos cumplan las políticas de uso de los datos.

[!DNL Adobe Experience Platform Data Governance] le permite administrar los datos de los clientes y garantizar el cumplimiento de las regulaciones, restricciones y políticas aplicables al uso de los datos. Desempeña un papel clave dentro de Experience Platform en varios niveles, incluida la catalogación, el linaje de datos, el etiquetado del uso de los datos, las políticas de uso de los datos y el control del uso de los datos para las acciones de marketing.

Obtenga más información sobre la gobernanza de datos y etiquetas de uso de datos en la [documentación de la gobernanza de datos](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/user-guide.html?lang=es){target="_blank"}.

## Ejemplos y casos de uso{#uc-datasets}

Obtenga información sobre cómo crear un esquema, un conjunto de datos y la introducción de datos para añadir perfiles de prueba en Adobe Journey Optimizer en [esta muestra de extremo a exteremo](../audience/creating-test-profiles.md)

Obtenga más información sobre la creación de conjuntos de datos en la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=es){target="_blank"}.

Aprenda a utilizar la interfaz de usuario de conjuntos de datos en la [documentación general sobre la ingesta de datos](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=es){target="_blank"}.

[Aquí](../data/datasets-query-examples.md) dispone de una lista de casos de uso con ejemplos de consulta.

>[!MORELIKETHIS]
>
>* [Información general sobre la ingesta de streaming](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=es){target="_blank"}
>* [Ingesta de datos en Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html?lang=es){target="_blank"}
