---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los recorridos
description: Introducción a los recorridos
feature: Journeys
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: d8fb8759fcd688deec56cb7247ddf082e6d6766d
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 19%

---


# Introducción a los recorridos{#jo-general-principle}

Uso [!DNL Journey Optimizer] para crear casos de uso de orquestación en tiempo real aprovechando los datos contextuales almacenados en eventos o fuentes de datos.

Diseñe escenarios avanzados de varios pasos con las siguientes capacidades:

* Enviar en tiempo real **envío unitario** se activa cuando se recibe un evento, o **en lote** uso de segmentos de Adobe Experience Platform.

* Aprovechar **datos contextuales** desde eventos, información de Adobe Experience Platform o datos de servicios API de terceros.

* Utilice la variable **acciones integradas** para enviar mensajes diseñados en [!DNL Journey Optimizer] o crear **acciones personalizadas** si utiliza un sistema de terceros para enviar mensajes.

* Con la variable **diseñador de recorridos**, cree sus casos de uso de varios pasos: arrastre y suelte fácilmente un evento de entrada o una actividad de segmento de lectura, agregue condiciones y envíe mensajes personalizados.

## Pasos para crear un recorrido{#steps-journey}

Utilice Adobe Journey Optimizer para diseñar y organizar recorridos personalizados desde un solo lienzo.

Adobe Journey Optimizer incluye un lienzo de orquestación omnicanal que permite a los especialistas en marketing armonizar el alcance de marketing con la participación de los clientes uno a uno. La interfaz de usuario le permite arrastrar y soltar fácilmente actividades de la paleta en el lienzo para crear su recorrido.

![](assets/interface-journeys.png)

Obtenga información sobre cómo iniciar y crear su primer recorrido en [esta página](journey-gs.md).

El diseñador de recorridos omnicanal le ayuda a crear recorridos de varios pasos con audiencias de destino, actualizaciones basadas en interacciones empresariales o de clientes en tiempo real y mensajes omnicanal mediante una interfaz intuitiva de arrastrar y soltar.

![](assets/journey38.png)

Más información en [esta sección](using-the-journey-designer.md).

Como ingeniero de datos, los pasos para configurar las recorridos, incluidas las fuentes de datos, los eventos y las acciones, se detallan en [esta sección](../configuration/about-data-sources-events-actions.md).


## Casos de uso{#uc-journey}

Obtenga información sobre cómo crear recorridos en los siguientes casos de uso integral.

Casos de uso empresarial:

* [Envío de mensajes multicanal](journeys-uc.md)
* [Envío de un mensaje mediante Campaign v7/v8](campaign-classic-use-case.md)
* [Envío de un mensaje a los suscriptores](message-to-subscribers-uc.md)

Casos de uso técnico:

* [Paso de colecciones de forma dinámica mediante acciones personalizadas](collections.md)
* [Aumento de envíos](ramp-up-deliveries-uc.md)
* [Limitar el rendimiento con fuentes de datos externas y acciones personalizadas](limit-throughput.md)

## Versiones de recorridos{#journey-versions}

En la lista recorrido, todas las versiones de recorrido se muestran con el número de versión. Consulte [esta página](../building-journeys/using-the-journey-designer.md).

Al buscar un recorrido, las versiones más recientes aparecen en la parte superior de la lista la primera vez que se abre la aplicación. A continuación, puede definir la clasificación que desee y la aplicación la mantendrá como una preferencia de usuario. La versión del recorrido también se muestra en la parte superior de la interfaz de edición de recorrido, encima del lienzo.

![](assets/journeyversions1.png)

>[!NOTE]
>
>En la mayoría de los casos, un perfil no puede estar presente varias veces en el mismo recorrido, al mismo tiempo. Si la reentrada está activada, un perfil puede volver a introducir un recorrido, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido. [Más información](end-journey.md).

Si necesita modificar a un recorrido activo, cree una nueva versión de su recorrido.

1. Abra la última versión de su recorrido en directo y haga clic en **[!UICONTROL Crear una nueva versión]** y confirme.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Solo puede crear una versión nueva a partir de la versión más reciente de un recorrido.

1. Realice las modificaciones necesarias, haga clic en **[!UICONTROL Publicación]** y confirme.

   ![](assets/journeyversions3.png)

Desde el momento en que se publique el recorrido, las personas empezarán a fluir a la última versión del recorrido. Las personas que ya han introducido una versión anterior permanecen en ella hasta que finalizan el recorrido. Si más adelante vuelven a entrar en el mismo recorrido, pasarán a la última versión.

Las versiones de recorrido se pueden detener individualmente. Todas las versiones de recorridos tienen el mismo nombre.

Cuando publica una nueva versión de un recorrido, la versión anterior finaliza automáticamente y cambia a la función **Cerrado** estado. No puede pasar ninguna entrada en el recorrido. Aunque detenga la última versión, la versión anterior permanecerá cerrada.

>[!NOTE]
>
>Obtenga más información sobre las versiones de recorrido, barreras y limitaciones, en [esta página](../start/guardrails.md#journey-versions-limitations)