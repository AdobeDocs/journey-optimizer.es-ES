---
title: Configuración de correo directo
description: Obtenga información sobre cómo configurar correo directo canal en Journey Optimizer
feature: Direct Mail, Surface
topic: Content Management
role: User
level: Experienced
keyword: direct, mail, configuration, direct-mail, provider
exl-id: ae5cc885-ade1-4683-b97e-eda1f2142041
source-git-commit: 65b7b8323e37a0143a3941af1b9c2fb8b595a376
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 22%

---

# Configuración de correo directo {#direct-mail-configuration}

[!DNL Journey Optimizer] Le permite personalizar y generar los archivos requeridos por los proveedores de correo directo para enviar correo a sus clientes.

Al [crear un mensaje de correo postal](../direct-mail/create-direct-mail.md), usted define los datos de la audiencia de destino, incluida la información de contacto elegida (por ejemplo, la dirección postal). A continuación, se genera y exporta automáticamente un archivo que contiene estos datos a un servidor, donde su proveedor de correo postal podrá recuperarlo y encargarse del envío real.

Antes de poder generar este archivo, debe crear lo siguiente:

1. [Una configuración de enrutamiento de archivos](#file-routing-configuration) para especificar el servidor donde se exportará el archivo y cifrar el archivo, si es necesario.

1. [Una configuración de correo postal](#direct-mail-configuration) que hace referencia a la configuración de enrutamiento de archivos. Si no ha configurado ninguna opción de enrutamiento de archivos, no podrá crear una configuración de correo postal.


>[!CAUTION]
>
>* Para crear una configuración de enrutamiento de archivos, necesita tener el permiso integrado **[!DNL Manage file routing]**. [Más información](../administration/ootb-product-profiles.md#content-library-manager)
>
>* Los archivos de correo postal solo se generan en el momento de la exportación; el sistema no almacena indefinidamente las exportaciones más antiguas. Para copias de seguridad más largas o permanentes, configure una opción de enrutamiento de archivos (SFTP o almacenamiento en la nube).

## Configurar el enrutamiento de archivos {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Definir la configuración de enrutamiento de archivos"
>abstract="Después de crear un mensaje de correo directo, el archivo que contiene los datos de audiencia de destino se genera y exporta a un servidor. Debe especificar los detalles del servidor para que su proveedor de correo directo pueda acceder y utilizar ese archivo para enviar correo directo."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/channels/direct-mail/create-direct-mail" text="Crear un mensaje de correo directo"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="Definir la configuración de enrutamiento de archivos"
>abstract="Debe definir dónde se exportará el archivo para que lo utilice su proveedor de correo directo."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="Configuración de enrutamiento de archivos"
>abstract="Seleccione la configuración de enrutamiento de archivos que desee, que define dónde se exportará el archivo para que lo utilice su proveedor de correo directo."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="Seleccionar el tipo de servidor para el archivo"
>abstract="Elija el tipo de servidor que desea utilizar para exportar los archivos de correo directo: Amazon S3, SFTP, Azure o Data Landing Zone."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="Elegir la región de AWS"
>abstract="Seleccione la región geográfica del servidor de AWS donde desea exportar los archivos de correo directo. Como práctica general, se prefiere elegir la región más cercana a la ubicación del proveedor de correo directo."

>[!NOTE]
>
>Actualmente, Amazon S3, SFTP, Azure y Data Landing Zone son compatibles con [!DNL Journey Optimizer].

Para enviar un mensaje de correo postal, [!DNL Journey Optimizer] genera y exporta el archivo que contiene los datos de la audiencia de destino a un servidor.

Debe especificar los detalles del servidor para que su proveedor de correo postal pueda acceder a ese archivo y utilizarlo para enviar correo.

Para configurar el enrutamiento de archivos, siga los pasos a continuación.

1. Acceda al menú **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo directo]** > **[!UICONTROL Enrutamiento de archivos]** y, a continuación, haga clic en **[!UICONTROL Crear configuración de enrutamiento de archivos]**.

   ![](assets/file-routing-config-button.png){width="800" align="center"}

1. Establezca un nombre para la configuración.

1. Seleccione el tipo de servidor que desea utilizar para exportar los archivos de correo postal: Amazon S3, SFTP, Azure o Data Landing Zone.

   ![](assets/file-routing-config-type.png){width="800" align="center"}

1. Rellene los campos específicos de cada tipo de servidor como se detalla en las pestañas siguientes.

>[!BEGINTABS]

>[!TAB Amazon S3]

Si seleccionó **[!UICONTROL Amazon S3]** como **[!UICONTROL tipo de servidor]**, rellene los detalles y las credenciales de su servidor:

* **Nombre del contenedor de AWS**:Para saber dónde encontrar el nombre del contenedor de AWS, consulte [esta página](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingBucket.html).

* **Clave** de acceso de AWS: para saber dónde encontrar su ID de clave de acceso de AWS, consulte [este Página](https://docs.aws.amazon.com/IAM/latest/UserGuide/security-creds.html#access-keys-and-secret-access-keys).

* **Clave** secreta de AWS: para saber dónde encontrar su clave secreta de AWS, consulte [este Página](https://aws.amazon.com/fr/blogs/security/wheres-my-secret-access-key/).

* **AWS área geográfica**: elija la área geográfica **de** AWS donde se ubicará la infraestructura del servidor. Las regiones de AWS son áreas geográficas que AWS utiliza para host sus infraestructuras nube. Como práctica general, se prefiere elegir la área geográfica que esté más cerca de usted correo directo ubicación del proveedor.

![](assets/file-routing-config-aws-region.png){width="800" align="center"}

>[!TAB SFTP]

Si seleccionó **[!UICONTROL SFTP]** como **[!UICONTROL tipo de servidor]**, indique los detalles y las credenciales de su servidor:

* **Cuenta**: Nombre de cuenta utilizado para conectarse al servidor SFTP.

* **Dirección del servidor**: &#x200B;URL del servidor SFTP.

* **Puerto**: número de puerto de conexión FTP.

* **Contraseña**:&#x200B; Contraseña utilizada para conectarse al servidor SFTP.

![](assets/file-routing-config-sftp-detail.png)

>[!NOTE]
>
>Para especificar una ruta en el servidor para guardar el archivo, actualice el campo **[!UICONTROL Nombre de archivo]** de la campaña de correo postal para incluir la ruta deseada. [Más información](create-direct-mail.md#extraction-file)

>[!TAB Azure]

Si seleccionó **[!UICONTROL Azure]** como el **[!UICONTROL tipo de servidor]**, rellene los detalles y credenciales del servidor:

* **Cadena de conexión de Azure**: Para encontrar su **cadena de conexión de Azure**, consulte [esta página](https://learn.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string#configure-a-connection-string-for-an-azure-storage-account).

  La **cadena de conexión de Azure** debe seguir el formato siguiente:

  `DefaultEndpointsProtocol=[http|https];AccountName=myAccountName;AccountKey=myAccountKey`

* **Nombre de contenedor**: Para encontrar su **Nombre de contenedor**, consulte [esta página](https://learn.microsoft.com/en-us/azure/storage/blobs/blob-containers-portal).

  El **nombre** del contenedor debe contener únicamente el nombre del contenedor sin ninguna barra oblicua.

  >[!NOTE]
  >
  >Para especificar una ruta dentro del contenedor para guardar el archivo, actualice el campo Nombre de archivo del **&#x200B;**&#x200B;correo directo del campaña para incluir la ruta deseada. [Más información](create-direct-mail.md#extraction-file)

  ![](assets/file-routing-config-azure-detail.png)

>[!TAB Zona de aterrizaje de datos]

Si seleccionó **[!UICONTROL Zona de aterrizaje]** de datos como tipo de **[!UICONTROL Servidor]**, no se requieren detalles específicos.

![](assets/file-routing-config-dlz-detail.png)

A todos los clientes de [!DNL Adobe Experience Platform] se les ha aprovisionado un contenedor de zona de aterrizaje de datos por zona protegida. Obtenga más información acerca de la zona de aterrizaje de datos en la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/cloud-storage/data-landing-zone){target="_blank"}.

>[!ENDTABS]

Para cifrar el archivo, copie y pegue su clave de cifrado en el campo de clave **de** cifrado PGP/GPG.

Una vez que haya completado los detalles de su tipo de servidor, seleccione **[!UICONTROL Enviar]**. El archivo enrutamiento configuración se crea con el **[!UICONTROL estado Activo]** . Ahora está listo para utilizarse en una [configuración](#direct-mail-surface) correo directo.

También puede seleccionar **[!UICONTROL Guardar como borrador]** para crear el archivo enrutamiento configuración, pero no podrá seleccionarlo en una configuración hasta que esté **[!UICONTROL activo]**.

## Crear una configuración de correo directo {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="Definir la configuración del correo directo"
>abstract="Una configuración de correo directo dispone de la configuración para el formato del archivo que contiene los datos de la audiencia de destino y que utilizará el proveedor de correo. También debe definir dónde se exportará el archivo seleccionando la configuración de enrutamiento del archivo."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/channels/direct-mail/direct-mail-configuration#file-routing-configuration" text="Configurar el enrutamiento de archivos"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="Definir el umbral de división del archivo"
>abstract="Debe establecer el número máximo de registros para cada archivo que contenga datos de audiencia. Puede seleccionar cualquier número entre 1 y 200 000 registros. Una vez alcanzado el umbral especificado, se creará otro archivo para los registros restantes."

Para poder enviar correo postal con [!DNL Journey Optimizer], debe crear una configuración de canal para definir la configuración del formato del archivo que utilizará el proveedor de correo.

Una configuración de correo postal también debe incluir la configuración de enrutamiento de archivos que define el servidor donde se exportará el archivo de correo postal.

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** y seleccione **[!UICONTROL Configuración general]** > **[!UICONTROL Configuraciones de canal]**. Haga clic en el botón **[!UICONTROL Crear configuración de canal]**. [Más información](../configuration/channel-surfaces.md)

   ![](assets/direct-mail-config-1.png)

1. Introduzca un nombre y una descripción (opcional) para la configuración y, a continuación, seleccione la canal que desea configurar.

   >[!NOTE]
   >
   > Los nombres deben comenzar con una letra (A-Z). Sólo puede contener caracteres alfanuméricos numérica. También puede utilizar caracteres de guion bajo `_`, punto `.` y guion `-`.

1. Para asignar etiquetas de uso de datos principales o personalizadas a la configuración, puedes seleccionar **[!UICONTROL Administrar acceso]**. [Obtenga más información sobre el control de acceso a nivel de objetos (OLAC).](../administration/object-based-access.md)

1. Seleccione el canal **[!UICONTROL Correo directo]**.

   ![](assets/direct-mail-config-2.png)

1. Seleccione **[!UICONTROL Acciones]** de marketing para asociar políticas de consentimiento a los mensajes que utilizan esta configuración. Todas las políticas de consentimiento asociadas con la acción marketing se aprovechan para respetar las preferencias de sus clientes. [Más información](../action/consent.md#surface-marketing-actions)

1. Defina los ajustes de correo directo en la sección dedicada de la configuración de canal.

   ![](assets/surface-direct-mail-settings.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-settings-with-insertion.png)-->

1. Seleccione el archivo formato: **[!UICONTROL CSV]** o **[!UICONTROL delimitado por]** texto.

1. Si selecciona **[!UICONTROL Delimitado por]** texto, defina el separador de columnas de su elección: tabulación, punto y coma, barra vertical o ampersand.

   ![](assets/surface-direct-mail-column-separator.png)

1. Seleccione la **[!UICONTROL configuración de enrutamiento de archivos]** entre las que creó. Define dónde se exportará el archivo para que lo utilice su proveedor de correo postal.

   >[!CAUTION]
   >
   >Si no ha configurado ninguna opción de enrutamiento de archivos, no podrá crear una configuración de correo postal. [Más información](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-file-routing-with-insertion.png)-->

1. Envíe la configuración de correo postal.

Ahora puede [crear un mensaje de correo postal](../direct-mail/create-direct-mail.md) dentro de una campaña. Una vez iniciada la campaña, el archivo que contiene los datos de la audiencia de destino se exporta automáticamente al servidor definido. El proveedor de correo postal podrá recuperar ese archivo y continuar con la entrega de correo postal.

>[!NOTE]
>
>Las filas duplicadas en las que todos los valores de la fila son iguales se eliminan automáticamente del archivo.

<!--
    In the **[!UICONTROL Insertion]** section, you can choose to automatically remove duplicate rows.

    Define the maximum number of records (i.e. rows) for each file containing profile data. After the specified threshold is reached, another file will be created for the remaining records.

    ![](assets/surface-direct-mail-split.png)

    For example, if there are 100,000 records in the file and the threshold limit is set to 60,000, the records will be split into two files. The first file will contain 60,000 rows, and the second file will contain the remaining 40,000 rows.

    >[!NOTE]
    >
    >NOTE You can set any number between 1 and 200,000 records, meaning each file must contain at least 1 row and no more than 200,000 rows.

-->