---
solution: Journey Optimizer
product: journey optimizer
title: Control de acceso de nivel de objeto
description: Obtenga información sobre el control de acceso de nivel de objeto que le permite definir autorizaciones para administrar el acceso a datos a una selección de objetos
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: objeto, nivel, acceso, control, etiquetas, olac, autorización
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 342b9210f79266cb11628dcdc411f90844a84e37
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 7%

---

# Control de acceso de nivel de objeto {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Control de acceso de nivel de objeto"
>abstract="Para mantener el acceso a este objeto, aplique solo las etiquetas para las que tenga permiso."

El control de acceso a nivel de objeto (OLAC) permite definir autorizaciones para administrar el acceso a datos a una selección de objetos:

*  Recorrido 
* Campaign
* Plantilla
* Fragmento
* Landing page
* Oferta
* Colección de ofertas estáticas
* Decisión de oferta
* Superficie de canal
* plan de calentamiento de IP

Su objetivo es proteger los activos digitales confidenciales de usuarios no autorizados, lo que permite una mayor protección de los datos personales.

En Adobe Journey Optimizer, OLAC permite proteger los datos y conceder acceso específico a objetos específicos.

## Creación de etiquetas {#create-assign-labels}

>[!IMPORTANT]
>
>Para poder crear etiquetas, debe formar parte de una función con el **[!UICONTROL Administrar etiquetas de uso]** permiso.

**[!UICONTROL Etiquetas]** permiten categorizar conjuntos de datos y campos según las políticas de uso que se aplican a esos datos. **[!UICONTROL Etiquetas]** se puede aplicar en cualquier momento, lo que proporciona flexibilidad en la forma en que se decide administrar los datos.

Puede crear etiquetas en la variable [!DNL Permissions] producto. Para obtener más información, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html).

**[!UICONTROL Etiquetas]** también se puede crear directamente en Journey Optimizer:

1. Desde un objeto Adobe Journey Optimizer, aquí se crea un **[!UICONTROL Campaign]**, haga clic en **[!UICONTROL Administrar acceso]** botón.

   ![](assets/olac_1.png)

1. Desde el **[!UICONTROL Administrar acceso]** , haga clic en **[!UICONTROL Crear etiqueta]**.

   ![](assets/olac_2.png)

1. Configure la etiqueta y debe especificar:
   * **[!UICONTROL Nombre]**
   * **[!UICONTROL Nombre descriptivo]**
   * **[!UICONTROL Descripción]**

   ![](assets/olac_3.png)

1. Clic **[!UICONTROL Crear]** para guardar su **[!UICONTROL Etiqueta]**.

Su recién creado **[!UICONTROL Etiqueta]** ahora está disponible en la lista. Si es necesario, puede modificarlo en la [!DNL Permissions] producto.

## Asignar etiquetas {#assign-labels}

>[!IMPORTANT]
>
>Para poder asignar etiquetas, debe formar parte de una función con permiso de administración, es decir, [!DNL Manage journeys], [!DNL Manage Campaigns] o [!DNL Manage decisions]. Sin este permiso, la variable **[!UICONTROL Administrar acceso]** el botón aparecerá atenuado.

Para asignar etiquetas de uso de datos personalizadas o principales a los objetos de Journey Optimizer:

1. Desde un objeto Adobe Journey Optimizer, aquí se crea un **[!UICONTROL Campaign]**, haga clic en **[!UICONTROL Administrar acceso]** botón.

   ![](assets/olac_1.png)

1. Desde el **[!UICONTROL Administrar acceso]** , seleccione las etiquetas de uso de datos personalizadas o principales para administrar el acceso a este objeto.

   Para obtener más información sobre las etiquetas de uso de datos principales, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. Clic **[!UICONTROL Guardar]** para aplicar esta restricción de etiqueta.

Para tener acceso a este objeto, los usuarios deberán tener la variable específica **[!UICONTROL Etiqueta]** incluido en su **[!UICONTROL Funciones]**.
Por ejemplo, un usuario con la etiqueta C1 solo tendrá acceso a los objetos con o sin etiqueta C1.

Para obtener más información sobre cómo asignar **[!UICONTROL Etiqueta]** a un **[!UICONTROL Rol]**, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html#manage-labels-for-a-role).