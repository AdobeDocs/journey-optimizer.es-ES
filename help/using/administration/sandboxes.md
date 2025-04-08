---
solution: Journey Optimizer
product: journey optimizer
title: Administración de zonas protegidas
description: Obtenga información sobre cómo administrar zonas protegidas
feature: Sandboxes
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: zonas protegidas, virtual, entornos, organización, plataforma
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 060d65e8d3fb1442b04626170a35d463d1faa514
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 60%

---

# Administración de zonas protegidas {#sandboxes}

## Usar zonas protegidas {#using-sandbox}

[!DNL Journey Optimizer] le permite particionar la instancia en entornos virtuales separados, llamados zonas protegidas.
Las zonas protegidas se asignan mediante funciones en Permisos. [Aprenda a asignar zonas protegidas](permissions.md#create-product-profile).

[!DNL Journey Optimizer] refleja las zonas protegidas de Adobe Experience Platform creadas para una organización determinada.
Las zonas protegidas de Adobe Experience Platform se pueden crear o restablecer desde la instancia de Adobe Experience Platform. [Obtenga más información en la Guía del usuario de zonas protegidas](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=es){target="_blank"}.

Puede encontrar el control del conmutador de simulador de pruebas en la parte superior derecha de la pantalla junto al nombre de la organización. Para cambiar de una zona protegida a otra, haga clic en la zona protegida activa y seleccione otra zona protegida en la lista desplegable.

![](assets/sandbox_5.png)

➡️ [Obtenga más información acerca de las zonas protegidas en este vídeo](#video)

## Asignar zonas protegidas {#assign-sandboxes}

>[!IMPORTANT]
>
> La administración de las zonas protegidas solamente la puede realizar un administrador de **[!UICONTROL Product]** o **[!UICONTROL System]**.

Puede elegir asignar diferentes zonas protegidas a **[!UICONTROL roles]** predeterminados o personalizados.

Para asignar zonas protegidas:

1. En [!DNL Permissions], en la ficha **[!UICONTROL Roles]**, seleccione un **[!UICONTROL Rol]**.

   ![](assets/sandbox_1.png)

1. Haga clic en **[!UICONTROL Edit]**.

1. En la lista desplegable de recursos **[!UICONTROL Zonas protegidas]**, seleccione la zona protegida que se asignará a su función.

   ![](assets/sandbox_3.png)

1. Si es necesario, haga clic en el icono X para quitar el acceso a las zonas protegidas de su **[!UICONTROL función]**.

   ![](assets/sandbox_4.png)

1. Haga clic en **[!UICONTROL Guardar]**.

## Acceso al contenido {#content-access}

Para configurar la accesibilidad del contenido, debe asignar una carpeta compartida de contenido a cada una de las zonas protegidas. Puede crear y configurar su carpeta compartida en la ficha **[!UICONTROL Almacenamiento]** que se muestra en [!DNL Admin Console] para administradores. Si tiene acceso a [!DNL Admin Console] como administrador del sistema, puede crear carpetas compartidas y añadir delegados con un nivel de acceso diferente a las carpetas compartidas.

![](assets/do-not-localize/content_access.png)

Tenga en cuenta que para que el contenido se sincronice con la zona protegida correcta, debe seguir la misma sintaxis que esta; por ejemplo, si la zona protegida se llama desarrollo, la carpeta compartida debe tener el mismo nombre.

[Obtenga información sobre cómo administrar carpetas](https://helpx.adobe.com/es/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"} compartidas.

## Vídeo práctico{#video}

Comprenda qué son las zonas protegidas y cómo distinguir entre las zonas protegidas de desarrollo y producción. Obtenga información sobre cómo crear, restablecer y eliminar zonas protegidas.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)