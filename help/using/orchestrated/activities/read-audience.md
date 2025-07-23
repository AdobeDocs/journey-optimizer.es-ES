---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Leer público
description: Aprenda a utilizar la actividad Leer público en una campaña organizada
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ef8eba57-cd33-4746-8eb4-5214ef9cbe2f
source-git-commit: 2ad659b391515c193418325c34a9dd56133b90d6
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 38%

---

# Leer público {#read-audience}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_read_audience"
>title="Actividad Crear público"
>abstract="La actividad **Crear público** le permite definir el público que participará en la campaña orquestada. Este público puede ser un público existente de Adobe Experience Platform o un público extraído de un archivo CSV. Cuando se envían mensajes en el contexto de una campaña orquestada, el público del mensaje no se define en la actividad del canal, sino en una actividad **Leer público** o **Crear público**."


+++ Índice

| Bienvenido a las campañas organizadas | Inicio de su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carga de archivos](../file-upload-schema.md)</li><li>[Ingesta de datos](../ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](../access-manage-orchestrated-campaigns.md) | [Pasos clave para crear una campaña organizada](../gs-campaign-creation.md)<br/><br/>[Creación y programación de las campañas](../create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](../orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabajo con el generador de reglas](../orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](../build-query.md)<br/><br/>[Edición de expresiones](../edit-expressions.md)<br/><br/>[Resegmentación](../retarget.md) | [Introducción a las actividades](about-activities.md)<br/><br/>Actividades:<br/>[AND-join](and-join.md) - [Generar público](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Actividades del canal](channels.md) - [Combinar](combine.md) - [Deduplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [Guardar público](save-audience.md) - [División](split.md) - [Esperar](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

La actividad **[!UICONTROL Leer audiencia]** le permite recuperar una audiencia existente (previamente guardada o importada) y reutilizarla dentro de una campaña orquestada. Esta actividad es especialmente útil para segmentar un conjunto predefinido de perfiles sin necesidad de ejecutar un nuevo proceso de segmentación.

Una vez cargada la audiencia, puede refinarla seleccionando un campo de identidad único y enriqueciéndola con atributos de perfil adicionales para fines de segmentación, personalización o creación de informes.

## Configuración de la actividad Leer audiencia {#read-audience-configuration}

Siga estos pasos para configurar la actividad **[!UICONTROL Leer audiencia]**:

1. Agregue una actividad **[!UICONTROL Leer audiencia]** a su campaña orquestada.

   ![](../assets/read-audience-1.png)

1. Ingrese una **[!UICONTROL etiqueta]** a su actividad.

1. Haga clic en ![icono de búsqueda de carpetas](../assets/do-not-localize/folder-search.svg) para seleccionar la audiencia a la que desea dirigirse para su campaña orquestada.

   ![](../assets/read-audience-2.png)

1. Seleccione la **[!UICONTROL entidad]** utilizada para identificar perfiles de forma única en su audiencia.

   ![](../assets/read-audience-3.png)

1. Seleccione **[!UICONTROL Agregar atributo de perfil]** para enriquecer la audiencia seleccionada con datos adicionales. La audiencia resultante contendrá una lista de destinatarios, cada uno enriquecido con los atributos de perfil seleccionados.

1. Elija los **[!UICONTROL atributos]** que desee agregar a su audiencia.

   ![](../assets/read-audience-4.png)

## Ejemplo

En el ejemplo siguiente, la actividad **[!UICONTROL Leer audiencia]** se usa para recuperar una audiencia de perfiles creada y guardada anteriormente que se suscribieron al boletín informativo. A continuación, la audiencia se enriquece con el atributo **Membresía de fidelidad** para habilitar la segmentación de usuarios que sean miembros registrados del programa de fidelidad.

![](../assets/read-audience-5.png)
