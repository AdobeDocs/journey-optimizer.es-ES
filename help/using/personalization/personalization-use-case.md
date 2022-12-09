---
solution: Journey Optimizer
product: journey optimizer
title: Caso de uso personalizado y dos puntos; notificación del estado de pedido
description: Obtenga información sobre cómo personalizar un mensaje con perfil, decisión de oferta e información de contexto.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Caso de uso de personalización: notificación del estado de pedido {#personalization-use-case}

En este caso de uso, verá cómo utilizar varios tipos de personalización en un único mensaje de notificación push. Se utilizan tres tipos de personalización:

* **Perfil**: personalización de mensajes basada en un campo de perfil
* **Decisión de oferta**: personalización basada en variables de administración de decisiones
* **Contexto**: personalización basada en datos contextuales del recorrido

El objetivo de este ejemplo es impulsar un evento a [!DNL Journey Optimizer] cada vez que se actualiza un pedido de cliente. A continuación, se envía una notificación push al cliente con información sobre el pedido y una oferta personalizada.

Para este caso de uso, se necesitan los siguientes requisitos previos:

* configure un evento de pedido que incluya el número de pedido, el estado y el nombre del elemento. Consulte esta [sección](../event/about-events.md).
* crear una decisión, consulte esta [sección](../offers/offer-activities/create-offer-activities.md).

## Paso 1: Creación del recorrido {#create-journey}

1. Haga clic en el **[!UICONTROL Journeys]** y cree un nuevo recorrido.

   ![](assets/perso-uc4.png)

1. Añada el evento de entrada y un **Push** actividad de acción.

   ![](assets/perso-uc5.png)

1. Configure y diseñe el mensaje de notificación push. Consulte esta [sección](../push/create-push.md).

## Paso 2: Añadir personalización en el perfil {#add-perso}

1. En el **Push** actividad, haga clic en **Editar contenido**.

1. Haga clic en el **Título** campo .

   ![](assets/perso-uc2.png)

1. Escriba el asunto y añada la personalización del perfil. Utilice la barra de búsqueda para encontrar el campo de nombre del perfil. En el texto del asunto, coloque el cursor donde desee insertar el campo de personalización y haga clic en el **+** icono. Haga clic en **Guardar**.

   ![](assets/perso-uc3.png)

## Paso 3: Añadir personalización en datos contextuales {#add-perso-contextual-data}

1. En el **Push** actividad, haga clic en **Editar contenido** y haga clic en el botón **Título** campo .

   ![](assets/perso-uc9.png)

1. Seleccione el **Atributos contextuales** para abrir el Navegador. Los atributos contextuales solo están disponibles si un recorrido ha pasado datos contextuales al mensaje. Haga clic en **Journey Orchestration**. Aparece la siguiente información contextual:

   * **Eventos**: esta categoría reagrupa todos los campos de los eventos colocados antes de la actividad de acción del canal en el recorrido.
   * **Propiedades del recorrido**: los campos técnicos relacionados con el recorrido de un perfil determinado, por ejemplo, el ID de recorrido o los errores específicos encontrados. Obtenga más información en [Documentación de Journey Orchestration](../building-journeys/expression/journey-properties.md).

   ![](assets/perso-uc10.png)

1. Expanda el **Eventos** y busque el campo de número de pedido relacionado con el evento. También puede utilizar el cuadro de búsqueda. Haga clic en el **+** para insertar el campo personalizado en el texto del asunto. Haga clic en **Guardar**.

   ![](assets/perso-uc11.png)

1. A continuación, haga clic en el botón **Cuerpo** campo .

   ![](assets/perso-uc12.png)

1. Escriba el mensaje e inserte, desde el **[!UICONTROL Contextual attributes]** , el nombre del elemento de pedido y el progreso del pedido.

   ![](assets/perso-uc13.png)

1. En el menú de la izquierda, seleccione **Decisiones de oferta** para insertar una variable de decisión. Seleccione la colocación y haga clic en el botón **+** junto a la decisión de agregarla al cuerpo.

   ![](assets/perso-uc14.png)

1. Haga clic en validar para asegurarse de que no hay errores y haga clic en **Guardar**.

   ![](assets/perso-uc15.png)

## Paso 4: Prueba y publicación del recorrido {#test-publish}

1. Haga clic en el **Prueba** y haga clic en **Activador de un evento**.

   ![](assets/perso-uc17.png)

1. Introduzca los diferentes valores que se van a pasar en la prueba. El modo de prueba solo funciona con perfiles de prueba. El identificador de perfil debe corresponder a un perfil de prueba. Haga clic en **Enviar**.

   ![](assets/perso-uc18.png)

   La notificación push se envía y se muestra en el teléfono móvil del perfil de prueba.

   ![](assets/perso-uc19.png)

1. Compruebe que no haya error y publique el recorrido.
