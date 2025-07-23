---
solution: Journey Optimizer
product: journey optimizer
title: Pasos de configuración
description: Aprenda a crear esquemas relacionales directamente a través de la interfaz de usuario.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 8c785431-9a00-46b8-ba54-54a10e288141
source-git-commit: 6447f5d1a060037c0ceaa374db20966097585f9c
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 10%

---

# Configuración de un esquema relacional manual {#manual-schema}

+++ Índice

| Bienvenido a las campañas organizadas | Inicio de su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br><ul><li>[Introducción a esquemas y conjuntos de datos](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Creación y programación de las campañas](create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabajo con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](build-query.md)<br/><br/>[Edición de expresiones](edit-expressions.md)<br/><br/>[Resegmentación](retarget.md) | [Introducción a las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[AND-join](activities/and-join.md) - [Generar público](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades del canal](activities/channels.md) - [Combinar](activities/combine.md) - [Deduplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar público](activities/save-audience.md) - [División](activities/split.md) - [Esperar](activities/wait.md) |

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

Cualquier esquema utilizado para la segmentación debe incluir al menos un campo de identidad de tipo `String` con un área de nombres de identidad asociada. Esto garantiza la compatibilidad con las capacidades de segmentación y resolución de identidades de Adobe Journey Optimizer.

+++Se admiten las siguientes funciones al crear esquemas relacionales en Adobe Experience Platform

* **ENUM**\
  Los campos ENUM son compatibles con la creación de esquemas manual y basada en DDL, lo que permite definir atributos con un conjunto fijo de valores permitidos.

* **Etiqueta de esquema para el control de datos**\
  El etiquetado es compatible a nivel de campo de esquema para aplicar políticas de gobernanza de datos como el control de acceso y las restricciones de uso. Para obtener más información, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es).

* **Clave compuesta**\
  Las claves principales compuestas son compatibles con las definiciones de esquema relacional, lo que permite el uso de varios campos juntos para identificar registros de forma exclusiva.

+++

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

   Al crear un esquema manual, asegúrese de que se incluyen los siguientes campos esenciales:

   * Al menos una clave principal
   * Un identificador de versión, como un campo de tipo `lastmodified`, `datetime` o `number`.
   * Para la ingesta de Change Data Capture (CDC), una columna especial denominada `_change_request_type` de tipo `String`, que indica el tipo de cambio de datos (por ejemplo, insertar, actualizar, eliminar) y habilita el procesamiento incremental.

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

Ahora debe habilitar el conjunto de datos para las campañas de orquestación.

## Habilitar conjunto de datos para campañas orquestadas {#enable}

Después de crear el conjunto de datos, debe habilitarlo explícitamente para Campañas orquestadas. Este paso garantiza que el conjunto de datos esté disponible para la orquestación y personalización en tiempo real dentro de Adobe Journey Optimizer.

1. Busque su conjunto de datos en la lista **[!UICONTROL Conjuntos de datos]**.

1. En la configuración de **[!UICONTROL Conjuntos de datos]**, habilite la opción **Campañas orquestadas** para que el conjunto de datos esté disponible para usar en sus campañas orquestadas.

   ![](assets/schema_manual_7.png){zoomable="yes"}

1. Espere unos minutos para que se complete el proceso de habilitación. Tenga en cuenta que la ingesta de datos y el uso de la campaña solo serán posibles una vez que esta configuración esté completamente activada.

Ahora puede empezar a introducir datos en el esquema utilizando el origen de su elección.

➡️ [Aprenda a ingerir datos](ingest-data.md)
