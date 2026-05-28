---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Cargar archivo
description: Aprenda a utilizar la actividad Cargar archivo para dirigirse a una audiencia de campaña organizada desde un archivo CSV o TXT sin ingerir el archivo en Adobe Experience Platform
exl-id: a7c3e891-4f2d-4b8e-9c1a-6e8f0d3b2a41
version: Campaign Orchestration
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 1234
ht-degree: 2%

---

# Carga de archivo {#load-file}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_load_file"
>title="Actividad Cargar archivo"
>abstract="La actividad **Cargar archivo** es una actividad **Administración de datos**. Utilícelo para trabajar con perfiles y datos almacenados en un archivo externo en el lienzo de Campaign Orchestrated y definir la audiencia de Campaign. Los datos del archivo se consumen en el momento de la ejecución y no se conservan como un conjunto de datos de Adobe Experience Platform."

La actividad **[!UICONTROL Cargar archivo]** es una actividad **[!UICONTROL Administración de datos]**. Utilícela para trabajar con perfiles y datos almacenados en un archivo externo. Admite **segmentación basada en archivos** en campañas orquestadas cuando la lista de destinatarios proviene de un sistema externo (por ejemplo, una exportación de CRM o un archivo de socio) y desea ejecutar una campaña sin crear primero una canalización de ingesta de Adobe Experience Platform completa.

>[!AVAILABILITY]
>
>La actividad **Cargar archivo** está disponible en **Disponibilidad limitada** para un conjunto de organizaciones. Para solicitar acceso, póngase en contacto con su representante de Adobe. Para ver las fases de disponibilidad, consulte [Ciclo de la versión de Journey Optimizer](../../rn/releases.md).
>
>Actualmente, la actividad no está disponible para usarla con **Healthcare Shield**.

## Mecanismos de protección y limitaciones {#limitations}

Las siguientes limitaciones se aplican a la actividad Cargar archivo:

* Puede cargar hasta 50 MB por archivo.
* Solo se admiten archivos CSV y TXT de estructura plana.
* Los datos cargados se utilizan cuando se ejecuta la campaña y no se almacenan como un conjunto de datos de Adobe Experience Platform.

Para ver los límites en las actividades de canal y lienzo, consulte [Protecciones y limitaciones](../guardrails.md#activities-limitations).

## Configuración de la actividad Cargar archivo {#load-file-configuration}

Configure la actividad en dos partes: defina la estructura de archivos esperada con un archivo de muestra y, a continuación, especifique el archivo que se cargará cuando se ejecute la campaña.

1. Agregue una actividad **[!UICONTROL Cargar archivo]** al lienzo de la campaña orquestada.

   ![](../assets/load-file.png)

1. Escriba una **[!UICONTROL etiqueta]** para la actividad.

### Definición del archivo de muestra {#sample-file}

Use un archivo de muestra para configurar **[!UICONTROL Columnas]** y **[!UICONTROL Formato]**. Los datos de ejemplo no se importan como audiencia de la campaña.

1. En la sección **[!UICONTROL Archivo de muestra]**, seleccione el archivo local que define la estructura esperada.

   >[!NOTE]
   >
   > El archivo de muestra se utiliza únicamente para configurar columnas y dar formato. Sus datos no se importan como audiencia de la campaña. El formato debe coincidir con los archivos que se cargarán cuando se ejecute la campaña.

1. En el menú desplegable **[!UICONTROL Tipo de archivo]**, especifique si el archivo usa **columnas delimitadas** o **columnas de ancho fijo**.

   ![](../assets/load-file-sample.png)

1. En la sección **[!UICONTROL Columnas]**, expanda cada columna y configure sus propiedades.

   ![](../assets/load-file-sample-columns.png)

   Después de seleccionar un **[!UICONTROL tipo de datos]**, aparecerán opciones adicionales para ese tipo. Expanda las secciones siguientes para ver los parámetros comunes a todas las columnas y las opciones específicas del tipo.

   +++Parámetros de columna comunes

   * **[!UICONTROL Ignorar columna]** — Excluye la columna de la importación cuando está seleccionada.
   * **[!UICONTROL Etiqueta]** — Nombre para mostrar de la columna (por ejemplo, `email`).
   * **[!UICONTROL Nombre interno]**: nombre del sistema para la columna, derivado del encabezado del archivo (solo lectura).
   * **[!UICONTROL Tipo de datos]** — Tipo de datos en la columna.
   * **[!UICONTROL Permitir valores NULL]** — Especifica cómo administrar los valores vacíos en la columna:

      * **[!UICONTROL Adobe Campaign default]**: genera un error solo para campos numéricos. De lo contrario, inserta un valor NULL.
      * **[!UICONTROL Valor vacío permitido]** — Autoriza valores vacíos. Por lo tanto, se inserta el valor NULL.
      * **[!UICONTROL Siempre rellenado]**: genera un error si un valor está vacío.

   * **[!UICONTROL Error al procesar]** — Define el comportamiento si se encuentra un error en la columna:

      * **[!UICONTROL Ignorar el valor]** — El valor se ignora.
      * **[!UICONTROL Rechazar la línea]** — No se procesa la línea completa.
      * **[!UICONTROL Usar un valor predeterminado en caso de error]**: reemplaza el valor que causa el error por un valor predeterminado definido en el campo **[!UICONTROL Valor predeterminado]**.
      * **[!UICONTROL Usar un valor predeterminado en caso de que no se reasigne el valor]**: reemplaza el valor que causa el error por un valor predeterminado, definido en el campo **[!UICONTROL Valor predeterminado]**, a menos que se haya definido una asignación para el valor incorrecto.
      * **[!UICONTROL Rechazar la línea cuando no haya ningún valor de reasignación]**: no se procesará la línea completa a menos que se haya definido una asignación para el valor erróneo.

   * **[!UICONTROL Valor predeterminado]**: valor predeterminado que se usará cuando **[!UICONTROL Error al procesar]** se establezca para usar un valor predeterminado.
   * **[!UICONTROL Reasignación de valores]**: asigne valores específicos a valores nuevos. Haga clic en **[!UICONTROL Agregar asignación]** para definir cada asignación (por ejemplo, reemplazar `True`/`False` por `1`/`0`).

   +++

   +++Parámetros de columnas de cadena

   * **[!UICONTROL Anchura]** — Número máximo de caracteres.
   * **[!UICONTROL Transformación de datos]**: transformación de mayúsculas y minúsculas aplicada a valores de cadena (por ejemplo, ninguna o mayúsculas/minúsculas).
   * **[!UICONTROL Administración de espacios en blanco]**: cómo administrar los espacios iniciales y finales en los valores de cadena.

   +++

   +++Parámetros de columnas de números enteros y números flotantes

   * **[!UICONTROL Formato]** — Define cómo se leen los valores numéricos en el archivo:

      * **[!UICONTROL Otro]** — Define el **[!UICONTROL separador de miles]** y el **[!UICONTROL separador decimal]** en la sección **[!UICONTROL Separadores]**.
      * **[!UICONTROL 1.000,00]**: coma como separador de miles y punto como separador decimal.
      * **[!UICONTROL 1 000,00]**: espacio como separador de miles y coma como separador decimal.

   * **[!UICONTROL Separadores]** (cuando **[!UICONTROL Formato]** es **[!UICONTROL Otro]**):

      * **[!UICONTROL Separador de miles]**: carácter que agrupa miles en valores numéricos (dejar vacío si no se utiliza).
      * **[!UICONTROL Separador decimal]**: carácter utilizado para la parte decimal de valores numéricos (por ejemplo, `,` o `.`).

   +++

   +++Parámetros de las columnas de fecha y hora

   Las opciones dependen de si **[!UICONTROL Tipo de datos]** es **Fecha**, **Hora** o **Fecha y hora**.

   **Fecha**

   * **[!UICONTROL Formato de fecha]** — Patrón que coincide con la forma en que aparecen las fechas en el archivo (por ejemplo, `yyyy/mm/dd`).
   * **[!UICONTROL Separadores]**:

      * **[!UICONTROL Año, mes, día]**: carácter entre los componentes año, mes y día (por ejemplo, `/`).

   **Hora**

   * **[!UICONTROL Formato de hora]**: Patrón que coincide con la forma en que aparecen las horas en el archivo (por ejemplo, `13:30` para las horas y los minutos de 24 horas).
   * **[!UICONTROL Separadores]**:

      * **[!UICONTROL Hora, minuto, segundo]**: carácter entre los componentes de hora, minuto y segundo (por ejemplo, `:`).

   **Fecha y hora**

   * **[!UICONTROL Formato de fecha]** — Patrón que coincide con la forma en que aparece la parte de fecha en el archivo.
   * **[!UICONTROL Formato de hora]** — Patrón que coincide con la forma en que aparece la parte de hora en el archivo.
   * **[!UICONTROL Separadores]**: caracteres entre componentes de fecha y hora.

   +++

1. En la sección **[!UICONTROL Formatting]**, especifique cómo se estructura el archivo para que las filas y columnas se lean correctamente cuando se ejecute la campaña. El archivo de destino debe utilizar el mismo formato que el archivo de muestra.

   ![](../assets/load-file-sample-formatting.png)

   * **[!UICONTROL Usar primera línea como encabezado de columna]**: cuando se selecciona, la primera línea del archivo se trata como nombres de columna. Esta opción suele habilitarse al configurar la muestra desde un archivo que incluye una fila de encabezado.
   * **[!UICONTROL Usar un número de línea como identificador]**: cuando se selecciona, cada fila se identifica con su número de línea en el archivo.
   * **[!UICONTROL Los registros abarcan varias líneas]**: cuando se seleccionan, un único registro puede abarcar varias líneas del archivo (por ejemplo, cuando los campos contienen saltos de línea).
   * **[!UICONTROL Líneas para omitir]**: número de líneas que se omitirán al principio del archivo antes de leer los datos (por ejemplo, líneas de comentarios o metadatos).
   * **[!UICONTROL Zona horaria]**: zona horaria aplicada cuando se importan valores de fecha y hora.
   * **[!UICONTROL Codificación]** — Codificación de caracteres del archivo. Seleccione la codificación que coincida con el archivo de origen.
   * **[!UICONTROL Delimitador de cadena]**: carácter utilizado para incluir valores de cadena en el archivo.
   * **[!UICONTROL Separador de columnas]**: carácter que separa las columnas de un archivo delimitado.

1. Haga clic en **[!UICONTROL Confirmar]** para validar la configuración del archivo de muestra.

### Definición del archivo de destino {#target-file}

Especifique el archivo que se cargará durante la ejecución de la campaña y cómo se relaciona cada fila con los destinatarios existentes.

1. En la sección **[!UICONTROL Archivo de destino]**, seleccione el archivo CSV o TXT que contiene el destino.

   ![](../assets/load-file-target.png)

   >[!CAUTION]
   >
   > Asegúrese de que el archivo de destino sigue el mismo formato, estructura de columnas y número de columnas que el archivo de muestra.

1. En la sección **[!UICONTROL Reject management]**, defina cómo se comporta la actividad cuando se producen errores durante el procesamiento del archivo:

   * **[!UICONTROL Número de errores permitidos]** — Número máximo de errores permitidos antes de que falle la actividad.
   * **[!UICONTROL Mantener rechazos en un archivo]**: cuando está habilitada, las filas que no se pudieron cargar se escriben en un archivo de rechazo del servidor para su revisión después de la ejecución.

1. De manera opcional, habilite **[!UICONTROL Eliminar archivo después de la importación]** para quitar el archivo cargado del servidor una vez que se ejecute la campaña.

Una vez que **[!UICONTROL Cargar archivo]** resuelva la audiencia, conecte la transición saliente a las actividades de flujo descendente. [Obtenga información sobre cómo organizar actividades de campaña](../orchestrate-activities.md)
