---
solution: Journey Optimizer
product: journey optimizer
title: Administrar marca
description: Aprenda a crear y administrar las directrices de marca
badge: label="Beta" type="Informative"
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 6c99d733b973efd790f8727bf867fbf0a952f6d9
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 24%

---

# Crear y administrar sus marcas {#brands}

>[!AVAILABILITY]
>
>Esta capacidad se presenta como una versión beta privada. Estará disponible de forma progresiva para todos los clientes en futuras versiones.

Las directrices de marca son un conjunto detallado de reglas y estándares que establecen la identidad visual y verbal de una marca. Actúan como referencia para mantener una representación de marca coherente en todas las plataformas de marketing y comunicación.

<!--Upload feature currently behind feature flag--

In [!DNL Journey Optimizer], you now have the option to manually input and organize your brand details or upload brand guideline documents for automatic information extraction.-->

## Acceso a marcas {#generative-access}

Para tener acceso al menú **[!UICONTROL Marcas]** en [!DNL Adobe Journey Optimizer], los usuarios necesitan que se les conceda el **[!UICONTROL kit de marca administrado]** o los permisos de **[!UICONTROL Habilitar el asistente de IA]**. [Más información](../administration/permissions.md)

+++  Aprenda a asignar permisos relacionados con la marca

1. En el producto **Permisos**, vaya a la pestaña **Funciones** y seleccione la **Función** que desee.

1. Haga clic en **Editar** para modificar los permisos.

1. Agregue el recurso **Asistente de IA** y, a continuación, seleccione **Kit de marca administrado** o **[!UICONTROL Habilitar el asistente de IA]** en el menú desplegable.

   Tenga en cuenta que el permiso **[!UICONTROL Habilitar el asistente de IA]** solo proporciona acceso de solo lectura al menú **[!UICONTROL Marcas]**.

   ![](assets/brands-permission.png){zoomable="yes"}

1. Haga clic en **Guardar** para aplicar los cambios.

   Los permisos de los usuarios que ya estén asignados a esta función se actualizarán automáticamente.

1. Para asignar esta función a nuevos usuarios, vaya a la pestaña **Usuarios** en el panel de control **Funciones** y haga clic en **Añadir usuario**.

1. Introduzca el nombre del usuario y su dirección de correo electrónico, o selecciónelo en la lista, y haga clic en **Guardar**.

1. Si el usuario no estaba ya creado, consulte [esta documentación](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/abac/permissions-ui/users).

+++

## Cree su marca {#create-brand-kit}

Para crear y administrar las directrices de marca, siga los pasos a continuación.

<!--Upload feature currently behind feature flag--

To create and manage your Brand guideline, you can either enter the details yourself, or upload your brand guidelines document to have the information extracted automatically:-->

1. En el menú **[!UICONTROL Marcas]**, haga clic en **[!UICONTROL Crear marca]**.

   ![](assets/brands-1.png)

1. Escriba un **[!UICONTROL Nombre]** para su marca<!--and a **[!UICONTROL Description]** to your brand guideline-->.

   ![](assets/brands-2-temp.png)

<!--Upload feature currently behind feature flag so hidden from doc - should be available again by EOM (Feb)--

1. Drag and drop or select your file to upload your brand guidelines and extract automatically relevant brand information. Click **[!UICONTROL Create brand]**.

    The information extraction process now begins. Note that it may take several minutes to complete.

    ![](assets/brands-2.png)

1. Your Content and visual creation standards are now automatically populated. Browse through the different tabs to adapt the information as needed.

-->

1. En la ficha **[!UICONTROL Estilo de escritura]**, haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar una directriz o exclusión, incluidos ejemplos.

   ![](assets/brands-3.png)

1. En la ficha **[!UICONTROL Contenido visual]**, haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar otra directriz o exclusión.

1. Para agregar una imagen que muestre el uso correcto, seleccione **[!UICONTROL Ejemplo]** y haga clic en **[!UICONTROL Seleccionar imagen]**. También puede añadir una imagen que muestre un uso incorrecto como ejemplo de exclusión.

   ![](assets/brands-4.png)

1. Una vez configurada, haz clic en **[!UICONTROL Guardar]** y luego en **[!UICONTROL Publicar]** para que la guía de marca esté disponible en el asistente de IA.

1. Para hacer modificaciones a tu marca publicada, haz clic en **[!UICONTROL Editar marca]**.

   >[!NOTE]
   >
   >Esto crea una copia temporal en el modo de edición y reemplaza la versión activa una vez publicada.

   ![](assets/brands-8.png)

1. En el panel **[!UICONTROL Marcas]**, abra el menú avanzado haciendo clic en el icono ![](assets/do-not-localize/Smock_More_18_N.svg) para:

   * Ver marca
   * Editar
   * Duplicar
   * Publicar
   * Cancelar publicación
   * Eliminar

   ![](assets/brands-6.png)

Ahora se puede acceder a las directrices de marca desde la lista desplegable **[!UICONTROL Marca]** del menú del asistente de IA, lo que le permite generar contenido y recursos alineados con las especificaciones. [Más información sobre el asistente de IA](gs-generative.md)

![](assets/brands-7.png)
