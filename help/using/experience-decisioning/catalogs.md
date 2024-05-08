---
title: Catálogo de artículos
description: Aprenda a trabajar con el catálogo de artículos
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilidad limitada"
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Catálogo de artículos {#catalog}

En Experience Decisioning, los catálogos sirven como contenedores centrales para organizar los elementos de decisión. Cada catálogo está vinculado a un esquema de Adobe Experience Platform, que incluye todos los atributos asignables a un elemento de decisión.

Por ahora, todos los elementos de decisión creados se consolidan dentro de un único catálogo &quot;Ofertas&quot;, accesible a través de la **[!UICONTROL Catálogos]** menú.

![](assets/catalogs-list.png)

Para acceder al esquema del catálogo donde se almacenan los atributos de los elementos de decisión, siga estos pasos:

1. En la lista de elementos, haga clic en **[!UICONTROL Editar esquema]** situado junto al botón **[!UICONTROL Crear elemento]** botón.

1. El esquema del catálogo se abre en una nueva pestaña, que sigue la estructura siguiente:

   * El **`_experience`** El nodo incluye atributos de elementos de decisión estándar como nombre, fecha de inicio y finalización y descripción.
   * El **`_<imsOrg>`** El nodo aloja atributos de elementos de decisión personalizados. De forma predeterminada, no se configuran atributos personalizados, pero puede agregar tantos como sea necesario para adaptarlos a sus necesidades. Una vez finalizado, los atributos personalizados aparecen en la pantalla de creación de elementos de decisión junto con los atributos estándar.

   ![](assets/catalogs-schema.png)

1. Para agregar un atributo personalizado al esquema, expanda la variable **`_<imsOrg>`** y haga clic en el botón &quot;+&quot; en la ubicación deseada en la estructura.

   ![](assets/catalogs-add.png)

1. Rellene los campos necesarios para el atributo añadido y haga clic en **[!UICONTROL Aplicar]**.

   >[!CAUTION]
   >
   >Por ahora, Experience Decisioning admite exclusivamente los siguientes tipos de datos: cadena, entero, booleano, fecha, hora y recurso de toma de decisiones. Cualquier campo que no pertenezca a estos tipos de datos no estará disponible para su uso durante la creación de un elemento de decisión o un catálogo.

   El valor que se introduce en un atributo con el atributo de recurso de toma de decisiones es una URL pública. La mayoría de las veces esto apuntaría a una imagen.

   Encontrará información detallada sobre cómo trabajar con esquemas de Adobe Experience Platform en la [Documentación del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=es).

1. Una vez añadidos los atributos personalizados deseados, guarde el esquema. El nuevo campo está ahora disponible en la pantalla de creación de decisiones de elementos, dentro de la variable **[!UICONTROL Atributos personalizados]** sección.
