---
solution: Journey Optimizer
product: journey optimizer
title: Administrar marca
description: Aprenda a crear y administrar las directrices de marca
badge: label="Beta" type="Informative"
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 4919c8c749f9216be526bab2437a815da0136df5
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 19%

---

# Crear y administrar sus marcas {#brands}

>[!AVAILABILITY]
>
>Esta capacidad se presenta como una versión beta privada. Estará disponible de forma progresiva para todos los clientes en futuras versiones.
>

Las directrices de marca son un conjunto detallado de reglas y estándares que establecen la identidad visual y verbal de una marca. Actúan como referencia para mantener una representación de marca coherente en todas las plataformas de marketing y comunicación.

En Journey Optimizer, ahora tiene la opción de introducir y organizar manualmente los detalles de la marca o cargar documentos de directrices de marca para extraer automáticamente información.

## Acceso a marcas {#generative-access}

Para acceder al menú Marca en Adobe Journey Optimizer, los usuarios deben recibir los permisos de **Managed brand kit** o **[!UICONTROL Habilitar el asistente de IA]**. [Más información](../administration/permissions.md)

+++  Obtenga información sobre cómo asignar permisos relacionados con la marca

1. En el producto **Permisos**, vaya a la pestaña **Funciones** y seleccione la **Función** que desee.

1. Haga clic en **Editar** para modificar los permisos.

1. Agregue el recurso **Asistente de IA** y, a continuación, seleccione **Kit de marca administrado** o **[!UICONTROL Habilitar el asistente de IA]** en el menú desplegable.

   Tenga en cuenta que el permiso **[!UICONTROL Habilitar el asistente de IA]** solo proporciona acceso de solo lectura al menú Marcas.

   ![](assets/brands-permission.png){zoomable="yes"}

1. Haga clic en **Guardar** para aplicar los cambios.

   Los permisos de los usuarios que ya estén asignados a esta función se actualizarán automáticamente.

1. Para asignar esta función a nuevos usuarios, vaya a la pestaña **Usuarios** en el panel de control **Funciones** y haga clic en **Añadir usuario**.

1. Introduzca el nombre del usuario y su dirección de correo electrónico, o selecciónelo en la lista, y haga clic en **Guardar**.

1. Si el usuario no estaba ya creado, consulte [esta documentación](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/abac/permissions-ui/users).


+++

## Cree su marca {#create-brand-kit}

Para crear y administrar las directrices de marca, puede introducir los detalles usted mismo o cargar el documento de directrices de marca para que la información se extraiga automáticamente:

1. En el menú **[!UICONTROL Marcas]**, haga clic en **[!UICONTROL Agregar marca]**.

   ![](assets/brands-1.png)

1. Escriba un **[!UICONTROL Nombre]** y una **[!UICONTROL Descripción]** para la directriz de marca.

1. Arrastre y suelte o seleccione el archivo para cargar las directrices de marca y extraer automáticamente la información de marca relevante. Haga clic en **[!UICONTROL Agregar marca]**.

   Ahora comienza el proceso de extracción de información. Tenga en cuenta que puede tardar varios minutos en completarse.

   ![](assets/brands-2.png)

1. Los estándares de creación visual y de contenido ahora se rellenan automáticamente. Examine las diferentes pestañas para adaptar la información según sea necesario.

1. En **[!UICONTROL Estándares de creación de contenido]**, haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar otra directriz, ejemplo o exclusión.

   ![](assets/brands-3.png)

1. En **[!UICONTROL Estándares de creación visual]**, haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar otra directriz, ejemplo o exclusión.

1. Para agregar un ejemplo de imagen, haga clic en **[!UICONTROL Seleccionar imagen]**. También puede añadir cualquier perspectiva incorrecta identificada.

   ![](assets/brands-4.png)

1. Una vez configurada, haga clic en **[!UICONTROL Guardar]** y luego en **[!UICONTROL Publicar]** para que las directrices de marcas estén disponibles en el asistente de IA.

1. Para hacer modificaciones a tu marca publicada, haz clic en **[!UICONTROL Editar marca]**. Tenga en cuenta que esto crea una copia temporal en el modo de edición y reemplaza la versión activa una vez publicada.

   ![](assets/brands-8.png)

1. En el panel **[!UICONTROL Marcas]**, abra el menú avanzado haciendo clic en el icono ![](assets/do-not-localize/Smock_More_18_N.svg) para:

   * Ver marca
   * Editar
   * Duplicar
   * Publicar
   * Cancelar publicación
   * Eliminar

   ![](assets/brands-6.png)

Ahora se puede acceder a las directrices de marca desde la lista desplegable Marcas en el menú asistente de IA, lo que le permite generar contenido y recursos alineados con las especificaciones. [Más información sobre el asistente de IA](gs-generative.md)

![](assets/brands-7.png)
