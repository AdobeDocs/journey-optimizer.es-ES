---
title: Control de acceso basado en atributos
description: Obtenga información sobre el control de acceso basado en atributos
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: 61293a2ad45d30d24e1b38d8a5df81534dc19b40
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 2%

---

# Control de acceso basado en atributos {#attribute-based-access}

>[!IMPORTANT]
>
>El uso del control de acceso basado en atributos está actualmente restringido a clientes seleccionados y se implementará en todos los entornos en una versión futura.

El control de acceso basado en atributos (ABAC) permite definir autorizaciones para administrar el acceso a los datos de equipos o grupos de usuarios específicos. Su objetivo es proteger los activos digitales confidenciales de los usuarios no autorizados, lo que permite una mayor protección de los datos personales.

En Adobe Journey Optimizer, ABAC le permite proteger datos y conceder acceso específico a elementos de campo específicos, incluidos esquemas del Modelo de datos de experiencia (XDM), atributos de perfil y segmentos.

Para obtener una lista más detallada de la terminología utilizada con ABAC, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html).

En este ejemplo, queremos añadir una etiqueta a la variable **Nacionalidad** campo de esquema para restringir el uso de usuarios no autorizados. Para que esto funcione, debe realizar los siguientes pasos:

1. Cree una nueva  **[!UICONTROL Función]** y asígnelo con el  **[!UICONTROL Etiqueta]** para que los usuarios puedan acceder y utilizar el campo de esquema .

1. Asignar un  **[!UICONTROL Etiqueta]** a **Nacionalidad** campo de esquema en Adobe Experience Platform.

1. Utilice la variable  **[!UICONTROL Campo Esquema]** en Adobe Journey Optimizer.

Tenga en cuenta que **[!UICONTROL Funciones]**, **[!UICONTROL Políticas]** y **[!UICONTROL Productos]** también se puede acceder con la API de control de acceso basada en atributos. Para obtener más información, consulte esta [Documentación](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html).

## Crear una función y asignar etiquetas {#assign-role}

>[!IMPORTANT]
>
>Antes de administrar los permisos de una función, primero debe crear una directiva. Para obtener más información, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html).

**[!UICONTROL Funciones]** son un conjunto de usuarios que comparten los mismos permisos, etiquetas y entornos limitados dentro de su organización. Cada usuario que pertenece a un **[!UICONTROL Función]** tiene derecho a las aplicaciones y servicios de Adobe contenidos en el producto.
También puede crear su propio **[!UICONTROL Funciones]** si desea ajustar el acceso de los usuarios a determinadas funcionalidades u objetos de la interfaz.

Ahora queremos conceder a los usuarios seleccionados acceso al **Nacionalidad** campo, con la etiqueta C2. Para ello, necesitamos crear un **[!UICONTROL Función]** con un conjunto específico de usuarios y concederles la etiqueta C2 que les permite usar la variable **Nacionalidad** detalles en un **[!UICONTROL Recorrido]**.

1. En el [!DNL Permissions] producto, seleccione **[!UICONTROL Función]** en el menú del panel izquierdo y haga clic en **[!UICONTROL Crear función]**. Tenga en cuenta que también puede agregar **[!UICONTROL Etiqueta]** a funciones integradas.

   ![](assets/role_1.png)

1. Agregue un **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]** a su **[!UICONTROL Función]**, aquí: Función demográfica restringida.

1. En la lista desplegable , seleccione su **[!UICONTROL Sandbox]**.

   ![](assets/role_2.png)

1. En el **[!UICONTROL Recursos]** , haga clic en **[!UICONTROL Adobe Experience Platform]** para abrir las distintas funciones. Aquí, seleccionamos **[!UICONTROL Recorridos]**.

   ![](assets/role_3.png)

1. En la lista desplegable , seleccione la opción **[!UICONTROL Permisos]** vinculado a la función seleccionada, como **[!UICONTROL Ver recorridos]** o **[!UICONTROL Publicar recorridos]**.

   ![](assets/role_6.png)

1. Después de guardar el **[!UICONTROL Función]**, haga clic en **[!UICONTROL Propiedades]** para configurar aún más el acceso a su función.

   ![](assets/role_7.png)

1. En el **[!UICONTROL Usuarios]** , haga clic en **[!UICONTROL Agregar usuarios]**.

   ![](assets/role_8.png)

1. En el **[!UICONTROL Etiquetas]** , seleccione **[!UICONTROL Agregar etiqueta]**.

   ![](assets/role_9.png)

1. Seleccione el **[!UICONTROL Etiquetas]** desea agregar a la función y haga clic en **[!UICONTROL Guardar]**. Para este ejemplo, se concede la etiqueta C2 a los usuarios para que tengan acceso al campo del esquema previamente restringido.

   ![](assets/role_4.png)

Los usuarios de la variable **Función restringida demográfica** ahora tienen acceso a los objetos etiquetados con C2.

## Asignación de etiquetas a un objeto en Adobe Experience Platform {#assign-label}

>[!WARNING]
>
>Un uso incorrecto de las etiquetas puede dañar el acceso a las personas y las infracciones de la política de déclencheur.

**[!UICONTROL Etiquetas]** se puede utilizar para asignar áreas de funciones específicas mediante el control de acceso basado en atributos.
En este ejemplo, queremos restringir el acceso a la variable **Nacionalidad** campo . Este campo solo es accesible para los usuarios con el **[!UICONTROL Etiqueta]** a su  **[!UICONTROL Función]**.

Tenga en cuenta que también puede agregar  **[!UICONTROL Etiqueta]** a  **[!UICONTROL Esquema]**,  **[!UICONTROL Conjuntos de datos]** y  **[!UICONTROL Segmentos]**.

1. Cree su **[!UICONTROL Esquema]**. Para obtener más información, consulte [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=es).

   ![](assets/label_1.png)

1. En el **[!UICONTROL Esquema]**, primero agregamos la variable **[!UICONTROL Detalles demográficos]** grupo de campos que contiene la variable **Nacionalidad** campo .

   ![](assets/label_2.png)

1. En el **[!UICONTROL Etiquetas]** , compruebe el nombre del campo restringido, aquí **Nacionalidad**. A continuación, en el menú del panel derecho, seleccione **[!UICONTROL Editar etiquetas de control]**.

   ![](assets/label_3.png)

1. Seleccione el **[!UICONTROL Etiqueta]**, en este caso, el C2 - Data no se puede exportar a un tercero. Para obtener una lista detallada de las etiquetas disponibles, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html#contract-labels).

   ![](assets/label_4.png)

1. Personalice aún más el esquema si es necesario y luego actívelo. Para ver los pasos detallados sobre cómo habilitar el esquema, consulte esta [página](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#profile).

El campo del esquema ahora solo será visible y ahora solo lo pueden utilizar los usuarios que forman parte de un conjunto de funciones con la etiqueta C2.
Aplicando una **[!UICONTROL Etiqueta]** a su **[!UICONTROL Nombre del campo]**, tenga en cuenta que la variable **[!UICONTROL Etiqueta]** se aplicará automáticamente al **Nacionalidad** en cada esquema creado.

![](assets/label_5.png)

## Acceder a objetos etiquetados en Adobe Journey Optimizer {#attribute-access-ajo}

Después de etiquetar **Nacionalidad** nombre de campo en un nuevo esquema y nuestra nueva función, ahora podemos ver el impacto de esta restricción en Adobe Journey Optimizer.
Para nuestro ejemplo, un primer usuario X con acceso a objetos etiquetados como C2 creará un Recorrido con una condición que segmente el **[!UICONTROL Nombre del campo]**. Un segundo usuario Y sin acceso a objetos etiquetados como C2 tendrá que publicar el Recorrido.

1. Desde Adobe Journey Optimizer, primero debe configurar la variable **[!UICONTROL Fuente de datos]** con el nuevo esquema.

   ![](assets/journey_1.png)

1. Agregar una nueva **[!UICONTROL Grupo de campos]** de su **[!UICONTROL Esquema]** a la integración **[!UICONTROL Fuente de datos]**. También puede crear una nueva **[!UICONTROLDfuente de datos]** y asociados **[!UICONTROL Grupos de campo]**.

   ![](assets/journey_2.png)

1. Después de seleccionar el **[!UICONTROL Esquema]**, haga clic en **[!UICONTROL Editar]** de la variable **[!UICONTROL Campos]** categoría.

   ![](assets/journey_3.png)

1. Seleccione el **[!UICONTROL Nombre del campo]** desea segmentar. Aquí seleccionamos el **Nacionalidad** campo .

   ![](assets/journey_4.png)

1. A continuación, cree un Recorrido que envíe un correo electrónico a los usuarios con una nacionalidad específica. Agregue un **[!UICONTROL Evento]** entonces **[!UICONTROL Condición]**.

   ![](assets/journey_5.png)

1. Seleccione el **Nacionalidad** para comenzar a crear la expresión.

   ![](assets/journey_6.png)

1. Edite su **[!UICONTROL Condición]** para dirigirse a una población específica con la variable **Nacionalidad** campo .

   ![](assets/journey_7.png)

1. Personalice su recorrido según sea necesario, aquí agregamos un **[!UICONTROL Correo electrónico]** acción.

   ![](assets/journey_8.png)

Si el usuario Y sin acceso a la etiqueta C2 objetos necesita acceder a este recorrido con este campo restringido:

* El usuario Y no podrá usar el nombre de campo restringido porque no será visible.

* El usuario Y no podrá editar la expresión con el nombre de campo restringido en el modo avanzado. Aparecerá el siguiente error `The expression is invalid. Field is no longer available or you don't have enough permission to see it`.

* El usuario Y puede eliminar la expresión.

* El usuario Y no podrá probar el Recorrido.

* El usuario Y no podrá publicar el Recorrido.
