---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los conjuntos de datos
description: Obtenga información sobre cómo utilizar conjuntos de datos de Adobe Experience Platform en Adobe Journey Optimizer
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 7e27f5502d64d0c91de2c67e4011e650e77c6a92
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 0%

---

# Introducción a los conjuntos de datos {#datasets-gs}

Todos los datos que se incorporan en Adobe Experience Platform se conservan dentro del lago de datos como conjuntos de datos. Un conjunto de datos es una construcción de almacenamiento y administración para una recopilación de datos, normalmente una tabla, que contiene un esquema (columnas) y campos (filas).

## Acceso a conjuntos de datos{#access-datasets}

La variable **Conjuntos de datos** espacio de trabajo en [!DNL Adobe Journey Optimizer] la interfaz de usuario de le permite explorar datos y crear conjuntos de datos.

Select **Conjuntos de datos** en el panel de navegación izquierdo para abrir el tablero Conjuntos de datos .

![](assets/datasets-home.png)

Adición de datos a [!DNL Adobe Experience Platform] es la base para crear un perfil. A continuación, podrá aprovechar los perfiles en [!DNL Adobe Journey Optimizer]. En primer lugar, defina esquemas, utilice herramientas de ETL para preparar y estandarizar sus datos y, a continuación, cree conjuntos de datos basados en sus esquemas.

Seleccione el **Examinar** para mostrar la lista de todos los conjuntos de datos disponibles para su organización. Se muestran los detalles de cada conjunto de datos enumerado, incluido su nombre, el esquema al que se adhiere el conjunto de datos y el estado de la ejecución de ingesta más reciente.

De forma predeterminada, solo se muestran los conjuntos de datos que ha introducido en . Si desea ver los conjuntos de datos generados por el sistema, habilite la variable **Mostrar conjuntos de datos del sistema** desde el filtro.

![](assets/ajo-system-datasets.png)

Seleccione el nombre de un conjunto de datos para acceder a la pantalla de actividad de conjunto de datos y ver los detalles del conjunto de datos seleccionado. La pestaña actividad incluye un gráfico que visualiza la tasa de consumo de los mensajes, así como una lista de lotes correctos y fallidos.

Estos son los diferentes conjuntos de datos disponibles:

**Informes**

* _Sistema de informes: conjunto de datos del evento de comentarios de mensajes_: Registros de envío de mensajes. Información sobre la entrega de mensajes desde Journey Optimizer con fines de creación de informes y segmentos. Los comentarios de los ISP de correo electrónico sobre las devoluciones también se registran en este conjunto de datos.
* _Creación de informes: conjunto de datos de evento de experiencia de seguimiento de correo electrónico_: Registros de interacción para el canal de correo electrónico que se utiliza para la creación de informes y segmentos. La información almacenada informa sobre las acciones realizadas por el usuario final en el correo electrónico (aperturas, clics, etc.).
* _Creación de informes: conjunto de datos de evento de experiencia de seguimiento push_: Registros de interacción para el canal push que se utilizan con fines de creación de informes y segmentos. La información almacenada informa sobre las acciones realizadas por el usuario final en las notificaciones push.
* _Creación de informes: Evento de paso de recorrido_: Captura todos los eventos de experiencia de los pasos del recorrido generados desde Journey Optimizer para que los consuman servicios como Reporting. También es fundamental para crear informes en Customer Journey Analytics para análisis de año y año. Vinculado a metadatos de recorrido.
* _Informes: recorridos_: Información sobre el alojamiento del conjunto de datos de metadatos de cada paso de un recorrido.
* _Informes - CCO_: Conjunto de datos del evento de comentarios que almacena los registros de envío de los correos electrónicos CCO. Para su uso en informes.

**Consentimiento**

* _Conjunto de datos del servicio de consentimiento_: almacena información de consentimiento de un perfil.

**Servicios inteligentes**

* _Puntuaciones de optimización en tiempo de envío/Puntuaciones de participación_: Puntuaciones de salida de Journey AI.

## Vista previa de conjuntos de datos{#preview-datasets}

En la pantalla de actividad Conjunto de datos, seleccione **Vista previa del conjunto de datos** cerca de la esquina superior derecha de la pantalla para obtener una vista previa del lote exitoso más reciente en este conjunto de datos. Cuando un conjunto de datos está vacío, el vínculo de vista previa se desactiva.

![](assets/dataset-preview.png)

## Crear conjuntos de datos{#create-datasets}

Para crear un nuevo conjunto de datos, comience seleccionando **Crear conjunto de datos** en el tablero Conjuntos de datos .

Puede:

* Crear conjunto de datos a partir del esquema. [Obtenga más información en esta documentación](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target=&quot;_blank&quot;}
* Cree un conjunto de datos a partir del archivo CSV. [Obtenga más información en esta documentación](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html){target=&quot;_blank&quot;}

Vea este vídeo para aprender a crear un conjunto de datos, asignarlo a un esquema, agregarle datos y confirmar que se han introducido los datos.

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)

## Administración de datos

En un conjunto de datos, examine la **Administración de datos** para comprobar las etiquetas en el conjunto de datos y en el nivel de campo. Administración de datos categoriza los datos según el tipo de políticas que se apliquen.

Una de las funciones principales de [!DNL Adobe Experience Platform] es reunir los datos de varios sistemas empresariales para permitir que los especialistas en marketing identifiquen, comprendan y capten mejor a los clientes. Estos datos pueden estar sujetos a restricciones de uso definidas por su organización o por las regulaciones legales. Por lo tanto, es importante asegurarse de que sus operaciones de datos cumplan las políticas de uso de los datos.

[!DNL Adobe Experience Platform Data Governance] le permite administrar los datos de los clientes y garantizar el cumplimiento de las regulaciones, restricciones y políticas aplicables al uso de los datos. Desempeña un papel clave en Experience Platform en varios niveles, incluida la catalogación, el linaje de datos, el etiquetado del uso de los datos, las políticas de uso de los datos y el control del uso de los datos para las acciones de marketing.

Obtenga más información sobre Administración de datos y etiquetas de uso de datos en la [Documentación de control de datos](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/user-guide.html){target=&quot;_blank&quot;}

## Ejemplos y casos de uso{#uc-datasets}

Obtenga información sobre cómo crear un esquema, un conjunto de datos y la ingesta de datos para añadir perfiles de prueba en Adobe Journey Optimizer en [esta muestra completa](../segment/creating-test-profiles.md)

Obtenga más información sobre la creación de conjuntos de datos en [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}.

Aprenda a utilizar la interfaz de usuario de conjuntos de datos en la [Documentación general de la ingesta de datos](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html){target=&quot;_blank&quot;}.

Hay disponible una lista de casos de uso con ejemplos de consulta [here](../data/datasets-query-examples.md).

**Consulte también**

* [Información general sobre la ingesta de flujos](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html){target=&quot;_blank&quot;}
* [Ingesta de datos en Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html){target=&quot;_blank&quot;}
