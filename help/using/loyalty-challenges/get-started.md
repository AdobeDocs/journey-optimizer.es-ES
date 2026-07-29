---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los retos de fidelización
description: Aprenda a crear y administrar desafíos de lealtad en Adobe Journey Optimizer para crear programas de lealtad atractivos y gratificantes.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1c84d9d0-cef7-4764-9f72-5428597a7203
feature_v2: []
subfeature_v2:
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: e62678a8b8aa22a56ef3a90c93e1290651198aa5
workflow-type: tm+mt
source-wordcount: 964
ht-degree: 13%

---

# Introducción a los desafíos de fidelidad {#get-started-loyalty-challenges}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_inventory"
>title="Desafíos de lealtad"
>abstract="Los desafíos de lealtad le permiten crear programas de lealtad atractivos e interactivos que impulsan el comportamiento de los clientes y profundizan las relaciones de marca. Cree desafíos que recompensen a los clientes por acciones específicas, desde hacer compras y escribir críticas hasta participar en redes sociales y recomendar a amigos."

>[!AVAILABILITY]
>
>Actualmente, Journey Optimizer Loyalty no está disponible para los clientes de Healthcare Shield y Privacy and Security Shield. La disponibilidad de Healthcare Shield y de los clientes de Privacy and Security Shield se actualizará cuando estén preparados para funciones futuras.

## Información general {#overview}

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

* **Traiga sus propios desafíos de datos** (disponibilidad restringida): El marco de desafíos (tareas y recompensas) se configura a partir de su integración de datos de Desafíos de fidelidad. La configuración, el contenido y la mensajería se configuran del mismo modo que para cualquier otro tipo de desafío.

>[!TIP]
>También puede crear y administrar desafíos de fidelidad mediante la **administración de desafíos de fidelidad** en [Habilidades de Recorrido de compañeros de CX](../start/ajo-coworker-skills.md#loyalty-challenge-management) con indicaciones de lenguaje natural para crear desafíos más rápido.

➡️ [Vea una descripción general de la característica](#video)

## Funcionamiento {#how-it-works}

El uso de Desafíos de fidelización implica tres fases amplias (configuración, ejecución y medición) que normalmente se comparten entre las funciones de administrador y profesional.

**1. Configure su programa** *(administrador)*

Antes de poder crear desafíos, un administrador configura las bases del programa: proveedores de recompensas, definiciones de eventos que asignan acciones del cliente a finalizaciones de tareas, inventario de productos y listas de exclusión. [Aprenda a configurar desafíos de lealtad](loyalty-admin.md).

**2. Autor y desafíos de inicio** *(profesional)*

Los especialistas en marketing crean desafíos al seleccionar un tipo (Estándar, Estándar, Streak, Secuencial o Traer sus propios datos), configurar opciones (audiencia, programación, reglas) y definir tareas y recompensas. Opcionalmente, pueden superar el desafío en interfaces de cara al miembro con una **tarjeta de contenido** o una **experiencia basada en código**, y configurar notificaciones de canal para momentos clave en el ciclo de vida del desafío. Una vez configurado, publica el desafío, genera el recorrido generado automáticamente y lo publica para que el desafío se ponga en marcha. [Aprenda a crear desafíos](create-challenges.md).

**3. Supervisar rendimiento** *(profesional/analista)*

Una vez que un desafío está activo, los paneles integrados de creación de informes proporcionan métricas de nivel de desafío: rendimiento de funnel de audiencia, tasas de finalización de tareas, emisión de recompensas e impacto en los ingresos. El motor de perspectivas con tecnología de IA también muestra recomendaciones contextuales para ayudar a optimizar el rendimiento del programa. [Más información acerca de los informes de lealtad](loyalty-reporting.md).

## Requisitos previos {#prerequisites}

Antes de usar Desafíos de fidelización, asegúrese de lo siguiente:

+++Permisos necesarios

Para utilizar Retos de fidelización, se le debe asignar una función de fidelización. Las funciones predeterminadas están disponibles para administradores, profesionales y analistas en la zona protegida de producción. Para los entornos limitados que no son de producción, el administrador debe crear una función personalizada con los permisos de Fidelidad necesarios.

Póngase en contacto con el administrador si no puede acceder a la función o necesita permisos adicionales. [Aprenda a configurar los permisos de los retos de fidelidad](loyalty-permissions.md).

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
    <a href="loyalty-admin.md"><strong>Configurar retos de fidelización</strong></a>
    </div>
    <p>
    <em>Configurar proveedores de recompensas, definiciones de eventos y configuraciones de organización</em>
    </p>
  </td>
</tr>
</table>

## Referencia de la API {#api-reference}

Para administrar los desafíos de fidelidad mediante programación, usa la [API de desafíos de fidelidad](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}. La API permite crear, actualizar y administrar desafíos y tareas a través de puntos de conexión REST.

## Vídeo práctico {#video}

**¿Es nuevo en los desafíos de fidelidad?** Vea esta descripción general para comprender las capacidades y ventajas:

>[!VIDEO](https://video.tv.adobe.com/v/3496441?quality=12)

