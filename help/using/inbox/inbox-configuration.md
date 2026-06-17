---
title: Configuración de bandeja de entrada
description: Configuración de canal de bandeja de entrada
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: d308ab4a-843c-4729-ad18-97d89c708357
source-git-commit: c2bb6cf702a14b4eef8f2209082e39cd73338378
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 3%

---

# Configurar bandeja de entrada {#inbox-configuration}

>[!BEGINSHADEBOX]

**En esta página:** defina una configuración de canal de bandeja de entrada que establezca el consentimiento, etiquetas de acceso opcionales y donde la bandeja de entrada aparezca en la web o en su aplicación de iOS o Android, de modo que pueda enviar experiencias de tarjeta de contenido a través de la bandeja de entrada.

>[!ENDSHADEBOX]

Para poder entregar experiencias de tarjeta de contenido a través de la Bandeja de entrada, debe definir una configuración de canal **Bandeja de entrada** en **[!UICONTROL Configuraciones de canal]**. Esa configuración vincula la superficie con el consentimiento, las etiquetas de acceso opcionales y dónde aparece la experiencia en la web o en la aplicación de iOS o Android. Siga los pasos a continuación para crear una configuración:

1. Acceda al menú **[!UICONTROL Canales]** > **[!UICONTROL Configuración general]** > **[!UICONTROL Configuraciones de canal]** y luego haga clic en **[!UICONTROL Crear configuración de canal]**.

   ![](assets/inbox-configuration-1.png)

1. Introduzca un nombre y una descripción (opcional) para la configuración.

   >[!NOTE]
   >
   > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos. También puede utilizar caracteres de guion bajo `_`, punto `.` y guion `-`.

1. Para asignar etiquetas de uso de datos principales o personalizadas a la configuración, puedes seleccionar **[!UICONTROL Administrar acceso]**. [Obtenga más información acerca del Control de acceso de nivel de objeto (OLAC)](../administration/object-based-access.md).

1. Seleccione el canal **[!UICONTROL Bandeja de entrada]**.

   ![](assets/inbox-configuration-2.png)

1. Seleccione **[!UICONTROL Acciones de marketing]** para asociar directivas de consentimiento a los mensajes que usan esta configuración. Todas las políticas de consentimiento asociadas con la acción de marketing se aprovechan para respetar las preferencias de los clientes. [Más información](../action/consent.md#surface-marketing-actions)

1. Seleccione la plataforma para la que se aplicará la experiencia Bandeja de entrada.

   ![](assets/inbox-configuration-3.png)

1. Para la web:

   * En **[!UICONTROL Dirección URL de la página]**, escriba o seleccione la dirección URL de la página donde debería aparecer la bandeja de entrada. Utilícelo cuando la experiencia esté limitada a una página.

   * En **[!UICONTROL Ubicación en la página]**, defina la ubicación en la página como, por ejemplo, la región o el identificador que el sitio utiliza para la superficie de la bandeja de entrada. [Más información](../web/web-configuration.md)

     ![](assets/inbox-configuration-4.png)

1. Para iOS y Android:

   * En **[!UICONTROL ID de aplicación]**, escriba o seleccione el identificador de su aplicación para que la configuración se aplique a la compilación correcta de iOS o Android.

   * En **[!UICONTROL Ubicación o ruta de acceso dentro de la aplicación]**, especifique la pantalla, la ruta o el contenedor donde los usuarios deben abrir la bandeja de entrada.

1. Envíe los cambios.

Ahora puede seleccionar la configuración al crear la experiencia de la bandeja de entrada.

➡️ [Siga los pasos detallados en esta página](inbox-create.md)
