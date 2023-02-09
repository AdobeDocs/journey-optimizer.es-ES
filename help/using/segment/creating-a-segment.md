---
solution: Journey Optimizer
product: journey optimizer
title: Generar un segmento
description: Aprenda a crear segmentos
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 5%

---

# Generación de segmentos {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="Crear una regla"
>abstract="El método de creación de reglas de compilación le permite crear una nueva definición de segmento mediante el servicio de segmentación de Adobe Experience Platform."

En este ejemplo, crearemos un segmento dirigido a todos los clientes que viven en Atlanta, San Francisco o Seattle y que nacieron después de 1980. Todos estos clientes deberían haber abierto la aplicación de Luma en los últimos 7 días y luego realizar una compra en un plazo de 2 horas después de abrir la aplicación.

➡️ [Aprenda a crear segmentos en este vídeo](#video-segment)

1. Acceda a la **[!UICONTROL Segmentos]** a continuación, haga clic en el **[!UICONTROL Crear segmento]** botón.

   ![](assets/create-segment.png)

   La pantalla de definición del segmento le permite configurar todos los campos obligatorios para definir el segmento. Obtenga información sobre cómo configurar segmentos en la variable [Documentación del servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target="_blank"}.

   ![](assets/segment-builder.png)

1. En el **[!UICONTROL Propiedades del segmento]** , proporcione un nombre y una descripción (opcional) para el segmento.

   ![](assets/segment-properties.png)

1. Arrastre y suelte los campos deseados del panel izquierdo al espacio de trabajo central y, a continuación, configúrelos según sus necesidades.

   >[!NOTE]
   >
   >Tenga en cuenta que los campos disponibles en el panel izquierdo varían en función de cómo **Perfil individual XDM** y **XDM ExperienceEvent** se han configurado esquemas para su organización.  Obtenga más información en la [Documentación del Modelo de datos de experiencia (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

   ![](assets/drag-fields.png)

   En este ejemplo, necesitamos confiar en **Atributos** y **Eventos** campos para crear el segmento:

   * **Atributos**: perfiles que viven en Atlanta, San Francisco o Seattle nacidos después de 1980

      ![](assets/add-attributes.png)

   * **Eventos**: perfiles que abrieron la aplicación de Luma en los últimos 7 días y luego realizaron una compra en un plazo de 2 horas después de abrir la aplicación.

      ![](assets/add-events.png)

1. Al añadir y configurar nuevos campos en el espacio de trabajo, la variable **[!UICONTROL Propiedades del segmento]** se actualiza automáticamente con información sobre los perfiles estimados que pertenecen al segmento.

   ![](assets/segment-estimate.png)

1. Una vez que el segmento esté listo, haga clic en **[!UICONTROL Guardar]**. Se muestra en la lista de segmentos de Adobe Experience Platform. Tenga en cuenta que hay una barra de búsqueda disponible para ayudarle a buscar un segmento específico en la lista.

El segmento ahora se puede usar en sus recorridos. Para obtener más información, consulte [esta sección](../segment/about-segments.md).

## Vídeo explicativo{#video-segment}

Aprenda a crear segmentos.

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
