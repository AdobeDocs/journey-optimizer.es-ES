---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los recorridos
description: Introducción a los recorridos
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: recorrido, descubrimiento, introducción
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 100%

---


# Introducción a los recorridos{#jo-general-principle}

Utilice [!DNL Journey Optimizer] para crear casos de uso de orquestación en tiempo real aprovechando los datos contextuales almacenados en eventos o fuentes de datos.

Diseñe escenarios avanzados de varios pasos con las siguientes capacidades:

* Envíe en tiempo real un **envío unitario** que se activa cuando se recibe un evento, o **en lote** con los públicos de Adobe Experience Platform.

* Aprovechar **datos contextuales** desde eventos, información de Adobe Experience Platform o datos de servicios API de terceros.

* Utilice las **acciones integradas** para enviar los mensajes diseñados en [!DNL Journey Optimizer] o crear **acciones personalizadas** si utiliza un sistema de terceros para enviar mensajes.

* Con el **diseñador de recorridos**, genere sus casos de uso de varios pasos: arrastre y suelte fácilmente un evento de entrada o una actividad de lectura de público, agregue condiciones y envíe mensajes personalizados.


>[!NOTE]
>
>En [esta página](../start/guardrails.md) se detallan los mecanismos de protección y limitaciones de los recorridos

## Pasos para crear un recorrido{#steps-journey}

Utilice Adobe Journey Optimizer para diseñar y organizar recorridos personalizados desde un solo lienzo. Los pasos principales para crear un recorrido son los siguientes:

![](assets/journey-creation-process.png)

Adobe Journey Optimizer incluye un lienzo de orquestación omnicanal que permite a los expertos en marketing armonizar el alcance del marketing con la participación individual del cliente. La interfaz de usuario permite arrastrar y soltar fácilmente actividades de la paleta en el lienzo para crear el recorrido.

![](assets/interface-journeys.png)

Aprenda a iniciar y crear el primer recorrido en [esta página](journey-gs.md).

El diseñador de recorridos omnicanal le ayuda a crear recorridos de varios pasos con públicos destinatarios, actualizaciones basadas en interacciones comerciales o de clientes en tiempo real y mensajes omnicanal mediante una interfaz intuitiva de arrastrar y soltar.

![](assets/journey38.png)

Obtenga más información en [esta sección](using-the-journey-designer.md).

Como ingeniero de datos, los pasos para configurar sus recorridos, incluidas las fuentes de datos, los eventos y las acciones, se detallan en [esta sección](../configuration/about-data-sources-events-actions.md).


## Casos de uso{#uc-journey}

Obtenga información sobre cómo crear recorridos en los siguientes casos de uso de extremo a extremo.

Casos de uso empresariales:

* [Envío de mensajes multicanal](journeys-uc.md)
* [Envío de un mensaje mediante Campaign v7/v8](ajo-ac.md)
* [Envío de un mensaje a los suscriptores](message-to-subscribers-uc.md)

Casos de uso técnicos:

* [Paso de colecciones de forma dinámica mediante acciones personalizadas](collections.md)
* [Aumento de envíos](ramp-up-deliveries-uc.md)
* [Limitación del rendimiento con fuentes de datos externas y acciones personalizadas](limit-throughput.md)

## Versiones de recorridos{#journey-versions}

En la lista de recorridos, todas las versiones del recorrido se muestran con el número de versión. Consulte [esta página](../building-journeys/using-the-journey-designer.md).

Cuando busca un recorrido, las versiones más recientes aparecen en la parte superior de la lista la primera vez que se abre la aplicación. A continuación, puede definir la clasificación que desee y la aplicación la mantendrá como preferencia del usuario. La versión del recorrido también se muestra en la parte superior de la interfaz de la edición de recorrido, encima del lienzo.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Normalmente, un perfil no puede estar presente varias veces en el mismo recorrido y al mismo tiempo. Si la reentrada está activada, un perfil puede volver a entrar en un recorrido, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido. [Más información](end-journey.md).

Si necesita modificar a un recorrido activo, cree una nueva versión del recorrido.

1. Abra la última versión del recorrido activo, haga clic en **[!UICONTROL Crear una nueva versión]** y confirme.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Solo puede crear una nueva versión a partir de la última versión de un recorrido.

1. Realice las modificaciones necesarias, haga clic en **[!UICONTROL Publicar]** y confirme.

   ![](assets/journeyversions3.png)

Desde el momento en que se publique el recorrido, las personas empezarán a fluir hacia la última versión del recorrido. Las personas que ya han accedido a una versión anterior permanecerán en ella hasta que finalicen el recorrido. Si más tarde vuelven a entrar en el mismo recorrido, accederán a la versión más reciente.

Las versiones de recorrido se pueden detener individualmente. Todas las versiones de los recorridos tienen el mismo nombre.

Cuando se publica una nueva versión de un recorrido, la versión anterior finaliza automáticamente y cambia al estado **Cerrado.**. No puede haber ninguna entrada en el recorrido. Aunque detenga la versión más reciente, la versión anterior permanecerá cerrada.
