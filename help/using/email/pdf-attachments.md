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
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 4%

---

# Adjuntar un archivo PDF a un correo electrónico {#pdf-attachments}

>[!CONTEXTUALHELP]
>id="ajo_pdf_attachments"
>title="Añadir un archivo adjunto de PDF"
>abstract="Busque y seleccione un archivo de PDF para adjuntarlo al correo electrónico.</br>Puede enviar hasta 6 mensajes por perfil con un archivo adjunto de PDF al año. El tamaño máximo de archivo permitido para cada archivo adjunto es 5 MB.</br>Para cualquier tamaño o volumen adicional, puede adquirir un complemento de paquete de archivos adjuntos. Para obtener más información, póngase en contacto con su representante de Adobe."

>[!AVAILABILITY]
>
>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

Puede adjuntar un archivo PDF estático a los mensajes de correo electrónico que envíe con [!DNL Journey Optimizer].

>[!IMPORTANT]
>
>* Puede enviar hasta 6 mensajes con un archivo adjunto de PDF por perfil y año.
>
>* El tamaño máximo de archivo permitido para cada archivo adjunto es 5 MB.
>
>Para cualquier tamaño o volumen adicional, puede adquirir un complemento de paquete de archivos adjuntos. Para obtener más información, póngase en contacto con su representante de Adobe.

Para adjuntar un archivo PDF a un mensaje de correo electrónico, siga los pasos a continuación.

1. Cree un correo electrónico en un recorrido o una campaña. [Más información](create-email.md)

1. En la ficha recorrido o campaña **[!UICONTROL Contenido]**, seleccione **[!UICONTROL Agregar recurso]** de la sección **[!UICONTROL Datos adjuntos]**.

   ![](assets/email-select-pdf.png)

1. Se muestra el repositorio de Assets Essentials.

   >[!NOTE]
   >
   >Al diseñar mensajes, puede acceder al repositorio de Assets Essentials directamente desde la interfaz de Journey Optimizer. Para obtener más información sobre la interfaz de usuario [!DNL Assets Essentials] incrustada, consulte [Documentación de Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=es){target="_blank"}.

1. Use el filtro **[!UICONTROL PDF]** en la sección **[!UICONTROL Tipo MIME]** para restringir la selección al formato de archivo correcto.

   ![](assets/email-assets-pdf.png)

   >[!NOTE]
   >
   >Solo se permite el formato PDF para los archivos adjuntos.

1. Seleccione el archivo que desee.

   * Solo puede seleccionar un archivo a la vez.
   * El tamaño máximo de archivo permitido para cada archivo adjunto es 5 MB.

1. Una vez finalizado, el nombre y el tamaño del archivo seleccionado se mostrarán en la sección **[!UICONTROL Datos adjuntos]**.

   Puede quitar el archivo seleccionado mediante el icono de Más acciones situado junto al nombre del archivo.

   ![](assets/email-remove-attachment.png)

>[!NOTE]
>
>Cuando guarda el mensaje como [plantilla de contenido](../content-management/create-content-templates.md), los datos adjuntos de PDF no se conservan con la plantilla. Si crea un nuevo correo electrónico a partir de la plantilla de contenido guardada, debe volver a adjuntar el archivo.
