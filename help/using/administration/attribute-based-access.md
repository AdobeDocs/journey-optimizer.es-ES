---
solution: Journey Optimizer
product: journey optimizer
title: Control de acceso basado en atributos
description: El control de acceso basado en atributos (ABAC) permite definir autorizaciones para administrar el acceso a datos para equipos o grupos de usuarios específicos.
feature: Access Management
topic: Administration
role: Admin,Leader
level: Intermediate
keywords: abac, atributo, autorizaciones, datos, acceso, confidencial, recursos
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 2%

---

# Control de acceso basado en atributos {#attribute-based-access}

El control de acceso basado en atributos (ABAC) permite definir autorizaciones para administrar el acceso a datos para equipos o grupos de usuarios específicos. Su objetivo es proteger los activos digitales confidenciales de usuarios no autorizados, lo que permite una mayor protección de los datos personales.

En Adobe Journey Optimizer, ABAC le permite proteger datos y conceder acceso específico a elementos de campo específicos, incluidos esquemas del Modelo de datos de experiencia (XDM), atributos de perfil y audiencias.

Para obtener una lista más detallada de la terminología utilizada con ABAC, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html?lang=es).

En este ejemplo, queremos añadir una etiqueta a **Nacionalidad** Campo de esquema para restringir el uso de usuarios no autorizados. Para que esto funcione, debe realizar los siguientes pasos:

1. Crear un nuevo  **[!UICONTROL Rol]** y asignarlo con el correspondiente  **[!UICONTROL Etiqueta]** para que los usuarios puedan acceder y utilizar el campo de esquema.

1. Asignar un  **[!UICONTROL Etiqueta]** a la **Nacionalidad** Campo de esquema en Adobe Experience Platform.

1. Utilice el  **[!UICONTROL Campo de esquema]** en Adobe Journey Optimizer.

Tenga en cuenta que **[!UICONTROL Funciones]**, **[!UICONTROL Políticas]** y **[!UICONTROL Productos]** también se puede acceder a con la API de control de acceso basada en atributos. Para obtener más información, consulte esta [Documentación](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html).

## Crear una función y asignar etiquetas {#assign-role}

>[!IMPORTANT]
>
>Antes de administrar permisos para una función, primero deberá crear una directiva. Para obtener más información, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html).

**[!UICONTROL Funciones]** son un conjunto de usuarios que comparten los mismos permisos, etiquetas y zonas protegidas dentro de la organización. Cada usuario que pertenece a un **[!UICONTROL Rol]** tiene derecho a las aplicaciones y servicios de Adobe contenidos en el producto.
También puede crear su propio **[!UICONTROL Funciones]** si desea ajustar el acceso de los usuarios a determinadas funcionalidades u objetos de la interfaz.

Ahora queremos otorgar a los usuarios seleccionados acceso al **Nacionalidad** campo, etiquetado como C2. Para ello, es necesario crear un nuevo **[!UICONTROL Rol]** con un conjunto específico de usuarios y concederles la etiqueta C2, que les permite utilizar el **Nacionalidad** detalles en una **[!UICONTROL Recorrido]**.

1. Desde el [!DNL Permissions] producto, seleccione **[!UICONTROL Rol]** en el menú del panel izquierdo y haga clic en **[!UICONTROL Crear función]**. Tenga en cuenta que también puede añadir **[!UICONTROL Etiqueta]** a las funciones integradas.

   ![](assets/role_1.png)

1. Añadir un **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]** a su nuevo **[!UICONTROL Rol]**, aquí: Grupo demográfico de funciones restringido.

1. En la lista desplegable, seleccione su **[!UICONTROL Sandbox]**.

   ![](assets/role_2.png)

1. Desde el **[!UICONTROL Recursos]** , haga clic en **[!UICONTROL Adobe Experience Platform]** para abrir las distintas funcionalidades. Aquí, seleccionamos **[!UICONTROL Recorridos]**.

   ![](assets/role_3.png)

1. En la lista desplegable, seleccione **[!UICONTROL Permisos]** vinculado a la función seleccionada, como **[!UICONTROL Ver recorridos]** o **[!UICONTROL Publicar recorridos]**.

   ![](assets/role_6.png)

1. Después de guardar el recién creado **[!UICONTROL Rol]**, haga clic en **[!UICONTROL Propiedades]** para configurar aún más el acceso a su función.

   ![](assets/role_7.png)

1. Desde el **[!UICONTROL Usuarios]** pestaña, haga clic en **[!UICONTROL Adición de usuarios]**.

   ![](assets/role_8.png)

1. Desde el **[!UICONTROL Etiquetas]** pestaña, seleccione **[!UICONTROL Añadir etiqueta]**.

   ![](assets/role_9.png)

1. Seleccione el **[!UICONTROL Etiquetas]** desea agregar a su función y haga clic en **[!UICONTROL Guardar]**. Para este ejemplo, concedemos la etiqueta C2 para que los usuarios tengan acceso al campo del esquema restringido anteriormente.

   ![](assets/role_4.png)

Los usuarios de **Demografía de la función restringida** Las funciones de ahora tienen acceso a los objetos etiquetados de C2.

## Asignación de etiquetas a un objeto en Adobe Experience Platform {#assign-label}

>[!WARNING]
>
>El uso incorrecto de las etiquetas puede interrumpir el acceso a las personas y las infracciones de las directivas de déclencheur.

**[!UICONTROL Etiquetas]** se puede utilizar para asignar áreas de funciones específicas mediante el control de acceso basado en atributos.
En este ejemplo, queremos restringir el acceso a **Nacionalidad** field. Este campo solo será accesible para los usuarios con el correspondiente **[!UICONTROL Etiqueta]** a su  **[!UICONTROL Rol]**.

Tenga en cuenta que también puede añadir  **[!UICONTROL Etiqueta]** hasta  **[!UICONTROL Esquema]**,  **[!UICONTROL Conjuntos de datos]** y  **[!UICONTROL Audiencias]**.

1. Cree su **[!UICONTROL Esquema]**. Para obtener más información, consulte [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=es).

   ![](assets/label_1.png)

1. En el recién creado **[!UICONTROL Esquema]**, primero agregamos el **[!UICONTROL Datos demográficos]** grupo de campos que contiene **Nacionalidad** field.

   ![](assets/label_2.png)

1. Desde el **[!UICONTROL Etiquetas]** pestaña, compruebe el nombre del campo restringido, aquí **Nacionalidad**. A continuación, en el menú del panel derecho, seleccione **[!UICONTROL Editar etiquetas de gobernanza]**.

   ![](assets/label_3.png)

1. Seleccione el correspondiente **[!UICONTROL Etiqueta]**, en este caso, los datos de C2 no se pueden exportar a terceros. Para obtener la lista detallada de las etiquetas disponibles, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html#contract-labels).

   ![](assets/label_4.png)

1. Personalice aún más el esquema si es necesario y, a continuación, actívelo. Para ver los pasos detallados sobre cómo habilitar el esquema, consulte esto [página](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#profile).

El campo del esquema ahora solo estará visible y ahora solo lo pueden utilizar los usuarios que formen parte de un conjunto de funciones con la etiqueta C2.
Mediante la aplicación de un **[!UICONTROL Etiqueta]** a su **[!UICONTROL Nombre de campo]**, tenga en cuenta que la variable **[!UICONTROL Etiqueta]** se aplicará automáticamente al **Nacionalidad** en cada esquema creado.

![](assets/label_5.png)

## Acceso a objetos etiquetados en Adobe Journey Optimizer {#attribute-access-ajo}

Después de etiquetar nuestro **Nacionalidad** nombre de campo en un nuevo esquema y nuestra nueva función, ahora podemos ver el impacto de esta restricción en Adobe Journey Optimizer.
Para nuestro ejemplo, un primer usuario X con acceso a objetos etiquetados como C2 creará un Recorrido con una condición dirigida a los restringidos **[!UICONTROL Nombre de campo]**. Un segundo usuario Y sin acceso a los objetos etiquetados como C2 tendrá que publicar el Recorrido.

1. Desde Adobe Journey Optimizer, primero debe configurar las **[!UICONTROL Fuente de datos]** con su nuevo esquema.

   ![](assets/journey_1.png)

1. Añadir un nuevo **[!UICONTROL Grupo de campos]** de los recién creados **[!UICONTROL Esquema]** a la versión integrada **[!UICONTROL Fuente de datos]**. También puede crear un nuevo **[!UICONTROL fuente de datos]** y asociados **[!UICONTROL Grupos de campos]**.

   ![](assets/journey_2.png)

1. Después de seleccionar el creado anteriormente **[!UICONTROL Esquema]**, haga clic en **[!UICONTROL Editar]** desde el **[!UICONTROL Campos]** categoría.

   ![](assets/journey_3.png)

1. Seleccione el **[!UICONTROL Nombre de campo]** que desea segmentar. Aquí seleccionamos el restringido **Nacionalidad** field.

   ![](assets/journey_4.png)

1. A continuación, cree un Recorrido que envíe un correo electrónico a los usuarios con una nacionalidad específica. Añadir un **[!UICONTROL Evento]** y luego un **[!UICONTROL Condición]**.

   ![](assets/journey_5.png)

1. Seleccione el restringido **Nacionalidad** para empezar a crear la expresión.

   ![](assets/journey_6.png)

1. Edite su **[!UICONTROL Condición]** para dirigirse a una población específica con el **Nacionalidad** field.

   ![](assets/journey_7.png)

1. Personalice su recorrido según sea necesario. Aquí agregamos una **[!UICONTROL Correo electrónico]** acción.

   ![](assets/journey_8.png)

Si el usuario Y sin acceso a los objetos de la etiqueta C2 necesita acceder a este recorrido con este campo restringido:

* El usuario Y no podrá utilizar el nombre de campo restringido, ya que no será visible.

* El usuario Y no podrá editar la expresión con el nombre de campo restringido en modo avanzado. Aparecerá el siguiente error `The expression is invalid. Field is no longer available or you don't have enough permission to see it`.

* El usuario Y puede eliminar la expresión.

* El usuario Y no podrá probar el Recorrido.

* El usuario Y no podrá publicar el Recorrido.
