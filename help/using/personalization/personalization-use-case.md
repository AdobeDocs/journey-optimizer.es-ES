---
solution: Journey Optimizer
product: journey optimizer
title: Caso de uso de Personalization&dos puntos; notificación del estado del pedido
description: Obtenga información sobre cómo personalizar un mensaje con información de perfil, decisión de oferta y contexto.
feature: Personalization, Use Cases
topic: Personalization
role: Developer
level: Intermediate
keywords: expresión, editor, caso de uso, personalización
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 2%

---

# Caso de uso de Personalization: notificación del estado del pedido {#personalization-use-case}

En este caso de uso, verá cómo utilizar varios tipos de personalización en un único mensaje de notificación push. Se utilizan tres tipos de personalización:

* **Perfil**: personalización de mensaje basada en un campo de perfil
* **Decisión de oferta**: personalización basada en variables de administración de decisiones
* **Contexto**: personalización basada en datos contextuales del recorrido

El objetivo de este ejemplo es insertar un evento en [!DNL Journey Optimizer] cada vez que se actualice un pedido de cliente. A continuación, se envía una notificación push al cliente con información sobre el pedido y una oferta personalizada.

Para este caso de uso, se necesitan los siguientes requisitos previos:

* configure un evento de pedido que incluya el número de pedido, el estado y el nombre del elemento. Consulte esta [sección](../event/about-events.md).
* crear una decisión, consulte esta [sección](../offers/offer-activities/create-offer-activities.md).

➡️ [Descubra un caso de uso similar en vídeo](#video)

## Paso 1: Creación del recorrido {#create-journey}

1. Haga clic en el menú **[!UICONTROL Recorridos]** y cree un nuevo recorrido.

   ![](assets/perso-uc4.png)

1. Añada el evento de entrada y una actividad de acción **Push**.

   ![](assets/perso-uc5.png)

1. Configure y diseñe su mensaje de notificación push. Consulte esta [sección](../push/create-push.md).

## Paso 2: Adición de una personalización al perfil {#add-perso}

1. En la actividad **Push**, haga clic en **Editar contenido**.

1. Haga clic en el campo **Título**.

   ![](assets/perso-uc2.png)

1. Introduzca el asunto y añada una personalización de perfil. Utilice la barra de búsqueda para encontrar el campo de nombre del perfil. En el texto del asunto, coloque el cursor donde desee insertar el campo de personalización y haga clic en el icono **+**. Haga clic en **Guardar**.

   ![](assets/perso-uc3.png)

## Paso 3: Adición de una personalización sobre los datos contextuales {#add-perso-contextual-data}

1. En la actividad **Push**, haga clic en **Editar contenido** y luego en el campo **Título**.

   ![](assets/perso-uc9.png)

1. Seleccione el menú **Atributos contextuales**. Los atributos contextuales solo están disponibles si un recorrido ha pasado datos contextuales al mensaje. Haga clic en **Journey Orchestration**. Aparecerá la siguiente información contextual:

   * **Eventos**: esta categoría reagrupa todos los campos de los eventos colocados antes de la actividad de acción de canal en el recorrido.
   * **Propiedades del Recorrido**: los campos técnicos relacionados con el recorrido de un perfil determinado, por ejemplo el identificador de recorrido o los errores específicos encontrados. Obtenga más información en [Documentación de Journey Orchestration](../building-journeys/expression/journey-properties.md).

   ![](assets/perso-uc10.png)

1. Expanda el elemento **Events** y busque el campo de número de pedido relacionado con su evento. También puede utilizar el cuadro de búsqueda. Haga clic en el icono **+** para insertar el campo de personalización en el texto del asunto. Haga clic en **Guardar**.

   ![](assets/perso-uc11.png)

1. Ahora haga clic en el campo **Cuerpo**.

   ![](assets/perso-uc12.png)

1. Escriba el mensaje e inserte, desde el menú **[!UICONTROL Atributos contextuales]**, el nombre del elemento de pedido y el progreso del pedido.

   ![](assets/perso-uc13.png)

1. En el menú de la izquierda, seleccione **Decisiones de oferta** para insertar una variable de toma de decisiones. Seleccione la ubicación y haga clic en el icono **+** junto a la decisión de agregarlo al cuerpo.

   ![](assets/perso-uc14.png)

1. Haga clic en Validar para asegurarse de que no haya errores y luego en **Guardar**.

   ![](assets/perso-uc15.png)

## Paso 4: Prueba y publicación del recorrido {#test-publish}

1. Haga clic en el botón **Prueba** y, a continuación, haga clic en **Déclencheur de un evento**.

   ![](assets/perso-uc17.png)

1. Introduzca los diferentes valores que desea aprobar en la prueba. El modo de prueba solo funciona con perfiles de prueba. El identificador de perfil debe corresponder a un perfil de prueba. Haga clic en **Enviar**.

   ![](assets/perso-uc18.png)

   La notificación push se envía y se muestra en el teléfono móvil del perfil de prueba.

   ![](assets/perso-uc19.png)

1. Compruebe que no haya ningún error y publique el recorrido.

## Vídeo práctico {#video}

El siguiente vídeo muestra un caso de uso similar que aprovecha los datos contextuales de un recorrido para personalizar un correo electrónico.

>[!VIDEO](https://video.tv.adobe.com/v/3425027?quality=12)
