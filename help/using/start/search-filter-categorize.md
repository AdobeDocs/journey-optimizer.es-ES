---
solution: Journey Optimizer
product: journey optimizer
title: Buscar, filtrar, organizar
description: Más información sobre la interfaz de usuario de Journey Optimizer
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
exl-id: 6151aea2-6a34-4000-ba48-161efe4d94d7
TQID: https://experienceleague.adobe.com/ViOHdq6ypY2xbYrPrEsYKF4-5CyQV9izbtzhGGOzsF0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 659
ht-degree: 0%

---

# Buscar, filtrar, organizar {#search-filter-organize}

A medida que los proyectos de Adobe Journey Optimizer crecen, encontrar y organizar contenido se vuelve esencial para un trabajo eficiente. Esta página muestra cómo localizar rápidamente recorridos, campañas y recursos mediante la búsqueda universal, filtrar listas para centrarse en elementos específicos y organizar su trabajo con etiquetas y categorías. Estas herramientas le ayudan a navegar por grandes volúmenes de contenido, mantener la coherencia entre equipos y optimizar los flujos de trabajo diarios.

## Buscar {#unified-search}

Desde la interfaz de Adobe Journey Optimizer, utilice la búsqueda unificada de Adobe Experience Cloud en el centro de la barra superior para buscar recursos, recorridos, conjuntos de datos y más en los entornos limitados.

Empiece a introducir contenido para mostrar los resultados principales. Los artículos de ayuda sobre las palabras clave introducidas también se muestran en los resultados.

![](assets/unified-search.png)

Presione **Intro** para acceder a todos los resultados y filtrar por objeto de negocio.

![](assets/search-and-filter.png)

## Filtrado de listas {#filter-lists}

En la mayoría de las listas, utilice la barra de búsqueda para buscar elementos específicos y definir criterios de filtrado.

Se puede acceder a los filtros haciendo clic en el icono de filtro en la parte superior izquierda de una lista. El menú de filtro permite filtrar los elementos mostrados según diferentes criterios: puede elegir mostrar solo los elementos de un determinado tipo o estado, los que ha creado o los modificados en los últimos 30 días. Las opciones difieren según el contexto.

Además, puede utilizar etiquetas unificadas para filtrar una lista en función de las etiquetas asignadas a un objeto. Por ahora, las etiquetas están disponibles para recorridos y campañas. [Aprenda a trabajar con etiquetas](#tags)

>[!NOTE]
>
>Tenga en cuenta que las columnas mostradas se pueden personalizar mediante el botón de configuración en la parte superior derecha de las listas. Personalization se guarda para cada usuario.

En las listas, puede realizar acciones básicas por cada elemento. Por ejemplo, puede duplicar o eliminar un elemento.

![](assets/journey4.png)

## Trabajo con etiquetas unificadas {#tags}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_tags"
>title="Etiquetas"
>abstract="Este campo le permite asignar etiquetas unificadas de Adobe Experience Platform a la campaña. Esto le permite clasificarlas fácilmente y mejorar la búsqueda desde la lista de campañas."

Con las [etiquetas unificadas](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/overview.html?lang=es) de Adobe Experience Platform, puede clasificar fácilmente los objetos de Journey Optimizer para mejorar la búsqueda desde las listas.

![](../rn/assets/do-not-localize/campaigns-tag.gif)

Añadir etiquetas significativas a las audiencias en Journey Optimizer le permite filtrar y buscar más adelante para encontrar audiencias más fácilmente. Las etiquetas se pueden utilizar además para organizar audiencias en carpetas relevantes en las que se puede buscar, crear ofertas y experiencias personalizadas y utilizarlas en reglas de decisión de experiencias.

### Añadir etiquetas a un objeto {#add-tags}

El campo **[!UICONTROL Etiquetas]** le permite definir etiquetas para el objeto. Las etiquetas están disponibles para los siguientes objetos:

* [Campañas](../campaigns/create-campaign.md)
* [Elementos de decisión](../experience-decisioning/items.md)
* [Fragmentos](../content-management/fragments.md)
* [Recorridos](../building-journeys/journey-properties.md)
* [Páginas de aterrizaje](../landing-pages/create-lp.md)
* [Listas de suscripción](../landing-pages/subscription-list.md)
* [Plantillas](../content-management/content-templates.md)
* [Configuraciones de canal](../configuration/channel-surfaces.md#channel-config-tags)

Puede seleccionar una etiqueta existente o crear una nueva. Para ello, siga los pasos a continuación.

1. Empiece a escribir el nombre de la etiqueta deseada o selecciónela en la lista.

   ![](assets/tags1.png)

   >[!NOTE]
   >
   > Las etiquetas no distinguen entre mayúsculas y minúsculas.

1. Si la etiqueta que está buscando no está disponible, haga clic en **[!UICONTROL Crear &quot;&quot;]** para definir una nueva: se agrega automáticamente al objeto actual y queda disponible para todos los demás objetos.

   ![](assets/tags4.png)

1. La lista de las etiquetas seleccionadas o creadas se muestra debajo del campo **[!UICONTROL Etiquetas]**. Puede definir tantas etiquetas como sea necesario.

>[!NOTE]
> 
> Si duplica o crea una nueva versión de un objeto, las etiquetas se conservan.

### Filtrar por etiquetas {#filter-on-tags}

Cada lista de objetos muestra una columna dedicada para que pueda visualizar fácilmente sus etiquetas.

Un filtro también está disponible para mostrar únicamente objetos con determinadas etiquetas.

![](assets/tags2.png)

Puede añadir o eliminar recorridos de cualquier tipo de campaña o campaña (en directo, borrador, etc.). Para ello, haga clic en el icono **[!UICONTROL Más acciones]** junto al objeto y seleccione **[!UICONTROL Editar etiquetas]**.

![](assets/tags3.png)

### Administración de etiquetas {#manage-tags}

Los administradores pueden eliminar etiquetas y organizarlas por categorías mediante el menú **[!UICONTROL Etiquetas]**, en **[!UICONTROL ADMINISTRACIÓN]**. Obtenga más información acerca de la administración de etiquetas en la [documentación de etiquetas unificadas](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/ui/managing-tags.html?lang=es).

>[!NOTE]
>
> Las etiquetas creadas directamente a partir del campo **[!UICONTROL Etiquetas]** en Journey Optimizer se agregan automáticamente a la categoría &quot;Sin categoría&quot; integrada.
