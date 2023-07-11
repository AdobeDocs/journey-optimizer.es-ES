---
solution: Journey Optimizer
product: journey optimizer
title: Administración de usuarios y funciones
description: Obtenga información sobre cómo administrar usuarios y funciones
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: producto, perfiles, zona protegida
source-git-commit: 6a81760170e53ed9c34142f3b0b367bd62c3464c
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 8%

---

# Administración de usuarios y funciones {#manage-permissions}

>[!IMPORTANT]
>
> Cada uno de los procedimientos detallados a continuación solo se puede llevar a cabo mediante una **[!UICONTROL Product]** o **[!UICONTROL Sistema]** administrador. Para obtener más información, consulte la [Documentación de Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Funciones]** consulte una colección de usuarios que comparten los mismos permisos y entornos limitados. Estas funciones le permiten administrar fácilmente el acceso y los permisos para diferentes grupos de usuarios dentro de su organización.

Con el [!DNL Journey Optimizer] producto, tiene la capacidad de elegir entre una gama de productos preexistentes **[!UICONTROL Funciones]**, cada uno con diferentes niveles de permisos, para asignarlos a los usuarios. Para obtener más información sobre los **[!UICONTROL Funciones]**, consulte esta [página](ootb-product-profiles.md).

Cuando un usuario pertenece a un **[!UICONTROL Rol]**, se les concede acceso a las aplicaciones y servicios de Adobe contenidos en el producto.

Si las funciones preexistentes no satisfacen las necesidades específicas de su organización, también puede crear funciones personalizadas **[!UICONTROL Funciones]** para ajustar el acceso a ciertas funcionalidades u objetos de la interfaz. De este modo, puede asegurarse de que cada usuario tenga acceso únicamente a los recursos y las herramientas que necesita para realizar sus tareas de forma eficaz.

## Asignar un rol {#assigning-role}

Puede elegir asignar un de forma predeterminada o personalizado **[!UICONTROL Rol]** a sus usuarios.

La lista de todas las funciones integradas con permisos asignados se encuentra en el [Funciones integradas](ootb-product-profiles.md) sección.

Para asignar un **[!UICONTROL Rol]**:

1. Para asignar una función a un usuario en [!DNL Permissions] producto, vaya a la **[!UICONTROL Funciones]** y seleccione la función que desee.

   ![](assets/do-not-localize/access_control_2.png)

1. Desde el **[!UICONTROL Usuarios]** pestaña, haga clic en **[!UICONTROL Agregar usuario]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Escriba el nombre o la dirección de correo electrónico del usuario o seleccione el usuario en la lista y haga clic en **[!UICONTROL Guardar]**.

   Si el usuario no se ha creado anteriormente en [!DNL Admin Console], consulte la [Documentación de Adición de usuarios](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

El usuario debería recibir entonces un correo electrónico que le redirija a su instancia.

Para obtener más información sobre la administración de usuarios, consulte la [Documentación del Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Al acceder a la instancia, el usuario verá una vista específica en función de los permisos asignados en la variable **[!UICONTROL Rol]**. Si el usuario no tiene acceso correcto a una función, aparecerá el siguiente mensaje:

`You don't have permission to access this feature. Permission needed: XX.`

## Editar una función existente {#edit-product-profile}

Para la configuración predeterminada o personalizada **[!UICONTROL Funciones]**, puede decidir en cualquier momento agregar o eliminar permisos.

En este ejemplo, queremos añadir **[!UICONTROL Permisos]** relacionadas con la **[!UICONTROL Recorridos]** recurso para usuarios asignados al visor de Recorrido **[!UICONTROL Rol]**. Los usuarios podrán entonces publicar recorridos.

Tenga en cuenta que si modifica una configuración predeterminada o personalizada **[!UICONTROL Rol]**, afectará a todos los usuarios asignados a esto **[!UICONTROL Rol]**.

1. Para asignar una función a un usuario en [!DNL Permissions] producto, vaya a la **[!UICONTROL Funciones]** y seleccione la función que desee, aquí el visor de Recorridos **[!UICONTROL Rol]**.
   ![](assets/do-not-localize/access_control_5.png)

1. De su **[!UICONTROL Rol]** panel, haga clic en **[!UICONTROL Editar]**.

   ![](assets/do-not-localize/access_control_6.png)

1. El **[!UICONTROL Recursos]** El menú muestra la lista de recursos que se aplican al **[!UICONTROL Experience Cloud: aplicaciones con tecnología de plataforma]** producto. Arrastre y suelte los recursos para asignar permisos.

   Desde el **[!UICONTROL Recorridos]** Menú desplegable de recursos, elegimos aquí el recorrido Publicar **[!UICONTROL Permiso]**.

   ![](assets/do-not-localize/access_control_14.png)

1. Si es necesario, en **[!UICONTROL Elementos de permisos incluidos]**, haga clic en el icono X junto a para quitar permisos o recursos a la función.

1. Cuando termine, haga clic en **[!UICONTROL Guardar]**.

Si es necesario, también puede crear una nueva función con permisos específicos. Para obtener más información, consulte [Crear una función nueva](#create-product-profile).

## Crear una nueva función {#create-product-profile}

[!DNL Journey Optimizer] le permite crear su propio **[!UICONTROL Funciones]** y asigne un conjunto de permisos y entornos limitados a los usuarios. Con **[!UICONTROL Funciones]**, puede autorizar o denegar el acceso a determinadas funcionalidades u objetos de la interfaz.

Para obtener más información sobre cómo crear y administrar zonas protegidas, consulte la documentación de [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=es){target="_blank"}.

En este ejemplo, crearemos una función denominada **Recorridos de solo lectura** donde concederemos derechos de solo lectura a la función Recorrido. Los usuarios solo podrán acceder y ver los recorridos, y no podrán acceder a otras funciones, como **[!DNL  Decision management]** in [!DNL Journey Optimizer].

Para crear su **Recorridos de solo lectura** **[!UICONTROL Rol]**:

1. Para asignar una función a un usuario en [!DNL Permissions] producto, vaya a la **[!UICONTROL Funciones]** y haga clic en **[!UICONTROL Crear función]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Añadir un **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]** para su nuevo **[!UICONTROL Rol]**. A continuación, haga clic en **[!UICONTROL Confirmar]**.

   ![](assets/do-not-localize/access_control_10.png)

1. Desde el **[!UICONTROL Sandbox]** menú desplegable de recursos, elija qué simulador de pruebas desea asignar a su **[!UICONTROL Rol]**. [Obtenga más información sobre las zonas protegidas](sandboxes.md).

   ![](assets/do-not-localize/access_control_13.png)

1. Seleccione entre los distintos recursos, como **[!DNL Journeys]**, **[!DNL Segments]** o **[!DNL Decision management]** disponible en [!DNL Journey Optimizer] aparece en el menú de la izquierda.

   Aquí se selecciona la **[!UICONTROL Recorridos]** recurso.

   ![](assets/do-not-localize/access_control_11.png)

1. Desde el **[!UICONTROL Recorridos]** , seleccione los permisos que desea asignar a su **[!UICONTROL Rol]**.

   Aquí seleccionamos **[!DNL View journeys]**, **[!DNL View journeys report]**  y **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Cuando termine, haga clic en **[!UICONTROL Guardar]**.

Su **[!UICONTROL Rol]** ahora se crea y configura. Ahora debe asignarlo a los usuarios.

Para obtener más información sobre la creación y administración de funciones, consulte la [Documentación del Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html?lang=es).
