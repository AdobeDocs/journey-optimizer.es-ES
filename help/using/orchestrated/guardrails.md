---
solution: Journey Optimizer
product: journey optimizer
title: Limitaciones y protecciones de campañas organizadas
description: Obtenga información acerca de las limitaciones y protecciones de campañas orquestadas
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
version: Campaign Orchestration
source-git-commit: a9b790bc833b5819862bf2f3284968d81f595f28
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 2%

---


# Mecanismos de protección y limitaciones {#guardrails}

A continuación, encontrará limitaciones y protecciones al utilizar campañas orquestadas.

## Limitaciones de flujo de datos

### Diseño y almacenamiento de datos

* El almacén de datos relacional admite un máximo de **200 tablas** (esquemas).

* Para campañas orquestadas, el tamaño total de cualquier esquema individual **no debe exceder los 100 GB**.

* Las actualizaciones diarias de un esquema deben estar **limitadas a menos del 20%** de su recuento total de registros para mantener el rendimiento y la estabilidad.

* Los datos relacionales son el modelo principal admitido para los casos de uso de ingesta, modelado de datos y segmentación.

* Los esquemas utilizados para la segmentación deben contener al menos **un campo de identidad de tipo`String`**, asignado a un área de nombres de identidad definida.

* El número promedio de atributos por esquema **no debe exceder las 50 columnas** para mantener la capacidad de administración y el rendimiento.

* Los esquemas basados en modelos no se pueden habilitar para Adobe Experience Platform **Perfiles**. Solo se admiten esquemas XDM estándar para **Perfiles** de Adobe Experience Platform. Los esquemas basados en modelos se pueden habilitar para campañas organizadas o campañas de acción. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/catalog/datasets/user-guide#enable-profile)

### Ingesta de datos

* Se requiere la ingesta de datos relacionales y de perfil.

* Toda la ingesta debe realizarse a través de **Cambiar captura de datos** orígenes:

   * Para **basado en archivos**: se requiere el campo `_change_request_type`. Los valores admitidos son `U` (actualizado) o `D` (eliminado).

   * Para **basado en la nube**: debe habilitarse el registro de tablas.

* **No se permiten actualizaciones parciales de registros**, cada fila debe proporcionarse como un registro completo.

* La ingesta por lotes para Campaign Orchestration está limitada a **una vez cada 15 minutos**.

* La latencia de ingesta, en el almacén relacional, suele oscilar entre **15 minutos y 2 horas**, en función de:

   * Volumen de datos

   * Concurrencia del sistema

   * Tipo de operación; por ejemplo, las inserciones son más rápidas que las actualizaciones

* **La relación del flujo de datos con el conjunto de datos es 1-1**. Esto significa que solo una fuente puede alimentar un conjunto de datos a la vez. Para cambiar la fuente, se debe eliminar el flujo de datos existente y crear uno nuevo con la nueva fuente.

### Modelado de datos

* Todos los esquemas, incluidas las tablas de hechos, deben incluir **un descriptor de versión** para garantizar el control de versiones y la trazabilidad adecuados.

* Cada tabla debe tener una **clave principal** definida para admitir la integridad de los datos y las operaciones de flujo descendente.

* El `table_name` asignado durante la creación del conjunto de datos es permanente y se utiliza en todas las funciones de segmentación y personalización.

* **No se admiten los grupos de campos** en el marco de modelado de datos actual.

* La compatibilidad con claves principales compuestas con flujos de carga de archivos no está disponible en este momento.

## Limitaciones de actividades

* Solo se admiten **atributos escalares** en las definiciones de audiencia; no se permiten **mapas y matrices**.

* **Las actividades de segmentación se basan principalmente en datos relacionales**. Aunque se pueden incluir datos de perfil, el uso de conjuntos de datos de perfil grandes puede afectar al rendimiento.

* Se aplican **límites en la cantidad de atributos de perfil** que se pueden usar en audiencias por lotes y de flujo continuo para mantener la eficiencia del sistema.

* **Las enumeraciones** son totalmente compatibles.

* **Las audiencias de lectura no se almacenan en caché**, cada ejecución de campaña almacena en déclencheur una evaluación de audiencia completa a partir de los datos subyacentes.

* Se recomienda **optimizar** al trabajar con definiciones de audiencia grandes o complejas para garantizar el rendimiento.

* **Las actividades de audiencias guardadas son estáticas**, y reflejan los datos disponibles en el momento de la ejecución de la campaña.

* **No se admite anexar a una actividad de audiencia guardada**. Cualquier modificación requiere una sobrescritura completa de la audiencia.

## Limitaciones de canal

En las campañas organizadas solo se admiten canales SMS, push y de correo electrónico.
