---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los retos de fidelización
description: Aprenda a crear y administrar desafíos de lealtad en Adobe Journey Optimizer para crear programas de lealtad atractivos y gratificantes.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Beta privada" type="Informative"
mini-toc-levels: 1
exl-id: 1c84d9d0-cef7-4764-9f72-5428597a7203
feature_v2: []
subfeature_v2: id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 2e01cd1880b8527911376d94188d0204f7649541
workflow-type: tm+mt
source-wordcount: 911
ht-degree: 13%

---

# Introducción a los desafíos de fidelidad {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Tabla de contenido**

**[Introducción a los retos de fidelización](get-started.md)** ◀︎ **Ya está aquí**

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Crear y administrar desafíos**

* [Acceder y administrar desafíos y tareas](access-loyalty-challenges.md)
* [Crear desafíos](create-challenges.md)
* [Creación de tareas](create-tasks.md)
* [Monitorización del rendimiento del desafío de fidelidad](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configurar e integrar**

* [Configuración de desafíos de lealtad](loyalty-admin.md)
* [Datos y conjuntos de datos de fidelización](loyalty-data-and-datasets.md)
* [Referencia de API de retos de fidelización](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica se encuentra actualmente en **versión beta privada**. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](../rn/releases.md).

## Información general {#overview}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_inventory"
>title="Desafíos de lealtad"
>abstract="Los desafíos de lealtad le permiten crear programas de lealtad atractivos e interactivos que impulsan el comportamiento de los clientes y profundizan las relaciones de marca. Cree desafíos que recompensen a los clientes por acciones específicas, desde hacer compras y escribir críticas hasta participar en redes sociales y recomendar a amigos."

Los desafíos de lealtad le permiten crear programas de lealtad atractivos e interactivos que impulsan el comportamiento de los clientes y profundizan las relaciones de marca. Cree desafíos que recompensen a los clientes por acciones específicas, desde hacer compras y escribir críticas hasta participar en redes sociales y recomendar a amigos.

Con Desafíos de fidelización, puede hacer lo siguiente:

* **Diseñe tipos de desafíos flexibles**: Cree desafíos estándar, de racha o secuenciales para que coincidan con sus objetivos comerciales
* **Configurar las recompensas estratégicamente**: Entregar puntos en los hitos de la tarea o al finalizar por completo para mantener la participación
* **Personalice la experiencia**: use tarjetas de contenido y mensajes multicanal para crear experiencias de marca envolventes
* **Integre sin problemas**: Conéctese con sus proveedores de fidelidad existentes y aproveche los datos de Experience Platform
* **Rastrear automáticamente**: Supervisar el progreso del cliente mediante recorridos autogenerados sin desarrollo personalizado
* **Medir el rendimiento**: Use paneles de informes integrados para hacer un seguimiento de KPI de programa, resultados de desafío y métricas de nivel de tarea

![](assets/challenges-gs.png)

Puede crear estos tipos de experiencias de desafío:

* **Desafíos estándar**: Los clientes completan cualquier número especificado de tareas en cualquier orden. Utilice este tipo cuando desee flexibilidad y varias rutas hasta la finalización.\
  *Ejemplo: &quot;Summer Wellness Challenge&quot; (Desafío de bienestar de verano): completar 3 de 5 tareas: comprar productos de salud, compartir en medios sociales, recomendar a un amigo, escribir una opinión o asistir a un evento virtual*

* **Retos de la racha**: Los clientes completan la misma tarea varias veces consecutivamente. Utilice este tipo para fomentar un comportamiento coherente y repetido a lo largo del tiempo.\
  *Ejemplo: &quot;Coffee Lover&#39;s Week&quot; (Semana del amante del café): compra productos de café durante 7 días consecutivos para obtener un premio de bebida gratis*

* **Desafíos secuenciales**: Los clientes completan las tareas en un orden definido. Utilice este tipo para guiar a los clientes a través de un recorrido específico o proceso de incorporación.\
  *Ejemplo: &quot;Nuevo Recorrido para miembros&quot; - Regístrese para recibir correos electrónicos → Realice su primera compra → Escriba una opinión sobre el producto → Consulte a un amigo (complete este pedido exacto)*

* **Traiga sus propios desafíos de datos** (disponibilidad restringida): El marco de desafíos (tareas y recompensas) se configura a partir de su integración de datos de Desafíos de fidelidad. Puede configurar Contenido, Mensajería y Audiencia como lo haría para cualquier otro tipo de desafío.

## Funcionamiento {#how-it-works}

La creación y el lanzamiento de un desafío de fidelidad siguen este flujo de trabajo:

1. **Crear un desafío**: defina las propiedades básicas del desafío, como nombre, tipo (Estándar, Streak, Secuencial o Traer sus propios datos cuando estén disponibles) e intervalo de fechas. [Aprenda a elegir un tipo de desafío](create-challenges.md#create-the-challenge).

1. **Agregar tareas**: defina las acciones específicas que deben completar los clientes, incluidos los tipos de tareas (compras, gastos o eventos personalizados), las cantidades, los filtros de productos y las recompensas.

1. **Diseñar tarjetas de contenido**: cree la representación visual de su desafío con tarjetas de contenido de Journey Optimizer que se muestran en los dispositivos del cliente. Las tarjetas de contenido muestran información de desafío, progreso y recompensas.

1. **Configurar mensajes** (opcional): configure mensajes multicanal (en la aplicación, correo electrónico, push) para las fases clave del ciclo vital: inicio, en curso y finalización.

1. **Seleccionar audiencia de destino** - Defina qué clientes pueden participar en su desafío seleccionando una audiencia de Adobe Experience Platform.

1. **Iniciar el desafío**: publique el desafío y genere un recorrido. Journey Optimizer crea automáticamente el recorrido para el desafío. Publique el recorrido generado automáticamente para que el desafío esté disponible para los clientes.

Para obtener instrucciones detalladas paso a paso, consulte [Crear desafíos](create-challenges.md).

## Requisitos previos {#prerequisites}

Antes de usar Desafíos de fidelización, asegúrese de lo siguiente:

+++Permisos necesarios

Para utilizar Desafíos de fidelización, necesita los permisos adecuados en Journey Optimizer y Adobe Experience Platform.

**Journey Optimizer:**

* `journeys.read`
* `journeys.write`
* `journeys.delete`
* `journeys.publish`
* `journeys_events.read`
* `journeys_events.write`
* `journeys_events.delete`
* `journeys_report.read`
* `messages.read`
* `messages_report.read`

**Adobe Experience Platform:**

* `segments.read`
* `profiles.read`
* `identity_namespace.read`

Póngase en contacto con el administrador si no puede acceder a la función o necesita permisos adicionales.

+++

+++Configuración del programa de fidelización (administradores)

Los administradores configuran los proveedores de recompensas, las definiciones de eventos, el inventario de productos, las exclusiones y la configuración global en el menú **[!UICONTROL Administrador de fidelidad]**. Los especialistas en marketing que solo crean desafíos no necesitan acceder a este menú. [Aprenda a configurar desafíos de lealtad](loyalty-admin.md)

Póngase en contacto con el administrador si el menú **[!UICONTROL Administrador de fidelidad]** no está visible en el panel de navegación izquierdo.

+++

+++Público destinatario

Asegúrese de que la audiencia de destino que necesita exista en Adobe Experience Platform antes de crear el desafío. Durante la configuración del desafío, seleccionará la audiencia que define qué clientes pueden participar. [Aprenda a trabajar con audiencias](../audience/about-audiences.md).

+++

## Profundicemos {#lets-dive-deeper}

Ahora que sabe cuáles son los Desafíos de Lealtad y cómo funcionan, es hora de profundizar en los detalles. Explore los siguientes temas para acceder a la interfaz, crear su primer desafío y definir las tareas que completarán sus clientes.

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
      <img alt="Acceso" src="assets/do-not-localize/icon-access.png" width="200"/>
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Acceder y administrar retos y tareas</strong></a>
    </div>
    <p>
    <em>Aprenda a acceder al inventario y a administrar desafíos y tareas</em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <img alt="Crear" src="assets/do-not-localize/icon-challenge.png" width="200"/>
    </a>
    <div>
    <a href="create-challenges.md"><strong>Crear retos</strong></a>
    </div>
    <p>
    <em>Aprenda a crear y configurar su primer desafío de fidelidad</em>
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
      <img alt="Tareas" src="assets/do-not-localize/icon-task.png" width="200"/>
    </a>
    <div>
    <a href="create-tasks.md"><strong>Crear tareas</strong></a>
    </div>
    <p>
    <em>Aprenda a definir las tareas que completan los clientes para los desafíos</em>
    </p>
  </td>
  <td>
    <a href="loyalty-reporting.md">
      <img alt="Informes" src="assets/do-not-localize/icon-reporting.png" width="200"/>
    </a>
    <div>
    <a href="loyalty-reporting.md"><strong>Monitorización del rendimiento</strong></a>
    </div>
    <p>
    <em>Rastree KPI de programas, resultados de desafíos y métricas de tareas con paneles integrados</em>
    </p>
  </td>
  <!--
    <a href="loyalty-admin.md"><strong>Configure the loyalty program</strong></a>
  <td>
    <a href="loyalty-admin.md">
    <em>Set up reward providers, event definitions, and org settings for fulfillment</em>
    </a>
    <div>
-->
    <a href="loyalty-admin.md"><strong>Configurar desafíos de lealtad</strong></a>
    </div>
    <p>
    <em>Configurar proveedores de recompensas, definiciones de eventos y configuraciones de organización</em>
    </p>
  </td>
</tr>
</table>

## Referencia de la API {#api-reference}

Para administrar los desafíos de fidelidad mediante programación, usa la [API de desafíos de fidelidad](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}. La API permite crear, actualizar y administrar desafíos y tareas a través de puntos de conexión REST.
