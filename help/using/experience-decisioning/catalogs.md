---
title: Catálogo de artículos
description: Aprenda a trabajar con el catálogo de artículos
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Catálogo de artículos {#catalog}

En Decisioning, los catálogos sirven como contenedores centrales para organizar los elementos de decisión. Cada catálogo está vinculado a un esquema de Adobe Experience Platform, que incluye todos los atributos asignables a un elemento de decisión.

Por ahora, todos los elementos de decisión creados se consolidan dentro de un único catálogo &quot;Ofertas&quot;, al que se puede acceder mediante el menú **[!UICONTROL Catálogos]**.

![](assets/catalogs-list.png)

## Mecanismos de protección y limitaciones

Para garantizar un rendimiento y una coherencia óptimos, Decisioning aplica las siguientes barreras y limitaciones:

* **Tipos de datos compatibles**

  Por ahora, Decisioning admite exclusivamente los siguientes tipos de datos: String, Integer, Boolean, Date, DateTime, Decisioning Asset y Object. Cualquier campo que no pertenezca a estos tipos de datos no estará disponible para su uso durante la creación de un elemento de decisión o un catálogo.


* **Límite de atributo personalizado**

  Cada elemento de decisión puede incluir hasta 100 atributos personalizados.

* **Restricciones de anidamiento**

  Se admite un máximo de cuatro niveles de anidación. Las imágenes no se admiten en el último nivel.

## Acceso y edición del esquema del catálogo {#access-catalog-schema}

Para acceder al esquema del catálogo donde se almacenan los atributos de los elementos de decisión, siga estos pasos:

1. En la lista de elementos, haga clic en el botón **[!UICONTROL Editar esquema]** ubicado junto al botón **[!UICONTROL Crear elemento]**.

1. El esquema del catálogo se abre en una nueva pestaña, que sigue la estructura siguiente:

   * El nodo **`_experience`** incluye atributos de elementos de decisión estándar como nombre, fecha de inicio y finalización y descripción.
   * El nodo **`_<imsOrg>`** contiene atributos de elementos de decisión personalizados. De forma predeterminada, no se configuran atributos personalizados, pero puede agregar tantos como sea necesario para adaptarlos a sus necesidades. Una vez finalizado, los atributos personalizados aparecen en la pantalla de creación de elementos de decisión junto con los atributos estándar.

   ![](assets/catalogs-schema.png)

1. Para agregar un atributo personalizado al esquema, expanda el nodo **`_<imsOrg>`** y haga clic en el botón &quot;+&quot; en la ubicación deseada en la estructura.

   ![](assets/catalogs-add.png)

1. Rellene los campos necesarios para el atributo agregado y haga clic en **[!UICONTROL Aplicar]**.

   El valor que se introduce en un atributo con el atributo de recurso de toma de decisiones es una URL pública. La mayoría de las veces esto apuntaría a una imagen.

   Encontrará información detallada sobre cómo trabajar con esquemas de Adobe Experience Platform en la [documentación del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=es).

1. Una vez añadidos los atributos personalizados deseados, guarde el esquema. El nuevo campo ya está disponible en la pantalla de creación de elementos de decisión, en la sección **[!UICONTROL Atributos personalizados]**.


   El ejemplo siguiente muestra una pantalla de creación de elementos con atributos personalizados como objetos definidos en el esquema.

   ![](assets/custom-attributes.png)

