---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del canal LINE
description: Aprenda a configurar su entorno para enviar mensajes de LINE con Journey Optimizer
feature: Line, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 8714ac6b2fd76ec859c358535fa322f0ac333a82
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 4%

---

# Configuración del canal LINE en Journey Optimizer {#line-configuration}

1. Acceda al menú **[!UICONTROL Canales]** > **[!UICONTROL Configuración general]** > **[!UICONTROL Configuraciones de canal]** y luego haga clic en **[!UICONTROL Crear configuración de canal]**.

   ![](assets/line-config-1.png)

1. Introduzca un nombre y una descripción (opcional) para la configuración y, a continuación, seleccione el canal que desea configurar.

   >[!NOTE]
   >
   > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos. También puede utilizar caracteres de guion bajo `_`, punto `.` y guion `-`.

1. Para asignar etiquetas de uso de datos principales o personalizadas a la configuración, puedes seleccionar **[!UICONTROL Administrar acceso]**. [Más información sobre el Control de acceso de nivel de objeto (OLAC)](../administration/object-based-access.md).

1. Seleccione el canal **LINE**.

   ![](assets/line-config-2.png)

1. Seleccione **[!UICONTROL Acciones de marketing]** para asociar directivas de consentimiento a los mensajes que usan esta configuración. Todas las políticas de consentimiento asociadas con la acción de marketing se aprovechan para respetar las preferencias de los clientes. [Más información](../action/consent.md#surface-marketing-actions)

1. Seleccione el tipo de mensaje para la configuración:

   * **Marketing**: Para mensajes promocionales, como promociones semanales de una tienda minorista. Estos mensajes requieren el consentimiento del usuario y deben cumplir con la política de LINE con respecto a las inclusiones de usuarios.
   * **Transaccional**: para mensajes no comerciales, como confirmaciones de pedidos, notificaciones de restablecimiento de contraseña o actualizaciones de envíos. Estos mensajes se pueden enviar incluso a usuarios que han cancelado la suscripción a comunicaciones de marketing, pero están estrictamente limitados a contextos transaccionales específicos.

1. Seleccione su **[!UICONTROL configuración de canal]**.

   Póngase en contacto con su representante de Adobe para configurar su **[!UICONTROL configuración de canal]**.

   ![](assets/line-config-2.png)

1. Seleccione el **[!UICONTROL ID de usuario de LINE]** que desee asignar. Este es el identificador utilizado para vincular mensajes a usuarios individuales dentro del canal LINE.

1. Escriba su **[!UICONTROL nombre de remitente]**, como el nombre de su marca.

1. Envíe los cambios.

Ahora puede seleccionar la configuración al crear el mensaje de LINE.
