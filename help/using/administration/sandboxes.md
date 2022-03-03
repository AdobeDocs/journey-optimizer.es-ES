---
title: Administración de entornos limitados
description: Obtenga información sobre cómo administrar entornos limitados
feature: Sandboxes
topic: Administration
role: Admin
level: Intermediate
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: db6e970230b4d22b50c2035ecf5e7307e66feb2d
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 66%

---

# Administración de entornos limitados {#sandboxes}

## Usar entornos limitados {#using-sandbox}

[!DNL Journey Optimizer] le permite particionar la instancia en entornos virtuales separados, llamados entornos limitados.
Los entornos limitados para pruebas se asignan mediante perfiles de producto en la Admin Console. [Aprenda a asignar entornos limitados](permissions.md#create-product-profile).

[!DNL Journey Optimizer] refleja los entornos limitados de Adobe Experience Platform creados para una organización determinada.
Los entornos limitados de Adobe Experience Platform se pueden crear o restablecer desde la instancia de Adobe Experience Platform. [Obtenga más información en la guía del usuario de Sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=es){target=&quot;_blank&quot;}.

Puede encontrar el control del conmutador de simulador de pruebas en la parte superior derecha de la pantalla junto al nombre de la organización. Para cambiar de un simulador de pruebas a otro, haga clic en el simulador de pruebas activo y seleccione otro simulador de pruebas en la lista desplegable.

![](assets/sandbox_5.png)

➡️ [Descubra esta función en vídeo](#video)

## Asignar entornos limitados {#assign-sandboxes}

>[!IMPORTANT]
>
> La administración de entornos limitados solo se puede realizar mediante una **[!UICONTROL Product]** o **[!UICONTROL System]** administrador. Para obtener más información, consulte [Documentación de Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html){target=&quot;_blank&quot;}.

Puede optar por asignar diferentes entornos limitados a la configuración predeterminada o personalizada **[!UICONTROL Product profiles]**.

Para asignar entornos limitados:

1. En el [!DNL Admin Console], en la **[!UICONTROL Products]** , seleccione **[!UICONTROL Adobe Experience Platform Apps]** producto.

1. Seleccione un **[!UICONTROL Product profile]**.

   ![](assets/sandbox_1.png)

1. Seleccione la pestaña **[!UICONTROL Permissions]** .

1. Seleccione el **[!UICONTROL Sandboxes]** capacidad.

   ![](assets/sandbox_2.png)

1. En **[!UICONTROL Available Permissions Items]**, haga clic en el icono de signo más (+) para asignar entornos limitados al perfil. [Más información sobre los entornos limitados](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=es){target=&quot;_blank&quot;}.

   ![](assets/sandbox_3.png)

1. Si es necesario, en **[!UICONTROL Included Permission Items]**, haga clic en el icono X situado junto a para eliminar los entornos limitados de acceso a su **[!UICONTROL Product profile]**.

   ![](assets/sandbox_4.png)

1. Haga clic en **[!UICONTROL Save]**.

## Acceso al contenido {#content-access}

Para configurar la accesibilidad del contenido, debe asignar una carpeta compartida de contenido a cada uno de los entornos limitados. Puede crear y configurar la carpeta compartida en la pestaña **[!UICONTROL Storage]** que se muestra en [!DNL Admin Console] para los administradores. Si tiene acceso a [!DNL Admin Console] como administrador del sistema, puede crear carpetas compartidas y añadir delegados con un nivel de acceso diferente a las carpetas compartidas.

![](assets/do-not-localize/content_access.png)

Tenga en cuenta que para que el contenido se sincronice con el entorno limitado correcto, debe seguir la misma sintaxis que este; por ejemplo, si el entorno limitado se llama desarrollo, la carpeta compartida debe tener el mismo nombre.

[Obtenga información sobre cómo administrar carpetas compartidas](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target=&quot;_blank&quot;}.

## Vídeo explicativo{#video}

Comprenda qué son los espacios aislados y cómo distinguir entre los espacios aislados de desarrollo y producción. Obtenga información sobre cómo crear, restablecer y eliminar espacios aislados.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)
