---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Generar público
description: Aprenda a utilizar la actividad Generar audiencia en una campaña organizada
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 74%

---


# Generar público {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Actividad Crear público"
>abstract="La actividad **Crear público** le permite definir el público que participará en la campaña orquestada. Cuando se envían mensajes en el contexto de una campaña orquestada, el público del mensaje no se define en la actividad del canal, sino en la actividad **Crear público**."

Como experto en marketing, puede crear segmentos de público complejos a través de una interfaz intuitiva, lo que le permite dirigirse a los usuarios en función de una amplia gama de criterios y comportamientos para adaptar las campañas de forma más eficaz.

Para ello, use la actividad de segmentación **[!UICONTROL Generar público]**. Esta actividad define la audiencia que entra en la campaña orquestada. Al enviar mensajes como parte de una campaña orquestada, la audiencia se define en la actividad **[!UICONTROL Generar audiencia]**, no dentro de la campaña orquestada.

## Configuración de la actividad Generar público {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Público"
>abstract="Seleccione el público, del mismo modo que utiliza un público a la hora de diseñar un nuevo envío."

Siga estos pasos para configurar la actividad **[!UICONTROL Generar público destinatario]**:

1. Añadir una actividad **[!UICONTROL Generar público destinatario]**.

   ![](../assets/build-audience.png)

1. Defina una **[!UICONTROL etiqueta]**.

1. Configure su público siguiendo los pasos que se detallan en las pestañas a continuación.

1. Elija la **[!UICONTROL Dimensión de segmentación]**. La dimensión de segmentación permite definir la población a la que se dirige la operación: destinatarios, beneficiarios de contratos, operadores, suscriptores, etc. De forma predeterminada, el público destinatario se selecciona entre los destinatarios.

1. Haga clic en **[!UICONTROL Continuar]**.

1. Utilice el generador de reglas para definir la consulta. [Obtenga más información acerca del Generador de reglas en esta sección](../orchestrated-rule-builder.md)

1. Especifique si se debe generar una transición de salida si el público está vacío.

## Ejemplos{#build-audience-examples}

Este es un ejemplo de una campaña organizada con dos actividades **[!UICONTROL Generar audiencia]**. La primera se dirige a los perfiles que tienen artículos en el carro de compras, seguida de un envío de correo electrónico. La segunda se dirige a los perfiles con una lista de deseos, seguida de un envío por SMS.

![](../assets/build-audience-2.png)
