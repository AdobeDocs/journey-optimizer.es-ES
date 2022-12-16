---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a Journey Optimizer para administradores de sistemas
description: Obtenga más información sobre cómo trabajar con Journey Optimizer como administrador de sistemas
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 9f67172f31ddc1caef9d014c365f71e470e45390
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 92%

---

# Introducción para administradores de sistemas {#get-started-sys-admins}

Antes de empezar a utilizar [!DNL Adobe Journey Optimizer], se requieren varios pasos para preparar su entorno.  Debe seguir estos pasos para que el [Ingeniero de datos](data-engineer.md) y el [Profesional del recorrido](marketer.md) puedan comenzar a trabajar con [!DNL Adobe Journey Optimizer].


Como **Administrador de sistemas**, necesita **comprender los perfiles de producto y asignar permisos** para la administración de zonas protegidas y la configuración de canal. También debe configurar las zonas protegidas y administrarlas para los perfiles de producto disponibles. Entonces, podrá asignar integrantes del equipo a perfiles de producto.

Estas funcionalidades pueden gestionarlas los **[!UICONTROL Administradores de producto]** que tengan acceso a Admin Console. [Obtenga más información acerca de Adobe Admin Console](https://helpx.adobe.com/es/enterprise/admin-guide.html){target=&quot;_blank&quot;}.

Obtenga información acerca de la administración de acceso en las siguientes páginas:

1. **Crear zonas protegidas** para dividir las instancias en entornos virtuales independientes y aislados. Las **zonas protegidas** se crean en [!DNL Journey Optimizer]. Obtenga más información en la sección [Zonas protegidas](../../administration/sandboxes.md).

   >[!NOTE]
   >Como **Administrador del sistema**, si no puede ver la variable **[!UICONTROL Sandboxes]** en [!DNL Journey Optimizer], actualice sus permisos en el [Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}. Obtenga información sobre cómo actualizar el perfil de producto en [esta página](../../administration/permissions.md#edit-product-profile).

1. **Explicación de los perfiles de producto**. Los perfiles de producto son un conjunto de derechos unitarios que permiten a los usuarios acceder a determinadas funcionalidades u objetos de la interfaz. Obtenga más información en la sección [Perfiles de producto predeterminados](../../administration/ootb-product-profiles.md).

1. **Defina permisos** para perfiles de producto, incluidas las **zonas protegidas**, y dé acceso a los integrantes del equipo asignándolos a diferentes perfiles de producto. Este paso se realiza en la [Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}. Los permisos son derechos unitarios que le permiten definir las autorizaciones asignadas al **[!UICONTROL Perfil del producto]**. Cada permiso se recopila en funcionalidades, por ejemplo, Recorrido u Ofertas, que representan las diferentes funcionalidades u objetos de [!DNL Journey Optimizer]. Obtenga más información en la sección [Niveles de permisos](../../administration/high-low-permissions.md).

Además, debe agregar usuarios que necesiten acceder a Assets Essentials a los perfiles de producto **Usuarios consumidores de Assets Essentials** o **Usuarios de Assets Essentials**. [Más información en la documentación de Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=es){target=&quot;_blank&quot;}.

>[!NOTE]
>Para los productos de Journey Optimizer obtenidos antes del 6 de enero de 2022, debe implementar [!DNL Adobe Experience Manager Assets Essentials] para su organización. Obtenga más información en la sección [Implementación de Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=es){target=&quot;_blank&quot;}.

Al acceder a [!DNL Journey Optimizer] por primera vez, se le aprovisiona una zona protegida de producción y se le asigna un determinado número de direcciones IP en función de su contrato.

Para poder crear sus recorridos y enviar mensajes, acceda al menú **ADMINISTRACIÓN**. Examine el menú **[!UICONTROL Canales]** para configurar los mensajes y las superficies de canal (es decir, los ajustes preestablecidos de mensaje).

>[!NOTE]
>Como **Administrador del sistema**, si no puede ver la variable **[!UICONTROL Canales]** en [!DNL Journey Optimizer], actualice sus permisos en el [Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}. Obtenga información sobre cómo actualizar el perfil de producto en [esta página](../../administration/permissions.md#edit-product-profile).

Siga estos pasos a continuación:

1. **Configuración de mensajes y canales**: definir superficies, adaptar y personalizar la configuración de correo electrónico, SMS y mensajes push

   * Defina la **configuración de notificaciones push** en [!DNL Adobe Experience Platform] y [!DNL Adobe Experience Platform Launch]. [Más información](../../push/push-gs.md)

   * Cree **superficies de canal** (es decir, ajustes preestablecidos de mensaje) para configurar todos los parámetros técnicos necesarios para el correo electrónico, los SMS y las notificaciones push. [Más información](../../configuration/channel-surfaces.md)

   * Configure el **Canal de SMS** para configurar todos los parámetros técnicos necesarios para SMS. [Más información](../../sms/sms-configuration.md)

   * Administre el número de días durante los cuales se realizan **reintentos** antes de enviar direcciones de correo electrónico a la lista de supresión. [Más información](../../configuration/manage-suppression-list.md)

1. **Delegue subdominios**: para cualquier nuevo subdominio que se vaya a utilizar en Journey Optimizer, el primer paso será delegarlo. [Más información](../../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **Cree grupos de IP**: mejore su capacidad de entrega de correo electrónico y su reputación agrupando direcciones IP aprovisionadas con su instancia. [Más información](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Administre las listas de supresión y las listas de permitidos**: mejore la capacidad de entrega con las listas de supresión y las de permitidos

   * Una [lista de supresión](../../reports/suppression-list.md) consiste en las direcciones de correo electrónico que desea excluir de las entregas, ya que el envío a estos contactos podría dañar su reputación y las tasas de entrega. Puede monitorizar todas las direcciones de correo electrónico que se excluyen automáticamente del envío de un recorrido. Por ejemplo, direcciones no válidas, direcciones con mensajes devueltos no entregados de forma frecuente y que podrían afectar negativamente a su reputación de correo electrónico y destinatarios que presentan una queja de correo no deseado de algún tipo contra uno de sus mensajes por correo electrónico. Obtenga información sobre cómo administrar la [lista de supresión](../../configuration/manage-suppression-list.md) y los [reintentos](../../configuration/retries.md).
   ![](../assets/suppression-list-filtering-example.png)

   * La [lista de permitidos](../../configuration/allow-list.md) permite especificar direcciones de correo electrónico o dominios individuales que serán los únicos destinatarios o dominios autorizados para recibir los correos electrónicos que envía desde una zona protegida específica. Esto puede impedir que envíe correos electrónicos accidentalmente a direcciones de clientes reales cuando se encuentre en un entorno de prueba. Obtenga información sobre cómo [habilitar la lista de permitidos](../../configuration/allow-list.md).
   Obtenga más información acerca de la administración de capacidad de entrega de[!DNL Adobe Journey Optimizer] [en esta página](../../reports/deliverability.md).
