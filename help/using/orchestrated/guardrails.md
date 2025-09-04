---
solution: Journey Optimizer
product: journey optimizer
title: Limitaciones y protecciones de campañas organizadas
description: Obtenga información acerca de las limitaciones y protecciones de campañas orquestadas
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---


# Protecciones y limitaciones {#guardrails}

A continuación, encontrará limitaciones y protecciones adicionales al utilizar campañas orquestadas.

## Limitaciones de flujo de datos

### Diseño y almacenamiento de datos

* El almacén de datos relacional admite un máximo de **200 tablas** (esquemas).

* Para campañas orquestadas, el tamaño total de cualquier esquema individual **no debe exceder los 100 GB**.

* Las actualizaciones diarias de un esquema deben estar **limitadas a menos del 20%** de su recuento total de registros para mantener el rendimiento y la estabilidad.

* Los datos relacionales son el modelo principal admitido para los casos de uso de ingesta, modelado de datos y segmentación.

* Los esquemas utilizados para la segmentación deben contener al menos **un campo de identidad de tipo`String`**, asignado a un área de nombres de identidad definida.

### Ingesta de datos

* Se requiere la ingesta de datos relacionales y de perfil.

* Toda la ingesta debe realizarse a través de **Cambiar captura de datos** orígenes:

   * Para **basado en archivos**: se requiere el campo `_change_request_type`.

   * Para **basado en la nube**: debe habilitarse el registro de tablas.

* **No se admiten actualizaciones directas en Snowflake o conjuntos de datos**. El sistema es de solo lectura, todos los cambios deben aplicarse mediante la captura de datos modificados.

* **No se admiten procesos ETL**. Los datos deben transformarse completamente al formato requerido antes de la ingesta.

* **No se permiten actualizaciones parciales**, cada fila debe proporcionarse como un registro completo.

* La ingesta por lotes para Campaign Orchestration está limitada a **una vez cada 15 minutos**.

* La latencia de ingesta, el tiempo desde la ingesta hasta la disponibilidad en Snowflake, generalmente oscila entre **15 minutos y 2 horas**, según lo siguiente:

   * Volumen de datos

   * Concurrencia del sistema

   * Tipo de operación; por ejemplo, las inserciones son más rápidas que las actualizaciones

### Modelado de datos

* Todos los esquemas, incluidas las tablas de hechos, deben incluir **un descriptor de versión** para garantizar el control de versiones y la trazabilidad adecuados.

* Cada tabla debe tener una **clave principal** definida para admitir la integridad de los datos y las operaciones de flujo descendente.

* El `table_name` asignado durante la creación del conjunto de datos es permanente y se utiliza en todas las funciones de segmentación y personalización.

* **No se admiten los grupos de campos** en el marco de modelado de datos actual.

## Limitaciones de actividades

* Solo se admiten **atributos escalares** en las definiciones de audiencia; no se permiten **mapas y matrices**.

* **Las actividades de segmentación se basan principalmente en datos relacionales**. Aunque se pueden incluir datos de perfil, el uso de conjuntos de datos de perfil grandes puede afectar al rendimiento.

* Se aplican **límites en la cantidad de atributos de perfil** que se pueden usar en audiencias por lotes y de flujo continuo para mantener la eficiencia del sistema.

* **Lista de valores (LOV)** y **enumeraciones** son totalmente compatibles.

* **Las audiencias de lectura no se almacenan en caché**, cada ejecución de campaña almacena en déclencheur una evaluación de audiencia completa a partir de los datos subyacentes.

* Se recomienda **optimizar** al trabajar con definiciones de audiencia grandes o complejas para garantizar el rendimiento.

* **Las actividades de audiencias guardadas son estáticas**, y reflejan los datos disponibles en el momento de la ejecución de la campaña.

* **No se admite anexar a una actividad de audiencia guardada**. Cualquier modificación requiere una sobrescritura completa de la audiencia.

## Limitaciones de canal

En las campañas organizadas solo se admiten canales SMS, push y de correo electrónico.
