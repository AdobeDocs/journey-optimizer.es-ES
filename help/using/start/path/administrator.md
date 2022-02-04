---
title: Introducción a Journey Optimizer para administrador del sistema
description: Como administrador del sistema, obtenga más información sobre cómo trabajar con Journey Optimizer
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 7a07f2348f08b4582a1310fb65d431c55451d9b6
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 2%

---

# Introducción para administradores de sistemas {#get-started-sys-admins}

![administrador](assets/do-not-localize/user-2.png)

Antes de empezar a utilizar [!DNL Adobe Journey Optimizer], se requieren varios pasos para preparar su entorno.  Debe realizar estos pasos para que la variable [Ingeniero de datos](data-engineer.md) y [Recorrido](marketer.md) puede empezar a trabajar con [!DNL Adobe Journey Optimizer].


Como **Administrador del sistema**, necesita **comprender los perfiles de producto y asignar permisos** para la administración de entornos limitados y la configuración de canales. También debe configurar entornos limitados y administrarlos para los perfiles de producto disponibles. A continuación, podrá asignar miembros del equipo a perfiles de producto.

Estas capacidades las puede administrar **[!UICONTROL Product administrators]** que tienen acceso a Admin Console. [Más información sobre Adobe Admin Console](https://helpx.adobe.com/es/enterprise/admin-guide.html){target=&quot;_blank&quot;}.

Obtenga información sobre la administración de acceso en las siguientes páginas:

1. **Crear entornos limitados** para particionar las instancias en entornos virtuales independientes y aislados. **Sandboxes** se crean en [!DNL Journey Optimizer]. Obtenga más información en la [Sandboxes](../../administration/sandboxes.md) para obtener más información.

   >[!NOTE]
   >Como **Administrador del sistema**, si no puede ver la variable **[!UICONTROL Sandboxes]** en [!DNL Journey Optimizer], actualice sus permisos en el [Admin Console](https://adminconsole.adobe.com/){_blank}. Obtenga información sobre cómo actualizar el perfil de producto en [esta página](../../administration/permissions.md#edit-product-profile).

1. **Explicación de los perfiles de producto**. Los perfiles de producto son un conjunto de derechos unitarios que permiten a los usuarios acceder a determinadas funcionalidades u objetos de la interfaz. Obtenga más información en la [Perfiles de producto integrados](../../administration/ootb-product-profiles.md) para obtener más información.

1. **Definir permisos** para perfiles de producto, incluido **Sandboxes**, y dé acceso a los integrantes del equipo asignándolos a diferentes perfiles de producto. Este paso se realiza en la [Admin Console](https://adminconsole.adobe.com/){_blank}. Los permisos son derechos unitarios que le permiten definir las autorizaciones asignadas a **[!UICONTROL Product profile]**. Cada permiso se recopila en funciones, como Recorrido, mensajes u ofertas, que representan las diferentes funcionalidades u objetos de [!DNL Journey Optimizer]. Obtenga más información en la [Niveles de permisos](../../administration/high-low-permissions.md) para obtener más información.

Además, debe agregar usuarios que necesiten acceder a Assets Essentials a la **Usuarios consumidores de Assets Essentials** o/y **Usuarios de Assets Essentials** Perfiles de producto. [Más información en la documentación de Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

>[!NOTE]
>Para los productos de Journey Optimizer obtenidos antes del 6 de enero de 2022, debe implementar [!DNL Adobe Experience Manager Assets Essentials] para su organización. Obtenga más información en la [Implementación de Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html)sección {target=&quot;_blank&quot;}.

Al acceder [!DNL Journey Optimizer] por primera vez, se le aprovisiona un simulador para pruebas de producción y se le asigna un determinado número de direcciones IP en función de su contrato.

Para poder crear sus recorridos y enviar mensajes, acceda al **ADMINISTRACIÓN** para abrir el Navegador. Examine la **[!UICONTROL Channels]** para configurar los mensajes de correo electrónico y los ajustes preestablecidos.

>[!NOTE]
>Como **Administrador del sistema**, si no puede ver la variable **[!UICONTROL Channels]** en [!DNL Journey Optimizer], actualice sus permisos en el [Admin Console](https://adminconsole.adobe.com/){_blank}. Obtenga información sobre cómo actualizar el perfil de producto en [esta página](../../administration/permissions.md#edit-product-profile).

Siga los pasos que se indican a continuación:

1. **Configuración de mensajes y canales**: definir ajustes preestablecidos, adaptar y personalizar la configuración de los mensajes push y de correo electrónico

   * Definir **configuración de notificaciones push** en ambos [!DNL Adobe Experience Platform] y [!DNL Adobe Experience Platform Launch]. [Más información](../../messages/push-gs.md)

   * Crear **ajustes preestablecidos de mensajes** para configurar todos los parámetros técnicos necesarios para los mensajes de correo electrónico y notificaciones push. [Más información](../../configuration/message-presets.md)

   * Administrar el número de días durante los cuales **reintentos** se realizan antes de enviar direcciones de correo electrónico a la lista de supresión. [Más información](../../configuration/manage-suppression-list.md)

1. **Delegación de subdominios**: para cualquier nuevo subdominio que se vaya a utilizar en Journey Optimizer, el primer paso será delegarlo. [Más información](../../configuration/about-subdomain-delegation.md)

   ![](../../assets/subdomain.png)

1. **Crear grupos de IP**: mejore su capacidad de envío de correo electrónico y su reputación agrupando direcciones IP aprovisionadas con su instancia. [Más información](../../configuration/ip-pools.md)

   ![](../../assets/ip-pool.png)

1. **Administrar la supresión y la lista de permitidos**: mejore la capacidad de envío con supresión y listas de permitidos

   * A [lista de supresión](../../messages/suppression-list.md) consiste en direcciones de correo electrónico que desea excluir de los envíos, ya que el envío a estos contactos podría dañar la reputación de envío y las tasas de envío. Puede supervisar todas las direcciones de correo electrónico que se excluyen automáticamente del envío de un recorrido, como direcciones no válidas, direcciones que devuelven mensajes de forma flexible y que podrían afectar negativamente a su reputación de correo electrónico y destinatarios que presentan una queja de correo no deseado de algún tipo contra uno de sus mensajes de correo electrónico. Obtenga información sobre cómo administrar la variable [lista de supresión](../../configuration/manage-suppression-list.md) y [reintentos](../../configuration/retries.md).
   ![](../../assets/suppression-list-filtering-example.png)

   * La variable [lista de permitidos](../../messages/allow-list.md) permite especificar direcciones de correo electrónico o dominios individuales que serán los únicos destinatarios o dominios autorizados para recibir los correos electrónicos que envía desde un entorno limitado específico. Esto puede impedir que envíe correos electrónicos accidentalmente a direcciones de clientes reales cuando se encuentre en un entorno de prueba. Obtenga información sobre cómo [habilitar la lista de permitidos](../../messages/allow-list.md).
   Obtenga más información sobre la administración de envíos en [!DNL Adobe Journey Optimizer] [en esta página](../../messages/deliverability.md).
