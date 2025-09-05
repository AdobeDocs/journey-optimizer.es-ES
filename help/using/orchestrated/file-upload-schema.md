---
solution: Journey Optimizer
product: journey optimizer
title: Pasos de configuración
description: Obtenga información sobre cómo crear un esquema relacional en Adobe Experience Platform cargando un DDL
exl-id: 88eb1438-0fe5-4a19-bfb6-2968a427e9e8
version: Campaign Orchestration
source-git-commit: 35cd3aac01467b42d0cba22de507f11546f4feb9
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 52%

---


# Creación de esquemas relacionales mediante un archivo DDL {#file-upload-schema}

Defina el modelo de datos relacionales necesario para las campañas orquestadas creando esquemas como **Suscripciones de fidelización**, **Transacciones de fidelización** y **Recompensas de fidelización**. Cada esquema debe incluir una clave principal, un atributo de versiones y las relaciones adecuadas para hacer referencia a entidades como **Destinatarios** o **Marcas**.

Los esquemas se pueden crear manualmente a través de la interfaz o importar de forma masiva mediante un archivo DDL.

En esta sección se proporciona una guía paso a paso sobre cómo crear un esquema relacional en Adobe Experience Platform cargando un archivo DDL (lenguaje de definición de datos). El uso de un archivo DDL permite definir la estructura de su modelo de datos por adelantado, incluidas las tablas, los atributos, las claves y las relaciones.

1. [Cargar un archivo DDL](#ddl-upload) para crear esquemas relacionales y definir su estructura.

1. [Defina relaciones](#relationships) entre tablas en su modelo de datos.

1. [Vincular esquemas](#link-schema) para conectar los datos relacionales con entidades de perfil existentes como Destinatarios o Marcas.

1. [Ingresar datos](ingest-data.md) en su conjunto de datos desde fuentes compatibles.

## Cargar un archivo DDL{#ddl-upload}

Al cargar un archivo DDL, puede definir la estructura del modelo de datos por adelantado, incluidas tablas, atributos, claves y relaciones.

Se admiten las cargas de archivos de esquema basados en Excel. Descargue la [plantilla proporcionada](assets/template.zip) para preparar fácilmente sus definiciones de esquema.

+++Se admiten las siguientes funciones al crear esquemas relacionales en Adobe Experience Platform

* **ENUM**\
  Los campos ENUM son compatibles con la creación de esquemas manual y basada en DDL, lo que permite definir atributos con un conjunto fijo de valores permitidos.
Vea el siguiente ejemplo:

  ```
  CREATE TABLE orders (
  order_id     INT NOT NULL,
  product_id   INT NOT NULL,
  order_date   DATE NOT NULL,
  customer_id  INT NOT NULL,
  quantity     INT NOT NULL,
  order_status enum ('PENDING', 'SHIPPED', 'DELIVERED', 'CANCELLED'),
  PRIMARY KEY (order_id, product_id)
  );
  ```

* **Etiqueta de esquema para el control de datos**\
  El etiquetado es compatible a nivel de campo de esquema para aplicar políticas de gobernanza de datos como el control de acceso y las restricciones de uso. Para obtener más información, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es).

* **Clave compuesta**\
  Las claves principales compuestas son compatibles con las definiciones de esquema relacional, lo que permite el uso de varios campos juntos para identificar registros de forma exclusiva.

+++

1. Inicie sesión en Adobe Experience Platform.

1. Vaya al menú **Administración de datos** > **Esquema**.

1. Haga clic en **Crear esquema**.

1. Seleccione **[!UICONTROL Relacional]** como su **Tipo de esquema**.

   ![](assets/admin_schema_1.png)

1. Seleccione **[!UICONTROL Cargar archivo DDL]** para definir un diagrama de relación de entidades y crear esquemas.

   La estructura de la tabla debe contener:
   * Al menos una clave principal.
   * Un identificador de versión, como un campo de tipo `lastmodified`, `datetime` o `number`.
   * Para la ingesta de Change Data Capture (CDC), una columna especial denominada `_change_request_type` de tipo `String`, que indica el tipo de cambio de datos (por ejemplo, insertar, actualizar, eliminar) y habilita el procesamiento incremental.
   * El archivo DDL no debe definir más de 200 tablas.


   >[!IMPORTANT]
   >
   > Cualquier esquema usado para la segmentación debe incluir al menos un campo de identidad de tipo `String` con un **área de nombres de identidad** asociado.\
   >Esto garantiza la compatibilidad con las capacidades de segmentación y resolución de identidades de Adobe Journey Optimizer.

1. Arrastre y suelte su archivo DDL y haga clic en **[!UICONTROL Siguiente]**.

   Tenga en cuenta que el tamaño máximo admitido para un archivo DDL es de 10 MB.

1. Escriba su **[!UICONTROL Nombre de esquema]**.

1. Configure cada esquema y sus columnas, asegurándose de especificar una clave principal.

   Un atributo, como `lastmodified`, debe designarse como descriptor de versión (tipo `datetime`, `long` o `int`) para garantizar que los conjuntos de datos se actualicen con los datos más recientes. Los usuarios pueden cambiar el descriptor de versión, que se vuelve obligatorio una vez configurado. Un atributo no puede ser a la vez una clave principal (PK) y un descriptor de versión.

   ![](assets/admin_schema_2.png)

1. Marque un atributo como `identity` y asígnelo a un área de nombres de identidad definida.

1. Cambie el nombre, elimine o agregue una descripción a cada tabla.

1. Haga clic en **[!UICONTROL Listo]** cuando haya finalizado.

Ahora puede comprobar las definiciones de tabla y campo dentro del lienzo. [Más información en la siguiente sección](#entities)

## Definición de relaciones {#relationships}

Para definir conexiones lógicas entre tablas dentro del esquema, siga los pasos que se indican a continuación.

1. Acceda a la vista de lienzo del modelo de datos y elija las dos tablas que desea vincular

1. Haga clic en el botón ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) junto a Unión de origen, y a continuación, arrastre y guíe la flecha hacia Unión de destino para establecer la conexión.

   >[!NOTE]
   >
   >Las claves compuestas son compatibles si se definen en el archivo DDL.

   ![](assets/admin_schema_5.png)

1. Complete el formulario proporcionado para definir el vínculo y haga clic en **Aplicar** una vez configurado.

   ![](assets/admin_schema_3.png)

   **Cardinalidad**:

   * **1-N**: una ocurrencia de la tabla de origen puede tener varias ocurrencias correspondientes de la tabla de destino, pero una ocurrencia de la tabla de destino puede tener como máximo una ocurrencia correspondiente de la tabla de origen.

   * **N-1**: una ocurrencia de la tabla de destino puede tener varias ocurrencias correspondientes de la tabla de origen, pero una ocurrencia de la tabla de origen puede tener como máximo una ocurrencia correspondiente de la tabla de destino.

   * **1-1**: una ocurrencia de la tabla de origen puede tener como máximo una ocurrencia correspondiente de la tabla de destino.

1. Todos los vínculos definidos en el modelo de datos se representan como flechas en la vista de lienzo. Haga clic en la flecha entre dos tablas para ver los detalles, realizar ediciones o quitar el vínculo según sea necesario.

   ![](assets/admin_schema_6.png)

1. Utilice la barra de herramientas para personalizar y ajustar el lienzo.

   ![](assets/toolbar.png)

   * **Aumentar**: amplíe el lienzo para ver los detalles del modelo de datos con mayor claridad.

   * **Reducir**: reduzca el tamaño del lienzo para obtener una vista más amplia del modelo de datos.

   * **Ajustar vista**: ajuste el zoom para ajustar todos los esquemas dentro del área visible.

   * **Filtro**: elija qué esquema desea mostrar en el lienzo.

   * **Forzar diseño automático**: organiza automáticamente los esquemas para mejorar la organización.

   * **Mostrar mapa**: active una superposición del minimapa para que sea más fácil navegar por diseños de esquema grandes o complejos.

1. Haga clic en **Guardar** cuando haya terminado. Esta acción crea los esquemas y los conjuntos de datos asociados y habilita el conjunto de datos para su uso en campañas organizadas.

1. Haga clic en **[!UICONTROL Abrir trabajos]** para supervisar el progreso del trabajo de creación. Este proceso puede tardar un par de minutos, según el número de tablas definidas en el archivo DDL.

   También puede acceder a sus trabajos relacionales si abre la ventana **[!UICONTROL Cargar archivo DDL]** y selecciona **[!UICONTROL Ver todos los trabajos relacionales]**.

   ![](assets/admin_schema_4.png)

## Vincular esquemas {#link-schema}

>[!IMPORTANT]
>
> El sistema solo reconoce las relaciones definidas explícitamente dentro del archivo DDL. Las relaciones de entidad que existan fuera del archivo DDL se ignorarán y no se procesarán.

Establezca una relación entre el esquema **Transacciones de lealtad** y el esquema **Destinatarios** para asociar cada transacción con el registro de cliente correcto.

1. Vaya a **[!UICONTROL Esquemas]** y abra las **Transacciones de lealtad** que creó anteriormente.

1. Haga clic en **[!UICONTROL Añadir relación]** desde las **[!UICONTROL Propiedades de campo]** del cliente.

   ![](assets/schema_1.png)

1. Seleccione **[!UICONTROL Varios a uno]** como la relación **[!UICONTROL Tipo]**.

1. Vincúlese al esquema **Destinatarios** existente.

   ![](assets/schema_2.png)

1. Escriba un **[!UICONTROL Nombre de relación del esquema actual]** y un **[!UICONTROL Nombre de relación del esquema de referencia]**.

1. Haga clic en **[!UICONTROL Aplicar]** para guardar los cambios.

Continúe creando una relación entre el esquema **recompensas por lealtad** y el esquema **Marcas** para asociar cada entrada de recompensa con la marca adecuada.

![](assets/schema_3.png)
