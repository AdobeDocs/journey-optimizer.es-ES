---
title: Colecciones
description: Aprenda a trabajar con colecciones
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilidad limitada"
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 51%

---

# Colecciones {#collections}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collections"
>title="Crear colecciones"
>abstract="Las colecciones le permiten categorizar y agrupar los elementos de decisión según sus preferencias. Estas categorías se crean creando reglas que aprovechan los atributos de los elementos de decisión."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collection_rules"
>title="Definición de reglas para la colección"
>abstract="Añada una o varias reglas para determinar los elementos que se incluirán en la colección. Elija un atributo de elemento para utilizarlo como criterio. Seleccione el operador deseado e introduzca el valor por el que desea filtrar. Añada tantas reglas como sea necesario."

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_collection"
>title="Elija una colección"
>abstract="Seleccione la colección que contiene las ofertas que se deben tener en cuenta. Este paso es obligatorio al crear una estrategia de selección. Las colecciones le permiten categorizar y agrupar los elementos de decisión según sus preferencias. Por ejemplo, puede crear una colección que incluya todos los elementos de decisión con el valor &quot;Yoga&quot; en el atributo personalizado &quot;Categoría&quot;."

Las colecciones le permiten categorizar y agrupar los elementos de decisión según sus preferencias. Estas categorías se crean creando reglas que aprovechan los atributos de los elementos de decisión.

Por ejemplo, supongamos que ha agregado un atributo personalizado &quot;Categoría&quot; al esquema de catálogo de los elementos de decisión. Esto le permite crear una colección que incluye todos los elementos de decisión con el valor &quot;Yoga&quot; en el atributo &quot;Categoría&quot;.

Se puede acceder a la lista de colecciones desde el menú **[!UICONTROL catálogos]**.

Para crear una colección, siga estos pasos:

1. Vaya a **[!UICONTROL catálogos]** > **[!UICONTROL Colecciones]** y haga clic en **[!UICONTROL Crear colección]**.
1. Proporcione un nombre y una descripción para la colección.
1. Añada una o varias reglas para determinar los elementos que se incluirán en la colección. Para ello, haga lo siguiente:

   1. Elija un atributo de elemento para utilizarlo como criterio. La lista de atributos incluye todos los atributos estándar y personalizados definidos en el esquema del catálogo. [Más información sobre el catálogo de artículos](catalogs.md)
   1. Seleccione el operador deseado e introduzca el valor por el que filtrar.
   1. Repita estos pasos para agregar tantas reglas como sea necesario. Cuando se agregan varias reglas, puede elegir entre los operadores **And** y **Or** para combinarlas. Para ello, haga clic en el distintivo del operador para cambiar entre las dos opciones.
   1. Haga clic en el botón **[!UICONTROL Vista previa de la colección]** para mostrar los elementos que cumplen las reglas que ha definido.

   ![](assets/collection-create.png)

1. Una vez definidas las reglas de recopilación, haga clic en **[!UICONTROL Crear]**. La colección ahora se muestra en la lista.
