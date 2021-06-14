---
title: Administración de entornos limitados
description: Obtenga información sobre cómo administrar entornos limitados
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: null
feature: Grupos de control
topic: Administración
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 75%

---

# Administración de entornos limitados {#sandboxes}

![](../assets/do-not-localize/badge.png)

## Usar entornos limitados {#using-sandbox}

[!DNL Journey Optimizer] le permite particionar la instancia en entornos virtuales separados, llamados entornos limitados.
Los entornos limitados para pruebas se asignan mediante perfiles de producto en la Admin Console. [Aprenda a asignar entornos limitados](permissions.md#create-product-profile).

[!DNL Journey Optimizer] refleja los entornos limitados de Adobe Experience Platform creados para una organización determinada.
Los entornos limitados de Adobe Experience Platform se pueden crear o restablecer desde la instancia de Adobe Experience Platform. [Obtenga más información en la Guía del usuario de entornos limitados](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=es).

Encontrará el control del conmutador de simulador de pruebas en la parte superior izquierda de la pantalla. Para cambiar de un simulador de pruebas a otro, haga clic en el simulador de pruebas activo y seleccione otro simulador de pruebas en la lista desplegable.

## Asignar entornos limitados {#assign-sandboxes}

>[!IMPORTANT]
>
> La administración de entornos limitados solo puede realizarla un administrador **[!UICONTROL Product]** o **[!UICONTROL System]**. Para obtener más información, consulte la [Documentación de la consola de administración](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

Puede optar por asignar diferentes entornos limitados a la configuración predeterminada o personalizada **[!UICONTROL Product profiles]**.

Para asignar entornos limitados:

1. En [!DNL Admin Console], en la pestaña **[!UICONTROL Products]**, seleccione el producto **[!UICONTROL Adobe Experience Platform Apps]**.

1. Seleccione un **[!UICONTROL Product profile]**.

   ![](../assets/sandbox_1.png)

1. Seleccione la pestaña **[!UICONTROL Permissions]** .

1. Seleccione la capacidad **[!UICONTROL Sandboxes]**.

   ![](../assets/sandbox_2.png)

1. En **[!UICONTROL Available Permissions Items]**, haga clic en el icono de signo más (+) para asignar entornos limitados al perfil. [Obtenga más información sobre los entornos limitados](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=es).

   ![](../assets/sandbox_3.png)

1. Si es necesario, en **[!UICONTROL Included Permission Items]**, haga clic en el icono X junto a para eliminar los entornos limitados de acceso a su **[!UICONTROL Product profile]**.

   ![](../assets/sandbox_4.png)

1. Haga clic en **[!UICONTROL Save]**.

## Acceso al contenido {#content-access}

Para configurar la accesibilidad del contenido, debe asignar una carpeta compartida de contenido a cada uno de los entornos limitados. Puede crear y configurar la carpeta compartida en la pestaña **[!UICONTROL Storage]** que se muestra en [!DNL Admin Console] para los administradores. Si tiene acceso a [!DNL Admin Console] como administrador del sistema, puede crear carpetas compartidas y añadir delegados con un nivel de acceso diferente a las carpetas compartidas.

![](../assets/do-not-localize/content_access.png)

Tenga en cuenta que para que el contenido se sincronice con el entorno limitado correcto, debe seguir la misma sintaxis que este; por ejemplo, si el entorno limitado se llama desarrollo, la carpeta compartida debe tener el mismo nombre.

[Obtenga información sobre cómo administrar carpetas](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html) compartidas.
