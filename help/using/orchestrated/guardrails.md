---
solution: Journey Optimizer
product: journey optimizer
title: Limitaciones y protecciones de campañas organizadas
description: Obtenga información acerca de las limitaciones y protecciones de campañas orquestadas
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/ViPJaOPo-AT-naQqq-PaPw-BI5YupYuYAEy56AUEp2A
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
topic_v2:
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 534
ht-degree: 3%

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

* No se pueden habilitar los esquemas relacionales para los **perfiles** de Adobe Experience Platform. Solo se admiten esquemas XDM estándar para **Perfiles** de Adobe Experience Platform. Los esquemas relacionales se pueden habilitar para campañas organizadas o campañas de acción. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/catalog/datasets/user-guide#enable-profile)

### Ingesta de datos {#data-ingestion}

* Se requiere la ingesta de datos relacionales y de perfil.

* Toda la ingesta debe realizarse a través de **Cambiar captura de datos** orígenes:

   * Para **basado en archivos**: se requiere el campo `_change_request_type`. Los valores admitidos son `u` (actualizado) o `d` (eliminado). Estos valores deben estar en minúsculas `u` y `d`, no en mayúsculas `U` y `D`.

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

En las campañas organizadas solo se admiten canales de SMS, push, de correo electrónico y de correo directo.
