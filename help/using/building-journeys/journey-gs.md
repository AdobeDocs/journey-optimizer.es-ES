---
solution: Journey Optimizer
product: journey optimizer
title: Creación de su primer recorrido
description: Pasos clave para crear su primer recorrido con Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, primero, inicio, inicio rápido, audiencia, evento, acción
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: d3ec39dc08b23f315914be57a617c921903fead8
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 26%

---

# Creación de su primer recorrido {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Creación de recorridos"
>abstract="Utilice **Adobe Journey Optimizer** para crear casos de uso de orquestación en tiempo real aprovechando los datos contextuales almacenados en eventos o fuentes de datos."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Recorridos"
>abstract="Diseñar recorridos de clientes para ofrecer experiencias personalizadas y contextuales. Journey Optimizer permite crear casos prácticos de orquestación en tiempo real con información contextual almacenada en eventos o fuentes de datos. La pestaña **Información general** muestra un panel con métricas clave relacionadas con los recorridos. La pestaña **Examinar** muestra la lista de recorridos existentes."

Cree recorridos de cliente de varios pasos que inicien una secuencia de interacciones, ofertas y mensajes en varios canales en tiempo real. Este enfoque garantiza que los clientes se involucren en los momentos óptimos en función de sus acciones y señales comerciales relevantes.

![muestra de lienzo de recorrido](assets/journey38.png)

Adobe Journey Optimizer incluye un lienzo de orquestación omnicanal que permite a los expertos en marketing armonizar el alcance del marketing con la participación individual del cliente. La interfaz de usuario de le permite arrastrar y soltar fácilmente actividades de la paleta en el lienzo para crear su recorrido. La interfaz de usuario de recorrido se detalla en [esta página](journey-ui.md).

Los pasos principales para crear un recorrido se detallan en esta página. Se racionalizan de la siguiente manera:

![Pasos de creación de recorrido: crear, diseñar, probar y publicar](assets/journey-creation-process.png)


## Requisitos previos {#start-prerequisites}

Para enviar mensajes con recorridos, se necesitan los siguientes requisitos previos:

1. **Configurar un evento**: si desea almacenar en déclencheur las recorridos de forma unitaria cuando se recibe un evento, debe configurar un evento. Usted define la información esperada y cómo procesarla. Este paso lo realiza un **usuario técnico**. [Más información](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Crear una audiencia**: su recorrido también puede escuchar audiencias de Adobe Experience Platform para enviar mensajes en lote a un conjunto especificado de perfiles. Para ello, debe crear audiencias. [Más información](../audience/about-audiences.md).

   ![](assets/segment2.png)

1. **Configuración del origen de datos**: puede definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos, por ejemplo, en las condiciones. También se configura una fuente de datos integrada de Adobe Experience Platform en el momento del aprovisionamiento. Este paso no es necesario si solo se aprovechan los datos de los eventos durante el recorrido. Este paso lo realiza un **usuario técnico**. [Más información](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Configurar una acción**: si usa un sistema de terceros para enviar mensajes, puede crear una acción personalizada. Obtenga más información en esta [sección](../action/action.md). Este paso lo realiza un **usuario técnico**. Si utiliza las funciones de mensajes integradas de Journey Optimizer, solo necesita añadir una acción de canal al recorrido y diseñar el contenido.

   ![](assets/custom2.png)



Como ingeniero de datos, los pasos para configurar sus recorridos, incluidas las fuentes de datos, los eventos y las acciones, se detallan en [esta sección](../configuration/about-data-sources-events-actions.md).


>[!NOTE]
>
>En [esta página](../start/guardrails.md) se detallan los mecanismos de protección y limitaciones de los recorridos

## Creación de un recorrido de varios pasos {#jo-build}

Para crear un recorrido de varios pasos, siga estos pasos:

1. En la sección de menú ADMINISTRACIÓN DE RECORRIDO, haga clic en **[!UICONTROL Recorridos]**.

1. Haga clic en el botón **[!UICONTROL Crear Recorrido]** para crear un recorrido nuevo.

1. Edite el panel de configuración del recorrido para definir el nombre del recorrido y sus propiedades. Aprenda a establecer las propiedades de su recorrido en [esta página](journey-properties.md).

   ![](assets/jo-properties.png)

A continuación, puede empezar a diseñar el recorrido.

## Diseño del recorrido {#jo-design}

El diseñador de recorridos omnicanal le ayuda a crear recorridos de varios pasos con públicos destinatarios, actualizaciones basadas en interacciones comerciales o de clientes en tiempo real y mensajes omnicanal mediante una interfaz intuitiva de arrastrar y soltar.

![](assets/journey38.png)

1. Para empezar, arrastre y suelte un evento o una actividad **Leer audiencia** de la paleta en el lienzo. Para obtener más información sobre el diseño de recorrido, consulte [esta sección](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Arrastre y suelte los siguientes pasos que seguirá el individuo. Por ejemplo, puede agregar una condición seguida de una acción del canal. Para obtener más información sobre las actividades, consulte [esta sección](about-journey-activities.md).

## Prueba del recorrido {#jo-test}

Una vez creado el recorrido, puede probarlo antes de publicarlo. Journey Optimizer ofrece el &quot;Modo de prueba&quot; como una forma de ver los perfiles de prueba a medida que se mueven por el recorrido, detectando posibles errores antes de la activación. La ejecución de pruebas rápidas le permite comprobar que los recorridos funcionan correctamente para que pueda publicarlos con confianza.

Obtenga más información en esta [sección](testing-the-journey.md)

## Publicar el recorrido {#jo-pub}

Debe publicar un recorrido para activarlo y hacer que esté disponible para que los nuevos perfiles lo introduzcan. Antes de publicar el recorrido, compruebe que sea válido y que no haya ningún error. No se puede publicar un recorrido con errores. Obtenga más información acerca de la publicación de recorrido en esta [sección](publishing-the-journey.md).

![](assets/jo-journeyuc2_32bis.png)

Una vez publicado, puede monitorizar su recorrido mediante las herramientas de sistema de informes específicas para medir la efectividad de su recorrido.

![](assets/jo-dynamic_report_journey_12.png)

Obtenga más información acerca de los informes de recorrido en esta [sección](../reports/live-report.md).

Tenga en cuenta que puede duplicar un recorrido existente o crear una nueva versión de un recorrido. Aprenda en [esta página](journey-ui.md)