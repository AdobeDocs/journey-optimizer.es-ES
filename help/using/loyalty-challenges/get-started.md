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
source-git-commit: e683461c6adbf45cacb30692e23927175685f9fb
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 1%

---


# Introducción a los retos de fidelización {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* **Introducción a los retos de fidelización** ◀︎ **Está aquí**: información general, flujo de trabajo, requisitos previos
* [Acceder y administrar desafíos de fidelidad](access-loyalty-challenges.md): administración de inventario, desafíos y tareas
* [Crear desafíos](create-challenges.md) - Generar y configurar desafíos
* [Crear tareas](create-tasks.md) - Definir tareas de desafío

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Para solicitar acceso, póngase en contacto con su representante de Adobe. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

## Información general {#overview}

Los Desafíos de fidelidad proporcionan una solución completa para crear programas de fidelidad a escala, desde la definición de tareas e hitos hasta la entrega de contenido y el seguimiento del rendimiento en todos los canales.

![](assets/challenges-gs.png)

Puede crear tres tipos de experiencias de desafío:

* **Desafíos estándar**: Los clientes completan cualquier número especificado de tareas en cualquier orden\
  *Ejemplo: completar 3 de 5 tareas disponibles*

* **Retos de la racha**: Los clientes completan la misma tarea varias veces consecutivamente\
  *Ejemplo: Realizar una compra en 7 días consecutivos*

* **Desafíos secuenciales**: Los clientes completan las tareas en un orden definido\
  *Ejemplo: compra → revisión → uso compartido (debe completarse en esta secuencia)*

Con los Retos de fidelización, puede configurar las recompensas y enviar notificaciones multicanal en etapas clave del ciclo vital mediante recorridos autogenerados, todo ello sin perder la integración con su sistema de administración de fidelidad externo.

## Funcionamiento {#how-it-works}

La creación y el lanzamiento de un desafío de fidelidad siguen este flujo de trabajo:

1. **Configurar la ingesta de datos** - Configurar conectores de origen de Experience Platform (como el [conector capilar](https://experienceleague.adobe.com/es/docs/experience-platform/sources/home#loyalty)) para ingerir datos de evento de lealtad que rastrean las acciones y el progreso de los clientes. Estos datos alimentan el seguimiento de desafíos y la finalización de tareas.

1. **Crear un desafío**: defina las propiedades básicas del desafío, como nombre, tipo (Estándar, Secuencial o Streak) e intervalo de fechas.

1. **Agregar tareas**: defina las acciones específicas que deben completar los clientes, incluidos los tipos de tareas (compras, gastos), cantidades, filtros de productos y recompensas.

1. **Diseñar tarjetas de contenido**: cree la representación visual de su desafío con tarjetas de contenido de Journey Optimizer que se muestran en los dispositivos del cliente. Las tarjetas de contenido muestran información de desafío, progreso y recompensas.

1. **Configurar mensajes** (opcional): configure mensajes multicanal (en la aplicación, correo electrónico, push) para las fases clave del ciclo vital: inicio, en curso y finalización.

1. **Seleccionar audiencia de destino** - Defina qué clientes pueden participar en su desafío seleccionando una audiencia de Adobe Experience Platform.

1. **recorrido de publicación**: Journey Optimizer genera automáticamente un recorrido para el desafío. Vaya al inventario de Recorridos y publique el recorrido generado automáticamente para que el desafío esté disponible para los clientes.

Para obtener instrucciones detalladas paso a paso, consulte [Crear desafíos](create-challenges.md).

## Requisitos previos {#prerequisites}

Antes de usar Desafíos de fidelización, asegúrese de lo siguiente:

+++Configuración de ingesta de datos

Los retos de fidelización dependen de los datos introducidos a través de los conectores de origen de Experience Platform para rastrear el progreso de los clientes y la finalización de las tareas.

1. **Configurar un conector de origen admitido**: actualmente, el conector Capillary está disponible. Se han planificado conectores adicionales para futuras versiones. [Más información acerca de los conectores de origen de fidelidad](https://experienceleague.adobe.com/es/docs/experience-platform/sources/home#loyalty).

1. **Validar la ingesta de datos**: Asegúrese de que los eventos de lealtad y los datos de clientes fluyen a Experience Platform y están disponibles en Journey Optimizer. Compruebe que el esquema de datos incluye los campos necesarios para rastrear las acciones de los clientes y el progreso.

Para obtener instrucciones detalladas, consulte [Resumen de fuentes de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/sources/home)

+++

+++Permisos necesarios

Para utilizar Desafíos de fidelización, necesita los permisos adecuados en Journey Optimizer. Los permisos obligatorios incluyen:

* Acceso a la función **[!UICONTROL Desafíos de fidelización (Beta)]**
* Permisos para crear y administrar recorridos
* Permisos para crear y administrar tarjetas de contenido
* Permisos para crear y administrar audiencias

Póngase en contacto con el administrador si no puede acceder a la función o necesita permisos adicionales.

+++

+++Público destinatario

Defina una audiencia de destino que especifique qué clientes pueden participar en los desafíos de fidelidad. Puede seleccionar audiencias existentes o crear nuevas directamente desde la interfaz de creación de desafíos. [Aprenda a trabajar con audiencias](../audience/about-audiences.md).

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
    <em>Definir acciones que completar para los desafíos</em>
    </p>
  </td>
</tr>
</table>
