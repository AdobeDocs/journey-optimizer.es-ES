---
solution: Journey Optimizer
product: journey optimizer
title: Adjuntar un archivo PDF a un correo electrónico
description: Obtenga información sobre cómo adjuntar archivos PDF estáticos a un correo electrónico
feature: Email Design
topic: Content Management
role: User
level: Beginner
keywords: correo electrónico, mensaje, adjunto, pdf, editor
exl-id: 71e218d0-5b3b-4db5-8b7b-d08df8f088c4
TQID: https://experienceleague.adobe.com/9IgYERskcUrIAhTb3xlNgWTRyY-04O58ZB8I0lYFh4g
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 351
ht-degree: 38%

---

# Adjuntar un archivo PDF a un correo electrónico {#pdf-attachments}

>[!CONTEXTUALHELP]
>id="ajo_pdf_attachments"
>title="Añadir PDF adjunto"
>abstract="Busque y seleccione un archivo de PDF para adjuntarlo al correo electrónico.</br>Puede enviar hasta seis mensajes con un archivo adjunto de PDF por perfil y año. El tamaño máximo permitido para cada archivo adjunto es de 5 MB.</br>Para cualquier tamaño o volumen adicional, puede adquirir un complemento de paquete de archivos adjuntos. Para obtener más información, póngase en contacto con su representante de Adobe."

Puede adjuntar un archivo PDF estático a los mensajes de correo electrónico que envíe con [!DNL Journey Optimizer].

>[!IMPORTANT]
>
>* Puede enviar hasta 6 mensajes con un archivo adjunto de PDF por perfil y año.
>
>* El tamaño máximo para cada archivo adjunto es 5 MB.
>
>Para cualquier tamaño o volumen adicional, puede comprar un complemento de archivos PDF adjuntos. Para obtener más información, póngase en contacto con su representante de Adobe.

Para adjuntar un archivo PDF a un mensaje de correo electrónico, siga los pasos a continuación.

1. Cree un correo electrónico en un recorrido o una campaña. [Más información](create-email.md)

1. En la ficha recorrido o campaña **[!UICONTROL Contenido]**, seleccione **[!UICONTROL Agregar recurso]** de la sección **[!UICONTROL Datos adjuntos]**.

   ![](assets/email-select-pdf.png)

1. Se muestra el repositorio de Assets Essentials.

   >[!NOTE]
   >
   >Al diseñar mensajes, puede acceder al repositorio de Assets Essentials directamente desde la interfaz de Journey Optimizer. Para obtener más información sobre la interfaz de usuario [!DNL Assets Essentials] incrustada, consulte [Documentación de Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}.

1. Use el filtro **[!UICONTROL PDF]** en la sección **[!UICONTROL Tipo MIME]** para restringir la selección al formato de archivo correcto.

   ![](assets/email-assets-pdf.png)

   >[!NOTE]
   >
   >Solo se permite el formato PDF para los archivos adjuntos.

1. Seleccione el archivo que desee.

   * Solo puede seleccionar un archivo a la vez.
   * El tamaño máximo para cada archivo adjunto es 5 MB.

1. Una vez finalizado, el nombre y el tamaño del archivo seleccionado se mostrarán en la sección **[!UICONTROL Datos adjuntos]**.

   Puede quitar el archivo seleccionado mediante el icono de Más acciones situado junto al nombre del archivo.

   ![](assets/email-remove-attachment.png)

>[!NOTE]
>
>Cuando guarda el mensaje como [plantilla de contenido](../content-management/create-content-templates.md), los datos adjuntos de PDF no se conservan con la plantilla. Si crea un nuevo correo electrónico a partir de la plantilla de contenido guardada, debe volver a adjuntar el archivo.
