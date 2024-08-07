---
solution: Journey Optimizer
product: journey optimizer
title: Generar definiciones de segmentos
description: Obtenga información sobre cómo crear audiencias a través de definiciones de segmentos
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: b9d70bf2b3e16638a03b59fd4036771ad959a631
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 16%

---

# Generar definiciones de segmentos {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="Crear una regla"
>abstract="El método de creación Generar regla le permite crear una nueva definición de público mediante el servicio de segmentación de Adobe Experience Platform."

En este ejemplo, crearemos una audiencia dirigida a todos los clientes que viven en Atlanta, San Francisco o Seattle y que nacieron después de 1980. Todos estos clientes deberían haber abierto la aplicación de Luma en los últimos 7 días y luego realizar una compra en las 2 horas siguientes a la apertura de la aplicación.

➡️ [Aprenda a crear audiencias en este vídeo](#video-segment)

1. En el menú **[!UICONTROL Audiencias]**, haga clic en el botón **[!UICONTROL Crear audiencia]** y seleccione **[!UICONTROL Generar regla]**.

   ![](assets/create-segment.png)

   La pantalla de definición del segmento le permite configurar todos los campos obligatorios para definir la audiencia. Aprenda a configurar audiencias en la [documentación del servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=es){target="_blank"}.

   ![](assets/segment-builder.png)

1. En el panel **[!UICONTROL Propiedades de audiencia]**, proporcione un nombre y una descripción (opcional) para la audiencia.

   ![](assets/segment-properties.png)

1. Arrastre y suelte los campos deseados del panel izquierdo al espacio de trabajo central y, a continuación, configúrelos según sus necesidades.

   >[!NOTE]
   >
   >Tenga en cuenta que los campos disponibles en el panel izquierdo varían según cómo se hayan configurado los esquemas **XDM Individual Profile** y **XDM ExperienceEvent** para su organización.  Obtenga más información en la [documentación del Modelo de datos de experiencia (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

   ![](assets/drag-fields.png)

   En este ejemplo, necesitamos basarnos en los campos **Atributos** y **Eventos** para generar la audiencia:

   * **Atributos**: perfiles que viven en Atlanta, San Francisco o Seattle nacidos después de 1980

     ![](assets/add-attributes.png)

   * **Eventos**: perfiles que abrieron la aplicación Luma en los últimos 7 días y que luego realizaron una compra en un plazo de 2 horas después de abrir la aplicación.

     ![](assets/add-events.png)

     >[!NOTE]
     >
     >El Adobe recomienda no utilizar abrir y enviar eventos con segmentación de flujo continuo. En su lugar, utilice señales reales de actividad del usuario como clics, compras o datos de señalizaciones. Para la lógica de frecuencia o supresión, utilice reglas empresariales en lugar de enviar eventos. [Más información](about-audiences.md#open-and-send-event-guardrails)

1. A medida que agrega y configura nuevos campos en el área de trabajo, el panel **[!UICONTROL Propiedades de la audiencia]** se actualiza automáticamente con información sobre los perfiles estimados que pertenecen a la audiencia.

   ![](assets/segment-estimate.png)

1. Una vez que la audiencia esté lista, haga clic en **[!UICONTROL Guardar]**. Se muestra en la lista de audiencias de Adobe Experience Platform. Tenga en cuenta que hay una barra de búsqueda disponible para ayudarle a buscar en una audiencia específica de la lista.

Ahora, la audiencia se puede utilizar en los recorridos. Para obtener más información, consulte [esta sección](../audience/about-audiences.md).

## Vídeo explicativo{#video-segment}

Descubra cómo Journey Optimizer utiliza reglas para generar público y aprenda a utilizar atributos, eventos y audiencias existentes para crear público.

>[!VIDEO](https://video.tv.adobe.com/v/3425020?quality=12)
