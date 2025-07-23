---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Reconciliación
description: Aprenda a utilizar la actividad Reconciliación en una campaña organizada
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 93%

---

# Reconciliación {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="Actividad de reconciliación"
>abstract="La actividad **Reconciliación** es una actividad de **Segmentación** que le permite definir el vínculo entre Adobe Journey Optimizer y los datos de una tabla de trabajo. "

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_field"
>title="Campo de selección de reconciliación"
>abstract="Campo de selección de reconciliación"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_condition"
>title="Condición de creación de reconciliación"
>abstract="Condición de creación de reconciliación"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_complement"
>title="Complemento de generación de reconciliación"
>abstract="Complemento de generación de reconciliación"


+++ Índice

| Bienvenido a las campañas organizadas | Inicio de su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carga de archivos](../file-upload-schema.md)</li><li>[Ingesta de datos](../ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](../access-manage-orchestrated-campaigns.md) | [Pasos clave para crear una campaña organizada](../gs-campaign-creation.md)<br/><br/>[Creación y programación de las campañas](../create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](../orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabajo con el generador de reglas](../orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](../build-query.md)<br/><br/>[Edición de expresiones](../edit-expressions.md)<br/><br/>[Resegmentación](../retarget.md) | [Introducción a las actividades](about-activities.md)<br/><br/>Actividades:<br/>[AND-join](and-join.md) - [Generar público](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Actividades del canal](channels.md) - [Combinar](combine.md) - [Deduplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - <b>[Reconciliación](reconciliation.md)</b> - [Guardar público](save-audience.md) - [División](split.md) - [Esperar](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

La actividad **[!UICONTROL Reconciliación]** es una actividad de **[!UICONTROL Segmentación]** que permite definir el vínculo entre los datos de la base de datos de Adobe Journey Optimizer y los datos de una tabla de trabajo, por ejemplo, los datos cargados desde un archivo externo.

La actividad **[!UICONTROL Enriquecimiento]** le permite añadir datos adicionales a su campaña organizada, por ejemplo, combinando datos de varias fuentes o vinculándolos a un recurso temporal. Por el contrario, la actividad **[!UICONTROL Reconciliación]** se usa para hacer coincidir datos externos o no identificados con los recursos existentes en la base de datos.

**[!UICONTROL Reconciliación]** requiere que los registros relacionados ya existan en el sistema. Por ejemplo, si importa un archivo de compra que enumera productos, marcas de tiempo e información de clientes, tanto los productos como los clientes deben estar presentes en la base de datos para establecer el vínculo.

## Configuración de la actividad Reconciliación {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="Dimensión de segmentación"
>abstract="Seleccionar la nueva dimensión de segmentación. Una dimensión permite definir la población objetivo: destinatarios, suscriptores de la aplicación, operadores, suscriptores, etc. De forma predeterminada, está seleccionada la dimensión de segmentación actual."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="Reglas de reconciliación"
>abstract="Seleccione las reglas de reconciliación que desee utilizar para la anulación de duplicación. Para utilizar atributos, seleccione **Atributos simples** y seleccione los campos de origen y destino. Para crear su propia condición de reconciliación utilizando el modelador de consultas, seleccione la opción **Condiciones de reconciliación avanzadas**."
>additional-url="https://experienceleague.adobe.com/es/docs/campaign-web/v8/query-database/query-modeler-overview" text="Uso del modelador de consultas"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="Seleccionar la dimensión de segmentación"
>abstract="Seleccione la dimensión de segmentación con la que se reconciliarán los datos de entrada."
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html?lang=es#targeting-dimensions" text="Dimensiones de segmentación"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="Mantener datos no reconciliados"
>abstract="De forma predeterminada, los datos no reconciliados se mantienen en la transición de salida y están disponibles en la tabla de trabajo para usarlos en el futuro. Para quitar los datos no reconciliados, desactive la opción **Mantener datos no reconciliados**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="Atributo de reconciliación"
>abstract="Seleccione el atributo que desea utilizar para reconciliar los datos y haga clic en Confirmar."

Siga estos pasos para configurar la actividad **[!UICONTROL Reconciliación]**:

1. Añada una actividad **[!UICONTROL Reconciliación]** al flujo de trabajo.

1. Elija una nueva dimensión de segmentación para definir a quién se está dirigiendo, como los destinatarios o los suscriptores.

1. Establezca los campos que se utilizarán para hacer coincidir los datos entrantes con los perfiles existentes.

1. Para hacer coincidir los datos usando campos básicos, seleccione **[!UICONTROL Atributos simples]**.

1. Establezca los campos coincidentes:

   * **[!UICONTROL Origen]**: enumera los campos de datos entrantes.

   * **[!UICONTROL Destino]**: hace referencia a campos en la dimensión de segmentación seleccionada.

   Se produce una coincidencia cuando ambos valores son iguales; por ejemplo, al hacer coincidir **[!UICONTROL Correo electrónico]** para identificar perfiles.

   ![](../assets/workflow-reconciliation-criteria.png)

1. Para añadir más reglas coincidentes, haga clic en **[!UICONTROL Añadir regla]**. Se deben cumplir todas las condiciones para que se produzca una coincidencia.

1. Para condiciones más complejas, elija **[!UICONTROL Condiciones de reconciliación avanzadas]**. Use el [modelador de consultas](../orchestrated-rule-builder.md) para definir la lógica personalizada.

1. Para filtrar qué datos desea reconciliar, haga clic en **[!UICONTROL Crear filtro]** y defina la condición en el modelador de consultas.

1. De forma predeterminada, los datos no coincidentes se mantienen en la transición de salida y están disponibles en la tabla de trabajo. Para quitarlos, habilite la opción **[!UICONTROL Mantener datos no reconciliados]**.

## Ejemplo {#example-reconciliation}

Este ejemplo utiliza la actividad **[!UICONTROL Reconciliación]** de Adobe Journey Optimizer para garantizar que los correos electrónicos se envíen únicamente a los clientes reconocidos. Los datos fluyen a través de la actividad **[!UICONTROL Leer público]** que se dirige a los usuarios con pedidos anteriores. A continuación, la actividad **[!UICONTROL Reconciliación]** hace coincidir estos datos entrantes con los perfiles existentes en la base de datos mediante el campo de correo electrónico.

![](../assets/workflow-reconciliation-sample-1.0.png)
