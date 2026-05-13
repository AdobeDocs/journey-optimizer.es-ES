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
TQID: https://experienceleague.adobe.com/R0Csd9gbvY-iyW81G-clHoXozEBYWBfjb0y9PWq4zZA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 30%

---

# Importar el contenido del correo electrónico {#existing-content}

[!DNL Journey Optimizer] le permite importar contenido existente de HTML para diseñar sus correos electrónicos. Este contenido puede ser el siguiente:

* Un **archivo HTML** con una hoja de estilos incorporada;
* Una carpeta **.zip** que incluye un archivo HTML, la hoja de estilo (.css) y las imágenes.

  >[!NOTE]
  >
  >No hay restricciones en la estructura de archivos .zip. Sin embargo, las referencias deben ser relativas y ajustarse a la estructura de árbol de la carpeta .zip.


>[!TIP]
>
>Si tienes diseños de imagen (JPEG o PNG) en lugar de archivos HTML, puedes usar el conversor de [imagen a HTML](../content-management/image-to-html.md) para convertirlos automáticamente en plantillas editables de correo electrónico de HTML usando IA.

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

## Vídeo tutorial {#video}

Obtenga información sobre cómo importar contenido HTML existente, modificar el diseño, añadir páginas espejo y cancelar la suscripción de vínculos, y cómo codificar el contenido.

>[!VIDEO](https://video.tv.adobe.com/v/334102?quality=12)
