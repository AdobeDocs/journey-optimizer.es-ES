---
title: Introducción a Journey Optimizer para administrador del sistema
description: As a System Administrator, learn more how to work with Journey Optimizer
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 2%

---

# Introducción para administradores de sistemas {#get-started-sys-admins}

![administrador](assets/do-not-localize/user-2.png)

Antes de empezar a utilizar [!DNL Adobe Journey Optimizer], se requieren varios pasos para preparar su entorno.  You must perform these steps so that the [Data Engineer](data-engineer.md) and [Journey Practicionner](marketer.md) can start working with [!DNL Adobe Journey Optimizer].


As a **System Administrator**, you need to **understand product profiles and assign permissions** for sandbox administration and channel configuration. También debe configurar entornos limitados y administrarlos para los perfiles de producto disponibles. A continuación, podrá asignar miembros del equipo a perfiles de producto.

Estas capacidades las puede administrar **[!UICONTROL Product administrators]** que tienen acceso a Admin Console. [Learn more about Adobe Admin Console](https://helpx.adobe.com/es/enterprise/admin-guide.html){target=&quot;_blank&quot;}.

Obtenga información sobre la administración de acceso en las siguientes páginas:

1. **Crear entornos limitados** para particionar las instancias en entornos virtuales independientes y aislados. **Sandboxes** se crean en [!DNL Journey Optimizer]. Obtenga más información en la [Sandboxes](../../administration/sandboxes.md) para obtener más información.

   >[!NOTE]
   >Como **Administrador del sistema**, si no puede ver la variable **[!UICONTROL Sandboxes]** en [!DNL Journey Optimizer], actualice sus permisos en el [Admin Console](https://adminconsole.adobe.com/){_blank}. Obtenga información sobre cómo actualizar el perfil de producto en [esta página](../../administration/permissions.md#edit-product-profile).

1. **Understand product profiles**. Product profiles are a set of unitary rights which allows users access to certain functionalities or objects in the interface. Learn more in the [Out-of-the-box product profiles](../../administration/ootb-product-profiles.md) section.

1. **Definir permisos** para perfiles de producto, incluido **Sandboxes**, y dé acceso a los integrantes del equipo asignándolos a diferentes perfiles de producto. This step is performed in the [Admin Console](https://adminconsole.adobe.com/){_blank}. Los permisos son derechos unitarios que le permiten definir las autorizaciones asignadas a **[!UICONTROL Product profile]**. Each permission is gathered under capabilities, e.g. Journey, Messages or Offers, which represents the different functionalities or objects in [!DNL Journey Optimizer]. Learn more in the [Permission levels](../../administration/high-low-permissions.md) section.

Además, debe agregar usuarios que necesiten acceder a Assets Essentials a la **Usuarios consumidores de Assets Essentials** o/y **Usuarios de Assets Essentials** Perfiles de producto. [Read more in Assets Essentials documentation](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

>[!NOTE]
>Para los productos de Journey Optimizer obtenidos antes del 6 de enero de 2022, debe implementar [!DNL Adobe Experience Manager Assets Essentials] para su organización. Obtenga más información en la [Implementación de Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html)sección {target=&quot;_blank&quot;}.

Al acceder [!DNL Journey Optimizer] por primera vez, se le aprovisiona un simulador para pruebas de producción y se le asigna un determinado número de direcciones IP en función de su contrato.

Para poder crear sus recorridos y enviar mensajes, acceda al **ADMINISTRACIÓN** para abrir el Navegador. Browse the **[!UICONTROL Channels]** menu to configure your email messages and presets.

>[!NOTE]
>Como **Administrador del sistema**, si no puede ver la variable **[!UICONTROL Channels]** en [!DNL Journey Optimizer], actualice sus permisos en el [Admin Console](https://adminconsole.adobe.com/){_blank}. Obtenga información sobre cómo actualizar el perfil de producto en [esta página](../../administration/permissions.md#edit-product-profile).

Follow the steps listed below:

1. **Configure messages and channels**: define presets, adapt and customize email and push messages settings

   * Definir **configuración de notificaciones push** en ambos [!DNL Adobe Experience Platform] y [!DNL Adobe Experience Platform Launch]. [Más información](../../configuration/push-gs.md)

   * Crear **ajustes preestablecidos de mensajes** para configurar todos los parámetros técnicos necesarios para los mensajes de correo electrónico y notificaciones push. [Más información](../../configuration/message-presets.md)

   * Administrar el número de días durante los cuales **reintentos** se realizan antes de enviar direcciones de correo electrónico a la lista de supresión. [Más información](../../configuration/manage-suppression-list.md)

1. **Delegate subdomains**: for any new subdomain to be used in Journey Optimizer, the first step will be to delegate it. [Más información](../../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **Create IP pools**: improve your email deliverability and reputation by grouping together IP addresses provisioned with your instance. [Más información](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Administrar la supresión y la lista de permitidos**: mejore la capacidad de envío con supresión y listas de permitidos

   * A [lista de supresión](../../reports/suppression-list.md) consiste en direcciones de correo electrónico que desea excluir de los envíos, ya que el envío a estos contactos podría dañar la reputación de envío y las tasas de envío. Puede supervisar todas las direcciones de correo electrónico que se excluyen automáticamente del envío de un recorrido, como direcciones no válidas, direcciones que devuelven mensajes de forma flexible y que podrían afectar negativamente a su reputación de correo electrónico y destinatarios que presentan una queja de correo no deseado de algún tipo contra uno de sus mensajes de correo electrónico. Learn how to manage the [suppression list](../../configuration/manage-suppression-list.md) and [retries](../../configuration/retries.md).
   ![](../assets/suppression-list-filtering-example.png)

   * The [allowed list](../../reports/allow-list.md) enables you to specify individual email addresses or domains that will be the only recipients or domains authorized to receive the emails you are sending from a specific sandbox. This can prevent you from sending emails accidentally to real customer addresses when you are in a testing environment. Obtenga información sobre cómo [habilitar la lista de permitidos](../../reports/allow-list.md).
   Obtenga más información sobre la administración de envíos en [!DNL Adobe Journey Optimizer] [en esta página](../../reports/deliverability.md).
