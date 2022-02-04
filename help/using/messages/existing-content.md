---
title: Importar o codificar correos electrónicos
description: Obtenga información sobre cómo importar contenido de correo electrónico o codificar sus correos electrónicos
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 52011299-0c65-49c3-9edd-ba7bed5d7205
source-git-commit: b43e3432ede1d4985e0a6b57b57c5efc3cf60c50
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 9%

---

# Importación o codificación del contenido del correo electrónico {#existing-content}

Journey Optimizer le permite importar contenido de HTML existente para diseñar sus correos electrónicos. Este contenido puede ser código HTML sin procesar o contenido de un archivo HTML existente o una carpeta zip.

Para codificar el contenido del HTML o importar contenido existente, siga los pasos a continuación:

1. [Creación de un mensaje ](create-message.md)

1. Abra el **[!UICONTROL Email Designer]** de la variable **[!UICONTROL Edit Content]** para obtener más información.

   ![](assets/import-html_1.png)

1. Seleccione **[!UICONTROL Code your own]** o **[!UICONTROL Import HTML]**. Consulte las secciones a continuación para ver los pasos siguientes.

## Codifique sus propios {#import-raw-html-code}

Utilice la variable **[!UICONTROL Code your own]** para poder importar el HTML sin procesar o codificar el contenido del correo electrónico. Este método requiere habilidades HTML.

>[!CAUTION]
>
> Imágenes de [Adobe Experience Manager Assets Essentials](assets-essentials.md) no se puede hacer referencia a al utilizar este método. Las imágenes a las que se hace referencia en el código del HTML deben almacenarse en una ubicación pública.

1. En la página de inicio del Diseñador de correo electrónico, seleccione **[!UICONTROL Code your own]**.

   ![](assets/code-your-own.png)

1. Introduzca o pegue el código de HTML sin procesar.

1. Utilice el panel izquierdo para aprovechar [!DNL Journey Optimizer] funcionalidades de personalización. Para obtener más información, consulte [esta sección](../personalization/personalize.md).

   ![](assets/code-editor.png)

1. Si desea abrir el Diseñador de correo electrónico para iniciar el correo electrónico desde un nuevo diseño, seleccione **[!UICONTROL Change your design]** en el menú de opciones.

   ![](assets/code-editor-change-design.png)

1. Haga clic en el **[!UICONTROL Preview]** para comprobar el diseño y la personalización de los mensajes mediante perfiles de prueba. Para obtener más información, consulte [esta sección](preview.md).

   ![](assets/code-editor-preview.png)

1. Una vez que el código esté listo, haga clic en **[!UICONTROL Save]** a continuación, vuelva a la pantalla de creación de mensajes para finalizar el mensaje.

   ![](assets/code-editor-save.png)

## Importar HTML {#import-html-content-from-file}

Puede importar contenido de HTML en el diseñador de correo electrónico. Este contenido puede ser:

* Un **archivo HTML** con una hoja de estilo incorporada,
* A **Carpeta .zip** con el archivo HTML, la hoja de estilo (.css) y las imágenes.

   >[!NOTE]
   >
   >No hay restricciones en la estructura de archivos .zip. Sin embargo, las referencias deben ser relativas y ajustarse a la estructura de árbol de la carpeta .zip.

Para importar un archivo con contenido de HTML, siga los pasos a continuación:

1. En la página de inicio del Diseñador de correo electrónico, seleccione **[!UICONTROL Import HTML]**.

   ![](assets/import-html_2.png)

1. Arrastre y suelte el HTML o el archivo .zip que contiene el contenido del HTML.

1. Una vez cargado el contenido del HTML, puede aprovechar las funcionalidades del Diseñador de correo electrónico para editar y previsualizar el correo electrónico. [Obtenga más información en esta sección](create-email-content.md).

   ![](assets/html-imported.png)
