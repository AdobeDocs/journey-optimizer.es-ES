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
TQID: https://experienceleague.adobe.com/Fni-bz0ax4B4q2wm87B7bfNXmybwfAyCu-ewclLwSCw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
subfeature_v2:
  - id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
  - id: cfdf3a89-7087-4a5c-a6d2-2f4eb64a3470
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: c46ce04b47a3576e6373cbe788f2bbccf6ddbed0
workflow-type: tm+mt
source-wordcount: 1205
ht-degree: 5%

---

# Administración de usuarios y funciones {#manage-permissions}

>[!BEGINSHADEBOX]

**En esta página:** Asigne, edite y cree funciones en el producto Permisos para que pueda proporcionar a cada usuario exactamente el acceso que necesita para realizar su trabajo en Journey Optimizer.

>[!ENDSHADEBOX]

**[!UICONTROL Los roles]** hacen referencia a una colección de usuarios que comparten los mismos permisos y zonas protegidas. Estas funciones le permiten administrar fácilmente el acceso y los permisos para diferentes grupos de usuarios dentro de su organización.

Con el producto [!DNL Journey Optimizer], puede elegir entre una serie de **[!UICONTROL roles]** preexistentes, cada uno con diferentes niveles de permisos, para asignarlos a los usuarios. Para obtener más información sobre los **[!UICONTROL roles]** disponibles, consulte esta [página](ootb-product-profiles.md).

Cuando un usuario pertenece a un **[!UICONTROL Rol]**, obtiene acceso a las aplicaciones y los servicios de Adobe contenidos en el producto.

Si las funciones preexistentes no satisfacen las necesidades específicas de su organización, también puede crear **[!UICONTROL funciones]** personalizadas para ajustar el acceso a ciertas funcionalidades u objetos de la interfaz. De este modo, se asegura de que cada usuario tenga acceso únicamente a los recursos y las herramientas que necesita para realizar sus tareas de forma eficaz.


>[!IMPORTANT]
>
>Los pasos y procedimientos detallados a continuación solamente los puede realizar un administrador de **[!UICONTROL Product]** o **[!UICONTROL System]**.


## Asignar un rol {#assigning-role}

Puede asignar una **[!UICONTROL función]** predeterminada o personalizada a los usuarios.

La lista de todas las funciones predeterminadas con permisos asignados está disponible en la sección [Funciones integradas](ootb-product-profiles.md).

Para asignar un **[!UICONTROL rol]**:

1. Para asignar una función a un usuario en el producto [!DNL Permissions], vaya a la pestaña **[!UICONTROL Funciones]** y seleccione la función que desee.

   ![](assets/do-not-localize/access_control_2.png)

1. En la pestaña **[!UICONTROL Usuarios]**, haga clic en **[!UICONTROL Añadir usuario]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Escriba el nombre o la dirección de correo electrónico del usuario o selecciónelo en la lista y haga clic en **[!UICONTROL Guardar]**.

   Si el usuario no se creó anteriormente en [!DNL Admin Console], consulte la [Documentación para agregar usuarios](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/users.html?lang=es){target="_blank"}.

   ![](assets/do-not-localize/access_control_4.png)

El usuario recibe un correo electrónico que lo redirige a su instancia.

Para obtener más información sobre la administración de usuarios, consulte la [documentación de control de acceso](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=es){target="_blank"}.

Al acceder a la instancia, el usuario ve una vista específica según los permisos asignados en la **[!UICONTROL función]**. Si el usuario no tiene el acceso correcto a una función, aparece el siguiente mensaje:

`You do not have permission to access this feature. Permission needed: XX.`

## Editar una función existente {#edit-product-profile}

Para los **[!UICONTROL roles]** integrados o personalizados, puede decidir en cualquier momento agregar o eliminar permisos.

En el ejemplo siguiente, queremos agregar **[!UICONTROL Permisos]** relacionados con el recurso **[!UICONTROL Recorridos]** para los usuarios asignados al visor de Recorrido **[!UICONTROL Rol]**. Los usuarios podrán entonces publicar recorridos.

>[!IMPORTANT]
>
>Los cambios realizados en una función integrada o personalizada afectarán a todos los usuarios asignados a esa función.

1. Para editar un rol en el producto [!DNL Permissions], vaya a la pestaña **[!UICONTROL Roles]** y seleccione el rol que desee, aquí el visualizador de Recorrido **[!UICONTROL Rol]**.
   ![](assets/do-not-localize/access_control_5.png)

1. En el panel **[!UICONTROL Rol]**, haga clic en **[!UICONTROL Editar]**.

   ![](assets/do-not-localize/access_control_6.png)

1. El menú **[!UICONTROL Recursos]** muestra la lista de recursos que se aplican al producto **[!UICONTROL Experience Cloud - Aplicaciones con plataforma]**. Arrastre y suelte los recursos para asignar permisos.

   Del menú desplegable de recursos **[!UICONTROL Recorridos]**, elegimos aquí el recorrido de publicación **[!UICONTROL Permiso]**.

   ![](assets/do-not-localize/access_control_14.png)

1. Si es necesario, en **[!UICONTROL Elementos de permisos incluidos]**, haga clic en el icono X para quitar permisos o recursos de la función.

1. Cuando termine, haga clic en **[!UICONTROL Guardar]**.

Si es necesario, también puede crear una función nueva con permisos específicos.

## Crear una nueva función {#create-product-profile}

[!DNL Journey Optimizer] le permite crear sus propios **[!UICONTROL roles]** y asignar un conjunto de permisos y zonas protegidas a los usuarios. Con **[!UICONTROL Roles]**, puede autorizar o denegar el acceso a determinadas funcionalidades u objetos de la interfaz.

Para obtener más información sobre cómo crear y administrar zonas protegidas, consulte la documentación de [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=es){target="_blank"}.

En este ejemplo, creamos una función denominada **Recorridos de solo lectura**, donde concedemos derechos de solo lectura a la función de Recorrido. Los usuarios solamente podrán acceder y ver recorridos y no podrán acceder a otras características como **[!DNL Decision management]** en [!DNL Journey Optimizer].

Para crear nuestros **Recorridos de solo lectura** **[!UICONTROL Rol]**:

1. Para asignar una función a un usuario en el producto [!DNL Permissions], vaya a la pestaña **[!UICONTROL Funciones]** y haga clic en **[!UICONTROL Crear función]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Agregue un **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]** para su nuevo **[!UICONTROL Rol]**. A continuación, haga clic en **[!UICONTROL Confirmar]**.

   ![](assets/do-not-localize/access_control_10.png)

1. En la lista desplegable de recursos de **[!UICONTROL espacio aislado]**, elija qué espacio aislado asignar a su **[!UICONTROL rol]**. [Obtenga más información sobre las zonas protegidas](sandboxes.md).

   ![](assets/do-not-localize/access_control_13.png)

1. Seleccione entre los diferentes recursos como **[!DNL Journeys]**, **[!DNL Segments]** o **[!DNL Decision management]** disponibles en [!DNL Journey Optimizer] que se muestran en el menú de la izquierda.

   Aquí seleccionamos el recurso **[!UICONTROL Recorridos]**.

   ![](assets/do-not-localize/access_control_11.png)

1. En la lista desplegable **[!UICONTROL Recorridos]**, seleccione los permisos que desea asignar a su **[!UICONTROL rol]**.

   Aquí seleccionamos **[!DNL View journeys]**, **[!DNL View journeys report]** y **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Cuando termine, haga clic en **[!UICONTROL Guardar]**.

Su **[!UICONTROL función]** se ha creado y configurado. Ahora debe asignarlo a los usuarios.

Para obtener más información sobre la creación y administración de funciones, consulte la [documentación de Adobe Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html?lang=es){target="_blank"}.

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

- **TL;DR:** Esta página muestra a los administradores de productos y sistemas las tres tareas de administración de funciones del producto Permisos: asignar una función existente a un usuario, editar los permisos de una función y crear una nueva función personalizada con permisos específicos y zonas protegidas.

**Intenciones:**

- Asignar una función integrada o personalizada a un usuario en Journey Optimizer
- Editar los permisos de una función existente (agregar o quitar derechos)
- Crear una nueva función personalizada con permisos específicos y asignaciones de zona protegida
- Comprender quién tiene la autoridad para realizar la administración de funciones y permisos

**Glosario:**

- **Función**: una colección de usuarios que comparten los mismos permisos y zonas protegidas, que se usan para administrar el acceso dentro de una organización *(específica del producto)*
- **Producto de permisos**: Interfaz de Adobe CX Enterprise (a la que se accede a través de [!DNL Permissions]) donde las funciones, los permisos y las zonas protegidas están configurados *(específico del producto)*
- **Función integrada**: una función preexistente con un conjunto de permisos definido disponible para su asignación inmediata sin la configuración personalizada *(específica del producto)*

**Protecciones:**

- Solo los administradores de productos o sistemas pueden asignar, editar o crear funciones (requisito previo estricto, como se indica en la nota importante de la página)
- Los cambios realizados en una función integrada o personalizada afectarán a todos los usuarios asignados a esa función (como se indica en la nota importante de la página)

**Terminología:**

- Nombre canónico: Producto Permisos — variantes: Permisos de Adobe, IU de permisos, Permisos empresariales de Adobe CX
- No confunda: &quot;Asignar una función&quot; (agregar un usuario a una función existente) ≠ &quot;Crear una función&quot; (definir una nueva función con sus propios permisos y zonas protegidas desde cero)
- No confunda: &quot;Editar una función existente&quot; (modificar permisos o zonas protegidas en una función existente; afecta a todos los usuarios asignados) ≠ &quot;Crear una nueva función&quot; (crear una nueva función sin afectar a ninguna función existente ni a sus usuarios)

**PREGUNTAS MÁS FRECUENTES:**

- **Q: ¿Quién puede asignar roles a los usuarios en Journey Optimizer?** — Solo los administradores de productos o sistemas.
- **Q: ¿Qué sucede si edito los permisos de una función integrada?** — Los cambios afectarán a todos los usuarios asignados actualmente a ese rol.
- **Q: ¿Dónde debo ir en el producto para administrar los roles?** — en el producto Permisos, vaya a la ficha Funciones.
- **Q: después de asignar un rol, ¿recibe el usuario una notificación?** — Sí; el usuario recibe automáticamente un correo electrónico que le redirige a la instancia.

+++
<!-- ai-accordion-version: 1 | source-hash: 09d3612e -->
