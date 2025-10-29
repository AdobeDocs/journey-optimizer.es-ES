---
solution: Journey Optimizer
product: journey optimizer
title: Importar el contenido del correo electrónico
description: Obtenga información sobre cómo importar contenido de correo electrónico
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: correo electrónico, importación, contenido, html, zip, css
exl-id: 52011299-0c65-49c3-9edd-ba7bed5d7205
source-git-commit: ddbab603e4ac612a49a3853fcac428950def1d98
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 34%

---

# Importar el contenido del correo electrónico {#existing-content}

[!DNL Journey Optimizer] le permite importar contenido existente de HTML para diseñar sus correos electrónicos. Este contenido puede ser el siguiente:

* Un **archivo HTML** con una hoja de estilos incorporada;
* Una carpeta **.zip** que incluye un archivo HTML, la hoja de estilo (.css) y las imágenes.

  >[!NOTE]
  >
  >No hay restricciones en la estructura de archivos .zip. Sin embargo, las referencias deben ser relativas y ajustarse a la estructura de árbol de la carpeta .zip.

<!--DOCAC-13676
>[!TIP]
>
>If you have image designs (JPEG or PNG) instead of HTML files, you can use the [Template Accelerator](image-to-html.md) to automatically convert them into editable HTML email templates using AI.-->

Para importar un archivo con contenido HTML, siga los pasos a continuación:

1. En la página de inicio de Email Designer, seleccione **[!UICONTROL Importar HTML]**.

   ![](assets/import-html_2.png)

1. Arrastre y suelte el archivo HTML o .zip que contiene el contenido HTML y haga clic en **[!UICONTROL Importar]**.

   ![](assets/html-imported_2.png)

1. Una vez cargado el contenido de HTML, el contenido estará en **[!UICONTROL modo de compatibilidad]**.

   En este modo, solo puede personalizar el texto, agregar vínculos o incluir recursos en el contenido.

1. Para poder aprovechar los componentes de contenido de Email Designer, accede a la pestaña **[!UICONTROL HTML converter]** y haz clic en **[!UICONTROL Convert]**.

   ![](assets/html-imported.png)

   >[!NOTE]
   >
   > El uso de una etiqueta `<table>` como primera capa de un archivo HTML puede causar la pérdida de estilo, incluida la configuración del fondo y el ancho en la etiqueta de la capa superior.

1. Ahora puede personalizar el archivo importado según sea necesario con las funcionalidades de Designer de correo electrónico. [Más información](content-from-scratch.md)

## Vídeo explicativo {#video}

Obtenga información sobre cómo importar contenido HTML existente, modificar el diseño, añadir páginas espejo y cancelar la suscripción de vínculos, y cómo codificar el contenido.

>[!VIDEO](https://video.tv.adobe.com/v/334102?quality=12)
