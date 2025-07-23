---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Generar público
description: Aprenda a utilizar la actividad Generar público en una campaña organizada
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 89%

---

# Generar público {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Actividad Crear público"
>abstract="La actividad **Crear público** le permite definir el público que participará en la campaña orquestada. Cuando se envían mensajes en el contexto de una campaña orquestada, el público del mensaje no se define en la actividad del canal, sino en la actividad **Crear publico**."

+++ Índice

| Bienvenido a las campañas organizadas | Inicio de su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carga de archivos](../file-upload-schema.md)</li><li>[Ingesta de datos](../ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](../access-manage-orchestrated-campaigns.md) | [Pasos clave para crear una campaña organizada](../gs-campaign-creation.md)<br/><br/>[Creación y programación de las campañas](../create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](../orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabajo con el generador de reglas](../orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](../build-query.md)<br/><br/>[Edición de expresiones](../edit-expressions.md)<br/><br/>[Resegmentación](../retarget.md) | [Introducción a las actividades](about-activities.md)<br/><br/>Actividades:<br/>[AND-join](and-join.md) - <b>[Generar público](build-audience.md)</b> - [Cambiar dimensión](change-dimension.md) - [Actividades del canal](channels.md) - [Combinar](combine.md) - [Deduplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [Guardar público](save-audience.md) - [División](split.md) - [Esperar](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

Como experto en marketing, puede crear segmentos de público complejos a través de una interfaz intuitiva, lo que le permite dirigirse a los usuarios en función de una amplia gama de criterios y comportamientos para adaptar las campañas de forma más eficaz.

Para ello, use la actividad de segmentación **[!UICONTROL Generar público]**. Esta actividad define el público que entra en la campaña organizada. Al enviar mensajes como parte de una campaña organizada, el público se define en la actividad **[!UICONTROL Generar público]**, no dentro de la campaña organizada.

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

1. Utilice el modelador de consultas para definir la consulta. [Obtenga más información sobre el modelador de Consultas en esta sección.](../orchestrated-rule-builder.md)

1. Especifique si se debe generar una transición de salida si el público está vacío.

## Ejemplos{#build-audience-examples}

A continuación, se muestra un ejemplo de campaña organizada con dos actividades **[!UICONTROL Generar público]**. La primera se dirige a los perfiles que tienen artículos en el carro de compras, seguida de un envío de correo electrónico. La segunda se dirige a los perfiles con una lista de deseos, seguida de un envío por SMS.

![](../assets/build-audience-2.png)
