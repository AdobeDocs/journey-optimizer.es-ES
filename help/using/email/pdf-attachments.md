---
solution: Journey Optimizer
product: journey optimizer
title: Adjuntar un archivo PDF a un correo electrónico
description: Obtenga información sobre cómo adjuntar archivos PDF estáticos o personalizados a un correo electrónico
feature: Email Design
topic: Content Management
role: User
level: Beginner
keywords: correo electrónico, mensaje, adjunto, pdf, editor, personalizado, activado por API
exl-id: 71e218d0-5b3b-4db5-8b7b-d08df8f088c4
TQID: https://experienceleague.adobe.com/9IgYERskcUrIAhTb3xlNgWTRyY-04O58ZB8I0lYFh4g
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
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: c1270581f5184ca1f5375a2838dfb2906805a259
workflow-type: tm+mt
source-wordcount: 916
ht-degree: 7%

---

# Adjuntar un archivo PDF a un correo electrónico {#pdf-attachments}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a adjuntar archivos PDF estáticos o personalizados a los correos electrónicos, incluidos los tipos de campañas compatibles y los límites de recuento, tamaño y volumen aplicables.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_pdf_attachments"
>title="Añadir un archivo adjunto de PDF"
>abstract="Busque y seleccione un archivo de PDF para adjuntarlo al correo electrónico.</br>Puede enviar hasta 6 mensajes por perfil con un archivo adjunto de PDF al año. El tamaño máximo de archivo permitido para cada archivo adjunto es 5 MB.</br>Para cualquier tamaño o volumen adicional, puede adquirir el complemento Archivos adjuntos de PDF. Para obtener más información, póngase en contacto con su representante de Adobe."

Puede adjuntar un archivo PDF estático a los mensajes de correo electrónico que envíe con [!DNL Journey Optimizer]. Si usa [campañas activadas por API](../campaigns/api-triggered-campaigns.md), también puede adjuntar un [archivo PDF personalizado para cada destinatario](#personalized-attachments).

Tenga en cuenta que los archivos adjuntos personalizados de PDF requieren una recuperación y un procesamiento de archivos adicionales. Las campañas que los utilizan pueden tener una latencia de procesamiento mayor y un rendimiento menor que las campañas sin archivos adjuntos, especialmente cuando se utilizan varios archivos PDF o de mayor tamaño.

>[!IMPORTANT]
>
>* Puede enviar hasta 6 mensajes con un archivo adjunto de PDF por perfil y año, ya sea estático o personalizado.
>
>* El tamaño máximo para cada archivo adjunto es 5 MB. En el caso de los mensajes de correo electrónico con [archivos adjuntos personalizados](#personalized-attachments), todos los archivos adjuntos estáticos y personalizados de PDF del correo electrónico comparten un límite combinado de 5 MB de forma predeterminada.
>
> Para cualquier tamaño o volumen adicional, puede adquirir el complemento Archivos adjuntos de PDF, que eleva el límite combinado de archivos adjuntos personalizados a 10 MB. Para obtener más información, póngase en contacto con su representante de Adobe.

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

## Adjunte archivos personalizados de PDF para campañas activadas por API {#personalized-attachments}

También puede adjuntar archivos PDF específicos del destinatario a un único correo electrónico enviado a través de una [campaña activada por API](../campaigns/api-triggered-campaigns.md). A diferencia de los archivos adjuntos estáticos, cada destinatario puede recibir un archivo diferente, como una factura, una tarjeta de embarque, un contrato o una etiqueta de envío.

El tamaño combinado de todos los archivos adjuntos estáticos y personalizados de PDF de un correo electrónico está limitado a 5 MB de forma predeterminada. Las organizaciones con el complemento de archivos adjuntos de PDF aplicable pueden utilizar un límite combinado de hasta 10 MB.

>[!IMPORTANT]
>
>* Los archivos adjuntos personalizados de PDF solo son compatibles con las campañas de correo electrónico transaccionales activadas por API.
>
>* Puede incluir hasta cinco archivos adjuntos de PDF en un correo electrónico. Este límite incluye archivos adjuntos estáticos y personalizados. Por ejemplo, un correo electrónico que contenga un PDF estático puede incluir hasta cuatro PDF personalizados. Si necesita enviar más, divídalos en varias comunicaciones.
>
>* Los archivos adjuntos personalizados y estáticos de PDF se contabilizan en la misma cuota. [Más información](#pdf-attachments)

Los archivos adjuntos personalizados de PDF deben cargarse en el contenedor de [zona de aterrizaje de datos](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/cloud-storage/data-landing-zone){target="_blank"} específico para los datos adjuntos y, a continuación, se hará referencia a él en la carga útil de la API. Actualmente, la zona de aterrizaje de datos es la única ubicación de almacenamiento compatible para archivos adjuntos personalizados de PDF.

1. Recupere las credenciales de la zona de aterrizaje de datos de su zona protegida utilizando `type=ajoemailattachments` para la misma organización de IMS y zona protegida que la solicitud de ejecución, tal como se describe en la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/cloud-storage/data-landing-zone){target="_blank"}. Según el proveedor de la nube, utilice el contenedor de Azure o el bloque de AWS y la carpeta devueltos por la API.

1. Genere los archivos PDF con la herramienta que elija y cárguelos en su contenedor de zona de aterrizaje de datos.

   Tenga en cuenta que la zona de aterrizaje de datos elimina automáticamente los archivos pasados siete días. Asegúrese de que los archivos de PDF permanezcan disponibles en el contenedor hasta que se complete la entrega del mensaje y los reintentos.

1. En la carga útil de la API, para cada destinatario, agregue una matriz `attachments` que contenga el nombre de archivo, el tipo de contenido y la ruta de la zona de aterrizaje de datos de PDF que se va a enviar. [Aprenda a personalizar el contenido de su campaña activada por API](../campaigns/api-triggered-campaign-content.md#contextual)

   ```json
   "attachments": [
     {
       "name": "invoice-12345.pdf",
       "contentType": "application/pdf",
       "source": {
         "type": "dlzPath",
         "path": "attachments/invoice-12345.pdf"
       }
     }
   ]
   ```

   Tenga en cuenta que `source.path` es la ruta de acceso del objeto relativa al contenedor de zona de aterrizaje de datos específico del archivo adjunto recuperado con `type=ajoemailattachments`. No incluya el nombre del contenedor de Azure, el bloque o la carpeta de AWS, las credenciales o una URL de almacenamiento completa.

En el momento del envío, [!DNL Journey Optimizer] recupera el archivo de la ubicación especificada y lo adjunta al mensaje para ese destinatario. Los archivos adjuntos personalizados de PDF son compatibles con [Alto rendimiento](../campaigns/api-triggered-high-throughput.md) campañas en la región principal. No son compatibles durante la conmutación por error regional.

Para obtener la referencia de carga útil de API completa, consulte la [documentación de API de ejecución de mensajes interactivos](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution){target="_blank"}.
