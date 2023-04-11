---
solution: Journey Optimizer
product: journey optimizer
title: Exportar conjuntos de datos a ubicaciones de almacenamiento en la nube
description: Obtenga información sobre cómo exportar sus conjuntos de datos mediante destinos de almacenamiento en la nube de Adobe Experience Platform.
role: User
level: Beginner
badge: label="Beta" type="Informative"
keywords: plataforma, lago de datos, crear, lago, conjuntos de datos, perfil
source-git-commit: c3ad875b50999da833d75e97a787cab9e24e38d4
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 4%

---


# Exportar conjuntos de datos a ubicaciones de almacenamiento en la nube {#export-datasets}

>[!AVAILABILITY]
>
>La función de exportación de conjuntos de datos está actualmente en fase beta y está disponible para todos los usuarios de Adobe Journey Optimizer. Póngase en contacto con su representante de Adobe para obtener acceso a los destinos si todavía no tiene acceso.

Journey Optimizer le permite establecer una conexión activa con ubicaciones de almacenamiento en la nube para exportar el contenido de sus conjuntos de datos.

Al exportar periódicamente los datos, puede asegurarse de que dispone de un registro completo y actualizado de las interacciones de los clientes, utilizar esta información para realizar informes o análisis y mantener el cumplimiento de los requisitos legales.

## Destinos de almacenamiento en la nube disponibles {#destinations}

Puede exportar conjuntos de datos a 6 destinos de almacenamiento en la nube a los que se puede acceder desde **[!UICONTROL Destinos]** en el **[!UICONTROL Catálogo]** pestaña .

![](assets/dataset-export-setup.png)

>[!AVAILABILITY]
>
>Todos estos destinos están disponibles en versión beta y están sujetos a cambios.

Encontrará información detallada sobre cada destino en la documentación de Adobe Experience Platform:

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html)
* [Azure Data Lake Gen 2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html)
* [Zona de aterrizaje de datos](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html)
* [Almacenamiento en la nube de Google](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html)

## Requisitos previos {#prerequisites}

Compruebe los siguientes requisitos previos antes de empezar a exportar sus conjuntos de datos:

* Para exportar conjuntos de datos, necesita la variable **Administrar destinos**, **Ver destinos**, **Activar destinos** y **Administrar y activar destinos de conjuntos de datos** [permisos de control de acceso](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions). Lea el [información general sobre el control de acceso](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html) o póngase en contacto con el administrador del producto para obtener los permisos necesarios.

* Esta función solo admite la exportación de datos de primera generación, es decir, datos sin procesar según se definen en la variable [Descripción del producto de Real-time Customer Data Platform](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2c-edition-prime-and-ultimate-packages.html). Asegúrese de que el conjunto de datos que desea exportar no contenga datos de segunda generación.

## Pasos principales para exportar conjuntos de datos {#main-steps}

Los pasos principales para exportar un conjunto de datos a una ubicación de almacenamiento en la nube son los siguientes:

![](assets/dataset-export-process.png)

Encontrará información detallada sobre cada paso en la documentación de Adobe Experience Platform: [Exportar conjuntos de datos a destinos de almacenamiento en la nube](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en).

1. **Configuración del destino de almacenamiento en la nube**. Si aún no lo ha hecho, conéctese a un destino de almacenamiento en la nube desde el catálogo de destinos. [Obtenga información sobre cómo crear una nueva conexión de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=en#setup)

   <!--![](assets/dataset-export-setup.png)-->

1. **Seleccione el destino de almacenamiento en la nube** donde desea exportar sus conjuntos de datos. En el catálogo de destinos, haga clic en el botón **[!UICONTROL Exportación de conjuntos de datos]** en la tarjeta deseada y seleccione la conexión que desea utilizar.

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >Si utiliza Adobe Journey Optimizer junto con perfiles de cliente en tiempo real, las tarjetas de destino mostrarán el botón &quot;Activar&quot;, que le permite exportar conjuntos de datos y activar segmentos para este destino, en función de los permisos que haya habilitado.

1. **Seleccionar los conjuntos de datos** que desea exportar al destino seleccionado.

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **Programar la exportación** del conjunto de datos. Especifique cuándo debe iniciarse la exportación y con qué frecuencia debe producirse.

   <!--![](assets/dataset-export-schedule.png)-->

1. **Revisar y confirmar la exportación** comprobando el resumen que aparece al final de la configuración.

   <!--![](assets/dataset-export-review.png)-->

Una vez finalizada la exportación, el contenido del conjunto de datos se deposita en la ubicación de almacenamiento en la nube según la programación que haya configurado. [Obtenga información sobre cómo verificar una exportación correcta del conjunto de datos](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify)
