---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de SMS
description: Aprenda a configurar la configuración de SMS/RCS/MMS para enviar mensajes móviles con Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
TQID: https://experienceleague.adobe.com/J5h64ccVVJUTCIk7FMMolKfEZy6rjEn-jwj1dEntnRM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: cf64c7f6-7428-4ae5-b158-8df9771f38f4id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0201927f8d9260e8ba1d0db7014d6a7b30d09062
workflow-type: tm+mt
source-wordcount: 522
ht-degree: 5%

---

# Creación de una configuración de mensaje de Mobile {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Definir la categoría de mensaje"
>abstract="Seleccione el tipo de mensajes móviles con esta configuración: Marketing para mensajes promocionales, que requieren el consentimiento del usuario, o Transaccional para mensajes no comerciales, como el restablecimiento de la contraseña."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=es#sms-opt-out-management" text="Exclusión en la comercialización de mensajes móviles"

Una vez configurado el canal de mensajes móviles, debe crear una configuración de canal para poder enviar mensajes SMS, RCS y MMS desde **[!DNL Journey Optimizer]**.

Para crear una configuración de canal, siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** y seleccione **[!UICONTROL Configuración general]** > **[!UICONTROL Configuraciones de canal]**. Haga clic en el botón **[!UICONTROL Crear configuración de canal]**.

   ![](assets/preset-create.png)

1. Introduzca un nombre y una descripción (opcional) para la configuración y, a continuación, seleccione el canal móvil.

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos. También puede utilizar caracteres de guion bajo `_`, punto `.` y guion `-`.

1. Seleccione el **[!UICONTROL tipo de SMS]** para esta configuración:

   * **[!UICONTROL Marketing]**: para mensajes promocionales que requieren el consentimiento del usuario.
   * **[!UICONTROL Transaccional]**: para mensajes no comerciales como confirmaciones de pedidos, restablecimientos de contraseñas o actualizaciones de envíos.

   >[!CAUTION]
   >
   >**Los mensajes transaccionales** se pueden enviar a perfiles que cancelaron la suscripción a comunicaciones de marketing, pero solo en contextos específicos.

   ![](assets/sms-surface-settings.png){width=80%}

1. Seleccione la **[!UICONTROL configuración móvil]** que desea asociar con la configuración.

   Para obtener más información sobre cómo configurar su entorno para que envíe mensajes de dispositivos móviles, consulte [esta sección](#create-api).

1. Escriba el **[!UICONTROL número de remitente]** &#x200B;que desee usar para sus comunicaciones.

1. Si desea utilizar la función de acortamiento de URL en los mensajes de Mobile, seleccione un elemento de la lista **[!UICONTROL Subdominio]**.

   >[!NOTE]
   >
   >Para poder seleccionar un subdominio, asegúrese de que ha configurado previamente al menos un subdominio SMS/RCS/MMS. [Descubra cómo](mobile-subdomains.md)

1. En la sección **[!UICONTROL Execution dimension]**, use el **[!UICONTROL Campo de ejecución de SMS]** para seleccionar entre los atributos de perfil el número de teléfono que desea usar en la prioridad si hay varios números disponibles en la base de datos. [Más información](../configuration/primary-email-addresses.md#override-execution-address-channel-config)

   >[!NOTE]
   >
   >De manera predeterminada, [!DNL Journey Optimizer] usa el número de teléfono especificado en [configuración general](../configuration/primary-email-addresses.md) en el nivel de espacio aislado. Al actualizar este campo, se anula el valor predeterminado de los recorridos y campañas que utilizan esta configuración.

1. Seleccione **[!UICONTROL Usar conjunto de datos personalizado para entrante]** para enrutar el SMS entrante de esta credencial a un conjunto de datos creado previamente que elija en el menú desplegable. [Más información acerca del uso de un conjunto de datos personalizado para palabras clave entrantes](custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >El esquema del conjunto de datos debe ser **[!UICONTROL XDM ExperienceEvent]** e incluir al menos estos grupos de campos:
   >* Adobe CJM ExperienceEvent: Detalles de interacción del mensaje
   >* Adobe CJM ExperienceEvent: Detalles de ejecución de mensajes
   >* Adobe CJM ExperienceEvent: Detalles del perfil de mensaje
   >
   >El esquema y el conjunto de datos deben estar habilitados para el perfil.

1. Una vez configurados todos los parámetros, haga clic en **[!UICONTROL Enviar]** para confirmar. También puede guardar la configuración de canal como borrador y reanudarla más adelante.

   ![](assets/sms-submit-surface.png)

1. Una vez creada la configuración del canal, se muestra en la lista con el estado **[!UICONTROL Procesando]**.

   >[!NOTE]
   >
   >Si las comprobaciones no se realizan correctamente, obtenga más información sobre los posibles motivos de error en [esta sección](../configuration/channel-surfaces.md).

1. Una vez que las comprobaciones son correctas, la configuración del canal obtiene el estado **[!UICONTROL Activo]**. Está listo para utilizarse para enviar mensajes.

   ![](assets/preset-active.png)

Ya está listo para enviar mensajes de Mobile con Journey Optimizer.
