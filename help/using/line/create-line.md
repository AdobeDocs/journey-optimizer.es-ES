---
solution: Journey Optimizer
product: journey optimizer
title: Creación de un mensaje de LINE
description: Obtenga información sobre cómo crear un mensaje de LINE en Journey Optimizer
feature: Line
topic: Content Management
role: User
level: Beginner
exl-id: a93d4dc9-f0e9-400c-b9a4-6cdac84390fd
source-git-commit: 12dbe0031e9037d879e0d2309c7c26cc3c00cc4e
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 5%

---

# Creación de un mensaje de LINE {#create-line}

## Añadir un mensaje de LINE {#create-line-journey-campaign}

Examine las pestañas siguientes para aprender a añadir un mensaje de LINE en una campaña o un recorrido.

>[!BEGINTABS]

>[!TAB Agregar un mensaje de LINE a un Recorrido]

1. Abra el recorrido y arrastre y suelte una actividad **LINE** desde la sección **Actions** de la paleta.

   ![](assets/jo-line-1.png)

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la configuración de mensaje que desea utilizar.

   Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md)

   El campo **[!UICONTROL configuration]** está rellenado previamente de forma predeterminada con la última configuración que el usuario usó para ese canal.

Ahora puede empezar a diseñar el contenido de su mensaje SMS desde el botón **[!UICONTROL Editar contenido]**, como se detalla a continuación.

>[!TAB Agregar un mensaje de LINE a una campaña]

1. Acceda al menú **[!UICONTROL Campañas]** y haga clic en **[!UICONTROL Crear campaña]**.

1. Seleccione el tipo de campaña que desea ejecutar

   * **Programado - Marketing**: ejecute la campaña inmediatamente o en una fecha especificada. Las campañas programadas están destinadas a enviar mensajes de marketing. Se configuran y ejecutan desde la interfaz de usuario de.

   * **Activado por API - Marketing/Transaccional**: ejecute la campaña mediante una llamada de API. Las campañas activadas por API están destinadas a enviar mensajes de marketing o transaccionales, es decir, mensajes enviados después de una acción realizada por un individuo: restablecimiento de contraseña, compra en el carro de compras, etc.

1. En la sección **[!UICONTROL Propiedades]**, edite el **[!UICONTROL Título]** y la **[!UICONTROL Descripción]** de su campaña.

1. Haga clic en el botón **[!UICONTROL Seleccionar audiencia]** para definir la audiencia a la que se dirigirá desde la lista de audiencias de Adobe Experience Platform disponibles. [Más información](../audience/about-audiences.md).

1. En el campo **[!UICONTROL Área de nombres de identidad]**, elija el área de nombres que desea usar para identificar a los individuos de la audiencia seleccionada. [Más información](../event/about-creating.md#select-the-namespace).

1. En la sección **[!UICONTROL Actions]**, elija **[!UICONTROL LINE]** y seleccione o cree una nueva configuración.

   Obtenga más información acerca de la configuración de LINE en [esta página](line-configuration.md).

   ![](assets/campaign-line-1.png)

1. Haga clic en **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido y crear tratamientos para medir su rendimiento e identificar la mejor opción para la audiencia objetivo. [Más información](../content-management/content-experiment.md)

1. En la sección **[!UICONTROL Seguimiento de acciones]**, especifique si desea rastrear los clics en los vínculos del mensaje SMS.

1. Las campañas están diseñadas para ejecutarse en una fecha específica o en una frecuencia recurrente. Aprenda a configurar la **[!UICONTROL programación]** de su campaña en [esta sección](../campaigns/create-campaign.md#schedule).

1. En el menú **[!UICONTROL déclencheur de acción]**, elige la **[!UICONTROL Frecuencia]** de tu mensaje SMS:

   * Una vez
   * Diaria
   * Semanal
   * Month

Ahora puede empezar a diseñar el contenido de su mensaje de texto desde el botón **[!UICONTROL Editar contenido]**, como se detalla a continuación.

>[!ENDTABS]

## Definición del contenido de LINE{#line-content}

Adobe Journey Optimizer admite los siguientes tipos de mensajes para LINE:

* **Texto**: envía mensajes de texto sin formato o con formato.
* **Adhesivos**: Incorpore los adhesivos nativos de LINE para agregar carácter y expresividad.
* **Imágenes**: adjunte imágenes para mejorar el atractivo visual.
* **Vídeos**: Comparte contenido de vídeo para la comunicación dinámica.
* **Ubicaciones**: envía información de ubicación con mapas.
* **Plantillas**: Utilice plantillas predefinidas para mensajes consistentes.
* **Mensajes de Flex**: cree diseños complejos con contenido enriquecido mediante mensajes de Flex basados en JSON.

Estos tipos de mensajes se pueden configurar editando directamente el contenido JSON, lo que permite estrategias de mensajería dinámicas y personalizadas.

Para configurar el contenido de LINE, siga los pasos a continuación.

1. En la pantalla de configuración del recorrido o la campaña, haga clic en el botón **[!UICONTROL Editar contenido]** para configurar el contenido del mensaje de texto.

1. Haga clic en **[!UICONTROL Editar código]** para editar el contenido JSON.

1. Utilice el editor de personalización para definir contenido, añadir personalización y contenido dinámico. Puede utilizar cualquier atributo, como el nombre del perfil o la ciudad, por ejemplo. También puede definir reglas condicionales. Vaya a las páginas siguientes para obtener más información sobre [personalización](../personalization/personalize.md) y [contenido dinámico](../personalization/get-started-dynamic-content.md) en el editor de personalización.

1. Haga clic en **[!UICONTROL Guardar]** y compruebe el mensaje en la vista previa.

1. Utilice el botón **[!UICONTROL Simular contenido]** para obtener una vista previa del contenido del mensaje de LINE y del contenido personalizado.

Una vez que haya realizado las pruebas y validado el contenido, puede enviar el mensaje de LINE a su audiencia. Estos pasos se detallan en [esta página](send-line.md)

Una vez enviado, puede medir el impacto de su LINE dentro de los informes de Campaña o Recorrido. Para obtener más información sobre la creación de informes, consulte [esta sección](../reports/campaign-global-report-cja.md).
