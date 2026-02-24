---
solution: Journey Optimizer
product: journey optimizer
title: Uso y asignación de zonas protegidas
description: Obtenga información sobre cómo administrar zonas protegidas
feature: Sandboxes
topic: Administration
role: Admin, Developer
level: Experienced
keywords: zonas protegidas, virtual, entornos, organización, plataforma
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 56faee8badff99ff9a39cfd85a78c1ed272cd2ca
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 23%

---

# Uso y asignación de zonas protegidas {#sandboxes}

**Las zonas protegidas** son entornos virtuales que dividen la instancia de Adobe Journey Optimizer en espacios de trabajo independientes y aislados para fines de desarrollo, prueba o producción. Encontrará administración de zonas protegidas en **Administración** > **Canales** > **Conecte sus sistemas y entornos** (o a través del conmutador de zonas protegidas en la parte superior derecha de la interfaz). Las zonas protegidas le ayudan a experimentar con seguridad, asignar diferentes accesos por función y mantener el contenido organizado. Esta página explica cómo usar y asignar zonas protegidas, cómo configurar el acceso al contenido y, en el artículo [Exportar objetos a otra zona protegida](../configuration/copy-objects-to-sandbox.md), cómo copiar recorridos y plantillas entre zonas protegidas.

## Usar zonas protegidas {#using-sandbox}

[!DNL Journey Optimizer] le permite particionar su instancia en entornos virtuales independientes llamados zonas protegidas. Las zonas protegidas se asignan mediante funciones en Permisos. [Aprenda a asignar zonas protegidas](permissions.md#create-product-profile).

[!DNL Journey Optimizer] refleja los entornos limitados de Adobe Experience Platform creados para una organización determinada. Las zonas protegidas de Adobe Experience Platform se pueden crear o restablecer desde la instancia de Adobe Experience Platform. [Obtenga más información en la Guía del usuario de zonas protegidas](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=es){target="_blank"}.

Puede encontrar el control del conmutador de simulador de pruebas en la parte superior derecha de la pantalla, junto al nombre de la organización. Para cambiar de una zona protegida a otra, haga clic en la zona protegida activa y seleccione otra zona protegida en la lista desplegable.

![](assets/sandbox_5.png)

➡️ [Obtenga más información acerca de las zonas protegidas en este vídeo](#video)

## Asignar zonas protegidas {#assign-sandboxes}

>[!IMPORTANT]
>
> Solo un administrador de **[!UICONTROL Product]** o **[!UICONTROL System]** puede llevar a cabo la administración de la zona protegida.

Puede elegir asignar diferentes zonas protegidas a **[!UICONTROL roles]** predeterminados o personalizados.

Para asignar zonas protegidas:

1. En [!DNL Permissions], en la ficha **[!UICONTROL Roles]**, seleccione un **[!UICONTROL Rol]**.

   ![](assets/sandbox_1.png)

1. Haga clic en **[!UICONTROL Edit]**.

1. En la lista desplegable de recursos **[!UICONTROL Zonas protegidas]**, seleccione la zona protegida que se asignará a su función.

   ![](assets/sandbox_3.png)

1. Si es necesario, haga clic en el icono X que hay junto a él para quitar el acceso a la zona protegida de su **[!UICONTROL función]**.

   ![](assets/sandbox_4.png)

1. Haga clic en **[!UICONTROL Guardar]**.

## Acceso al contenido {#content-access}

Para configurar la accesibilidad del contenido, asigne una carpeta compartida de contenido a cada uno de los entornos limitados. Puede crear y configurar carpetas compartidas en la ficha **[!UICONTROL Almacenamiento]** que se muestra en [!DNL Admin Console] para los administradores. Si tiene acceso a [!DNL Admin Console] como administrador del sistema, puede crear carpetas compartidas y agregar delegados con diferentes niveles de acceso a las carpetas compartidas.

![](assets/do-not-localize/content_access.png)

Tenga en cuenta que para que el contenido se sincronice con la zona protegida correcta, debe seguir la misma sintaxis que esta. Por ejemplo, si la zona protegida se llama &quot;desarrollo&quot;, la carpeta compartida debe tener el mismo nombre.

[Obtenga información sobre cómo administrar carpetas](https://helpx.adobe.com/es/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"} compartidas.

## Vídeo práctico{#video}

Comprenda qué son las zonas protegidas y cómo distinguir entre las zonas protegidas de desarrollo y producción. Obtenga información sobre cómo crear, restablecer y eliminar zonas protegidas.

>[!VIDEO](https://video.tv.adobe.com/v/3416653?captions=spa&quality=12)