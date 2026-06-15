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
topic_v2:
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: cda41058be1eb26538f4b0ef8c7b6c3f1c01eccd
workflow-type: tm+mt
source-wordcount: 756
ht-degree: 2%

---

# Mecanismos de protección y limitaciones {#guardrails}

>[!BEGINSHADEBOX]

**En esta página:** Revise las protecciones y limitaciones que se aplican al almacenamiento de datos, la ingesta, el modelado de datos, las actividades y los canales en campañas orquestadas.

>[!ENDSHADEBOX]

A continuación, encontrará limitaciones y protecciones al utilizar campañas orquestadas.

## Limitaciones de flujo de datos

### Diseño y almacenamiento de datos

* **Máximo de tablas**: el almacén de datos relacional admite un máximo de 200 tablas (esquemas).

* **Tamaño del esquema**: para las campañas orquestadas, el tamaño total de cualquier esquema individual no debe exceder los 100 GB.

* **Volumen de actualización diaria**: las actualizaciones diarias de un esquema deben estar limitadas a menos del 20% del recuento total de registros para mantener el rendimiento y la estabilidad.

* **Modelo de datos relacional**: los datos relacionales son el modelo principal admitido para los casos de uso de ingesta, modelado de datos y segmentación.

* **Campo de identidad**: los esquemas utilizados para la segmentación deben contener al menos un campo de identidad de tipo `String`, asignado a un área de nombres de identidad definida.

* **Atributos por esquema**: el número promedio de atributos por esquema no debe exceder las 50 columnas para mantener la capacidad de administración y el rendimiento.

* **Habilitación de perfiles**: no se pueden habilitar esquemas relacionales para perfiles de Adobe Experience Platform. Solo se admiten esquemas XDM estándar para perfiles de Adobe Experience Platform. Los esquemas relacionales se pueden habilitar para campañas organizadas o campañas de acción. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/catalog/datasets/user-guide#enable-profile)

### Ingesta de datos {#data-ingestion}

* **Ingesta relacional y de perfil**: se requiere la ingesta de datos relacionales + de perfil.

* **Cambiar fuentes de captura de datos**. Toda la ingesta debe realizarse mediante Cambiar fuentes de captura de datos:

   * **Fuentes basadas en archivos** - El campo `_change_request_type` es obligatorio. Los valores admitidos son `u` (actualizado) o `d` (eliminado). Estos valores deben estar en minúsculas `u` y `d`, no en mayúsculas `U` y `D`.

   * **Fuentes basadas en la nube**: el registro de tablas debe estar habilitado.

* **Solo registros completos**: no se permiten actualizaciones parciales de registros; cada fila debe proporcionarse como un registro completo.

* **Frecuencia de ingesta por lotes**. La ingesta por lotes para Campaign Orchestration está limitada a una vez cada 15 minutos.

* **Latencia de ingesta**: la latencia de ingesta en el almacén relacional suele oscilar entre 15 minutos y 2 horas, en función de:

   * Volumen de datos

   * Concurrencia del sistema

   * Tipo de operación (por ejemplo, las inserciones son más rápidas que las actualizaciones)

* **Relación entre el flujo de datos y el conjunto de datos**: la relación entre el flujo de datos y el conjunto de datos es 1-1. Solo una fuente puede alimentar un conjunto de datos a la vez. Para cambiar la fuente, elimine el flujo de datos existente y cree un nuevo flujo de datos con la nueva fuente.

### Modelado de datos

* **Descriptor de versión**: todos los esquemas, incluidas las tablas de hechos, deben incluir un descriptor de versión para garantizar un control de versión y una trazabilidad adecuados.

* **Clave principal**: cada tabla debe tener una clave principal definida para admitir la integridad de los datos y las operaciones de flujo descendente.

* **Nombre de tabla permanente**: `table_name` asignado durante la creación del conjunto de datos es permanente y se utiliza en las características de segmentación y personalización.

* **Grupos de campos**: los grupos de campos no se admiten en el marco de trabajo de modelado de datos actual.

* **Claves principales compuestas**: la compatibilidad con claves principales compuestas con flujos de carga de archivos no está disponible en este momento.

## Limitaciones de actividades {#activities-limitations}

* **Límite de actividades de canal**: una campaña organizada admite un máximo de 10 actividades de canal (correo electrónico, SMS, push o correo directo). Solo las actividades de canal cuentan para este límite. Las actividades de segmentación y control de flujo no cuentan (por ejemplo, Generar audiencia, Esperar, Dividir, Enriquecimiento, Reconciliación, Bifurcación, Fin o Prueba).

  Si se supera el límite al guardar o publicar, se produce un error en la operación. Para permanecer dentro del límite, reduzca el número de actividades de canal o la entrega de mensajes divididos en varias campañas orquestadas.

* **Límite de actividades de lienzo**: el número de actividades en un lienzo de campaña orquestado está limitado a 500. Este límite se aplica a todos los tipos de actividades en el lienzo. Es independiente del límite de actividades de canal que se aplica en la publicación. Para mantener la capacidad y el rendimiento, mantenga los flujos de trabajo por debajo de 100 actividades en la práctica.

* **Solo atributos escalares**: en las definiciones de audiencia solo se admiten atributos escalares; no se permiten asignaciones y matrices.

* **Datos relacionales para la segmentación**: las actividades de segmentación se basan principalmente en datos relacionales. Aunque se pueden incluir datos de perfil, el uso de conjuntos de datos de perfil grandes puede afectar al rendimiento.

* **Límites de atributos de perfil**: se aplican límites al número de atributos de perfil que se pueden usar en audiencias por lotes y de flujo continuo para mantener la eficacia del sistema.

* **Enumeraciones**: las enumeraciones son totalmente compatibles.

* **Leer audiencias no almacenadas en caché**: las audiencias leídas no se almacenan en caché; cada ejecución de campaña almacena en déclencheur una evaluación de audiencia completa a partir de los datos subyacentes.

* **Optimización de audiencias**: se recomienda usar la optimización cuando se trabaja con definiciones de audiencia grandes o complejas para garantizar el rendimiento.

* **Las audiencias guardadas son estáticas**. Las actividades de audiencia guardadas son estáticas; reflejan los datos disponibles en el momento de la ejecución de la campaña.

* **No se anexó a la audiencia guardada**. No se admite anexar a una actividad de audiencia guardada. Cualquier modificación requiere una sobrescritura completa de la audiencia.

## Limitaciones de canal

En las campañas organizadas solo se admiten canales de SMS, push, de correo electrónico y de correo directo.
