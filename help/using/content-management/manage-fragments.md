---
solution: Journey Optimizer
product: journey optimizer
title: Administrar fragmentos
description: Obtenga información sobre cómo administrar los fragmentos de contenido
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 1fc708e1-a993-4a2a-809c-c5dc08a4bae1
source-git-commit: c42fc1069e11b8e34b7477fc26ed8a6b4ef95ac7
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 27%

---

# Administrar fragmentos {#manage-fragments}

Para administrar los fragmentos, acceda a la lista de fragmentos desde el menú de la izquierda **[!UICONTROL Administración de contenido]** > **[!UICONTROL Fragmentos]**.

Se muestran todos los fragmentos que se crearon en la zona protegida actual: [del menú **[!UICONTROL Fragmentos]**](#create-fragments), o bien utilizando la opción [Guardar como fragmento](#save-as-fragment).

![](assets/fragment-list-filters.png)

Puede filtrar fragmentos según sus características:

* Estado (Borrador o Activo)
* Tipo (visual o expresión)
* Fecha de creación o modificación
* Estado (archivado o no)
* Etiquetas

También puede elegir mostrar todos los fragmentos o solo los elementos que el usuario actual ha creado o modificado.

Desde el botón **[!UICONTROL Más acciones]** situado junto a cada fragmento, puede:

* Duplique un fragmento.
* Use la opción **[!UICONTROL Explorar referencias]** para ver los recorridos, campañas o plantillas donde se usa. [Más información](#explore-references)
* Archivar un fragmento. [Más información](#archive-fragments)
* Editar las etiquetas de un fragmento [Aprenda a trabajar con etiquetas unificadas](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## Estados de los fragmentos

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="Nuevos estados de fragmentos"
>abstract="Al haberse introducido los estados “**Activo**” y “**Borrador**” con la versión de junio de Journey Optimizer, todos los fragmentos creados antes de esta versión tienen el estado “Borrador”, incluso si se utilizan en un recorrido o una campaña. Si realiza cualquier cambio en estos fragmentos, debe publicarlos para que tengan el estado “Activo” y propagar los cambios a las campañas y recorridos asociados. También debe crear una nueva versión del recorrido/campaña y publicarla. <br/>La publicación requiere el permiso de usuario para <a href="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manage">Publicar fragmento</a>."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manager" text="Más información sobre los permisos de fragmentos de contenido"

Los fragmentos pueden tener varios estados:

* **[!UICONTROL Borrador]**: el fragmento se está editando y no se ha aprobado.

* **[!UICONTROL Activo]**: el fragmento se aprobó y está activo. [Más información sobre cómo publicar un fragmento](../content-management/create-fragments.md#publish)

  Cuando se edita un fragmento activo, aparece un icono específico junto a su estado. Haga clic en este icono para abrir la versión de borrador del fragmento.

* **[!UICONTROL Publicación]**: el fragmento se aprobó y se está publicando.
* **[!UICONTROL Archivado]**: el fragmento se ha archivado. [Aprenda a archivar fragmentos](#archive-fragments)

>[!CAUTION]
>
>Al haberse introducido los estados “**Activo**” y “**Borrador**” con la versión de junio de Journey Optimizer, todos los fragmentos creados antes de esta versión tienen el estado “Borrador”, incluso si se utilizan en un recorrido o una campaña. Si realiza cualquier cambio en estos fragmentos, debe publicarlos para que tengan el estado “Activo” y propagar los cambios a las campañas y recorridos asociados. También debe crear una nueva versión del recorrido/campaña y publicarla. La publicación requiere el permiso de usuario [Fragmento de Publish](../administration/ootb-product-profiles.md#content-library-manager).

## Editar fragmentos {#edit-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="Actualización de fragmentos de las campañas"
>abstract="Esta campaña no se actualizará si publica cambios en el fragmento. Requiere que se publique una nueva versión para poder admitir la funcionalidad de actualización de fragmentos."

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="Actualización de fragmentos de los recorridos"
>abstract="Este recorrido no se actualizará si publica cambios en el fragmento. Requiere que se publique una nueva versión para poder admitir la funcionalidad de actualización de fragmentos."

Para editar un fragmento, siga los pasos a continuación.

1. Haga clic en el fragmento deseado de la lista **[!UICONTROL Fragmentos]**.

1. Las propiedades del fragmento se abren con una previsualización de su contenido.

1. Si el fragmento que se está editando tiene el estado **Activo**, haga clic en el botón **Modificar** para crear una versión de borrador del fragmento. La versión actual del fragmento seguirá activa hasta que publique la versión de borrador.

1. Realice los cambios deseados en el fragmento. Para editar su contenido, haga clic en el botón **Editar** y, a continuación, edite el contenido como lo haría al crear un fragmento desde cero. [Aprenda a crear un fragmento](#create-from-scratch)

   >[!NOTE]
   >
   >Al editar un fragmento de expresión, puede eliminar cualquier campo de personalización, pero no puede añadir nuevos al contenido del fragmento. Si desea agregar campos de personalización, duplique el fragmento para crear uno nuevo.

   También puede comprobar la lista de recorridos, campañas y plantillas de contenido donde se está utilizando el fragmento seleccionando la opción **Referencias del explorador**. [Más información](#explore-references)

   ![](assets/fragment-edit.png)

1. Una vez que los cambios estén listos, haz clic en el botón **Publish** para activar las modificaciones.

Al editar un fragmento, los cambios se propagan automáticamente a todo el contenido mediante ese fragmento, incluidos los recorridos activos y las campañas, excepto en el contenido en el que se ha roto la herencia del fragmento original. Aprenda a romper la herencia en las secciones [Agregar fragmentos visuales a los correos electrónicos](../email/use-visual-fragments.md#break-inheritance) y [Aprovechar fragmentos de expresiones](../personalization/use-expression-fragments.md#break-inheritance).

## Explorar referencias {#explore-references}

Puede mostrar la lista de los recorridos, campañas y plantillas de contenido que están utilizando actualmente un fragmento. Para ello, seleccione **[!UICONTROL Explorar referencias]** en el menú **[!UICONTROL Más acciones]** de la lista de fragmentos o en la pantalla de propiedades del fragmento.

![](assets/fragment-explore-references.png)

Seleccione una pestaña para alternar entre recorridos, campañas, plantillas y fragmentos. Puede ver su estado y hacer clic en un nombre para redirigirlo al elemento correspondiente donde se hace referencia al fragmento.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Si el fragmento se utiliza en un recorrido, campaña o plantilla que tenga una etiqueta que le impida acceder a él, verá un mensaje de alerta sobre la pestaña seleccionada. [Más información sobre el Control de acceso de nivel de objeto (OLAC)](../administration/object-based-access.md)

## Archivar fragmentos {#archive-fragments}

Puede limpiar la lista de fragmentos de los elementos que ya no son relevantes para su marca.

Para ello, haga clic en el botón **[!UICONTROL Más acciones]** que está junto al fragmento deseado y seleccione **[!UICONTROL Archivar]**. Desaparecerá de la lista de fragmentos, lo que impide que los usuarios lo utilicen en futuros correos electrónicos o plantillas.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Si archiva un fragmento que se usa en un contenido, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->ese contenido no se verá afectado.

Para desarchivar un fragmento, filtre los **[!UICONTROL elementos archivados]** y seleccione **[!UICONTROL Desarchivar]** del menú **[!UICONTROL Más acciones]**. Ahora vuelve a ser accesible desde la lista de fragmentos y se puede utilizar en cualquier correo electrónico o plantilla.

![](assets/fragment-list-unarchive.png)
