---
title: Envío de mensajes de correo directo con recorridos
description: Obtenga información sobre cómo crear y enviar mensajes de correo postal con recorridos.
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
badge: label="Disponibilidad limitada" type="Informative"
hidefromtoc: true
hide: true
robots: noindex
googlebot: noindex
keywords: correo directo, mensaje, campaña
exl-id: 44886355-ee3a-4323-899a-35d967487924
source-git-commit: 755ffdb0a9986ce8c2175a9bc61ed4a56714ff7d
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 19%

---

# Envío de mensajes de correo directo con recorridos {#direct-mail-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_direct_mail"
>title="Actividad Finalizar"
>abstract="El correo directo es un canal sin conexión que le permite personalizar y generar los archivos de extracción necesarios para que los proveedores de correo postal de terceros envíen correo a sus clientes."

>[!AVAILABILITY]
>
>Esta capacidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada).

El correo directo es un canal sin conexión que le permite personalizar y generar los archivos de extracción necesarios para que los proveedores de correo postal de terceros envíen correo a sus clientes.

Al crear un mensaje de correo postal, [!DNL Journey Optimizer] genera automáticamente un archivo que contiene todos los perfiles de destino y los datos seleccionados, como direcciones postales y atributos de perfil. Este archivo se envía al servidor de su elección para que el proveedor de correo postal de terceros elegido pueda acceder a él, quien se encargará del proceso de envío.

Debe trabajar con el proveedor de correo postal de terceros que haya elegido para obtener de sus clientes los consentimientos necesarios, si corresponde, para que sus clientes puedan recibir correo de usted. El uso de los servicios de correo está sujeto a términos y condiciones adicionales del proveedor de correo postal de terceros correspondiente. Adobe no controla ni es responsable del uso que se haga de los productos de terceros. Para cualquier problema o solicitud de asistencia relacionada con el envío de su mensaje de correo postal, póngase en contacto con su proveedor de correo postal elegido.

>[!NOTE]
>
>Esta página detalla el proceso para crear y enviar mensajes de correo postal con recorridos. Para obtener más información sobre el canal de correo postal y cómo crear campañas de correo postal, consulte esta sección: [Introducción al correo postal](../direct-mail/get-started-direct-mail.md).

## Crear una configuración de enrutamiento de archivos

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_frequency"
>title="Elegir la región de AWS"
>abstract="Si la configuración de enrutamiento de archivos se va a enviar mediante recorridos, puede especificar la frecuencia con la que se enviará el archivo al servidor."

Antes de crear un mensaje de correo postal, asegúrese de haber configurado una configuración de enrutamiento de archivos que especifique el servidor donde se debe cargar y almacenar el archivo de extracción. Para ello, siga estos pasos:

1. Acceda al menú **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo directo]** > **[!UICONTROL Enrutamiento de archivos]** y, a continuación, haga clic en **[!UICONTROL Crear configuración de enrutamiento de archivos]**.

1. Defina las propiedades de configuración de enrutamiento de archivos, como su nombre y el tipo de servidor que desea utilizar. Encontrará información detallada sobre cómo configurar una configuración de enrutamiento de archivos en la sección [Configuración de correo directo](../direct-mail/direct-mail-configuration.md#file-routing-configuration).

   Si la configuración de enrutamiento de archivos se va a enviar mediante recorridos, puede especificar la frecuencia con la que se enviará el archivo al servidor.

   ![](assets/file-routing-journey.png)

1. Haga clic en **[!UICONTROL Enviar]** para confirmar la creación de la configuración de enrutamiento de archivos. La configuración se creó con el estado **[!UICONTROL Activo]**. Ahora está listo para que se le haga referencia en una configuración de correo postal.

## Crear una configuración de correo directo {#direct-mail-surface}

Una configuración de correo directo dispone de la configuración para el formato del archivo que contiene los datos de la audiencia de destino y que utilizará el proveedor de correo. También debe definir dónde se exportará el archivo seleccionando la configuración de enrutamiento de archivos. Encontrará información detallada sobre cómo crear una configuración de correo postal en la sección [Configuración de correo postal](../direct-mail/direct-mail-configuration.md#file-routing-configuration).

Una vez que la configuración del correo postal esté lista, puede agregar una acción de correo postal al recorrido.

## Añada una acción Direct mail a su recorrido

Para añadir una acción de correo postal en un recorrido, siga estos pasos:

1. Abra el recorrido y arrastre y suelte una actividad **[!UICONTROL Correo postal]** desde la sección **Acciones** de la paleta.

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la configuración de mensaje que desea utilizar. El campo **[!UICONTROL configuration]** está rellenado previamente de forma predeterminada con la última configuración que el usuario usó para ese canal. Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md).

1. Configure el archivo de extracción para enviarlo a su proveedor de correo postal. Para ello, haga clic en el botón **[!UICONTROL Editar contenido]**.

   ![](assets/direct-mail-add-journey.png)

1. Ajuste las propiedades del archivo de extracción, como el nombre del archivo o las columnas que desea mostrar. Para obtener más información sobre cómo configurar las propiedades del archivo de extracción, consulte esta sección: [Crear un mensaje de correo postal](../direct-mail/create-direct-mail.md#extraction-file).

   ![](assets/direct-mail-journey-content.png)

1. Una vez definido el contenido del archivo de extracción, puede utilizar perfiles de prueba para previsualizarlo. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este en el mensaje con los datos del perfil de prueba.

   Para ello, haga clic en **[!UICONTROL Simular contenido]** y añada un perfil de prueba para comprobar cómo se representa el archivo de extracción con los datos del perfil de prueba. Encontrará información detallada sobre cómo seleccionar perfiles de prueba y obtener una vista previa del contenido en la sección [Administración de contenido](../content-management/preview-test.md).

   ![](assets/direct-mail-simulate.png){width="800" align="center"}

Cuando el archivo de extracción esté listo, complete la configuración de su [recorrido](../building-journeys/journey-gs.md) para enviarlo.
