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
source-git-commit: cd8ce89dd6ed9c60d41e9f83ccfb080bdb4a19f9
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 33%

---

# Importar el contenido del correo electrónico {#existing-content}

[!DNL Journey Optimizer] permite importar contenido existente del HTML para diseñar los correos electrónicos. Este contenido puede ser el siguiente:

* Un **archivo de HTML** con una hoja de estilo incorporada;
* A **carpeta .zip** incluyendo un archivo de HTML, la hoja de estilo (.css) y las imágenes.

  >[!NOTE]
  >
  >No hay restricciones en la estructura de archivos .zip. Sin embargo, las referencias deben ser relativas y ajustarse a la estructura de árbol de la carpeta .zip.

Para importar un archivo con contenido HTML, siga los pasos a continuación:

1. En la página de inicio del Diseñador de correo electrónico, seleccione **[!UICONTROL Importar HTML]**.

   ![](assets/import-html_2.png)

1. Arrastre y suelte el archivo HTML o .zip que contiene el contenido HTML y haga clic en **[!UICONTROL Importar]**.

   ![](assets/html-imported_2.png)

1. Una vez cargado el contenido del HTML, el contenido se encuentra en **[!UICONTROL Modo de compatibilidad]**.

   En este modo, solo puede personalizar el texto, agregar vínculos o incluir recursos en el contenido.

1. Para poder aprovechar los componentes de contenido del Diseñador de correo electrónico, acceda al **[!UICONTROL convertidor HTML]** y haga clic en **[!UICONTROL Convertir]**.

   ![](assets/html-imported.png)

   >[!NOTE]
   >
   > Uso de un `<table>` como la primera capa de un archivo de HTML puede causar pérdida de estilo, incluida la configuración de fondo y anchura en la etiqueta de capa superior.

1. Ahora puede personalizar el archivo importado según sea necesario con las funcionalidades del Diseñador de correo electrónico [Más información](content-from-scratch.md).

## Vídeo explicativo {#video}

Obtenga información sobre cómo importar contenido HTML existente, modificar el diseño, añadir páginas espejo y cancelar la suscripción de vínculos, y cómo codificar el contenido.

>[!VIDEO](https://video.tv.adobe.com/v/334102?quality=12)
