---
solution: Journey Optimizer
product: journey optimizer
title: Control de acceso de nivel de objeto
description: Obtenga información sobre el control de acceso a nivel de objeto que permite definir autorizaciones para administrar el acceso a los datos de una selección de objetos
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: objeto, nivel, acceso, control, etiquetas, olac, autorización
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 10%

---

# Control de acceso de nivel de objeto {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Control de acceso de nivel de objeto"
>abstract="Si aplica etiquetas a las que no tiene acceso, se revocará el acceso a este objeto."

>[!IMPORTANT]
>
>El uso del control de acceso a nivel de objeto está restringido actualmente a clientes seleccionados y se implementará en todos los entornos en una versión futura.

El control de acceso a nivel de objeto (OLAC) permite definir autorizaciones para administrar el acceso a los datos de una selección de objetos:

*  Recorrido 
* Campaign
* Landing page
* Ofertas
* Colección de ofertas
* Offer decisioning

Su objetivo es proteger los activos digitales confidenciales de los usuarios no autorizados, lo que permite una mayor protección de los datos personales.

En Adobe Journey Optimizer, OLAC le permite proteger datos y conceder acceso específico a objetos específicos.

## Creación de etiquetas {#create-assign-labels}

>[!IMPORTANT]
>
>Para poder crear etiquetas, debe formar parte de una función con la variable **[!UICONTROL Administrar etiquetas de uso]** permiso.

**[!UICONTROL Las etiquetas permiten categorizar conjuntos de datos y campos según las políticas de uso que se aplican a esos datos.]** **[!UICONTROL Etiquetas]** se puede aplicar en cualquier momento, lo que proporciona flexibilidad en la forma en que elige administrar los datos.

Puede crear etiquetas en la variable [!DNL Permissions] producto. Para obtener más información, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html).

**[!UICONTROL Etiquetas]** también se puede crear directamente en Journey Optimizer:

1. A partir de un objeto Adobe Journey Optimizer, aquí se crea un objeto **[!UICONTROL Campaign]**, haga clic en **[!UICONTROL Administrar acceso]** botón.

   ![](assets/olac_1.png)

1. En el **[!UICONTROL Administrar acceso]** ventana, haga clic en **[!UICONTROL Crear etiqueta]**.

   ![](assets/olac_2.png)

1. Configure la etiqueta y debe especificar:
   * **[!UICONTROL Nombre]**
   * **[!UICONTROL Nombre reconocible]**
   * **[!UICONTROL Descripción]**

   ![](assets/olac_3.png)

1. Haga clic en **[!UICONTROL Crear]** para guardar su **[!UICONTROL Etiqueta]**.

Su recién creada **[!UICONTROL Etiqueta]** ya está disponible en la lista . Si es necesario, puede modificarlo en la [!DNL Permissions] producto.

## Asignar etiquetas {#assign-labels}

>[!IMPORTANT]
>
>Para poder asignar etiquetas, debe formar parte de una función con un permiso de gestión, es decir, [!DNL Manage journeys], [!DNL Manage Campaigns] o [!DNL Manage decisions]. Sin este permiso, la variable **[!UICONTROL Administrar acceso]** se atenuará.

Para asignar etiquetas de uso de datos principales o personalizadas a los objetos de Journey Optimizer:

1. A partir de un objeto Adobe Journey Optimizer, aquí se crea un objeto **[!UICONTROL Campaign]**, haga clic en **[!UICONTROL Administrar acceso]** botón.

   ![](assets/olac_1.png)

1. En el **[!UICONTROL Administrar acceso]** , seleccione las etiquetas de uso de datos principales o personalizadas para administrar el acceso a este objeto.

   Para obtener más información sobre las etiquetas de uso de datos principales, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. Haga clic en **[!UICONTROL Guardar]** para aplicar esta restricción de etiqueta.

Para tener acceso a este objeto, los usuarios deberán tener la variable **[!UICONTROL Etiqueta]** incluido en su **[!UICONTROL Funciones]**.
Por ejemplo, un usuario con la etiqueta C1 solo tendrá acceso a objetos etiquetados o no etiquetados C1.

Para obtener más información sobre cómo asignar **[!UICONTROL Etiqueta]** a **[!UICONTROL Función]**, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=en#manage-labels-for-a-role).
