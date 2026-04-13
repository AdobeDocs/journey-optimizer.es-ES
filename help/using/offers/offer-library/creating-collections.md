---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Crear colecciones
description: Obtenga información sobre cómo organizar ofertas mediante colecciones
badge: label="Heredado" type="Informative"
feature: Decision Management, Collections
topic: Integrations
role: User
level: Intermediate
exl-id: 0c8808e3-9148-4a33-9fd5-9218e02c2dfd
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 34%

---

# Crear colecciones {#create-collections}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../experience-decisioning/gs-experience-decisioning.md)

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_collection"
>title="Acerca de las colecciones de ofertas"
>abstract="Con las colecciones de ofertas, puede organizar las ofertas reagrupándolas en las categorías que desee."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic"
>title="Colección dinámica"
>abstract="Utilice los calificadores de colección para calificar dinámicamente ofertas para una colección."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static"
>title="Colección estática"
>abstract="Seleccione y agrupe ofertas manualmente según los criterios como estado, calificadores de colección, fecha y canal."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static_select"
>title="Vista previa de la colección estática"
>abstract="Las colecciones estáticas se crean seleccionando manualmente las ofertas individuales para incluirlas en la colección. La colección solo se puede actualizar añadiendo manualmente más ofertas."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic_select"
>title="Vista previa de la colección dinámica"
>abstract="Las colecciones dinámicas recopilan ofertas basadas en calificadores de colección. Estas colecciones se actualizan automáticamente. Por ejemplo, si se crea una oferta nueva con el calificador de colección “deportes”, se añade automáticamente a la colección correspondiente."

Las colecciones le permiten organizar sus ofertas reagrupándolas en categorías de su elección. Por ejemplo, puede crear una colección &quot;sport&quot; que contenga únicamente ofertas relacionadas con el deporte.

➡️ [Descubra esta funcionalidad en vídeo](#video)

Se puede acceder a la lista de colecciones de ofertas en el menú **[!UICONTROL Ofertas]**.

![](../assets/collections_list.png)

Puede crear dos tipos de colecciones:

* **Las colecciones dinámicas** son colecciones de ofertas basadas en calificadores de colección (anteriormente conocidas como &quot;etiquetas&quot;). Estas colecciones se actualizan automáticamente. Por ejemplo, si se crea una oferta nueva con el calificador de recopilación seleccionado, esta se agrega automáticamente a la colección.

* **Las colecciones estáticas** son colecciones creadas seleccionando manualmente ofertas individuales para incluirlas en la colección. La colección solo se puede actualizar añadiendo manualmente más ofertas.

Para crear una colección, siga estos pasos:

1. Vaya a la ficha **[!UICONTROL Colecciones]** y, a continuación, haga clic en **[!UICONTROL Crear colección]**.

1. Especifique el nombre y el tipo de colección que desea crear.

   ![](../assets/collection_create.png)

1. Para crear una colección dinámica, usa el panel izquierdo para seleccionar el calificador de colección de las ofertas que se agregarán a la colección y luego haz clic en **[!UICONTROL Guardar]**. Todas las ofertas con el calificador de colección seleccionado se guardarán en la colección.

   Para obtener más información sobre la creación de calificadores de colección, consulte [Crear calificadores de colección](../offer-library/creating-tags.md).

   ![](../assets/dynamic_collection.png)

1. Para crear una colección estática, utilice el panel izquierdo para filtrar la lista de ofertas (estado, calificador de colección, fecha, canal, tipo de contenido) y, a continuación, seleccione las ofertas que desea agregar a la colección.

   ![](../assets/static_collection.png)

   >[!NOTE]
   >
   >Las colecciones estáticas no se actualizan automáticamente. Para añadir ofertas a una colección estática, debe editarlas y añadirlas manualmente.

1. Para asignar etiquetas de uso de datos principales o personalizadas a una colección estática, selecciona **[!UICONTROL Administrar acceso]**. [Más información acerca del Control de acceso de nivel de objeto (OLAC)](../../administration/object-based-access.md)

   >[!NOTE]
   >
   >El uso de OLAC no está disponible para colecciones dinámicas. Debe administrarse en el nivel de oferta. Por lo tanto, es posible que no vea ninguna oferta en una colección dinámica si no tiene acceso a ninguna de estas ofertas.

1. Una vez creada la colección, se muestra en la lista. Puede seleccionarlo para editarlo o eliminarlo.

   ![](../assets/collection_created.png)

## Vídeo práctico {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329376?quality=12)


