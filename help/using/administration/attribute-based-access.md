---
solution: Journey Optimizer
product: journey optimizer
title: Control de acceso basado en atributos
description: El control de acceso basado en atributos permite definir autorizaciones para administrar el acceso a datos para equipos o grupos de usuarios específicos.
feature: Access Management
topic: Administration
role: Admin,Leader
level: Intermediate
keywords: abac, atributo, autorizaciones, datos, acceso, confidencial, recursos
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: 1a2c6e97fcd30245cff1bf08fd5771ce8bc84ddc
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 2%

---

# Control de acceso basado en atributos {#attribute-based-access}

La capacidad de control de acceso basado en atributos le permite definir autorizaciones para administrar el acceso a datos para equipos o grupos de usuarios específicos. Su objetivo es proteger los activos digitales confidenciales de usuarios no autorizados, lo que proporciona una mayor protección de los datos personales.

Utilice el control de acceso basado en atributos en Adobe Journey Optimizer para proteger datos y conceder acceso específico a elementos de campo específicos, incluidos esquemas XDM (Experience Data Model), atributos de perfil y audiencias.

Para obtener una lista más detallada de la terminología utilizada con el control de acceso basado en atributos, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html?lang=es){target="_blank"}.

En este ejemplo, se agrega una etiqueta al campo de esquema **Nationality** para impedir que lo utilicen usuarios no autorizados. Para que esto funcione, realice los siguientes pasos:

1. Cree un nuevo **[!UICONTROL Rol]** y asígnelo con la **[!UICONTROL Etiqueta]** correspondiente para que los usuarios puedan acceder y utilizar el campo de esquema.

1. Asigne una **[!UICONTROL Etiqueta]** al campo de esquema **Nacionalidad** en Adobe Experience Platform.

1. Utilice el **[!UICONTROL campo de esquema]** en Adobe Journey Optimizer.

Tenga en cuenta que también se puede tener acceso a **[!UICONTROL Roles]**, **[!UICONTROL Políticas]** y **[!UICONTROL Productos]** con la API de control de acceso basada en atributos. Para obtener más información, consulte esta [documentación](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html?lang=es){target="_blank"}.

## Crear una función y asignar etiquetas {#assign-role}

>[!IMPORTANT]
>
>&#x200B;>Antes de administrar permisos para una función, cree una directiva. Para obtener más información, consulte la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html?lang=es){target="_blank"}.

**[!UICONTROL Las funciones]** son un conjunto de usuarios que comparten los mismos permisos, etiquetas y zonas protegidas dentro de su organización. Cada usuario que pertenece a un **[!UICONTROL Rol]** tiene derecho a las aplicaciones y servicios de Adobe contenidos en el producto. También puede crear sus propios **[!UICONTROL roles]** para ajustar el acceso de los usuarios a ciertas funcionalidades u objetos de la interfaz.

Para conceder a los usuarios seleccionados acceso al campo **Nacionalidad** etiquetado como C2, cree un nuevo **[!UICONTROL Rol]** con un conjunto específico de usuarios y asígneles la etiqueta C2, permitiéndoles usar los detalles de **Nacionalidad** en un **[!UICONTROL Recorrido]**.

1. En el producto [!DNL Permissions], seleccione **[!UICONTROL Rol]** en el menú del panel izquierdo y haga clic en **[!UICONTROL Crear rol]**. Tenga en cuenta que también puede agregar **[!UICONTROL Label]** a los roles integrados.

   ![Crear una función nueva en el producto Permisos](assets/role_1.png)

1. Agregue un **[!UICONTROL Nombre]** y una **[!UICONTROL Descripción]** a su nuevo **[!UICONTROL Rol]**, aquí: Demografía de rol restringida.

1. En la lista desplegable, selecciona tu **[!UICONTROL espacio aislado]**.

   ![](assets/role_2.png)

1. En el menú **[!UICONTROL Recursos]**, haga clic en **[!UICONTROL Adobe Experience Platform]** para abrir las diferentes funcionalidades. Aquí seleccionamos **[!UICONTROL Recorridos]**.

   ![](assets/role_3.png)

1. En la lista desplegable, seleccione los **[!UICONTROL Permisos]** vinculados a la característica seleccionada, como **[!UICONTROL Ver recorridos]** o **[!UICONTROL Publicar recorridos]**.

   ![](assets/role_6.png)

1. Después de guardar la **[!UICONTROL función]** recién creada, haga clic en **[!UICONTROL Propiedades]** para seguir configurando el acceso a la función.

   ![](assets/role_7.png)

1. En la ficha **[!UICONTROL Usuarios]**, haga clic en **[!UICONTROL Agregar usuarios]**.

   ![](assets/role_8.png)

1. En la ficha **[!UICONTROL Etiquetas]**, seleccione **[!UICONTROL Agregar etiqueta]**.

   ![](assets/role_9.png)

1. Seleccione las **[!UICONTROL Etiquetas]** que desee agregar a su rol y haga clic en **[!UICONTROL Guardar]**. Para este ejemplo, conceda la etiqueta C2 para que los usuarios accedan al campo del esquema restringido anteriormente.

   ![Guardar la configuración de la etiqueta](assets/role_4.png)

Los usuarios con el rol **demográfico de rol restringido** ahora tienen acceso a los objetos etiquetados como C2.

## Asignación de etiquetas a un objeto en Adobe Experience Platform {#assign-label}

>[!WARNING]
>
>El uso incorrecto de las etiquetas puede interrumpir el acceso de las personas y las infracciones de las directivas de déclencheur.

**[!UICONTROL Las etiquetas]** se pueden usar para asignar áreas de características específicas mediante el control de acceso basado en atributos. En este ejemplo, el acceso al campo **Nationality** está restringido. Solo podrán acceder a este campo los usuarios que tengan la **[!UICONTROL Etiqueta]** correspondiente asignada a su **[!UICONTROL Rol]**.

Tenga en cuenta que también puede agregar **[!UICONTROL Label]** a **[!UICONTROL Schema]**, **[!UICONTROL Datasets]** y **[!UICONTROL Audiences]**.

1. Cree su **[!UICONTROL esquema]**. Para obtener más información, consulte [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=es){target="_blank"}.

   ![](assets/label_1.png)

1. En el **[!UICONTROL esquema]** recién creado, agregamos primero el grupo de campos **[!UICONTROL Detalles demográficos]** que contiene el campo **Nacionalidad**.

   ![](assets/label_2.png)

1. En la ficha **[!UICONTROL Etiquetas]**, compruebe el nombre del campo restringido, aquí **Nacionalidad**. A continuación, en el menú del panel derecho, seleccione **[!UICONTROL Editar etiquetas de control]**.

   ![Editar etiquetas de gobernanza para el campo](assets/label_3.png)

1. Seleccione la **[!UICONTROL Etiqueta]** correspondiente, en este caso, C2 - Los datos no se pueden exportar a terceros. Para obtener la lista detallada de las etiquetas disponibles, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=es#contract-labels){target="_blank"}.

   ![](assets/label_4.png)

1. Personalice aún más el esquema si es necesario y, a continuación, actívelo. Para ver los pasos detallados sobre cómo habilitar el esquema, consulte esta [página](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html?lang=es#profile){target="_blank"}.

El campo del esquema ahora solo lo podrán ver y utilizar los usuarios que formen parte de un conjunto de funciones con la etiqueta C2. Al aplicar una **[!UICONTROL Etiqueta]** a su **[!UICONTROL Nombre de campo]**, la **[!UICONTROL Etiqueta]** se aplicará automáticamente al campo **Nacionalidad** en cada esquema creado.

![](assets/label_5.png)

## Acceso a objetos etiquetados en Adobe Journey Optimizer {#attribute-access-ajo}

Después de etiquetar el nombre del campo **Nationality** en un nuevo esquema y rol, el impacto de esta restricción se puede observar en Adobe Journey Optimizer. Para este ejemplo:

* El usuario X, con acceso a los objetos etiquetados como C2, crea un recorrido con una condición dirigida al **[!UICONTROL nombre de campo]** restringido.
* El usuario Y, sin acceso a los objetos etiquetados como C2, intenta publicar el recorrido.


1. En Adobe Journey Optimizer, configure **[!UICONTROL Fuente de datos]** con su nuevo esquema.

   ![Configuración de la fuente de datos](assets/journey_1.png)

1. Agregue un nuevo **[!UICONTROL grupo de campos]** de su **[!UICONTROL esquema]** recién creado al **[!UICONTROL origen de datos]** integrado. También puede crear un nuevo **[!UICONTROL origen de datos]** externo y **[!UICONTROL grupos de campos]** asociados.

   ![Agregar un grupo de campos al origen de datos](assets/journey_2.png)

1. Después de seleccionar el **[!UICONTROL esquema]** creado anteriormente, haga clic en **[!UICONTROL Editar]** en la categoría **[!UICONTROL Campos]**.

   ![](assets/journey_3.png)

1. Seleccione el **[!UICONTROL nombre de campo]** al que desee destinarlo. Aquí seleccionamos el campo **Nacionalidad** restringida.

   ![](assets/journey_4.png)

1. Cree un recorrido que envíe un correo electrónico a los usuarios con una nacionalidad específica. Agregar un **[!UICONTROL evento]** y una **[!UICONTROL condición]**.

   ![](assets/journey_5.png)

1. Seleccione el campo **Nacionalidad** restringido para empezar a crear su expresión.

   ![](assets/journey_6.png)

1. Edite la **[!UICONTROL condición]** para dirigirse a una población específica con el campo **Nacionalidad** restringido.

   ![](assets/journey_7.png)

1. Personalice su recorrido según sea necesario. Aquí agregamos una acción **[!UICONTROL Correo electrónico]**.

   ![Agregar una acción de correo electrónico al recorrido](assets/journey_8.png)

Si el usuario Y, sin acceso a los objetos de la etiqueta C2, necesita acceder a este recorrido con el campo restringido:

* El usuario Y no podrá utilizar el nombre de campo restringido, ya que no será visible.
* El usuario Y no podrá editar la expresión con el nombre de campo restringido en modo avanzado. Aparecerá el siguiente error: `The expression is invalid. Field is no longer available or you don't have enough permission to see it`.
* El usuario Y puede eliminar la expresión.
* El usuario Y no podrá probar el recorrido.
* El usuario Y no podrá publicar el recorrido.