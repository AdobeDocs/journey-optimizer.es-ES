---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Guardar público
description: Aprenda a utilizar la actividad Guardar audiencia en una campaña organizada
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/YBp0ehescfw8tVa1pJD2YQuQqRXJ9iG8nDDq9FKzHPs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: cda41058be1eb26538f4b0ef8c7b6c3f1c01eccd
workflow-type: tm+mt
source-wordcount: 576
ht-degree: 20%

---

# Guardar público {#save-audience}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a utilizar la actividad de segmentación Guardar audiencia para crear o sobrescribir una audiencia reutilizable de la población creada anteriormente en una campaña orquestada.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Actividad Guardar público"
>abstract="La actividad **Guardar público** es una actividad de **Segmentación** que le permite actualizar un público existente o crear uno nuevo a partir de la población generada anteriormente en la campaña organizada. Una vez creados, estos públicos se añaden a la lista de públicos de la aplicación y se puede acceder a ellos desde el menú **Públicos**."

La actividad **[!UICONTROL Guardar audiencia]** es una actividad de **[!UICONTROL Segmentación]** que se usa para crear una audiencia nueva o actualizar una existente en función de la población generada anteriormente en la campaña orquestada. Una vez guardada, la audiencia se agrega a la lista de audiencias de aplicación y se puede acceder a ella desde el menú **[!UICONTROL Audiencias]**.

Normalmente se utiliza para capturar segmentos de audiencia creados dentro del mismo flujo de trabajo de campaña, lo que los hace disponibles para su reutilización en campañas futuras. Normalmente, está conectado a otras actividades de segmentación, como **[!UICONTROL Generar audiencia]** o **[!UICONTROL Combinar]**, para guardar la población de destino final.
Tenga en cuenta que con la actividad **[!UICONTROL Guardar audiencia]** no puede actualizar una audiencia existente. Solo puede crear una audiencia nueva o sobrescribir una existente con una definición nueva.

## Configuración de la actividad Guardar público {#save-audience-configuration}

Siga estos pasos para configurar la actividad **[!UICONTROL Guardar público]**:

1. Agregue una actividad **[!UICONTROL Guardar audiencia]** a su campaña orquestada.

1. Escriba una **[!UICONTROL etiqueta de público]** que identifique el público guardado.

   >[!NOTE]
   >
   >La audiencia **[!UICONTROL Label]** debe ser única en todas las campañas. No puede reutilizar un nombre de audiencia que ya se haya usado en la actividad **[!UICONTROL Guardar audiencia]** de otra campaña.

1. Elija un **[!UICONTROL campo de asignación de perfiles&#x200B;]** de su dimensión de segmentación de campañas. Esta asignación define cómo los perfiles de la **audiencia guardada** están vinculados a la dimensión de destino de la campaña durante la ejecución.

   Solo las asignaciones compatibles con la dimensión de destino actual, es decir, la de la transición entrante, están disponibles en la lista desplegable para garantizar la reconciliación adecuada entre la audiencia y el contexto de la campaña.

   ➡️ [Siga los pasos detallados en esta página para crear su dimensión de segmentación de campaña](../target-dimension.md)

   ![](../assets/save-audience-1.png)

1. Haga clic en **[!UICONTROL Agregar asignaciones de audiencia]** para incluir datos adicionales de los atributos de la **[!UICONTROL dimensión de destino]** o de los **[!UICONTROL atributos de perfil]** enriquecidos.

   Esto le permite asociar más información con la actividad **[!UICONTROL Audiencia guardada]** más allá de la asignación de perfil principal, lo que mejora las opciones de segmentación y personalización.

   ![](../assets/save-audience-2.png)

1. Finalice la configuración guardando y publicando la campaña orquestada. Así se generará y almacenará su público.

1. Publique la campaña para la audiencia que se va a crear o reemplazar, ya que la actividad **[!UICONTROL Guardar audiencia]** no se ejecuta mientras la campaña esté en **[!UICONTROL modo borrador]**.

>[!NOTE]
>
>En el momento de la publicación, las actividades **[!UICONTROL Guardar audiencia]** siempre se ejecutan antes que cualquier actividad de mensaje en el flujo de trabajo. Se crea el shell de audiencia y los perfiles comienzan a ingerirse en Audience Portal antes de que cualquier actividad de canal comience a procesarse. [Obtenga más información acerca de la secuencia de ejecución en tiempo de publicación](../start-monitor-campaigns.md#publication-sequence)

El contenido de la audiencia guardada está disponible en la vista de detalles de la audiencia, a la que se puede acceder desde el menú **[!UICONTROL Audiencias]**, o se puede seleccionar al segmentar una audiencia, por ejemplo, con una actividad **[!UICONTROL Leer audiencia]**.

![](../assets/save-audience-4.png)

>[!NOTE]
>
>Si la definición de la audiencia utiliza atributos de esquema de Experience Platform etiquetados con Data Usage (DULE), la audiencia guardada hereda automáticamente esas etiquetas. No es necesario que vuelva a aplicarlos. [Más información sobre la administración de datos](../../action/action-privacy.md)

## Ejemplo {#save-audience-example}

En el siguiente ejemplo se muestra cómo crear un público simple mediante la segmentación. Una consulta identifica a todos los destinatarios que reservaron un viaje en los últimos 30 días filtrando esta población dentro de la campaña orquestada. Al elegir **Destinatarios - CRMID** como **dimensión de segmentación**, la audiencia se dirige a cada evento de reserva individual en lugar de solo al destinatario en su conjunto. A continuación, la actividad **[!UICONTROL Guardar público]** captura estos perfiles para crear un público reutilizable de compradores recientes.

![](../assets/save-audience-3.png)
