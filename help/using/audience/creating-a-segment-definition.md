---
solution: Journey Optimizer
product: journey optimizer
title: Generar definiciones de segmentos
description: Obtenga información sobre cómo crear audiencias a través de definiciones de segmentos
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 5%

---

# Generar definiciones de segmentos {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="Crear una regla"
>abstract="El método de creación de reglas Build permite crear una nueva definición de audiencia utilizando el servicio de Audiencias de Adobe Experience Platform."

En este ejemplo, crearemos una audiencia dirigida a todos los clientes que viven en Atlanta, San Francisco o Seattle y que nacieron después de 1980. Todos estos clientes deberían haber abierto la aplicación de Luma en los últimos 7 días y luego realizar una compra en las 2 horas siguientes a la apertura de la aplicación.

➡️ [Aprenda a crear audiencias en este vídeo](#video-segment)

1. Acceda a la **[!UICONTROL Audiencias]** , luego haga clic en el **[!UICONTROL Crear audiencia]** botón.

   ![](assets/create-segment.png)

   La pantalla de definición del segmento le permite configurar todos los campos obligatorios para definir la audiencia. Obtenga información sobre cómo configurar audiencias en [Documentación del Servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target="_blank"}.

   ![](assets/segment-builder.png)

1. En el **[!UICONTROL Propiedades de audiencia]** , proporcione un nombre y una descripción (opcional) para la audiencia.

   ![](assets/segment-properties.png)

1. Arrastre y suelte los campos deseados del panel izquierdo al espacio de trabajo central y, a continuación, configúrelos según sus necesidades.

   >[!NOTE]
   >
   >Tenga en cuenta que los campos disponibles en el panel izquierdo varían según la forma en que **Perfil individual de XDM** y **ExperienceEvent de XDM** se han configurado esquemas para su organización.  Obtenga más información en la [Documentación del Modelo de datos de experiencia (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

   ![](assets/drag-fields.png)

   En este ejemplo, tenemos que confiar en **Atributos** y **Eventos** campos para crear la audiencia:

   * **Atributos**: perfiles que viven en Atlanta, San Francisco o Seattle nacidos después de 1980

     ![](assets/add-attributes.png)

   * **Eventos**: perfiles que abrieron la aplicación de Luma en los últimos 7 días y que luego realizaron una compra en las 2 horas siguientes a la apertura de la aplicación.

     ![](assets/add-events.png)

1. Al añadir y configurar nuevos campos en el espacio de trabajo, la variable **[!UICONTROL Propiedades de audiencia]** Este panel se actualiza automáticamente con información sobre los perfiles estimados que pertenecen a la audiencia.

   ![](assets/segment-estimate.png)

1. Cuando la audiencia esté lista, haga clic en **[!UICONTROL Guardar]**. Se muestra en la lista de audiencias de Adobe Experience Platform. Tenga en cuenta que hay una barra de búsqueda disponible para ayudarle a buscar en una audiencia específica de la lista.

Ahora, la audiencia se puede utilizar en los recorridos. Para obtener más información, consulte [esta sección](../audience/about-audiences.md).

## Vídeo explicativo{#video-segment}

Obtenga información sobre cómo crear audiencias.

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
