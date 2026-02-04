---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los retos de fidelización
description: Aprenda a crear y administrar desafíos de lealtad en Adobe Journey Optimizer para crear programas de lealtad atractivos.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privada" type="Informative"
source-git-commit: 5120eb51311348b8561b0a20f982576f6c945921
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---


# Introducción a los retos de fidelización {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* **Introducción a los retos de fidelización** ◀︎ **Está aquí**: información general, flujo de trabajo, requisitos previos
* [Desafíos de fidelidad de acceso](access-loyalty-challenges.md): inventario y filtrado
* [Crear desafíos](create-challenges.md) - Generar y configurar desafíos
* [Crear tareas](create-tasks.md) - Definir tareas de desafío
* [Administrar desafíos](manage-challenges.md): editar, supervisar y optimizar

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Para solicitar acceso, póngase en contacto con su representante de Adobe. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

## Información general {#overview}

Los Desafíos de fidelidad proporcionan una solución completa para crear programas de fidelidad a escala, desde la definición de tareas e hitos hasta la entrega de contenido y el seguimiento del rendimiento en todos los canales.

Puede crear tres tipos de experiencias de desafío:

* **Desafíos estándar**: Los clientes completan cualquier número especificado de tareas en cualquier orden
* **Retos de la racha**: Los clientes completan la misma tarea varias veces consecutivamente
* **Desafíos secuenciales**: Los clientes completan las tareas en un orden definido

Con los Retos de fidelización, puede configurar recompensas, enviar notificaciones de varios canales en etapas clave del ciclo vital y monitorizar el rendimiento a través de recorridos generados automáticamente, todo mientras mantiene la integración con su sistema de administración de fidelidad externo.

<!-- SCREENSHOT: High-level diagram showing Loyalty Challenges architecture with: Data ingestion from source connectors -> Challenge creation in JO -> Content cards & messaging -> Customer device -> Journey tracking -->

## Funcionamiento {#how-it-works}

<!-- SCHEMA: Visual workflow diagram showing the 8 steps in the loyalty challenge creation process with icons for each step -->

La creación y el lanzamiento de un desafío de fidelidad siguen este flujo de trabajo:

1. **Configurar la ingesta de datos**: configure los conectores de origen de Experience Platform (como el conector Capilar) para introducir datos de evento de lealtad que hagan un seguimiento de las acciones y el progreso de los clientes. Estos datos alimentan el seguimiento de desafíos y la finalización de tareas.

1. **Crear un desafío**: defina las propiedades básicas del desafío, como nombre, tipo (Estándar, Streak o Secuencial), audiencia e intervalo de fechas. Consulte [Crear desafíos](create-challenges.md) para ver los pasos detallados.

1. **Agregar tareas**: defina las acciones específicas que deben completar los clientes, incluidos los tipos de tareas (compras, gastos, visitas, participaciones, eventos personalizados), cantidades, filtros de productos y recompensas. Consulte [Crear tareas](create-tasks.md) para obtener instrucciones detalladas.

1. **Diseñar tarjetas de contenido**: cree la representación visual de su desafío con las [tarjetas de contenido](../content-card/create-content-card.md) de Journey Optimizer que se muestran en los dispositivos del cliente. Las tarjetas de contenido muestran información de desafío, progreso y recompensas.

1. **Configurar mensajes** (opcional): configura mensajes multicanal ([en la aplicación](../in-app/get-started-in-app.md), [correo electrónico](../email/get-started-email.md), [push](../push/get-started-push.md)) para las fases clave del ciclo vital: inicio, en curso y finalización.

1. **Revisar y publicar**: pruebe el desafío con [perfiles de prueba](../content-management/test-profiles.md) y publíquelo para que esté disponible para la audiencia de destino.

1. **Activar recorrido**: cuando publica un desafío, Journey Optimizer crea automáticamente un [recorrido](../building-journeys/journey-gs.md) en estado de Borrador que organiza la entrega y la mensajería de la tarjeta de contenido. Vaya al inventario de Recorridos, busque el recorrido generado automáticamente (denominado &quot;Desafío: [Nombre del desafío]&quot;) y [actívelo](../building-journeys/publish-journey.md) para que el desafío esté disponible para sus clientes.

1. **Monitorizar el rendimiento**: haga un seguimiento de la participación, las tasas de finalización, la distribución de recompensas y la participación en los mensajes mediante informes integrados y el lienzo de recorrido. Consulte [Administrar desafíos](manage-challenges.md) para obtener detalles de supervisión.

## Requisitos previos {#prerequisites}

Antes de usar Desafíos de fidelización, asegúrese de lo siguiente:

+++Configuración de ingesta de datos

Los retos de fidelización dependen de los datos introducidos a través de los conectores de origen de Experience Platform para rastrear el progreso de los clientes y la finalización de las tareas.

1. **Configurar un conector de origen admitido**: actualmente, el conector Capillary está disponible de forma general. Se han planificado conectores adicionales para futuras versiones.

1. **Validar la ingesta de datos**: Asegúrese de que los eventos de lealtad y los datos de clientes fluyen a Experience Platform y están disponibles en Journey Optimizer. Compruebe que el esquema de datos incluye los campos necesarios para rastrear las acciones de los clientes y el progreso.

Para obtener instrucciones detalladas, consulte:

* [Documentación de fuentes de Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Configuración de conectores de origen en Journey Optimizer](../start/get-started-sources.md)

+++

+++Permisos necesarios

Para utilizar Desafíos de fidelización, necesita los permisos adecuados en Journey Optimizer. Los permisos obligatorios incluyen:

* Acceso a la función **[!UICONTROL Retos de fidelización]**
* Permisos para crear y administrar recorridos
* Permisos para crear y administrar tarjetas de contenido
* Permisos para crear y administrar audiencias

Póngase en contacto con el administrador si no puede acceder a la función o necesita permisos adicionales.

+++

+++Públicos destinatarios

Cree audiencias de destino en Experience Platform antes de crear desafíos. Estas audiencias definen qué clientes pueden participar en los desafíos de fidelidad. Para obtener más información sobre cómo crear audiencias, consulte [Introducción a las audiencias](../audience/about-audiences.md).

+++

## Próximos pasos {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Desafíos de fidelidad de acceso</strong></a>
    </div>
    <p>
    <em>Aprenda a acceder al inventario y filtrar los desafíos</em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <!--<img alt="Create" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-challenges.md"><strong>Crear desafíos</strong></a>
    </div>
    <p>
    <em>Cree y configure su primer desafío de fidelidad</em>
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
    <!--<img alt="Tasks" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-tasks.md"><strong>Crear tareas</strong></a>
    </div>
    <p>
    <em>Defina acciones y recompensas para los desafíos</em>
    </p>
  </td>
  <td>
    <a href="manage-challenges.md">
    <!--<img alt="Manage" src="../assets/do-not-localize/monitor-button.svg">-->
    </a>
    <div>
    <a href="manage-challenges.md"><strong>Administrar desafíos</strong></a>
    </div>
    <p>
    <em>Editar, supervisar y optimizar desafíos</em>
    </p>
  </td>
</tr>
</table>
