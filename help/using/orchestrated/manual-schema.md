---
solution: Journey Optimizer
product: journey optimizer
title: Pasos de configuración
description: Aprenda a crear esquemas relacionales directamente a través de la interfaz de usuario.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 8c785431-9a00-46b8-ba54-54a10e288141
source-git-commit: 3dc0bf4acc4976ca1c46de46cf6ce4f2097f3721
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 3%

---

# Configuración de un esquema relacional manual {#manual-schema}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br><ul><li>[Introducción a esquemas y conjuntos de datos](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](orchestrate-activities.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md)<br/><br/>[Redireccionamiento](retarget.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar](activities/save-audience.md) - [División](activities/split.md) [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

Los esquemas relacionales se pueden crear directamente a través de la interfaz de usuario, lo que permite una configuración detallada de atributos, claves principales, campos de versiones y relaciones.

En el ejemplo siguiente se define manualmente el esquema **Pertenencias de fidelidad** para ilustrar la estructura necesaria para las campañas organizadas.

1. [Cree un esquema relacional manualmente](#schema) mediante la interfaz de Adobe Experience Platform.

1. [Agregar atributos](#schema-attributes) como ID de cliente, nivel de pertenencia y campos de estado.

1. [Vincule su esquema](#link-schema) a esquemas integrados como Destinatarios para la segmentación de campañas.

1. [Cree un conjunto de datos](#dataset) basado en su esquema y actívelo para su uso en campañas organizadas.

1. [Ingresar datos](ingest-data.md) en su conjunto de datos desde fuentes compatibles.

## Cree su esquema {#schema}

Comience creando un nuevo esquema relacional manualmente en Adobe Experience Platform. Este proceso permite definir la estructura de esquema desde cero, incluido su nombre y comportamiento.

1. Inicie sesión en Adobe Experience Platform.

1. Vaya al menú **[!UICONTROL Administración de datos]** > **[!UICONTROL Esquema]**.

1. Haga clic en **[!UICONTROL Crear esquema]**.

1. Seleccione **[!UICONTROL Relacional]** como su **Tipo de esquema**.

   ![](assets/admin_schema_1.png){zoomable="yes"}

1. Elija **[!UICONTROL Crear manualmente]** para generar el esquema agregando campos manualmente.

1. Escriba su **[!UICONTROL nombre para mostrar del esquema]**.

1. Elija **[!UICONTROL Registro]** como su **[!UICONTROL comportamiento de esquema]**.

   ![](assets/schema_manual_8.png){zoomable="yes"}

1. Haga clic en **Finalizar** para continuar con la creación del esquema.

Ahora puede empezar a añadir atributos al esquema para definir su estructura.

## Añadir atributos al esquema {#schema-attributes}

A continuación, añada atributos para definir la estructura del esquema. Estos campos representan los puntos de datos clave utilizados en las campañas orquestadas, como los identificadores de cliente, los detalles de pertenencia y las fechas de actividad. Definirlos con precisión garantiza una personalización, segmentación y seguimiento fiables.

1. En el lienzo, haga clic en ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) junto a su **nombre de esquema** para empezar a agregar atributos.

   ![](assets/schema_manual_1.png){zoomable="yes"}

1. Escriba su atributo **[!UICONTROL Nombre de campo]**, **[!UICONTROL Nombre para mostrar]** y **[!UICONTROL Tipo]**.

   En este ejemplo, agregamos los atributos detallados en la tabla siguiente al esquema **Pertenencias de fidelización**.

+++ Ejemplos de atributos

   | Nombre del atributo | Tipo de datos | Atributos adicionales |
   |-|-|-|
   | cliente | CADENA | Clave principal |
   | member_level | CADENA | Requerido |
   | points_balance | ENTERO | Requerido |
   | enrollment_date | FECHA | Requerido |
   | last_status_change | FECHA | Requerido |
   | expiration_date | FECHA | - |
   | is_active | BOOLEANO | Requerido |
   | última modificación | DATETIME | Requerido |

+++

1. Asigne los campos apropiados como **[!UICONTROL Clave principal]** y **[!UICONTROL Descriptor de versión]**.

   La clave principal **[!UICONTROL Primary Key]** garantiza que cada registro se identifique de forma única, mientras que el descriptor de versión **[!UICONTROL Version]** captura las actualizaciones con el tiempo, lo que permite la captura de datos modificados y admite la creación de reflejo de datos.

   ![](assets/schema_manual_2.png){zoomable="yes"}

1. Haga clic en **[!UICONTROL Guardar]**.

Una vez creados los atributos, debe vincular el esquema recién creado con un esquema integrado.

## Vincular esquemas {#link-schema}

La creación de una relación entre dos esquemas permite enriquecer las campañas orquestadas con datos almacenados fuera del esquema de perfil principal.

1. En el esquema recién creado, seleccione el atributo que desee usar como vínculo y haga clic en **[!UICONTROL Agregar relación]**.

   ![](assets/schema_manual_3.png){zoomable="yes"}

1. Elija **[!UICONTROL Esquema de referencia]** y **[!UICONTROL Campo de referencia]** con los que establecer la relación.

   En este ejemplo, el atributo `customer` está vinculado al esquema `recipients`.

   ![](assets/schema_manual_4.png){zoomable="yes"}

1. Introduzca un Nombre de relación del esquema actual y del esquema de referencia.

1. Haga clic en **[!UICONTROL Aplicar]** una vez configurado.

Una vez establecida la relación, debe crear un conjunto de datos basado en el esquema.

## Crear un conjunto de datos para el esquema {#dataset}

Después de definir el esquema, el siguiente paso es crear un conjunto de datos basado en él. Este conjunto de datos almacena los datos ingeridos y debe estar habilitado para que las campañas organizadas puedan acceder a él en Adobe Journey Optimizer. Al habilitar esta opción, se garantiza que el conjunto de datos se reconozca para su uso en flujos de trabajo de orquestación y personalización en tiempo real.

1. Vaya al menú **[!UICONTROL Administración de datos]** > **[!UICONTROL Conjuntos de datos]** y haga clic en **[!UICONTROL Crear conjunto de datos]**.

   ![](assets/schema_manual_5.png){zoomable="yes"}

1. Seleccione **[!UICONTROL Crear conjunto de datos a partir del esquema]**.

1. Elija el esquema creado anteriormente, aquí **Pertenencias de fidelización**, y haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/schema_manual_6.png){zoomable="yes"}

1. Escriba un **[!UICONTROL Nombre]** para su **[!UICONTROL Conjunto de datos]** y haga clic en **[!UICONTROL Finalizar]**.

1. Habilite la opción **Campañas orquestadas** para que el conjunto de datos esté disponible para usar en sus campañas de AJO.

   La activación puede tardar unos minutos. La ingesta de datos solo es posible después de que la opción esté completamente activada.

   ![](assets/schema_manual_7.png){zoomable="yes"}

Ahora puede empezar a introducir datos en el esquema utilizando el origen de su elección.

➡️ [Aprenda a ingerir datos](ingest-data.md)
