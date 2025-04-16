---
solution: Journey Optimizer
product: journey optimizer
title: Uso del actividad de audiencia de compilación
description: Aprenda a utilizar el actividad de audiencia de compilación de una campaña orquestada
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
>abstract="La **actividad Build audiencia** permite definir la audiencia que entrará en el campaña orquestado. Al enviar mensajes en el contexto de un campaña orquestado, el audiencia de mensaje no se define en el actividad de canal, sino en el **actividad Build audiencia** ."

La actividad **Generar público destinatario** es una actividad de **Segmentación**. Este actividad permite definir la audiencia que entrará en el campaña orquestado. Al enviar mensajes en el contexto de un campaña orquestado, el audiencia de mensaje no se define en el actividad de canal, sino en el **actividad Build audiencia** .

Para definir la población del público destinatario, puede hacer lo siguiente:

* Seleccione un público destinatario de Adobe Experience Platform.
* Cree una nueva audiencia con el consulta modelador definiendo y combinando criterios de filtrado.

>[!NOTE]
>
>Los Audiences cargados desde un archivo no se pueden segmentar mediante un actividad de audiencia de compilación. Para ello, debe utilizar una actividad de **archivo de carga** seguida de una **actividad de reconciliación** .

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

>[!TAB Crear los tuyos (consulta)]

Para crear su propia consulta, seguir estos pasos:

1. Seleccione **Crear su propia (consulta)**.
1. Elija la **Dimensión de segmentación**. La dimensión de segmentación permite definir la población a la que se dirige la operación: destinatarios, beneficiarios de contratos, operadores, suscriptores, etc. De forma predeterminada, el público destinatario se selecciona entre los destinatarios.
1. Haga clic en **Continuar**.
1. Utilice el modelador de consulta para definir su consulta, de la misma manera que crea un audiencia al diseñar un nuevo correo electrónico.

>[!TAB Leer audiencia]

Para seleccionar un público destinatario existente, siga estos pasos:

1. Seleccione **Leer público destinatario**.
1. Haga clic en **Continuar**.
1. Seleccione el público, del mismo modo que utiliza un público a la hora de diseñar un nuevo envío.

>[!ENDTABS]

## Ejemplos{#build-audience-examples}

Este es un ejemplo de un campaña orquestado con dos **actividades de audiencia** de compilación. El primero se dirige al público de jugadores de póquer, seguido de un envío por correo electrónico. El segundo se dirige al público de clientes VIP, seguido de un envío por SMS.

![](../assets/workflow-audience-example.png)
