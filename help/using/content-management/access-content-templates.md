---
solution: Journey Optimizer
product: journey optimizer
title: Acceso y administración de plantillas de contenido
description: Obtenga información sobre cómo acceder y administrar plantillas de contenido
topic: Content Management
role: User
level: Beginner
exl-id: ef6110c4-1aa6-4835-b0b0-b3c4fe0e7024
source-git-commit: 62b5cfd480414c898ab6f123de8c6b9f99667b7d
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 5%

---

# Acceso y administración de plantillas de contenido {#access-manage-templates}

## Plantillas de contenido de acceso {#access}

Para acceder a la lista de plantillas de contenido, seleccione **[!UICONTROL Administración de contenido]** > **[!UICONTROL Plantillas de contenido]** en el menú de la izquierda.

![](assets/content-template-list.png)

Se muestran todas las plantillas que se crearon en la zona protegida actual, ya sea desde un recorrido o desde una campaña con la opción **[!UICONTROL Guardar como plantilla]**, ya sea desde el menú **[!UICONTROL Plantillas de contenido]**. [Aprenda a crear plantillas](#create-content-templates)

Puede ordenar las plantillas de contenido por:
* Tipo
* Canal
* Fecha de creación o modificación
* Etiquetas: [Más información sobre las etiquetas](../start/search-filter-categorize.md#tags)

También puede elegir mostrar únicamente los elementos que ha creado o modificado.

![](assets/content-template-list-filters.png)

## Editar y eliminar plantillas de contenido {#edit}

* Para editar el contenido de una plantilla, haga clic en el elemento deseado de la lista y realice los cambios necesarios. También puede editar las propiedades de la plantilla de contenido haciendo clic en el botón Editar junto al nombre de la plantilla.

  ![](assets/content-template-edit.png)

* Para eliminar una plantilla, selecciona el botón **[!UICONTROL Más acciones]** junto a la plantilla deseada y selecciona **[!UICONTROL Eliminar]**.

  ![](assets/content-template-list-delete.png)

>[!NOTE]
>
>Cuando se edita o elimina una plantilla, las campañas o los recorridos, incluido el contenido creado con esta plantilla, no se ven afectados.

## Mostrar plantillas como miniaturas {#template-thumbnails}

Seleccione el modo **[!UICONTROL Grid view]** para mostrar cada plantilla como una miniatura.

>[!AVAILABILITY]
>
>Esta capacidad se lanza con disponibilidad limitada (LA) para un pequeño conjunto de clientes.

![](assets/content-template-grid-view.png)

>[!NOTE]
>
>Actualmente, solo se pueden generar las miniaturas adecuadas para plantillas de contenido de correo electrónico de tipo HTML.

Al actualizar un contenido, es posible que tenga que esperar unos segundos antes de que los cambios se reflejen en la miniatura.

## Exportar plantillas de contenido a otra zona protegida {#export}

Journey Optimizer permite copiar una plantilla de contenido de una zona protegida a otra. Por ejemplo, puede copiar una plantilla del entorno de zona protegida de ensayo en la zona protegida de producción.

El proceso de copia se lleva a cabo mediante una **exportación e importación de paquetes** entre las zonas protegidas de origen y destino. Encontrará información detallada sobre cómo exportar objetos e importarlos en una zona protegida de destino en esta sección: [Copiar objetos en otra zona protegida](../configuration/copy-objects-to-sandbox.md)
