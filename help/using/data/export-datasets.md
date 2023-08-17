---
solution: Journey Optimizer
product: journey optimizer
title: Exportación de conjuntos de datos a ubicaciones de almacenamiento en la nube
description: Obtenga información sobre cómo exportar conjuntos de datos mediante destinos de almacenamiento en la nube de Adobe Experience Platform.
role: User
level: Beginner
badge: label="Beta" type="Informative"
keywords: plataforma, lago de datos, crear, lago, conjuntos de datos, perfil
exl-id: 66b5c691-ddc4-4e9b-9386-2ce6c307451c
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 4%

---

# Exportación de conjuntos de datos a ubicaciones de almacenamiento en la nube {#export-datasets}

>[!AVAILABILITY]
>
>La función de exportación de conjuntos de datos se encuentra actualmente en fase beta y está disponible para todos los usuarios de Adobe Journey Optimizer.

Journey Optimizer le permite establecer una conexión activa con ubicaciones de almacenamiento en la nube para exportar el contenido de sus conjuntos de datos.

Al exportar periódicamente los datos, puede asegurarse de que dispone de un registro completo y actualizado de las interacciones con los clientes, de que utiliza esta información con fines de informes o análisis y de que cumple los requisitos legales.

## Destinos de almacenamiento en la nube disponibles {#destinations}

Puede exportar conjuntos de datos a 6 destinos de almacenamiento en la nube a los que se puede acceder desde el **[!UICONTROL Destinos]** menú, en el **[!UICONTROL Catálogo]** pestaña.

![](assets/dataset-export-setup.png)

>[!AVAILABILITY]
>
>Todos estos destinos están disponibles en versión beta y sujetos a cambios.

Encontrará información detallada sobre cada destino en la documentación de Adobe Experience Platform:

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html)
* [Azure Data Lake Gen 2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html)
* [Zona de aterrizaje de datos](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html)
* [Almacenamiento de Google Cloud](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html)

## Requisitos previos {#prerequisites}

Compruebe los siguientes requisitos previos antes de empezar a exportar los conjuntos de datos:

* Para exportar conjuntos de datos, necesita el **Ver destinos** y **Administrar y activar destinos de conjuntos de datos** [permisos de control de acceso](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions). Lea el [información general de control de acceso](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html) o póngase en contacto con el administrador del producto para obtener los permisos necesarios.

* Asegúrese de que el conjunto de datos que desea exportar no contenga datos de segunda generación. Esta función solo admite la exportación de datos de primera generación, es decir, datos sin procesar tal como se definen en la [Descripción del producto de Real-time Customer Data Platform](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2c-edition-prime-and-ultimate-packages.html). Los datos de primera generación incluyen conjuntos de datos traídos a través de fuentes de Adobe Experience Platform o conjuntos de datos recopilados mediante soluciones de Adobe como el conector de datos de Analytics y registros de Journey Optimizer/conjuntos de datos de informes.

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

1. **Seleccionar los conjuntos de datos** que desea exportar al destino seleccionado.

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **Programación de la exportación** del conjunto de datos. Especifique cuándo debe iniciarse la exportación y con qué frecuencia debe producirse.

   <!--![](assets/dataset-export-schedule.png)-->

1. **Revise y confirme la exportación** comprobando el resumen que se muestra al final de la configuración.

   <!--![](assets/dataset-export-review.png)-->

Una vez completada la exportación, el contenido del conjunto de datos se deposita en la ubicación de almacenamiento en la nube según la programación configurada. [Obtenga información sobre cómo verificar la exportación de conjuntos de datos correcta](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify)
