---
title: Configuración de correo postal
description: Obtenga información sobre cómo configurar el canal de correo postal en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: bca233ab888e2ca33b866bc3def31653f2d55ea9
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# Configuración de correo postal {#direct-mail-configuration}

[!DNL Journey Optimizer] le permite personalizar y generar los archivos requeridos por los proveedores de correo postal para enviar correos a sus clientes.

When [creación de un mensaje de correo postal](../messages/create-direct-mail.md), puede definir los datos de audiencia de destino, incluida la información de contacto elegida (dirección postal, por ejemplo). A continuación, se genera y exporta automáticamente un archivo que contiene estos datos a un servidor, donde su proveedor de correo postal podrá recuperarlo y hacerse cargo del envío real.

Antes de poder generar este archivo, debe crear:

1. A [configuración de enrutamiento de archivos](#file-routing-configuration) para especificar el servidor donde se exportará el archivo.

1. A [superficie de correo postal](#direct-mail-surface) que hará referencia a la configuración de enrutamiento del archivo.

>[!CAUTION]
>
>Si no ha configurado ninguna opción de enrutamiento de archivos, no podrá crear una superficie de correo postal.

## Configuración del enrutamiento de archivos {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Definir la configuración de enrutamiento de archivos"
>abstract="Después de crear un mensaje de correo postal, el archivo que contiene los datos de audiencia de destino se genera y exporta a un servidor. Debe especificar los detalles del servidor para que su proveedor de correo postal pueda acceder y utilizar ese archivo para enviar correo postal."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/create-direct-mail.html" text="Crear un mensaje de correo postal"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="Definir la configuración de enrutamiento de archivos"
>abstract="Debe definir dónde se exportará el archivo para que lo utilice su proveedor de correo postal."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="Configuración de enrutamiento de archivos"
>abstract="Seleccione la configuración de enrutamiento de archivos que elija, que define dónde se exportará el archivo para que lo utilice su proveedor de correo postal."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="Seleccione el tipo de servidor para el archivo"
>abstract="Elija qué tipo de servidor desea utilizar para exportar los archivos de correo postal. Actualmente, Journey Optimizer solo admite Amazon S3 y SFTP."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="Elija la región de AWS"
>abstract="Seleccione la región geográfica del servidor de AWS donde desea exportar los archivos de correo postal. Como práctica general, se prefiere elegir la región más cercana a la ubicación del proveedor de correo postal."

Para enviar un mensaje de correo postal, [!DNL Journey Optimizer] genera y exporta el archivo que contiene los datos de audiencia de destino a un servidor.

Debe especificar los detalles del servidor para que su proveedor de correo postal pueda acceder y utilizar ese archivo para enviar correo.

Para configurar el enrutamiento del archivo, siga los pasos a continuación.

1. Acceda a la **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de enrutamiento de archivos]** > **[!UICONTROL Enrutamiento de archivos]** a continuación, haga clic en **[!UICONTROL Crear configuración de enrutamiento]**.

   ![](assets/file-routing-config-button.png)

1. Establezca un nombre para la configuración.

1. Seleccione el **[!UICONTROL Tipo de servidor]** que desea utilizar para exportar los archivos de correo postal.

   ![](assets/file-routing-config-type.png)

   >[!NOTE]
   >
   >Actualmente solo Amazon S3 y SFTP son compatibles con [!DNL Journey Optimizer].

1. Rellene los detalles y las credenciales del servidor, como la dirección del servidor, la clave de acceso, etc.

   ![](assets/file-routing-config-sftp-details.png)

1. Si ha seleccionado **[!UICONTROL Amazon S3]**, elija el **[!UICONTROL Región de AWS]** donde se ubicará la infraestructura del servidor.

   ![](assets/file-routing-config-aws-region.png)

   >[!NOTE]
   >
   >Las regiones de AWS son áreas geográficas que AWS utiliza para alojar sus infraestructuras de nube. Como práctica general, se prefiere elegir la región más cercana a la ubicación del proveedor de correo postal.

1. Seleccione **[!UICONTROL Enviar]**. La configuración de enrutamiento de archivos se crea con la variable **[!UICONTROL Activo]** estado. Ahora está listo para utilizarse en un [superficie de correo postal](#direct-mail-surface).

   >[!NOTE]
   >
   >También puede seleccionar **[!UICONTROL Guardar como borrador]** para crear la configuración de enrutamiento del archivo, pero no podrá seleccionarla en una superficie hasta que **[!UICONTROL Activo]**.

## Crear una superficie de correo postal {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="Definir la configuración de correo postal"
>abstract="Una superficie de correo postal contiene la configuración para el formato del archivo que contiene los datos de audiencia de destino y que utilizará el proveedor de correo. También debe definir dónde se exportará el archivo seleccionando la configuración de enrutamiento del archivo."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/direct-mail-configuration.html#file-routing-configuration" text="Configuración del enrutamiento de archivos"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="Definir el umbral de división del archivo"
>abstract="Debe establecer el número máximo de registros para cada archivo que contenga datos de audiencia. Puede seleccionar cualquier número entre 1 y 200 000 registros. Una vez alcanzado el umbral especificado, se creará otro archivo para los registros restantes."

Para poder enviar correo postal con [!DNL Journey Optimizer], debe crear una superficie de canal para definir la configuración del formato del archivo que utilizará el proveedor de correo.

Una superficie de correo postal también debe incluir la configuración de enrutamiento de archivos que define el servidor donde se exportará el archivo de correo postal.

1. Cree una superficie de canal. [Más información](channel-surfaces.md)

1. Seleccione el **[!UICONTROL Correo postal]** canal.

   ![](assets/surface-direct-mail-channel.png)

1. Defina la configuración de correo postal en la sección dedicada de la configuración de la superficie del canal.

   ![](assets/surface-direct-mail-settings.png)

1. Seleccione el formato de archivo: **[!UICONTROL CSV]** o **[!UICONTROL Texto delimitado]**.

1. En el **[!UICONTROL Inserción]** , puede elegir quitar automáticamente las filas duplicadas.

1. Defina el número máximo de registros (es decir, filas) para cada archivo que contenga datos de perfil. Una vez alcanzado el umbral especificado, se creará otro archivo para los registros restantes.

   ![](assets/surface-direct-mail-split.png)

   Por ejemplo, si hay 100 000 registros en el archivo y el límite de umbral se establece en 60 000, los registros se dividirán en dos archivos. El primer archivo contendrá 60 000 filas y el segundo archivo contendrá las 40 000 filas restantes.

   >[!NOTE]
   >
   >Puede establecer cualquier número entre 1 y 200 000 registros, lo que significa que cada archivo debe contener al menos 1 fila y no más de 200 000 filas.

1. Finalmente, seleccione la **[!UICONTROL Configuración de enrutamiento de archivos]** entre los que ha creado. Esto define dónde se exportará el archivo para que lo utilice su proveedor de correo postal.

   >[!CAUTION]
   >
   >Si no ha configurado ninguna opción de enrutamiento de archivos, no podrá crear una superficie de correo postal. [Más información](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png)

1. Envíe la superficie de correo postal.

Ahora puede [crear un mensaje de correo postal](../messages/create-direct-mail.md) dentro de una campaña. Una vez iniciada la campaña, el archivo que contiene los datos de audiencia de destino se exportará automáticamente al servidor que haya definido. El proveedor de correo postal podrá recuperar ese archivo y continuar con la entrega de correo postal.