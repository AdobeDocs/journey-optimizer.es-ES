---
solution: Journey Optimizer
product: journey optimizer
title: Exportación de conjuntos de datos a ubicaciones de almacenamiento en la nube
description: Obtenga información sobre cómo exportar conjuntos de datos mediante destinos de almacenamiento en la nube de Adobe Experience Platform.
feature: Datasets
role: User
level: Beginner
keywords: plataforma, lago de datos, crear, lago, conjuntos de datos, perfil
exl-id: 66b5c691-ddc4-4e9b-9386-2ce6c307451c
source-git-commit: f2d4531bd3b0b84dc1b52e818cbbeee36733314f
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 9%

---

# Exportación de conjuntos de datos a ubicaciones de almacenamiento en la nube {#export-datasets}

Journey Optimizer le permite establecer una conexión activa con ubicaciones de almacenamiento en la nube para exportar el contenido de sus conjuntos de datos.

Al exportar periódicamente los datos, puede asegurarse de que dispone de un registro completo y actualizado de las interacciones de los clientes, lo que lo hace fácilmente disponible para fines de creación de informes, archivado o análisis de datos.

## Destinos de almacenamiento en la nube disponibles {#destinations}

Puede exportar conjuntos de datos a 6 destinos de almacenamiento en la nube a los que se puede acceder desde el **[!UICONTROL Destinos]** menú, en el **[!UICONTROL Catálogo]** pestaña.

![](assets/dataset-export-setup.png)


Encontrará información detallada sobre cada destino en la documentación de Adobe Experience Platform:

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html)
* [Azure Data Lake Gen 2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html)
* [Zona de aterrizaje de datos](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html)
* [Almacenamiento de Google Cloud](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html)

## Conjuntos de datos disponibles para exportar {#datasets}

Comprenda, a partir de la tabla siguiente, qué conjuntos de datos de Journey Optimizer puede exportar.

| Conjunto de datos | Descripción |
| ------- | ------- | 
| Conjunto de datos de evento de comentarios AJO BCC | Conjunto de datos de evento de comentarios AJO BCC |
| Conjunto de datos de clasificación AJO | Conjunto de datos para la ingesta de eventos de comentarios de aplicaciones push y de correo electrónico desde Journey Optimizer. Creado mediante SDK. |
| Conjunto de datos del servicio de consentimiento AJO | Almacena la información de consentimiento de un perfil. |
| Conjunto de datos de evento de experiencia de seguimiento de correo electrónico AJO | Registros de interacción del canal de correo electrónico que se utilizan para fines de creación de informes y audiencias.  |
| Conjunto de datos de entidad de AJO | Conjunto de datos para almacenar metadatos de entidad para mensajes enviados al usuario final.  |
| Conjunto de datos de evento de actividad entrante AJO | Conjunto de datos para canales web e inApp de Journey Optimizer para eventos de envío e interacción. |
| Conjunto de datos del perfil de mensajería interactiva AJO | Almacena perfiles creados para admitir campañas activadas por API |
| Conjunto de datos de evento de comentarios de mensajes AJO | Registros de envío de mensajes. Información sobre el envío de mensajes desde Journey Optimizer con fines de creación de informes y públicos. Los comentarios de los ISP de correo electrónico sobre los rechazos también se registran en este conjunto de datos. |
| Extensión de contadores de perfil AJO | Contiene un mapa de objetos que contienen counter_value y expiryDate, escrito por counter_id |
| Conjunto de datos del perfil push AJO | Almacena tokens push de un perfil. |
| Conjunto de datos de evento de experiencia de seguimiento push AJO | Registros de interacción del canal push que se utilizan para fines de creación de informes y audiencias.  |
| Conjunto de datos de superficies AJO | Conjunto de datos vacío relacionado con el esquema de superficies entrantes de Journey Optimizer |
| AOOutputForUPSDataset | Contiene todas las pertenencias a audiencias de AO que se van a escribir en UPS |
| Conjunto de datos del perfil de Audience Orchestration | Generado por composición de audiencia para audiencias de Composición de audiencia. Contiene todas las audiencias de Composición de audiencias, sus atributos y datos de enriquecimiento |
| Repositorio de objetos de decisión: actividades | también se conoce como Decisiones en la interfaz de usuario. Pero estos son los objetos que crea un usuario que reúne todos los componentes, incluida la lógica de toma de decisiones. Por ejemplo, para una ubicación concreta (ubicación), qué ofertas deben considerarse (colección de ofertas) y qué método de clasificación utilizar en esas ofertas. |
| Repositorio de objetos de decisión: ofertas de reserva | este es el repositorio para el otro tipo de oferta que crea un usuario. Específicamente, si no cumplen los requisitos para ver una oferta personalizada y necesitan ver algo, al menos verán la oferta de reserva. Este conjunto de datos contiene los atributos para este tipo de oferta |
| Repositorio de objetos de decisión: ofertas personalizadas | este es el repositorio de un tipo de oferta que crea un usuario. Por lo tanto, este conjunto de datos contiene los atributos sobre este tipo de oferta | Ultimate |
| Repositorio de objetos de decisión: ubicaciones | este es el repositorio de objetos que definen la ubicación de donde debe mostrarse una oferta. |
| Eventos de paso de recorrido | Registra todos los eventos de experiencia de los pasos de Recorrido generados desde Journey Optimizer que deben consumir servicios como Creación de informes. |
| Recorridos | Información del alojamiento del conjunto de datos de metadatos de cada paso en un recorrido |
| ODE DecisionEvents: toma de decisiones de producción | Cada vez que tomamos una decisión basada en una solicitud, la consideramos un evento de decisión |

## Requisitos previos {#prerequisites}

Para exportar conjuntos de datos, necesita el [permisos de control de acceso](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions) se enumera a continuación. Lea el [información general de control de acceso](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html) o póngase en contacto con el administrador del producto para obtener los permisos necesarios.

| Categoría | Permiso |
|--|--|
| Destinos | Administrar y activar destinos de conjuntos de datos |
| Administración de datos | Ver conjuntos de datos |
| Destinos | Ver destinos |

## Pasos principales para exportar conjuntos de datos {#main-steps}

Los pasos principales para exportar un conjunto de datos a una ubicación de almacenamiento en la nube son los siguientes:

![](assets/dataset-export-process.png)

Encontrará información detallada sobre cada paso en la documentación de Adobe Experience Platform: [Exportar conjuntos de datos a destinos de almacenamiento en la nube](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html).

1. **Configure su destino de almacenamiento en la nube**. Si aún no lo ha hecho, conéctese a un destino de almacenamiento en la nube desde el catálogo de destinos. [Obtenga información sobre cómo crear una nueva conexión de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html#setup)

   <!--![](assets/dataset-export-setup.png)-->

1. **Seleccione el destino de almacenamiento en la nube** donde desee exportar los conjuntos de datos. En el catálogo de destinos, haga clic en **[!UICONTROL Exportar conjuntos de datos]** en la tarjeta deseada y seleccione la conexión que desea utilizar.

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >Si utiliza Adobe Journey Optimizer junto con los perfiles del cliente en tiempo real, las tarjetas de destino mostrarán un botón &quot;Activar&quot;, que le permitirá exportar conjuntos de datos y activar audiencias para este destino, según los permisos que haya activado.

1. **Seleccionar los conjuntos de datos** que desea exportar al destino seleccionado. [Obtenga más información sobre los conjuntos de datos de Journey Optimizer disponibles para exportar](#datasets)

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **Programación de la exportación** del conjunto de datos. Especifique cuándo debe iniciarse la exportación y con qué frecuencia debe producirse.

   <!--![](assets/dataset-export-schedule.png)-->

1. **Revise y confirme la exportación** comprobando el resumen que se muestra al final de la configuración.

   <!--![](assets/dataset-export-review.png)-->

Una vez completada la exportación, el contenido del conjunto de datos se deposita en la ubicación de almacenamiento en la nube según la programación configurada. [Obtenga información sobre cómo verificar la exportación de conjuntos de datos correcta](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify)
