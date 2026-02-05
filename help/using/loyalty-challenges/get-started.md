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
mini-toc-levels: 2
source-git-commit: f50cc244f6d5ec8b38844e8240e72502ddfe3ae0
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 1%

---


# Introducción a los retos de fidelización {#get-started-loyalty-challenges}

>[!AVAILABILITY]
>
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Para solicitar acceso, póngase en contacto con su representante de Adobe. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* **Introducción a los retos de fidelización** ◀︎ **Está aquí**: información general, flujo de trabajo, requisitos previos
* [Acceder y administrar desafíos y tareas](access-loyalty-challenges.md): administración de inventario, desafíos y tareas
* [Crear desafíos](create-challenges.md) - Generar y configurar desafíos
* [Crear tareas](create-tasks.md) - Definir tareas de desafío

>[!ENDSHADEBOX]

## Información general {#overview}

Los retos de fidelidad le permiten crear programas de fidelidad atractivos y con interacción que impulsan el comportamiento de los clientes y profundizan las relaciones de marca. Cree desafíos que recompensen a los clientes por acciones específicas, desde hacer compras y escribir críticas hasta interactuar en medios sociales y hacer referencia a amigos.

Con Desafíos de fidelización, puede hacer lo siguiente:

* **Diseñe tipos de desafíos flexibles**: Cree desafíos estándar, de racha o secuenciales para que coincidan con sus objetivos comerciales
* **Configurar las recompensas estratégicamente**: Entregar puntos en los hitos de la tarea o al finalizar por completo para mantener la participación
* **Personalice la experiencia**: use tarjetas de contenido y mensajes multicanal para crear experiencias de marca envolventes
* **Integre sin problemas**: Conéctese con sus proveedores de fidelidad existentes y aproveche los datos de Experience Platform
* **Rastrear automáticamente**: Supervisar el progreso del cliente mediante recorridos autogenerados sin desarrollo personalizado

![](assets/challenges-gs.png)

Puede crear tres tipos de experiencias de desafío:

* **Desafíos estándar**: Los clientes completan cualquier número especificado de tareas en cualquier orden. Utilice este tipo cuando desee flexibilidad y varias rutas hasta la finalización.\
  *Ejemplo: &quot;Summer Wellness Challenge&quot; (Desafío de bienestar de verano): completar 3 de 5 tareas: comprar productos de salud, compartir en medios sociales, recomendar a un amigo, escribir una opinión o asistir a un evento virtual*

* **Retos de la racha**: Los clientes completan la misma tarea varias veces consecutivamente. Utilice este tipo para fomentar un comportamiento coherente y repetido a lo largo del tiempo.\
  *Ejemplo: &quot;Coffee Lover&#39;s Week&quot; (Semana del amante del café): compra productos de café durante 7 días consecutivos para obtener un premio de bebida gratis*

* **Desafíos secuenciales**: Los clientes completan las tareas en un orden definido. Utilice este tipo para guiar a los clientes a través de un recorrido específico o proceso de incorporación.\
  *Ejemplo: &quot;Nuevo Recorrido para miembros&quot; - Regístrese para recibir correos electrónicos → Realice su primera compra → Escriba una opinión sobre el producto → Consulte a un amigo (complete este pedido exacto)*

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

Antes de empezar, configure un conector de origen compatible. Actualmente, el conector capilar está disponible. Se han planificado conectores adicionales para futuras versiones. [Más información acerca de los conectores de origen de fidelidad](https://experienceleague.adobe.com/es/docs/experience-platform/sources/home#loyalty).

+++

<!--+++Required permissions

To use Loyalty Challenges, you need appropriate permissions in Journey Optimizer. Required permissions include:

TBD

Contact your administrator if you cannot access the feature or need additional permissions.

+++-->

+++Público destinatario

Asegúrese de que la audiencia de destino que necesita exista en Adobe Experience Platform antes de crear el desafío. Durante la configuración del desafío, seleccionará la audiencia que define qué clientes pueden participar. [Aprenda a trabajar con audiencias](../audience/about-audiences.md).

+++

## Próximos pasos {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Acceder y administrar desafíos y tareas</strong></a>
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
    <em>Aprenda a crear y configurar su primer desafío de fidelidad</em>
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
    <em>Aprenda a configurar las acciones que completan los clientes para los desafíos</em>
    </p>
  </td>
</tr>
</table>
