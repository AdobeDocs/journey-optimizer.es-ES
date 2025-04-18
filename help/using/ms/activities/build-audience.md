---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Generar audiencia
description: Aprenda a utilizar la actividad Generar audiencia en una campaña organizada
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 45%

---

# Generar público {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Actividad generar público"
>abstract="La actividad **Generar audiencia** le permite definir la audiencia que entrará en la campaña orquestada. Cuando se envían mensajes en el contexto de una campaña orquestada, la audiencia del mensaje no se define en la actividad del canal, sino en la actividad **Generar audiencia**."

La actividad **Generar público destinatario** es una actividad de **Segmentación**. Esta actividad le permite definir la audiencia que entra en la campaña orquestada. Cuando se envían mensajes en el contexto de una campaña orquestada, la audiencia del mensaje no se define en la actividad del canal, sino en la actividad **Generar audiencia**.

Para definir la población del público destinatario, puede hacer lo siguiente:

* Seleccione un público destinatario de Adobe Experience Platform.
* Cree una nueva audiencia con el modelador de consultas definiendo y combinando criterios de filtrado.

>[!NOTE]
>
>Las audiencias cargadas desde un archivo no se pueden segmentar con una actividad Generar audiencia. Para ello, necesita usar una actividad **Cargar archivo** seguida de una actividad **Reconciliación**.

<!--
The **Build audience** activity can be placed at the beginning of the workflow or after any other activity. Any activity can be placed after the **Build audience**.
-->

## Configuración de la actividad Generar público {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Público"
>abstract="Seleccione el público, del mismo modo que utiliza un público a la hora de diseñar un nuevo envío."

Siga estos pasos para configurar la actividad **Generar público destinatario**:

![](../assets/workflow-audience.png)

1. Añadir una actividad **Generar público destinatario**.
1. Defina una etiqueta.
1. Defina el tipo de público destinatario: **Crear la suya propia** o **Leer público destinatario**.
1. Configure su audiencia siguiendo los pasos detallados en las pestañas a continuación.

>[!BEGINTABS]

>[!TAB Cree su propia (consulta)]

Para crear su propia consulta, siga estos pasos:

1. Seleccione **Crear su propia (consulta)**.
1. Elija la **Dimensión de segmentación**. La dimensión de segmentación permite definir la población a la que se dirige la operación: destinatarios, beneficiarios de contratos, operadores, suscriptores, etc. De forma predeterminada, el público destinatario se selecciona entre los destinatarios.
1. Haga clic en **Continuar**.
1. Utilice el modelador de consultas para definir la consulta, del mismo modo que crea una audiencia al diseñar un nuevo correo electrónico.

>[!TAB Leer audiencia]

Para seleccionar un público destinatario existente, siga estos pasos:

1. Seleccione **Leer público destinatario**.
1. Haga clic en **Continuar**.
1. Seleccione el público, del mismo modo que utiliza un público a la hora de diseñar un nuevo envío.

>[!ENDTABS]

## Ejemplos{#build-audience-examples}

Este es un ejemplo de una campaña orquestada con dos actividades **Generar audiencia**. El primero se dirige al público de jugadores de póquer, seguido de un envío por correo electrónico. El segundo se dirige al público de clientes VIP, seguido de un envío por SMS.

![](../assets/workflow-audience-example.png)
