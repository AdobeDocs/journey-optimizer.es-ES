---
solution: Journey Optimizer
product: journey optimizer
title: Pasos de configuración
description: Aprenda a crear esquemas basados en modelos directamente a través de la interfaz de usuario.
exl-id: 8c785431-9a00-46b8-ba54-54a10e288141
version: Campaign Orchestration
source-git-commit: e189bb6a52691770655a436e45c6788d1011a8ca
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 4%

---

# Configuración de un esquema manual basado en modelos {#manual-schema}

Los esquemas basados en modelos se pueden crear directamente a través de la interfaz de usuario, lo que permite una configuración detallada de atributos, claves principales, campos de versiones y relaciones.

El ejemplo siguiente define manualmente el esquema **Pertenencias de fidelización** para ilustrar la estructura necesaria para las campañas orquestadas.

1. [Cree un esquema basado en modelos manualmente](#schema) mediante la interfaz de Adobe Experience Platform.

1. [Agregar atributos](#schema-attributes) como ID de cliente, nivel de pertenencia y campos de estado.

1. [Vincule su esquema](#link-schema) a esquemas integrados como Destinatarios para la segmentación de campañas.

1. [Cree un conjunto de datos](#dataset) basado en su esquema y actívelo para usarlo en campañas orquestadas.

1. [Introducir datos](ingest-data.md) en su conjunto de datos desde fuentes compatibles.

➡️ [Obtenga más información acerca de esquemas manuales basados en modelos en la documentación de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/ui/resources/schemas#create-manually)

## Cree su esquema {#schema}

Comience creando un nuevo esquema basado en modelos manualmente en Adobe Experience Platform. Este proceso permite definir la estructura de esquema desde cero, incluido su nombre y comportamiento.

1. Inicie sesión en Adobe Experience Platform.

1. Vaya al menú **[!UICONTROL Administración de datos]** > **[!UICONTROL Esquema]**.

1. Haga clic en **[!UICONTROL Crear esquema]**.

1. Seleccione **[!UICONTROL Basado en modelo]** como su **Tipo de esquema**.

   ![](assets/admin_schema_1.png){zoomable="yes"}

1. Elija **[!UICONTROL Crear manualmente]** para generar el esquema agregando campos manualmente.

1. Escriba su **[!UICONTROL nombre para mostrar del esquema]**.

   ![](assets/schema_manual_8.png){zoomable="yes"}

1. Haga clic en **Finalizar** para continuar con la creación del esquema.

Ahora puede empezar a añadir atributos al esquema para definir su estructura.

## Añadir atributos al esquema {#schema-attributes}

A continuación, añada atributos para definir la estructura del esquema. Estos campos representan los puntos de datos clave utilizados en campañas organizadas, como identificadores de clientes, detalles de pertenencia y fechas de actividades. Definirlos con precisión garantiza una personalización, segmentación y seguimiento fiables.

Cualquier esquema utilizado para la segmentación debe incluir al menos un campo de identidad de tipo `String` con un área de nombres de identidad asociada. Esto garantiza la compatibilidad con las capacidades de segmentación y resolución de identidades de Adobe Journey Optimizer.

+++Se admiten las siguientes funciones al crear esquemas basados en modelos en Adobe Experience Platform

* **ENUM**\
  Los campos ENUM son compatibles con la creación de esquemas manual y basada en DDL, lo que permite definir atributos con un conjunto fijo de valores permitidos.

* **Etiqueta de esquema para el control de datos**\
  El etiquetado es compatible a nivel de campo de esquema para aplicar políticas de gobernanza de datos como el control de acceso y las restricciones de uso. Para obtener más información, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es).

* **Clave compuesta**\
  Las claves principales compuestas son compatibles con las definiciones de esquema basadas en modelos, lo que permite el uso de varios campos juntos para identificar registros de forma exclusiva.

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
   * Para la ingesta de Change Data Capture (CDC), una columna especial denominada `_change_request_type` de tipo `String`, que indica el tipo de cambio de datos (por ejemplo, insertar, actualizar, eliminar) y habilita el procesamiento incremental. Tenga en cuenta que `_change_request_type` no debe formar parte del esquema de tabla, solo debe agregarse al archivo de datos durante la ingesta.

   ![](assets/schema_manual_2.png){zoomable="yes"}

1. Haga clic en **[!UICONTROL Guardar]**.

Después de crear y guardar atributos, puede vincular el esquema con otros esquemas relacionales definiendo relaciones.

## Vincular esquemas {#link-schema}

La creación de una relación entre dos esquemas permite mejorar las campañas organizadas con datos que van más allá del esquema de perfil principal.

1. En el esquema recién creado, seleccione el atributo que desee usar como vínculo y haga clic en **[!UICONTROL Agregar relación]**.

   ![](assets/schema_manual_3.png){zoomable="yes"}

1. Elija **[!UICONTROL Esquema de referencia]** y **[!UICONTROL Campo de referencia]** con los que establecer la relación.

   En este ejemplo, el atributo `customer` está vinculado al esquema `recipients`.

   ![](assets/schema_manual_4.png){zoomable="yes"}

1. Introduzca un Nombre de relación del esquema actual y del esquema de referencia.

1. Haga clic en **[!UICONTROL Aplicar]** una vez configurado.

## Crear un conjunto de datos para el esquema {#dataset}

Después de definir el esquema, ahora puede crear un conjunto de datos basado en él. El conjunto de datos almacena los datos ingeridos y debe estar habilitado para que las campañas orquestadas sean accesibles.

1. Vaya al menú **[!UICONTROL Administración de datos]** > **[!UICONTROL Conjuntos de datos]** y haga clic en **[!UICONTROL Crear conjunto de datos]**.

   ![](assets/schema_manual_5.png){zoomable="yes"}

1. Seleccione **[!UICONTROL Crear conjunto de datos a partir del esquema]**.

1. Elija el esquema creado anteriormente, aquí **Pertenencias de fidelización**, y haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/schema_manual_6.png){zoomable="yes"}

1. Escriba un **[!UICONTROL Nombre]** para su **[!UICONTROL Conjunto de datos]** y haga clic en **[!UICONTROL Finalizar]**.

Ahora debe habilitar el conjunto de datos para campañas orquestadas.

## Habilitar conjunto de datos para campañas orquestadas {#enable}

>[!CONTEXTUALHELP]
>id="ajo_oc_enable_dataset_for_oc"
>title="Campañas orquestadas"
>abstract="Después de crear el conjunto de datos, debe habilitarlo explícitamente para Campañas orquestadas. Este paso garantiza que el conjunto de datos esté disponible para la orquestación y personalización en tiempo real dentro de Adobe Journey Optimizer."


Después de crear el conjunto de datos, debe habilitarlo explícitamente para Campañas orquestadas. Este paso garantiza que el conjunto de datos esté disponible para la orquestación y personalización en tiempo real dentro de Adobe Journey Optimizer.

Consulte [Documentación de Adobe Developer](https://developer.adobe.com/journey-optimizer-apis/references/orchestrated-campaign-dataset/#tag/DatasetEnablement) para validar o habilitar la extensión de Campaign orquestada en el conjunto de datos.

1. Busque su conjunto de datos en la lista **[!UICONTROL Conjuntos de datos]**.

1. En la configuración de **[!UICONTROL Conjuntos de datos]**, habilite la opción **Campañas orquestadas** para marcar el conjunto de datos disponible para usar en sus campañas orquestadas.

   ![](assets/schema_manual_7.png){zoomable="yes"}

1. Espere unos minutos para que se complete el proceso de habilitación. Tenga en cuenta que la ingesta de datos y el uso de la campaña solo serán posibles una vez que esta configuración esté completamente activada.

Ahora puede empezar a introducir datos en el esquema utilizando el origen de su elección.

➡️ [Aprenda a ingerir datos](ingest-data.md)
