---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad de reconciliación
description: Aprenda a utilizar la actividad de reconciliación en una campaña organizada
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 5872e192c849b7a7909f0b50caa1331b15490d79
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 37%

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

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicie su primera campaña orquestada | Consultar la base de datos | Actividades de campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](../configuration-steps.md)<br/><br/>[Pasos clave para la creación de campañas orquestadas](../gs-campaign-creation.md) | [Crear una campaña orquestada](../create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](../orchestrate-activities.md)<br/><br/>[Enviar mensajes con campañas orquestadas](../send-messages.md)<br/><br/>[Iniciar y supervisar la campaña](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabaje con el Modeler de consultas](../orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](../build-query.md)<br/><br/>[Editar expresiones](../edit-expressions.md) | [Empiece con las actividades](about-activities.md)<br/><br/>Actividades:<br/>[Y únase](and-join.md) - [Generar audiencia](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Combinar](combine.md) - [Anulación de duplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [División](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

La actividad **Reconciliation** es una actividad **Targeting** que permite definir el vínculo entre los datos de Adobe Journey Optimizer y los de una tabla de trabajo; por ejemplo, los datos cargados de un archivo externo.

La actividad Enrichment permite agregar datos adicionales a la campaña orquestada; por ejemplo, combinando datos de varias fuentes o vinculándolos a un recurso temporal. Por el contrario, la actividad Reconciliación se utiliza para hacer coincidir datos externos o no identificados con los recursos existentes en la base de datos.

La reconciliación requiere que los registros relacionados ya existan en el sistema. Por ejemplo, si importa un archivo de compra que enumera productos, marcas de tiempo e información de clientes, tanto los productos como los clientes deben estar presentes en la base de datos para establecer el vínculo.

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

Siga estos pasos para configurar la actividad **Reconciliation**:

1. Agregue una actividad **Reconciliation** a su campaña orquestada.

1. Seleccionar la nueva dimensión de segmentación. Una dimensión permite definir la población objetivo: destinatarios, suscriptores de la aplicación, operadores, suscriptores, etc.

1. Seleccione los campos que se utilizarán para la reconciliación. Se pueden utilizar uno o más criterios de reconciliación.

   1. Para usar atributos para reconciliar datos, seleccione la opción **Atributos simples**. El campo **Source** enumera los campos disponibles en la transición de entrada que deben conciliarse. El campo **Destino** corresponde a los campos de la dimensión de segmentación seleccionada. Los datos se concilian cuando el origen y el destino son iguales. Por ejemplo, seleccione los campos **Correo electrónico** para anular la duplicación de perfiles según su dirección de correo electrónico.

      Para agregar otros criterios de reconciliación, haga clic en el botón **Agregar regla**. Si se especifican varias condiciones de vínculo, todas deben verificarse para que los datos puedan vincularse.

      ![](../assets/workflow-reconciliation-criteria.png)

   1. Para usar otros atributos para reconciliar datos, seleccione la opción **Condiciones de reconciliación avanzadas**. A continuación, puede crear su propia condición de reconciliación utilizando el modelador de consultas.

1. Puede filtrar los datos para conciliarlos usando el botón **Crear filtro**. Esto permite crear una condición personalizada mediante el modelador de consultas.

De forma predeterminada, los datos no conciliados se mantienen en la transición saliente y están disponibles en la tabla de trabajo para su uso futuro. Para quitar los datos no reconciliados, desactive la opción **Mantener datos no reconciliados**.
