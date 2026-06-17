---
solution: Journey Optimizer
product: journey optimizer
title: Complemento de rendimiento para el rendimiento (push) unitario (entrega de mensajes)
description: Aprenda a configurar y utilizar el complemento de rendimiento para el rendimiento (push) unitario (entrega de mensajes) en Adobe Journey Optimizer.
feature: Push
topic: Content Management
role: User
level: Intermediate
exl-id: 2d0677ad-41c8-4299-a7c8-0e4f8a1716f7
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 3%

---


# Complemento de rendimiento para el rendimiento (push) unitario (entrega de mensajes) {#performance-add-on-for-throughput-push-unitary-mes}

>[!AVAILABILITY]
>
>Esta funcionalidad está disponible en **AJO26.7** (27-07-2026).

## Información general {#overview}

Adobe Journey Optimizer presenta el complemento de rendimiento **Rendimiento para el rendimiento - (push) unitario - Entrega de mensajes**, que permite a las organizaciones ofrecer experiencias de cliente más relevantes y personalizadas en todos los canales push.

En esta página se explica cómo configurar y utilizar esta función en sus campañas y recorridos.

## Requisitos previos {#prerequisites}

Antes de empezar:

* Tiene acceso a Adobe Journey Optimizer con los permisos necesarios de **Push**.
* Se ha configurado una superficie de canal push. Consulte [Configurar el canal push](../configuration/channel-surfaces.md).

## Funcionamiento {#how-it-works}

Complemento de rendimiento para el rendimiento (push) unitario: la entrega de mensajes se integra directamente con el motor de ejecución de AJO. Cuando un perfil llega a una acción push en un recorrido o campaña, la función aplica los parámetros configurados en el momento del envío.

Funcionalidades clave:

* **Personalización de nivel de perfil**: la configuración se adapta por destinatario mediante atributos de perfil y contexto.
* **Compatibilidad con Recorridos y campañas**: funciona tanto en recorridos organizados como en campañas únicas.
* **Métricas en tiempo real** — los resultados aparecen en [informes push](../reports/push-report.md).

## Configurar el complemento Rendimiento para el rendimiento {#configure}

1. En el menú de la izquierda de AJO, vaya a **Canales** > **Configuraciones push**.
1. Seleccione o cree una configuración de canal.
1. En la sección **Complemento de rendimiento para**, habilite la característica.
1. Defina los parámetros necesarios.
1. Haga clic en **Save**.

>[!NOTE]
>
>Los cambios de configuración se aplican a las nuevas ejecuciones de recorrido. Los recorridos en curso no se ven afectados.

## Temas relacionados {#related-topics}

* [Introducción a las notificaciones push](get-started-push.md)
* [Creación de una notificación push](create-push.md)
* [Notas de la versión AJO26.7](../rn/release-notes.md)
