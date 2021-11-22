---
product: experience platform
solution: Experience Platform
title: Conceder acceso a Offer Decisioning
description: Obtenga información sobre cómo administrar los permisos de los usuarios para el servicio de Offer Decisioning a través de Adobe Admin Console.
feature: Collections
role: User
level: Intermediate
exl-id: 2a2fece9-1ad5-498e-b0ee-5bb0b73a2cd5
source-git-commit: 43fb98a08555e6b889ad537e79dba78286dafeb9
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 7%

---

# Conceder acceso a la gestión de decisiones {#granting-acess-to-decision-management}

Los permisos para acceder y utilizar las funcionalidades de offer decisioning se administran mediante la variable [Adobe Admin Console](https://helpx.adobe.com/es/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

Para conceder acceso a la funcionalidad de Administración de decisiones, debe crear una **[!UICONTROL Product profile]** y asigne los permisos correspondientes a sus usuarios. Más información sobre la administración [!DNL Journey Optimizer] usuarios y permisos en [esta sección](../../administration/permissions.md).

Los permisos específicos de Administración de decisiones se enumeran en [esta sección](../../administration/high-low-permissions.md#manage-decisioning).

<!--If you are a [!DNL Journey Optimizer] user leveraging the **Decision Management** functionality, you need to have the [Decision management permissions](../../administration/high-low-permissions.md#decisions-permissions) enabled to acces all related capabilities. Learn more on managing [!DNL Journey Optimizer] users and permissions in [this section](../../administration/permissions.md).

If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service, follow the steps [below](#granting-acess-to-offer-decisioning) to grant access to [!DNL Offer Decisioning].

Grant access to Offer Decisioning

The steps below only apply to **Experience Platform users** leveraging the [!DNL Offer Decisioning] service.-->

1. Abra el [Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html)y, a continuación, seleccione **[!UICONTROL Adobe Experience Platform]**.

   <!--![](../../assets/offers_admin_console.png)-->

1. Se muestran los perfiles de producto del servicio. Para crear un nuevo perfil de producto, haga clic en el botón **[!UICONTROL New Profile]** botón.

   ![](../../assets/offers_rights_productprofile.png)

   >[!NOTE]
   >
   >Puede tener tantos perfiles de producto como desee, correspondientes a las distintas funciones que desee configurar para su organización.

1. Especifique el nombre y la descripción del perfil de producto y haga clic en **[!UICONTROL Next]**.

   ![](../../assets/create-product-profile.png)

   <!--To access the product profile’s permissions, select the **[!UICONTROL Permissions]** line.-->

1. Seleccione los servicios que desea habilitar para el perfil de producto. De forma predeterminada, se seleccionan todos los servicios, lo que se recomienda para garantizar que todas las funcionalidades del Experience Platform estén disponibles.

   ![](../../assets/enable-services.png)

1. En el **[!UICONTROL Decision Management]** , haga clic en el botón **+** para asignar permisos al perfil del producto y, a continuación, haga clic en **[!UICONTROL Save]**.

   ![](../../assets/configure-profile.png)

   Los permisos disponibles son:

   **[!UICONTROL Manage Decisioning Activities]**

   * Leer, escribir, eliminar ofertas
   * Leer, escribir y eliminar decisiones (anteriormente conocidas como actividades de oferta)
   * Leer, escribir y eliminar ubicaciones

   **[!UICONTROL Execute Decisioning Activities]**:

   * Leer ofertas
   * Leer decisiones
   * Leer ubicaciones

   **[!UICONTROL Manage Decisioning Options]**:

   * Leer, escribir, eliminar ofertas
   * Leer decisiones
   * Leer, escribir y eliminar ubicaciones



1. Se muestra un resumen de los permisos del perfil del producto. Ahora puede asignar usuarios al perfil del producto para que accedan a estos permisos.

   ![](../../assets/product-profile-created.png)

>[!NOTE]
>
>Para obtener más información sobre cómo administrar los permisos de usuario, consulte la [documentación del Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

