---
title: Control de acceso basado en atributos
description: Obtenga información sobre el control de acceso basado en atributos
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: f00d503ef5ea38b35b7f56821a9f523dca9fbb94
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 0%

---

# Control de acceso basado en atributos {#attribute-based-access}

>[!IMPORTANT]
>
>Actualmente, el uso del control de acceso basado en atributos está disponible en acceso anticipado solo para usuarios seleccionados. Si desea aprovechar esta función, póngase en contacto con el administrador de cuentas de Adobe.

El control de acceso basado en atributos (ABAC) permite definir autorizaciones para administrar el acceso a los datos de equipos o grupos de usuarios específicos. Su objetivo es proteger los activos digitales confidenciales de los usuarios no autorizados, lo que permite una mayor protección de los datos personales.

En Adobe Journey Optimizer, ABAC le permite proteger datos y conceder acceso específico a elementos de campo específicos, incluidos esquemas del Modelo de datos de experiencia (XDM), atributos de perfil y segmentos.

<!--For a more detailed list of the terminology used with ABAC, refer to Adobe Experience Platform documentation.-->

En este ejemplo, queremos añadir una etiqueta a la variable **Nacionalidad** campo de esquema para restringir el uso de usuarios no autorizados. Para que esto funcione, debe realizar los siguientes pasos:

1. Asignar un  **[!UICONTROL Label]** a **Nacionalidad** campo de esquema en Adobe Experience Platform.

2. Cree una nueva  **[!UICONTROL Role]** y asígnelo con el  **[!UICONTROL Label]** para que los usuarios puedan acceder y utilizar el campo de esquema .

3. Utilice la variable  **[!UICONTROL Schema field]** en Adobe Journey Optimizer.

## Asignación de etiquetas a un objeto en Adobe Experience Platform {#assign-label}

>[!WARNING]
>
>Un uso incorrecto de las etiquetas puede dañar el acceso a las personas y las infracciones de la política de déclencheur.

**[!UICONTROL Labels]** se puede utilizar para asignar áreas de funciones específicas mediante el control de acceso basado en atributos.
En este ejemplo, queremos restringir el acceso a la variable **Nacionalidad** campo . Este campo solo es accesible para los usuarios con el **[!UICONTROL Label]** a su  **[!UICONTROL Role]**.

Tenga en cuenta que también puede agregar  **[!UICONTROL Label]** a  **[!UICONTROL Schema]**,  **[!UICONTROL Datasets]** y  **[!UICONTROL Segments]**.

1. Cree su **[!UICONTROL Schema]**. Para obtener más información, consulte [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en).

   ![](assets/label_1.png)

1. En el **[!UICONTROL Schema]**, primero agregamos la variable **[!UICONTROL Demographic details]** grupo de campos que contiene la variable **Nacionalidad** campo .

   ![](assets/label_2.png)

1. En el **[!UICONTROL Labels]** , compruebe el nombre del campo restringido, aquí **Nacionalidad**. A continuación, en el menú del panel derecho, seleccione **[!UICONTROL Edit governance labels]**.

   ![](assets/label_3.png)

1. Seleccione el **[!UICONTROL Label]**, en este caso, el C2 - Data no se puede exportar a un tercero. Para obtener una lista detallada de las etiquetas disponibles, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html#contract-labels).

   ![](assets/label_4.png)

1. Personalice aún más el esquema si es necesario y luego actívelo. Para ver los pasos detallados sobre cómo habilitar el esquema, consulte esta [página](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#profile).

El campo del esquema ahora solo será visible y ahora solo lo pueden utilizar los usuarios que forman parte de un conjunto de funciones con la etiqueta C2.
Aplicando una **[!UICONTROL Label]** a su **[!UICONTROL Field name]**, tenga en cuenta que la variable **[!UICONTROL Label]** se aplicará automáticamente al **Nacionalidad** en cada esquema creado.

![](assets/label_5.png)

## Crear una función y asignar etiquetas {#assign-role}

**[!UICONTROL Roles]** son un conjunto de usuarios que comparten los mismos permisos, etiquetas y entornos limitados dentro de su organización. Cada usuario que pertenece a un **[!UICONTROL Role]** tiene derecho a las aplicaciones y servicios de Adobe contenidos en el producto.
También puede crear su propio **[!UICONTROL Roles]** si desea ajustar el acceso de los usuarios a determinadas funcionalidades u objetos de la interfaz.

Ahora queremos conceder a los usuarios seleccionados acceso al **Nacionalidad** campo, con la etiqueta C2. Para ello, necesitamos crear un **[!UICONTROL Role]** con un conjunto específico de usuarios y concederles la etiqueta C2 que les permite usar la variable **Nacionalidad** detalles en un **[!UICONTROL Message]** o **[!UICONTROL Journey]**.

1. En el [!DNL Permissions] producto, seleccione **[!UICONTROL Role]** en el menú del panel izquierdo y haga clic en **[!UICONTROL Create role]**. Tenga en cuenta que también puede agregar **[!UICONTROL Label]** a funciones integradas.

   ![](assets/role_1.png)

1. Agregue un **[!UICONTROL Name]** y **[!UICONTROL Description]** a su **[!UICONTROL Role]**, aquí: Función demográfica restringida.

1. En la lista desplegable , seleccione su **[!UICONTROL Sandbox]**.

   ![](assets/role_2.png)

1. En el **[!UICONTROL Resources]** , haga clic en **[!UICONTROL Adobe Experience Platform]** para abrir las distintas funciones. Aquí, seleccionamos **[!UICONTROL Messages]**.

   ![](assets/role_3.png)

1. En la lista desplegable , seleccione la opción **[!UICONTROL Permissions]** vinculado a la función seleccionada, como **[!UICONTROL View messages]** o **[!UICONTROL Publish journeys]**.

   ![](assets/role_6.png)

1. Después de guardar el **[!UICONTROL Role]**, haga clic en **[!UICONTROL Properties]** para configurar aún más el acceso a su función.

   ![](assets/role_7.png)

1. En la pestaña **[!UICONTROL Users]**, haga clic en **[!UICONTROL Add users]**.

   ![](assets/role_8.png)

1. En la pestaña **[!UICONTROL Labels]**, seleccione **[!UICONTROL Add label]**.

   ![](assets/role_9.png)

1. Seleccione el **[!UICONTROL Labels]** desea agregar a la función y haga clic en **[!UICONTROL Save]**. Para este ejemplo, se concede la etiqueta C2 a los usuarios para que tengan acceso al campo del esquema previamente restringido.

   ![](assets/role_4.png)

Los usuarios de la variable **Función restringida demográfica** ahora tienen acceso a los objetos etiquetados con C2.

## Acceder a objetos etiquetados en Adobe Journey Optimizer {#attribute-access-ajo}

Después de etiquetar **Nacionalidad** nombre de campo en un nuevo esquema y nuestra nueva función, ahora podemos ver el impacto de esta restricción en Adobe Journey Optimizer.
Para nuestro ejemplo, un primer usuario X con acceso a objetos etiquetados como C2 creará un Recorrido con una condición que segmente el **[!UICONTROL Field name]**. Un segundo usuario Y sin acceso a objetos etiquetados como C2 tendrá que publicar el Recorrido.

1. Desde Adobe Journey Optimizer, primero debe configurar la variable **[!UICONTROL Data source]** con el nuevo esquema.

   ![](assets/journey_1.png)

1. Agregar una nueva **[!UICONTROL Field group]** de su **[!UICONTROL Schema]** a la integración **[!UICONTROL Data source]**. También puede crear una nueva **[!UICONTROLDfuente de datos]** y asociados **[!UICONTROL Field groups]**.

   ![](assets/journey_2.png)

1. Después de seleccionar el **[!UICONTROL Schema]**, haga clic en **[!UICONTROL Edit]** de la variable **[!UICONTROL Fields]** categoría.

   ![](assets/journey_3.png)

1. Seleccione el **[!UICONTROL Field name]** desea segmentar. Aquí seleccionamos el **Nacionalidad** campo .

   ![](assets/journey_4.png)

1. A continuación, cree un Recorrido que envíe un mensaje a los usuarios con una nacionalidad específica. Agregue un **[!UICONTROL Event]** entonces **[!UICONTROL Condition]**.

   ![](assets/journey_5.png)

1. Seleccione el **Nacionalidad** para comenzar a crear la expresión.

   ![](assets/journey_6.png)

1. Edite su **[!UICONTROL Condition]** para dirigirse a una población específica con la variable **Nacionalidad** campo .

   ![](assets/journey_7.png)

1. Personalice su recorrido según sea necesario, aquí agregamos un **[!UICONTROL Message]** acción.

   ![](assets/journey_8.png)

Si el usuario Y sin acceso a los objetos C2 de la etiqueta necesita acceder a este recorrido o a cualquier mensaje con este campo restringido:

* El usuario Y no podrá usar el nombre de campo restringido porque no será visible.

* El usuario Y no podrá editar la expresión con el nombre de campo restringido en el modo avanzado. Aparecerá el siguiente error `The expression is invalid. Field is no longer available or you don't have enough permission to see it`.

* El usuario Y puede eliminar la expresión.

* El usuario Y no podrá probar el Recorrido o el mensaje.

* El usuario Y no podrá publicar el Recorrido o el mensaje.

