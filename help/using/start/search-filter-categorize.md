---
solution: Journey Optimizer
product: journey optimizer
title: Buscar, filtrar, organizar
description: Más información acerca de la interfaz de usuario de Journey Optimizer
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
exl-id: 6151aea2-6a34-4000-ba48-161efe4d94d7
source-git-commit: cbd121dda4093fdea6f6bded02e8ae3e188e827d
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 87%

---

# Buscar, filtrar, organizar {#search-filter-organize}

## Buscar {#unified-search}

Desde la interfaz de Adobe Journey Optimizer, utilice la búsqueda unificada de Adobe Experience Cloud en el centro de la barra superior para buscar recursos, recorridos, conjuntos de datos y más en los entornos limitados.

Empiece a introducir contenido para mostrar los resultados principales. Los artículos de ayuda sobre las palabras clave introducidas también se muestran en los resultados.

![](assets/unified-search.png)

Pulse **Entrar** para acceder a todos los resultados y filtrar por objeto empresarial.

![](assets/search-and-filter.png)

## Filtrar listas {#filter-lists}

En la mayoría de las listas, utilice la barra de búsqueda para buscar elementos específicos y defina los criterios de filtrado.

Se puede acceder a los filtros haciendo clic en el icono de filtro en la parte superior izquierda de la lista. El menú de filtro permite filtrar los elementos mostrados según diferentes criterios: puede elegir mostrar solo los elementos de un determinado tipo o estado, los que ha creado o los modificados en los últimos 30 días. Las opciones difieren según el contexto.

Además, puede utilizar etiquetas unificadas para filtrar una lista en función de las etiquetas asignadas a un objeto. Por ahora, las etiquetas están disponibles para recorridos y campañas. [Descubra cómo trabajar con campañas](#tags)

>[!NOTE]
>
>Tenga en cuenta que las columnas mostradas se pueden personalizar mediante el botón de configuración en la parte superior derecha de las listas. La personalización se guarda para cada usuario.

En las listas, puede realizar acciones básicas por cada elemento. Por ejemplo, puede duplicar o eliminar un elemento.

![](assets/journey4.png)

## Trabajar con etiquetas unificadas {#tags}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_tags"
>title="Etiquetas"
>abstract="Este campo le permite asignar Etiquetas unificadas de Adobe Experience Platform a la campaña. Esto le permite clasificarlos fácilmente y mejorar la búsqueda desde la lista de campañas."

Con [Etiquetas unificadas](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/overview.html?lang=es) de Adobe Experience Platform, puede clasificar fácilmente sus objetos de Journey Optimizer para mejorar la búsqueda en las listas. 

![](../rn/assets/do-not-localize/campaigns-tag.gif)

Si añade etiquetas significativas a los públicos en Journey Optimizer podrá filtrar y buscar más adelante para encontrar públicos más fácilmente. Las etiquetas se pueden utilizar además para organizar públicos en carpetas relevantes en las que se puede buscar, crear ofertas y experiencias personalizadas y utilizarlas en reglas de decisión de experiencias.

### Añadir etiquetas a un objeto {#add-tags}

El campo **[!UICONTROL Etiquetas]** le permite definir etiquetas para el objeto. Las etiquetas están disponibles para los siguientes objetos:

* [Campañas](../campaigns/create-campaign.md#create)
* [Elementos de decisión](../experience-decisioning/items.md)
* [Fragmentos](../content-management/fragments.md)
* [Recorridos](../building-journeys/journey-properties.md)
* [Páginas de aterrizaje](../landing-pages/create-lp.md)
* [Listas de suscripciones](../landing-pages/subscription-list.md)
* [Plantillas](../content-management/content-templates.md)

Puede seleccionar una etiqueta existente o crear una nueva. Para ello, siga los pasos que aparecen a continuación.

1. Empiece a escribir el nombre de la etiqueta deseada y selecciónela en la lista.

   ![](assets/tags1.png)

   >[!NOTE]
   >
   > Las etiquetas no distinguen entre mayúsculas y minúsculas.

1. Si la etiqueta que está buscando no está disponible, haga clic en **[!UICONTROL Crear &quot;&quot;]** para definir una nueva: se añadirá automáticamente al objeto actual y estará disponible para todos los demás objetos.

   ![](assets/tags4.png)

1. La lista de las etiquetas seleccionadas o creadas se muestra debajo del campo **[!UICONTROL Etiquetas]**. Puede definir tantas etiquetas como sea necesario.

>[!NOTE]
> 
> Si duplica o crea una nueva versión de un objeto, se conservan las etiquetas.

### Filtrar por etiquetas {#filter-on-tags}

Cada lista de objetos muestra una columna dedicada para que pueda visualizar fácilmente sus etiquetas.

Un filtro también está disponible para mostrar únicamente objetos con determinadas etiquetas.

![](assets/tags2.png)

Puede añadir o eliminar etiquetas de cualquier tipo de recorrido o campaña (activa, borrador, etc.). Para ello, haga clic en el icono **[!UICONTROL Más acciones]** junto al objeto y seleccione **[!UICONTROL Editar etiquetas]**.

![](assets/tags3.png)

### Administrar etiquetas {#manage-tags}

Los administradores pueden eliminar etiquetas y organizarlas por categorías utilizando la variable **[!UICONTROL Etiquetas]** en **[!UICONTROL ADMINISTRACIÓN]**. Obtenga más información sobre la administración de etiquetas en [Documentación de etiquetas unificadas](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/ui/managing-tags.html?lang=es).

>[!NOTE]
>
> Etiquetas creadas directamente a partir del campo **[!UICONTROL Etiquetas]** en Journey Optimizer se añaden automáticamente a la categoría integrada &quot;Sin categoría&quot;.
