---
title: Caso de uso de decisión
description: Aprenda a crear decisiones utilizando experimentos con el canal basado en código
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
source-git-commit: 3fb9e6cd61e73e9ddf1971f6aa8e15c8b82b8445
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 7%

---

# Caso de uso de decisión {#experience-decisioning-uc}

En este caso de uso, se crea una campaña en la que se definen dos tratamientos de entrega, cada uno con una política de decisión diferente, para medir cuál ofrece el mejor rendimiento para la audiencia de destino.

## Creación de elementos de decisión y estrategias de selección

Primero debe crear elementos, agruparlos en colecciones, configurar reglas y métodos de clasificación. Estos elementos le permiten crear estrategias de selección.

1. Vaya a **[!UICONTROL Decisiones]** > **[!UICONTROL catálogos]** y cree varios elementos de decisión. Establezca restricciones utilizando audiencias o reglas para restringir cada elemento solo a perfiles específicos. [Más información](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. Cree **colecciones** para categorizar y agrupar los elementos de decisión según sus preferencias. [Más información](collections.md)

1. Cree **reglas de decisión** para determinar a quién se puede mostrar un elemento de decisión. [Más información](rules.md)

1. Cree **métodos de clasificación** y aplíquelos dentro de las estrategias de decisión para determinar el orden de prioridad al seleccionar elementos de decisión. [Más información](ranking.md)

1. Genere **estrategias de selección** que aprovechen colecciones, reglas de decisión y métodos de clasificación para identificar los elementos de decisión adecuados para mostrarlos a los perfiles. [Más información](selection-strategies.md)

## Creación de políticas de decisión

Para presentar la mejor oferta dinámica y experiencia a los visitantes de su sitio web o aplicación móvil, agregue una política de decisión a una campaña basada en código.

<!--Define two delivery treatments each containing a different decision policy.-->

1. Cree una campaña y seleccione la acción **[!UICONTROL Experiencia basada en código]**. [Más información](../code-based/create-code-based.md)

1. Desde la ventana **[!UICONTROL Editar contenido]**, empiece a personalizar el tratamiento A.

1. Seleccione el icono **[!UICONTROL Decisiones]**, haga clic en **[!UICONTROL Crear una decisión]** y rellene los detalles de la decisión. [Más información](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Defina las estrategias de selección para su decisión. Haga clic en **[!UICONTROL Agregar estrategia]**.

1. Haga clic en **[!UICONTROL Crear]**. La nueva decisión se agregó en **[!UICONTROL Decisiones]**.

   ![](assets/decision-code-based-decision-added.png)

1. Haga clic en el icono de más acciones (tres puntos) y seleccione **[!UICONTROL Agregar]**. Ahora puede agregar todos los atributos de decisión que desee dentro de esto.

   ![](assets/decision-code-based-add-decision.png)

1. También puede añadir cualquier otro atributo disponible en el editor de personalización, como atributos de perfil.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. En la página de resumen de la campaña, haga clic en **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido. [Más información](../content-management/content-experiment.md)

1. En la ventana **[!UICONTROL Editar contenido]**, seleccione el tratamiento B para cambiar el contenido y repita los pasos anteriores para crear otra decisión.

1. Guarde el contenido.


