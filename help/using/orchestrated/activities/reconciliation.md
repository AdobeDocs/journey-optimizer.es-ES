---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad de reconciliación
description: Aprenda a utilizar la actividad de reconciliación en una campaña organizada
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 779c90f0be57749a63da103d18cc642106c5f837
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 32%

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

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](../configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](../access-manage-orchestrated-campaigns.md) | [Pasos clave para crear una campaña orquestada](../gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](../create-orchestrated-campaign.md)<br/><br/>[Organice las actividades](../orchestrate-activities.md)<br/><br/>[Inicie y supervise la campaña](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabaje con el generador de reglas](../orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](../build-query.md)<br/><br/>[Edite expresiones](../edit-expressions.md)<br/><br/>[Redireccionamiento](../retarget.md) | [Empiece con las actividades](about-activities.md)<br/><br/>Actividades:<br/>[Y únase](and-join.md) - [Generar audiencia](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Actividades de canal](channels.md) - [Combinar](combine.md) - [Anulación de duplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - <b>[Reconciliación](reconciliation.md)</b> - [Guardar](save-audience.md) - [División](split.md) [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

Documentación en curso

>[!ENDSHADEBOX]

La actividad **[!UICONTROL Reconciliation]** es una actividad **[!UICONTROL Targeting]** que permite definir el vínculo entre los datos de Adobe Journey Optimizer y los de una tabla de trabajo; por ejemplo, los datos cargados de un archivo externo.

La actividad **[!UICONTROL Enrichment]** le permite agregar datos adicionales a su campaña orquestada, por ejemplo, combinando datos de varias fuentes o vinculándolos a un recurso temporal. Por el contrario, la actividad **[!UICONTROL Reconciliation]** se usa para hacer coincidir datos externos o no identificados con los recursos existentes en la base de datos.

**[!UICONTROL La reconciliación]** requiere que los registros relacionados ya existan en el sistema. Por ejemplo, si importa un archivo de compra que enumera productos, marcas de tiempo e información de clientes, tanto los productos como los clientes deben estar presentes en la base de datos para establecer el vínculo.

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

Siga estos pasos para configurar la actividad **[!UICONTROL Reconciliation]**:

1. Agregue una actividad **[!UICONTROL Reconciliation]** al flujo de trabajo.

1. Elija una nueva dimensión de segmentación para definir a quién está dirigiendo, como destinatarios o suscriptores.

1. Establezca los campos que se utilizarán para hacer coincidir los datos entrantes con los perfiles existentes.

1. Para hacer coincidir datos usando campos básicos, seleccione **[!UICONTROL Atributos simples]**.

1. Establezca los campos coincidentes:

   * **[!UICONTROL Source]**: enumera los campos de datos entrantes.

   * **[!UICONTROL Destino]**: hace referencia a campos en la dimensión de segmentación seleccionada.

   Se produce una coincidencia cuando ambos valores son iguales; por ejemplo, al hacer coincidir **[!UICONTROL Email]** se identifican perfiles.

   ![](../assets/workflow-reconciliation-criteria.png)

1. Para agregar más reglas coincidentes, haga clic en **[!UICONTROL Agregar regla]**. Se deben cumplir todas las condiciones para que se produzca una coincidencia.

1. Para condiciones más complejas, elija **[!UICONTROL Condiciones de reconciliación avanzadas]**. Use el [modelador de consultas](../orchestrated-rule-builder.md) para definir la lógica personalizada.

1. Para filtrar qué datos reconciliar, haga clic en **[!UICONTROL Crear filtro]** y defina la condición en el modelador de consultas.

1. De forma predeterminada, los registros no coincidentes se conservan en la transición saliente y se almacenan en la tabla de resultados. Para eliminarlos, habilita la opción **[!UICONTROL Conservar datos no reconciliados]**.

## Ejemplo {#example-reconciliation}

En este ejemplo se utiliza la actividad **[!UICONTROL Reconciliation]** de Adobe Journey Optimizer para garantizar que los mensajes de correo electrónico se envíen únicamente a los clientes reconocidos. Los datos fluyen a través de una actividad **[!UICONTROL Leer audiencia]** que se dirige a usuarios con pedidos anteriores. A continuación, la actividad **[!UICONTROL Reconciliation]** hace coincidir estos datos entrantes con los perfiles existentes en la base de datos mediante el campo de correo electrónico.

![](../assets/workflow-reconciliation-sample-1.0.png)
