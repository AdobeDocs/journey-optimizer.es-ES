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
source-git-commit: 419c7b3913ca4da50c69ed36ffc1a8c8520607b4
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 3%

---


# Introducción a los retos de fidelización {#get-started-loyalty-challenges}

>[!AVAILABILITY]
>
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Póngase en contacto con su representante de Adobe para obtener acceso.

Los retos de fidelidad le permiten crear ofertas de participación personalizadas para sus clientes, lo que le ayuda a orquestar programas de fidelidad a escala. Puede diseñar desafíos con tareas e hitos específicos, recompensar a los clientes por completarlos y ofrecer la experiencia a través de canales de Adobe Journey Optimizer.

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* **Introducción a los retos de fidelización** ◀︎ **Ya está aquí**: información general rápida y pasos siguientes
* [Comprender los desafíos de fidelidad](get-started.md): características, flujo de trabajo, requisitos previos
* [Crear desafíos](create-challenges.md) - Generar y configurar desafíos
* [Administrar desafíos](manage-challenges.md): editar, supervisar y optimizar

>[!ENDSHADEBOX]

## Información general rápida {#quick-overview}

Utilice los retos de fidelización para:

* **Crear tres tipos de desafíos**: estándar (cualquier tarea), de Streak (tareas repetidas) o secuenciales (tareas ordenadas)
* **Diseño de contenido de desafío**: use tarjetas de contenido para mostrar los desafíos en los dispositivos de los clientes
* **Configurar requisitos de tareas**: defina acciones como compras, visitas o eventos personalizados con recompensas
* **Enviar notificaciones multicanal**: Envíe mensajes a través de la aplicación, el correo electrónico y la notificación push en las fases clave
* **Rastrear rendimiento**: supervisar mediante recorridos autogenerados e informes integrados

## Funcionamiento {#how-it-works-overview}

La creación de un desafío de fidelidad sigue este flujo de trabajo:

1. **Configurar la ingesta de datos** - Configurar conectores de origen para rastrear acciones de clientes
2. **Crear un desafío** - Definir tipo, audiencia y fechas
3. **Agregar tareas** - Configurar acciones y recompensas
4. **Diseñar contenido** - Crear tarjetas de contenido y mensajes opcionales
5. **Publicar**: Journey Optimizer genera y activa automáticamente un recorrido
6. **Monitor** - Rastrear participación y rendimiento

>[!NOTE]
>
>El recorrido generado automáticamente aparece en el inventario de recorridos y se puede personalizar si es necesario. Sin embargo, los cambios realizados directamente en el recorrido no se sincronizan con la configuración de desafío.

## Requisitos previos {#prerequisites-overview}

Antes de usar Desafíos de fidelización:

* Configure los conectores de origen de Experience Platform (por ejemplo, Capilar) para introducir datos de evento de lealtad
* Asegúrese de que tiene los permisos adecuados en Journey Optimizer
* Creación de audiencias de destino en Experience Platform

Para conocer los requisitos previos detallados, consulte [Comprender los desafíos de fidelidad](get-started.md#prerequisites).

## Limitaciones importantes {#limitations-overview}

* **Sin sistema de contabilidad**: Los retos de fidelización no hacen un seguimiento de los valores monetarios ni de los saldos de puntos. Journey Optimizer llama a su sistema de administración de lealtad externo para administrar la asignación de puntos.
* **Solo selección de audiencias**: puede seleccionar audiencias existentes, pero no puede crear nuevas audiencias desde la interfaz de usuario de Desafíos de fidelización.

## Próximos pasos {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="get-started.md">
    <img alt="Comprender" src="../assets/do-not-localize/learn-more-button.svg">
    </a>
    <div>
    <a href="get-started.md"><strong>Comprender los desafíos de fidelidad</strong></a>
    </div>
    <p>
    <em>Obtenga información acerca de características, flujo de trabajo y capacidades</em>
    <p>
  </td>
  <td>
    <a href="create-challenges.md">
      <img alt="Crear" src="../assets/do-not-localize/start-button.svg">
    </a>
    <div>
    <a href="create-challenges.md"><strong>Crear desafíos</strong></a>
    </div>
    <p>
    <em>Cree y configure su primer desafío de fidelidad</em>
    <p>
  </td>
  <td>
    <a href="manage-challenges.md">
    <img alt="Administrar" src="../assets/do-not-localize/monitor-button.svg">
    </a>
    <div>
    <a href="manage-challenges.md"><strong>Administrar desafíos</strong></a>
    </div>
    <p>
    <em>Editar, supervisar y optimizar desafíos</em>
    <p>
  </td>
</tr>
</table>
