---
solution: Journey Optimizer
product: journey optimizer
title: Exportación de mensajes en Journey Optimizer
description: Obtenga información sobre cómo exportar mensajes
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: exportación, mensajes, HIPAA, correos electrónicos, SMS, configuración
exl-id: 7b50c933-9738-4b1b-acae-08f0a8d41dab
source-git-commit: ab0f100d53cb987919eb134442bf05e64c30719a
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 3%

---

# Exportar contenido del mensaje {#message-export}

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="Conservar y exportar el contenido enviado"
>abstract="Si selecciona esta opción, puede escribir el contenido del correo electrónico o los mensajes SMS enviados mediante esta configuración en un conjunto de datos de [!DNL Experience Platform]. Los registros se conservan durante 7 días naturales a partir de la ingesta, durante los cuales puede exportarlos a su propio almacenamiento."

>[!AVAILABILITY]
>
>Esta funcionalidad solo está disponible para el canal de correo electrónico y SMS, para organizaciones que han adquirido la oferta del complemento Exportación de mensajes. Para obtener más información, contacte con su representante de Adobe.

**Message Export** le permite transferir el contenido de mensajes SMS y de correo electrónico enviados desde [!DNL Journey Optimizer] a su propio almacenamiento a través de [!DNL Adobe Experience Platform] destinos, lo que le permite enviar datos de [!DNL Experience Platform] a extremos externos. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/home){target="_blank"}

Con esta función, el contenido de los mensajes de correo electrónico y SMS enviados a través de [!DNL Journey Optimizer] que se han marcado para la exportación se escribe en el [!DNL Experience Platform] **conjunto de datos de exportación de mensajes de AJO**. [Más información sobre los conjuntos de datos](../data/get-started-datasets.md)

A continuación, los registros se conservan en el conjunto de datos durante siete días naturales a partir de la ingesta, durante los cuales puede exportarlos al sistema externo de su elección.

## Mecanismos de protección

* Esta función solo admite los canales **Correo electrónico** y **SMS**.
* Los registros del conjunto de datos de exportación de mensajes de AJO se conservan **durante siete días naturales a partir de la ingesta**.
* El relleno no es compatible con los mensajes enviados antes de habilitar la exportación de mensajes como se describe a continuación.

## Habilitar exportación de mensajes {#enable-message-export}

El proceso de incorporación de la función Exportación de mensajes consta de dos pasos:

1. [Configurar el flujo de datos de exportación](#set-up-export-dataflow) en [!DNL Experience Platform];
1. [Habilitar exportación de mensajes](#config-message-export) en la configuración de canal de [!DNL Journey Optimizer].

>[!WARNING]
>
>Solo aparecen los registros nuevos después de habilitar las exportaciones y enviar mensajes. No se admiten rellenos para el contenido antes de configurar el proceso de exportación y habilitar la opción Exportar mensaje.

### Configuración del flujo de datos de exportación {#set-up-export-dataflow}

Antes de poder exportar los datos, debe configurar el proceso de exportación definiendo el destino [!DNL Experience Platform] y el conjunto de datos que se utilizará. Siga los pasos a continuación.

>[!NOTE]
>
>Esta configuración debe configurarse para cada zona protegida.

1. Elija un Experience Platform [tipo de destino](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/destination-types){target="_blank"}. Hay disponible una lista de plataformas de destino disponibles que están listas para recibir datos en [esta página](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/catalog/overview){target="_blank"}.

1. En [!DNL Experience Platform], configure el destino definiendo credenciales, contenedor/contenedor, prefijo de ruta y opciones de seguridad. [Descubra cómo](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. Cree un flujo de exportación de conjunto de datos con los siguientes datos:

   * Conjunto de datos Source: seleccione **Conjunto de datos de exportación de mensajes AJO**.
   * Formato del archivo: seleccione JSON o Parquet (elija uno basado en las herramientas de flujo descendente).
   * Programación: asegúrese de que se ejecuta dentro del período de retención de 7 días.

### Habilitar la exportación de mensajes en la configuración de canal {#config-message-export}

Para aplicar Message Export a sus campañas y recorridos, debe habilitar la opción específica en el nivel de configuración del canal. Siga los pasos a continuación.

1. En [!DNL Journey Optimizer], edite o cree el correo electrónico o SMS [configuración de canal](channel-surfaces.md#create-channel-surface) deseado.

1. Seleccione la opción **[!UICONTROL Habilitar exportación de mensajes]**.

   ![](assets/config-message-export.png)

1. Guarde los cambios y envíe la configuración de canal.

Una vez que haya enviado mensajes a través de campañas o recorridos usando esta configuración de canal, los mensajes de correo electrónico y SMS se escriben en el **conjunto de datos de exportación de mensajes de AJO**. A continuación, puede [acceder a los registros](#access-exported-data) del conjunto de datos y exportarlos al destino de almacenamiento seleccionado en función del flujo de datos de exportación que haya definido.

>[!NOTE]
>
>Al deshabilitar la opción **[!UICONTROL Habilitar exportación de mensajes]**, se detienen los nuevos registros para que esta configuración de canal no se ingrese en el conjunto de datos. Los registros existentes se conservarán hasta que caduque la retención.

## Acceso a datos de mensajes exportados {#access-exported-data}

Una vez enviados los mensajes mediante una configuración de canal con la opción Message Export habilitada, podrá obtener acceso a los datos exportados y revisarlos en el **conjunto de datos de exportación de mensajes de AJO**.

Para ver los datos de mensajes exportados:

1. En [!DNL Journey Optimizer], vaya a **[!UICONTROL Administración de datos]** > **[!UICONTROL Conjuntos de datos]** en el panel de navegación izquierdo. [Más información sobre los conjuntos de datos](../data/get-started-datasets.md)

1. Asegúrese de mostrar los conjuntos de datos generados por el sistema.

1. Seleccione el **conjunto de datos de exportación de mensajes de AJO** de la lista.

   ![](assets/datasets-list.png)

1. En la página de detalles del conjunto de datos, haga clic en **[!UICONTROL Vista previa del conjunto de datos]** para ver los registros más recientes.

   ![](assets/ajo-message-export-dataset.png)

El conjunto de datos contiene información completa para cada mensaje enviado a través de la configuración de canal con Exportación de mensajes habilitada, que incluye: línea de asunto, cuerpo del mensaje, dirección de correo electrónico del destinatario o número de teléfono, dirección del remitente o número de teléfono, fecha y hora de envío, datos de personalización, etc.

Todos los registros del conjunto de datos se conservarán durante **siete días naturales a partir de la ingesta**. Durante este período de retención, puede acceder a los datos para realizar auditorías de conformidad o consultas legales, o exportarlos a su propio sistema de almacenamiento a través del destino configurado de Experience Platform.

