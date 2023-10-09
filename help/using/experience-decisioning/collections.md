---
title: Colecciones
description: Aprenda a trabajar con colecciones
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 17%

---

# Colecciones {#collections}

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción a Experience Decisioning](gs-experience-decisioning.md)
* Administración de los elementos de decisión
   * [Configuración del catálogo de elementos](catalogs.md)
   * [Creación de elementos de decisión](items.md)
   * **[Administración de colecciones de elementos](collections.md)**
* Configuración de la selección de elementos
   * [Crear reglas de decisión](rules.md)
   * [Creación de métodos de clasificación](ranking.md)
* [Creación de estrategias de selección](selection-strategies.md)
* [Creación de políticas de decisión](create-decision.md)

>[!ENDSHADEBOX]

Las colecciones le permiten categorizar y agrupar los elementos de decisión según sus preferencias. Estas categorías se crean creando reglas que aprovechan los atributos de los elementos de decisión.

Por ejemplo, supongamos que ha agregado un atributo personalizado &quot;Categoría&quot; al esquema de catálogo de los elementos de decisión. Esto le permite crear una colección que incluye todos los elementos de decisión con el valor &quot;Yoga&quot; en el atributo &quot;Categoría&quot;.

Se puede acceder a la lista de colecciones desde el **[!UICONTROL Elementos]** menú.

Para crear una colección, siga estos pasos:

1. Vaya a **[!UICONTROL Elementos]** > **[!UICONTROL Colecciones]** y haga clic en **[!UICONTROL Crear colección]**.
1. Proporcione un nombre y una descripción para la colección.
1. Agregue una o varias reglas para determinar los elementos que se incluirán en la colección. Para ello:

   1. Elija un atributo de elemento para utilizarlo como criterio. La lista de atributos incluye todos los atributos estándar y personalizados definidos en el esquema del catálogo. [Más información sobre el catálogo de artículos](catalogs.md)
   1. Seleccione el operador deseado e introduzca el valor por el que filtrar.
   1. Repita estos pasos para agregar tantas reglas como sea necesario. Cuando se añaden varias reglas, puede elegir entre las siguientes **Y** y **O** operadores para combinarlos. Para ello, haga clic en el distintivo del operador para cambiar entre las dos opciones.

   ![](assets/collection-create.png)

1. Una vez definidas las reglas de recopilación, haga clic en **[!UICONTROL Crear]**. La colección ahora se muestra en la lista.
