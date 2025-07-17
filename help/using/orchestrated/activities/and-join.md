---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad AND-join
description: Aprenda a utilizar la actividad AND-join en una campaña organizada
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 34%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Actividad AND-join"
>abstract="La actividad **And-join** le permite sincronizar varias ramas de ejecución de una campaña orquestada. Se activa una vez que hayan finalizado todas las actividades anteriores. Esto le permite asegurarse de que determinadas actividades se completen antes de continuar con la ejecución de la campaña orquestada."


+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carga de archivos](../file-upload-schema.md)</li><li>[Ingesta de datos](../ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](../access-manage-orchestrated-campaigns.md) | [Pasos clave para crear una campaña orquestada](../gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](../create-orchestrated-campaign.md)<br/><br/>[Organice las actividades](../orchestrate-activities.md)<br/><br/>[Inicie y supervise la campaña](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabaje con el generador de reglas](../orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](../build-query.md)<br/><br/>[Edite expresiones](../edit-expressions.md)<br/><br/>[Redireccionamiento](../retarget.md) | [Empiece con las actividades](about-activities.md)<br/><br/>Actividades:<br/><b>[Y únase](and-join.md)</b> - [Generar audiencia](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Actividades de canal](channels.md) - [Combinar](combine.md) - [Anulación de duplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [Guardar](save-audience.md) - [División](split.md) [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

La actividad **[!UICONTROL Combinación-Y]** es una actividad de **[!UICONTROL Control de flujo]**. Permite sincronizar varias ramas de ejecución de una campaña orquestada.

Esta actividad solo activa su transición saliente una vez que se activan todas las transiciones entrantes; es decir, una vez que todas las actividades anteriores han finalizado. Esto le permite asegurarse de que ciertas actividades han finalizado antes de continuar ejecutándose la campaña orquestada.

## Configuración de la actividad And-join{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Combinación de opciones"
>abstract="Seleccione las actividades que desea unir. En el menú desplegable **Conjunto principal**, elija qué población de transición entrante desea conservar."

Siga estos pasos para configurar la actividad **[!UICONTROL Combinación-Y]**:

![](../assets/workflow-andjoin.png)

1. Añada varias actividades, como actividades de canal, para crear al menos dos ramas de ejecución distintas.

1. Inserte una actividad **[!UICONTROL AND-join]** en una de las ramas.

1. En la sección **[!UICONTROL Combinar opciones]**, seleccione todas las actividades anteriores a las que desee unirse.

1. En el menú desplegable **[!UICONTROL Conjunto principal]**, elija la población de transición entrante que desea conservar.

## Ejemplo{#and-join-example}

Este ejemplo ilustra dos ramas de campaña coordinadas, cada una de las cuales incluye una entrega por correo electrónico, una dirigida a los miembros oro y otra plata. **[!UICONTROL AND-join]** se activa una vez que se activan ambas transiciones entrantes, y el SMS se enviará solo después de que se completen ambos envíos de correo electrónico, después de un retraso de 7 días.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
